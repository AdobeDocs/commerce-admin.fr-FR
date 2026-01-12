---
title: Affectations de produits de catégorie
description: Découvrez comment utiliser les paramètres [!UICONTROL Products in Category] pour contrôler quels produits sont actuellement affectés à la catégorie.
exl-id: e7ab11c0-2d55-4824-a397-a1c858344d4f
feature: Catalog Management, Categories, Products
source-git-commit: 5aea3aa13ab0eb74866fc0cbcbfe08b5099abe95
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# Affectations de produits de catégorie

Pour une catégorie, utilisez la section _[!UICONTROL Products in Category]_&#x200B;pour passer en revue les produits actuellement affectés à la catégorie. Les filtres de recherche en haut de chaque colonne sont utilisés pour ajouter et supprimer des produits de la catégorie. Vous pouvez également utiliser des [règles de catégorie](../merchandising-promotions/category-product-rules.md) ( ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce uniquement) pour modifier de manière dynamique la sélection de produits lorsqu’un ensemble de conditions est rempli. Pour en savoir plus, voir [Marchandiseur visuel](../merchandising-promotions/visual-merchandiser.md)).

>[!TIP]
>
>Lors de la configuration des règles de catégorie, les produits sont _triés_, _mis en correspondance_, _affectés_ et _non affectés_ en fonction de cette règle **_uniquement_** lorsque cette catégorie est enregistrée. Pour vous assurer qu’un nouveau produit est affecté en fonction de la règle lorsque vous l’ajoutez au catalogue, vous **devez réenregistrer chaque catégorie** définie pour correspondre aux produits par règle. En outre, si un statut de stock de produits est remplacé par `In Stock` ou `Out of Stock` et que les produits de la catégorie sont _triés_ conformément à la règle **Tri automatique**, vous devez cliquer sur **[!UICONTROL Save Category]**.

![Produits de catégorie](./assets/category-products-in-category.png){width="600" zoomable="yes"}

>[!NOTE]
>
>La colonne _Stock_ affiche la quantité de produits disponible pour _&#x200B;**portée de catégorie sélectionnée**&#x200B;_ uniquement. Lorsque plusieurs stocks sont gérés pour des produits, vous devez basculer entre les portées correspondantes pour afficher d’autres valeurs de colonne _Stock_ dans la grille _Produits de catégorie_.

## Application d’une règle de catégorie

{{ee-feature}}

1. Définissez **[!UICONTROL Match products by rule]** sur `Yes`.

   Les options de tri et de condition automatiques s’affichent.

   ![Pour faire correspondre les produits par règle](./assets/category-match-products-by-rule.png){width="600" zoomable="yes"}

1. Définissez l’ordre de **[!UICONTROL Automatic Sorting]**.

   Ce tri automatique est basé sur les conditions actuelles.

   - `Stock level` - Déplacer vers le haut ou le bas.
   - `Special price` - Déplacer vers le haut ou le bas.
   - `New Products` - Commencez par répertorier les produits les plus récents.
   - `Color` - Triez par couleur dans l’ordre alphabétique.
   - `Name` - Triez les ressources par nom, par ordre croissant ou décroissant.
   - `SKU` - Trier par ordre croissant ou décroissant par SKU
   - `Price` - Triez par ordre croissant ou décroissant de prix.

1. Cliquez sur **[!UICONTROL Add Condition]** et procédez comme suit :

   - Sélectionnez le **[!UICONTROL Attribute]** qui est à la base de la condition.
   - Sélectionnez le **[!UICONTROL Operator]** requis pour former l’expression.
   - Saisissez le **[!UICONTROL Value]** à mettre en correspondance.

   ![Ajouter une condition à la règle de catégorie](./assets/category-rule-create.png){width="600" zoomable="yes"}

   Répétez ce processus pour chaque attribut à utiliser afin de décrire les conditions à remplir. Par exemple, pour faire correspondre des produits créés il y a de 7 à 30 jours, procédez comme suit :

   - Définissez **[!UICONTROL Date Created]** sur `Less than 30`.
   - Définissez **[!UICONTROL Logic]** sur `AND`.
   - Définissez **[!UICONTROL Date Modified]** sur `Greater than 7`.

