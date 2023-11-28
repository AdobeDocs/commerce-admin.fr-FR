---
title: Ajout de produits à un catalogue partagé
description: Découvrez comment ajouter des produits à un catalogue partagé, individuellement ou en groupes par catégorie.
exl-id: c88b46b4-cea8-4f65-b7e4-6681bab64d41
feature: B2B, Companies, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# Ajout de produits à un catalogue partagé

Les produits peuvent être ajoutés à un catalogue partagé, individuellement ou en groupes de plusieurs produits par catégorie.

Les exigences suivantes doivent être respectées pour qu’un produit complexe (par exemple un lot, groupé ou configurable) soit visible à partir du storefront dans un catalogue partagé :

- Tous [produits associés](../catalog/product-configurations.md) Les options et doivent être affectées au même catalogue partagé et activées dans le catalogue principal.
- Pour [configurable](../catalog/product-create-configurable.md) et [groupé](../catalog/product-create-grouped.md) produits, seuls les produits associés activés sont visibles.
- Pour un [lot](../catalog/product-create-bundle.md) produit, toutes les options doivent être incluses dans le catalogue partagé.

  ![Sélection de produits pour le catalogue](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## Méthode 1 : ajout d’un seul produit

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Pour le produit dans la grille que vous souhaitez ajouter, accédez à la _[!UICONTROL Action]_colonne et cliquez sur **[!UICONTROL Edit]**.

1. Faire défiler vers le bas, développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur _[!UICONTROL Product in Shared Catalogs]_et procédez comme suit :

   - Cochez la case de chaque catalogue partagé où doit apparaître le produit. Pour choisir tous les catalogues, cliquez sur **[!UICONTROL Select all]**.

     ![Produit dans les catalogues partagés](./assets/shared-catalog-assign-from-product.png){width="600" zoomable="yes"}

     Le nom de chaque catalogue sélectionné apparaît dans la _[!UICONTROL Shared Catalogs]_champ .

     ![Catalogues partagés affectés](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

   - Cliquez sur **[!UICONTROL Done]** pour enregistrer les paramètres.

1. Une fois terminé, cliquez sur **[!UICONTROL Save]**.

## Méthode 2 : ajout de plusieurs produits

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Pour le catalogue partagé dans la grille, accédez à la _[!UICONTROL Action]_et sélectionnez **[!UICONTROL Set Pricing and Structure]**.

1. Dans l’arborescence des catégories, effectuez l’une des opérations suivantes :

   - Pour inclure tous les produits, cliquez sur **[!UICONTROL Select all]** ou cochez la case de la catégorie parent.
   - Pour inclure des catégories spécifiques de produits, cochez la case de chaque catégorie à inclure.
   - Pour inclure ou exclure un produit individuel, cochez ou désélectionnez la case correspondant.

   La notation sous chaque catégorie de l’arborescence indique le nombre de produits de la catégorie qui sont actuellement inclus dans le catalogue partagé. La notation sous le [catégorie racine](../catalog/category-root.md) affiche le nombre total de produits de toutes les catégories actuellement sélectionnées pour le catalogue partagé.

1. Pour visualiser les produits de la catégorie dans la grille, cliquez sur le nom de la catégorie dans l&#39;arborescence.

   Lorsqu’une catégorie est sélectionnée, les événements suivants se produisent :

   - Le bouton bascule de la première colonne de la grille est défini sur `On` pour chaque produit sélectionné.
   - Si un produit est affecté à plusieurs catégories et qu’il est omis dans l’une d’elles, il reste disponible par le biais des autres catégories et via [recherche catalogue](../catalog/search.md).
   - Le système définit automatiquement [Autorisations de catégorie](../catalog/category-permissions.md) to `Allow` pour les produits sélectionnés.
