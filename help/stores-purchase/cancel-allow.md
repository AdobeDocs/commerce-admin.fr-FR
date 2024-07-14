---
title: Autoriser l’annulation de la commande
description: Découvrez comment offrir des fonctionnalités d’annulation à vos clients.
feature: Orders, Storefront
exl-id: 5a8ef668-f929-4188-8574-0bccdd076f3e
source-git-commit: a9d1dc4fe50e98f0f1dfc8ec204930e2cc885d6e
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---

# Autoriser l’annulation de la commande

Lorsque cette option est activée, vous pouvez annuler une commande directement à partir du compte du client. Annuler est désactivé par défaut.

## Critères d’annulation à activer pour une commande

- L’option de configuration _Autoriser l’annulation de la commande_ doit être activée.

- Si la commande est à l’état `Hold`, `Canceled`, `Complete` ou `Closed`, l’option Annuler est désactivée sur le storefront.

- Si l’un des éléments de la commande a été expédié, l’option Annuler est désactivée sur le storefront.

- Si un article est payé, l’option Annuler est activée et le remboursement est créé pour cet article.

- Si la commande est à l’état `Pending` ou `Processing`, l’option Annuler est activée sur le storefront.

## Configurer pour autoriser l’annulation du client et personnaliser les raisons de l’annulation

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et sélectionnez **[!UICONTROL Sales]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Order cancellation]** .

   ![Options d’annulation de commande](../configuration-reference/sales/assets/sales-order-cancellation.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Order cancellation through GraphQL]** sur `Yes`.

   Ce paramètre active la fonctionnalité d’annulation du compte client sur le storefront.

1. Dans le **[!UICONTROL Order Order cancellation reasons]**, vous pouvez ajouter, supprimer ou modifier un motif d’annulation.

   Avec ce paramètre, les raisons de l’annulation s’affichent sur le storefront pour le client lorsqu’il annule une commande.
Assurez-vous d’avoir spécifié au moins une raison.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Annuler depuis le storefront

Un client peut lancer la fonctionnalité d’annulation d’une commande spécifique à partir de trois pages :

- _Ma page Commandes_

- _Page Afficher la commande_

- _Page Mon compte_

### Mes commandes

Le bouton _Annuler la commande_ s’affiche sur la page Mes commandes si la commande peut être annulée.

![Exemple de storefront - Ma page Commandes](./assets/my-order-page-view-cancel.png){width="700" zoomable="yes"}

### Page Aperçu de la commande

Le bouton _Annuler la commande_ s’affiche sur la page Afficher la commande si la commande peut être annulée.

![Page Détails de la commande](./assets/order-view-page-cancel.png){width="700" zoomable="yes"}

### Mon compte

Le bouton _Annuler la commande_ s’affiche dans la section Commandes récentes de la page Mon compte, si la commande peut être annulée.

![Ma page de compte](./assets/my-account-page-view-cancel.png){width="700" zoomable="yes"}
