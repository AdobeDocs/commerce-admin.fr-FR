---
title: Gestion d’un panier
description: Découvrez comment assister un client avec son panier directement depuis l’administrateur.
exl-id: beb41dfa-ef87-4065-96fd-0649a5c4c21c
feature: Customer Service, Shopping Cart
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 1%

---

# Gestion d’un panier

{{ee-feature}}

Pour démarrer une session d’achat assistée, le client doit être connecté à son compte à partir du storefront afin de rendre les informations disponibles. Si le client ne dispose pas d’un compte, vous pouvez [créer un](../customers/account-create.md).

![Panier dans le compte client](./assets/customer-account-manage-cart-items.png){width="600" zoomable="yes"}

## Contrôle des actions

| Option | Description |
|--- |--- |
| [!UICONTROL Remove] | Supprime des articles du panier actuel. |
| [!UICONTROL Move to Wish List] | Déplace les éléments vers la liste des souhaits de client sélectionnée. |

{style="table-layout:auto"}

## Boutons de contrôle

| Bouton | Description |
|--- |--- |
| [!UICONTROL Clear my shopping cart] | Efface le panier actuel de tous les produits. |
| [!UICONTROL Update Items and Quantities|]Saisissez la quantité requise dans la variable **[!UICONTROL Qty]** et mettre à jour le nombre d’articles dans le panier. |
| [!UICONTROL Add selections to my cart] | Ajoute les produits de toutes les sections au panier. |

{style="table-layout:auto"}

## Vérification de la connexion du client

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Now Online]**.

   Tous les visiteurs du magasin et les clients connectés apparaissent dans la liste.

   ![Clients maintenant en ligne](./assets/customers-now-online.png){width="700" zoomable="yes"}

## Offrir des achats assistés

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Dans la liste, ouvrez l’enregistrement du client en mode d’édition.

   >[!TIP]
   >
   >Pour rechercher rapidement l’enregistrement du client, utilisez la méthode [Filtres](../getting-started/admin-grid-controls.md) contrôle.

   Dans le profil du client sous _[!UICONTROL Personal Information]_, la variable_[!UICONTROL Last Logged In]_ date et heure indique que le client est en ligne.

   ![Profil client d’un client en ligne](./assets/customer-account-manage-cart.png){width="600" zoomable="yes"}

1. Pour passer en mode d’achat assisté, cliquez sur **[!UICONTROL Manage Shopping Cart]** dans la barre de boutons supérieure.

   ![Mode d’achat assisté](./assets/customer-manage-shopping-cart.png){width="600" zoomable="yes"}

## Ajout de produits au panier par attribut

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Products]** .

1. Recherchez un produit à l’aide des filtres situés en haut de chaque colonne.

1. Cliquez sur **[!UICONTROL Search]**.

1. Suivez l’une des étapes suivantes en fonction du type de produit :

### Ajout d’un produit simple

1. Cliquez sur le produit que vous souhaitez commander.

   Cette action sélectionne l’enregistrement et définit **[!UICONTROL Quantity]** par défaut de `1`.

1. Si nécessaire, mettez à jour la quantité commandée.

1. Sur la gauche au-dessus de la grille, cliquez sur **[!UICONTROL Add selections to my cart]**.

   ![Ajout d’un produit au panier](./assets/customer-account-manage-cart-order-products.png){width="600" zoomable="yes"}

   L’article est ajouté au panier en haut de la page.

   ![Mise à jour du panier](./assets/customer-account-manage-cart-update-cart.png){width="600" zoomable="yes"}

### Ajout d’un produit avec configuration

Trois types de produits doivent être configurés avant d’être ajoutés au panier : `Bundle Product`, `Configurable Product`, et `Grouped Product`.

1. Dans la grille, cliquez sur **[!UICONTROL Configure]** en regard du nom du produit.

   ![Configuration du produit](./assets/customer-account-manage-cart-order-configurable-product.png){width="600" zoomable="yes"}

