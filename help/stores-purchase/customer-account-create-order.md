---
title: Création d’une commande
description: Découvrez comment créer une commande pour un client dans Commerce Admin.
exl-id: 8a766a5b-55d6-4d78-859e-38937e0183d3
feature: Orders, Customer Service
source-git-commit: 0e2d79f6b716f5d59aa9cd60b096608a6b2dbb98
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 1%

---

# Création d’une commande

Pour les clients enregistrés qui ont besoin d’aide, vous pouvez créer une commande entière directement à partir de l’administrateur. Le formulaire _[!UICONTROL Create New Order]_&#x200B;contient toutes les informations nécessaires au processus de passage en caisse normal, avec des résumés des activités du tableau de bord du compte du client.

![Créer une commande pour un client](./assets/create-new-order.png){width="700" zoomable="yes"}

## Étape 1 : créer une commande

1. Dans la barre latérale _Admin_, cliquez sur **[!UICONTROL Customers]**.

1. Recherchez le client dans la grille.

1. Dans la colonne _Action_, cliquez sur **[!UICONTROL Edit]**.

1. Dans l’en-tête de l’espace de travail, cliquez sur **[!UICONTROL Create Order]**.

   ![En-tête Workspace](./assets/order-create-buttons.png){width="700" zoomable="yes"}

   Vous pouvez également créer une commande dans l’espace de travail [Commande](orders.md#orders-workspace) en cliquant sur **[!UICONTROL Create New Order]**.

## Étape 2 : Ajouter des produits

Si votre boutique comporte plusieurs vues, choisissez celle où la commande doit être passée.

### Ajouter des produits à partir de la barre latérale [!UICONTROL Customer's Activities]

Vous pouvez transférer des articles vers le panier à partir de la liste de souhaits d’un client ou de tout article récemment consulté, comparé ou commandé.

1. Développez ![Sélecteur de développement](../assets/icon-display-expand.png) l’une des sections suivantes :

   - **[!UICONTROL Wish List]**
   - **[!UICONTROL Last Ordered Items]**
   - **[!UICONTROL Products in Comparison List]**
   - **[!UICONTROL Recently Compared Products]**
   - **[!UICONTROL Recently Viewed Products]**

1. Cochez la case de chaque produit dans le panneau de gauche.

1. Faites défiler vers le bas et cliquez sur **[!UICONTROL Update Changes]**.

   L’article apparaît dans le formulaire de commande.

   ![Ajouter au panier](./assets/create-order-add-wishlist.png){width="600" zoomable="yes"}

### Ajouter des produits à partir du catalogue

1. Cliquez sur **[!UICONTROL Add Products]**.

   ![Ajouter des produits](./assets/account-add-wishlist-product.png){width="600" zoomable="yes"}

1. Dans la grille, cochez la case de chaque produit à ajouter au panier et saisissez le **[!UICONTROL Qty]** à acheter.

   ![Sélectionner des produits](./assets/create-order-from-catalog.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >La grille de sélection de produits affiche toujours les prix de base standard des produits, sans remises et sans règles de prix de panier ou de groupe appliquées. Le prix final du produit est calculé uniquement lorsque le produit est ajouté à une commande ou à un panier.

1. Configurez les options de produit disponibles :

   - Cliquez sur **[!UICONTROL Configure]**.

   - Renseignez les options selon vos besoins.

   - Cliquez sur **[!UICONTROL OK]**.

   - Cliquez sur **[!UICONTROL Add Selected Product(s) to Order]** pour mettre à jour le panier.

1. Si un produit est configuré pour des [options de cadeau](../catalog/product-gift-options.md), définissez les options selon vos besoins.

1. Remplacez le prix d’un article si nécessaire :

   - Cochez la case **[!UICONTROL Custom Price]** et saisissez le nouveau prix dans la case ci-dessous.

   - Pour mettre à jour les totaux du panier, cliquez sur **[!UICONTROL Update Items and Quantities]**.

   ![Prix personnalisé](./assets/create-order-custom-price.png){width="600" zoomable="yes"}

1. Renseignez les sections suivantes selon vos besoins pour la commande :

   - [!UICONTROL Order Currency]
   - [!UICONTROL Apply Coupon Codes / Gift Card Code]
   - [!UICONTROL Payment Method]
   - [!UICONTROL Shipping Method]
   - [!UICONTROL Order Comments]
   - [[!UICONTROL [Attributs d&#39;ordre personnalisés]]](../stores-purchase/order-processing.md#custom-order-attributes)

>[!NOTE]
>
>Consultez le [ Guide des services de paiement ](https://experienceleague.adobe.com/fr/docs/commerce/payment-services/guide-overview) pour plus d’informations sur les modes de paiement afin de prendre en charge cette fonctionnalité lorsque l’extension des services de paiement est installée et configurée.

## Étape 3 : envoyer la commande

Cliquez sur **[!UICONTROL Submit Order]**.

Une confirmation est envoyée au client qui peut consulter les détails de la commande à partir de son compte.
