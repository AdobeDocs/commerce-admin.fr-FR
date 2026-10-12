---
title: Types de produits
description: Découvrez comment [!DNL Inventory Management] prend en charge la gestion des stocks et des commandes pour tous les types de produits Adobe Commerce et Magento Open Source.
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
TQID: 'https://experienceleague.adobe.com/3F5vZOseQC7ILpL0j-ksjWP-GW7c0gUN9Zy7hylzzHU'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: 8dc0e58b-adf0-51bb-8db5-bb36e3e656fb
    internal-label: Inventory
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '214'
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
