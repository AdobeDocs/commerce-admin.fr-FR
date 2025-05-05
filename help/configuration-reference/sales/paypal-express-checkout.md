---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL PayPal Express Checkout]'
description: Vérifiez les paramètres de configuration dans la section [!UICONTROL PayPal Express Checkout] de la page [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] de l’administrateur Commerce.
exl-id: aae5b1d9-f47e-447a-b40c-924f8d2ee824
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1702'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Express Checkout]

>[!IMPORTANT]
>
>**Exigences de PSD2 :** <br/>
>À compter du 14 septembre 2019, les banques européennes pourront refuser les paiements qui ne répondent pas aux exigences de [PSD2](../../getting-started/compliance-payment-services-directive.md). Aucune action n’est nécessaire pour que le paiement express PayPal soit conforme au PSD2, car toutes les exigences sont gérées par PayPal.

{{config}}

## [!UICONTROL Required PayPal Settings]

![Paramètres requis pour le paiement express PayPal](./assets/paypal-express-required-settings.png)<!-- zoom -->

<!-- [PayPal Express Checkout Required Settings](../../stores-purchase/paypal-express-checkout.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable this Solution] | Site Web | Active [!DNL PayPal Express Checkout] en tant que méthode de paiement disponible pour vos clients. Options : `Yes` / `No` |
| [!UICONTROL Enable In-Context Checkout Experience] | Site Web | Active la méthode de paiement intégrée (In-Context Checkout) paypal rationalisée comme méthode de paiement disponible pour vos clients. Options : `Yes` / `No` |
| [!UICONTROL Enable PayPal Credit] | Site Web | Active le crédit PayPal pour permettre aux clients d’acheter maintenant, mais de payer ultérieurement. Vous êtes payé d&#39;avance, mais les clients ont plus de temps à payer. Options : `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Express Checkout]

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | Site Web | Indique l’adresse électronique que vous avez spécifiée lors de la création de votre compte marchand PayPal. L’adresse électronique est sensible à la casse et doit correspondre exactement à votre adresse électronique dans le système PayPal. |
| [!UICONTROL API Authentication Methods] | Site Web | Détermine la méthode utilisée pour l’authentification API. Options : <br/>**`API Signature`**- Affiche le champ _[!UICONTROL API Signature]_&#x200B;dans le formulaire.<br/>**`API Certificate`**- Affiche le champ&#x200B;_[!UICONTROL API Certificate]_ dans le formulaire. |
| [!UICONTROL API Username] | Site Web | Nom d’utilisateur de l’API associé à votre compte marchand PayPal. |
| [!UICONTROL API Password] | Site Web | Mot de passe de l’API associé à votre compte marchand PayPal. |
| [!UICONTROL API Signature] | Site Web | Signature d’API associée à votre compte marchand PayPal. |
| [!UICONTROL API Certificate] | Site Web | Naviguez pour charger votre certificat d’API. |
| [!UICONTROL Get Credentials from PayPal] |  | Récupère vos informations d’identification d’API auprès de PayPal. |
| [!UICONTROL Sandbox Credentials] |  | Récupère vos informations d’identification sandbox auprès de PayPal. |
| [!UICONTROL Sandbox Mode] | Site Web | Pour exécuter le paiement express PayPal dans un environnement de test, saisissez les informations d’identification de votre API de test et définissez cette variable sur `Yes`. Options : `Yes` / `No` |
| [!UICONTROL API Uses Proxy] | Site Web | Si votre système utilise un serveur proxy pour établir la connexion entre Commerce et le système PayPal, définissez-le sur `Yes`. Options : `Yes` / `No` |
| [!UICONTROL Proxy Host] | Site Web | Si l’API utilise un proxy, cela spécifie l’adresse IP de l’hôte proxy. |
| [!UICONTROL Proxy Port] | Site Web | Si l’API utilise un proxy, cela spécifie le port utilisé par l’hôte proxy. |

