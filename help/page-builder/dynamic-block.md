---
title: Ajouter du contenu - Bloc dynamique
description: Découvrez le type de contenu Bloc dynamique utilisé pour ajouter un bloc dynamique réutilisable au [!DNL Page Builder] scène.
exl-id: 04c90f47-9e32-4d34-ac0d-a2f2cec95ffc
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 0%

---

# Ajouter du contenu - Bloc dynamique

Utilisez le type de contenu Bloc dynamique pour ajouter une [bloc dynamique](../content-design/dynamic-blocks.md) à la fonction [[!DNL Page Builder] étape](workspace.md#stage).

![Bloc dynamique sur la vitrine](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Boîte à outils Bloc dynamique

| Outil | Icône | Description |
| --------- | ------------- | ----------------- |
| Déplacer | ![Icône Déplacer](./assets/pb-icon-move.png){width="25"} | Déplace le conteneur de blocs et son contenu vers une autre position sur la scène. |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} | Ouvre la _Modifier le bloc_ , où vous pouvez choisir le bloc et modifier les propriétés du conteneur. |
| Masquer | ![Icône Masquer](./assets/pb-icon-hide.png){width="25"} | Masque le conteneur de blocs actif et son contenu. |
| Afficher | ![Icône Afficher](./assets/pb-icon-show.png){width="25"} | Affiche le conteneur de blocs masqué et son contenu. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="25"} | Effectue une copie du conteneur de blocs et de son contenu. |
| Supprimer | ![Icône Supprimer](./assets/pb-icon-remove.png){width="25"} | Supprime le conteneur de blocs et son contenu de la scène. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Ajouter un bloc dynamique existant à l’étape

1. Accédez au [!DNL Page Builder] espace de travail sur la page cible, le bloc, le produit ou la catégorie.

1. Dans le [!DNL Page Builder] panneau, développer **[!UICONTROL Add Content]** et faites glisser un **[!UICONTROL Dynamic Block]** espace réservé sur la scène.

   ![Glissement d’un espace réservé de bloc dynamique vers l’étape](./assets/pb-dynamic-block-drag.png){width="600" zoomable="yes"}

