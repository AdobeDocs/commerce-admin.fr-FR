---
title: Mises en page
description: Découvrez les sections sur la disposition des pages et comment configurer les dispositions par défaut.
exl-id: 397a92cf-6f20-4729-8d7c-c5f672fc1c9a
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '878'
ht-degree: 0%

---

# Mises en page

La disposition de chaque page de votre magasin se compose de sections ou de conteneurs distincts, qui définissent l’en-tête, le pied de page et les zones de contenu de la page. Selon la disposition, chaque page peut comporter une, deux, trois colonnes ou plus. Vous pouvez considérer la mise en page comme le _plan d’étage_ de la page et affecter une mise en page spécifique à utiliser par défaut pour les pages de CMS, de produits et de catégories.

Sur la page, les blocs de contenu flottent pour remplir l’espace disponible, en fonction de la section de la [mise en page](layout-updates.md) où ils sont affectés à apparaître. Notez que si vous modifiez la disposition pour passer d’une disposition à trois colonnes à une disposition à deux colonnes, le contenu de la zone principale s’étend pour remplir l’espace disponible. Notez également que tous les blocs associés à la barre latérale inutilisée semblent disparaître. Cependant, si vous restaurez la disposition à trois colonnes, les blocs réapparaîtront. Cette approche fluide, ou _mise en page liquide_, permet de modifier la mise en page sans avoir à retravailler le contenu. Si vous êtes habitué à travailler avec des pages HTML individuelles, cette approche modulaire _bloc de création_ nécessite une autre façon de penser.

![Deux colonnes standard avec mise en page de la barre de gauche](./assets/storefront-2-column-ee.png){width="700" zoomable="yes"}

## Configurer les dispositions par défaut

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche sous _[!UICONTROL General]_, choisissez **[!UICONTROL Web]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Default Layouts]** .

   ![Dispositions par défaut](./assets/web-default-layouts.png){width="600" zoomable="yes"}

1. Choisissez le **[!UICONTROL Default Product Layout]** à utiliser pour les pages de produits.

   Ce paramètre détermine la disposition utilisée par défaut pour les pages de produits.

   - `No layout updates` - Les mises à jour de disposition ne sont pas disponibles pour les pages de produits.
   - `Empty` - Utilise une mise en page vierge pour les pages de produits.
   - `1 column` - Utilise une disposition sur une seule colonne pour les pages de produits.
   - `2 columns with left bar` - Utilise une disposition à deux colonnes avec la barre latérale gauche pour les pages de produits.
   - `2 columns with right bar` - Utilise une disposition à deux colonnes avec la barre latérale droite pour les pages de produits.
   - `3 columns` - Utilise une disposition à trois colonnes avec des barres latérales à gauche et à droite pour les pages de produits.

   Lorsque [Page Builder](../page-builder/introduction.md) est activé, d’autres options de pleine largeur sont disponibles. Vous pouvez ensuite utiliser les outils de contenu du Créateur de page pour concevoir la mise en page de vos pages de produit.

   - `Page -- Full Width` : utilise la disposition _Page - Pleine largeur_ pour les pages de produits.
   - `Category -- Full Width` : utilise la mise en page _Catégorie - Pleine largeur_ pour les pages de produits.
   - `Product -- Full Width` - (Recommandé) Utilise la disposition _Produit - Pleine largeur_ pour les pages de produit.

1. Choisissez le **[!UICONTROL Default Category Layout]** à utiliser pour les pages de catégorie.

   Ce paramètre détermine la disposition utilisée par défaut pour les pages de catégorie.

   - `No layout updates` - Les mises à jour de disposition ne sont pas disponibles pour les pages de catégorie.
   - `Empty` - Utilise une mise en page vierge pour les pages de catégorie.
   - `1 column` - Utilise une disposition sur une seule colonne pour les pages de catégorie.
   - `2 columns with left bar` : utilise une disposition à deux colonnes avec la barre latérale gauche pour les pages de catégories.
   - `2 columns with right bar` : utilise une disposition à deux colonnes avec la barre latérale droite pour les pages de catégories.
   - `3 columns` : utilise une disposition à trois colonnes avec des barres latérales à gauche et à droite pour les pages de catégories.

   Lorsque [Page Builder](../page-builder/introduction.md) est activé, d’autres options de pleine largeur sont disponibles. Vous pouvez ensuite utiliser les outils de contenu du Créateur de page pour concevoir la mise en page de vos pages de catégorie.

   - `Page -- Full Width` : utilise la disposition _Page - Pleine largeur_ pour les pages de catégorie.
   - `Category -- Full Width` - (Recommandé) Utilise la disposition _Catégorie - Pleine largeur_ pour les pages de catégorie.
   - `Product -- Full Width` : utilise la mise en page _Produit - Pleine largeur_ pour les pages de catégorie.

