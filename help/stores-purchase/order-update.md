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

Lorsque vous aidez un client qui a passé une commande, vous devez déterminer l’état de la commande. Les options disponibles pour une `Pending` l’ordre diffère des options d’un `Processing` commande. Pour plus d’informations, voir [Traitement de la commande](order-processing.md).

## Commandes en attente

Une fois qu’un client a passé une commande, mais avant que le paiement ne soit reçu, la commande est dans `Pending` statut. Vous pouvez modifier la commande, la suspendre ou l’annuler entièrement. La barre de boutons d’une commande en attente répertorie les actions disponibles pour une commande.

![Options d’ordre en attente](./assets/order-button-bar-pending.png){width="600" zoomable="yes"}

Si vous modifiez des parties importantes d’une commande, celle-ci est annulée et une nouvelle commande est générée. Vous pouvez toutefois modifier l’adresse de facturation ou de livraison sans générer de nouvelle commande.

| Bouton | Description |
|--- |--- |
| **[!UICONTROL Back]** | Renvoie à la page Commandes sans enregistrer les modifications. |
| **[!UICONTROL Login as Customer]** | Permet à un utilisateur administrateur d’assister les clients dans leurs commandes. |
| **[!UICONTROL Cancel]** | Annule l’ordre en attente. |
| **[!UICONTROL Send Email]** | Envoie au client un e-mail sur la commande en attente. |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Modifie l’état de l’ordre en attente en `On Hold`. Pour libérer la suspension, choisissez _[!UICONTROL Unhold]_. |
| **[!UICONTROL Invoice]** | Crée une [facture](invoices.md#create-an-invoice) de la commande en attente en convertissant la commande en facture et en définissant l’état de la commande sur `processing`. |
| **[!UICONTROL Ship]** | Crée une [envoi](shipments.md#create-a-shipment) Enregistrez la commande. |
| **[!UICONTROL Reorder]** | Crée un nouvel ordre en attente qui est un doublon de l’ordre en attente actuel. |
| **[!UICONTROL Edit]** | Ouvre un ordre en attente en mode d’édition. Le bouton Modifier est disponible uniquement pour les commandes en attente ou pour les commandes basées sur des commandes négociées. [citations](../b2b/quotes.md). |

{style="table-layout:auto"}

## Ordre de traitement

Une commande entre dans une `Processing` state lorsque :

* Le paiement d’une commande est reçu/capturé et la facture est générée lorsque l’action de paiement est définie sur `Authorize and Capture`.
* Une transaction de commande est autorisée, mais le paiement n’est pas encore capturé, lorsque l’action de paiement est définie sur `Authorize`.

La variable [configuration des actions de paiement](../configuration-reference/sales/payment-methods.md#payment-actions) détermine les actions de commande disponibles une fois la commande créée.

Vous ne pouvez pas modifier de manière substantielle une `Processing` commande, mais vous pouvez modifier l’adresse de facturation et de livraison.

![Options d’ordre de traitement](./assets/order-button-bar-processing.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Lorsque l’action de paiement du mode de paiement est définie sur `Authorize and Capture`, une facture est automatiquement créée lorsque le client passe une commande. Dans ce cas, vous pouvez rembourser des fonds en utilisant une [note de crédit](credit-memo-create.md), mais ne le peut pas [cancel](#cancel-a-pending-order) ou [void](#void-a-processing-order) la commande.

| Bouton | Description |
|--- |--- |
| **[!UICONTROL Back]** | Renvoie à la page Commandes sans enregistrer les modifications. |
| **[!UICONTROL Send Email]** | Envoie un courrier électronique au client au sujet de la commande. |
| **[!UICONTROL Void]** | [Voix](#void-a-processing-order) une transaction de commande ou une transaction de commande partielle. |
| **[!UICONTROL Credit Memo]** | Lance le processus de création d’une [note de crédit](credit-memo-create.md). |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Modifie l’état de la commande client en `On Hold`. Pour libérer le blocage de la commande client, choisissez _[!UICONTROL Unhold]_. |
| **[!UICONTROL Reorder]** | Crée un nouvel ordre en attente en fonction de l’ordre actuel. |
| **[!UICONTROL Create Returns]** | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Lance le processus en [return](returns.md) un ou plusieurs éléments de la commande. |

{style="table-layout:auto"}

## Vider une commande de traitement

Lorsqu’une commande est toujours dans une `Processing` et l’intégration de paiement est définie sur `Authorize` (not) `Authorize and Capture`), vous pouvez uniquement annuler une transaction ou une commande. [Annuler une commande](#cancel-a-pending-order) permet également d’annuler l’autorisation.

Lorsqu’une commande est passée à l’aide d’un mode de paiement avec l’action de paiement définie sur `Authorize and Capture` vous pouvez rembourser les fonds par note de crédit, mais vous ne pouvez pas les annuler car ils sont facturés et le paiement est capturé.

Votre mode de paiement détermine les actions de paiement disponibles. Voir [Actions de paiement](../configuration-reference/sales/payment-methods.md#payment-actions) pour plus d’informations.

**_Pour annuler une commande :_**

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Dans le **[!UICONTROL Action]** pour l’ordre à modifier, cliquez sur **[!UICONTROL View]**.

1. Cliquez sur **[!UICONTROL Void]** pour annuler la commande.

1. À l’invite, cliquez sur **[!UICONTROL OK]** pour annuler la commande.

Vous pouvez effectuer tous les remboursements nécessaires à l’aide d’un [note de crédit](credit-memo-create.md) une fois les fonds saisis. Vous pouvez également créer une [autorisation de retour de marchandises (RMA)](returns.md) émis pour les retours de produits. Pour en savoir plus, voir [Traitement de la commande](order-processing.md).

## Modifier une commande en attente

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Dans le **[!UICONTROL Action]** pour l’ordre à modifier, cliquez sur **[!UICONTROL View]**.

1. Cliquez sur **[!UICONTROL Edit]**.

   ![Modifier l’ordre](./assets/order-edit.png){width="600" zoomable="yes"}

1. À l’invite, cliquez sur **[!UICONTROL OK]** pour continuer la modification.

1. Mettez à jour la commande si nécessaire.

1. Appliquez vos modifications :
   * Pour enregistrer les modifications apportées à l’adresse de facturation ou de livraison, cliquez sur **[!UICONTROL Save]**.
   * Pour enregistrer les modifications apportées aux éléments de ligne et retraiter l’ordre, cliquez sur **[!UICONTROL Submit Order]**.

## Mettre une commande en attente

Si le mode de paiement préféré du client n’est pas disponible ou si l’article est temporairement en rupture de stock, vous pouvez suspendre la commande.

1. Dans le _Commandes_ grille, recherchez la variable `Pending` ordre que vous souhaitez mettre en attente.

1. Dans le _Action_ colonne, cliquez sur **[!UICONTROL View]**.

1. Cliquez sur **[!UICONTROL Hold]** pour suspendre la commande.

Pour supprimer le blocage d’une commande, modifiez-le à nouveau, puis cliquez sur **[!UICONTROL Unhold]**.

## Annuler une commande en attente

L’annulation d’une commande modifie son état à partir de `Pending` to `Canceled`.

1. Dans le _[!UICONTROL Orders]_grille, recherchez l&#39;ordre en attente à annuler.

1. Dans le _[!UICONTROL Action]_colonne, cliquez sur **[!UICONTROL View]**.

1. Cliquez sur **[!UICONTROL Cancel]** pour annuler la commande.

L’état de la commande est désormais `Canceled`.
