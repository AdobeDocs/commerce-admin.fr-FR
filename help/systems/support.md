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

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL New Backup]**.

   La génération de la sauvegarde prend quelques minutes. Vous pouvez surveiller les résultats du traitement en cliquant sur **[!UICONTROL Refresh Status]**. Une fois la sauvegarde terminée, elle s’affiche dans la grille _[!UICONTROL Data Collector]_.

1. Pour afficher un journal avec les détails de sauvegarde, procédez comme suit :

   - Dans la colonne _[!UICONTROL Action]_, sélectionnez **[!UICONTROL Show Log]**.

   - Cliquez sur **[!UICONTROL Back]** pour revenir à la grille.

   ![journal du collecteur de données](./assets/data-collector-log.png){width="600" zoomable="yes"}

### Exporter les données de sauvegarde

1. Dans la première colonne, cochez la case de la sauvegarde à exporter.

1. Utilisez le menu **[!UICONTROL Export]** pour choisir le format des données d&#39;export.

   ![Format d’exportation](./assets/data-collector-export.png){width="600" zoomable="yes"}

1. Accédez au fichier à partir de l’emplacement de téléchargement du navigateur Web et **[!UICONTROL Save]**.

### Téléchargement des données de sauvegarde

Une fois la sauvegarde générée, vous pouvez télécharger la copie du code et des données de la base de données.

1. Recherchez l’entité de sauvegarde nécessaire dans la grille.

1. Assurez-vous qu’il a l’état `Complete`.

1. Cliquez sur le nom de l’entité dans les colonnes _[!UICONTROL Code Dump]_ou_[!UICONTROL DB Dump]_ .

Le processus de téléchargement doit démarrer automatiquement.

## Suppression des données de sauvegarde

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. Recherchez et sélectionnez les données de sauvegarde à supprimer.

1. Dans la colonne _[!UICONTROL Action]_, cliquez sur **[!UICONTROL Delete]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

## Rapports système

L’outil de reporting du système vous permet de prendre des instantanés complets, ou partiels, périodiques du système et de les enregistrer à des fins de référence ultérieure. Vous pouvez comparer les paramètres de performances avant et après les cycles de développement du code ou les modifications apportées aux paramètres du serveur. L’outil de création de rapports du système peut réduire considérablement le temps passé à préparer et à envoyer les informations requises par l’assistance pour lancer une enquête.

Dans la grille Rapports système, vous pouvez afficher et télécharger des rapports existants, supprimer des rapports et créer des rapports.

### Accès aux rapports système

Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.

![ Admin - Rapports système ](./assets/reports.png){width="600" zoomable="yes"}

### Générer un rapport

1. Cliquez sur **[!UICONTROL New Report]**.

1. Dans la liste **[!UICONTROL Groups]**, sélectionnez chaque ensemble d’informations à inclure dans le rapport. Par défaut, tous les groupes sont sélectionnés.

   ![Rapport système - sélectionner des groupes](./assets/report-create.png){width="600" zoomable="yes"}

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Create]**.

   La génération du rapport peut prendre quelques minutes, selon le nombre de types de rapports sélectionnés. Lorsque le rapport est prêt, il s’affiche en haut de la grille avec la date et l’heure générées.

### Affichage des informations sur le module

Vous trouverez des informations utiles sur les modules installés.

**_Pour afficher les informations de rapport pour chaque module installé :_**

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.
1. Cliquez sur **[!UICONTROL New Report]**.
1. Sélectionnez `Modules` dans la liste **[!UICONTROL Groups]**.
1. Cliquez sur **[!UICONTROL Create]**.
1. Une fois le rapport généré, cliquez sur **[!UICONTROL Select]**, puis sur **[!UICONTROL View]** pour afficher toutes les versions de module.
1. Cliquez sur **[!UICONTROL Download]** pour télécharger le rapport.

### Gestion des rapports système

Dans la colonne **[!UICONTROL Action]** de la grille, sélectionnez l’une des options suivantes :

