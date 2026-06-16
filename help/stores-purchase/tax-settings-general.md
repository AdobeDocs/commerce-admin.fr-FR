---
title: Paramètres de configuration des taxes
description: Découvrez comment configurer les paramètres de taxe de base, y compris les classes de taxe, le calcul et la destination de taxe par défaut.
exl-id: e32747f9-20d0-4717-9cee-aa1bcffebb65
feature: Taxes
TQID: https://experienceleague.adobe.com/qM41ryN8UDdW9ZlCF8YGrCRZ6hUiaw2OsSumslKnjI8
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1053
ht-degree: 0%

---

# Paramètres de configuration des taxes

Les instructions suivantes vous guident tout au long de la configuration de base de la taxe pour votre instance Commerce. Avant de configurer vos taxes, assurez-vous de connaître les exigences fiscales de vos [paramètres régionaux](store-localize.md#step-3-change-the-locale-of-the-store-view). Ensuite, effectuez le paramétrage fiscal en fonction de vos besoins.

Les autorisations d’administrateur [autorisations](../systems/permissions.md) peuvent être définies de manière à restreindre l’[accès](../systems/permissions-user-roles.md) aux ressources fiscales, en fonction de l’entreprise _besoin de savoir_. Pour créer un rôle d&#39;administrateur avec un accès aux paramètres de taxe, choisissez les ressources Ventes/Taxe et Système/Taxe. Si vous configurez un site web pour une région différente de votre point d’origine d’expédition par défaut, vous devez également autoriser l’accès aux ressources Système/Expédition pour le rôle. Les paramètres d’expédition déterminent le taux de taxe de la boutique utilisé pour les prix du catalogue.

## Configurer les paramètres généraux de taxe

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Pour une configuration multisite, définissez **[!UICONTROL Store View]** sur le site web et le magasin cibles de la configuration.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Tax]**.

1. Définissez les paramètres de configuration suivants.

   Si nécessaire, décochez la case **[!UICONTROL Use system value]** de tous les paramètres grisés.

