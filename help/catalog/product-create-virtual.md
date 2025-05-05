---
title: Produit virtuel
description: Découvrez comment créer un produit virtuel qui représente un article non tangible, tel qu’un abonnement, un service, une garantie ou un abonnement.
exl-id: 8788ba04-e911-429e-9e48-ce589f0c9fa1
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# Produit virtuel

Les produits virtuels, ou les biens numériques, représentent des éléments non tangibles tels que des adhésions, des services, des garanties ou des abonnements et des téléchargements numériques de livres, de musique, de vidéos ou d’autres produits. Les produits virtuels peuvent être vendus individuellement ou inclus dans les types de produits [Grouped Product](product-create-grouped.md), [Configurable Product](product-create-configurable.md) ou [Bundle Product](product-create-bundle.md).

Outre l’absence du champ _[!UICONTROL Weight]_, le processus de création d’un produit virtuel et d’un produit simple est le même. Les instructions suivantes montrent le processus de création d’un produit virtuel à l’aide d’un [modèle de produit](attribute-sets.md), des champs obligatoires et des paramètres de base. Lorsque vous avez terminé les étapes de base, vous pouvez définir les autres paramètres du produit selon vos besoins.

>[!NOTE]
>
>PayPal a abandonné la prise en charge de la vente de produits numériques via PayPal Express Checkout. Ils vous recommandent d’utiliser [PayPal payment Standard](../stores-purchase/paypal-payments-standard.md) ou toute autre passerelle de paiement PayPal pour traiter toute commande qui inclut des produits virtuels.

![Produit virtuel](./assets/product-virtual-membership.png){width="700" zoomable="yes"}

## Etape 1 : Sélection du type de produit

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Dans le menu _[!UICONTROL Add Product]_( ![Flèche de menu](../assets/icon-menu-down-arrow-red.png){width="25"} ) dans le coin supérieur droit, choisissez **[!UICONTROL Virtual Product]**.

   ![Ajouter un produit virtuel](./assets/product-add-virtual.png){width="700" zoomable="yes"}

## Étape 2 : sélection du jeu d’attributs

Pour choisir le [jeu d’attributs](attribute-sets.md) utilisé comme modèle pour le produit, effectuez l’une des opérations suivantes :

- Cliquez dans le champ **[!UICONTROL Attribute Set]** et saisissez tout ou partie du nom du jeu d’attributs.

- Dans la liste affichée, choisissez le jeu d’attributs à utiliser.

Le formulaire est mis à jour pour refléter la modification.

![Choisir un jeu d’attributs](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Étape 3 : Définissez les paramètres requis

1. Saisissez le **[!UICONTROL Product Name]**.

1. Acceptez la valeur par défaut **[!UICONTROL SKU]** basée sur le nom du produit ou saisissez-en une autre.

1. Saisissez le produit **[!UICONTROL Price]**.

1. Comme le produit n’est pas encore prêt à être publié, définissez **[!UICONTROL Enable Product]** sur `No`.

1. Cliquez sur **[!UICONTROL Save]** et continuez.

   Lorsque le produit est enregistré, le programme de sélection [Affichage magasin](introduction.md#product-scope) s’affiche dans le coin supérieur gauche.

1. Sélectionnez l’ **[!UICONTROL Store View]** où le produit doit être disponible.

   ![Choisir la vue de magasin](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Étape 4 : définition des paramètres de base

1. Définissez **[!UICONTROL Tax Class]** sur l’une des options suivantes :

   - `None`
   - `Taxable Goods`

1. Saisissez le **[!UICONTROL Quantity]** du produit en stock et procédez comme suit :

   - Acceptez le paramètre par défaut **[!UICONTROL Stock Status]** de `In Stock`.

     Un produit virtuel n’étant pas fourni, le champ **[!UICONTROL Weight]** n’est pas utilisé.

   - Acceptez le paramètre par défaut **[!UICONTROL Visibility]** de `Catalog, Search`.

   >[!NOTE]
   >
   >Si vous activez [Inventory management](../inventory-management/introduction.md), les marchands à source unique définissent la quantité dans cette section. Les négociants multi-sources ajoutent des sources et des quantités dans la section Sources . Voir la section suivante _Attribuer des sources et des quantités (Inventory management)_ .

1. Pour attribuer **[!UICONTROL Categories]** au produit, cliquez sur la zone **[!UICONTROL Select…]** et effectuez l’une des opérations suivantes :

   **Choisissez une catégorie existante** :

   - Commencez à taper dans la zone jusqu’à ce que vous trouviez une correspondance.

   - Cochez la case de la catégorie à attribuer.

   **Créer une catégorie** :

   - Cliquez sur **[!UICONTROL New Category]**.

   - Saisissez le **[!UICONTROL Category Name]** et choisissez le **[!UICONTROL Parent Category]**, qui détermine sa position dans la structure de menus.

   - Cliquez sur **[!UICONTROL Create Category]**.

   Il peut y avoir d’autres attributs individuels qui décrivent le produit. La sélection varie en fonction de l’ensemble d’attributs. Vous pouvez la terminer ultérieurement.

### Affecter des sources et des quantités ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## Étape 5 : renseigner les informations sur le produit

Renseignez les informations des sections suivantes si nécessaire :

- [Contenu](product-content.md)
- [Images et vidéos](product-images-and-video.md)
- [Optimisation du moteur de recherche](product-search-engine-optimization.md)
- [Produits associés, ventes consécutives et ventes croisées](related-products-up-sells-cross-sells.md)
- [Options personnalisables](settings-advanced-custom-options.md)
- [Produits sur les sites web](settings-basic-websites.md)
- [Conception](settings-advanced-design.md)
- [Options de cadeau](product-gift-options.md)

>[!NOTE]
>
>L’option _[!UICONTROL Is this downloadable product?]_&#x200B;est désactivée par défaut. L’activation de cette fonction pour un produit virtuel rend le produit [Téléchargeable](product-create-downloadable.md#downloadable-product).

## Étape 6 : Publish du produit

1. Si vous êtes prêt à publier le produit dans le catalogue, définissez **[!UICONTROL Enable Product]** sur `Yes`.

1. Effectuez l’une des opérations suivantes :

   - **Méthode 1 :** Enregistrer et prévisualiser

      - Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]**.

      - Pour afficher le produit dans votre boutique, sélectionnez **[!UICONTROL Customer View]** dans le menu _Admin_ ( ![Flèche de menu](../assets/icon-menu-down-arrow-black.png) ).

     Le magasin s’ouvre dans un nouvel onglet du navigateur.

     ![Affichage client](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Méthode 2 :** Enregistrer et fermer

     Dans le menu _[!UICONTROL Save]_(![Flèche de menu](../assets/icon-menu-down-arrow-red.png){width="25"} ), choisissez **[!UICONTROL Save & Close]**.

## Les choses à retenir

- Les produits virtuels sont utilisés pour les produits non tangibles tels que les services, les abonnements et les garanties.

- Les produits virtuels sont comme des produits simples, mais sans poids.

- Les options d’expédition n’apparaissent pas lors du passage en caisse, sauf s’il existe un produit tangible dans le panier.
