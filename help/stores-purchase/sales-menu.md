---
title: '[!UICONTROL Sales] menu'
description: L’Administration Commerce comprend le menu [!UICONTROL Sales] qui permet d’accéder aux outils servant à traiter les commandes en fonction de leur emplacement dans le workflow.
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
source-git-commit: 621b4729e23952ddd720b4dcc49b5341baae64cc
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 0%

---

# [!UICONTROL Sales] menu

Le menu Ventes répertorie les transactions en fonction de leur emplacement dans le workflow de commande. Vous pouvez considérer chacune des options comme une étape différente de la durée de vie d&#39;une commande.

>[!BEGINTABS]

>[!TAB Adobe Commerce]

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

![Menu Ventes](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

>[!TAB Adobe Commerce as a Cloud Service]

[!BADGE SaaS uniquement]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce as a Cloud Service et Adobe Commerce Optimizer (infrastructure SaaS gérée par Adobe)."}

![Menu Ventes](./assets/admin-menu-sales-accs.png){width="450" zoomable="yes"}

>[!ENDTABS]

## Afficher le menu [!UICONTROL Sales]

Dans la barre latérale _Admin_, cliquez sur **[!UICONTROL Sales]**.

## Options de menu

### [!UICONTROL Quotes]

![Adobe Commerce B2B](../assets/b2b.svg) (disponible avec Adobe Commerce B2B)

Les acheteurs autorisés peuvent [négocier le prix](../b2b/quotes.md) avec le vendeur en envoyant une [demande](../b2b/quote-request.md) à partir du panier.

### [!UICONTROL Quote Templates]

![Adobe Commerce B2B](../assets/b2b.svg) (disponible avec Adobe Commerce B2B)

Permet aux acheteurs et aux vendeurs de rationaliser le processus de devis en créant des modèles de devis [réutilisables et personnalisables](../b2b/quote-templates-overview.md).

### [!UICONTROL Orders]

Lorsqu&#39;une [commande](orders.md) est passée, une commande client est créée comme enregistrement temporaire de la transaction. Le paiement n&#39;a pas été traité et la commande peut toujours être annulée.

### [!UICONTROL Invoices]

Une [facture](invoices.md) est un enregistrement de la réception du paiement d&#39;une commande. Plusieurs factures peuvent être créées pour une seule commande, chacune avec autant de produits achetés que vous spécifiez, ou aussi peu. En fonction de l&#39;action de paiement, le paiement peut être automatiquement capturé lors de la génération de la facture.

### [!UICONTROL Shipments]

Une [expédition](shipments.md) est un enregistrement des produits d&#39;une commande qui ont été expédiés. Comme pour les factures, plusieurs livraisons peuvent être associées à une seule commande, jusqu’à ce que tous les produits de la commande soient expédiés.

### [!UICONTROL Credit Memos]

Un [avoir](credit-memos.md) est un document qui indique le montant dû au client pour un remboursement complet ou partiel. Le montant peut être appliqué à un achat ou remboursé au client.

### [!UICONTROL Returns]

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

Une [autorisation de retour de marchandise](returns.md) (RMA) peut être accordée aux clients qui demandent à renvoyer un article pour le remplacer ou le rembourser. Des autorisations de retour client peuvent être émises pour les types de produits Simple, Groupé, Configurable et Bundle. Cependant, les RMA ne sont pas disponibles pour les produits virtuels et téléchargeables, ni pour les cartes-cadeaux.

### [!UICONTROL Billing Agreements]

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

Un [accord de facturation](paypal-billing-agreements.md) est similaire à un bon de commande, sauf qu&#39;il ne se limite pas à un seul achat. Lors du passage en caisse, le client choisit le contrat de facturation comme mode de paiement. Un accord de facturation simplifie le processus de passage en caisse, car le client n&#39;a pas à saisir d&#39;informations de paiement pour chaque achat.

### [!UICONTROL Transactions]

La page [Transactions](transactions.md) répertorie toutes les activités de paiement qui ont eu lieu entre votre magasin et tous les systèmes de paiement et donne accès à des informations plus détaillées.

### [!UICONTROL Braintree Virtual Terminal]

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

Sur la page Braintree Virtual Terminal , un utilisateur administrateur peut accepter le paiement du montant sélectionné. Pour rendre la fonctionnalité de terminal disponible, un commerçant doit configurer les paramètres de base de [Braintree](braintree.md). Braintree offre une expérience de paiement entièrement personnalisable avec détection des fraudes et intégration PayPal.

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

(L’option d’archivage doit être activée) [L’archivage des commandes](order-archive.md) et d’autres documents commerciaux améliore régulièrement les performances et libère votre espace de travail des informations inutiles.
