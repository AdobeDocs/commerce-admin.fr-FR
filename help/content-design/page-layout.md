---
title: Dispositions de pages
description: Découvrez les sections de mise en page et comment configurer les mises en page par défaut.
exl-id: 397a92cf-6f20-4729-8d7c-c5f672fc1c9a
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# Dispositions de pages

La mise en page de chaque page de votre magasin se compose de sections ou de conteneurs distincts, qui définissent l’en-tête, le pied de page et les zones de contenu de la page. Selon la disposition, chaque page peut contenir une, deux, trois colonnes ou plus. Vous pouvez considérer la disposition comme la _plan de plancher_ de la page et attribuez une mise en page spécifique à utiliser comme valeur par défaut pour les pages CMS, de produit et de catégorie.

Sur la page, les blocs de contenu flottent pour remplir l’espace disponible, selon la section de la fonction [mise en page](layout-updates.md) où elles doivent apparaître. Notez que si vous changez la mise en page de trois colonnes à deux colonnes, le contenu de la zone principale se développe pour remplir l’espace disponible. Notez également que les blocs associés à la barre latérale inutilisée semblent disparaître. Toutefois, si vous restaurez la mise en page à trois colonnes, les blocs réapparaîtront. Cette approche fluide, ou _disposition liquide_, permet de modifier la mise en page sans avoir à retravailler le contenu. Si vous êtes habitué à travailler avec des pages de HTML individuelles, ce module, _bloc de création_ l&#39;approche nécessite une manière différente de penser.

![Mise en page standard à deux colonnes avec barre gauche](./assets/storefront-2-column-ee.png){width="700" zoomable="yes"}

## Configuration des dispositions par défaut

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, sous _[!UICONTROL General]_, choisissez **[!UICONTROL Web]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Default Layouts]** .

   ![Dispositions par défaut](./assets/web-default-layouts.png){width="600" zoomable="yes"}

1. Choisissez la **[!UICONTROL Default Product Layout]** que vous souhaitez utiliser pour les pages de produits.

   Ce paramètre détermine la mise en page utilisée par défaut pour les pages de produits.

   - `No layout updates` - Les mises à jour de mise en page ne sont pas disponibles pour les pages de produits.
   - `Empty` - Utilise une mise en page vierge pour les pages de produits.
   - `1 column` : utilise une mise en page à une seule colonne pour les pages de produits.
   - `2 columns with left bar` : permet d’utiliser une mise en page à deux colonnes avec la barre latérale à gauche pour les pages du produit.
   - `2 columns with right bar` : permet d’utiliser une mise en page à deux colonnes avec la barre latérale à droite pour les pages du produit.
   - `3 columns` : permet d’utiliser une mise en page à trois colonnes avec des encadrés à gauche et à droite pour les pages de produits.

   When [Page Builder](../page-builder/introduction.md) est activée, d’autres options de pleine largeur sont disponibles. Vous pouvez ensuite utiliser les outils de contenu du Créateur de pages pour concevoir la mise en page de vos pages de produits.

   - `Page -- Full Width` - Utilise la variable _Page - Largeur complète_  mise en page pour les pages de produits.
   - `Category -- Full Width` - Utilise la variable _Catégorie - Largeur complète_ mise en page pour les pages de produits.
   - `Product -- Full Width` - (Recommandé) Utilise la variable _Produit - Largeur complète_ mise en page pour les pages de produits.

1. Choisissez la **[!UICONTROL Default Category Layout]** que vous souhaitez utiliser pour les pages de catégorie.

   Ce paramètre détermine la mise en page utilisée par défaut pour les pages de catégorie.

   - `No layout updates` - Les mises à jour de mise en page ne sont pas disponibles pour les pages de catégorie.
   - `Empty` : permet d’utiliser une mise en page vierge pour les pages de catégorie.
   - `1 column` : permet d’utiliser une mise en page à une seule colonne pour les pages de catégorie.
   - `2 columns with left bar` : permet d’utiliser une mise en page à deux colonnes avec la barre latérale gauche pour les pages de catégorie.
   - `2 columns with right bar` : permet d’utiliser une mise en page à deux colonnes avec la barre latérale à droite pour les pages de catégorie.
   - `3 columns` : permet d’utiliser une mise en page à trois colonnes avec des encadrés à gauche et à droite pour les pages de catégorie.

   When [Page Builder](../page-builder/introduction.md) est activée, d’autres options de pleine largeur sont disponibles. Vous pouvez ensuite utiliser les outils de contenu du Créateur de pages pour concevoir la mise en page de vos pages de catégorie.

   - `Page -- Full Width` - Utilise la variable _Page - Largeur complète_ mise en page pour les pages de catégorie.
   - `Category -- Full Width` - (Recommandé) Utilise la variable _Catégorie - Largeur complète_ mise en page pour les pages de catégorie.
   - `Product -- Full Width` - Utilise la variable _Produit - Largeur complète_ mise en page pour les pages de catégorie.

