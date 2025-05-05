---
title: Règles de catégorie pour le marchandisage
description: Découvrez comment créer des règles pour modifier de manière dynamique les sélections de produits en fonction d’un ensemble de conditions.
exl-id: 765b863a-bb83-418b-9fca-ef0a148b09eb
feature: Categories, Merchandising
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '1098'
ht-degree: 0%

---

# Règles de catégorie pour le marchandisage

{{ee-feature}}

Les règles de catégorie modifient dynamiquement la sélection de produits en fonction d’un ensemble de conditions. Chaque catégorie ne peut avoir qu’une seule règle de catégorie, bien qu’une seule règle puisse avoir plusieurs conditions. Par exemple, vous pouvez créer une règle de catégorie pour une marque spécifique. Les produits de la même marque sont automatiquement ajoutés à la liste, même s’ils ne sont pas affectés à la même catégorie. Vous pouvez ajouter autant de conditions à l’expression que nécessaire pour décrire les produits que vous souhaitez inclure.

>[!TIP]
>
>Lors de la configuration des règles de catégorie, les produits sont _triés_, _mis en correspondance_, _affectés_ et _non affectés_ en fonction de cette règle **_uniquement_** lorsque cette catégorie est enregistrée. Par exemple, si vous ajoutez un produit au catalogue et souhaitez l’affecter en fonction de la règle, vous **devez réenregistrer chaque catégorie** définie pour correspondre aux produits par règle. En outre, si un statut de stock de produits est modifié en `In Stock` ou `Out of Stock` et que les produits de la catégorie doivent être _triés_ conformément à la règle de **[!UICONTROL Automatic Sorting]**, vous devez cliquer sur **[!UICONTROL Save Category]**.

Chaque condition se compose d’un attribut, d’une valeur et d’un opérateur logique. Seuls les attributs dont la propriété _[[!UICONTROL Use in Product Listing]](../catalog/attribute-product-create.md)_est définie sur `Yes` peuvent être utilisés dans les règles de catégorie. Vous devez définir cette propriété pour l’attribut si vous souhaitez utiliser un attribut qui n’est pas inclus dans les listes de produits. Bien que les attributs de date ne soient pas pris en charge, vous pouvez utiliser les attributs Date de création ou Date de modification pour définir une date ou une plage de dates. Par exemple, pour inclure uniquement les produits qui ont été créés au cours de la semaine écoulée, définissez « Date de création » sur une valeur de `<7`.

>[!NOTE]
>
>Veillez à configurer chaque attribut utilisé dans la règle en tant qu’attribut [_intelligent_](smart-attributes-configure.md).

![Règle de produit de catégorie](../catalog/assets/category-product-rule-with-stock.png){width="600" zoomable="yes"}

Les règles de produits de catégorie peuvent accélérer le processus d’affectation de produits spécifiques à des catégories, en fonction des conditions qui déterminent quels produits apparaissent dans la catégorie. Les attributs « intelligents » pouvant être utilisés avec les règles de produit de catégorie sont spécifiés dans la configuration [Visual Merchandiser](visual-merchandiser.md).

>[!NOTE]
>
>Soyez prudent lorsque vous appliquez une règle de produit de catégorie, car tous les produits qui ne remplissent pas la condition sont supprimés de la catégorie. Par exemple, si vous créez une règle qui inclut uniquement les débardeurs violets, tous les autres débardeurs sont supprimés de la catégorie.

## Étape 1 : configurer les attributs _intelligents_

1. Pour chaque attribut à utiliser dans la règle, assurez-vous que la propriété storefront [[!UICONTROL Use in Product Listing]](../catalog/product-attributes.md) est définie sur `Yes`.

   >[!NOTE]
   >
   >Assurez-vous que l’attribut que vous sélectionnez n’est PAS un _[!UICONTROL Input Type]_&#x200B;à sélection multiple.

1. Effectuez la [configuration](smart-attributes-configure.md) pour identifier chaque attribut _intelligent_ à utiliser avec Visual Merchandiser.

## Étape 2 : créer la règle de catégorie

1. Dans l’arborescence des catégories, ouvrez la catégorie à modifier.

1. Dans la section **[!UICONTROL Products in Category]**, définissez **[!UICONTROL Match products by rule]** sur `Yes`.

   Les options de tri et de condition automatiques s’affichent.

1. Cliquez sur **[!UICONTROL Add Condition]**.

1. Sélectionnez le **[!UICONTROL Attribute]** qui est à la base de la condition.

1. Définissez **[!UICONTROL Operator]** sur l’une des options suivantes :

   - `Equal`
   - `Not equal`
   - `Greater than`
   - `Greater than or equal to`
   - `Less than`
   - `Less than or equal to`
   - `Contains`

1. Saisissez le **[!UICONTROL Value]** à mettre en correspondance.

   ![Ajouter une condition à la règle de catégorie](../catalog/assets/category-rule-create.png){width="500"}

1. Répétez ce processus pour chaque attribut nécessaire à la description des conditions à remplir.

   Par exemple, pour faire correspondre des produits créés il y a entre sept et 30 jours, procédez comme suit :

   - Définissez **[!UICONTROL Date Created]** sur `Less than 30`.

   - Définissez **[!UICONTROL Logic]** sur `AND`.

     >[!NOTE]
     >
     >Lorsque vous choisissez `AND`, la règle s’applique aux produits pour lesquels toutes les conditions sont remplies. Lorsque vous choisissez `OR`, cela s’applique aux produits pour lesquels au moins une condition est remplie.

   - Définissez **[!UICONTROL Date Modified]** sur `Greater than 7`.

