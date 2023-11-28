---
title: Gestion des commandes du storefront
description: Découvrez comment les clients peuvent afficher et gérer leur historique de commandes sur le storefront Commerce.
exl-id: 85d953e6-f5a1-4a5e-a6ef-36b9cf6988bb
feature: Orders, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# Gestion des commandes du storefront

Les clients ont accès à toutes leurs commandes depuis leur compte . Les commandes peuvent être affichées, filtrées, suivies et soumises à nouveau en tant que nouvelles commandes. Selon l’état de la commande, les clients peuvent imprimer leurs commandes, factures, envois et enregistrements de remboursement.

## Filtrage des commandes

{{b2b-feature}}

Votre initial _[!UICONTROL My Orders]_Les résultats contiennent également les commandes correspondantes d’utilisateurs subordonnés de tous les sites web de l’instance de commerce. Un client associé à un compte d’entreprise peut filtrer la liste des commandes afin de trouver rapidement des enregistrements dans les résultats. Pour afficher les options de filtrage, le client clique sur **[!UICONTROL Filter]**, et clics **[!UICONTROL Close]**pour masquer les filtres.

![Mes commandes](./assets/account-dashboard-my-orders-b2b.png){width="700" zoomable="yes"}

| Filtrer | Description |
| ------ | ----------- |
| [!UICONTROL SKU or Product Name] | Entrez un SKU ou un nom de produit. |
| [!UICONTROL Order Number] | Il peut s’agir d’un numéro de commande complet ou partiel. |
| [!UICONTROL Order Status] | Choisit une valeur dans la liste déroulante pour filtrer par état. |
| [!UICONTROL Invoice Number] | Saisissez un numéro de facture complet ou partiel. |
| [!UICONTROL Order Date] | Définit un ou les deux champs de date à filtrer par date de commande. |
| [!UICONTROL Created by] | Filtre les commandes de la société par le créateur de commandes. |
| [!UICONTROL Order Total] | Définit les valeurs min, max ou les deux valeurs à filtrer par total de commande. |

## Afficher une commande

Un client trouve la commande dans la liste et clique sur **[!UICONTROL View Order]**. Dans l’ordre d’ouverture, ils peuvent effectuer l’une des opérations suivantes :

![Afficher la commande](./assets/customer-account-order-items-ordered.png){width="700" zoomable="yes"}

### Afficher les produits récemment commandés

La variable **[!UICONTROL Recent Orders]** s’affiche dans la barre latérale et sur la **[!UICONTROL My Account]** pour les clients connectés après avoir passé une commande. Il affiche cinq produits du dernier achat.

Le client peut lire les produits dans le panier en sélectionnant les produits et en cliquant sur **[!UICONTROL Add to Cart]**. Ils peuvent également afficher la dernière commande en cliquant sur **[!UICONTROL View all]**, qui redirige vers le _[!UICONTROL My Account]_et la **[!UICONTROL Recent Orders]**bloque.

### Ordre d’impression

1. Le client clique **[!UICONTROL Print Order]**.

1. Suivez les instructions de la boîte de dialogue Imprimer pour terminer l’impression.

### Imprimer les factures

1. Sur le **[!UICONTROL Invoices]** , le client clique sur l’une des options suivantes :

   - **[!UICONTROL Print All Invoices]**

   - **[!UICONTROL Print Invoice]**

   ![Facturations](./assets/customer-account-order-invoices.png){width="700" zoomable="yes"}

1. Utilise la boîte de dialogue Imprimer pour terminer l’impression.

### Imprimer les envois

1. Sur le **[!UICONTROL Order Shipments]** , le client clique sur l’une des options suivantes :

   - **[!UICONTROL Print All Shipments]**

   - **[!UICONTROL Print Shipment]**

   ![Imprimer tous les envois](./assets/customer-account-order-shipments.png){width="700" zoomable="yes"}

1. Utilise la boîte de dialogue Imprimer pour terminer l’impression.

### Tracker une diffusion

1. Sur le **[!UICONTROL Order Shipments]** , cliquez sur **[!UICONTROL Track this Shipment]**.

   Toutes les informations de suivi disponibles s’affichent dans une fenêtre contextuelle.

1. Une fois prêt, le client clique **[!UICONTROL Close Window]**.

### Rôles d’impression

1. Sur le **Remboursement** , le client clique sur l’une des options suivantes :

   - **Imprimer tous les remboursements**

   - **Imprimer le remboursement**

   ![Remboursement](./assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

1. Utilise la boîte de dialogue Imprimer pour terminer l’impression.

Les réordres sont disponibles pour les clients lorsque la variable [_Autoriser la réorganisation_](reorders-allow.md) l’option de configuration est activée.

Un client peut lancer la fonctionnalité de réorganisation d’une commande spécifique à partir de deux pages :

- Ma page Commandes
- Page Afficher la commande

## Révisions

La variable _[!UICONTROL Reorder]_Le lien s’affiche dans la liste avec les commandes proches de la balise_[!UICONTROL View]_ lien.

![Lien de réorganisation sur la page Ma commande](./assets/account-dashboard-reorder.png){width="700" zoomable="yes"}

**Cas 1.** Tous les produits de la commande peuvent être réorganisés.

Le client est redirigé vers le panier et tous les produits sont ajoutés au panier.

**Cas 2.** Certains/tous les produits de la commande ne peuvent pas être réorganisés.

>[!NOTE]
>
>Il est possible de réorganiser `Not Visible Individually` produits.

La variable _[!UICONTROL Reorder]_n’apparaît pas sur le lien_[!UICONTROL My Orders]_ et _[!UICONTROL View Order]_pages.

![Ma page Commande](./assets/account-dashboard-reorder-grid.png){width="700" zoomable="yes"}

>[!TIP]
>
>Si le panier n’est pas vide et que le client clique **[!UICONTROL Reorder]** (de la fonction [!UICONTROL My Orders] ou [!UICONTROL Order View] ), les produits existants restent dans le panier avec les produits de réorganisation ajoutés.
