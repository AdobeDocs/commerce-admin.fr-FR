---
title: Remboursements dans le tableau de bord du compte client
description: Les clients de la boutique peuvent consulter les informations de remboursement associées à la commande dans le tableau de bord de leur compte.
exl-id: 8fd6d4e7-74ba-4f39-9a19-7c77ee63b913
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Remboursements dans le tableau de bord du compte client

{{ee-feature}}

Si un remboursement a été effectué pour une commande, les clients peuvent consulter dans le tableau de bord de leur compte les informations de remboursement associées à la commande. Si vous avez activé l’option [!UICONTROL _Afficher l’historique de crédit de magasin aux clients_] pour [&#x200B; la configuration de crédit de magasin &#x200B;](../customers/credit-configure.md), les clients peuvent également accéder à leur historique de [crédit de magasin](../customers/store-credit.md).

## Afficher un remboursement sur la vitrine

1. Depuis le storefront, le client se connecte à son compte.

1. Localise leur ordre à l’aide de l’une des méthodes suivantes :

   * Recherchez l’ordre dans la liste des **commandes récentes** et cliquez sur **[!UICONTROL View]**.
   * Dans le panneau de gauche, sélectionnez **[!UICONTROL My Orders]**. Recherchez ensuite l’ordre dans la liste et cliquez sur **[!UICONTROL View]**.

1. Le client clique sur l’onglet **[!UICONTROL Refunds]** pour afficher les détails du remboursement.

   ![Détails du remboursement sur le storefront](assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

## Afficher l’historique et le solde du crédit de la boutique en ligne

Méthode 1 : **à partir du tableau de bord du compte client**

1. Depuis le storefront, le client se connecte à son compte.

1. Si le remboursement a été appliqué au crédit de magasin, sélectionnez **[!UICONTROL Store Credit]** dans le panneau de gauche.

1. Le montant remboursé à leur crédit de magasin apparaît dans la liste avec la date et l’heure de l’action.

   ![Montant remboursé pour stocker le crédit](assets/customer-account-store-credit.png){width="700" zoomable="yes"}

   >[!INFO]
   >
   >La page Crédit de la boutique fournit également un lien permettant au client d’échanger une [carte-cadeau](../stores-purchase/product-gift-card-workflow.md#check-status-and-balance-of-the-gift-card).

Méthode 2 : **sur la page _Révision et paiements_**

1. Le client ajoute un produit au panier.

2. Passe à la page _Passage en caisse_ .

3. Transmet l’étape **[!UICONTROL Shipping]**.

4. Si le crédit de magasin est disponible, le client clique sur **[!UICONTROL Use Store Credit]**.

   ![Stocker le crédit à partir de la page Révision et paiements](assets/customer-account-order-refund-from-checkout.png){width="700" zoomable="yes"}

5. Si le client change d&#39;avis sur l&#39;utilisation du crédit de magasin, cliquez sur **[!UICONTROL Remove]** dans la section _Résumé de la commande_ .

## Actions de paiement dans l’administrateur

Vous pouvez configurer des actions de paiement pour votre [mode de paiement](../configuration-reference/sales/payment-methods.md) spécifique. Chaque mode de paiement possède un ensemble différent d’actions de paiement.

| Action de paiement | Description |
|--- |---|
| [!UICONTROL Capture Online] | Lorsque la facture est envoyée, le système capture le paiement à partir de la passerelle de paiement tierce. Un utilisateur administrateur peut alors créer un avoir et annuler la facture. |
| [!UICONTROL Capture Offline] | Lorsque la facture est envoyée, le système ne récupère pas le paiement. On suppose que le paiement est capturé directement par le biais de la passerelle et que le paiement ne peut pas être capturé par le biais d’Adobe Commerce. Un utilisateur administrateur peut alors créer un avoir, mais ne peut pas annuler la facture. (Même si la commande a utilisé un paiement en ligne, la facture est essentiellement une facture hors ligne.) |
| [!UICONTROL Not Capture] | Lorsque la facture est envoyée, le système ne récupère pas le paiement. On suppose que le paiement est capturé par Adobe Commerce ultérieurement. Il existe un bouton [!UICONTROL _Capturer_] dans la facture finalisée. Avant de procéder à l&#39;extraction, vous pouvez annuler la facture. Après l’acquisition, vous pouvez créer un avoir et annuler la facture. |

{style="table-layout:auto"}

>[!WARNING]
>
>Sélectionnez l’option [!UICONTROL _Ne pas capturer_] , sauf si vous êtes certain que vous allez capturer le paiement par Adobe Commerce ultérieurement. Vous ne pouvez pas créer d’avoir tant que le paiement n’a pas été capturé à l’aide du bouton [!UICONTROL _Capture_] .
