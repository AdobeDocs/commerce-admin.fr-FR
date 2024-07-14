---
title: Gestion des ressources de la galerie multimédia
description: Découvrez comment gérer les fichiers multimédias chargés et les ressources que vous acquérez par le biais d’une intégration Adobe Stock.
exl-id: 4fc489ae-b1e5-4aa4-832d-cd88c58d103a
feature: Page Content, Media
source-git-commit: a93e96353f4be0e771064cdcfbdf794772386a28
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# Gestion des ressources de la galerie multimédia

La nouvelle [galerie de médias](media-gallery.md) fournit des outils pour gérer les fichiers multimédias téléchargés et les ressources que vous acquérez par le biais d’une [intégration Adobe Stock](adobe-stock.md). Si vous avez enregistré un [aperçu d’image](adobe-stock-save-preview.md) Adobe Stock, vous pouvez également [obtenir une licence](adobe-stock-license-image.md) de l’image dans la nouvelle galerie de médias.

## Chargement d’une ressource

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Cliquez sur **[!UICONTROL Upload Image]**.

1. Sélectionnez le fichier à charger.

   La ressource sélectionnée est automatiquement téléchargée vers le dossier sélectionné (ou vers la racine de stockage si aucun dossier n’est sélectionné).

## Affichage des détails de la ressource

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Cliquez sur les trois points sous la ressource (![Icône Détails](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}), puis cliquez sur **[!UICONTROL View Details]**.

   ![Actions de ressources](./assets/media-gallery-asset-actions.png){width="600" zoomable="yes"}

   Les détails de la ressource s’affichent dans le panneau des diapositives. Ils incluent les informations sur l’emplacement d’utilisation de la ressource :

   - **[!UICONTROL Categories]**
   - **[!UICONTROL Products]**
   - **[!UICONTROL Pages]**
   - **[!UICONTROL Blocks]**

   ![Détails de la ressource](./assets/media-gallery-asset-details.png){width="600" zoomable="yes"}

   Pour afficher les détails, cliquez sur les liens **[!UICONTROL Used In]** . La grille de l’exemple suivant affiche toutes les catégories dans lesquelles une ressource spécifique est utilisée.

   ![Grille de catégorie](./assets/media-gallery-asset-categories.png){width="600" zoomable="yes"}

   Il est également possible de supprimer la ressource de la section _Afficher les détails_.

## Modification d’une ressource

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Cliquez sur les trois points sous la ressource (![Icône de menu Ressource](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}), puis cliquez sur **[!UICONTROL Edit]**.

   ![Modifier la ressource](./assets/media-gallery-edit-asset.png){width="600" zoomable="yes"}

1. Si nécessaire, modifiez l’une des valeurs de métadonnées suivantes :

   - **[!UICONTROL Title]**
   - **[!UICONTROL Description]**
   - **[!UICONTROL Tags/Keywords]**

   Ces données sont enregistrées dans la base de données et dans les métadonnées du fichier. Actuellement, les formats XMP et IPTC sont pris en charge.

   Vous pouvez télécharger l’image avec les métadonnées mises à jour.

## Utilisation d’une ressource

Assets peut être largement utilisé dans l’ensemble de l’administrateur, par exemple [ajouter ou modifier une page](page-add.md), [créer ou modifier une catégorie](../catalog/category-create.md) ou [insérer des images depuis l’éditeur de contenu](editor-insert-image.md).

1. Accédez à la nouvelle galerie de médias à partir d’une zone qui vous permet d’utiliser des ressources multimédia.

1. Sélectionnez la ressource et cliquez sur **[!UICONTROL Add Selected]**.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}

## Suppression de ressources

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Cliquez sur **[!UICONTROL Delete Images...]** et cochez la case pour chaque ressource à supprimer.

1. Dans la boîte de dialogue de confirmation, cliquez sur **[!UICONTROL Delete Image]**.

   ![Confirmation de suppression](./assets/media-gallery-bulk-delete-confirm.png){width="500" zoomable="yes"}

## Recherche de ressources

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Utilisez l’entrée **[!UICONTROL Search by keywords]** pour effectuer une recherche d’image par mots-clés/balises.

   La recherche dans l’exemple suivant trouve les ressources qui contiennent une balise spécifique (`mountain`).

   ![Recherche de ressources](./assets/media-gallery-asset-search.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Pour savoir comment mettre à jour les balises d’image, reportez-vous à la section _[Modification d’une ressource](#edit-an-asset)_ .

## Filtrage des ressources

>[!NOTE]
>
>La fonctionnalité _Utilisée dans_ nécessite que [!UICONTROL Media Gallery Image Optimization] soit activé dans les [paramètres de configuration](media-gallery-image-optimization.md).

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Cliquez sur l’onglet **[!UICONTROL Filters]** .

   ![Filtres](./assets/media-gallery-filters.png){width="600" zoomable="yes"}

1. Définissez les options de filtrage.

   Vous pouvez filtrer les ressources en fonction de leur utilisation par les entités :

   - **[!UICONTROL Used in Categories]**
   - **[!UICONTROL Used in Products]**
   - **[!UICONTROL Used in Pages]**
   - **[!UICONTROL Used in Blocks]**

   Vous pouvez également filtrer les ressources par **[!UICONTROL Store View]**, **[!UICONTROL License Status]** et **[!UICONTROL Content Status]**. Définissez une plage de dates pour **[!UICONTROL Uploaded Date]** et/ou **[!UICONTROL Modification Date]** afin de filtrer les ressources en fonction des dates du fichier.

1. Cliquez sur **[!UICONTROL Apply Filters]** pour afficher les résultats.

   Le filtrage dans l’exemple suivant trouve les ressources utilisées dans une catégorie spécifique (`cars`) et qui sont activées.

   ![Filtre pour Assets activé par catégorie](./assets/media-gallery-filter-by-category.png){width="600" zoomable="yes"}

## Recherche de doublons d’image

1. Cliquez sur l’onglet **[!UICONTROL Filters]** et cochez la case **[!UICONTROL Show duplicates]** .

1. Pour afficher les résultats, cliquez sur **[!UICONTROL Apply Filters]**.
