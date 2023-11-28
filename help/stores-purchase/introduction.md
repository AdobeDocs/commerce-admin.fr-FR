---
title: Présentation des magasins et de l’expérience d’achat
description: Découvrez les fonctionnalités utilisées pour créer et gérer vos magasins en ligne et l’expérience d’achat pour vos clients.
exl-id: 7ced9cbc-49b4-48f7-aae2-fcb48fdb888f
source-git-commit: a56509eeedbb30a1e9cacfd521ea4c18e0241d94
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---

# Présentation des magasins et de l’expérience d’achat

Adobe Commerce et Magento Open Source fournissent un ensemble complet de fonctionnalités pour créer et gérer vos magasins en ligne et l’expérience d’achat de vos clients. Dans votre instance Commerce, vous pouvez gérer la hiérarchie de magasins de sites web, magasins et vues. Vous pouvez également configurer les taxes et les taux de devise requis pour exécuter les magasins pour plusieurs paramètres régionaux, y compris les classes de taxe pour les produits et les groupes de clients.

## Structure du magasin

Une instance unique d’Adobe Commerce ou de Magento Open Source peut prendre en charge plusieurs sites, magasins ou vues de magasin qui utilisent différents attributs et contenus. Un scénario type consiste à configurer des magasins avec différentes options dans différents domaines. Par exemple, vous souhaitez peut-être un ensemble de catégories et de produits sur un domaine et un autre ensemble de catégories et de produits sur un autre domaine dans une autre langue. Les vendeurs peuvent configurer les sites web, les magasins et les vues des magasins dans l’administrateur.

Lorsque la variable [hiérarchie](stores.md) est défini, vous pouvez appliquer des paramètres de configuration en fonction des [scope](../getting-started/websites-stores-views.md#scope-settings) de sorte que chaque site, magasin et vue de magasin fournisse le catalogue de produits et l’expérience de storefront que vous souhaitez.

## Point d’achat

Adobe Commerce et Magento Open Source réduisent les erreurs de commande en vérifiant automatiquement le SKU et la disponibilité de tous les éléments avant l’envoi d’une commande. Vous pouvez configurer la variable [panier](cart.md) et [options de passage en caisse](checkout-process.md) pour offrir une expérience d’achat optimale, de la transaction à la diffusion. Les clients qui sont connectés à leur compte peuvent effectuer rapidement l’extraction, car la plupart des informations se trouvent déjà dans leurs comptes. La variable _Passage en caisse_ guide le client tout au long de chaque étape du processus pour terminer la transaction de commande. Si vous activez [achat instantané](checkout-instant-purchase.md), les clients peuvent accélérer le processus de passage en caisse à l’aide des informations enregistrées dans leur compte.

>[!TIP]
>
>![B2B pour Adobe Commerce](../assets/b2b.svg) Avec l’installation et l’activation de B2B pour Adobe Commerce, vous pouvez configurer _Ordre rapide_ pour les clients associés à un compte d’entreprise. Cette fonction réduit le processus de commande à plusieurs clics lorsqu’ils connaissent le nom ou le SKU des produits qu’ils souhaitent commander. Vous pouvez également configurer la prise en charge des devis négociables pour les comptes de votre société. Pour plus d’informations sur les fonctionnalités B2B, voir [Guide de l’utilisateur B2B pour Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

## Assistance commerciale

Les clients ont parfois besoin d’aide pour effectuer un achat. Certains clients aiment faire leurs achats en ligne, mais préfèrent commander par téléphone. Vous pouvez offrir une assistance immédiate aux invités et aux clients qui se sont inscrits pour un compte auprès de votre boutique.

- [Gestion du panier](shopping-assisted-cart-manage.md)
- [Créer des commandes](customer-account-create-order.md) pour les clients enregistrés
- [Mettre à jour les commandes](order-update.md)

![Panier](./assets/storefront-cart-price-group-discount.png){width="700" zoomable="yes"}

Découvrez les achats assistés par les vendeurs en regardant cette vidéo :

>[!VIDEO](https://video.tv.adobe.com/v/343662/?quality=12)

## Gestion des commandes et opérations

Dans l’administrateur, les marchands peuvent accéder aux informations à chaque étape du workflow de commande et traiter les commandes :

- La variable [Commandes](orders.md) La page fournit aux commerçants une liste facile d’accès de toutes les commandes en cours. Elle comprend également des outils pour modifier et traiter les commandes existantes et créer des commandes pour le compte des clients.

- La variable [Facturations](invoices.md) listes de pages Une facture est basée sur une commande de vente temporaire et fournit un enregistrement permanent de la commande.

- La variable [Expéditions](shipments.md) La page répertorie l’enregistrement de l’expédition de chaque facture prête à être expédiée.

- La variable [Avoir](credit-memos.md) La page permet aux commerçants de traiter et de gérer une note de crédit, qui est un document qui indique le montant dû au client. Le montant peut être appliqué à un achat ou remboursé au client.

- ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) La variable [Renvoie](returns.md) La page répertorie les demandes de marchandisage renvoyées actuelles et est utilisée pour entrer de nouvelles demandes de retour.

- La variable [Transactions](transactions.md) Cette page répertorie toutes les activités de paiement qui ont eu lieu entre votre boutique et un système de paiement et permet d’accéder à des informations plus détaillées.

## Livraison et diffusion

Des études montrent que les magasins offrant aux clients un choix de plusieurs [méthodes de diffusion](delivery.md) présentent des taux de conversion plus élevés que les magasins qui utilisent une seule méthode. L’administrateur fournit divers outils que les commerçants peuvent utiliser pour configurer plusieurs méthodes de diffusion et [compagnies de transport](carriers.md)et à imprimer [libellé d’expédition](shipping-labels.md).
