---
title: '[!DNL Page Builder] Workspace'
description: Découvrez les outils disponibles dans l [!DNL Page Builder] espace de travail lorsque vous créez des pages de base, des pages de produit et de catalogue, des blocs et des blocs dynamiques.
exl-id: 1cd7b300-0a18-490f-bc11-36de3fec13dc
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '1426'
ht-degree: 0%

---

# [!DNL Page Builder] Workspace

Lorsque l’option [[!DNL Page Builder] est activée](setup.md), la section _[!UICONTROL Content]_&#x200B;et le processus de création de contenu sont modifiés afin de tirer parti des outils de [!DNL Page Builder] avancés pour les pages CMS [pages](../content-design/page-add.md), [produit](../catalog/product-content.md) et [catégorie](../catalog/categories-content-settings.md), [blocs](../content-design/block-add.md) et [blocs dynamiques](../content-design/dynamic-blocks.md). Cette section comprend un champ_ En-tête de contenu _, un aperçu du contenu et un accès facile à l’espace de travail de [!DNL Page Builder] en plein écran.

![Section de contenu avec [!DNL Page Builder] aperçu](./assets/pb-content-preview.png){width="700" zoomable="yes"}

## Titre du contenu

Comme les moteurs de recherche recherchent des en-têtes de niveau 1 (H1), l’ajout d’un en-tête de niveau 1 est un moyen facile de s’assurer que la page est correctement indexée.

>[!NOTE]
>
>Le champ _[!UICONTROL Content Heading]_&#x200B;qui s’affiche en haut de la page est un champ hérité qui prend en charge le contenu créé avec des versions [!DNL Commerce] antérieures. Mais cela ne fait pas partie de la [!DNL Page Builder]. Le [!UICONTROL Content Heading] est formaté en tant qu’en-tête H1 en fonction de la feuille de style associée au thème actif. Il est positionné juste au-dessus de la zone de contenu actif définie par l’étape [!DNL Page Builder].

Pour un meilleur contrôle du positionnement et du format des en-têtes de tous les niveaux, il est recommandé de laisser le champ _[!UICONTROL Content Heading]_&#x200B;vide et d’utiliser le type de contenu [!DNL Page Builder] [En-tête](heading.md).

