---
title: Disposition - Ligne
description: Découvrez le type de contenu Ligne, utilisé pour ajouter une ligne dans l’étape [!DNL Page Builder] d’.
exl-id: 0aa8bf6f-7ae3-4718-9f76-430ed63ba05c
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '1620'
ht-degree: 0%

---

# Disposition - Ligne

Utilisez le type de contenu _Ligne_ pour ajouter une ligne dans le [[!DNL Page Builder] étape](workspace.md#stage).

{{$include /help/_includes/page-builder-save-timeout.md}}

## Boîte à outils Ligne

La boîte à outils de lignes s’affiche lorsque vous pointez sur le conteneur de lignes. La boîte à outils comprend des options permettant de déplacer, masquer, dupliquer, modifier ou supprimer la ligne. La sélection de paramètres détermine l’aspect, l’arrière-plan et la mise en page de la ligne. Vous pouvez faire glisser d’autres éléments de contenu sur la ligne à partir du panneau [!DNL Page Builder] sur la gauche.

![Boîte à outils Ligne](./assets/pb-layout-page-add-content-row-tools.png){width="600" zoomable="yes"}

| Outil | Icon | Description |
| --------- | ---------- | ----------- |
| Déplacer | ![&#x200B; Icône Déplacer &#x200B;](./assets/pb-icon-move.png){width="25"} | Déplace la ligne vers une autre position par rapport aux autres lignes de la scène. |
| (libellé) | [!UICONTROL Row] | Identifie le conteneur de contenu actuel sous la forme d’une ligne. Pointez sur le conteneur pour afficher la boîte à outils. |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} | Ouvre la page Modifier une ligne, qui permet de modifier les propriétés du conteneur. |
| Masquer | ![Icône Masquer](./assets/pb-icon-hide.png){width="25"} | Masque la ligne courante. |
| Afficher | ![Afficher l’icône](./assets/pb-icon-show.png){width="25"} | Affiche la ligne masquée. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="25"} | Crée une copie de la ligne. |
| Supprimer | ![Icône Supprimer](./assets/pb-icon-remove.png){width="25"} | Supprime le conteneur de lignes et son contenu de l’étape. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Ajouter une ligne

1. Dans le panneau [!DNL Page Builder] sous _[!UICONTROL Layout]_, faites glisser un nouveau **[!UICONTROL Row]**&#x200B;vers la scène, juste en dessous de la première ligne.

