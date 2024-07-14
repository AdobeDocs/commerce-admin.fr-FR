---
title: Règles de catégorie pour le marchandisage
description: Découvrez comment créer une règle pour modifier dynamiquement les sélections de produits en fonction d’un ensemble de conditions.
exl-id: 765b863a-bb83-418b-9fca-ef0a148b09eb
feature: Categories, Merchandising
source-git-commit: 50951e5aae51067cdba2d8b50c1e530c7f79007a
workflow-type: tm+mt
source-wordcount: '1081'
ht-degree: 0%

---

# Règles de catégorie pour le marchandisage

{{ee-feature}}

Les règles de catégorie modifient dynamiquement la sélection de produits en fonction d’un ensemble de conditions. Chaque catégorie ne peut avoir qu’une seule règle de catégorie, bien que la règle unique puisse avoir plusieurs conditions. Vous pouvez par exemple créer une règle de catégorie pour une marque spécifique. Les produits de la même marque sont automatiquement ajoutés à la liste, même s’ils ne sont pas affectés à la même catégorie. Vous pouvez ajouter autant de conditions que nécessaire à l’expression pour décrire les produits que vous souhaitez inclure.

>[!TIP]
>
>Lors de la configuration des règles de catégorie, les produits sont _triés_, _correspondants_, _assigned_ et _non attribués_ selon cette règle **_uniquement_** lorsque cette catégorie est enregistrée. Par exemple, si vous ajoutez un produit au catalogue et que vous souhaitez l’affecter en fonction de la règle, vous **devez réenregistrer chaque catégorie** définie pour correspondre aux produits par règle. En outre, si un état de stock de produit est modifié en `In Stock` ou `Out of Stock` et que les produits de la catégorie doivent être _triés_ en fonction de la règle **[!UICONTROL Automatic Sorting]**, vous devez cliquer sur **[!UICONTROL Save Category]**.

Chaque condition se compose d’un attribut, d’une valeur et d’un opérateur logique. Seuls les attributs avec la propriété _[[!UICONTROL Use in Product Listing]](../catalog/attribute-product-create.md)_définie sur `Yes` peuvent être utilisés dans les règles de catégorie. Vous devez définir cette propriété pour l’attribut si vous souhaitez utiliser un attribut qui n’est pas inclus dans les listes de produits. Bien que les attributs de date ne soient pas pris en charge, vous pouvez utiliser les attributs Date de création ou Date de modification pour définir une date ou une plage de dates. Par exemple, pour inclure uniquement les produits créés au cours de la semaine écoulée, définissez &quot;Date de création&quot; sur la valeur `<7`.

>[!NOTE]
>
>Veillez à configurer chaque attribut utilisé dans la règle comme [_attribut_ intelligent](smart-attributes-configure.md).

![Règle de produit de catégorie](../catalog/assets/category-product-rule-with-stock.png){width="600" zoomable="yes"}

Les règles de produits de catégorie peuvent accélérer le processus d’attribution de produits spécifiques à des catégories, en fonction des conditions qui déterminent quels produits apparaissent dans la catégorie. Les attributs &quot;intelligents&quot; pouvant être utilisés avec des règles de produit de catégorie sont spécifiés dans la configuration [Visual Merchandiser](visual-merchandiser.md).

>[!NOTE]
>
>Soyez prudent lorsque vous appliquez une règle de produit de catégorie, car tous les produits qui ne respectent pas la condition sont supprimés de la catégorie. Par exemple, si vous créez une règle qui inclut uniquement les cuves violettes, toutes les autres cuves sont retirées de la catégorie .

## Étape 1 : configuration des attributs _smart_

1. Pour chaque attribut à utiliser dans la règle, assurez-vous que la propriété [[!UICONTROL Use in Product Listing]](../catalog/product-attributes.md) storefront est définie sur `Yes`.

   >[!NOTE]
   >
   >Assurez-vous que l&#39;attribut que vous sélectionnez n&#39;est PAS un _[!UICONTROL Input Type]_multi-select.

1. Renseignez la [configuration](smart-attributes-configure.md) pour identifier chaque attribut _smart_ à utiliser avec Visual Merchandiser.

## Étape 2 : création de la règle de catégorie

1. Dans l&#39;arborescence des catégories, ouvrez la catégorie à éditer.

1. Dans la section **[!UICONTROL Products in Category]**, définissez **[!UICONTROL Match products by rule]** sur `Yes`.

   Les options de tri et de condition automatiques s’affichent.

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

1. Saisissez le **[!UICONTROL Value]** qui doit correspondre.

   ![Ajouter une condition à la règle de catégorie](../catalog/assets/category-rule-create.png){width="500"}

1. Répétez cette procédure pour chaque attribut nécessaire pour décrire les conditions à remplir.

   Par exemple, pour faire correspondre des produits créés il y a entre sept et 30 jours, procédez comme suit :

   - Définissez **[!UICONTROL Date Created]** sur `Less than 30`.

   - Définissez **[!UICONTROL Logic]** sur `AND`.

     >[!NOTE]
     >
     >Lorsque vous choisissez `AND`, la règle s&#39;applique aux produits pour lesquels toutes les conditions sont remplies. Lorsque vous choisissez `OR`, cela s&#39;applique aux produits pour lesquels au moins une condition est remplie.

   - Définissez **[!UICONTROL Date Modified]** sur `Greater than 7`.

