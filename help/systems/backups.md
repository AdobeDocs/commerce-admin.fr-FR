---
title: Sauvegardes système
description: Découvrez comment créer et planifier des sauvegardes système, y compris le système de fichiers, la base de données et les fichiers multimédias.
exl-id: 3a9655c1-c124-42be-a487-b31404dada90
feature: System, Configuration
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---

# Sauvegardes système

Adobe Commerce et Magento Open Source vous offrent la possibilité de sauvegarder différentes parties du système, telles que les fichiers du système de fichiers, de la base de données et des médias, et de restaurer automatiquement les données. Un enregistrement pour chaque sauvegarde apparaît dans la grille de la page _Sauvegardes_. La suppression d’un enregistrement de la liste supprime également le fichier archivé. Les fichiers de sauvegarde de la base de données sont compressés au format GZ. Pour les sauvegardes système et les sauvegardes de base de données et de médias, le format TGZ est utilisé. Il est recommandé de limiter l’accès aux outils de sauvegarde et de sauvegarder avant d’installer des extensions et des mises à jour.

- **Restreindre l’accès aux outils de sauvegarde.** L’accès à l’outil de gestion des sauvegardes et des restaurations peut être limité en configurant des [rôles utilisateur](permissions-user-roles.md) pour les ressources de sauvegarde et de restauration. Pour restreindre l’accès, ne cochez pas la case correspondante. Pour autoriser l’accès aux ressources de restauration, vous devez également accorder l’accès aux ressources de sauvegarde.

- **Sauvegardez avant d’installer des extensions et des mises à jour.** Effectuez toujours une sauvegarde avant d’installer une extension ou une mise à jour.

{{$include /help/_includes/backups-note.md}}

## Activation et planification des sauvegardes

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) le **[!UICONTROL Backup Settings]**.

1. Définissez **[!UICONTROL Enabled Schedule Backup]** sur `Yes`.

1. Pour planifier des sauvegardes automatiques, définissez les options de planification suivantes :

   - Définissez **[!UICONTROL Enabled Schedule Backup]** sur `Yes`.
   - Définissez **[!UICONTROL Scheduled Backup Type]** sur le type de sauvegarde à exécuter à l’intervalle planifié.
   - Définissez **[!UICONTROL Start Time]** sur l’heure de la journée à laquelle exécuter l’opération de sauvegarde.
   - Définissez **[!UICONTROL Frequency]** sur `Daily`, `Weekly` ou `Monthly`.
   - Définissez **[!UICONTROL Maintenance Mode]** sur `Yes`.

   ![Configuration avancée - sauvegardes](../configuration-reference/advanced/assets/system-scheduled-backup-settings.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Création d’une sauvegarde

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Backups]**.

1. Dans le coin supérieur droit, cliquez sur le type de sauvegarde à créer :

   - **[!UICONTROL System Backup]** - Crée une sauvegarde complète de la base de données et du système de fichiers. Au cours du processus, vous pouvez choisir d’inclure le dossier de médias dans la sauvegarde.

   - **[!UICONTROL Database and Media Backup]** - Crée une sauvegarde de la base de données et du dossier des médias.

   - **[!UICONTROL Database Backup]** - Crée une sauvegarde de la base de données.

   ![Outils système - sauvegardes](./assets/tools-backups.png){width="600" zoomable="yes"}

1. Pour mettre le magasin en mode de maintenance pendant la sauvegarde, cochez la case.

   Une fois la sauvegarde terminée, le mode de maintenance est automatiquement désactivé.

1. Pour une sauvegarde du système, cochez la case **[!UICONTROL Include Media folder to System Backup]** pour inclure le dossier des médias.

1. Lorsque vous y êtes invité, confirmez l’action.



<!-- Last updated from includes: 2023-02-22 09:59:54 -->
