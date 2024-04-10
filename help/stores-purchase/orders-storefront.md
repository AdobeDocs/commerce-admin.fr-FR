---
title: Gestion des commandes de Storefront
description: Découvrez comment les clients peuvent afficher et gérer leur historique de commandes sur le storefront Commerce.
exl-id: 85d953e6-f5a1-4a5e-a6ef-36b9cf6988bb
feature: Orders, Storefront
source-git-commit: c13a4b730ed70ed4829cc20b13c2723137dcbb3a
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Gestion des commandes de Storefront

Les clients ont accès à toutes leurs commandes à partir de leur compte. Les commandes peuvent être affichées, filtrées, suivies et soumises à nouveau en tant que nouvelles commandes. En fonction du statut de la commande, les clients peuvent imprimer leurs commandes, factures, livraisons et enregistrements de remboursement.

## Filtrer les commandes

{{b2b-feature}}

Votre initial _[!UICONTROL My Orders]_les résultats contiennent également les ordres correspondants d’utilisateurs subordonnés de tous les sites web de l’instance de commerce. Un client associé à un compte d’entreprise peut filtrer la liste des commandes pour rechercher rapidement des enregistrements dans les résultats. Pour afficher les options de filtrage, le client clique sur **[!UICONTROL Filter]**, et clics **[!UICONTROL Close]**pour masquer les filtres.

![Mes commandes](./assets/account-dashboard-my-orders-b2b.png){width="700" zoomable="yes"}

| Filtre | Description |
| ------ | ----------- |
| [!UICONTROL SKU or Product Name] | Saisit un SKU ou un nom de produit. |
| [!UICONTROL Order Number] | Il peut s’agir d’un numéro de commande complet ou partiel. |
| [!UICONTROL Order Status] | Choisit une valeur dans la liste déroulante pour filtrer par statut. |
| [!UICONTROL Invoice Number] | Saisit un numéro de facture complet ou partiel. |
| [!UICONTROL Order Date] | Définit un ou deux champs de date pour le filtrage par date de commande. |
| [!UICONTROL Created by] | Filtre les commandes de la société par leur créateur. |
| [!UICONTROL Order Total] | Définit les valeurs min., max. ou les deux valeurs pour filtrer par ordre de total. |

## Afficher une commande

Un client trouve l’ordre dans la liste et clique dessus **[!UICONTROL View Order]**. Dans l’ordre d’ouverture, il peut effectuer l’une des opérations suivantes :

![Afficher la commande](./assets/customer-account-order-items-ordered.png){width="700" zoomable="yes"}

### Afficher les produits récemment commandés

Le **[!UICONTROL Recent Orders]** Le bloc s’affiche dans la barre latérale et sur la **[!UICONTROL My Account]** page pour les clients qui sont connectés après avoir passé une commande. Il affiche cinq produits du dernier achat.

Le client peut lire les produits dans le panier en les sélectionnant et en cliquant dessus. **[!UICONTROL Add to Cart]**. Ils peuvent également afficher la dernière commande en cliquant sur **[!UICONTROL View all]**, qui redirige vers _[!UICONTROL My Account]_et la **[!UICONTROL Recent Orders]**bloc.

### Imprimer la commande

1. Le client clique **[!UICONTROL Print Order]**.

1. Suit les instructions de la boîte de dialogue Imprimer pour terminer l’impression.

### Imprimer les factures

1. Le **[!UICONTROL Invoices]** le client clique sur l’une des options suivantes :

   - **[!UICONTROL Print All Invoices]**

   - **[!UICONTROL Print Invoice]**

   ![Factures](./assets/customer-account-order-invoices.png){width="700" zoomable="yes"}

1. Utilise la boîte de dialogue Imprimer pour terminer l’impression.

### Imprimer les expéditions

1. Le **[!UICONTROL Order Shipments]** le client clique sur l’une des options suivantes :

   - **[!UICONTROL Print All Shipments]**

   - **[!UICONTROL Print Shipment]**

   ![Imprimer toutes les expéditions](./assets/customer-account-order-shipments.png){width="700" zoomable="yes"}

1. Utilise la boîte de dialogue Imprimer pour terminer l’impression.

### Suivi d’une expédition

1. Le **[!UICONTROL Order Shipments]** , cliquez sur **[!UICONTROL Track this Shipment]**.

   Toutes les informations de suivi disponibles s’affichent dans une fenêtre contextuelle.

1. Une fois prêt, le client clique sur **[!UICONTROL Close Window]**.

### Imprimer les remboursements

