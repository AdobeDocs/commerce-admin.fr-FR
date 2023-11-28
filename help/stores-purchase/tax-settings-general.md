---
title: Paramètres de configuration des taxes
description: Découvrez comment configurer les paramètres de taxe de base, y compris les classes de taxe, le calcul et la destination de taxe par défaut.
exl-id: e32747f9-20d0-4717-9cee-aa1bcffebb65
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1052'
ht-degree: 0%

---

# Paramètres de configuration des taxes

Les instructions suivantes vous expliquent la configuration de base des taxes pour votre instance Commerce. Avant de configurer vos impôts, assurez-vous de bien connaître les exigences fiscales de vos [locale](store-localize.md#step-3-change-the-locale-of-the-store-view). Ensuite, effectuez le paramétrage fiscal en fonction de vos besoins.

Administration [permissions](../systems/permissions.md) peut être défini sur restreindre . [access](../systems/permissions-user-roles.md) pour taxer les ressources, en fonction de l’entreprise _avoir besoin de savoir_. Pour créer un rôle d’administrateur avec accès aux paramètres de taxe, sélectionnez les ressources Ventes/Taxe et Système/Taxe . Si vous configurez un site web pour une région qui diffère de votre point d’origine d’expédition par défaut, vous devez également autoriser l’accès aux ressources système/d’expédition pour le rôle . Les paramètres d’expédition déterminent le taux de taxe de magasin utilisé pour les prix du catalogue.

## Configuration des paramètres généraux de taxe

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Pour une configuration multi-site, définissez **[!UICONTROL Store View]** sur le site web et le magasin qui est la cible de la configuration.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Tax]**.

1. Définissez les paramètres de configuration suivants.

   Si nécessaire, effacez le **[!UICONTROL Use system value]** de tous les paramètres qui sont grisés.

