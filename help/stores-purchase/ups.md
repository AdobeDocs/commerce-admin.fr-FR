---
title: United Parcel Service (UPS)
description: Découvrez comment configurer UPS en tant qu’opérateur de livraison pour votre magasin.
exl-id: a7965b2f-2473-4b63-a247-3b2230cde5d8
feature: Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# United Parcel Service (UPS)

United Parcel Service (UPS) offre des services de navigation intérieure et internationale par voie terrestre et aérienne à plus de 220 pays.

{{ups-api}}

>[!NOTE]
>
>UPS peut utiliser le [poids dimensionnel](carriers.md#dimensional-weight) pour déterminer certains tarifs de livraison. Cependant, Adobe Commerce ne prend en charge que le calcul des coûts d’expédition en fonction du poids.

## Étape 1 : ouverture d’un compte d’expédition UPS

Pour proposer cette méthode d&#39;expédition à vos clients, vous devez d&#39;abord ouvrir un compte auprès d&#39;UPS.

## Étape 2 : activation d’UPS pour votre magasin

1. Sur la _barre latérale d’administration_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, sous **[!UICONTROL Sales]**, choisissez **[!UICONTROL Delivery Methods]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL UPS]** .

1. Définissez **[!UICONTROL Enabled for Checkout]** sur `Yes`.

