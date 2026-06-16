---
title: Autoriser l'annulation de la commande
description: Découvrez comment offrir des fonctionnalités d’annulation à vos clients.
feature: Orders, Storefront
exl-id: 5a8ef668-f929-4188-8574-0bccdd076f3e
TQID: https://experienceleague.adobe.com/a0jMKgF4a0qXUe15oT2syai6-kGSegU1BX56PO9SSKs
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 291
ht-degree: 0%

---

# Autoriser l&#39;annulation de la commande

Lorsque cette option est activée, vous pouvez annuler une commande directement à partir du compte du client. L’option Annuler est désactivée par défaut.

## Critères d&#39;annulation activés pour une commande

- L&#39;option de configuration _Autoriser l&#39;annulation de la commande_ doit être activée.

- Si la commande a le statut `Hold`, `Canceled`, `Complete` ou `Closed`, l’option Annuler est désactivée sur le storefront.

- Si l’un des articles de la commande a été expédié, l’option d’annulation est désactivée sur le storefront.

- Si un article est payé, l&#39;option d&#39;annulation est activée et le remboursement est créé pour cet article.

- Si la commande a le statut `Pending` ou `Processing`, l’option d’annulation est activée sur le storefront.

## Configurez pour autoriser l’annulation du client et personnaliser les raisons de l’annulation

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et sélectionnez **[!UICONTROL Sales]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Order cancellation]** .

   ![Options d’annulation de commande](../configuration-reference/sales/assets/sales-order-cancellation.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Order cancellation through GraphQL]** sur `Yes`.

   Ce paramètre active la fonctionnalité d’annulation du compte client sur le storefront.

1. Dans le **[!UICONTROL Order Order cancellation reasons]**, vous pouvez ajouter, supprimer ou modifier n’importe quel motif d’annulation.

   Avec ce paramètre, les raisons d’annulation s’affichent sur le storefront pour le client lorsqu’il annule une commande.
Assurez-vous d’avoir spécifié au moins une raison.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Annuler à partir du storefront

Un client peut lancer la fonctionnalité d&#39;annulation pour une commande spécifique à partir de trois pages :

- Page _Mes commandes_

- Page _Vue Commande_

- Page _Mon compte_

### Mes commandes

Le bouton _Annuler la commande_ s’affiche sur la page Mes commandes si la commande peut être annulée.

![Exemple de storefront - Page Mes commandes](./assets/my-order-page-view-cancel.png){width="700" zoomable="yes"}

### Page Vue Commande

Le bouton _Annuler la commande_ s’affiche sur la page Afficher la commande si la commande peut être annulée.

![Page Détails de la commande](./assets/order-view-page-cancel.png){width="700" zoomable="yes"}

### Mon compte

Le bouton _Annuler la commande_ s’affiche dans la section Commandes récentes de la page Mon compte, si la commande peut être annulée.

![Page Mon compte](./assets/my-account-page-view-cancel.png){width="700" zoomable="yes"}