1. Pour appliquer automatiquement un ordre de tri à la liste de produits générée dynamiquement, définissez **[!UICONTROL Automatic Sorting]**.

   ![Tri automatique](./assets/automatic-sorting-field.png){width="600" zoomable="yes"}

   Les options d’ordre de tri sont définies globalement et appliquées en fonction des conditions actuelles. Vous ne pouvez pas définir un ordre de tri différent pour le site web, le magasin ou le niveau d’affichage du magasin.

   | Option de tri | Description |
   |-----------| -----------|
   | [!UICONTROL Stock quantity] | Trier en fonction du stock, depuis le haut ou le bas : `Move low stock to top` ou `Move out of stock to bottom` |
   | [!UICONTROL Special price] | Trier en fonction du prix, du haut ou du bas : `Special price to top` ou `Special price to bottom` |
   | [!UICONTROL New Products] | Liste des produits les plus récents : `Newest products first` |
   | [!UICONTROL Color] | Trier par ordre alphabétique par couleur : `Sort by color` |
   | [!UICONTROL Product Names] | Triez par nom par ordre croissant ou décroissant : `Name A - Z` ou `Name Z -A`. |
   | [!UICONTROL SKU] | Triez par SKU par ordre croissant ou décroissant : `SKU: Ascending` ou `SKU: Descending`. |
   | [!UICONTROL Price] | Triez par prix par ordre croissant ou décroissant : `Price: High to low` ou `Price: Low to high` |

   {style="table-layout:auto"}

1. Cliquez ensuite sur **[!UICONTROL Save Category]**.

>[!NOTE]
>
>Lors de la configuration d’une règle de catégorie, les produits sont associés et affectés à la règle lorsque la catégorie est enregistrée. Si vous ajoutez un produit au catalogue et souhaitez l’inclure dans la règle, vous devez réenregistrer chaque catégorie définie pour correspondre aux produits par règle. Cela permet de s’assurer que le nouveau produit est inclus.

### Options de menu

- **[!UICONTROL Match products by rule]** - Détermine si la liste des produits de la catégorie est générée dynamiquement par une règle de catégorie. Options : `Yes` / `No`

- **[!UICONTROL Automatic Sorting]** - Applique automatiquement un ordre de tri à la liste des produits de la catégorie. Options : `None`, `Move low stock to top`, `Move low stock to bottom`, `Special price to top`, `Special price to bottom`, `Newest products first`, `Sort by color`, `Name: A - Z`, `Name: Z - A`, `SKU: Ascending`, `SKU: Descending` et `Price: High to Low` `Price: Low to High`

  >[!NOTE]
  >
  >Si vous disposez d&#39;un produit configurable avec des produits enfants, le stock de produits parents est calculé en fonction du total combiné des stocks de produits enfants. Prenons l’exemple d’un produit configurable _Chemise de fitness Proteus_ avec des produits enfants orange, rouge et jaune dont les stocks sont différents. Le stock de produits parents est calculé en fonction du stock total combiné de produits enfants orange, rouge et jaune. Avec l’option `Move low stock to top`, il calcule le stock de produits parents en combinant tous ses stocks de produits enfants vendables et les trie en conséquence.

- **[!UICONTROL Add Condition]** - Ajoute une autre condition à la règle.

- **[!UICONTROL Attribute]** - Détermine l’attribut utilisé comme base de la condition. Options :

  | Option | Description |
  | ------ | ----------- |
  | `Clone Category ID(s)` | Clone dynamiquement les produits, sans les trier ni les classer, à partir de plusieurs catégories en fonction de l’ID de catégorie. |
  | `Color` | Inclut des produits en fonction de la couleur. |
  | `Date Created (days ago)` | Inclut les produits en fonction du nombre de jours écoulés depuis leur ajout au catalogue. |
  | `Date Modified (days ago)` | Inclut les produits en fonction du nombre de jours écoulés depuis la dernière modification des produits. |
  | `Name` | Inclut des produits en fonction du nom du produit. |
  | `Price` | Inclut des produits basés sur le prix. Cet attribut ne s’applique pas aux produits configurables, car ils n’ont pas leur propre prix. |
  | `Quantity` | Inclut les produits en fonction de la quantité en stock. |
  | `SKU` | Inclut des produits basés sur un SKU. |

  {style="table-layout:auto"}

  >[!NOTE]
  >
  >La quantité d&#39;un produit configurable avec options enfants est calculée en combinant toutes les quantités de produits enfants vendables. Prenons l’exemple d’un produit configurable _Basic Fitness Tank_ avec des options de couleur violette, rouge et jaune et différentes quantités de chacune. Dans ce cas, la quantité du produit parent (réservoir de conditionnement physique de base) correspond à la quantité commercialisable combinée des produits enfants violets, rouges et jaunes.

- **[!UICONTROL Operator]** - Spécifie l’opérateur appliqué à la valeur d’attribut pour remplir la condition. Sauf si un opérateur est spécifié, `Equal` est utilisé par défaut. Options : `Equal`, `Not equal`, `Greater than`, `Greater than or equal to`, `Less than`, `Less than or equal to` et `Contains`

- **[!UICONTROL Value]** - Indique la valeur que l’attribut doit avoir pour remplir la condition.

- **[!UICONTROL Logic]** - La colonne Logique permet de définir plusieurs conditions et s’affiche uniquement lorsqu’une autre condition est ajoutée. Les opérateurs suivent les règles de priorité de MySQL [opérateurs booléens](https://dev.mysql.com/doc/refman/8.0/en/operator-precedence.html). Options : `AND` / `OR`
