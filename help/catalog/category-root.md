---
title: Catégorie et hiérarchie racine
description: Découvrez la hiérarchie des catégories et la catégorie racine, qui agit comme un conteneur pour le menu principal dans l’arborescence des catégories.
exl-id: b419cb45-4fe5-42c4-be20-667c7e1e4354
feature: Catalog Management, Categories, Site Navigation
TQID: https://experienceleague.adobe.com/nkUEOu8IqMM21waPwmkp76YckH6cToL6MiaSK--klho
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fc
subfeature_v2: id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 437
ht-degree: 0%

---

# Catégorie et hiérarchie racine

Les produits du menu principal sont déterminés par la catégorie racine affectée au [magasin](../stores-purchase/stores.md#add-stores). La catégorie racine est essentiellement un conteneur pour le menu principal dans l’arborescence des catégories. Vous pouvez créer une catégorie racine avec un ensemble de produits entièrement nouveau ou copier des produits d’une catégorie racine existante. La catégorie racine peut être affectée au magasin actuel ou à tout autre magasin du même site web.

![Diagramme de hiérarchie de catalogue](./assets/catalog-hierarchy-scope.svg){width="550"}

De l’côté de l’administrateur, la structure des catégories est comme une arborescence à l’envers, avec la racine en haut. La racine porte un nom, mais pas de clé URL, et n’apparaît pas dans la [navigation supérieure](navigation-top.md) du magasin. Toutes les autres catégories du menu sont imbriquées sous la racine. La catégorie racine étant le niveau le plus élevé du catalogue, votre magasin ne peut avoir qu’une seule catégorie racine active à la fois. Vous pouvez toutefois créer des catégories racine supplémentaires pour d’autres structures de catalogue et différents magasins.

L’exemple suivant montre comment créer une catégorie racine et l’affecter à un autre magasin.

## Étape 1 : créer une catégorie racine

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Sur la gauche, cliquez sur **[!UICONTROL Add Root Category]**.

   ![Nouvelle catégorie racine ](./assets/category-root-ee.png){width="600" zoomable="yes"}

1. Saisissez un **[!UICONTROL Category Name]**.

   Le nom que vous choisissez est initialement attribué à toutes les vues de magasin.

1. Si vous souhaitez ajouter des produits au catalogue à partir du catalogue actuel, procédez comme suit :

   - Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section _Produits dans la catégorie_.

   - Utilisez les [filtres de recherche](../getting-started/admin-grid-controls.md) pour trouver les produits de votre choix et cochez la case correspondant à chaque produit à copier dans le nouveau catalogue.

1. Cliquez ensuite sur **[!UICONTROL Save]**.

## Étape 2 : créer le menu principal

1. Sur la gauche, sélectionnez la nouvelle catégorie racine que vous avez créée à l’étape précédente.

1. Pour créer la [structure des catégories](category-create.md) pour le menu principal, cliquez sur **[!UICONTROL Add Subcategory]** et suivez les instructions.

## Étape 3 : affecter la catégorie racine au magasin

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Dans la colonne _Magasins_ de la grille, cliquez sur le magasin auquel vous souhaitez affecter le nouveau catalogue.

1. Définissez **[!UICONTROL Root Category]** sur la nouvelle catégorie racine que vous avez créée.

1. Assurez-vous qu’un **[!UICONTROL Default Store View]** est affecté au magasin.

   Le magasin doit avoir au moins une vue de [magasin](../stores-purchase/store-views.md).

1. Cliquez ensuite sur **[!UICONTROL Save Store]**.

1. Pour vérifier que le magasin dispose d’un nouveau catalogue, procédez comme suit :

   - Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

     Tous les produits qui ont été copiés dans le nouveau catalogue apparaissent dans la grille.

   - Pour vérifier que le nouveau catalogue et le menu principal fonctionnent correctement, rendez-vous sur le storefront.
