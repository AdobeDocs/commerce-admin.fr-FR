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

L’administrateur [actions](action-log.md) archive répertorie les fichiers journaux CSV stockés sur le serveur. Dans la configuration, vous pouvez spécifier la durée de stockage des entrées du journal et la fréquence à laquelle elles sont archivées. Par défaut, le nom de fichier inclut la date actuelle au format ISO :  `yyyyMMddHH`

>[!NOTE]
>
>L’archivage des logs requiert une [tâche cron](cron.md) à configurer.

## Configuration de l’archive de journal

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Admin Actions Log Archiving]** et définissez les options suivantes :

   - **[!UICONTROL Log Entry Lifetime, Days]** — Saisissez le nombre de jours pendant lesquels vous souhaitez conserver les entrées de journal dans la base de données avant leur suppression.
   - **[!UICONTROL Log Archiving Frequency]** — Définissez sur `Daily`, `Weekly`, ou `Monthly`.

   ![Configuration avancée - archivage des journaux des actions d’administration](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   Pour obtenir la liste détaillée des paramètres de configuration, voir [Archivage du journal des actions d’administration](../configuration-reference/advanced/system.md) dans le _Référence de configuration_.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

## Afficher l’archive

Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Archive]**.

![Archive de journal des actions](./assets/action-log-archive.png){width="600" zoomable="yes"}
