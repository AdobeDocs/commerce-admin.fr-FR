---
title: Gestion d’un panier
description: Découvrez comment aider un client à gérer son panier directement depuis l’administration.
exl-id: beb41dfa-ef87-4065-96fd-0649a5c4c21c
feature: Customer Service, Shopping Cart
source-git-commit: 69cd571b66a81159c2c99e6652907f22142568cb
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 1%

---

# Gestion d’un panier

{{ee-feature}}

Pour démarrer une session d’achat assistée, le client doit être connecté à son compte à partir du storefront pour rendre les informations disponibles. Si le client ne dispose pas d’un compte, vous pouvez [en créer un](../customers/account-create.md).

![Panier dans le compte client](./assets/customer-account-manage-cart-items.png){width="600" zoomable="yes"}

## Contrôle des actions

| Option | Description |
|--- |--- |
| [!UICONTROL Remove] | Supprime les articles du panier actuel |
| [!UICONTROL Move to Wish List] | Déplace les éléments vers la liste de souhaits du client sélectionné |

{style="table-layout:auto"}

## Boutons de contrôle

| Bouton | Description |
|--- |--- |
| [!UICONTROL Clear my shopping cart] | Supprime tous les articles du panier. |
| [!UICONTROL Update Items and Quantities|]Saisissez la quantité requise dans le champ **[!UICONTROL Qty]** et mettez à jour le nombre d’articles dans le panier. |
| [!UICONTROL Add selections to my cart] | Ajoute les produits de toutes les sections au panier. |

{style="table-layout:auto"}

## Vérifier que le client est connecté

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Now Online]**.

   Tous les visiteurs du magasin et les clients connectés apparaissent dans la liste.

   ![Clients maintenant en ligne](./assets/customers-now-online.png){width="700" zoomable="yes"}

## Achats assistés par l’offre

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Dans la liste, ouvrez l’enregistrement du client en mode d’édition.

   >[!TIP]
   >
   >Pour trouver l’enregistrement du client rapidement, utilisez la commande [Filtres](../getting-started/admin-grid-controls.md).

   Dans le profil client sous _[!UICONTROL Personal Information]_, la date et l’heure&#x200B;_[!UICONTROL Last Logged In]_ indiquent que le client est en ligne.

   ![Profil client d’un client en ligne](./assets/customer-account-manage-cart.png){width="600" zoomable="yes"}

1. Pour passer en mode d’aide à l’achat, cliquez sur **[!UICONTROL Manage Shopping Cart]** dans la barre de boutons supérieure.

   ![Mode d’achat assisté](./assets/customer-manage-shopping-cart.png){width="600" zoomable="yes"}

## Ajouter des produits au panier par attribut

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Products]** .

1. Recherchez un produit à l’aide de l’un des filtres en haut de chaque colonne.

1. Cliquez sur **[!UICONTROL Search]**.

1. Utilisez l’une des séries d’étapes suivantes en fonction du type de produit :

### Ajouter un produit simple

1. Cliquez sur le produit que vous souhaitez commander.

   Cette action sélectionne l&#39;enregistrement et **[!UICONTROL Quantity]** la valeur par défaut de `1`.

1. Si nécessaire, mettez à jour la quantité commandée.

1. Sur la gauche, au-dessus de la grille, cliquez sur **[!UICONTROL Add selections to my cart]**.

   ![Ajouter un produit au panier](./assets/customer-account-manage-cart-order-products.png){width="600" zoomable="yes"}

   L’élément de ligne est ajouté au panier en haut de la page.

   ![Panier mis à jour](./assets/customer-account-manage-cart-update-cart.png){width="600" zoomable="yes"}

### Ajout d’un produit avec la configuration

Il existe trois types de produits qui doivent être configurés avant d’être ajoutés au panier : `Bundle Product`, `Configurable Product` et `Grouped Product`.

1. Dans la grille, cliquez sur **[!UICONTROL Configure]** en regard du nom du produit.

   ![Configuration du produit](./assets/customer-account-manage-cart-order-configurable-product.png){width="600" zoomable="yes"}

1. Dans la boîte de dialogue _Produits associés_, choisissez chaque option de produit pour décrire l’article à commander, saisissez le **[!UICONTROL Quantity]**, puis cliquez sur **[!UICONTROL OK]**.

   Le produit est sélectionné avec une coche et la quantité commandée apparaît dans la grille.