### [!UICONTROL Tax Classes]

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Tax Classes]** .

   ![Classes d&#39;impôts](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

   - **Classe de taxe pour l&#39;expédition** — Définissez-la sur la classe appropriée. Les classes par défaut sont : `None` et `Taxable Goods`
   - **Classe de taxe pour les options de cadeau** — ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Définissez sur la classe appropriée. Les classes par défaut sont : `None` et `Taxable Goods`
   - **Classe de taxe par défaut pour le produit** — Définissez sur la classe appropriée. Les classes par défaut sont : `None` et `Taxable Goods`
   - **Classe de taxe par défaut pour le client** — Définissez sur la classe appropriée. La classe par défaut est : `Retail Customer` et `Wholesale Customer`

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

### [!UICONTROL Calculation Settings]

1. Développez la section **[!UICONTROL Calculation Settings]** .

   ![Paramètres de calcul](../configuration-reference/sales/assets/tax-calculation-settings.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Tax Calculation Method Based On]** sur l’une des options suivantes :

   - `Unit Price` - Le prix de chaque produit
   - `Row Total` - Total de la ligne dans la commande, moins les remises
   - `Total` - Total de la commande

1. Définissez **[!UICONTROL Tax Calculation Based On]** sur l’une des options suivantes :

   - `Shipping Address` - Adresse à laquelle la commande doit être expédiée
   - `Billing Address` - Adresse de facturation du client ou de la société
   - `Shipping Origin` - Adresse spécifiée comme [point d’origine](shipping-settings.md#point-of-origin) pour votre boutique

1. Définissez **[!UICONTROL Catalog Prices]** sur `Excluding Tax` ou `Including Tax`.

1. Définissez **[!UICONTROL Shipping Prices]** sur `Excluding Tax` ou `Including Tax`.

1. Définissez **[!UICONTROL Apply Customer Tax]** sur l’une des options suivantes pour déterminer si la taxe est appliquée au prix d’origine ou au prix réduit : `After Discount` ou `Before Discount`

1. Définissez **[!UICONTROL Apply Discount on Prices]** sur l&#39;un des éléments suivants pour déterminer si les remises incluent ou excluent la taxe : `Excluding Tax` ou `Including Tax`

1. Définissez **[!UICONTROL Apply Tax On]** sur `Custom price if available` ou `Original price only`.

1. Définissez **[!UICONTROL Enable Cross-Border Trade]** sur l’une des options suivantes :

   - `Yes` - Utilisez une tarification cohérente pour les différents taux de taxe. Si le prix catalogue inclut la taxe, sélectionnez ce paramètre pour fixer le prix indépendamment du taux de taxe du client.
   - `No` - Variez le prix en fonction du taux de taxe.

   >[!IMPORTANT]
   >
   >Si le [commerce transfrontalier](#cross-border-price-consistency) est activé, la marge bénéficiaire change en fonction du taux d&#39;imposition. Le bénéfice est déterminé par la formule (`Revenue - CustomerVAT - CostOfGoodsSold`). Pour permettre le commerce transfrontalier, les prix doivent être fixés en incluant la taxe.

### [!UICONTROL Default Tax Destination Calculation]

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Default Tax Destination Calculation]** .

   ![Calcul de la destination de taxe par défaut](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. Spécifiez les **[!UICONTROL Default Country]** pour les calculs de taxe.

1. Le cas échéant, spécifiez la **[!UICONTROL Default State]** pour les calculs de taxe.

1. Le cas échéant, spécifiez la **[!UICONTROL Default Post Code]** pour les calculs de taxe.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

### [!UICONTROL Price Display Settings]

>[!IMPORTANT]
>
>Certaines combinaisons de paramètres liés à un affichage des prix qui incluent et excluent la taxe peuvent être déroutantes pour le client. Pour éviter de déclencher un message d’avertissement, consultez les [paramètres recommandés](taxes.md#warning-messages).

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Price Display Settings]** .

   ![Paramètres d’affichage des prix](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Display Product Prices in Catalog]** sur l’une des options suivantes :

   - `Excluding Tax` - Les prix du catalogue qui apparaissent dans le storefront n&#39;incluent pas les taxes.
   - `Including Tax` - Les prix du catalogue dans le storefront incluent la taxe uniquement si une règle de taxe correspond à l&#39;origine de la taxe ou si l&#39;adresse du client correspond à la règle de taxe. Cela peut se produire une fois qu’un client a créé un compte, s’est connecté ou a utilisé l’outil Estimation des taxes et des frais d’expédition dans le panier.
   - `Including and Excluding Tax` - Les prix du catalogue qui apparaissent dans le storefront sont affichés avec et sans taxe.

1. Définissez **[!UICONTROL Display Shipping Prices]** sur `Excluding Tax`, `Including Tax` ou `Including and Excluding Tax`.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

### [!UICONTROL Shopping Cart Display Settings]

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Shopping Cart Display Settings]** .

   ![Paramètres d’affichage du panier](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. Pour chacun des paramètres suivants, choisissez comment vous souhaitez que les taxes et les prix apparaissent dans le panier, en fonction des exigences de votre magasin et des paramètres régionaux :

   - Définissez **[!UICONTROL Display Prices]** sur `Excluding Tax`, `Including Tax` ou `Including and Excluding Tax`.

   - Définissez **[!UICONTROL Display Subtotal]** sur `Excluding Tax`, `Including Tax` ou `Including and Excluding Tax`.

   - Définissez **[!UICONTROL Display Shipping Amount]** sur `Excluding Tax`, `Including Tax` ou `Including and Excluding Tax`.

   - ![](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Définissez **[!UICONTROL Display Gift Wrapping Prices]** sur `Excluding Tax`, `Including Tax` ou `Including and Excluding Tax`.

   - ![](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Définissez **[!UICONTROL Display Printed Card Prices]** sur `Excluding Tax`, `Including Tax` ou `Including and Excluding Tax`.

1. Définissez les options d’affichage suivantes sur `Yes` ou `No`, selon vos besoins :

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

### [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

1. Développez ![Développement](../assets/icon-display-expand.png) la section **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** .

   ![Paramètres d&#39;affichage des commandes, factures, avoirs](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. Indiquez comment les prix et les taxes apparaissent dans les commandes, les factures et les avoirs :

   - Définissez **[!UICONTROL Display Prices]** sur `Excluding Tax`, `Including Tax` ou `Including and Excluding Tax`.

   - Définissez **[!UICONTROL Display Subtotal]** sur `Excluding Tax`, `Including Tax` ou `Including and Excluding Tax`.

   - Définissez **[!UICONTROL Display Shipping Amount]** sur `Excluding Tax`, `Including Tax` ou `Including and Excluding Tax`.

   - ![](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Définissez **[!UICONTROL Display Gift Wrapping Prices]** sur `Excluding Tax`, `Including Tax` ou `Including and Excluding Tax`.

   - ![](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Définissez **[!UICONTROL Display Printed Card Prices]** sur `Excluding Tax`, `Including Tax` ou `Including and Excluding Tax`.

1. Définissez les options d’affichage suivantes sur `Yes` ou `No`, selon vos besoins :

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

### [!UICONTROL Fixed Product Taxes]

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Fixed Product Taxes]** .

   ![Taxes sur les produits fixes](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Enable FPT]** sur `Yes` ou `No`, selon vos besoins.

1. Si FPT est activé, spécifiez les options d’affichage FPT :

   - **[!UICONTROL Display Prices in Product Lists]**
   - **[!UICONTROL Display Price On Product view Page]**
   - **[!UICONTROL Display Prices in Sales Modules]**
   - **[!UICONTROL Display Prices in Emails]**

   - `Including FPT Only` - Les prix affichés incluent les taxes fixes sur les produits. Le montant FPT n’est pas affiché séparément.
   - `Including FPT and FPT description` - Les prix affichés incluent les taxes fixes sur les produits. Le montant FPT est affiché séparément.
   - `Excluding FPT. Including FPT description and final price` - Les prix affichés n&#39;incluent pas les taxes fixes sur les produits. Le montant FPT est affiché séparément.
   - `Excluding FPT` - Les prix affichés n&#39;incluent pas les taxes fixes sur les produits. Le montant FPT n’est pas affiché séparément.

1. Définissez **[!UICONTROL Apply Discounts to FPT]** sur `Yes` ou `No`, selon vos besoins.

1. Définissez **[!UICONTROL FPT Tax Configuration]** pour déterminer comment le FPT est calculé.

   - `Not Taxed` - Sélectionnez cette option si votre juridiction d’imposition ne taxe pas FPT. (Par exemple, la Californie.)
   - `Taxed` - Sélectionnez cette option si votre juridiction d’imposition taxe FPT. (Par exemple, le Canada.)
   - `Loaded and Displayed with Tax` - Cliquez sur cette option si FPT est ajouté au total de la commande avant l&#39;application de la taxe. (Par exemple, les pays de l&#39;UE.)

1. Définissez **[!UICONTROL Include FPT in Subtotal]** sur `Yes` ou `No`, selon vos besoins.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Cohérence transfrontalière des prix

Le commerce transfrontalier (également appelé cohérence des prix) soutient l&#39;Union européenne (UE) et d&#39;autres commerçants qui veulent maintenir des prix cohérents pour les clients dont les taux de taxe sont différents du taux de taxe du magasin.

Les commerçants qui exercent leurs activités dans plusieurs régions et régions géographiques peuvent afficher un prix unique en incluant la taxe dans le prix du produit. La tarification est propre et épurée, quelles que soient les structures et les taux d&#39;imposition qui varient d&#39;un pays à l&#39;autre. Ces paramètres nécessitent qu’une extension de calcul des taxes soit installée à partir du [Marketplace](../getting-started/commerce-marketplace.md), tel que _Vertex Cloud_.

>[!NOTE]
>
>Lorsque le commerce transfrontalier est activé, votre marge bénéficiaire change en fonction du taux d&#39;imposition. Le bénéfice est déterminé par la formule suivante : <br>
>`Revenue - CustomerVAT - CostOfGoodsSold`

**_Pour permettre la cohérence des prix transfrontaliers:_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Pour une configuration multisite, définissez **[!UICONTROL Store View]** sur le site web et le magasin cibles de la configuration.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Tax]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Calculation Settings]** .

1. Définissez **[!UICONTROL Catalog Prices]** sur `Including Tax`.

1. Pour permettre la cohérence des prix transfrontaliers, définissez **[!UICONTROL Enable Cross Border Trade]** sur `Yes`.

   ![Activer les paramètres de commerce transfrontalier](./assets/cross-border-calculations-settings.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
