---
title: '[!DNL Page Builder] Workspace'
description: Découvrez les outils disponibles dans l’espace de travail  [!DNL Page Builder] lorsque vous créez des pages de base, des pages de produits et de catalogues, des blocs et des blocs dynamiques.
exl-id: 1cd7b300-0a18-490f-bc11-36de3fec13dc
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '1426'
ht-degree: 0%

---

# [!DNL Page Builder] Workspace

Lorsque [[!DNL Page Builder] est activé](setup.md), la section _[!UICONTROL Content]_et le processus de création de contenu sont modifiés pour tirer parti des [!DNL Page Builder] outils avancés pour les [pages](../content-design/page-add.md) du CMS, les [pages](../catalog/product-content.md) et les [pages de catégorie](../catalog/categories-content-settings.md), les [blocs](../content-design/block-add.md) et les [blocs dynamiques](../content-design/dynamic-blocks.md). Cette section comprend un champ_ En-tête de contenu _, un aperçu du contenu et un accès facile à l’espace de travail [!DNL Page Builder] plein écran.

![Section de contenu avec [!DNL Page Builder] aperçu](./assets/pb-content-preview.png){width="700" zoomable="yes"}

## En-tête du contenu

Comme les moteurs de recherche recherchent les en-têtes de niveau 1 (H1), l’ajout d’un en-tête de niveau 1 est un moyen facile de s’assurer que la page est correctement indexée.

>[!NOTE]
>
>Le champ _[!UICONTROL Content Heading]_qui apparaît en haut de la page est un champ hérité qui prend en charge le contenu créé avec les versions antérieures de [!DNL Commerce]. Il ne fait toutefois pas partie de [!DNL Page Builder]. Le [!UICONTROL Content Heading] est formaté en tant qu’en-tête H1 en fonction de la feuille de style associée au thème actuel. Il est positionné juste au-dessus de la zone de contenu active définie par l’étape [!DNL Page Builder].

Pour mieux contrôler le positionnement et le format des en-têtes de tous les niveaux, il est recommandé de laisser le champ _[!UICONTROL Content Heading]_vide et d’utiliser le type de contenu [!DNL Page Builder] [En-tête](heading.md) .

