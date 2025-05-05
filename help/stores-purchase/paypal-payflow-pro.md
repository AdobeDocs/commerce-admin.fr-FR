---
title: PayPal Payflow Pro
description: Découvrez comment configurer PayPal Payflow Pro en tant que solution de paiement en ligne sur votre boutique.
exl-id: c720b33c-44e1-4954-b5be-38932393a43c
feature: Payments
source-git-commit: c0d6523f820558c8cd6cfa6b745568784b9e784c
workflow-type: tm+mt
source-wordcount: '2194'
ht-degree: 0%

---

# PayPal Payflow Pro

La passerelle PayPal Payflow Pro, anciennement appelée _Verisign_, est disponible pour les clients des États-Unis, du Canada, de l’Australie et de la Nouvelle-Zélande. Contrairement aux autres méthodes de paiement PayPal, les marchands sont facturés une mensualité fixe, plus des frais fixes pour chaque transaction, quel que soit le numéro.

![Passage en caisse avec PayPal](./assets/storefront-cart-paypal.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>**Exigences de PSD2 :** <br/>
>À compter du 14 septembre 2019, les banques européennes pourront refuser les paiements qui ne répondent pas aux exigences de [PSD2](../getting-started/compliance-payment-services-directive.md). Pour se conformer à PSD2, PayPal Payflow Pro doit être intégré à un module externe tiers. Pour en savoir plus, voir [3-D Secure for Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-mpi/).

## Conditions

- [Compte professionnel PayPal][1] - La passerelle PayPal Payflow Pro relie le compte marchand de PayPal au site web marchand, en tant que passerelle et compte marchand.

- Si vous gérez plusieurs sites web Adobe Commerce et Magento Open Source, vous devez disposer d’un compte marchand PayPal distinct pour chaque site web.

## Workflow client

1. **Le client va au passage en caisse** - Pendant le passage en caisse, le client choisit de payer avec PayPal Payflow Pro, et saisit les informations de carte de crédit. Les clients ne sont pas tenus de disposer de comptes PayPal personnels. Cependant, en fonction du pays du commerce, les clients peuvent également utiliser leur compte personnel PayPal pour payer la commande.
1. **Le client envoie la commande** : le client envoie la commande et les informations de commande sont envoyées à PayPal pour traitement. Le client ne quitte pas la page de passage en caisse de votre site.
1. **PayPal termine la transaction** - Les paiements sont acceptés au moment de la commande. Selon l&#39;action de paiement spécifiée dans le paramétrage, une commande client ou une commande client et une facture sont créées.

## Workflow de traitement des commandes en ligne

1. **L’administrateur envoie une facture en ligne** : l’administrateur du magasin envoie une facture en ligne et, par conséquent, une transaction et une facture correspondantes sont créées.
1. **PayPal reçoit la transaction** - Les informations de commande sont envoyées à PayPal. Un enregistrement de la transaction et une facture sont générés. Vous pouvez afficher toutes les transactions de la passerelle Payflow Pro dans votre [compte marchand PayPal][2].

>[!NOTE]
>
>Les factures partielles et les remboursements partiels ne sont pas pris en charge par PayPal Payflow Pro.

## Configuration de votre compte PayPal

1. Connectez-vous à votre [compte professionnel PayPal][2].

1. Configurez les [pages de passage en caisse hébergées][4] à l’aide du Gestionnaire PayPal avec les paramètres suivants :

   - Sous **[!UICONTROL Choose your settings]**, définissez **[!UICONTROL Transaction Process Mode]** sur `Live`.

   - Sous **[!UICONTROL Display options on payment page]**, définissez **Annuler la méthode d’URL** sur `POST`.

   - Sous **[!UICONTROL Billing Information]**, cochez les cases de code de sécurité de carte **[!UICONTROL CSC]** pour les champs obligatoires et modifiables.

   - Sous **[!UICONTROL Payment Confirmation]**, définissez **[!UICONTROL Return URL Method]** sur `POST`.

   - Sous **[!UICONTROL Security Options]**, renseignez les paramètres suivants :

      - **[!UICONTROL AVS]** : `No`
      - **[!UICONTROL CSC]** : `No`
      - **[!UICONTROL Enable Secure Token]** : `Yes`

   - Sélectionnez **[!UICONTROL Customize]**, puis **[!UICONTROL Layout C]**.

     La disposition C affiche uniquement les champs de carte de crédit et de débit. Elle peut être encadrée sur votre site ou utilisée comme fenêtre contextuelle autonome. La taille est fixée à 490 x 565 pixels, avec un espace supplémentaire pour les messages d’erreur. Sur certains systèmes, ce paramètre corrige un problème de redirection transparente.

1. Une fois les paramètres de configuration terminés, cliquez sur **[!UICONTROL Save and Publish]**.

1. Dans le menu Gestionnaire PayPal, choisissez **[!UICONTROL Account Administration]**.

1. Sous **[!UICONTROL Manage Security]**, cliquez sur **[!UICONTROL Transaction Settings]** et procédez comme suit :

   - Définissez **[!UICONTROL Allow reference transactions]** sur `Yes`.

   - Cliquez sur **[!UICONTROL Confirm]**.

     >[!NOTE]
     >
     >Si vous disposez de plusieurs sites web Commerce, vous devez créer un compte avancé PayPal des paiements distinct pour chacun d’eux.

1. Configurez un autre utilisateur (recommandé par PayPal) :

   - Dans la deuxième ligne du menu principal, cliquez sur **[!UICONTROL Manage Users]**.

   - Pour ajouter un autre utilisateur au compte, cliquez sur **[!UICONTROL Add User]**. Le lien se trouve juste au-dessus du titre Gérer les utilisateurs .

   - Renseignez les champs requis dans les sections suivantes du formulaire _[!UICONTROL Add User]_:

      - [!UICONTROL Admin Confirmation]
      - [!UICONTROL User Information]
      - [!UICONTROL User Login Information]
      - [!UICONTROL Assign Privilege to User]

   - Cliquez sur **[!UICONTROL Update]**.

1. Veillez à vous déconnecter de votre compte PayPal.

## Configuration de PayPal Payflow Pro dans Commerce

>[!TIP]
>
>Cliquez à tout moment sur **[!UICONTROL Save Config]** pour enregistrer votre progression.

### Etape 1 : lancer la configuration

Cette méthode de configuration suppose que vous disposez d’un compte PayPal existant.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Payment Methods]**.