1. Choisissez la **[!UICONTROL Default Page Layout]** à utiliser pour les pages CMS.

   Ce paramètre détermine la mise en page utilisée par défaut pour les pages CMS.

   - `No layout updates` - Les mises à jour de mise en page ne sont pas disponibles pour les pages CMS.
   - `Empty` : utilise une mise en page vierge pour les pages CMS.
   - `1 column` : utilise une mise en page à une seule colonne pour les pages CMS.
   - `2 columns with left bar` : utilise une mise en page à deux colonnes avec la barre latérale à gauche pour les pages CMS.
   - `2 columns with right bar` : utilise une mise en page à deux colonnes avec la barre latérale à droite pour les pages CMS.
   - `3 columns` : permet d’utiliser une mise en page à trois colonnes avec des encadrés à gauche et à droite pour les pages CMS.

   When [Page Builder](../page-builder/introduction.md) est activée, d’autres options de pleine largeur sont disponibles. Vous pouvez ensuite utiliser les outils de contenu du Créateur de pages pour concevoir la mise en page de vos pages CMS.

   - `Page -- Full Width` - (Recommandé) Utilise la variable _Page - Largeur complète_ mise en page pour les pages CMS.
   - `Category - Full Width` - Utilise la variable _Catégorie - Largeur complète_ mise en page pour les pages CMS.
   - `Product - Full Width` - Utilise la variable _Produit - Largeur complète_ mise en page pour les pages CMS.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

## Disposition de pages standard

### Une colonne

![Diagramme : mise en page à une colonne](./assets/layout-1-col-th.png){zoomable=&quot;yes&quot;}

La variable _[!UICONTROL 1 Column]_La mise en page peut être utilisée pour créer une page d’accueil spectaculaire avec une grande image ou un point focal. Il s’agit également d’un bon choix pour une page d’entrée ou toute autre page qui comporte une combinaison de texte, d’images et de vidéo.

### Deux colonnes avec la barre de gauche

![Diagramme : mise en page à deux colonnes avec barre de gauche](./assets/layout-2-col-lft-bar-th.png){zoomable=&quot;yes&quot;}

La variable _[!UICONTROL 2 Columns with Left Bar]_La mise en page est souvent utilisée pour les pages avec une navigation à gauche, telles qu’un catalogue ou des pages de résultats de recherche avec une navigation par couches. Il s’agit également d’un excellent choix pour les pages d’accueil qui nécessitent une navigation supplémentaire ou des blocs de contenu pris en charge sur la gauche.

### Deux colonnes avec barre droite

![Diagramme : mise en page à deux colonnes avec barre droite](./assets/layout-2-col-rt-bar-th.png){zoomable=&quot;yes&quot;}

Avec _[!UICONTROL 2 Columns with Right Bar]_mise en page, la zone de contenu principale est suffisamment grande pour accueillir une image ou une bannière accrocheuse. Cette disposition est également souvent utilisée pour les pages de produit avec des blocs de contenu pris en charge à droite.

### Trois colonnes

![Diagramme : mise en page à trois colonnes](./assets/layout-3-col-th.png){zoomable=&quot;yes&quot;}

La variable _[!UICONTROL 3 Column]_La mise en page comporte une colonne centrale suffisamment large pour le texte principal de la page, avec une marge de navigation supplémentaire et des blocs de contenu de prise en charge de chaque côté.

### Vide

![Diagramme - disposition vide](./assets/layout-blank-th.png){zoomable=&quot;yes&quot;}

La variable _[!UICONTROL Empty]_La mise en page peut être utilisée pour définir des mises en page personnalisées.
