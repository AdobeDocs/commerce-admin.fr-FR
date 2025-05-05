---
title: Trier les produits de catégorie
description: Découvrez comment définir manuellement le positionnement des produits dans une catégorie ou en appliquant un ordre de tri prédéfini.
exl-id: 09c66a5d-57d4-4e78-a8d8-e3047c1bd35a
feature: Catalog Management, Categories, Products
source-git-commit: 14c3eb7d54776382bfa196efdac446d42c8dc940
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# Trier les produits de catégorie

{{ee-feature}}

La position des produits d’une catégorie peut être spécifiée manuellement en les faisant glisser et en les déposant en position ou en appliquant un ordre de tri prédéfini. Par défaut, les produits peuvent être triés par niveau de stock, âge, couleur, nom, SKU et prix. Le tri automatique remplace l’ordre de tri actuel et réinitialise les positions de glisser-déposer qui ont été définies manuellement. L’ordre de tri des couleurs et le niveau de stock minimal requis pour que les produits soient inclus dans la liste sont définis dans la configuration [Visual Merchandiser](../configuration-reference/catalog/visual-merchandiser.md).

>[!NOTE]
>
>Sur les pages de catégorie, `Out of stock` produits sont toujours affichés **_après_** `In Stock` produits sur la liste de produits avec tous les types de tri.

Vous pouvez configurer les options de catégorie séparément pour chaque [vue de magasin](../stores-purchase/stores.md#add-stores) afin de déterminer la sélection de produits, leur position relative dans la liste et les attributs disponibles pour les règles de catégorie. Cependant, il existe un seul ordre de tri **_global_** et une position de produit dans le catalogue. Ils sont partagés sur l’ensemble des [vues de magasin](../stores-purchase/store-views.md), des magasins et des sites web.

## Etape 1 : définir la portée de la configuration

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Si nécessaire, choisissez le **[!UICONTROL Store View]** où les paramètres s’appliquent.

   Pour une installation multi-magasin, le paramètre _[!UICONTROL Store View]_&#x200B;applique l’ordre de tri à toutes les vues disponibles dans le magasin.

1. Dans l&#39;arborescence de gauche, choisissez la catégorie à modifier.

   ![Arborescence de catégorie](./assets/category-selected.png){width="700" zoomable="yes"}

## Étape 2 : trier les produits

>[!NOTE]
>
>Lors du tri d’une catégorie selon un attribut de produit, les produits avec les mêmes valeurs d’attribut sont également triés par leur _[!UICONTROL Product ID]_&#x200B;dans l’ordre croissant.

Dans la section _[!UICONTROL Products in Category]_, cliquez sur l’icône de mosaïque ( ![Afficher les mosaïques](../assets/icon-view-tiles.png) ) pour afficher les mosaïques de produit dans une grille. Utilisez la méthode manuelle ou automatique pour trier les produits.

![Mosaïques de produit](./assets/category-products-tiles.png){width="600" zoomable="yes"}

### Méthode 1 : tri manuel

1. Définissez **[!UICONTROL Sort Order]** selon vos préférences.

   ![Ordre de tri](./assets/category-edit-sort-order.png){width="600" zoomable="yes"}

1. Pour appliquer le nouvel ordre de tri, cliquez sur **[!UICONTROL Sort]**.

1. Pour enregistrer l’ordre de tri, cliquez sur **[!UICONTROL Save Category]**.

1. Lorsque vous y êtes invité, mettez à jour les indexeurs non valides.

### Méthode 2 : tri automatique

1. Définissez **[!UICONTROL Match products by rule]** (![/Toggle yes](../assets/toggle-yes.png)) sur `Yes`.


1. Définissez **[!UICONTROL Automatic Sorting]** selon vos préférences.

1. Pour créer une règle de catégorie, suivez les instructions de l’étape suivante.

## Étape 3 : création d’une règle de catégorie

1. Définissez **[!UICONTROL Match products by rule]** (![/Toggle yes](../assets/toggle-yes.png)) sur `Yes`.

1. Cliquez sur **[!UICONTROL Add Condition]**.

1. Sélectionnez le **[!UICONTROL Attribute]** qui est la base de la condition.

1. Définissez **[!UICONTROL Operator]** sur l’une des options suivantes :

   - `Equal`
   - `Not equal`
   - `Greater than`
   - `Greater than or equal to`
   - `Less than`
   - `Less than or equal to`
   - `Contains`

1. Saisissez le **[!UICONTROL Value]** approprié.

   ![Condition de catégorie](./assets/category-rule-create.png){width="600" zoomable="yes"}

1. Pour ajouter une autre condition, cliquez sur **[!UICONTROL Add Condition]** et répétez le processus.

## Étape 4 : enregistrement, actualisation et vérification

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Category]**.

1. Lorsque vous êtes invité à actualiser le cache, cliquez sur **[!UICONTROL Cache Management]** et actualisez chaque cache non valide.

1. Dans le storefront, vérifiez que la sélection de produits, le tri et les règles de catégorie fonctionnent correctement.

   Si vous devez effectuer des ajustements, modifiez les paramètres et réessayez.
