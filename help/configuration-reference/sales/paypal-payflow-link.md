---
title: '[!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Payflow Link]'
description: Passez en revue les paramètres de configuration dans la section [!UICONTROL PayPal Payflow Link] de la page [!UICONTROL Sales] &gt ; [!UICONTROL Payment Methods] de l’Administration Commerce.
exl-id: 5ea30b22-e251-4d93-be2c-d34138ef2f7d
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Payflow Link]

>[!IMPORTANT]
>
>**Conditions requises pour PSD2 :** <br/>
>À compter du 14 septembre 2019, les banques européennes pourraient refuser les paiements qui ne répondent pas aux exigences de [PSD2](../../getting-started/compliance-payment-services-directive.md). Pour se conformer à PSD2, [!DNL PayPal Payflow Link] doit être intégré à [!DNL Cardinal Commerce]. Pour en savoir plus, consultez la section [3-D Secure for Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

{{config}}

## [!UICONTROL Required Settings]

![Paramètres requis](./assets/paypal-payflow-link-settings.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | Site internet | (Facultatif) Toute adresse e-mail associée à votre compte marchand PayPal. Les adresses e-mail sont sensibles à la casse et doivent correspondre exactement aux adresses qui se trouvent dans votre compte. |
| [!UICONTROL Partner] | Site internet | Votre identifiant de partenaire PayPal, le cas échéant. |
| [!UICONTROL Vendor] | Site internet | Votre nom d&#39;utilisateur PayPal. |
| Utilisateur | Site internet | ID d&#39;un utilisateur supplémentaire sur votre compte PayPal. S&#39;il n&#39;y a pas d&#39;autres utilisateurs sur le réseau, entrez votre ID de fournisseur ou de marchand. |
| [!UICONTROL Password] | Site internet | Mot de passe associé à votre compte marchand PayPal. |
| [!UICONTROL Test Mode] | Site internet | Lorsqu&#39;elle est activée, exécute PayPal Payflow Pro dans un environnement de test. Désactivez le mode test lorsque vous êtes prêt à activer le mode production. Options : `Yes` / `No` |
| [!UICONTROL Use Proxy] | Site internet | Un proxy peut être utilisé pour rediriger le trafic lorsque le pare-feu du serveur empêche l’accès direct au serveur PayPal. Le cas échéant, identifie le serveur proxy utilisé pour établir la connexion au serveur PayPal. Options : `Yes` / `No` <br/><br/>Si cette option est activée, définissez les options de proxy : <br/>**`Proxy Host`**- Adresse IP de l’hôte proxy.<br/>**`Proxy Port`** - Numéro du port du proxy. |
| [!UICONTROL Enable Payflow Link] | Site internet | Détermine si PayPal Payflow Link est disponible pour vos clients comme mode de paiement. |
| [!UICONTROL Enable Express Checkout] | Site internet | Détermine si PayPal Express Checkout est disponible pour vos clients comme mode de paiement. |
| [!UICONTROL Enable PayPal Credit] | Site internet | Détermine si le crédit PayPal est disponible pour vos clients en tant qu&#39;option de paiement. |

{style="table-layout:auto"}

## [!UICONTROL Advertise PayPal Credit]

![Annoncer un crédit PayPal](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | Site internet | ID d&#39;éditeur associé à votre compte de crédit PayPal. |
| [!UICONTROL Get Publisher ID from PayPal] |  | Récupère votre ID d&#39;éditeur à partir de PayPal. |
| [!UICONTROL Home Page] | Site internet | Détermine la position et la taille de la bannière [!DNL PayPal Credit] sur la page d’accueil. Options : <br/>**`Display`**- Détermine si une bannière [!DNL PayPal Credit] s’affiche sur la page d’accueil de votre boutique. Options : `Yes` / `No`<br/>**`Position`** - Détermine la position de la bannière [!DNL PayPal Credit] sur la page d’accueil. Options : En-tête (centre) / Barre latérale (droite) <br/>**`Size`**- Détermine la taille de la bannière [!DNL PayPal Credit] sur la page d’accueil. Options : `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | Site internet | Détermine la position et la taille de la bannière de [!DNL PayPal Credit] sur les pages de catégorie. Options : (identique à [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | Site internet | Détermine la position et la taille de la bannière de [!DNL PayPal Credit] sur les pages de produits. Options : (identique à [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | Site internet | Détermine la position et la taille de la bannière [!DNL PayPal Credit] sur la page du panier. Options : (identique à [!UICONTROL Home Page]) |

{style="table-layout:auto"}

### [!UICONTROL Basic Settings]

![Paramètres de base](./assets/payment-methods-paypal-payflow-link-basic-settings.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Title] | Affichage de la boutique | Nom qui identifie PayPal Payflow Link comme mode de paiement lors du passage en caisse. |
| [!UICONTROL Sort Order] | Affichage de la boutique | Nombre qui détermine l&#39;ordre dans lequel le lien de flux de paiement PayPal apparaît lorsqu&#39;il est répertorié avec d&#39;autres modes de paiement lors du passage en caisse. |
| [!UICONTROL Payment Action] | Site internet | Détermine l&#39;action entreprise par PayPal lors de la soumission d&#39;une commande. Options : <br/>**`Authorization`**- Valide l’achat, mais bloque les fonds. Le montant n&#39;est pas retiré tant qu&#39;il n&#39;a pas été « capturé » par le commerçant.<br/>**`Sale`** - Le montant de l&#39;achat est autorisé et immédiatement retiré du compte du client. |

{style="table-layout:auto"}

### [!UICONTROL Advanced Settings]

![Paramètres avancés](./assets/payment-methods-paypal-payflow-link-advanced-settings.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Payment Applicable From] | Site internet | Détermine la plage de la sélection de pays applicable. Options : Tous Les Pays Autorisés / Pays Spécifiques |
| [!UICONTROL Countries Payment Applicable From] | Site internet | Identifie chaque pays d&#39;où le paiement est accepté. Seuls les clients disposant d&#39;une adresse de facturation dans un pays sélectionné peuvent effectuer des achats avec ce mode de paiement. |
| [!UICONTROL Debug Mode] | Site internet | Enregistre les messages envoyés entre votre magasin et le système de paiement dans un fichier journal. Options : `Yes` / `No` <br/><br/>**_Note:_** Le fichier journal est stocké sur le serveur et n’est accessible que par les développeurs. Conformément aux normes PCI Data Security, les informations de carte de crédit ne sont pas enregistrées dans le fichier journal. |
| [!UICONTROL Enable SSL Verification] | Site internet | Détermine si le canal sécurisé sur l’hôte est vérifié avant qu’une transaction ne soit effectuée. Options : `Yes` / `No` |
| [!UICONTROL CVV Entry is Editable] | Site internet | Détermine si le client ou la cliente peut modifier le fichier CVV après l’avoir saisi. Options : `Yes` / `No` |
| [!UICONTROL Require CVV Entry] | Site internet | Détermine si les clients doivent saisir le code CVV au verso de leur carte de crédit. Options : `Yes` / `No` |
| [!UICONTROL Send Email Confirmation] | Site internet | Détermine si le client reçoit un e-mail de confirmation du paiement. Options : `Yes` / `No` |
| [!UICONTROL URL Method for Cancel  URL and Return URL] | Site internet | Détermine la méthode utilisée pour échanger des informations avec le serveur PayPal lors d&#39;une transaction. Options : <br/>**`GET`**- Récupère les informations issues d’un processus. (Il s’agit de la méthode par défaut.)<br/>**`POST`** - Envoie un bloc de données, telles que des données saisies dans un formulaire, au processus de gestion des données. |

{style="table-layout:auto"}

## [!UICONTROL Settlement Report Settings]

![Paramètres du rapport de règlement](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| **[!UICONTROL SFTP Credentials]** |  |  |
| [!UICONTROL Login] | Site internet | Nom d&#39;utilisateur requis pour se connecter au serveur FTP sécurisé de PayPal. |
| [!UICONTROL Password] | Site internet | Mot de passe requis pour se connecter au serveur FTP sécurisé de PayPal. |
| [!UICONTROL Sandbox Mode] | Site internet | Lorsqu’il est activé, exécute les rapports dans un environnement de test avant la mise en production dans l’environnement de production. Options : `Yes` / `No` |
| [!UICONTROL Custom Endpoint Hostname or IP-Address] | Site internet | URL de gestion des rapports de règlement. Valeur par défaut : `reports.paypal.com` |
| [!UICONTROL Custom Path] | Site internet | Chemin d’accès où les rapports de règlement sont enregistrés sur votre serveur. Valeur par défaut : `/ppreports/outgoing` |
| **[!UICONTROL Scheduled Fetching]** |  |  |
| [!UICONTROL Enable Automatic Fetching] | Site internet | Lorsqu&#39;elle est activée, récupère automatiquement les rapports de règlement selon le calendrier. Options : `Yes` / `No` |
| [!UICONTROL Schedule] | Global | Détermine la fréquence de génération des rapports de règlement par PayPal. Options : `Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days` |
| [!UICONTROL Time of Day] | Global | Détermine l&#39;heure, la minute et la seconde auxquelles les rapports de règlement sont générés. |

{style="table-layout:auto"}

## [!UICONTROL Frontend Experience Settings]

![Paramètres d’expérience front-end](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | Affichage de la boutique | Détermine le logo PayPal qui apparaît dans votre boutique. Il existe quatre styles de base dans deux tailles. Options : `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| Style des pages marchandes PayPal |  |  |
| [!UICONTROL Page Style] | Affichage de la boutique | Détermine l&#39;apparence de votre page de vendeur PayPal. Valeurs autorisées : <br/>**`paypal`**- Utilise le style de page PayPal.<br/>**`primary`** - Utilise le style de page que vous avez identifié comme style « principal » dans le profil de votre compte. <br/>**`your_custom_value`**- Utilise un style de page de paiement personnalisé, spécifié dans le profil de votre compte. |
| [!UICONTROL Header Image URL] | Affichage de la boutique | URL de l’image qui s’affiche dans le coin supérieur gauche de la page de passage en caisse. La taille maximale est de 750 x 90 pixels. <br/><br/>**_Note:_** PayPal recommande de stocker l&#39;image sur un serveur sécurisé (https). Dans le cas contraire, le navigateur du client peut signaler que « la page contient des éléments sécurisés et non sécurisés ». |
| [!UICONTROL Header Image Background Color] | Affichage de la boutique | Code [couleur hexadécimale](https://en.wikipedia.org/wiki/Web_colors) de six caractères pour la couleur d’arrière-plan de l’en-tête sur la page de passage en caisse. Vous pouvez saisir le code en majuscules et en minuscules. |
| [!UICONTROL Header Image Border Color] | Affichage de la boutique | Code couleur hexadécimal de six caractères pour la bordure de deux pixels autour de l’en-tête. |
| [!UICONTROL Page Background Color] | Affichage de la boutique | Code couleur hexadécimal de six caractères pour la couleur d’arrière-plan de la page de passage en caisse qui s’affiche derrière l’en-tête et le formulaire de paiement. |

{style="table-layout:auto"}

### [!UICONTROL Basic Settings - PayPal Express Checkout]

![Paramètres de base de PayPal Express Checkout](./assets/payment-methods-paypal-payflow-link-express-checkout-basic-settings.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Title] | Affichage de la boutique | Un nom qui identifie le mode de paiement de PayPal Express Checkout lors du passage en caisse. |
| [!UICONTROL Sort Order] | Affichage de la boutique | Nombre qui détermine l&#39;ordre dans lequel apparaît le paiement PayPal Express lorsqu&#39;il est indiqué avec d&#39;autres modes de paiement lors du paiement. Saisissez `0` pour le haut de la liste. |
| [!UICONTROL Payment Action] | Site internet | Détermine l&#39;action entreprise par PayPal lorsqu&#39;il reçoit une commande. Options : <br/>**`Authorization`**- Valide l’achat, mais bloque les fonds. Le montant n&#39;est pas retiré tant qu&#39;il n&#39;a pas été « capturé » par le commerçant.<br/>**`Sale`** - Le montant de l&#39;achat est autorisé et immédiatement retiré du compte du client. <br/>**`Order`**- Représente un accord avec PayPal qui permet au marchand de capturer un ou plusieurs montants jusqu&#39;au total commandé à partir du compte acheteur du client, dans un délai défini. Cela peut prendre jusqu’à 29 jours. Une ou plusieurs factures doivent être générées à partir de l’administrateur Commerce pour récupérer les fonds. |
| [!UICONTROL URL Display on Product Details Page] | Affichage de la boutique | Détermine si le bouton « Passer en caisse avec PayPal » s&#39;affiche sur les pages de produits. Options : `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Advanced Settings - PayPal Express Checkout]

![Paramètres avancés](./assets/payment-methods-paypal-payflow-link-express-checkout-advanced-settings.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | Affichage de la boutique | Détermine si PayPal Express Checkout apparaît comme option de paiement dans le panier. Options : Oui (Recommandé) / Non |
| [!UICONTROL Payment Action Applicable From] | Site internet | Détermine la plage de la sélection de pays applicable. Options : Tous Les Pays Autorisés / Pays Spécifiques |
| [!UICONTROL Countries Payment Applicable From] | Site internet | Identifie chaque pays d&#39;où le paiement est accepté. Seuls les clients disposant d&#39;une adresse de facturation dans un pays sélectionné peuvent effectuer des achats avec ce mode de paiement. |
| [!UICONTROL Debug Mode] | Site internet | Enregistre les messages envoyés entre votre boutique et le système de paiement PayPal dans un fichier journal. Options : `Yes` / `No` <br/><br/>**_Note:_** Le fichier journal est stocké sur le serveur et n’est accessible que par les développeurs. Conformément aux normes PCI Data Security, les informations de carte de crédit ne sont pas enregistrées dans le fichier journal. |
| [!UICONTROL Enable SSL Verification] | Site internet | Permet de vérifier le certificat de sécurité de l&#39;hôte. Options : `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Site internet | Affiche un résumé complet des articles de la ligne du panier du client sur le site PayPal. Options : `Yes` / `No` |
| [!UICONTROL Skip Order Review Step] | Site internet | Détermine si les clients peuvent terminer la transaction à partir du site PayPal ou s&#39;ils doivent retourner dans votre magasin et terminer l&#39;étape de révision de la commande avant d&#39;envoyer la commande. Options : `Yes` / `No` |

{style="table-layout:auto"}