![En-tête de contenu et autres en-têtes](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

## Prévisualiser

Lorsque vous développez la section _[!UICONTROL Content]_&#x200B;et que du contenu existant est créé avec [!DNL Page Builder], elle affiche un aperçu du contenu tel qu’il apparaîtrait sur une page. Cliquez sur **[!UICONTROL Edit with Page Builder]**&#x200B;ou dans la zone d’aperçu du contenu pour ouvrir l’espace de travail [!DNL Page Builder], où vous pouvez effectuer les mises à jour nécessaires.

![&#x200B; Aperçu de la description du produit &#x200B;](./assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Pour les formulaires de produits et de catégories, cet aperçu de contenu est activé par défaut, mais peut être désactivé. Si les performances pâtissent du chargement de l’aperçu, vous pouvez le désactiver dans les paramètres [Configuration de la gestion de contenu](../configuration-reference/general/content-management.md#advanced-content-tools).

## Étape

Lorsque vous ouvrez l’espace de travail [!DNL Page Builder] depuis l’aperçu, la scène est l’espace de travail principal où vous pouvez créer et mettre en forme le contenu, et même apporter des modifications rapides au contenu en direct. L’étape est initialement vide, fournissant la surface de conception dans laquelle vous pouvez faire glisser des lignes, des colonnes et des onglets depuis le panneau de gauche.

>[!NOTE]
>
>Depuis la version 2.4.1, la modification de contenu n’est plus possible en plein écran que pour toutes les zones contrôlées par [!DNL Page Builder] (pages CMS, pages de produits et de catégories, blocs et blocs dynamiques). La modification en plein écran met l’accent sur votre contenu et fournit une vue qui correspond mieux à l’expérience utilisateur sur le storefront.

![Évaluation avec contenu de page](./assets/pb-workspace-simple-page.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Fenêtres d’affichage

Une _fenêtre d’affichage_ est la zone visible d’une page web que l’utilisateur voit. En mode de conception plein écran, les boutons de fenêtre d’affichage s’affichent au-dessus de l’étape de [!DNL Page Builder] pour vous montrer le contenu tel que l’utilisateur du site le voit sur le storefront.

![Boutons de fenêtre](./assets/pb-workspace-viewport-buttons.png){width="500" zoomable="yes"}

[!DNL Page Builder] définit également des points d’arrêt pour les fenêtres d’affichage. Les points d’arrêt définissent les largeurs minimale et maximale à l’intérieur desquelles certains styles sont appliqués. Les fenêtres d’affichage [!DNL Page Builder] fournissent les points d’arrêt de contenu suivants :

- **Point d’arrêt du bureau**—`min-width: 1024px`. Ce point d’arrêt applique les styles définis pour les largeurs de fenêtre d’affichage qui mesurent 1 024 pixels et plus.
- **Points d’arrêt mobiles**—`max-width: 768px, min-width: 640px`. Ces points d’arrêt appliquent des styles définis pour les largeurs de fenêtre d’affichage comprises entre 768 et 640 pixels.

[!DNL Page Builder] fenêtres d’affichage offrent deux fonctionnalités : **_aperçus de contenu_** et **_paramètres de point d’arrêt_**.

### Aperçus de contenu

Par défaut, [!DNL Page Builder] fournit deux aperçus de fenêtre d’affichage :

- **Bureau** — Affiche l&#39;aperçu du contenu sans largeur prédéfinie. Les styles définis par le bureau (utilisant une largeur minimale du point d’arrêt de 1 024 pixels) sont toujours appliqués à la page. Cependant, la largeur de la fenêtre d’affichage Bureau est définie par des paramètres pour les types de contenu de conteneur, tels que Lignes. La sélection de la fenêtre du Bureau permet de voir comment votre contenu est mis en forme sur le storefront lorsque la largeur de page du navigateur est de 1 024 pixels et plus.

  ![Aperçu de la fenêtre d’affichage du bureau avec une largeur minimale de 1 024 pixels](./assets/pb-workspace-viewport-desktop.png){width="500" zoomable="yes"}

- **Mobile** : affiche l&#39;aperçu du contenu sur une largeur prédéfinie de 768 pixels. Contrairement à la fenêtre d’affichage de bureau, la fenêtre d’affichage mobile affiche le contenu de votre page sur une largeur de 768 pixels, ainsi que les styles définis pour les largeurs de point d’arrêt de 768 pixels (maximum) et 640 pixels (minimum).

  ![Aperçu de la fenêtre d’affichage mobile avec une largeur minimale de 768 pixels](./assets/pb-workspace-viewport-mobile.png){width="500" zoomable="yes"}

### Paramètres des points d’arrêt

Les boutons de fenêtre d’affichage offrent également la possibilité d’appliquer différents styles de point d’arrêt aux types de contenu en fonction de la fenêtre d’affichage sélectionnée. Par défaut, [!DNL Page Builder] fournit des paramètres de point d’arrêt pour les champs de _[!UICONTROL Minimum Height]_&#x200B;des lignes, colonnes, onglets, éléments d’onglet, bannières, curseurs et diapositives. Lorsque vous sélectionnez la fenêtre d’affichage mobile, puis ouvrez l’éditeur pour l’un de ces types de contenu, vous pouvez saisir des valeurs de champ spécifiques aux points d’arrêt de la fenêtre d’affichage mobile. Les champs de type de contenu qui autorisent des paramètres de point d’arrêt spécifiques affichent une icône à droite du champ, similaire à l’exemple suivant pour une ligne :

![Indicateur d’icône pour le paramètre de point d’arrêt](./assets/pb-workspace-viewport-field-breakpoint.png){width="400"}

## Panneau

Le panneau [!DNL Page Builder] est situé à gauche de la scène et contient les types de contenu qui peuvent être déplacés vers la scène. Un conteneur spécifique au type de contenu s’affiche alors avec une boîte à outils d’options. Les types de contenu sont organisés dans le panneau comme suit :

### Disposition

La section _[!UICONTROL Layout]_&#x200B;du panneau [!DNL Page Builder] permet d’ajouter des lignes, des colonnes ou des onglets à la scène. Lorsque vous faites glisser un type de contenu du panneau vers la scène, un conteneur s’affiche avec une boîte à outils d’options spécifiques au type de contenu.

Par défaut, l’étape [!DNL Page Builder] est vide. Lorsque vous faites glisser des types de contenu de mise en page du panneau vers la scène, vous pouvez les placer au-dessus, en dessous ou à l’intérieur d’autres conteneurs de mise en page sur la page. Les lignes ne peuvent être ajoutées que directement à l&#39;étape.

![[!DNL Page Builder] avec les types de contenu de disposition et l’étape](./assets/pb-stage-toolbox.png){width="600" zoomable="yes"}

| Type de contenu de mise en page | Description |
| ------------------- |------------ |
| [Ligne](row.md) | Vous pouvez uniquement faire glisser une nouvelle ligne du panneau vers la scène, et la placer au-dessus ou au-dessous d’un autre groupe de lignes, onglets ou colonnes. Vous pouvez également utiliser l’option Dupliquer pour faire une copie d’une ligne existante. |
| [Colonne](column.md) | Vous pouvez faire glisser une colonne du panneau à la scène ou aux lignes et onglets. Le nombre maximal de colonnes pouvant être ajoutées est déterminé par le nombre de divisions de la grille spécifié dans la [configuration](setup.md). |
| [&#x200B; Onglets &#x200B;](tabs.md) | Vous pouvez faire glisser un seul onglet du panneau vers la scène ou vers des lignes et des colonnes. Vous pouvez ajouter d’autres onglets à partir de la palette. |

{style="table-layout:auto"}

### Éléments

Utilisez la section _[!UICONTROL Elements]_&#x200B;du panneau [!DNL Page Builder] pour ajouter du texte, des en-têtes, des boutons, des séparateurs et du code HTML à n’importe quel conteneur de disposition sur la [[!DNL Page Builder] scène](workspace.md#stage). Lorsque vous faites glisser un type de contenu du panneau vers une ligne, une colonne ou un ensemble d’onglets sur la scène, un conteneur s’affiche. Utilisez la boîte à outils Type de contenu pour accéder aux paramètres spécifiques au type.

Panneau ![[!DNL Page Builder] avec les types de contenu d’éléments &#x200B;](./assets/pb-elements.png){width="600" zoomable="yes"}

| Type de contenu de l’élément | Description |
| -------------------- | ----------- |
| [Texte &#x200B;](text.md) | Ajoute un conteneur de texte et un éditeur à l’étape. |
| [Titre](heading.md) | Ajoute un conteneur d’en-tête à l’étape. |
| [&#x200B; Boutons &#x200B;](buttons.md) | Ajoute un conteneur pour un bouton individuel ou un ensemble de boutons à la scène. |
| [Diviseur](divider.md) | Ajoute un conteneur pour un séparateur à la scène. |
| [Code HTML](html-code.md) | Ajoute un conteneur pour le code HTML à l’étape. |

{style="table-layout:auto"}

### Média

Utilisez la section _[!UICONTROL Media]_&#x200B;du panneau [!DNL Page Builder] pour ajouter des images, des vidéos, des bannières, des curseurs et des [!DNL Google Maps] à n’importe quel conteneur de dispositions sur la [[!DNL Page Builder] scène](workspace.md#stage). Lorsqu’un type de contenu multimédia est déplacé du panneau vers la scène, un conteneur s’affiche avec une boîte à outils d’options spécifiques au type de contenu.

![[!DNL Page Builder] de contenu multimédia](./assets/pb-media-content-types.png){width="600" zoomable="yes"}

| Type de contenu multimédia | Description |
| ------------------- | ------------------------------------------ |
| [Image &#x200B;](image.md) | Ajoute un conteneur d’images à l’étape. |
| [Vidéo](video.md) | Ajoute un conteneur vidéo à l’étape. |
| [Bannière](banner.md) | Ajoute un conteneur de bannières à l’étape. |
| [Curseur](slider.md) | Ajoute un conteneur curseur à la scène. |
| [Map](map.md) | Ajoute un conteneur [!DNL Google Maps] à l’étape. |

{style="table-layout:auto"}

### Ajouter du contenu

Utilisez la section _[!UICONTROL Add Content]_&#x200B;du panneau [!DNL Page Builder] pour ajouter du contenu existant à l’[[!DNL Page Builder] étape](workspace.md#stage). Lorsque vous faites glisser un type de contenu multimédia du panneau vers la scène, un conteneur s’affiche. Utilisez la boîte à outils Type de contenu pour accéder aux_ Paramètres _qui sont spécifiques au type.

![[!DNL Page Builder] un panneau avec Ajouter des types de contenu](./assets/pb-add-content.png){width="600" zoomable="yes"}

| Type de contenu | Description |
| ---------------------------------------------------------------- | -------------------------------------------- |
| [Bloquer](block.md) | Ajoute un bloc existant à l’étape. |
| [Bloc dynamique](dynamic-block.md) | Ajoute un bloc dynamique existant à l&#39;étape. |
| [Produits](products.md) | Ajoute une liste de produits à l’étape. |
| ![Adobe Commerce uniquement](../assets/adobe-logo.svg) [Recommandations de produits](recommendations.md) | Ajoute une unité de recommandation à l’étape. |

{style="table-layout:auto"}

## Boîte à outils

Chaque conteneur de contenu de l’étape comporte une boîte à outils d’options. Les options varient selon le type de contenu, mais incluent généralement Déplacer, Paramètres, Masquer/Afficher, Dupliquer et Supprimer.

### Afficher la boîte à outils

Pointez sur le conteneur pour afficher la boîte à outils et choisissez une option.

![Options de la boîte à outils Ligne](./assets/pb-tutorial1-row-toolbox.png){width="600" zoomable="yes"}

### Options de la boîte à outils

| Option | Icon | Description |
| --------- | ---------------------------------------- | ------------ |
| Déplacer | ![&#x200B; Icône Déplacer &#x200B;](./assets/pb-icon-move.png){width="25"} | Déplace le conteneur de contenu actuel vers un autre emplacement sur la scène. |
| Ajouter | ![Icône Ajouter](./assets/pb-icon-add.png){width="25"} | Ajoute des éléments enfants tels qu’un bouton, une diapositive ou un onglet. |
| (libellé) |           | Identifie le type de contenu du conteneur. |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} | Ouvre les propriétés du conteneur de contenu en mode d’édition. |
| Masquer | ![Icône Masquer](./assets/pb-icon-hide.png){width="25"} | Masque le conteneur de contenu actuel. |
| Afficher | ![Afficher l’icône](./assets/pb-icon-show.png){width="25"} | Affiche le conteneur de contenu actuel. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="25"} | Effectue une copie du conteneur de contenu actuel. |
| Supprimer | ![Supprimer](./assets/pb-icon-remove.png){width="25"} | Supprime le conteneur de contenu actuel de l’étape. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
