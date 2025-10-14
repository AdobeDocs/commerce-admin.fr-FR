---
title: Présentation des paiements
description: Découvrez les méthodes et services de paiement pris en charge de manière native dans Adobe Commerce et Magento Open Source.
exl-id: 474bf6df-96e2-4db3-ad3c-1804b5de33b0
feature: Payments
source-git-commit: 489c72652693a15ffe1c745277bbaa9da084dcba
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Présentation des paiements

Adobe Commerce et Magento Open Source prennent en charge un large éventail de méthodes et de services de paiement. Cela inclut plusieurs méthodes de paiement hors ligne, notamment le paiement par chèque ou mandat-poste et le paiement contre remboursement (COD). Il existe également des intégrations natives pour de nombreuses solutions et passerelles de paiement en ligne, y compris Braintree en tant qu’extension groupée développée par des fournisseurs.

>[!TIP]
>
>Payment Services pour Adobe Commerce et Magento Open Source offre une solution en libre-service clé en main, y compris les tests de sandbox et une configuration simple, pour offrir un traitement des paiements robuste et sécurisé. Pour en savoir plus sur cet ensemble d&#39;outils puissants et sur la manière dont il peut vous fournir l&#39;insight et le contrôle dont vous avez besoin pour offrir la meilleure expérience à vos acheteurs, consultez le [Guide d&#39;utilisation des services de paiement](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html?lang=fr). Il s’agit de la solution de paiement par défaut dans [Adobe Commerce as a Cloud Service](https://experienceleague.adobe.com/fr/docs/commerce/cloud-service/overview).

>[!NOTE]
>
>Examinez les [Directives de conformité PCI](../getting-started/compliance-pci.md) qui décrivent les exigences définies par l’industrie des cartes de paiement (PCI) pour les entreprises qui acceptent le paiement par carte de crédit sur Internet.

## Changements dans la version 2.4

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

Certaines intégrations de paiements et extensions groupées ont été supprimées dans les versions 2.4.x et déplacées vers Commerce Marketplace. Retrouvez les dernières extensions officielles d&#39;intégration des paiements dans le [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target="_blank"}.

- **Amazon Pay** et **Klarna** : les versions 2.4.0 à 2.4.3 d’Adobe Commerce et Magento Open Source incluaient ces extensions développées par le fournisseur. À compter de la version 2.4.4, ces extensions ne sont plus incluses dans la version de base et doivent être installées et mises à jour à partir de Commerce Marketplace. La Marketplace permet également d’accéder à la documentation actuelle fournie par le développeur d’extensions.

  Si l’une de ces extensions groupées est activée et configurée, vous devez mettre à jour votre fichier composer.json dans le cadre du processus de mise à niveau vers la version 2.4.4 et pour gérer les mises à jour d’extension à l’avenir. Voir [Mise à niveau des modules](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html?lang=fr) dans le _Guide de mise à niveau_ pour plus d’informations.

- **Worldpay**, **Eway**, **CyberSource** et **Authorize.Net** : Pour plus d’informations sur la manière d’effectuer une transition sécurisée depuis ces intégrations de paiement, consultez le [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target="_blank"}.

## Modes de paiement hors ligne

Adobe Commerce et Magento Open Source comprennent plusieurs méthodes de paiement hors ligne intégrées, qui ne nécessitent pas les services d’une société de traitement des paiements tierce :

- [Passage en caisse du sous-total zéro](zero-subtotal-checkout.md)
- [Paiement À La Livraison](cash-on-delivery.md)
- [Paiement par virement bancaire](bank-transfer.md)
- [Chèque / Mandat](check-money-order.md)
- [Bon de commande](purchase-order.md)
- [Paiement sur le compte](../b2b/enable-basic-features.md#configure-payment-on-account) ![Adobe Commerce B2B](../assets/b2b.svg) (disponible avec Adobe Commerce B2B)

## Modes de paiement en ligne

Adobe Commerce et Magento Open Source prennent en charge de nombreuses solutions de paiement qui offrent des services aux commerçants partout dans le monde. Contrairement aux solutions de paiement qui transfèrent le contrôle sur un autre site pour effectuer la transaction, une passerelle de paiement vous permet d&#39;accepter les paiements par carte de crédit directement depuis votre magasin sans que le client quitte votre site.

### Solutions recommandées

- [&#x200B; Services de paiement &#x200B;](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html?lang=fr)
- [!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."} [PayPal Express Checkout](paypal-express-checkout.md)
- [!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."} [Braintree](braintree.md)

### Autres solutions de paiement PayPal

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

Consultez [Solutions de paiement PayPal](paypal.md) pour plus d’informations sur les options de mode de paiement PayPal.

#### Solutions PayPal tout-en-un

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

- [Paiements PayPal avancés](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [Paiements PayPal Standard](paypal-payments-standard.md)

#### Passerelles de paiement PayPal

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [Lien de flux de paiement PayPal](paypal-payflow-link.md)

## Protection contre la fraude

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

Les services et filtres de protection contre la fraude examinent les commandes envoyées avant que la transaction ne soit traitée afin de détecter les commandes frauduleuses et de vous protéger contre les frais de retour. Adobe Commerce et Magento Open Source prennent en charge les solutions de protection contre la fraude suivantes :

- [Filtre de gestion des fraudes PayPal](paypal.md#paypal-fraud-management-filters)

- [Solutions de protection contre la fraude sur le marché][1]

>[!NOTE]
>
>Pour prendre en charge les mises à jour de conformité en matière de sécurité, la protection contre les fraudes de Signifyd est supprimée de Commerce à partir de la version 2.4.0. Si vous utilisez l’intégration Signifyd dans une version 2.3.x ou antérieure, il est recommandé de passer à l’extension [Signifyd Fraud &amp; Chargeback Protection](https://marketplace.magento.com/signifyd-module-connect.html){:target="_blank"}. Veillez à tenir à jour l’extension conformément aux directives du fournisseur.

## Résolution des problèmes liés aux ressources

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

Pour obtenir de l’aide sur la résolution des problèmes de paiement, consultez la [Base de connaissances du support technique](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html?lang=fr).

[1]: https://marketplace.magento.com/catalogsearch/result?q=fraud%20protection
