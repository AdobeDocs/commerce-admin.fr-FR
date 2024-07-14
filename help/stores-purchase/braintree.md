---
title: Braintree
description: Découvrez comment configurer Braintree en tant que solution de paiement en ligne sur votre boutique.
exl-id: 781b385f-926e-4047-b7da-6f7c090d75d8
feature: Payments
source-git-commit: fcd08ea5d8c3bd498eb4beae41bdf2f078a89f55
workflow-type: tm+mt
source-wordcount: '2625'
ht-degree: 0%

---

# Braintree

Braintree offre une expérience de paiement entièrement personnalisable avec la détection des fraudes et l’intégration de PayPal. Il prend en charge [!DNL Apple Pay], [!DNL Google Pay], ACH, Venmo et les méthodes de paiement locales. Braintree réduit la charge de conformité PCI pour les commerçants, car la transaction a lieu sur le système de Braintree. L’intégration des paiements Braintree est développée par [GENE Commerce](https://www.gene.co.uk/gene-braintree-payments/).

>[!NOTE]
>
>Si vous effectuez une mise à niveau vers la version 2.4.x à partir d’une version antérieure d’Adobe Commerce ou d’un Magento Open Source avec l’extension Braintree de Commerce Marketplace installée, reportez-vous aux [2.4 Update Notes](#24-upgrade-notes) à la fin de cette page.


## Étape 1 : Obtention des informations d’identification de votre Braintree

Accédez à [Paiements de Braintree][1] et inscrivez-vous à un compte.

## Étape 2 : définition des paramètres de base

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Payment Methods]**.

   - Si votre installation Commerce comporte plusieurs sites web, magasins ou vues, dans le coin supérieur gauche, sélectionnez l’ **[!UICONTROL Store View]** où s’applique la configuration.

   - Dans la section _[!UICONTROL Merchant Location]_, vérifiez que **[!UICONTROL Merchant Country]**est défini sur l’emplacement de votre entreprise.

1. Sous _[!UICONTROL Recommended Solutions]_, dans la section_[!UICONTROL Braintree Payments] (par [GENE Commerce](https://www.gene.co.uk/gene-braintree-payments/) v4.6.1 - [Notes de mise à jour](https://support.gene.co.uk/support/solutions/articles/35000228529)_, cliquez sur **[!UICONTROL Configure]**.

   ![Configurer le Braintree](./assets/braintree-payments.png){width="600" zoomable="yes"}

1. Pour **[!UICONTROL Title]**, saisissez un titre qui identifie Braintree comme option de paiement lors du passage en caisse.

1. Définissez l’opération actuelle **[!UICONTROL Environment]** pour les transactions du Braintree sur `Sandbox` ou `Production`

   Lors du test de la configuration dans un environnement de test, utilisez uniquement les [numéros de carte de crédit][2] recommandés par le Braintree. Lorsque vous êtes prêt à passer en production avec Braintree, définissez **[!UICONTROL Environment]** sur `Production`.

   ![Paramètres de base des informations d’identification](./assets/braintree-settings1.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Payment Action]** sur l’une des options suivantes :

   - `Authorize Only` - Approuve l’achat et met un frein aux fonds. Le montant n’est pas retiré du compte bancaire du client tant que la vente n’a pas été _capturée_ par le commerçant.|
   - `Intent Sale` - Le montant de l’achat est autorisé et immédiatement retiré du compte du client. **_Remarque :_** Cette valeur était _Autoriser et capturer_ dans les versions 2.3.x et antérieures.|

1. Saisissez le **[!UICONTROL Sandbox Merchant ID / Merchant ID]** de votre compte de Braintree.

1. Saisissez les informations d’identification suivantes à partir de votre compte de Braintree :

   - **[!UICONTROL Sandbox Public Key / Public Key]**
   - **[!UICONTROL Sandbox Private Key / Private Key]**

   >[!NOTE]
   >
   >Il existe des champs distincts pour les environnements **(Sandbox et Production)** et les autres champs sont générés en fonction de l’environnement sélectionné.

1. Avant d’enregistrer la configuration, cliquez sur **[!UICONTROL Validate Credentials]** pour valider vos informations d’identification.

1. Définissez **[!UICONTROL Enable Card Payments]** sur `Yes`.

   ![Paramètres de base](./assets/braintree-settings2.png){width="600" zoomable="yes"}

   Si vous souhaitez pouvoir stocker les informations sur les clients en toute sécurité, afin que les clients n’aient pas à les ré-entrer chaque fois qu’ils effectuent un achat, définissez **[!UICONTROL Enable Vault for Card Payments]** sur `Yes`.

## Étape 3 : définition des paramètres avancés

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Advanced Braintree Settings]** .

   ![Paramètres avancés](../configuration-reference/sales/assets/payment-methods-braintree-advanced-config.png){width="550" zoomable="yes"}

1. Pour **[!UICONTROL Vault Title]**, saisissez un titre descriptif pour votre référence qui identifie le coffre où sont stockées les informations de votre carte client.

1. Saisissez le **[!UICONTROL Merchant Account ID]** de votre compte de Braintree.

   Si vous ne spécifiez pas le compte marchand à utiliser, Braintree traite la transaction à l’aide de votre compte marchand par défaut.

1. Pour offrir une expérience de passage en caisse plus rapide avec les options de paiement express au début du processus de passage en caisse, y compris PayPal, PayLater, Apple Pay et Google Pay, définissez **[!UICONTROL Enable Checkout Express Payments]** sur `Yes`.

1. Si vous souhaitez empêcher l’envoi de la transaction pour évaluation dans le cadre des contrôles des outils de fraude avancés, définissez **[!UICONTROL Skip Fraud Checks on Admin Orders]** sur `Yes` pour les commandes passées via l’administrateur.

1. Définissez le **[!UICONTROL Bypass Fraud Protection Threshold]** de sorte que les `Advanced Fraud Protection` vérifications soient contournées lorsque le seuil est atteint ou dépassé.

   Si vous laissez ce champ vide, cette option est désactivée.

1. Si vous souhaitez que le système enregistre un fichier journal des interactions entre votre magasin et votre Braintree, définissez **[!UICONTROL Debug]** sur `Yes`.

1. Pour obliger les clients à fournir le code de sécurité à trois chiffres depuis l’arrière d’une carte de crédit, définissez **[!UICONTROL CVV Verification]** sur `Yes`.

   Si vous utilisez la vérification CVV, veillez à activer AVS et/ou CVV dans la section _Paramètres/Traitement_ de votre compte de Braintree.

1. Pour envoyer les articles du panier pour tous les modes de paiement, définissez **[!UICONTROL Send Card Line Items]** sur `Yes`.

1. Pour **[!UICONTROL Credit Card Types]**, sélectionnez chaque carte de crédit acceptée par votre boutique comme paiement par le biais de Braintree.

   Pour sélectionner plusieurs types de carte, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre dans lequel le Braintree apparaît lorsqu’il est répertorié avec d’autres méthodes de paiement lors du passage en caisse.

## Étape 4 : Définition des paramètres du webhook du Braintree

![Paramètres des webhooks Braintree](../configuration-reference/sales/assets/payment-methods-braintree-webhooks-config.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Enable Webhook]** sur `Yes` pour activer la fonctionnalité webhook pour la protection contre la fraude, les paiements ACH et les méthodes de paiement locales.

1. Copiez l’URL dans le champ **[!UICONTROL Fraud Protection URL]** et ajoutez-la à votre compte de Braintree en tant que _[!UICONTROL Webhook Destination URL]_.

   >[!IMPORTANT]
   >
   >Cette URL doit être sécurisée et accessible au public.

1. Définissez le champ **[!UICONTROL Fraud Protection Approve Order Status]** pour déterminer quand la protection contre la fraude est approuvée par Braintree.

   L’état de la commande sélectionnée est affecté à la commande Commerce.

1. Définissez le champ **[!UICONTROL Fraud Protection Reject Order Status]** pour déterminer quand la protection contre la fraude est rejetée par le Braintree.

   L’état de la commande sélectionnée est affecté à la commande Commerce.

## Étape 5 : Renseigner les paramètres spécifiques au pays

1. Définissez **[!UICONTROL Payment from Applicable Countries]** sur l’une des options suivantes :

   - `All Allowed Countries` - Les clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiés dans votre configuration de magasin peuvent utiliser ce mode de paiement.
   - `Specific Countries` - Après avoir choisi cette option, la liste _[!UICONTROL Payment from Specific Countries]_s’affiche. Maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et sélectionnez chaque pays de la liste dans lequel les clients peuvent effectuer des achats dans votre boutique.

   ![Paramètres spécifiques à un pays](../configuration-reference/sales/assets/payment-methods-braintree-country-specific-config.png){width="600" zoomable="yes"}

1. Pour configurer **[!UICONTROL Country Specific Credit Card Types]** :

   - Cliquez sur **[!UICONTROL Add]**.

   - Définissez le **[!UICONTROL Country]** et choisissez chaque **[!UICONTROL Allowed Credit Card Type]**.

   - Répétez cette procédure pour identifier les cartes de crédit acceptées dans chaque pays.

## Étape 6 : achèvement de l’ACCÈS via les paramètres du Braintree

![ACH par Braintree](../configuration-reference/sales/assets/payment-methods-braintree-ach-config.png){width="600" zoomable="yes"}

1. Pour inclure ACH comme option de paiement avec Braintree, définissez **[!UICONTROL Enable ACH Direct Debit]** sur `Yes`.

1. Les clients peuvent coffre-fort leur méthode de paiement à usage unique ACH Direct Debit et le stocker pour une utilisation ultérieure. Une fois la valeur définie, les clients peuvent réutiliser le débit direct ACH sans avoir à entrer à nouveau ou à authentifier leurs informations de paiement si la valeur **[!UICONTROL Enable Vault for ACH Direct Debit]** est définie sur `Yes`.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre dans lequel l’option de paiement ACH du Braintree apparaît lorsqu’elle est répertoriée avec d’autres options de paiement lors du passage en caisse.

## Étape 7 : terminez le [!UICONTROL Apple Pay] par les paramètres du Braintree

![Paramètres du Braintree ApplePay](../configuration-reference/sales/assets/payment-methods-braintree-applepay-config.png){width="600" zoomable="yes"}

1. Pour inclure [!DNL Apple Pay] comme option de paiement avec Braintree, définissez **[!UICONTROL Enable ApplePay through Braintree]** sur `Yes`.

   Veillez tout d&#39;abord à [vérifier votre nom de domaine](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3) dans votre compte de Braintree.

1. Si vous souhaitez pouvoir stocker les informations sur les clients en toute sécurité, afin que les clients n’aient pas à les ré-entrer chaque fois qu’ils effectuent un achat avec Apple Pay, définissez **[!UICONTROL Enable Vault for ApplePay]** sur `Yes`.

1. Définissez **[!UICONTROL Payment Action]** sur l’une des options suivantes :

   - `Authorize Only` - Approuve l’achat et met un frein aux fonds. Le montant n’est pas retiré du compte bancaire du client tant que la vente n’a pas été _capturée_ par le commerçant.
   - `Intent Sale` - Le montant de l’achat est autorisé et immédiatement retiré du compte du client.

1. Pour **[!UICONTROL Merchant Name]**, saisissez le texte qui spécifie le libellé affiché pour les clients dans la boîte de dialogue Payer Apple.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre dans lequel l’option de paiement [!DNL Apple Pay] apparaît lorsqu’elle est répertoriée avec d’autres options de paiement lors du passage en caisse.

## Etape 8 : paramétrage des modes de paiement locaux

1. Pour inclure les méthodes de paiement locales comme option de paiement avec Braintree, définissez **[!UICONTROL Enable Local Payment Methods]** sur `Yes`.

1. Pour **[!UICONTROL Title]**, saisissez le texte à utiliser pour le libellé qui apparaît dans la section Mode de paiement de passage en caisse (valeur par défaut : `Local Payments`).

1. Pour **[!UICONTROL Fallback Button Text]**, saisissez le texte à utiliser pour le bouton qui s’affiche sur la page du Braintree de secours pour ramener le client sur le site web (par exemple, `Complete Checkout`).

1. Pour **[!UICONTROL Redirect on Fail]**, saisissez l’URL vers laquelle les clients doivent être redirigés lorsque les transactions du mode de paiement local sont annulées, échouent ou rencontrent des erreurs. Il doit s’agir de la page de paiement du passage en caisse (par exemple, `https://www.domain.com/checkout#payment`).

1. Pour **[!UICONTROL Allowed Payment Methods]**, sélectionnez le mode de paiement local à activer.

   Options : `Bancontact` / `EPS` / `giropay` / `iDeal` / `Klarna Pay Now` / `SOFORT` / `MyBank` / `P24` / `SEPA/ELV Direct Debit` (pas encore pris en charge)

   ![Paramètres des méthodes de paiement locales](../configuration-reference/sales/assets/payment-methods-braintree-local-payment-config.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >L’extension de Braintree groupé ne prend pas en charge tous les modes de paiement locaux répertoriés dans la [documentation du développeur de Braintree](https://developer.paypal.com/braintree/docs/guides/local-payment-methods/overview). D&#39;autres modes de paiement locaux sont en cours de développement et seront pris en charge dans les prochaines versions.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre dans lequel le mode de paiement local apparaît lorsqu’il est répertorié avec d’autres options de paiement lors du passage en caisse.

## Étape 9 : terminez le [!DNL Google Pay] par les paramètres du Braintree

![Google Payer par le biais du Braintree](../configuration-reference/sales/assets/payment-methods-braintree-googlepay-config.png){width="600" zoomable="yes"}

1. Pour inclure [!DNL Google Pay] comme option de paiement avec Braintree, définissez **[!UICONTROL Enable GooglePay Through Braintree]** sur `Yes`.

1. Si vous souhaitez pouvoir stocker les informations sur les clients en toute sécurité, afin que les clients n’aient pas à les ré-entrer chaque fois qu’ils effectuent un achat avec le paiement Google, définissez **[!UICONTROL Enable Vault for GooglePay]** sur `Yes`.

1. Définissez **[!UICONTROL Payment Action]** sur l’une des options suivantes :

   - `Authorize Only` - Approuve l’achat et met un frein aux fonds. Le montant n’est pas retiré du compte bancaire du client tant que la vente n’a pas été _capturée_ par le commerçant.
   - `Intent Sale` - Le montant de l’achat est autorisé et immédiatement retiré du compte du client.

1. Définissez **[!UICONTROL Button Color]** pour déterminer la couleur du bouton [!DNL Google Pay] : `White` ou `Black`

1. Pour **[!UICONTROL Merchant ID]**, saisissez votre MerchantID (fourni par Google).

1. Pour **[!UICONTROL Accepted Cards]**, sélectionnez le type de carte qu’un client peut utiliser pour passer une commande à l’aide de [!DNL Google Pay].

   Options : `Visa` / `MasterCard` / `AMEX` / `Discover` / `JCB`

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre dans lequel [!DNL Google Pay] apparaît lorsqu’il est répertorié avec d’autres options de paiement lors du passage en caisse.

## Étape 10 : achèvement de Venmo via les paramètres du Braintree

1. Pour inclure Venmo comme option de paiement avec Braintree, définissez **[!UICONTROL Enable Venmo through Braintree]** sur `Yes`.

1. Définissez **[!UICONTROL Enable Vault for Venmo]** sur `Yes` pour permettre l’utilisation d’un coffre sécurisé pour stocker le compte Venmo des clients afin que les clients n’aient pas besoin de se reconnecter à leur compte Venmo pour de futures transactions.

   ![Venmo par Braintree](../configuration-reference/sales/assets/payment-methods-braintree-venmo-config.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Payment Action]** sur l’une des options suivantes :

   - `Authorize Only` - Approuve l’achat et met un frein aux fonds. Le montant n’est pas retiré du compte bancaire du client tant que la vente n’a pas été _capturée_ par le commerçant.
   - `Intent Sale` - Le montant de l’achat est autorisé et immédiatement retiré du compte du client.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre dans lequel Venmo apparaît lorsqu’il est répertorié avec d’autres options de paiement lors du passage en caisse.

## Étape 11 : achèvement de PayPal via les paramètres du Braintree

![PayPal via les paramètres du Braintree](./assets/braintree-paypal.png){width="550" zoomable="yes"}

1. Pour inclure PayPal comme option de paiement avec Braintree, définissez **[!UICONTROL Enable PayPal through Braintree]** sur `Yes`.

1. Spécifiez votre méthode de paiement PayPal par Braintree :

   >[!NOTE]
   >
   >**[!DNL PayPal Credit]** ou **[!DNL PayPal PayLater]** peuvent être activés. Les deux méthodes ne peuvent pas être activées de la même manière.

   - Pour inclure [!DNL PayPal Credit] comme option de paiement avec Braintree, définissez **[!UICONTROL Enable PayPal Credit through Braintree]** sur `Yes`.

     Lorsque **Activer PayPal via Braintree** est défini sur `Yes`, seul ce champ s’affiche.

     >[!NOTE]
     >
     >PayPal Credit est disponible uniquement aux États-Unis et au Royaume-Uni. Le crédit PayPal est désactivé si la valeur sélectionnée pour le champ _[!UICONTROL Merchant Country]_n’est pas `US` ou `UK`.

   - Pour inclure [!DNL PayPal PayLater] comme option de paiement avec Braintree, définissez **[!UICONTROL Enable PayPal PayLater through Braintree]** sur `Yes`.

     Lorsque **[!UICONTROL Enable PayPal PayLater through Braintree]** est défini sur `Yes`, seul ce champ s’affiche.

     Vous pouvez afficher des messages PayLater sur votre site pour les offres, par exemple _Payer dans 3_, ce qui permet aux clients de payer trois mensualités sans intérêts. L’intégration de Braintree peut afficher des messages sur votre site pour promouvoir cette fonctionnalité. Vous ne pouvez pas promouvoir des offres PayLater avec tout autre contenu, contenu marketing ou matériel.

1. Pour **[!UICONTROL Title]**, saisissez un titre qui identifie l’option de paiement du Braintree par PayPal lors du passage en caisse.

1. Définissez **[!UICONTROL Vault Enabled]** sur `Yes` pour permettre l’utilisation d’un coffre sécurisé afin de stocker le compte PayPal des clients. Un compte PayPal valide peut être utilisé pour les transactions ultérieures, ce qui réduit le nombre d’étapes pour les clients.

1. Définissez **[!UICONTROL Send Cart Line Items for PayPal]** sur `Yes` pour envoyer les éléments de ligne (articles de commande) à PayPal, ainsi que les cartes-cadeaux, l’encapsulage des cadeaux pour les articles, l’encapsulage des cadeaux pour la commande, le crédit de magasin, l’expédition et la taxe comme éléments de ligne.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre dans lequel l’option de paiement PayPal du Braintree apparaît lorsqu’elle est répertoriée avec d’autres options de paiement lors du passage en caisse.

1. Pour afficher votre nom commercial différemment de ce qui est défini dans votre [configuration de magasin](../getting-started/store-details.md#store-information), saisissez le nom dans le champ **[!UICONTROL Override Merchant Name]** tel que vous souhaitez le voir apparaître.

1. Définissez **[!UICONTROL Payment Action]** sur l’une des options suivantes :

   - `Authorize Only` - Approuve l’achat et met un frein aux fonds. Le montant n’est pas retiré du compte bancaire du client tant que la vente n’a pas été _capturée_ par le commerçant.
   - `Authorize and Capture` - Le montant de l’achat est autorisé et immédiatement retiré du compte du client.

1. Définissez **[!UICONTROL Payment from Applicable Countries]** sur l’une des valeurs suivantes pour les transactions du Braintree traitées par PayPal :

   - `All Allowed Countries` - Les clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiés dans votre configuration de magasin peuvent utiliser ce mode de paiement.
   - `Specific Countries` - Après avoir choisi cette option, la liste _[!UICONTROL Payment from Specific Countries]_s’affiche. Maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et sélectionnez chaque pays de la liste dans lequel les clients peuvent effectuer des achats dans votre boutique.

1. Pour obliger les clients à fournir une adresse de facturation, définissez **[!UICONTROL Require Customer's Billing Address]** sur `Yes`.

   >[!NOTE]
   >
   >Cette fonctionnalité doit être activée pour votre compte par le support technique de PayPal.

1. Pour enregistrer un fichier journal des interactions entre votre boutique et PayPal via Braintree, définissez **[!UICONTROL Debug]** sur `Yes`.

1. Pour afficher le bouton PayPal sur la page du mini panier et du panier, définissez **[!UICONTROL Display on Shopping Cart]** sur `Yes`.

## Étape 12 : Définition des paramètres de style

1. Pour **[!UICONTROL Location]**, choisissez l’emplacement de rendu des boutons et messages PayPal : `Mini-Cart and Cart Page`, `Checkout Page` ou `Product Page`

   ![Paramètres de style PayPal](../configuration-reference/sales/assets/payment-methods-braintree-paypal-styling.png){width="600" zoomable="yes"}

### [!UICONTROL Mini-Cart and Cart Page]

Les options et paramètres de cette section varient en fonction du paramètre défini dans le champ _[!UICONTROL Location]_.

1. Définissez **[!UICONTROL PayPal Button Type]** sur l’un des trois types de boutons : `PayPal Button` / `PayPal Pay Later Button` / `PayPal Credit Button`

**[!UICONTROL PayPal Button]**

Les options et paramètres de cette section varient en fonction du type de bouton sélectionné dans le champ _[!UICONTROL PayPal Button Type]_.

1. Pour afficher le bouton PayPal sur le storefront à l’emplacement sélectionné, définissez **[!UICONTROL Show PayPal Button]** sur `Yes`.

1. Pour **[!UICONTROL Button Label]**, sélectionnez l’étiquette du bouton PayPal : `Paypal`, `Checkout`, `Buynow` ou `Pay`

1. Pour **[!UICONTROL Color]**, sélectionnez la couleur du bouton PayPal : `Blue`, `Black`, `Gold` ou `Silver`

1. Pour **[!UICONTROL Shape]**, sélectionnez la forme de bouton PayPal : `Pill` ou `Rectangle`

1. Pour **[!UICONTROL Size (Deprecated)]**, sélectionnez la taille du bouton PayPal : `Medium`, `Large` ou `Responsive`

>[!NOTE]
>
>Le champ de configuration **[!DNL Size(Deprecated)]** est obsolète et n’est pas utilisé pour appliquer un style aux boutons PayPal.

**[!UICONTROL PayLater Messaging]**

1. Pour afficher la messagerie [!DNL PayLater] sur le storefront à l’emplacement sélectionné, définissez **[!UICONTROL Show PayLater Messaging]** sur `Yes`.

   Ce message inclut l’affichage de [!DNL PayLater] messages pour les offres disponibles ([restrictions appliquées](https://developer.paypal.com/docs/checkout/pay-later/us/)).

1. Pour **[!UICONTROL Message Layout]**, sélectionnez la disposition du message [!DNL PayLater] : `Text` ou `Flex`

1. Pour **[!UICONTROL Logo]**, sélectionnez le type de logo PayPal : `Inline`, `Primary`, `Alternative` ou `None`

1. Pour **[!UICONTROL Logo Position]**, sélectionnez la position du logo PayPal : `Left`, `Right` ou `Top`

1. Pour **[!UICONTROL Text Color]**, sélectionnez la couleur du texte du message [!DNL PayLater] : `Black`, `White`, `Monochrome` ou `Grayscale`

Lorsque ces options sont définies, vous pouvez voir l’aperçu des boutons PayPal et des messages PayLater. Vous pouvez utiliser des commandes pour appliquer les paramètres ou réinitialiser les valeurs :

- Pour stocker les paramètres de style sélectionnés pour les boutons et la messagerie PayLater et les appliquer à l’emplacement actuel et au type de bouton actuel, cliquez sur **[!UICONTROL Apply]**.

- pour stocker les paramètres de style sélectionnés pour les boutons et les valeurs de messagerie PayLater et les appliquer à tous les types de boutons et emplacements, cliquez sur **[!UICONTROL Apply to All Buttons]**.

- Pour renvoyer les paramètres de style aux valeurs par défaut recommandées pour les boutons et la messagerie PayLater et les appliquer à tous les types de boutons et emplacements, cliquez sur **[!UICONTROL Reset to Recommended Defaults]**.

## Étape 13 : définition des paramètres de vérification 3D

1. Si vous souhaitez ajouter une étape de vérification pour les clients utilisant des cartes de crédit qui sont inscrits dans un programme de vérification (par exemple _Vérifié par VISA_), définissez **[!UICONTROL 3D Secure Verification]** sur `Yes`.

   Au cours du processus, le montant de la transaction qui est soumis à vérification est comparé au montant envoyé pour autorisation.

2. Pour toujours contester la requête sécurisée 3D pour toutes les transactions, définissez **[!UICONTROL Always request 3DS]** sur `Yes`.

3. Pour **[!UICONTROL Threshold Amount]**, saisissez le montant minimum de commande nécessaire pour déclencher la vérification 3D.

4. Définissez **[!UICONTROL Verify for Applicable Countries]** sur l’une des options suivantes :

   - `All Allowed Countries` - Les clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiés dans votre configuration de magasin peuvent utiliser ce mode de paiement.
   - `Specific Countries` - Après avoir choisi cette option, la liste _[!UICONTROL Verify for Specific Countries]_s’affiche. Maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et sélectionnez chaque pays de la liste dans lequel les clients peuvent effectuer des achats dans votre boutique.

   ![Paramètres de vérification 3D](../configuration-reference/sales/assets/payment-methods-braintree-3d-secure-verify-config.png){width="600" zoomable="yes"}

## Étape 14 : configuration des descripteurs dynamiques du Braintree

Les descripteurs suivants sont utilisés pour identifier les achats sur les relevés de carte de crédit client. Vous pouvez réduire le nombre de rebonds en identifiant clairement la société associée à chaque achat. Si les descripteurs dynamiques ne sont pas activés pour votre compte, contactez l’assistance du Braintree.

![Descripteurs dynamiques](../configuration-reference/sales/assets/payment-methods-braintree-dynamic-config.png){width="600" zoomable="yes"}

1. Saisissez le descripteur dynamique pour **[!UICONTROL Name]**, **[!UICONTROL Phone]** et **[!UICONTROL URL]** en fonction des instructions suivantes :

   - **[!UICONTROL Name]** - Le descripteur de nom comporte deux parties, séparées par un astérisque (*). Par exemple :

     `company*myproduct`

     La première partie du descripteur identifie la société ou l’application de données côté serveur et la deuxième partie identifie le produit. La longueur des parties `company` et `product` du descripteur peut être allouée comme suit, pour une longueur combinée allant jusqu’à 22 caractères.

     **_Caractères dans le descripteur de nom_**

     _Option 1 :_ `Company` doit comporter trois caractères, `Product` peut comporter jusqu’à 18 caractères.

     _Option 2 :_ `Company` doit comporter sept caractères, `Product` peut comporter jusqu’à 14 caractères

     _Option 3_ : `Company` doit comporter 12 caractères, `Product` peut comporter jusqu’à neuf caractères.

   - **[!UICONTROL Phone]** - Le descripteur de téléphone doit comporter de 10 à 14 caractères et ne peut contenir que des nombres, des tirets, des parenthèses et des points. Par exemple :

     `9999999999`

     `(999) 999-9999`

     `999.999.9999`

   - **[!UICONTROL URL]** - Le descripteur d’URL représente votre nom de domaine et peut contenir jusqu’à 13 caractères. Par exemple :

     `company.com`

1. Une fois la configuration de votre Braintree terminée, cliquez sur **[!UICONTROL Save Config]**.

## Notes de mise à niveau 2.4

À partir d’Adobe Commerce et de Magento Open Source 2.4.0, l’extension Braintree est incluse dans la version. Si vous effectuez une migration vers Commerce 2.4.x à partir d’une version antérieure à 2.4.0 dans laquelle l’extension de Braintree Marketplace est installée, vous devez désinstaller cette extension (`paypal/module-braintree` ou `gene/module-braintree`) et mettre à jour toutes les personnalisations de code afin d’utiliser l’espace de noms `PayPal_Braintree` au lieu de `Magento_Braintree`. Les paramètres de configuration de l’extension principale du Braintree Commerce les paiements regroupés et l’extension distribuée sur le Commerce Marketplace persistent et les paiements placés avec ces versions précédentes peuvent toujours être capturés, annulés ou remboursés normalement.

[1]: https://www.braintreepayments.com/
[2]: https://developers.braintreepayments.com/reference/general/testing/php
