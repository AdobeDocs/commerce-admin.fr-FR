---
title: Paramètres du produit - [!UICONTROL Customizable Options]
description: Pour un produit, les paramètres [!UICONTROL Customizable Options] vous permettent d’offrir une sélection d’options avec des types de texte, de sélection et de saisie de date.
exl-id: 7d23c5c5-2b2a-4f2a-b843-9c27b851be5f
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 0%

---

# Paramètres du produit - [!UICONTROL Customizable Options]

L’ajout d’options personnalisables à un produit est un moyen facile d’offrir une sélection d’options avec des types de texte, de sélection et de saisie de date. Les options personnalisables sont une bonne solution si vos besoins en inventaire sont simples. Cependant, puisqu’elles sont basées sur des variations d’un seul SKU, elles ne peuvent pas être utilisées pour gérer le stock ou comme base des conditions des règles de prix. Si vous disposez de plusieurs produits avec les mêmes options, vous pouvez configurer un produit et importer les options dans les autres produits.

Lorsqu’un client achète un produit avec une option personnalisable, une description de chaque option sélectionnée s’affiche sous la description du produit, et tout balisage (ou Markdown) associé est automatiquement appliqué au prix de l’article.

![Détails du produit avec option personnalisable](./assets/storefront-customizable-option-product-detail.png){width="700" zoomable="yes"}

Si une règle de prix de panier est déclenchée par l’achat, le calcul initial s’applique d’abord au prix du produit et ensuite au prix de l’article avec tout ajustement pour les options personnalisables applicables. Dans l’exemple suivant, le client achète un sac à dos pour 74,00 $, plus une option personnalisable pour un monogramme. Une annotation de 14,80 $ est appliquée au prix de base du produit, et le prix ajusté est indiqué comme étant de 88,80 $. Dans ce cas, l’achat du sac dupliqué déclenche une règle de prix du panier basée sur le SKU du produit et applique une remise à l’achat, ainsi que la livraison gratuite. Bien que la règle de prix du panier ne soit pas déclenchée par l’option personnalisable, elle applique la remise au contenu du panier, qui inclut les balises de l’option personnalisable.

![Panier avec option et règle de prix personnalisables](./assets/storefront-customizable-option-cart-price-rule.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Une remise de règle de prix de catalogue n’est pas appliquée aux options personnalisables à prix fixe.

## Création d’options personnalisables

1. Ouvrez le produit en mode d’édition.

1. Faites défiler l’écran vers le bas et développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur _[!UICONTROL Customizable Options]_.

1. Cliquez sur **[!UICONTROL Add Option]**.

   ![Options personnalisables](./assets/product-customizable-options.png){width="600" zoomable="yes"}

1. Renseignez les nouveaux paramètres d’option :

   - Pour **[!UICONTROL Option Title]**, saisissez un nom pour l’option.

   - Définissez le **[!UICONTROL Option Type]** pour le type d’entrée de données.

   - Si cette option n’est pas requise pour acheter le produit, désélectionnez la case à cocher **[!UICONTROL Required]** .

1. Renseignez les champs en fonction du type de saisie des données :

   - Pour **[!UICONTROL Title]**, saisissez un nom pour cette option.

   - (Facultatif) Pour **[!UICONTROL Price]**, saisissez les balises ou les balises du prix de base du produit qui s’appliquent à cette option.

   - Définissez **[!UICONTROL Price Type]** sur l’une des options suivantes :

      - `Fixed` - Le prix de la variation diffère du prix du produit de base par un montant monétaire fixe, tel que 1 $.
      - `Percentage` - Le prix de la variation diffère du prix du produit de base d’un pourcentage, comme 10 %.

   - (Facultatif) Saisissez un **[!UICONTROL SKU]** pour l’option. L’option SKU est un suffixe ajouté au SKU du produit.

   - Si _[!UICONTROL Option Type]_&#x200B;est `File`, définissez les paramètres du fichier. Pour **[!UICONTROL Compatible File Extensions]**, saisissez les extensions valides sous forme de valeurs séparées par des virgules (telles que `png, jpg, gif`). Pour **[!UICONTROL Maximum Image Size]**, saisissez la taille maximale de l’image en pixels. S’il s’agit d’une entrée de texte, saisissez la valeur maximale pour **[!UICONTROL Maximum Characters]**.

   ![Ajouter des valeurs pour l’option de personnalisation](./assets/product-customizable-options-add-values.png){width="600" zoomable="yes"}

1. (Facultatif) Si vous souhaitez ajouter une autre option personnalisable, cliquez sur **[!UICONTROL Add Option]**.

   - Définissez les paramètres comme auparavant.

   - Pour modifier l’ordre des options, cliquez sur l’icône _[!UICONTROL Order]_![Icône Ordre de tri](../assets/icon-sort-order.png) et faites glisser l’option vers un nouvel emplacement dans la liste.

   Répétez cette étape pour chaque option à ajouter.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

## Importation d’options personnalisables

1. Dans la section _Options personnalisables_, cliquez sur **[!UICONTROL Import Options]**.


1. Tous les produits avec des options personnalisables apparaissent dans la grille.

1. Dans la liste, cochez la case du produit avec les options que vous souhaitez importer.

1. Cliquez sur **[!UICONTROL Import]**.

1. Une fois l’opération terminée, vous pouvez continuer à ajouter d’autres options personnalisées ou cliquer sur **[!UICONTROL Save and Close]**.

## Types d’entrée

| Type | Description |
|---------------------|---------------|
| [!UICONTROL Text] | Une ligne de saisie ou une zone de texte dans laquelle le client peut saisir les informations requises. Options : <br />**[!UICONTROL Field]**- Champ de saisie d’une seule ligne pour le texte.<br />**[!UICONTROL Area]** - Champ de saisie multi-lignes. Ce type ne prend pas en charge la mise en forme avancée telle que l’HTML. Utilisez les caractères max. pour limiter la longueur du texte qui peut être saisi et assurer une représentation correcte du texte saisi dans l’administrateur. |
| [!UICONTROL File] | Permet au client de télécharger un fichier. |
| [!UICONTROL Select] | Permet au client de sélectionner une ou plusieurs options, selon le type d&#39;entrée utilisé. Options : <br />**[!UICONTROL Drop-down]**- Liste déroulante d’options qui n’autorise qu’une sélection.<br />**[!UICONTROL Radio Buttons]** - Ensemble d’options qui ne permet qu’une sélection.<br />**[!UICONTROL Checkbox]**- Une case à cocher est une variante d’une option oui/non. Si le produit comporte plusieurs cases à cocher, plusieurs sélections peuvent être effectuées.<br />**[!UICONTROL Multiple Select]** - Zone de liste déroulante d’options qui accepte plusieurs sélections. Pour sélectionner plusieurs options, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et cliquez sur chaque option. |
| [!UICONTROL Date] | Permet au client de saisir une date ou une heure ou de choisir la valeur dans un calendrier. Options : <br />**[!UICONTROL Date]**- Champ de saisie d’une valeur de date. La date peut être saisie directement dans le champ ou sélectionnée dans une liste ou un calendrier. La méthode et le format d’entrée sont déterminés par la configuration [des options de date et d’heure](attributes-input-types.md#date-and-time-options).<br />**[!UICONTROL Date & Time]** - Champ de saisie pour une valeur de date et d’heure.<br />**[!UICONTROL Time]**- Champ de saisie pour une valeur temporelle. |

{style="table-layout:auto"}
