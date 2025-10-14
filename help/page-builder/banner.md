---
title: Média - Bannière
description: Découvrez le type de contenu Bannière utilisé pour ajouter un composant illustré et interactif à l’étape  [!DNL Page Builder] .
exl-id: 287d866c-8a63-4531-8c1b-40d560a07947
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '2302'
ht-degree: 0%

---

# Média - Bannière

Utilisez le type de contenu _Bannière_ pour ajouter un composant illustré et interactif qui engage les utilisateurs avec un call to action et un bouton dans l’[[!DNL Page Builder] étape](workspace.md#stage).

>[!NOTE]
>
>Ce qui était auparavant l’option _Bannière_ dans le menu Contenu, est désormais [Bloc dynamique](../content-design/dynamic-blocks.md).

![Bannière sur une page d’accueil de storefront](./assets/pb-banner-homepage.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Boîte à outils Bannière

La boîte à outils de bannière s’affiche lorsque vous pointez sur le conteneur de bannières.

![Boîte à outils Bannière](./assets/pb-tutorial1-banner-toolbox.png){width="600" zoomable="yes"}

| Outil | Icon | Description |
|--- |--- |--- |
| Déplacer | ![&#x200B; Icône Déplacer &#x200B;](./assets/pb-icon-move.png){width="25"} | Déplace la bannière vers une autre position sur la scène. |
| (libellé) | Bannière | Identifie le conteneur de contenu actuel en tant que bannière. Pointez sur le conteneur pour afficher la boîte à outils. |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} | Ouvre la page Modifier la bannière , qui permet de modifier les propriétés de la bannière et du conteneur. |
| Masquer | ![Icône Masquer](./assets/pb-icon-hide.png){width="25"} | Masque la bannière active. |
| Afficher | ![Afficher l’icône](./assets/pb-icon-show.png){width="25"} | Affiche la bannière masquée. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="25"} | Copie la bannière. |
| Supprimer | ![Icône Supprimer](./assets/pb-icon-remove.png){width="25"} | Supprime la bannière de l’étape. |
| [!UICONTROL Upload New Image] |  | Télécharge une image de votre système de fichiers local vers la galerie pour l’arrière-plan de bannière. |
| [!UICONTROL Select from Gallery] |  | Utilise une image existante de la galerie pour l’arrière-plan de bannière. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Ajouter une bannière

1. Dans le panneau [!DNL Page Builder], développez **[!UICONTROL Media]** et faites glisser un espace réservé **[!UICONTROL Banner]** vers la scène.

   ![Faire glisser un type de contenu de bannière vers l’étape](./assets/pb-tutorial1-banner-drag-to-stage.png){width="600" zoomable="yes"}

   Les boutons _[!UICONTROL Upload Image]_&#x200B;et&#x200B;_[!UICONTROL Select from Gallery]_ sont inclus afin que vous puissiez apporter des modifications rapides au contenu de la bannière directement depuis l’étape. Vous pouvez également modifier le contenu de la page de _[!UICONTROL Edit Banner]_.

1. Cliquez dans l’espace réservé de la bannière pour afficher l’[éditeur de texte](../content-design/editor.md) et saisissez le contenu de la bannière.

   Vous pouvez également inclure du contenu de bannière plus complexe à l’aide des paramètres [Contenu](#content).

## Modifier les paramètres de la bannière

1. Pointez sur le conteneur de bannières pour afficher la boîte à outils et sélectionnez l’icône _Paramètres_ (![icône Paramètres](./assets/pb-icon-settings.png)).

1. Consultez les sections suivantes pour obtenir des informations détaillées sur la mise à jour des paramètres disponibles :

   - [[!UICONTROL Appearance]](#appearance)
   - [[!UICONTROL Content]](#content)
   - [[!UICONTROL Background]](#background)
   - [[!UICONTROL Advanced]](#advanced)

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]** dans le coin supérieur droit pour fermer la page _[!UICONTROL Edit Banner]_.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

## [!UICONTROL Appearance]

Les bannières sont faciles à configurer et à gérer, car elles sont basées sur l’un des quatre modèles prédéfinis.

- Sélectionnez l’un des types d’emplacement de bannière suivants :

  | Placement | Description |
  | --------- | ----------- |
  | [!UICONTROL Poster] | Centre le contenu et le bouton sur la bannière. Le recouvrement, s’il est utilisé, étend la largeur complète de la bannière. |
  | [!UICONTROL Collage Left] | Place le contenu et le bouton dans une zone définie sur le côté gauche de la bannière. S’il est utilisé, le recouvrement ne couvre que la zone définie. |
  | [!UICONTROL Collage Center] | Place le contenu et le bouton dans une zone définie centrée sur la bannière. S’il est utilisé, le recouvrement ne couvre que la zone définie. |
  | [!UICONTROL Collage Right] | Place le contenu et le bouton dans une zone définie sur le côté droit de la bannière. S’il est utilisé, le recouvrement ne couvre que la zone définie. |

  {style="table-layout:auto"}

  ![Apparence - collage droit](./assets/pb-tutorial1-row-banner-settings-appearance-collage-right.png){width="600" zoomable="yes"}

- (Facultatif) Saisissez le **[!UICONTROL Minimum Height]** de la ligne.

  La hauteur minimale peut être un nombre avec une unité CSS valide (telle que `100px`, `50%`, `50em`, `100vh`) ou un calcul (tel que `100vh - 237px`).

  Par exemple, vous pouvez définir la hauteur minimale d’une bannière pour étirer toute la hauteur de la page, ce qui vous offre des options attrayantes pour les images et vidéos d’arrière-plan pleine page.

## [!UICONTROL Background]

Il existe de nombreuses options pour définir l’affichage en arrière-plan d’une bannière. Vous pouvez appliquer une couleur ou une image d’arrière-plan simple et gérer des effets plus sophistiqués.

### [!UICONTROL Background Color]

Spécifiez la couleur d’arrière-plan en choisissant une nuance, en cliquant sur le sélecteur de couleurs ou en saisissant un nom de couleur valide ou une valeur hexadécimale équivalente. Ce paramètre détermine la couleur d’arrière-plan de la ligne. Vous pouvez également régler l’opacité de la couleur.

![Aucune couleur (par défaut)](./assets/pb-settings-background-color-no-color.png){width="200"}

Vous pouvez définir la valeur de l’une des trois façons suivantes :

- Un nom de couleur prédéfini, tel que `White`
- Valeur hexadécimale de la couleur, telle que `#ffffff`
- Valeur rgba de la couleur, avec le pourcentage d’opacité, tel que `rgba(255, 255, 255, 0.75)`

Pour sélectionner une couleur, cliquez sur l’échantillon à gauche de la zone _Aucune couleur_.

![Choix d’un échantillon de couleur](./assets/pb-settings-background-color-picker-swatch.png){width="600" zoomable="yes"}

Si vous cliquez sur la zone de couleur pour ouvrir à nouveau le sélecteur de couleurs, la zone située sous le curseur affiche les valeurs actuelles rouge, vert, bleu et alpha (rgba). Le dernier nombre indique le pourcentage d’opacité actuel sous la forme d’une décimale. Vous pouvez utiliser le curseur pour ajuster l’opacité ou saisir la valeur décimale souhaitée.

![Définition de l’opacité](./assets/pb-settings-background-color.png){width="600" zoomable="yes"}

>[!NOTE]
>
>[!DNL Page Builder] prend également en charge un calque de transparence, ou couche _alpha_, dans les images d’arrière-plan qui peuvent être utilisées pour créer des arrière-plans avec différents degrés d’opacité.

### [!UICONTROL Background Type]

Un type d’arrière-plan peut être une image ou une vidéo. [!DNL Page Builder] est défini par défaut sur `Image` et affiche divers paramètres d’image. Si vous sélectionnez `Video`, [!DNL Page Builder] permute les paramètres de l’image avec les paramètres vidéo. Les deux paramètres de type arrière-plan sont décrits dans les sections suivantes.

![Type d’arrière-plan](./assets/pb-background-type.png){width="200"}

### Paramètres de type d’image

Si vous définissez le _Type d’arrière-plan_ sur `Image`, utilisez les paramètres suivants pour définir l’affichage de l’image d’arrière-plan.

![Bannière avec image de fond](./assets/pb-tutorial1-banner-background.png){width="600" zoomable="yes"}

- **[!UICONTROL Background Image]** - Si nécessaire, utilisez les outils fournis pour choisir une image d’arrière-plan à appliquer à la bannière :

  | Outil | Description |
  | ---- | ----------- |
  | [!UICONTROL Upload] | Télécharge un fichier image de votre ordinateur local dans la galerie, puis l’applique comme image d’arrière-plan pour la bannière. |
  | [!UICONTROL Select from Gallery] | Vous invite à choisir une image existante de la galerie comme image d’arrière-plan pour la bannière. |
  | ![&#x200B; Icône Appareil photo &#x200B;](./assets/pb-icon-camera.png){width="25"} | Vous permet de faire glisser l’image vers la mosaïque de la caméra ou d’accéder à l’image dans votre système de fichiers local. |

  {style="table-layout:auto"}

- **[!UICONTROL Background Mobile Image]** - Si nécessaire, utilisez les mêmes outils pour choisir une image d’arrière-plan différente à utiliser pour l’affichage sur les appareils mobiles.

- **[!UICONTROL Background Size]** - Définissez cette option pour déterminer la mise à l’échelle de l’image d’arrière-plan par rapport à la largeur de la bannière :

  | Option | Description |
  | ------ | ----------- |
  | `Cover` | L’image d’arrière-plan couvre toute la largeur de la bannière. |
  | `Contain` | L’image d’arrière-plan est limitée à la largeur de la zone de contenu. |
  | `Auto` | Applique la taille de la feuille de style active. |

  {style="table-layout:auto"}

  ![Taille de l’arrière-plan](./assets/pb-layout-row-settings-background-size-cover.png){width="200"}

- **[!UICONTROL Background Position]** - Définissez cette option pour déterminer comment l’image d’arrière-plan est ancrée par rapport à la bannière :

  | Ancrer | Positions |
  | ------ | ----------- |
  | `Top` | Gauche / Centre / Droite |
  | `Center` | Gauche / Centre / Droite |
  | `Bottom` | Gauche / Centre / Droite |

  {style="table-layout:auto"}

  Le point d’ancrage est semblable à une goupille qui attache l’image à la bannière à la position d’arrière-plan spécifiée.

- **[!UICONTROL Background Attachment]** - Définissez le type de pièce jointe pour déterminer le déplacement de l’image d’arrière-plan par rapport à la page de défilement :

  | Option | Description |
  | ------ | ----------- |
  | `Scroll` | L’image d’arrière-plan jointe est synchronisée pour se déplacer vers le bas lors du défilement de la page. |
  | `Fixed` | (Non disponible pour les appareils mobiles) L’image d’arrière-plan ne se déplace pas lorsque le conteneur défile sur l’image et est fixe à la position d’arrière-plan spécifiée. |

  {style="table-layout:auto"}

- **[!UICONTROL Background Repeat]** - Si vous souhaitez répéter l’image d’arrière-plan pour remplir l’espace, modifiez `Yes` ce paramètre.

### Paramètres de type vidéo

Si vous définissez la _[!UICONTROL Background Type]_&#x200B;sur `Video`, utilisez les paramètres suivants pour définir l’affichage de l’image d’arrière-plan.

- **[!UICONTROL Video URL]** - Saisissez une URL de vidéo valide. Les URL de vidéo valides peuvent être des liens vers :

   - Vidéos YouTube : `https://youtu.be/CoDhMRUUjeI`
   - Vidéos Vimeo : `https://vimeo.com/190156113`
   - Fichiers vidéo valides (`.mp4` recommandé) : `https://myvideos.com/spiral.mp4`

  ![URL de la vidéo d’arrière-plan](./assets/pb-video-url.png){width="200"}

- **[!UICONTROL Overlay Color]** - Sélectionnez une couleur pour appliquer une teinte transparente à la vidéo.

- **[!UICONTROL Infinite Loop]** - Définissez sur `No` pour que la vidéo soit lue une fois et arrêtée. Lorsqu’elle est définie sur `Yes` (par défaut), la vidéo se répète en boucle infinie.

- **[!UICONTROL Lazy Load]** - Définissez sur `No` pour que la vidéo se charge avec la page, même si elle n’est pas visible. Lorsqu’elle est définie sur `Yes` (par défaut), la vidéo se charge à partir de la source uniquement lorsqu’elle est visible à l’écran.

- **[!UICONTROL Play Only When Visible]** - Définissez sur `No` pour que la vidéo commence à être lue immédiatement après son chargement, qu’elle soit visible ou non. Lorsqu’elle est définie sur `Yes` (par défaut), la vidéo ne commence à être lue que lorsqu’elle est visible.

- **[!UICONTROL Fallback Image]** - Si nécessaire, spécifiez une image à afficher à l’écran avant le chargement de la vidéo et si la vidéo ne se charge pas pour une raison quelconque.

## [!UICONTROL Content]

Vous pouvez modifier le contenu de la bannière directement sur la scène ou lorsque vous modifiez les paramètres. Les paramètres fournissent des fonctionnalités de contenu plus complexes, telles que des liens de bannière, des boutons et des recouvrements. La position du contenu reflète le paramètre d’emplacement [Apparence](#appearance).

### Contenu simple sur la scène

1. Cliquez sur le texte de l’espace réservé et saisissez le texte que vous souhaitez afficher sur la bannière.

   La barre d’outils de l’éditeur apparaît au-dessus de la zone de texte.

   ![Modifier le contenu sur l’étape](./assets/pb-tutorial1-banner-stage-text.png){width="600" zoomable="yes"}

1. Utilisez la barre d’outils de l’éditeur pour saisir et mettre en forme le texte, ainsi que pour insérer des éléments, tels que des liens, des images et des widgets.

   ![Phase avec texte formaté](./assets/pb-tutorial1-banner-stage-text-format-line2.png){width="600" zoomable="yes"}

### Contenu complexe dans les paramètres

1. Pointez sur le conteneur de bannières pour afficher la boîte à outils et sélectionnez l’icône _Paramètres_ ( ![icône Paramètres](./assets/pb-icon-settings.png){width="25"} ).

1. Faites défiler jusqu’à la section _[!UICONTROL Content]_&#x200B;et utilisez l’éditeur de **[!UICONTROL Message Text]**&#x200B;pour saisir et mettre en forme le texte de la bannière.

   Vous pouvez également insérer des éléments, tels que des liens de texte, des images et des widgets.

   ![Éditeur de texte de message](./assets/pb-tutorial1-banner-settings-content-message-text.png){width="600" zoomable="yes"}

1. Si nécessaire, spécifiez un **[!UICONTROL Link]** pour la bannière.

   Le lien est la page de destination qui s’affiche lorsque le client clique sur le bouton ou la zone de la bannière. Vous pouvez utiliser l’un des trois types de liens suivants :

   - **[!UICONTROL URL]** - Liens vers une URL relative ou complète.
   - **[!UICONTROL Product]** : identifie la page de destination en fonction du nom du produit ou du SKU. Recherchez le produit par nom en fonction d’un nom partiel ou complet. Choisissez le produit dans la liste des résultats de la recherche.
   - **[!UICONTROL Category]** - Identifie la page de destination en tant que catégorie ou sous-catégorie spécifique dans l’arborescence des catégories. Recherchez la catégorie en fonction d’un nom partiel ou complet. Sélectionnez la catégorie dans la section développée de l’arborescence affichée.
   - **[!UICONTROL Page]** - Identifie la page de destination en tant que page de contenu spécifique. Recherchez la page en fonction d’un nom partiel ou complet. Sélectionnez la page dans la liste des résultats de la recherche.

   >[!NOTE]
   >
   >À compter de la version 2.4.1, [!DNL Page Builder] ne prend plus en charge la liaison de la bannière et des liens dans le texte imbriqué en raison de problèmes d’affichage sur le storefront. Si vous utilisez un lien dans le _[!UICONTROL Message Text]_, vous ne pouvez pas configurer l’option&#x200B;_[!UICONTROL Link]_ . Si vous préférez utiliser un seul lien pour l’ensemble de la bannière, vous pouvez supprimer tous les liens du texte.<br/>
   >
   >![La configuration du lien est bloquée](./assets/pb-nested-link-blocked.png){width="200"}


1. Si nécessaire, ajoutez un bouton pour inviter les clients à suivre le lien.

   Le paramètre Apparence de la bannière place un lien ou un bouton unique sous le texte. Renseignez les propriétés du lien ou du bouton que vous souhaitez ajouter.

   ![Apparence avec texte et bouton (ou lien)](./assets/pb-tutorial1-row-banner-settings-appearance-collage-right.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Vous pouvez également utiliser plusieurs boutons ou liens en ajoutant un [bloc](block.md) à la bannière. Pour éviter tout conflit, conservez tous les liens ou boutons dans un bloc distinct et n’ajoutez pas de lien ou de bouton directement à la bannière.

   - Définissez **[!UICONTROL Show Button]** sur l’une des options suivantes :

     | Option | Description |
     | ------ | ----------- |
     | `Always` | Un bouton apparaît toujours sur la bannière. |
     | `On Hover` | Un bouton s’affiche sur la bannière uniquement lorsque vous survolez la zone. |
     | `Never Show` | Un bouton n’apparaît jamais sur la bannière. |

     {style="table-layout:auto"}

   - Saisissez le **[!UICONTROL Button Text]** à afficher sur le bouton.

   - Définissez **[!UICONTROL Button Type]** sur l’une des options suivantes :

     | Option | Description |
     | ------ | ----------- |
     | `Primary` | Applique le style du bouton principal à partir de la feuille de style actuelle. |
     | `Secondary` | Applique le style du bouton secondaire de la feuille de style en cours, le cas échéant. |
     | `Link` | Crée un lien hypertexte plutôt qu’un bouton. |

     {style="table-layout:auto"}

     Le style de bouton du thème actuel détermine le format du bouton. En règle générale, un bouton principal a une couleur d’arrière-plan plus proéminente qu’un bouton secondaire.

1. Définissez **[!UICONTROL Show Overlay]** sur l’une des options suivantes :

   | Option | Description |
   | ------ | ----------- |
   | `Always` | Le recouvrement est toujours visible. |
   | `On Hover` | Le recouvrement s’affiche uniquement lorsque vous survolez la zone. |
   | `Never Show` | Le recouvrement n’est pas visible. |

   {style="table-layout:auto"}

   Vous pouvez utiliser une superposition pour appliquer une couleur d’arrière-plan à la zone de contenu active définie par le paramètre [!UICONTROL Appearance]. L’image d’arrière-plan de la bannière reste visible sur toute la largeur de la bannière.

   Si vous choisissez d’afficher une superposition, définissez le **[!UICONTROL Overlay Color]** :

   - Cliquez sur l’échantillon **Aucune couleur** et choisissez-en un.
   - Dans le champ **Aucune couleur** , saisissez un nom de couleur valide ou une valeur hexadécimale.

   ![&#x200B; Couleur de recouvrement &#x200B;](./assets/pb-tutorial1-banner-settings-overlay-color.png){width="600" zoomable="yes"}

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

   ![Bannière avec message texte et bouton](./assets/pb-tutorial1-banner-stage-background-color.png){width="600" zoomable="yes"}


## [!UICONTROL Search Engine Optimization] {#seo}

Le texte de ces paramètres est visible par les moteurs de recherche et améliore la façon dont la page est indexée.

- Par **[!UICONTROL Alternative Text]**, saisissez une description textuelle _alt_ pour les outils d’accessibilité numérique à afficher.

  L’utilisation de texte secondaire est une bonne pratique en matière d’accessibilité et est requise par la loi dans certains paramètres régionaux. Dans HTML, l’attribut `alt` est un sous-ensemble de la balise `image` : `<image title="tooltip" alt="description" src="image.jpg">`.

- Par **[!UICONTROL Title Attribute]**, saisissez le texte à afficher sous forme d’info-bulle lorsque vous pointez dessus.

  Il est recommandé de choisir un titre descriptif et riche en mots-clés pour améliorer la manière dont l’image est indexée par les moteurs de recherche. Dans HTML, l’attribut `title` est un sous-ensemble de la balise `image` : `<image title="tooltip" alt="description" src="image.jpg">`.

## [!UICONTROL Advanced]

1. Pour contrôler le positionnement horizontal des conteneurs de contenu ajoutés à la bannière, choisissez une **[!UICONTROL Alignment]** :

   | Option | Description |
   | ------ | ----------- |
   | `Default` | Applique le paramètre d’alignement par défaut spécifié dans la feuille de style du thème actif. |
   | `Left` | Aligne les conteneurs de contenu le long de la bordure gauche du conteneur de bannière, en tenant compte de la marge intérieure spécifiée. |
   | `Center` | Aligne le conteneur de contenu au centre du conteneur de bannières, en tenant compte de la marge intérieure spécifiée. |
   | `Right` | Aligne le conteneur de contenu le long de la bordure droite du conteneur de bannières, en tenant compte de la marge intérieure spécifiée. |

   {style="table-layout:auto"}

1. Définissez le style de **[!UICONTROL Border]** appliqué aux quatre côtés du conteneur de bannières :

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

1. Si vous définissez un style de bordure autre que `None`, renseignez les options d’affichage des bordures :

   - **[!UICONTROL Border Color]** - Spécifiez la couleur en choisissant un échantillon, en cliquant sur le sélecteur de couleurs ou en saisissant un nom de couleur valide ou une valeur hexadécimale équivalente.

     ![Couleur de bordure](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

   - **[!UICONTROL Border Width]** - Saisissez le nombre de pixels pour la largeur de la ligne de bordure.

   - **[!UICONTROL Border Radius]** - Saisissez le nombre de pixels pour définir la taille du rayon utilisé pour arrondir chaque coin de la bordure.

1. (Facultatif) Spécifiez les noms des **[!UICONTROL CSS classes]** de la feuille de style actuelle à appliquer au conteneur de bannières.

   Séparez plusieurs noms de classe par un espace.

1. Saisissez les valeurs, en pixels, du **[!UICONTROL Margins and Padding]** pour spécifier les marges extérieures et la marge intérieure de la bannière.

   Saisissez chaque valeur correspondante dans le diagramme de conteneur de bannières.

   | Option | Description |
   | ------ | ----------- |
   | [!UICONTROL Margins] | Quantité d’espace vide appliqué au bord extérieur de tous les côtés du conteneur. |
   | [!UICONTROL Padding] | Quantité d’espace vide appliqué au bord intérieur de tous les côtés du conteneur. |

   {style="table-layout:auto"}

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
