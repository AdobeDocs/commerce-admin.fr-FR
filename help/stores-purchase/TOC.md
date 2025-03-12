---
user-guide-title: Guide de l’expérience d’achat et des magasins
user-guide-description: Informations complètes destinées aux administrateurs de site, aux agents du service client et aux responsables des ventes travaillant dans Adobe Commerce et Magento Open Source.
breadcrumb-title: Expérience d’achat et de magasins
role: Admin, User
feature: Storefront
recommendations: noDisplay
source-git-commit: 9ff5a82a4d3bd2b979e5475351ae6c3babf26ca4
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 3%

---


# Guide de l’expérience d’achat et des magasins {#stores-sales}

+ [Guide de l’expérience d’achat et des magasins](guide-overview.md)
+ [Présentation des magasins et de l’expérience d’achat](introduction.md)
+ {#site-store} de gestion des sites et des magasins
   + [Menu Magasins](stores-menu.md)
   + [Structure du magasin et du site](stores.md)
   + [Vues de la boutique](store-views.md)
   + [Localisation de la boutique](store-localize.md)
   + [Stocker les URL](store-urls.md)
   + Taxes {#taxes}
      + [Vue d’ensemble](taxes.md)
      + [Paramètres de configuration des taxes](tax-settings-general.md)
      + [Paramètres d’affichage des prix](display-settings.md)
      + [Règles fiscales](tax-rules.md)
      + [Classes d&#39;impôts](tax-class.md)
      + [Taxe fixe sur les produits](fixed-product-tax.md)
      + [Calcul des taxes cachées](hidden-tax-calculation.md)
      + [Zones fiscales et taux](tax-zones-rates.md)
      + [TVA (taxe sur la valeur ajoutée)](vat.md)
      + [Directives fiscales par pays](international-tax-guidelines.md)
   + {#currency} de devise
      + [Vue d’ensemble](currency.md)
      + [Configuration de la devise](currency-configuration.md)
      + [Mettre à jour les taux de change](currency-update.md)
   + [E-mails de vente](sales-email.md)
   + [Documents vente](sales-documents.md)
+ {#point-of-purchase} du point d’achat
   + [Achat instantané](checkout-instant-purchase.md)
   + {#cart} de panier
      + [Vue d’ensemble](cart.md)
      + [Configuration du panier](cart-configuration.md)
      + [Persistance du panier](cart-persistent.md)
      + [Classer par SKU](order-by-sku.md)
   + {#assist} d’assistance à l’achat
      + [Gestion d’un panier](shopping-assisted-cart-manage.md)
      + [Création d’une commande](customer-account-create-order.md)
      + [Mettre à jour une commande client](order-update.md)
   + {#checkout} de passage en caisse
      + [Vue d’ensemble](checkout-process.md)
      + [Passage en caisse d’une page](checkout-one-page.md)
      + [Passage en caisse des invités](checkout-guest.md)
      + [Termes et conditions](terms-and-conditions.md)
      + [Recherche d’adresses](checkout-address-search.md)
      + [Notification d’échec de paiement](checkout-payment-failed-emails.md)
      + [Ordre de tri des totaux de passage en caisse](checkout-totals-sort-order.md)
   + Cartes-cadeaux {#gift-cards}
      + [Achat et remboursement par carte-cadeau](product-gift-card-workflow.md)
      + [Comptes de carte cadeau](product-gift-card-accounts.md)
+ {#shopper-tools} des outils de l’acheteur
   + [Envoyer un e-mail à un ami](email-a-friend.md)
   + Listes de souhaits {#wish-lists}
      + [Vue d’ensemble](wishlists.md)
      + [Configuration des listes de souhaits](wishlist-configuration.md)
      + [Expérience storefront de liste de souhaits](wishlist-storefront.md)
   + [Comparer les produits](product-compare.md)
   + [Récemment consulté ou comparé](products-viewed-compared.md)
   + [Autoriser les nouvelles commandes](reorders-allow.md)
   + [Autoriser l&#39;annulation de la commande](cancel-allow.md)
+ {#payments} des paiements
   + [Vue d’ensemble](payments.md)
   + Solutions de paiement PayPal {#paypal}
      + [Présentation des solutions PayPal](paypal.md)
      + [PayPal Express Checkout](paypal-express-checkout.md)
      + [Paiements PayPal avancés](paypal-payments-advanced.md)
      + [PayPal Payments Pro](paypal-payments-pro.md)
      + [Paiements PayPal Standard](paypal-payments-standard.md)
      + [PayPal Payflow Pro](paypal-payflow-pro.md)
      + [Lien de flux de paiement PayPal](paypal-payflow-link.md)
      + [Contrats de facturation PayPal](paypal-billing-agreements.md)
      + [Rapports de règlement PayPal](paypal-settlement-reports.md)
   + [Braintree](braintree.md)
   + [Modes de paiement stockés](stored-payment-methods.md)
   + Modes de paiement hors ligne {#offline}
      + [Chèques et mandats](check-money-order.md)
      + [Contre remboursement](cash-on-delivery.md)
      + [Virements bancaires](bank-transfer.md)
      + [Commandes fournisseur](purchase-order.md)
      + [Passage en caisse du sous-total zéro](zero-subtotal-checkout.md)
+ Gérer les {#order-management} de flux de commande
   + [Menu Ventes](sales-menu.md)
   + Commandes {#orders}
      + [Vue d’ensemble](orders.md)
      + [Workflow et traitement](order-processing.md)
      + [Expédier une commande](order-ship.md)
      + [Statut de la commande](order-status.md)
      + [Opérations de commande planifiées](order-scheduled-operations.md)
      + [Archiver les commandes](order-archive.md)
      + [Gestion des commandes de Storefront](orders-storefront.md)
   + [Factures](invoices.md)
   + [Expéditions](shipments.md)
   + {#credit-memos} des avoirs
      + [Vue d’ensemble](credit-memos.md)
      + [Émettre un avoir](credit-memo-create.md)
   + Renvoie {#returns}
      + [Vue d’ensemble](returns.md)
      + [Configurer les retours](rma-configure.md)
      + [Attributs de retour](attributes-returns.md)
      + [Retourne l’expérience du storefront](rma-customer-experience.md)
   + [Transactions](transactions.md)
+ {#delivery} de diffusion
   + [Vue d’ensemble](delivery.md)
   + [Paramètres d’expédition](shipping-settings.md)
   + Méthodes de diffusion de base {#basic-methods}
      + [Livraison gratuite](shipping-free.md)
      + [Taux forfaitaire](shipping-flat-rate.md)
      + [Taux de table](shipping-table-rate.md)
      + [Diffusion en magasin](shipping-in-store-delivery.md)
   + {#shipping-carriers} des transporteurs
      + [Paramétrage du transporteur](carriers.md)
      + [UPS](ups.md)
      + [USPS](usps.md)
      + [FedEx](fedex.md)
      + [DHL](dhl.md)
   + Étiquettes d&#39;expédition {#shipping-labels}
      + [Aperçu de l’étiquette d’expédition](shipping-labels.md)
      + [Configurer les étiquettes d&#39;expédition](shipping-label-configure.md)
      + [Créer des étiquettes d&#39;expédition](shipping-label-create.md)
+ [Retour aux guides de l’utilisateur des administrateurs](https://experienceleague.adobe.com/en/docs/commerce-admin/user-guides/home)

