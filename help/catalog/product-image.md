---
title: Gestion des images et des vidéos de produit
description: Découvrez la gestion des ressources d’image et vidéo pour vos listes de produits.
exl-id: 3cb4ab8a-8966-400f-be94-a517634d1334
feature: Catalog Management, Products, Media
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# Gestion des images et des vidéos de produit

Pour chaque produit, vous pouvez télécharger plusieurs images et vidéos, réorganiser leur ordre et contrôler leur utilisation. Si vous disposez d’une grande quantité d’images à gérer, vous préférerez peut-être les importer sous la forme d’un lot plutôt que de les télécharger individuellement. Pour plus d’informations, voir [Importer des images de produit](../systems/data-import-product-images.md).

Si vous prévoyez de télécharger des images volumineuses pour affichage sur la page _[!UICONTROL Product Details]_, vous pouvez définir une taille maximale en pixels (largeur et hauteur) et redimensionner automatiquement les fichiers lors du téléchargement. Une option permet d’activer le redimensionnement automatique des fichiers image plus volumineux au fur et à mesure du téléchargement. Pour plus d’informations, voir [Redimensionnement d’image de produit](product-image-config.md#product-image-resizing).

## Mettre à jour les images du produit

1. Ouvrez le produit en mode d’édition.

1. Pour utiliser une vue de magasin spécifique, définissez le programme de sélection **[!UICONTROL Store View]** dans le coin supérieur gauche sur la vue applicable.

   >[!NOTE]
   >
   >Les nouvelles images de produit sont **_toujours_** chargées et visibles dans toutes les **_vues de magasin, même si la portée `All Store Views` n’est pas utilisée pour le transfert._** <br/><br/>Pour masquer une image de produit d’une vue de magasin spécifique, vous devez passer à cette vue de magasin , cocher la case **[!UICONTROL Hide from Product Page]** de l’image et cliquer sur **[!UICONTROL Save]**.

1. Faites défiler l’écran vers le bas et développez la section _[!UICONTROL Images and Videos]_.

### Chargement d’une image

Pour une meilleure compatibilité, il est recommandé de télécharger toutes les images de produit avec le profil colorimétrique `sRGB`. Tous les autres profils colorimétriques sont automatiquement convertis dans le profil colorimétrique `sRGB` lors du chargement de l’image du produit, ce qui peut entraîner une incohérence des couleurs dans l’image chargée.

La longueur du nom du fichier image, y compris son extension, ne peut pas dépasser 90 caractères.

Pour télécharger une image, effectuez l’une des opérations suivantes :

- Faites glisser une image de votre bureau et déposez-la sur la mosaïque _Caméra_ ( ![Icône de caméra](../assets/icon-camera.png) ) dans la zone _[!UICONTROL Images And Videos]_.

- Dans la zone _[!UICONTROL Images And Videos]_, cliquez sur la mosaïque_ Appareil photo _( ![Icône Appareil photo](../assets/icon-camera.png) ), sélectionnez le fichier image sur votre ordinateur, puis cliquez sur **[!UICONTROL Open]**.

  ![Télécharger ou faire glisser et déposer](./assets/product-images-and-video-jewel-tee.png){width="600" zoomable="yes"}

### Réorganiser les images

Pour modifier l’ordre des images dans la galerie, cliquez sur l’icône _[!UICONTROL Sort]_( ![Icône Trier](./assets/inventory-icon-sort.png) ) au bas de la mosaïque de l’image et faites glisser l’image vers une autre position dans la zone_[!UICONTROL Images And Videos]_.

![Modifier l’ordre](./assets/product-images-and-videos-drag.png){width="600" zoomable="yes"}

### Suppression d’une image

Pour supprimer une image de la galerie, cliquez sur l’icône **[!UICONTROL Delete]** ( ![Icône Corbeille](../assets/icon-delete-trashcan.png) ) dans le coin supérieur droit de la mosaïque de l’image, puis cliquez sur **[!UICONTROL Save]**.

### Définition des détails d’image

Cliquez sur l’image que vous souhaitez ouvrir en mode détaillé et effectuez l’une des opérations suivantes :

![Affichage des détails de l’image](./assets/product-image-detail-jewel-tee.png){width="600" zoomable="yes"}

Pour fermer la vue détaillée, cliquez sur l’icône _Fermer_ ( ![Icône Fermer](../assets/icon-close-x.png) ) dans le coin supérieur droit.

Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

#### Saisir du texte alternatif

Le texte de remplacement d’image est référencé par les lecteurs d’écran afin d’améliorer l’accessibilité web et par les moteurs de recherche lors de l’indexation du site. Certains navigateurs affichent le texte de remplacement à la souris. Le texte de remplacement peut contenir plusieurs mots et contenir des mots-clés soigneusement sélectionnés.

Dans la zone _[!UICONTROL Alt Text]_, saisissez une brève description de l’image.

#### Attribution de rôles

Par défaut, tous les rôles sont affectés à la première image chargée dans le produit. Pour réaffecter un rôle à une autre image, procédez comme suit :

Dans la zone _[!UICONTROL Role]_, sélectionnez le rôle que vous souhaitez affecter à l’image.

Lorsque vous revenez à la section _Images et vidéos_ , les rôles actuellement affectés apparaissent sous chaque image.

![Rôles attribués](./assets/product-images-video-swatch.png){width="600" zoomable="yes"}

#### Masquer une image

Pour exclure une image de la galerie de miniatures, cochez la case **[!UICONTROL Hidden]** et cliquez sur **[!UICONTROL Save]**.

![Images masquées](./assets/product-images-and-videos-hidden.png){width="600" zoomable="yes"}

## Rôles d’image

| Rôle d’image | Description |
|--- |--- |
| [!UICONTROL Thumbnail] | Les images miniatures apparaissent dans la galerie de miniatures, dans le panier et dans certains blocs, tels que Éléments associés. Exemple de taille : 50 x 50 pixels |
| [!UICONTROL Small Image] | La petite image est utilisée pour les images de produit dans les listes sur les pages de résultats de recherche et de catégorie, ainsi que pour afficher les images de produit nécessaires aux sections telles que Valeurs incitatives, Ventes croisées et Nouvelle liste de produits. Exemple de taille : 470 x 470 pixels |
| [!UICONTROL Base Image] | L’image de base est l’image principale de la page des détails du produit. Le zoom sur l’image est activé si vous téléchargez une image plus grande que le conteneur d’images. Selon le niveau de zoom que vous souhaitez obtenir, l’image de base doit être deux ou trois fois la taille du conteneur. Exemples de tailles : 470 x 470 pixels (sans zoom), 1 100 x 1 100 pixels (avec zoom) |
| [!UICONTROL Swatch] | Un [échantillon](swatches.md) peut être utilisé pour illustrer la couleur, le motif ou la texture. Exemple de taille : 50 x 50 pixels |

{style="table-layout:auto"}

## Filigranes

Si vous allez au détriment de la création de vos propres images de produit originales, il n&#39;y a pas grand chose à faire pour empêcher des concurrents sans scrupules de les voler en un clic de souris. Cependant, vous pouvez en faire une cible moins attrayante en plaçant un filigrane sur chaque image afin de les identifier comme votre propriété. Un fichier de filigrane peut être une image de JPG (JPEG), de GIF ou PNG. Les types de fichiers GIF et PNG prennent en charge les calques transparents qui peuvent être utilisés pour donner au filigrane un arrière-plan transparent.

Le filigrane utilisé pour l’image _small_ dans l’exemple suivant est un logo noir avec un arrière-plan transparent et enregistré en tant que fichier PNG avec les paramètres suivants :

- Taille : 50x50
- Opacité : 5
- Position : mosaïque

![filigrane en mosaïque](./assets/storefront-watermark-tiled.png){width="700" zoomable="yes"}

### Ajout de filigranes aux images de produit

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

   Pour plus d’informations sur les configurations de conception, voir [Configuration de conception](../content-design/configuration.md).

1. Recherchez la vue de magasin que vous souhaitez configurer et cliquez sur **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_.

1. Sous _[!UICONTROL Other Settings]_, développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Product Image Watermarks]**.

   ![Filigranes d’image du produit - Base](./assets/config-design-product-image-watermarks-base.png){width="600" zoomable="yes"}

   Les paramètres d’image **[!UICONTROL Base]**, **[!UICONTROL Thumbnail]**, **[!UICONTROL Small]** et **[!UICONTROL Swatch Image]** sont identiques.

