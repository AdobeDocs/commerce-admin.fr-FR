---
title: Menu '[!UICONTROL Sales]'
description: L’administrateur Commerce comprend le menu [!UICONTROL Sales], qui permet d’accéder aux outils permettant d’utiliser les commandes en fonction de leur emplacement dans le workflow.
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# Menu [!UICONTROL Sales]

Le menu Ventes répertorie les transactions en fonction de leur emplacement dans le workflow de commande. Vous pouvez considérer chacune des options comme une étape différente dans la durée de vie d’une commande.

![Menu des ventes](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

## Afficher le menu [!UICONTROL Sales]

Dans la barre latérale _Admin_, cliquez sur **[!UICONTROL Sales]**.

## Options de menu

### [!UICONTROL Quotes]

![Adobe Commerce B2B](../assets/b2b.svg) (Disponible avec Adobe Commerce B2B)

Les acheteurs autorisés peuvent [négocier le prix](../b2b/quotes.md) avec le vendeur en envoyant une [demande](../b2b/quote-request.md) au panier.

### [!UICONTROL Orders]

Lorsqu’une [commande](orders.md) est placée, une commande client est créée en tant qu’enregistrement temporaire de la transaction. Le paiement n&#39;a pas été traité et la commande peut toujours être annulée.

### [!UICONTROL Invoices]

Une [facture](invoices.md) est un enregistrement de la réception du paiement pour une commande. Plusieurs factures peuvent être créées pour une seule commande, chacune comportant autant de produits que le nombre spécifié de produits achetés. En fonction de l&#39;action de paiement, le paiement peut être capturé automatiquement lors de la génération de la facture.

### [!UICONTROL Shipments]

Un [envoi](shipments.md) est un enregistrement des produits dans une commande qui a été expédiée. Comme pour les factures, plusieurs envois peuvent être associés à une seule commande, jusqu’à ce que tous les produits de la commande soient expédiés.

### [!UICONTROL Credit Memos]

Un [note de crédit](credit-memos.md) est un document qui indique le montant dû au client pour un remboursement complet ou partiel. Le montant peut être appliqué à un achat ou remboursé au client.

### [!UICONTROL Returns]

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

Une [autorisation de marchandisage renvoyée](returns.md) (RMA) peut être accordée aux clients qui demandent de renvoyer un article pour le remplacement ou le remboursement. Les RMA peuvent être émises pour les types de produits Simple, Groupé, Configurable et Bundle. Toutefois, les RMA ne sont pas disponibles pour les produits virtuels et téléchargeables ni pour les cartes-cadeaux.

### [!UICONTROL Billing Agreements]

Un [contrat de facturation](paypal-billing-agreements.md) est similaire à un bon de commande, sauf qu’il ne se limite pas à un seul achat. Lors du passage en caisse, le client choisit le contrat de facturation comme mode de paiement. Un contrat de facturation simplifie le processus de passage en caisse, car le client n’a pas à saisir les informations de paiement pour chaque achat.

### [!UICONTROL Transactions]

La page [Transactions](transactions.md) répertorie toutes les activités de paiement qui ont eu lieu entre votre boutique et tous les systèmes de paiement et permet d’accéder à des informations plus détaillées.

### [!UICONTROL Braintree Virtual Terminal]

Sur la page Terminal virtuel du Braintree, un utilisateur administrateur peut accepter le paiement pour le montant sélectionné. Pour rendre la fonction de terminal disponible, un commerçant doit configurer les [paramètres de Braintree](braintree.md) de base. Braintree offre une expérience de paiement entièrement personnalisable avec la détection des fraudes et l’intégration de PayPal.

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

(L’option Archiver doit être activée) [L’archivage des commandes](order-archive.md) et d’autres documents de vente améliore régulièrement les performances et permet à votre espace de travail d’éviter toute information inutile.
