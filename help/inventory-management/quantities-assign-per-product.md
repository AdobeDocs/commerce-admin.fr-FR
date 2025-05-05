---
title: Attribuer des quantités de stock par produit
description: Découvrez comment mettre à jour les quantités de stock de votre produit et suivre les quantités de stock disponibles.
exl-id: 935385bb-6657-4d49-980e-96a3d0d3a187
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Attribuer des quantités par produit

Après avoir ajouté [sources](sources-assign-per-product.md), mettez à jour les quantités d’inventaire de votre produit. Ces valeurs effectuent le suivi des montants en stock disponibles.

Pour masquer l’inventaire d’une source des envois sans supprimer la source, définissez _[!UICONTROL Source Item Status]_&#x200B;sur `Out of Stock`. Les options SSA et d’expédition accèdent uniquement aux sources répertoriées en tant que `In Stock` avec la quantité de stock disponible.

Toutes les quantités et sources mises à jour s’affichent dans la grille de produits.

## Mettre à jour les quantités

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Recherchez et ouvrez un produit en mode d’édition.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Sources]** .

1. Définissez **[!UICONTROL Source Item Status]** sur `In Stock`.

1. pour mettre à jour la quantité du stock disponible, saisissez un montant pour **[!UICONTROL Qty]**.

1. Pour définir une notification pour les quantités d&#39;inventaire, effectuez l&#39;une des opérations suivantes :

   - Quantité de notification personnalisée - Décochez la case **[!UICONTROL Use Default]** et saisissez un montant dans **[!UICONTROL Notify Qty]**.
   - Quantité de notification par défaut : cochez la case **[!UICONTROL Use Default]** . [!DNL Commerce] vérifie et utilise le paramètre dans _[!UICONTROL Advanced Inventory]_&#x200B;ou la configuration de magasin globale.

   ![Mettre à jour les quantités de produits par Source](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Effectuez l’une des opérations suivantes pour enregistrer :

   - Cliquez sur **[!UICONTROL Save]**.

   - Dans le menu **[!UICONTROL Save]** (![Flèche de menu](../assets/icon-menu-down-arrow-red.png)), choisissez **[!UICONTROL Save & Close]**.


La grille de produits est mise à jour avec une liste de toutes les sources et des quantités associées. Pour les produits avec plus de cinq sources affectées, passez la souris sur la colonne _[!UICONTROL Quantity per Source]_&#x200B;pour afficher la liste complète.

![Quantités de produits par source](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
