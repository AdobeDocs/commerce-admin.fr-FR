---
title: Media - Image
description: En savoir plus sur le type de contenu Image , utilisé pour ajouter une image de JPG, de GIF ou PNG à la variable [!DNL Page Builder] scène.
exl-id: 1b8d906e-7570-4c1f-87a0-992400faf55c
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1551'
ht-degree: 0%

---

# Media - Image

Utilisez la variable _Image_ type de contenu pour ajouter une image de JPG, de GIF ou PNG à la variable [[!DNL Page Builder] étape](workspace.md#stage). Outre l’image de bureau par défaut, vous pouvez spécifier une image secondaire pour les appareils mobiles. Vous pouvez également ajouter une légende qui s’affiche sous l’image et associer l’image à n’importe quelle URL, produit, catégorie ou page.

>[!TIP]
>
>Vous pouvez utiliser la variable [Intégration Adobe Stock](../content-design/adobe-stock.md) pour rechercher et enregistrer une ressource appropriée parmi les millions fournis par [Adobe Stock](https://stock.adobe.com). Voir [Utilisation d’images Adobe Stock](../content-design/adobe-stock-manage.md) pour plus d’informations sur la recherche, l’affinage et l’enregistrement de ressources Adobe Stock dans votre galerie.

{{$include /help/_includes/page-builder-save-timeout.md}}

## Zone d’outils Image

La boîte à outils d’image s’affiche lorsque vous placez le pointeur de la souris sur le conteneur d’images.

![Zone d’outils Image](./assets/pb-media-image-giftcard-column-toolbox.png){width="500" zoomable="yes"}

| Outil | Icône | Description |
|--- |--- |--- |
| Déplacer | ![Icône Déplacer](./assets/pb-icon-move.png){width="25"} | Déplace l’image vers une autre position sur la scène. |
| (label) | Image | Identifie le conteneur de contenu actuel en tant qu’image. Passez la souris sur le conteneur d’images pour afficher la boîte à outils. |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} | Ouvre la _Modifier l’image_ dans laquelle vous pouvez modifier les propriétés de l’image et du conteneur. |
| Masquer | ![Icône Masquer](./assets/pb-icon-hide.png){width="25"} | Masque l’image active. |
| Afficher | ![Icône Afficher](./assets/pb-icon-show.png){width="25"} | Affiche l’image masquée. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="25"} | Effectue une copie de l’image. |
| Supprimer | ![Icône Supprimer](./assets/pb-icon-remove.png){width="25"} | Supprime l’image de la scène. |
| Charger une nouvelle image |  | Télécharge une image de votre système de fichiers local vers la galerie. |
| Sélectionner dans la galerie |  | Choisit une image existante dans la galerie. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Ajout d’une image

