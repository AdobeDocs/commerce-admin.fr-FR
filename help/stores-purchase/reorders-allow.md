---
title: Autoriser les nouvelles commandes
description: Découvrez comment offrir des fonctionnalités de réorganisation à vos clients.
exl-id: 9fe4c4fb-8596-4fd0-a93b-927ebdfc0c94
feature: Orders, Storefront
TQID: https://experienceleague.adobe.com/comSKludWZnDkDjdZyhi4-9WNAE9scH3dgSce08IyJo
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 432
ht-degree: 0%

---

# Autoriser les nouvelles commandes

Lorsque cette option est activée, les commandes peuvent être effectuées directement à partir du compte client ou de la commande d’origine dans l’_Admin_. Les réapprovisionnements sont activés par défaut.

![Lien de réorganisation du client dans l’Administration](./assets/customer-reorder.png){width="700" zoomable="yes"}

## Critères d’activation de la réorganisation pour une commande

- L’option de configuration _Autoriser la réorganisation_ doit être activée.

- Si l’ordre est à l’état `Hold` ou `Payment Review`, l’option de réorganisation est désactivée.

- Si l’un des articles de la commande est indisponible, en rupture de stock ou désactivé, l’option de réorganisation est désactivée sur le storefront.

- Un _administrateur_ peut réorganiser l’ordre même si l’un des éléments est en rupture de stock ou désactivé.

## Configurer pour autoriser les nouvelles commandes client

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales]** en dessous.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Reorder]** .

   ![Réorganiser les options](../configuration-reference/sales/assets/sales-reorder.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Allow Reorder]** sur `Yes`.

   Ce paramètre active la fonctionnalité de réorganisation à partir du compte client sur le storefront ou de la liste des commandes dans l’Admin.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Réorganiser à partir du storefront

Un client peut lancer la fonctionnalité de réorganisation pour une commande spécifique à partir de deux pages :

- Page _Mes commandes_

- Page _Vue Commande_

### Mes commandes

Le bouton _Réorganiser_ est toujours affiché dans la liste avec Commandes (même si tous les produits de la commande ne peuvent pas être réorganisés).

![Exemple de storefront - Page Mes commandes](./assets/my-order-page-view.png){width="700" zoomable="yes"}

**Cas 1.** Tous les produits de la commande sont **disponibles** pour la réorganisation

L’utilisateur est redirigé vers le panier et tous les produits sont ajoutés au panier

![Panier](./assets/shopping-cart-page.png){width="700" zoomable="yes"}

**Cas 2.** Certains/tous les produits de la commande ne sont **pas disponibles** pour la réorganisation

>[!NOTE]
>
>Il est possible de réorganiser les produits `Not Visible Individually`.

Le bouton _Réorganiser_ n’apparaît pas sur les pages _Mes commandes_ et _Afficher la commande_.

![Page Mes commandes 1](./assets/my-orders-view-page1.png){width="700" zoomable="yes"}

### Page Vue Commande

**Cas 1.** Tous les produits de la commande sont disponibles pour la réorganisation

L’utilisateur est redirigé vers le panier et tous les produits sont ajoutés au panier

**Cas 2.** Certains/tous les produits de la commande ne sont **pas disponibles** pour la réorganisation

>[!NOTE]
>
>Il est possible de réorganiser les produits `Not Visible Individually`.

Le bouton _Réorganiser_ n’apparaît pas sur les pages _Mes commandes_ et _Afficher la commande_.

![Page Détails de la commande](./assets/order-view-page.png){width="700" zoomable="yes"}

### Panier non vide

Si le panier n’est pas vide et que l’utilisateur clique sur **[!UICONTROL Reorder]** (à partir de la page _Mes commandes_ ou _Vue des commandes_), les produits existants restent dans le panier avec les produits de nouvelle commande ajoutés.

![Réorganiser les éléments](./assets/shopping-cart-view1.png){width="700" zoomable="yes"}

## Réorganiser à partir de l’administrateur

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Recherchez la commande et ouvrez en mode **[!UICONTROL View]**.

1. Cliquez sur **[!UICONTROL Reorder]** qui s’affiche dans la barre de boutons supérieure.

   ![Détails de la commande dans l’Administration](./assets/order-view-admin.png){width="600" zoomable="yes"}

   Après avoir cliqué sur **[!UICONTROL Reorder]**, la page _Créer une nouvelle commande_ s’ouvre avec des produits à réorganiser.

   ![Créer une réorganisation](./assets/create-reorder-page.png){width="600" zoomable="yes"}

1. Renseignez tous les champs obligatoires selon vos besoins.

1. Pour envoyer la commande, cliquez sur **[!UICONTROL Submit Order]**.