{style="table-layout:auto"}

### [!UICONTROL Advertise PayPal Credit]

![Publicité du crédit PayPal](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | Site Web | Identifiant de l’éditeur associé à votre compte de crédit PayPal. |
| [!UICONTROL Get Publisher ID from PayPal] |  | Récupère votre identifiant d’éditeur auprès de PayPal. |
| [!UICONTROL Home Page] | Site Web | Détermine la position et la taille de la bannière [!DNL PayPal Credit] sur la page d’accueil. Options : <br/>**Affichage** - Affiche une bannière [!DNL PayPal Credit] sur la page d’accueil de votre magasin. Options : `Yes` / `No` <br/>**Position** - Détermine la position de la bannière [!DNL PayPal Credit] sur la page d’accueil. Options : En-tête (centre) / Barre latérale (droite) <br/>**Taille** - Détermine la taille de la bannière [!DNL PayPal Credit] sur la page d’accueil. Options : `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | Site Web | Détermine la position et la taille de la bannière [!DNL PayPal Credit] sur les pages de catégorie. Options : (identique à pour [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | Site Web | Détermine la position et la taille de la bannière [!DNL PayPal Credit] sur les pages de produits. Options : (identique à pour [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | Site Web | Détermine la position et la taille de la bannière [!DNL PayPal Credit] sur la page du panier. Options : (identique à pour [!UICONTROL Home Page]) |

{style="table-layout:auto"}

## [!UICONTROL Basic Settings]

![Paramètres de base](./assets/payment-methods-paypal-express-checkout-basic-settings.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Title] | Affichage en magasin | Nom qui identifie le mode de paiement PayPal Express Checkout lors du passage en caisse. |
| [!UICONTROL Sort Order] | Affichage en magasin | Numéro qui détermine la commande que le paiement express PayPal apparaît lorsqu’il est répertorié avec d’autres méthodes de paiement lors du passage en caisse. Saisissez `0` en haut de la liste. |
| [!UICONTROL Payment Action] | Site Web | Détermine l’action effectuée par PayPal lors de la réception d’une commande. Options : <br/>**`Authorization`**- Approuve l’achat, mais met un frein aux fonds. Le montant n’est pas retiré tant qu’il n’a pas été &quot;capturé&quot; par le marchand.<br/>**`Sale`** - Le montant de l’achat est autorisé et immédiatement retiré du compte du client. <br/>**`Order`**- Représente un accord avec PayPal qui permet au marchand de capturer un ou plusieurs montants au total commandé du compte acheteur du client, dans une période définie. Cela peut aller jusqu’à 29 jours. Une ou plusieurs factures doivent être générées par l’administrateur Commerce pour capturer les fonds. |
| [!UICONTROL Display on Product Details Page] | Affichage en magasin | Détermine si le bouton &quot;Passage en caisse avec PayPal&quot; s’affiche sur les pages du produit. Les options incluent : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Settings]

![Paramètres avancés](./assets/payment-methods-paypal-express-checkout-advanced-settings.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | Affichage en magasin | Détermine si le paiement express PayPal apparaît comme option de paiement dans le panier. Options : `Yes` (PayPal recommandé) / `No` |
| [!UICONTROL Payment Action Applicable From] | Site Web | Détermine la plage de la sélection de pays applicable. Options : `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | Site Web | Identifie chaque pays à partir duquel le paiement est accepté. Seuls les clients ayant une adresse de facturation dans un pays sélectionné peuvent effectuer des achats avec ce mode de paiement. |
| [!UICONTROL Debug Mode] | Site Web | Enregistre les messages envoyés entre votre boutique et le système de paiement dans un fichier journal. Options : `Yes` / `No` <br/><br/>**_Remarque :_**&#x200B;Le fichier journal est stocké sur le serveur et est accessible uniquement aux développeurs. Conformément aux normes de sécurité des données PCI, les informations de carte de crédit ne sont pas enregistrées dans le fichier journal. |
| [!UICONTROL Enable SSL Verification] | Site Web | Active la vérification du certificat de sécurité hôte. Options : `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Site Web | Affiche un résumé complet des éléments de ligne du panier du client sur le site PayPal. Options : `Yes` / `No` |
| [!UICONTROL Transfer Shipping Options] | Site Web | Comprend jusqu’à dix options de livraison sur le site PayPal. Options : `Yes` / `No` |
| [!UICONTROL Shortcut Buttons Flavor] | Affichage en magasin | Détermine le type d’image utilisé pour le bouton d’acceptation de PayPal. Options : <br/>**`Dynamic`**- (Recommandé) Affiche une image qui peut être modifiée dynamiquement à partir du serveur PayPal.<br/>**`Static`** : affiche une image statique qui ne peut pas être modifiée dynamiquement. |
| [!UICONTROL Enable PayPal Guest Checkout] | Site Web | Permet aux clients qui ne disposent pas de comptes PayPal d’effectuer des achats avec PayPal Express Checkout. Options : `Yes` / `No` |
| [!UICONTROL Require Customer's Billing Address] | Site Web | Détermine si l’adresse de facturation du client est requise. Options : `Yes` / `No` / `For Virtual Quotes Only` |
| [!UICONTROL Billing Agreement Signup] | Site Web | Détermine si les clients peuvent conclure un [contrat de facturation](../../stores-purchase/paypal-billing-agreements.md) avec votre boutique. Options : <br/>**`Auto`**- Le client peut s’inscrire à un contrat de facturation lors du passage en caisse express.<br/>**`Ask Customer`** - On demande aux clients s&#39;ils veulent s&#39;inscrire à un contrat de facturation. <br/>**`Never`**- Les clients ne peuvent pas s’inscrire à un contrat de facturation. |
| [!UICONTROL Skip Order Review Step] | Site Web | Détermine si les clients peuvent effectuer la transaction à partir du site PayPal ou s’ils doivent retourner dans votre boutique et terminer l’étape de vérification de la commande avant d’envoyer la commande. Options : `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Billing Agreement Settings]