1. Pour appliquer automatiquement un ordre de tri à la liste de produits générée dynamiquement, définissez **[!UICONTROL Automatic Sorting]**.

   ![Tri automatique](./assets/automatic-sorting-field.png){width="600" zoomable="yes"}

   Les options d’ordre de tri sont définies globalement et appliquées selon les conditions actuelles. Vous ne pouvez pas définir un ordre de tri différent pour le niveau d’affichage du site web, du magasin ou du magasin.

   | Option de tri | Description |
   |-----------| -----------|
   | [!UICONTROL Stock quantity] | Tri en fonction du stock, du haut ou du bas : `Move low stock to top` ou `Move out of stock to bottom` |
   | [!UICONTROL Special price] | Tri en fonction du prix, du haut ou du bas : `Special price to top` ou `Special price to bottom` |
   | [!UICONTROL New Products] | Liste des produits les plus récents : `Newest products first` |
   | [!UICONTROL Color] | Trier par ordre alphabétique par couleur : `Sort by color` |
   | [!UICONTROL Product Names] | Tri par nom dans l’ordre croissant ou décroissant : `Name A - Z` ou `Name Z -A` |
   | [!UICONTROL SKU] | Tri par SKU dans l’ordre croissant ou décroissant : `SKU: Ascending` ou `SKU: Descending` |
   | [!UICONTROL Price] | Tri par prix dans l’ordre croissant ou décroissant : `Price: High to low` ou `Price: Low to high` |

   {style="table-layout:auto"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Category]**.

>[!NOTE]
>
>Lors de la configuration d’une règle de catégorie, les produits sont mis en correspondance et affectés à la règle lors de l’enregistrement de la catégorie. Si vous ajoutez un produit au catalogue et souhaitez l’inclure dans la règle, vous devez réenregistrer chaque catégorie définie pour qu’elle corresponde aux produits par règle. Cela garantit que le nouveau produit est inclus.

### Options de menu

- **[!UICONTROL Match products by rule]** - Détermine si la liste de produits de la catégorie est générée dynamiquement par une règle de catégorie. Options : `Yes` / `No`

- **[!UICONTROL Automatic Sorting]** - Applique automatiquement un ordre de tri à la liste des produits de catégorie. Options : `None`, `Move low stock to top`, `Move low stock to bottom`, `Special price to top`, `Special price to bottom`, `Newest products first`, `Sort by color`, `Name: A - Z`, `Name: Z - A`, `SKU: Ascending`, `SKU: Descending`, `Price: High to Low` et `Price: Low to High`

  >[!NOTE]
  >
  >Si vous disposez d’un produit configurable avec des produits enfants, le stock de produit parent est calculé en fonction du total combiné des stocks de produits enfants. Prenons l’exemple d’un produit configurable _Proteus Fitness Shirt_ avec des produits enfants orange, rouge et jaune dont les stocks diffèrent. Le stock de produit parent est calculé en fonction du total combiné du stock de produits enfants orange, rouge et jaune. Avec l’option `Move low stock to top`, il calcule le stock de produits parents en combinant tous ses stocks de produits enfants commercialisables et le trie en conséquence.

- **[!UICONTROL Add Condition]** - Ajoute une autre condition à la règle.

- **[!UICONTROL Attribute]** - Détermine l’attribut utilisé comme base de la condition. Options :

  | Option | Description |
  | ------ | ----------- |
  | `Clone Category ID(s)` | Cloner dynamiquement les produits, sans leur tri ni leur ordre, à partir de plusieurs catégories en fonction de l’ID de catégorie. |
  | `Color` | Inclut des produits en fonction de leur couleur. |
  | `Date Created (days ago)` | Inclut les produits en fonction du nombre de jours depuis l’ajout des produits au catalogue. |
  | `Date Modified (days ago)` | Inclut les produits en fonction du nombre de jours depuis la dernière modification des produits. |
  | `Name` | Inclut des produits en fonction du nom du produit. |
  | `Price` | Inclut les produits en fonction du prix. Cet attribut ne s’applique pas aux produits configurables, car ils n’ont pas leur propre prix. |
  | `Quantity` | Inclut les produits en fonction de la quantité en stock. |
  | `SKU` | Inclut des produits basés sur le SKU. |

  {style="table-layout:auto"}

  >[!NOTE]
  >
  >La quantité d’un produit configurable avec des options enfants est calculée en combinant toutes les quantités de produit enfant vendables. Prenons l’exemple d’un produit configurable _Basic Fitness Tank_ avec des options de couleur violet, rouge et jaune et différentes quantités de chaque produit. Dans ce cas, la quantité de produit parent (Basic Fitness Tank) est la quantité vendue combinée des produits enfants de couleur violet, rouge et jaune.

- **[!UICONTROL Operator]** - Indique l’opérateur appliqué à la valeur d’attribut pour remplir la condition. À moins qu’un opérateur ne soit spécifié, `Equal` est utilisé par défaut. Options : `Equal`, `Not equal`, `Greater than`, `Greater than or equal to`, `Less than`, `Less than or equal to` et `Contains`

- **[!UICONTROL Value]** - Indique la valeur que l’attribut doit avoir pour remplir la condition.

- **[!UICONTROL Logic]** - La colonne Logique permet de définir plusieurs conditions et n’apparaît que lorsqu’une autre condition est ajoutée. Les opérateurs suivent les règles de priorité pour les [ opérateurs booléens ](https://dev.mysql.com/doc/refman/8.0/en/operator-precedence.html) de MySQL. Options : `AND` / `OR`
