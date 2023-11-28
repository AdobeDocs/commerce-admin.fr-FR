---
user-guide-title: Guide d’expérience des magasins et des achats
user-guide-description: Informations complètes à l’intention des administrateurs du site, des agents du service client et des responsables commerciaux travaillant dans Adobe Commerce et Magento Open Source.
breadcrumb-title: Magasins et expérience d’achat
role: Admin, User
feature: Storefront
recommendations: noDisplay
source-git-commit: 3eb659825e6bc5db1828c2362ee68893b4d1405b
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 3%

---


# Guide d’expérience des magasins et des achats {#stores-sales}

+ [Guide d’expérience des magasins et des achats](guide-overview.md)
+ [Présentation des magasins et de l’expérience d’achat](introduction.md)
+ Gestion des sites et des magasins {#site-store}
   + [Menu Magasins](stores-menu.md)
   + [Structure du magasin et du site](stores.md)
   + [Vues du magasin](store-views.md)
   + [Localisation de la boutique](store-localize.md)
   + [URL de magasin](store-urls.md)
   + Taxes {#taxes}
      + [Vue d’ensemble](taxes.md)
      + [Paramètres de configuration des taxes](tax-settings-general.md)
      + [Paramètres d&#39;affichage des prix](display-settings.md)
      + [Règles fiscales](tax-rules.md)
      + [Classes fiscales](tax-class.md)
      + [Impôt fixe sur les produits](fixed-product-tax.md)
      + [Calcul des taxes masquées](hidden-tax-calculation.md)
      + [Zones et taux d&#39;imposition](tax-zones-rates.md)
      + [TVA](vat.md)
      + [Directives fiscales par pays](international-tax-guidelines.md)
   + Devise {#currency}
      + [Vue d’ensemble](currency.md)
      + [Configuration des devises](currency-configuration.md)
      + [Mise à jour des taux de change](currency-update.md)
   + [Courriers électroniques de vente](sales-email.md)
   + [Documents commerciaux](sales-documents.md)
+ Point d’achat {#point-of-purchase}
   + [achat instantané](checkout-instant-purchase.md)
   + Panier {#cart}
      + [Vue d’ensemble](cart.md)
      + [Configuration du panier](cart-configuration.md)
      + [Persistance du panier](cart-persistent.md)
      + [Commande par SKU](order-by-sku.md)
   + Assistance commerciale {#assist}
      + [Gestion d’un panier](shopping-assisted-cart-manage.md)
      + [Création d’une commande](customer-account-create-order.md)
      + [Mettre à jour une commande client](order-update.md)
   + Passage en caisse {#checkout}
      + [Vue d’ensemble](checkout-process.md)
      + [Passage en caisse d’une page](checkout-one-page.md)
      + [Passage en caisse des invités](checkout-guest.md)
      + [Conditions générales](terms-and-conditions.md)
      + [Recherche d’adresses](checkout-address-search.md)
      + [Notification d’échec de paiement](checkout-payment-failed-emails.md)
      + [Ordre de tri des totaux de paiement](checkout-totals-sort-order.md)
   + Cartes cadeau {#gift-cards}
      + [Achat et rachat de cartes-cadeaux](product-gift-card-workflow.md)
      + [Comptes de carte cadeau](product-gift-card-accounts.md)
+ Outils d’achat {#shopper-tools}
   + [Envoyer un email à un ami](email-a-friend.md)
   + Listes de souhaits {#wish-lists}
      + [Vue d’ensemble](wishlists.md)
      + [Configurer des listes de souhaits](wishlist-configuration.md)
      + [Expérience de storefront de liste de souhaits](wishlist-storefront.md)
   + [Comparaison de produits](product-compare.md)
   + [Récemment consultés ou comparés](products-viewed-compared.md)
   + [Autoriser les réordres](reorders-allow.md)
+ Paiements {#payments}
   + [Vue d’ensemble](payments.md)
   + Solutions de paiement PayPal {#paypal}
      + [Présentation des solutions PayPal](paypal.md)
      + [Passage en caisse express PayPal](paypal-express-checkout.md)
      + [Paiements avancés de PayPal](paypal-payments-advanced.md)
      + [PayPal payment Pro](paypal-payments-pro.md)
      + [PayPal payment Standard](paypal-payments-standard.md)
      + [PayPal Payflow Pro](paypal-payflow-pro.md)
      + [Lien de flux de production PayPal](paypal-payflow-link.md)
      + [Contrats de facturation PayPal](paypal-billing-agreements.md)
      + [Rapports de règlement PayPal](paypal-settlement-reports.md)
   + [Braintree](braintree.md)
   + [Méthodes de paiement stockées](stored-payment-methods.md)
   + Méthodes de paiement hors ligne {#offline}
      + [Vérifications et commandes monétaires](check-money-order.md)
      + [Encaisse lors de l&#39;envoi](cash-on-delivery.md)
      + [Transferts bancaires](bank-transfer.md)
      + [Commandes](purchase-order.md)
      + [Aucun sous-total passage en caisse](zero-subtotal-checkout.md)
+ Gestion du flux de commande {#order-management}
   + [Menu Ventes](sales-menu.md)
   + Commandes {#orders}
      + [Vue d’ensemble](orders.md)
      + [Workflow et traitement](order-processing.md)
      + [Envoyer une commande](order-ship.md)
      + [État de la commande](order-status.md)
      + [Opérations de commande planifiées](order-scheduled-operations.md)
      + [Archiver les commandes](order-archive.md)
      + [Gestion des commandes du storefront](orders-storefront.md)
   + [Facturations](invoices.md)
   + [Expéditions](shipments.md)
   + Avoir {#credit-memos}
      + [Vue d’ensemble](credit-memos.md)
      + [Envoi d’une note de crédit](credit-memo-create.md)
   + Renvoie {#returns}
      + [Vue d’ensemble](returns.md)
      + [Configurer les retours](rma-configure.md)
      + [Attributs de retour](attributes-returns.md)
      + [Renvoie l’expérience storefront](rma-customer-experience.md)
   + [Transactions](transactions.md)
+ Diffusion {#delivery}
   + [Vue d’ensemble](delivery.md)
   + [Paramètres d&#39;expédition](shipping-settings.md)
   + Méthodes de diffusion de base {#basic-methods}
      + [Envoi gratuit](shipping-free.md)
      + [Taux d&#39;aplati](shipping-flat-rate.md)
      + [Taux des tables](shipping-table-rate.md)
      + [Diffusion en magasin](shipping-in-store-delivery.md)
   + Transporteurs de livraison {#shipping-carriers}
      + [Configuration des opérateurs de livraison](carriers.md)
      + [UPS](ups.md)
      + [USPS](usps.md)
      + [FedEx](fedex.md)
      + [DHL](dhl.md)
   + Libellés d’expédition {#shipping-labels}
      + [Présentation des libellés d’expédition](shipping-labels.md)
      + [Configuration des libellés d’expédition](shipping-label-configure.md)
      + [Création de libellés d’expédition](shipping-label-create.md)