1. Pour formater la ligne, passez la souris sur le conteneur de lignes pour afficher la boîte à outils et choisissez l’icône _Paramètres_ ( ![icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

   Consultez les sections suivantes pour obtenir des informations détaillées sur la définition des paramètres disponibles.

   ![Ajout d’une ligne](./assets/pb-layout-row-add.png){width="600" zoomable="yes"}

## Modifier les paramètres des lignes

1. Pointez sur le conteneur de lignes pour afficher la boîte à outils et choisissez l’icône _Paramètres_ ( ![icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

   ![Boîte à outils Ligne](./assets/pb-tutorial1-row-toolbox.png){width="600" zoomable="yes"}

1. Consultez les sections suivantes pour obtenir des informations détaillées sur la mise à jour des paramètres disponibles.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

## Apparence

Utilisez les paramètres _Apparence_ pour déterminer comment le contenu s’affiche dans la ligne.

![Paramètres d’apparence](./assets/pb-row-layout.png){width="600" zoomable="yes"}

- Pour déterminer l’aspect de la couleur et/ou de l’image d’arrière-plan par rapport au conteneur et à la largeur de la zone de contenu, choisissez l’alignement :

  | Option | Description |
  | ------ | ----------- |
  | [!UICONTROL Contained] | La couleur ou l’image d’arrière-plan est limitée à la largeur de page maximale définie par le thème. |
  | [!UICONTROL Full Width] | Limite le contenu à la largeur maximale de page définie par le thème. La couleur et/ou l’image d’arrière-plan ne sont pas limitées et s’étendent sur toute la largeur de la ligne. |
  | [!UICONTROL Full Bleed] | Le contenu, l’image d’arrière-plan et/ou la couleur ne sont pas limités et étendent toute la largeur de la ligne. Le fond perdu ne peut être utilisé qu’avec des [thèmes](../content-design/themes.md) qui prennent en charge la mise en page. |

  {style="table-layout:auto"}

- Saisissez le **[!UICONTROL Minimum Height]** de la ligne. Cette valeur peut être un nombre avec une unité CSS valide (par exemple `100px`, `50%`, `50em`, `100vh`) ou un calcul (par exemple `100vh - 237px`).

  Par exemple, vous pouvez définir la hauteur minimale d’une ligne pour étirer toute la hauteur de la page, ce qui vous offre des options attrayantes pour les images et vidéos d’arrière-plan de toute la page.

- Sélectionnez un paramètre de **[!UICONTROL Vertical Alignment]** pour aligner tous les conteneurs de contenu ajoutés à la ligne (Haut, Centre ou Bas).

## Contexte

Il existe de nombreuses options pour définir l’affichage en arrière-plan d’une ligne. Vous pouvez appliquer une couleur ou une image d’arrière-plan simple et gérer des effets plus sophistiqués.

### Couleur d’arrière-plan

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

Un type d’arrière-plan peut être une image ou une vidéo. [!DNL Page Builder] est défini par défaut sur `Image` et affiche divers paramètres d’image. Si vous sélectionnez `Video`, [!DNL Page Builder] permute les paramètres de l’image avec les paramètres vidéo. Les deux types d’arrière-plan sont décrits comme suit.

![Type d’arrière-plan](./assets/pb-background-type.png){width="200"}

### Paramètres de type d’image

Si vous définissez la _[!UICONTROL Background Type]_&#x200B;sur `Image`, utilisez les paramètres suivants pour définir l’affichage de l’image d’arrière-plan.

![Image d’arrière-plan](./assets/pb-tutorial1-row-settings-background-image-selected.png){width="600" zoomable="yes"}

- **[!UICONTROL Background Image]** - Si nécessaire, utilisez les outils fournis pour choisir une image d’arrière-plan à appliquer à la ligne :

  | Option | Description |
  | ------ | ----------- |
  | [!UICONTROL Upload] | Télécharge un fichier image de votre ordinateur local dans la galerie, puis l’applique comme image d’arrière-plan pour la ligne. |
  | [!UICONTROL Select from Gallery] | Vous invite à choisir une image existante de la galerie comme image d’arrière-plan pour la ligne. |
  | ![&#x200B; Icône Appareil photo &#x200B;](./assets/pb-icon-camera.png){width="25"} | Vous permet de faire glisser l’image vers la mosaïque de la caméra ou d’accéder à l’image dans votre système de fichiers local. |

  {style="table-layout:auto"}

- **[!UICONTROL Background Mobile Image]** - Si nécessaire, utilisez les mêmes outils pour choisir une image d’arrière-plan différente à utiliser pour l’affichage sur les appareils mobiles.

- **[!UICONTROL Background Size]** - Définissez cette option pour déterminer la mise à l’échelle de l’image d’arrière-plan par rapport à la largeur de la ligne :

  | Option | Description |
  | ------ | ----------- |
  | `Cover` | L’image d’arrière-plan couvre toute la largeur de la ligne. |
  | `Contain` | L’image d’arrière-plan est limitée à la largeur de la zone de contenu. |
  | `Auto` | Applique la taille de la feuille de style active. |

  {style="table-layout:auto"}

  ![Taille de l’arrière-plan](./assets/pb-layout-row-settings-background-size-cover.png){width="250"}

- **[!UICONTROL Background Position]** - Définissez cette option pour déterminer comment l’image d’arrière-plan est ancrée par rapport à la ligne :

  | Point d’ancrage | Position |
  | ------ | ----------- |
  | `Top` | Gauche / Centre / Droite |
  | `Center` | Gauche / Centre / Droite |
  | `Bottom` | Gauche / Centre / Droite |

  {style="table-layout:auto"}

  Le point d’ancrage est semblable à une goupille qui attache l’image à la ligne à la position d’arrière-plan spécifiée.

- **[!UICONTROL Background Attachment]** - Définissez le type de pièce jointe pour déterminer le déplacement de l’image d’arrière-plan par rapport à la page de défilement :

  | Option | Description |
  | ------ | ----------- |
  | `Scroll` | L’image d’arrière-plan jointe est synchronisée pour se déplacer vers le bas lors du défilement de la page. Utilisez l’arrière-plan parallèle pour contrôler la vitesse de défilement. |
  | `Fixed` | (Non disponible pour les appareils mobiles) L’image d’arrière-plan ne se déplace pas lorsque le conteneur défile sur l’image et est fixe à la position d’arrière-plan spécifiée. |

  {style="table-layout:auto"}

- **[!UICONTROL Background Repeat]** - Définissez sur `Yes` pour répéter l’image d’arrière-plan afin de remplir l’espace disponible dans la ligne.

### Paramètres de type vidéo

Si vous définissez le _Type d’arrière-plan_ sur `Video`, utilisez les paramètres suivants pour définir l’affichage de l’image d’arrière-plan.

- **[!UICONTROL Video URL]** - Saisissez une URL de vidéo valide. Les URL de vidéo valides peuvent être des liens vers :

   - Vidéos YouTube : `https://youtu.be/CoDhMRUUjeI`
   - Vidéos Vimeo : `https://vimeo.com/190156113`
   - Fichiers vidéo valides (`.mp4` recommandé) : `https://myvideos.com/spiral.mp4`

  ![URL de la vidéo d’arrière-plan](./assets/pb-video-url.png){width="300"}

- **[!UICONTROL Overlay Color]** - Sélectionnez une couleur pour appliquer une teinte transparente à la vidéo.

- **[!UICONTROL Infinite Loop]** - Définissez sur `No` pour que la vidéo soit lue une fois et arrêtée. Lorsque cette option est définie sur `Yes` (par défaut), la vidéo se répète en boucle infinie.

- **[!UICONTROL Lazy Load]** - Définissez sur `No` pour que la vidéo se charge avec la page, même si elle n’est pas visible. Lorsque cette option est définie sur `Yes` (par défaut), la vidéo se charge à partir de la source uniquement lorsqu’elle est visible à l’écran.

- **[!UICONTROL Play Only When Visible]** - Définissez sur `No` pour que la vidéo commence à être lue immédiatement après son chargement, qu’elle soit visible ou non. Lorsque cette option est définie sur `Yes` (par défaut), la vidéo ne commence à être lue que lorsqu’elle est visible.

- **[!UICONTROL Fallback Image]** - Si nécessaire, spécifiez une image à afficher à l’écran avant le chargement de la vidéo et si la vidéo ne se charge pas pour une raison quelconque.

## Arrière-plan parallèle

Utilisez ces options pour contrôler la vitesse d’une image ou d’une vidéo d’arrière-plan qui défile par rapport au défilement de la page. L’arrière-plan peut être défini pour défiler plus lentement afin de créer une impression d’immersion.

- Définissez **Activer l’arrière-plan parallèle** sur `Yes`.
- Saisissez la **Vitesse parallèle** comme valeur décimale entre `-1.0` et `2.0`.

![Paramètres d’arrière-plan Parallax](./assets/pb-settings-parallax-background.png){width="600" zoomable="yes"}

## Avancé

- Pour contrôler le positionnement horizontal des conteneurs de contenu ajoutés à la ligne, choisissez une **[!UICONTROL Alignment]** :

  | Option | Description |
  | ------ | ----------- |
  | `Default` | Applique le paramètre d’alignement par défaut spécifié dans la feuille de style du thème actif. |
  | `Left` | Aligne les conteneurs de contenu le long de la bordure gauche du conteneur de ligne, en tenant compte de la marge intérieure spécifiée. |
  | `Center` | Aligne le conteneur de contenu au centre du conteneur de lignes, en tenant compte de la marge intérieure spécifiée. |
  | `Right` | Aligne le conteneur de contenu le long de la bordure droite du conteneur de lignes, en tenant compte de la marge intérieure spécifiée. |

  {style="table-layout:auto"}

- Définissez le style de **[!UICONTROL Border]** appliqué aux quatre côtés du conteneur de lignes :

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

  La ligne de l’exemple suivant a un rayon de bordure de 15.

  ![Ligne avec rayon de bordure de 15](./assets/pb-settings-border-radius-15.png){width="500"}

- (Facultatif) Spécifiez les noms des **[!UICONTROL CSS classes]** de la feuille de style actuelle à appliquer au conteneur de lignes.

  Séparez plusieurs noms de classe par un espace.

- Saisissez les valeurs, en pixels, du **[!UICONTROL Margins and Padding]** pour spécifier les marges extérieures et la marge intérieure de la ligne.

  Saisissez chaque valeur correspondante dans le diagramme de conteneur de lignes.

  | Zone conteneur | Description |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | Quantité d’espace vide appliqué au bord extérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |
  | [!UICONTROL Padding] | Quantité d’espace vide appliqué au bord intérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |

  {style="table-layout:auto"}

  ![Marges et marge intérieure](./assets/pb-layout-row-settings-margin-padding-default.png){width="600" zoomable="yes"}

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
