---
title: Opérations de commande planifiées
description: Découvrez les opérations de commande planifiées et les paramètres cron des commandes qui prennent en charge cette fonctionnalité.
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
source-git-commit: db859c40cd6f052a8f1153e245c23d9f1ea97d33
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Opérations de commande planifiées

Utilisation [Cron](../systems/cron.md) tâches pour planifier les tâches de traitement de l’ordre suivantes :

![Grille des commandes](./assets/orders-grid.png){width="700" zoomable="yes"}

## Définition de la durée de vie des commandes de paiement en attente

La durée de vie des commandes en attente est déterminée par la variable _Paramètres Cron des commandes_ configuration. La valeur par défaut est définie sur 480 minutes, soit huit heures.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez la variable **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales]** en-dessous.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Orders Cron Settings]** .

   ![Paramètres Cron des commandes](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. Pour **[!UICONTROL Pending Payment Order Lifetime (minutes)]**, saisissez le nombre de minutes avant l’expiration d’un paiement en attente.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Activation des mises à jour de grille planifiées et de la réindexation

La configuration Paramètres de grille planifie les mises à jour des grilles de gestion des commandes suivantes et réindexe les données comme prévu par [Cron](../systems/cron.md):

- [Commandes](orders.md#orders-workspace)
- [Facturations](invoices.md)
- [Expéditions](shipments.md)
- [Avoir](credit-memos.md)

En planifiant ces tâches, vous pouvez éviter les verrous qui se produisent lorsque les données sont enregistrées et réduire le temps de traitement. Lorsque cette option est activée, les mises à jour ne sont effectuées que pendant la tâche cron planifiée. Pour de meilleurs résultats, Cron doit être configuré pour s’exécuter une fois par minute.

**_Pour activer les mises à jour et la réindexation :_**

When [Mode de production](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#production-mode) (le mode par défaut utilisé dans Adobe Commerce sur l’infrastructure cloud) est activé, exécutez la commande suivante :

``bin/magento config:set dev/grid/async_indexing 1``

When [Mode par défaut](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#default-mode) est activée, procédez comme suit :

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez la variable **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Developer]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Grid Settings]** .

1. Définir **[!UICONTROL Asynchronous Indexing]** to `Enable`.

   ![Paramètres de grille](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Config]**.
