---
title: PayPal Express Checkout
description: Découvrez comment configurer PayPal Express Checkout en tant que solution de paiement en ligne sur votre boutique.
exl-id: 0cd90306-cf47-4a5f-8994-6ae96904ae2f
feature: Payments
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '3110'
ht-degree: 0%

---

# PayPal Express Checkout

PayPal Express Checkout permet de stimuler les ventes en permettant à vos clients de payer par carte de crédit ou en sécurisant leurs comptes PayPal personnels. Lors du passage en caisse, le client est redirigé vers le site sécurisé PayPal pour compléter les informations de paiement. Le client est ensuite renvoyé à votre magasin pour effectuer le reste du processus de passage en caisse. Choisir Express Checkout ajoute le bouton PayPal familier à votre boutique, qui a été signalé pour augmenter les ventes.

>[!IMPORTANT]
>
>**Conditions requises pour PSD2 :** <br/>
>À compter du 14 septembre 2019, les banques européennes pourraient refuser les paiements qui ne répondent pas aux exigences de [PSD2](../getting-started/compliance-payment-services-directive.md). Aucune action n&#39;est nécessaire pour que PayPal Express Checkout soit conforme à PSD2, car toutes les exigences sont gérées par PayPal.

Les clients disposant de comptes PayPal actuels peuvent effectuer un achat en une seule étape en cliquant sur le bouton _[!UICONTROL Check out with PayPal]_. Express Checkout peut être utilisé en mode autonome ou avec l&#39;une des solutions tout-en-un de PayPal. Si vous acceptez déjà les cartes de crédit en ligne, vous pouvez proposer le paiement Express comme option supplémentaire pour attirer de nouveaux clients qui préfèrent payer avec PayPal.

>[!NOTE]
>
>PayPal a mis fin à la prise en charge de la vente de biens numériques par PayPal Express Checkout et vous recommande d&#39;utiliser [PayPal Payments Standard](paypal-payments-standard.md) ou une autre passerelle de paiement PayPal pour traiter toute commande qui inclut des [produits virtuels](../catalog/product-create-virtual.md).

## Conditions requises

- Marchand : [Compte PayPal professionnel][1]
- Client : [Compte PayPal personnel][2]

## Workflow de passage en caisse express

Contrairement aux autres modes de paiement, PayPal Express Checkout permet au client de passer en caisse au début du processus de paiement habituel à partir de la page du produit, du mini panier et du panier.

1. **Le client passe une commande** - Le client clique/appuie sur le bouton _[!UICONTROL Check out with PayPal]_.
1. **Le client est redirigé vers le site PayPal** - Le client est redirigé vers le site PayPal pour terminer la transaction.
1. **Le client se connecte à son compte PayPal** - Le client doit se connecter à son compte PayPal pour terminer la transaction. Le système de paiement utilise les informations de facturation et d’expédition de leur compte PayPal.
1. **Le client revient à la page de passage en caisse** - Le client est redirigé vers la page de passage en caisse de votre magasin pour examiner la commande.
1. **Le client passe une commande** - Le client passe la commande et les informations de la commande sont envoyées à PayPal.
1. **PayPal règle la transaction** - PayPal reçoit la commande et règle la transaction.

>[!NOTE]
>
>PayPal Express Checkout ne prend pas en charge les commandes avec plusieurs adresses.

## Extraction contextuelle

La _Conclusion de la transaction en contexte_ de PayPal facilite plus que jamais le paiement en ligne. Les clients ne perdent jamais de vue votre boutique lors de cette commande simplifiée en un ou deux clics. La fonctionnalité de passage en caisse contextuelle fonctionne aussi bien sur les Mac et les PC et offre une expérience cohérente sur les ordinateurs de bureau, les tablettes et les appareils mobiles. Pour en savoir plus, voir [Paiement contextuel dans le Paiement express][5].

![Démonstration de la vérification en contexte PayPal](./assets/storefront-paypal-in-context.png){width="700" zoomable="yes"}

[_Démonstration de la vérification en contexte PayPal_][6]

Lorsque vous configurez votre boutique pour [!DNL PayPal Express Checkout], vous pouvez activer cette option.

## Configuration de votre compte PayPal

