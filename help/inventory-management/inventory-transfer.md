---
title: Transférer l’inventaire à la source
description: Découvrez comment les marchands multi-sources peuvent transférer l’inventaire des produits d’un emplacement source à un autre.
exl-id: 30438412-bc93-4e65-8b6a-5ddb50afa7ff
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# Transférer l’inventaire à la source

En fonction des besoins de l’entreprise et de l’état de l’emplacement, les marchands multi-sources transfèrent souvent l’inventaire des produits d’un emplacement source à un autre. Par exemple, vous fermez peut-être un emplacement d’entrepôt ou vous n’expédiez plus de produits spécifiques d’un emplacement, déplaçant toutes les opérations de ces produits vers un nouvel emplacement.

Cette option vous permet de sélectionner un ou plusieurs produits, la source d’origine à transférer l’inventaire et la source de destination à recevoir les quantités :

- Les quantités d’inventaire, l’état de l’article source (en stock/en rupture de stock) et l’état de notification de la quantité de la source sélectionnée sont déplacés par produit.

- Si un produit n’a pas cette source, il est ignoré.

- L’inventaire de tous les produits de la source est déplacé. Vous ne pouvez pas transférer une quantité partielle.

>[!NOTE]
>
>Si les sources d&#39;origine et de destination se trouvent dans des stocks différents, cela affecte la quantité agrégée de ventes et les réservations pour les commandes en cours.

Vous pouvez également annuler l’affectation de la source lors du transfert des quantités d’inventaire.

{{$include /help/_includes/unassign-source.md}}

![Transférer l’inventaire vers une autre source](assets/inventory-bulk-transfer-source.gif)

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Sélectionnez les produits pour lesquels vous souhaitez modifier les sources.

   Recherchez des produits et cochez des cases pour les transférer.

1. Cliquez sur le bouton **[!UICONTROL Actions]** dans la partie supérieure et choisissez **[!UICONTROL Transfer Inventory to Source]**.

1. Cliquez sur **[!UICONTROL OK]** dans la boîte de dialogue de confirmation.

1. Pour transférer des produits vers une nouvelle destination, sélectionnez l’origine (_[!UICONTROL from]_).

1. pour transférer des produits vers une nouvelle destination, sélectionnez la destination (_[!UICONTROL to]_).

1. Pour supprimer la source des produits, cochez la case facultative . **[!UICONTROL Unassign from origin source after transfer]**.

   ![Sélection de l’origine et de la destination du transfert](assets/inventory-bulk-transfer-summary.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Transfer Inventory]**.

   Toutes les quantités de produits sont déduites de la source d&#39;origine et ajoutées à la source de destination. La quantité et la quantité vendable sont automatiquement mises à jour.
