---
title: Autoriser l'annulation de la commande
description: Découvrez comment offrir des fonctionnalités d’annulation à vos clients.
feature: Orders, Storefront
source-git-commit: 613c081c02dd9b5e55de37dccd021af4e429d424
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---


# Autoriser l&#39;annulation de la commande

Lorsque cette option est activée, vous pouvez annuler une commande directement à partir du compte du client. L’option Annuler est désactivée par défaut.

## Critères d&#39;annulation activés pour une commande

- Le _Autoriser l&#39;annulation de la commande_ l’option de configuration doit être activée.

- Si l’ordre est dans `Hold`, `Canceled`, `Complete`, ou `Closed` statut, l’option annuler est désactivée sur le storefront.

- Si l&#39;un des articles de la commande a été expédié, l&#39;option d&#39;annulation est désactivée sur le storefront.

- Si un article est payé, l&#39;option d&#39;annulation est activée et le remboursement est créé pour cet article.

- Si l’ordre est dans `Pending` ou `Processing` statut, l’option annuler est activée sur le storefront.

## Configurez pour autoriser l’annulation du client et personnaliser les raisons de l’annulation

1. Le _Admin_ barre latérale, accéder à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et sélectionnez **[!UICONTROL Sales]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) le **[!UICONTROL Order cancellation]** section.

   ![Options d’annulation de commande](../configuration-reference/sales/assets/sales-order-cancellation.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Order cancellation through GraphQL]** vers `Yes`.

   Ce paramètre active la fonctionnalité d’annulation du compte client sur le storefront.

1. Dans le **[!UICONTROL Order Order cancellation reasons]** vous pouvez ajouter, supprimer ou modifier n’importe quel motif d’annulation.

   Avec ce paramètre, les raisons d’annulation s’affichent sur le storefront pour le client lorsqu’il annule une commande.
Assurez-vous d’avoir spécifié au moins une raison.

1. Clic **[!UICONTROL Save Config]**.

## Annuler à partir du storefront

Un client peut lancer la fonctionnalité d&#39;annulation pour une commande spécifique à partir de trois pages :

- _Mes commandes_ page

- _Vue Commande_ page

- _Mon compte_ page

### Mes commandes

Le _Annuler la commande_ s’affiche dans la page Mes commandes si la commande peut être annulée.

![Exemple de storefront - Page Mes commandes](./assets/my-order-page-view-cancel.png){width="700" zoomable="yes"}

### Page d’affichage des commandes

Le _Annuler la commande_ Le bouton s’affiche sur la page Afficher la commande si la commande peut être annulée.

![Page Détails de la commande](./assets/order-view-page-cancel.png){width="700" zoomable="yes"}

### Mon compte

Le _Annuler la commande_ s’affiche dans la section Commandes récentes de la page Mon compte si la commande peut être annulée.

![Page Mon compte](./assets/my-account-page-view-cancel.png){width="700" zoomable="yes"}