Avant de configurer PayPal Express Checkout dans Commerce Admin, vous devez configurer votre compte marchand sur le site PayPal.

1. Connectez-vous à votre compte PayPal Advanced sur [manager.paypal.com][3].

1. Accédez à **[!UICONTROL Service Settings]** > **[!UICONTROL Hosted Checkout Pages]** > **[!UICONTROL Set Up]** et définissez les paramètres suivants :

   - **[!UICONTROL AVS]** : `No`
   - **[!UICONTROL CSC]** : `No`
   - **[!UICONTROL Enable Secure Token]** : `Yes`

1. Cliquez sur **[!UICONTROL Save Changes]**.

1. Configurer un autre utilisateur (recommandé par PayPal) :

   - Accédez à [manager.paypal.com][3] et connectez-vous à votre compte.

   - Pour configurer un autre utilisateur, suivez les instructions.

   - Cliquez sur **[!UICONTROL Update]**.

## Configurer PayPal Express Checkout dans Commerce

Vous pouvez avoir deux solutions PayPal actives en même temps : PayPal Express Checkout, plus une solution tout-en-un. Si vous activez une autre solution, celle utilisée précédemment est automatiquement désactivée.

>[!NOTE]
>
>Cliquez sur **[!UICONTROL Save Config]** à tout moment pour enregistrer votre progression.

### Étape 1 : Commencer la configuration

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Payment Methods]**.

1. Si votre installation comporte plusieurs sites web, boutiques ou vues, définissez **[!UICONTROL Store View]** sur la vue de la boutique dans laquelle vous souhaitez appliquer cette configuration.

1. Dans la section _[!UICONTROL Merchant Location]_, sélectionnez le **[!UICONTROL Merchant Country]**&#x200B;où se trouve votre entreprise.

   Ce paramètre détermine la sélection des solutions PayPal qui apparaissent dans la configuration.

   ![Pays commerçant](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. Sous _[!UICONTROL Recommended Solutions]_, cliquez sur **[!UICONTROL Configure]**&#x200B;pour **[!UICONTROL PayPal Express Checkout]**.

   ![Configurer PayPal Express Checkout](./assets/paypal-express-checkout.png){width="600"}

### Étape 2 : activer et connecter votre compte PayPal

1. Si nécessaire, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) dans la section **[!UICONTROL Required PayPal Settings]** .

   ![Connecter votre compte PayPal](./assets/paypal-express-required.png){width="600" zoomable="yes"}

1. Connectez votre compte à des fins de test ou de production :

   - Pour le mode test (développement) , cliquez sur **[!UICONTROL Sandbox Credentials]** et saisissez vos informations d’identification [sandbox PayPal][7].
   - Pour le mode de production, cliquez sur **[!UICONTROL Connect with PayPal]** et saisissez les informations d’identification de votre compte de production.

   Une fois votre connexion validée, vous pouvez continuer.

1. Définissez **[!UICONTROL Enable this Solution]** sur `Yes`.

