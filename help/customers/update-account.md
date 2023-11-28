---
title: Mise à jour d’un profil client
description: Accédez aux informations sur l’activité du client, telles que le moment où le client s’est connecté ou s’est déconnecté pour la dernière fois de son compte, et mettez à jour son profil.
exl-id: 8e805095-76b2-4237-98dc-aa32f15f2637
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Mise à jour d’un profil client

Le panneau de gauche de _[!UICONTROL Customer Information]_Cette page contient des informations sur l’activité des clients, les adresses, les statistiques de commandes, les commandes récentes, le contenu du panier, les avis sur les produits et les abonnements à des newsletters.

![Profil client](assets/cust-profile.png){width="700" zoomable="yes"}

## Modification d’un compte client

Méthode 1 : **_Modification rapide_**

1. Dans la première colonne, cochez la case du compte client à éditer.

1. Définissez la variable **[!UICONTROL Actions]** colonne à `Edit`.

   >[!INFO]
   >
   >La valeur de chaque valeur pouvant être mise à jour apparaît dans une zone de texte. Seules certaines valeurs de l’enregistrement client sélectionné peuvent être modifiées à partir de la grille.

   ![Modification rapide](assets/customers-grid-quick-edit.png){width="700" zoomable="yes"}

1. Mettez à jour l’une des valeurs suivantes, si nécessaire :

   * **[!UICONTROL Email]**
   * **[!UICONTROL Web Site]**
   * **[!UICONTROL Tax/VAT Number]**
   * **[!UICONTROL Gender]**

1. Cliquez sur **[!UICONTROL Save]**.

Méthode 2 : **_Modification complète_**

1. Dans la grille, recherchez l’enregistrement du client à modifier.

1. Dans le _Actions_ à l’extrême droite, cliquez sur **[!UICONTROL Edit]**.

1. Apportez les modifications nécessaires aux informations de l’entreprise.

   >[!INFO]
   >
   >Pour en savoir plus, voir [Mise à jour d’un profil client](../customers/update-account.md).

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Customer]**.

>[!INFO]
>
>Si vous souhaitez annuler toutes les modifications avant de les enregistrer, cliquez sur **[!UICONTROL Reset]** dans la barre de boutons supérieure pour revenir à toutes les modifications apportées à la dernière version enregistrée.

## Informations sur le client

### [!UICONTROL Customer View]

La variable _Vue du client_ répertorie les informations sur le client, inclut **[!UICONTROL Personal Information]**, **[!UICONTROL Reward Points Balance]**, et **[!UICONTROL Store Credit Balance]**.

### [!UICONTROL Account Information]

La variable [Informations du compte](../customers/account-dashboard-account-information.md) Cet onglet fournit des informations détaillées sur le client, où un utilisateur administrateur peut modifier des informations personnelles, des e-mails, de l’aide aux achats à distance, la date de naissance et joindre le client à un site web ou à une entreprise.

### [!UICONTROL Addresses]

La variable [Adresses](../customers/account-dashboard-address-book.md) Cet onglet contient les adresses de facturation et de livraison par défaut du client, ainsi que toute adresse supplémentaire qu’il utilise fréquemment.

### [!UICONTROL Orders]

La variable [Commandes](../stores-purchase/orders.md) contient une liste de toutes les commandes client actuelles, l’administrateur peut suivre leur progression.

### [!UICONTROL Returns]

{{ee-feature}}

La variable [Renvoie](../stores-purchase/returns.md) répertorie les demandes client actuellement renvoyées.

### [!UICONTROL Shopping cart]

La variable [panier](../stores-purchase/cart.md) affiche les produits qui se trouvent actuellement dans le panier, mais pour une raison quelconque, l’achat n’a pas été effectué.

### [!UICONTROL Wish List]

A [liste de souhaits](../stores-purchase/wishlists.md) affiche une liste des produits qu’un client peut transférer ultérieurement au panier.

### [!UICONTROL Gift Registry]

{{ee-feature}}

La variable [Registre des cadeaux](../merchandising-promotions/gift-registry-storefront.md) Cette section répertorie les registres de cadeaux actuels du client et l’événement associé.


### [!UICONTROL Store Credit]

{{ee-feature}}

La variable [Crédit de la boutique](../customers/store-credit.md) affiche un montant restauré dans un compte client, l’administrateur peut gérer cette valeur.

### [!UICONTROL Newsletter]

La variable [Newsletter](../merchandising-promotions/newsletters.md) affiche tous les emails envoyés au client actuel.

### [!UICONTROL Billing Agreements]

La variable [Accords de facturation](../stores-purchase/paypal-billing-agreements.md) répertorie tous les contrats de facturation PayPal entre le magasin et le client.

### [!UICONTROL Product Reviews]

La variable [Révisions de produit](../catalog/settings-advanced-product-reviews.md) affiche toutes les révisions soumises par ce client.

### [!UICONTROL Reward Points]

{{ee-feature}}

La variable [Points de récompense](../merchandising-promotions/rewards-loyalty.md) présente le solde actuel des points de récompense du client. Un utilisateur administrateur peut gérer cette valeur.

## Barre de boutons

| Bouton | Description |
|----------|--------------|
| **[!UICONTROL Back]** | Renvoie la page Clients sans enregistrer les modifications. |
| **[!UICONTROL Login as Customer]** | Permet au commerçant de se connecter en tant que client. |
| **[!UICONTROL Delete Customer]** | Supprime le compte client. |
| **[!UICONTROL Reset]** | Réinitialise les modifications non enregistrées du formulaire client à leurs valeurs précédentes. |
| **[!UICONTROL Create Order]** | [Crée une commande](../stores-purchase/customer-account-create-order.md) qui est associé au compte client. |
| **[!UICONTROL Reset Password]** | Réinitialise le mot de passe du client. |
| **[!UICONTROL Force Sign-In]** | Efface les jetons associés au mot de passe du client et permet à l’administrateur d’accéder au compte. |
| **[!UICONTROL Manage Shopping Cart]** | Permet d’accéder au panier d’achat d’un client. |
| **[!UICONTROL Save and Continue Edit]** | Enregistre les modifications et conserve le compte client ouvert. |
| **[!UICONTROL Save Customer]** | Enregistre les modifications et ferme le compte client. |

{style="table-layout:auto"}
