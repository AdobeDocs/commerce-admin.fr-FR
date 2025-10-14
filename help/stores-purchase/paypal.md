---
title: Solutions de paiement PayPal
description: Découvrez les intégrations de solutions de paiement PayPal disponibles pour votre boutique.
exl-id: d447b98e-d30c-4759-9ae0-94ccbeed9ba4
feature: Payments
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '1247'
ht-degree: 0%

---

# Solutions de paiement PayPal

PayPal est un leader mondial des paiements en ligne et un moyen rapide et sécurisé pour vos clients de payer en ligne. La sélection des solutions PayPal disponibles varie selon l&#39;emplacement du commerçant. PayPal Express Checkout et PayPal Payments Standard peuvent être utilisés dans toutes les régions du monde. Pour en savoir plus, voir [Solutions PayPal par pays](#paypal-solutions-by-country).

>[!IMPORTANT]
>
>**Conditions requises pour PSD2 :** <br/>
>À compter du 14 septembre 2019, les banques européennes pourront refuser les paiements qui ne répondent pas aux exigences de [PSD2](../getting-started/compliance-payment-services-directive.md). Pour la plupart des solutions PayPal, aucune action n&#39;est nécessaire pour se conformer à PSD2, car ces exigences sont gérées par PayPal.

## Compte professionnel PayPal

Pour proposer PayPal comme mode de paiement dans votre boutique, vous devez disposer d&#39;un compte PayPal [compte professionnel][1] et/ou d&#39;un [compte PayPal Payflow][2]. Les conditions requises pour le compte sont spécifiées dans la description de chaque solution PayPal. Votre compte marchand PayPal est également utilisé pour gérer les [&#x200B; filtres de fraude](#paypal-fraud-management-filters) appliqués aux achats effectués à partir de votre boutique.

Les clients qui utilisent PayPal Express Checkout ou Express Checkout pour Payflow Pro doivent disposer d&#39;un compte acheteur PayPal. PayPal Payments Standard (Website Payments Standard dans certains pays) peut être utilisé directement ou par l&#39;intermédiaire d&#39;un compte acheteur lorsque le commerçant active _Compte PayPal facultatif_. Par défaut, ce paramètre est activé afin que les clients puissent choisir de saisir leurs informations de carte de crédit ou de créer un compte acheteur avec PayPal. Lorsqu&#39;ils sont désactivés, les clients doivent d&#39;abord créer un compte acheteur PayPal avant d&#39;effectuer un achat.

Website Payments Pro, Website Payments Pro Payflow Edition, Payflow Pro Gateway et Payflow Link exigent que les clients saisissent les informations de carte de crédit lors du passage en caisse.

## Crédit PayPal et PayLater

PayPal PayLater offre à vos clients un accès rapide au financement, afin qu&#39;ils puissent acheter maintenant et payer au fil du temps, sans frais supplémentaires pour vous. Vous n&#39;êtes pas facturé lorsque les clients choisissent les options de crédit PayPal, et vous ne payez que vos frais de transaction PayPal normaux. Pour en savoir plus, consultez le [site web PayPal][3].

Donnez un coup de pouce à vos ventes lorsque vous faites de la publicité sur le financement. PayPal permet de transformer les navigateurs en acheteurs avec un financement avec PayPal PayLater. Vos clients peuvent payer au fil du temps, tandis que vous êtes payé à l&#39;avance, sans frais supplémentaires pour vous. Utilisez les bannières publicitaires PayPal gratuites pour annoncer le financement PayPal comme option de paiement lorsque vos clients passent en caisse avec PayPal. Il a été démontré que le programme PayPal Advertising génère des achats supplémentaires et augmente la taille moyenne des achats de 15 % ou plus.

Vous pouvez facilement ajouter des bannières publicitaires gratuites et prêtes à l&#39;emploi aux pages de votre site et le bouton _Crédit PayPal_ à votre panier lors du passage en caisse pour rappeler à vos clients que le financement est facilement disponible.

>[!NOTE]
>
>À partir de la version 2.4.3, PayPal PayLater est pris en charge dans les déploiements qui incluent PayPal. Cette fonctionnalité permet aux acheteurs de payer une commande par versements bimensuels au lieu de payer le montant total au moment de l’achat. L&#39;expérience de crédit PayPal est obsolète.

