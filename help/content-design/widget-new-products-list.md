---
title: Nouveau widget Liste de produits
description: Découvrez comment utiliser le nouveau widget Liste de produits pour afficher une liste des produits ajoutés le plus récemment.
exl-id: bdff3655-cd14-4a19-a51f-4cabeb274d2a
feature: Page Content, Products
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Nouveau widget Liste de produits

La liste des nouveaux produits est un exemple de contenu dynamique et se compose de données actives extraites de votre catalogue de produits. Par défaut, la variable _Nouveaux produits_ liste comprend les huit premiers des produits ajoutés le plus récemment. Cependant, il peut également être configuré pour inclure uniquement les produits d’une période spécifiée.

![Nouvelle liste de produits sur la page d’accueil du storefront](./assets/storefront-home-page-new-products.png){width="700" zoomable="yes"}

## Étape 1 : définir chaque produit comme nouveau

![Magento Open Source](../assets/open-source.svg) Cette étape s’applique uniquement au Magento Open Source.

![Adobe Commerce](../assets/adobe-logo.svg) Pour les magasins Adobe Commerce, voir [Planification d’une mise à jour](content-staging-scheduled-update.md) puis passez à l’étape 2 de cette page.

_[!UICONTROL Set Product as New]_la plage de dates ne peut être configurée que dans les mises à jour planifiées.

La définition d’un produit comme nouveau ajoute le produit à la variable _Nouveaux produits_ liste. Vous pouvez revenir à ce paramètre lorsque vous ne souhaitez plus l’inclure dans la liste, à tout moment.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Recherchez chaque produit que vous souhaitez afficher et ouvrir en mode d’édition.

1. Pour **[!UICONTROL Set Product as New]**, activez l’option pour définir le produit comme un nouveau produit ou non.

   ![Définition du produit comme nouveau](./assets/product-set-as-new.png){width="400" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

1. Lorsque vous êtes invité à réindexer et à actualiser le cache de la page, cliquez sur les liens en haut de la page et suivez les instructions.

## Étape 2 : création du widget

Le code qui détermine le contenu de la liste Nouveaux produits et son emplacement dans votre magasin est généré par l’outil Widget.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Widget]**.

1. Dans le _[!UICONTROL Settings]_, procédez comme suit :

   - Définir **[!UICONTROL Type]** to `Catalog New Products List`.

   - Choisissez la **[!UICONTROL Design Theme]** qui est utilisé par le magasin.

1. Cliquez sur **[!UICONTROL Continue]**.

   ![Nouveaux paramètres du widget de liste de produits](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Dans le _[!UICONTROL Storefront Properties]_, procédez comme suit :

   - Pour **[!UICONTROL Widget Title]**, saisissez un titre descriptif pour le widget. (Ce titre est visible uniquement à partir de la fonction _Administration_.)

   - Pour **[!UICONTROL Assign to Store Views]**, sélectionnez les vues de magasin où le widget est visible.

     Vous pouvez sélectionner une vue de magasin spécifique, ou `All Store Views`. Pour sélectionner plusieurs vues, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

   - (Facultatif) Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre dans lequel cet élément apparaît avec les autres dans la même partie de la page. (`0` = first, `1` = second, `3` = troisième, etc.)

   ![Mises à jour de la mise en page](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

## Etape 3 : sélection de l&#39;emplacement

1. Dans le _[!UICONTROL Layout Updates]_, cliquez sur **[!UICONTROL Add Layout Update]**.

1. Définir **[!UICONTROL Display On]** to `Specified Page.`

1. Définir **[!UICONTROL Page]** to `CMS Home Page`.

1. Définir **[!UICONTROL Block Reference]** to `Main Content Area`.

1. Définir **[!UICONTROL Template]** à l’une des options suivantes :

   - `New Product List Template`
   - `New Products Grid Template`

     ![Mises à jour de la mise en page](./assets/widget-layout-update-new-products-list.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save and Continue Edit]**.

   Pour l’instant, vous pouvez ignorer le message pour actualiser le cache.

## Étape 4 : Configuration de la liste

1. Dans le panneau de gauche, choisissez **[!UICONTROL Widget Options]**.

1. Définir **[!UICONTROL Display Products]** à l’une des options suivantes :

   - `All Products` - Répertorie les produits dans l’ordre, en commençant par le plus récemment ajouté.
   - `New Products` - Répertorie uniquement les produits identifiés comme _new_. Un produit est considéré comme nouveau au cours de la période spécifiée dans _[!UICONTROL Set Product As New From/To]_. La liste est vide si la période expire sans aucun nouveau produit défini.

1. Pour fournir un contrôle de navigation aux listes comportant plusieurs pages, définissez **[!UICONTROL Display Page Control]** to `Yes`.

   Pour **[!UICONTROL Number of Products per Page]**, saisissez le nombre de produits à afficher sur chaque page.

1. Définissez la variable **[!UICONTROL Number of Products to Display]** au nombre de nouveaux produits que vous souhaitez inclure dans la liste.

   Le paramètre par défaut est `10`.

1. Pour **[!UICONTROL Cache Lifetime (Seconds)]**, choisissez la fréquence à laquelle vous souhaitez actualiser la liste des nouveaux produits.

   Par défaut, le cache est défini sur 86 400 secondes (24 heures).

   ![Options de widget](./assets/widget-options-new-product-list.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

1. Lorsque vous êtes invité à actualiser le cache, cliquez sur le lien contenu dans le message situé en haut de la page et suivez les instructions.

## Étape 5 : Aperçu de votre travail

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Recherchez la page dans la grille où la fonction _Nouveaux produits_ s’affiche et cliquez sur le bouton **[!UICONTROL Preview]** dans le _[!UICONTROL Action]_colonne .
