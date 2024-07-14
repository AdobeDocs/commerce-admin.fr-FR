---
title: Ajout d’attributs à un produit
description: Découvrez comment ajouter des attributs aux produits de votre catalogue.
exl-id: 1f92807a-2362-48a2-8d3a-4aef90a5671f
feature: Catalog Management, Products
source-git-commit: 99049260b4ff490845affd1c98fa4d2536edebd7
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 0%

---

# Ajout d’attributs à un produit

Bien que les attributs soient principalement gérés à partir du menu [Magasins](../stores-purchase/stores-menu.md), vous pouvez également ajouter de nouveaux attributs _à la volée_ lorsque vous travaillez sur un produit. Vous pouvez choisir dans la liste des attributs existants ou créer un attribut. Le nouvel attribut est ajouté au [jeu d’attributs](../catalog/attribute-sets.md) sur lequel repose le produit.

## Étape 1 : Ajout d’un attribut

1. Ouvrez le produit en mode d’édition.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Attribute]**.

   ![Nouveau produit avec jeu d’attributs par défaut](./assets/product-attribute-add.png){width="600" zoomable="yes"}

1. Pour ajouter un attribut existant au produit, utilisez les [contrôles de filtre](../getting-started/admin-grid-controls.md) pour trouver l’attribut dans la grille et procédez comme suit :

   - Cochez la case dans la première colonne de chaque attribut à ajouter.

   - Cliquez sur **[!UICONTROL Add Selected]**.

   ![Sélectionner un attribut](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

1. Pour définir un nouvel attribut, cliquez sur **[!UICONTROL Create New Attribute]** et complétez les éléments de l’étape 2.

## Etape 2 : décrire les propriétés de l&#39;attribut de base

![Propriétés d’attribut](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

1. Sous _[!UICONTROL Attribute Properties]_, saisissez un **[!UICONTROL Attribute Label]**pour identifier l’attribut.

1. Définissez **[!UICONTROL Catalog Input Type for Store Owner]** sur le type de [contrôle d’entrée](attributes-input-types.md) à utiliser pour la saisie de données.

   Si l’attribut est utilisé pour un [produit configurable](product-create-configurable.md), choisissez `Dropdown`. Définissez ensuite **[!UICONTROL Required]** sur `Yes`.

1. Pour les types d’entrée `Dropdown` et `Multiple Select`, procédez comme suit :

   - Sous **[!UICONTROL Values]**, cliquez sur **[!UICONTROL Add Value]**.

   - Saisissez la première valeur que vous souhaitez voir apparaître dans la liste.

     Vous pouvez saisir une valeur pour l’administrateur et une traduction de la valeur pour chaque vue de magasin. Si vous n’avez qu’une seule vue de magasin, vous ne pouvez saisir que la valeur Admin ; elle est également utilisée pour le storefront.

   - Cliquez sur **[!UICONTROL Add Value]** et répétez l’étape précédente pour chaque option que vous souhaitez inclure dans la liste.

   - Sélectionnez **[!UICONTROL Is Default]** pour utiliser l’option comme valeur par défaut.

   ![Valeurs](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

1. Si vous souhaitez que le client choisisse une option avant que le produit puisse être acheté, définissez **[!UICONTROL Required]** sur `Yes`.

## Étape 3 : description des propriétés avancées (facultatif)

![Propriétés d’attribut avancées](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. Saisissez un **[!UICONTROL Attribute Code]** unique en minuscules, sans espaces.

1. Définissez **[!UICONTROL Scope]** pour indiquer où, dans votre hiérarchie de magasins, l’attribut peut être utilisé.

   Si l’attribut est utilisé pour un [produit configurable](product-create-configurable.md), choisissez `Global`.

1. Si cet attribut s’applique uniquement à ce produit, définissez **[!UICONTROL Unique Value]** sur `Yes`.

1. Pour exécuter un test de validité de toutes les données saisies dans un champ de texte, définissez **[!UICONTROL Input Validation for Store Owner]** sur le type de données que le champ doit contenir.

   Ce champ n’est pas disponible pour les types d’entrée avec des valeurs sélectionnées. La validation d’entrée peut être utilisée pour l’une des opérations suivantes :

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![Validation d’entrée](./assets/product-attribute-input-validation.png){width="500"}

1. Si vous souhaitez pouvoir inclure l’attribut en tant que colonne dans la grille Produits, définissez **[!UICONTROL Add to Column Options]** sur `Yes`.

1. Si vous souhaitez pouvoir filtrer la grille _[!UICONTROL Products]_en fonction de cette colonne, définissez **[!UICONTROL Use in Filter Options]**sur `Yes`.

## Etape 4 : Saisir le libellé du champ

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Manage titles]** .

1. Saisissez un **[!UICONTROL Title]** à utiliser comme libellé pour le champ.

   Si votre boutique est disponible dans différentes langues, vous pouvez saisir un titre traduit pour chaque affichage.

   ![Gérer les titres](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## Étape 5 : décrire les propriétés du storefront

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Storefront Properties]** .

   ![Propriétés Storefront](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

1. Pour rendre l’attribut disponible pour la recherche, définissez **[!UICONTROL Use in Search]** sur `Yes`.

1. Pour inclure l’attribut dans la comparaison de produits, définissez **[!UICONTROL Comparable on Storefront]** sur `Yes`.

1. Pour inclure des attributs de liste déroulante, de sélection multiple ou de prix dans la navigation par couches, définissez **[!UICONTROL Use in Search Results Layered Navigation]** sur l’un des paramètres suivants :

   - `Filterable (with results)` - La navigation par calques inclut uniquement les filtres pour lesquels les produits correspondants peuvent être trouvés. Toute valeur d’attribut qui s’applique déjà à tous les produits répertoriés dans la liste n’apparaît pas comme filtre disponible. Les valeurs d’attribut avec un nombre de correspondances de produits nul (0) sont également omises dans la liste des filtres disponibles.<br/><br/>La liste filtrée des produits inclut uniquement les produits qui correspondent au filtre. La liste des produits n’est mise à jour que si les filtres sélectionnés changent ce qui est affiché.

   - `Filterable (no results)` - La navigation en couches comprend des filtres pour toutes les valeurs d’attribut disponibles et leur nombre de produits, y compris les produits avec zéro (0) correspondance de produits. Si la valeur d’attribut est un échantillon, la valeur apparaît sous forme de filtre, mais est barrée.

   >[!NOTE]
   >
   >Lorsque le paramètre _[!UICONTROL Use in Search]_est défini sur `No`, le paramètre_[!UICONTROL Use in Search Results Layered Navigation]_ n’est pas affiché et l’attribut product n’est pas utilisé dans la recherche avec une valeur de paramètre [!UICONTROL Use in Layered Navigation].

1. Pour utiliser l’attribut dans la navigation par couches sur les pages de résultats de recherche, définissez **[!UICONTROL Use in Search Results Layered Navigation]** sur `Yes` et saisissez un nombre dans le champ **[!UICONTROL Position]**.

   Le numéro de position indique la position relative de l’attribut dans le bloc de navigation superposé.

   >[!NOTE]
   >
   >Le champ _[!UICONTROL Position]_est grisé par défaut et vous devez enregistrer l’attribut avant de pouvoir modifier ce paramètre.

1. Pour utiliser l’attribut dans les règles de prix, définissez **[!UICONTROL Use for Promo Rule Conditions]** sur `Yes`.

1. Pour autoriser le formatage du texte avec HTML, définissez **[!UICONTROL Allow HTML Tags on Storefront]** sur `Yes`.

   Ce paramètre rend l’éditeur WYSIWYG disponible lors de la modification du champ.

1. Pour inclure l’attribut sur la page du produit, définissez **[!UICONTROL Visible on Catalog Pages on Storefront]** sur `Yes`.

1. Définissez les paramètres suivants, comme pris en charge par votre thème :

   - Pour inclure l’attribut dans les listes de produits, définissez **[!UICONTROL Used in Product Listing]** sur `Yes`.

   - Pour utiliser l’attribut comme paramètre de tri pour les listes de produits, définissez **[!UICONTROL Used for Sorting in Product Listing]** sur `Yes`.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Attribute]**.
