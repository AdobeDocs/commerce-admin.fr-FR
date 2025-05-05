---
title: Expérience de storefront de liste de souhaits
description: Découvrez les outils de gestion des listes de souhaits disponibles pour vos clients sur le storefront.
exl-id: df8cf89a-c897-4a9a-9e84-3bae946683a4
feature: Customers, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 0%

---

# Expérience de storefront de liste de souhaits

Une liste de souhaits est un moyen pratique pour les clients de rappeler des produits qu’ils aiment, mais qu’ils ne sont pas prêts à acheter. Les articles d’une liste de souhaits peuvent être partagés avec d’autres personnes ou ajoutés au panier. Si le client dispose de plusieurs listes de souhaits, le nom de la liste de souhaits actuelle s’affiche en haut de la page. Les clients peuvent gérer leurs listes de souhaits depuis le tableau de bord de leur compte. Les administrateurs de magasin peuvent également aider les clients à gérer leurs listes de souhaits à partir de l’administrateur.

![Exemple de storefront - My Wish List](./assets/storefront-my-wishlist.png){width="700" zoomable="yes"}

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce prend en charge l’utilisation de plusieurs listes de souhaits par compte client.

![Magento Open Source](../assets/open-source.svg) La base de code du Magento Open Source prend en charge l’utilisation d’une seule liste de souhaits par compte client.

## Créer une liste de souhaits

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

Dans le storefront, un client peut créer une liste de souhaits à partir du tableau de bord de son compte, d’une page de produit, d’une page de catalogue et du panier.

### Méthode 1 : depuis un compte client

1. Dans la barre latérale du tableau de bord de leur compte, le client choisit **[!UICONTROL My Wish List]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Create New Wish List]**.

1. Saisissez le nom de la liste de souhaits.