1. Pour activer [PayPal In-Context Checkout](#in-context-checkout) :

   - Définissez **[!UICONTROL Enable In-Context Checkout Experience]** sur `Yes`.

   - Saisissez votre **[!UICONTROL Merchant Account ID]** PayPal.

     L&#39;ID de votre compte marchand se trouve dans le profil de votre compte professionnel PayPal.

>[!NOTE]
>
>[Crédit PayPal](paypal.md#paypal-credit-and-pay-later) est activé par défaut pour cette option de paiement.

### Étape 3 : remplir les paramètres PayPal requis

1. Si nécessaire, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) dans la section **[!UICONTROL Express Checkout]** .

   ![PayPal Express Checkout requis](./assets/paypal-express-settings.png){width="600" zoomable="yes"}

1. (Facultatif) Saisissez le **[!UICONTROL Email Associated with PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >Les adresses e-mail respectent la casse. Pour recevoir le paiement, l&#39;adresse e-mail que vous entrez doit correspondre à l&#39;adresse e-mail indiquée dans votre compte marchand PayPal.

   Si vous n&#39;avez pas de compte PayPal, cliquez sur **[!UICONTROL Start accepting payments via PayPal]**.

1. Définissez **[!UICONTROL API Authentication Methods]** sur l’une des options suivantes :

   - `API Signature` - Cette méthode d&#39;authentification PayPal est la plus simple à mettre en œuvre et est basée sur votre nom d&#39;utilisateur, mot de passe et une chaîne unique de caractères et de chiffres qui identifie votre compte. Les informations d’identification de signature API n’expirent pas.
   - `API Certificate` - Cette méthode d&#39;authentification PayPal est plus sécurisée, est basée sur votre nom d&#39;utilisateur, votre mot de passe et un certificat téléchargeable. Les informations d’identification d’API expirent au bout de trois ans et doivent être renouvelées.

   Si nécessaire, effectuez les opérations suivantes :

   - **[!UICONTROL API Username]**
   - **[!UICONTROL API Password]**
   - **[!UICONTROL API Signature]**

1. Si vous utilisez des informations d’identification provenant de votre compte sandbox, définissez **[!UICONTROL Sandbox Mode]** sur `Yes`.

   Lors du test de la configuration dans un sandbox, utilisez uniquement les [numéros de carte de crédit][4] recommandés par PayPal. Lorsque vous êtes prêt à passer en production, revenez à la configuration et définissez le mode Sandbox sur `No` et connectez-vous à votre compte PayPal de production.

1. Si votre système utilise un serveur proxy pour établir la connexion entre Commerce et le système de paiement PayPal, définissez **[!UICONTROL API Uses Proxy]** sur `Yes` et effectuez les opérations suivantes :

   - **[!UICONTROL Proxy Host]**
   - **[!UICONTROL Proxy Port]**

À la fin de cette séquence d’étapes, les paramètres PayPal requis sont terminés. Vous pouvez continuer avec les paramètres de base et avancés ou cliquer sur **[!UICONTROL Save Config]** et revenir ultérieurement pour ajuster la configuration

### Étape 4 : Configurer le crédit PayPal publicitaire / Annoncer PayPal PayLater (facultatif)

À partir de la version 2.4.3, PayPal PayLater est pris en charge dans les déploiements qui incluent PayPal. Cette fonctionnalité permet aux acheteurs de payer une commande par versements bimensuels au lieu de payer le montant total au moment de l’achat. L&#39;expérience de crédit PayPal est obsolète.

Définissez **[!UICONTROL Enable PayPal PayLater Experience]** sur l’une des options suivantes :

- `Yes` - Pour configurer Advertiser PayPal PayLater
- `No` - Pour configurer le crédit PayPal Advertising

>[!NOTE]
>
>Le paramètre **[!UICONTROL Enable PayPal PayLater Experience]** ne désactive pas la fonction [!DNL PayPal PayLater] et ne supprime pas les boutons **_[!UICONTROL PayPal PayLater]_** du storefront. Pour désactiver les boutons **_[!UICONTROL PayPal PayLater]_** et **_[!UICONTROL PayPal Credit]_** du storefront, vous devez sélectionner la valeur `PayPal Credit` pour le paramètre **[!UICONTROL Disable Funding Options]** ([!UICONTROL Advanced Settings] sous [!UICONTROL Frontend Experience Settings]).

#### Annoncer le crédit PayPal

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Advertise PayPal Credit]** .

1. Pour obtenir les informations relatives à votre compte, cliquez sur **[!UICONTROL Get Publisher ID from PayPal]** et suivez les instructions.

1. Saisissez votre **[!UICONTROL Publisher ID]**.

   ![Annoncer un crédit PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Home Page]** .

1. Pour placer une bannière sur la page, définissez **[!UICONTROL Display]** sur `Yes`.

1. Définissez **[!UICONTROL Position]** sur l’une des options suivantes :

   - `Header (center)`
   - `Sidebar (right)`

1. Définissez **[!UICONTROL Size]** sur l’une des options suivantes :

   - `190 x 100`
   - `234 x 60`
   - `300 x 50`
   - `468 x 60`
   - `728 x 90`
   - `800 x 66`

   ![Annoncer les paramètres de la page d&#39;accueil du crédit PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. Développez ![Sélecteur de développement](../assets/icon-display-expand.png) les sections restantes et répétez les étapes précédentes :

   - [!UICONTROL Catalog Category Page]
   - [!UICONTROL Catalog Product Page]
   - [!UICONTROL Checkout Cart Page]

#### Annoncer PayPal PayLater

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Advertise PayPal PayLater]** .

1. Définissez **[!UICONTROL Enable PayPal PayLater]** sur `Yes`.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Home Page]** .