1. Utilisez l’une des méthodes suivantes pour ajouter la ressource image de filigrane :

   - Cliquez sur **[!UICONTROL Upload]** et sélectionnez sur votre système le fichier image que vous souhaitez charger pour l’utiliser comme filigrane.
   - Cliquez sur **[!UICONTROL Select from Gallery]** et sélectionnez une ressource image dans la [galerie de médias](../content-design/media-gallery.md).

1. Définissez les paramètres d’affichage du filigrane :

   - Saisissez le **[!UICONTROL Image Opacity]** en pourcentage. Par exemple : `40`

   - Saisissez le **[!UICONTROL Image Size]** en pixels. Par exemple : `200 x 200`

   - Définissez **[!UICONTROL Image Position]** pour déterminer l’emplacement du filigrane.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous êtes invité à actualiser le cache, cliquez sur **[!UICONTROL Cache Management]** dans le message système et actualisez le cache non valide.

   ![Actualiser le cache](./assets/msg-cache-management.png){width="600" zoomable="yes"}

>[!TIP]
>
>Vous pouvez cliquer sur **[!UICONTROL Use Default Value]** ![Flèche de retour](../assets/icon-arrow-return.png) pour restaurer la valeur par défaut.

### Suppression d’un filigrane

1. Dans le coin inférieur gauche de l’image, cliquez sur l’icône **[!UICONTROL Delete]** ( ![Icône Corbeille](../assets/icon-delete-trashcan-solid.png) ).

   ![Supprimer le filigrane](./assets/product-image-watermark-delete.png){width="300"}

1. Cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous êtes invité à actualiser le cache, cliquez sur **[!UICONTROL Cache Management]** dans le message système et actualisez le cache non valide.

   Si l’image de filigrane persiste dans le storefront, revenez à la gestion du cache et cliquez sur **[!UICONTROL Flush Magento Cache]**.
