---
title: PayPal payment Standard
description: Découvrez comment configurer PayPal payment Standard en tant que solution de paiement en ligne sur votre boutique.
exl-id: b4024dac-34d7-4f1a-ad9d-0fc406194609
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2073'
ht-degree: 0%

---

# PayPal payment Standard

[PayPal payment Standard][4] est le moyen le plus simple d’accepter des paiements en ligne. Vous pouvez offrir à vos clients la commodité de paiement par carte de crédit et par PayPal en ajoutant simplement un bouton de passage en caisse à votre boutique.

>[!NOTE]
>
>Pour les commerçants en dehors des États-Unis, on l&#39;appelle _Payes standard du site Web de PayPal_.

Avec PayPal payment Standard, vous pouvez balayer les cartes de crédit sur les appareils mobiles. Il n&#39;y a pas de frais mensuels et vous pouvez être payé par eBay. Les cartes de crédit prises en charge comprennent Visa, MasterCard, Discover et American Express. De plus, les clients peuvent payer directement à partir de leurs comptes personnels PayPal. PayPal payment Standard est disponible dans tous les pays sur la liste de référence mondiale de PayPal.

>[!IMPORTANT]
>
>**Exigences de PSD2 :** <br/>
>À compter du 14 septembre 2019, les banques européennes pourraient refuser les paiements qui ne satisfont pas [PSD2](../getting-started/compliance-payment-services-directive.md) conditions requises. Aucune action n’est nécessaire pour que PayPal payment Standard soit conforme au PSD 2, car toutes les exigences sont traitées par PayPal.

## Exigences du marché

- [Compte professionnel PayPal][1]

## Processus de passage en caisse

Pour les clients, PayPal payment Standard est un processus en une seule étape si les informations de carte de crédit sur leurs comptes personnels PayPal sont à jour.

1. **Ordre des lieux du client** - Le client clique/appuie sur la balise _Payer maintenant_ pour terminer l’achat.

1. **PayPal traite la transaction** - Le client est redirigé vers le site PayPal pour terminer la transaction.

## Configuration de PayPal payment Standard

>[!NOTE]
>
>PayPal payment Standard ne peut pas être utilisé simultanément avec toute autre méthode PayPal, y compris le passage en caisse express. Si vous modifiez des solutions de paiement, celle utilisée précédemment est désactivée.

>[!TIP]
>
>Cliquez sur **[!UICONTROL Save Config]** à tout moment pour enregistrer votre progression.

### Etape 1 : lancer la configuration

Cette méthode de configuration suppose que vous disposez d’un compte PayPal existant.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Payment Methods]**.

1. Si votre installation Commerce comporte plusieurs sites web, magasins ou vues, définissez **[!UICONTROL Store View]** à la vue magasin dans laquelle vous souhaitez appliquer cette configuration.

