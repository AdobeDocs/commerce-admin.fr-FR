---
title: Outils d’assistance
description: Découvrez les outils d’assistance fournis que vous pouvez utiliser pour identifier les problèmes dans votre système.
exl-id: f67616e6-7879-4fd3-947a-16856f8447ba
source-git-commit: 97eeb733836f0336401664c5cfb3df2b9f2f2ccf
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# Outils d’assistance

{{ee-feature}}

Les outils d’assistance sont conçus pour identifier les problèmes connus de votre système. Ils peuvent être utilisés comme ressource au cours des processus de développement et d’optimisation, et comme outil de diagnostic pour aider notre équipe d’assistance à identifier et résoudre les problèmes.

## Collecteur de données

Le collecteur de données rassemble les informations sur votre système dont notre équipe d’assistance a besoin pour résoudre les problèmes liés à votre installation d’Adobe Commerce. La sauvegarde créée prend plusieurs minutes et comprend à la fois un vidage de code et de base de données. Les données peuvent être exportées dans un fichier CSV ou XML Excel.

![Système - Collecteur de données](./assets/data-collector.png){width="600" zoomable="yes"}

### Exécution du collecteur de données

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL New Backup]**.

   La génération de la sauvegarde prend quelques minutes. Vous pouvez surveiller les résultats du traitement en cliquant sur **[!UICONTROL Refresh Status]**. Une fois la sauvegarde terminée, elle s’affiche dans la variable _[!UICONTROL Data Collector]_grid.

1. Pour afficher un journal avec les détails de sauvegarde, procédez comme suit :

   - Dans le _[!UICONTROL Action]_colonne, sélectionnez **[!UICONTROL Show Log]**.

   - Cliquez sur **[!UICONTROL Back]** pour revenir à la grille.

   ![journal du collecteur de données](./assets/data-collector-log.png){width="600" zoomable="yes"}

### Exporter les données de sauvegarde

1. Dans la première colonne, cochez la case de la sauvegarde à exporter.

1. Utilisez la variable **[!UICONTROL Export]** pour choisir le format des données d&#39;export.

   ![Format d’exportation](./assets/data-collector-export.png){width="600" zoomable="yes"}

1. Accédez au fichier à partir de l’emplacement de téléchargement du navigateur Web et **[!UICONTROL Save]** c&#39;est le cas.

### Téléchargement des données de sauvegarde

Une fois la sauvegarde générée, vous pouvez télécharger la copie du code et des données de la base de données.

1. Recherchez l’entité de sauvegarde nécessaire dans la grille.

1. Assurez-vous qu’il comporte une `Complete` statut.

1. Cliquez sur le nom de l’entité dans _[!UICONTROL Code Dump]_ou_[!UICONTROL DB Dump]_ colonnes.

Le processus de téléchargement doit démarrer automatiquement.

## Suppression des données de sauvegarde

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. Recherchez et sélectionnez les données de sauvegarde à supprimer.

1. Dans le _[!UICONTROL Action]_colonne, cliquez sur **[!UICONTROL Delete]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

## Rapports système

L’outil de reporting du système vous permet de prendre des instantanés complets, ou partiels, périodiques du système et de les enregistrer à des fins de référence ultérieure. Vous pouvez comparer les paramètres de performances avant et après les cycles de développement du code ou les modifications apportées aux paramètres du serveur. L’outil de création de rapports du système peut réduire considérablement le temps passé à préparer et à envoyer les informations requises par l’assistance pour lancer une enquête.

Dans la grille Rapports système, vous pouvez afficher et télécharger des rapports existants, supprimer des rapports et créer des rapports.

### Accès aux rapports système

Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.

![Admin - Rapports système](./assets/reports.png){width="600" zoomable="yes"}

### Générer un rapport

1. Cliquez sur **[!UICONTROL New Report]**.

1. Dans le **[!UICONTROL Groups]** sélectionnez chaque ensemble d’informations à inclure dans le rapport. Par défaut, tous les groupes sont sélectionnés.

   ![Rapport système - sélection de groupes](./assets/report-create.png){width="600" zoomable="yes"}

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Create]**.

   La génération du rapport peut prendre quelques minutes, selon le nombre de types de rapports sélectionnés. Lorsque le rapport est prêt, il s’affiche en haut de la grille avec la date et l’heure générées.

### Affichage des informations sur le module

Vous trouverez des informations utiles sur les modules installés.

