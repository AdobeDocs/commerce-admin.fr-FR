---
title: Produit de carte-cadeau
description: Découvrez comment créer un produit de carte-cadeau qui produit un code unique à racheter par un client destinataire lors de son passage en caisse.
exl-id: bc4b60fe-10b3-4d17-85ce-35c2720c90a2
feature: Catalog Management, Products, Gift
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 0%

---

# Produit de carte-cadeau

{{ee-feature}}

Chaque carte-cadeau comporte un code unique, qui ne peut être consommé que par un seul client lors du passage en caisse. A [pool de code](../stores-purchase/product-gift-card-accounts.md#step-3-establish-the-gift-card-code-pool) doit être établi avant que les cartes-cadeaux puissent être vendues. Voir [Workflow de carte cadeau](../stores-purchase/product-gift-card-workflow.md) pour plus d’informations sur le mode de consommation des cartes-cadeaux dans le panier.

![Page de produit de carte-cadeau](./assets/storefront-giftcard-product-page.png){width="700" zoomable="yes"}

Il existe trois types de cadeaux :

- **Virtuel** - Une carte-cadeau virtuelle est envoyée à l’adresse électronique du destinataire, qui est requise lors de l’achat de la carte-cadeau. Une adresse de livraison n’est pas nécessaire.

- **Physique** - Une carte-cadeau physique est envoyée à l’adresse du destinataire, qui est requise lors de l’achat de la carte-cadeau.

- **Combiné** - Une carte-cadeau combinée est envoyée au destinataire par courrier électronique. L’adresse email et l’adresse de livraison du destinataire sont obligatoires lors de l’achat de la carte-cadeau.

## Créer un produit de carte-cadeau

Les instructions suivantes montrent le processus de création d’une carte-cadeau à l’aide d’une [modèle de produit](attribute-sets.md), champs obligatoires et paramètres de base. Chaque champ requis est marqué d’un astérisque rouge (`*`). Lorsque vous avez terminé les étapes de base, vous pouvez définir les autres paramètres du produit selon vos besoins.

### Etape 1 : Sélection du type de produit

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Dans le coin supérieur droit du _[!UICONTROL Add Product]_( ![Flèche de menu](../assets/icon-menu-down-arrow-red.png){width="25"}  ), choisissez **[!UICONTROL Gift Card]**.

   ![Ajouter une carte cadeau](./assets/product-add-gift-card.png){width="700" zoomable="yes"}

### Étape 2 : sélection du jeu d’attributs

Vous pouvez utiliser la valeur par défaut `Gift Card` ensemble d’attributs ou sélectionnez une autre. Pour choisir le jeu d’attributs utilisé comme modèle pour le produit, effectuez l’une des opérations suivantes :

- Cliquez sur dans le **[!UICONTROL Attribute Set]** et saisissez tout ou partie du nom du jeu d’attributs.

- Dans la liste affichée, choisissez le jeu d’attributs à utiliser.

![Choisir un jeu d’attributs](./assets/product-create-choose-attribute-set-gift-card.png){width="600" zoomable="yes"}

### Étape 3 : Définissez les paramètres requis

1. Saisissez un **[!UICONTROL Product Name]** pour la carte-cadeau.

   Vous pouvez également indiquer le type de carte-cadeau dans le nom. Par exemple : _Luma Virtual Gift Card_.

1. Saisissez un **[!UICONTROL SKU]** pour le produit.

   Par défaut, le nom du produit est utilisé comme SKU par défaut.

1. Définir **[!UICONTROL Card Type]** à l’une des options suivantes :

   - `Virtual` - Les cartes de voeux virtuelles sont remises par courrier électronique au destinataire.
   - `Physical` - Les cartes de cadeaux physiques peuvent être produites en masse à l&#39;avance et revêtues de codes uniques.
   - `Combined` - Une carte-cadeau combinée présente les caractéristiques d’une carte-cadeau virtuelle et physique.

   ![Type de carte cadeau](./assets/product-create-gift-card-type.png){width="600" zoomable="yes"}

1. Pour offrir au client un choix de montants fixes, cliquez sur **[!UICONTROL Add Amount]** et saisissez la première valeur fixe de la carte sous forme de décimale.

   Pour saisir la sélection des montants fixes, répétez cette étape pour chacun d&#39;eux.

1. Pour donner aux clients la possibilité de définir la valeur de la carte-cadeau, procédez comme suit :

   - Définir **[!UICONTROL Open Amount]** to `Yes`.

   - Pour définir la plage de valeurs minimales et maximales acceptables, saisissez la variable **[!UICONTROL Open Amount From]** et **[!UICONTROL To]** valeurs.

   Vous pouvez créer des cartes-cadeaux avec prix fixe, prix d’ouverture ou les deux.

   ![Montants des cartes cadeau](./assets/product-create-gift-card-amounts.png){width="600" zoomable="yes"}

### Étape 4 : définition des paramètres de base

1. Pour une carte-cadeau physique ou combinée, saisissez la variable **[!UICONTROL Quantity]** en stock.

1. Si la carte-cadeau doit être expédiée, saisissez la variable **[!UICONTROL Weight]** du package.

1. Dans le **[!UICONTROL Categories]** champ, choisissez `Gift Card`.

Il peut y avoir d’autres attributs individuels qui décrivent le produit. La sélection varie le jeu d’attributs et vous pouvez les terminer ultérieurement.

### Étape 5 : renseigner les informations sur la carte-cadeau

La variable _[!UICONTROL Gift Card Information]_de la section des paramètres du produit peuvent être utilisés pour remplacer la variable [configuration des cartes de voeux](../configuration-reference/sales/gift-cards.md) paramètres qui déterminent la manière dont la carte est gérée.

1. Faites défiler l’écran vers le bas jusqu’à _[!UICONTROL Gift Card Information]_.

   Les paramètres par défaut de cette section sont déterminés par la configuration du système.

   ![Informations sur les cartes cadeau](./assets/product-gift-card-information.png){width="600" zoomable="yes"}

1. Modifiez les champs supplémentaires en fonction du mode de fonctionnement de la carte-cadeau :

   - **[!UICONTROL Treat Balance as Store Credit]** - Détermine si le détenteur de la carte-cadeau peut rembourser le solde en tant que crédit de magasin.

   - **[!UICONTROL Lifetime (days)]** - Détermine le nombre de jours après l’achat jusqu’à l’expiration de la carte-cadeau. Si vous ne souhaitez pas définir de limite de durée de vie de la carte, laissez ce champ vide.

   - **[!UICONTROL Allow Message]** - Détermine si l’acheteur de la carte-cadeau peut saisir un message pour le destinataire. Un message cadeau peut être inclus pour les cartes-cadeaux virtuelles (envoyées par courrier électronique) et physiques (envoyées).

   - **[!UICONTROL Email Template]** - Détermine le modèle d’email utilisé pour la notification envoyée au destinataire d’une carte-cadeau.

### Étape 6 : renseigner les informations sur le produit

Renseignez les informations des sections suivantes si nécessaire :

- [Contenu](product-content.md)
- [Images et vidéos](product-images-and-video.md)
- [Produits associés, ventes consécutives et ventes croisées](related-products-up-sells-cross-sells.md)
- [Optimisation du moteur de recherche](product-search-engine-optimization.md)
- [Options personnalisables](settings-advanced-custom-options.md)
- [Produits sur les sites web](settings-basic-websites.md)
- [Conception](settings-advanced-design.md)
- [Options de cadeau](product-gift-options.md)

### Etape 7 : Publier le produit

1. Si vous êtes prêt à publier le produit dans le catalogue, définissez **Activer le produit** passer à `Yes`.

1. Effectuez l’une des opérations suivantes :

   **Méthode 1 :** Enregistrer et prévisualiser

   - Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]**.

   - Pour afficher le produit dans votre boutique, choisissez **[!UICONTROL Customer View]** sur le _Administration_ ( ![Flèche de menu](../assets/icon-menu-down-arrow-black.png) ),

   ![Vue du client](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **Méthode 2 :** Enregistrer et fermer

   Sur le _[!UICONTROL Save]_( ![Flèche de menu](../assets/icon-menu-down-arrow-red.png){width="25"} ), choisissez **[!UICONTROL Save & Close]**.

## Les choses à retenir

- A _pool de code_ de numéros uniques doivent être générés pour qu’une carte-cadeau puisse être proposée en vente.

- Les cartes cadeau peuvent être définies sur `Redeemable` ou `Non-Redeemable`.

- Les taxes **_non appliqué_** aux cartes-cadeaux lors de l’achat d’une carte-cadeau. Les taxes ne sont appliquées aux produits que lorsqu’une carte-cadeau achetée est utilisée pour acheter des produits.

- La durée de vie d’une carte-cadeau peut être illimitée ou définie sur un nombre spécifié de jours.

- La valeur d’une carte-cadeau peut être définie sur un montant fixe ou sur un montant ouvert avec une valeur minimale et maximale.

- Un compte de carte-cadeau pour le client peut être créé lorsque la commande est passée ou au moment de la facture.