Pour les commerçants américains, le crédit PayPal est activé par défaut pour l&#39;option de paiement [PayPal Express Checkout](paypal-express-checkout.md). Pour le désactiver pour ce mode de paiement, consultez la section _Fonctionnalités_ de la [Configuration du paiement PayPal Express](paypal-express-checkout.md#features).

PayPal Credit est désactivé par défaut pour les autres solutions de paiement PayPal, mais peut être activé dans la configuration du mode de paiement pour les solutions de support :

- [Paiements avancés](paypal-payments-advanced.md)
- [Payments Pro](paypal-payments-pro.md)
- [Payments Standard](paypal-payments-standard.md)
- [Payflow Pro](paypal-payflow-pro.md)
- [Lien de flux de production](paypal-payflow-link.md)

>[!IMPORTANT]
>
>Avant de configurer PayPal Credit ou PayPal PayLater pour votre boutique, assurez-vous qu&#39;il est activé dans votre compte marchand PayPal.

## Solutions PayPal intégrées

Avec PayPal et Adobe Commerce, vous pouvez accepter les paiements de toutes les principales cartes de débit et de crédit. PayPal offre un confort supplémentaire sans effort supplémentaire, car même vos clients qui n&#39;ont pas de compte PayPal peuvent payer leurs achats avec PayPal.

>[!NOTE]
>
>Vous ne pouvez pas avoir plus d&#39;une méthode PayPal activée dans votre boutique à la fois, à l&#39;exception de PayPal Express Checkout. PayPal Express Checkout peut être utilisé avec d&#39;autres méthodes de paiement PayPal, à l&#39;exception de PayPal Payments Standard. Si vous modifiez les solutions de paiement, la méthode précédente est désactivée.

### PayPal Express Checkout

[PayPal Express Checkout](paypal-express-checkout.md)

### Solutions de paiement PayPal tout-en-un

Aux États-Unis, PayPal propose les solutions PCI suivantes pour répondre aux besoins de votre entreprise en croissance.

