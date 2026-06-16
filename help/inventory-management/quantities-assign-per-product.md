---
title: Affecter des quantités en stock par produit
description: Découvrez comment mettre à jour les quantités en stock de votre produit et suivre les quantités en stock disponibles.
exl-id: 935385bb-6657-4d49-980e-96a3d0d3a187
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/0OBXyHUbsWVXmEnWEWd0CGcBNhci57w8HGtDCGCWuOk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 210
ht-degree: 0%

---

# Attribuer des quantités par produit

Après avoir ajouté [sources](sources-assign-per-product.md), mettez à jour les quantités en stock de votre produit. Ces valeurs effectuent le suivi des stocks disponibles en stock.

Pour masquer le stock d&#39;une source des expéditions sans supprimer la source, définissez _[!UICONTROL Source Item Status]_sur `Out of Stock`. Les options SSA et expédition accèdent uniquement aux sources répertoriées comme `In Stock` avec la quantité en stock disponible.

Toutes les quantités et toutes les sources mises à jour s&#39;affichent dans la grille de produits.

## Mettre à jour les quantités

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Rechercher et ouvrir un produit en mode d’édition

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Sources]** .

1. Définissez **[!UICONTROL Source Item Status]** sur `In Stock`.

1. pour mettre à jour la quantité du stock disponible, saisissez un montant pour **[!UICONTROL Qty]**.

1. Pour définir une notification pour les quantités en stock, effectuez l&#39;une des opérations suivantes :

   - Quantité de notification personnalisée - Décochez la case **[!UICONTROL Use Default]** et saisissez un montant en **[!UICONTROL Notify Qty]**.
   - Quantité de notification par défaut - Cochez la case **[!UICONTROL Use Default]**. [!DNL Commerce] vérifie et utilise le paramètre dans la configuration de magasin _[!UICONTROL Advanced Inventory]_ou globale.

   ![Mettre à jour les quantités de produits par Source](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Effectuez l’une des opérations suivantes pour enregistrer :

   - Cliquez sur **[!UICONTROL Save]**.

   - Dans le menu **[!UICONTROL Save]** (![flèche du menu](../assets/icon-menu-down-arrow-red.png)), choisissez **[!UICONTROL Save & Close]**.


La grille de produits est mise à jour avec une liste de toutes les sources et des quantités associées. Pour les produits comportant plus de cinq sources affectées, passez la souris sur la colonne _[!UICONTROL Quantity per Source]_pour afficher la liste complète.

![Quantités de produits par source](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
