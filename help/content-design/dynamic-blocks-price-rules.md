---
title: Blocs dynamiques dans les règles de prix
description: Associez un bloc dynamique à une règle de prix promotionnel.
exl-id: e1564df2-1c06-4d11-a32d-6f5c0be974e3
feature: Page Content, Price Rules
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Blocs dynamiques dans les règles de prix

{{ee-feature}}

Tout [bloc dynamique](dynamic-blocks.md) que vous créez peut être associé à une promotion. Pour effectuer l’association, vous devez d’abord créer le bloc dynamique et la [règle de prix de catalogue](../merchandising-promotions/price-rules-catalog.md) ou [règle de prix de panier](../merchandising-promotions/price-rules-cart.md). L’association peut être établie en travaillant sur une règle de prix ou en travaillant sur un bloc dynamique.

>[!IMPORTANT]
>
>Après avoir créé cette association, le bloc dynamique s’affiche **uniquement** lorsque la règle se déclenche. Si la promotion est ciblée sur le segment A, le bloc s’affiche sur le segment A. Si la promotion n’est pas active, le bloc n’est pas affiché.

## Associer un bloc dynamique à une règle de prix

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_&#x200B;et choisissez l’une des options suivantes :

   - **[!UICONTROL Catalog Price Rules]**
   - **[!UICONTROL Cart Price Rules]**

1. Dans la grille, recherchez la règle à associer au bloc dynamique et ouvrez-la en mode d’édition.

1. Faites défiler vers le bas et développez le **[!UICONTROL Related Dynamic Blocks]** ![Sélecteur d’extension](../assets/icon-display-expand.png).

1. Dans la première colonne, définissez le filtre sur `Any`, puis cliquez sur **[!UICONTROL Reset Filter]**.

   La grille répertorie désormais tous les blocs dynamiques disponibles.

1. Cochez la case de chaque bloc dynamique que vous souhaitez associer à la règle.

   ![Ajout des blocs dynamiques sélectionnés](./assets/price-rule-cart-related-dynamic-blocks-any.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save]**.

## Associer une règle de prix à un bloc dynamique

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

1. Recherchez le bloc dynamique dans la grille et ouvrez-le en mode d’édition.

1. Faites défiler vers le bas et développez **[!UICONTROL Related Promotions]**.

   Toutes les règles de prix actuellement associées apparaissent dans la grille.

1. Ajoutez une nouvelle règle associée ou supprimez une association actuelle.

   - Pour associer une promotion de panier, cliquez sur **[!UICONTROL Add Cart Price Rules]**.

   - Pour associer une promotion liée à un produit, cliquez sur **[!UICONTROL Add Catalog Price Rules]**.

1. Dans la grille, cochez la case de chaque règle à associer au bloc dynamique.

1. Cliquez sur **[!UICONTROL Add Selected]**.

   ![Ajouter des règles de prix sélectionnées à un bloc dynamique](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save]**.
