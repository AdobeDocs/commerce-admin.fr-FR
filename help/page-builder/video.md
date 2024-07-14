---
title: Media - Video
description: Découvrez le type de contenu Vidéo, utilisé pour ajouter une vidéo hébergée sur YouTube ou Vimeo à la scène  [!DNL Page Builder] .
exl-id: 9cd075e7-c10d-4c34-8932-c1ccb32bf198
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '918'
ht-degree: 0%

---

# Media - Video

Utilisez le type de contenu _Vidéo_ pour ajouter une vidéo hébergée sur [YouTube][1] ou [Vimeo][2] à la [[!DNL Page Builder] scène](workspace.md#stage). Il est facile d’incorporer des vidéos dans une page ou un bloc ou dans des descriptions de produits et de catégories.

![Vidéo sur la page d’accueil du storefront](./assets/pb-storefront-video.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Boîte à outils vidéo

![Boîte à outils vidéo](./assets/pb-media-video-toolbox.png){width="600" zoomable="yes"}

| Outil | Icône | Description |
|--- |--- |--- |
| Déplacer | ![Icône Déplacer](./assets/pb-icon-move.png){width="25"} | Déplace la vidéo vers une autre position sur la scène. |
| (label) | [!UICONTROL Video] | Identifie le conteneur de contenu actuel en tant que vidéo. Passez la souris sur le conteneur d’images pour afficher la boîte à outils. |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} | Ouvre la page _[!UICONTROL Edit Video]_dans laquelle vous pouvez modifier les propriétés de la vidéo et du conteneur. |
| Masquer | ![Icône Masquer](./assets/pb-icon-hide.png){width="25"} | Masque la vidéo en cours. |
| Afficher | ![Icône Afficher](./assets/pb-icon-show.png){width="25"} | Affiche la vidéo masquée. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="25"} | Effectue une copie de la vidéo. |
| Supprimer | ![Supprimer l’icône](./assets/pb-icon-remove.png){width="25"} | Supprime la vidéo de la scène. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Ajout d’une vidéo