![Paramètres du contrat de facturation](./assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site Web | Lorsque cette option est activée, les contrats de facturation apparaissent aux clients comme une option de paiement lors du passage en caisse. Options : `Yes` / `No` |
| [!UICONTROL Title] | Affichage en magasin | Libellé de l’option de contrat de facturation PayPal qui apparaît comme option de paiement lors du passage en caisse. |
| [!UICONTROL Sort Order] | Affichage en magasin | Détermine l’ordre dans lequel les contrats de facturation sont répertoriés avec d’autres modes de paiement lors du passage en caisse. |
| [!UICONTROL Payment Action] | Site Web | Détermine la manière dont PayPal gère la transaction : Options : <br/>**Authorization** - Approuve l’achat, mais met un frein aux fonds. Le montant n’est pas retiré tant qu’il n’a pas été &quot;capturé&quot; par le marchand. <br/>**Vente** - Le montant de l’achat est autorisé et immédiatement retiré du compte du client. |
| [!UICONTROL Payment Applicable From] | Site Web | Détermine la plage de la sélection de pays applicable. Options : tous les pays autorisés/pays spécifiques |
| [!UICONTROL Countries Payment Applicable From] | Site Web | Identifie chaque pays à partir duquel le paiement est accepté. Seuls les clients ayant une adresse de facturation dans un pays sélectionné peuvent effectuer des achats avec ce mode de paiement. |
| [!UICONTROL Debug Mode] | Site Web | Enregistre la communication avec le système de paiement dans un fichier journal. Options : `Yes` / `No` <br/><br/>**_Remarque :_**&#x200B;Le fichier journal est stocké sur le serveur et est accessible uniquement aux développeurs. Conformément aux normes de sécurité des données PCI, les informations de carte de crédit ne sont pas enregistrées dans le fichier journal. |
| [!UICONTROL Enable SSL Verification] | Site Web | Permet d’activer une étape de vérification afin de garantir que la transaction a lieu sur un canal SSL chiffré. Options : `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Site Web | Lorsqu’elle est activée, affiche un résumé des éléments de ligne du panier sur la page des paiements PayPal. Options : `Yes` / `No` |
| [!UICONTROL Allow in Billing Agreement Wizard] | Site Web | Lorsqu’elle est activée, les clients peuvent lancer un contrat de facturation à partir du tableau de bord de leur compte client. |

{style="table-layout:auto"}

### [!UICONTROL Settlement Report Settings]

![Paramètres des rapports de règlement](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| **[!UICONTROL SFTP Credentials]** |  |  |
| [!UICONTROL Login] | Site Web | Votre nom d’utilisateur requis pour se connecter au serveur FTP sécurisé de PayPal. |
| [!UICONTROL Password] | Site Web | Votre mot de passe requis pour se connecter au serveur FTP sécurisé de PayPal. |
| [!UICONTROL Sandbox Mode] | Site Web | Lorsqu’elle est activée, exécute les rapports dans un environnement de test avant la mise en ligne dans l’environnement de production. Options : `Yes` / `No` |
| [!UICONTROL Custom Endpoint Hostname or IP-Address] | Site Web | URL à laquelle les rapports de règlement sont gérés. Valeur par défaut : `reports.paypal.com` |
| [!UICONTROL Custom Path] | Site Web | Chemin d’accès où les rapports de résolution sont enregistrés sur votre serveur. Valeur par défaut : `/ppreports/outgoing` |
| **[!UICONTROL Scheduled Fetching]** |  |  |
| [!UICONTROL Enable Automatic Fetching] | Site Web | Lorsque cette option est activée, récupère les rapports de règlement automatiquement selon le calendrier. Options : `Yes` / `No` |
| [!UICONTROL Schedule] | Site Web | Détermine la fréquence de génération des rapports de règlement par PayPal. Options : `Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days` |
| [!UICONTROL Time of Day] | Site Web | Détermine l’heure, la minute et la seconde pendant lesquelles les rapports de règlement sont générés. |

{style="table-layout:auto"}

### [!UICONTROL Frontend Experience Settings]

![ Paramètres de l’expérience frontale - Style de pages marchandes PayPal ](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | Affichage en magasin | Détermine le logo PayPal qui apparaît dans votre boutique. Il existe quatre styles de base en deux tailles. Options : `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| **[!UICONTROL PayPal Merchant Pages Style]** |  |  |
| [!UICONTROL Page Style] | Affichage en magasin | Détermine l’aspect de votre page de commerce PayPal. Valeurs autorisées : **`paypal`** - Utilise le style de page PayPal. <br/>**`primary`**- Utilise le style de page que vous avez identifié comme le style &quot;principal&quot; dans votre profil de compte.<br/>**`your_custom_value`** - Utilise un style de page de paiement personnalisé, qui est spécifié dans votre profil de compte. |
| [!UICONTROL Header Image URL] | Affichage en magasin | URL de l’image qui apparaît dans le coin supérieur gauche de la page de passage en caisse. La taille maximale est de 750 x 90 pixels. <br/><br/>**_Remarque :_**&#x200B;PayPal recommande que l’image soit stockée sur un serveur sécurisé (https). Sinon, le navigateur du client peut avertir que &quot;la page contient des éléments sécurisés et non sécurisés&quot;. |
| [!UICONTROL Header Image Background Color] | Affichage en magasin | Code [hexadécimal ](https://en.wikipedia.org/wiki/Web_colors) à six caractères pour la couleur d’arrière-plan de l’en-tête sur la page de passage en caisse. Vous pouvez saisir le code en majuscules ou en minuscules. |
| [!UICONTROL Header Image Border Color] | Affichage en magasin | Code [hexadécimal de couleur](https://en.wikipedia.org/wiki/Web_colors) à six caractères pour la bordure de deux pixels autour de l’en-tête. |
| [!UICONTROL Page Background Color] | Affichage en magasin | Code [hexadécimal ](https://en.wikipedia.org/wiki/Web_colors) à six caractères pour la couleur d’arrière-plan de la page de passage en caisse qui apparaît derrière l’en-tête et le formulaire de paiement. |

{style="table-layout:auto"}

#### [!UICONTROL Customize Smart Buttons (Basic)]

![Paramètres de l’expérience frontale - Personnaliser les boutons intelligents](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings2.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Customize Button] | Affichage en magasin | Détermine si les boutons intelligents PayPal peuvent être personnalisés pour correspondre à la mise en page et au thème de votre magasin. Vous pouvez appliquer ces modifications indépendamment sur la page Passage en caisse, sur les pages Produit , sur la page Panier et dans le mini panier. |
| [!UICONTROL Label] | Affichage en magasin | Texte affiché par PayPal sur le bouton de paiement intelligent. Options : <br/>**`Checkout`**(s’affiche comme &quot;paiement PayPal&quot;)<br/>**`Pay`** (s’affiche comme &quot;paiement avec PayPal&quot;) <br/>**`Buy Now`**(s’affiche comme &quot;achat avec PayPal&quot;)<br/>**`PayPal`** (s’affiche comme &quot;paiementPal&quot;) <br/>**`Installment`**(s’affiche comme &quot;paiementPal&quot;)<br/>**`Credit`** (s’affiche comme &quot;paiementPal CREDIT&quot;) |
| [!UICONTROL Layout] | Affichage en magasin | Détermine s’il faut afficher les boutons intelligents PayPal verticalement ou horizontalement. Options : <br/>**`Vertical`**- L’acheteur doit se connecter à PayPal ou créer un compte PayPal, que l’option &quot;Activer le passage en caisse des invités&quot; soit sélectionnée ou non.<br/>**`Horizontal`** - Lorsque &quot;Activer le passage en caisse des invités&quot; est sélectionné, affiche le bouton **`Pay with Debit Card or Credit Card`** dans la fenêtre contextuelle PayPal. Dans le cas contraire, l&#39;acheteur doit se connecter à PayPal ou créer un compte PayPal. |
| [!UICONTROL Size] | Affichage en magasin | Définit la taille du bouton de paiement intelligent. Options : <br/>**`Medium`**- 250 pixels par 35 pixels<br/>**`Large`** - 350 pixels par 40 pixels <br/>**`Responsive`**- (Par défaut) S’ajuste à la largeur du conteneur. La largeur minimale est de 100 pixels et la largeur maximale est de 500 pixels. La hauteur s’ajuste dynamiquement en fonction de la largeur. |
| [!UICONTROL Shape] | Affichage en magasin | Définit la forme du bouton de paiement intelligent. Options : `Pill` (par défaut) / `Rectangle` |
| [!UICONTROL Color] | Affichage en magasin | Définissez la couleur du bouton de paiement intelligent. Options : `Gold` (par défaut) / `Blue` / `Silver` / `Black` |

{style="table-layout:auto"}

#### [!UICONTROL Customize Smart Buttons (Features)]

![Paramètres de l’expérience frontale - Personnaliser les boutons intelligents (fonctionnalités)](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings3.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Disable Funding Options] | Affichage en magasin | Détermine les autres options de financement PayPal qui s’affichent sur la page Passage en caisse . Les options sélectionnées ne s’affichent jamais sur la page Passage en caisse. Les options non sélectionnées s’affichent uniquement si PayPal prend en charge la devise du magasin et l’emplacement de l’acheteur. Options : `PayPal Credit` / `PayPal Guest Checkout` `Credit Card Icons` / `Elektronisches Lastschriftverfahren - German ELV` |

{style="table-layout:auto"}
