---
title: Remboursements dans le tableau de bord du compte client
description: Les clients de la boutique peuvent consulter les informations de remboursement associées à la commande dans le tableau de bord de leur compte.
exl-id: 8fd6d4e7-74ba-4f39-9a19-7c77ee63b913
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 0%

---

# Remboursements dans le tableau de bord du compte client

{{ee-feature}}

Si un remboursement a été effectué pour une commande, les clients peuvent consulter dans le tableau de bord de leur compte les informations de remboursement associées à la commande. Si vous avez activé la variable [!UICONTROL _Afficher l’historique du crédit de magasin aux clients_] option pour [Configuration du crédit de magasin](../customers/credit-configure.md), les clients peuvent également accéder à leurs [Crédit de la boutique](../customers/store-credit.md) historique.

## Afficher un remboursement sur la vitrine

1. Depuis le storefront, le client se connecte à son compte.

1. Localise leur ordre à l’aide de l’une des méthodes suivantes :

   * Trouver l&#39;ordre dans la liste des **Commandes récentes** et clic **[!UICONTROL View]**.
   * Dans le panneau de gauche, en choisissant **[!UICONTROL My Orders]**. Recherchez ensuite l’ordre dans la liste et cliquez sur **[!UICONTROL View]**.

1. Le client clique sur la variable **[!UICONTROL Refunds]** pour visualiser le détail du remboursement.

   ![Détails du remboursement sur le storefront](assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

## Afficher l’historique et le solde du crédit de la boutique en ligne

Méthode 1 : **Depuis le tableau de bord du compte client**

1. Depuis le storefront, le client se connecte à son compte.

1. Si le remboursement a été appliqué au crédit de magasin, choisissez **[!UICONTROL Store Credit]** dans le panneau de gauche.

1. Le montant remboursé à leur crédit de magasin apparaît dans la liste avec la date et l’heure de l’action.

   ![Montant remboursé pour stocker le crédit](assets/customer-account-store-credit.png){width="700" zoomable="yes"}

   >[!INFO]
   >
   >La page Crédit de la boutique fournit également un lien permettant au client de récupérer un [carte cadeau](../stores-purchase/product-gift-card-workflow.md#check-status-and-balance-of-the-gift-card).

Méthode 2 : **Dans la _Révision et paiements_ page**

1. Le client ajoute un produit au panier.

2. Accède à la fonction _Passage en caisse_ page.

3. Transmet la variable **[!UICONTROL Shipping]** étape .

4. Si le crédit de magasin est disponible, le client clique **[!UICONTROL Use Store Credit]**.

   ![Crédit de magasin sur la page Révision et paiements](assets/customer-account-order-refund-from-checkout.png){width="700" zoomable="yes"}

5. Si le client change d’avis sur l’utilisation du crédit de magasin, cliquez sur **[!UICONTROL Remove]** dans le _Synthèse des commandes_ .

## Actions de paiement dans l’administrateur

Vous pouvez configurer des actions de paiement pour votre [Mode de paiement](../configuration-reference/sales/payment-methods.md). Chaque mode de paiement possède un ensemble différent d’actions de paiement.

| Action de paiement | Description |
|--- |---|
| [!UICONTROL Capture Online] | Lorsque la facture est envoyée, le système capture le paiement à partir de la passerelle de paiement tierce. Un utilisateur administrateur peut alors créer un avoir et annuler la facture. |
| [!UICONTROL Capture Offline] | Lorsque la facture est envoyée, le système ne récupère pas le paiement. On suppose que le paiement est capturé directement par le biais de la passerelle et que le paiement ne peut pas être capturé par le biais d’Adobe Commerce. Un utilisateur administrateur peut alors créer un avoir, mais ne peut pas annuler la facture. (Même si la commande a utilisé un paiement en ligne, la facture est essentiellement une facture hors ligne.) |
| [!UICONTROL Not Capture] | Lorsque la facture est envoyée, le système ne récupère pas le paiement. On suppose que le paiement est capturé par Adobe Commerce ultérieurement. Il existe une [!UICONTROL _Capture_] dans la facture terminée. Avant de procéder à l&#39;extraction, vous pouvez annuler la facture. Après l’acquisition, vous pouvez créer un avoir et annuler la facture. |

{style="table-layout:auto"}

>[!WARNING]
>
>Sélectionnez la variable [!UICONTROL _Pas de capture_] à moins que vous ne soyez certain que vous allez capturer le paiement par le biais d’Adobe Commerce ultérieurement. Vous ne pouvez pas créer d’avoir tant que le paiement n’a pas été capturé à l’aide de la variable [!UICONTROL _Capture_] bouton .
