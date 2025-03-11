---
title: United Parcel Service (UPS)
description: Découvrez comment configurer UPS en tant que transporteur pour votre boutique.
exl-id: a7965b2f-2473-4b63-a247-3b2230cde5d8
feature: Shipping/Delivery
source-git-commit: 614a94856c114244c8fdb281c73650878849a2fb
workflow-type: tm+mt
source-wordcount: '1013'
ht-degree: 0%

---

# United Parcel Service (UPS)

United Parcel Service (UPS) offre des services d&#39;expédition nationaux et internationaux par voie terrestre et aérienne à plus de 220 pays.

{{ups-api}}

>[!NOTE]
>
>UPS peut utiliser [poids dimensionnel](carriers.md#dimensional-weight) pour déterminer certains tarifs d&#39;expédition. Cependant, Adobe Commerce ne prend en charge que le calcul des coûts d’expédition en fonction du poids.

## Étape 1 : Ouvrir un compte d&#39;expédition UPS

Pour proposer cette méthode d&#39;expédition à vos clients, vous devez d&#39;abord ouvrir un compte UPS et remplir la demande pour obtenir un numéro de compte Expéditeur. Voir [Ouvrir un compte UPS gratuit](https://www.ups.com/us/en/business-solutions/open-an-account).

## Étape 2 : obtenir des informations d’identification OAUTH UPS

Suivez les étapes du guide [Prise en main des API UPS](https://developer.ups.com/get-started) pour obtenir les informations d’identification d’API (identifiant client et secret client) afin d’activer l’intégration UPS. Vous devez créer une application UPS pour obtenir les informations d’identification.

Lorsque vous configurez les paramètres de l’onduleur dans l’administration, utilisez les valeurs d’identification des `username` et des `password`.

## Étape 3 : Activer l&#39;onduleur pour votre magasin

1. Dans la _barre latérale d’administration_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, sous **[!UICONTROL Sales]**, choisissez **[!UICONTROL Delivery Methods]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL UPS]** .

1. Définissez **[!UICONTROL Enabled for Checkout]** sur `Yes`.

1. Pour un compte REST UPS (par défaut), procédez comme suit :

   - Saisissez vos informations d&#39;identification UPS : UPS ClientID comme **[!UICONTROL User ID]**, UPS Client Secret comme **[!UICONTROL Password]**.

   - Définissez **[!UICONTROL Mode]** sur `Live` pour envoyer des données au système d&#39;expédition UPS via une connexion sécurisée. (Le mode de développement n’envoie pas de données via une connexion sécurisée.)

   - Vérifiez les **[!UICONTROL Gateway URL]** requises pour envoyer des requêtes. Utilisez une URL de sandbox (`https://wwwcie.ups.com/`) pour le mode test et une URL de production pour les requêtes en direct (`https://onlinetools.ups.com`). Veillez à utiliser les points d’entrée respectifs pour chaque requête avec l’hôte donné.

   - Vérifiez le **[!UICONTROL Tracking URL]** requis pour obtenir les informations de suivi. Utilisez une URL de sandbox (`https://wwwcie.ups.com/`) pour le mode test et une URL de production pour les requêtes en direct (`https://onlinetools.ups.com`). Veillez à utiliser les points d’entrée respectifs pour chaque requête avec l’hôte donné.

   - Définissez **[!UICONTROL Origin of the Shipment]** dans la région d&#39;origine de l&#39;expédition.

   - Si vous disposez de tarifs spéciaux avec UPS, définissez **[!UICONTROL Enable Negotiated Rates]** sur `Yes` et saisissez le **[!UICONTROL Shipper Number]** à six chiffres qui vous est attribué par UPS.

   - Définissez **[!UICONTROL Live Account]** sur l’une des options suivantes :

      - `Yes` : exécute l’onduleur en mode de production et le propose comme méthode d’expédition à vos clients. Assurez-vous d’utiliser les points d’entrée appropriés sous URL de passerelle et URL de suivi.
      - `No` : exécute l’UPS en mode test. Assurez-vous d’utiliser les points d’entrée appropriés sous URL de passerelle et URL de suivi.

   >[!NOTE]
   >
   >Le type de service United Parcel standard est planifié en vue de son abandon. Pour les nouvelles configurations, utilisez le type de `United Parcel Service REST` par défaut. Le type REST est également requis pour générer des [étiquettes d’expédition](shipping-labels.md).<br/>
   >Pour la version 2.4.7, **[!UICONTROL UPS Type]** est supprimé, car les types `UPS` et `UPS XML` sont planifiés en vue de leur obsolescence, et `UPS REST` est la valeur par défaut. Les API United Parcel Service (UPS) utilisées par l’intégration native d’Adobe Commerce sont temporairement obsolètes, car elles ne prennent actuellement pas en charge le modèle de sécurité OAuth 2.0.

   >[!IMPORTANT]
   >
   >L’onduleur cesse la prise en charge du protocole HTTP, qui est utilisé dans la valeur par défaut actuelle (valeur système). Décochez la case **[!UICONTROL Use system value]** et modifiez l’URL pour utiliser HTTPS. Exemple : `https://www.ups.com/using/services/rave/qcostcgi.cgi`

1. Par **[!UICONTROL Title]**, saisissez le nom de cette option d&#39;expédition telle que vous souhaitez qu&#39;elle apparaisse lors du passage en caisse.

   Par défaut, ce champ est défini sur `United Parcel Service`.

   ![Activer UPS](../configuration-reference/sales/assets/delivery-methods-ups1.png){width="600" zoomable="yes"}

## Étape 3 : remplir la description du conteneur

1. Définissez **[!UICONTROL Packages Request Type]** sur l’une des options suivantes :

   - `Use origin weight (few requests)`
   - `Divide to equal weight (one request)`

1. Par **[!UICONTROL Container]**, spécifiez le type d’emballage type utilisé pour l’expédition :

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

1. Définissez **[!UICONTROL Weight Unit]** sur le système utilisé pour mesurer le poids du produit.

   Le système de poids pris en charge par UPS varie selon les pays. En cas de doute, demandez à UPS quel système de poids vous devez utiliser. Les options incluent :

   - `LBS`
   - `KGS`

1. Définissez **[!UICONTROL Destination Type]** sur l’une des options suivantes :

   - `Residential` - La plupart de vos envois sont de type B2C (business to consumer).
   - `Commercial` - La plupart de vos envois sont interentreprises (B2B).

1. Saisissez le **[!UICONTROL Maximum Package Weight]** autorisé par le transporteur.

1. Définissez **[!UICONTROL Pickup Method]** sur l’une des options suivantes :

   - `Regular Daily Pickup`
   - `On Call Air`
   - `One Time Pickup`
   - `Letter Center`
   - `Customer Counter`

1. Saisissez le **[!UICONTROL Minimum Package Weight]** autorisé par le transporteur.

   ![Description du conteneur](./assets/ups2.png){width="600" zoomable="yes"}

## Étape 5 : configurer les frais de gestion

Les frais de manutention sont facultatifs et apparaissent comme des frais supplémentaires qui s&#39;ajoutent aux frais d&#39;expédition de l&#39;UPS. Si vous souhaitez inclure des frais de manutention, procédez comme suit :

1. Définissez **[!UICONTROL Calculate Handling Fee]** l’une des méthodes suivantes :

   - `Fixed`
   - `Percent`

1. Pour déterminer comment les frais de gestion sont appliqués, définissez **[!UICONTROL Handling Applied]** sur l’une des options suivantes :

   - `Per Order`
   - `Per Package`

1. Saisissez le montant de la **[!UICONTROL Handling Fee]** à facturer.

   Pour saisir un pourcentage, utilisez le format décimal. Par exemple, saisissez `0.25` pour 25 %.

   ![Frais de gestion](./assets/ups3.png){width="600" zoomable="yes"}

## Étape 6 : spécifier les méthodes autorisées et les pays applicables

1. Par **[!UICONTROL Allowed Methods]**, choisissez chaque méthode d&#39;expédition UPS disponible pour vos clients.

   Les méthodes s’affichent sous UPS lors du passage en caisse. Pour sélectionner plusieurs méthodes, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et cliquez sur chaque option.

1. Si vous souhaitez fournir une option [Livraison gratuite](shipping-free.md) via UPS, définissez les options de livraison gratuite :

   - Définissez **[!UICONTROL Free Method]** sur la méthode que vous souhaitez utiliser pour la livraison gratuite. Si vous ne voulez pas offrir la livraison gratuite par UPS, choisissez `None`.

   - Pour exiger un montant de commande minimum qui qualifie une commande pour une livraison gratuite avec UPS, définissez **[!UICONTROL Enable Free Shipping Threshold]** sur `Enable`. Saisissez ensuite la valeur minimale en **[!UICONTROL Free Shipping Amount Threshold]**.

1. Si nécessaire, modifiez la **[!UICONTROL Displayed Error Message]**.

   Cette zone de texte est prédéfinie avec un message par défaut, mais vous pouvez saisir un message différent que vous souhaitez afficher si l’onduleur n’est plus disponible.

   ![Méthodes autorisées](./assets/ups4.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Ship to Applicable Countries]** sur l’une des options suivantes :

   - `All Allowed Countries` - Les clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiés dans la configuration de votre boutique peuvent utiliser cette méthode de diffusion.
   - `Specific Countries` - Lorsque vous sélectionnez cette option, la liste _Livrer à des pays spécifiques_ s&#39;affiche. Sélectionnez dans la liste chaque pays où ce mode de diffusion peut être utilisé.

1. Définissez **[!UICONTROL Show Method if Not Applicable]** sur l’une des options suivantes :

   - `Yes` - Répertorie tous les modes d&#39;expédition UPS disponibles lors du passage en caisse, y compris les modes qui ne s&#39;appliquent pas à l&#39;expédition.
   - `No` - Répertorie uniquement les modes d&#39;expédition UPS applicables à l&#39;expédition.

   ![Pays applicables](./assets/ups5.png){width="600" zoomable="yes"}

1. Pour créer un fichier journal contenant les détails des expéditions UPS effectuées à partir de votre magasin, définissez **[!UICONTROL Debug]** sur `Yes`.

1. Par **[!UICONTROL Sort Order]**, saisissez un nombre pour déterminer l&#39;ordre dans lequel l&#39;onduleur apparaît lorsqu&#39;il est répertorié avec d&#39;autres méthodes de diffusion lors du passage en caisse.

   `0` = premier, `1` = deuxième, `2` = troisième, etc.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Étape 7 : Configurer l&#39;adresse d&#39;origine d&#39;expédition

1. Assurez-vous que les [Informations de la boutique](../getting-started/store-details.md#store-information) sont complètes.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et sélectionnez **[!UICONTROL Shipping Settings]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Origin]** sur la page et configurez l’adresse d’origine d’expédition.

   ![Configuration des ventes - Options d’adresse d’origine d’expédition](./assets/shipping-origin.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Commerce ne déclare pas le prix total de la commande à UPS lors du calcul des frais d&#39;expédition. Ce comportement ne peut pas être modifié.