1. Dans le [!DNL Page Builder] panneau, développer **[!UICONTROL Media]** et faites glisser un **[!UICONTROL Image]** balise d’emplacement du conteneur cible.

   Vous pouvez ajouter une image à une ligne, une colonne ou un onglet. Dans l’exemple suivant, l’image est glissée sur une colonne vide.

   ![Faire glisser un type de contenu d’image sur la scène](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

1. Utilisez l’une des méthodes suivantes pour ajouter la ressource image :

   ![Télécharger l’image ou effectuer une sélection à partir des outils de galerie sur l’étape](./assets/pb-media-image-upload-select.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >La taille de fichier maximale est de 4 Mo. Les types de fichiers pris en charge sont JPG, GIF et PNG.

   - _**Charger une nouvelle image**_: utilisez cette méthode pour charger un nouveau fichier image à partir de votre système.

      - Cliquez sur **[!UICONTROL Upload Image]**.

      - Recherchez et sélectionnez l’image à ajouter à la galerie et au conteneur cible.

     Vous pouvez également faire glisser un fichier image de votre système et le déposer sur le _Appareil photo_ ( ![Icône Appareil photo](./assets/pb-icon-camera.png){width="20"} ).

   - _**Sélectionner une ressource existante**_: utilisez cette méthode pour sélectionner une ressource image existante dans le stockage/la galerie multimédia.

      - Cliquez sur **[!UICONTROL Select from Gallery]**.

      - Utilisez l’arborescence pour accéder à l’image.

      - Cliquez sur la miniature, puis sur **[!UICONTROL Add Selected]**.

        ![Ajouter une image sélectionnée](./assets/pb-media-image-gallery-add-selected.png){width="600" zoomable="yes"}

   - _**Rechercher et sélectionner une image Adobe Stock**_: utilisez cette méthode pour trouver une image à partir d’Adobe Stock.

     >[!NOTE]
     >
     >Cette méthode requiert une [Intégration d’Adobe Stock](../content-design/adobe-stock.md) configuré pour votre administrateur.

      - Cliquez sur **[!UICONTROL Search Adobe Stock]** et recherchez une image.

      - Enregistrez l’aperçu ou l’image sous licence dans la galerie.

        Voir [Utilisation d’images Adobe Stock](../content-design/adobe-stock-manage.md) pour plus d’informations sur l’utilisation des ressources Adobe Stock.

      - Sélectionnez la miniature de la ressource dans la galerie, puis cliquez sur **[!UICONTROL Add Selected]**.

   L’image apparaît dans le conteneur cible à l’emplacement de l’espace réservé. Contrairement à une image d’arrière-plan, vous pouvez déplacer l’image vers une autre position dans le conteneur actif ou vers un autre conteneur.

   >[!NOTE]
   >
   >La variable [Bannière](banner.md) et [Curseur](slider.md) les types de contenu incluent également : _Télécharger l’image_ et _Sélectionner dans la galerie_ pour ajouter des images.

   ![Image dans une colonne](./assets/pb-media-image-column1-giftcard.png){width="500" zoomable="yes"}

## Modification des paramètres d’image

1. Passez la souris sur le conteneur d’images pour afficher la zone d’outils et sélectionnez l’option _Paramètres_ (![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).
Le nom, les dimensions et la taille du fichier apparaissent sous l’image active.

   ![Image actuelle](./assets/pb-media-image-settings-image.png){width="600" zoomable="yes"}

1. Pour modifier la **[!UICONTROL Image]**, effectuez l’une des opérations suivantes :

   - _**Charger une nouvelle image**_: utilisez cette méthode pour charger un nouveau fichier image à partir de votre système.

      - Cliquez sur **[!UICONTROL Upload Image]**.

      - Recherchez et sélectionnez l’image à ajouter à la galerie et au conteneur cible.

   - _**Sélectionner une ressource existante**_: utilisez cette méthode pour sélectionner une ressource image existante dans le stockage/la galerie multimédia.

      - Cliquez sur **[!UICONTROL Select from Gallery]**.

      - Utilisez l’arborescence pour accéder à l’image.

      - Cliquez sur la miniature, puis sur **[!UICONTROL Add Selected]**.

        ![Ajouter une image sélectionnée](./assets/pb-media-image-gallery-add-selected.png){width="600" zoomable="yes"}

   - **Rechercher et sélectionner une image Adobe Stock**: utilisez cette méthode pour trouver une image à partir d’Adobe Stock.

     >[!NOTE]
     >
     >Cette méthode requiert une [Intégration d’Adobe Stock](../content-design/adobe-stock.md) configuré pour votre administrateur.

      - Cliquez sur **[!UICONTROL Search Adobe Stock]** et recherchez une image.

      - Enregistrez l’aperçu ou l’image sous licence dans la galerie.

        Voir [Utilisation d’images Adobe Stock](../content-design/adobe-stock-manage.md) pour plus d’informations sur l’utilisation des ressources Adobe Stock.

      - Sélectionnez la miniature de la ressource dans la galerie, puis cliquez sur **[!UICONTROL Add Selected]**.

1. Pour ajouter une **[!UICONTROL Mobile Image]**, utilisez les mêmes méthodes que celles décrites à l’étape précédente pour sélectionner une image à utiliser pour l’affichage sur les appareils mobiles.

   ![Image mobile](./assets/pb-media-image-settings-mobile-image.png){width="600" zoomable="yes"}

1. Si nécessaire, indiquez une **[!UICONTROL Link]** pour l’image.

   Le lien est la page de destination qui s’affiche lorsque le client clique sur l’image. Vous pouvez utiliser l’un des trois types de liens suivants :

   - **[!UICONTROL URL]** - Liens vers une URL relative ou complète.

   - **[!UICONTROL Product]** - Identifie la page de destination en fonction du nom du produit ou du SKU. Recherchez le produit par nom en fonction d’un nom partiel ou complet. Sélectionnez le produit dans la liste des résultats de recherche.

     ![Choix d’un produit à lier](./assets/pb-media-image-settings-image-link-product-results.png){width="600" zoomable="yes"}

   - **[!UICONTROL Category]** - Identifie la page de destination en tant que catégorie ou sous-catégorie spécifique dans l’arborescence des catégories. Recherchez la catégorie selon un nom partiel ou complet. Sélectionnez la catégorie dans la section développée de l&#39;arborescence affichée.

     ![Choix d’une catégorie à lier](./assets/pb-media-image-settings-image-link-category-tree.png){width="600" zoomable="yes"}

   - **[!UICONTROL Page]** - Identifie la page de destination en tant que page de contenu spécifique. Recherchez la page en fonction d’un nom partiel ou complet. Sélectionnez la page dans la liste des résultats de recherche.

     ![Choix d’une page à lier](./assets/pb-media-image-settings-image-link-page-results.png){width="600" zoomable="yes"}

   Si vous souhaitez empêcher le visiteur de quitter votre boutique, sélectionnez la variable **[!UICONTROL Open in new tab]** . Lorsque la case à cocher est décochée, la destination liée s’ouvre dans le même onglet du navigateur, ce qui peut permettre de faire quitter votre boutique au visiteur.

1. Pour ajouter une **[!UICONTROL Image Caption]**, saisissez le texte à afficher sous l’image.

   Le format de la légende est déterminé par la feuille de style associée au thème actif.

   La légende apparaît généralement sous l’image et fournit des informations sur l’image aux visiteurs et aux moteurs de recherche. Si votre site est disponible en plusieurs langues, vous pouvez utiliser la même image, mais traduire la légende. Par HTML, la variable `<figcaption>` est un sous-ensemble de la balise `<figure>` balise . `<figcaption>This is the image caption</figcaption>`

1. Mettez à jour les autres paramètres si nécessaire :

   - [Optimisation du moteur de recherche](#search-engine-optimization)
   - [Avancé](#advanced)

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir au [!DNL Page Builder] workspace.

## Déplacer une image

1. Passez la souris sur le conteneur d’images pour afficher la boîte à outils et sélectionnez l’option _Déplacer_ (![Icône Déplacer](./assets/pb-icon-move.png){width="20"} ).

   ![Déplacement d’une image](./assets/pb-media-image-column1-move-giftcard.png){width="500" zoomable="yes"}

1. Sélectionnez l’image et faites-la glisser jusqu’à sa nouvelle position, juste en dessous de la ligne directrice rouge.

   ![Utilisation de la ligne guide rouge pour positionner l’image](./assets/pb-media-image-column2-move-giftcard-red-guideline.png){width="500" zoomable="yes"}

## Supprimer une image

1. Passez la souris sur le conteneur d’images pour afficher la boîte à outils et sélectionnez l’option _Supprimer_ ( ![Icône Supprimer](./assets/pb-icon-remove.png){width="20"} ).

1. Lorsque vous y êtes invité, cliquez sur **[!UICONTROL OK]**.

## Optimisation du moteur de recherche

Le texte de ces paramètres est visible par les moteurs de recherche et améliore la manière dont la page est indexée.

- Pour **[!UICONTROL Alternative Text]**, saisissez une _alt_ description textuelle des outils d’accessibilité numérique à afficher.

  L’utilisation de texte de remplacement est une bonne pratique en matière d’accessibilité. Elle est requise par la loi dans certains paramètres régionaux. Par HTML, la variable `alt` est un sous-ensemble de la propriété `image` tag : `<image title="tooltip" alt="description" src="image.jpg">`.

- Pour **[!UICONTROL Title Attribute]**, saisissez le texte à afficher sous forme d’info-bulle lorsque vous pointez dessus.

  Il est recommandé de choisir un titre descriptif et riche en mots-clés afin d’améliorer l’indexation de l’image par les moteurs de recherche. Par HTML, la variable `title` est un sous-ensemble de la propriété `image` tag : `<image title="tooltip" alt="description" src="image.jpg">`.

## [!UICONTROL Advanced]

- Pour contrôler le positionnement horizontal des images ajoutées au conteneur, sélectionnez une **[!UICONTROL Alignment]**.

  | Option | Description |
  | ------ | ----------- |
  | `Default` | Applique le paramètre d’alignement par défaut spécifié dans la feuille de style du thème actif. |
  | `Left` | Aligne le contenu de l’image le long de la bordure gauche du conteneur d’images, en tenant compte de la marge intérieure spécifiée. |
  | `Center` | Aligne le contenu de l’image dans le centre du conteneur d’images, en tenant compte de la marge intérieure qui est spécifiée. |
  | `Right` | Aligne le contenu de l’image le long de la bordure droite du conteneur d’images, en tenant compte de la marge intérieure spécifiée. |

  {style="table-layout:auto"}

- Définissez la variable **[!UICONTROL Border]** style appliqué aux quatre côtés du conteneur d’images :

  | Option | Description |
  | ------ | ----------- |
  | `Default` | Applique le style de bordure par défaut spécifié par la feuille de style associée. |
  | `None` | Ne fournit aucune indication visible des bordures du conteneur. |
  | `Dotted` | La bordure du conteneur s’affiche sous la forme d’une ligne pointillée. |
  | `Dashed` | La bordure du conteneur s’affiche sous la forme d’une ligne en pointillés. |
  | `Solid` | La bordure du conteneur s’affiche sous la forme d’une ligne pleine. |
  | `Double` | La bordure du conteneur s’affiche sous la forme d’une ligne double. |
  | `Groove` | La bordure du conteneur s’affiche sous forme de ligne droite. |
  | `Ridge` | La bordure du conteneur s’affiche sous la forme d’une ligne à droite. |
  | `Inset` | La bordure du conteneur s’affiche sous la forme d’une ligne d’insertion. |
  | `Outset` | La bordure du conteneur apparaît comme une ligne de départ. |

  {style="table-layout:auto"}

- Si vous définissez un style de bordure autre que `None`, renseignez les options d’affichage des bordures :

  ![Couleur de la bordure](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

  | Option | Description |
  | ------ |------------ |
  | [!UICONTROL Border Color] | Définissez la couleur en choisissant un échantillon, en cliquant sur le sélecteur de couleurs ou en saisissant un nom de couleur valide ou une valeur hexadécimale équivalente. |
  | [!UICONTROL Border Width] | Saisissez le nombre de pixels pour la largeur de la ligne de bordure. |
  | [!UICONTROL Border Radius] | Saisissez le nombre de pixels pour définir la taille du rayon utilisé pour arrondir chaque coin de la bordure. |

  {style="table-layout:auto"}

- (Facultatif) Indiquez les noms des **[!UICONTROL CSS classes]** de la feuille de style actuelle à appliquer au conteneur d’images.

  Séparez plusieurs noms de classe par un espace.

- Saisissez des valeurs, en pixels, pour la variable **[!UICONTROL Margins and Padding]** pour spécifier les marges extérieures et la marge intérieure du conteneur d’images.

  Saisissez chaque valeur correspondante dans le diagramme du conteneur d’images.

  | Zone de conteneur | Description |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | Espace vide appliqué au bord extérieur de tous les côtés du conteneur. |
  | [!UICONTROL Padding] | Espace blanc appliqué au bord intérieur de tous les côtés du conteneur. |

  {style="table-layout:auto"}
