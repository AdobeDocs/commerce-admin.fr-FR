---
title: '[!UICONTROL Sales] > [!UICONTROL Checkout]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Checkout] de [!UICONTROL Sales] &gt ; de l’administrateur Commerce.
exl-id: a912beb0-37a9-407b-83bd-dc6cd0554dc4
feature: Configuration, Checkout
TQID: https://experienceleague.adobe.com/clTASsRXJy-IJagl7oAV3LuviEosmuIi4rYEjMpjbIE
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 648
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Checkout]

{{config}}

## [!UICONTROL Checkout Options]

![Options de paiement](./assets/checkout-checkout-options.png)<!-- zoom -->

<!--[Checkout Options](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/checkout/checkout-process#checkout-options) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|------------------------------------------------------------------|--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Guest Checkout Login] | Affichage de la boutique | Activez ce paramètre pour permettre aux utilisateurs non authentifiés (storefront et API) de demander si une adresse e-mail est déjà associée à un compte client. Vous pouvez l’utiliser pour améliorer le workflow de passage en caisse pour les invités en affichant une invite de connexion si l’adresse e-mail saisie est déjà enregistrée dans un compte client, mais au prix de la divulgation d’informations à des utilisateurs non authentifiés.  Options : `Yes` / `No` |
| [!UICONTROL Enable Onepage Checkout] | Affichage de la boutique | Détermine si [ Extraction d’une page ](../../stores-purchase/checkout-process.md#checkout-options) est le format d’extraction par défaut. Options : `Yes` / `No` |
| [!UICONTROL Allow Guest Checkout] | Affichage de la boutique | Détermine si les invités peuvent passer en caisse [sans s’enregistrer](../../stores-purchase/checkout-guest.md) pour un compte dans votre boutique. Options : `Yes` / `No` |
| [!UICONTROL Enable Terms and Conditions] | Affichage de la boutique | Détermine si les clients sont tenus d&#39;accepter les [conditions générales](../../stores-purchase/terms-and-conditions.md) de la vente avant d&#39;effectuer un achat. Options : `Yes` / `No` |
| [!UICONTROL Display Billing Address On] | Affichage de la boutique | Détermine l’emplacement de l’adresse de facturation lors du passage en caisse. Options : `Payment Method` / `Payment Page` |
| [!UICONTROL Maximum Number of Items to Display in Order Summary] | Affichage de la boutique | Détermine le nombre maximal d&#39;éléments pouvant apparaître dans le _récapitulatif de la commande_ lors du passage en caisse. La valeur par défaut est `10`. |
| [!UICONTROL Enable Address Search] | Site internet | ![](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine si les clients peuvent utiliser la fonctionnalité [recherche d’adresses](../../stores-purchase/checkout-address-search.md) pour les étapes Expédition et Révision et paiements. Lorsque cette option est activée, utilisez Limite du nombre d’adresses client pour définir le nombre d’adresses enregistrées requises pour activer cette fonctionnalité lors du passage en caisse. Options : `Yes` / `No` |
| Limite du nombre d&#39;adresses client | Site internet | ![](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Lorsque la recherche d’adresses est activée, détermine le nombre d’adresses enregistrées requises pour activer cette fonctionnalité lors du passage en caisse. Lorsque le nombre d&#39;adresses enregistrées du client atteint ou dépasse ce nombre, seule l&#39;adresse par défaut est rendue aux étapes _Expédition_ et _Révision et paiements_. Le client peut utiliser une fonction de recherche pour modifier l’adresse sélectionnée. La valeur par défaut est `10`. |

{style="table-layout:auto"}

## [!UICONTROL Shopping Cart]

![Panier](./assets/checkout-shopping-cart.png)<!-- zoom -->

<!--[Shopping Cart](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Quote Lifetime (days)] | Site internet | Détermine la [durée de vie d&#39;un prix proposé](../../stores-purchase/cart-configuration.md#quote-lifetime) en jours. |
| [!UICONTROL After Adding a Product Redirect to Shopping Cart] | Affichage de la boutique | Détermine si la page [panier](../../stores-purchase/cart-configuration.md#redirect-to-cart) s’affiche immédiatement après l’ajout d’un produit au panier. Options : `Yes` / `No` |
| [!UICONTROL Number of Items to Display Pager] | Affichage de la boutique | Détermine le nombre d’articles dans le panier avant le déclenchement du pager. Valeur par défaut : `20` |
| [!UICONTROL Show Cross-sell Items in the Shopping Cart] | Affichage de la boutique | Indique si les [articles de vente croisée](../../catalog/related-products-up-sells-cross-sells.md#cross-sells) sont affichés dans le panier, ce qui offre des options de vente supplémentaires aux clients. Options : `Yes` (par défaut) / `No` |
| [!UICONTROL Grouped Product Image] | Affichage de la boutique | Détermine l’image [miniature](../../stores-purchase/cart-configuration.md#cart-thumbnails) qui s’affiche pour un [produit groupé](../../catalog/product-create-grouped.md) dans le panier. Options : `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Configurable Product Image] | Affichage de la boutique | Détermine l’image [miniature](../../stores-purchase/cart-configuration.md#cart-thumbnails) qui s’affiche pour un produit configurable dans le panier. Options : `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Preview Quote Lifetime (minutes)] | Affichage de la boutique | Détermine l’âge maximal du devis en minutes lors de la prévisualisation à partir du panier. |
| [!UICONTROL Enable Clear Shopping Cart] | Site internet | Détermine si le panier affiche l’option permettant aux utilisateurs et utilisatrices d’effacer le contenu du panier en une seule action. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL My Cart Link]

![Lien Mon panier](./assets/checkout-my-cart-link.png)<!-- zoom -->

<!-- [*My Cart Link*](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#mini-cart) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Display Cart Summary] | Site internet | Détermine la valeur qui apparaît entre parenthèses après le lien Mon panier . Options : `Display number of items in cart` / `Display item quantities` |

{style="table-layout:auto"}

## Mini panier

![Mini panier](./assets/checkout-mini-cart.png)<!-- zoom -->

<!-- [*Mini Cart*](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#mini-cart) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Display Mini Cart] | Affichage de la boutique | Détermine si le mini panier s’affiche sur les pages du magasin lorsque l’utilisateur clique sur l’icône du panier dans l’en-tête. L&#39;affichage du mini panier dépend du thème. Options : `Yes` / `No` |
| [!UICONTROL Number of Items to Display Scrollbar] | Affichage de la boutique | Détermine le nombre d’éléments pouvant apparaître dans le mini panier avant le déclenchement de la barre de défilement. Valeur par défaut : `5` |
| [!UICONTROL Maximum Number of Items to Display] | Affichage de la boutique | Détermine le nombre maximal d’articles pouvant apparaître dans le mini panier. Valeur par défaut : `10` |

{style="table-layout:auto"}

## [!UICONTROL Payment Failed Emails]

![E-mails en échec de paiement](./assets/checkout-payment-failed-emails.png)<!-- zoom -->

<!-- [*Payment Failed Emails*](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/checkout/checkout-payment-failed-emails) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Payment Failed Email Receiver] | Affichage de la boutique | Identifie le contact du magasin qui reçoit les e-mails d’échec de paiement. Récepteur par défaut : `General Contact` |
| [!UICONTROL Payment Failed Email Sender] | Affichage de la boutique | Identifie le contact du magasin qui apparaît comme l’expéditeur des e-mails d’échec de paiement. Expéditeur par défaut : `General Contact` |
| [!UICONTROL Payment Failed Template] | Affichage de la boutique | Identifie le modèle utilisé pour les e-mails d’échec de paiement. Modèle par défaut : `Payment Failed` |
| [!UICONTROL Send Payment Failed Copy To] | Affichage de la boutique | Fournit l’adresse e-mail de toute personne souhaitant recevoir une copie d’un e-mail d’échec de paiement. Séparez les adresses multiples par une virgule. |
| [!UICONTROL Send Payment Failed Copy Method] | Affichage de la boutique | Indique la méthode e-mail utilisée pour envoyer la copie. Options : <br />**`Bcc`**- envoie une copie de courtoisie invisible en incluant le destinataire dans l’en-tête du même e-mail envoyé au client ou à la cliente. Le destinataire en Cci n’est pas visible pour le client.<br />**`Separate Email`** - Envoie la copie sous forme d’e-mail distinct. |

{style="table-layout:auto"}
