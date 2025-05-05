---
title: Affectations de produits de catégorie
description: Découvrez comment utiliser les paramètres [!UICONTROL Products in Category] pour contrôler quels produits sont actuellement affectés à la catégorie.
exl-id: e7ab11c0-2d55-4824-a397-a1c858344d4f
feature: Catalog Management, Categories, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 0%

---

# Affectations de produits de catégorie

Pour une catégorie, utilisez la section _[!UICONTROL Products in Category]_&#x200B;pour passer en revue les produits actuellement affectés à la catégorie. Les filtres de recherche situés en haut de chaque colonne sont utilisés pour ajouter et supprimer des produits de la catégorie. Vous pouvez également utiliser des [règles de catégorie](../merchandising-promotions/category-product-rules.md) ( ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce uniquement) pour modifier dynamiquement la sélection de produits lorsqu’un ensemble de conditions est satisfait. Pour en savoir plus, voir [Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md)).

>[!TIP]
>
>Lors de la configuration des règles de catégorie, les produits sont _triés_, _correspondants_, _assigned_ et _non attribués_ selon cette règle **_uniquement_** lorsque cette catégorie est enregistrée. Pour vous assurer qu’un nouveau produit est attribué en fonction de la règle lorsque vous l’ajoutez au catalogue, vous **devez réenregistrer chaque catégorie** définie pour correspondre aux produits par règle. En outre, si un statut de stock de produit est modifié en `In Stock` ou `Out of Stock` et que les produits de la catégorie sont _triés_ conformément à la règle **Tri automatique**, vous devez cliquer sur **[!UICONTROL Save Category]**.

![Produits de catégorie](./assets/category-products-in-category.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Sur les pages de catégorie, `Out of stock` produits sont toujours affichés **_après_** `In Stock` produits sur la liste de produits avec tous les types de tri.

>[!NOTE]
>
>La colonne _Stock_ affiche uniquement la quantité vendable de produits pour _&#x200B;**l’étendue de catégorie sélectionnée**&#x200B;_. Lorsque plusieurs stocks sont gérés pour les produits, vous devez basculer entre les portées correspondantes pour afficher d’autres valeurs de colonne _Stock_ dans la grille _Produits de catégorie_.

## Appliquer une règle de catégorie

{{ee-feature}}

1. Définissez **[!UICONTROL Match products by rule]** sur `Yes`.

   Les options de tri et de condition automatiques s’affichent.

   ![Pour faire correspondre des produits par règle](./assets/category-match-products-by-rule.png){width="600" zoomable="yes"}

1. Définissez l’ordre **[!UICONTROL Automatic Sorting]**.

   Ce tri automatique est basé sur les conditions actuelles.

   - `Stock level` - Déplacer vers le haut ou le bas.
   - `Special price` - Déplacer vers le haut ou le bas.
   - `New Products` - Listez d’abord les produits les plus récents.
   - `Color` - Trier par ordre alphabétique par couleur.
   - `Name` - Tri par ordre croissant ou décroissant selon le nom.
   - `SKU` - Tri par ordre croissant ou décroissant selon le SKU
   - `Price` - Tri par ordre croissant ou décroissant selon le prix.

1. Cliquez sur **[!UICONTROL Add Condition]** et procédez comme suit :

   - Sélectionnez le **[!UICONTROL Attribute]** qui est la base de la condition.
   - Sélectionnez les **[!UICONTROL Operator]** requis pour former l’expression.
   - Saisissez le **[!UICONTROL Value]** qui doit correspondre.

   ![Ajouter une condition à la règle de catégorie](./assets/category-rule-create.png){width="600" zoomable="yes"}

   Répétez cette procédure pour chaque attribut à utiliser pour décrire les conditions à remplir. Par exemple, pour faire correspondre les produits créés il y a 7 à 30 jours, procédez comme suit :

   - Définissez **[!UICONTROL Date Created]** sur `Less than 30`.
   - Définissez **[!UICONTROL Logic]** sur `AND`.
   - Définissez **[!UICONTROL Date Modified]** sur `Greater than 7`.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Category]**.

### Options de page

| Option | Description |
|--- |--- |
| [!UICONTROL Match products by rule] | Détermine si la liste des produits de la catégorie est générée dynamiquement par une règle de catégorie. Options : `Yes` / `No` |
| [!UICONTROL Automatic Sorting] | Applique automatiquement un ordre de tri à la liste des produits de la catégorie. Options : <br/>`None`<br/>`Move low stock to top`<br/>`Move low stock to bottom`<br/>`Special price to top`<br/>`Special price to bottom`<br/>`Newest products first`<br/>`Sort by color`<br/>`Name: A - Z`<br/>`Name: Z - A`<br/>`SKU: Ascending`<br/>`SKU: Descending`<br/>`Price: High to Low`<br/>`Price: Low to High` |
| [!UICONTROL Add Condition] | Ajoute une autre condition à la règle. |