1. Pour placer une bannière sur la page, définissez **[!UICONTROL Display]** sur `Yes`.

1. Définissez **[!UICONTROL Position]** sur l’une des options suivantes :

   - `Header (center)`
   - `Sidebar`

1. Définissez **[!UICONTROL Style Layout]** sur l’une des options suivantes :

   - `Text`
   - `Flex`

1. Pour [!UICONTROL Style Layout] **[!UICONTROL Text]** uniquement, définissez **[!UICONTROL Logo Type]** sur l’une des options suivantes :

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. Pour [!UICONTROL Style Layout] **[!UICONTROL Text]** uniquement, définissez **[!UICONTROL Logo Position]** sur l’une des options suivantes :

   - `Left`
   - `Right`
   - `Top`

1. Pour [!UICONTROL Style Layout] **[!UICONTROL Text]** uniquement, définissez **[!UICONTROL Text Color]** sur l’une des options suivantes :

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. Pour [!UICONTROL Style Layout] **[!UICONTROL Text]** uniquement, définissez **[!UICONTROL Text Size]** sur l’une des options suivantes :

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. Pour [!UICONTROL Style Layout] **[!UICONTROL Flex]** uniquement, définissez **[!UICONTROL Ratio]** sur l’une des options suivantes :

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. Pour [!UICONTROL Style Layout] **[!UICONTROL Flex]** uniquement, définissez **[!UICONTROL Color]** sur l’une des options suivantes :

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

   ![Annoncer les paramètres de la page d&#39;accueil du crédit PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. Développez ![Sélecteur de développement](../assets/icon-display-expand.png) les sections restantes et répétez les étapes précédentes :

   - [!UICONTROL Catalog Product Page]
   - [!UICONTROL Checkout Cart Page]
   - [!UICONTROL Checkout Payment Step]
   - [!UICONTROL Catalog Category Page]

### Étape 5 : définition des paramètres de base

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Basic Settings - PayPal Express Checkout]** .

   ![Paramètres de base](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. Par **[!UICONTROL Title]**, saisissez un titre qui identifie ce mode de paiement lors du passage en caisse.

   Il est recommandé d’utiliser le titre _PayPal_ pour toutes les vues de la boutique.

1. Si vous proposez plusieurs modes de paiement, saisissez un nombre pour **[!UICONTROL Sort Order]** afin de déterminer l&#39;ordre dans lequel le paiement PayPal Express apparaît lorsqu&#39;il est répertorié avec les autres modes de paiement.

   Ce nombre est relatif aux autres modes de paiement. (`0` = premier, `1` = deuxième, `2` = troisième, etc.)

1. Définissez **[!UICONTROL Payment Action]** sur l’une des options suivantes :

   - `Authorization` - Valide l&#39;achat et met un blocage sur les fonds. Le montant n&#39;est pas retiré tant qu&#39;il n&#39;est pas _saisi_ par le commerçant.
   - `Sale` - Le montant de l&#39;achat est autorisé et immédiatement retiré du compte du client.
   - `Order` - Le montant de la commande n&#39;est pas saisi ou autorisé dans le solde client, le compte bancaire ou la carte de crédit de PayPal. L&#39;action de paiement Commande représente un accord entre le système de paiement PayPal et le commerçant. Il permet au commerçant de capturer un ou plusieurs montants jusqu’au total de la commande à partir du compte acheteur du client, sur une période allant jusqu’à 29 jours. Une fois les fonds commandés, le commerçant peut les saisir à tout moment au cours de la période de 29 jours suivante. La capture du montant de la commande ne peut être effectuée qu’à partir de l’administrateur Commerce en créant une ou plusieurs factures.

1. Pour afficher le bouton _[!UICONTROL Check out with PayPal]_&#x200B;sur la page produit, définissez **[!UICONTROL Display on Product Details Page]**&#x200B;sur `Yes`.

1. Si l&#39;action de paiement est définie sur `Order`, effectuez les opérations suivantes :

   - **[!UICONTROL Authorization Honor Period (days)]** - Détermine la durée de validité de l’autorisation principale. La valeur doit être égale à la valeur correspondante dans votre compte marchand PayPal. La valeur par défaut de votre compte marchand PayPal est `3`. Pour augmenter ce nombre, contactez PayPal. L&#39;autorisation devient invalide à 23 h 49, heure du Pacifique des États-Unis, le dernier jour.

   - **[!UICONTROL Order Valid Period (days)]** - Détermine la durée de validité de la commande. Lorsque la commande n’est plus valide, vous ne pouvez plus créer de factures pour celle-ci. Indiquez une valeur égale à la valeur Période de commande valide dans votre compte marchand PayPal. La valeur par défaut de votre compte marchand PayPal est `29`. Pour modifier ce numéro, contactez PayPal.

   - **[!UICONTROL Number of Child Authorizations]** - Spécifie le nombre maximal d&#39;autorisations pour une seule commande, ce qui détermine le nombre maximal de factures partielles en ligne que vous pouvez créer pour une commande. Cette valeur doit être égale au paramètre correspondant de votre compte marchand PayPal. Le nombre par défaut d&#39;autorisations enfants dans votre compte PayPal est `1`. Pour augmenter ce nombre, contactez PayPal.

### Étape 6 : définition des paramètres avancés

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Advanced Settings]** .

   ![Paramètres avancés - PayPal Express Checkout](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Display on Shopping Cart]** sur `Yes`.

