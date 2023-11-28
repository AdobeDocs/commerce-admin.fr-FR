---
title: Sauvegardes système
description: Découvrez comment créer et planifier des sauvegardes système, y compris le système de fichiers, la base de données et les fichiers multimédias.
exl-id: 3a9655c1-c124-42be-a487-b31404dada90
feature: System, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Sauvegardes système

Adobe Commerce et Magento Open Source vous permettent de sauvegarder différentes parties du système (système de fichiers, base de données et fichiers multimédias, par exemple) et de restaurer automatiquement les données. Un enregistrement pour chaque sauvegarde s’affiche dans la grille de la fonction _Sauvegardes_ page. La suppression d’un enregistrement de la liste supprime également le fichier archivé. Les fichiers de sauvegarde de la base sont compressés au format GZ. Pour les sauvegardes du système et de la base de données et des médias, le format TGZ est utilisé. Il est recommandé de restreindre l’accès aux outils de sauvegarde et de procéder à la sauvegarde avant d’installer les extensions et les mises à jour.

- **Limitation de l’accès aux outils de sauvegarde.** L’accès aux sauvegardes et à l’outil de gestion des restaurations peut être limité en configurant [rôles utilisateur](permissions-user-roles.md) pour les ressources de sauvegarde et de restauration. Pour restreindre l’accès, laissez la case correspondante désélectionnée. Pour donner accès aux ressources de restauration, vous devez également accorder l’accès aux ressources de sauvegarde.

- **Effectuez une sauvegarde avant d’installer des extensions et des mises à jour.** Effectuez toujours une sauvegarde avant d’installer une extension ou une mise à jour.

{{$include /help/_includes/backups-note.md}}

## Activation et planification de sauvegardes

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Backup Settings]**.

1. Définir **[!UICONTROL Enabled Schedule Backup]** to `Yes`.

1. Pour planifier des récupérations automatiques, définissez les options de planification :

   - Définir **[!UICONTROL Enabled Schedule Backup]** to `Yes`.
   - Définir **[!UICONTROL Scheduled Backup Type]** au type de sauvegarde à exécuter à l’intervalle planifié.
   - Définir **[!UICONTROL Start Time]** à l’heure de la journée pour exécuter l’opération de sauvegarde.
   - Définir **[!UICONTROL Frequency]** to `Daily`, `Weekly`, ou `Monthly`.
   - Définir **[!UICONTROL Maintenance Mode]** to `Yes`.

   ![Configuration avancée - sauvegardes](../configuration-reference/advanced/assets/system-scheduled-backup-settings.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

## Création d’une sauvegarde

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Backups]**.

1. Dans le coin supérieur droit, cliquez sur le type de sauvegarde à créer :

   - **[!UICONTROL System Backup]** - Crée une sauvegarde complète de la base de données et du système de fichiers. Au cours du processus, vous pouvez choisir d’inclure le dossier media dans la sauvegarde.

   - **[!UICONTROL Database and Media Backup]** - Crée une sauvegarde de la base de données et du dossier multimédia.

   - **[!UICONTROL Database Backup]** - Crée une sauvegarde de la base de données.

   ![Outils système - sauvegardes](./assets/tools-backups.png){width="600" zoomable="yes"}

1. Pour mettre le magasin en mode de maintenance pendant la sauvegarde, cochez la case .

   Une fois la sauvegarde terminée, le mode de maintenance est désactivé automatiquement.

1. Pour une sauvegarde du système, sélectionnez l’option **[!UICONTROL Include Media folder to System Backup]** pour inclure le dossier media.

1. Lorsque vous y êtes invité, confirmez l’action.