1. Dans le _[!UICONTROL Merchant Location]_, sélectionnez **[!UICONTROL Merchant Country]**où se trouve votre entreprise.

   Ce paramètre détermine la sélection des solutions PayPal qui apparaissent dans la configuration.

   ![Pays du commerce](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. Développer **[!UICONTROL PayPal All-in-One Payment Solutions]** et cliquez sur **[!UICONTROL Configure]** pour **[!UICONTROL Payments Standard]**.

   ![PayPal payment Standard](./assets/paypal-payments-standard.png){width="700" zoomable="yes"}

### Étape 2 : activation et connexion de votre compte PayPal

![Configuration de PayPal payment Standard](./assets/paypal-payments-display.png){width="600" zoomable="yes"}

1. Connectez votre compte à des fins de test ou de production :

   - Pour le mode test (développement), cliquez sur **[!UICONTROL Sandbox Credentials]** et saisissez votre [Environnement de test PayPal][3] informations d’identification.
   - Pour le mode de production, cliquez sur **[!UICONTROL Connect with PayPal]** et saisissez vos informations d’identification de compte de production.

   Une fois votre connexion validée, vous pouvez continuer.

1. Définir **[!UICONTROL Enable this Solution]** to `Yes`.

1. Si vous souhaitez proposer [Crédit PayPal](paypal.md#paypal-credit-and-pay-later) à vos clients, définissez **[!UICONTROL Enable PayPal Credit]** to `Yes`.

### Étape 3 : renseigner les paramètres de la norme de paiement

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Payments Standard]** .

   ![Paramètres requis](../configuration-reference/sales/assets/payment-methods-paypal-payments-standard-required.png){width="600" zoomable="yes"}

1. Saisissez le **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >Les adresses électroniques sont sensibles à la casse. Pour recevoir le paiement, l’adresse électronique que vous saisissez doit correspondre à l’adresse électronique spécifiée dans votre compte marchand PayPal.

   Si vous ne disposez pas d’un compte PayPal, cliquez sur **[!UICONTROL Start accepting payments via PayPal]**.

1. Définir **[!UICONTROL API Authentication Methods]** à l’une des options suivantes :

   - `API Signature` - Cette méthode d’authentification PayPal est la plus facile à mettre en oeuvre. Elle est basée sur votre nom d’utilisateur, votre mot de passe et une chaîne de caractères et de nombres uniques qui identifient votre compte. Les informations d’identification de signature d’API n’expirent pas.
   - `API Certificate` - Cette méthode d’authentification PayPal est plus sécurisée, basée sur votre nom d’utilisateur, votre mot de passe et un certificat téléchargeable. Les informations d’identification API expirent après trois ans et doivent être renouvelées.

   Au besoin, procédez comme suit :

   - **[!UICONTROL API Username]**
   - **[!UICONTROL API Password]**
   - **[!UICONTROL API Signature]**

1. Si vous utilisez des informations d’identification de votre compte sandbox, définissez **[!UICONTROL Sandbox Mode]** to `Yes`.

   Lors du test de la configuration dans un environnement de test, utilisez uniquement [numéros de carte de crédit][2] qui sont recommandés par PayPal. Lorsque vous êtes prêt à passer en production, revenez à la configuration et définissez le mode Sandbox sur . `No` et connectez-vous à votre compte PayPal de production.

1. Si votre système utilise un serveur proxy pour établir la connexion entre Adobe Commerce ou Magento Open Source et le système de paiement PayPal, définissez **[!UICONTROL API Uses Proxy]** to `Yes` et procédez comme suit :

   - **[!UICONTROL Proxy Host]**
   - **[!UICONTROL Proxy Port]**

### Étape 4 : configuration du crédit PayPal de publicité/de la publicité PayPal de publicité plus tard (facultatif)

À compter de la version 2.4.3, PayPal PayLater est pris en charge dans les déploiements qui incluent PayPal. Cette fonctionnalité permet aux acheteurs de payer une commande par versements bimensuels au lieu de payer le montant complet au moment de l’achat. L’expérience de crédit PayPal est obsolète.

Définir **[!UICONTROL Enable PayPal PayLater Experience]** à l’une des options suivantes :

- `Yes` - Pour configurer Advertising PayPal PayLater
- `No` - Pour configurer le crédit Advertising PayPal

#### Publicité Crédit PayPal

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Advertise PayPal Credit]** .

   ![Paramètres de la page d’accueil du crédit PayPal Advertiser](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. Pour obtenir les informations sur votre compte, cliquez sur **[!UICONTROL Get Publisher ID from PayPal]** et suivez les instructions.

1. Saisissez votre **[!UICONTROL Publisher ID]**.

   ![Publicité Crédit PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Home Page]** .

1. Pour placer une bannière sur la page, définissez **[!UICONTROL Display]** to `Yes`.

1. Définir **[!UICONTROL Position]** à l’une des options suivantes :

   - `Header (center)`
   - `Sidebar (right)`

1. Définir **[!UICONTROL Size]** à l’une des options suivantes :

   - `190 x 100`
   - `234 x 60`
   - `300 x 50`
   - `468 x 60`
   - `728 x 90`
   - `800 x 66`

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) les sections restantes et répétez les étapes précédentes :

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### Publicité PayPal PayLater

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Advertise PayPal PayLater]** .

