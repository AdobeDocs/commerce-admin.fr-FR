---
title: Configurer les retours
description: Découvrez comment activer les retours pour votre boutique et configurer les méthodes d’expédition prises en charge.
exl-id: a1b508fc-7e42-4d37-bf7e-dea17a40d39b
feature: Returns, Configuration
TQID: https://experienceleague.adobe.com/TgVsqEceM-mTY91OCl7XRL0Uwk8VJAHatv0kHiOM00g
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 353
ht-degree: 0%

---

# Configurer les retours

{{ee-feature}}

Lorsqu’elles sont activées, les requêtes RMA peuvent être envoyées par les clients à partir du storefront. Un retour client ne peut être généré que s&#39;il existe un article dans la commande pouvant être renvoyé. Les demandes de renvoi d’éléments individuels sont gérées par l’attribut _Activer RMA_ dans chaque enregistrement de produit. Par défaut, les paramètres de configuration sont appliqués au produit (_[!UICONTROL Use Config Settings]_est sélectionné). Si_[!UICONTROL Enable RMA]_ est défini sur `No`, le produit n’apparaît pas dans la liste des éléments pouvant être renvoyés. Si vous modifiez le paramètre _Activer RMA_, il s&#39;applique à la fois aux nouvelles commandes et aux commandes existantes.

## Activer les RMA pour votre magasin

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales]** en dessous.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL RMA Settings]** .

   ![Paramètres RMA](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Enable RMA on Storefront]** sur `Yes`.

   Ce paramètre détermine si les clients peuvent créer et afficher des demandes RMA à partir du storefront. Les autorisations de retour client peuvent être appliquées aux commandes nouvelles et existantes.

1. Définissez **[!UICONTROL Enable RMA on Product Level]** sur `Yes`.

   Ce paramètre détermine le comportement de l’attribut _Activer RMA_ pour les produits individuels sur le storefront :

   - Lorsque [!UICONTROL Enable RMA on Product Level] est défini sur `Yes`, les clients du storefront peuvent renvoyer tous les produits individuels. Il comprend les valeurs d’attribut de produit _[!UICONTROL Enable RMA]_= `Yes` et_[!UICONTROL Enable RMA]_ = `No`.
   - Lorsque [!UICONTROL Enable RMA on Product Level] est défini sur `No`, les clients du storefront peuvent uniquement renvoyer les produits avec une valeur d’attribut de produit _[!UICONTROL Enable RMA]_= `Yes`.

1. Définissez **[!UICONTROL Use Store Address]** sur l’une des valeurs suivantes :

   - `Yes` - Envoyez les produits renvoyés à l’adresse du magasin.
   - `No` - Saisissez une autre adresse pour les retours de produits.

   ![Paramètres RMA avec une autre adresse](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Config]**.

## Configurer des méthodes d&#39;expédition pour les retours

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Delivery Methods]**.

1. Développez la section correspondant au transporteur que vous souhaitez utiliser pour le service de retour, par exemple **[!UICONTROL UPS]**.

   ![Activer le service RMA pour l&#39;opérateur](./assets/rma-delivery-method.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Enabled for RMA]** sur `Yes`.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Modifier les RMA autorisés au niveau du produit

Si vous activez les autorisations de retour client pour votre magasin et que votre catalogue contient des produits dont le retour ne doit pas être autorisé, vous pouvez modifier le paramètre au niveau du produit,

1. Ouvrez le produit en mode d’édition.

1. Faites défiler vers le bas et développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Autosettings]** .

1. Décochez la case **[!UICONTROL Use Config Setting]** , le cas échéant.

1. Activez/désactivez le paramètre **[!UICONTROL Enable RMA]** sur `No`.

   ![Désactiver RMA pour un produit](./assets/product-advanced-autosettings-enable-rma.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save]**.
