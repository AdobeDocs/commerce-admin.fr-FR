---
title: achat instantané
description: Découvrez l’achat instantané et comment il peut fournir un passage en caisse rapide pour les comptes clients enregistrés.
exl-id: f299f364-d7e3-4567-8c7b-955129011a19
feature: Checkout
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# achat instantané

_achat instantané_ permet aux clients d’accélérer le processus de passage en caisse à l’aide d’informations enregistrées dans leur compte. Lorsque cette option est activée, la variable _achat instantané_ apparaît sous le bouton _Ajouter au panier_ sur la page produit pour les clients qui répondent aux exigences.

![Page de produit avec l’option Achat instantané affichée](./assets/storefront-checkout-instant-purchase.png){width="700" zoomable="yes"}

## Exigences du client

- Le client est [connecté](../customers/customer-sign-in.md) à leur compte.

- Le compte client comporte une [adresse de facturation et de livraison par défaut](../customers/account-dashboard-address-book.md).

- Au moins un [méthode d&#39;expédition](delivery.md) est disponible pour le pays spécifié dans l’adresse de livraison par défaut.

- Le compte client comporte une [paiement stocké](../stores-purchase/stored-payment-methods.md) avec vault activé.

  Les méthodes de paiement suivantes peuvent être utilisées pour fournir un accès sécurisé aux informations de carte de crédit enregistrées :

   - [Cartes de crédit Braintree](braintree.md) (Les achats instantanés ne peuvent pas être utilisés avec les cartes de crédit du Braintree si 3D Secure est activé.)
   - [Braintree avec PayPal activé](braintree.md)
   - [PayPal Payflow Pro](paypal-payflow-pro.md)

## Achat instantané sur le storefront

1. Sur le storefront, le client accède à la page de produit de l’article à acheter.

1. Sélection des options et clics requis **[!UICONTROL Instant Purchase]**.

   ![Boîte de dialogue de confirmation pour confirmer l’achat instantané](./assets/storefront-checkout-instant-purchase-confirmation.png){width="500" zoomable="yes"}

1. Révision de la **[!UICONTROL Instant Purchase Confirmation]** informations et clics **[!UICONTROL OK]** pour terminer la transaction.

   Un message de confirmation et un numéro de commande s’affichent en haut de la page du produit.

## Configuration d’un achat instantané

### Etape 1 : ouvrir la page de configuration

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

### Étape 2 : configuration du coffre du mode de paiement

Vous pouvez utiliser Achat instantané avec Braintree ou Services de paiement pour Adobe Commerce et Magento Open Source. La mise en valeur doit être activée pour qu’un acheteur puisse utiliser la fonction Achat instantané .

Découvrez comment configurer le mode de paiement et activer la mise en valeur pour Braintree ou les services de paiement :

- [Braintree](braintree.md)
- [Documentation des services de paiement](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html)

### Étape 3 : Activer les achats instantanés

1. Dans le panneau de gauche, sous _[!UICONTROL Sales]_, choisissez **[!UICONTROL Sales]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Instant Purchase]** .

1. Si cette modification concerne une vue de magasin spécifique, [choix de la vue magasin](../configuration-reference/scope-change.md#set-the-scope) où la configuration s’applique.

   Lorsque vous y êtes invité, cliquez sur **[!UICONTROL OK]** pour continuer.

1. Définir **[!UICONTROL Enabled]** to `Yes`.

1. Saisissez le **[!UICONTROL Button Text]** que vous souhaitez afficher sur le bouton.

   Le texte du bouton peut être modifié pour chaque vue ou langue de magasin. Par défaut, le texte du bouton est `Instant Purchase`.

   ![Configuration - Options d’achat instantané](../configuration-reference/sales/assets/sales-instant-purchase.png){width="600" zoomable="yes"}

   Pour une description détaillée de chacun de ces paramètres de configuration, voir [achat instantané](../configuration-reference/sales/sales.md#instant-purchase) dans le _Guide de référence de configuration_.

1. Cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous y êtes invité, cliquez sur **[!UICONTROL Cache Management]** dans le message système et suivez les instructions pour vider le cache.
