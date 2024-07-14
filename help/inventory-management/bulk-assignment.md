---
title: Affectation et annulation d’attribution de sources d’inventaire en bloc
description: Découvrez comment utiliser l’outil Affecter des sources pour gérer les affectations de sources pour les produits.
exl-id: 1f1e81a5-fb06-46b7-84ca-7feea4942093
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---

# Affectation et annulation d’affectation de sources en bloc

Utilisez l’outil _Affecter des sources_ pour ajouter une ou plusieurs sources à vos produits. L’outil vous aide à créer et à affecter des sources personnalisées à vos stocks par défaut ou personnalisés et à préparer de nouveaux emplacements et stocks.

Après avoir ajouté de nouvelles sources personnalisées, vous pouvez ajouter [quantités d&#39;inventaire par produit](quantities-assign-per-product.md) ou pour plusieurs produits par l&#39;intermédiaire de l&#39;administrateur ou à l&#39;aide de la [fonction d&#39;import](inventory-import-export.md).

![Ajouter des sources d’inventaire pour les produits sélectionnés](assets/inventory-bulk-assign-sources.gif)

## Attribuer des sources et des quantités

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Sélectionnez les produits pour lesquels vous souhaitez modifier les sources.

   Recherchez ou recherchez les produits et cochez ces cases.

1. Cliquez sur le menu **[!UICONTROL Actions]** en haut de l’écran et choisissez **[!UICONTROL Assign Inventory Source]**.

1. Cliquez sur **[!UICONTROL OK]** dans la boîte de dialogue de confirmation.

1. Pour toutes les sources à ajouter aux produits, cochez les cases.

1. Cliquez sur **[!UICONTROL Assign Sources]**.

   ![Sélectionner les produits à ajouter des sources](assets/inventory-bulk-assign-sources-summary.png){width="600" zoomable="yes"}

Les sources sont ajoutées aux produits dont la quantité d’inventaire est de 0. Vous pouvez ajouter [quantités d&#39;inventaire](quantities-assign-per-product.md) par source.

## Annulation de l’affectation des sources et des quantités

Lorsque vous annulez l’attribution d’une source à un produit, vous indiquez que ce dernier n’est plus stocké à cet emplacement. Ce processus efface complètement toutes les données d’inventaire pour la source actuellement affectée au produit. Si vous souhaitez déplacer l’inventaire existant vers un nouvel emplacement, envisagez d’utiliser l’option _Transférer l’inventaire_ .

{{$include /help/_includes/unassign-source.md}}

Il est vivement recommandé de terminer toutes les commandes et tous les envois de ces produits avant de supprimer la source.

![Annulation de l’affectation de sources aux produits sélectionnés](assets/inventory-bulk-unassign-sources.gif)

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Sélectionnez les produits pour lesquels vous souhaitez modifier les sources.

   Recherchez ou recherchez les produits et cochez ces cases.

1. Cliquez sur le menu **[!UICONTROL Actions]** en haut de l’écran et choisissez **[!UICONTROL Unassign Inventory Source]**.

1. Cliquez sur **[!UICONTROL OK]** dans la boîte de dialogue de confirmation.

1. Sélectionnez la source que vous souhaitez supprimer des produits.

   La page affiche une alerte indiquant que l’annulation de l’attribution supprime toutes les données source et quantité spécifiques du produit.

1. Cliquez sur **[!UICONTROL Unassign Sources]**.

   ![Supprimer des sources des produits sélectionnés](assets/inventory-bulk-unassign-sources-summary.png){width="600" zoomable="yes"}
