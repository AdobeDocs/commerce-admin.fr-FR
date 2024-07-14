---
title: Présentation des paiements
description: Découvrez les méthodes de paiement et les services pris en charge en mode natif dans Adobe Commerce et Magento Open Source.
exl-id: 474bf6df-96e2-4db3-ad3c-1804b5de33b0
feature: Payments
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 0%

---

# Présentation des paiements

Adobe Commerce et Magento Open Source prennent en charge divers modes de paiement et services que vous pouvez proposer pour faciliter le passage en caisse et faciliter la commodité du client. Cette liste comprend plusieurs modes de paiement hors ligne, dont le paiement par chèque ou par mandat, et l&#39;encaisse à la livraison (DCO). Il existe également des intégrations natives pour de nombreuses solutions de paiement en ligne et passerelles, dont Braintree en tant qu’extension groupée développée par les fournisseurs.

>[!TIP]
>
>Les services de paiement pour Adobe Commerce et Magento Open Source fournissent une solution de libre-service clé en main, notamment des tests d’environnement de test et une configuration simple, pour fournir un traitement de paiement robuste et sécurisé. Pour en savoir plus sur cet ensemble d’outils puissant et sur la manière dont il peut vous donner les informations et le contrôle dont vous avez besoin pour créer la meilleure expérience pour vos acheteurs, consultez le [Guide de l’utilisateur des services de paiement](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html).

>[!NOTE]
>
>Passez en revue les [directives de conformité PCI](../getting-started/compliance-pci.md) qui décrivent les exigences définies par le secteur des cartes de paiement (PCI) pour les entreprises qui acceptent le paiement par carte de crédit sur Internet.

## Changements dans la version 2.4

Certaines intégrations de paiement et extensions groupées ont été supprimées dans les versions 2.4.x et déplacées vers Commerce Marketplace. Vous trouverez les dernières extensions officielles d’intégration des paiements dans [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target=&quot;_blank&quot;}.

- **Amazon Pay** et **Klarna** : les versions Adobe Commerce et Magento Open Source 2.4.0 à 2.4.3 incluaient ces extensions développées par des fournisseurs. À compter de la version 2.4.4, ces extensions ne sont plus incluses dans la version principale et doivent être installées et mises à jour à partir du Commerce Marketplace . Le Marketplace permet également d’accéder à la documentation actuelle fournie par le développeur de l’extension.

  Si l’une de ces extensions groupées est activée et configurée, vous devez mettre à jour votre fichier compositeur.json dans le cadre du processus de mise à niveau 2.4.4 et gérer les mises à jour d’extension à l’avenir. Pour plus d’informations, voir [Mise à niveau de modules](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) dans le _Guide de mise à niveau_ .

- **Worldpay**, **Eway**, **CyberSource** et **Authorize.Net** : pour plus d&#39;informations sur la transition sécurisée à partir de ces intégrations de paiement, consultez le [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target=&quot;_blank&quot;}.

## Méthodes de paiement hors ligne

Adobe Commerce et Magento Open Source incluent plusieurs méthodes de paiement hors ligne intégrées, qui ne nécessitent pas les services d’une société de traitement de paiement tierce :

- [Achat de sous-total nul](zero-subtotal-checkout.md)
- [Paiement en espèces à la livraison](cash-on-delivery.md)
- [Paiement de transfert bancaire](bank-transfer.md)
- [Vérifier / Commande monétaire](check-money-order.md)
- [Bon de commande](purchase-order.md)
- [ Paiement sur le compte ](../b2b/enable-basic-features.md#configure-payment-on-account) ![Adobe Commerce B2B](../assets/b2b.svg) (Disponible avec Adobe Commerce B2B)

## Méthodes de paiement en ligne

Adobe Commerce et Magento Open Source prennent en charge de nombreuses solutions de paiement qui offrent des services commerciaux dans toutes les régions du monde. Contrairement aux solutions de paiement qui transfèrent le contrôle vers un autre site pour terminer la transaction, une passerelle de paiement vous permet d’accepter les paiements par carte de crédit directement depuis votre boutique sans que le client ne quitte votre site.

### Solutions recommandées

- [Services de paiement](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html)
- [Passage en caisse express PayPal](paypal-express-checkout.md)
- [Braintree](braintree.md)

### Autres solutions de paiement PayPal

Pour plus d’informations sur les options de mode de paiement PayPal, voir [Solutions de paiement PayPal](paypal.md) .

#### Solutions tout-en-un PayPal

- [Paiements avancés de PayPal](paypal-payments-advanced.md)
- [PayPal payment Pro](paypal-payments-pro.md)
- [PayPal payment Standard](paypal-payments-standard.md)

#### Passerelles de paiement PayPal

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [Lien de flux de production PayPal](paypal-payflow-link.md)

## Protection contre les fraudes

Les services et filtres de protection contre les fraudes examinent les commandes envoyées avant le traitement de la transaction afin de détecter les commandes frauduleuses et de vous protéger des frais de rebonds. Adobe Commerce et Magento Open Source prennent en charge les solutions de protection contre la fraude suivantes :

- [Filtre de gestion des fraudes PayPal](paypal.md#paypal-fraud-management-filters)

- [ Solutions de protection contre la fraude sur Marketplace][1]

>[!NOTE]
>
>Pour prendre en charge les mises à jour relatives à la conformité en matière de sécurité, la protection de la fraude Signifyd est supprimée de Commerce à compter de la version 2.4.0. Si vous avez utilisé l’intégration Signifyd dans une version 2.3.x ou antérieure, il est recommandé de passer à l’[extension Signifyd Fraud &amp; Chargeback Protection](https://marketplace.magento.com/signifyd-module-connect.html){:target=&quot;_blank&quot;}. Veillez à mettre à jour l’extension conformément aux directives du fournisseur.

## Ressources de dépannage

Pour obtenir de l’aide sur la résolution des problèmes de paiement, consultez la [base de connaissances de l’assistance](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html?lang=en).

[1]: https://marketplace.magento.com/catalogsearch/result?q=fraud%20protection