1. Choisissez le **[!UICONTROL Default Page Layout]** à utiliser pour les pages CMS.

   Ce paramètre détermine la mise en page utilisée par défaut pour les pages CMS.

   - `No layout updates` - Les mises à jour de disposition ne sont pas disponibles pour les pages CMS.
   - `Empty` - Utilise une mise en page vierge pour les pages CMS.
   - `1 column` - Utilise une disposition sur une seule colonne pour les pages CMS.
   - `2 columns with left bar` - Utilise une disposition à deux colonnes avec la barre latérale gauche pour les pages CMS.
   - `2 columns with right bar` - Utilise une disposition à deux colonnes avec la barre latérale droite pour les pages CMS.
   - `3 columns` : utilise une disposition à trois colonnes avec des barres latérales à gauche et à droite pour les pages CMS.

   Lorsque [Page Builder](../page-builder/introduction.md) est activé, d’autres options de pleine largeur sont disponibles. Vous pouvez ensuite utiliser les outils de contenu du Créateur de page pour concevoir la mise en page de vos pages CMS.

   - `Page -- Full Width` - (recommandé) Utilise la disposition _Page - Pleine largeur_ pour les pages CMS.
   - `Category - Full Width` : utilise la mise en page _Catégorie - Pleine largeur_ pour les pages CMS.
   - `Product - Full Width` : utilise la mise en page _Produit - Pleine largeur_ pour les pages CMS.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Mises en page standard

### Une colonne

![Diagramme - Disposition une colonne](./assets/layout-1-col-th.png){zoomable="yes"}

La disposition _[!UICONTROL 1 Column]_&#x200B;peut être utilisée pour créer une page d’accueil dramatique avec une grande image ou un point focal. Il s’agit également d’un bon choix pour une page de destination ou toute autre page qui combine texte, images et vidéo.

### Deux colonnes avec barre gauche

![Diagramme - disposition à deux colonnes avec barre gauche](./assets/layout-2-col-lft-bar-th.png){zoomable="yes"}

La disposition _[!UICONTROL 2 Columns with Left Bar]_&#x200B;est souvent utilisée pour les pages avec navigation à gauche, comme un catalogue ou des pages de résultats de recherche avec navigation superposée. Il s’agit également d’un excellent choix pour les pages d’accueil qui nécessitent une navigation supplémentaire ou des blocs de contenu de prise en charge sur la gauche.

### Deux colonnes avec barre de droite

![Diagramme - disposition à deux colonnes avec barre de droite](./assets/layout-2-col-rt-bar-th.png){zoomable="yes"}

Avec une disposition _[!UICONTROL 2 Columns with Right Bar]_, la zone de contenu principale est suffisamment grande pour accueillir une image ou une bannière attrayante. Cette disposition est également souvent utilisée pour les pages de produits avec des blocs de contenu complémentaire à droite.

### Trois colonnes

![Diagramme - disposition à trois colonnes](./assets/layout-3-col-th.png){zoomable="yes"}

La disposition _[!UICONTROL 3 Column]_&#x200B;comporte une colonne centrale suffisamment large pour le texte principal de la page, avec de l’espace de chaque côté pour une navigation supplémentaire et des blocs de contenu connexe.

### Vide

![Diagramme - disposition vide](./assets/layout-blank-th.png){zoomable="yes"}

La mise en page _[!UICONTROL Empty]_&#x200B;peut être utilisée pour définir des mises en page personnalisées.
