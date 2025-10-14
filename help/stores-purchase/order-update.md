---
title: Mettre à jour une commande
description: Découvrez comment mettre à jour la commande d’un client dans l’Admin.
exl-id: 15c73d27-f4bd-47d6-8d36-902074f9c3e6
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# Mettre à jour une commande

Lorsque vous aidez un client qui a passé une commande, vous devez déterminer l’état de la commande. Les options disponibles pour une commande `Pending` sont différentes des options pour une commande `Processing`. Pour plus d’informations, voir [Traitement d’une commande](order-processing.md).

## Commandes en attente

Une fois qu’un client a passé une commande, mais avant que le paiement ne soit reçu, la commande est à l’état `Pending`. Vous pouvez modifier la commande, la suspendre ou l’annuler entièrement. La barre de boutons d’une commande en attente répertorie les actions disponibles pour une commande.

![Options de commande en attente](./assets/order-button-bar-pending.png){width="600" zoomable="yes"}

Si vous modifiez des parties importantes d’une commande, celle-ci est annulée et une nouvelle commande est générée. Vous pouvez toutefois modifier l’adresse de facturation ou de livraison sans générer de nouvelle commande.

| Bouton | Description |
|--- |--- |
| **[!UICONTROL Back]** | Renvoie à la page Commandes sans enregistrer les modifications. |
| **[!UICONTROL Login as Customer]** | Permet à un utilisateur administrateur d’assister les clients dans leurs commandes. |
| **[!UICONTROL Cancel]** | Annule l’ordre en attente. |
| **[!UICONTROL Send Email]** | Envoie au client un e-mail sur la commande en attente. |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Définit l’état de l’ordre en attente sur `On Hold`. Pour libérer la suspension, choisissez _[!UICONTROL Unhold]_. |
| **[!UICONTROL Invoice]** | Crée une [facture](invoices.md#create-an-invoice) à partir de la commande en attente en convertissant la commande en facture, et passe l’état de la commande à `processing`. |
| **[!UICONTROL Ship]** | Crée un enregistrement [shipping](shipments.md#create-a-shipment) pour la commande. |
| **[!UICONTROL Reorder]** | Crée un nouvel ordre en attente qui est un doublon de l’ordre en attente actuel. |
| **[!UICONTROL Edit]** | Ouvre un ordre en attente en mode d’édition. Le bouton Modifier est disponible uniquement pour les commandes en attente ou pour les commandes basées sur des [guillemets](../b2b/quotes.md) négociés. |

{style="table-layout:auto"}

## Ordre de traitement

Une commande entre dans un état `Processing` lorsque :

* Le paiement d’une commande est reçu/capturé et la facture est générée, lorsque l’action de paiement est définie sur `Authorize and Capture`.
* Une transaction de commande est autorisée, mais le paiement n’est pas encore capturé, lorsque l’action de paiement est définie sur `Authorize`.

La [configuration de l’action de paiement](../configuration-reference/sales/payment-methods.md#payment-actions) détermine les actions de commande disponibles après la création d’une commande.

Vous ne pouvez pas modifier substantiellement une commande `Processing`, mais vous pouvez modifier l’adresse de facturation et de livraison.

![Options d’ordre de traitement](./assets/order-button-bar-processing.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Lorsque l’action de paiement du mode de paiement est définie sur `Authorize and Capture`, une facture est automatiquement créée lorsque le client passe une commande. Dans ce cas, vous pouvez rembourser des fonds à l’aide d’un [avoir &#x200B;](credit-memo-create.md), mais vous ne pouvez pas [annuler](#cancel-a-pending-order) ou [annuler](#void-a-processing-order) la commande.

| Bouton | Description |
|--- |--- |
| **[!UICONTROL Back]** | Renvoie à la page Commandes sans enregistrer les modifications. |
| **[!UICONTROL Send Email]** | Envoie un courrier électronique au client au sujet de la commande. |
| **[!UICONTROL Void]** | [Void](#void-a-processing-order) une transaction de commande ou une transaction de commande partielle. |
| **[!UICONTROL Credit Memo]** | Lance le processus de création d’une [note de crédit](credit-memo-create.md). |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Définit l’état de la commande client sur `On Hold`. Pour libérer le blocage de la commande client, choisissez _[!UICONTROL Unhold]_. |
| **[!UICONTROL Reorder]** | Crée un nouvel ordre en attente en fonction de l’ordre actuel. |
| **[!UICONTROL Create Returns]** | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Lance le processus pour [renvoyer](returns.md) un ou plusieurs éléments de la commande. |

{style="table-layout:auto"}

## Vider une commande de traitement

Lorsqu’une commande est toujours dans un état `Processing` et que l’intégration de paiement est définie sur `Authorize` (et non `Authorize and Capture`), vous pouvez uniquement annuler une transaction ou annuler une commande. [Annuler une commande](#cancel-a-pending-order) annule également l’autorisation.

Lorsqu’une commande est passée à l’aide d’un mode de paiement dont l’action de paiement est définie sur `Authorize and Capture`, vous pouvez rembourser les fonds par le biais d’un avoir à rembourser, mais ne pouvez pas l’annuler car ils sont facturés et le paiement est capturé.

Votre mode de paiement détermine les actions de paiement disponibles. Voir [Actions de paiement](../configuration-reference/sales/payment-methods.md#payment-actions) pour plus d’informations.

**_Pour annuler une commande :_**

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Dans la colonne **[!UICONTROL Action]** de la commande à éditer, cliquez sur **[!UICONTROL View]**.

1. Cliquez sur **[!UICONTROL Void]** pour annuler la commande.

1. À l’invite, cliquez sur **[!UICONTROL OK]** pour annuler la commande.

Vous pouvez effectuer tous les remboursements nécessaires à l’aide d’un [avoir](credit-memo-create.md) une fois que les fonds ont été capturés. Vous pouvez également créer une [autorisation de retour de marchandises (RMA)](returns.md) émise pour les retours de produits. Pour en savoir plus, voir [Traitement d’une commande](order-processing.md).

## Modifier une commande en attente

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Dans la colonne **[!UICONTROL Action]** de la commande à éditer, cliquez sur **[!UICONTROL View]**.

1. Cliquez sur **[!UICONTROL Edit]**.

   ![Modifier l’ordre](./assets/order-edit.png){width="600" zoomable="yes"}

1. À l’invite, cliquez sur **[!UICONTROL OK]** pour continuer la modification.

1. Mettez à jour la commande si nécessaire.

1. Appliquez vos modifications :
   * Pour enregistrer les modifications apportées à l’adresse de facturation ou de livraison, cliquez sur **[!UICONTROL Save]**.
   * Pour enregistrer les modifications apportées aux éléments de ligne et retraiter l’ordre, cliquez sur **[!UICONTROL Submit Order]**.

## Mettre une commande en attente

Si le mode de paiement préféré du client n’est pas disponible ou si l’article est temporairement en rupture de stock, vous pouvez suspendre la commande.

1. Dans la grille _Commandes_, recherchez l’ordre `Pending` que vous souhaitez suspendre.

1. Dans la colonne _Action_, cliquez sur **[!UICONTROL View]**.

1. Cliquez sur **[!UICONTROL Hold]** pour suspendre la commande.

Pour supprimer le blocage d’une commande, modifiez à nouveau la commande et cliquez sur **[!UICONTROL Unhold]**.

## Annuler une commande en attente

L’annulation d’une commande passe de `Pending` à `Canceled`.

1. Dans la grille _[!UICONTROL Orders]_, recherchez l&#39;ordre d&#39;annulation en attente.

1. Dans la colonne _[!UICONTROL Action]_, cliquez sur **[!UICONTROL View]**.

1. Cliquez sur **[!UICONTROL Cancel]** pour annuler la commande.

L’état de la commande est désormais `Canceled`.
