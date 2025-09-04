---
title: Produit simple
description: Découvrez comment créer un produit simple qui peut être vendu individuellement ou dans le cadre d’un produit groupé, configurable ou groupé.
exl-id: 3ac9b28d-3929-4fd6-97ca-145ea6d6897c
feature: Catalog Management, Products
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Produit simple

L’une des clés pour tirer parti de la puissance des types de produits est d’apprendre à utiliser un produit simple et autonome. Un produit simple peut être vendu individuellement ou dans le cadre d’un produit groupé, configurable ou groupé. Un produit simple avec des options personnalisées est parfois appelé _produit composite_.

Les instructions suivantes illustrent le processus de création d’un produit simple à l’aide d’un [modèle de produit](attribute-sets.md), de champs obligatoires et de paramètres de base. Chaque champ obligatoire est signalé par un astérisque rouge (`*`). Lorsque vous avez terminé les principes de base, vous pouvez définir les autres paramètres du produit selon vos besoins.

![Produit simple](./assets/product-simple.png){width="700" zoomable="yes"}

## Étape 1 : sélection du type de produit

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Dans le menu _[!UICONTROL Add Product]_( ![Flèche du menu](../assets/icon-menu-down-arrow-red.png){width="25"} ) en haut à droite, choisissez **[!UICONTROL Simple Product]**.

   ![Ajouter un produit simple](./assets/product-add-simple.png){width="700" zoomable="yes"}

## Étape 2 : sélection du jeu d’attributs

Pour choisir le [jeu d’attributs](attribute-sets.md) utilisé comme modèle pour le produit :

- Cliquez dans le champ **[!UICONTROL Attribute Set]** et saisissez le nom complet ou partiel du jeu d’attributs.

- Dans la liste qui s’affiche, choisissez le jeu d’attributs à utiliser.

Le formulaire est mis à jour pour refléter la modification.

![Choisir un jeu d’attributs](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Étape 3 : effectuez les paramètres requis

1. Saisissez le **[!UICONTROL Product Name]**.

1. Acceptez le **[!UICONTROL SKU]** par défaut basé sur le nom du produit ou saisissez-en un autre.

1. Saisissez le **[!UICONTROL Price]** du produit.

1. Comme le produit n’est pas encore prêt à être publié, définissez l’option **[!UICONTROL Enable Product]** sur `No`.

1. cliquez sur **[!UICONTROL Save]** et continuez.

   Lorsque le produit est enregistré, le sélecteur [Vue Boutique](introduction.md#product-scope) s’affiche dans le coin supérieur gauche.

1. Choisissez le **[!UICONTROL Store View]** où le produit doit être disponible.

   ![Choisir la vue du magasin](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Étape 4 : définition des paramètres de base

1. Définissez **[!UICONTROL Tax Class]** sur l’une des options suivantes :

   - `None`
   - `Taxable Goods`
   - `Refund Adjustments`
   - `Gift Options`
   - `Order Gift Wrapping`
   - `Item Gift Wrapping`
   - `Printed Gift Card`
   - `Reward Points`
   - `VAT Reduced`
   - `VAT Standard`

1. Saisissez le **[!UICONTROL Quantity]** du produit en stock.

   Par défaut, **[!UICONTROL Stock Status]** est défini sur `In Stock`.

   >[!NOTE]
   >
   >Si vous activez [Inventory management](../inventory-management/introduction.md), les commerçants Single Source définissent la quantité dans cette section. Les marchands Multi Source ajoutent des sources et des quantités dans la section Sources . Voir la section suivante _Attribuer des sources et des quantités (Inventory management)_.

1. Saisissez le **[!UICONTROL Weight]** du produit.

1. Acceptez le paramètre de **[!UICONTROL Visibility]** par défaut de `Catalog, Search`.

1. Pour attribuer des _[!UICONTROL Categories]_au produit, cliquez sur la zone de **[!UICONTROL Select…]**et effectuez l’une des opérations suivantes :

   **Choisissez une catégorie existante** :

   - Commencez à taper dans la zone jusqu’à ce que vous trouviez une correspondance.

   - Cochez la case de chaque catégorie à affecter.

   **Créer une catégorie** :

   - Cliquez sur **[!UICONTROL New Category]**.

   - Saisissez le **[!UICONTROL Category Name]** et choisissez le **[!UICONTROL Parent Category]**, qui détermine sa position dans la structure du menu.

   - Cliquez sur **[!UICONTROL Create Category]**.

1. Pour mettre le produit en avant dans la liste des [nouveaux produits](../content-design/widget-new-products-list.md), cochez la case **[!UICONTROL Set Product as New]**.

1. Choisissez le **[!UICONTROL Country of Manufacture]**.

D’autres attributs individuels peuvent décrire le produit. La sélection varie en fonction du jeu d’attributs. Vous pouvez les effectuer ultérieurement.

### Affecter des sources et des quantités ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## Étape 5 : compléter les informations sur le produit

Faites défiler vers le bas et renseignez les informations des sections suivantes selon vos besoins :

- [Contenu](product-content.md)
- [Images et vidéos](product-images-and-video.md)
- [Produits associés, ventes incitatives et ventes croisées](related-products-up-sells-cross-sells.md)
- [Optimisation du moteur de recherche](product-search-engine-optimization.md)
- [Options personnalisables](settings-advanced-custom-options.md)
- [Produits dans les sites web](settings-basic-websites.md)
- [Conception](settings-advanced-design.md)
- [Options de cadeau](product-gift-options.md)

## Étape 6 : publier le produit

1. Si vous êtes prêt à publier le produit dans le catalogue, définissez le commutateur de **[!UICONTROL Enable Product]** sur `Yes`.

1. Effectuez l’une des opérations suivantes :

   - **Méthode 1 :** Enregistrer et prévisualiser

      - Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]**.

      - Pour afficher le produit dans votre boutique, choisissez **[!UICONTROL Customer View]** dans le menu _Admin_ (![Flèche de menu](../assets/icon-menu-down-arrow-black.png)).

     Le magasin s’ouvre dans un nouvel onglet du navigateur.

     ![Affichage client](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Méthode 2 :** Enregistrer et fermer

     Dans le menu _[!UICONTROL Save]_( ![flèche du menu](../assets/icon-menu-down-arrow-red.png){width="25"} ), choisissez **[!UICONTROL Save & Close]**.

## Éléments à retenir

- Les produits simples peuvent être inclus dans des types de produits configurables, groupés et groupés.

- Une configuration de produit simple remplace les configurations de produit configurables pour un produit spécifique.

- Un produit simple peut avoir des options personnalisées avec différents types d’entrée, ce qui permet de vendre de nombreuses variations de produit à partir d’un seul SKU.

<!-- Last updated from includes: 2023-05-19 17:14:58 -->