### [!UICONTROL Tax Classes]

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Tax Classes]** .

   ![Classes d’impôts](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

   - **Classe fiscale d’expédition** — Définissez sur la classe appropriée. Les classes par défaut sont les suivantes : `None` et `Taxable Goods`
   - **Classe fiscale des options de cadeau** — ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Définissez cette variable sur la classe appropriée. Les classes par défaut sont les suivantes : `None` et `Taxable Goods`
   - **Classe de taxe par défaut pour le produit** — Définissez sur la classe appropriée. Les classes par défaut sont les suivantes : `None` et `Taxable Goods`
   - **Classe de taxe par défaut pour le client** — Définissez sur la classe appropriée. La classe par défaut est : `Retail Customer` et `Wholesale Customer`

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

### [!UICONTROL Calculation Settings]

1. Développez l’objet **[!UICONTROL Calculation Settings]** .

   ![Paramètres de calcul](../configuration-reference/sales/assets/tax-calculation-settings.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Tax Calculation Method Based On]** à l’une des options suivantes :

   - `Unit Price` - Le prix de chaque produit
   - `Row Total` - Total de l’article dans la commande, moins remises
   - `Total` - Total de la commande

1. Définir **[!UICONTROL Tax Calculation Based On]** à l’une des options suivantes :

   - `Shipping Address` - Adresse à laquelle la commande doit être expédiée.
   - `Billing Address` - Adresse de facturation du client ou de la société
   - `Shipping Origin` - L’adresse spécifiée en tant que [point d’origine](shipping-settings.md#point-of-origin) pour votre boutique

1. Définir **[!UICONTROL Catalog Prices]** to `Excluding Tax` ou `Including Tax`.

1. Définir **[!UICONTROL Shipping Prices]** to `Excluding Tax` ou `Including Tax`.

1. Définir **[!UICONTROL Apply Customer Tax]** à l’un des éléments suivants pour déterminer si la taxe s’applique au prix d’origine ou au prix actualisé : `After Discount` ou `Before Discount`

1. Définir **[!UICONTROL Apply Discount on Prices]** à l’un des éléments suivants pour déterminer si les remises incluent ou excluent la taxe : `Excluding Tax` ou `Including Tax`

1. Définir **[!UICONTROL Apply Tax On]** to `Custom price if available` ou `Original price only`.

1. Définir **[!UICONTROL Enable Cross-Border Trade]** à l’une des options suivantes :

   - `Yes` - Utiliser des prix cohérents pour différents taux d’imposition. Si le prix du catalogue inclut la taxe, choisissez ce paramètre pour fixer le prix, quel que soit le taux d’imposition du client.
   - `No` - Varier le prix en fonction du taux d&#39;imposition.

   >[!IMPORTANT]
   >
   >If [commerce transfrontalier](#cross-border-price-consistency) est activée, la marge bénéficiaire change par taux d’imposition. Le bénéfice est déterminé par la formule (`Revenue - CustomerVAT - CostOfGoodsSold`). Pour permettre le commerce transfrontalier, les prix doivent être fixés de manière à inclure les taxes.

### [!UICONTROL Default Tax Destination Calculation]

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Default Tax Destination Calculation]** .

   ![Calcul de la destination de la taxe par défaut](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. Spécifiez la variable **[!UICONTROL Default Country]** pour le calcul des impôts.

1. Le cas échéant, indiquez la variable **[!UICONTROL Default State]** pour le calcul des impôts.

1. Le cas échéant, indiquez la variable **[!UICONTROL Default Post Code]** pour le calcul des impôts.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

### [!UICONTROL Price Display Settings]

>[!IMPORTANT]
>
>Certaines combinaisons de paramètres liés à un affichage de prix qui incluent et excluent des taxes peuvent dérouter le client. Pour éviter de déclencher un message d’avertissement, reportez-vous au [paramètres recommandés](taxes.md#warning-messages).

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Price Display Settings]** .

   ![Paramètres d’affichage des prix](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Display Product Prices in Catalog]** à l’une des options suivantes :

   - `Excluding Tax` - Les prix du catalogue qui apparaissent sur le storefront ne comprennent pas la taxe.
   - `Including Tax` - Les prix du catalogue dans la vitrine incluent la taxe uniquement si une règle de taxe correspond à l’origine de la taxe ou si l’adresse du client correspond à la règle de taxe. Cela peut se produire lorsqu’un client crée un compte, se connecte ou utilise l’outil Estimer les impôts et l’expédition dans le panier.
   - `Including and Excluding Tax` - Les prix du catalogue qui apparaissent dans le storefront sont affichés avec et sans taxe.

1. Définir **[!UICONTROL Display Shipping Prices]** to `Excluding Tax`, `Including Tax`, ou `Including and Excluding Tax`.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

### [!UICONTROL Shopping Cart Display Settings]

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Shopping Cart Display Settings]** .

   ![Paramètres d’affichage du panier](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. Pour chacun des paramètres suivants, choisissez la manière dont vous souhaitez que les taxes et les prix apparaissent dans le panier, en fonction des exigences de votre boutique et de vos paramètres régionaux :

   - Définir **[!UICONTROL Display Prices]** to `Excluding Tax`, `Including Tax`, ou `Including and Excluding Tax`.

   - Définir **[!UICONTROL Display Subtotal]** to `Excluding Tax`, `Including Tax`, ou `Including and Excluding Tax`.

   - Définir **[!UICONTROL Display Shipping Amount]** to `Excluding Tax`, `Including Tax`, ou `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Défini **[!UICONTROL Display Gift Wrapping Prices]** to `Excluding Tax`, `Including Tax`, ou `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Défini **[!UICONTROL Display Printed Card Prices]** to `Excluding Tax`, `Including Tax`, ou `Including and Excluding Tax`.

1. Définissez les options d’affichage suivantes sur : `Yes` ou `No`, selon vos besoins :

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

### [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

1. Développer ![Extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** .

   ![Paramètres d’affichage des commandes, factures et notes de crédit](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. Indiquez le mode d’affichage des prix et des taxes dans les commandes, les factures et les notes de crédit :

   - Définir **[!UICONTROL Display Prices]** to `Excluding Tax`, `Including Tax`, ou `Including and Excluding Tax`.

   - Définir **[!UICONTROL Display Subtotal]** to `Excluding Tax`, `Including Tax`, ou `Including and Excluding Tax`.

   - Définir **[!UICONTROL Display Shipping Amount]** to `Excluding Tax`, `Including Tax`, ou `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Défini **[!UICONTROL Display Gift Wrapping Prices]** to `Excluding Tax`, `Including Tax`, ou `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Défini **[!UICONTROL Display Printed Card Prices]** to `Excluding Tax`, `Including Tax`, ou `Including and Excluding Tax`.

1. Définissez les options d’affichage suivantes sur : `Yes` ou `No`, selon vos besoins :

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

### [!UICONTROL Fixed Product Taxes]

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Fixed Product Taxes]** .

   ![Taxes sur les produits fixes](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Enable FPT]** à `Yes` ou `No`, selon vos besoins.

1. Si FPT est activé, spécifiez les options d’affichage FPT :

   - **[!UICONTROL Display Prices in Product Lists]**
   - **[!UICONTROL Display Price On Product view Page]**
   - **[!UICONTROL Display Prices in Sales Modules]**
   - **[!UICONTROL Display Prices in Emails]**

   - `Including FPT Only` - Les prix affichés incluent les taxes sur les produits fixes. Le montant FPT n’est pas affiché séparément.
   - `Including FPT and FPT description` - Les prix affichés incluent les taxes sur les produits fixes. Le montant FPT est affiché séparément.
   - `Excluding FPT. Including FPT description and final price` - Les prix affichés ne comprennent pas les taxes sur les produits fixes. Le montant FPT est affiché séparément.
   - `Excluding FPT` - Les prix affichés ne comprennent pas les taxes sur les produits fixes. Le montant FPT n’est pas affiché séparément.

1. Définir **[!UICONTROL Apply Discounts to FPT]** to `Yes` ou `No`, selon vos besoins.

1. Définir **[!UICONTROL FPT Tax Configuration]** pour déterminer le mode de calcul du FPT.

   - `Not Taxed` - Sélectionnez cette option si votre juridiction fiscale ne taxe pas le TPT. (Par exemple, la Californie.)
   - `Taxed` - Sélectionnez cette option si votre juridiction fiscale applique le TPT. (Par exemple, Canada.)
   - `Loaded and Displayed with Tax` - Cliquez sur cette option si FPT est ajouté au total de la commande avant d’appliquer la taxe. (Par exemple, les pays de l&#39;UE.)

1. Définir **[!UICONTROL Include FPT in Subtotal]** to `Yes` ou `No`, selon vos besoins.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

## Cohérence transfrontalière des prix

Le commerce transfrontalier (également appelé cohérence des prix) soutient l&#39;Union européenne (UE) et d&#39;autres commerçants qui veulent maintenir des prix cohérents pour les clients dont les taux d&#39;imposition sont différents du taux d&#39;imposition des magasins.

Les commerçants opérant dans plusieurs régions et zones géographiques peuvent afficher un seul prix en incluant la taxe dans le prix du produit. Les prix sont propres et ordonnés indépendamment des structures et des taux d&#39;imposition qui varient d&#39;un pays à l&#39;autre. Ces paramètres nécessitent qu’une extension de calcul des taxes soit installée à partir de la variable [Marché](../getting-started/commerce-marketplace.md), par exemple _Vertex Cloud_.

>[!NOTE]
>
>Lorsque le commerce transfrontalier est activé, votre marge bénéficiaire change par taux d’imposition. Le profit est déterminé par la formule :<br>
>`Revenue - CustomerVAT - CostOfGoodsSold`

**_Pour assurer la cohérence transfrontalière des prix :_**

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Pour une configuration multi-site, définissez **[!UICONTROL Store View]** sur le site web et le magasin qui est la cible de la configuration.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Tax]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Calculation Settings]** .

1. Définir **[!UICONTROL Catalog Prices]** to `Including Tax`.

1. Pour assurer la cohérence des prix transfrontaliers, définissez **[!UICONTROL Enable Cross Border Trade]** to `Yes`.

   ![Activation des paramètres commerciaux transfrontaliers](./assets/cross-border-calculations-settings.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.
