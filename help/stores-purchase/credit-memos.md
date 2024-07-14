---
title: Avoir
description: Découvrez les notes de crédit et comment elles sont utilisées pour émettre un remboursement partiel ou complet.
exl-id: dc2faf86-0182-4661-9543-bc6e00e06dbf
feature: Orders, Invoices, Returns
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# Avoir

Un _note de crédit_ est un document qui indique le montant dû au client pour un remboursement complet ou partiel. Le montant peut être appliqué à un achat ou remboursé au client. Vous pouvez imprimer une note de crédit pour une seule commande ou pour plusieurs commandes par lot. Avant de pouvoir imprimer une note de crédit, elle doit d’abord être générée pour la commande. La page _Avoir de crédit_ répertorie les avoir émis à l’intention des clients.

![Mémos de crédit](./assets/credit-memos.png){width="700" zoomable="yes"}

## Méthode de remboursement

Le [mode de paiement](payments.md) de la commande détermine, dans une certaine mesure, le mode de remboursement d’une commande.

Vous pouvez rembourser les commandes de trois manières :

- Crédit du compte : les commandes payées à l’aide d’un compte de crédit peuvent être remboursées en tant que crédit du compte :
   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) [Crédit de boutique](../customers/store-credit-using.md)
   - ![Adobe Commerce B2B](../assets/b2b.svg) (Disponible avec Adobe Commerce B2B) [Paiement sur compte](../b2b/enable-basic-features.md#configure-payment-on-account) (méthode hors ligne)
   - ![Adobe Commerce B2B](../assets/b2b.svg) (Disponible avec Adobe Commerce B2B) [Crédit entreprise](../b2b/credit-company.md)
- [Remboursement en ligne](payments.md#online-payment-methods) : les commandes payées par carte de crédit via une passerelle de paiement, telle que PayPal ou Braintree, sont remboursées en ligne par l’intermédiaire du processeur de paiement.
- [Remboursement hors ligne](payments.md#offline-payment-methods) : les commandes payées par espèces à la livraison ([DCO](cash-on-delivery.md)) ou par [chèque ou mandat d’achat](check-money-order.md) sont remboursées hors ligne.

Vous pouvez accorder un remboursement hors ligne ou un crédit de compte (s’il est activé) pour n’importe quel mode de paiement.

Une commande qui a été payée en espèces à la livraison ([DCO](cash-on-delivery.md)) ou par [chèque ou mandat](check-money-order.md)) est remboursée hors ligne.

## Workflow de remboursement

1. **Action de paiement** - Si la configuration [Action de paiement](credit-memo-create.md#payment-action-setting) est définie sur `Authorize`, vous devez générer une facture avant de créer une note de crédit, passez à l’étape 2. Si celle-ci est définie sur `Authorize and Capture`, une facture a déjà été générée et passez à l’étape 3.

1. **Générer une facture** - [ Créez une facture](invoices.md#create-an-invoice) pour la commande, de sorte que vous puissiez envoyer un remboursement au client via un avoir.

1. **Créer un avoir** - [Émettez un avoir](credit-memo-create.md) dans l’administrateur pour un [achat de crédit](credit-memo-create.md#issue-a-refund-for-a-credit-purchase) ou un [chèque ou mandat bancaire](credit-memo-create.md#issue-an-offline-refund-for-check-or-money-order).

## Descriptions des colonnes

| Colonne | Description |
|--- |--- |
| [!UICONTROL Select] | Cochez les cases correspondant aux éléments de la note de crédit à soumettre à une action ou utilisez le contrôle de sélection dans l’en-tête de colonne. Options : `Select All` / `Deselect All` |
| [!UICONTROL Credit Memo] | Identifiant numérique unique attribué lors de l’envoi d’une demande de note de crédit. |
| [!UICONTROL Created] | Date et heure auxquelles l’acheteur a d’abord soumis la demande de note de crédit. |
| [!UICONTROL Order#] | Identifiant de la commande dont les produits sont renvoyés. |
| [!UICONTROL Order Date] | Date et heure auxquelles l’acheteur a passé une commande. |
| [!UICONTROL Bill-to Name] | Nom de la personne chargée de payer la commande. |
| [!UICONTROL Status] | Indique l’état actuel d’une demande de note de crédit. |
| [!UICONTROL Refunded] | Montant total remboursé de la commande. |
| [!UICONTROL Actions] | **[!UICONTROL View]** - Ouvre la demande de note de crédit et conserve un enregistrement de la négociation entre l’acheteur et le vendeur. |
| [!UICONTROL Order Status] | Indique l’état de la commande. |
| [!UICONTROL Purchased From] | Indique la vue du site web, du magasin et du magasin où la commande a été passée. |
| [!UICONTROL Billing Address] | Adresse de facturation du client qui a passé la commande. |
| [!UICONTROL Shipping Address] | Adresse à laquelle la commande doit être expédiée. |
| [!UICONTROL Customer Name] | Prénom et nom du client qui a passé la commande. |
| [!UICONTROL Email] | Adresse électronique de la personne qui a passé la commande. |
| [!UICONTROL Customer Group] | Groupe de clients auquel le client est affecté. |
| [!UICONTROL Payment Method] | Mode de paiement à utiliser pour le paiement. |
| [!UICONTROL Shipping Information] | Méthode à utiliser pour envoyer la commande. |
| [!UICONTROL Subtotal] | Sous-total de la commande, sans frais d’expédition et de gestion, ni taxes. |
| [!UICONTROL Shipping & Handling] | Montant imputé à l’expédition et à la manipulation. |
| [!UICONTROL Adjustment Refund] | Montant ajouté au montant total remboursé en tant que remboursement supplémentaire. |
| [!UICONTROL Adjustment Fee] | Montant soustrait du montant total remboursé. |
| [!UICONTROL Grand Total] | Total de la commande. |

{style="table-layout:auto"}
