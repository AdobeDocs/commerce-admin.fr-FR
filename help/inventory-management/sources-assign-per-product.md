---
title: Attribution de sources d’inventaire par produit
description: Découvrez comment attribuer une source d’inventaire à un produit.
exl-id: 7e47be25-633e-4f5d-bb61-0d9e79b6dbad
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# Attribution de sources par produit

Avant de modifier les quantités et les paramètres, vous devez attribuer [sources](sources-manage.md) aux produits.

{{$include /help/_includes/unassign-source.md}}

## Affectation de sources à un produit

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Ouvrez un produit en mode _Modifier_ .

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Sources]** .

   Cette section vous permet de modifier la source, de mettre à jour les quantités d’inventaire, etc.

   >[!NOTE]
   >
   >Actuellement, seuls les produits simples, configurables, virtuels, téléchargeables et regroupés prennent en charge plusieurs sources. Les produits en bundle peuvent être créés et gérés uniquement avec les Source et Stock par défaut.

   ![Section Sources de produits](assets/inventory-product-sources-before.png){width="600" zoomable="yes"}

1. Pour ajouter une source, cliquez sur **[!UICONTROL Assign Sources]**.

1. Sur la page _[!UICONTROL Assign Sources]_, cochez la case en regard de chaque source à affecter au produit.

   ![Produit - attribuer des sources](assets/inventory-product-assign-sources.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Done]** pour ajouter les sources.

1. Effectuez l’une des opérations suivantes pour enregistrer :

   - Cliquez sur **[!UICONTROL Save]**.
   - Dans le menu _[!UICONTROL Save]_(![flèche de menu](../assets/icon-menu-down-arrow-red.png)), choisissez **[!UICONTROL Save & Close]**.

Après avoir affecté des sources, mettez à jour la [quantité d’inventaire](quantities-assign-per-product.md) pour chaque source de produit.