1. Définir **[!UICONTROL Enable PayPal PayLater]** to `Yes`.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Home Page]** .

   ![Paramètres de la page d’accueil du crédit PayPal Advertiser](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. Pour placer une bannière sur la page, définissez **[!UICONTROL Display]** to `Yes`.

1. Définir **[!UICONTROL Position]** à l’une des options suivantes :

   - `Header (center)`
   - `Sidebar`

1. Définir **[!UICONTROL Style Layout]** à l’une des options suivantes :

   - `Text`
   - `Flex`

1. Pour [!UICONTROL Style Layout] **[!UICONTROL Text]** uniquement, défini **[!UICONTROL Logo Type]** à l’une des options suivantes :

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. Pour [!UICONTROL Style Layout] **[!UICONTROL Text]** uniquement, défini **[!UICONTROL Logo Position]** à l’une des options suivantes :

   - `Left`
   - `Right`
   - `Top`

1. Pour [!UICONTROL Style Layout] **[!UICONTROL Text]** uniquement, défini **[!UICONTROL Text Color]** à l’une des options suivantes :

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. Pour [!UICONTROL Style Layout] **[!UICONTROL Text]** uniquement, défini **[!UICONTROL Text Size]** à l’une des options suivantes :

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. Pour [!UICONTROL Style Layout] **[!UICONTROL Flex]** uniquement, défini **[!UICONTROL Ratio]** à l’une des options suivantes :

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. Pour [!UICONTROL Style Layout] **[!UICONTROL Flex]** uniquement, défini **[!UICONTROL Color]** à l’une des options suivantes :

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) les sections restantes et répétez les étapes précédentes :

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **Étape de paiement du passage en caisse**
   - **[!UICONTROL Catalog Category Page]**

### Étape 5 : définition des paramètres de base

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Basic Settings - PayPal Website Payments Standard]** .

   ![Paramètres de base](./assets/paypal-payments-basic.png){width="600" zoomable="yes"}

1. Pour **[!UICONTROL Title]**, saisissez un titre qui identifie ce mode de paiement lors du passage en caisse.

   Il est recommandé d’utiliser le titre _PayPal_ pour toutes les vues de magasin.

1. Si vous proposez plusieurs modes de paiement, saisissez un nombre pour **[!UICONTROL Sort Order]** afin de déterminer l’ordre dans lequel PayPal payment Standard apparaît lorsqu’il est répertorié avec les autres méthodes de paiement.

   Ce nombre est relatif aux autres modes de paiement. (`0` = first, `1` = second, `2` = troisième, etc.)

1. Définir **[!UICONTROL Payment Action]** à l’une des options suivantes :

   - `Authorization` - Valide l&#39;achat et met un frein aux fonds. Le montant n’est pas retiré tant qu’il n’a pas été capturé par le marchand.
   - `Sale` - Le montant de l’achat est autorisé et immédiatement retiré du compte du client.

1. Pour afficher la variable _[!UICONTROL Check out with PayPal]_sur la page produit, définissez **[!UICONTROL Display on Product Details Page]**to `Yes`.

### Étape 6 : Paramètres avancés

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Advanced Settings]** .

   ![Paramètres avancés](../configuration-reference/sales/assets/payment-methods-paypal-payment-standard-advanced.png){width="600" zoomable="yes"}

1. Pour rendre PayPal payment Standard disponible depuis le panier et le mini panier, définissez **[!UICONTROL Display on Shopping Cart]** to `Yes`.

