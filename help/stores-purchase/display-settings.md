---
title: Paramètres d'affichage des prix
description: Découvrez l’affichage des taxes dans le catalogue, le panier, les commandes, les factures et les notes de crédit qui prennent en charge l’expérience d’achat des clients.
exl-id: 6f97c474-ef6e-4ca6-899d-812c58b993ca
feature: Checkout, Invoices, Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# Paramètres d&#39;affichage des prix

Les paramètres d’affichage des prix déterminent si les prix de produit et d’expédition incluent ou excluent la taxe, ou affichent deux versions du prix : l’une avec et l’autre sans taxe.

Si le prix du produit inclut la taxe, la taxe n’apparaît que si une règle de taxe correspond à l’origine de la taxe ou si une adresse du client correspond à la règle de taxe. Les événements pouvant déclencher une correspondance sont notamment lorsqu’un client crée un compte, se connecte ou génère une estimation de la taxe et de l’expédition à partir du panier.

>[!IMPORTANT]
>
>L’affichage des prix qui incluent et excluent la taxe peut dérouter le client. Pour éviter de déclencher un message d’avertissement, reportez-vous aux [directives](international-tax-guidelines.md) pour votre pays et aux [paramètres recommandés](taxes.md#warning-messages) pour éviter les messages d’avertissement.

![Paramètres d’affichage du prix](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

Pour une description détaillée de chacun de ces paramètres de configuration, voir [Paramètres d’affichage du prix](../configuration-reference/sales/tax.md#price-display-settings) dans le _Guide de référence de configuration_.

## Configuration des paramètres d’affichage des prix

Lorsque le paramétrage du calcul des taxes, des taux et des classes est terminé, les taxes sont calculées selon ces paramètres. Cependant, l’affichage des taxes dans le catalogue, le panier, les commandes, les factures et les notes de crédit doit également être configuré pour prendre en charge l’expérience client sur le storefront.

Il est recommandé d’afficher les prix avec les taxes associées (y compris les taxes, ou les deux, les taxes comprises et les taxes exclues) afin que les clients sachent comment ces calculs sont appliqués avant de passer une commande.

### Étape 1 : configuration des paramètres d&#39;affichage des prix du catalogue

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Tax]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Price Display Settings]** .

1. Pour **[!UICONTROL Display Product Prices in Catalog]**, sélectionnez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

   >[!NOTE]
   >
   >Si vous définissez cette option sur `Including Tax`, la taxe n’apparaît que si une règle de taxe correspond à l’origine de la taxe ou si une adresse de client correspond à la règle de taxe. Les événements qui peuvent déclencher une correspondance incluent la création d’un compte client, la connexion ou l’utilisation de l’outil d’estimation des taxes et des frais d’expédition dans le panier.

1. Pour **[!UICONTROL Display Shipping Prices]**, sélectionnez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

Si vous choisissez d&#39;afficher les deux prix (avec et sans taxe), la vitrine ressemble à ce qui suit :

![Exemple d&#39;affichage de prix incluant des taxes sur le storefront](./assets/catalog-prices-tax.png){width="700" zoomable="yes"}

### Étape 2 : configuration des paramètres d’affichage du panier

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Shopping Cart Display Settings]** .

   ![ Paramètres d’affichage du panier](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. Pour **[!UICONTROL Display Prices]**, sélectionnez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Pour **[!UICONTROL Display Subtotal]**, sélectionnez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Pour **[!UICONTROL Display Shipping Amount]**, sélectionnez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Pour **[!UICONTROL Display Gift Wrapping Prices]**, sélectionnez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Pour **[!UICONTROL Display Printed Card Prices]**, sélectionnez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Pour chacune de ces options restantes, basculez sur `Yes` ou `No` selon vos préférences :

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

### Étape 3 : configuration des paramètres d’affichage de la commande, de la facture et de la note de crédit

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** .

   ![Commandes, factures, Paramètres d’affichage des notes de crédit](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. Pour **[!UICONTROL Display Prices]**, sélectionnez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Pour **[!UICONTROL Display Subtotal]**, sélectionnez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Pour **[!UICONTROL Display Shipping Amount]**, sélectionnez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Pour **[!UICONTROL Display Gift Wrapping Prices]**, sélectionnez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Pour **[!UICONTROL Display Printed Card Prices]**, sélectionnez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Pour chacune de ces options restantes, basculez sur `Yes` ou `No` selon vos préférences :

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
