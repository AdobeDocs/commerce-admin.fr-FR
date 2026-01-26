---
title: Disposition - Onglets
description: Découvrez le type de contenu Onglets, utilisé pour ajouter un ensemble d’onglets dans l’étape [!DNL Page Builder] du .
exl-id: e83d248d-7cf3-4ccc-a03d-ede32c7e71ae
feature: Page Builder, Page Content
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '2039'
ht-degree: 0%

---

# Disposition - Onglets

Utilisez le type de contenu _Onglets_ pour ajouter un ensemble d’onglets à la [[!DNL Page Builder] étape](workspace.md#stage). Lorsque vous faites glisser l’espace réservé Onglets du panneau à la scène, un seul onglet par défaut s’affiche initialement. Vous pouvez ajouter d’autres onglets pour créer un ensemble complet. La largeur de l’ensemble d’onglets est déterminée par la largeur de son conteneur parent et par les paramètres de remplissage.

![Ensemble d’onglets](./assets/pb-layout-tab-example.png){width="500" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Boîte à outils

Lorsque vous utilisez le type de contenu _Onglets_, vous ajoutez et modifiez des onglets individuels et le conteneur d’onglets qui contient un ou plusieurs onglets. Chaque onglet possède sa propre boîte à outils que vous utilisez pour concevoir des onglets sur l’étape de [!DNL Page Builder].

### Boîte à outils Onglet individuel

![Boîte à outils Onglet](./assets/pb-layout-tab1-toolbox.png){width="500" zoomable="yes"}

| Outil | Icon | Description |
|--- |--- |--- |
| Déplacer | ![ Icône Déplacer ](./assets/pb-icon-move.png){width="25"} | Cette commande en regard du libellé de l’onglet est utilisée pour déplacer l’onglet individuel vers une autre position dans l’ensemble d’onglets. |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} | Ouvre la page Modifier les onglets, qui permet de modifier les propriétés de chaque onglet. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="25"} | Effectue une copie de l’onglet. |
| Supprimer | ![Icône Supprimer](./assets/pb-icon-remove.png){width="25"} | Supprime l’onglet du jeu d’onglets. |

{style="table-layout:auto"}

### Boîte à outils Conteneur d’onglets

![Boîte à outils Conteneur d’onglets](./assets/pb-tabs-toolbox-settings.png){width="500" zoomable="yes"}

| Outil | Icon | Description |
|--- |--- |--- |
| Déplacer | ![ Icône Déplacer ](./assets/pb-icon-move.png){width="25"} | Déplace le jeu d&#39;onglets vers un autre emplacement de la grille dans le conteneur parent. |
| Ajouter | ![Icône Ajouter](./assets/pb-icon-add.png){width="25"} | Ajoute un onglet au jeu d’onglets. |
| (libellé) | [!UICONTROL Tabs] | Identifie le conteneur actuel en tant que jeu d’onglets. Pointez sur la bordure supérieure du conteneur pour afficher la boîte à outils. |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} | Ouvre la page Modifier l’onglet , qui permet de modifier les propriétés du conteneur. |
| Masquer | ![Icône Masquer](./assets/pb-icon-hide.png){width="25"} | Masque le conteneur d’onglets. |
| Afficher | ![Afficher l’icône](./assets/pb-icon-show.png){width="25"} | Affiche le conteneur d’onglets masqués. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="25"} | Effectue une copie de l’onglet actif. |
| Supprimer | ![Icône Supprimer](./assets/pb-icon-remove.png){width="25"} | Supprime l’ensemble d’onglets actuel de l’étape. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Ajout d’un onglet individuel

1. Dans le panneau [!DNL Page Builder] sous _[!UICONTROL Layout]_, faites glisser l’espace réservé&#x200B;**[!UICONTROL Tabs]**directement vers la scène ou vers une ligne ou une colonne de la scène.

   ![Faire glisser les onglets sur une ligne](./assets/pb-layout-tabs-drag-row.png){width="600" zoomable="yes"}

