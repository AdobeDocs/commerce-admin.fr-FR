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

Après ajout [sources](sources-assign-per-product.md), mettez à jour les quantités d’inventaire de votre produit. Ces valeurs effectuent le suivi des montants en stock disponibles.

Pour masquer l’inventaire d’une source des envois sans supprimer la source, définissez _[!UICONTROL Source Item Status]_to `Out of Stock`. Les options d’ASS et d’expédition n’accèdent qu’aux sources répertoriées comme `In Stock` avec la quantité de stock disponible.

Toutes les quantités et sources mises à jour s’affichent dans la grille de produits.

## Mettre à jour les quantités

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Recherchez et ouvrez un produit en mode d’édition.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Sources]** .

1. Définir **[!UICONTROL Source Item Status]** to `In Stock`.

1. pour mettre à jour la quantité du stock disponible, saisissez un montant pour **[!UICONTROL Qty]**.

1. Pour définir une notification pour les quantités d&#39;inventaire, effectuez l&#39;une des opérations suivantes :

   - Quantité de notification personnalisée - Désélectionnez l’option **[!UICONTROL Use Default]** et saisissez un montant dans **[!UICONTROL Notify Qty]**.
   - Quantité de notification par défaut : sélectionnez la valeur **[!UICONTROL Use Default]** . [!DNL Commerce] vérifie et utilise le paramètre de la fonction _[!UICONTROL Advanced Inventory]_ou configuration de magasin globale.

   ![Mise à jour des quantités de produits par source](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Effectuez l’une des opérations suivantes pour enregistrer :

   - Cliquez sur **[!UICONTROL Save]**.

   - Sur le **[!UICONTROL Save]** (![Flèche de menu](../assets/icon-menu-down-arrow-red.png)), choisissez **[!UICONTROL Save & Close]**.


La grille de produits est mise à jour avec une liste de toutes les sources et des quantités associées. Pour les produits comportant plus de cinq sources affectées, passez la souris sur la variable _[!UICONTROL Quantity per Source]_pour afficher la liste complète.

![Quantités de produits par source](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
