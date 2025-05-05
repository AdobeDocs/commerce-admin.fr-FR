---
title: Opérations de commande planifiées
description: Découvrez les opérations de commande planifiées et les paramètres cron de commande qui prennent en charge cette fonctionnalité.
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
source-git-commit: fdc14758788fa5cd0391371ebfafb478dadec8a4
workflow-type: tm+mt
source-wordcount: '252'
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

**_Pour activer les mises à jour et la réindexation, procédez comme suit_**

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."} Lorsque [Mode de production](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html?lang=fr#production-mode) (mode par défaut utilisé dans Adobe Commerce sur les infrastructures cloud) est activé, exécutez la commande suivante :

`bin/magento config:set dev/grid/async_indexing 1`

Lorsque le [mode par défaut](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html?lang=fr#default-mode) est activé, procédez comme suit :

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez la section **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Developer]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Grid Settings]** .

1. Définissez **[!UICONTROL Asynchronous Indexing]** sur `Enable`.

   ![Paramètres de grille](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Config]**.