- `View` - Utilisez cette fonction pour afficher les détails du rapport.
- `Delete` - Utilisez cette fonction pour supprimer le rapport généré de la liste.
- `Download` - Utilisez cette fonction pour enregistrer le rapport en tant que fichier d’HTML.

### Affichage des détails du rapport système

1. Pour le rapport dont vous avez besoin, sélectionnez **[!UICONTROL View]** dans la colonne _[!UICONTROL Actions]_.

1. Dans le panneau de gauche, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) de chaque section du rapport pour afficher les détails.

   ![Informations générales sur les rapports du système](./assets/report-information.png){width="600" zoomable="yes"}

### Rapports système disponibles

| Groupe de rapports | Informations incluses |
| ------------ | -------------------- |
| [!UICONTROL General] | Version d’Adobe Commerce<br>Nombre de données<br>État du cache<br>État de l’index |
| [!UICONTROL Environment] | Informations sur l’environnement <br>État de MySQL |
| [!UICONTROL Data] | Dupliquer Les Catégories Par Clé D&#39;URL<br>Dupliquer Les Produits Par Clé D&#39;URL<br>Dupliquer Les Produits Par SKU<br>Dupliquer Les Commandes Par Id D&#39;Incrémentation<br>Dupliquer Les Utilisateurs Par Email<br>Données De Catégories Corrompues |
| [!UICONTROL Modules] | Liste des modules personnalisés<br>Liste des modules désactivés<br>Liste de tous les modules |
| [!UICONTROL Configuration] | Configuration<br>Données provenant de `app/etc/env.php`<br>méthodes de livraison<br>méthodes de paiement<br>matrice des fonctionnalités de paiement |
| [!UICONTROL Logs] | Fichiers journaux<br>Principaux messages système<br>Principaux messages système du jour<br>Principaux messages de débogage<br>Principaux messages de débogage du jour<br>Principaux messages d’exception<br>Principaux messages d’exception d’aujourd’hui |
| [!UICONTROL Attributes] | Attributs EAV Définis Par L’Utilisateur<br>Nouveaux Attributs EAV<br>Types D’Entité<br>Tous Les Attributs EAV<br>Attributs EAV De Catégorie<br>Attributs EAV De Produit<br>Attributs Customer EAV<br>Attribut Customer Address EAV<br>Attribut RMA Item EAV Attributs |
| [!UICONTROL Events] | Événements globaux personnalisés<br>Événements d’administration personnalisés<br>Événements front-end personnalisés<br>Événements Doc personnalisés<br>Événements Crontab personnalisés<br>Événements SOAP personnalisés<br>Événements globaux principaux<br>Événements principaux d’administration<br>Événements principaux front-end<br>Événements principaux Doc<br>Événements principaux Crontab<br>Événements principaux<br>}Événements REST événements principaux<br>Événements principaux}}Événements principaux1}Événements principaux1}Événements principaux1}Événements principaux1}Événements de REST<br>Événements principauxÉvénements principaux2}Événements principaux1}Événements principaux1}Événements principaux2}Évén3}Tous les événements globaux<br>Tous les événements d’administration<br>Tous les événements frontend<br>Tous les événements Doc<br>Tous les événements REST<br>Tous les événements SOAP<br>Tous les événements Crontab |
| [!UICONTROL Cron] | Planifications cron par code d’état<br>Planifications cron par code de tâche<br>Erreurs dans la file d’attente des plannings cron<br>Liste des plannings cron<br>Tâches Cron globales personnalisées<br>Tâches Cron configurables personnalisées<br>Tâches Cron principales<br>Tâches Cron configurables<br>Toutes les tâches Cron globales<br> |
| [!UICONTROL Design] | Adminhtml Liste de thèmes<br>Liste de thèmes front |
| [!UICONTROL Stores] | Arborescence De Sites Web<br>Liste De Sites Web<br>Liste De Magasins<br>Liste De Vues De Magasin |
| Connecteur OMS <br>_(visible avec l’intégration OMS){1_ | Version du connecteur<br>Surveillance du connecteur<br>Résultats du traitement des messages |

{style="table-layout:auto"}
