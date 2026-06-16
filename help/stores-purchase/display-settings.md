---
title: Paramètres d’affichage des prix
description: Découvrez l’affichage des taxes dans le catalogue, le panier, les commandes, les factures et les avoirs qui prennent en charge l’expérience d’achat du client.
exl-id: 6f97c474-ef6e-4ca6-899d-812c58b993ca
feature: Checkout, Invoices, Taxes
TQID: https://experienceleague.adobe.com/XIcN-vl8owiToGhM3Et2euyNWgnJdsgSl6urwJcRdLE
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 519
ht-degree: 0%

---

# Paramètres d’affichage des prix

Les paramètres d’affichage des prix déterminent si les prix des produits et des frais d’expédition incluent ou excluent la taxe, ou affichent deux versions du prix : l’une avec et l’autre sans taxe.

Si le prix du produit inclut la taxe, la taxe n&#39;apparaît que s&#39;il existe une règle de taxe correspondant à l&#39;origine de la taxe ou si une adresse client correspond à la règle de taxe. Les événements pouvant déclencher une correspondance incluent le moment où un client crée un compte, se connecte ou génère une estimation de taxe et d’expédition à partir du panier.

>[!IMPORTANT]
>
>L’affichage des prix qui incluent et excluent la taxe peut prêter à confusion pour le client. Pour éviter de déclencher un message d’avertissement, consultez les [directives](international-tax-guidelines.md) pour votre pays et [paramètres recommandés](taxes.md#warning-messages) pour éviter les messages d’avertissement.

![Paramètres d’affichage des prix](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

Pour obtenir une description détaillée de chacun de ces paramètres de configuration, consultez [Paramètres d’affichage du prix](../configuration-reference/sales/tax.md#price-display-settings) dans le _Guide de référence de configuration_.

## Configurer les paramètres d’affichage des prix

Lorsque la configuration du calcul des taxes, taux et classes est terminée, les taxes sont calculées en fonction de ces paramètres. Cependant, l’affichage des taxes dans le catalogue, le panier, les commandes, les factures et les avoirs doit également être configuré pour prendre en charge l’expérience client sur le storefront.

Il est recommandé d&#39;afficher les prix avec les taxes associées (taxes comprises ou les deux, taxes comprises et taxes exclues) afin que les clients sachent comment ces calculs sont appliqués avant de passer une commande.

### Étape 1 : Configurer les paramètres d&#39;affichage des prix de catalogue

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Tax]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Price Display Settings]** .

1. Par **[!UICONTROL Display Product Prices in Catalog]**, choisissez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

   >[!NOTE]
   >
   >Si vous définissez cette option sur `Including Tax`, la taxe n&#39;apparaît que s&#39;il existe une règle de taxe correspondant à l&#39;origine de la taxe ou si une adresse client correspond à la règle de taxe. Les événements pouvant déclencher une correspondance incluent la création d’un compte client, la connexion ou l’utilisation de l’outil d’estimation Taxe et expédition dans le panier.

1. Par **[!UICONTROL Display Shipping Prices]**, choisissez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

Si vous choisissez d’afficher les deux prix (avec et sans taxe), le storefront ressemble à ce qui suit :

![Exemple d&#39;affichage des prix incluant les taxes sur le storefront](./assets/catalog-prices-tax.png){width="700" zoomable="yes"}

### Étape 2 : Configurer les paramètres d’affichage du panier

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Shopping Cart Display Settings]** .

   ![Paramètres d’affichage du panier](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. Par **[!UICONTROL Display Prices]**, choisissez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Par **[!UICONTROL Display Subtotal]**, choisissez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Par **[!UICONTROL Display Shipping Amount]**, choisissez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Par **[!UICONTROL Display Gift Wrapping Prices]**, choisissez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Par **[!UICONTROL Display Printed Card Prices]**, choisissez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Pour chacune de ces options restantes, basculez sur `Yes` ou `No` selon vos préférences :

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

### Étape 3 : Configurer les paramètres d&#39;affichage des commandes, des factures et des avoirs

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** .

   ![Paramètres d&#39;affichage des commandes, factures, avoirs](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. Par **[!UICONTROL Display Prices]**, choisissez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Par **[!UICONTROL Display Subtotal]**, choisissez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Par **[!UICONTROL Display Shipping Amount]**, choisissez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Par **[!UICONTROL Display Gift Wrapping Prices]**, choisissez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Par **[!UICONTROL Display Printed Card Prices]**, choisissez l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Pour chacune de ces options restantes, basculez sur `Yes` ou `No` selon vos préférences :

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
