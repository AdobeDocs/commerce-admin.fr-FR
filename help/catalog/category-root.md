---
title: Catégorie et hiérarchie racine
description: Découvrez la hiérarchie de catégories et la catégorie racine, qui agit comme un conteneur pour le menu principal dans l’arborescence des catégories.
exl-id: b419cb45-4fe5-42c4-be20-667c7e1e4354
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---

# Catégorie et hiérarchie racine

Les produits du menu principal sont déterminés par la catégorie racine affectée au [magasin](../stores-purchase/stores.md#add-stores). La catégorie racine est essentiellement un conteneur pour le menu principal dans l’arborescence des catégories. Vous pouvez créer une catégorie racine avec un ensemble entièrement nouveau de produits ou copier des produits d’une catégorie racine existante. La catégorie racine peut être affectée au magasin actuel ou à tout autre magasin du même site web.

![&#x200B; Diagramme de hiérarchie de catalogue &#x200B;](./assets/catalog-hierarchy-scope.svg){width="550"}

Depuis l’administrateur, la structure de catégorie est semblable à une arborescence ascendante, avec la racine au-dessus. La racine a un nom, mais aucune clé d’URL et n’apparaît pas dans la [navigation supérieure](navigation-top.md) du magasin. Toutes les autres catégories du menu sont imbriquées sous la racine. Comme la catégorie racine est le niveau le plus élevé du catalogue, votre boutique ne peut avoir qu’une seule catégorie racine active à la fois. Vous pouvez toutefois créer d’autres catégories racine pour d’autres structures de catalogue et différents magasins.

L’exemple suivant montre comment créer une catégorie racine et l’affecter à un autre magasin.

## Étape 1 : création d’une catégorie racine

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Sur la gauche, cliquez sur **[!UICONTROL Add Root Category]**.

   ![Nouvelle catégorie racine](./assets/category-root-ee.png){width="600" zoomable="yes"}

1. Saisissez un **[!UICONTROL Category Name]**.

   Le nom que vous choisissez est initialement attribué à toutes les vues de magasin.

1. Si vous souhaitez ajouter des produits au catalogue à partir du catalogue actuel, procédez comme suit :

   - Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) _Produits dans la catégorie_ .

   - Utilisez les [filtres de recherche](../getting-started/admin-grid-controls.md) pour rechercher les produits que vous souhaitez et cochez la case correspondant à chaque produit que vous souhaitez copier dans le nouveau catalogue.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

## Etape 2 : construire le menu principal

1. Sur la gauche, sélectionnez la nouvelle catégorie racine que vous avez créée à l’étape précédente.

1. Pour créer la [structure de catégorie](category-create.md) pour le menu principal, cliquez sur **[!UICONTROL Add Subcategory]** et suivez les instructions.

## Étape 3 : Attribution de la catégorie racine au magasin

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Dans la colonne _Magasins_ de la grille, cliquez sur le magasin auquel vous souhaitez attribuer le nouveau catalogue.

1. Définissez **[!UICONTROL Root Category]** sur la nouvelle catégorie racine que vous avez créée.

1. Assurez-vous que **[!UICONTROL Default Store View]** est affecté au magasin.

   Le magasin doit avoir au moins une [vue de magasin](../stores-purchase/store-views.md).

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Store]**.

1. Pour vérifier que le magasin comporte un nouveau catalogue, procédez comme suit :

   - Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

     Tous les produits copiés dans le nouveau catalogue apparaissent dans la grille.

   - Pour vérifier que le nouveau catalogue et le nouveau menu principal fonctionnent correctement, consultez le storefront.
