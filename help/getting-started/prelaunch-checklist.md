---
title: Liste de contrôle de prélancement
description: Utilisez cette liste pour vérifier les paramètres de configuration requis afin de vous assurer que tout est correct avant que votre magasin ne passe en production.
exl-id: 649809c2-7217-4274-b365-c682bfff24ba
feature: Site Management, System
role: Admin, Leader
TQID: https://experienceleague.adobe.com/cthgB115wuL6ewlKBtfOXwfqevj2jpbdARQHB9pvIcc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 416
ht-degree: 0%

---

# Liste de contrôle de prélancement

Une fois la conception, le développement et les tests de votre boutique terminés, vérifiez les paramètres de configuration suivants pour vous assurer que tout est correct avant que la boutique _ne soit activée_. Pour une description complète de chaque paramètre de configuration, consultez le [_Guide de référence de configuration_](../configuration-reference/guide-overview.md).

## Paramètres généraux

- [URL de magasin](../stores-purchase/store-urls.md) - Vérifiez que les URL de magasin pour le storefront et l’administrateur sont correctes pour un environnement de production en ligne.
- Certificat de sécurité - Avant de lancer votre boutique, installez un certificat de sécurité signé et approuvé à 100 % pour le domaine spécifié dans l’URL de base.
- [Adresses e-mail de la boutique](../getting-started/store-details.md#store-email-addresses) - Renseignez toutes les adresses e-mail utilisées pour envoyer et recevoir des notifications par e-mail, telles que les nouvelles commandes, les factures, les expéditions, les avoirs, les alertes de prix de produit et les newsletters. Assurez-vous que chaque champ contient une adresse e-mail professionnelle valide.

## Paramètres marketing

- [Modèles d’e-mail](../systems/email-templates.md) - Mettez à jour les modèles d’e-mail par défaut pour refléter votre marque. Veillez à mettre à jour la configuration si vous créez des modèles.
- [Communications commerciales](../stores-purchase/introduction.md#order-management-and-operations) - Assurez-vous que vos factures et vos bons de livraison comprennent les bons renseignements commerciaux et reflètent votre marque.
- [Outils Google &#x200B;](../merchandising-promotions/google-tools.md) - [!DNL Commerce] intègre l’API Google pour permettre à votre entreprise d’utiliser Google Analytics et Google AdWords.

## Paramètres des ventes

- [Options du panier](../stores-purchase/cart-configuration.md) - Examinez les paramètres de configuration du panier pour voir si vous souhaitez modifier des éléments, tels que la définition du montant de commande minimal et de la durée de vie des prix du panier.
- [Options de passage en caisse](../stores-purchase/checkout-process.md#checkout-options) - Examinez les options de passage en caisse pour voir si vous souhaitez modifier des éléments, tels que la configuration des termes et conditions et la configuration de la passage en caisse des invités.
- [Taxes](../stores-purchase/taxes.md) - Assurez-vous que les taxes sont correctement configurées en fonction des règles fiscales de votre entreprise et des exigences locales.
- [Modes de livraison](../stores-purchase/delivery.md) - Activez tous les transporteurs et modes de livraison à utiliser par la société.
- [PayPal](../stores-purchase/paypal.md) - Si vous prévoyez d&#39;offrir à vos clients la possibilité de payer avec PayPal, ouvrez un compte marchand PayPal et configurez un mode de paiement. Exécutez des transactions de test en mode Sandbox avant la mise en ligne du magasin.
- [Modes de paiement](../stores-purchase/payments.md) - Activez les modes de paiement que vous prévoyez d’utiliser et vérifiez qu’ils sont correctement configurés. Vérifiez les paramètres de statut de la commande, la devise acceptée, les pays autorisés, etc.

## Paramètres système

[Cron (tâches planifiées)](../systems/cron.md) - Les tâches Cron sont utilisées pour traiter les e-mails, les règles de prix de catalogue, les newsletters, les alertes clients, les plans de site Google, la mise à jour des taux de change, etc. Assurez-vous que les tâches cron sont définies pour s’exécuter à l’intervalle de temps approprié, en minutes.
