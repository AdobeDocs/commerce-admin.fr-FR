---
title: Remboursements dans le tableau de bord du compte client
description: Les clients du magasin peuvent afficher les informations de remboursement associées à la commande dans le tableau de bord de leur compte.
exl-id: 8fd6d4e7-74ba-4f39-9a19-7c77ee63b913
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/ggaeec6NA2K12-eHl7ESC10nU2u11ihbaxaPlbNAE9I
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 485
ht-degree: 0%

---

# Remboursements dans le tableau de bord du compte client

{{ee-feature}}

Si un remboursement a été émis pour une commande, les clients peuvent consulter les informations de remboursement associées à la commande dans leur tableau de bord de compte. Si vous avez activé l’option [!UICONTROL _Afficher l’historique de crédit de la boutique aux clients_] pour [Configuration du crédit de la boutique](../customers/credit-configure.md), les clients peuvent également accéder à leur historique de [crédit de la boutique](../customers/store-credit.md).

## Afficher un remboursement sur le storefront

1. À partir du storefront, le client se connecte à son compte.

1. Localise leur commande à l’aide de l’une des méthodes suivantes :

   * Recherche de la commande dans la liste des **Commandes récentes** et clic sur **[!UICONTROL View]**.
   * Dans le panneau de gauche, choisissez **[!UICONTROL My Orders]**. Recherchez ensuite l’ordre dans la liste, puis cliquez sur **[!UICONTROL View]**.

1. Le client clique sur l&#39;onglet **[!UICONTROL Refunds]** pour consulter les détails du remboursement.

   ![Détails du remboursement sur le storefront](assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

## Afficher le solde et l&#39;historique du crédit de la boutique sur le storefront

Méthode 1 : **à partir du tableau de bord du compte client**

1. À partir du storefront, le client se connecte au compte .

1. Si le remboursement a été appliqué au crédit de la boutique, sélectionne **[!UICONTROL Store Credit]** dans le panneau de gauche.

1. Le montant remboursé à leur crédit de magasin apparaît dans la liste avec la date et l’heure de l’action.

   ![Montant remboursé pour stocker le crédit](assets/customer-account-store-credit.png){width="700" zoomable="yes"}

   >[!INFO]
   >
   >La page Crédit de la boutique fournit également un lien permettant au client d’utiliser une [carte cadeau](../stores-purchase/product-gift-card-workflow.md#check-status-and-balance-of-the-gift-card).

Méthode 2 : **à partir de la page _Révision et paiements_**

1. Le client ajoute un produit au panier.

2. Accède à la page _Passage en caisse_.

3. Passe l’étape **[!UICONTROL Shipping]**.

4. Si le crédit de la boutique est disponible, le client clique sur **[!UICONTROL Use Store Credit]**.

   ![Stocker le crédit de la page Vérification et paiements](assets/customer-account-order-refund-from-checkout.png){width="700" zoomable="yes"}

5. Si le client change d&#39;avis au sujet de l&#39;utilisation du crédit de la boutique, clique sur **[!UICONTROL Remove]** dans la section _Résumé de la commande_.

## Actions de paiement dans l’administrateur

Vous pouvez configurer des actions de paiement pour votre [Mode de paiement](../configuration-reference/sales/payment-methods.md) spécifique. Chaque mode de paiement comporte un ensemble différent d&#39;actions de paiement.

| Action de paiement | Description |
|--- |---|
| [!UICONTROL Capture Online] | Lorsque la facture est soumise, le système capture le paiement à partir de la passerelle de paiement tierce. Un utilisateur administrateur peut ensuite créer un avoir et annuler la facture. |
| [!UICONTROL Capture Offline] | Lorsque la facture est soumise, le système ne capture pas le paiement. On suppose que le paiement est capturé directement par le biais de la passerelle et qu’il ne peut pas être capturé via Adobe Commerce. Un utilisateur administrateur peut ensuite créer un avoir, mais ne peut pas annuler la facture. (Même si la commande a utilisé un paiement en ligne, la facture est essentiellement une facture hors ligne.) |
| [!UICONTROL Not Capture] | Lorsque la facture est soumise, le système ne capture pas le paiement. On suppose que le paiement est capturé ultérieurement via Adobe Commerce. La facture remplie contient un bouton [!UICONTROL _Capturer_]. Avant la capture, vous pouvez annuler la facture. Après la capture, vous pouvez créer un avoir et annuler la facture. |

{style="table-layout:auto"}

>[!WARNING]
>
>Sélectionnez l’option [!UICONTROL _Pas de capture_] sauf si vous êtes certain de capturer le paiement via Adobe Commerce ultérieurement. Vous ne pouvez pas créer d&#39;avoir tant que le paiement n&#39;a pas été saisi à l&#39;aide du bouton [!UICONTROL _Capturer_].