{style="table-layout:auto"}

### Conditions de page

| Option | Description |
|--- |--- |
| [!UICONTROL Attribute] | Détermine l’attribut utilisé comme base de la condition. Options : <br/>**[!UICONTROL Clone Category ID(s)]**- Cloner dynamiquement les produits, sans leur tri ni leur ordre, à partir de plusieurs catégories basées sur l’ID de catégorie.<br/>**[!UICONTROL Color]** - Inclut des produits en fonction de leur couleur. <br/>**[!UICONTROL Date Created (days ago)]**- Inclut les produits en fonction du nombre de jours depuis l’ajout des produits au catalogue.<br/>**[!UICONTROL Date Modified (days ago)]** - Inclut les produits en fonction du nombre de jours depuis la dernière modification des produits. <br/>**[!UICONTROL Name]**- Inclut des produits en fonction du nom du produit.<br/>**[!UICONTROL Price]** - Inclut les produits en fonction du prix. <br/>**[!UICONTROL Quantity]**- Inclut les produits en fonction de la quantité en stock.<br/>**&#x200B; SKU &#x200B;**- Inclut des produits basés sur le SKU. |
| [!UICONTROL Operator] | Indique l’opérateur appliqué à la valeur d’attribut pour remplir la condition. À moins qu’un opérateur ne soit spécifié, `Equal` est utilisé par défaut. Options : `Equal` / `Not equal` / `Greater than` / `Greater than or equal to` / `Less than` / `Less than or equal to` / `Contains` |
| [!UICONTROL Value] | Indique la valeur que l’attribut doit avoir pour remplir la condition. |
| [!UICONTROL Logic] | Utilisé pour définir plusieurs conditions et apparaît uniquement lorsqu’une autre condition est ajoutée. Options : `OR` / `AND` |

{style="table-layout:auto"}

>[!NOTE]
>
>La quantité d’un produit configurable avec des options enfants est calculée en combinant toutes les quantités de produit enfant vendables. Prenons l’exemple d’un produit configurable _Endurance Fitness Tank_ avec des options de couleur violet, rouge et jaune et différentes quantités de chaque produit. Dans ce scénario, la quantité du produit parent est la quantité vendue combinée des produits enfants de couleur violet, rouge et jaune.

## Contrôles


## Contrôles de page

{{ee-feature}}

| Contrôle | Description |
|----------|--------------|
| ![Afficher en tant que liste](../assets/icon-view-list.png) | Afficher sous forme de liste |
| ![Afficher comme mosaïques](../assets/icon-view-tiles.png) | Afficher comme mosaïques |
| ![Basculer sur no](../assets/toggle-no.png) | Correspondance par règle - Non |
| ![Activer/désactiver oui](../assets/toggle-yes.png) | Correspondance par règle - Oui |
| ![Déplacer le contrôleur](../assets/icon-move.png) | La commande glisser-déposer permet de saisir un produit et de le déplacer vers une autre position sur la page active de la grille. Pour en savoir plus, voir [Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md). |
| ![Contrôleur de position](../assets/control-position.png) | Détermine la position du produit dans la liste. |

{style="table-layout:auto"}

## Contrôles de page

{{ce-feature}}

| Contrôle | Description |
|----------|--------------|
| ![Case à cocher sélectionnée](../assets/checkbox-selected.png) | Cochez la case dans l’en-tête de la première colonne pour sélectionner tous les produits ou effacer toutes les sélections. Le contrôle de la première ligne détermine le type de recherche et peut être défini pour inclure n’importe quel enregistrement ou n’inclure que les enregistrements attribués ou non à la catégorie. La case à cocher située dans la première colonne de chaque ligne identifie les produits à ajouter à la catégorie. Options : `Yes` / `No` / `Any` |
| [!UICONTROL Search Filters] | Les contrôles de filtre en haut de chaque colonne peuvent être utilisés pour saisir des valeurs spécifiques que vous souhaitez inclure ou omettre dans la liste, selon le paramètre Tout sélectionner . |
| [!UICONTROL Reset Filter] | Efface tous les filtres de recherche. |
| [!UICONTROL Search] | Recherche le catalogue en fonction des critères de filtrage et affiche le résultat. |

{style="table-layout:auto"}
