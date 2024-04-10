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

Bien que les attributs soient principalement gérés à partir du [Magasins](../stores-purchase/stores-menu.md) vous pouvez également ajouter de nouveaux attributs _en vol_ lorsque vous travaillez sur un produit. Vous pouvez choisir dans la liste des attributs existants ou créer un attribut. Le nouvel attribut est ajouté au [jeu d’attributs](../catalog/attribute-sets.md) sur lequel le produit est basé.

## Étape 1 : ajouter un attribut

1. Ouvrez le produit en mode d’édition.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Attribute]**.

   ![Nouveau produit avec un jeu d’attributs par défaut](./assets/product-attribute-add.png){width="600" zoomable="yes"}

1. Pour ajouter un attribut existant au produit, utilisez [contrôles de filtre](../getting-started/admin-grid-controls.md) pour rechercher l’attribut dans la grille et procéder comme suit :

   - Cochez la case située dans la première colonne de chaque attribut à ajouter.

   - Clic **[!UICONTROL Add Selected]**.

   ![Sélectionner un attribut](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

1. Pour définir un nouvel attribut, cliquez sur **[!UICONTROL Create New Attribute]** et effectuez les tâches de l’étape 2.

## Étape 2 : décrire les propriétés d’attribut de base

![Propriétés d’attribut](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

1. Sous _[!UICONTROL Attribute Properties]_, saisissez un **[!UICONTROL Attribute Label]**pour identifier l’attribut.

1. Définir **[!UICONTROL Catalog Input Type for Store Owner]** au type de [contrôle d&#39;entrée](attributes-input-types.md) à utiliser pour la saisie de données.

   Si l’attribut est utilisé pour un [produit configurable](product-create-configurable.md), choisissez `Dropdown`. Ensuite, définissez **[!UICONTROL Required]** vers `Yes`.

1. Pour `Dropdown` et `Multiple Select` types d’entrée, procédez comme suit :

   - Sous **[!UICONTROL Values]**, cliquez sur **[!UICONTROL Add Value]**.

   - Saisissez la première valeur qui doit apparaître dans la liste.

     Vous pouvez saisir une valeur pour l’administrateur et une traduction de la valeur pour chaque vue de magasin. Si vous n’avez qu’une seule vue de magasin, vous ne pouvez saisir que la valeur Admin. Elle est également utilisée pour le storefront.

   - Clic **[!UICONTROL Add Value]** et répétez l’étape précédente pour chaque option que vous souhaitez inclure dans la liste.

   - Sélectionner **[!UICONTROL Is Default]** pour utiliser l’option comme valeur par défaut.

   ![Valeurs](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

1. Si vous souhaitez que le client choisisse une option avant l’achat du produit, définissez **[!UICONTROL Required]** vers `Yes`.

## Étape 3 : décrire les propriétés avancées (facultatif)

![Propriétés d’attribut avancées](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. Saisir un unique **[!UICONTROL Attribute Code]** en minuscules et sans espaces.

1. Définir **[!UICONTROL Scope]** pour indiquer où, dans la hiérarchie de votre magasin, l’attribut peut être utilisé.

   Si l’attribut est utilisé pour un [produit configurable](product-create-configurable.md), choisissez `Global`.

1. Si cet attribut s’applique uniquement à ce produit, définissez **[!UICONTROL Unique Value]** vers `Yes`.

1. Pour exécuter un test de validité de toutes les données saisies dans un champ de texte, définissez **[!UICONTROL Input Validation for Store Owner]** au type de données que le champ doit contenir.

   Ce champ n’est pas disponible pour les types d’entrée avec des valeurs sélectionnées. La validation d’entrée peut être utilisée pour l’un des éléments suivants :

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![Validation des entrées](./assets/product-attribute-input-validation.png){width="500"}

1. Si vous souhaitez pouvoir inclure l’attribut en tant que colonne dans la grille Produits, définissez **[!UICONTROL Add to Column Options]** vers `Yes`.

1. Si vous souhaitez pouvoir filtrer les _[!UICONTROL Products]_grille selon cette colonne, définir **[!UICONTROL Use in Filter Options]**vers `Yes`.

## Étape 4 : saisir le libellé du champ

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) le **[!UICONTROL Manage titles]** section.

1. Saisir un **[!UICONTROL Title]** à utiliser comme libellé pour le champ.

   Si votre boutique est disponible dans différentes langues, vous pouvez saisir un titre traduit pour chaque affichage.

   ![Gérer les titres](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## Étape 5 : décrire les propriétés du storefront

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) le **[!UICONTROL Storefront Properties]** section.

   ![Propriétés du storefront](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

1. Pour rendre l’attribut disponible pour la recherche, définissez **[!UICONTROL Use in Search]** vers `Yes`.

1. Pour inclure l’attribut dans la comparaison de produits, définissez **[!UICONTROL Comparable on Storefront]** vers `Yes`.

1. Pour inclure des attributs de liste déroulante, de sélection multiple ou de prix dans une navigation superposée, définissez **[!UICONTROL Use in Search Results Layered Navigation]** à l’un des éléments suivants :

   - `Filterable (with results)` - La navigation en couches inclut uniquement les filtres pour lesquels des produits correspondants peuvent être trouvés. Toute valeur d’attribut qui s’applique déjà à tous les produits affichés dans la liste n’apparaît pas comme un filtre disponible. Les valeurs d’attribut avec un nombre de zéro (0) correspondance de produit sont également omises de la liste des filtres disponibles.<br/><br/>La liste filtrée de produits inclut uniquement les produits qui correspondent au filtre. La liste des produits n’est mise à jour que si les filtres sélectionnés modifient ce qui s’affiche.

   - `Filterable (no results)` - La navigation en couches comprend des filtres pour toutes les valeurs d’attribut disponibles et leur nombre de produits, y compris les produits sans correspondance de produit (0). Si la valeur de l’attribut est un échantillon, la valeur apparaît comme un filtre, mais est barrée.

   >[!NOTE]
   >
   >Lorsque le _[!UICONTROL Use in Search]_paramètre est défini sur `No`, le_[!UICONTROL Use in Search Results Layered Navigation]_ le paramètre n’est pas affiché et l’attribut de produit n’est pas utilisé dans la recherche avec [!UICONTROL Use in Layered Navigation] définition de la valeur .

1. Pour utiliser l’attribut dans une navigation superposée sur les pages de résultats de recherche, définissez **[!UICONTROL Use in Search Results Layered Navigation]** vers `Yes` et saisissez un nombre dans le champ **[!UICONTROL Position]** champ .

   Le numéro de position indique la position relative de l’attribut dans le bloc de navigation superposé.

   >[!NOTE]
   >
   >Le _[!UICONTROL Position]_Le champ est grisé par défaut et vous devez enregistrer l’attribut avant de pouvoir modifier ce paramètre.

1. Pour utiliser l’attribut dans les règles de prix, définissez **[!UICONTROL Use for Promo Rule Conditions]** vers `Yes`.

1. Pour permettre la mise en forme du texte avec le HTML, définissez **[!UICONTROL Allow HTML Tags on Storefront]** vers `Yes`.

   Ce paramètre rend l’éditeur WYSIWYG disponible lors de la modification du champ.

1. Pour inclure l’attribut dans la page de produit, définissez **[!UICONTROL Visible on Catalog Pages on Storefront]** vers `Yes`.

1. Renseignez les paramètres suivants comme pris en charge par votre thème :

   - Pour inclure l’attribut dans les listes de produits, définissez **[!UICONTROL Used in Product Listing]** vers `Yes`.

   - Pour utiliser l’attribut comme paramètre de tri pour les listes de produits, définissez **[!UICONTROL Used for Sorting in Product Listing]** vers `Yes`.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Attribute]**.