1. Si votre installation Commerce comporte plusieurs sites web, magasins ou vues, définissez **[!UICONTROL Store View]** sur la vue de magasin dans laquelle vous souhaitez appliquer cette configuration.

1. Dans la section _[!UICONTROL Merchant Location]_, sélectionnez l’**[!UICONTROL Merchant Country]**&#x200B;où se trouve votre entreprise.

   Ce paramètre détermine la sélection des solutions PayPal qui apparaissent dans la configuration.

   ![Pays commerçant](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. Développez **[!UICONTROL PayPal Payment Gateways]** (si nécessaire) et cliquez sur **[!UICONTROL Configure]** pour **[!UICONTROL Payflow Pro]**.

   ![Configurer - Payflow Pro](./assets/payflow-pro.png){width="600" zoomable="yes"}

### Étape 2 : Remplir les paramètres PayPal requis

![ Paramètres requis - PayPal Payflow Pro](./assets/payflow-pro-required-a.png){width="600" zoomable="yes"}

1. (Facultatif) Saisissez le **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >Les adresses électroniques sont sensibles à la casse. Pour recevoir le paiement, l’adresse électronique doit correspondre à l’adresse électronique spécifiée dans votre compte marchand PayPal.

1. Saisissez l’une des informations d’identification suivantes que vous utilisez pour vous connecter à votre compte marchand PayPal :

   - **[!UICONTROL Partner]** - Votre identifiant de partenaire PayPal.
   - **[!UICONTROL User]** - Si vous configurez un ou plusieurs utilisateurs supplémentaires sur le compte, cette valeur est l’identifiant de l’utilisateur autorisé à traiter les transactions. Si, toutefois, vous n’avez pas configuré d’utilisateurs supplémentaires, **[!UICONTROL USER]** a la même valeur que **[!UICONTROL Vendor]**.
   - **[!UICONTROL Vendor]** - Votre identifiant de connexion marchand créé lorsque vous vous êtes inscrit au compte.

1. Saisissez le **[!UICONTROL Password]** associé à votre compte PayPal.

1. Pour exécuter des transactions de test, définissez **[!UICONTROL Test Mode]** sur `Yes`.

   Lors du test de la configuration dans un environnement de test, utilisez uniquement les [numéros de carte de crédit][3] recommandés par PayPal. Lorsque vous êtes prêt à passer en production, revenez à la configuration et définissez le mode test sur `No`.

1. Si votre système utilise un serveur proxy pour établir la connexion au système PayPal, définissez **[!UICONTROL Use Proxy]** sur `Yes` et procédez comme suit :

   - Saisissez l’adresse IP du **[!UICONTROL Proxy Host]**.

   - Saisissez le numéro de port de **[!UICONTROL Proxy Port]**.

     Un proxy est utilisé lorsque le pare-feu du serveur empêche l’accès direct au serveur PayPal. Dans ce cas, un serveur tiers est utilisé pour relayer le trafic.

1. Définissez **[!UICONTROL Enable this Solution]** sur `Yes`.

1. Si vous souhaitez proposer le [crédit PayPal](paypal.md#paypal-credit-and-pay-later) à vos clients, définissez **[!UICONTROL Enable PayPal Credit]** sur `Yes`.

1. Si vous souhaitez stocker en toute sécurité les informations de paiement/carte de crédit des clients, de sorte que les clients n&#39;aient pas à saisir à nouveau les informations de paiement, définissez **[!UICONTROL Vault Enabled]** sur `Yes`.

### Étape 3 : configuration du crédit PayPal de publicité/de la publicité PayPal de publicité (facultatif)

À compter de la version 2.4.3, PayPal PayLater est pris en charge dans les déploiements qui incluent PayPal. Cette fonctionnalité permet aux acheteurs de payer une commande par versements bimensuels au lieu de payer le montant complet au moment de l’achat. L’expérience de crédit PayPal est obsolète.

Définissez **[!UICONTROL Enable PayPal PayLater Experience]** sur l’une des options suivantes :

- `Yes` - Pour configurer Advertising PayPal PayLater
- `No` - Pour configurer le crédit Advertising PayPal

#### Publicité Crédit PayPal

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Advertise PayPal Credit]** .

   ![Publicité du crédit PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. Pour obtenir les informations sur votre compte, cliquez sur **[!UICONTROL Get Publisher ID from PayPal]** et suivez les instructions.

1. Saisissez votre **[!UICONTROL Publisher ID]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Home Page]** .

   ![ Paramètres de page d’accueil du crédit PayPal ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

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

1. Développez le ![sélecteur d’extension](../assets/icon-display-expand.png) des sections restantes et répétez les étapes précédentes pour les paramètres de la page d’accueil :

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### Publicité PayPal PayLater

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Advertise PayPal PayLater]** .

1. Définissez **[!UICONTROL Enable PayPal PayLater]** sur `Yes`.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Home Page]** .

   ![ Paramètres de page d’accueil du crédit PayPal ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. Pour placer une bannière sur la page, définissez **[!UICONTROL Display]** sur `Yes`.

1. Définissez **[!UICONTROL Position]** sur l’une des options suivantes :

   - `Header (center)`
   - `Sidebar`

1. Définissez **[!UICONTROL Style Layout]** sur l’une des options suivantes :

   - `Text`
   - `Flex`

1. Pour [!UICONTROL Style Layout] **[!UICONTROL Text]** uniquement, définissez **[!UICONTROL Logo Type]** sur l&#39;une des options suivantes :

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. Pour [!UICONTROL Style Layout] **[!UICONTROL Text]** uniquement, définissez **[!UICONTROL Logo Position]** sur l&#39;une des options suivantes :

   - `Left`
   - `Right`
   - `Top`

1. Pour [!UICONTROL Style Layout] **[!UICONTROL Text]** uniquement, définissez **[!UICONTROL Text Color]** sur l&#39;une des options suivantes :

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. Pour [!UICONTROL Style Layout] **[!UICONTROL Text]** uniquement, définissez **[!UICONTROL Text Size]** sur l&#39;une des options suivantes :

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. Pour [!UICONTROL Style Layout] **[!UICONTROL Flex]** uniquement, définissez **[!UICONTROL Ratio]** sur l&#39;une des options suivantes :

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. Pour [!UICONTROL Style Layout] **[!UICONTROL Flex]** uniquement, définissez **[!UICONTROL Color]** sur l&#39;une des options suivantes :

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

1. Développez le ![sélecteur d’extension](../assets/icon-display-expand.png) des sections restantes et répétez les étapes précédentes :

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### Étape 4 : définition des paramètres de base

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Basic Settings - PayPal Payflow Pro]** .

   ![Paramètres de base - PayPal Payflow Pro_](../configuration-reference/sales/assets/payment-methods-paypal-payflow-pro-basic-settings.png){width="600" zoomable="yes"}

