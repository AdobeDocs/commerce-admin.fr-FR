---
title: Avoirs
description: Découvrez les avoirs et la manière dont ils sont utilisés pour émettre un remboursement partiel ou complet.
exl-id: dc2faf86-0182-4661-9543-bc6e00e06dbf
feature: Orders, Invoices, Returns
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 0%

---

# Avoirs

Un _avoir_ est un document qui indique le montant dû au client pour un remboursement complet ou partiel. Le montant peut être appliqué à un achat ou remboursé au client. Vous pouvez imprimer un avoir pour une seule commande ou pour plusieurs commandes sous la forme d&#39;un lot. Avant qu&#39;un avoir puisse être imprimé, il doit d&#39;abord être généré pour la commande. La page _avoirs_ répertorie les avoirs qui ont été émis à des clients.

![Avoirs](./assets/credit-memos.png){width="700" zoomable="yes"}

## Méthode de remboursement

Le [mode de paiement](payments.md) de la commande détermine, dans une certaine mesure, le mode de remboursement de la commande.

Vous pouvez rembourser les commandes de trois façons :

- Crédit du compte—Les commandes payées à l&#39;aide d&#39;un compte de crédit peuvent être remboursées sous forme de crédit du compte :
   - ![](../assets/adobe-logo.svg) (Adobe Commerce uniquement) [crédit de la boutique](../customers/store-credit-using.md)
   - ![Adobe Commerce B2B](../assets/b2b.svg) (disponible avec Adobe Commerce B2B) [Paiement sur le compte](../b2b/enable-basic-features.md#configure-payment-on-account) (méthode hors ligne)
   - ![Adobe Commerce B2B](../assets/b2b.svg) (disponible avec Adobe Commerce B2B) [Crédit d’entreprise](../b2b/credit-company.md)
- [Remboursement en ligne](payments.md#online-payment-methods) - Les commandes payées par carte de crédit via une passerelle de paiement, telle que PayPal ou Braintree, sont remboursées en ligne via le processeur de paiement.
- [Remboursement hors ligne](payments.md#offline-payment-methods)—Les commandes payées par règlement à la livraison ([COD](cash-on-delivery.md)) ou par [chèque ou mandat](check-money-order.md) sont remboursées hors ligne.

Vous pouvez émettre un remboursement hors ligne ou un crédit de compte (si activé) pour n’importe quel mode de paiement.

Une commande qui a été payée en espèces à la livraison ([COD](cash-on-delivery.md)) ou par [chèque ou mandat-poste](check-money-order.md) est remboursée hors ligne.

## Workflow de remboursement

1. **Action de paiement** - Si la configuration [Action de paiement](credit-memo-create.md#payment-action-setting) est définie sur `Authorize`, vous devez générer une facture avant de créer un avoir. Passez à l&#39;étape 2. Si le paramètre est défini sur `Authorize and Capture`, une facture a déjà été générée. Passez à l’étape 3.

1. **Générer une facture** - [Créer une facture](invoices.md#create-an-invoice) pour la commande, afin de pouvoir envoyer un remboursement au client via un avoir.

1. **Créer un avoir** - [Émettez un avoir](credit-memo-create.md) dans l&#39;administrateur pour un [achat crédit](credit-memo-create.md#issue-a-refund-for-a-credit-purchase), un [chèque ou un mandat](credit-memo-create.md#issue-an-offline-refund-for-check-or-money-order).

## Descriptions des colonnes

| Colonne | Description |
|--- |--- |
| [!UICONTROL Select] | Cochez les cases des éléments d&#39;avoir qui doivent faire l&#39;objet d&#39;une action ou utilisez le contrôle de sélection dans l&#39;en-tête de colonne. Options : `Select All` / `Deselect All` |
| [!UICONTROL Credit Memo] | Identifiant numérique unique attribué lors de la soumission d&#39;une demande d&#39;avoir. |
| [!UICONTROL Created] | Date et heure auxquelles l&#39;acheteur a soumis pour la première fois la demande d&#39;avoir. |
| [!UICONTROL Order#] | ID de la commande dont les produits sont renvoyés. |
| [!UICONTROL Order Date] | Date et heure auxquelles l&#39;acheteur a passé une commande. |
| [!UICONTROL Bill-to Name] | Nom de la personne responsable du paiement de la commande. |
| [!UICONTROL Status] | Indique le statut actuel d&#39;une demande d&#39;avoir. |
| [!UICONTROL Refunded] | Montant total remboursé de la commande. |
| [!UICONTROL Actions] | **[!UICONTROL View]** - Ouvre la demande d&#39;avoir et conserve un enregistrement de la négociation entre l&#39;acheteur et le vendeur. |
| [!UICONTROL Order Status] | Indique le statut de la commande. |
| [!UICONTROL Purchased From] | Indique l’affichage du site web, du magasin et du magasin dans lequel la commande a été passée. |
| [!UICONTROL Billing Address] | Adresse de facturation du client qui a passé la commande. |
| [!UICONTROL Shipping Address] | Adresse à laquelle la commande doit être expédiée. |
| [!UICONTROL Customer Name] | Prénom et nom du client qui a passé la commande. |
| [!UICONTROL Email] | Adresse e-mail de la personne qui a passé la commande. |
| [!UICONTROL Customer Group] | Groupe de clients auquel le client est affecté. |
| [!UICONTROL Payment Method] | Mode de paiement à utiliser pour le paiement. |
| [!UICONTROL Shipping Information] | Méthode à utiliser pour expédier la commande. |
| [!UICONTROL Subtotal] | Sous-total de la commande, sans expédition ni manutention, ni taxe. |
| [!UICONTROL Shipping & Handling] | Montant facturé pour l&#39;expédition et la manutention. |
| [!UICONTROL Adjustment Refund] | Montant ajouté au montant total remboursé sous forme de remboursement supplémentaire. |
| [!UICONTROL Adjustment Fee] | Montant soustrait du montant total remboursé. |
| [!UICONTROL Grand Total] | Total de la commande. |

{style="table-layout:auto"}
