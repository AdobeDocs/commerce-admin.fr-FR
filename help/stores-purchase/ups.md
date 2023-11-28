---
title: United Parcel Service (UPS)
description: Découvrez comment configurer UPS en tant qu’opérateur de livraison pour votre magasin.
exl-id: a7965b2f-2473-4b63-a247-3b2230cde5d8
feature: Shipping/Delivery
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 0%

---

# United Parcel Service (UPS)

United Parcel Service (UPS) offre des services de navigation intérieure et internationale par voie terrestre et aérienne à plus de 220 pays.

{{ups-api}}

>[!NOTE]
>
>UPS peut utiliser [poids dimensionnel](carriers.md#dimensional-weight) pour déterminer certains tarifs d’expédition. Cependant, Adobe Commerce ne prend en charge que le calcul des coûts d’expédition en fonction du poids.

## Étape 1 : ouverture d’un compte d’expédition UPS

Pour proposer cette méthode d&#39;expédition à vos clients, vous devez d&#39;abord ouvrir un compte auprès d&#39;UPS.

## Étape 2 : activation d’UPS pour votre magasin

{{beta2-updates}}

1. Sur le _Barre latérale d’administration_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, sous **[!UICONTROL Sales]**, choisissez **[!UICONTROL Delivery Methods]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL UPS]** .

1. Définir **[!UICONTROL Enabled for Checkout]** to `Yes`.

1. Pour un compte XML UPS (par défaut), définissez **[!UICONTROL UPS Type]** to `United Parcel Service XML` et procédez comme suit :

   - Saisissez vos informations d’identification UPS : **[!UICONTROL User ID]**, **[!UICONTROL Access License Number]** (compte UPS à 16 chiffres `Access Key`), et **[!UICONTROL Password]**

   - Définir **[!UICONTROL Mode]** to `Live` pour envoyer des données au système d’expédition UPS par le biais d’une connexion sécurisée. (Le mode de développement n’envoie pas de données via une connexion sécurisée.)

   - Vérifiez les **[!UICONTROL Gateway XML URL]** qui est requis pour envoyer des requêtes par fichier XML.

   - Définir **[!UICONTROL Origin of the Shipment]** à la région d&#39;origine de l&#39;expédition.

   - Si vous avez des taux spéciaux avec UPS, définissez **[!UICONTROL Enable Negotiated Rates]** to `Yes` et saisissez le **[!UICONTROL Shipper Number]** qui vous a été attribué par UPS.

1. Pour un compte UPS standard, définissez **[!UICONTROL UPS Type]** to `United Parcel Service` et procédez comme suit :

   >[!NOTE]
   >
   >Le type de service United Parcel standard est programmé pour l’obsolescence. Pour les nouvelles configurations, vous devez utiliser la valeur par défaut  `United Parcel Service XML` type. Le type XML est également nécessaire pour générer [libellé d’expédition](shipping-labels.md).

   - Définir **[!UICONTROL Live Account]** à l’une des options suivantes :

      - `Yes` : exécute UPS en mode de production et offre UPS comme méthode d’expédition à vos clients.
      - `No` : exécute UPS en mode test.

   - Dans le **[!UICONTROL Gateway URL]** , saisissez l&#39;URL utilisée pour calculer les tarifs d&#39;expédition UPS.

     >[!IMPORTANT]
     >
     >UPS interrompt la prise en charge du protocole HTTP, qui est utilisé dans la valeur par défaut actuelle (valeur système). Effacez la variable **[!UICONTROL Use system value]** et modifiez l’URL pour utiliser HTTPS. Exemple : `https://www.ups.com/using/services/rave/qcostcgi.cgi`

1. Pour **[!UICONTROL Title]**, saisissez le nom de cette option d’expédition tel que vous souhaitez le voir apparaître lors du passage en caisse.

   Par défaut, ce champ est défini sur `United Parcel Service`.

   ![Activer UPS](../configuration-reference/sales/assets/delivery-methods-ups1.png){width="600" zoomable="yes"}

## Étape 3 : compléter la description du conteneur

1. Définir **[!UICONTROL Packages Request Type]** à l’une des options suivantes :

   - `Use origin weight (few requests)`
   - `Divide to equal weight (one request)`

1. Pour **[!UICONTROL Container]**, indiquez le type de conditionnement type utilisé pour l’expédition :

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

1. Définir **[!UICONTROL Weight Unit]** au système de mesure du poids du produit.

   Le système de poids pris en charge par UPS varie selon les pays. En cas de doute, demandez à UPS quel système de poids vous devriez utiliser. Les options incluent :

   - `LBS`
   - `KGS`