1. Passez la souris sur le conteneur de blocs dynamiques vide pour afficher la boîte à outils et sélectionner l’option _Paramètres_ ( ![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

   ![Boîte à outils Bloc dynamique](./assets/pb-dynamic-block-settings.png){width="600" zoomable="yes"}

1. Sur le _Modifier le bloc dynamique_ page, cliquez sur **[!UICONTROL Select Dynamic Block]** et utilisez la liste pour sélectionner le bloc.

   ![Sélectionner un bloc dynamique](./assets/pb-dynamic-block-select.png){width="600" zoomable="yes"}

   Dans la liste, recherchez le bloc dynamique à insérer, puis cliquez sur **[!UICONTROL Select]**. Cliquez ensuite sur **[!UICONTROL Add Selected]**.

   ![Sélectionner un bloc dynamique dans la liste](./assets/pb-add-content-dynamic-block-select-list.png){width="600" zoomable="yes"}

   Un résumé des informations du bloc dynamique apparaît ci-dessous.

   ![Résumé des blocs dynamiques](./assets/pb-add-content-dynamic-block-summary.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Template]** à l’une des options suivantes :

   | Option | Description |
   | ------ | ----------- |
   | `Dynamic Block Block Template` | Ajoute un bloc autonome. |
   | `Dynamic Block Inline Template` | Insère le contenu du bloc dans le texte. |

   {style="table-layout:auto"}

   ![Modèle de bloc dynamique](./assets/pb-add-content-dynamic-block-template.png){width="200"}

1. Définissez les Paramètres avancés selon vos besoins.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir au [!DNL Page Builder] workspace.

### Paramètres avancés

1. Pour contrôler le positionnement du bloc dynamique dans le conteneur parent, sélectionnez une **[!UICONTROL Alignment]**:

   | Option | Description |
   | ------ | ----------- |
   | `Default` | Applique le paramètre d’alignement par défaut spécifié dans la feuille de style du thème actif. |
   | `Left` | Aligne la liste le long de la bordure gauche du conteneur parent, en tenant compte de toute marge intérieure spécifiée. |
   | `Center` | Aligne la liste au centre du conteneur parent, en tenant compte de toute marge intérieure spécifiée. |
   | `Right` | Aligne le bloc le long de la bordure droite du conteneur parent, en tenant compte de toute marge intérieure spécifiée. |

   {style="table-layout:auto"}

1. Définissez la variable **[!UICONTROL Border]** style appliqué aux quatre côtés du conteneur de blocs dynamiques :

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

1. Si vous définissez un style de bordure autre que `None`, renseignez les options d’affichage des bordures :

   | Option | Description |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Définissez la couleur en choisissant un échantillon, en cliquant sur le sélecteur de couleurs ou en saisissant un nom de couleur valide ou une valeur hexadécimale équivalente. |
   | [!UICONTROL Border Width] | Saisissez le nombre de pixels pour la largeur de la ligne de bordure. |
   | [!UICONTROL Border Radius] | Saisissez le nombre de pixels pour définir la taille du rayon utilisé pour arrondir chaque coin de la bordure. |

   {style="table-layout:auto"}

1. (Facultatif) Indiquez les noms des **[!UICONTROL CSS classes]** de la feuille de style actuelle à appliquer au conteneur.

   Séparez plusieurs noms de classe par un espace.

1. Saisissez des valeurs, en pixels, pour la variable **[!UICONTROL Margins and Padding]** pour déterminer les marges extérieures et la marge intérieure du conteneur de blocs dynamiques.

   Saisissez les valeurs correspondantes dans le diagramme.

   | Zone de conteneur | Description |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | Espace vide appliqué au bord extérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Espace blanc appliqué au bord intérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

## Modification des paramètres du conteneur de blocs dynamique

1. Passez la souris sur le conteneur de blocs dynamiques pour afficher la boîte à outils et sélectionner l’option _Paramètres_ ( ![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

   ![Boîte à outils Bloc dynamique](./assets/pb-add-content-dynamic-block-toolbox.png){width="500" zoomable="yes"}

1. Si nécessaire, modifiez le bloc dynamique :

   - Cliquez sur **[!UICONTROL Select Dynamic Block]**.

     ![Sélectionner un autre bloc dynamique](./assets/pb-add-content-dynamic-block-select.png){width="20"}

   - Dans la liste des blocs dynamiques actifs, cliquez sur **[!UICONTROL Select]** pour le bloc que vous souhaitez ajouter.

1. Mettez à jour les paramètres restants si nécessaire.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir au [!DNL Page Builder] workspace.

## Dupliquer un bloc dynamique

1. Passez la souris sur le conteneur de blocs dynamiques pour afficher la boîte à outils et sélectionner l’option _Dupliquer_ ( ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="20"} ).

   Le doublon apparaît juste en dessous de l’original.

   ![Duplication d&#39;un bloc dynamique](./assets/pb-add-content-dynamic-block-duplicate.png){width="500" zoomable="yes"}

1. Pour déplacer le nouveau bloc dynamique vers une autre position, passez la souris sur son conteneur, puis choisissez _Déplacer_ ( ![Icône Déplacer](./assets/pb-icon-move.png){width="20"} ) dans la boîte à outils.

1. Sélectionnez le bloc dynamique et faites-le glisser jusqu&#39;à ce que la ligne directrice rouge apparaisse à la nouvelle position.

   Les bordures supérieure et inférieure de chaque conteneur apparaissent sous la forme de lignes en pointillés lorsque le bloc dynamique est déplacé.

## Suppression d’un bloc dynamique de la scène

1. Passez la souris sur le conteneur de blocs dynamiques pour afficher la boîte à outils et sélectionner l’option _Supprimer_ ( ![Icône Supprimer](./assets/pb-icon-remove.png){width="20"} ).

1. Lorsque vous y êtes invité, cliquez sur **[!UICONTROL OK]**.