1. Définir **[!UICONTROL Payment from Applicable Countries]** à l’une des options suivantes :

   - `All Allowed Countries` - Clients de tous les [pays](../getting-started/store-details.md#country-options) spécifié dans votre configuration de magasin peut utiliser ce mode de paiement.
   - `Specific Countries` - Après avoir choisi cette option, la variable _[!UICONTROL Payment from Specific Countries]_s’affiche. Pour sélectionner plusieurs pays, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

1. Pour enregistrer les communications avec le système de paiement dans le fichier journal, définissez **[!UICONTROL Debug Mode]** to `Yes`.

   >[!NOTE]
   >
   >Le fichier journal est stocké sur le serveur et accessible uniquement aux développeurs. Conformément aux normes de sécurité des données PCI, les informations de carte de crédit ne sont pas enregistrées dans le fichier journal.

1. Pour activer la vérification SSL, définissez **[!UICONTROL Enable SSL Verification]** to `Yes`.

1. Pour afficher un résumé de chaque élément de ligne dans la commande de votre page de paiements PayPal, définissez **[!UICONTROL Transfer Cart Line Items]** to `Yes`.

   Pour inclure jusqu’à dix options d’expédition dans le résumé, définissez **[!UICONTROL Transfer Shipping Options]** to `Yes`. (Cette option s’affiche uniquement si les éléments de ligne sont définis pour le transfert.)

1. Pour déterminer le type d’image utilisé pour le bouton d’acceptation de PayPal, définissez **[!UICONTROL Shortcut Buttons Flavor]** à l’une des options suivantes :

   - `Dynamic` - (Recommandé) Affiche une image qui peut être modifiée dynamiquement à partir du serveur PayPal.
   - `Static` : affiche une image spécifique qui ne peut pas être modifiée dynamiquement.

1. Pour permettre aux clients qui ne disposent pas d’un compte PayPal d’effectuer un achat avec cette méthode, définissez **[!UICONTROL Enable PayPal Guest Checkout]** to `Yes`.

1. Définir **[!UICONTROL Require Customer's Billing Address]** à l’une des options suivantes :

   - `Yes` - Nécessite l’adresse de facturation du client pour tous les achats.
   - `No` - Ne nécessite pas l’adresse de facturation du client pour les achats.
   - `For Virtual Quotes Only` - Nécessite l’adresse de facturation du client pour les devis virtuels uniquement.

1. Pour autoriser un client à entrer dans une [Contrat de facturation PayPal](paypal-billing-agreements.md) avec votre boutique lorsqu’aucun contrat de facturation actif n’est disponible dans le compte client, définissez **[!UICONTROL Billing Agreement Signup]** à l’une des options suivantes :

   - `Auto` - Le client peut soit conclure un contrat de facturation lors du passage en caisse express, soit utiliser un autre mode de paiement.
   - `Ask Customer` - Le client peut décider s’il souhaite conclure un contrat de facturation au cours du workflow Passage en caisse express.
   - `Never` - Le client ne peut pas conclure de contrat de facturation lors du workflow Passage en caisse express.

   >[!NOTE]
   >
   >Les marchands doivent demander l&#39;assistance technique de PayPal pour activer les contrats de facturation dans leurs comptes. La variable _Signature d’un contrat de facturation_ ne peut être activé que lorsque PayPal a confirmé que les contrats de facturation sont activés pour votre compte marchand.

1. Pour permettre au client de terminer la transaction à partir du site PayPal sans retourner dans votre magasin pour la consultation de la commande, définissez **[!UICONTROL Skip Order Review Step]** to `Yes`.

### Étape 7 : Terminer et enregistrer les paramètres de configuration

1. Renseignez les sections suivantes, selon les besoins pour votre magasin :

   - [Paramètres du contrat de facturation PayPal](#paypal-billing-agreement-settings)
   - [Paramètres du rapport de règlement](#settlement-report-settings)
   - [Paramètres de l’expérience frontale](#frontend-experience-settings)

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

#### Paramètres du contrat de facturation PayPal

A [contrat de facturation](paypal-billing-agreements.md) est un contrat de vente entre le marchand et le client qui a été autorisé par PayPal pour une utilisation avec plusieurs commandes. Pendant le processus de paiement, l’option de paiement du contrat de facturation s’affiche uniquement pour les clients qui ont déjà conclu un contrat de facturation avec votre société. Une fois que PayPal a autorisé l’accord, le système de paiement émet un identifiant de référence unique pour identifier chaque commande associée à l’accord. Comme pour un bon de commande, il n’existe aucune limite au nombre de contrats de facturation qu’un client peut configurer avec votre société.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL PayPal Billing Agreement Settings]** .

   ![Paramètres de contrat de facturation](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Enabled]** to `Yes`.

1. Pour **[!UICONTROL Title]**, saisissez un titre qui identifie la méthode du contrat de facturation PayPal lors du passage en caisse.

1. Si vous proposez plusieurs modes de paiement, saisissez un nombre dans la variable **[!UICONTROL Sort Order]** pour déterminer la séquence dans laquelle le contrat de facturation apparaît lorsqu’il est répertorié avec d’autres méthodes de paiement lors du passage en caisse.

1. Définir **[!UICONTROL Payment Action]** à l’une des options suivantes :

   - `Authorization` - Valide l&#39;achat et met un frein aux fonds. Le montant n’est pas retiré tant qu’il n’a pas été &quot;capturé&quot; par le marchand.
   - `Sale` - Le montant de l’achat est autorisé et immédiatement retiré du compte du client.

1. Définir **[!UICONTROL Payment Applicable From]** à l’une des options suivantes :

   - `All Allowed Countries` - Les clients de tous les pays spécifiés dans votre configuration de magasin peuvent utiliser ce mode de paiement.
   - `Specific Countries` - Après avoir choisi cette option, la variable _[!UICONTROL Payment from Specific Countries]_s’affiche. Pour sélectionner plusieurs pays, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chacun d’eux.

1. Pour enregistrer les communications avec le système de paiement dans le fichier journal, définissez **[!UICONTROL Debug Mode]** to `Yes`.

   >[!NOTE]
   >
   >Le fichier journal est stocké sur le serveur et accessible uniquement aux développeurs. Conformément aux normes de sécurité des données PCI, les informations de carte de crédit ne sont pas enregistrées dans le fichier journal.

1. Pour activer la vérification SSL, définissez **[!UICONTROL Enable SSL Verification]** to `Yes`.

1. Pour afficher un résumé de chaque article dans la commande du client sur votre page de paiements PayPal, définissez **[!UICONTROL Transfer Cart Line Items]** to `Yes`.

1. Pour permettre aux clients d’initier un contrat de facturation à partir du tableau de bord de leur compte client, définissez **[!UICONTROL Allow in Billing Agreement Wizard]** to `Yes`.

#### Paramètres du rapport de règlement

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Settlement Report Settings]** .

   ![Paramètres du rapport de règlement](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. Pour **[!UICONTROL SFTP Credentials]**, procédez comme suit :

   - Si vous vous êtes inscrit au serveur FTP sécurisé PayPal, saisissez les informations d’identification de connexion SFTP suivantes :

      - Connexion
      - Mot de passe

   - Pour exécuter des rapports de test avant de passer en direct avec le passage en caisse express sur votre site, définissez **[!UICONTROL Sandbox Mode]** to `Yes`.

   - Saisissez le **[!UICONTROL Custom Endpoint Hostname or IP Address]**.

     Par défaut, la valeur est `reports.paypal.com`.

   - Saisissez le **[!UICONTROL Custom Path]** où les rapports sont enregistrés.

     Par défaut, la valeur est `/ppreports/outgoing`.

1. Pour générer des rapports selon un calendrier précis, renseignez les **[!UICONTROL Scheduled Fetching]** settings :

   - Définir **[!UICONTROL Enable Automatic Fetching]** to `Yes`.

   - Définir **[!UICONTROL Schedule]** à l’une des options suivantes :

      - `Daily`
      - `Every 3 Days`
      - `Every 7 Days`
      - `Every 10 Days`
      - `Every 14 Days`
      - `Every 30 Days`
      - `Every 40 Days`

     PayPal conserve chaque rapport pendant 45 jours.

   - Définir **[!UICONTROL Time of Day]** à l’heure, à la minute et à la seconde auxquelles les rapports doivent être générés.

#### Paramètres de l’expérience frontale

Utilisez la variable _[!UICONTROL Frontend Experience Settings]_pour choisir les logos PayPal qui apparaissent sur votre site et personnaliser l’aspect de vos pages marchandes PayPal.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Frontend Experience Settings]** .

   ![Paramètres de l’expérience frontale](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. Sélectionnez la variable **[!UICONTROL PayPal Product Logo]** que vous souhaitez voir apparaître dans le bloc PayPal de votre magasin.

   Les logos PayPal sont disponibles en quatre styles et deux tailles :

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. Pour personnaliser l’aspect de vos pages marchandes PayPal :

   - Saisissez le nom du **[!UICONTROL Page Style]** que vous souhaitez appliquer à vos pages marchandes PayPal :

      - `paypal` - Utilise le style de page PayPal.
      - `primary` : permet d’utiliser le style de page que vous avez identifié comme _primary_ style dans votre profil de compte.
      - `your_custom_value` - Utilise un style de page de paiement personnalisé, qui est spécifié dans votre profil de compte.

   - Pour **[!UICONTROL Header Image URL]**, saisissez l’URL de l’image que vous souhaitez voir apparaître dans le coin supérieur gauche de la page de paiement. La taille de fichier maximale est de 750 pixels de large par 90 pixels de haut.

     >[!NOTE]
     >
     >PayPal recommande que l’image réside sur un serveur sécurisé (https). Sinon, un navigateur peut avertir que _la page contient des éléments sécurisés et non sécurisés._.

   - Pour définir la couleur de vos pages, saisissez le code hexadécimal à six caractères, sans le champ `#` pour chacun des symboles suivants :

      - **[!UICONTROL Header Background Color]** - Couleur d’arrière-plan de l’en-tête de la page de passage en caisse.
      - **[!UICONTROL Header Border Color]** - Couleur de bordure de deux pixels autour de l’en-tête.
      - **[!UICONTROL Page Background Color]** - Couleur d’arrière-plan de la page de passage en caisse et autour de l’en-tête et du formulaire de paiement.

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[3]: https://developer.paypal.com/docs/api-basics/sandbox/
[4]: https://developer.paypal.com/docs/paypal-payments-standard/mobile-paypal-payments-standard/
