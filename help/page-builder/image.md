---
title: Média - Image
description: Découvrez le type de contenu Image, utilisé pour ajouter une image JPG, GIF ou PNG à l’étape [!DNL Page Builder] image.
exl-id: 1b8d906e-7570-4c1f-87a0-992400faf55c
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '1550'
ht-degree: 0%

---

# Média - Image

Utilisez le type de contenu _Image_ pour ajouter une image JPG, GIF ou PNG à l’[[!DNL Page Builder] étape](workspace.md#stage). Outre l’image de bureau par défaut, vous pouvez spécifier une image secondaire pour les appareils mobiles. Vous pouvez également ajouter une légende qui s’affiche sous l’image et lier l’image à une URL, un produit, une catégorie ou une page.

>[!TIP]
>
>Vous pouvez utiliser l’intégration [Adobe Stock](../content-design/adobe-stock.md) pour rechercher et enregistrer une ressource appropriée parmi les millions fournis par [Adobe Stock](https://stock.adobe.com). Consultez [Utilisation d’images Adobe Stock](../content-design/adobe-stock-manage.md) pour plus d’informations sur la recherche, l’affinement et l’enregistrement de ressources Adobe Stock dans votre galerie.

{{$include /help/_includes/page-builder-save-timeout.md}}

## Boîte à outils Image

La boîte à outils Image s’affiche lorsque vous placez le pointeur de la souris sur le conteneur d’images.

![Boîte à outils Image](./assets/pb-media-image-giftcard-column-toolbox.png){width="500" zoomable="yes"}

| Outil | Icon | Description |
|--- |--- |--- |
| Déplacer | ![&#x200B; Icône Déplacer &#x200B;](./assets/pb-icon-move.png){width="25"} | Déplace l&#39;image vers un autre emplacement sur la scène. |
| (libellé) | Image | Identifie le conteneur de contenu actuel en tant qu’image. Pointez sur le conteneur d’image pour afficher la boîte à outils. |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} | Ouvre la page _Modifier l’image_, dans laquelle vous pouvez modifier les propriétés de l’image et du conteneur. |
| Masquer | ![Icône Masquer](./assets/pb-icon-hide.png){width="25"} | Masque l&#39;image courante. |
| Afficher | ![Afficher l’icône](./assets/pb-icon-show.png){width="25"} | Affiche l’image masquée. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="25"} | Effectue une copie de l’image. |
| Supprimer | ![Icône Supprimer](./assets/pb-icon-remove.png){width="25"} | Supprime l’image de l’étape. |
| Charger une nouvelle image |  | Télécharge une image de votre système de fichiers local vers la galerie. |
| Sélectionner dans la Galerie |  | Choisit une image existante dans la galerie. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Ajout d’une image

1. Dans le panneau [!DNL Page Builder], développez **[!UICONTROL Media]** et faites glisser un espace réservé **[!UICONTROL Image]** vers le conteneur cible.

   Vous pouvez ajouter une image à une ligne, une colonne ou un onglet. Dans l’exemple suivant, l’image est glissée sur une colonne vide.

   ![Faire glisser un type de contenu d’image sur l’étape](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

1. Utilisez l’une des méthodes suivantes pour ajouter la ressource image :

   ![Chargez l’image ou sélectionnez-en une parmi les outils de la Galerie sur la scène](./assets/pb-media-image-upload-select.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >La taille de fichier maximale est de 4 Mo. Les types de fichiers pris en charge sont JPG, GIF et PNG.

   - _&#x200B;**Charger une nouvelle image**&#x200B;_ : utilisez cette méthode pour charger un nouveau fichier image à partir de votre système.

      - Cliquez sur **[!UICONTROL Upload Image]**.

      - Recherchez et choisissez l’image à ajouter au conteneur galerie et cible.

     Vous pouvez également faire glisser un fichier image de votre système et le déposer sur l’icône _Appareil photo_ ( ![Icône d’appareil photo](./assets/pb-icon-camera.png){width="20"} ).

   - _&#x200B;**Sélectionner une ressource existante**&#x200B;_ : utilisez cette méthode pour sélectionner une ressource image existante dans la galerie ou le stockage de médias.

      - Cliquez sur **[!UICONTROL Select from Gallery]**.

      - Utilisez l’arborescence pour accéder à l’image.

      - Cliquez sur la miniature, puis sur **[!UICONTROL Add Selected]**.

        ![Ajouter une image sélectionnée](./assets/pb-media-image-gallery-add-selected.png){width="600" zoomable="yes"}

   - _&#x200B;**Rechercher et sélectionner une image Adobe Stock**&#x200B;_ : utilisez cette méthode pour rechercher une image dans Adobe Stock.

     >[!NOTE]
     >
     >Cette méthode nécessite une intégration [Adobe Stock](../content-design/adobe-stock.md) configurée pour votre administrateur.

      - Cliquez sur **[!UICONTROL Search Adobe Stock]** et recherchez une image.

      - Enregistrez l’aperçu ou l’image sous licence dans la galerie.

        Voir [Utilisation d’images Adobe Stock](../content-design/adobe-stock-manage.md) pour plus d’informations sur l’utilisation des ressources Adobe Stock.

      - Sélectionnez la miniature de la ressource dans la galerie et cliquez sur **[!UICONTROL Add Selected]**.

   L’image s’affiche dans le conteneur cible à l’emplacement de l’espace réservé. Contrairement à une image d’arrière-plan, vous pouvez déplacer l’image vers un autre emplacement au sein du conteneur actif ou vers un autre conteneur.

   >[!NOTE]
   >
   >Les types de contenu [Bannière](banner.md) et [Curseur](slider.md) incluent également les options _Charger l’image_ et _Sélectionner dans la galerie_ pour ajouter des images.

   ![Image dans une colonne](./assets/pb-media-image-column1-giftcard.png){width="500" zoomable="yes"}

## Modifier les paramètres de l’image

1. Pointez sur le conteneur d’image pour afficher la boîte à outils et sélectionnez l’icône _Paramètres_ (![icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).
Le nom, les dimensions et la taille du fichier s’affichent sous l’image actuelle.

   ![Image actuelle](./assets/pb-media-image-settings-image.png){width="600" zoomable="yes"}

1. Pour modifier le **[!UICONTROL Image]** actuel, effectuez l’une des opérations suivantes :

   - _&#x200B;**Charger une nouvelle image**&#x200B;_ : utilisez cette méthode pour charger un nouveau fichier image à partir de votre système.

      - Cliquez sur **[!UICONTROL Upload Image]**.

      - Recherchez et choisissez l’image à ajouter au conteneur galerie et cible.

   - _&#x200B;**Sélectionner une ressource existante**&#x200B;_ : utilisez cette méthode pour sélectionner une ressource image existante dans la galerie ou le stockage de médias.

      - Cliquez sur **[!UICONTROL Select from Gallery]**.

      - Utilisez l’arborescence pour accéder à l’image.

      - Cliquez sur la miniature, puis sur **[!UICONTROL Add Selected]**.

        ![Ajouter une image sélectionnée](./assets/pb-media-image-gallery-add-selected.png){width="600" zoomable="yes"}

   - **Rechercher et sélectionner une image Adobe Stock** : utilisez cette méthode pour rechercher une image dans Adobe Stock.

     >[!NOTE]
     >
     >Cette méthode nécessite une intégration [Adobe Stock](../content-design/adobe-stock.md) configurée pour votre administrateur.

      - Cliquez sur **[!UICONTROL Search Adobe Stock]** et recherchez une image.

      - Enregistrez l’aperçu ou l’image sous licence dans la galerie.

        Voir [Utilisation d’images Adobe Stock](../content-design/adobe-stock-manage.md) pour plus d’informations sur l’utilisation des ressources Adobe Stock.

      - Sélectionnez la miniature de la ressource dans la galerie et cliquez sur **[!UICONTROL Add Selected]**.

1. Pour ajouter une **[!UICONTROL Mobile Image]**, utilisez les mêmes méthodes que celles décrites à l’étape précédente pour sélectionner une image à utiliser pour l’affichage sur les appareils mobiles.

   ![&#x200B; Image mobile &#x200B;](./assets/pb-media-image-settings-mobile-image.png){width="600" zoomable="yes"}

1. Si nécessaire, spécifiez un **[!UICONTROL Link]** pour l’image.

   Le lien est la page de destination qui s’affiche lorsque le client clique sur l’image. Vous pouvez utiliser l’un des trois types de liens suivants :

   - **[!UICONTROL URL]** - Liens vers une URL relative ou complète.

   - **[!UICONTROL Product]** : identifie la page de destination en fonction du nom du produit ou du SKU. Recherchez le produit par nom en fonction d’un nom partiel ou complet. Choisissez le produit dans la liste des résultats de la recherche.

     ![Choix d’un produit à lier](./assets/pb-media-image-settings-image-link-product-results.png){width="600" zoomable="yes"}

   - **[!UICONTROL Category]** - Identifie la page de destination en tant que catégorie ou sous-catégorie spécifique dans l’arborescence des catégories. Recherchez la catégorie en fonction d’un nom partiel ou complet. Sélectionnez la catégorie dans la section développée de l’arborescence affichée.

     ![Choix d’une catégorie à lier](./assets/pb-media-image-settings-image-link-category-tree.png){width="600" zoomable="yes"}

   - **[!UICONTROL Page]** - Identifie la page de destination en tant que page de contenu spécifique. Recherchez la page en fonction d’un nom partiel ou complet. Sélectionnez la page dans la liste des résultats de la recherche.

     ![Choix d’une page à lier](./assets/pb-media-image-settings-image-link-page-results.png){width="600" zoomable="yes"}

   Si vous souhaitez empêcher le visiteur de quitter votre boutique, cochez la case **[!UICONTROL Open in new tab]** . Lorsque la case à cocher est désactivée, la destination liée s’ouvre dans le même onglet du navigateur, ce qui peut efficacement éloigner le visiteur de votre magasin.

1. Pour ajouter un **[!UICONTROL Image Caption]**, saisissez le texte qui doit apparaître sous l’image.

   Le format de la légende est déterminé par la feuille de style associée au thème actif.

   La légende s’affiche généralement sous l’image et fournit des informations sur l’image à l’intention des visiteurs et des moteurs de recherche. Si votre site est disponible dans plusieurs langues, vous pouvez utiliser la même image, mais traduire la légende. Dans HTML, la balise `<figcaption>` est un sous-ensemble de la balise `<figure>` . `<figcaption>This is the image caption</figcaption>`

1. Mettez à jour l’un des autres paramètres si nécessaire :

   - [Optimisation du moteur de recherche](#search-engine-optimization)
   - [Avancé](#advanced)

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

## Déplacer une image

1. Pointez sur le conteneur d’image pour afficher la boîte à outils et sélectionnez l’icône _Déplacer_ (![Icône Déplacer](./assets/pb-icon-move.png){width="20"} ).

   ![Déplacer une image](./assets/pb-media-image-column1-move-giftcard.png){width="500" zoomable="yes"}

1. Sélectionnez l’image et faites-la glisser vers sa nouvelle position, juste en dessous de la ligne directrice rouge.

   ![Utilisation de la consigne rouge pour positionner l’image](./assets/pb-media-image-column2-move-giftcard-red-guideline.png){width="500" zoomable="yes"}

## Suppression d’une image

1. Pointez sur le conteneur d’image pour afficher la boîte à outils et sélectionnez l’icône _Supprimer_ ( ![Icône Supprimer](./assets/pb-icon-remove.png){width="20"} ).

1. Lorsque vous êtes invité à confirmer, cliquez sur **[!UICONTROL OK]**.

## Optimisation du moteur de recherche

Le texte de ces paramètres est visible par les moteurs de recherche et améliore la façon dont la page est indexée.

- Par **[!UICONTROL Alternative Text]**, saisissez une description textuelle _alt_ pour les outils d’accessibilité numérique à afficher.

  L’utilisation de texte secondaire est une bonne pratique en matière d’accessibilité et est requise par la loi dans certains paramètres régionaux. Dans HTML, l’attribut `alt` est un sous-ensemble de la balise `image` : `<image title="tooltip" alt="description" src="image.jpg">`.

- Par **[!UICONTROL Title Attribute]**, saisissez le texte à afficher sous forme d’info-bulle lorsque vous pointez dessus.

  Il est recommandé de choisir un titre descriptif et riche en mots-clés pour améliorer la manière dont l’image est indexée par les moteurs de recherche. Dans HTML, l’attribut `title` est un sous-ensemble de la balise `image` : `<image title="tooltip" alt="description" src="image.jpg">`.

## [!UICONTROL Advanced]

- Pour contrôler le positionnement horizontal des images ajoutées au conteneur, choisissez une **[!UICONTROL Alignment]**.

  | Option | Description |
  | ------ | ----------- |
  | `Default` | Applique le paramètre d’alignement par défaut spécifié dans la feuille de style du thème actif. |
  | `Left` | Aligne le contenu de l’image le long de la bordure gauche du conteneur d’images, en tenant compte de la marge intérieure spécifiée. |
  | `Center` | Aligne le contenu de l’image au centre du conteneur d’images en tenant compte de la marge intérieure spécifiée. |
  | `Right` | Aligne le contenu de l’image le long de la bordure droite du conteneur d’images, en tenant compte de la marge intérieure spécifiée. |

  {style="table-layout:auto"}

- Définissez le style de **[!UICONTROL Border]** appliqué aux quatre côtés du conteneur d’images :

  | Option | Description |
  | ------ | ----------- |
  | `Default` | Applique le style de bordure par défaut spécifié par la feuille de style associée. |
  | `None` | Ne fournit aucune indication visible des bordures du conteneur. |
  | `Dotted` | La bordure du conteneur s’affiche sous la forme d’une ligne pointillée. |
  | `Dashed` | La bordure du conteneur s’affiche sous la forme d’une ligne en tirets. |
  | `Solid` | La bordure du conteneur s’affiche sous la forme d’une ligne continue. |
  | `Double` | La bordure du conteneur s’affiche sous la forme d’une ligne double. |
  | `Groove` | La bordure du conteneur s’affiche sous la forme d’une ligne rainurée. |
  | `Ridge` | La bordure du conteneur s’affiche sous la forme d’une ligne crantée. |
  | `Inset` | La bordure du conteneur s’affiche sous la forme d’une ligne insérée. |
  | `Outset` | La bordure du conteneur s’affiche sous la forme d’une ligne de départ. |

  {style="table-layout:auto"}

- Si vous définissez un style de bordure autre que `None`, renseignez les options d’affichage des bordures :

  ![Couleur de bordure](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

  | Option | Description |
  | ------ |------------ |
  | [!UICONTROL Border Color] | Spécifiez la couleur en choisissant une nuance, en cliquant sur le sélecteur de couleurs ou en saisissant un nom de couleur valide ou une valeur hexadécimale équivalente. |
  | [!UICONTROL Border Width] | Saisissez le nombre de pixels pour la largeur de la ligne de bordure. |
  | [!UICONTROL Border Radius] | Saisissez le nombre de pixels pour définir la taille du rayon utilisé pour arrondir chaque coin de la bordure. |

  {style="table-layout:auto"}

- (Facultatif) Spécifiez les noms des **[!UICONTROL CSS classes]** de la feuille de style actuelle à appliquer au conteneur d’images.

  Séparez plusieurs noms de classe par un espace.

- Saisissez les valeurs, en pixels, du **[!UICONTROL Margins and Padding]** pour spécifier les marges extérieures et la marge intérieure du conteneur d’images.

  Saisissez chaque valeur correspondante dans le diagramme de conteneur d’images.

  | Zone conteneur | Description |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | Quantité d’espace vide appliqué au bord extérieur de tous les côtés du conteneur. |
  | [!UICONTROL Padding] | Quantité d’espace vide appliqué au bord intérieur de tous les côtés du conteneur. |

  {style="table-layout:auto"}

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
