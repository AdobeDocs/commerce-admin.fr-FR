---
title: Actions en bloc
description: Découvrez comment configurer et afficher le journal des actions en bloc.
exl-id: 3907d9ef-3592-4dbb-805f-97b79bafd8ab
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---

# Actions en bloc

{{ee-feature}}

Le journal des actions en masse enregistre les détails des opérations de masse asynchrones qui s’exécutent en arrière-plan, comme l’importation/exportation ou l’attribution de [prix personnalisés](../b2b/catalog-shared-manage.md#update-custom-pricing) à plusieurs produits dans un [ catalogue partagé](../b2b/catalog-shared.md).

![Journal des actions en masse](./assets/bulk-actions-log.png){width="600" zoomable="yes"}

## Configuration des actions en bloc

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) et définissez l’option d’enregistrement du journal :**[!UICONTROL Bulk Actions]**

   **[!UICONTROL Days Saved in Log]** — Saisissez le nombre de jours pendant lesquels les actions en bloc sont enregistrées dans un journal.

   ![Configuration avancée - actions en masse](../configuration-reference/advanced/assets/system-bulk-actions.png){width="600" zoomable="yes"}

   Pour obtenir la liste détaillée des paramètres de configuration, voir [_Actions en bloc_](../configuration-reference/advanced/system.md) dans la _référence sur la configuration_.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

## Affichage des actions en bloc

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Bulk Actions]**.

1. Recherchez l’action souhaitée dans le journal.

1. Dans la colonne _[!UICONTROL Action]_, cliquez sur **[!UICONTROL Details]**.
