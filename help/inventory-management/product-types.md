---
title: Types de produits
description: Découvrez comment prend  [!DNL Inventory Management]  charge la gestion des stocks et des commandes pour tous les types de produits Adobe Commerce et Magento Open Source.
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/3F5vZOseQC7ILpL0j-ksjWP-GW7c0gUN9Zy7hylzzHU
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 213
ht-degree: 0%

---

# Types de produits

[!DNL Inventory Management] prend en charge la gestion des stocks et des commandes pour tous les types de produits dans Adobe Commerce et Magento Open Source : simple, configurable, virtuel, téléchargeable, groupé et groupé. Les options et les exigences peuvent différer selon le type de produit pour les sources, les stocks et l’expédition.

- [Les commerçants monosources](merchant-sourcing.md#single-source-merchants) créent et mettent à jour les paramètres et les quantités des produits sans nécessiter de mises à jour supplémentaires. Tous les produits créés et nouvellement importés sont automatiquement affectés au Source par défaut et au Stock par défaut, immédiatement disponibles pour les clients si activé et En stock.

- [Marchands multi-sources](merchant-sourcing.md#multi-source-merchants) attribuez des sources, des quantités par source et des paramètres pendant ou après la création du produit. [!DNL Commerce] affecte tous les produits nouvellement importés au Source par défaut, ce qui nécessite des modifications supplémentaires pour affecter des sources et des quantités.

| Type de produit | Algorithme de sélection des expéditions et des Source |
|--|--|
| [[!UICONTROL Simple]](../catalog/product-create-simple.md){target="_blank"} | Prend en charge les recommandations et les remplacements SSA lors de l’expédition. |
| [[!UICONTROL Configurable]](../catalog/product-create-configurable.md){target="_blank"} | Prend en charge les recommandations et les remplacements SSA lors de l’expédition. |
| [[!UICONTROL Virtual]](../catalog/product-create-virtual.md){target="_blank"} | Utilise toujours la recommandation SSA. Le système exécute l’algorithme implicitement lors de la création des factures et utilise toujours les résultats suggérés.<br/>Vous ne pouvez pas ajuster ces résultats. |
| [[!UICONTROL Downloadable]](../catalog/product-create-downloadable.md){target="_blank"} | Utilise toujours la recommandation SSA. Le système exécute l’algorithme implicitement lors de la création des factures et utilise toujours les résultats suggérés. <br/>Vous ne pouvez pas ajuster ces résultats. |
| [[!UICONTROL Bundle]](../catalog/product-create-bundle.md){target="_blank"} | Prend en charge les recommandations et les remplacements SSA lors de l’expédition. |
| [[!UICONTROL Grouped]](../catalog/product-create-grouped.md){target="_blank"} | Prend en charge les recommandations et les remplacements SSA lors de l’expédition. |
