---
title: Media - Image
description: Découvrez le type de contenu Image, utilisé pour ajouter une image de JPG, de GIF ou PNG à l’étape  [!DNL Page Builder] .
exl-id: 1b8d906e-7570-4c1f-87a0-992400faf55c
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1550'
ht-degree: 0%

---

# Media - Image

Utilisez le type de contenu _Image_ pour ajouter une image de GIF, de  ou PNG à l’ [[!DNL Page Builder] étape](workspace.md#stage). Outre l’image de bureau par défaut, vous pouvez spécifier une image secondaire pour les appareils mobiles. Vous pouvez également ajouter une légende qui s’affiche sous l’image et associer l’image à n’importe quelle URL, produit, catégorie ou page.

>[!TIP]
>
>Vous pouvez utiliser l’ [intégration Adobe Stock](../content-design/adobe-stock.md) pour rechercher et enregistrer une ressource appropriée parmi les millions de ressources fournies par [Adobe Stock](https://stock.adobe.com). Voir [Utilisation d’images Adobe Stock](../content-design/adobe-stock-manage.md) pour plus d’informations sur la recherche, l’affinage et l’enregistrement de ressources Adobe Stock dans votre galerie.

{{$include /help/_includes/page-builder-save-timeout.md}}

## Zone d’outils Image

La boîte à outils d’image s’affiche lorsque vous placez le pointeur de la souris sur le conteneur d’images.

![Boîte à outils d’image](./assets/pb-media-image-giftcard-column-toolbox.png){width="500" zoomable="yes"}

| Outil | Icône | Description |
|--- |--- |--- |
| Déplacer | ![Icône Déplacer](./assets/pb-icon-move.png){width="25"} | Déplace l’image vers une autre position sur la scène. |
| (label) | Image | Identifie le conteneur de contenu actuel en tant qu’image. Passez la souris sur le conteneur d’images pour afficher la boîte à outils. |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} | Ouvre la page _Modifier l’image_ où vous pouvez modifier les propriétés de l’image et du conteneur. |
| Masquer | ![Icône Masquer](./assets/pb-icon-hide.png){width="25"} | Masque l’image active. |
| Afficher | ![Icône Afficher](./assets/pb-icon-show.png){width="25"} | Affiche l’image masquée. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="25"} | Effectue une copie de l’image. |
| Supprimer | ![Supprimer l’icône](./assets/pb-icon-remove.png){width="25"} | Supprime l’image de la scène. |
| Charger une nouvelle image |  | Télécharge une image de votre système de fichiers local vers la galerie. |
| Sélectionner dans la galerie |  | Choisit une image existante dans la galerie. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Ajout d’une image