**_Pour afficher les informations de rapport pour chaque module installé :_**

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.
1. Cliquez sur **[!UICONTROL New Report]**.
1. Sélectionner `Modules` de la **[!UICONTROL Groups]** liste.
1. Cliquez sur **[!UICONTROL Create]**.
1. Une fois le rapport généré, cliquez sur **[!UICONTROL Select]** puis **[!UICONTROL View]** pour afficher toutes les versions de module.
1. Cliquez sur **[!UICONTROL Download]** pour télécharger le rapport.

### Gestion des rapports système

Dans le **[!UICONTROL Action]** de la grille, sélectionnez l’une des options suivantes :

- `View` - Utilisez cette fonction pour afficher les détails du rapport.
- `Delete` - Utilisez cette fonction pour supprimer le rapport généré de la liste.
- `Download` - Utilisez cette fonction pour enregistrer le rapport en tant que fichier de HTML.

### Affichage des détails du rapport système

1. Pour le rapport nécessaire, sélectionnez **[!UICONTROL View]** dans le _[!UICONTROL Actions]_colonne .

1. Dans le panneau de gauche, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) chaque section du rapport pour visualiser le détail.

   ![Informations générales sur les rapports du système](./assets/report-information.png){width="600" zoomable="yes"}

### Rapports système disponibles

| Groupe de rapports | Informations incluses |
| ------------ | -------------------- |
| [!UICONTROL General] | Version d’Adobe Commerce<br>Nombre de données<br>État du cache<br>État de l’index |
| [!UICONTROL Environment] | Informations sur l’environnement<br>État MySQL |
| [!UICONTROL Data] | Dupliquer les catégories par clé URL<br>Dupliquer les produits par clé URL<br>Dupliquer des produits par SKU<br>Dupliquer Les Commandes Par Identifiant D’Incrémentation<br>Duplication d’utilisateurs par courrier électronique<br>Données de catégories corrompues |
| [!UICONTROL Modules] | Liste des modules personnalisés<br>Liste des modules désactivés<br>Liste de tous les modules |
| [!UICONTROL Configuration] | Configuration<br>Données provenant de `app/etc/env.php`<br>Méthodes d’expédition<br>Méthodes de paiement<br>Matrice de fonctionnalité de paiements |
| [!UICONTROL Logs] | Fichiers journaux<br>Messages système principaux<br>Les messages système les plus courants<br>Messages de débogage principaux<br>Principaux messages de débogage actuels<br>Messages d’exception principaux<br>Les principaux messages d’exception d’aujourd’hui |
| [!UICONTROL Attributes] | Attributs EAV définis par l’utilisateur<br>Nouveaux attributs EAV<br>Types d’entité<br>Tous les attributs d’assurance qualité<br>Attributs d’expérience visuelle de catégorie<br>Attributs EAV de produit<br>Attributs du client EAV<br>Attribut EAV de l’adresse du client<br>Attributs EAV d’élément RMA |
| [!UICONTROL Events] | Événements globaux personnalisés<br>Événements d’administration personnalisés<br>Événements frontaux personnalisés<br>Événements de document personnalisés<br>Événements Crontab personnalisés<br>Événements REST personnalisés<br>Événements SOAP personnalisés<br>Principaux événements globaux<br>Événements d’administration principaux<br>Principaux événements Frontières<br>Événements de document principaux<br>Événements Core Crontab<br>Événements REST principaux<br>Événements SOAP principaux<br>Tous les événements globaux<br>Tous les événements d’administration<br>Tous les événements frontaux<br>Tous les événements de document<br>Tous les événements REST<br>Tous les événements SOAP<br>Tous les événements de type Contab |
| [!UICONTROL Cron] | Planifications cron par code d’état<br>Planifications cron par code de tâche<br>Erreurs dans la file d’attente des plannings cron<br>Liste des planifications Cron<br>Tâches Cron globales personnalisées<br>Tâches Cron Configurables Personnalisées<br>Tâches principales globales Cron<br>Tâches Cron Configurables De Base<br>Toutes les tâches Cron globales<br>Toutes les tâches Cron configurables |
| [!UICONTROL Design] | Liste des thèmes Adminhtml<br>Liste des thèmes front-end |
| [!UICONTROL Stores] | Arborescence de site Web<br>Liste des sites web<br>Liste des magasins<br>Liste des vues du magasin |
| Connecteur OMS <br>_(visible avec l’intégration OMS)_ | Version du connecteur<br>Surveillance des connecteurs<br>Résultats du traitement des messages |

{style="table-layout:auto"}
