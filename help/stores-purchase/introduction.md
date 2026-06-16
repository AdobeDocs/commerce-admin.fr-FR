---
title: Présentation des magasins et de l’expérience d’achat
description: Découvrez les fonctionnalités utilisées pour créer et gérer vos magasins en ligne et l’expérience d’achat de vos clients.
exl-id: 7ced9cbc-49b4-48f7-aae2-fcb48fdb888f
TQID: https://experienceleague.adobe.com/wP31dNMG9kiajirB5WTj-lEhTtHqKnl4FfqPsa3tFxs
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 680
ht-degree: 0%

---

# Présentation des magasins et de l’expérience d’achat

Adobe Commerce et Magento Open Source fournissent un ensemble complet de fonctionnalités pour créer et gérer vos magasins en ligne et l’expérience d’achat de vos clients. Dans votre instance Commerce, vous pouvez gérer la hiérarchie de magasin des sites web, des magasins et des vues. Vous pouvez également configurer les taxes et les taux de change requis pour exécuter des magasins pour plusieurs paramètres régionaux, y compris des classes de taxe pour des produits et des groupes de clients.

## Structure de magasin

Une seule instance d’Adobe Commerce ou de Magento Open Source peut prendre en charge plusieurs sites, boutiques ou vues de boutique qui utilisent différents attributs et contenus. Un scénario type consiste à configurer des magasins avec différentes options dans différents domaines. Par exemple, vous pouvez vouloir un ensemble de catégories et de produits sur un domaine et un autre ensemble de catégories et de produits sur un domaine différent dans une autre langue. Les commerçants peuvent configurer les sites web, les magasins et les vues de magasin dans l’Administration.

Lorsque la [hiérarchie](stores.md) est définie, vous pouvez appliquer des paramètres de configuration en fonction de la [portée](../getting-started/websites-stores-views.md#scope-settings) afin que chaque vue de site, de magasin et de magasin fournisse le catalogue de produits et l’expérience de storefront que vous souhaitez.

## Point d’achat

Adobe Commerce et Magento Open Source réduisent les erreurs de commande en vérifiant automatiquement le SKU et la disponibilité de tous les éléments avant l’envoi d’une commande. Vous pouvez configurer les options [panier](cart.md) et [passage en caisse](checkout-process.md) pour offrir une expérience d’achat optimale, de la transaction à la diffusion. Les clients connectés à leurs comptes peuvent passer rapidement en caisse, car la plupart des informations se trouvent déjà dans leurs comptes. La page _Passage en caisse_ guide le client à travers chaque étape du processus pour terminer la transaction de commande. Si vous activez [Achat instantané](checkout-instant-purchase.md), les clients peuvent accélérer le processus de passage en caisse à l’aide des informations enregistrées dans leur compte.

>[!TIP]
>
>![Adobe Commerce B2B](../assets/b2b.svg) Avec l’installation et l’activation d’Adobe Commerce B2B, vous pouvez configurer _commande rapide_ pour les clients associés à un compte de société. Cette fonction réduit le processus de commande à plusieurs clics lorsqu’ils connaissent le nom ou le SKU des produits qu’ils souhaitent commander. Vous pouvez également configurer la prise en charge des devis négociables pour les comptes de votre société. Pour plus d’informations sur les fonctionnalités B2B, consultez le [Guide de l’utilisateur Adobe Commerce B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

## Assistance pour les achats

Les clients ont parfois besoin d’aide pour effectuer un achat. Certains clients aiment faire des achats en ligne, mais préfèrent commander par téléphone. Vous pouvez offrir une assistance immédiate aux clients et aux invités qui se sont inscrits à un compte auprès de votre boutique.

- [Gérer le panier](shopping-assisted-cart-manage.md)
- [Créer des commandes](customer-account-create-order.md) pour les clients enregistrés
- [Mettre à jour les commandes](order-update.md)

![Panier](./assets/storefront-cart-price-group-discount.png){width="700" zoomable="yes"}

Découvrez les achats assistés par le vendeur en regardant cette vidéo :

>[!VIDEO](https://video.tv.adobe.com/v/343662/?quality=12&learn=on)

## Gestion des commandes et opérations

Dans Admin, les commerçants peuvent accéder aux informations à chaque étape du workflow de commande et traiter les commandes :

- La page [Commandes](orders.md) fournit aux commerçants une liste facile d&#39;accès de toutes les commandes actuelles et comprend des outils pour modifier et traiter les commandes existantes, et créer des commandes au nom des clients.

- La page [Factures](invoices.md) répertorie une facture basée sur une commande client temporaire et fournit un enregistrement permanent de la commande.

- La page [Expéditions](shipments.md) répertorie l&#39;enregistrement d&#39;expédition de chaque facture prête à être expédiée.

- La page [avoirs](credit-memos.md) permet aux commerçants de traiter et de gérer un avoir, qui est un document indiquant le montant dû au client. Le montant peut être appliqué à un achat ou remboursé au client.

- ![](../assets/adobe-logo.svg) (Adobe Commerce uniquement) La page [Retours](returns.md) répertorie les demandes de retour de marchandises (RMA) actuelles et permet de saisir de nouvelles demandes de retour.

- La page [Transactions](transactions.md) répertorie toutes les activités de paiement qui ont eu lieu entre votre magasin et un système de paiement et donne accès à des informations plus détaillées.

## Expédition et livraison

Des études montrent que les magasins offrant aux clients le choix entre plusieurs [méthodes de diffusion](delivery.md) ont des taux de conversion plus élevés que les magasins utilisant une seule méthode. L’administrateur fournit divers outils que les commerçants peuvent utiliser pour configurer plusieurs méthodes de livraison et [transporteurs](carriers.md), et pour imprimer des [étiquettes d’expédition](shipping-labels.md).