1. Pour permettre à d’autres personnes d’afficher leur liste de souhaits, cochez la case **[!UICONTROL Public Wish List]** .

   >[!NOTE]
   >
   >La principale différence entre `Public` et `Private` listes de souhaits réside dans le fait que les listes de souhaits privées ne sont pas [consultables](wishlist-configuration.md#add-wish-list-search) par le biais de listes de souhaits.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

   ![Créer une liste de souhaits](./assets/account-dashboard-wishlist-create-new.png){width="700" zoomable="yes"}

### Méthode 2 : à partir de la page de catalogue

1. Depuis le storefront, le client accède à la page de catalogue qui contient le produit qu’il souhaite ajouter à une liste de souhaits.

1. Passez la souris sur le produit.

1. Le client clique sur la flèche en regard de l’icône _Ajouter à la liste des souhaits_ et sélectionne l’ **[!UICONTROL Create New Wish List]**.

1. Entrez le nom de la liste de souhaits.

1. Pour permettre à d’autres personnes d’afficher leur liste de souhaits, cochez la case **[!UICONTROL Public Wish List]** .

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

### Méthode 3 : à partir de la page des détails du produit

1. Depuis le storefront, le client accède à la page de détails du produit qu’il souhaite ajouter à une liste de souhaits.

1. Cliquez sur la flèche en regard de **[!UICONTROL Add to Wish List]** et sélectionnez **[!UICONTROL Create New Wish List]**.

1. Entrez le **[!UICONTROL Wish List Name]**.

1. Pour permettre à d’autres personnes d’afficher leur liste de souhaits, cochez la case **[!UICONTROL Public Wish List]** .

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

   ![Créer une liste de souhaits à partir de la page Détails du produit](./assets/account-dashboard-wishlist-create-from-pdp.png){width="700" zoomable="yes"}

### Méthode 4 : à partir du panier

1. Le client ouvre la page **[!UICONTROL Shopping Cart]**.

1. Sous l’élément , cliquez sur la flèche en regard de **[!UICONTROL Move to Wishlist]** et choisissez **[!UICONTROL Create New Wish List]**.

1. Entrez le **[!UICONTROL Wish List Name]**.

1. Pour permettre à d’autres personnes d’afficher leur liste de souhaits, cochez la case **[!UICONTROL Public Wish List]** .

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

![Créer une liste de souhaits à partir de la page Panier](./assets/account-dashboard-wishlist-create-from-cart.png){width="700" zoomable="yes"}

## Mettre à jour la liste des produits

1. Dans la liste des souhaits, le client pointe vers le produit pour afficher les options.

1. Pour ajouter un **[!UICONTROL Comment]** sur le produit, saisissez le texte dans la zone située sous le prix.

   ![Modifier les options](./assets/account-dashboard-wishlist-edit-options.png){width="700" zoomable="yes"}

1. Pour modifier la sélection des options de produit, cliquez sur **[!UICONTROL Edit]** et procédez comme suit :

   - Met à jour les options de la page des détails du produit.
   - Clics **[!UICONTROL Update Wish List]**.

## Ajouter un produit de liste de souhaits au panier

1. Dans la liste de souhaits, le client pointe vers le produit que vous souhaitez ajouter.

1. Met à jour **[!UICONTROL Qty]** et modifiez les autres options si nécessaire.

1. Clics **[!UICONTROL Add to Cart]**.

## Partager la liste des souhaits

1. Le client clique sur **[!UICONTROL Share Wishlist]**.

1. Entrez l’adresse email de chaque personne qui doit recevoir la liste de souhaits, séparée par une virgule.

1. Ajoute un **[!UICONTROL Message]** à inclure dans l’email.

1. Clics **[!UICONTROL Share Wish List]**.

   ![Share Your Wish List](./assets/account-dashboard-wishlist-sharing.png){width="700" zoomable="yes"}

   Le message est envoyé à partir de votre principal [contact de magasin](../getting-started/store-details.md#store-email-addresses) et comprend une miniature de chaque produit, avec des liens vers votre boutique.

   ![ &lbrace;Shared Wish List Email](./assets/account-dashboard-wishlist-sharing-email.png){width="500" zoomable="yes"}

## Modifier les listes de souhaits

Les clients peuvent modifier leur liste de souhaits de plusieurs manières depuis le tableau de bord de leur compte.

### Déplacer des éléments vers une autre liste

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

1. Le client sélectionne la case à cocher de chaque élément à déplacer.

1. Clique sur **[!UICONTROL Move Selected to Wish List]** et effectue l’une des opérations suivantes :

   - Choisit une liste de souhaits existante.
   - Clics **[!UICONTROL Create New Wish List]**.

### Copier des éléments dans une autre liste

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

1. Coche la case de chaque élément à déplacer.

1. Clique sur **[!UICONTROL Copy Selected to Wish List]** et effectue l’une des opérations suivantes :

   - Choisit une liste de souhaits existante.
   - Clics **[!UICONTROL Create New Wish List]**.

## Supprimer une liste de souhaits

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

1. Le client ouvre la liste des souhaits à supprimer.

1. Clics **[!UICONTROL Delete Wish List]**.

1. Lorsque vous êtes invité à confirmer l’opération, cliquez sur **[!UICONTROL OK]**.

>[!IMPORTANT]
>
>Cette action ne peut pas être annulée.

## Transfert des éléments de la liste de souhaits vers le panier

Pour transférer tous les éléments de la liste de souhaits dans le panier, le client clique sur **[!UICONTROL Add All to Cart]**.

Pour ajouter un seul élément, le client effectue les opérations suivantes :

1. Pointez sur l’élément et entrez le **[!UICONTROL Qty]** qu’il souhaite ajouter au panier.

1. Clics **[!UICONTROL Add to Cart]**.

## Trouver une liste de souhaits client

Si le [widget de recherche de liste de souhaits](wishlist-configuration.md#add-wish-list-search) inclus dans vos pages de magasin, les clients peuvent effectuer une recherche par nom ou adresse électronique du propriétaire de la liste de souhaits.

1. Dans le widget de recherche de la liste de souhaits, le client sélectionne une option de recherche.

1. Entrez le nom ou l’adresse électronique du propriétaire de la liste de souhaits et cliquez sur **[!UICONTROL Search]**.

   La page _Recherche de liste de souhaits_ s’ouvre et toutes les listes de souhaits correspondantes sont affichées dans la section des résultats de recherche.

   >[!NOTE]
   >
   >Seules les listes noires publiques s’affichent dans les résultats de recherche : les listes noires privées des clients ne sont pas visibles par le public.

1. Pour afficher la liste des éléments de liste de souhaits, cliquez sur **[!UICONTROL View]**.

   Le nom du propriétaire et la date de la dernière mise à jour sont affichés pour chaque liste de souhaits.

1. Pour ajouter un produit à son panier, le client sélectionne la case à cocher située sous le produit et clique sur **[!UICONTROL Add to Cart]**.

   Vous pouvez également ajouter à votre compte des éléments de la liste de souhaits d’un autre client.
