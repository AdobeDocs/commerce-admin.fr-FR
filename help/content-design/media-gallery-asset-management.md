---
title: Gestion des ressources de Media Gallery
description: Découvrez comment gérer les fichiers multimédias chargés et les ressources que vous acquérez par le biais d’une intégration Adobe Stock.
exl-id: 4fc489ae-b1e5-4aa4-832d-cd88c58d103a
feature: Page Content, Media
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# Gestion des ressources de Media Gallery

La nouvelle [Galerie de médias](media-gallery.md) fournit des outils pour gérer les fichiers multimédias chargés et les ressources que vous acquérez par le biais d’une intégration [Adobe Stock](adobe-stock.md). Si vous avez enregistré une image Adobe Stock [aperçu de l’image](adobe-stock-save-preview.md), vous pouvez également [obtenir la licence](adobe-stock-license-image.md) l’image dans la nouvelle galerie de médias.

## Chargement d’un élément

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Cliquez sur **[!UICONTROL Upload Image]**.

1. Sélectionnez le fichier à charger.

   La ressource sélectionnée est automatiquement chargée dans le dossier sélectionné (ou à la racine de stockage si aucun dossier n’est sélectionné).

## Affichage des détails de la ressource

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Cliquez sur les trois points situés sous la ressource (![icône Détails](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}), puis sur **[!UICONTROL View Details]**.

   ![Actions sur les ressources](./assets/media-gallery-asset-actions.png){width="600" zoomable="yes"}

   Les détails de la ressource s’affichent dans un panneau de diapositives. Ils incluent les informations sur l’emplacement où la ressource est utilisée :

   - **[!UICONTROL Categories]**
   - **[!UICONTROL Products]**
   - **[!UICONTROL Pages]**
   - **[!UICONTROL Blocks]**

   ![Détails de la ressource](./assets/media-gallery-asset-details.png){width="600" zoomable="yes"}

   Pour afficher les détails, cliquez sur les liens **[!UICONTROL Used In]** . La grille de l’exemple suivant affiche toutes les catégories dans lesquelles une ressource spécifique est utilisée.

   ![Grille des catégories](./assets/media-gallery-asset-categories.png){width="600" zoomable="yes"}

   Il est également possible de supprimer la ressource de la section _Afficher les détails_.

## Modification d’un élément

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Cliquez sur les trois points situés sous la ressource (![icône du menu Ressource](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}), puis cliquez sur **[!UICONTROL Edit]**.

   ![Modifier la ressource](./assets/media-gallery-edit-asset.png){width="600" zoomable="yes"}

1. Si nécessaire, modifiez l’une des valeurs de métadonnées suivantes :

   - **[!UICONTROL Title]**
   - **[!UICONTROL Description]**
   - **[!UICONTROL Tags/Keywords]**

   Ces données sont enregistrées dans la base de données et dans les métadonnées du fichier lui-même. Actuellement, les formats XMP et IPTC sont pris en charge.

   Vous pouvez télécharger l’image avec les métadonnées mises à jour.

## Utilisation d’une ressource

Assets peut être largement utilisé dans l’ensemble de l’administration, par exemple [ajouter ou modifier une page](page-add.md), [créer ou modifier une catégorie](../catalog/category-create.md) ou [insérer des images à partir de l’éditeur de contenu](editor-insert-image.md).

1. Accédez à la nouvelle Galerie de médias à partir d’une zone qui vous permet d’utiliser des ressources multimédias.

1. Sélectionnez la ressource et cliquez sur **[!UICONTROL Add Selected]**.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}

## Suppression de ressources

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Cliquez sur **[!UICONTROL Delete Images...]** et cochez la case correspondant à chaque ressource à supprimer.

1. Dans la boîte de dialogue de confirmation, cliquez sur **[!UICONTROL Delete Image]**.

   ![Confirmation de suppression](./assets/media-gallery-bulk-delete-confirm.png){width="500" zoomable="yes"}

## Recherche de ressources

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Utilisez l’entrée **[!UICONTROL Search by keywords]** pour rechercher des images par mots-clés/balises.

   La recherche dans l’exemple suivant permet de trouver les ressources qui contiennent une balise spécifique (`mountain`).

   ![Recherche de ressources](./assets/media-gallery-asset-search.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Pour découvrir comment mettre à jour les balises d’image, consultez la section _[Modification d’une ressource](#edit-an-asset)_.

## Filtrage des ressources

>[!NOTE]
>
>La fonctionnalité _Utilisé dans_ nécessite que [!UICONTROL Media Gallery Image Optimization] soit activé dans les [paramètres de configuration](media-gallery-image-optimization.md).

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Cliquez sur l’onglet **[!UICONTROL Filters]** .

   ![&#x200B; Filtres &#x200B;](./assets/media-gallery-filters.png){width="600" zoomable="yes"}

1. Définissez les options de filtrage.

   Vous pouvez filtrer les ressources en fonction de l’utilisation par les entités :

   - **[!UICONTROL Used in Categories]**
   - **[!UICONTROL Used in Products]**
   - **[!UICONTROL Used in Pages]**
   - **[!UICONTROL Used in Blocks]**

   Vous pouvez également filtrer les ressources par **[!UICONTROL Store View]**, **[!UICONTROL License Status]** et **[!UICONTROL Content Status]**. Définissez une période pour **[!UICONTROL Uploaded Date]** et/ou **[!UICONTROL Modification Date]** afin de filtrer les ressources en fonction des dates de fichier.

1. Cliquez sur **[!UICONTROL Apply Filters]** pour afficher les résultats.

   Le filtrage de l’exemple suivant recherche les ressources utilisées dans une catégorie spécifique (`cars`) et activées.

   ![Filtrer les Assets activées par catégorie](./assets/media-gallery-filter-by-category.png){width="600" zoomable="yes"}

## Rechercher les doublons d&#39;images

1. Cliquez sur l’onglet **[!UICONTROL Filters]** et cochez la case **[!UICONTROL Show duplicates]** .

1. Pour afficher les résultats, cliquez sur **[!UICONTROL Apply Filters]**.

<!-- Last updated from includes: 2024-01-30 15:43:39 -->
