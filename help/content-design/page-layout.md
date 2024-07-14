---
title: Dispositions de pages
description: Découvrez les sections de mise en page et comment configurer les mises en page par défaut.
exl-id: 397a92cf-6f20-4729-8d7c-c5f672fc1c9a
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 0%

---

# Dispositions de pages

La mise en page de chaque page de votre magasin se compose de sections ou de conteneurs distincts, qui définissent l’en-tête, le pied de page et les zones de contenu de la page. Selon la disposition, chaque page peut contenir une, deux, trois colonnes ou plus. Vous pouvez considérer la mise en page comme le _plan de sol_ de la page et attribuer une mise en page spécifique à utiliser par défaut pour les pages CMS, de produit et de catégorie.

Sur la page, les blocs de contenu flottent pour remplir l’espace disponible, selon la section de la [mise en page](layout-updates.md) où ils doivent apparaître. Notez que si vous changez la mise en page de trois colonnes à deux colonnes, le contenu de la zone principale se développe pour remplir l’espace disponible. Notez également que les blocs associés à la barre latérale inutilisée semblent disparaître. Toutefois, si vous restaurez la mise en page à trois colonnes, les blocs réapparaîtront. Cette approche fluide, ou _disposition liquide_, permet de modifier la mise en page sans avoir à retravailler le contenu. Si vous êtes habitué à travailler avec des pages d’HTML individuelles, cette approche modulaire de _bloc de création_ nécessite une manière de penser différente.

![ Standard à deux colonnes avec mise en page à barre gauche](./assets/storefront-2-column-ee.png){width="700" zoomable="yes"}

## Configuration des dispositions par défaut

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche sous _[!UICONTROL General]_, choisissez **[!UICONTROL Web]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Default Layouts]** .

   ![ Mises en page par défaut](./assets/web-default-layouts.png){width="600" zoomable="yes"}

1. Sélectionnez le **[!UICONTROL Default Product Layout]** que vous souhaitez utiliser pour les pages de produits.

   Ce paramètre détermine la mise en page utilisée par défaut pour les pages de produits.

   - `No layout updates` - Les mises à jour de mise en page ne sont pas disponibles pour les pages de produits.
   - `Empty` - Utilise une mise en page vierge pour les pages de produits.
   - `1 column` - Utilise une mise en page à une seule colonne pour les pages de produits.
   - `2 columns with left bar` - Utilise une mise en page à deux colonnes avec la barre latérale gauche pour les pages de produit.
   - `2 columns with right bar` - Utilise une mise en page à deux colonnes avec la barre latérale à droite pour les pages de produit.
   - `3 columns` - Utilise une mise en page à trois colonnes avec des encadrés à gauche et à droite pour les pages de produits.

   Lorsque [Page Builder](../page-builder/introduction.md) est activé, d’autres options de pleine largeur sont disponibles. Vous pouvez ensuite utiliser les outils de contenu du Créateur de pages pour concevoir la mise en page de vos pages de produits.

   - `Page -- Full Width` - Utilise la disposition _Page - Largeur complète_ pour les pages de produit.
   - `Category -- Full Width` - Utilise la disposition _Catégorie - Largeur complète_ pour les pages de produits.
   - `Product -- Full Width` - (Recommandé) Utilise la disposition _Produit - Largeur complète_ pour les pages de produit.

1. Sélectionnez le **[!UICONTROL Default Category Layout]** à utiliser pour les pages de catégorie.

   Ce paramètre détermine la mise en page utilisée par défaut pour les pages de catégorie.

   - `No layout updates` - Les mises à jour de mise en page ne sont pas disponibles pour les pages de catégorie.
   - `Empty` - Utilise une mise en page vierge pour les pages de catégorie.
   - `1 column` - Utilise une mise en page à une seule colonne pour les pages de catégorie.
   - `2 columns with left bar` - Utilise une mise en page à deux colonnes avec la barre latérale gauche pour les pages de catégorie.
   - `2 columns with right bar` - Utilise une mise en page à deux colonnes avec la barre latérale droite pour les pages de catégorie.
   - `3 columns` - Utilise une mise en page à trois colonnes avec des encadrés à gauche et à droite pour les pages de catégorie.

   Lorsque [Page Builder](../page-builder/introduction.md) est activé, d’autres options de pleine largeur sont disponibles. Vous pouvez ensuite utiliser les outils de contenu du Créateur de pages pour concevoir la mise en page de vos pages de catégorie.

   - `Page -- Full Width` - Utilise la disposition _Page - Largeur complète_ pour les pages de catégorie.
   - `Category -- Full Width` - (Recommandé) Utilise la disposition _Catégorie - Largeur complète_ pour les pages de catégorie.
   - `Product -- Full Width` - Utilise la disposition _Produit - Largeur complète_ pour les pages de catégorie.

