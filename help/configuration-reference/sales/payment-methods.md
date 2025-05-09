---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods]'
description: Vérifiez les paramètres de configuration sur la page de [!UICONTROL Payment Methods] d’[!UICONTROL Sales] &gt; de l’administrateur Commerce.
exl-id: 6545b980-c8ef-460a-a884-d5315f5ad513
feature: Configuration, Payments
source-git-commit: 489c72652693a15ffe1c745277bbaa9da084dcba
workflow-type: tm+mt
source-wordcount: '1772'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods]

>[!TIP]
>
>Payment Services pour Adobe Commerce et Magento Open Source offre une solution en libre-service clé en main, y compris les tests de sandbox et une configuration simple, pour offrir un traitement des paiements robuste et sécurisé. Pour en savoir plus sur cet ensemble d&#39;outils puissants et sur la manière dont il peut vous fournir l&#39;insight et le contrôle dont vous avez besoin pour offrir la meilleure expérience à vos acheteurs, consultez le [_Guide d&#39;utilisation des services de paiement_](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html).

{{config}}

## [!UICONTROL Merchant Location]

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

![Emplacement du commerçant](./assets/payment-methods-merchant-location.png)<!-- zoom -->

<!-- [Merchant Location](https://experienceleague.adobe.com/en/docs/commerce-admin/start/setup/store-details#merchant-location) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Merchant Country] | Site internet | Indique le pays dans lequel le commerçant est inscrit pour exercer ses activités. |

{style="table-layout:auto"}

## Solutions recommandées

Les solutions de paiement suivantes sont recommandées comme un moyen facile pour les commerçants qui commencent tout juste à accepter le paiement en ligne par compte PayPal ou carte de crédit. Au fur et à mesure que votre entreprise se développe, vous pouvez les combiner avec d&#39;autres solutions de paiement PayPal.

- [Services de paiement](payment-services.md)
- [!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."} [PayPal Express Checkout](paypal-express-checkout.md)
- [!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."} [Braintree](braintree.md)

>[!NOTE]
>
>Certaines intégrations de paiements et extensions groupées ont été supprimées dans les versions 2.4.x et déplacées vers Commerce Marketplace. Retrouvez les dernières extensions officielles d&#39;intégration des paiements dans [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target="_blank"}.
><br/>
>**Amazon Pay** et **Klarna** : les versions 2.4.0 à 2.4.3 d’Adobe Commerce et Magento Open Source incluaient ces extensions développées par le fournisseur. À compter de la version 2.4.4, ces extensions ne sont plus incluses dans la version de base et doivent être installées et mises à jour à partir de Commerce Marketplace. La Marketplace permet également d’accéder à la documentation actuelle fournie par le développeur d’extensions.
><br/>
>Si l’une de ces extensions groupées est activée et configurée, vous devez mettre à jour votre fichier `composer.json` dans le cadre du processus de mise à niveau vers la version 2.4.4 et pour gérer les mises à jour d’extension à l’avenir. Pour plus d’informations, consultez [Mise à niveau des modules](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) dans le _Guide de mise à niveau_.<br/>
><br/>
>**Worldpay**, **Eway**, **CyberSource** et **Authorize.Net** : pour plus d’informations sur la manière d’effectuer une transition sécurisée depuis ces intégrations de paiement, consultez le [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target="_blank"}.

## Autres méthodes PayPal

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

PayPal propose diverses solutions de paiement qui répondent aux besoins des entreprises de toutes tailles, et qui sont engagées dans les affaires partout dans le monde. PayPal vous donne la possibilité d&#39;accepter les paiements de toutes les principales cartes de débit et de crédit. PayPal offre un confort supplémentaire sans effort supplémentaire, car même les clients qui n&#39;ont pas de compte PayPal peuvent payer leurs achats avec PayPal.

### Méthodes tout-en-un PayPal

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

- [Paiement PayPal avancé](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [Paiements PayPal Standard](paypal-payments-standard.md)

### Passerelles de paiement PayPal

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

- [PayPal Payflow Pro](paypal-payflow-pro.md) (avec paiement express)
- [Lien de flux de paiement PayPal](paypal-payflow-link.md) (comprend le paiement express)

## Modes de paiement de base

Les modes de paiement ci-après sont intégrés à Commerce et ne font pas appel à un prestataire de services de paiement tiers pour traiter la transaction. La plupart des méthodes de paiement de base sont gérées hors ligne, plutôt qu’en ligne.

### [!UICONTROL Check / Money Order]

![Chèque / Mandat](./assets/payment-methods-check-money-order.png)<!-- zoom -->

<!-- [Check / Money Order](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/payments/offline/check-money-order) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site internet | Détermine si les clients peuvent payer par chèque ou mandat. Options : `Yes` / `No` |
| [!UICONTROL Title] | Affichage de la boutique | Nom de ce mode de paiement qui apparaît aux clients lors du passage en caisse. |
| [!UICONTROL New Order Status] | Site internet | Détermine le statut initial [commande](../../stores-purchase/order-status.md) attribué aux commandes payées par chèque ou mandat. Valeur par défaut : `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Site internet | Détermine les pays d&#39;où vous acceptez le paiement par chèque ou mandat. Options : `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Site internet | Indique les pays spécifiques à partir desquels vous acceptez le paiement par chèque ou mandat. |
| [!UICONTROL Make Check Payable to] | Affichage de la boutique | Nom de l&#39;entité à laquelle les chèques et les mandats doivent être rendus payables. |
| [!UICONTROL Send Check to] | Affichage de la boutique | Adresse postale ou BP où les chèques et les mandats doivent être envoyés. |
| [!UICONTROL Minimum Order Total] | Site internet | Montant de commande le plus faible pouvant être payé par chèque ou mandat. |
| [!UICONTROL Maximum Order Total] | Site internet | Montant de commande le plus élevé pouvant être payé par chèque ou mandat. <br/><br/>**_Remarque :_**&#x200B;une commande est qualifiée si le total est compris entre le total minimum ou maximum de la commande ou s&#39;il correspond à ce total. |
| [!UICONTROL Sort Order] | Site internet | Nombre qui détermine l&#39;ordre dans lequel le paiement par chèque ou mandat-poste apparaît lorsqu&#39;il est indiqué avec d&#39;autres modes de paiement lors du passage en caisse. Saisissez `0` pour le placer en haut de la liste. |

{style="table-layout:auto"}

### [!UICONTROL Bank Transfer Payment]

![Paiement par virement bancaire](./assets/payment-methods-bank-transfer-payment.png)<!-- zoom -->

<!-- [Bank Transfer Payment](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/payments/offline/bank-transfer) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site internet | Détermine si les clients peuvent payer en transférant le paiement directement de leur banque vers votre compte marchand. Options : `Yes` / `No` |
| [!UICONTROL Title] | Affichage de la boutique | Nom de ce mode de paiement qui apparaît aux clients lors du passage en caisse. |
| [!UICONTROL New Order Status] | Site internet | Détermine le statut initial de commande affecté aux commandes payées par virement bancaire. Valeur par défaut : `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Site internet | Détermine les pays d&#39;où vous acceptez le paiement par virement bancaire. Options : `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Site internet | Indique les pays spécifiques à partir desquels vous acceptez un paiement par virement bancaire. |
| [!UICONTROL Minimum Order Total] | Site internet | Montant de commande le plus faible pouvant être payé par virement bancaire. |
| [!UICONTROL Maximum Order Total] | Site internet | Montant de commande le plus élevé pouvant être payé par virement bancaire. <br/><br/>**_Remarque :_**&#x200B;une commande est qualifiée si le total est compris entre le total minimum ou maximum de la commande ou s&#39;il correspond à ce total. |
| [!UICONTROL Sort Order] | Site internet | Nombre qui détermine l&#39;ordre dans lequel apparaît le paiement par virement bancaire lorsqu&#39;il est indiqué avec d&#39;autres modes de paiement lors du passage en caisse. Saisissez `0` pour le placer en haut de la liste. |

{style="table-layout:auto"}

### [!UICONTROL Payment on Account]

{{b2b-feature}}

![Paiement en compte](./assets/payment-methods-payment-on-account.png)<!-- zoom -->

<!-- [Payment on Account](https://experienceleague.adobe.com/en/docs/commerce-admin/b2b/enable-basic-features#configure-payment-on-account) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site internet | Détermine si les entreprises peuvent utiliser le crédit d&#39;entreprise pour effectuer des achats. Options : `Yes` / `No` |
| [!UICONTROL Title] | Affichage de la boutique | Nom de ce mode de paiement qui apparaît aux clients lors du passage en caisse. |
| [!UICONTROL New Order Status] | Site internet | Détermine le statut des nouvelles commandes imputées à un compte de société. Options : `Pending (default)` / `Processing` / `Suspected Fraud` |
| [!UICONTROL Payment from Applicable Countries] | Site internet | Détermine les pays dans lesquels vous autorisez les sociétés à imputer les achats sur leurs comptes. Options : `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Site internet | Identifie les pays spécifiques dans lesquels les entreprises peuvent imputer les achats sur leurs comptes. |
| [!UICONTROL Minimum Order Total] | Site internet | Spécifie le plus petit montant de commande pouvant être imputé à un compte société. |
| [!UICONTROL Maximum Order Total] | Site internet | Montant de commande le plus élevé pouvant être imputé à un compte d’entreprise. <br/><br/>**_Remarque :_**&#x200B;une commande est qualifiée si le total est compris entre le total minimum ou maximum de la commande ou s&#39;il correspond à ce total. |
| [!UICONTROL Sort Order] | Site internet | Nombre qui détermine l&#39;ordre dans lequel apparaît le paiement en compte lorsqu&#39;il est indiqué avec d&#39;autres modes de paiement lors du passage en caisse. Saisissez `0` pour le placer en haut de la liste. |

{style="table-layout:auto"}

>[!NOTE]
>
>Le paiement en compte n’est pas pris en charge pour les commandes avec [plusieurs adresses d’expédition](../../stores-purchase/shipping-settings.md#multiple-addresses) et n’apparaît pas parmi les options de paiement.

### [!UICONTROL Cash On Delivery Payment]

![Paiement À La Livraison](./assets/payment-methods-cash-on-delivery-payment.png)<!-- zoom -->

<!-- [Cash On Delivery Payment](../../stores-purchase/cash-on-delivery.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site internet | Détermine si les clients peuvent payer en transférant le paiement directement de leur banque vers votre compte marchand. Options : `Yes` / `No` |
| [!UICONTROL Title] | Affichage de la boutique | Nom de ce mode de paiement qui apparaît aux clients lors du passage en caisse. |
| [!UICONTROL New Order Status] | Site internet | Détermine le statut initial de commande affecté aux commandes payées par virement bancaire. Valeur par défaut : `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Site internet | Détermine les pays d&#39;où vous acceptez le paiement par virement bancaire. Options : `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Site internet | Indique les pays spécifiques à partir desquels vous acceptez un paiement par virement bancaire. |
| [!UICONTROL Minimum Order Total] | Site internet | Spécifie le plus petit montant de commande qui peut être payé par virement bancaire. |
| [!UICONTROL Maximum Order Total] | Site internet | Montant de commande le plus élevé pouvant être payé par virement bancaire. <br/><br/>**_Remarque :_**&#x200B;une commande est qualifiée si le total est compris entre le total minimum ou maximum de la commande ou s&#39;il correspond à ce total. |
| [!UICONTROL Sort Order] | Site internet | Nombre qui détermine l&#39;ordre dans lequel apparaît le paiement par virement bancaire lorsqu&#39;il est indiqué avec d&#39;autres modes de paiement lors du passage en caisse. Saisissez `0` pour le placer en haut de la liste. |

{style="table-layout:auto"}

### [!UICONTROL Zero Subtotal Checkout]

![Passage En Caisse Du Sous-Total Zéro](./assets/payment-methods-zero-subtotal-checkout.png)<!-- zoom -->

<!-- [Zero Subtotal Checkout](../../stores-purchase/zero-subtotal-checkout.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Title] | Affichage de la boutique | Nom utilisé pour ce mode de paiement lors du passage en caisse. Valeur par défaut : Aucune information de paiement requise |
| [!UICONTROL Enabled] | Site internet | Détermine si le passage en caisse du sous-total zéro est disponible pour que l&#39;administrateur du magasin puisse gérer les commandes dont le sous-total est égal à zéro, par exemple une commande qui a été taxée, mais pour laquelle une remise a réduit le montant à zéro. Options : `Yes` / `No` |
| [!UICONTROL New Order Status] | Site internet | Détermine le statut initial de la commande affecté aux commandes traitées comme passage en caisse du sous-total zéro. Valeur par défaut : `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Site internet | Détermine les pays à partir desquels le passage en caisse du sous-total zéro peut être appliqué. Options : `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Site internet | Indique les pays spécifiques pour lesquels le passage en caisse du sous-total zéro peut être appliqué. |
| [!UICONTROL Sort Order] | Site internet | Un nombre qui détermine l&#39;ordre dans lequel le titre, tel que « Aucune information de paiement n&#39;est requise », apparaît lorsqu&#39;il est indiqué avec d&#39;autres modes de paiement lors de la commande. Saisissez `0` pour le placer en haut de la liste. |

{style="table-layout:auto"}

## [!UICONTROL Payment actions]

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

Les actions de paiement sont configurées _par mode de paiement_. L&#39;action de paiement détermine à quel moment les fonds sont saisis et quand les factures sont créées pour vos commandes client.

Consultez la section Paramètres de base de chaque mode de paiement pour obtenir une liste complète des options de configuration individuelles.

| Action de paiement | Description |
|--- |---|
| [!UICONTROL Authorization] | Valide l&#39;achat, mais met en attente les fonds. Le montant n&#39;est pas retiré tant qu&#39;il n&#39;est pas saisi par le commerçant. |
| [!UICONTROL Authorize] | Autorise le compte de l&#39;acheteur pour le total de la commande mais ne capture pas le paiement. Saisissez le paiement en créant une facture. Les commandes autorisées peuvent être annulées. |
| [!UICONTROL Authorize and Capture] | Autorise le compte de l&#39;acheteur pour le total de la commande et capture le paiement. Une facture est automatiquement créée. Vous pouvez rembourser les fonds capturés via un avoir. Vous ne pouvez pas annuler une commande une fois que le paiement a été saisi. |
| [!UICONTROL Charge on shipment] | Amazon reçoit une demande de capture et facture le client lors de la création d’une facture dans Commerce. |
| [!UICONTROL Charge on order] | Amazon crée la facture et facture le client au moment de la commande. |
| [!UICONTROL Not Capture] | Lorsque la facture est soumise, le système ne capture pas le paiement. Il est supposé que vous capturez le paiement via Commerce ultérieurement. La facture remplie contient un bouton Capturer. Avant la capture, vous pouvez annuler la facture. Après la capture, vous pouvez créer un avoir et annuler la facture. |
| [!UICONTROL Order] | Représente un accord avec PayPal qui permet au marchand de capturer un ou plusieurs montants jusqu&#39;au total de la commande à partir du compte acheteur du client, dans un délai défini (jusqu&#39;à 29 jours). |
| [!UICONTROL Sale] | Le montant de l&#39;achat est autorisé et immédiatement retiré du compte du client. |

{style="table-layout:auto"}

>[!NOTE]
>
>Ne sélectionnez pas l’option _[!UICONTROL Not Capture]_, sauf si vous êtes certain de pouvoir récupérer le paiement via Commerce ultérieurement. Vous ne pouvez pas créer d&#39;avoir tant que le paiement n&#39;a pas été saisi à l&#39;aide du bouton Capturer.

## [!UICONTROL Purchase Order]

![Bon de commande](./assets/payment-methods-purchase-order.png)<!-- zoom -->

<!-- [Purchase Order](../../stores-purchase/purchase-order.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site internet | Détermine si les clients peuvent payer par bon de commande. Options : `Yes` / `No` |
| [!UICONTROL Title] | Affichage de la boutique | Nom de ce mode de paiement qui apparaît aux clients lors du passage en caisse. |
| [!UICONTROL New Order Status] | Site internet | Détermine le [statut de la commande](../../stores-purchase/order-status.md) initial affecté aux commandes payées par le bon de commande. Valeur par défaut : En attente |
| [!UICONTROL Payment from Applicable Countries] | Site internet | Détermine les pays d&#39;où vous acceptez le paiement par commande. Options : `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Site internet | Indique les pays spécifiques à partir desquels vous acceptez le paiement par commande. |
| [!UICONTROL Minimum Order Total] | Site internet | Montant de commande le plus faible pouvant être payé par le bon de commande. |
| [!UICONTROL Maximum Order Total] | Site internet | Montant de commande le plus élevé pouvant être payé par le bon de commande. <br/><br/>**_Remarque :_**&#x200B;une commande est qualifiée si le total est compris entre le total minimum ou maximum de la commande ou s&#39;il correspond à ce total. |
| [!UICONTROL Sort Order] | Site internet | Nombre qui détermine l&#39;ordre dans lequel le paiement par commande apparaît lorsqu&#39;il est répertorié avec d&#39;autres modes de paiement lors du passage en caisse. Saisissez `0` pour le placer en haut de la liste. |

{style="table-layout:auto"}
