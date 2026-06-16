---
title: Contrôles de grille d'administration
description: Découvrez comment travailler dans les pages d’administration qui gèrent les données et affichent une collection d’enregistrements dans une grille.
exl-id: a4a9531d-eb2f-41d6-bb36-dc6d8811ee95
TQID: https://experienceleague.adobe.com/-BGRS0qjthE3-oWu1DbrxeEUVk1aXdgW-RPRO1dYND0
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 519
ht-degree: 0%

---

# Contrôles de grille d&#39;administration

Les pages d’administration qui gèrent les données affichent une collection d’enregistrements dans une grille. Les commandes en haut de chaque colonne peuvent être utilisées pour trier les données. L’ordre de tri actuel est indiqué par une flèche ascendante ou descendante dans l’en-tête de colonne. Vous pouvez spécifier les colonnes à afficher dans la grille et les faire glisser vers différentes positions. Vous pouvez également enregistrer différentes dispositions de colonnes en tant que vues utilisables ultérieurement. La colonne **[!UICONTROL Action]** répertorie les opérations qui peuvent être appliquées à un enregistrement individuel. En outre, la date de l’affichage actuel de la plupart des grilles peut être exportée dans un fichier [CSV](../systems/data-csv.md) ou XML.

![Page Commandes - affichage en grille](./assets/admin-workspace-grid.png){width="700" zoomable="yes"}

## Trier la liste

1. Cliquez sur un en-tête de colonne.

   La flèche indique que l’ordre actuel est croissant ou décroissant.

1. Utilisez les commandes de pagination pour afficher des pages supplémentaires dans la collection.

   ![Affichage en grille - commandes de page](./assets/pagination-controls.png){width="300"}

## Paginer la liste

1. Définissez le contrôle **[!UICONTROL Pagination]** sur le nombre d’enregistrements que vous souhaitez afficher par page.

1. Cliquez sur **[!UICONTROL Next]** et **[!UICONTROL Previous]** pour parcourir la liste, ou saisissez une **[!UICONTROL Page Number]** spécifique.

## Filtrer la liste

1. Cliquez sur **[!UICONTROL Filters]**.

1. Renseignez autant de filtres que nécessaire pour décrire l’enregistrement que vous souhaitez rechercher.

1. Cliquez sur **[!UICONTROL Apply Filters]**.

   ![Liste des commandes - contrôles de filtre](./assets/admin-workspace-filters.png){width="700" zoomable="yes"}

## Exporter les données

1. Sélectionnez les enregistrements à exporter.

   >[!NOTE]
   >
   >Les données de produit ne peuvent pas être exportées à partir de la grille. Pour en savoir plus, voir [Exporter](../systems/data-export.md).

1. Dans le menu _Exporter_ (![Sélecteur de menu](../assets/icon-export.png)) dans le coin supérieur droit, choisissez l’un des formats de fichiers suivants :

   - `CSV`
   - `Excel XML`

   ![Liste des commandes - options d’exportation](./assets/customers-grid-export.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Export]**.

1. Recherchez le fichier téléchargé des données exportées à l’emplacement utilisé pour les téléchargements par votre navigateur.

## Disposition Grille

La sélection des colonnes et leur ordre dans la grille peuvent être modifiés selon vos préférences et enregistrés en tant que _vue_. Vous pouvez contrôler les attributs qui s’affichent dans la grille sous la configuration d’attributs individuels. De nombreux attributs affichés dans la grille de produit peuvent affecter le temps de chargement et les performances de l’administrateur.

![Colonnes de grille de commande](./assets/admin-grid-columns.png){width="700" zoomable="yes"}

### Modifier la sélection des colonnes

1. Dans le coin supérieur droit, cliquez sur le contrôle _Colonnes_ (![Contrôle Colonnes](../assets/icon-columns.png)).

1. Modifiez les sélections de colonnes :

   - Cochez la case de n’importe quelle colonne à ajouter à la grille.
   - Décochez la case de toute colonne que vous souhaitez supprimer de la grille.
   - Pour revenir à la vue de grille par défaut, cliquez sur **[!UICONTROL Reset]**.

Veillez à faire défiler l’écran vers le bas pour afficher toutes les colonnes disponibles.

### Déplacer une colonne

1. Cliquez sur l’en-tête de la colonne et maintenez la touche enfoncée.

1. Faites glisser la colonne vers sa nouvelle position et relâchez-la.

### Enregistrer une vue de grille

1. Cliquez sur le contrôle _Affichage_ (![Contrôle d&#39;affichage](../assets/icon-view-eye.png)).

1. Cliquez sur **[!UICONTROL Save Current View]**.

1. Saisissez un **[!UICONTROL name]** pour la vue.

1. Pour enregistrer toutes les modifications, cliquez sur la _Flèche_ (![&#x200B; Enregistrer toutes les modifications](../assets/icon-arrow-save.png)).

   Le nom de la vue apparaît désormais comme vue actuelle.

### Modifier l’affichage de la grille

1. Cliquez sur la commande _Affichage_ (![Icône d&#39;affichage](../assets/icon-view-eye.png)).

1. Effectuez l’une des opérations suivantes :

   - Pour utiliser une autre vue, cliquez sur son nom.
   - Pour modifier le nom d&#39;une vue, cliquez sur l&#39;icône _Modifier_ (![icône Modifier](../assets/icon-edit-pencil.png)) et mettez à jour le nom.
   - Pour supprimer une vue, cliquez sur l&#39;icône _Modifier_ (![icône Modifier](../assets/icon-edit-pencil.png)), puis sur l&#39;icône _Supprimer_ (![icône Supprimer](../assets/icon-delete-trashcan-solid.png)).
