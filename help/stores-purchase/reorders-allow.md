---
title: Autoriser les réordres
description: Découvrez comment offrir des fonctionnalités de réorganisation à vos clients.
exl-id: 9fe4c4fb-8596-4fd0-a93b-927ebdfc0c94
feature: Orders, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# Autoriser les réordres

Lorsque cette option est activée, les commandes peuvent être effectuées directement à partir du compte client ou de la commande d’origine dans la variable _Administration_. Les réordres sont activés par défaut.

![Lien de réorganisation du client dans l’administrateur](./assets/customer-reorder.png){width="700" zoomable="yes"}

## Critères de réorganisation activés pour une commande

- La variable _Autoriser la réorganisation_ l’option de configuration doit être activée.

- Si la commande est dans `Hold` ou `Payment Review` , l’option de réorganisation est désactivée.

- Si l’un des éléments de la commande est indisponible, en rupture de stock ou désactivé, l’option de réorganisation est désactivée sur le storefront.

- Un _Administration_ peut être réorganisé même si l’un des éléments est en rupture de stock ou est désactivé.

## Configuration pour autoriser les commandes client

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales]** en-dessous.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Reorder]** .

   ![Options de réorganisation](../configuration-reference/sales/assets/sales-reorder.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Allow Reorder]** to `Yes`.

   Ce paramètre permet de réorganiser la fonctionnalité à partir du compte client sur le storefront ou de la liste des commandes dans l’administrateur.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Réorganiser à partir du storefront

Un client peut lancer la fonctionnalité de réorganisation d’une commande spécifique à partir de deux pages :

- _Mes commandes_ page

- _Mode Commande_ page

### Mes commandes

La variable _Réorganiser_ est toujours affiché dans la liste avec Commandes (même si tous les produits de la commande ne sont pas disponibles pour réorganisation).

![Exemple de storefront - page Mes commandes](./assets/my-order-page-view.png){width="700" zoomable="yes"}

**Cas 1.** Tous les produits de la commande sont **available** pour réorganiser

L’utilisateur est redirigé vers le panier et tous les produits sont ajoutés au panier.

![Panier](./assets/shopping-cart-page.png){width="700" zoomable="yes"}

**Cas 2.** Certains/tous les produits de la commande sont **non disponible** pour réorganiser

>[!NOTE]
>
>Il est possible de réorganiser `Not Visible Individually` produits.

La variable _Réorganiser_ n’apparaît pas sur le bouton _Mes commandes_ et _Afficher la commande_ pages.

![Ma page Commandes 1](./assets/my-orders-view-page1.png){width="700" zoomable="yes"}

### Page Aperçu de la commande

**Cas 1.** Tous les produits de la commande peuvent être réorganisés.

L’utilisateur est redirigé vers le panier et tous les produits sont ajoutés au panier.

**Cas 2.** Certains/tous les produits de la commande sont **non disponible** pour réorganiser

>[!NOTE]
>
>Il est possible de réorganiser `Not Visible Individually` produits.

La variable _Réorganiser_ n’apparaît pas sur le bouton _Mes commandes_ et _Afficher la commande_ pages.

![Page Détails de la commande](./assets/order-view-page.png){width="700" zoomable="yes"}

### Le panier n’est pas vide

Si le panier n’est pas vide et que l’utilisateur clique **[!UICONTROL Reorder]** (de la fonction _Mes commandes_  ou _Mode Commande_ ), les produits existants restent dans le panier avec les produits de réorganisation ajoutés.

![Réorganiser les éléments](./assets/shopping-cart-view1.png){width="700" zoomable="yes"}

## Réorganiser à partir de l’administrateur

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Recherchez l’ordre et ouvrez-le. **[!UICONTROL View]** mode .

1. Cliquez sur **[!UICONTROL Reorder]** qui s’affiche dans la barre de boutons supérieure.

   ![Détails de la commande dans l’administrateur](./assets/order-view-admin.png){width="600" zoomable="yes"}

   Cliquez ensuite sur **[!UICONTROL Reorder]**, la variable _Créer une commande_ s’ouvre avec les produits de réorganisation.

   ![Créer une réorganisation](./assets/create-reorder-page.png){width="600" zoomable="yes"}

1. Renseignez tous les champs requis selon vos besoins.

1. Pour envoyer la commande, cliquez sur **[!UICONTROL Submit Order]**.