1. Dans le _Produits associés_ , sélectionnez chaque option de produit pour décrire l’élément à commander, puis saisissez la variable **[!UICONTROL Quantity]**, puis cliquez sur **[!UICONTROL OK]**.

   Le produit est sélectionné avec une coche et la quantité commandée apparaît dans la grille.

1. Pour ajouter le produit au panier, cliquez sur **[!UICONTROL Add selections to my cart]**.

   ![Produit configurable dans le panier](./assets/customer-account-manage-cart-order-configurable-product-cart.png){width="600" zoomable="yes"}

1. Au besoin, mettez à jour les options de produit dans le panier :

   - Cliquez sur **[!UICONTROL Configure]**.

   - Mettez à jour les options, puis cliquez sur **[!UICONTROL OK]**.

## Ajouter un produit par SKU

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Add to Shopping Cart by SKU]** .

1. Ajoutez des produits individuellement en **[!UICONTROL SKU]** ou ajoutez des produits en chargeant un fichier CSV.

### Ajouter des éléments individuellement par SKU

1. Saisissez le **[!UICONTROL SKU]** et **[!UICONTROL Qty]** de l’élément à commander.

1. Pour commander un autre produit, cliquez sur **[!UICONTROL Add another]**.

   ![Ajout de produits par SKU](./assets/customer-account-manage-cart-order-product-by-sku.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Add selections to my cart]**.

1. Si l’élément est un produit configurable, choisissez les options du produit lorsque vous y êtes invité, puis cliquez sur **[!UICONTROL Add to Shopping Cart]**.

### Ajout de produits en chargeant un fichier CSV

1. Préparer une [fichier csv](../systems/data-csv.md) avec les éléments à ajouter au panier.

   Le fichier ne doit contenir que deux colonnes, avec `sku` et `qty` dans l’en-tête .

1. Téléchargez le fichier préparé :

   - Cliquez sur **[!UICONTROL Choose File]**.

   - Sélectionnez le fichier à charger dans votre répertoire.

## Transfert d’un élément

Vous pouvez transférer des articles vers le panier à partir de la liste de souhaits d’un client, ainsi que des articles récemment consultés, comparés ou commandés. Le nombre d’éléments dans chaque section apparaît entre parenthèses après l’en-tête de section.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) l’une des sections suivantes :

   - [!UICONTROL Wish List]
   - [!UICONTROL Products in the Comparison List]
   - [!UICONTROL Recently Compared Products]
   - [!UICONTROL Recently Viewed Products]
   - [!UICONTROL Last Ordered Items]

1. Dans la grille, sélectionnez chaque produit à commander et saisissez le **[!UICONTROL Quantity]**.

1. Pour saisir les options d’un produit configurable, cliquez sur **[!UICONTROL Configure]** et définissez les options de produit selon les besoins.

1. Cliquez sur **[!UICONTROL Add selections to my cart]**.

1. Appliquez un code de bon si disponible :

   - Pour **[!UICONTROL Apply Coupon Code]**, saisissez un code de bon valide.

   - Cliquez sur le bouton _Appliquer_ ( ![Icône fléchée](../assets/icon-apply-arrow.png) ).

1. Ajustez la quantité commandée selon les besoins :

   - Dans le **[!UICONTROL Qty]** de la colonne du produit à ajuster, indiquez le montant correct.

   - Cliquez sur **[!UICONTROL Update Items and Quantities]**.

## Création de la commande

1. Cliquez sur **[!UICONTROL Create Order]**.

   La variable _[!UICONTROL Create New Order]_affiche les articles du panier, suivis des informations d’expédition et de paiement.

1. Renseignez les informations d’expédition et de paiement.

1. Cliquez sur **[!UICONTROL Submit Order]**.

Pour en savoir plus, voir [Création d’une commande](customer-account-create-order.md).
