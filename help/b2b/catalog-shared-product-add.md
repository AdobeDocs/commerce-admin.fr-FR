---
title: Ajout de produits à un catalogue partagé
description: Découvrez comment ajouter des produits à un catalogue partagé, individuellement ou en groupes par catégorie.
exl-id: c88b46b4-cea8-4f65-b7e4-6681bab64d41
feature: B2B, Companies, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Ajout de produits à un catalogue partagé

Les produits peuvent être ajoutés à un catalogue partagé, individuellement ou en groupes de plusieurs produits par catégorie.

Les exigences suivantes doivent être respectées pour qu’un produit complexe (par exemple un lot, groupé ou configurable) soit visible à partir du storefront dans un catalogue partagé :

- Tous les [produits associés](../catalog/product-configurations.md) et options doivent être affectés au même catalogue partagé et activés dans le catalogue principal.
- Pour les produits [configurables](../catalog/product-create-configurable.md) et [groupés](../catalog/product-create-grouped.md), seuls les produits associés activés sont visibles.
- Pour un produit [bundle](../catalog/product-create-bundle.md), toutes les options doivent être incluses dans le catalogue partagé.

  ![Sélectionner des produits pour le catalogue](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## Méthode 1 : ajout d’un seul produit

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Pour le produit dans la grille que vous souhaitez ajouter, accédez à la colonne _[!UICONTROL Action]_et cliquez sur **[!UICONTROL Edit]**.

1. Faites défiler la page vers le bas, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) de la section _[!UICONTROL Product in Shared Catalogs]_et procédez comme suit :

   - Cochez la case de chaque catalogue partagé où doit apparaître le produit. Pour choisir tous les catalogues, cliquez sur **[!UICONTROL Select all]**.

     ![Produit dans les catalogues partagés](./assets/shared-catalog-assign-from-product.png){width="600" zoomable="yes"}

     Le nom de chaque catalogue sélectionné apparaît dans le champ _[!UICONTROL Shared Catalogs]_.

     ![Catalogues partagés affectés](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

   - Cliquez sur **[!UICONTROL Done]** pour enregistrer les paramètres.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

## Méthode 2 : ajout de plusieurs produits

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Pour le catalogue partagé dans la grille, accédez à la colonne _[!UICONTROL Action]_et sélectionnez **[!UICONTROL Set Pricing and Structure]**.

1. Dans l’arborescence des catégories, effectuez l’une des opérations suivantes :

   - Pour inclure tous les produits, cliquez sur **[!UICONTROL Select all]** ou cochez la case de la catégorie parente.
   - Pour inclure des catégories spécifiques de produits, cochez la case de chaque catégorie à inclure.
   - Pour inclure ou exclure un produit individuel, cochez ou désélectionnez la case correspondant.

   La notation sous chaque catégorie de l’arborescence indique le nombre de produits de la catégorie qui sont actuellement inclus dans le catalogue partagé. La notation sous la [catégorie racine](../catalog/category-root.md) indique le nombre total de produits de toutes les catégories actuellement sélectionnées pour le catalogue partagé.

1. Pour visualiser les produits de la catégorie dans la grille, cliquez sur le nom de la catégorie dans l&#39;arborescence.

   Lorsqu’une catégorie est sélectionnée, les événements suivants se produisent :

   - Le bouton bascule dans la première colonne de la grille est défini sur `On` pour chaque produit sélectionné.
   - Si un produit est affecté à plusieurs catégories et est omis dans l’une d’elles, il reste disponible par le biais des autres catégories et de la [recherche catalogue](../catalog/search.md).
   - Le système définit automatiquement les [autorisations de catégorie](../catalog/category-permissions.md) sur `Allow` pour les produits sélectionnés.
