---
title: Outils d’assistance
description: Découvrez les outils d’assistance fournis que vous pouvez utiliser pour identifier les problèmes de votre système.
exl-id: f67616e6-7879-4fd3-947a-16856f8447ba
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: addde8c3e41b641712f5b08107c1d68b40cd4159
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---

# Outils d’assistance

{{ee-feature}}

Les outils d’assistance sont conçus pour identifier les problèmes connus de votre système. Ils peuvent être utilisés comme ressource au cours des processus de développement et d’optimisation, et comme outil de diagnostic pour aider notre équipe d’assistance à identifier et résoudre les problèmes.

## Rapports système

L’outil de création de rapports système vous permet de créer des instantanés complets ou partiels périodiques du système et de les enregistrer pour référence ultérieure. Vous pouvez comparer les paramètres de performances avant et après les cycles de développement du code ou les modifications apportées aux paramètres du serveur. L’outil de création de rapports du système peut réduire considérablement le temps consacré à la préparation et à la soumission des informations requises par le support technique pour lancer une enquête.

Dans la grille Rapports système, vous pouvez afficher et télécharger des rapports existants, supprimer des rapports et en créer.

### Accès aux rapports système

Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.

![Administrateur - Rapports système](./assets/reports.png){width="600" zoomable="yes"}

### Générer un rapport

1. Cliquez sur **[!UICONTROL New Report]**.

1. Dans la liste **[!UICONTROL Groups]**, sélectionnez chaque ensemble d’informations à inclure dans le rapport. Par défaut, tous les groupes sont sélectionnés.

   ![Rapport système - Sélection de groupes](./assets/report-create.png){width="600" zoomable="yes"}

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Create]**.

   La génération du rapport peut prendre quelques minutes, selon le nombre de types de rapports sélectionnés. Lorsque le rapport est prêt, il s’affiche en haut de la grille avec la date et l’heure générées.

### Affichage des informations sur le module

Vous trouverez des informations utiles sur les modules installés.

**_Pour afficher les informations de rapport pour chaque module installé, procédez comme suit_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.
1. Cliquez sur **[!UICONTROL New Report]**.
1. Sélectionnez `Modules` dans la liste **[!UICONTROL Groups]**.
1. Cliquez sur **[!UICONTROL Create]**.
1. Une fois le rapport généré, cliquez sur **[!UICONTROL Select]** puis **[!UICONTROL View]** pour afficher toutes les versions de module.
1. Cliquez sur **[!UICONTROL Download]** pour télécharger le rapport.

### Gestion des rapports système

Dans la colonne **[!UICONTROL Action]** de la grille, sélectionnez l’une des options suivantes :

- `View` - Utilisez cette fonction pour afficher les détails du rapport.
- `Delete` - Utilisez cette fonction pour supprimer le rapport généré de la liste.
- `Download` - Utilisez cette fonction pour enregistrer le rapport en tant que fichier HTML.

### Affichage des détails du rapport système

1. Pour le rapport dont vous avez besoin, sélectionnez **[!UICONTROL View]** dans la colonne _[!UICONTROL Actions]_.

1. Dans le panneau de gauche, développez ![Sélecteur de développement](../assets/icon-display-expand.png) chaque section du rapport pour afficher les détails.

   ![Informations générales sur le rapport système](./assets/report-information.png){width="600" zoomable="yes"}

### Rapports système disponibles

| Groupe de rapports | Informations incluses |
| ------------ | -------------------- |
| [!UICONTROL General] | Version Adobe Commerce<br>Nombre de données<br>Statut du cache<br>Statut de l’index |
| [!UICONTROL Environment] | Informations sur l’environnement <br> statut MySQL |
| [!UICONTROL Data] | Dupliquer les catégories par clé URL<br>Dupliquer les produits par clé URL<br>Dupliquer les produits par SKU<br>Dupliquer les commandes par incrément ID<br>Dupliquer les utilisateurs par e-mail<br>Données de catégories corrompues |
| [!UICONTROL Modules] | Liste Des Modules Personnalisés<br>Liste Des Modules Désactivés<br>Liste De Tous Les Modules |
| [!UICONTROL Configuration] | Configuration<br>Données de `app/etc/env.php`<br>Modes d&#39;expédition<br>Modes de paiement<br>Matrice des fonctionnalités de paiement |
| [!UICONTROL Logs] | Fichiers journaux<br>Principaux messages système<br>Principaux messages système actuels<br>Principaux messages de débogage<br>Principaux messages de débogage d&#39;aujourd&#39;hui<br>Principaux messages d&#39;exception<br>Principaux messages d&#39;exception d&#39;aujourd&#39;hui |
| [!UICONTROL Attributes] | Attributs EAV définis par l’utilisateur<br>Nouveaux attributs EAV<br>Types d’entité<br>Tous les attributs EAV<br>Catégorie Attributs EAV<br>Produit Attributs EAV<br>Attributs EAV client<br>Adresse client Attribut EAV<br>Attributs EAV d’article RMA Attributs EAV |
| [!UICONTROL Events] | Événements globaux personnalisés<br>Événements d’administration personnalisés<br>Événements frontaux personnalisés<br>Événements de document personnalisés<br>Événements Crontab personnalisés<br>Événements REST personnalisés<br>Événements SOAP personnalisés<br>Événements globaux principaux<br>Événements d’administration principaux<br>Événements frontaux principaux<br>Événements Crontab principaux<br>Événements REST principaux<br>Événements SOAP principaux<br>Tous les événements globaux<br>Tous les événements admin<br>Tous les événements frontaux<br>Tous les événements REST<br>Tous les événements SOAP<br><br><br> Tous les événements Crontab |
| [!UICONTROL Cron] | Cron Planifie par code de statut<br>Cron Planifie par code de tâche<br>Erreurs dans la file d&#39;attente des planifications Cron<br>Liste des planifications Cron<br>Tâches Cron globales personnalisées<br>Tâches Cron configurables personnalisées<br>Tâches Cron globales principales<br>Tâches Cron configurables principales<br>Toutes les tâches Cron globales<br>Toutes les tâches Cron configurables |
| [!UICONTROL Design] | Adminhtml Themes List<br>Frontend Themes List |
| [!UICONTROL Stores] | Arborescence <br> Sites Web Liste<br>Liste De Magasins Liste <br> Vues De Magasin |
| Connecteur OMS <br>_(visible avec l’intégration OMS)_ | Version du connecteur<br>Surveillance du connecteur<br>Résultats du traitement des messages |

{style="table-layout:auto"}
