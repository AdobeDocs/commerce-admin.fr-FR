---
title: '[!UICONTROL Sales] menu'
description: L’administrateur Commerce comprend la variable [!UICONTROL Sales] qui permet d’accéder aux outils permettant d’utiliser les commandes en fonction de leur emplacement dans le workflow.
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
source-git-commit: a7c6203cf738e3fb9be887d637010ca9c155937a
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# [!UICONTROL Sales] menu

Le menu Ventes répertorie les transactions en fonction de leur emplacement dans le workflow de commande. Vous pouvez considérer chacune des options comme une étape différente dans la durée de vie d’une commande.

![Menu Ventes](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

## Afficher le [!UICONTROL Sales] menu

Sur le _Administration_ barre latérale, cliquez sur **[!UICONTROL Sales]**.

## Options de menu

### [!UICONTROL Quotes]

![B2B pour Adobe Commerce](../assets/b2b.svg) (Disponible avec B2B pour Adobe Commerce)

Les acheteurs autorisés peuvent [négocier le prix](../b2b/quotes.md) avec le vendeur en envoyant un [requête](../b2b/quote-request.md) du panier.

### [!UICONTROL Orders]

Lorsqu’une [order](orders.md) est placée, une commande client est créée en tant qu’enregistrement temporaire de la transaction. Le paiement n&#39;a pas été traité et la commande peut toujours être annulée.

### [!UICONTROL Invoices]

Un [facture](invoices.md) est un enregistrement de la réception du paiement pour une commande. Plusieurs factures peuvent être créées pour une seule commande, chacune comportant autant de produits que le nombre spécifié de produits achetés. En fonction de l&#39;action de paiement, le paiement peut être capturé automatiquement lors de la génération de la facture.

### [!UICONTROL Shipments]

A [envoi](shipments.md) est un enregistrement des produits d’une commande qui ont été expédiés. Comme pour les factures, plusieurs envois peuvent être associés à une seule commande, jusqu’à ce que tous les produits de la commande soient expédiés.

### [!UICONTROL Credit Memos]

A [note de crédit](credit-memos.md) est un document qui indique le montant dû au client pour un remboursement complet ou partiel. Le montant peut être appliqué à un achat ou remboursé au client.

### [!UICONTROL Returns]

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

A [autorisation de marchandisage renvoyée](returns.md) (RMA) peut être accordé aux clients qui demandent de renvoyer un article pour le remplacement ou le remboursement. Les RMA peuvent être émises pour les types de produits Simple, Groupé, Configurable et Bundle. Toutefois, les RMA ne sont pas disponibles pour les produits virtuels et téléchargeables ni pour les cartes-cadeaux.

### [!UICONTROL Billing Agreements]

A [contrat de facturation](paypal-billing-agreements.md) est similaire à un bon de commande, sauf qu’il ne se limite pas à un seul achat. Lors du passage en caisse, le client choisit le contrat de facturation comme mode de paiement. Un contrat de facturation simplifie le processus de passage en caisse, car le client n’a pas à saisir les informations de paiement pour chaque achat.

### [!UICONTROL Transactions]

La variable [Transactions](transactions.md) Cette page répertorie toutes les activités de paiement qui ont eu lieu entre votre boutique et tous les systèmes de paiement et permet d’accéder à des informations plus détaillées.

### [!UICONTROL Braintree Virtual Terminal]

Sur la page Terminal virtuel du Braintree, un utilisateur administrateur peut accepter le paiement pour le montant sélectionné. Pour rendre la fonction de terminal disponible, un commerçant doit configurer les [Paramètres du Braintree](braintree.md). Braintree offre une expérience de paiement entièrement personnalisable avec la détection des fraudes et l’intégration de PayPal.

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

(L’option Archiver doit être activée) [Archivage des commandes](order-archive.md) et d’autres documents de vente améliorent régulièrement les performances et permettent à votre espace de travail d’éviter toute information inutile.
