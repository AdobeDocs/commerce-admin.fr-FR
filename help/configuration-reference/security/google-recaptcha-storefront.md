---
title: '[!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront] de l’administrateur Commerce.
exl-id: 6c03ee68-7421-4c74-bdc1-0855f088b7f9
feature: Configuration, Security
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1299'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Storefront]

>[!IMPORTANT]
>
>Avant de pouvoir configurer Google reCAPTCHA, vous devez vous assurer que `PHP.ini` comprend le paramètre suivant : `allow_url_fopen = 1`. Cela peut nécessiter l’aide des développeurs. Voir [Paramètres PHP](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) dans le _Guide d’installation_.

{{config}}

Pour plus d’informations sur l’utilisation de Google reCAPTCHA pour sécuriser votre boutique, voir Google [reCAPTCHA](../../systems/security-google-recaptcha.md) dans le _Guide des systèmes d’administration_.

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2 (&quot;Je ne suis pas un robot&quot;)](./assets/recaptcha-storefront-v2-not-robot.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--|--|--|
| [!UICONTROL Google API Website Key] | Site Web | Clé de site web créée lors de l’enregistrement de votre compte Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Site Web | Clé secrète associée à votre compte Google reCAPTCHA. |
| [!UICONTROL Size] | Site Web | Taille de la zone reCAPTCHA de Google qui s’affiche lorsqu’un client se connecte à son compte. Options : `Normal` (par défaut) / `Compact` |
| [!UICONTROL Theme] | Site Web | Détermine le style de la zone Google reCAPTCHA. Options : `Light Theme` (par défaut) / `Dark Theme` |
| [!UICONTROL Language Code] | Affichage en magasin | La variable [code à deux caractères](https://developers.google.com/recaptcha/docs/language) qui spécifie la langue utilisée pour le texte et la messagerie reCAPTCHA de Google. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 Invisible](./assets/recaptcha-storefront-v2-invisible.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--|--|--|
| [!UICONTROL Google API Website Key] | Site Web | Clé de site web créée lors de l’enregistrement de votre compte Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Site Web | Clé secrète associée à votre compte Google reCAPTCHA. |
| [!UICONTROL Invisible Badge Position] | Site Web | Position du badge reCAPTCHA invisible sur chaque page. Options : `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Global | Détermine le style de la zone Google reCAPTCHA. Options : `Light Theme` (par défaut) / `Dark Theme` |
| [!UICONTROL Language Code] | Affichage en magasin | A [code à deux caractères](https://developers.google.com/recaptcha/docs/language) qui spécifie la langue utilisée pour le texte et la messagerie reCAPTCHA de Google. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3 Invisible](./assets/recaptcha-storefront-v3-invisible.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--|--|--|
| [!UICONTROL Google API Website Key] | Site Web | Clé de site web créée lors de l’enregistrement de votre compte Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Site Web | Clé secrète associée à votre compte Google reCAPTCHA. |
| [!UICONTROL Minimum Score Threshold] | Global | Score minimum qui identifie une interaction utilisateur comme risque potentiel, où 1.0 est une interaction utilisateur type et 0.0 est probablement un bot. Valeur par défaut : `0.5` |
| [!UICONTROL Invisible Badge Position] | Site Web | Position du badge reCAPTCHA invisible sur chaque page. Options : `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Site Web | Détermine le style de la zone Google reCAPTCHA. Options : `Light Theme` (par défaut) / `Dark Theme` |
| [!UICONTROL Language Code] | Affichage en magasin | A [code à deux caractères](https://developers.google.com/recaptcha/docs/language) qui spécifie la langue utilisée pour le texte et la messagerie reCAPTCHA de Google. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Failure Messages]

![Messages d’échec](./assets/recaptcha-storefront-failure-messages.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | Affichage en magasin | Message affiché dans le storefront si la vérification échoue. Texte par défaut : `reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | Affichage en magasin | Message affiché dans le storefront si reCAPTCHA ne parvient pas à renvoyer un résultat de vérification. Texte par défaut : `Something went wrong with reCAPTCHA. Please contact the store owner.` |

{style="table-layout:auto"}

## [!UICONTROL Storefront]

![Storefront](./assets/recaptcha-storefront.png)<!-- zoom -->

>[!NOTE]
>
>Le type reCAPTCHA que vous choisissez doit correspondre au type associé à la clé API de votre compte reCAPTCHA Google.

>[!WARNING]
>
>Lors de l’utilisation de reCAPTCHA version 3, un véritable utilisateur avec un score faible ne peut pas continuer. Pour la version 2, un véritable utilisateur avec un score faible reçoit un défi. Examinez attentivement si les utilisateurs authentiques ayant un score faible doivent avoir la possibilité de résoudre un problème (version 2) ou être bloqués (version 3).

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--|--|--|
| [!UICONTROL Enable for Customer Login] | Site Web | Indique le type de reCAPTCHA utilisé lorsque les clients [connexion](../../customers/customer-sign-in.md) à leurs comptes. Options :<br/>**`No`**- (par défaut) Ne valide pas la demande de connexion.<br />**`reCAPTCHA v2 ("I am not a robot")`** - L’utilisateur doit sélectionner la variable _Je ne suis pas un robot_ .<br />**`Invisible reCAPTCHA v2`**: valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions basées sur un score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Forgot Password] | Site Web | Indique le type de reCAPTCHA utilisé lorsque les clients demandent une [réinitialisation du mot de passe](../../customers/password-reset.md). Options :<br/>**`No`**- (par défaut) Ne valide pas la demande de réinitialisation du mot de passe.<br />**`reCAPTCHA v2 ("I am not a robot")`** - L’utilisateur doit sélectionner la variable _Je ne suis pas un robot_ .<br />**`Invisible reCAPTCHA v2`**: valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions basées sur un score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Create New Customer Account] | Site Web | Indique le type de reCAPTCHA utilisé lorsque le client s’inscrit à une [nouveau compte](../../customers/account-create.md). Options :<br/>**`No`**- (par défaut) Ne valide pas la demande de compte.<br />**`reCAPTCHA v2 ("I am not a robot")`** - L’utilisateur doit sélectionner la variable _Je ne suis pas un robot_ .<br />**`Invisible reCAPTCHA v2`**: valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions basées sur un score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Edit Customer Account] | Site Web | Indique le type de reCAPTCHA utilisé lorsque le client modifie ses [informations du compte](../../customers/account-dashboard-account-information.md). Options :<br/>**`No`**- (par défaut) Ne valide pas la demande de compte.<br />**`reCAPTCHA v2 ("I am not a robot")`** - L’utilisateur doit sélectionner la variable _Je ne suis pas un robot_ .<br />**`Invisible reCAPTCHA v2`**: valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions basées sur un score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Create New Company Account] | Site Web | ![B2B pour Adobe Commerce](../../assets/b2b.svg) (Disponible avec B2B pour Adobe Commerce uniquement) Indique le type de reCAPTCHA utilisé lors d’une nouvelle [compte de société](../../b2b/account-company-create.md) est créée. Options :<br/>**`No`**- (par défaut) Ne valide pas la demande de compte.<br />**`reCAPTCHA v2 ("I am not a robot")`** - L’utilisateur doit sélectionner la variable _Je ne suis pas un robot_ .<br />**`Invisible reCAPTCHA v2`**: valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions basées sur un score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Contact Us] | Site Web | Indique le type de reCAPTCHA utilisé pour envoyer un message à partir de la variable [Nous contacter](../../getting-started/store-details.md#contact-us-form) de votre boutique. Options :<br/>**`No`**- (par défaut) Ne valide pas la demande de message.<br />**`reCAPTCHA v2 ("I am not a robot")`** - L’utilisateur doit sélectionner la variable _Je ne suis pas un robot_ .<br />**`Invisible reCAPTCHA v2`**: valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions basées sur un score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Product Review] | Site Web | Indique le type de reCAPTCHA utilisé lorsque les clients envoient une [examen du produit](../../merchandising-promotions/product-reviews.md). Options :<br/>**`No`**- (par défaut) Ne valide pas la demande de révision de produit.<br />**`reCAPTCHA v2 ("I am not a robot")`** - L’utilisateur doit sélectionner la variable _Je ne suis pas un robot_ .<br />**`Invisible reCAPTCHA v2`**: valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions basées sur un score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Newsletter Subscription] | Site Web | Indique le type de reCAPTCHA invisible utilisé lorsque les clients s’inscrivent à une [abonnement à la newsletter](../../merchandising-promotions/newsletter-subscribers.md). Options :<br/>**`No`**- (par défaut) Ne valide pas la demande d’abonnement à la newsletter.<br />**`reCAPTCHA v2 ("I am not a robot")`** - L’utilisateur doit sélectionner la variable _Je ne suis pas un robot_ .<br />**`Invisible reCAPTCHA v2`**: valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions basées sur un score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Gift Card] | Site Web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Indique le type de reCAPTCHA utilisé lorsque les clients saisissent une variable [carte cadeau](../../catalog/product-gift-card-create.md) code. Options :<br/>**`No`**- (par défaut) Ne valide pas l’envoi du code de carte-cadeau.<br />**`reCAPTCHA v2 ("I am not a robot")`** - L’utilisateur doit sélectionner la variable _Je ne suis pas un robot_ .<br />**`Invisible reCAPTCHA v2`**: valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions basées sur un score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Invitation Create Account] | Site Web | Indique le type de reCAPTCHA utilisé lorsque les clients envoient une création de compte. [invitation](../../merchandising-promotions/invitations.md) code. Options :<br/>**`No`**- (par défaut) Ne valide pas l’envoi du courrier électronique d’invitation.<br />**`reCAPTCHA v2 ("I am not a robot")`** - L’utilisateur doit sélectionner la variable _Je ne suis pas un robot_ .<br />**`Invisible reCAPTCHA v2`**: valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions basées sur un score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Send to Friend] | Site Web | Indique le type de reCAPTCHA utilisé lorsque les clients [partager un produit ;](../../stores-purchase/email-a-friend.md) avec un ami. Options :<br/>**`No`**- (par défaut) Ne valide pas l’envoi du courrier électronique.<br />**`reCAPTCHA v2 ("I am not a robot")`** - L’utilisateur doit sélectionner la variable _Je ne suis pas un robot_ .<br />**`Invisible reCAPTCHA v2`**: valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions basées sur un score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Wishlist Sharing] | Site Web | Indique le type de reCAPTCHA utilisé lorsque les clients [partager une liste de souhaits ;](../../stores-purchase/wishlist-storefront.md#share-the-wish-list). Options :<br/>**`No`**- (par défaut) Ne valide pas l’envoi du message et de l’email.<br />**`reCAPTCHA v2 ("I am not a robot")`** - L’utilisateur doit sélectionner la variable _Je ne suis pas un robot_ .<br />**`Invisible reCAPTCHA v2`**: valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions basées sur un score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Coupon Codes] | Site Web | Indique le type de reCAPTCHA utilisé lorsque les clients saisissent une [code de coupon](../../merchandising-promotions/price-rules-cart-coupon.md). Options :<br/>**`No`**- (par défaut) Ne valide pas l’envoi du code de coupon.<br />**`reCAPTCHA v2 ("I am not a robot")`** - L’utilisateur doit sélectionner la variable _Je ne suis pas un robot_ .<br />**`Invisible reCAPTCHA v2`**: valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions basées sur un score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for PayPal Payflow Pro payment form] | Site Web | Indique le type de reCAPTCHA utilisé lorsque les clients paient un achat avec [PayPal Payflow Pro](../../stores-purchase/paypal-payflow-pro.md). Options :<br/>**`No`**- (par défaut) Ne valide pas la demande de réinitialisation du mot de passe.<br />**`reCAPTCHA v2 ("I am not a robot")`** - L’utilisateur doit sélectionner la variable _Je ne suis pas un robot_ .<br />**`Invisible reCAPTCHA v2`**: valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions basées sur un score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |

{style="table-layout:auto"}
