---
title: Présentation des magasins et de l’expérience d’achat
description: Découvrez les fonctionnalités utilisées pour créer et gérer vos magasins en ligne et l’expérience d’achat pour vos clients.
exl-id: 7ced9cbc-49b4-48f7-aae2-fcb48fdb888f
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# Présentation des magasins et de l’expérience d’achat

Adobe Commerce et Magento Open Source fournissent un ensemble complet de fonctionnalités pour créer et gérer vos magasins en ligne et l’expérience d’achat de vos clients. Dans votre instance Commerce, vous pouvez gérer la hiérarchie des magasins de sites web, magasins et vues. Vous pouvez également configurer les taxes et les taux de devise requis pour exécuter les magasins pour plusieurs paramètres régionaux, y compris les classes de taxe pour les produits et les groupes de clients.

## Structure du magasin

Une instance unique d’Adobe Commerce ou de Magento Open Source peut prendre en charge plusieurs sites, magasins ou vues de magasin qui utilisent différents attributs et contenus. Un scénario type consiste à configurer des magasins avec différentes options dans différents domaines. Par exemple, vous souhaitez peut-être un ensemble de catégories et de produits sur un domaine et un autre ensemble de catégories et de produits sur un autre domaine dans une autre langue. Les vendeurs peuvent configurer les sites web, les magasins et les vues des magasins dans l’administrateur.

Lorsque la [hiérarchie](stores.md) est définie, vous pouvez appliquer des paramètres de configuration en fonction de [portée](../getting-started/websites-stores-views.md#scope-settings) afin que chaque site, magasin et magasin vue fournisse le catalogue de produits et l’expérience de storefront que vous souhaitez.

## Point d’achat

Adobe Commerce et Magento Open Source réduisent les erreurs de commande en vérifiant automatiquement le SKU et la disponibilité de tous les éléments avant l’envoi d’une commande. Vous pouvez configurer les [panier](cart.md) et les [ options de passage en caisse](checkout-process.md) pour offrir une expérience d’achat optimale, de la transaction à la diffusion. Les clients qui sont connectés à leur compte peuvent effectuer rapidement l’extraction, car la plupart des informations se trouvent déjà dans leurs comptes. La page _Passage en caisse_ guide le client à chaque étape du processus pour terminer la transaction de commande. Si vous activez l’ [achat instantané](checkout-instant-purchase.md), les clients peuvent accélérer le processus de passage en caisse à l’aide des informations enregistrées dans leur compte.

>[!TIP]
>
>![Adobe Commerce B2B](../assets/b2b.svg) Avec l’installation et l’activation d’Adobe Commerce B2B, vous pouvez configurer la _commande rapide_ pour les clients associés à un compte d’entreprise. Cette fonction réduit le processus de commande à plusieurs clics lorsqu’ils connaissent le nom ou le SKU des produits qu’ils souhaitent commander. Vous pouvez également configurer la prise en charge des devis négociables pour les comptes de votre société. Pour plus d’informations sur les fonctionnalités B2B, consultez le [Guide de l’utilisateur d’Adobe Commerce B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=fr).

## Assistance commerciale

Les clients ont parfois besoin d’aide pour effectuer un achat. Certains clients aiment faire leurs achats en ligne, mais préfèrent commander par téléphone. Vous pouvez offrir une assistance immédiate aux invités et aux clients qui se sont inscrits pour un compte auprès de votre boutique.

- [Gestion du panier](shopping-assisted-cart-manage.md)
- [Créer des commandes](customer-account-create-order.md) pour les clients enregistrés
- [Mettre à jour les commandes](order-update.md)

![Panier](./assets/storefront-cart-price-group-discount.png){width="700" zoomable="yes"}

Découvrez les achats assistés par les vendeurs en regardant cette vidéo :

>[!VIDEO](https://video.tv.adobe.com/v/3410201/?quality=12&learn=on&captions=fre_fr)

## Gestion des commandes et opérations

Dans l’administrateur, les marchands peuvent accéder aux informations à chaque étape du workflow de commande et traiter les commandes :

- La page [Commandes](orders.md) fournit aux commerçants une liste facile d’accès de toutes les commandes en cours, comprend des outils pour modifier et traiter les commandes existantes, et créer des commandes pour le compte des clients.

- La page [Factures](invoices.md) répertorie Une facture est basée sur une commande de vente temporaire et fournit un enregistrement permanent de la commande.

- La page [Expéditions](shipments.md) répertorie l’enregistrement d’expédition de chaque facture prête à être expédiée.

- La page [Avoir de crédit](credit-memos.md) permet aux marchands de traiter et gérer un avoir, qui est un document qui indique le montant dû au client. Le montant peut être appliqué à un achat ou remboursé au client.

- ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) La page [Renvoie](returns.md) répertorie les demandes de marchandises renvoyées (RMA) actuelles et est utilisée pour entrer de nouvelles demandes de retour.

- La page [Transactions](transactions.md) répertorie toutes les activités de paiement qui ont eu lieu entre votre boutique et un système de paiement, et permet d’accéder à des informations plus détaillées.

## Livraison et diffusion

Des études montrent que les magasins offrant aux clients le choix de plusieurs [méthodes de diffusion](delivery.md) ont des taux de conversion plus élevés que les magasins utilisant une seule méthode. L’administrateur fournit divers outils que les commerçants peuvent utiliser pour configurer plusieurs méthodes de diffusion et des [opérateurs d’expédition](carriers.md) et pour imprimer des [libellés d’expédition](shipping-labels.md).