1. Dans le panneau [!DNL Page Builder], développez **[!UICONTROL Media]** et faites glisser un espace réservé **[!UICONTROL Image]** vers le conteneur cible.

   Vous pouvez ajouter une image à une ligne, une colonne ou un onglet. Dans l’exemple suivant, l’image est glissée sur une colonne vide.

   ![Faire glisser un type de contenu d’image vers l’étape](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

1. Utilisez l’une des méthodes suivantes pour ajouter la ressource image :

   ![Télécharger l’image ou effectuer une sélection à partir des outils de galerie sur l’étape](./assets/pb-media-image-upload-select.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >La taille de fichier maximale est de 4 Mo. Les types de fichiers pris en charge sont JPG, GIF et PNG.

   - _**Télécharger une nouvelle image**_ : utilisez cette méthode pour charger un nouveau fichier image à partir de votre système.

      - Cliquez sur **[!UICONTROL Upload Image]**.

      - Recherchez et sélectionnez l’image à ajouter à la galerie et au conteneur cible.

     Vous pouvez également faire glisser un fichier image de votre système et le déposer sur l’icône _Camera_ ( ![Icône de caméra](./assets/pb-icon-camera.png){width="20"} ).

   - _**Sélectionner une ressource existante**_ : utilisez cette méthode pour sélectionner une ressource d’image existante dans le stockage/la galerie de médias.

      - Cliquez sur **[!UICONTROL Select from Gallery]**.

      - Utilisez l’arborescence pour accéder à l’image.

      - Cliquez sur la miniature et sur **[!UICONTROL Add Selected]**.

        ![Ajouter une image sélectionnée](./assets/pb-media-image-gallery-add-selected.png){width="600" zoomable="yes"}

   - _**Recherchez et sélectionnez une image Adobe Stock**_ : utilisez cette méthode pour trouver une image à partir d’Adobe Stock.

     >[!NOTE]
     >
     >Cette méthode nécessite une [intégration Adobe Stock](../content-design/adobe-stock.md) configurée pour votre administrateur.

      - Cliquez sur **[!UICONTROL Search Adobe Stock]** et recherchez une image.

      - Enregistrez l’aperçu ou l’image sous licence dans la galerie.

        Pour plus d’informations sur l’utilisation des ressources Adobe Stock, voir [Utilisation d’images Adobe Stock](../content-design/adobe-stock-manage.md) .

      - Sélectionnez la miniature de la ressource dans la galerie et cliquez sur **[!UICONTROL Add Selected]**.

   L’image apparaît dans le conteneur cible à l’emplacement de l’espace réservé. Contrairement à une image d’arrière-plan, vous pouvez déplacer l’image vers une autre position dans le conteneur actif ou vers un autre conteneur.

   >[!NOTE]
   >
   >Les types de contenu [Bannière](banner.md) et [Curseur](slider.md) incluent également les options _Télécharger l’image_ et _Sélectionner dans la galerie_ pour ajouter des images.

   ![Image dans une colonne](./assets/pb-media-image-column1-giftcard.png){width="500" zoomable="yes"}

## Modification des paramètres d’image

1. Pointez sur le conteneur d’images pour afficher la boîte à outils et sélectionnez l’icône _Paramètres_ (![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).
Le nom, les dimensions et la taille du fichier apparaissent sous l’image active.

   ![Image actuelle](./assets/pb-media-image-settings-image.png){width="600" zoomable="yes"}

1. Pour modifier le **[!UICONTROL Image]** actif, effectuez l’une des opérations suivantes :

   - _**Télécharger une nouvelle image**_ : utilisez cette méthode pour charger un nouveau fichier image à partir de votre système.

      - Cliquez sur **[!UICONTROL Upload Image]**.

      - Recherchez et sélectionnez l’image à ajouter à la galerie et au conteneur cible.

   - _**Sélectionner une ressource existante**_ : utilisez cette méthode pour sélectionner une ressource d’image existante dans le stockage/la galerie de médias.

      - Cliquez sur **[!UICONTROL Select from Gallery]**.

      - Utilisez l’arborescence pour accéder à l’image.

      - Cliquez sur la miniature et sur **[!UICONTROL Add Selected]**.

        ![Ajouter une image sélectionnée](./assets/pb-media-image-gallery-add-selected.png){width="600" zoomable="yes"}

   - **Recherchez et sélectionnez une image Adobe Stock** : utilisez cette méthode pour trouver une image à partir d’Adobe Stock.

     >[!NOTE]
     >
     >Cette méthode nécessite une [intégration Adobe Stock](../content-design/adobe-stock.md) configurée pour votre administrateur.

      - Cliquez sur **[!UICONTROL Search Adobe Stock]** et recherchez une image.

      - Enregistrez l’aperçu ou l’image sous licence dans la galerie.

        Pour plus d’informations sur l’utilisation des ressources Adobe Stock, voir [Utilisation d’images Adobe Stock](../content-design/adobe-stock-manage.md) .

      - Sélectionnez la miniature de la ressource dans la galerie et cliquez sur **[!UICONTROL Add Selected]**.

1. Pour ajouter un **[!UICONTROL Mobile Image]**, utilisez les mêmes méthodes que celles décrites à l&#39;étape précédente pour sélectionner une image à utiliser pour l&#39;affichage sur les appareils mobiles.

   ![Image mobile](./assets/pb-media-image-settings-mobile-image.png){width="600" zoomable="yes"}

1. Si nécessaire, spécifiez un **[!UICONTROL Link]** pour l’image.

   Le lien est la page de destination qui s’affiche lorsque le client clique sur l’image. Vous pouvez utiliser l’un des trois types de liens suivants :

   - **[!UICONTROL URL]** - Liens vers une URL relative ou complète.

   - **[!UICONTROL Product]** - Identifie la page de destination en fonction du nom du produit ou du SKU. Recherchez le produit par nom en fonction d’un nom partiel ou complet. Sélectionnez le produit dans la liste des résultats de recherche.

     ![Choisir un produit à lier](./assets/pb-media-image-settings-image-link-product-results.png){width="600" zoomable="yes"}

   - **[!UICONTROL Category]** - Identifie la page de destination en tant que catégorie ou sous-catégorie spécifique dans l’arborescence des catégories. Recherchez la catégorie selon un nom partiel ou complet. Sélectionnez la catégorie dans la section développée de l&#39;arborescence affichée.

     ![Choix d’une catégorie à lier](./assets/pb-media-image-settings-image-link-category-tree.png){width="600" zoomable="yes"}

   - **[!UICONTROL Page]** - Identifie la page de destination en tant que page de contenu spécifique. Recherchez la page en fonction d’un nom partiel ou complet. Sélectionnez la page dans la liste des résultats de recherche.

     ![Choix d’une page à lier](./assets/pb-media-image-settings-image-link-page-results.png){width="600" zoomable="yes"}

   Si vous souhaitez empêcher le visiteur de quitter votre boutique, cochez la case **[!UICONTROL Open in new tab]** . Lorsque la case à cocher est décochée, la destination liée s’ouvre dans le même onglet du navigateur, ce qui peut permettre de faire quitter votre boutique au visiteur.

1. Pour ajouter un **[!UICONTROL Image Caption]**, saisissez le texte qui doit apparaître sous l’image.

   Le format de la légende est déterminé par la feuille de style associée au thème actif.

   La légende apparaît généralement sous l’image et fournit des informations sur l’image aux visiteurs et aux moteurs de recherche. Si votre site est disponible en plusieurs langues, vous pouvez utiliser la même image, mais traduire la légende. En HTML, la balise `<figcaption>` est un sous-ensemble de la balise `<figure>`. `<figcaption>This is the image caption</figcaption>`

1. Mettez à jour les autres paramètres si nécessaire :

   - [Optimisation du moteur de recherche](#search-engine-optimization)
   - [Avancé](#advanced)

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

## Déplacer une image

1. Pointez sur le conteneur d’images pour afficher la boîte à outils et sélectionnez l’icône _Déplacer_ (![Icône Déplacer](./assets/pb-icon-move.png){width="20"} ).

   ![Déplacement d’une image](./assets/pb-media-image-column1-move-giftcard.png){width="500" zoomable="yes"}

1. Sélectionnez l’image et faites-la glisser jusqu’à sa nouvelle position, juste en dessous de la ligne directrice rouge.

   ![Utilisation de la ligne guide rouge pour positionner l&#39;image](./assets/pb-media-image-column2-move-giftcard-red-guideline.png){width="500" zoomable="yes"}

## Supprimer une image

1. Pointez sur le conteneur d’images pour afficher la boîte à outils et sélectionnez l’icône _Supprimer_ ( ![Icône Supprimer](./assets/pb-icon-remove.png){width="20"} ).

1. Lorsque vous êtes invité à confirmer l’opération, cliquez sur **[!UICONTROL OK]**.

## Optimisation du moteur de recherche

Le texte de ces paramètres est visible par les moteurs de recherche et améliore la manière dont la page est indexée.

- Pour **[!UICONTROL Alternative Text]**, saisissez une description textuelle _alt_ pour les outils d’accessibilité numérique à afficher.

  L’utilisation de texte de remplacement est une bonne pratique en matière d’accessibilité. Elle est requise par la loi dans certains paramètres régionaux. En HTML, l’attribut `alt` est un sous-ensemble de la balise `image` : `<image title="tooltip" alt="description" src="image.jpg">`.

- Pour **[!UICONTROL Title Attribute]**, saisissez le texte à afficher sous forme d’info-bulle lorsque vous pointez dessus.

  Il est recommandé de choisir un titre descriptif et riche en mots-clés afin d’améliorer l’indexation de l’image par les moteurs de recherche. En HTML, l’attribut `title` est un sous-ensemble de la balise `image` : `<image title="tooltip" alt="description" src="image.jpg">`.

## [!UICONTROL Advanced]

- Pour contrôler le positionnement horizontal des images ajoutées au conteneur, choisissez un **[!UICONTROL Alignment]**.

  | Option | Description |
  | ------ | ----------- |
  | `Default` | Applique le paramètre d’alignement par défaut spécifié dans la feuille de style du thème actif. |
  | `Left` | Aligne le contenu de l’image le long de la bordure gauche du conteneur d’images, en tenant compte de la marge intérieure spécifiée. |
  | `Center` | Aligne le contenu de l’image dans le centre du conteneur d’images, en tenant compte de la marge intérieure qui est spécifiée. |
  | `Right` | Aligne le contenu de l’image le long de la bordure droite du conteneur d’images, en tenant compte de la marge intérieure spécifiée. |

  {style="table-layout:auto"}

- Définissez le style **[!UICONTROL Border]** appliqué aux quatre côtés du conteneur d’images :

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

- Si vous définissez un style de bordure autre que `None`, renseignez les options d’affichage de la bordure :

  ![Couleur de bordure](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

  | Option | Description |
  | ------ |------------ |
  | [!UICONTROL Border Color] | Définissez la couleur en choisissant un échantillon, en cliquant sur le sélecteur de couleurs ou en saisissant un nom de couleur valide ou une valeur hexadécimale équivalente. |
  | [!UICONTROL Border Width] | Saisissez le nombre de pixels pour la largeur de la ligne de bordure. |
  | [!UICONTROL Border Radius] | Saisissez le nombre de pixels pour définir la taille du rayon utilisé pour arrondir chaque coin de la bordure. |

  {style="table-layout:auto"}

- (Facultatif) Indiquez les noms de **[!UICONTROL CSS classes]** dans la feuille de style actuelle à appliquer au conteneur d’images.

  Séparez plusieurs noms de classe par un espace.

- Saisissez des valeurs, en pixels, pour que **[!UICONTROL Margins and Padding]** spécifient les marges extérieures et la marge intérieure du conteneur d’images.

  Saisissez chaque valeur correspondante dans le diagramme du conteneur d’images.

  | Zone de conteneur | Description |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | Espace vide appliqué au bord extérieur de tous les côtés du conteneur. |
  | [!UICONTROL Padding] | Espace blanc appliqué au bord intérieur de tous les côtés du conteneur. |

  {style="table-layout:auto"}
