---
title: Autoriser les réordres
description: Découvrez comment offrir des fonctionnalités de réorganisation à vos clients.
exl-id: 9fe4c4fb-8596-4fd0-a93b-927ebdfc0c94
feature: Orders, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---

# Autoriser les réordres

Lorsque cette option est activée, les commandes peuvent être effectuées directement à partir du compte client ou de la commande d’origine dans l’ _Admin_. Les réordres sont activés par défaut.

![Lien de réorganisation du client dans l’Admin](./assets/customer-reorder.png){width="700" zoomable="yes"}

## Critères de réorganisation activés pour une commande

- L’option de configuration _Autoriser la réorganisation_ doit être activée.

- Si la commande est à l’état `Hold` ou `Payment Review`, l’option de réorganisation est désactivée.

- Si l’un des éléments de la commande est indisponible, en rupture de stock ou désactivé, l’option de réorganisation est désactivée sur le storefront.

- Un _administrateur_ peut réorganiser même si l’un des éléments est en rupture de stock ou est désactivé.

## Configuration pour autoriser les commandes client

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et sélectionnez **[!UICONTROL Sales]** sous .

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Reorder]** .

   ![Options de réorganisation](../configuration-reference/sales/assets/sales-reorder.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Allow Reorder]** sur `Yes`.

   Ce paramètre permet de réorganiser la fonctionnalité à partir du compte client sur le storefront ou de la liste des commandes dans l’administrateur.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Réorganiser à partir du storefront

Un client peut lancer la fonctionnalité de réorganisation d’une commande spécifique à partir de deux pages :

- _Ma page Commandes_

- _Page Afficher la commande_

### Mes commandes

Le bouton _Réorganiser_ est toujours affiché dans la liste avec Commandes (même si tous les produits de la commande ne sont pas disponibles pour la réorganisation).

![Exemple de storefront - Ma page Commandes](./assets/my-order-page-view.png){width="700" zoomable="yes"}

**Cas 1.** Tous les produits de la commande sont **disponibles** pour réorganisation

L’utilisateur est redirigé vers le panier et tous les produits sont ajoutés au panier.

![Panier](./assets/shopping-cart-page.png){width="700" zoomable="yes"}

**Cas 2.** Certains/tous les produits de la commande ne sont **pas disponibles** pour la réorganisation

>[!NOTE]
>
>Il est possible de réorganiser des produits `Not Visible Individually`.

Le bouton _Réorganiser_ n’apparaît pas sur les pages _Mes commandes_ et _Afficher la commande_.

![Ma page Commandes 1](./assets/my-orders-view-page1.png){width="700" zoomable="yes"}

### Page Aperçu de la commande

**Cas 1.** Tous les produits de la commande peuvent être réorganisés.

L’utilisateur est redirigé vers le panier et tous les produits sont ajoutés au panier.

**Cas 2.** Certains/tous les produits de la commande ne sont **pas disponibles** pour la réorganisation

>[!NOTE]
>
>Il est possible de réorganiser des produits `Not Visible Individually`.

Le bouton _Réorganiser_ n’apparaît pas sur les pages _Mes commandes_ et _Afficher la commande_.

![Page Détails de la commande](./assets/order-view-page.png){width="700" zoomable="yes"}

### Le panier n’est pas vide

Si le panier n’est pas vide et que l’utilisateur clique sur **[!UICONTROL Reorder]** (à partir de la page _Mes commandes_ ou _consultation de la commande_), les produits existants restent dans le panier avec les produits de réorganisation ajoutés.

![Réorganiser les éléments](./assets/shopping-cart-view1.png){width="700" zoomable="yes"}

## Réorganiser à partir de l’administrateur

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Recherchez l’ordre et ouvrez-le en mode **[!UICONTROL View]**.

1. Cliquez sur **[!UICONTROL Reorder]** qui s’affiche dans la barre de boutons supérieure.

   ![Détails de la commande dans l’administrateur](./assets/order-view-admin.png){width="600" zoomable="yes"}

   Une fois que vous avez cliqué sur **[!UICONTROL Reorder]**, la page _Créer une nouvelle commande_ s’ouvre avec les produits de réorganisation.

   ![Créer une réorganisation](./assets/create-reorder-page.png){width="600" zoomable="yes"}

1. Renseignez tous les champs requis selon vos besoins.

1. Pour envoyer la commande, cliquez sur **[!UICONTROL Submit Order]**.
