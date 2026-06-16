---
title: Opérations de commande planifiées
description: Découvrez les opérations de commande planifiées et les paramètres cron de commande qui prennent en charge cette fonctionnalité.
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
TQID: https://experienceleague.adobe.com/pViPmBFGErjXeFyvBNBVuJiw8Pn51JIGkeZ2mJAf72M
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 284
ht-degree: 0%

---

# Opérations de commande planifiées

Utilisez les traitements [Cron](../systems/cron.md) pour planifier les tâches de traitement de commande suivantes :

![Grille Commandes](./assets/orders-grid.png){width="700" zoomable="yes"}

## Définir la durée de vie de l&#39;ordre de paiement en attente

La durée de vie des commandes avec paiements en attente est déterminée par la configuration _Paramètres cron des commandes_. La valeur par défaut est définie sur 480 minutes, soit huit heures.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez la section **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales]** en dessous.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Orders Cron Settings]** .

   ![Paramètres Cron des commandes](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. Par **[!UICONTROL Pending Payment Order Lifetime (minutes)]**, saisissez le nombre de minutes avant l&#39;expiration d&#39;un paiement en attente.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Activer les mises à jour de grille planifiées et la réindexation

La configuration Paramètres de grille planifie la mise à jour des grilles d&#39;Oracle Order Management suivantes et réindexe les données comme prévu par [Cron](../systems/cron.md) :

- [Commandes](orders.md#orders-workspace)
- [Factures](invoices.md)
- [Expéditions](shipments.md)
- [Avoirs](credit-memos.md)

En planifiant ces tâches, vous pouvez éviter les verrous qui se produisent lors de l’enregistrement des données et réduire le temps de traitement. Lorsque cette option est activée, les mises à jour n’ont lieu que pendant la tâche cron planifiée. Pour de meilleurs résultats, Cron doit être configuré pour s’exécuter une fois par minute.

**_Pour activer les mises à jour et la réindexation:_**

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."} Lorsque [Mode de production](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#production-mode) (mode par défaut utilisé dans Adobe Commerce sur les infrastructures cloud) est activé, exécutez la commande suivante :

`bin/magento config:set dev/grid/async_indexing 1`

Lorsque le [mode par défaut](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#default-mode) est activé, procédez comme suit :

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez la section **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Developer]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Grid Settings]** .

1. Définissez **[!UICONTROL Asynchronous Indexing]** sur `Enable`.

   ![Paramètres de grille](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Config]**.