1. Pour **[!UICONTROL Title]**, saisissez un titre qui identifie PayPal Payflow Pro lors du passage en caisse.

   Il est recommandé d’utiliser le titre _Débit ou Carte de crédit_.

1. Si vous proposez plusieurs méthodes de paiement, saisissez un nombre pour **[!UICONTROL Sort Order]** afin de déterminer l’ordre dans lequel Payflow Pro apparaît lorsqu’il est répertorié avec les autres méthodes de paiement.

   Ce nombre est relatif aux autres modes de paiement. (`0` = premier, `1` = deuxième, `2` = troisième, etc.)

1. Définissez **[!UICONTROL Payment Action]** sur l’une des options suivantes :

   - `Authorization` - Approuve l’achat et met un frein aux fonds. Le montant n’est pas retiré tant qu’il n’a pas été capturé par le marchand.
   - `Sale` - Le montant de l’achat est autorisé et immédiatement retiré du compte du client.

1. Pour **[!UICONTROL Credit Card Settings]**, sélectionnez les cartes de crédit que vous acceptez pour paiement dans votre boutique.

   Pour sélectionner plusieurs cartes, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chacune d’elles.

   >[!NOTE]
   >
   >American Express requiert un accord supplémentaire.

### Étape 5 : définition des paramètres avancés

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Advanced Settings]** .

   ![Paramètres avancés - PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payflow-pro-advanced-settings.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Payment Applicable From]** sur l’une des options suivantes :

   - `All Allowed Countries` - Les clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiés dans votre configuration de magasin peuvent utiliser ce mode de paiement.
   - `Specific Countries` - Après avoir choisi cette option, la liste _[!UICONTROL Payment from Specific Countries]_&#x200B;s’affiche. Maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et sélectionnez chaque pays de la liste dans lequel les clients peuvent effectuer des achats dans votre boutique.