1. Le **Remboursements** le client clique sur l’une des options suivantes :

   - **Imprimer tous les remboursements**

   - **Imprimer le remboursement**

   ![Remboursements](./assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

1. Utilise la boîte de dialogue Imprimer pour terminer l’impression.

Les commandes renouvelées sont disponibles pour les clients lorsque [_Autoriser la réorganisation_](reorders-allow.md) L’option de configuration est activée.

Un client peut lancer la fonctionnalité de réorganisation pour une commande spécifique à partir de deux pages :

- Page Mes commandes
- Page Vue Commande

## Réordonner

Le _[!UICONTROL Reorder]_le lien s’affiche dans la liste avec les commandes à proximité de la_[!UICONTROL View]_ lien.

![Lien de réorganisation sur la page Ma commande](./assets/account-dashboard-reorder.png){width="700" zoomable="yes"}

**Cas 1.** Tous les produits de la commande sont disponibles pour la réorganisation

Le client est redirigé vers le panier et tous les produits y sont ajoutés.

**Cas 2.** Certains/tous les produits de la commande ne sont pas disponibles pour la réorganisation

>[!NOTE]
>
>Il est possible de réorganiser `Not Visible Individually` produits.

Le _[!UICONTROL Reorder]_le lien n’apparaît pas sur_[!UICONTROL My Orders]_ et _[!UICONTROL View Order]_pages.

![Page Ma commande](./assets/account-dashboard-reorder-grid.png){width="700" zoomable="yes"}

>[!TIP]
>
>Si le panier n’est pas vide et que le client clique **[!UICONTROL Reorder]** (à partir du [!UICONTROL My Orders] ou [!UICONTROL Order View] page), les produits existants restent dans le panier avec les produits de réorganisation ajoutés.

## Annuler des commandes

L’option Annuler est disponible pour les clients lorsque [_Autoriser Annuler_](cancel-allow.md) L’option de configuration est activée.

Un client peut lancer la fonctionnalité d&#39;annulation pour une commande spécifique à partir de trois pages :

- Page Mes commandes
- Page Vue Commande
- Page Mon compte

Le _[!UICONTROL Cancel Order]_le lien s’affiche à côté de_[!UICONTROL Reorder]_ lien. Si la commande ne peut pas être annulée, le lien n’est pas affiché.

![Annuler le lien sur la page Ma commande](./assets/account-dashboard-cancel.png){width="700" zoomable="yes"}

Pour annuler, le client :

1. Clics **[!UICONTROL Cancel Order]**

1. Fournit un motif d’annulation

   ![Annuler les motifs de commande](./assets/cancel-order-reasons.png){width="700" zoomable="yes"}

   Vous pouvez personnaliser les raisons d’annulation sur le [_Autoriser Annuler_](cancel-allow.md) page.

1. Clics **[!UICONTROL Confirm]**

   ![Annuler sur la page Ma commande](./assets/cancel-order.png){width="700" zoomable="yes"}

   Après l’annulation, les commandes qui étaient dans _[!UICONTROL Pending]_Statut, remplacer par_[!UICONTROL Canceled]_ statut, les commandes qui se trouvaient dans _[!UICONTROL Processing]_Statut, remplacer par_[!UICONTROL Closed]_ statut et un remboursement sera traité.

   Une fois l’annulation terminée, un e-mail est envoyé au client.

   ![E-mail d’annulation de commande](./assets/cancel-order-email.png){width="700" zoomable="yes"}

   Les informations d&#39;annulation sont ajoutées à l&#39;historique des commandes du client. Il apparaît dans les notes de la commande et dans l&#39;onglet Historique des commentaires .

   ![Annuler les notes de commande](./assets/cancel-order-notes.png){width="700" zoomable="yes"}

   ![Annuler l’historique des commentaires](./assets/cancel-order-comments.png){width="700" zoomable="yes"}

   Si, pour une raison quelconque, la commande passe à un statut qui ne peut pas être annulé et que le client n’a pas actualisé la page, le lien permettant d’annuler la commande s’affiche toujours. Cependant, lorsqu’ils tentent d’annuler, un message d’erreur s’affiche.

   ![Message d’erreur relatif à l’annulation de la commande](./assets/cancel-order-error-message.png){width="700" zoomable="yes"}

   Après avoir actualisé la page, vous pouvez constater que la commande était déjà terminée. C’est pourquoi l’annulation n’a pas fonctionné.

   ![Annuler la commande après actualisation](./assets/cancel-order-after-refresh.png){width="700" zoomable="yes"}
