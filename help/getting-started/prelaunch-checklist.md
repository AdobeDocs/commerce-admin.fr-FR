---
title: Liste de contrôle de relance
description: Utilisez cette liste pour vérifier les paramètres de configuration requis afin de vous assurer que tout est correct avant que votre magasin ne passe en production.
exl-id: 649809c2-7217-4274-b365-c682bfff24ba
feature: Site Management, System
role: Admin, Leader
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---

# Liste de contrôle de relance

Une fois que vous avez terminé la conception, le développement et le test de votre magasin, vérifiez les paramètres de configuration suivants pour vous assurer que tout est correct avant que le magasin _ne soit actif_. Pour une description complète de chaque paramètre de configuration, voir la [_référence de configuration_](../configuration-reference/guide-overview.md).

## Paramètres généraux

- [URL de magasin](../stores-purchase/store-urls.md) - Vérifiez que les URL de magasin pour le storefront et l’administrateur sont correctes pour un environnement de production actif.
- Certificat de sécurité : avant de lancer votre boutique, installez un certificat de sécurité entièrement signé et approuvé pour le domaine spécifié dans l’URL de base.
- [Stocker les adresses électroniques](../getting-started/store-details.md#store-email-addresses) : renseignez toutes les adresses électroniques utilisées pour envoyer et recevoir des notifications par e-mail, telles que de nouvelles commandes, factures, envois, notes de crédit, alertes de prix des produits et newsletters. Assurez-vous que chaque champ contient une adresse électronique professionnelle valide.

## Paramètres marketing

- [Modèles d’email](../systems/email-templates.md) - Mettez à jour les modèles d’email par défaut pour refléter votre marque. Veillez à mettre à jour la configuration si vous créez des modèles.
- [Communications commerciales](../stores-purchase/introduction.md#order-management-and-operations) - Assurez-vous que vos factures et vos bordereaux d’emballage contiennent les informations commerciales correctes et reflètent votre marque.
- [Outils Google](../merchandising-promotions/google-tools.md) - [!DNL Commerce] fournit une intégration à l’API Google pour permettre à votre entreprise d’utiliser des Google Analytics et des AdWords Google.

## Paramètres des ventes

- [Options de panier](../stores-purchase/cart-configuration.md) - Examinez les paramètres de configuration du panier pour voir si vous souhaitez apporter des modifications, comme la définition du montant minimum de commande et de la durée de vie des prix dans le panier.
- [Options de passage en caisse](../stores-purchase/checkout-process.md#checkout-options) - Examinez les options de passage en caisse pour voir si vous souhaitez apporter des modifications, par exemple la configuration des conditions générales et la configuration du passage en caisse des invités.
- [Taxes](../stores-purchase/taxes.md) - Assurez-vous que les taxes sont correctement configurées en fonction de vos règles fiscales et de vos besoins locaux.
- [Méthodes de diffusion](../stores-purchase/delivery.md) - Permet à tous les opérateurs et méthodes de diffusion d’être utilisés par l’entreprise.
- [PayPal](../stores-purchase/paypal.md) - Si vous envisagez d’offrir à vos clients la possibilité de payer avec PayPal, ouvrez un compte marchand PayPal et configurez un mode de paiement. Exécutez certaines transactions de test en mode sandbox avant que le magasin ne soit mis en service.
- [Méthodes de paiement](../stores-purchase/payments.md) - Activez les méthodes de paiement que vous prévoyez d’utiliser et assurez-vous qu’elles sont correctement configurées. Vérifiez les paramètres d’état de la commande, la devise acceptée, les pays autorisés, etc.

## Paramètres système

[Cron (tâches planifiées)](../systems/cron.md) - Les tâches Cron sont utilisées pour traiter les e-mails, les règles de prix de catalogue, les newsletters, les alertes client, les plans de site Google, mettre à jour les taux de change, etc. Assurez-vous que les tâches Cron sont définies pour s’exécuter à l’intervalle de temps approprié, en minutes.