![En-tête de contenu et autres en-têtes](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

## Prévisualiser

Lorsque vous développez la section _[!UICONTROL Content]_et qu’il existe du contenu créé avec [!DNL Page Builder], elle affiche un aperçu du contenu tel qu’il apparaîtrait dans une page. Cliquez sur **[!UICONTROL Edit with Page Builder]**ou à l’intérieur de la zone d’aperçu du contenu pour ouvrir l’espace de travail [!DNL Page Builder], où vous pouvez effectuer les mises à jour nécessaires.

![Aperçu de la description du produit](./assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Pour les formulaires de produit et de catégorie, cet aperçu de contenu est activé par défaut, mais peut être désactivé. Si les performances souffrent du chargement de l’aperçu, vous pouvez désactiver l’aperçu dans les paramètres [Configuration de la gestion de contenu](../configuration-reference/general/content-management.md#advanced-content-tools).

## Évaluation

Lorsque vous ouvrez l’espace de travail [!DNL Page Builder] à partir de l’aperçu, l’étape est la principale zone de travail dans laquelle vous pouvez créer et formater du contenu, et même apporter des modifications rapides au contenu en direct. La scène est initialement vide. Elle fournit la surface de conception sur laquelle vous pouvez faire glisser des lignes, des colonnes et des onglets à partir du panneau de gauche.

>[!NOTE]
>
>À compter de la version 2.4.1, la modification du contenu s’affiche désormais en plein écran uniquement pour toutes les zones contrôlées par [!DNL Page Builder] : pages CMS, pages de produits et de catégories, blocs et blocs dynamiques. La modification en plein écran met l’accent sur votre contenu et fournit une vue qui correspond mieux à l’expérience de l’utilisateur sur le storefront.

![Intermédiaire avec le contenu de la page](./assets/pb-workspace-simple-page.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Fenêtres d’affichage

Une _fenêtre d’affichage_ est la zone visible d’une page web qu’un utilisateur voit. En mode de conception plein écran, les boutons de fenêtre d’affichage s’affichent au-dessus de l’étape [!DNL Page Builder] pour vous montrer le contenu tel que l’utilisateur le voit sur le storefront.

![Boutons d’affichage](./assets/pb-workspace-viewport-buttons.png){width="500" zoomable="yes"}

[!DNL Page Builder] définit également des points d’arrêt pour les fenêtres d’affichage. Les points d’arrêt définissent les largeurs minimales et maximales au sein desquelles certains styles sont appliqués. Les fenêtres d’affichage [!DNL Page Builder] fournissent les points d’arrêt de contenu suivants :

- **Point d’arrêt du bureau**—`min-width: 1024px`. Ce point d’arrêt applique les styles définis pour les largeurs de fenêtre d’affichage qui mesurent 1 024 pixels et plus.
- **Points d’arrêt mobiles**—`max-width: 768px, min-width: 640px`. Ces points d’arrêt appliquent des styles définis pour les largeurs de fenêtre d’affichage comprises entre 768 et 640 pixels.

Les fenêtres d’affichage [!DNL Page Builder] offrent deux fonctionnalités : **_aperçus de contenu_** et **_paramètres de point d’arrêt_**.

### Prévisualisations du contenu

Par défaut, [!DNL Page Builder] fournit deux aperçus de fenêtre d’affichage :

- **Bureau** : affiche l’aperçu du contenu sans largeur prédéfinie. Les styles définis par l’appli de bureau (à l’aide d’une largeur minimale de 1 024 pixels au point d’arrêt) sont toujours appliqués à la page. Toutefois, la largeur de la fenêtre d’affichage de l’appli de bureau est définie par les paramètres pour les types de contenu de conteneur, tels que Lignes. La sélection de la fenêtre d’affichage de bureau indique le style de votre contenu sur le storefront lorsque la largeur de la page du navigateur est de 1 024 pixels et plus large.

  ![Aperçu de la fenêtre d’affichage de bureau avec une largeur minimale de 1 024 pixels](./assets/pb-workspace-viewport-desktop.png){width="500" zoomable="yes"}

- **Mobile** : affiche l’aperçu du contenu sur une largeur prédéfinie de 768 pixels. Contrairement à la fenêtre d’affichage pour ordinateur de bureau, la fenêtre d’affichage mobile affiche le contenu de votre page avec une largeur de 768 pixels, ainsi que les styles définis pour les largeurs de point d’arrêt de 768 pixels (maximum) et de 640 pixels (minimum).

  ![Aperçu de la fenêtre d’affichage mobile avec largeur minimale de 768 pixels](./assets/pb-workspace-viewport-mobile.png){width="500" zoomable="yes"}

### Paramètres des points d’arrêt

Les boutons de fenêtre d’affichage offrent également la possibilité d’appliquer différents styles de point d’arrêt aux types de contenu en fonction de la fenêtre d’affichage sélectionnée. Par défaut, [!DNL Page Builder] fournit des paramètres de point d’arrêt pour les champs _[!UICONTROL Minimum Height]_de Lignes, Colonnes, Onglets, Éléments d’onglet, Bannières, Curseurs et Diapositives. Lorsque vous sélectionnez la fenêtre d’affichage Mobile, puis ouvrez l’éditeur pour l’un de ces types de contenu, vous pouvez saisir des valeurs de champ spécifiques aux points d’arrêt de la fenêtre d’affichage Mobile . Les champs de type Contenu qui autorisent des paramètres de point d’arrêt spécifiques affichent une icône à droite du champ, comme dans l’exemple suivant pour une ligne :

![Indicateur d’icône pour le paramètre de point d’arrêt](./assets/pb-workspace-viewport-field-breakpoint.png){width="400"}

## Panneau

Le panneau [!DNL Page Builder] se trouve à gauche de l’étape et contient les types de contenu qui peuvent être déplacés vers l’étape. Un conteneur spécifique au type de contenu s’affiche alors avec une boîte à outils d’options. Les types de contenu sont organisés dans le panneau comme suit :

### Disposition

La section _[!UICONTROL Layout]_du panneau [!DNL Page Builder] est utilisée pour ajouter des lignes, des colonnes ou des onglets à la scène. Lorsque vous faites glisser un type de contenu du panneau vers la scène, un conteneur s’affiche avec une boîte à outils d’options spécifiques au type de contenu.

Par défaut, l’étape [!DNL Page Builder] est vide. Lorsque vous faites glisser des types de contenu de mise en page du panneau vers la scène, vous pouvez les placer au-dessus, en dessous ou à l’intérieur d’autres conteneurs de mise en page sur la page. Les lignes ne peuvent être ajoutées directement à la scène que.

![[!DNL Page Builder] panneau avec types de contenu de mise en page et étape](./assets/pb-stage-toolbox.png){width="600" zoomable="yes"}

| Type de contenu de mise en page | Description |
| ------------------- |------------ |
| [Ligne](row.md) | Une nouvelle ligne peut uniquement être glissée du panneau vers la scène et positionnée au-dessus ou en dessous d’une autre ligne, d’un autre onglet ou d’un autre groupe de colonnes. Vous pouvez également utiliser l’option Dupliquer pour copier une ligne existante. |
| [Colonne](column.md) | Vous pouvez faire glisser une colonne du panneau vers la scène ou vers des lignes et des onglets. Le nombre maximal de colonnes pouvant être ajoutées est déterminé par le nombre de divisions de grille spécifiées dans la [configuration](setup.md). |
| [Onglets](tabs.md) | Vous pouvez faire glisser un seul onglet du panneau vers la scène ou vers des lignes et des colonnes. Des onglets supplémentaires peuvent être ajoutés à partir de la boîte à outils. |

{style="table-layout:auto"}

### Éléments

Utilisez la section _[!UICONTROL Elements]_du panneau [!DNL Page Builder] pour ajouter du texte, des en-têtes, des boutons, des séparateurs et du code d’HTML à n’importe quel conteneur de mises en page sur l’ [[!DNL Page Builder] étape](workspace.md#stage). Lorsque vous faites glisser un type de contenu du panneau vers une ligne ou une colonne, ou vers un ensemble d’onglets sur la scène, un conteneur s’affiche. Utilisez la boîte à outils de type de contenu pour accéder aux paramètres spécifiques au type.

![[!DNL Page Builder] panneau avec types de contenu d’élément](./assets/pb-elements.png){width="600" zoomable="yes"}

| Type de contenu de l’élément | Description |
| -------------------- | ----------- |
| [Texte](text.md) | Ajoute un conteneur de texte et un éditeur à l’étape. |
| [Heading](heading.md) | Ajoute un conteneur d’en-tête à la scène. |
| [Boutons](buttons.md) | Ajoute un conteneur pour un bouton individuel ou un ensemble de boutons à la scène. |
| [Diviseur](divider.md) | Ajoute un conteneur pour un séparateur à la scène. |
| [Code HTML](html-code.md) | Ajoute un conteneur pour le code d’HTML à la scène. |

{style="table-layout:auto"}

### Média

Utilisez la section _[!UICONTROL Media]_du panneau [!DNL Page Builder] pour ajouter des images, des vidéos, des bannières, des curseur et [!DNL Google Maps] à n’importe quel conteneur de mises en page sur l’ [[!DNL Page Builder] étape](workspace.md#stage). Lorsqu’un type de contenu multimédia est glissé du panneau vers la scène, un conteneur s’affiche avec une boîte à outils contenant les options propres au type de contenu.

![[!DNL Page Builder] panneau avec types de contenu multimédia](./assets/pb-media-content-types.png){width="600" zoomable="yes"}

| Type de contenu du média | Description |
| ------------------- | ------------------------------------------ |
| [Image](image.md) | Ajoute un conteneur d’images à la scène. |
| [Vidéo](video.md) | Ajoute un conteneur vidéo à la scène. |
| [Bannière](banner.md) | Ajoute un conteneur de bannières à la scène. |
| [Curseur](slider.md) | Ajoute un conteneur de curseur à la scène. |
| [Map](map.md) | Ajoute un conteneur [!DNL Google Maps] à la scène. |

{style="table-layout:auto"}

### Ajouter du contenu

Utilisez la section _[!UICONTROL Add Content]_du panneau [!DNL Page Builder] pour ajouter du contenu existant à la [[!DNL Page Builder] scène](workspace.md#stage). Lorsque vous faites glisser un type de contenu multimédia du panneau vers la scène, un conteneur s’affiche. Utilisez la boîte à outils de type de contenu pour accéder aux_ Paramètres _spécifiques au type.

Panneau ![[!DNL Page Builder] avec Ajouter des types de contenu](./assets/pb-add-content.png){width="600" zoomable="yes"}

| Type de contenu | Description |
| ---------------------------------------------------------------- | -------------------------------------------- |
| [Bloc](block.md) | Ajoute un bloc existant à la scène. |
| [Bloc dynamique](dynamic-block.md) | Ajoute un bloc dynamique existant à la scène. |
| [Produits](products.md) | Ajoute une liste de produits à la scène. |
| ![Adobe Commerce uniquement](../assets/adobe-logo.svg) [Recommendations de produit](recommendations.md) | Ajoute une unité de recommandation à l’étape. |

{style="table-layout:auto"}

## Toolbox

Chaque conteneur de contenu sur la scène comporte une boîte à outils d’options. Les options varient selon le type de contenu, mais incluent généralement Déplacer, Paramètres, Masquer/Afficher, Dupliquer et Supprimer.

### Afficher la boîte à outils

Pointez sur le conteneur pour afficher la boîte à outils et sélectionnez une option.

![Options de boîte à outils de lignes](./assets/pb-tutorial1-row-toolbox.png){width="600" zoomable="yes"}

### Options de boîte à outils

| Option | Icône | Description |
| --------- | ---------------------------------------- | ------------ |
| Déplacer | ![Icône Déplacer](./assets/pb-icon-move.png){width="25"} | Déplace le conteneur de contenu actuel vers une autre position sur la scène. |
| Ajouter | ![Ajouter une icône](./assets/pb-icon-add.png){width="25"} | Ajoute des éléments enfants tels qu’un bouton, une diapositive ou un onglet. |
| (label) |           | Identifie le type de contenu du conteneur. |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} | Ouvre les propriétés du conteneur de contenu en mode d’édition. |
| Masquer | ![Icône Masquer](./assets/pb-icon-hide.png){width="25"} | Masque le conteneur de contenu actuel. |
| Afficher | ![Icône Afficher](./assets/pb-icon-show.png){width="25"} | Affiche le conteneur de contenu actuel. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="25"} | Effectue une copie du conteneur de contenu actuel. |
| Supprimer | ![Supprimer](./assets/pb-icon-remove.png){width="25"} | Supprime le conteneur de contenu actuel de la scène. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}