1. Définir **[!UICONTROL Destination Type]** à l’une des options suivantes :

   - `Residential` - La plupart de vos envois sont destinés au consommateur (B2C).
   - `Commercial` - La plupart de vos envois sont des affaires vers des entreprises (B2B).

1. Saisissez le **[!UICONTROL Maximum Package Weight]** autorisé par l’opérateur.

1. Définir **[!UICONTROL Pickup Method]** à l’une des options suivantes :

   - `Regular Daily Pickup`
   - `On Call Air`
   - `One Time Pickup`
   - `Letter Center`
   - `Customer Counter`

1. Saisissez le **[!UICONTROL Minimum Package Weight]** autorisé par l’opérateur.

   ![Description du conteneur](./assets/ups2.png){width="600" zoomable="yes"}

## Étape 4 : configuration des frais de gestion

Les frais de gestion sont facultatifs et s’affichent sous la forme de frais supplémentaires, ajoutés aux frais d’expédition UPS. Si vous souhaitez inclure des frais de traitement, procédez comme suit :

1. Définir **[!UICONTROL Calculate Handling Fee]** à l’une des méthodes suivantes :

   - `Fixed`
   - `Percent`

1. Pour déterminer la manière dont les frais de traitement sont appliqués, définissez **[!UICONTROL Handling Applied]** à l’une des options suivantes :

   - `Per Order`
   - `Per Package`

1. Saisissez le montant de la variable **[!UICONTROL Handling Fee]** à charger.

   Pour saisir un pourcentage, utilisez le format décimal . Par exemple, saisissez `0.25` pour 25 %.

   ![Gestion des frais](./assets/ups3.png){width="600" zoomable="yes"}

## Étape 5 : spécification des méthodes autorisées et des pays applicables

1. Pour **[!UICONTROL Allowed Methods]**, choisissez chaque méthode d’expédition UPS à la disposition de vos clients.

   Les méthodes apparaissent sous UPS lors du passage en caisse. Pour sélectionner plusieurs méthodes, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

1. Si vous souhaitez fournir une [Livraison gratuite](shipping-free.md) via UPS, définissez les options d’expédition gratuites :

   - Définir **[!UICONTROL Free Method]** à la méthode que vous souhaitez utiliser pour la livraison gratuite. Si vous ne souhaitez pas proposer de livraison gratuite via UPS, choisissez `None`.

   - Pour exiger un montant minimum de commande qui qualifie une commande d’expédition gratuite avec UPS, définissez **[!UICONTROL Enable Free Shipping Threshold]** to `Enable`. Ensuite, saisissez la valeur minimale de **[!UICONTROL Free Shipping Amount Threshold]**.

1. Si nécessaire, modifiez la variable **[!UICONTROL Displayed Error Message]**.

   Cette zone de texte est prédéfinie avec un message par défaut, mais vous pouvez saisir un autre message que vous souhaitez afficher si UPS devient indisponible.

   ![Méthodes autorisées](./assets/ups4.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Ship to Applicable Countries]** à l’une des options suivantes :

   - `All Allowed Countries` - Clients de tous les [pays](../getting-started/store-details.md#country-options) spécifié dans votre configuration de magasin peut utiliser cette méthode de diffusion.
   - `Specific Countries` - Lorsque vous sélectionnez cette option, la variable _Ship to Specific Countries_ s’affiche. Sélectionnez chaque pays de la liste dans lequel ce mode de diffusion peut être utilisé.

1. Définir **[!UICONTROL Show Method if Not Applicable]** à l’une des options suivantes :

   - `Yes` - Répertorie toutes les méthodes d’expédition UPS disponibles lors du passage en caisse, y compris les méthodes qui ne s’appliquent pas à l’expédition.
   - `No` - Répertorie uniquement les méthodes d’expédition UPS applicables à l’expédition.

   ![Pays applicables](./assets/ups5.png){width="600" zoomable="yes"}

1. Pour créer un fichier journal contenant les détails des envois UPS effectués depuis votre magasin, définissez **[!UICONTROL Debug]** to `Yes`.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre dans lequel UPS apparaît lorsqu’il est répertorié avec d’autres méthodes de remise lors du passage en caisse.

   `0` = first, `1` = second, `2` = troisième, etc.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Étape 6 : configuration de l’adresse d’origine de la livraison

1. Assurez-vous que la variable [Informations sur le magasin](../getting-started/store-details.md#store-information) est terminée.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et sélectionnez **[!UICONTROL Shipping Settings]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Origin]** sur la page et configurez l’adresse d’origine de l’expédition.

   ![Configuration des ventes - Options d’adresse d’origine de livraison](./assets/shipping-origin.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Commerce ne déclare pas le prix de la commande complète à UPS lors du calcul des frais de livraison. Ce comportement ne peut pas être modifié.
