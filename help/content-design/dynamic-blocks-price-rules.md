---
title: Blocs dynamiques dans les règles de prix
description: Associez un bloc dynamique à une règle de prix promotionnel.
exl-id: e1564df2-1c06-4d11-a32d-6f5c0be974e3
feature: Page Content, Price Rules
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Blocs dynamiques dans les règles de prix

{{ee-feature}}

Quelconque [bloc dynamique](dynamic-blocks.md) que vous créez peut être associé à une promotion. Pour créer l’association, vous devez d’abord créer le bloc dynamique et le [règle de prix du catalogue](../merchandising-promotions/price-rules-catalog.md) ou [règle de prix du panier](../merchandising-promotions/price-rules-cart.md). L&#39;association peut être réalisée lorsque vous travaillez sur une règle de prix ou lorsque vous travaillez sur un bloc dynamique.

>[!IMPORTANT]
>
>Une fois cette association créée, le bloc dynamique s&#39;affiche. **only** lorsque la règle se déclenche. Si la promotion est ciblée sur le segment A, le bloc s’affiche sur le segment A. Si la promotion n&#39;est pas active, le bloc ne s&#39;affiche pas.

## Associer un bloc dynamique à une règle de prix

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_et sélectionnez l’une des options suivantes :

   - **[!UICONTROL Catalog Price Rules]**
   - **[!UICONTROL Cart Price Rules]**

1. Dans la grille, recherchez la règle que vous souhaitez associer au bloc dynamique et ouvrez-la en mode d&#39;édition.

1. Faire défiler vers le bas et développer ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Related Dynamic Blocks]**.

1. Dans la première colonne, définissez le filtre sur `Any` et cliquez sur **[!UICONTROL Reset Filter]**.

   La grille répertorie désormais tous les blocs dynamiques disponibles.

1. Cochez la case de chaque bloc dynamique à associer à la règle.

   ![Ajouter les blocs dynamiques sélectionnés](./assets/price-rule-cart-related-dynamic-blocks-any.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

## Associer une règle de prix à un bloc dynamique

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

1. Recherchez le bloc dynamique dans la grille et ouvrez-le en mode d&#39;édition.

1. Faire défiler vers le bas et développer **[!UICONTROL Related Promotions]**.

   Toutes les règles de prix actuellement associées apparaissent dans la grille.

1. Ajoutez une nouvelle règle associée ou supprimez une association actuelle.

   - Pour associer une promotion de panier, cliquez sur **[!UICONTROL Add Cart Price Rules]**.

   - Pour associer une promotion associée à un produit, cliquez sur **[!UICONTROL Add Catalog Price Rules]**.

1. Dans la grille, cochez la case de chaque règle à associer au bloc dynamique.

1. Cliquez sur **[!UICONTROL Add Selected]**.

   ![Ajouter des règles de prix sélectionnées à un bloc dynamique](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.
