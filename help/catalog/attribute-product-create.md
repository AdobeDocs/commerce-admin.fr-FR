---
title: Création et suppression d’attributs de produit
description: Découvrez comment créer et supprimer des attributs de produit, utilisés pour décrire les caractéristiques spécifiques des produits de votre catalogue.
exl-id: fd0e5d5b-a917-4e55-8ec2-7ebb040d3d06
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1166'
ht-degree: 0%

---

# Création et suppression d’attributs de produit

Vous pouvez créer des attributs lorsque vous travaillez sur un produit ou à partir de la page _[!UICONTROL Product Attributes]_. Les étapes suivantes montrent comment créer des attributs à partir du menu_[!UICONTROL Stores]_.

## Etape 1 : décrire les propriétés d&#39;attribut de base

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Cliquez sur **[!UICONTROL Add New Attribute]**.

   ![Nouvelles propriétés d’attribut](./assets/attribute-properties.png){width="600" zoomable="yes"}

1. Pour **[!UICONTROL Default Label]**, saisissez un libellé qui identifie l’attribut.

1. Pour déterminer le type de contrôle d’entrée utilisé pour la saisie de données, définissez **[!UICONTROL Catalog Input Type for Store Owner]** sur l’un des paramètres suivants :

   | Propriété | Description |
   |--- |--- |
   | `Text Field` | Champ de saisie d’une seule ligne pour le texte. |
   | `Text Area` | Champ de saisie multi-lignes permettant de saisir des paragraphes de texte, comme une description de produit. Vous pouvez utiliser l’éditeur WYSIWYG pour mettre en forme le texte avec des balises d’HTML ou saisir les balises directement dans le texte. |
   | `Text Editor` | Éditeur de texte entièrement fonctionnel à l’emplacement de l’attribut. |
   | Date | Affiche une valeur de date au [format recommandé](attributes-input-types.md#date-and-time-options) et [fuseau horaire](../getting-started/store-details.md#locale-options). Les valeurs de date peuvent être sélectionnées à partir d’une liste ou d’un calendrier ( ![Icône Calendrier](../assets/icon-calendar.png) ). <br/><br/>**_Remarque :_**Selon la configuration de votre système, les utilisateurs de_Admin _peuvent saisir des dates directement dans un champ ou sélectionner une date dans le calendrier ou la liste. Pour plus d&#39;informations sur la spécification des valeurs de date et d&#39;heure, voir [Options de date et d&#39;heure](attributes-input-types.md#date-and-time-options). |
   | `Yes/No` | Affiche une liste déroulante avec des options prédéfinies `Yes` et `No`. |
   | `Dropdown` | Affiche une liste déroulante de valeurs qui n’acceptent qu’une seule sélection. Le type d’entrée Liste déroulante est un composant clé de [produits configurables](product-create-configurable.md). |
   | `Multiple Select` | Affiche une liste déroulante de valeurs qui acceptent plusieurs sélections. |
   | `Price` | Ce type d’entrée est utilisé pour créer des champs de prix qui s’ajoutent aux attributs prédéfinis : Prix, Prix spécial, Prix de niveau et Coût. La devise utilisée est déterminée par votre configuration système. |
   | `Media Image` | Associe une image supplémentaire à un produit, tel qu’un logo de produit, des instructions de soin ou des ingrédients d’une étiquette alimentaire. Lorsque vous ajoutez un attribut d’image multimédia au jeu d’attributs d’un produit, il devient un type d’image supplémentaire, avec Base, Petit et Miniature. L’attribut image du média peut être exclu du [navigateur multimédia storefront](catalog-images-video.md#storefront-media-browser). |
   | `Fixed Product Tax` | Permet de définir des [taux FPT](../stores-purchase/fixed-product-tax.md) en fonction des exigences de vos paramètres régionaux. |
   | `Visual Swatch` | Affiche un échantillon représentant la couleur, la texture ou le motif d’un produit configurable. Un [échantillon visuel](swatches.md) peut être rempli avec une valeur de couleur hexadécimale ou afficher une image téléchargée qui représente la couleur, le matériau, la texture ou le motif de l’option. |
   | `Text Swatch` | Représentation textuelle d’une option de produit configurable fréquemment utilisée pour sa taille. [Les échantillons de texte](swatches.md#text-based-swatches) peuvent également inclure des valeurs de couleur hexadécimales. |
   | `Page Builder` | Espace de travail [Page Builder](../page-builder/introduction.md) entièrement fonctionnel à l’emplacement d’attribut qui permet d’ajouter facilement du contenu engageant à la page du produit. |

   {style="table-layout:auto"}

1. Si vous souhaitez avoir besoin d’une sélection d’options avant que le client puisse acheter le produit, définissez **[!UICONTROL Values Required]** sur `Yes`.

1. Pour les types d’entrée [!UICONTROL Dropdown] et [!UICONTROL Multiple Select], procédez comme suit :

   - Sous _[!UICONTROL Manage Options]_, cliquez sur **[!UICONTROL Add Option]**.

   - Saisissez la première valeur que vous souhaitez voir apparaître dans la liste.

     Vous pouvez saisir une valeur pour l’administrateur et une traduction de la valeur pour chaque vue de magasin. Si vous n’avez qu’une seule vue de magasin, vous pouvez saisir uniquement la valeur Admin ; elle est également utilisée pour le storefront.

   - Cliquez sur **[!UICONTROL Add Option]** et répétez l’étape précédente pour chaque option que vous souhaitez inclure dans la liste.

   - Sélectionnez **[!UICONTROL Is Default]** pour utiliser l’option comme valeur par défaut.

   ![Attribut de produit - gérer les options](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

## Étape 2 : description des propriétés avancées (si nécessaire)

1. Saisissez un **[!UICONTROL Attribute Code]** unique en minuscules, sans espaces.

   ![Attribut de produit - propriétés avancées](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

   Les options disponibles dépendent du paramètre _[!UICONTROL Catalog Input Type for Store Owner]_.

1. Définissez **[!UICONTROL Scope]** pour indiquer où, dans votre [hiérarchie de magasin](../getting-started/websites-stores-views.md), l’attribut peut être utilisé.

1. Si vous souhaitez empêcher toute entrée de valeur en double, définissez **[!UICONTROL Unique Value]** sur `Yes`.

1. Pour les types d’entrée qui sont des valeurs saisies, exécutez un test de validité de toutes les données saisies dans un champ de texte en définissant **[!UICONTROL Input Validation for Store Owner]** sur le type de données que le champ doit contenir.

   Ce champ n’est pas disponible pour les types d’entrée avec des valeurs sélectionnées. Le test peut valider l’un des éléments suivants :

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![Validation d’entrée](./assets/product-attribute-input-validation.png){width="400"}

1. Pour ajouter cet attribut à la [liste de produits](products-list.md), définissez les options suivantes sur `Yes`.

   - **Ajouter aux options de colonne** - Inclut l’attribut en tant que colonne dans la liste _[!UICONTROL Products]_.
   - **Utiliser dans les options de filtre** - Ajoute un contrôle de filtre à l’en-tête de colonne dans la liste _[!UICONTROL Products]_.

## Etape 3 : Saisir le libellé du champ

1. Dans le volet de navigation de gauche, choisissez **[!UICONTROL Manage Labels]**.

1. Saisissez un **[!UICONTROL Title]** à utiliser comme libellé pour le champ.

   Si votre boutique est disponible dans différentes langues, vous pouvez saisir un titre traduit pour chaque affichage.

   ![Attribut de produit - gérer les titres](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## Étape 4 : description des propriétés du storefront

1. Dans le volet de navigation de gauche, choisissez **[!UICONTROL Storefront Properties]**.

   ![ Attributs de produit - propriétés storefront](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

   Les options disponibles dépendent du paramètre _[!UICONTROL Catalog Input Type for Store Owner]_.

1. Si l’attribut doit être disponible pour la recherche, définissez **[!UICONTROL Use in Search]** sur `Yes`.

   - Définissez la valeur **[!UICONTROL Search Weight]** pour contrôler où l’élément apparaît dans les résultats de recherche : 1 (poids le plus faible) à 10 (poids le plus élevé).

   - Définissez le **[!UICONTROL Visible in Advanced Search]** selon vos besoins. En savoir plus dans [Recherche avancée](search.md#advanced-search).

1. Pour inclure l’attribut dans la comparaison de produits, définissez **[!UICONTROL Comparable on Storefront]** sur `Yes`.

1. Pour les champs de liste déroulante, de sélection multiple et de prix, procédez comme suit :

   - Pour utiliser l’attribut comme filtre dans la navigation par couches, définissez **[!UICONTROL Use in Layered Navigation]** sur `Yes`.

   - Pour utiliser l’attribut dans la navigation par couches sur les pages de résultats de recherche, définissez **[!UICONTROL Use in Search Results Layered Navigation]** sur `Yes`.

   - Pour **[!UICONTROL Position]**, saisissez un nombre pour indiquer la position relative de l’attribut dans le bloc de navigation superposé.

1. Pour utiliser l’attribut dans les règles de prix, définissez **[!UICONTROL Use for Promo Rule Conditions]** sur `Yes`.

1. Pour autoriser le formatage du texte avec HTML, définissez **[!UICONTROL Allow HTML Tags on Frontend]** sur `Yes`.

   Ce paramètre rend l’éditeur WYSIWYG disponible pour le champ.

1. Pour inclure l’attribut sur la page du produit, définissez **[!UICONTROL Visible on Catalog Pages on Storefront]** sur `Yes`.

1. Définissez les paramètres suivants si votre thème est pris en charge :

   - Pour inclure l’attribut dans les listes de produits, définissez **[!UICONTROL Used in Product Listing]** sur `Yes`.

   - Pour utiliser l’attribut comme paramètre de tri pour les listes de produits, définissez **[!UICONTROL Used for Sorting in Product Listing]** sur `Yes`.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Attribute]**.

## Étape 5 : Attribution de l’attribut créé au jeu d’attributs

Pour qu’un attribut soit visible sur la page de création du produit, ajoutez-le à un jeu d’attributs spécifique.

1. Après avoir effectué les étapes précédentes, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Sélectionnez le jeu d’attributs dont vous avez besoin dans la liste et ouvrez-le en mode d’édition.

1. Faites glisser l’attribut créé de la liste **[!UICONTROL Unassigned Attributes]** vers le dossier approprié dans la colonne **Groups**.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

## Attributs des produits configurables

Tout attribut utilisé comme liste déroulante d’options pour un [produit configurable](product-create-configurable.md) doit avoir les propriétés suivantes :

| Propriété | Valeur |
|----------|------ |
| Type d’entrée de catalogue pour le propriétaire du magasin | Liste déroulante |
| Portée | Global |

{style="table-layout:auto"}

## Suppression d’un attribut

Lorsqu’un attribut est supprimé, il est supprimé de tous les produits et jeux d’attributs associés. Les attributs système font partie des fonctionnalités de base de votre magasin et ne peuvent pas être supprimés.

Avant de supprimer un attribut, assurez-vous qu’il n’est actuellement utilisé par aucun produit de votre catalogue. Pour déterminer facilement si un attribut est utilisé, utilisez l’outil [Export](../systems/data-export.md) pour vérifier la liste des attributs d’entité de produit. Si l’attribut n’est pas inclus dans la liste, il n’est utilisé par aucun produit du catalogue.

**_Pour supprimer un attribut :_**

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Recherchez l’attribut dans la liste et ouvrez-le en mode d’édition.

1. Cliquez sur **[!UICONTROL Delete Attribute]**.

   ![Supprimer l’attribut](./assets/attribute-delete.png){width="600" zoomable="yes"}

1. Lorsque vous êtes invité à confirmer l’opération, cliquez sur **[!UICONTROL OK]**.
