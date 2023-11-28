---
title: Ajout d’attributs à un produit
description: Découvrez comment ajouter des attributs aux produits de votre catalogue.
exl-id: 1f92807a-2362-48a2-8d3a-4aef90a5671f
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# Ajout d’attributs à un produit

Bien que les attributs soient principalement gérés à partir de la variable [Magasins](../stores-purchase/stores-menu.md) , vous pouvez également ajouter de nouveaux attributs. _à la volée_ lors de l’utilisation d’un produit. Vous pouvez choisir dans la liste des attributs existants ou créer un attribut. Le nouvel attribut est ajouté à la variable [jeu d’attributs](../catalog/attribute-sets.md) sur laquelle le produit est basé.

## Étape 1 : Ajout d’un attribut

1. Ouvrez le produit en mode d’édition.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Attribute]**.

   ![Nouveau produit avec jeu d’attributs par défaut](./assets/product-attribute-add.png){width="600" zoomable="yes"}

1. Pour ajouter un attribut existant au produit, utilisez la variable [contrôles de filtre](../getting-started/admin-grid-controls.md) pour trouver l’attribut dans la grille et procédez comme suit :

   - Cochez la case dans la première colonne de chaque attribut à ajouter.

   - Cliquez sur **[!UICONTROL Add Selected]**.

   ![Sélection d’un attribut](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

1. Pour définir un nouvel attribut, cliquez sur **[!UICONTROL Create New Attribute]** et remplissez les éléments de l’étape 2.

## Etape 2 : décrire les propriétés de l&#39;attribut de base

![Propriétés d’attribut](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

1. Sous _[!UICONTROL Attribute Properties]_, saisissez une **[!UICONTROL Attribute Label]**pour identifier l’attribut.

1. Définir **[!UICONTROL Catalog Input Type for Store Owner]** au type de [contrôle d’entrée](attributes-input-types.md) à utiliser pour la saisie de données.

   Si l’attribut est utilisé pour un [produit configurable](product-create-configurable.md), choisissez `Dropdown`. Définissez ensuite **[!UICONTROL Required]** to `Yes`.

1. Pour `Dropdown` et `Multiple Select` types d’entrée, procédez comme suit :

   - Sous **[!UICONTROL Values]**, cliquez sur **[!UICONTROL Add Value]**.

   - Saisissez la première valeur que vous souhaitez voir apparaître dans la liste.

     Vous pouvez saisir une valeur pour l’administrateur et une traduction de la valeur pour chaque vue de magasin. Si vous n’avez qu’une seule vue de magasin, vous ne pouvez saisir que la valeur Admin ; elle est également utilisée pour le storefront.

   - Cliquez sur **[!UICONTROL Add Value]** et répétez l’étape précédente pour chaque option à inclure dans la liste.

   - Sélectionner **[!UICONTROL Is Default]** pour utiliser l’option comme valeur par défaut.

   ![Valeurs](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

1. Si vous souhaitez que le client choisisse une option avant d’acheter le produit, définissez **[!UICONTROL Required]** to `Yes`.

## Étape 3 : description des propriétés avancées (facultatif)

![Propriétés d’attribut avancées](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. Saisissez une variable **[!UICONTROL Attribute Code]** en minuscules, sans espaces.

1. Définir **[!UICONTROL Scope]** pour indiquer où, dans votre hiérarchie de magasins, l’attribut peut être utilisé.

   Si l’attribut est utilisé pour un [produit configurable](product-create-configurable.md), choisissez `Global`.

1. Si cet attribut s’applique uniquement à ce produit, définissez **[!UICONTROL Unique Value]** to `Yes`.

1. Pour effectuer un test de validité de toutes les données saisies dans un champ de texte, définissez **[!UICONTROL Input Validation for Store Owner]** du type de données que le champ doit contenir.

   Ce champ n’est pas disponible pour les types d’entrée avec des valeurs sélectionnées. La validation d’entrée peut être utilisée pour l’une des opérations suivantes :

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![Validation d’entrée](./assets/product-attribute-input-validation.png){width="500"}

1. Si vous souhaitez pouvoir inclure l’attribut en tant que colonne dans la grille Produits , définissez **[!UICONTROL Add to Column Options]** to `Yes`.

1. Si vous souhaitez pouvoir filtrer la variable _[!UICONTROL Products]_grille en fonction de cette colonne, définissez **[!UICONTROL Use in Filter Options]**to `Yes`.

## Etape 4 : Saisir le libellé du champ

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Manage titles]** .

1. Saisissez un **[!UICONTROL Title]** à utiliser comme libellé pour le champ.

   Si votre boutique est disponible dans différentes langues, vous pouvez saisir un titre traduit pour chaque affichage.

   ![Gestion des titres](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## Étape 5 : décrire les propriétés du storefront

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Storefront Properties]** .

   ![Propriétés Storefront](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

1. Pour rendre l’attribut disponible pour la recherche, définissez **[!UICONTROL Use in Search]** to `Yes`.

1. Pour inclure l’attribut dans la comparaison de produits, définissez **[!UICONTROL Comparable on Storefront]** to `Yes`.

1. Pour inclure des attributs de liste déroulante, de sélection multiple ou de prix dans la navigation par couches, définissez **[!UICONTROL Use in Search Results Layered Navigation]** à l’une des options suivantes :

   - `Filterable (with results)` - La navigation par calques inclut uniquement les filtres pour lesquels les produits correspondants sont disponibles. Toute valeur d’attribut qui s’applique déjà à tous les produits répertoriés dans la liste n’apparaît pas comme filtre disponible. Les valeurs d’attribut avec un nombre de correspondances de produits nul (0) sont également omises dans la liste des filtres disponibles.<br/><br/>La liste filtrée des produits inclut uniquement les produits qui correspondent au filtre. La liste des produits n’est mise à jour que si les filtres sélectionnés changent ce qui est affiché.

   - `Filterable (no results)` - La navigation par couches comprend des filtres pour toutes les valeurs d’attribut disponibles et leur nombre de produits, y compris les produits avec zéro (0) correspondance de produit. Si la valeur d’attribut est un échantillon, la valeur apparaît sous forme de filtre, mais est barrée.

1. Pour utiliser dans la navigation par couches sur les pages de résultats de recherche, définissez **[!UICONTROL Use in Search Results Navigation]** to `Yes` et saisissez un nombre dans le champ **[!UICONTROL Position]** champ .

   Le numéro de position indique la position relative de l’attribut dans le bloc de navigation superposé.

1. Pour utiliser l’attribut dans les règles de prix, définissez **[!UICONTROL Use for Promo Rule Conditions]** to `Yes`.

1. Pour que le texte puisse être formaté avec le HTML, définissez **[!UICONTROL Allow HTML Tags on Storefront]** to `Yes`.

   Ce paramètre rend l’éditeur WYSIWYG disponible lors de la modification du champ.

1. Pour inclure l’attribut dans la page du produit, définissez **[!UICONTROL Visible on Catalog Pages on Storefront]** to `Yes`.

1. Définissez les paramètres suivants, comme pris en charge par votre thème :

   - Pour inclure l’attribut dans les listes de produits, définissez **[!UICONTROL Used in Product Listing]** to `Yes`.

   - Pour utiliser l’attribut comme paramètre de tri pour les listes de produits, définissez **[!UICONTROL Used for Sorting in Product Listing]** to `Yes`.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Attribute]**.
