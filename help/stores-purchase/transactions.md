---
title: Transactions
description: Découvrez la page Transactions et comment l’utiliser pour effectuer le suivi de l’activité entre votre magasin et un système de paiement.
exl-id: 5970db88-146d-4caf-aab4-d9315357a4fe
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 1%

---

# Transactions

La page _Transactions_ répertorie toutes les activités de paiement qui ont eu lieu entre votre magasin et un système de paiement et donne accès à des informations plus détaillées.

## Afficher les transactions

Dans la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Transactions]**.

![Grille des transactions](./assets/transactions.png){width="600" zoomable="yes"}

| Colonne | Description |
|--- |--- |
| [!UICONTROL ID] | Identifiant numérique unique attribué à chaque transaction. |
| [!UICONTROL Order ID] | Identifiant unique attribué lorsqu’un client passe une commande. |
| [!UICONTROL Transaction ID] | Identifiant numérique unique attribué lorsqu’une transaction se produit après qu’un client a passé une commande. |
| [!UICONTROL Parent Transaction ID] | Numéro d’ID de la transaction parent. |
| [!UICONTROL Payment Method] | Mode de paiement associé à une transaction. |
| [!UICONTROL Transaction Type] | Type de transaction : Commande, Autorisation, Capture, Annulation ou Remboursement. |
| [!UICONTROL Closed] | Indique si une transaction est clôturée ou non. |
| [!UICONTROL Created] | Date et heure de création de la transaction. |

{style="table-layout:auto"}

## Afficher les détails de la transaction

Cliquez sur l’entrée que vous souhaitez afficher.

Sur la page Détails de la transaction, vous pouvez voir les détails de la transaction et la grille des transactions enfants.

### Données de transaction

Cette section contient des informations relatives à la transaction et fournit un lien vers la page de commande dans la colonne **ID de commande**.

| Colonne | Description |
|--- |--- |
| [!UICONTROL Transaction ID] | Numéro d&#39;ID de transaction. |
| [!UICONTROL Parent Transaction ID] | Numéro d&#39;identification correspondant à la transaction parent, le cas échéant. |
| [!UICONTROL Transaction Type] | Type de transaction : Commande, Autorisation, Capture, Annulation ou Remboursement. |
| [!UICONTROL Is Closed] | Indique si une transaction est clôturée ou non. |
| [!UICONTROL Created At] | Date et heure de création de la transaction. |

{style="table-layout:auto"}

### Transactions enfants

Les transactions enfants sont affichées dans la grille après la création des factures pour les [commandes](orders.md). Ce format permet d&#39;effectuer le suivi de l&#39;historique des transactions selon une hiérarchie de transactions.

### [!UICONTROL Transaction Details]

Cette section contient les informations supplémentaires relatives à une transaction donnée. Les informations s’affichent sous la forme de clés et de valeurs. Les clés disponibles sont les suivantes :

- authAmount
- authCode
- VSResponse
- billTo
- cardCodeResponse
- client
- customerIP
- lineItems
- marketType
- ordre
- paiement
- produit
- recurringBilling
- responseCode
- responseReasonCode
- responseReasonDescription
- setupAmount
- solution
- submitTimeLocal
- submitTimeUTC
- taxExempt
- transactionStatus

>[!NOTE]
>
>Si les détails de la transaction ne sont pas disponibles ou sont obsolètes, cliquez sur **[!UICONTROL Fetch]** dans la barre de boutons pour les mettre à jour.