1. Pour écrire des communications avec le système de paiement dans le fichier journal, définissez **[!UICONTROL Debug Mode]** sur `Yes`.

   >[!NOTE]
   >
   >Conformément aux normes de sécurité des données PCI, les informations de carte de crédit ne sont pas enregistrées dans le fichier journal.

1. Pour activer la vérification de l’authentification de l’hôte, définissez **[!UICONTROL Enable SSL Verification]** sur `Yes`.

1. Pour obliger les clients à saisir un code CVV, définissez **[!UICONTROL Require CVV Entry]** sur `Yes`.

1. Renseignez les sections suivantes, selon les besoins pour votre magasin :

   - [Paramètres CVV et AVS](#cvv-and-avs-settings)
   - [Paramètres du rapport de règlement](#settlement-report-settings)
   - [Paramètres de l’expérience frontale](#frontend-experience-settings)

#### Paramètres CVV et AVS

Pour déterminer quand une transaction doit être refusée lorsque le système de vérification des adresses identifie une incohérence, indiquez comment gérer différents scénarios.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL CVV and AVS Settings]** .

   ![Paramètres CVV et AVS - PayPal Payflow Pro](./assets/payflow-pro-cvv-avs.png){width="600" zoomable="yes"}

1. Pour rejeter une transaction basée sur une discordance de rue incorrecte, définissez **[!UICONTROL AVS Street Does Not Match]** sur `Yes`.

1. Pour rejeter une transaction basée sur un code postal sans correspondance, définissez **[!UICONTROL AVS Zip Does Not Match]** sur `Yes`.

1. Pour rejeter une transaction en fonction d’un identifiant de pays discordant, définissez **[!UICONTROL International AVS Indicator Does Not Match]** sur `Yes`.

1. Pour rejeter une transaction basée sur un code CVV différent, définissez **[!UICONTROL International Card Security Code Does Not Match]** sur `Yes`.

#### Paramètres du rapport de règlement

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Settlement Report Settings]** .

   ![Paramètres des rapports de règlement - PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. Pour **[!UICONTROL SFTP Credentials]**, procédez comme suit :

   - Si vous vous êtes inscrit au serveur FTP sécurisé PayPal, saisissez les informations d’identification de connexion SFTP suivantes :

      - Connexion
      - Mot de passe

   - Pour exécuter des rapports de test avant de passer en direct avec le passage en caisse express sur votre site, définissez **[!UICONTROL Sandbox Mode]** sur `Yes`.

   - Saisissez le **[!UICONTROL Custom Endpoint Hostname or IP Address]**.

     Par défaut, la valeur est `reports.paypal.com`.

   - Saisissez le **[!UICONTROL Custom Path]** où les rapports sont enregistrés.

     Par défaut, la valeur est `/ppreports/outgoing`.

1. Pour générer des rapports selon un planning, renseignez les paramètres **[!UICONTROL Scheduled Fetching]** :

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

   - Définissez **[!UICONTROL Time of Day]** sur l’heure, la minute et la seconde lorsque vous souhaitez que les rapports soient générés.

#### Paramètres de l’expérience frontale

Utilisez les paramètres d’expérience de la frontière pour choisir les logos PayPal qui apparaissent sur votre site et personnaliser l’aspect de vos pages de marchand PayPal.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Frontend Experience Settings]** .

   ![ Paramètres de l’expérience front-end - PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. Sélectionnez le **[!UICONTROL PayPal Product Logo]** que vous souhaitez voir apparaître dans le bloc PayPal de votre boutique.

   Les logos PayPal sont disponibles en quatre styles et deux tailles :

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. Pour personnaliser l’aspect de vos pages marchandes PayPal :

   - Saisissez le nom du **[!UICONTROL Page Style]** que vous souhaitez appliquer à vos pages marchandes PayPal :

      - `paypal` - Utilise le style de page PayPal.
      - `primary` - Utilise le style de page que vous avez identifié comme le style _primary_ de votre profil de compte.
      - `your_custom_value` - Utilise un style de page de paiement personnalisé, qui est spécifié dans votre profil de compte.

   - Pour **[!UICONTROL Header Image URL]**, saisissez l’URL de l’image que vous souhaitez afficher dans le coin supérieur gauche de la page de paiement. La taille de fichier maximale est de 750 pixels de large par 90 pixels de haut.

     >[!NOTE]
     >
     >PayPal recommande que l’image réside sur un serveur sécurisé (https). Sinon, un navigateur peut avertir que _la page contient des éléments sécurisés et non sécurisés_.

   - Pour définir la couleur de vos pages, saisissez le code hexadécimal à six caractères, sans le symbole `#`, pour chacun des éléments suivants :

      - **[!UICONTROL Header Background Color]** - Couleur de fond de l’en-tête de la page de passage en caisse.
      - **[!UICONTROL Header Border Color]** - Couleur de bordure de deux pixels autour de l’en-tête.
      - **[!UICONTROL Page Background Color]** - Couleur de fond de la page de passage en caisse et autour de l’en-tête et du formulaire de paiement.

### Étape 6 : renseigner les paramètres de base pour le paiement express PayPal

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Basic Settings - PayPal Express Checkout]** .

   ![Paramètres de base du passage en caisse express](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. Pour **[!UICONTROL Title]**, saisissez un titre qui identifie ce mode de paiement lors du passage en caisse.

   Il est recommandé de définir le titre sur _PayPal_ pour chaque vue de magasin.

1. Si vous proposez plusieurs méthodes de paiement, saisissez un numéro pour **[!UICONTROL Sort Order]** afin de déterminer l’ordre dans lequel le paiement express PayPal apparaît lorsqu’il est répertorié avec les autres méthodes de paiement.

   Ce nombre est relatif aux autres modes de paiement. (`0` = premier, `1` = deuxième, `2` = troisième, etc.)

1. Définissez **[!UICONTROL Payment Action]** sur l’une des options suivantes :

   - `Authorization` - Approuve l’achat et met un frein aux fonds. Le montant n’est pas retiré tant qu’il n’a pas été _capturé_ par le commerçant.
   - `Sale` - Le montant de l’achat est autorisé et immédiatement retiré du compte du client.

1. Pour afficher le bouton _[!UICONTROL Check out with PayPal]_&#x200B;sur la page du produit, définissez **[!UICONTROL Display on Product Details Page]**&#x200B;sur `Yes`.

### Étape 7 : Définition des paramètres avancés du paiement express PayPal

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Advanced Settings]** .

   ![Paramètre avancé de passage en caisse express](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Display on Shopping Cart]** sur `Yes`.

1. Définissez **[!UICONTROL Payment Applicable From]** sur l’une des options suivantes :

   - `All Allowed Countries` - Les clients de tous les pays spécifiés dans votre configuration de magasin peuvent utiliser ce mode de paiement.
   - `Specific Countries` - Après avoir choisi cette option, la liste _[!UICONTROL Payment from Specific Countries]_&#x200B;s’affiche. Pour sélectionner plusieurs pays, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque élément.

1. Pour écrire des communications avec le système de paiement dans le fichier journal, définissez **[!UICONTROL Debug Mode]** sur `Yes`.

   >[!NOTE]
   >
   >Conformément aux normes de sécurité des données PCI, les informations de carte de crédit ne sont pas enregistrées dans le fichier journal.

1. Pour activer la vérification de l’authentification de l’hôte, définissez **[!UICONTROL Enable SSL Verification]** sur `Yes`.

1. Pour afficher un résumé complet de la commande du client par article sur le site PayPal, définissez **[!UICONTROL Transfer Cart Line Items]** sur `Yes`.

1. Pour permettre au client de terminer la transaction à partir du site PayPal sans retourner dans votre magasin pour la consultation de la commande, définissez **[!UICONTROL Skip Order Review Step]** sur `Yes`.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

### Étape 8 : Ajout de Google reCAPTCHA

Pour mieux protéger le passage en caisse de PayPal Payflow Pro, activez Google reCAPTCHA. Il comprend des options pour exécuter reCAPTCHA à l’aide d’une interface cliquable ou d’un contrôle invisible pour valider le client. L’option invisible est recommandée pour augmenter la conversion de ventes et protéger votre boutique. Pour plus d’informations, voir [Google reCAPTCHA](../systems/security-google-recaptcha.md).

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://manager.paypal.com/
[3]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[4]: https://developer.paypal.com/docs/payflow/integration-guide/configure-hosted-checkout/#configuring-hosted-pages-using-paypal-manager
