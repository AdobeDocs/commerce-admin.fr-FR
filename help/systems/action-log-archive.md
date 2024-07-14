---
title: Archive de journal des actions
description: Découvrez comment configurer et afficher l’archive du journal des actions d’administration.
exl-id: a839f1c6-b5e2-4881-bfaa-267e47585441
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Archive de journal des actions

{{ee-feature}}

L’archive Admin [actions](action-log.md) répertorie les fichiers journaux CSV stockés sur le serveur. Dans la configuration, vous pouvez spécifier la durée de stockage des entrées du journal et la fréquence à laquelle elles sont archivées. Par défaut, le nom de fichier inclut la date actuelle au format ISO :  `yyyyMMddHH`

>[!NOTE]
>
>L&#39;archivage des logs nécessite la configuration d&#39;une [tâche cron](cron.md).

## Configuration de l’archive de journal

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) et définissez les options suivantes :**[!UICONTROL Admin Actions Log Archiving]**

   - **[!UICONTROL Log Entry Lifetime, Days]** — Saisissez le nombre de jours pendant lesquels vous souhaitez conserver les entrées de journal dans la base de données avant leur suppression.
   - **[!UICONTROL Log Archiving Frequency]** — Défini sur `Daily`, `Weekly` ou `Monthly`.

   ![Configuration avancée - archivage des journaux des actions d’administration](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   Pour obtenir la liste détaillée des paramètres de configuration, voir [Archivage du journal des actions d’administration](../configuration-reference/advanced/system.md) dans la _référence de configuration_.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

## Afficher l’archive

Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Archive]**.

![Archive de journal des actions](./assets/action-log-archive.png){width="600" zoomable="yes"}
