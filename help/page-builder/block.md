---
title: Ajouter du contenu - Bloc
description: Découvrez le type de contenu Bloc utilisé pour ajouter un bloc réutilisable à l’étape  [!DNL Page Builder] .
exl-id: fcedb125-e0c8-4b59-bd26-7f3912e0db2a
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Ajouter du contenu - Bloc

Utilisez le type de contenu _Block_ pour ajouter un [block](../content-design/blocks.md) existant et actif à l’ [[!DNL Page Builder] étape](workspace.md#stage). Dans l&#39;exemple suivant, la première colonne contient le bloc avec un menu latéral pour la page. La deuxième colonne contient une image.

![Bloc avec un menu latéral](./assets/pb-add-content-block-example.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Blocage d’outil

| Outil | Icône | Description |
| --------- | -------- | ------------- |
| Déplacer | ![Icône Déplacer](./assets/pb-icon-move.png) | Déplace le conteneur de blocs et son contenu vers une autre position sur la scène. |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png) | Ouvre la page Modifier le bloc, dans laquelle vous pouvez sélectionner le bloc, et modifier les propriétés du conteneur. |
| Masquer | ![Icône Masquer](./assets/pb-icon-hide.png) | Masque le conteneur de blocs actif et son contenu. |
| Afficher | ![Icône Afficher](./assets/pb-icon-show.png) | Affiche le conteneur de blocs masqué et son contenu. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png) | Effectue une copie du conteneur de blocs et de son contenu. |
| Supprimer | ![Supprimer l’icône](./assets/pb-icon-remove.png) | Supprime le conteneur de blocs et son contenu de la scène. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Ajouter un bloc existant

1. Accédez à l’espace de travail [!DNL Page Builder] sur la page cible, le bloc, le bloc dynamique, le produit ou la catégorie.

1. Dans le panneau [!DNL Page Builder], développez **[!UICONTROL Add Content]** et faites glisser un espace réservé **[!UICONTROL Block]** sur la scène.

   ![Faire glisser un bloc sur la scène](./assets/pb-add-content-block-drag.png){width="600" zoomable="yes"}

1. Passez la souris sur le conteneur de blocs vide pour afficher la boîte à outils et sélectionnez l’icône _Paramètres_ ( ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} ).

1. Cliquez sur **[!UICONTROL Select Block]**.

   ![Sélectionner un bloc](./assets/pb-add-content-block-select.png){width="200"}

1. Dans la ligne du bloc que vous souhaitez ajouter, cliquez sur **[!UICONTROL Select]** dans la dernière colonne.

   ![Bloc sélectionné](./assets/pb-add-content-block-selected.png){width="600" zoomable="yes"}

   Le nom du bloc sélectionné apparaît sur la page.

   ![Nom du bloc](./assets/pb-add-content-block-name.png){width="200"}

1. Définissez les autres paramètres si nécessaire, à l’aide des descriptions de champ à la fin de cette page à titre de référence.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

### Paramètres avancés

1. Pour contrôler le positionnement du bloc dans le conteneur parent, choisissez un **[!UICONTROL Alignment]** :

   | Option | Description |
   | ------ | ----------- |
   | `Default` | Applique le paramètre d’alignement par défaut spécifié dans la feuille de style du thème actif. |
   | `Left` | Aligne la liste le long de la bordure gauche du conteneur parent, en tenant compte de toute marge intérieure spécifiée. |
   | `Center` | Aligne la liste au centre du conteneur parent, en tenant compte de toute marge intérieure spécifiée. |
   | `Right` | Aligne le bloc le long de la bordure droite du conteneur parent, en tenant compte de toute marge intérieure spécifiée. |

   {style="table-layout:auto"}

1. Définissez un style **[!UICONTROL Border]** appliqué aux quatre côtés du conteneur de blocs :

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

1. Si vous définissez un style de bordure autre que `None`, renseignez les options d’affichage de la bordure :

   | Option | Description |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Définissez la couleur en choisissant un échantillon, en cliquant sur le sélecteur de couleurs ou en saisissant un nom de couleur valide ou une valeur hexadécimale équivalente. |
   | [!UICONTROL Border Width] | Saisissez le nombre de pixels pour la largeur de la ligne de bordure. |
   | [!UICONTROL Border Radius] | Saisissez le nombre de pixels pour définir la taille du rayon utilisé pour arrondir chaque coin de la bordure. |

   {style="table-layout:auto"}

1. (Facultatif) Indiquez les noms de **[!UICONTROL CSS classes]** dans la feuille de style actuelle à appliquer au conteneur.

   Séparez plusieurs noms de classe par un espace.

1. Saisissez des valeurs, en pixels, pour le **[!UICONTROL Margins and Padding]** afin de déterminer les marges extérieures et la marge intérieure du conteneur de blocs.

   Saisissez les valeurs correspondantes dans le diagramme.

   | Zone de conteneur | Description |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | Espace vide appliqué au bord extérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Espace blanc appliqué au bord intérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

## Modification des paramètres de bloc

1. Passez la souris sur le conteneur de blocs et sélectionnez l’icône _Paramètres_ ( ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} ) dans la boîte à outils.

   ![Bloc d’outils](./assets/pb-add-content-block-toolbox.png){width="600" zoomable="yes"}

1. Pour choisir un autre bloc, cliquez sur **[!UICONTROL Select Block]**.

   - Dans la liste des blocs actifs, cliquez sur **[!UICONTROL Select]** le bloc que vous souhaitez ajouter.
   - Cliquez sur **[!UICONTROL Add Selected]**.

1. Mettez à jour les paramètres restants si nécessaire, à l’aide des descriptions de champ à la fin de cette page à titre de référence.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

## Dupliquer un bloc

1. Pointez sur le conteneur de blocs pour afficher la boîte à outils et sélectionnez l’icône _Dupliquer_ (![Icône Dupliquer](./assets/pb-icon-duplicate.png)).

   Le doublon apparaît juste en dessous de l’original.

1. Pour déplacer le nouveau bloc vers une nouvelle position, passez la souris sur le conteneur, puis cliquez sur _Déplacer_ (![Icône Déplacer](./assets/pb-icon-move.png)) dans la boîte à outils.

1. Sélectionnez le bloc et faites-le glisser jusqu’à ce que la ligne directrice rouge apparaisse à la nouvelle position.

   Les bordures supérieure et inférieure de chaque conteneur apparaissent sous la forme de lignes en pointillés lorsque le bloc est déplacé.

## Supprimer un bloc de l’étape

1. Pointez sur le conteneur de blocs pour afficher la boîte à outils et sélectionnez l’icône _Supprimer_ (![Icône Supprimer](./assets/pb-icon-remove.png)).

1. Lorsque vous êtes invité à confirmer l’opération, cliquez sur **[!UICONTROL OK]**.