1. Pour ajouter le produit au panier, cliquez sur **[!UICONTROL Add selections to my cart]**.

   ![Produit configurable dans le panier](./assets/customer-account-manage-cart-order-configurable-product-cart.png){width="600" zoomable="yes"}

1. Mettez à jour les options du produit dans le panier si nécessaire :

   - Cliquez sur **[!UICONTROL Configure]**.

   - Mettez à jour les options, puis cliquez sur **[!UICONTROL OK]**.

## Ajouter un produit par SKU

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Add to Shopping Cart by SKU]** .

1. Ajoutez des produits individuellement en **[!UICONTROL SKU]** ou ajoutez des produits en chargeant un fichier CSV.

### Ajouter des éléments individuellement par SKU

1. Saisissez le **[!UICONTROL SKU]** et le **[!UICONTROL Qty]** de l&#39;article à commander.

1. Pour commander un autre produit, cliquez sur **[!UICONTROL Add another]**.

   ![Ajouter des produits par SKU](./assets/customer-account-manage-cart-order-product-by-sku.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Add selections to my cart]**.

1. Si l’élément est un produit configurable, choisissez les options du produit lorsque vous y êtes invité, puis cliquez sur **[!UICONTROL Add to Shopping Cart]**.

### Ajouter des produits en chargeant un fichier CSV

1. Préparez un [fichier CSV](../systems/data-csv.md) avec les articles à ajouter au panier.

   Le fichier ne doit contenir que deux colonnes, avec `sku` et `qty` dans l’en-tête.

1. Chargez le fichier préparé :

   - Cliquez sur **[!UICONTROL Choose File]**.

   - Sélectionnez le fichier à charger dans votre répertoire .

## Transférer un article

Vous pouvez transférer des articles vers le panier à partir de la liste de souhaits d’un client ou d’une cliente, et d’articles récemment consultés, comparés ou commandés. Le nombre d’éléments dans chaque section apparaît entre parenthèses après l’en-tête de section.

1. Développez ![Sélecteur de développement](../assets/icon-display-expand.png) l’une des sections suivantes :

   - [!UICONTROL Wish List]
   - [!UICONTROL Products in the Comparison List]
   - [!UICONTROL Recently Compared Products]
   - [!UICONTROL Recently Viewed Products]
   - [!UICONTROL Last Ordered Items]

1. Dans la grille, sélectionnez chaque produit à commander et saisissez le **[!UICONTROL Quantity]**.

1. Pour saisir les options d’un produit configurable, cliquez sur **[!UICONTROL Configure]** et définissez les options du produit selon vos besoins.

1. Cliquez sur **[!UICONTROL Add selections to my cart]**.

1. Appliquez un ou plusieurs codes de coupon, le cas échéant :

   - Par **[!UICONTROL Apply Coupon Code]**, saisissez un code de coupon valide.

   - Cliquez sur la flèche _Appliquer_ ( ![icône de flèche](../assets/icon-apply-arrow.png) ).

1. Ajustez la quantité commandée selon les besoins :

   - Dans la colonne **[!UICONTROL Qty]** du produit à ajuster, indiquez le montant correct.

   - Cliquez sur **[!UICONTROL Update Items and Quantities]**.

## Création de la commande

1. Cliquez sur **[!UICONTROL Create Order]**.

   La page _[!UICONTROL Create New Order]_&#x200B;affiche les articles du panier, suivis des informations d’expédition et de paiement.

1. Complétez les informations d&#39;expédition et de paiement.

1. Cliquez sur **[!UICONTROL Submit Order]**.

Pour en savoir plus, voir [Créer une commande](customer-account-create-order.md).

## Supprimer tous les articles d’un panier

La suppression de tous les articles du panier d’un client en mode d’achat assisté est utile si le client souhaite recommencer à zéro, a ajouté des articles incorrects ou doit effacer son panier avant de passer une nouvelle commande. Cela permet de s’assurer que le panier ne contient que les produits que le client souhaite réellement acheter.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Dans la liste, ouvrez l’enregistrement du client en mode d’édition.

1. Cliquez sur **[!UICONTROL Manage Shopping Cart]** dans la barre de boutons supérieure.

1. Cliquez sur **[!UICONTROL Clear my shopping cart]**.

   ![Effacer mon panier](./assets/customer-manage-shopping-cart-clear.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL OK]** lorsque vous êtes invité à confirmer l’action.
