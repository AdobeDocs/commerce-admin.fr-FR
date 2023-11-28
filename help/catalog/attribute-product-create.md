---
title: Création et suppression d’attributs de produit
description: Découvrez comment créer et supprimer des attributs de produit, utilisés pour décrire les caractéristiques spécifiques des produits de votre catalogue.
exl-id: fd0e5d5b-a917-4e55-8ec2-7ebb040d3d06
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1159'
ht-degree: 0%

---

# Création et suppression d’attributs de produit

Vous pouvez créer des attributs lorsque vous travaillez sur un produit ou à partir de la fonction _[!UICONTROL Product Attributes]_page. Les étapes suivantes montrent comment créer des attributs à partir du_[!UICONTROL Stores]_ .

## Etape 1 : décrire les propriétés d&#39;attribut de base

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Cliquez sur **[!UICONTROL Add New Attribute]**.

   ![Nouvelles propriétés d’attribut](./assets/attribute-properties.png){width="600" zoomable="yes"}

1. Pour **[!UICONTROL Default Label]**, saisissez un libellé qui identifie l’attribut.

1. Pour déterminer le type de contrôle d’entrée utilisé pour la saisie de données, définissez **[!UICONTROL Catalog Input Type for Store Owner]** à l’une des options suivantes :

   | Propriété | Description |
   |--- |--- |
   | `Text Field` | Champ de saisie d’une seule ligne pour le texte. |
   | `Text Area` | Champ de saisie multi-lignes permettant de saisir des paragraphes de texte, comme une description de produit. Vous pouvez utiliser l’éditeur WYSIWYG pour mettre en forme le texte avec des balises de HTML ou saisir les balises directement dans le texte. |
   | `Text Editor` | Éditeur de texte entièrement fonctionnel à l’emplacement de l’attribut. |
   | Date | Affiche une valeur de date dans la variable [format préféré](attributes-input-types.md#date-and-time-options) et [fuseau horaire](../getting-started/store-details.md#locale-options). Les valeurs de date peuvent être sélectionnées à partir d’une liste ou d’un calendrier ( ![Icône Calendrier](../assets/icon-calendar.png) ). <br/><br/>**_Remarque :_**Selon la configuration de votre système,_Administration _les utilisateurs peuvent saisir des dates directement dans un champ ou sélectionner une date dans le calendrier ou la liste. Pour plus d’informations sur la spécification des valeurs de date et d’heure, voir [Options de date et d’heure](attributes-input-types.md#date-and-time-options). |
   | `Yes/No` | Affiche une liste déroulante avec des options prédéfinies de `Yes` et `No`. |
   | `Dropdown` | Affiche une liste déroulante de valeurs qui n’acceptent qu’une seule sélection. Le type d’entrée Liste déroulante est un composant clé de [produits configurables](product-create-configurable.md). |
   | `Multiple Select` | Affiche une liste déroulante de valeurs qui acceptent plusieurs sélections. |
   | `Price` | Ce type d’entrée est utilisé pour créer des champs de prix qui s’ajoutent aux attributs prédéfinis : Prix, Prix spécial, Prix de niveau et Coût. La devise utilisée est déterminée par votre configuration système. |
   | `Media Image` | Associe une image supplémentaire à un produit, tel qu’un logo de produit, des instructions de soin ou des ingrédients d’une étiquette alimentaire. Lorsque vous ajoutez un attribut d’image multimédia au jeu d’attributs d’un produit, il devient un type d’image supplémentaire, avec Base, Petit et Miniature. L’attribut image du média peut être exclu de la variable [navigateur multimédia storefront](catalog-images-video.md#storefront-media-browser). |
   | `Fixed Product Tax` | Permet de définir [Taux FPT](../stores-purchase/fixed-product-tax.md) selon les exigences de vos paramètres régionaux. |
   | `Visual Swatch` | Affiche un échantillon représentant la couleur, la texture ou le motif d’un produit configurable. A [échantillon visuel](swatches.md) peut être rempli avec une valeur hexadécimale ou afficher une image téléchargée qui représente la couleur, le matériau, la texture ou le motif de l’option. |
   | `Text Swatch` | Représentation textuelle d’une option de produit configurable fréquemment utilisée pour sa taille. [Esquisses de texte](swatches.md#text-based-swatches) peut également inclure des valeurs de couleur hexadécimales. |
   | `Page Builder` | Fonctionnement complet [Page Builder](../page-builder/introduction.md) workspace à l’emplacement d’attribut qui facilite l’ajout de contenu engageant à la page de produit. |

   {style="table-layout:auto"}

1. Si vous souhaitez qu’une option soit sélectionnée avant que le client puisse acheter le produit, définissez **[!UICONTROL Values Required]** to `Yes`.

1. Pour [!UICONTROL Dropdown] et [!UICONTROL Multiple Select] types d’entrée, procédez comme suit :

   - Sous _[!UICONTROL Manage Options]_, cliquez sur **[!UICONTROL Add Option]**.

   - Saisissez la première valeur que vous souhaitez voir apparaître dans la liste.

     Vous pouvez saisir une valeur pour l’administrateur et une traduction de la valeur pour chaque vue de magasin. Si vous n’avez qu’une seule vue de magasin, vous pouvez saisir uniquement la valeur Admin ; elle est également utilisée pour le storefront.

   - Cliquez sur **[!UICONTROL Add Option]** et répétez l’étape précédente pour chaque option à inclure dans la liste.

   - Sélectionner **[!UICONTROL Is Default]** pour utiliser l’option comme valeur par défaut.

   ![Attribut de produit - options de gestion](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

## Étape 2 : description des propriétés avancées (si nécessaire)

1. Saisissez une variable **[!UICONTROL Attribute Code]** en minuscules, sans espaces.

   ![Attribut de produit - propriétés avancées](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

   Les options disponibles dépendent du _[!UICONTROL Catalog Input Type for Store Owner]_.

1. Définir **[!UICONTROL Scope]** pour indiquer où dans votre [hiérarchie des magasins](../getting-started/websites-stores-views.md) que l’attribut peut être utilisé.

1. Si vous souhaitez empêcher toute saisie de valeur en double, définissez **[!UICONTROL Unique Value]** to `Yes`.

1. Pour les types d’entrée qui sont des valeurs saisies, effectuez un test de validité des données saisies dans un champ de texte en définissant **[!UICONTROL Input Validation for Store Owner]** du type de données que le champ doit contenir.

   Ce champ n’est pas disponible pour les types d’entrée avec des valeurs sélectionnées. Le test peut valider l’un des éléments suivants :

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![Validation d’entrée](./assets/product-attribute-input-validation.png){width="400"}

1. Pour ajouter cet attribut à la variable [Liste de produits](products-list.md), définissez les options suivantes sur `Yes`.

   - **Ajouter aux options de colonne** - Inclut l’attribut sous forme de colonne dans la variable _[!UICONTROL Products]_liste.
   - **Utilisation dans les options de filtre** : ajoute un contrôle de filtre à l’en-tête de colonne dans la variable _[!UICONTROL Products]_liste.

## Etape 3 : Saisir le libellé du champ

1. Dans le volet de navigation de gauche, choisissez **[!UICONTROL Manage Labels]**.

1. Saisissez un **[!UICONTROL Title]** à utiliser comme libellé pour le champ.

   Si votre boutique est disponible dans différentes langues, vous pouvez saisir un titre traduit pour chaque affichage.

   ![Attribut de produit - Gestion des titres](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## Étape 4 : description des propriétés du storefront

1. Dans le volet de navigation de gauche, choisissez **[!UICONTROL Storefront Properties]**.

   ![Attributs de produit - propriétés storefront](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

   Les options disponibles dépendent du _[!UICONTROL Catalog Input Type for Store Owner]_.

1. Si l’attribut doit être disponible pour la recherche, définissez **[!UICONTROL Use in Search]** to `Yes`.

   - Définissez la variable **[!UICONTROL Search Weight]** pour contrôler où l’élément apparaît dans les résultats de recherche : 1 (poids le plus faible) à 10 (poids le plus élevé).

   - Définissez la variable **[!UICONTROL Visible in Advanced Search]** selon les besoins. En savoir plus dans [Recherche avancée](search.md#advanced-search).

1. Pour inclure l’attribut dans la comparaison de produits, définissez **[!UICONTROL Comparable on Storefront]** to `Yes`.

1. Pour les champs de liste déroulante, de sélection multiple et de prix, procédez comme suit :

   - Pour utiliser l’attribut comme filtre dans la navigation par couches, définissez **[!UICONTROL Use in Layered Navigation]** to `Yes`.

   - Pour utiliser l’attribut dans la navigation par couches sur les pages de résultats de recherche, définissez **[!UICONTROL Use in Search Results Layered Navigation]** to `Yes`.

   - Pour **[!UICONTROL Position]**, saisissez un nombre pour indiquer la position relative de l’attribut dans le bloc de navigation superposé.

1. Pour utiliser l’attribut dans les règles de prix, définissez **[!UICONTROL Use for Promo Rule Conditions]** to `Yes`.

1. Pour que le texte puisse être formaté avec le HTML, définissez **[!UICONTROL Allow HTML Tags on Frontend]** to `Yes`.

   Ce paramètre rend l’éditeur WYSIWYG disponible pour le champ.

1. Pour inclure l’attribut dans la page du produit, définissez **[!UICONTROL Visible on Catalog Pages on Storefront]** to `Yes`.

1. Définissez les paramètres suivants si votre thème est pris en charge :

   - Pour inclure l’attribut dans les listes de produits, définissez **[!UICONTROL Used in Product Listing]** to `Yes`.

   - Pour utiliser l’attribut comme paramètre de tri pour les listes de produits, définissez **[!UICONTROL Used for Sorting in Product Listing]** to `Yes`.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Attribute]**.

## Étape 5 : Attribution de l’attribut créé au jeu d’attributs

Pour qu’un attribut soit visible sur la page de création du produit, ajoutez-le à un jeu d’attributs spécifique.

1. Une fois les étapes précédentes terminées, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Sélectionnez le jeu d’attributs dont vous avez besoin dans la liste et ouvrez-le en mode d’édition.

1. Faites glisser l’attribut créé à partir du **[!UICONTROL Unassigned Attributes]** vers le dossier approprié dans la **Groupes** colonne .

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

## Attributs des produits configurables

Tout attribut utilisé comme liste déroulante d’options pour un [produit configurable](product-create-configurable.md) doivent posséder les propriétés suivantes :

| Propriété | Valeur |
|----------|------ |
| Type d’entrée de catalogue pour le propriétaire du magasin | Liste déroulante |
| Portée | Global |

{style="table-layout:auto"}

## Suppression d’un attribut

Lorsqu’un attribut est supprimé, il est supprimé de tous les produits et jeux d’attributs associés. Les attributs système font partie des fonctionnalités de base de votre magasin et ne peuvent pas être supprimés.

Avant de supprimer un attribut, assurez-vous qu’il n’est actuellement utilisé par aucun produit de votre catalogue. Pour déterminer facilement si un attribut est utilisé, utilisez la variable [Exporter](../systems/data-export.md) pour vérifier la liste des attributs d’entité de produit. Si l’attribut n’est pas inclus dans la liste, il n’est utilisé par aucun produit du catalogue.

**_Pour supprimer un attribut :_**

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Recherchez l’attribut dans la liste et ouvrez-le en mode d’édition.

1. Cliquez sur **[!UICONTROL Delete Attribute]**.

   ![Supprimer l’attribut](./assets/attribute-delete.png){width="600" zoomable="yes"}

1. Lorsque vous y êtes invité, cliquez sur **[!UICONTROL OK]**.
