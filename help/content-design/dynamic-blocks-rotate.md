---
title: Ajouter un bloc dynamique tournant
description: Présenter un diaporama de contenu interactif sur le storefront en ajoutant plusieurs blocs dynamiques à un élément de rotation.
exl-id: 3d338014-cf26-4171-b48b-d37b3d7b0e81
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 0%

---

# Ajouter un bloc dynamique tournant

{{ee-feature}}

Pour présenter un diaporama de contenu interactif, vous pouvez ajouter plusieurs [blocs dynamiques](dynamic-blocks.md) à un rotation. La variable [widget](widgets.md) est utilisé pour placer le robot de rotation à un emplacement spécifique sur une seule page ou sur plusieurs pages dans votre magasin.

![Rotation en bloc dynamique](./assets/widget-dynamic-block-rotator.png){width="700" zoomable="yes"}

## Etape 1 : créer des blocs dynamiques individuels

À [créer les blocs dynamiques ;](dynamic-blocks.md) que vous souhaitez placer dans le rotation, suivez les instructions suivantes :

## Étape 2 : Ajout d’un widget de rotation de bloc dynamique

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Widget]**.

1. Sous _Paramètres_, définit **[!UICONTROL Type]** to `Dynamic Blocks Rotator`.

1. Choisir le **[!UICONTROL Design Theme]** du magasin.

   Ce paramètre identifie le module actuel ou [thème](themes.md) qui détermine la mise en page du magasin.

1. Cliquez sur **[!UICONTROL Continue]**.

   ![Paramètres de rotation de bloc dynamique](./assets/widget-dynamic-block-rotator-settings.png){width="600" zoomable="yes"}

## Étape 3 : Remplir les options

1. Sous _Propriétés Storefront_, définissez les options suivantes :

   - Saisissez un **[!UICONTROL Title]** pour le rotation.

   - Dans le **[!UICONTROL Assign to Store Views]** , sélectionnez la variable [vues du magasin](../getting-started/websites-stores-views.md) où le/la rotation est disponible.

   - (Facultatif) Saisissez un **[!UICONTROL Sort Order]** Nombre pour déterminer la position du/de la personne effectuant le rotation dans le conteneur cible. Il est relatif aux autres widgets qui peuvent être affectés au même conteneur.

   ![Propriétés Rotator storefront](./assets/widget-dynamic-block-rotator-storefront-properties.png){width="600" zoomable="yes"}

1. Sous _Options de mise en page_, cliquez sur **[!UICONTROL Add Layout Update]** et procédez comme suit :

   - Définir **[!UICONTROL Display on]** sur la page, ou le type de page, où doit apparaître le composant de rotation.

      - `Categories` : affiche le/la rotation sur l’une des options suivantes : [ancre](../catalog/navigation-layered.md) ou des pages de catégorie autres que les ancres. Options : catégories d’ancre / catégories autres que l’ancre
      - `Products` - Affiche le composant pivotant sur un type spécifique de page de produit ou sur toutes les pages de produit. Options : tous les types de produits / [Produit simple](../catalog/product-create-simple.md) /  [Produit virtuel](../catalog/product-create-virtual.md) / [Produit groupé](../catalog/product-create-bundle.md) / [Produit téléchargeable](../catalog/product-create-downloadable.md) / [Carte cadeau](../catalog/product-gift-card-create.md) / [Produit configurable](../catalog/product-create-configurable.md) / [Produit groupé](../catalog/product-create-grouped.md)
      - `Generic Pages` : affiche le curseur sur toutes les pages, une page spécifique ou uniquement sur les pages avec une disposition spécifique. Options : `All Pages` / `Specified Page` / `Page Layouts`

     Dans l’exemple, le rotation doit être placé sur un `Specified Page`.

   - Sélectionnez le **[!UICONTROL Page]** où doit s’afficher le rotation.

   - Définir **[!UICONTROL Container]** à la partie du [mise en page](page-layout.md#standard-page-layouts) où doit s’afficher le rotation.

     Si d’autres widgets sont affectés au même conteneur, ils s’affichent dans l’ordre de tri.

   - Accepter `Dynamic Block Template` par défaut **[!UICONTROL Template]**.

     Ce paramètre détermine le modèle utilisé pour mettre en forme le composant de rotation, selon que le composant de rotation doit être autonome ou placé dans le texte existant.

     ![Mises à jour de la mise en page du Rotator](./assets/widget-dynamic-block-rotator-layout-updates.png){width="600" zoomable="yes"}

   - Cliquez sur **[!UICONTROL Save and Continue Edit]**.

1. Dans le panneau de gauche, choisissez **[!UICONTROL Widget Options]**.

1. Pour le **[!UICONTROL Dynamic Blocks to Display]**, acceptez `Specified Dynamic Blocks`.

   Ce paramètre détermine le type de blocs dynamiques inclus dans le rotation.

   - `Specified Dynamic Blocks` - Inclut uniquement des blocs dynamiques spécifiques.
   - `Cart Price Rule Related` - Inclut uniquement les blocs dynamiques associés à une règle de prix de panier.
   - `Catalog Price Rule Related` - Inclut uniquement les blocs dynamiques associés à une règle de prix de catalogue.

1. À **[!UICONTROL Restrict the Dynamic Block Types]** pouvant être utilisé avec le widget, sélectionnez `Content Area`.

   Ce paramètre limite la bannière à une partie spécifique de la mise en page.

   - `Content Area` - Place le bloc dynamique dans la zone de contenu principale de la page.
   - `Footer` - Place le bloc dynamique dans le pied de page.
   - `Header` - Place le bloc dynamique dans l’en-tête de page.
   - `Left Column` - Place le bloc dynamique dans la colonne gauche de la mise en page, le cas échéant.
   - `Right Column` - Place le bloc dynamique dans la colonne de droite de la mise en page, le cas échéant.

1. Définir **[!UICONTROL Rotation Mode]** à l’une des options suivantes :

   - `Display all instead of rotating` - Affiche une pile de blocs dynamiques, où tous sont visibles.
   - `One at a time, Random` - Affiche les blocs dynamiques spécifiés dans un ordre aléatoire. Lorsque la page est actualisée, un bloc dynamique différent (aléatoire) s’affiche.
   - `One at the time, Series` : affiche les blocs dynamiques spécifiés dans la séquence dans laquelle ils ont été ajoutés. Lorsque la page est actualisée, le bloc dynamique suivant de la séquence s’affiche.
   - `One at the time, Shuffle` : affiche un bloc dynamique à la fois dans un ordre variable. Cette option est similaire au `One at a time, Random` , mais le même bloc dynamique n&#39;est pas répété.

     ![Options du widget de rotation](./assets/widget-dynamic-block-rotator-widget-options.png){width="600" zoomable="yes"}

1. Dans le **[!UICONTROL Specify Dynamic Blocks]** grille, cochez la case de chaque bloc dynamique que vous souhaitez inclure dans le composant de rotation.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.
