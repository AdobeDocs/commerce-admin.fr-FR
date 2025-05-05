---
title: Nouveau widget Liste de produits
description: Découvrez comment utiliser le nouveau widget Liste de produits pour afficher une liste des produits ajoutés le plus récemment.
exl-id: bdff3655-cd14-4a19-a51f-4cabeb274d2a
feature: Page Content, Products
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 0%

---

# Nouveau widget Liste de produits

La liste des nouveaux produits est un exemple de contenu dynamique et se compose de données actives extraites de votre catalogue de produits. Par défaut, la liste _Nouveaux produits_ comprend les huit premiers produits parmi les derniers ajoutés. Cependant, il peut également être configuré pour inclure uniquement les produits d’une période spécifiée.

![Nouvelle liste de produits sur la page d’accueil du storefront](./assets/storefront-home-page-new-products.png){width="700" zoomable="yes"}

## Étape 1 : définir chaque produit comme nouveau

![Magento Open Source](../assets/open-source.svg) Cette étape s’applique uniquement au Magento Open Source.

![Adobe Commerce](../assets/adobe-logo.svg) Pour les magasins Adobe Commerce, reportez-vous à la section [Planification d’une mise à jour](content-staging-scheduled-update.md) et passez à l’étape 2 de cette page.

Le paramètre de plage de dates _[!UICONTROL Set Product as New]_&#x200B;ne peut être configuré que dans les mises à jour planifiées.

La définition d&#39;un produit comme nouveau ajoute le produit à la liste _Nouveaux produits_. Vous pouvez revenir à ce paramètre lorsque vous ne souhaitez plus l’inclure dans la liste, à tout moment.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Recherchez chaque produit que vous souhaitez afficher et ouvrir en mode d’édition.

1. Pour **[!UICONTROL Set Product as New]**, activez l’option pour définir le produit comme nouveau produit ou non.

   ![Définition du produit comme nouveau](./assets/product-set-as-new.png){width="400" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

1. Lorsque vous êtes invité à réindexer et à actualiser le cache de la page, cliquez sur les liens en haut de la page et suivez les instructions.

## Étape 2 : création du widget

Le code qui détermine le contenu de la liste Nouveaux produits et son emplacement dans votre magasin est généré par l’outil Widget.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Widget]**.

1. Dans la section _[!UICONTROL Settings]_, procédez comme suit :

   - Définissez **[!UICONTROL Type]** sur `Catalog New Products List`.

   - Sélectionnez le **[!UICONTROL Design Theme]** utilisé par le magasin.

1. Cliquez sur **[!UICONTROL Continue]**.

   ![ Nouveaux paramètres de widget de liste de produits ](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Dans la section _[!UICONTROL Storefront Properties]_, procédez comme suit :

   - Pour **[!UICONTROL Widget Title]**, saisissez un titre descriptif pour le widget. (Ce titre est visible uniquement à partir de _Admin_.)

   - Pour **[!UICONTROL Assign to Store Views]**, sélectionnez les vues de magasin où le widget est visible.

     Vous pouvez sélectionner une vue de magasin spécifique, ou `All Store Views`. Pour sélectionner plusieurs vues, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

   - (Facultatif) Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre dans lequel cet élément apparaît avec les autres dans la même partie de la page. (`0` = premier, `1` = deuxième, `3` = troisième, etc.)

   ![Mises à jour de mise en page](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

## Etape 3 : sélection de l&#39;emplacement

1. Dans la section _[!UICONTROL Layout Updates]_, cliquez sur **[!UICONTROL Add Layout Update]**.

1. Définissez **[!UICONTROL Display On]** sur `Specified Page.`

1. Définissez **[!UICONTROL Page]** sur `CMS Home Page`.

1. Définissez **[!UICONTROL Block Reference]** sur `Main Content Area`.

1. Définissez **[!UICONTROL Template]** sur l’une des options suivantes :

   - `New Product List Template`
   - `New Products Grid Template`

     ![Mises à jour de mise en page](./assets/widget-layout-update-new-products-list.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save and Continue Edit]**.

   Pour l’instant, vous pouvez ignorer le message pour actualiser le cache.

## Étape 4 : Configuration de la liste

1. Dans le panneau de gauche, choisissez **[!UICONTROL Widget Options]**.

1. Définissez **[!UICONTROL Display Products]** sur l’une des options suivantes :

   - `All Products` - Répertorie les produits en séquence, en commençant par le plus récemment ajouté.
   - `New Products` - Répertorie uniquement les produits identifiés comme _new_. Un produit est considéré comme nouveau pendant la période spécifiée dans _[!UICONTROL Set Product As New From/To]_. La liste est vide si la période expire sans aucun nouveau produit défini.

1. Pour fournir un contrôle de navigation pour les listes comportant plusieurs pages, définissez **[!UICONTROL Display Page Control]** sur `Yes`.

   Pour **[!UICONTROL Number of Products per Page]**, saisissez le nombre de produits que vous souhaitez afficher sur chaque page.

1. Définissez l’option **[!UICONTROL Number of Products to Display]** sur le nombre de nouveaux produits que vous souhaitez inclure dans la liste.

   Le paramètre par défaut est `10`.

1. Pour **[!UICONTROL Cache Lifetime (Seconds)]**, choisissez la fréquence à laquelle vous souhaitez actualiser la liste des nouveaux produits.

   Par défaut, le cache est défini sur 86 400 secondes (24 heures).

   ![Options de widget](./assets/widget-options-new-product-list.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

1. Lorsque vous êtes invité à actualiser le cache, cliquez sur le lien contenu dans le message situé en haut de la page et suivez les instructions.

## Étape 5 : Aperçu de votre travail

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Recherchez la page dans la grille où doit apparaître la liste _Nouveaux produits_ et cliquez sur le lien **[!UICONTROL Preview]** dans la colonne _[!UICONTROL Action]_.
