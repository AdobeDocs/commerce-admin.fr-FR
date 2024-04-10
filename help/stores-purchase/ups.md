---
title: United Parcel Service (UPS)
description: Découvrez comment configurer UPS en tant que transporteur pour votre boutique.
exl-id: a7965b2f-2473-4b63-a247-3b2230cde5d8
feature: Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# United Parcel Service (UPS)

United Parcel Service (UPS) offre des services de transport maritime national et international par voie terrestre et aérienne à plus de 220 pays.

{{ups-api}}

>[!NOTE]
>
>UPS peut utiliser [poids dimensionnel](carriers.md#dimensional-weight) pour déterminer certains frais d’expédition. Cependant, Adobe Commerce ne prend en charge que le calcul des frais de livraison en fonction du poids.

## Étape 1 : Ouvrir un compte d&#39;expédition UPS

Pour proposer cette méthode d&#39;expédition à vos clients, vous devez d&#39;abord ouvrir un compte avec UPS.

## Étape 2 : Activer l&#39;onduleur pour votre magasin

1. Le _Barre latérale d’administration_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, sous **[!UICONTROL Sales]**, choisissez **[!UICONTROL Delivery Methods]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) le **[!UICONTROL UPS]** section.

1. Définir **[!UICONTROL Enabled for Checkout]** vers `Yes`.

1. Pour un compte REST UPS (par défaut), procédez comme suit :

   - Entrez vos informations d&#39;identification UPS : UPS ClientID comme **[!UICONTROL User ID]**, secret client UPS en tant que **[!UICONTROL Password]**

   - Définir **[!UICONTROL Mode]** vers `Live` pour envoyer des données au système d&#39;expédition UPS via une connexion sécurisée. (Le mode de développement n’envoie pas de données via une connexion sécurisée.)

   - Vérifier le **[!UICONTROL Gateway URL]** qui est nécessaire pour envoyer des requêtes. Utilisez une URL de sandbox pour le mode test et une URL de production pour les requêtes dynamiques.

   - Vérifier le **[!UICONTROL Tracking URL]** qui est nécessaire pour obtenir des informations de suivi. Utilisez une URL de sandbox pour le mode test et une URL de production pour les requêtes dynamiques.

   - Définir **[!UICONTROL Origin of the Shipment]** vers la région d&#39;origine de l&#39;expédition.

   - Si vous bénéficiez de tarifs spéciaux avec UPS, définissez **[!UICONTROL Enable Negotiated Rates]** vers `Yes` et saisissez les six chiffres **[!UICONTROL Shipper Number]** affecté(e)(s) par UPS.

   - Définir **[!UICONTROL Live Account]** à l’un des éléments suivants :

      - `Yes` - Exécute l&#39;onduleur en mode production et propose l&#39;onduleur comme mode d&#39;expédition à vos clients.
      - `No` : exécute l’onduleur en mode test.

   >[!NOTE]
   >
   >L&#39;abandon du type standard United Parcel Service est programmé. Pour les nouvelles configurations, utilisez la valeur par défaut `United Parcel Service REST` tapez . Le type REST est également requis pour la génération [étiquettes d&#39;expédition](shipping-labels.md).<br/>
   >Pour la version 2.4.7, **[!UICONTROL UPS Type]**  est supprimé parce que `UPS` et `UPS XML` l’obsolescence des types est planifiée. `UPS REST` est la valeur par défaut. Les API United Parcel Service (UPS) utilisées par l’intégration native d’Adobe Commerce sont temporairement obsolètes, car elles ne prennent actuellement pas en charge le modèle de sécurité OAuth 2.0.

   >[!IMPORTANT]
   >
   >L’onduleur cesse la prise en charge du protocole HTTP, qui est utilisé par défaut (valeur système). Effacer le **[!UICONTROL Use system value]** et modifiez l’URL pour utiliser HTTPS. Exemple : `https://www.ups.com/using/services/rave/qcostcgi.cgi`

1. Pour **[!UICONTROL Title]**, saisissez le nom de cette option d’expédition telle que vous souhaitez qu’elle apparaisse lors du passage en caisse.

   Par défaut, ce champ est défini sur `United Parcel Service`.

   ![Activer UPS](../configuration-reference/sales/assets/delivery-methods-ups1.png){width="600" zoomable="yes"}

## Étape 3 : remplir la description du conteneur

1. Définir **[!UICONTROL Packages Request Type]** à l’un des éléments suivants :

   - `Use origin weight (few requests)`
   - `Divide to equal weight (one request)`

1. Pour **[!UICONTROL Container]**, spécifiez le type d’emballage type utilisé pour l’expédition :

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

1. Définir **[!UICONTROL Weight Unit]** au système utilisé pour mesurer le poids du produit.

   Le système de poids pris en charge par UPS varie selon les pays. En cas de doute, demandez à UPS quel système de poids vous devez utiliser. Les options incluent :

   - `LBS`
   - `KGS`

