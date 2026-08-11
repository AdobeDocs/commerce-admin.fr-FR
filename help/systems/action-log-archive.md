---
title: Archive du journal des actions
description: Découvrez comment configurer et afficher l’archive du journal des actions d’administration.
exl-id: a839f1c6-b5e2-4881-bfaa-267e47585441
feature: Logs, Configuration
TQID: https://experienceleague.adobe.com/xgyeoO5XJFZPopM9bsIn2oOtrxl4fyuEY2du5ryXeTY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 756e3b7f8c70e0b3fc6f30691a15bd7e20517655
workflow-type: tm+mt
source-wordcount: 220
ht-degree: 0%

---

# Archive du journal des actions

{{ee-feature}}

L’archive Admin [actions](action-log.md) répertorie les fichiers journaux CSV stockés sur le serveur.

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."} dans la configuration, vous pouvez spécifier la durée pendant laquelle les entrées de journal sont stockées et la fréquence à laquelle elles sont archivées. Par défaut, le nom de fichier inclut la date actuelle au format ISO : `yyyyMMddHH`

>[!NOTE]
>
>L’archivage des journaux nécessite la configuration d’une tâche [cron](cron.md).

## Configuration de l’archive du journal

badgePaas : label=« PaaS uniquement » type=« Informative » url=« https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions » tooltip=« S’applique aux projets Adobe Commerce sur Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-Premise uniquement. »

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
