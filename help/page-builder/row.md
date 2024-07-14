---
title: Disposition - Ligne
description: Découvrez le type de contenu Ligne , utilisé pour ajouter une ligne dans l’étape  [!DNL Page Builder] .
exl-id: 0aa8bf6f-7ae3-4718-9f76-430ed63ba05c
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '1620'
ht-degree: 0%

---

# Disposition - Ligne

Utilisez le type de contenu _Row_ pour ajouter une ligne dans l’ [[!DNL Page Builder] stage](workspace.md#stage).

{{$include /help/_includes/page-builder-save-timeout.md}}

## Boîte à outils de rangée

La boîte à outils de rangée s’affiche lorsque vous passez la souris sur le conteneur de rangées. La boîte à outils contient des options permettant de déplacer, masquer, dupliquer, modifier ou supprimer la ligne. La sélection des paramètres détermine l’aspect, l’arrière-plan et la mise en page de la ligne. D’autres éléments de contenu peuvent être déplacés vers la ligne à partir du panneau [!DNL Page Builder] sur la gauche.

![Boîte à outils de lignes](./assets/pb-layout-page-add-content-row-tools.png){width="600" zoomable="yes"}

| Outil | Icône | Description |
| --------- | ---------- | ----------- |
| Déplacer | ![Icône Déplacer](./assets/pb-icon-move.png){width="25"} | Déplace la rangée vers une autre position par rapport aux autres rangées de la scène. |
| (label) | [!UICONTROL Row] | Identifie le conteneur de contenu actuel sous la forme d’une ligne. Passez la souris sur le conteneur pour afficher la boîte à outils. |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} | Ouvre la page Modifier la rangée, dans laquelle vous pouvez modifier les propriétés du conteneur. |
| Masquer | ![Icône Masquer](./assets/pb-icon-hide.png){width="25"} | Masque la ligne actuelle. |
| Afficher | ![Icône Afficher](./assets/pb-icon-show.png){width="25"} | Affiche la ligne masquée. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="25"} | Effectue une copie de la ligne. |
| Supprimer | ![Supprimer l’icône](./assets/pb-icon-remove.png){width="25"} | Supprime le conteneur de lignes et son contenu de la scène. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Ajouter une ligne

1. Dans le panneau [!DNL Page Builder] sous _[!UICONTROL Layout]_, faites glisser un nouveau **[!UICONTROL Row]**sur la scène, juste en dessous de la première ligne.