1. Définissez **[!UICONTROL Payment Applicable From]** sur l’une des options suivantes :

   - `All Allowed Countries` - Les clients de tous les pays spécifiés dans la configuration de votre boutique peuvent utiliser ce mode de paiement.
   - `Specific Countries` - Après avoir choisi cette option, la liste des _[!UICONTROL Payment from Specific Countries]_&#x200B;s’affiche. Pour sélectionner plusieurs pays, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et cliquez sur chaque élément.

1. Pour écrire des communications avec le système de paiement dans le fichier journal, définissez **[!UICONTROL Debug Mode]** sur `Yes`.

   Le fichier journal de PayPal Payments Advanced est `_payflow_advanced.log`.

   >[!NOTE]
   >
   >Conformément aux normes PCI Data Security, les informations de carte de crédit ne sont pas enregistrées dans le fichier journal.

1. Pour activer la vérification de l’authenticité de l’hôte, définissez **[!UICONTROL Enable SSL Verification]** sur `Yes`.

1. Pour afficher un résumé complet de la commande client par ligne à partir du site PayPal, définissez **[!UICONTROL Transfer Cart Line Items]** sur `Yes`.

1. Pour inclure jusqu’à dix options d’expédition dans le résumé, définissez **[!UICONTROL Transfer Shipping Options]** sur `Yes`. (Cette option s&#39;affiche uniquement si les lignes sont définies pour le transfert.)

1. Pour déterminer le type d&#39;image utilisé pour le bouton d&#39;acceptation PayPal, définissez **[!UICONTROL Shortcut Buttons Flavor]** sur l&#39;une des options suivantes :

   - `Dynamic` - (Recommandé) Affiche une image qui peut être modifiée dynamiquement à partir du serveur PayPal.
   - `Static` - Affiche une image spécifique qui ne peut pas être modifiée dynamiquement.

1. Pour permettre aux clients sans compte PayPal d&#39;effectuer un achat avec cette méthode, définissez **[!UICONTROL Enable PayPal Guest Checkout]** sur `Yes`.

1. Définissez **[!UICONTROL Require Customer's Billing Address]** sur l’une des options suivantes :

   - `Yes` - Nécessite l&#39;adresse de facturation du client pour tous les achats.
   - `No` - Ne nécessite pas l&#39;adresse de facturation du client pour tout achat.
   - `For Virtual Quotes Only` - Adresse de facturation du client requise pour les devis virtuels uniquement.

   >[!NOTE]
   >
   >Cette fonctionnalité doit être activée pour le compte marchand via le support technique de PayPal.

1. (Facultatif) Définissez la **[!UICONTROL Billing Agreement Signup]** pour permettre aux clients de signer un [accord de facturation](paypal-billing-agreements.md) avec votre boutique dans le système de paiement PayPal lorsqu’aucun accord de facturation actif n’est disponible dans le compte client :

   - `Auto` - Le client peut signer un accord de facturation pendant le flux de passage en caisse express ou utiliser un autre mode de paiement.
   - `Ask Customer` - Le client peut décider de signer ou non un accord de facturation pendant le flux de passage en caisse express.
   - `Never` - Le client ne peut pas signer de contrat de facturation pendant le flux de passage en caisse express.

   >[!NOTE]
   >
   >Les commerçants doivent demander [Assistance technique des commerçants PayPal](https://developer.paypal.com/support/) pour activer les accords de facturation dans leurs comptes. Le paramètre _Inscription à un contrat de facturation_ n&#39;est activé qu&#39;une fois que PayPal a confirmé que les contrats de facturation sont activés pour votre compte commercial.

1. Pour permettre au client de terminer la transaction à partir du site PayPal sans retourner dans votre magasin pour la révision de commande, définissez **[!UICONTROL Skip Order Review Step]** sur `Yes`.

1. Renseignez les sections supplémentaires selon les besoins de votre boutique :

   - [Paramètres du contrat de facturation PayPal](#paypal-billing-agreement-settings)
   - [Paramètres du rapport de règlement](#settlement-report-settings)
   - [Paramètres de l’expérience front-end](#frontend-experience-settings)
   - [Personnaliser les boutons intelligents](#customize-smart-buttons)
   - [Fonctionnalités](#features)

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

#### Paramètres du contrat de facturation PayPal

Un [accord de facturation](paypal-billing-agreements.md) est un accord de vente entre le vendeur et le client qui a été autorisé par PayPal à être utilisé avec plusieurs commandes. Pendant le processus de passage en caisse, l’option de paiement Accord de facturation ne s’affiche que pour les clients qui ont déjà conclu un accord de facturation avec votre société. Une fois que PayPal a autorisé le contrat, le système de paiement émet un ID de référence unique pour identifier chaque commande associée au contrat. Comme pour une commande fournisseur, il n’existe aucune limite au nombre de contrats de facturation qu’un client peut configurer avec votre société.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL PayPal Billing Agreement Settings]** .

   ![Paramètres du contrat de facturation](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Enabled]** sur `Yes`.

1. Par **[!UICONTROL Title]**, saisissez un titre qui identifie la méthode de l&#39;accord de facturation PayPal lors du passage en caisse.

1. Si vous proposez plusieurs modes de paiement, saisissez un nombre dans le champ **[!UICONTROL Sort Order]** pour déterminer l&#39;ordre dans lequel le contrat de facturation apparaît lorsqu&#39;il est indiqué avec d&#39;autres modes de paiement lors de la commande.

1. Définissez **[!UICONTROL Payment Action]** sur l’une des options suivantes :

   - `Authorization` - Valide l&#39;achat et met un blocage sur les fonds. Le montant n&#39;est pas retiré tant qu&#39;il n&#39;a pas été « capturé » par le commerçant.
   - `Sale` - Le montant de l&#39;achat est autorisé et immédiatement retiré du compte du client.

1. Définissez **[!UICONTROL Payment Applicable From]** sur l’une des options suivantes :

   - `All Allowed Countries` - Les clients de tous les pays spécifiés dans la configuration de votre boutique peuvent utiliser ce mode de paiement.
   - `Specific Countries` - Après avoir choisi cette option, la liste des _[!UICONTROL Payment from Specific Countries]_&#x200B;s’affiche. Pour sélectionner plusieurs pays, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et cliquez sur chacun d&#39;eux.

1. Pour enregistrer les communications avec le système de paiement dans le fichier journal, **[!UICONTROL Debug Mode]** sur `Yes`.

   >[!NOTE]
   >
   >Le fichier journal est stocké sur le serveur et n’est accessible que par les développeurs. Conformément aux normes PCI Data Security, les informations de carte de crédit ne sont pas enregistrées dans le fichier journal.

1. Pour activer la vérification SSL, définissez **[!UICONTROL Enable SSL Verification]** sur `Yes`.

1. Pour afficher une synthèse de chaque article de la commande du client sur votre page de paiements PayPal, définissez **[!UICONTROL Transfer Cart Line Items]** sur `Yes`.

1. Pour permettre aux clients de lancer un accord de facturation à partir du tableau de bord de leur compte client, définissez **[!UICONTROL Allow in Billing Agreement Wizard]** sur `Yes`.

#### Paramètres du rapport de règlement

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Settlement Report Settings]** .

   ![Paramètres du rapport de règlement](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. Par **[!UICONTROL SFTP Credentials]**, procédez comme suit :

   - Si vous vous êtes inscrit au serveur FTP sécurisé PayPal, saisissez les informations d&#39;identification SFTP suivantes :

      - Login
      - Mot de passe

   - Pour exécuter des rapports de test avant la _mise en ligne_ avec le paiement express sur votre site, définissez **[!UICONTROL Sandbox Mode]** sur `Yes`.

   - Saisissez le **[!UICONTROL Custom Endpoint Hostname or IP Address]**.

     Par défaut, la valeur est : `reports.paypal.com`

   - Saisissez le **[!UICONTROL Custom Path]** où les rapports sont enregistrés.

     Par défaut, la valeur est : `/ppreports/outgoing`

1. Pour générer des rapports selon un planning, définissez les paramètres **[!UICONTROL Scheduled Fetching]** :

   - Définissez **[!UICONTROL Enable Automatic Fetching]** sur `Yes`.

   - Définissez **[!UICONTROL Schedule]** sur l’une des options suivantes :

      - `Daily`
      - `Every 3 Days`
      - `Every 7 Days`
      - `Every 10 Days`
      - `Every 14 Days`
      - `Every 30 Days`
      - `Every 40 Days`

     PayPal conserve chaque rapport pendant 45 jours.

   - Définissez **[!UICONTROL Time of Day]** sur l’heure, la minute et la seconde auxquelles vous souhaitez que les rapports soient générés.

#### Paramètres de l’expérience front-end

Utilisez les paramètres d’expérience Frontend pour choisir les logos PayPal à afficher sur votre site et personnaliser l’apparence de vos pages marchandes PayPal.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Frontend Experience Settings]** .

   ![Paramètres d’expérience front-end](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. Sélectionnez les **[!UICONTROL PayPal Product Logo]** qui doivent apparaître dans le bloc PayPal de votre boutique.

   Les logos PayPal sont disponibles en quatre styles et deux tailles :

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. Pour personnaliser l&#39;apparence de vos pages marchandes PayPal, procédez comme suit :

   - Saisissez le nom du **[!UICONTROL Page Style]** que vous souhaitez appliquer à vos pages marchandes PayPal :

      - `paypal` - Utilise le style de page PayPal.
      - `primary` - Utilise le style de page que vous avez identifié comme style _principal_ dans le profil de votre compte.
      - `your_custom_value` - Utilise un style de page de paiement personnalisé, spécifié dans le profil de votre compte.

   - Par **[!UICONTROL Header Image URL]**, saisissez l’URL de l’image que vous souhaitez afficher dans le coin supérieur gauche de la page de paiement. La taille de fichier maximale est de 750 pixels de large sur 90 pixels de haut.

     >[!NOTE]
     >
     >PayPal recommande que l&#39;image réside sur un serveur sécurisé (https). Sinon, un navigateur peut vous avertir que _la page contient des éléments sécurisés et non sécurisés_.

   - Pour définir la couleur de vos pages, saisissez le code hexadécimal à six caractères, sans le symbole `#`, pour chacun des éléments suivants :

      - **[!UICONTROL Header Background Color]** - Couleur d’arrière-plan de l’en-tête de la page de passage en caisse.
      - **[!UICONTROL Header Border Color]** : couleur de la bordure de deux pixels autour de l’en-tête.
      - **[!UICONTROL Page Background Color]** - Couleur d’arrière-plan de la page de passage en caisse et autour de l’en-tête et du formulaire de paiement.

#### Personnaliser les boutons intelligents

La fonction _Boutons de paiement intelligent_ vous permet de personnaliser le bouton PayPal, qui peut être affiché sur les pages Passage en caisse, Détails du produit, Panier et Mini Panier. Les recherches internes de PayPal suggèrent que les options par défaut sont hautement reconnaissables et pourraient entraîner une augmentation des taux d&#39;achat, mais leurs valeurs par défaut pourraient ne pas correspondre au style de votre boutique. Vous pouvez choisir les options suivantes :

- Taille, couleur et forme du bouton PayPal
- Texte qui apparaît sur le bouton PayPal
- La disposition, lorsque plusieurs boutons sont affichés (horizontal ou vertical)

Pour personnaliser les boutons, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) chacune des sections suivantes et définissez les paramètres :

- **[!UICONTROL Checkout Page]**
- **[!UICONTROL Product Pages]**
- **[!UICONTROL Cart Page]**
- **[!UICONTROL Mini Cart]**

![Paramètres de la page de paiement](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings2.png){width="600" zoomable="yes"}

**_Pour configurer l’affichage du bouton pour chaque type de page, procédez comme suit_**

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section .

1. Définissez **[!UICONTROL Customize Button]** sur `Yes`.

1. Pour définir le texte que PayPal affiche sur le bouton de paiement intelligent, définissez **[!UICONTROL Label]** sur l&#39;un des éléments suivants :

   - `Checkout` - Passage en caisse PayPal
   - `Pay` - Passage en caisse PayPal
   - `Buy Now` - Acheter maintenant avec PayPal
   - `PayPal` - PayPal
   - `Installment` - PayPal
   - `Credit` - Crédit PayPal

1. Définissez **[!UICONTROL Layout]** sur l’une des options suivantes :

   - `Vertical` - (Par défaut) Affiche les boutons intelligents PayPal verticalement. L&#39;acheteur doit se connecter à PayPal ou créer un compte PayPal, que **[!UICONTROL Enable Guest Checkout]** soit sélectionné ou non.
   - `Horizontal` - Affiche les boutons intelligents PayPal horizontalement. Lorsque **[!UICONTROL Enable Guest Checkout]** est sélectionné, le bouton **[!UICONTROL Pay with Debit Card or Credit Card]** s&#39;affiche dans la fenêtre pop-up PayPal. Sinon, l&#39;acheteur doit se connecter à PayPal ou créer un compte PayPal.

1. Définissez **[!UICONTROL Size]** sur l’une des options suivantes :

   - `Medium` - 250 pixels sur 35 pixels.
   - `Large` - 350 pixels sur 40 pixels.
   - `Responsive` - (Par défaut) S’ajuste à la largeur du conteneur. La largeur minimale est de 100 pixels et la largeur maximale est de 500 pixels. La hauteur s’ajuste dynamiquement en fonction de la largeur.

1. Définissez **[!UICONTROL Shape]** sur l’une des options suivantes :

   - `Pill` - (Par défaut) Le bouton a la forme d’une pilule (long au centre et incurvé aux extrémités).
   - `Rectangle` - Forme carrée, sans courbes, dans un rectangle.

1. Définissez **[!UICONTROL Color]** sur l’une des options suivantes :

   - `Gold` (par défaut)
   - `Blue`
   - `Silver`
   - `Black`

#### Fonctionnalités

Les paramètres des fonctionnalités vous permettent de désactiver certaines fonctionnalités liées à cette solution PayPal.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Features]** .

   ![Paramètres de la page de paiement](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings3.png){width="600" zoomable="yes"}

1. Définissez la **[!UICONTROL Disable Funding Options]** pour déterminer quelles autres options de financement PayPal sont affichées sur la page _Passage en caisse_.

   Les options sélectionnées ne s’affichent pas sur la page _Passage en caisse_. Les options non sélectionnées s&#39;affichent uniquement si PayPal prend en charge la devise du magasin et le lieu de l&#39;acheteur. Les options incluent :

   - Crédit PayPal
   - Venmo
   - Icônes de carte de crédit PayPal Guest Checkout
   - Elektronisches Lastschriftverfahren - Allemand ELV

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypal.com/webapps/mpp/buying-online
[3]: https://manager.paypal.com/
[4]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[5]: https://www.paypal.com/rs/webapps/mpp/express-checkout
[6]: https://demo.paypal.com/us/demo/navigation?merchant=bigbox&amp;page=incontextProductCheckout
[7]: https://developer.paypal.com/docs/api-basics/sandbox/