1. Cliquez sur le libellé **[!UICONTROL Tab 1]** pour afficher la boîte à outils de l’onglet individuel et choisissez l’icône _Paramètres_ ( ![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

1. Saisissez le **[!UICONTROL Tab Name]** à utiliser comme libellé.

   ![Saisie du nom de l’onglet](./assets/pb-layout-tab1-toolbox-settings-general-tab-name.png){width="600" zoomable="yes"}

1. Si nécessaire, saisissez le **[!UICONTROL Minimum Height]** de l’onglet .

   Cette valeur peut être un nombre avec une unité CSS valide (par exemple `100px`, `50%`, `50em`, `100vh`) ou un calcul (par exemple `100vh - 237px`).

1. Sélectionnez un paramètre de **[!UICONTROL Vertical Alignment]** pour aligner tous les conteneurs de contenu ajoutés à l’onglet (Haut, Centre ou Bas).

1. Si nécessaire, définissez les autres options en vous aidant des instructions des sections suivantes :

   - [[!UICONTROL Background]](#background)
   - [[!UICONTROL Advanced]](#advanced)

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

## Ajouter un ensemble d’onglets

Les étapes suivantes commencent par un onglet individuel et créent un ensemble de trois onglets dans un conteneur d’onglets. Si vous ne disposez pas déjà d’un onglet individuel, suivez les instructions précédentes pour ajouter un seul onglet à l’étape.

1. Pointez sur le conteneur d’onglets pour afficher la boîte à outils et sélectionnez l’icône _Ajouter_ ( ![icône Ajouter](./assets/pb-icon-add.png){width="20"} ).

1. Cliquez dans le libellé **[!UICONTROL Tab 2]** pour afficher le curseur et saisissez votre propre libellé pour l’onglet.

1. Cliquez à nouveau sur le deuxième onglet de l’étape et sélectionnez l’icône _Dupliquer_ ( ![icône Dupliquer](./assets/pb-icon-duplicate.png){width="20"} ).

1. Cliquez dans le libellé VotreNom **[!UICONTROL Copy]** pour afficher le curseur et saisissez votre propre libellé pour le troisième onglet.

![Correspondance d’un ensemble d’onglets avec la palette](./assets/pb-layout-tabs3-toolbox-main.png){width="600" zoomable="yes"}

## Déplacer un onglet dans la visionneuse

1. Cliquez sur l’onglet à déplacer.

1. Sélectionnez l’icône _Déplacer_ ( ![Icône Déplacer](./assets/pb-icon-move.png){width="20"} ) qui s’affiche juste avant le texte du libellé de l’onglet et faites-la glisser jusqu’à un nouvel emplacement dans l’ensemble d’onglets.

## Ajouter du contenu à un onglet

Vous pouvez ajouter n’importe quel type de contenu à un onglet comme vous le feriez pour une ligne. Suivez les étapes ci-après pour ajouter un type de contenu texte à titre d’exemple.

1. Cliquez sur l’onglet où vous souhaitez ajouter le contenu.

1. Dans le panneau [!DNL Page Builder], développez **[!UICONTROL Elements]** et faites glisser un espace réservé **Texte** vers l’onglet.

1. Saisissez ou collez du texte dans l’éditeur et utilisez la barre d’outils de l’éditeur pour le mettre en forme selon vos besoins.

   Voir [Éléments - Texte](text.md) pour plus d’informations sur l’utilisation du type de contenu texte.

   ![Modification du contenu texte ajouté dans l’onglet](./assets/pb-layout-tab-text.png){width="500" zoomable="yes"}

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]**.

## Modifier les paramètres d’onglets individuels

1. Pointez sur un onglet individuel pour afficher la boîte à outils et choisissez l’icône _Paramètres_ ( ![icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

1. Si nécessaire, modifiez l’un des paramètres de base de l’onglet :

   - **[!UICONTROL Tab Name]** - Saisir le texte révisé du libellé de l’onglet. Vous pouvez également modifier le libellé directement sur l’étape.

   - **[!UICONTROL Minimum Height]** - Saisissez en pixels si vous souhaitez remplacer la hauteur automatique. Par exemple, vous pouvez définir la hauteur minimale pour qu’elle corresponde à la hauteur d’une image d’arrière-plan afin de vous assurer que l’image complète est visible.

   - **[!UICONTROL Vertical Alignment]** - Sélectionnez la position verticale des conteneurs de contenu ajoutés à l’onglet.

1. Modifiez les autres paramètres si nécessaire à l’aide des sections suivantes pour plus de détails.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

### Contexte

- **[!UICONTROL Background Color]** - Spécifiez la couleur d’arrière-plan en choisissant une nuance, en cliquant sur le sélecteur de couleurs ou en saisissant un nom de couleur valide ou une valeur hexadécimale équivalente. Ce paramètre détermine la couleur d’arrière-plan de la ligne. Vous pouvez également régler l’opacité de la couleur.

  ![Aucune couleur (par défaut)](./assets/pb-settings-background-color-no-color.png){width="200"}

  Vous pouvez saisir une valeur de trois façons :

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

- **[!UICONTROL Background Image]** - Si nécessaire, utilisez les outils fournis pour choisir une image d’arrière-plan à appliquer à l’onglet :

  | Outil | Description |
  |--- |--- |
  | [!UICONTROL Upload] | Télécharge un fichier image de votre ordinateur local dans la galerie, puis l’applique comme image d’arrière-plan pour l’onglet. |
  | [!UICONTROL Select from Gallery] | Vous invite à choisir une image existante de la galerie comme image d’arrière-plan pour l’onglet. |
  | ![ Icône Appareil photo ](./assets/pb-icon-camera.png){width="25"} | Vous permet de faire glisser l’image vers la mosaïque de la caméra ou d’accéder à l’image dans votre système de fichiers local. |

  {style="table-layout:auto"}

- **[!UICONTROL Background Mobile Image]** - Si nécessaire, utilisez les mêmes outils pour choisir une image d’arrière-plan différente à utiliser pour l’affichage sur les appareils mobiles.

- **[!UICONTROL Background Size]** - Choisissez la manière dont l’image d’arrière-plan est mise à l’échelle par rapport à la largeur de l’onglet :

  | Option | Description |
  |--- |--- |
  | `Cover` | L’image d’arrière-plan couvre toute la largeur de l’onglet. |
  | `Contain` | L’image d’arrière-plan est limitée à la largeur de la zone de tabulation. |
  | `Auto` | Applique la taille de la feuille de style active. |

  {style="table-layout:auto"}

- **[!UICONTROL Background Position]** - Choisissez le mode d’ancrage de l’image d’arrière-plan par rapport à l’onglet : `Top Left` / `Top Center` / `Top Right` / `Center Left` / `Center` / `Center Right` / `Bottom Left` / `Bottom Center` / `Bottom Right`

- **[!UICONTROL Background Attachment]** - Choisissez le type de pièce jointe pour déterminer le déplacement de l’image d’arrière-plan par rapport à la page de défilement :

  | Option | Description |
  | --- | --- |
  | `Scroll` | L’image d’arrière-plan jointe est synchronisée pour se déplacer vers le bas lors du défilement de la page. |
  | `Fixed` | (Non disponible pour les appareils mobiles) L’image d’arrière-plan ne se déplace pas lorsque le conteneur défile sur l’image et est fixe à la position d’arrière-plan spécifiée. |

  {style="table-layout:auto"}

- **[!UICONTROL Background Repeat]** - Définissez sur `Yes` pour répéter l’image d’arrière-plan afin de remplir l’espace disponible dans l’onglet.

### Avancé

- Pour contrôler l’alignement horizontal des conteneurs de contenu ajoutés à l’onglet, choisissez une **[!UICONTROL Alignment]** .

  | Option | Description |
  | --- | --- |
  | `Default` | Applique le paramètre d’alignement par défaut spécifié dans la feuille de style du thème actif. |
  | `Left` | Aligne les conteneurs de contenu le long de la bordure gauche de l’onglet, en tenant compte de la marge intérieure spécifiée. |
  | `Center` | Aligne le conteneur de contenu au centre de l’onglet, en tenant compte de la marge intérieure spécifiée. |
  | `Right` | Aligne le conteneur de contenu le long de la bordure droite de l’onglet, en tenant compte de la marge intérieure spécifiée. |

  {style="table-layout:auto"}

- Définissez le style de **[!UICONTROL Border]** appliqué aux quatre côtés du conteneur d’onglets :

  | Option | Description |
  | --- | --- |
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

  ![Ligne avec un rayon de bordure de 15](./assets/pb-settings-border-radius-15.png){width="500"}

- (Facultatif) Spécifiez les noms des **[!UICONTROL CSS classes]** de la feuille de style actuelle à appliquer au conteneur de colonnes.

  Séparez plusieurs noms de classe par un espace.

- Saisissez les valeurs, en pixels, du **[!UICONTROL Margins and Padding]** pour spécifier les marges extérieures et la marge intérieure de la colonne.

  Saisissez chaque valeur correspondante dans le diagramme de conteneur d’onglets.

  | Zone conteneur | Description |
  | -------------- | ---------- |
  | [!UICONTROL Margins] | Quantité d’espace vide appliqué au bord extérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |
  | [!UICONTROL Padding] | Quantité d’espace vide appliqué au bord intérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |

  {style="table-layout:auto"}

## Modifier les paramètres du jeu d&#39;onglets

1. Passez la souris sur la bordure supérieure du conteneur de jeux d’onglets pour afficher la boîte à outils et choisissez l’icône _Paramètres_ ( ![icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

1. Si nécessaire, modifiez la **[!UICONTROL Default Active Tab]**.

   Sélectionnez l’onglet de l’ensemble qui doit être actif lors du chargement de la page.

1. Saisissez la **[!UICONTROL Minimum Height]**, en pixels, si vous souhaitez remplacer la hauteur automatique du jeu de tabulations.

1. Pour positionner les onglets de navigation dans la partie supérieure de l’ensemble d’onglets, choisissez l’**[!UICONTROL Tab Navigation Alignment]** (`Left`, `Center` ou `Right`).

   ![Onglets de navigation alignés à droite](./assets/pb-layout-tabs-navigation-alignment-right.png){width="500" zoomable="yes"}

1. Définissez les Options avancées pour le jeu d’onglets :

   - Pour contrôler le positionnement du jeu d’onglets dans le conteneur parent, choisissez une **[!UICONTROL Alignment]** :

     | Option | Description |
     | ------ | ---------- |
     | `Default` | Applique le paramètre d’alignement par défaut spécifié dans la feuille de style du thème actif. |
     | `Left` | Aligne le jeu d’onglets le long de la bordure gauche du conteneur parent, en tenant compte de la marge intérieure spécifiée. |
     | `Center` | Aligne le jeu d’onglets au centre du conteneur parent, en tenant compte de la marge intérieure spécifiée. |
     | `Right` | Aligne le jeu d’onglets le long de la bordure droite du conteneur parent, en tenant compte de la marge intérieure spécifiée. |

     {style="table-layout:auto"}

   - Définissez le style de **[!UICONTROL Border]** appliqué aux quatre côtés du conteneur d’onglets :

     | Option | Description |
     | ------ | ---------- |
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

   - (Facultatif) Spécifiez les noms des **[!UICONTROL CSS classes]** de la feuille de style actuelle à appliquer au conteneur d’onglets.

     Séparez plusieurs noms de classe par un espace.

   - Saisissez les valeurs, en pixels, du **[!UICONTROL Margins and Padding]** pour déterminer les marges extérieures et la marge intérieure du conteneur d’onglets.

     Saisissez les valeurs correspondantes dans le diagramme de conteneur d’onglets.

     | Zone conteneur | Description |
     | -------------- | ---------- |
     | [!UICONTROL Margins] | Quantité d’espace vide appliqué au bord extérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | Quantité d’espace vide appliqué au bord intérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].


<!-- Last updated from includes: 2023-09-11 14:30:19 -->
