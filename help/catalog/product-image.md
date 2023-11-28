---
title: Gestion des images et des vidéos de produit
description: Découvrez la gestion des ressources d’image et vidéo pour vos listes de produits.
exl-id: 3cb4ab8a-8966-400f-be94-a517634d1334
feature: Catalog Management, Products, Media
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1013'
ht-degree: 0%

---

# Gestion des images et des vidéos de produit

Pour chaque produit, vous pouvez télécharger plusieurs images et vidéos, réorganiser leur ordre et contrôler leur utilisation. Si vous disposez d’une grande quantité d’images à gérer, vous préférerez peut-être les importer sous la forme d’un lot plutôt que de les télécharger individuellement. Pour plus d’informations, voir [Importation d’images de produit](../systems/data-import-product-images.md).

Si vous prévoyez de télécharger des images volumineuses à afficher sur la page _[!UICONTROL Product Details]_, vous pouvez envisager de définir une taille maximale en pixels (largeur et hauteur) et de redimensionner automatiquement les fichiers au moment du téléchargement. Une option permet d’activer le redimensionnement automatique des fichiers image plus volumineux au fur et à mesure du téléchargement. Pour plus d’informations, voir [Redimensionnement des images du produit](product-image-config.md#product-image-resizing).

## Mettre à jour les images du produit

1. Ouvrez le produit en mode d’édition.

1. Pour utiliser une vue de magasin spécifique, définissez la variable **[!UICONTROL Store View]** sélectionnez la vue appropriée dans le coin supérieur gauche.

   >[!NOTE]
   >
   >Les nouvelles images de produit sont **_always_** chargé et visible dans **_all_** vues de magasin, même si la variable `All Store Views` n’est pas utilisée pour le chargement. <br/><br/>Pour masquer une image de produit d’une vue de magasin spécifique, vous devez passer à cette vue de magasin , sélectionnez la variable **[!UICONTROL Hide from Product Page]** , puis cliquez sur **[!UICONTROL Save]**.

1. Faites défiler l’écran vers le bas et développez _[!UICONTROL Images and Videos]_.

### Chargement d’une image

Pour une meilleure compatibilité, il est recommandé de télécharger toutes les images de produit avec la variable `sRGB` profil de couleurs. Tous les autres profils de couleurs sont automatiquement convertis en `sRGB` profil colorimétrique lors du chargement de l’image du produit, ce qui peut entraîner une incohérence des couleurs dans l’image chargée.

La longueur du nom du fichier image, y compris son extension, ne peut pas dépasser 90 caractères.

Pour télécharger une image, effectuez l’une des opérations suivantes :

- Faites glisser une image depuis votre bureau et déposez-la sur le _Appareil photo_ ( ![Icône Appareil photo](../assets/icon-camera.png) ) dans le _[!UICONTROL Images And Videos]_de la boîte.

- Dans le _[!UICONTROL Images And Videos]_, cliquez sur le bouton_ Appareil photo _( ![Icône Appareil photo](../assets/icon-camera.png) ), sélectionnez le fichier image sur votre ordinateur, puis cliquez sur **[!UICONTROL Open]**.

  ![Chargement ou glisser-déposer](./assets/product-images-and-video-jewel-tee.png){width="600" zoomable="yes"}

### Réorganiser les images

Pour modifier l’ordre des images dans la galerie, cliquez sur le bouton _[!UICONTROL Sort]_( ![Icône Tri](./assets/inventory-icon-sort.png) ) au bas de la mosaïque de l’image et faites glisser l’image vers un autre emplacement dans la balise_[!UICONTROL Images And Videos]_ de la boîte.

![Modifier l’ordre](./assets/product-images-and-videos-drag.png){width="600" zoomable="yes"}

### Suppression d’une image

Pour supprimer une image de la galerie, cliquez sur le bouton **[!UICONTROL Delete]** ( ![Icône Corbeille](../assets/icon-delete-trashcan.png) ) dans le coin supérieur droit de la mosaïque d’image, puis cliquez sur **[!UICONTROL Save]**.

### Définition des détails d’image

Cliquez sur l’image que vous souhaitez ouvrir en mode détaillé et effectuez l’une des opérations suivantes :

![Affichage des détails de l’image](./assets/product-image-detail-jewel-tee.png){width="600" zoomable="yes"}

Pour fermer la vue détaillée, cliquez sur le bouton _Fermer_ ( ![Icône Fermer](../assets/icon-close-x.png) ) dans le coin supérieur droit.

Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

#### Saisir du texte alternatif

Le texte de remplacement d’image est référencé par les lecteurs d’écran afin d’améliorer l’accessibilité web et par les moteurs de recherche lors de l’indexation du site. Certains navigateurs affichent le texte de remplacement à la souris. Le texte de remplacement peut contenir plusieurs mots et contenir des mots-clés soigneusement sélectionnés.

Dans le _[!UICONTROL Alt Text]_saisissez une brève description de l’image.

#### Attribution de rôles

Par défaut, tous les rôles sont affectés à la première image chargée dans le produit. Pour réaffecter un rôle à une autre image, procédez comme suit :

Dans le _[!UICONTROL Role]_, choisissez le rôle à attribuer à l’image.

Lorsque vous revenez à la variable _Images et vidéos_ , les rôles affectés actuellement apparaissent sous chaque image.

![Rôles attribués](./assets/product-images-video-swatch.png){width="600" zoomable="yes"}

#### Masquer une image

Pour exclure une image de la galerie de miniatures, sélectionnez la **[!UICONTROL Hidden]** case à cocher et clic **[!UICONTROL Save]**.

![Images masquées](./assets/product-images-and-videos-hidden.png){width="600" zoomable="yes"}

## Rôles d’image

| Rôle d’image | Description |
|--- |--- |
| [!UICONTROL Thumbnail] | Les images miniatures apparaissent dans la galerie de miniatures, dans le panier et dans certains blocs, tels que Éléments associés. Exemple de taille : 50 x 50 pixels |
| [!UICONTROL Small Image] | La petite image est utilisée pour les images de produit dans les listes sur les pages de résultats de recherche et de catégorie, ainsi que pour afficher les images de produit nécessaires aux sections telles que Valeurs incitatives, Ventes croisées et Nouvelle liste de produits. Exemple de taille : 470 x 470 pixels |
| [!UICONTROL Base Image] | L’image de base est l’image principale de la page des détails du produit. Le zoom sur l’image est activé si vous téléchargez une image plus grande que le conteneur d’images. Selon le niveau de zoom que vous souhaitez obtenir, l’image de base doit être deux ou trois fois la taille du conteneur. Exemples de tailles : 470 x 470 pixels (sans zoom), 1 100 x 1 100 pixels (avec zoom) |
| [!UICONTROL Swatch] | A [échantillon](swatches.md) peut être utilisé pour illustrer la couleur, le motif ou la texture. Exemple de taille : 50 x 50 pixels |

{style="table-layout:auto"}

## Filigranes

Si vous allez au détriment de la création de vos propres images de produit originales, il n&#39;y a pas grand chose à faire pour empêcher des concurrents sans scrupules de les voler en un clic de souris. Cependant, vous pouvez en faire une cible moins attrayante en plaçant un filigrane sur chaque image afin de les identifier comme votre propriété. Un fichier de filigrane peut être une image de JPG (JPEG), de GIF ou PNG. Les types de fichiers GIF et PNG prennent en charge les calques transparents qui peuvent être utilisés pour donner au filigrane un arrière-plan transparent.

Le filigrane utilisé pour la variable _small_ L’image dans l’exemple suivant est un logo noir avec un arrière-plan transparent et enregistré en tant que fichier PNG avec les paramètres suivants :

- Taille : 50x50
- Opacité : 5
- Position : mosaïque

![filigrane en mosaïque](./assets/storefront-watermark-tiled.png){width="700" zoomable="yes"}

### Ajout de filigranes aux images de produit

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

   Pour plus d’informations sur les configurations de conception, voir [Configuration de la conception](../content-design/configuration.md).

1. Recherchez la vue de magasin à configurer, puis cliquez sur **[!UICONTROL Edit]** dans le _[!UICONTROL Action]_colonne .

1. Sous _[!UICONTROL Other Settings]_, développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Product Image Watermarks]**.

   ![Filigranes d’image de produit - Base](./assets/config-design-product-image-watermarks-base.png){width="600" zoomable="yes"}

   La variable **[!UICONTROL Base]**, **[!UICONTROL Thumbnail]**, **[!UICONTROL Small]**, et **[!UICONTROL Swatch Image]** les paramètres d’image sont identiques.

