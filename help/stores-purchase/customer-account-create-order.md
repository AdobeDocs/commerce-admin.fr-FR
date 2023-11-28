---
title: Création d’une commande
description: Découvrez comment créer une commande pour un client dans l’administrateur Commerce.
exl-id: 8a766a5b-55d6-4d78-859e-38937e0183d3
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 1%

---

# Création d’une commande

Pour les clients enregistrés qui ont besoin d’aide, vous pouvez créer une commande entière directement à partir de l’administrateur. La variable _[!UICONTROL Create New Order]_form comprend toutes les informations nécessaires au processus de passage en caisse normal, avec des résumés d’activité provenant du tableau de bord du compte du client.

![Création d’une commande pour un client](./assets/create-new-order.png){width="700" zoomable="yes"}

## Étape 1 : création d’une commande

1. Sur le _Administration_ barre latérale, cliquez sur **[!UICONTROL Customers]**.

1. Trouvez le client dans la grille.

1. Dans le _Action_ colonne, cliquez sur **[!UICONTROL Edit]**.

1. Dans l’en-tête de l’espace de travail, cliquez sur **[!UICONTROL Create Order]**.

   ![En-tête de Workspace](./assets/order-create-buttons.png){width="700" zoomable="yes"}

   Vous pouvez également créer une commande dans la variable [Espace de travail de commande](orders.md#orders-workspace) en cliquant **[!UICONTROL Create New Order]**.

## Étape 2 : Ajout de produits

Si votre boutique comporte plusieurs vues, choisissez la vue du magasin où la commande doit être placée.

### Ajoutez des produits à partir du [!UICONTROL Customer's Activities] barre latérale

Vous pouvez transférer des articles vers le panier à partir de la liste de souhaits d’un client, ou tout article récemment consulté, comparé ou commandé.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) l’une des sections suivantes :

   - **[!UICONTROL Wish List]**
   - **[!UICONTROL Last Ordered Items]**
   - **[!UICONTROL Products in Comparison List]**
   - **[!UICONTROL Recently Compared Products]**
   - **[!UICONTROL Recently Viewed Products]**

1. Cochez la case de chaque produit dans le panneau de gauche.

1. Faites défiler la page vers le bas et cliquez sur **[!UICONTROL Update Changes]**.

   L’élément apparaît dans le formulaire de commande.

   ![Ajouter au panier](./assets/create-order-add-wishlist.png){width="600" zoomable="yes"}

### Ajout de produits du catalogue

1. Cliquez sur **[!UICONTROL Add Products]**.

   ![Ajouter des produits](./assets/account-add-wishlist-product.png){width="600" zoomable="yes"}

1. Dans la grille, cochez la case de chaque produit à ajouter au panier et saisissez le **[!UICONTROL Qty]** à acheter.

   ![Sélectionner des produits](./assets/create-order-from-catalog.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >La grille de sélection de produits affiche toujours les prix de base réguliers pour les produits, sans aucune remise et aucune règle de prix de panier ou de groupe appliquée. Le prix final du produit est calculé uniquement lorsque le produit est ajouté à une commande/un panier.

1. Configurez les options de produit disponibles :

   - Cliquez sur **[!UICONTROL Configure]**.

   - Renseignez les options suivant vos besoins.

   - Cliquez sur **[!UICONTROL OK]**.

   - Cliquez sur **[!UICONTROL Add Selected Product(s) to Order]** pour mettre à jour le panier.

1. Si un produit est configuré pour [options de cadeau](../catalog/product-gift-options.md), définissez les options selon les besoins.

1. Remplacez le prix d’un article si nécessaire :

   - Sélectionnez la variable **[!UICONTROL Custom Price]** et saisissez le nouveau prix dans la case ci-dessous.

   - Pour mettre à jour les totaux du panier, cliquez sur **[!UICONTROL Update Items and Quantities]**.

   ![Prix personnalisé](./assets/create-order-custom-price.png){width="600" zoomable="yes"}

1. Renseignez les sections suivantes selon les besoins pour la commande :

   - [!UICONTROL Order Currency]
   - [!UICONTROL Apply Coupon Codes / Gift Card Code]
   - [!UICONTROL Payment Method]
   - [!UICONTROL Shipping Method]
   - [!UICONTROL Order Comments]

>[!NOTE]
>
>Voir [Guide des services de paiement](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/create-order.html) pour plus d’informations sur les méthodes de paiement pour prendre en charge cette fonctionnalité lorsque l’extension des services de paiement est installée et configurée.

## Etape 3 : Envoyer la commande

Cliquez sur **[!UICONTROL Submit Order]**.

Une confirmation est envoyée au client qui peut afficher les détails de la commande depuis son compte.
