---
title: Renvoie
description: Découvrez le workflow des retours et l’émission d’une autorisation de marchandisage renvoyée.
exl-id: 9dde0360-aa99-4fc4-92ff-976d9874ffec
feature: Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# Renvoie

A _autorisation de marchandisage renvoyée_ (RMA) peut être accordé aux clients qui demandent de renvoyer un article pour le remplacement ou le remboursement. En règle générale, le client contacte le marchand pour demander un remboursement. S’il est approuvé, un numéro de RAM unique est attribué pour identifier le produit renvoyé. Dans la configuration, vous pouvez activer la RAM pour tous les produits ou n’autoriser la RAM que pour certains produits. La variable _[!UICONTROL Returns]_grid répertorie les demandes de marchandises renvoyées actuelles (RMA) et est utilisée pour entrer de nouvelles demandes de retour.

![Renvoie la grille](./assets/return.png){width="600" zoomable="yes"}

Les RMA peuvent être émises pour des types de produits simples, regroupés, configurables et regroupés. Toutefois, les RMA ne sont pas disponibles pour les produits virtuels, les produits téléchargeables et les cartes-cadeaux.

## Descriptions des colonnes

| Colonne | Description |
|--- |--- |
| [!UICONTROL Select] | Cochez les cases correspondant aux retours à soumettre à une action ou utilisez le contrôle de sélection dans l’en-tête de colonne. Options : `Select All` / `Deselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL RMA] | Identifiant numérique unique attribué à chaque retour. |
| [!UICONTROL Requested] | Date et heure auxquelles le retour a été placé |
| [!UICONTROL Order] | Numéro unique de la commande d’origine |
| [!UICONTROL Ordered] | Date et heure auxquelles la commande a été passée |
| [!UICONTROL Customer] | Nom du client ou de l’acheteur qui a passé la commande |
| [!UICONTROL Status] | Etat de retour. Options : `Pending` / `Authorized` / `Partially Authorized` / `Approved` / `Rejected` / `Processed and Closed` / `Closed` |
| [!UICONTROL Action] | **[!UICONTROL View]** ouvre le retour en mode édition. |

{style="table-layout:auto"}

## RMA et workflow de retour

1. **Réception de la demande** - Si [enabled](rma-configure.md#enable-rmas-for-your-store) pour le storefront, les clients enregistrés et les invités peuvent demander une RAM. Vous pouvez également [envoyer une requête RMA dans l’Admin ;](#create-a-return-request-in-the-admin).

2. **RMA émis** - Après avoir examiné la demande, vous pouvez l’autoriser partiellement, complètement ou annuler la demande. Si vous autorisez le retour et acceptez de payer l’expédition retour, vous pouvez créer une commande d’expédition à partir de l’administrateur avec un opérateur pris en charge.

3. **Marchandisage reçue et retour de produits traité** - Le diagramme de flux suivant décrit l’ordre opérationnel pour terminer le processus de retour :

   ![Workflow de retour de produit](./assets/workflow-customer-returns.png){width="500"}

## État RMA

Au cours de son cycle de vie, une autorisation de marchandisage renvoyée (RMA) peut se voir attribuer de nombreux états (comme En attente ou Autorisé). L’état RMA indique l’état d’avancement d’une demande RMA émise par l’utilisateur ou le marchand.

| État | Description |
|--- |--- |
| [!UICONTROL Pending] | État initial affecté à une demande de RAM lorsqu’elle est générée par un utilisateur sur le storefront ou par le commerçant dans l’administrateur. |
| [!UICONTROL Authorized] | Ce statut est attribué à la RAM lorsque tous les articles demandés sont autorisés par le commerçant dans l’Admin pour les retours. |
| [!UICONTROL Partially Authorized] | Ce statut est attribué à la RAM si l’un des articles demandés a été refusé et que d’autres produits sont autorisés. |
| [!UICONTROL Denied] | Ce statut est attribué à la RAM si tous les éléments demandés sont rejetés par le commerçant dans l’Admin pour les retours. |
| [!UICONTROL Return Received] | Ce statut est attribué par le marchand à la RMA lorsque les articles demandés sont reçus de l’utilisateur. |
| [!UICONTROL Return Partially Received] | Ce statut est attribué par le marchand à la RAM lorsque les éléments demandés sont partiellement renvoyés et que certains éléments sont refusés de traitement. |
| [!UICONTROL Approved] | Ce statut est attribué par le marchand à la RAM lorsque les articles demandés sont approuvés pour être traités plus avant. |
| [!UICONTROL Rejected] | Ce statut est attribué par le marchand à la RAM lorsque les éléments demandés sont rejetés pour être traités plus avant. |
| [!UICONTROL Processed and Closed] | Ce statut est attribué par le marchand à la RAM lorsque tous les articles demandés sont approuvés pour être traités plus avant. |
| [!UICONTROL Closed] | Ce statut est attribué par le commerçant à la RMA lorsque les articles demandés ne sont pas traités pour être renvoyés. |

{style="table-layout:auto"}

## Création d’une requête de retour dans l’Admin

Un commerçant peut créer une demande de retour au nom du client auprès de l’administrateur. Les clients peuvent [création d’une requête de retour](rma-customer-experience.md) sur le storefront d’un magasin Adobe Commerce.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Sales]** > **[!UICONTROL Returns]**.

1. Cliquez sur **[!UICONTROL New Return Request]**.

1. Pour créer une requête de retour, cliquez sur une commande comportant une `Complete` statut.

1. Sous , _[!UICONTROL Return Information]_, sélectionnez **[!UICONTROL Return Items]**.

1. Pour ajouter des éléments à renvoyer, cliquez sur **[!UICONTROL Add Items]**.

1. Cochez la case correspondant au produit requis, puis cliquez sur **[!UICONTROL Add Selected Product to returns]**.

1. Pour **[!UICONTROL Requested]**, saisissez le nombre d’éléments à renvoyer.

1. Définir **[!UICONTROL Return Reason]** à l’une des options suivantes :

   - `Wrong Color`
   - `Wrong Size`
   - `Out of Service`
   - `Other`

   Si le motif du retour est différent des choix répertoriés, vous pouvez saisir le vôtre si vous sélectionnez la variable `Other` .

1. Définir **[!UICONTROL Item Condition]** à l’une des options suivantes :

   - `Unopened`
   - `Opened`
   - `Damaged`

1. Définir **[!UICONTROL Resolution]** à l’une des options suivantes :

   - `Exchange`
   - `Refund`
   - `Store Credit`

1. Pour créer un retour, cliquez sur **[!UICONTROL Submit Returns]**.

   ![Éléments RMA demandés](./assets/return-item-request.png){width="600" zoomable="yes"}

   La nouvelle demande de RAM envoyée apparaît sur la **[!UICONTROL Returns]** avec une `Pending` statut.