1. Définir **[!UICONTROL Destination Type]** à l’un des éléments suivants :

   - `Residential` - La plupart de vos envois sont d&#39;entreprise à consommateur (B2C).
   - `Commercial` - La plupart de vos envois sont interentreprises (B2B).

1. Saisir le **[!UICONTROL Maximum Package Weight]** autorisé par le transporteur.

1. Définir **[!UICONTROL Pickup Method]** à l’un des éléments suivants :

   - `Regular Daily Pickup`
   - `On Call Air`
   - `One Time Pickup`
   - `Letter Center`
   - `Customer Counter`

1. Saisir le **[!UICONTROL Minimum Package Weight]** autorisé par le transporteur.

   ![Description du conteneur](./assets/ups2.png){width="600" zoomable="yes"}

## Étape 4 : configurer les frais de gestion

Les frais de manutention sont facultatifs et s&#39;affichent sous forme de frais supplémentaires qui s&#39;ajoutent aux frais d&#39;expédition de l&#39;onduleur. Si vous souhaitez inclure des frais de manutention, procédez comme suit :

1. Définir **[!UICONTROL Calculate Handling Fee]** selon l’une des méthodes suivantes :

   - `Fixed`
   - `Percent`

1. Pour déterminer comment les frais de gestion sont appliqués, définissez **[!UICONTROL Handling Applied]** à l’un des éléments suivants :

   - `Per Order`
   - `Per Package`

1. Saisir le montant de **[!UICONTROL Handling Fee]** à facturer.

   Pour saisir un pourcentage, utilisez le format décimal. Par exemple, saisissez . `0.25` pour 25 %.

   ![Frais de gestion](./assets/ups3.png){width="600" zoomable="yes"}

## Étape 5 : spécifier les méthodes autorisées et les pays applicables

1. Pour **[!UICONTROL Allowed Methods]**, choisissez chaque mode d&#39;expédition UPS disponible pour vos clients.

   Les méthodes s’affichent sous UPS lors du passage en caisse. Pour sélectionner plusieurs méthodes, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et cliquez sur chaque option.

1. Si vous souhaitez fournir un [Livraison gratuite](shipping-free.md) via UPS, définissez les options de livraison gratuite :

   - Définir **[!UICONTROL Free Method]** à la méthode que vous souhaitez utiliser pour la livraison gratuite. Si vous ne souhaitez pas offrir la livraison gratuite via UPS, choisissez `None`.

   - Pour exiger un montant de commande minimum qui qualifie une commande pour une livraison gratuite avec UPS, définissez **[!UICONTROL Enable Free Shipping Threshold]** vers `Enable`. Saisissez ensuite la valeur minimale en . **[!UICONTROL Free Shipping Amount Threshold]**.

1. Si nécessaire, modifiez le **[!UICONTROL Displayed Error Message]**.

   Cette zone de texte est prédéfinie avec un message par défaut, mais vous pouvez saisir un message différent que vous souhaitez afficher si l&#39;onduleur n&#39;est plus disponible.

   ![Méthodes autorisées](./assets/ups4.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Ship to Applicable Countries]** à l’un des éléments suivants :

   - `All Allowed Countries` - Clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiée dans la configuration de votre boutique peut utiliser cette méthode de diffusion.
   - `Specific Countries` - Lorsque vous choisissez cette option, le _Expédition vers des pays spécifiques_ La liste s’affiche. Sélectionnez dans la liste les pays où cette méthode de diffusion peut être utilisée.

1. Définir **[!UICONTROL Show Method if Not Applicable]** à l’un des éléments suivants :

   - `Yes` - Répertorie tous les modes d&#39;expédition UPS disponibles lors du passage en caisse, y compris les modes qui ne s&#39;appliquent pas à l&#39;expédition.
   - `No` - Répertorie uniquement les méthodes d&#39;expédition UPS applicables à l&#39;expédition.

   ![Pays applicables](./assets/ups5.png){width="600" zoomable="yes"}

1. Pour créer un fichier journal contenant les détails des expéditions UPS effectuées à partir de votre magasin, définissez **[!UICONTROL Debug]** vers `Yes`.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre pour déterminer l’ordre dans lequel l’onduleur apparaît lorsqu’il est répertorié avec d’autres méthodes de diffusion lors du passage en caisse.

   `0` = first, `1` = seconde, `2` = troisième, etc.

1. Clic **[!UICONTROL Save Config]**.

## Étape 6 : configurer l&#39;adresse d&#39;origine d&#39;expédition

1. Assurez-vous que vos [Informations sur la boutique](../getting-started/store-details.md#store-information) est terminé.

1. Le _Admin_ barre latérale, accéder à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et sélectionnez **[!UICONTROL Shipping Settings]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Origin]** sur la page et configurez l’adresse d’origine d’expédition.

   ![Configuration des ventes - options d’adresse d’origine d’expédition](./assets/shipping-origin.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Lors du calcul des frais d&#39;expédition, Commerce ne déclare pas le prix de la commande complète à UPS. Ce comportement ne peut pas être modifié.
