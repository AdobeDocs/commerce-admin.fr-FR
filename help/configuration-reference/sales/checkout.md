---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Checkout]'
description: Examinez les paramètres de configuration sur le [!UICONTROL Sales] &gt; [!UICONTROL Checkout] de l’Administration de Commerce.
exl-id: a912beb0-37a9-407b-83bd-dc6cd0554dc4
feature: Configuration, Checkout
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Checkout]

{{config}}

## [!UICONTROL Checkout Options]

![Options de passage en caisse](./assets/checkout-checkout-options.png)<!-- zoom -->

<!--[Checkout Options](https://docs.magento.com/user-guide/sales/checkout-options.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|------------------------------------------------------------------|--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Guest Checkout Login] | Affichage de la boutique | Activez ce paramètre pour permettre aux utilisateurs non authentifiés (storefront et API) de demander si une adresse e-mail est déjà associée à un compte client. Vous pouvez l’utiliser pour améliorer le workflow de passage en caisse pour les invités en affichant une invite de connexion si l’adresse e-mail saisie est déjà enregistrée sur un compte client, mais au prix de la divulgation d’informations à des utilisateurs non authentifiés.  Options : `Yes` / `No` |
| [!UICONTROL Enable Onepage Checkout] | Affichage de la boutique | Détermine si [Passage en caisse d’une page](../../stores-purchase/checkout-process.md#checkout-options) est le format de passage en caisse par défaut. Options : `Yes` / `No` |
| [!UICONTROL Allow Guest Checkout] | Affichage de la boutique | Détermine si les invités peuvent passer par [passage en caisse sans enregistrement](../../stores-purchase/checkout-guest.md) pour un compte dans votre boutique. Options : `Yes` / `No` |
| [!UICONTROL Enable Terms and Conditions] | Affichage de la boutique | Détermine si les clients doivent accepter le [Termes et conditions](../../stores-purchase/terms-and-conditions.md) de la vente avant d&#39;effectuer un achat. Options : `Yes` / `No` |
| [!UICONTROL Display Billing Address On] | Affichage de la boutique | Détermine l’emplacement de l’adresse de facturation lors du passage en caisse. Options : `Payment Method` / `Payment Page` |
| [!UICONTROL Maximum Number of Items to Display in Order Summary] | Affichage de la boutique | Détermine le nombre maximal d’éléments pouvant apparaître dans le _Récapitulatif de la commande_ lors du passage en caisse. La valeur par défaut est . `10`. |
| [!UICONTROL Enable Address Search] | Site internet | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine si les clients peuvent utiliser [recherche d&#39;adresses](../../stores-purchase/checkout-address-search.md) pour les étapes Expédition et Révision et paiements. Lorsque cette option est activée, utilisez Limite du nombre d’adresses client pour définir le nombre d’adresses enregistrées requises pour activer cette fonctionnalité lors du passage en caisse. Options : `Yes` / `No` |
| Limite du nombre d&#39;adresses client | Site internet | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Lorsque la recherche d’adresses est activée, détermine le nombre d’adresses enregistrées requises pour activer cette fonctionnalité lors du passage en caisse. Lorsque le nombre d’adresses enregistrées du client atteint ou dépasse ce nombre, seule l’adresse par défaut est rendue sur le _Expédition_ et _Révision et paiements_ étapes. Le client peut utiliser une fonction de recherche pour modifier l’adresse sélectionnée. La valeur par défaut est . `10`. |

{style="table-layout:auto"}

## [!UICONTROL Shopping Cart]

![Panier](./assets/checkout-shopping-cart.png)<!-- zoom -->

<!--[Shopping Cart](https://docs.magento.com/user-guide/sales/cart-configuration.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Quote Lifetime (days)] | Site internet | Détermine l’ [durée de vie d&#39;un prix coté](../../stores-purchase/cart-configuration.md#quote-lifetime), en jours. |
| [!UICONTROL After Adding a Product Redirect to Shopping Cart] | Affichage de la boutique | Détermine si le paramètre [la page panier s’affiche](../../stores-purchase/cart-configuration.md#redirect-to-cart) immédiatement après l’ajout d’un produit au panier. Options : `Yes` / `No` |
| [!UICONTROL Number of Items to Display Pager] | Affichage de la boutique | Détermine le nombre d’articles dans le panier avant le déclenchement du pager. Valeur par défaut : `20` |
| [!UICONTROL Show Cross-sell Items in the Shopping Cart] | Affichage de la boutique | Indique si [articles de vente croisée](../../catalog/related-products-up-sells-cross-sells.md#cross-sells) sont affichées dans le panier, fournissant des options de vente supplémentaires aux clients. Options : `Yes` (par défaut) / `No` |
| [!UICONTROL Grouped Product Image] | Affichage de la boutique | Détermine l’ [vignette](../../stores-purchase/cart-configuration.md#cart-thumbnails) image affichée pour une [produit groupé](../../catalog/product-create-grouped.md) dans le panier. Options : `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Configurable Product Image] | Affichage de la boutique | Détermine l’ [vignette](../../stores-purchase/cart-configuration.md#cart-thumbnails) image qui s’affiche pour un produit configurable dans le panier. Options : `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Preview Quote Lifetime (minutes)] | Affichage de la boutique | Détermine l&#39;âge maximal du devis en minutes lors de la prévisualisation à partir du panier. |
| [!UICONTROL Enable Clear Shopping Cart] | Site internet | Détermine si le panier affiche l’option permettant aux utilisateurs d’effacer le contenu du panier en une seule action. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL My Cart Link]

![Lien Mon panier](./assets/checkout-my-cart-link.png)<!-- zoom -->

<!-- [*My Cart Link*](https://docs.magento.com/user-guide/sales/mini-cart.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Display Cart Summary] | Site internet | Détermine la valeur qui apparaît entre parenthèses après le lien Mon panier . Options : `Display number of items in cart` / `Display item quantities` |

{style="table-layout:auto"}

## Mini panier

![Mini panier](./assets/checkout-mini-cart.png)<!-- zoom -->

<!-- [*Mini Cart*](https://docs.magento.com/user-guide/sales/mini-cart.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Display Mini Cart] | Affichage de la boutique | Détermine si le mini panier s’affiche sur les pages du magasin lorsque l’utilisateur clique sur l’icône du panier dans l’en-tête. L&#39;affichage du mini panier dépend du thème. Options : `Yes` / `No` |
| [!UICONTROL Number of Items to Display Scrollbar] | Affichage de la boutique | Détermine le nombre d’éléments pouvant apparaître dans le mini panier avant le déclenchement de la barre de défilement. Valeur par défaut : `5` |
| [!UICONTROL Maximum Number of Items to Display] | Affichage de la boutique | Détermine le nombre maximal d’articles pouvant apparaître dans le mini panier. Valeur par défaut : `10` |

{style="table-layout:auto"}

## [!UICONTROL Payment Failed Emails]

![E-mails d’échec de paiement](./assets/checkout-payment-failed-emails.png)<!-- zoom -->

<!-- [*Payment Failed Emails*](https://docs.magento.com/user-guide/sales/checkout-payment-failed-emails.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Payment Failed Email Receiver] | Affichage de la boutique | Identifie le contact du magasin qui reçoit les e-mails d’échec de paiement. Récepteur par défaut : `General Contact` |
| [!UICONTROL Payment Failed Email Sender] | Affichage de la boutique | Identifie le contact du magasin qui apparaît comme l’expéditeur des e-mails d’échec de paiement. Expéditeur par défaut : `General Contact` |
| [!UICONTROL Payment Failed Template] | Affichage de la boutique | Identifie le modèle utilisé pour les e-mails d’échec de paiement. Modèle par défaut : `Payment Failed` |
| [!UICONTROL Send Payment Failed Copy To] | Affichage de la boutique | Fournit l&#39;adresse e-mail de toute personne souhaitant recevoir une copie d&#39;un e-mail d&#39;échec de paiement. Séparez les adresses multiples par une virgule. |
| [!UICONTROL Send Payment Failed Copy Method] | Affichage de la boutique | Indique la méthode e-mail utilisée pour envoyer la copie. Options : <br />**`Bcc`**- Envoie une copie de courtoisie invisible en incluant le destinataire dans l’en-tête du même e-mail envoyé au client. Le destinataire en Cci n’est pas visible pour le client.<br />**`Separate Email`** - Envoie la copie sous forme d’e-mail distinct. |

{style="table-layout:auto"}