1. Pour mettre en forme la ligne, passez la souris sur le conteneur de lignes pour afficher la boîte à outils et choisissez l’icône _Paramètres_ ( ![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

   Pour plus d’informations sur l’exécution des paramètres disponibles, reportez-vous aux sections suivantes.

   ![Ajout d’une ligne](./assets/pb-layout-row-add.png){width="600" zoomable="yes"}

## Modification des paramètres de ligne

1. Pointez sur le conteneur de lignes pour afficher la boîte à outils et sélectionnez l’icône _Paramètres_ ( ![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

   ![Boîte à outils de lignes](./assets/pb-tutorial1-row-toolbox.png){width="600" zoomable="yes"}

1. Pour plus d’informations sur la mise à jour des paramètres disponibles, reportez-vous aux sections suivantes.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

## Apparence

Utilisez les paramètres _Apparence_ pour déterminer le mode d’affichage du contenu dans la ligne.

![Paramètres d’aspect](./assets/pb-row-layout.png){width="600" zoomable="yes"}

- Pour déterminer la couleur de fond et/ou l’image d’arrière-plan par rapport au conteneur et à la largeur de la zone de contenu, choisissez l’alignement :

  | Option | Description |
  | ------ | ----------- |
  | [!UICONTROL Contained] | La couleur ou l’image d’arrière-plan est limitée à la largeur maximale de page définie par le thème. |
  | [!UICONTROL Full Width] | Limite le contenu à la largeur maximale de la page définie par le thème. La couleur de fond et/ou l’image n’est pas limitée et étend la largeur totale de la ligne. |
  | [!UICONTROL Full Bleed] | Le contenu et l’image d’arrière-plan et/ou la couleur ne sont pas limités et s’étendent sur toute la largeur de la ligne. Le fond perdu ne peut être utilisé qu’avec les [thèmes](../content-design/themes.md) qui prennent en charge la mise en page. |

  {style="table-layout:auto"}

- Saisissez le **[!UICONTROL Minimum Height]** pour la ligne. Cette valeur peut être un nombre avec n’importe quelle unité CSS valide (telle que `100px`, `50%`, `50em`, `100vh`) ou un calcul (telle que `100vh - 237px`).

  Vous pouvez, par exemple, définir la hauteur minimale d’une ligne pour étirer la hauteur totale de la page, ce qui vous donne des options attrayantes pour les images et vidéos d’arrière-plan de la page entière.

- Choisissez un paramètre **[!UICONTROL Vertical Alignment]** pour aligner les conteneurs de contenu qui sont ajoutés à la ligne (Haut, Centre ou Bas).

## Contexte

Il existe de nombreuses options pour définir l’affichage en arrière-plan d’une ligne. Vous pouvez appliquer une simple couleur ou une image d’arrière-plan et gérer des effets plus sophistiqués.

### Couleur d’arrière-plan

Spécifiez la couleur d’arrière-plan en choisissant un échantillon, en cliquant sur le sélecteur de couleurs ou en saisissant un nom de couleur valide ou une valeur hexadécimale équivalente. Ce paramètre détermine la couleur d’arrière-plan de la ligne. Vous pouvez également régler l’opacité de la couleur.

![Aucune couleur (par défaut)](./assets/pb-settings-background-color-no-color.png){width="200"}

Vous pouvez définir la valeur de l’une des trois façons suivantes :

- Un nom de couleur prédéfini, tel que `White`
- La valeur de couleur hexadécimale de la couleur, par exemple `#ffffff`
- La valeur rgba de la couleur, avec le pourcentage d’opacité, comme `rgba(255, 255, 255, 0.75)`

Si vous souhaitez choisir une couleur, cliquez sur l’échantillon à gauche de la zone _Aucune couleur_.

![Choix d’un échantillon de couleur](./assets/pb-settings-background-color-picker-swatch.png){width="600" zoomable="yes"}

Si vous cliquez sur la zone de couleur pour ouvrir à nouveau le sélecteur de couleurs, la zone située sous le curseur affiche les valeurs actuelles rouge, vert, bleu et alpha (rgba). Le dernier chiffre indique le pourcentage d’opacité actuel sous forme décimale. Vous pouvez utiliser le curseur pour ajuster l’opacité ou saisir la valeur décimale souhaitée.

![Paramètre d’opacité](./assets/pb-settings-background-color.png){width="600" zoomable="yes"}

>[!NOTE]
>
>[!DNL Page Builder] prend également en charge une couche de transparence, ou _couche alpha_, dans les images d’arrière-plan qui peuvent être utilisées pour créer des arrière-plans avec différents degrés d’opacité.

### [!UICONTROL Background Type]

Un type d’arrière-plan peut être une image ou une vidéo. [!DNL Page Builder] est défini par défaut sur `Image` et affiche divers paramètres d’image. Si vous sélectionnez `Video`, [!DNL Page Builder] permute les paramètres de l’image avec les paramètres vidéo. Les deux types d’arrière-plan sont décrits comme suit.

![Type d’arrière-plan](./assets/pb-background-type.png){width="200"}

### Paramètres de type d’image

Si vous définissez _[!UICONTROL Background Type]_sur `Image`, utilisez les paramètres suivants pour définir l’affichage de l’image d’arrière-plan.

![Image d’arrière-plan](./assets/pb-tutorial1-row-settings-background-image-selected.png){width="600" zoomable="yes"}

- **[!UICONTROL Background Image]** - Si nécessaire, utilisez les outils fournis pour choisir une image d’arrière-plan à appliquer à la ligne :

  | Option | Description |
  | ------ | ----------- |
  | [!UICONTROL Upload] | Télécharge un fichier image de l’ordinateur local vers la galerie, puis l’applique comme image d’arrière-plan de la ligne. |
  | [!UICONTROL Select from Gallery] | Vous invite à choisir une image existante de la galerie comme image d’arrière-plan pour la ligne. |
  | ![Icône Appareil photo](./assets/pb-icon-camera.png){width="25"} | Permet de faire glisser l’image sur la mosaïque de l’appareil photo ou de naviguer jusqu’à l’image dans votre système de fichiers local. |

  {style="table-layout:auto"}

- **[!UICONTROL Background Mobile Image]** - Si nécessaire, utilisez les mêmes outils pour choisir une image d’arrière-plan différente à utiliser pour l’affichage sur les appareils mobiles.

- **[!UICONTROL Background Size]** - Définissez cette option pour déterminer la mise à l’échelle de l’image d’arrière-plan par rapport à la largeur de la ligne :

  | Option | Description |
  | ------ | ----------- |
  | `Cover` | L’image d’arrière-plan couvre toute la largeur de la rangée. |
  | `Contain` | L’image d’arrière-plan est limitée à la largeur de la zone de contenu. |
  | `Auto` | Applique la taille de la feuille de style actuelle. |

  {style="table-layout:auto"}

  ![Taille d’arrière-plan](./assets/pb-layout-row-settings-background-size-cover.png){width="250"}

- **[!UICONTROL Background Position]** - Définissez cette option pour déterminer comment l’image d’arrière-plan est ancrée par rapport à la ligne :

  | Point d’ancrage | Position |
  | ------ | ----------- |
  | `Top` | Gauche/Centre/Droite |
  | `Center` | Gauche/Centre/Droite |
  | `Bottom` | Gauche/Centre/Droite |

  {style="table-layout:auto"}

  Le point d’ancrage est semblable à une épingle push qui joint l’image à la rangée à la position d’arrière-plan spécifiée.

- **[!UICONTROL Background Attachment]** - Définissez le type de pièce jointe pour déterminer le déplacement de l’image d’arrière-plan par rapport à la page de défilement :

  | Option | Description |
  | ------ | ----------- |
  | `Scroll` | L’image d’arrière-plan jointe est synchronisée pour se déplacer vers le bas au fur et à mesure que la page fait défiler. Utilisez l’arrière-plan de Parallax pour contrôler la vitesse de défilement. |
  | `Fixed` | (Non disponible pour les appareils mobiles) L’image d’arrière-plan ne se déplace pas lorsque le conteneur fait défiler l’image et est fixe à la position d’arrière-plan spécifiée. |

  {style="table-layout:auto"}

- **[!UICONTROL Background Repeat]** - Défini sur `Yes` pour répéter l’image d’arrière-plan afin de remplir l’espace disponible dans la ligne.

### Paramètres de type vidéo

Si vous définissez le _Type d’arrière-plan_ sur `Video`, utilisez les paramètres suivants pour définir l’affichage de l’image d’arrière-plan.

- **[!UICONTROL Video URL]** - Entrez une URL de vidéo valide. Les URL de vidéo valides peuvent être des liens vers :

   - Vidéos YouTube : `https://youtu.be/CoDhMRUUjeI`
   - Vidéos Vimeo : `https://vimeo.com/190156113`
   - Fichiers vidéo valides (`.mp4` recommandé) : `https://myvideos.com/spiral.mp4`

  ![URL de la vidéo d’arrière-plan](./assets/pb-video-url.png){width="300"}

- **[!UICONTROL Overlay Color]** - Sélectionnez une couleur pour appliquer une teinte transparente à la vidéo.

- **[!UICONTROL Infinite Loop]** - Définissez cette variable sur `No` pour que la vidéo soit lue une fois et s’arrête. Lorsque cette option est définie sur `Yes` (valeur par défaut), la vidéo se répète en boucle infinie.

- **[!UICONTROL Lazy Load]** - Défini sur `No` pour que la vidéo se charge avec la page, même lorsqu’elle n’est pas visible. Lorsque cette option est définie sur `Yes` (par défaut), la vidéo se charge à partir de la source uniquement lorsqu’elle est visible à l’écran.

- **[!UICONTROL Play Only When Visible]** - Définissez cette variable sur `No` pour que la lecture de la vidéo démarre immédiatement après son chargement, qu’elle soit visible ou non. Lorsque cette option est définie sur `Yes` (valeur par défaut), la lecture de la vidéo démarre uniquement lorsqu’elle est visible.

- **[!UICONTROL Fallback Image]** - Si nécessaire, spécifiez une image à afficher à l’écran avant le chargement de la vidéo et si la vidéo ne se charge pas pour une raison quelconque.

## Contexte de Parallax

Utilisez ces options pour contrôler la vitesse d’une image ou d’une vidéo d’arrière-plan de défilement par rapport au défilement de la page. L’arrière-plan peut être défini pour défiler plus lentement afin de créer un sentiment d’immersion.

- Définissez **Activer l’arrière-plan Parallax** sur `Yes`.
- Saisissez la **vitesse de parallaxe** comme valeur décimale entre `-1.0` et `2.0`.

![Paramètres d’arrière-plan de Parallax](./assets/pb-settings-parallax-background.png){width="600" zoomable="yes"}

## Avancé

- Pour contrôler le positionnement horizontal des conteneurs de contenu qui sont ajoutés à la ligne, choisissez un **[!UICONTROL Alignment]** :

  | Option | Description |
  | ------ | ----------- |
  | `Default` | Applique le paramètre d’alignement par défaut spécifié dans la feuille de style du thème actif. |
  | `Left` | Aligne les conteneurs de contenu le long de la bordure gauche du conteneur de lignes, en tenant compte de toute marge intérieure spécifiée. |
  | `Center` | Aligne le conteneur de contenu au centre du conteneur de lignes, en tenant compte de la marge intérieure qui est spécifiée. |
  | `Right` | Aligne le conteneur de contenu le long de la bordure droite du conteneur de lignes, en tenant compte de toute marge intérieure spécifiée. |

  {style="table-layout:auto"}

- Définissez le style **[!UICONTROL Border]** appliqué aux quatre côtés du conteneur de lignes :

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

  La ligne de l’exemple suivant a un rayon de bordure de 15.

  ![Rangée avec un rayon de bordure de 15](./assets/pb-settings-border-radius-15.png){width="500"}

- (Facultatif) Indiquez les noms de **[!UICONTROL CSS classes]** dans la feuille de style actuelle à appliquer au conteneur de lignes.

  Séparez plusieurs noms de classe par un espace.

- Entrez des valeurs, en pixels, pour que **[!UICONTROL Margins and Padding]** indique les marges extérieures et le remplissage intérieur de la ligne.

  Saisissez chaque valeur correspondante dans le diagramme de conteneur de lignes.

  | Zone de conteneur | Description |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | Espace vide appliqué au bord extérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |
  | [!UICONTROL Padding] | Espace blanc appliqué au bord intérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |

  {style="table-layout:auto"}

  ![Marges et marge intérieure](./assets/pb-layout-row-settings-margin-padding-default.png){width="600" zoomable="yes"}
