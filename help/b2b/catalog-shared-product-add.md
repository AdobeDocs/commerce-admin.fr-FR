---
title: Ajout de produits à un catalogue partagé
description: Découvrez comment ajouter des produits à un catalogue partagé, individuellement ou par groupes par catégorie.
exl-id: c88b46b4-cea8-4f65-b7e4-6681bab64d41
feature: B2B, Companies, Catalog Management
TQID: https://experienceleague.adobe.com/f-5xQDov-Q3tfYw8MBDQPinimUIUkGe-q2Nfzm8L9ps
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 402
ht-degree: 0%

---

# Ajout de produits à un catalogue partagé

Les produits peuvent être ajoutés à un catalogue partagé individuellement ou par groupes de plusieurs produits par catégorie.

Pour qu’un produit complexe (tel qu’une offre groupée, groupée ou configurable) soit visible depuis le storefront dans un catalogue partagé, les conditions suivantes doivent être remplies :

- Tous les [produits associés](../catalog/product-configurations.md) et options doivent être affectés au même catalogue partagé et activés dans le catalogue principal.
- Pour les produits [configurables](../catalog/product-create-configurable.md) et [groupés](../catalog/product-create-grouped.md) seuls les produits associés activés sont visibles.
- Pour un produit [bundle](../catalog/product-create-bundle.md), toutes les options doivent être incluses dans le catalogue partagé.

  ![Sélectionner les produits pour le catalogue](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## Méthode 1 : Ajouter un seul produit

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Pour le produit dans la grille que vous souhaitez ajouter, accédez à la colonne _[!UICONTROL Action]_&#x200B;et cliquez sur **[!UICONTROL Edit]**.

1. Faites défiler vers le bas, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section _[!UICONTROL Product in Shared Catalogs]_, puis procédez comme suit :

   - Cochez la case de chaque catalogue partagé dans lequel le produit doit apparaître. Pour sélectionner tous les catalogues, cliquez sur **[!UICONTROL Select all]**.

     ![Produit dans les catalogues partagés](./assets/shared-catalog-assign-from-product.png){width="600" zoomable="yes"}

     Le nom de chaque catalogue sélectionné s’affiche dans le champ _[!UICONTROL Shared Catalogs]_.

     ![Catalogues partagés affectés](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

   - Cliquez sur **[!UICONTROL Done]** pour enregistrer les paramètres.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

## Méthode 2 : ajout de plusieurs produits

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Pour le catalogue partagé dans la grille, accédez à la colonne _[!UICONTROL Action]_&#x200B;et sélectionnez **[!UICONTROL Set Pricing and Structure]**.

1. Dans l’arborescence des catégories, effectuez l’une des opérations suivantes :

   - Pour inclure tous les produits, cliquez sur **[!UICONTROL Select all]** ou cochez la case de la catégorie parent.
   - Pour inclure des catégories spécifiques de produits, cochez la case de chaque catégorie à inclure.
   - Pour inclure ou exclure un produit individuel, cochez ou décochez la case du produit.

   La notation sous chaque catégorie de l’arborescence indique le nombre de produits de la catégorie actuellement inclus dans le catalogue partagé. La notation sous la [catégorie racine](../catalog/category-root.md) indique le nombre total de produits de toutes les catégories actuellement sélectionnées pour le catalogue partagé.

1. Pour afficher les produits de catégorie dans la grille, cliquez sur le nom de la catégorie dans l’arborescence.

   Lorsqu’une catégorie est sélectionnée, les événements suivants se produisent :

   - Le bouton (bascule) de la première colonne de la grille est défini sur `On` pour chaque produit sélectionné.
   - Si un produit est affecté à plusieurs catégories et est omis dans l’une d’entre elles, il reste disponible dans les autres catégories et dans [recherche catalogue](../catalog/search.md).
   - Le système définit automatiquement les [autorisations de catégorie](../catalog/category-permissions.md) sur `Allow` pour les produits sélectionnés.
