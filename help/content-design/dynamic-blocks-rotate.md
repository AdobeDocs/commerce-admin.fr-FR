---
title: Ajouter un bloc dynamique rotatif
description: Présentez un diaporama de contenu interactif sur le storefront en ajoutant plusieurs blocs dynamiques à un rotateur.
exl-id: 3d338014-cf26-4171-b48b-d37b3d7b0e81
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 0%

---

# Ajouter un bloc dynamique rotatif

{{ee-feature}}

Pour présenter un diaporama de contenu interactif, vous pouvez ajouter plusieurs [blocs dynamiques](dynamic-blocks.md) à un rotateur. L’outil [widget](widgets.md) permet de placer le rotateur à un emplacement spécifique sur une seule page ou sur plusieurs pages de votre boutique.

![Rotateur de bloc dynamique](./assets/widget-dynamic-block-rotator.png){width="700" zoomable="yes"}

## Étape 1 : créer des blocs dynamiques individuels

Pour [créer les blocs dynamiques](dynamic-blocks.md) à placer dans le rotateur, procédez comme suit :

## Étape 2 : Ajouter un widget rotatif de bloc dynamique

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Widget]**.

1. Sous _Paramètres_, définissez **[!UICONTROL Type]** sur `Dynamic Blocks Rotator`.

1. Choisissez le **[!UICONTROL Design Theme]** actuel du magasin.

   Ce paramètre identifie le package actuel ou [thème](themes.md) qui détermine la mise en page du magasin.

1. Cliquez sur **[!UICONTROL Continue]**.

   ![Paramètres de rotation de bloc dynamique](./assets/widget-dynamic-block-rotator-settings.png){width="600" zoomable="yes"}

## Étape 3 : effectuez les options

1. Sous _Propriétés du storefront_, définissez les options suivantes :

   - Saisissez un **[!UICONTROL Title]** pour le rotateur.

   - Dans la liste **[!UICONTROL Assign to Store Views]**, sélectionnez les [ vues de magasin](../getting-started/websites-stores-views.md) où le rotateur est disponible.

   - (Facultatif) Saisissez un nombre **[!UICONTROL Sort Order]** pour déterminer la position du rotateur dans le conteneur cible. Il est relatif aux autres widgets qui peuvent être affectés au même conteneur.

   ![Propriétés du storefront Rotator](./assets/widget-dynamic-block-rotator-storefront-properties.png){width="600" zoomable="yes"}

1. Sous _Options de mise en page_, cliquez sur **[!UICONTROL Add Layout Update]** et procédez comme suit :

   - Définissez **[!UICONTROL Display on]** sur la page, ou le type de page, où le rotateur doit apparaître.

      - `Categories` - Affiche le rotateur sur les pages de catégorie ancre[&#128279;](../catalog/navigation-layered.md) ou  ancre. Options : Catégories d’ancrage / Catégories non-ancres
      - `Products` - Affiche le rotateur sur un type spécifique de page de produit ou sur toutes les pages de produit. Options : Tous les types de produits / [Produit simple](../catalog/product-create-simple.md) / [Produit virtuel](../catalog/product-create-virtual.md) / [Produit groupé](../catalog/product-create-bundle.md) / [Produit téléchargeable](../catalog/product-create-downloadable.md) / [Carte cadeau](../catalog/product-gift-card-create.md) / [Produit configurable](../catalog/product-create-configurable.md) / [Produit groupé](../catalog/product-create-grouped.md)
      - `Generic Pages` - Affiche le rotateur sur toutes les pages, sur une page spécifique ou uniquement sur les pages avec une certaine disposition. Options : `All Pages` / `Specified Page` / `Page Layouts`

     Dans l&#39;exemple, le rotateur doit être placé sur un `Specified Page`.

   - Sélectionnez le **[!UICONTROL Page]** spécifique où le rotateur doit apparaître.

   - Définissez **[!UICONTROL Container]** sur la partie de la [mise en page](page-layout.md#standard-page-layouts) où le rotateur doit apparaître.

     Si d’autres widgets sont affectés au même conteneur, ils apparaissent dans l’ordre selon l’ordre de tri.

   - Acceptez `Dynamic Block Template` comme **[!UICONTROL Template]** par défaut.

     Ce paramètre détermine le modèle utilisé pour formater le rotateur, selon que le rotateur doit être autonome ou placé dans un texte existant.

     ![Mises à jour de la disposition Rotateur](./assets/widget-dynamic-block-rotator-layout-updates.png){width="600" zoomable="yes"}

   - Cliquez sur **[!UICONTROL Save and Continue Edit]**.

1. Dans le panneau de gauche, choisissez **[!UICONTROL Widget Options]**.

1. Pour le **[!UICONTROL Dynamic Blocks to Display]**, acceptez `Specified Dynamic Blocks`.

   Ce paramètre détermine le type de blocs dynamiques inclus dans le rotateur.

   - `Specified Dynamic Blocks` - Inclut uniquement des blocs dynamiques spécifiques.
   - `Cart Price Rule Related` - Inclut uniquement les blocs dynamiques associés à une règle de prix de panier.
   - `Catalog Price Rule Related` - Inclut uniquement les blocs dynamiques associés à une règle de prix de catalogue.

1. Pour **[!UICONTROL Restrict the Dynamic Block Types]** qui peut être utilisé avec le widget, sélectionnez `Content Area`.

   Ce paramètre limite la bannière à une partie spécifique de la mise en page.

   - `Content Area` - Place le bloc dynamique dans la zone de contenu principale de la page.
   - `Footer` - Place le bloc dynamique dans le pied de page.
   - `Header` - Place le bloc dynamique dans l’en-tête de la page.
   - `Left Column` - Place le bloc dynamique dans la colonne de gauche de la mise en page, le cas échéant.
   - `Right Column` - Place le bloc dynamique dans la colonne de droite de la mise en page, le cas échéant.

1. Définissez **[!UICONTROL Rotation Mode]** sur l’une des options suivantes :

   - `Display all instead of rotating` - Affiche une pile de blocs dynamiques, où tous sont visibles.
   - `One at a time, Random` - Affiche les blocs dynamiques spécifiés dans un ordre aléatoire. Lorsque la page est actualisée, un bloc dynamique différent (et aléatoire) s’affiche.
   - `One at the time, Series` - Affiche les blocs dynamiques spécifiés dans l’ordre dans lequel ils ont été ajoutés. Lorsque la page est actualisée, le bloc dynamique suivant de la séquence s’affiche.
   - `One at the time, Shuffle` - Affiche un bloc dynamique à la fois dans un ordre mélangé. Cette option est similaire à l’option `One at a time, Random`, sauf que le même bloc dynamique n’est pas répété.

     ![Options du widget Rotateur](./assets/widget-dynamic-block-rotator-widget-options.png){width="600" zoomable="yes"}

1. Dans la grille de **[!UICONTROL Specify Dynamic Blocks]**, cochez la case de chaque bloc dynamique à inclure dans le rotateur.

1. Cliquez ensuite sur **[!UICONTROL Save]**.