1. Utilisez l’une des méthodes suivantes pour ajouter la ressource image de filigrane :

   - Cliquez sur **[!UICONTROL Upload]** et sélectionnez le fichier image que vous souhaitez charger pour l’utiliser comme filigrane sur votre système.
   - Cliquez sur **[!UICONTROL Select from Gallery]** et sélectionnez une ressource image dans la [Galerie de médias](../content-design/media-gallery.md).

1. Définissez les paramètres d’affichage du filigrane :

   - Saisissez le **[!UICONTROL Image Opacity]** en pourcentage. Par exemple: `40`

   - Saisissez le **[!UICONTROL Image Size]** en pixels. Par exemple: `200 x 200`

   - Définir **[!UICONTROL Image Position]** pour déterminer où le filigrane apparaît.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous y êtes invité, cliquez sur **[!UICONTROL Cache Management]** dans le message système et actualisez le cache non valide.

   ![Actualiser le cache](./assets/msg-cache-management.png){width="600" zoomable="yes"}

>[!TIP]
>
>Cliquez sur **[!UICONTROL Use Default Value]** ![Flèche de retour](../assets/icon-arrow-return.png) pour restaurer la valeur par défaut.

### Suppression d’un filigrane

1. Dans le coin inférieur gauche de l’image, cliquez sur le bouton **[!UICONTROL Delete]** ( ![Icône Corbeille](../assets/icon-delete-trashcan-solid.png) ).

   ![Supprimer le filigrane](./assets/product-image-watermark-delete.png){width="300"}

1. Cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous y êtes invité, cliquez sur **[!UICONTROL Cache Management]** dans le message système et actualisez le cache non valide.

   Si l’image de filigrane persiste dans le storefront, revenez à la gestion du cache et cliquez sur **[!UICONTROL Flush Magento Cache]**.
