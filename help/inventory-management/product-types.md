---
title: Types de produits
description: Découvrez comment  [!DNL Inventory Management] prend en charge la gestion des stocks et des commandes pour tous les types de produits Adobe Commerce et Magento Open Source.
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# Types de produits

[!DNL Inventory Management] prend en charge la gestion des stocks et des commandes pour tous les types de produits dans Adobe Commerce et Magento Open Source : simple, configurable, virtuel, téléchargeable, groupé et groupé. Les options et les exigences peuvent différer selon le type de produit pour les sources, les stocks et l’expédition.

- [ Les vendeurs uniques ](merchant-sourcing.md#single-source-merchants) créent et mettent à jour des paramètres et des quantités de produits sans nécessiter de mises à jour supplémentaires. Tous les produits créés et nouvellement importés sont automatiquement attribués au Source par défaut et au Stock par défaut, immédiatement disponibles pour les clients s’ils sont activés et en stock.

- [Les marchands multi-sources](merchant-sourcing.md#multi-source-merchants) attribuent des sources, des quantités par source et des paramètres pendant ou après la création du produit. [!DNL Commerce] affecte tous les produits nouvellement importés au Source par défaut, ce qui nécessite des modifications supplémentaires pour affecter les sources et les quantités.

| Type de produit | Algorithme de sélection de la livraison et du Source |
|--|--|
| [[!UICONTROL Simple]](../catalog/product-create-simple.md){target="_blank"} | Prend en charge les recommandations SSA et les remplacements lors de l’expédition. |
| [[!UICONTROL Configurable]](../catalog/product-create-configurable.md){target="_blank"} | Prend en charge les recommandations SSA et les remplacements lors de l’expédition. |
| [[!UICONTROL Virtual]](../catalog/product-create-virtual.md){target="_blank"} | Utilise toujours la recommandation SSA. Le système exécute l’algorithme implicitement lorsqu’il crée des factures et utilise toujours les résultats suggérés.<br/>Vous ne pouvez pas ajuster ces résultats. |
| [[!UICONTROL Downloadable]](../catalog/product-create-downloadable.md){target="_blank"} | Utilise toujours la recommandation SSA. Le système exécute l’algorithme implicitement lorsqu’il crée des factures et utilise toujours les résultats suggérés. <br/>Vous ne pouvez pas ajuster ces résultats. |
| [[!UICONTROL Bundle]](../catalog/product-create-bundle.md){target="_blank"} | Prend en charge les recommandations SSA et les remplacements lors de l’expédition. |
| [[!UICONTROL Grouped]](../catalog/product-create-grouped.md){target="_blank"} | Prend en charge les recommandations SSA et les remplacements lors de l’expédition. |