- [Paiements PayPal avancés](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [Paiements PayPal Standard](paypal-payments-standard.md)

![Solutions de paiement PayPal tout-en-un](./assets/paypal-all-in-one.png){width="600" zoomable="yes"}

### Passerelles de paiement PayPal

Une passerelle de paiement est un service commercial fourni par un fournisseur de services d’application de commerce électronique qui autorise le traitement des paiements directs ou par carte de crédit. Ils servent d&#39;intermédiaires entre les clients et les banques.

Les passerelles de paiement sont disponibles dans les environnements en ligne et hors ligne. Les paiements peuvent être acceptés par téléphone, en ligne ou via une application mobile. La transaction est envoyée au système de traitement du fournisseur de services, puis envoyée à la banque du client pour vérification et confirmation. S&#39;il est vérifié, le commerçant reçoit le paiement sans avoir de contact direct avec le compte bancaire du client.

Il existe deux types de passerelles de paiement : directes et hébergées.

- Les passerelles de paiement direct permettent aux utilisateurs de saisir leurs informations de carte sur le site web du magasin.
- Les passerelles de paiement hébergées redirigent les utilisateurs vers une page de paiement hébergée, en dehors du site web du magasin.

La passerelle de paiement assure la sécurité et la protection de toutes les parties impliquées dans une transaction.

PayPal propose deux solutions de passerelle de paiement pour votre entreprise. Vous pouvez laisser PayPal héberger votre passage en caisse sur son site de paiement sécurisé, ou vous pouvez prendre le contrôle de l&#39;ensemble de l&#39;expérience de paiement avec une solution personnalisable.

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [Lien de flux de paiement PayPal](paypal-payflow-link.md)

![Configurer des passerelles de paiement PayPal](./assets/paypal-payment-gateway.png){width="600" zoomable="yes"}

## Filtres de gestion des fraudes PayPal

Les filtres de gestion des fraudes PayPal facilitent la détection et la réponse aux transactions frauduleuses et peuvent être configurés pour signaler, bloquer pour révision ou refuser les paiements plus risqués. Les actions relatives aux valeurs Commerce [état de la commande](order-status.md) ont changé en fonction des paramètres de filtrage des fraudes :

| Action | Résultat |
| --- | --- |
| [!UICONTROL Review] | La commande suspecte reçoit le statut _Révision des règlements_ lors du passage de la commande. Vous pouvez vérifier la commande et approuver ou annuler le paiement dans l&#39;Admin ou du côté PayPal. Lorsque vous cliquez sur **[!UICONTROL Accept Payment]** ou **[!UICONTROL Deny Payment]**, aucune nouvelle transaction pour la commande n&#39;est créée. <br/><br/>Si vous modifiez le statut de la transaction sur le site PayPal, vous devez cliquer sur **[!UICONTROL Get Payment Update]** dans la page Commande de l&#39;administrateur pour appliquer les modifications. Si vous cliquez sur **[!UICONTROL Accept Payment]** ou **[!UICONTROL Deny Payment]**, les modifications apportées sur le site PayPal sont appliquées. |
| [!UICONTROL Deny] | La commande suspecte ne peut pas être passée par le client, car la transaction correspondante est rejetée par PayPal. <br/><br/>Pour refuser le paiement de l’administrateur, cliquez sur **[!UICONTROL Deny Payment]** dans le coin supérieur droit de la page. Le statut de la commande passe à `Canceled`, la transaction est annulée et les fonds sont libérés sur le compte client. Les informations correspondantes sont ajoutées dans la section _[!UICONTROL Comments History]_&#x200B;de la vue de commande. |
| [!UICONTROL Flag] | La commande suspecte obtient le statut `Processing` lorsqu’elle est passée. La transaction correspondante est marquée avec un indicateur dans la liste des transactions du compte marchand. |

{style="table-layout:auto"}

## Solutions PayPal par pays

| Pays | Solution de paiement PayPal |
|--- |--- |
| Australie | [!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Pro Hosted Solution]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Canada | [!DNL PayPal Website Payments Standard]<br/>[!DNL PayPal Website Payments Pro]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) (y compris le passage en caisse express)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| France | [!DNL PayPal Integral Evolution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Allemagne | [[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Hong Kong (RAS de la Chine) | [!DNL PayPal Website Payments Pro Hosted Solution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Italie | [!DNL PayPal ProPay]<br/>[[!DNL Pal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Japon | [!DNL PayPal Website Payments Plus]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Nouvelle Zélande | [[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Espagne | [!DNL PayPal Pasarela Integral]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Royaume-Uni | [!DNL PayPal Payments Pro Hosted Solution] (y compris le passage en caisse express)<br/>[[!DNL PayPal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| États-Unis | [[!DNL PayPal Payments Advanced]](paypal-payments-advanced.md) (y compris le paiement express)<br/>[[!DNL PayPal Payments Pro]](paypal-payments-pro.md) (y compris le paiement express)<br/>[[!DNL PayPal Payments Standard+]](paypal-payments-standard.md)<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md) (y compris le paiement express)<br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) (y compris le paiement express)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |

{style="table-layout:auto"}

### Autres pays

PayPal Express Checkout et PayPal Website Payments Standard sont disponibles dans les pays suivants :

- Argentine
- Autriche
- Belgique
- Brésil
- Bulgarie
- Chili
- Costa Rica
- Chypre
- République tchèque
- Danemark
- République Dominicaine
- Équateur
- Estonie
- Finlande
- Guyane Française
- Gibraltar
- Grèce
- Guadeloupe
- Hongrie
- Islande
- Inde
- Indonésie
- Irlande
- Israël
- Jamaïque
- Lettonie
- Liechtenstein
- Lituanie
- Luxembourg
- Malaisie
- Malte
- Martinique
- Mexique
- Pays-Bas
- Norvège
- Philippines
- Pologne
- Portugal
- Réunion
- Roumanie
- Saint Marin
- Singapour
- Slovaquie
- Slovénie
- Afrique du Sud
- Corée du Sud
- Suède
- Suisse
- Taïwan
- Thaïlande
- Turquie
- Émirats arabes unis
- Uruguay
- Vénézuela
- Vietnam


[1]: https://manager.paypal.com/
[2]: https://developer.paypal.com/docs/payflow/payflow-gateway/
[3]: https://www.paypal.com/us/business/buy-now-pay-later
