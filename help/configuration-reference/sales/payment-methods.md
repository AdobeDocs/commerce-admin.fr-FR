---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] de l’administrateur Commerce.
exl-id: 6545b980-c8ef-460a-a884-d5315f5ad513
feature: Configuration, Payments
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '1653'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods]

>[!TIP]
>
>Les services de paiement pour Adobe Commerce et Magento Open Source fournissent une solution de libre-service clé en main, notamment des tests d’environnement de test et une configuration simple, pour fournir un traitement de paiement robuste et sécurisé. Pour en savoir plus sur cet ensemble d’outils puissant et sur la manière dont il peut vous donner les informations et le contrôle dont vous avez besoin pour créer la meilleure expérience pour vos acheteurs, consultez le [_Guide de l’utilisateur des services de paiement_](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html).

{{config}}

## [!UICONTROL Merchant Location]

![Emplacement du site marchand](./assets/payment-methods-merchant-location.png)<!-- zoom -->

<!-- [Merchant Location](https://experienceleague.adobe.com/en/docs/commerce-admin/start/setup/store-details#merchant-location) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Merchant Country] | Site Web | Identifie le pays dans lequel le commerçant est enregistré pour mener une activité commerciale. |

{style="table-layout:auto"}

## Solutions recommandées

Les solutions de paiement suivantes sont recommandées pour les marchands qui commencent tout juste à accepter le paiement en ligne par compte ou carte de crédit PayPal. Au fur et à mesure que votre entreprise se développe, vous pouvez combiner ces solutions avec des solutions de paiement PayPal supplémentaires.

- [Passage en caisse express PayPal](paypal-express-checkout.md)
- [Braintree](braintree.md)
- [Services de paiement](payment-services.md)

>[!NOTE]
>
>Certaines intégrations de paiement et extensions groupées ont été supprimées dans les versions 2.4.x et déplacées vers Commerce Marketplace. Vous trouverez les dernières extensions officielles d’intégration des paiements dans [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target="_blank"}.
><br/>
>**Amazon Pay** et **Klarna** : Adobe Commerce et les versions Magento Open Sources 2.4.0 à 2.4.3 incluaient ces extensions développées par des fournisseurs. À compter de la version 2.4.4, ces extensions ne sont plus incluses dans la version principale et doivent être installées et mises à jour à partir du Commerce Marketplace . Le Marketplace permet également d’accéder à la documentation actuelle fournie par le développeur de l’extension.
><br/>
>Si l’une de ces extensions groupées est activée et configurée, vous devez mettre à jour votre fichier `composer.json` dans le cadre du processus de mise à niveau 2.4.4 et gérer les mises à jour d’extension à l’avenir. Voir [Mise à niveau des modules](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) dans le _Guide de mise à niveau_ pour plus d’informations.<br/>
><br/>
>**Worldpay**, **Eway**, **CyberSource** et **Authorize.Net** : pour plus d&#39;informations sur la transition sécurisée à partir de ces intégrations de paiement, consultez le [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target="_blank"}.

## Autres méthodes PayPal

PayPal propose différentes solutions de paiement qui répondent aux besoins des entreprises de toutes tailles et qui sont actives dans le monde entier. PayPal vous permet d&#39;accepter les paiements de toutes les principales cartes de débit et de crédit. PayPal offre des avantages supplémentaires sans effort supplémentaire, car même les clients qui n&#39;ont pas de compte PayPal peuvent payer leurs achats avec PayPal.

### Méthodes tout-en-un PayPal

- [Paiement PayPal avancé](paypal-payments-advanced.md)
- [PayPal payment Pro](paypal-payments-pro.md)
- [PayPal payment Standard](paypal-payments-standard.md)

### Passerelles de paiement PayPal

- [ PayPal Payflow Pro](paypal-payflow-pro.md) (comprend le passage en caisse express)
- [Lien de flux de paiement PayPal](paypal-payflow-link.md) (comprend le passage en caisse express)

## Modes de paiement de base

Les méthodes de paiement suivantes sont intégrées à Commerce et n’utilisent pas de fournisseur de paiement tiers pour traiter la transaction. Beaucoup des méthodes de paiement de base ont été gérées hors ligne, plutôt qu&#39;en ligne.

### [!UICONTROL Check / Money Order]

![Vérifier / Commande d’argent](./assets/payment-methods-check-money-order.png)<!-- zoom -->

<!-- [Check / Money Order](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/payments/offline/check-money-order) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site Web | Détermine si les clients peuvent payer par chèque ou mandat. Options : `Yes` / `No` |
| [!UICONTROL Title] | Affichage en magasin | Nom de ce mode de paiement qui s’affiche pour les clients lors de leur passage en caisse. |
| [!UICONTROL New Order Status] | Site Web | Détermine le [statut de la commande](../../stores-purchase/order-status.md) initial attribué aux commandes payées par un chèque ou un mandat. Valeur par défaut : `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Site Web | Détermine les pays à partir desquels vous acceptez le paiement par chèque ou mandat. Options : `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Site Web | Identifie les pays spécifiques d’où vous acceptez le paiement par chèque ou par mandat. |
| [!UICONTROL Make Check Payable to] | Affichage en magasin | Nom de l’entité à qui les chèques et les mandats doivent être émis. |
| [!UICONTROL Send Check to] | Affichage en magasin | Adresse postale ou boîte de commande où les chèques et les commandes doivent être envoyés. |
| [!UICONTROL Minimum Order Total] | Site Web | Montant le plus petit de la commande qui peut être payé par chèque ou mandat. |
| [!UICONTROL Maximum Order Total] | Site Web | Montant de la commande la plus importante pouvant être payé par chèque ou mandat. <br/><br/>**_Remarque :_**Une commande est admissible si le total est compris entre le total de la commande ou correspond au total de la commande minimale ou maximale. |
| [!UICONTROL Sort Order] | Site Web | Numéro qui détermine la commande que le paiement par chèque ou par bon de commande apparaît lorsqu’il est répertorié avec d’autres méthodes de paiement lors du passage en caisse. Saisissez `0` pour le placer en haut de la liste. |

{style="table-layout:auto"}

### [!UICONTROL Bank Transfer Payment]

![Paiement de transfert de banque](./assets/payment-methods-bank-transfer-payment.png)<!-- zoom -->

<!-- [Bank Transfer Payment](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/payments/offline/bank-transfer) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site Web | Détermine si les clients peuvent payer en transférant directement le paiement de leur banque vers votre compte marchand. Options : `Yes` / `No` |
| [!UICONTROL Title] | Affichage en magasin | Nom de ce mode de paiement qui s’affiche pour les clients lors de leur passage en caisse. |
| [!UICONTROL New Order Status] | Site Web | Détermine l’état initial de la commande attribuée aux commandes payées par transfert bancaire. Valeur par défaut : `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Site Web | Détermine les pays d’où vous acceptez le paiement par transfert bancaire. Options : `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Site Web | Identifie les pays spécifiques d’où vous acceptez le paiement par transfert bancaire. |
| [!UICONTROL Minimum Order Total] | Site Web | Le plus petit montant de commande qui peut être payé par transfert bancaire. |
| [!UICONTROL Maximum Order Total] | Site Web | Montant de la commande la plus importante pouvant être payé par transfert bancaire. <br/><br/>**_Remarque :_**Une commande est admissible si le total est compris entre le total de la commande ou correspond au total de la commande minimale ou maximale. |
| [!UICONTROL Sort Order] | Site Web | Numéro qui détermine la commande selon laquelle le paiement par transfert bancaire s’affiche lorsqu’il est répertorié avec d’autres méthodes de paiement lors du passage en caisse. Saisissez `0` pour le placer en haut de la liste. |

{style="table-layout:auto"}

### [!UICONTROL Payment on Account]

{{b2b-feature}}

![Paiement sur compte](./assets/payment-methods-payment-on-account.png)<!-- zoom -->

<!-- [Payment on Account](https://experienceleague.adobe.com/en/docs/commerce-admin/b2b/enable-basic-features#configure-payment-on-account) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site Web | Détermine si les entreprises peuvent utiliser le crédit de la société pour effectuer des achats. Options : `Yes` / `No` |
| [!UICONTROL Title] | Affichage en magasin | Nom de ce mode de paiement qui s’affiche pour les clients lors de leur passage en caisse. |
| [!UICONTROL New Order Status] | Site Web | Détermine l’état des nouvelles commandes imputées à un compte de société. Options : `Pending (default)` / `Processing` / `Suspected Fraud` |
| [!UICONTROL Payment from Applicable Countries] | Site Web | Détermine les pays dans lesquels vous autorisez les entreprises à facturer des achats à leurs comptes. Options : `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Site Web | Identifie les pays spécifiques où les entreprises peuvent facturer des achats à leurs comptes. |
| [!UICONTROL Minimum Order Total] | Site Web | Indique le montant de commande le plus petit qui peut être imputé à un compte d’entreprise. |
| [!UICONTROL Maximum Order Total] | Site Web | Montant de commande le plus important pouvant être imputé à un compte de société. <br/><br/>**_Remarque :_**Une commande est admissible si le total est compris entre le total de la commande ou correspond au total de la commande minimale ou maximale. |
| [!UICONTROL Sort Order] | Site Web | Numéro qui détermine la commande selon laquelle le paiement sur le compte apparaît lorsqu’il est répertorié avec d’autres méthodes de paiement lors du passage en caisse. Saisissez `0` pour le placer en haut de la liste. |

{style="table-layout:auto"}

>[!NOTE]
>
>Le paiement sur compte n’est pas pris en charge pour les commandes comportant [ plusieurs adresses de livraison ](../../stores-purchase/shipping-settings.md#multiple-addresses) et n’apparaît pas parmi les options de paiement.

### [!UICONTROL Cash On Delivery Payment]

![Paiement en espèces à la livraison](./assets/payment-methods-cash-on-delivery-payment.png)<!-- zoom -->

<!-- [Cash On Delivery Payment](../../stores-purchase/cash-on-delivery.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site Web | Détermine si les clients peuvent payer en transférant directement le paiement de leur banque vers votre compte marchand. Options : `Yes` / `No` |
| [!UICONTROL Title] | Affichage en magasin | Nom de ce mode de paiement qui s’affiche pour les clients lors de leur passage en caisse. |
| [!UICONTROL New Order Status] | Site Web | Détermine l’état initial de la commande attribuée aux commandes payées par transfert bancaire. Valeur par défaut : `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Site Web | Détermine les pays d’où vous acceptez le paiement par transfert bancaire. Options : `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Site Web | Identifie les pays spécifiques d’où vous acceptez le paiement par transfert bancaire. |
| [!UICONTROL Minimum Order Total] | Site Web | Indique le montant de commande le plus petit qui peut être payé par transfert bancaire. |
| [!UICONTROL Maximum Order Total] | Site Web | Montant de la commande la plus importante pouvant être payé par transfert bancaire. <br/><br/>**_Remarque :_**Une commande est admissible si le total est compris entre le total de la commande ou correspond au total de la commande minimale ou maximale. |
| [!UICONTROL Sort Order] | Site Web | Numéro qui détermine la commande selon laquelle le paiement par transfert bancaire s’affiche lorsqu’il est répertorié avec d’autres méthodes de paiement lors du passage en caisse. Saisissez `0` pour le placer en haut de la liste. |

{style="table-layout:auto"}

### [!UICONTROL Zero Subtotal Checkout]

![Zéro passage en caisse sous-total](./assets/payment-methods-zero-subtotal-checkout.png)<!-- zoom -->

<!-- [Zero Subtotal Checkout](../../stores-purchase/zero-subtotal-checkout.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Title] | Affichage en magasin | Nom utilisé pour ce mode de paiement lors du passage en caisse. Valeur par défaut : aucune information de paiement requise |
| [!UICONTROL Enabled] | Site Web | Détermine si le sous-total zéro est disponible pour l’administrateur du magasin afin de gérer les commandes dont le sous-total est nul, par exemple une commande qui a été imposée, mais qu’une remise a réduit le montant à zéro. Options : `Yes` / `No` |
| [!UICONTROL New Order Status] | Site Web | Détermine l’état de la commande initiale attribuée aux commandes traitées en tant que passage en caisse du sous-total zéro. Valeur par défaut : `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Site Web | Détermine les pays à partir desquels le passage en caisse du sous-total zéro peut être appliqué. Options : `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Site Web | Identifie les pays spécifiques pour lesquels un passage en caisse partiel zéro peut être appliqué. |
| [!UICONTROL Sort Order] | Site Web | Numéro qui détermine l’ordre dans lequel le titre, par exemple &quot;Aucune information de paiement n’est requise&quot;, s’affiche lorsqu’il est répertorié avec d’autres méthodes de paiement lors de l’extraction. Saisissez `0` pour le placer en haut de la liste. |

{style="table-layout:auto"}

## [!UICONTROL Payment actions]

Les actions de paiement sont configurées _par mode de paiement_. L’action de paiement détermine le moment où les fonds sont capturés et où des factures sont créées pour vos commandes client.

Consultez la section Paramètres de base de chaque rubrique de mode de paiement individuel pour obtenir une liste complète des options de configuration individuelles.

| Action de paiement | Description |
|--- |---|
| [!UICONTROL Authorization] | Approuve l’achat, mais met la main sur les fonds. Le montant n’est pas retiré tant que le marchand ne l’a pas capturé. |
| [!UICONTROL Authorize] | Autorise le compte de l’acheteur pour le total de la commande, mais ne capture pas le paiement. Effectuez le paiement en créant une facture. Les commandes autorisées peuvent être annulées ou annulées. |
| [!UICONTROL Authorize and Capture] | Autorise le compte de l’acheteur pour le total de la commande et capture le paiement. Une facture est automatiquement créée. Vous pouvez rembourser les fonds capturés par l’intermédiaire d’un avoir à vue. Vous ne pouvez pas annuler une commande une fois le paiement capturé. |
| [!UICONTROL Charge on shipment] | Amazon reçoit une demande de capture et facture le client lorsqu&#39;une facture est créée dans Commerce. |
| [!UICONTROL Charge on order] | Amazon crée la facture et facture le client lors de la commande. |
| [!UICONTROL Not Capture] | Lorsque la facture est envoyée, le système ne récupère pas le paiement. Nous partons du principe que vous récupérez le paiement par l’intermédiaire de Commerce ultérieurement. La facture terminée comporte un bouton Capturer . Avant de procéder à l&#39;acquisition, vous pouvez annuler la facture. Après l’acquisition, vous pouvez créer un avoir et annuler la facture. |
| [!UICONTROL Order] | Représente un accord avec PayPal qui permet au marchand de capturer un ou plusieurs montants au total de la commande à partir du compte de l’acheteur du client, dans une période définie (jusqu’à 29 jours). |
| [!UICONTROL Sale] | Le montant de l&#39;achat est autorisé et immédiatement retiré du compte du client. |

{style="table-layout:auto"}

>[!NOTE]
>
>Ne sélectionnez pas l’option _[!UICONTROL Not Capture]_, sauf si vous êtes certain que vous allez capturer le paiement par Commerce ultérieurement. Vous ne pouvez pas créer d’avoir tant que le paiement n’a pas été capturé à l’aide du bouton Capturer .

## [!UICONTROL Purchase Order]

![Bon de commande](./assets/payment-methods-purchase-order.png)<!-- zoom -->

<!-- [Purchase Order](../../stores-purchase/purchase-order.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site Web | Détermine si les clients peuvent payer par bon de commande. Options : `Yes` / `No` |
| [!UICONTROL Title] | Affichage en magasin | Nom de ce mode de paiement qui s’affiche pour les clients lors de leur passage en caisse. |
| [!UICONTROL New Order Status] | Site Web | Détermine le [statut de commande](../../stores-purchase/order-status.md) initial attribué aux commandes payées par le bon de commande. Valeur par défaut : En attente |
| [!UICONTROL Payment from Applicable Countries] | Site Web | Détermine les pays à partir desquels vous acceptez le paiement par bon de commande. Options : `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Site Web | Identifie les pays spécifiques d’où vous acceptez le paiement par bon de commande. |
| [!UICONTROL Minimum Order Total] | Site Web | Montant de commande le plus petit qui peut être payé par le bon de commande. |
| [!UICONTROL Maximum Order Total] | Site Web | Montant de commande le plus élevé qui peut être payé par le bon de commande. <br/><br/>**_Remarque :_**Une commande est admissible si le total est compris entre le total de la commande ou correspond au total de la commande minimale ou maximale. |
| [!UICONTROL Sort Order] | Site Web | Numéro qui détermine la commande que le paiement par bon de commande apparaît lorsqu’il est répertorié avec d’autres méthodes de paiement lors du passage en caisse. Saisissez `0` pour le placer en haut de la liste. |

{style="table-layout:auto"}
