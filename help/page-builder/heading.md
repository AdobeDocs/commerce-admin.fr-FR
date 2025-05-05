---
title: Éléments - En-tête
description: Découvrez le type de contenu En-tête , utilisé pour ajouter un conteneur de texte avec un niveau d’en-tête de H1 à H6 à l’étape  [!DNL Page Builder] .
exl-id: dc51e7f6-a235-49dc-a978-1419a63fa33e
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# Éléments - En-tête

Les niveaux d’en-tête établissent une hiérarchie qui organise le contenu et aide les moteurs de recherche à indexer chaque page. Utilisez le type de contenu _Heading_ dans l’ [[!DNL Page Builder] stage](workspace.md#stage) pour ajouter un conteneur de texte avec un niveau d’en-tête de H1 à H6 à l’étape. Les en-têtes sont formatés selon la feuille de style associée au thème actif.

Le champ [En-tête de contenu](workspace.md) de la section _[!UICONTROL Content]_&#x200B;peut être utilisé pour ajouter un en-tête H1 en haut de la page. Cependant, le champ est hérité des versions précédentes de [!DNL Commerce] et est fourni pour prendre en charge le contenu plus ancien. Ce champ ne tire pas parti des fonctionnalités avancées de [!DNL Page Builder]. Il est recommandé de laisser le champ En-tête de contenu vide et d’utiliser le type de contenu En-tête [!DNL Page Builder] pour ajouter des en-têtes de n’importe quel niveau à la page.

L’exemple suivant illustre l’affichage de l’en-tête de contenu et du type de contenu En-tête lors du formatage par le thème Luma.

![Niveaux d’en-tête et d’en-tête de contenu sur le storefront](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

Vous pouvez faire glisser un en-tête de la section _Eléments_ du panneau [!DNL Page Builder] vers une ligne, une colonne ou un ensemble d’onglets sur la scène. Le niveau d’en-tête et l’alignement peuvent être contrôlés à partir de la barre d’outils de l’éditeur sur l’étape, ou à l’aide de la commande _Paramètres_ ( ![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

{{$include /help/_includes/page-builder-save-timeout.md}}

## Éditeur d’en-tête

![Éditeur d’en-tête avec barre d’outils](./assets/pb-elements-heading-toolbar.png){width="500" zoomable="yes"}

## Barre d’outils Conteneur d’en-tête

Comme pour tous les conteneurs de contenu, la boîte à outils s’affiche lorsque vous placez le pointeur de la souris sur le conteneur.

![Boîte à outils du conteneur d’en-tête](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

| Outil | Icône | Description |
| --------- | ----------------- | ---------------------- |
| Déplacer | ![Icône Déplacer](./assets/pb-icon-move.png){width="25"} | Déplace le conteneur d’en-têtes vers un autre emplacement valide sur la page. |
| (label) | En-tête | Identifie le conteneur actif comme en-tête. |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} | Ouvre la page Modifier l’en-tête dans laquelle vous pouvez modifier les propriétés du conteneur. |
| Masquer | ![Icône Masquer](./assets/pb-icon-hide.png){width="25"} | Masque le conteneur d’en-tête. |
| Afficher | ![Icône Afficher](./assets/pb-icon-show.png){width="25"} | Affiche le conteneur d’en-têtes masqué. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="25"} | Effectue une copie du conteneur d’en-tête. |
| Supprimer | ![Supprimer l’icône](./assets/pb-icon-remove.png){width="25"} | Supprime le conteneur d’en-têtes et son contenu de la scène. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Ajouter un en-tête

1. Dans le panneau [!DNL Page Builder], développez **[!UICONTROL Elements]** et faites glisser un espace réservé **[!UICONTROL Heading]** sur une ligne, une colonne ou un ensemble d’onglets sur la scène.

   ![Faire glisser un en-tête vers l’étape](./assets/pb-elements-heading-drag.png){width="600" zoomable="yes"}

1. Dans l’éditeur, saisissez le texte de titre sur l’espace réservé `Edit Heading Text`.

   Par défaut, le texte de l’en-tête se voit attribuer un type d’en-tête de niveau 2 (H2).

   ![Espace réservé dans l’éditeur d’en-tête](./assets/pb-elements-header-editor-placeholder.png){width="500" zoomable="yes"}

1. Dans la barre d’outils, choisissez le type d’en-tête approprié entre H1 et H6.

1. Modifiez l’alignement, si nécessaire.

## Modification des paramètres d’en-tête

1. Pointez sur le conteneur d’en-tête pour afficher la boîte à outils et sélectionnez l’icône _Paramètres_ ( ![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

   ![Boîte à outils d’en-tête](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

1. Si nécessaire, mettez à jour le contenu de l’en-tête (**[!UICONTROL Heading Type]** et **[!UICONTROL Heading Text]**).

   Vous pouvez également mettre à jour ce contenu dans l’éditeur d’en-tête.

1. Mettez à jour les paramètres _[!UICONTROL Advanced]_&#x200B;si nécessaire.

   - Pour contrôler le positionnement de l’en-tête dans le conteneur parent, choisissez un **[!UICONTROL Alignment]** :

     | Option | Description |
     | ------ | ----------- |
     | `Default` | Applique le paramètre d’alignement par défaut spécifié dans la feuille de style du thème actif. |
     | `Left` | Aligne la liste le long de la bordure gauche du conteneur parent, en tenant compte de toute marge intérieure spécifiée. |
     | `Center` | Aligne la liste au centre du conteneur parent, en tenant compte de toute marge intérieure spécifiée. |
     | `Right` | Aligne le bloc le long de la bordure droite du conteneur parent, en tenant compte de toute marge intérieure spécifiée. |

     {style="table-layout:auto"}

   - Définissez le style **[!UICONTROL Border]** appliqué aux quatre côtés du conteneur d’en-tête :

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

     | Option | Description |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Définissez la couleur en choisissant un échantillon, en cliquant sur le sélecteur de couleurs ou en saisissant un nom de couleur valide ou une valeur hexadécimale équivalente. |
     | [!UICONTROL Border Width] | Saisissez le nombre de pixels pour la largeur de la ligne de bordure. |
     | [!UICONTROL Border Radius] | Saisissez le nombre de pixels pour définir la taille du rayon utilisé pour arrondir chaque coin de la bordure. |

     {style="table-layout:auto"}

   - (Facultatif) Indiquez les noms de **[!UICONTROL CSS classes]** dans la feuille de style actuelle à appliquer au conteneur.

     Séparez plusieurs noms de classe par un espace.

   - Saisissez des valeurs, en pixels, pour le **[!UICONTROL Margins and Padding]** afin de déterminer les marges extérieures et la marge intérieure du conteneur d’en-tête.

     Saisissez les valeurs correspondantes dans le diagramme.

     | Zone de conteneur | Description |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | Espace vide appliqué au bord extérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | Espace blanc appliqué au bord intérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

## Dupliquer un en-tête

Pour un en-tête formaté avec des paramètres spécifiques, il est plus efficace de le dupliquer plutôt que de recommencer avec un nouvel espace réservé.

1. Pointez sur le conteneur d’en-tête pour afficher la boîte à outils et sélectionnez l’icône _Dupliquer_ ( ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="20"} ).

   Le doublon apparaît juste en dessous de l’original.

   ![Duplication d’un conteneur d’en-tête](./assets/pb-elements-heading-duplicate.png){width="500" zoomable="yes"}

1. Pointez sur le nouveau conteneur d’en-tête pour afficher la boîte à outils et sélectionnez l’icône _Déplacer_ ( ![Icône Déplacer](./assets/pb-icon-move.png){width="20"} ).

   ![Déplacement d’un en-tête](./assets/pb-elements-heading-move.png){width="500" zoomable="yes"}

1. Sélectionnez l’en-tête et faites-le glisser jusqu’à ce que la ligne directrice rouge marque la nouvelle position.

   Les bordures supérieure et inférieure de chaque conteneur apparaissent sous forme de lignes tirets lorsque l’en-tête est déplacé.

   ![Déplacement de l’en-tête dupliqué en position](./assets/pb-elements-heading-move-guideline.png){width="500" zoomable="yes"}

1. Si vous souhaitez modifier le niveau d’en-tête, cliquez sur le texte de l’en-tête et choisissez le nouveau niveau dans la barre d’outils de l’éditeur.

   ![Choix d’un nouveau niveau d’en-tête](./assets/pb-elements-heading-change-heading-level.png){width="500" zoomable="yes"}
