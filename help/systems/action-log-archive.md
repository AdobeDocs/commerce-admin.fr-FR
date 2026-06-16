---
title: Archive du journal des actions
description: Découvrez comment configurer et afficher l’archive du journal des actions d’administration.
exl-id: a839f1c6-b5e2-4881-bfaa-267e47585441
feature: Logs, Configuration
TQID: https://experienceleague.adobe.com/xgyeoO5XJFZPopM9bsIn2oOtrxl4fyuEY2du5ryXeTY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 160
ht-degree: 0%

---

# Archive du journal des actions

{{ee-feature}}

L’archive Admin [actions](action-log.md) répertorie les fichiers journaux CSV stockés sur le serveur. Dans la configuration d’, vous pouvez spécifier la durée pendant laquelle les entrées du journal sont stockées et la fréquence à laquelle elles sont archivées. Par défaut, le nom de fichier inclut la date actuelle au format ISO : `yyyyMMddHH`

>[!NOTE]
>
>L’archivage des journaux nécessite la configuration d’une tâche [cron](cron.md).

## Configuration de l’archive du journal

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Admin Actions Log Archiving]** et définissez les options suivantes :

   - **[!UICONTROL Log Entry Lifetime, Days]** — Entrez le nombre de jours pendant lesquels vous souhaitez conserver les entrées de journal dans la base de données avant de les supprimer.
   - **[!UICONTROL Log Archiving Frequency]** — Définissez sur `Daily`, `Weekly` ou `Monthly`.

   ![Configuration avancée - archivage du journal des actions d’administration](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   Pour obtenir la liste détaillée des paramètres de configuration, voir [Archivage du journal des actions d’administration](../configuration-reference/advanced/system.md) dans la _Référence de configuration_.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Afficher l’archive

Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Archive]**.

![Archive du journal des actions](./assets/action-log-archive.png){width="600" zoomable="yes"}
