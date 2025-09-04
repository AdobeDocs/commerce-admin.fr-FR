---
title: Disposition - Colonne
description: Découvrez le type de contenu de colonne, utilisé pour diviser une page en plusieurs colonnes au cours de l [!DNL Page Builder] étape.
exl-id: 9701e1b5-3584-4602-9512-051567274f21
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '1574'
ht-degree: 0%

---

# Disposition - Colonne

Utilisez le type de contenu _Colonne_ pour diviser une page en plusieurs colonnes dans la [[!DNL Page Builder] étape](workspace.md#stage). Lorsque vous ajoutez une colonne à une ligne ou un onglet ou directement à la phase, le groupe de colonnes est initialement divisé en deux colonnes de largeur égale. Vous pouvez ajouter ou supprimer des colonnes, si nécessaire. Vous pouvez redimensionner une colonne en faisant glisser la bordure entre deux colonnes. La largeur de la colonne suivante est ajustée pour remplir l’espace disponible dans la ligne, la tabulation ou l’étape. Une seule colonne étend toute la largeur de la scène ou de son conteneur.

![Ajout d’une colonne](./assets/pb-layout-column-add-drag-placeholder.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Mises à jour de la version 2.4.5

Les fonctionnalités de Page Builder sont mises à jour dans la version 2.4.5 afin que les utilisateurs utilisent désormais _[!DNL Columns]_comme conteneur parent pour les colonnes individuelles. Ce nouveau conteneur prend également en charge les propriétés pour l’arrière-plan et élimine la nécessité d’encapsuler les colonnes dans une ligne. Il réduit les balises inutiles et offre un contrôle plus fin de l’affichage et de l’expérience du storefront.

Vous pouvez modifier la disposition du conteneur de [!DNL Columns] en faisant glisser une colonne au-dessus ou en dessous d’autres colonnes du groupe et en les empilant. Cela ouvre une nouvelle variété de combinaisons de mises en page possibles qui peuvent être obtenues sans avoir besoin d’être personnalisées par les développeurs.

Regardez cette vidéo pour découvrir comment le conteneur [!DNL Columns] peut être utilisé pour affiner vos mises en page :

>[!VIDEO](https://video.tv.adobe.com/v/345828?quality=12&learn=on)

## Boîte à outils Colonnes

Chaque colonne comporte une boîte à outils d’options qui s’affiche lorsque vous pointez sur le conteneur.

| Outil | Icon | Description |
|--- |--- |--- |
| Déplacer | ![ Icône Déplacer ](./assets/pb-icon-move.png){width="25"} | Déplace la colonne et son contenu vers une autre position par rapport aux autres colonnes. |
| (libellé) | Colonne | Identifie le conteneur actuel sous forme d’une colonne. Pointez sur le conteneur de colonnes pour afficher la palette. |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} | Ouvre la page Modifier la colonne , qui permet de modifier les propriétés du conteneur. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="25"} | Effectue une copie de la colonne active. |
| Supprimer | ![Icône Supprimer](./assets/pb-icon-remove.png){width="25"} | Supprime la colonne courante et son contenu. |

{style="table-layout:auto"}

## Grille de colonne

Le [grid](workspace.md) garantit que le contenu est aligné de manière cohérente dans une colonne et permet à la page de s’afficher correctement sur les ordinateurs de bureau et les appareils mobiles. Pour plus d’informations, consultez la section [Outils de contenu avancés](setup.md) de la configuration [!DNL Page Builder].

![Divisions de grille sur une ligne avec une colonne](./assets/pb-layout-column-one-grid.png){width="500" zoomable="yes"}

Dans l’exemple à deux colonnes suivant, les nombres entre parenthèses (6/12) dans la bordure supérieure de chaque conteneur de colonne indiquent le nombre de divisions de la grille dans chaque colonne et le nombre total de divisions. Dans ce cas, la colonne est la largeur de six unités de grille sur un total de 12.

![Divisions de grille sur une ligne avec deux colonnes](./assets/pb-layout-column-two-grid.png){width="600" zoomable="yes"}

## Ajouter une colonne

1. Dans le panneau [!DNL Page Builder] sous _[!UICONTROL Layout]_, faites glisser un **[!UICONTROL Column]**vers la scène.

   ![Faire glisser une colonne vers l’étape](./assets/pb-layout-column-add-drag-placeholder.png){width="600" zoomable="yes"}

   Le groupe de colonnes est maintenant divisé en deux colonnes de largeur égale. Chaque colonne est un conteneur distinct pour le contenu et possède son propre jeu d’options de boîte à outils.

   ![Deux colonnes égales](./assets/pb-layout-columns-two-empty.png){width="600" zoomable="yes"}

1. Dans le coin supérieur gauche du groupe de colonnes, cliquez sur l’outil _Grille_ (![Contrôle de grille](./assets/pb-icon-grid-control.png)) et ajustez la taille de la grille selon vos besoins.

   Le positionnement du contenu sur la grille permet d’aligner le contenu de manière cohérente et d’effectuer correctement le rendu de la page sur les ordinateurs de bureau et les appareils mobiles. Pour plus d’informations, consultez la section [Outils de contenu avancés](../configuration-reference/general/content-management.md) de la configuration [!DNL Page Builder].

   ![Divisions de grille sur deux colonnes](./assets/pb-layout-column-two-grid.png){width="600" zoomable="yes"}

## Redimensionnement d’une colonne

1. Passez la souris sur la bordure entre deux colonnes.

   La bordure est mise en surbrillance et la boîte à outils de la colonne sélectionnée s’affiche.

   ![Bordure en surbrillance entre deux colonnes](./assets/pb-column-resize-border.png){width="600" zoomable="yes"}

1. Maintenez le bouton de la souris enfoncé pour afficher la grille et faites glisser la bordure vers un nouvel emplacement sur la grille.

   La largeur des deux colonnes s’ajuste pour refléter la modification. La nouvelle largeur de chaque colonne apparaît après le libellé, par exemple `4/12` (quatre sur 12) et `8/12` (huit sur 12).

   ![Colonnes redimensionnées](./assets/pb-columns-resized-grid.png){width="600" zoomable="yes"}

## Supprimer une colonne

1. Pointez sur la colonne à supprimer pour afficher la boîte à outils et choisissez l’icône _Supprimer_ ( ![Icône Supprimer](./assets/pb-icon-remove.png){width="20"} ).

   ![Boîte à outils Colonnes](./assets/pb-column-toolbox-remove.png){width="600" zoomable="yes"}

1. Si la colonne contient du contenu, cliquez sur **[!UICONTROL OK]** pour confirmer.

   Pour accélérer le processus à l’avenir, vous pouvez ignorer l’étape de confirmation en cochant la case **[!UICONTROL Do not show this again]** .

   Le groupe de colonnes comporte désormais une seule colonne (12/12) et une grille. Étant donné que la grille n’est disponible que pour les colonnes, vous pouvez utiliser cette technique pour afficher la grille.

   ![Colonne simple avec grille](./assets/pb-column-single-grid.png){width="600" zoomable="yes"}

1. Si vous souhaitez que le groupe de colonnes étende la colonne restante à toute la largeur de la ligne ou de l’étape :

   - Pointez sur la colonne pour afficher la boîte à outils et sélectionnez l’icône _Paramètres_ ( ![icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

   - Faites défiler l’écran jusqu’à la section _[!UICONTROL Advanced]_et définissez les quatre valeurs **[!UICONTROL Padding]**sur `0`.

     ![Utilisation d’une marge intérieure nulle](./assets/pb-tutorial1-row-settings-advanced-margins-padding-zero.png){width="600" zoomable="yes"}

   - Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]** pour fermer la page _[!UICONTROL Edit Column]_.

1. Cliquez sur l’icône _Fermer le plein écran_ ( ![Icône Fermer le plein écran](./assets/pb-icon-reduce.png){width="20"} ) dans le coin supérieur droit de l’espace de travail, puis cliquez sur **[!UICONTROL Save]** dans le coin supérieur droit.

## Modifier les paramètres de colonne

1. Pointez sur la colonne pour afficher la boîte à outils et sélectionnez l’icône _Paramètres_ ( ![icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

   ![Boîte à outils Colonnes](./assets/pb-column-toolbox-settings.png){width="600" zoomable="yes"}

1. Modifiez les paramètres de **[!UICONTROL Appearance]** selon vos besoins.

   - Choisissez le paramètre d’alignement qui détermine la position de la colonne par rapport à son conteneur.

     | Option | Description |
     | ------ | ----------- |
     | `Full Height` | La colonne étend toute la hauteur de son conteneur. |
     | `Top Aligned` | La colonne est alignée en haut de son conteneur. |
     | `Centered` | La colonne est centrée au milieu de son conteneur. |
     | `Bottom Aligned` | La colonne est alignée au bas de son conteneur. |

     {style="table-layout:auto"}

   - Si nécessaire, saisissez le **[!UICONTROL Minimum Height]** de la colonne. Par exemple, vous pouvez définir la hauteur minimale pour qu’elle corresponde à la hauteur d’une image d’arrière-plan.

   - Si vous définissez la hauteur minimale, définissez la **[!UICONTROL Vertical Alignment]** pour contrôler la position des conteneurs de contenu qui sont ajoutés à la colonne (`Top`, `Center` ou `Bottom`).

1. Modifiez l’arrière-plan du contenu de la colonne.

   - **[!UICONTROL Background Color]** - Spécifiez la couleur en choisissant un échantillon, en cliquant sur le sélecteur de couleurs ou en saisissant un nom de couleur valide ou une valeur hexadécimale équivalente. Ce paramètre détermine la couleur d’arrière-plan de la colonne.

   - **[!UICONTROL Background Image]** - Si nécessaire, utilisez les outils fournis pour choisir une image d’arrière-plan à appliquer à la colonne :

     | Outil | Description |
     | ------ | ----------- |
     | [!UICONTROL Upload] | Télécharge un fichier image de votre ordinateur local dans la galerie, puis l’applique en tant qu’image d’arrière-plan de la colonne. |
     | [!UICONTROL Select from Gallery] | Vous invite à choisir une image existante de la galerie comme image d’arrière-plan pour la colonne. |
     | ![ Icône Appareil photo ](./assets/pb-icon-camera.png){width="25"} | Vous permet de faire glisser l’image vers la mosaïque de la caméra ou d’accéder à l’image dans votre système de fichiers local. |

     {style="table-layout:auto"}

   - **[!UICONTROL Background Mobile Image]** - Si nécessaire, utilisez les mêmes outils pour choisir une image d’arrière-plan différente à utiliser pour l’affichage sur les appareils mobiles.

   - **[!UICONTROL Background Size]** - Modifiez ce paramètre pour déterminer la mise à l’échelle de l’image d’arrière-plan par rapport à la largeur de la colonne :

     | Option | Description |
     | ------ | ----------- |
     | `Cover` | L’image d’arrière-plan couvre toute la largeur de la colonne. |
     | `Contain` | L’image d’arrière-plan est limitée à la largeur de la zone de contenu. |
     | `Auto` | Applique la taille d’arrière-plan par défaut spécifiée dans la feuille de style du thème actif. |

     {style="table-layout:auto"}

   - **[!UICONTROL Background Position]** - Modifiez ce paramètre pour déterminer le point d’ancrage de l’image par rapport à la colonne. Options : `Top Left`, `Top Center`, `Top Right`, `Center Left`, `Center`, `Center Right`, `Bottom Left`, `Bottom Center` ou `Bottom Right`

   - **[!UICONTROL Background Attachment]** - Modifiez ce paramètre pour déterminer le déplacement de l’image d’arrière-plan par rapport à la page de défilement :

     | Option | Description |
     | ------ | ----------- |
     | `Scroll` | L’image d’arrière-plan est synchronisée pour se déplacer vers le bas lors du défilement de la page. |
     | `Fixed` | (Non disponible pour les appareils mobiles) L’image d’arrière-plan ne se déplace pas lorsque le conteneur défile sur l’image et est fixe à la position d’arrière-plan spécifiée. |

     {style="table-layout:auto"}

   - **[!UICONTROL Background Repeat]** - Si vous souhaitez répéter l’image d’arrière-plan pour remplir l’espace, modifiez `Yes` ce paramètre.

1. Mettez à jour les paramètres _[!UICONTROL Advanced]_selon vos besoins.

   - Pour contrôler le positionnement horizontal des conteneurs de contenu ajoutés à la colonne, choisissez une **[!UICONTROL Alignment]** :

     | Option | Description |
     | ------ | ----------- |
     | `Default` | Applique le paramètre d’alignement par défaut spécifié dans la feuille de style du thème actif. |
     | `Left` | Aligne les conteneurs de contenu le long de la bordure gauche du conteneur de colonne, en tenant compte de la marge intérieure spécifiée. |
     | `Center` | Aligne le conteneur de contenu au centre du conteneur de colonne, en tenant compte de la marge intérieure spécifiée. |
     | `Right` | Aligne le conteneur de contenu le long de la bordure droite du conteneur de colonne, en tenant compte de la marge intérieure spécifiée. |

     {style="table-layout:auto"}

   - Définissez le style de **[!UICONTROL Border]**, qui est appliqué aux quatre côtés du conteneur de colonne :

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

   - (Facultatif) Spécifiez les noms des **[!UICONTROL CSS classes]** de la feuille de style actuelle à appliquer au conteneur de colonnes.

     Séparez plusieurs noms de classe par un espace.

   - Saisissez les valeurs, en pixels, du **[!UICONTROL Margins and Padding]** pour spécifier les marges extérieures et la marge intérieure de la colonne.

     Saisissez chaque valeur correspondante dans le diagramme de conteneur de colonnes.

     | Zone conteneur | Description |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | Quantité d’espace vide appliqué au bord extérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | Quantité d’espace vide appliqué au bord intérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

<!-- Last updated from includes: 2023-01-19 14:32:13 -->