1. Sélectionnez le **[!UICONTROL Default Page Layout]** que vous souhaitez utiliser pour les pages CMS.

   Ce paramètre détermine la mise en page utilisée par défaut pour les pages CMS.

   - `No layout updates` - Les mises à jour de mise en page ne sont pas disponibles pour les pages CMS.
   - `Empty` - Utilise une disposition vierge pour les pages CMS.
   - `1 column` - Utilise une mise en page à une seule colonne pour les pages CMS.
   - `2 columns with left bar` - Utilise une mise en page à deux colonnes avec la barre latérale gauche pour les pages CMS.
   - `2 columns with right bar` - Utilise une mise en page à deux colonnes avec la barre latérale à droite pour les pages CMS.
   - `3 columns` - Utilise une mise en page à trois colonnes avec des encadrés à gauche et à droite pour les pages CMS.

   Lorsque [Page Builder](../page-builder/introduction.md) est activé, d’autres options de pleine largeur sont disponibles. Vous pouvez ensuite utiliser les outils de contenu du Créateur de pages pour concevoir la mise en page de vos pages CMS.

   - `Page -- Full Width` - (Recommandé) Utilise la disposition _Page - Largeur complète_ pour les pages CMS.
   - `Category - Full Width` - Utilise la disposition _Catégorie - Largeur complète_ pour les pages CMS.
   - `Product - Full Width` - Utilise la disposition _Produit - Largeur complète_ pour les pages CMS.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

## Disposition de pages standard

### Une colonne

![Diagramme - mise en page à une colonne](./assets/layout-1-col-th.png){zoomable="yes"}

La disposition _[!UICONTROL 1 Column]_peut être utilisée pour créer une page d’accueil spectaculaire avec une grande image ou un point focal. Il s’agit également d’un bon choix pour une page d’entrée ou toute autre page qui comporte une combinaison de texte, d’images et de vidéo.

### Deux colonnes avec la barre de gauche

![Diagramme - mise en page à deux colonnes avec barre de gauche](./assets/layout-2-col-lft-bar-th.png){zoomable="yes"}

La disposition _[!UICONTROL 2 Columns with Left Bar]_est souvent utilisée pour les pages avec une navigation à gauche, comme un catalogue ou des pages de résultats de recherche avec une navigation par couches. Il s’agit également d’un excellent choix pour les pages d’accueil qui nécessitent une navigation supplémentaire ou des blocs de contenu pris en charge sur la gauche.

### Deux colonnes avec barre droite

![Diagramme - mise en page à deux colonnes avec barre droite](./assets/layout-2-col-rt-bar-th.png){zoomable="yes"}

Avec une disposition _[!UICONTROL 2 Columns with Right Bar]_, la zone de contenu principale est suffisamment grande pour accueillir une image ou une bannière accrocheuse. Cette disposition est également souvent utilisée pour les pages de produit avec des blocs de contenu pris en charge à droite.

### Trois colonnes

![Diagramme - mise en page à trois colonnes](./assets/layout-3-col-th.png){zoomable="yes"}

La mise en page _[!UICONTROL 3 Column]_comporte une colonne centrale suffisamment large pour le texte principal de la page, avec une marge de navigation supplémentaire et des blocs de contenu de prise en charge sur chaque côté.

### Vide

![Diagramme - mise en page vide](./assets/layout-blank-th.png){zoomable="yes"}

La disposition _[!UICONTROL Empty]_peut être utilisée pour définir des mises en page personnalisées.