1. Avant de commencer, accédez à la vidéo [YouTube][1] ou [Vimeo][2] que vous souhaitez incorporer et copiez le lien.

   Vous pouvez également copier un lien direct vers un fichier vidéo valide. Voir [Paramètres vidéo de base](#basic-video-settings) pour consulter des liens valides.

1. Dans l’administrateur [!DNL Commerce], revenez à l’espace de travail [!DNL Page Builder] où vous souhaitez ajouter la vidéo.

1. Dans le panneau [!DNL Page Builder], développez **[!UICONTROL Media]** et faites glisser un espace réservé **[!UICONTROL Video]** sur la scène.

   ![Glissement d’un espace réservé de vidéo vers l’étape](./assets/pb-media-video-drag.png){width="600" zoomable="yes"}

1. Pointez sur le conteneur vidéo pour afficher la boîte à outils et sélectionnez l’icône _Paramètres_ ( ![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

1. Pour **[!UICONTROL Video URL]**, collez l’URL de la vidéo que vous avez copiée.

   L’URL de la vidéo [!DNL Page Builder] utilisée dans cet exemple est : `https://www.youtube.com/watch?v=Y0KNS7C5dZA`.

1. Pour limiter l’ **[!UICONTROL Maximum Width]** de la vidéo, entrez la largeur maximale en pixels.

   Si la vidéo est vide, elle est aussi large que le conteneur le permet, ce qui permet des marges et une marge intérieure.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

## Modification des paramètres vidéo

1. Pointez sur le conteneur vidéo pour afficher la boîte à outils et sélectionnez l’icône _Paramètres_ ( ![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

1. Modifiez les paramètres en fonction des sections suivantes :

   - [De base](#basic-video-settings)
   - [Avancé](#advanced)

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

### Paramètres vidéo de base

1. Pour modifier la vidéo active, mettez à jour le **[!UICONTROL Video URL]**.

   Saisissez une URL de vidéo valide. Les URL de vidéo valides peuvent être des liens vers :

   - Vidéos YouTube : `https://youtu.be/CoDhMRUUjeI`
   - Vidéos Vimeo : `https://vimeo.com/190156113`
   - Fichiers vidéo valides (`.mp4` recommandé) : `https://myvideos.com/spiral.mp4`

1. Pour modifier la largeur autorisée pour la vidéo dans le storefront, saisissez le nouveau **[!UICONTROL Maximum Width]** en pixels.

   Si la valeur est vide, la vidéo étend la largeur totale du conteneur, sans tenir compte des marges et de la marge intérieure.

1. Pour démarrer automatiquement la vidéo après le chargement de la page, définissez **[!UICONTROL Autoplay]** sur `Yes`.

   Si la lecture automatique est définie sur `Yes`, la vidéo est coupée lors de la lecture conformément à la stratégie. Toutefois, même avec ce paramètre, les périphériques mobiles ne peuvent pas lire vos vidéos automatiquement. Pour plus d’informations sur ces stratégies, reportez-vous aux ressources de développement suivantes :

   - [Stratégie de lecture automatique à partir de Vimeo](https://vimeo.zendesk.com/hc/en-us/articles/115004485728-Autoplaying-and-looping-embedded-videos)
   - [Stratégie de lecture automatique à partir de Google (Chrome/YouTube)](https://developer.chrome.com/blog/autoplay/)
   - [Stratégie de lecture automatique pour les vidéos locales](https://developer.mozilla.org/en-US/docs/Web/Media/Autoplay_guide)

   Si la lecture automatique est définie sur `No`, la vidéo est lue à la demande de l’utilisateur uniquement.

### [!UICONTROL Advanced]

1. Pour contrôler le positionnement horizontal de la vidéo dans le conteneur, choisissez un **[!UICONTROL Alignment]** :

   | Option | Description |
   | ------ | ----------- |
   | `Default` | Applique le paramètre d’alignement par défaut spécifié dans la feuille de style du thème actif. |
   | `Left` | Aligne le contenu le long de la bordure gauche du conteneur vidéo, en tenant compte de la marge intérieure spécifiée. |
   | `Center` | Aligne le contenu au centre du conteneur vidéo, en tenant compte de la marge intérieure qui est spécifiée. |
   | `Right` | Aligne le contenu le long de la bordure droite du conteneur vidéo, en tenant compte de la marge intérieure spécifiée. |

   {style="table-layout:auto"}

- Définissez le style **[!UICONTROL Border]** appliqué aux quatre côtés du conteneur vidéo :

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

- (Facultatif) Indiquez les noms de **[!UICONTROL CSS classes]** dans la feuille de style actuelle à appliquer au conteneur vidéo.

  Séparez plusieurs noms de classe par un espace.

- Entrez des valeurs, en pixels, pour que **[!UICONTROL Margins and Padding]** indique les marges extérieures et la marge intérieure du conteneur vidéo.

  Saisissez chaque valeur correspondante dans le diagramme de conteneur vidéo.

  | Zone de conteneur | Description |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | Espace vide appliqué au bord extérieur de tous les côtés du conteneur. |
  | [!UICONTROL Padding] | Espace blanc appliqué au bord intérieur de tous les côtés du conteneur. |

  {style="table-layout:auto"}

## Déplacement d’une vidéo

1. Passez la souris sur le conteneur vidéo pour afficher la boîte à outils et sélectionnez l’icône _Déplacer_ ( ![Icône Déplacer](./assets/pb-icon-move.png){width="20"} ).

   ![Déplacement d’une vidéo](./assets/pb-media-video-toolbox-move-col1.png){width="500" zoomable="yes"}

1. Sélectionnez la vidéo et faites-la glisser vers sa nouvelle position, juste en dessous de la ligne directrice rouge.

   ![Utilisation de la ligne directrice rouge pour placer la vidéo](./assets/pb-media-video-toolbox-move-col2.png){width="500" zoomable="yes"}

## Supprimer une vidéo de l’étape

1. Passez la souris sur le conteneur vidéo pour afficher la boîte à outils et sélectionnez l’icône _Supprimer_ (![Supprimer l’icône](./assets/pb-icon-remove.png)).

1. Lorsque vous êtes invité à confirmer l’opération, cliquez sur **[!UICONTROL OK]**.

[1]: https://www.youtube.com/
[2]: https://vimeo.com/
