---
title: Produit virtuel
description: Découvrez comment créer un produit virtuel qui représente un élément non tangible, tel qu’un abonnement, un service, une garantie ou un abonnement.
exl-id: 8788ba04-e911-429e-9e48-ce589f0c9fa1
feature: Catalog Management, Products
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# Produit virtuel

Les produits virtuels, ou biens numériques, représentent des éléments non tangibles tels que des adhésions, des services, des garanties ou des abonnements et des téléchargements numériques de livres, de musique, de vidéos ou d’autres produits. Les produits virtuels peuvent être vendus individuellement ou inclus dans les types de produits [Produit groupé](product-create-grouped.md), [Produit configurable](product-create-configurable.md) ou [Produit groupé](product-create-bundle.md).

Outre l’absence du champ _[!UICONTROL Weight]_, le processus de création d’un produit virtuel et d’un produit simple est le même. Les instructions suivantes illustrent le processus de création d’un produit virtuel à l’aide d’un [modèle de produit](attribute-sets.md), de champs obligatoires et de paramètres de base. Lorsque vous avez terminé les principes de base, vous pouvez définir les autres paramètres du produit selon vos besoins.

>[!NOTE]
>
>PayPal a mis fin à la prise en charge de la vente de produits numériques par PayPal Express Checkout. Il vous recommande d&#39;utiliser [PayPal Payments Standard](../stores-purchase/paypal-payments-standard.md) ou toute autre passerelle de paiement PayPal pour traiter toute commande qui inclut des produits virtuels.

![Produit virtuel](./assets/product-virtual-membership.png){width="700" zoomable="yes"}

## Étape 1 : sélection du type de produit

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Dans le menu _[!UICONTROL Add Product]_( ![Flèche du menu](../assets/icon-menu-down-arrow-red.png){width="25"} ) dans le coin supérieur droit, choisissez **[!UICONTROL Virtual Product]**.

   ![Ajouter un produit virtuel](./assets/product-add-virtual.png){width="700" zoomable="yes"}

## Étape 2 : sélection du jeu d’attributs

Pour choisir le [jeu d’attributs](attribute-sets.md) utilisé comme modèle pour le produit, effectuez l’une des opérations suivantes :

- Cliquez dans le champ **[!UICONTROL Attribute Set]** et saisissez tout ou partie du nom du jeu d’attributs.

- Dans la liste qui s’affiche, choisissez le jeu d’attributs à utiliser.

Le formulaire est mis à jour pour refléter la modification.

![Choisir un jeu d’attributs](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Étape 3 : effectuez les paramètres requis

1. Saisissez le **[!UICONTROL Product Name]**.

1. Acceptez le **[!UICONTROL SKU]** par défaut basé sur le nom du produit ou saisissez-en un autre.

1. Saisissez le **[!UICONTROL Price]** du produit.

1. Comme le produit n’est pas encore prêt à être publié, définissez **[!UICONTROL Enable Product]** sur `No`.

1. Cliquez sur **[!UICONTROL Save]** et continuez.

   Lorsque le produit est enregistré, le sélecteur [Vue Boutique](introduction.md#product-scope) s’affiche dans le coin supérieur gauche.

1. Choisissez le **[!UICONTROL Store View]** où le produit doit être disponible.

   ![Choisir la vue Boutique](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Étape 4 : définition des paramètres de base

1. Définissez **[!UICONTROL Tax Class]** sur l’une des options suivantes :

   - `None`
   - `Taxable Goods`

1. Saisissez le **[!UICONTROL Quantity]** du produit en stock et procédez comme suit :

   - Acceptez le paramètre de **[!UICONTROL Stock Status]** par défaut de `In Stock`.

     Comme un produit virtuel n’est pas livré, le champ **[!UICONTROL Weight]** n’est pas utilisé.

   - Acceptez le paramètre de **[!UICONTROL Visibility]** par défaut de `Catalog, Search`.

   >[!NOTE]
   >
   >Si vous activez [Inventory management](../inventory-management/introduction.md), les commerçants à source unique définissent la quantité dans cette section. Les commerçants multi-sources ajoutent des sources et des quantités dans la section Sources . Voir la section suivante _Attribuer des sources et des quantités (Inventory management)_.

1. Pour attribuer des **[!UICONTROL Categories]** au produit, cliquez sur la zone de **[!UICONTROL Select…]** et effectuez l’une des opérations suivantes :

   **Choisissez une catégorie existante** :

   - Commencez à taper dans la zone jusqu’à ce que vous trouviez une correspondance.

   - Cochez la case de la catégorie à affecter.

   **Créer une catégorie** :

   - Cliquez sur **[!UICONTROL New Category]**.

   - Saisissez le **[!UICONTROL Category Name]** et choisissez le **[!UICONTROL Parent Category]**, qui détermine sa position dans la structure du menu.

   - Cliquez sur **[!UICONTROL Create Category]**.

   D’autres attributs individuels peuvent décrire le produit. La sélection varie selon le jeu d’attributs et vous pouvez les terminer ultérieurement.

### Affecter des sources et des quantités ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## Étape 5 : compléter les informations sur le produit

Renseignez les informations des sections suivantes selon vos besoins :

- [Contenu](product-content.md)
- [Images et vidéos](product-images-and-video.md)
- [Optimisation du moteur de recherche](product-search-engine-optimization.md)
- [Produits associés, ventes incitatives et ventes croisées](related-products-up-sells-cross-sells.md)
- [Options personnalisables](settings-advanced-custom-options.md)
- [Produits dans les sites web](settings-basic-websites.md)
- [Conception](settings-advanced-design.md)
- [Options de cadeau](product-gift-options.md)

>[!NOTE]
>
>L’option _[!UICONTROL Is this downloadable product?]_&#x200B;est désactivée par défaut. L’activation de cette fonctionnalité pour un produit virtuel rend le produit [téléchargeable](product-create-downloadable.md#downloadable-product).

## Étape 6 : publier le produit

1. Si vous êtes prêt à publier le produit dans le catalogue, définissez **[!UICONTROL Enable Product]** sur `Yes`.

1. Effectuez l’une des opérations suivantes :

   - **Méthode 1 :** Enregistrer et prévisualiser

      - Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]**.

      - Pour afficher le produit dans votre boutique, choisissez **[!UICONTROL Customer View]** dans le menu _Admin_ ( ![Flèche de menu](../assets/icon-menu-down-arrow-black.png) ).

     Le magasin s’ouvre dans un nouvel onglet du navigateur.

     ![Affichage client](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Méthode 2 :** Enregistrer et fermer

     Dans le menu _[!UICONTROL Save]_(![Flèche de menu](../assets/icon-menu-down-arrow-red.png){width="25"} ), choisissez **[!UICONTROL Save & Close]**.

## Éléments à retenir

- Les produits virtuels sont utilisés pour des produits non tangibles tels que des services, des abonnements et des garanties.

- Les produits virtuels sont très similaires aux produits simples, mais sans poids.

- Les options d’expédition n’apparaissent pas lors du passage en caisse, sauf s’il existe un produit tangible dans le panier.

<!-- Last updated from includes: 2023-05-19 17:14:58 -->
