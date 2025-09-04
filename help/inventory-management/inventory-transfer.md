---
title: Transférer le stock vers la source
description: Découvrez comment les commerçants multi-sources peuvent transférer des stocks de produits d’un emplacement source à un autre.
exl-id: 30438412-bc93-4e65-8b6a-5ddb50afa7ff
feature: Inventory, Configuration
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# Transférer le stock vers la source

Selon les besoins de l&#39;entreprise et le statut de l&#39;emplacement, les commerçants multi-sources transfèrent souvent les stocks de produits d&#39;un emplacement source à un autre. Par exemple, vous pouvez fermer un emplacement d’entrepôt ou ne plus expédier de produits spécifiques à partir d’un emplacement, et déplacer toutes les opérations de ces produits vers un nouvel emplacement.

Cette option permet de sélectionner un ou plusieurs produits, l&#39;origine du transfert du stock et l&#39;origine de destination des quantités à recevoir :

- Les quantités en stock, le statut de l&#39;article Source (en stock/en rupture de stock) et la quantité à notifier pour l&#39;origine sélectionnée sont déplacés par produit.

- Si un produit n’a pas cette source, il est ignoré.

- Tout le stock de produits pour la source est déplacé. Vous ne pouvez pas transférer une quantité partielle.

>[!NOTE]
>
>Si les origines et les destinations se trouvent dans des stocks différents, cela affecte la quantité vendable agrégée et les réservations pour les commandes en cours.

Vous pouvez également annuler l&#39;affectation de l&#39;origine lors du transfert des quantités en stock.

{{$include /help/_includes/unassign-source.md}}

![Transférer le stock vers une autre source](assets/inventory-bulk-transfer-source.gif)

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Sélectionnez les produits pour lesquels vous souhaitez modifier les sources.

   Parcourez ou recherchez des produits et sélectionnez les cases à cocher à transférer.

1. Cliquez sur le menu **[!UICONTROL Actions]** en haut et choisissez **[!UICONTROL Transfer Inventory to Source]**.

1. Cliquez sur **[!UICONTROL OK]** dans la boîte de dialogue de confirmation.

1. Pour transférer des produits vers une nouvelle destination, sélectionnez l’origine (_[!UICONTROL from]_) source.

1. pour transférer des produits vers une nouvelle destination, sélectionnez la source destination (_[!UICONTROL to]_).

1. Pour supprimer la source des produits, cochez la case facultative **[!UICONTROL Unassign from origin source after transfer]**.

   ![Sélectionner l’origine et la destination du transfert](assets/inventory-bulk-transfer-summary.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Transfer Inventory]**.

   Toutes les quantités de produit sont déduites de la source d&#39;origine et ajoutées à la source de destination. Les champs Quantité et Quantité commercialisable sont automatiquement mis à jour.

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
