---
title: Mise à jour d’un profil client
description: Accédez aux informations sur l’activité du client, telles que la date de la dernière connexion ou déconnexion du client à son compte, et mettez à jour le profil client.
exl-id: 8e805095-76b2-4237-98dc-aa32f15f2637
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 0%

---

# Mise à jour d’un profil client

Le panneau de gauche de la page _[!UICONTROL Customer Information]_&#x200B;contient des informations sur l’activité des clients, les adresses, les statistiques des commandes, les commandes récentes, le contenu des paniers, les avis de produits et les abonnements aux newsletters.

![Profil client](assets/cust-profile.png){width="700" zoomable="yes"}

## Modification d’un compte client

Méthode 1 : **_Modification rapide_**

1. Dans la première colonne, cochez la case du compte client à modifier.

1. Définissez la colonne **[!UICONTROL Actions]** sur `Edit`.

   >[!INFO]
   >
   >La valeur de chaque valeur qui peut être mise à jour apparaît dans une zone de texte. Seules certaines valeurs de l’enregistrement client sélectionné peuvent être modifiées à partir de la grille.

   ![&#x200B; Modification rapide &#x200B;](assets/customers-grid-quick-edit.png){width="700" zoomable="yes"}

1. Mettez à jour l’une des valeurs suivantes, si nécessaire :

   * **[!UICONTROL Email]**
   * **[!UICONTROL Web Site]**
   * **[!UICONTROL Tax/VAT Number]**
   * **[!UICONTROL Gender]**

1. Cliquez sur **[!UICONTROL Save]**.

Méthode 2 : **_Modification complète_**

1. Dans la grille, recherchez l’enregistrement du client à modifier.

1. Dans la colonne _Actions_ tout à droite, cliquez sur **[!UICONTROL Edit]**.

1. Apportez les modifications nécessaires aux informations de la société.

   >[!INFO]
   >
   >Pour en savoir plus, voir [Mettre à jour un profil client](../customers/update-account.md).

1. Cliquez ensuite sur **[!UICONTROL Save Customer]**.

>[!INFO]
>
>Si vous souhaitez annuler toutes les modifications avant d’enregistrer, cliquez sur **[!UICONTROL Reset]** dans la barre de boutons supérieure pour rétablir toutes les modifications dans la dernière version enregistrée.

## Informations sur le client

### [!UICONTROL Customer View]

L’onglet _Affichage du client_ répertorie les informations sur le client, notamment les **[!UICONTROL Personal Information]**, les **[!UICONTROL Reward Points Balance]** et les **[!UICONTROL Store Credit Balance]**.

### [!UICONTROL Account Information]

L’onglet [&#x200B; Informations du compte &#x200B;](../customers/account-dashboard-account-information.md) fournit des informations détaillées sur le client. Un utilisateur administrateur peut alors modifier ses informations personnelles, son adresse e-mail, l’assistance pour les achats à distance, sa date de naissance et joindre le client à un site web ou à une société.

### [!UICONTROL Addresses]

L’onglet [Adresses](../customers/account-dashboard-address-book.md) contient les adresses de facturation et d’expédition par défaut du client, ainsi que toutes les adresses supplémentaires qu’il utilise fréquemment.

### [!UICONTROL Orders]

La grille [Commandes](../stores-purchase/orders.md) contient une liste de toutes les commandes client actuelles. L’administrateur peut suivre leur progression.

### [!UICONTROL Returns]

{{ee-feature}}

L’onglet [Renvoie](../stores-purchase/returns.md) répertorie les demandes client actuellement renvoyées.

### [!UICONTROL Shopping cart]

L’onglet [panier](../stores-purchase/cart.md) affiche les produits qui se trouvent actuellement dans le panier, mais pour une raison quelconque, l’achat n’a pas été effectué.

### [!UICONTROL Wish List]

Une [liste de souhaits](../stores-purchase/wishlists.md) affiche une liste de produits qu’un client peut transférer ultérieurement au panier.

### [!UICONTROL Gift Registry]

{{ee-feature}}

La section [Registre des cadeaux](../merchandising-promotions/gift-registry-storefront.md) répertorie les registres des cadeaux actuels du client et l’événement associé.


### [!UICONTROL Store Credit]

{{ee-feature}}

L’onglet [Crédit de la boutique](../customers/store-credit.md) affiche un montant restauré sur un compte client. L’administrateur peut gérer cette valeur.

### [!UICONTROL Newsletter]

L’onglet [Newsletter](../merchandising-promotions/newsletters.md) affiche tous les e-mails envoyés au client actuel.

### [!UICONTROL Billing Agreements]

L’onglet [Contrats de facturation](../stores-purchase/paypal-billing-agreements.md) répertorie tous les contrats de facturation PayPal entre le magasin et le client.

### [!UICONTROL Product Reviews]

L’onglet [Examens des produits](../catalog/settings-advanced-product-reviews.md) affiche tous les avis soumis par ce client.

### [!UICONTROL Reward Points]

{{ee-feature}}

La section [Points de récompense](../merchandising-promotions/rewards-loyalty.md) indique le solde actuel des points de récompense du client. Un utilisateur administrateur peut gérer cette valeur.

## Barre de boutons

| Bouton | Description |
|----------|--------------|
| **[!UICONTROL Back]** | Retourne à la page Clients sans enregistrer les modifications. |
| **[!UICONTROL Login as Customer]** | Permet au commerçant de se connecter en tant que client. |
| **[!UICONTROL Delete Customer]** | Supprime le compte client. |
| **[!UICONTROL Reset]** | Réinitialise toutes les modifications non enregistrées dans le formulaire client à leurs valeurs précédentes. |
| **[!UICONTROL Create Order]** | [Crée une commande](../stores-purchase/customer-account-create-order.md) associée au compte client. |
| **[!UICONTROL Reset Password]** | Réinitialise le mot de passe du client. |
| **[!UICONTROL Force Sign-In]** | Efface les jetons associés au mot de passe du client et fournit à l’administrateur l’accès au compte. |
| **[!UICONTROL Manage Shopping Cart]** | Permet d’accéder au panier d’un client. |
| **[!UICONTROL Save and Continue Edit]** | Enregistre les modifications et maintient le compte client ouvert. |
| **[!UICONTROL Save Customer]** | Enregistre les modifications et ferme le compte client. |

{style="table-layout:auto"}