1. Pour un compte REST UPS (par défaut), procédez comme suit :

   - Saisissez vos informations d’identification UPS : UPS ClientID **[!UICONTROL User ID]**, UPS Client Secret **[!UICONTROL Password]**.

   - Définissez **[!UICONTROL Mode]** sur `Live` pour envoyer des données au système d’expédition UPS via une connexion sécurisée. (Le mode de développement n’envoie pas de données via une connexion sécurisée.)

   - Vérifiez les **[!UICONTROL Gateway URL]** requis pour envoyer des requêtes. Utilisez une URL d’environnement de test pour le mode test et une URL de production pour les requêtes en direct.

   - Vérifiez les **[!UICONTROL Tracking URL]** nécessaires pour obtenir les informations de suivi. Utilisez une URL d’environnement de test pour le mode test et une URL de production pour les requêtes en direct.

   - Définissez **[!UICONTROL Origin of the Shipment]** sur la région d’origine de l’envoi.

   - Si vous avez des taux spéciaux avec UPS, définissez **[!UICONTROL Enable Negotiated Rates]** sur `Yes` et saisissez les **[!UICONTROL Shipper Number]** à six chiffres qui vous ont été attribués par UPS.

   - Définissez **[!UICONTROL Live Account]** sur l’une des options suivantes :

      - `Yes` : exécute UPS en mode de production et offre UPS comme méthode d’expédition à vos clients.
      - `No` : exécute UPS en mode test.

   >[!NOTE]
   >
   >Le type de service United Parcel standard est programmé pour l’obsolescence. Pour les nouvelles configurations, utilisez le type `United Parcel Service REST` par défaut. Le type REST est également nécessaire pour générer les [libellés d&#39;expédition](shipping-labels.md).<br/>
   >Pour la version 2.4.7, **[!UICONTROL UPS Type]** est supprimé car les types `UPS` et `UPS XML` sont programmés pour l’obsolescence et `UPS REST` est la valeur par défaut. Les API UPS (United Parcel Service) utilisées par l’intégration native d’Adobe Commerce sont temporairement obsolètes, car elles ne prennent actuellement pas en charge le modèle de sécurité OAuth 2.0.

   >[!IMPORTANT]
   >
   >UPS interrompt la prise en charge du protocole HTTP, qui est utilisé dans la valeur par défaut actuelle (valeur système). Décochez la case **[!UICONTROL Use system value]** et modifiez l’URL pour utiliser HTTPS. Exemple : `https://www.ups.com/using/services/rave/qcostcgi.cgi`

1. Pour **[!UICONTROL Title]**, saisissez le nom de cette option d’expédition tel que vous souhaitez le voir apparaître lors du passage en caisse.

   Par défaut, ce champ est défini sur `United Parcel Service`.

   ![Activer UPS](../configuration-reference/sales/assets/delivery-methods-ups1.png){width="600" zoomable="yes"}

## Étape 3 : compléter la description du conteneur

1. Définissez **[!UICONTROL Packages Request Type]** sur l’une des options suivantes :

   - `Use origin weight (few requests)`
   - `Divide to equal weight (one request)`

1. Pour **[!UICONTROL Container]**, indiquez le type de package type utilisé pour l’expédition :

   - `Customer Packaging`
   - `UPS Letter Envelope`
   - `Customer Supplied Package`
   - `UPS Tube`
   - `PAK`
   - `UPS Express Box`
   - `UPS Worldwide 25 kilo`
   - `UPS Worldwide 10 kilo`
   - `Pallet`
   - `Small Express Box`
   - `Medium Express Box`
   - `Large Express Box`

1. Définissez **[!UICONTROL Weight Unit]** sur le système que vous utilisez pour mesurer le poids du produit.

   Le système de poids pris en charge par UPS varie selon les pays. En cas de doute, demandez à UPS quel système de poids vous devriez utiliser. Les options incluent :

   - `LBS`
   - `KGS`

1. Définissez **[!UICONTROL Destination Type]** sur l’une des options suivantes :

   - `Residential` - La plupart de vos envois sont destinés au consommateur (B2C).
   - `Commercial` - La plupart de vos envois sont des affaires à l’entreprise (B2B).

1. Saisissez le **[!UICONTROL Maximum Package Weight]** autorisé par l’opérateur.

1. Définissez **[!UICONTROL Pickup Method]** sur l’une des options suivantes :

   - `Regular Daily Pickup`
   - `On Call Air`
   - `One Time Pickup`
   - `Letter Center`
   - `Customer Counter`

1. Saisissez le **[!UICONTROL Minimum Package Weight]** autorisé par l’opérateur.

   ![Description du conteneur](./assets/ups2.png){width="600" zoomable="yes"}

## Étape 4 : configuration des frais de gestion

Les frais de gestion sont facultatifs et s’affichent sous la forme de frais supplémentaires, ajoutés aux frais d’expédition UPS. Si vous souhaitez inclure des frais de traitement, procédez comme suit :

1. Définissez **[!UICONTROL Calculate Handling Fee]** sur l’une des méthodes suivantes :

   - `Fixed`
   - `Percent`

1. Pour déterminer comment les frais de gestion sont appliqués, définissez **[!UICONTROL Handling Applied]** sur l’une des options suivantes :

   - `Per Order`
   - `Per Package`

1. Saisissez le montant de **[!UICONTROL Handling Fee]** à charger.

   Pour saisir un pourcentage, utilisez le format décimal . Par exemple, saisissez `0.25` pour 25 %.

   ![Frais de gestion](./assets/ups3.png){width="600" zoomable="yes"}

## Étape 5 : spécification des méthodes autorisées et des pays applicables

1. Pour **[!UICONTROL Allowed Methods]**, choisissez chaque méthode d’expédition UPS à la disposition de vos clients.

   Les méthodes apparaissent sous UPS lors du passage en caisse. Pour sélectionner plusieurs méthodes, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

1. Si vous souhaitez fournir une option de [livraison gratuite](shipping-free.md) via UPS, définissez les options de livraison gratuite :

   - Définissez **[!UICONTROL Free Method]** sur la méthode que vous souhaitez utiliser pour la livraison gratuite. Si vous ne souhaitez pas proposer la livraison gratuite par UPS, choisissez `None`.

   - Pour exiger un montant minimum de commande qui qualifie une commande de livraison gratuite avec UPS, définissez **[!UICONTROL Enable Free Shipping Threshold]** sur `Enable`. Ensuite, saisissez la valeur minimale dans **[!UICONTROL Free Shipping Amount Threshold]**.

1. Si nécessaire, modifiez le **[!UICONTROL Displayed Error Message]**.

   Cette zone de texte est prédéfinie avec un message par défaut, mais vous pouvez saisir un autre message que vous souhaitez afficher si UPS devient indisponible.

   ![Méthodes autorisées](./assets/ups4.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Ship to Applicable Countries]** sur l’une des options suivantes :

   - `All Allowed Countries` - Les clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiés dans votre configuration de magasin peuvent utiliser cette méthode de diffusion.
   - `Specific Countries` - Lorsque vous sélectionnez cette option, la liste _Ship to Specific Countries_ s’affiche. Sélectionnez chaque pays de la liste dans lequel ce mode de diffusion peut être utilisé.

1. Définissez **[!UICONTROL Show Method if Not Applicable]** sur l’une des options suivantes :

   - `Yes` - Répertorie toutes les méthodes d’expédition UPS disponibles lors du passage en caisse, y compris les méthodes qui ne s’appliquent pas à l’expédition.
   - `No` - Répertorie uniquement les méthodes d’expédition UPS applicables à l’expédition.

   ![Pays applicables](./assets/ups5.png){width="600" zoomable="yes"}

1. Pour créer un fichier journal contenant les détails des envois UPS effectués à partir de votre magasin, définissez **[!UICONTROL Debug]** sur `Yes`.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer la séquence dans laquelle UPS apparaît lorsqu&#39;il est répertorié avec d&#39;autres méthodes de diffusion lors du passage en caisse.

   `0` = premier, `1` = second, `2` = troisième, etc.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Étape 6 : configuration de l’adresse d’origine de la livraison

1. Assurez-vous que vos [informations de magasin](../getting-started/store-details.md#store-information) sont terminées.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et sélectionnez **[!UICONTROL Shipping Settings]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Origin]** sur la page et configurez l’adresse d’origine de l’expédition.

   ![Configuration des ventes - options d’adresse d’origine de livraison](./assets/shipping-origin.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Commerce ne déclare pas le prix complet de la commande à UPS lors du calcul des frais de livraison. Ce comportement ne peut pas être modifié.
