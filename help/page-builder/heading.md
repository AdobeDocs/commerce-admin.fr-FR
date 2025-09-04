---
title: Éléments - En-tête
description: Découvrez le type de contenu Titre, utilisé pour ajouter un conteneur de texte avec un niveau d’en-tête compris entre H1 et H6 à l’ [!DNL Page Builder] .
exl-id: dc51e7f6-a235-49dc-a978-1419a63fa33e
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# Éléments - En-tête

Les niveaux d’en-tête établissent une hiérarchie qui organise le contenu et aide les moteurs de recherche à indexer chaque page. Utilisez le type de contenu _Titre_ dans le [[!DNL Page Builder] étape](workspace.md#stage) pour ajouter un conteneur de texte avec un niveau d’en-tête compris entre H1 et H6 à l’étape. Les en-têtes sont formatés en fonction de la feuille de style associée au thème actif.

Le champ [En-tête de contenu](workspace.md) de la section _[!UICONTROL Content]_&#x200B;peut être utilisé pour ajouter un en-tête H1 en haut de la page. Cependant, le champ est un héritage des versions [!DNL Commerce] précédentes et est fourni pour prendre en charge le contenu plus ancien. Ce champ ne tire pas parti des fonctionnalités avancées de [!DNL Page Builder]. Il est recommandé de laisser le champ En-tête de contenu vide et d’utiliser le type de contenu En-tête de [!DNL Page Builder] pour ajouter des en-têtes de n’importe quel niveau à la page.

L’exemple suivant montre comment l’en-tête de contenu et le type de contenu En-tête apparaissent lorsqu’ils sont formatés par le thème Luma .

![En-tête de contenu et niveaux d’en-tête sur le storefront](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

Vous pouvez faire glisser un en-tête de la section _Éléments_ du panneau [!DNL Page Builder] vers une ligne, une colonne ou un ensemble d’onglets sur la scène. Le niveau de titre et l&#39;alignement peuvent être contrôlés à partir de la barre d&#39;outils de l&#39;éditeur sur la scène ou à l&#39;aide de la commande _Paramètres_ ( ![icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

{{$include /help/_includes/page-builder-save-timeout.md}}

## Éditeur de titre

![Éditeur de titre avec barre d’outils](./assets/pb-elements-heading-toolbar.png){width="500" zoomable="yes"}

## Boîte à outils Conteneur d’en-têtes

Comme pour tous les conteneurs de contenu, la boîte à outils s’affiche lorsque vous pointez sur le conteneur.

![Boîte à outils Conteneur d’en-têtes](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

| Outil | Icon | Description |
| --------- | ----------------- | ---------------------- |
| Déplacer | ![ Icône Déplacer ](./assets/pb-icon-move.png){width="25"} | Déplace le conteneur d’en-tête vers un autre emplacement valide sur la page. |
| (libellé) | Titre | Identifie le conteneur actuel en tant qu’en-tête. |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} | Ouvre la page Modifier l’en-tête , qui permet de modifier les propriétés du conteneur. |
| Masquer | ![Icône Masquer](./assets/pb-icon-hide.png){width="25"} | Masque le conteneur d’en-tête. |
| Afficher | ![Afficher l’icône](./assets/pb-icon-show.png){width="25"} | Affiche le conteneur d’en-tête masqué. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="25"} | Crée une copie du conteneur d’en-tête. |
| Supprimer | ![Icône Supprimer](./assets/pb-icon-remove.png){width="25"} | Supprime le conteneur d’en-tête et son contenu de l’étape. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Ajouter un en-tête

1. Dans le panneau [!DNL Page Builder], développez **[!UICONTROL Elements]** et faites glisser un espace réservé **[!UICONTROL Heading]** vers une ligne, une colonne ou un ensemble d’onglets sur la scène.

   ![Faire glisser un titre vers l’étape](./assets/pb-elements-heading-drag.png){width="600" zoomable="yes"}

1. Dans l’éditeur, saisissez le texte d’en-tête au-dessus de l’espace réservé `Edit Heading Text`.

   Par défaut, le texte d’en-tête se voit attribuer un type d’en-tête de niveau 2 (H2).

   ![Espace réservé dans l’éditeur d’en-têtes](./assets/pb-elements-header-editor-placeholder.png){width="500" zoomable="yes"}

1. Dans la barre d’outils, choisissez le type d’en-tête approprié entre H1 et H6.

1. Modifiez l’alignement, si nécessaire.

## Modifier les paramètres d’en-tête

1. Pointez sur le conteneur d’en-tête pour afficher la boîte à outils et choisissez l’icône _Paramètres_ ( ![icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

   ![Boîte à outils Titre](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

1. Mettez à jour le contenu de l’en-tête (**[!UICONTROL Heading Type]** et **[!UICONTROL Heading Text]**) si nécessaire.

   Vous pouvez également mettre à jour ce contenu dans l’éditeur d’en-têtes.

1. Mettez à jour les paramètres _[!UICONTROL Advanced]_&#x200B;selon vos besoins.

   - Pour contrôler le positionnement de l’en-tête dans le conteneur parent, choisissez une **[!UICONTROL Alignment]** :

     | Option | Description |
     | ------ | ----------- |
     | `Default` | Applique le paramètre d’alignement par défaut spécifié dans la feuille de style du thème actif. |
     | `Left` | Aligne la liste le long de la bordure gauche du conteneur parent, en tenant compte de la marge intérieure spécifiée. |
     | `Center` | Aligne la liste au centre du conteneur parent, en tenant compte de la marge intérieure spécifiée. |
     | `Right` | Aligne le bloc le long de la bordure droite du conteneur parent, en tenant compte de la marge intérieure spécifiée. |

     {style="table-layout:auto"}

   - Définissez le style de **[!UICONTROL Border]** appliqué aux quatre côtés du conteneur d’en-tête :

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

     | Option | Description |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Spécifiez la couleur en choisissant une nuance, en cliquant sur le sélecteur de couleurs ou en saisissant un nom de couleur valide ou une valeur hexadécimale équivalente. |
     | [!UICONTROL Border Width] | Saisissez le nombre de pixels pour la largeur de la ligne de bordure. |
     | [!UICONTROL Border Radius] | Saisissez le nombre de pixels pour définir la taille du rayon utilisé pour arrondir chaque coin de la bordure. |

     {style="table-layout:auto"}

   - (Facultatif) Spécifiez les noms des **[!UICONTROL CSS classes]** de la feuille de style actuelle à appliquer au conteneur.

     Séparez plusieurs noms de classe par un espace.

   - Saisissez les valeurs, en pixels, du **[!UICONTROL Margins and Padding]** pour déterminer les marges extérieures et la marge intérieure du conteneur d’en-tête.

     Saisissez les valeurs correspondantes dans le diagramme.

     | Zone conteneur | Description |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | Quantité d’espace vide appliqué au bord extérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | Quantité d’espace vide appliqué au bord intérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

## Dupliquer un en-tête

Pour un en-tête formaté avec des paramètres spécifiques, il est plus efficace de dupliquer l’en-tête plutôt que de recommencer avec un nouvel espace réservé.

1. Pointez sur le conteneur d’en-tête pour afficher la boîte à outils et choisissez l’icône _Dupliquer_ ( ![icône Dupliquer](./assets/pb-icon-duplicate.png){width="20"} ).

   Le duplicata apparaît juste en dessous de l’original.

   ![Duplication d’un conteneur d’en-tête](./assets/pb-elements-heading-duplicate.png){width="500" zoomable="yes"}

1. Pointez sur le nouveau conteneur d’en-tête pour afficher la boîte à outils et choisissez l’icône _Déplacer_ ( ![Icône Déplacer](./assets/pb-icon-move.png){width="20"} ).

   ![Déplacer un en-tête](./assets/pb-elements-heading-move.png){width="500" zoomable="yes"}

1. Sélectionnez et faites glisser le titre jusqu&#39;à ce que la ligne directrice rouge marque la nouvelle position.

   Les bordures supérieure et inférieure de chaque conteneur apparaissent sous forme de lignes en tirets lorsque le titre est déplacé.

   ![Mise en position du titre dupliqué](./assets/pb-elements-heading-move-guideline.png){width="500" zoomable="yes"}

1. Si vous souhaitez modifier le niveau de titre, cliquez sur le texte du titre et choisissez le nouveau niveau dans la barre d&#39;outils de l&#39;éditeur.

   ![Choix d’un nouveau niveau d’en-tête](./assets/pb-elements-heading-change-heading-level.png){width="500" zoomable="yes"}

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