1. Cliquez ensuite sur **[!UICONTROL Save Category]**.

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
| [!UICONTROL Attribute] | Détermine l’attribut utilisé comme base de la condition. Options : <br/>**[!UICONTROL Clone Category ID(s)]**- clone dynamiquement les produits, sans leur tri ni leur ordre, à partir de plusieurs catégories en fonction de l’ID de catégorie.<br/>**[!UICONTROL Color]** - Inclut des produits en fonction de la couleur. <br/>**[!UICONTROL Date Created (days ago)]**- Inclut les produits en fonction du nombre de jours écoulés depuis leur ajout au catalogue.<br/>**[!UICONTROL Date Modified (days ago)]** - Inclut les produits en fonction du nombre de jours écoulés depuis la dernière modification des produits. <br/>**[!UICONTROL Name]**- Inclut les produits en fonction du nom du produit.<br/>**[!UICONTROL Price]** - Inclut les produits en fonction du prix. <br/>**[!UICONTROL Quantity]**- Inclut les produits en fonction de la quantité en stock.<br/>**&#x200B; SKU &#x200B;**- Inclut les produits basés sur SKU. |
| [!UICONTROL Operator] | Spécifie l&#39;opérateur appliqué à la valeur d&#39;attribut pour remplir la condition. Sauf si un opérateur est spécifié, `Equal` est utilisé par défaut. Options : `Equal` / `Not equal` / `Greater than` / `Greater than or equal to` / `Less than` / `Less than or equal to` / `Contains` |
| [!UICONTROL Value] | Indique la valeur que l’attribut doit avoir pour remplir la condition. |
| [!UICONTROL Logic] | Utilisé pour définir plusieurs conditions, et s’affiche uniquement lorsqu’une autre condition est ajoutée. Options : `OR` / `AND` |

{style="table-layout:auto"}

>[!NOTE]
>
>La quantité d&#39;un produit configurable avec options enfants est calculée en combinant toutes les quantités de produits enfants. Prenons l’exemple d’un produit configurable _Endurance Fitness Tank_ avec des options de couleur violette, rouge et jaune et différentes quantités de chacune. Dans ce scénario, la quantité du produit parent est la quantité combinée des produits enfants violets, rouges et jaunes.

## Contrôles


## Contrôles de page

{{ee-feature}}

| Contrôle | Description |
|----------|--------------|
| ![Afficher comme liste](../assets/icon-view-list.png) | Afficher comme liste |
| ![Afficher en mosaïque](../assets/icon-view-tiles.png) | Afficher en mosaïques |
| ![Basculer no](../assets/toggle-no.png) | Correspondance par règle - Non |
| ![Activer/désactiver oui](../assets/toggle-yes.png) | Correspondance par règle - Oui |
| ![Déplacer contrôleur](../assets/icon-move.png) | La commande Glisser-déposer permet de saisir un produit et de le déplacer vers un autre emplacement de la page active de la grille. Pour en savoir plus, voir [Marchandiseur visuel](../merchandising-promotions/visual-merchandiser.md). |
| ![Contrôleur de position](../assets/control-position.png) | Détermine la position du produit dans la liste. |

{style="table-layout:auto"}

## Contrôles de page

{{ce-feature}}

| Contrôle | Description |
|----------|--------------|
| ![Case à cocher sélectionnée](../assets/checkbox-selected.png) | Utilisez la case à cocher située dans l’en-tête de la première colonne pour sélectionner tous les produits ou effacer toutes les sélections. Le contrôle de la première ligne détermine le type de recherche et peut être défini pour inclure n&#39;importe quel enregistrement ou inclure uniquement les enregistrements affectés ou non affectés à la catégorie. La case à cocher située dans la première colonne de chaque ligne identifie les produits à ajouter à la catégorie. Options : `Yes` / `No` / `Any` |
| [!UICONTROL Search Filters] | Les contrôles de filtre en haut de chaque colonne peuvent être utilisés pour saisir des valeurs spécifiques que vous souhaitez inclure ou omettre dans la liste, selon le paramètre Tout sélectionner . |
| [!UICONTROL Reset Filter] | Efface tous les filtres de recherche. |
| [!UICONTROL Search] | Effectue une recherche dans le catalogue en fonction des critères de filtrage et affiche le résultat. |

{style="table-layout:auto"}
