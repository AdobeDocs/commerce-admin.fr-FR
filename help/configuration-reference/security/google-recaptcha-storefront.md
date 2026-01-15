---
title: '[!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront]'
description: Vérifiez les paramètres de configuration sur la page de [!UICONTROL Security] d’[!UICONTROL Google reCAPTCHA Storefront] &gt; de l’administrateur Commerce.
exl-id: 6c03ee68-7421-4c74-bdc1-0855f088b7f9
feature: Configuration, Security
source-git-commit: 528e57df775b53b6137e1542ad0583c60d2f47ff
workflow-type: tm+mt
source-wordcount: '1481'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Storefront]

>[!IMPORTANT]
>
>Avant de pouvoir configurer Google reCAPTCHA, vous devez vous assurer que votre fichier `PHP.ini` inclut le paramètre suivant : `allow_url_fopen = 1`. Cela peut nécessiter l’aide d’un développeur. Voir [PHP Settings](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) dans le _Installation Guide_.

{{config}}

Pour plus d’informations sur l’utilisation de Google reCAPTCHA pour sécuriser votre magasin, consultez la section Google [reCAPTCHA](../../systems/security-google-recaptcha.md) dans le _Guide d’administration des systèmes_.

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2 (« Je ne suis pas un robot »)](./assets/recaptcha-storefront-v2-not-robot.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--|--|--|
| [!UICONTROL Google API Website Key] | Site internet | Clé de site web créée lors de l’enregistrement de votre compte reCAPTCHA Google. |
| [!UICONTROL Google API Secret Key] | Site internet | Clé secrète associée à votre compte Google reCAPTCHA. |
| [!UICONTROL Size] | Site internet | Taille de la zone reCAPTCHA de Google qui s’affiche lorsqu’un client se connecte à son compte. Options : `Normal` (par défaut) / `Compact` |
| [!UICONTROL Theme] | Site internet | Détermine le style de la zone reCAPTCHA Google. Options : `Light Theme` (par défaut) / `Dark Theme` |
| [!UICONTROL Language Code] | Affichage de la boutique | Le [code à deux caractères](https://developers.google.com/recaptcha/docs/language) qui spécifie la langue utilisée pour le texte et la messagerie reCAPTCHA de Google. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 invisible](./assets/recaptcha-storefront-v2-invisible.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--|--|--|
| [!UICONTROL Google API Website Key] | Site internet | Clé de site web créée lors de l’enregistrement de votre compte reCAPTCHA Google. |
| [!UICONTROL Google API Secret Key] | Site internet | Clé secrète associée à votre compte Google reCAPTCHA. |
| [!UICONTROL Invisible Badge Position] | Site internet | Position du badge reCAPTCHA invisible sur chaque page. Options : `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Global | Détermine le style de la zone reCAPTCHA Google. Options : `Light Theme` (par défaut) / `Dark Theme` |
| [!UICONTROL Language Code] | Affichage de la boutique | Code [ à deux caractères](https://developers.google.com/recaptcha/docs/language) qui spécifie la langue utilisée pour le texte et la messagerie reCAPTCHA de Google. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3 invisible](./assets/recaptcha-storefront-v3-invisible.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--|--|--|
| [!UICONTROL Google API Website Key] | Site internet | Clé de site web créée lors de l’enregistrement de votre compte reCAPTCHA Google. |
| [!UICONTROL Google API Secret Key] | Site internet | Clé secrète associée à votre compte Google reCAPTCHA. |
| [!UICONTROL Minimum Score Threshold] | Global | Score minimal qui identifie une interaction utilisateur comme un risque potentiel, où 1,0 est une interaction utilisateur type et 0,0 est probablement un robot. Valeur par défaut : `0.5` |
| [!UICONTROL Invisible Badge Position] | Site internet | Position du badge reCAPTCHA invisible sur chaque page. Options : `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Site internet | Détermine le style de la zone reCAPTCHA Google. Options : `Light Theme` (par défaut) / `Dark Theme` |
| [!UICONTROL Language Code] | Affichage de la boutique | Code [ à deux caractères](https://developers.google.com/recaptcha/docs/language) qui spécifie la langue utilisée pour le texte et la messagerie reCAPTCHA de Google. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Enterprise]

[!BADGE SaaS uniquement]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce as a Cloud Service (infrastructure SaaS gérée par Adobe)."}

[!BADGE  Sandbox ]{type=Caution tooltip="Les éléments répertoriés ne sont actuellement disponibles que dans les environnements Sandbox. Adobe commence par rendre les nouvelles versions disponibles dans les environnements Sandbox afin que vous disposiez du temps nécessaire pour tester les modifications à venir avant que la version ne soit disponible dans les environnements de production."}

![reCAPTCHA v3 Enterprise](./assets/recaptcha-storefront-v3-enterprise.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--|--|--|
| [!UICONTROL Site Key] | Site internet | Clé de site créée lors de l’enregistrement de votre compte Google reCAPTCHA Enterprise. |
| [!UICONTROL Google Cloud Project ID] | Site internet | L’ID de projet s’affiche dans la section **Informations sur le projet** du tableau de bord du projet. |
| [!UICONTROL Service Account JSON] | Site internet | Téléchargez la clé de compte de service à partir de la console Google Cloud et collez son contenu dans ce champ. |
| [!UICONTROL Minimum Score Threshold] | Site internet | Score minimal qui identifie une interaction utilisateur comme un risque potentiel, où 1,0 est une interaction utilisateur type et 0,0 est probablement un robot. Valeur par défaut : `0.5` |
| [!UICONTROL Badge Position] | Site internet | Position du badge reCAPTCHA invisible sur chaque page. Options : `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Site internet | Détermine le style de la zone reCAPTCHA Google. Options : `Light Theme` (par défaut) / `Dark Theme` |
| [!UICONTROL Language Code] | Affichage de la boutique | Code [ à deux caractères](https://developers.google.com/recaptcha/docs/language) qui spécifie la langue utilisée pour le texte et la messagerie reCAPTCHA de Google. Laissez le champ vide pour utiliser la langue par défaut du navigateur de l’utilisateur. |
| [!UICONTROL Validation Failure Message] | Affichage de la boutique | Message à afficher lorsque la validation échoue. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Failure Messages]

![Messages d’échec](./assets/recaptcha-storefront-failure-messages.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | Affichage de la boutique | Message affiché dans le storefront si la vérification échoue. Texte par défaut : `reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | Affichage de la boutique | Le message qui s’affiche dans le storefront si reCAPTCHA ne parvient pas à renvoyer un résultat de vérification. Texte par défaut : `Something went wrong with reCAPTCHA. Please contact the store owner.` |

{style="table-layout:auto"}

## [!UICONTROL Storefront]

![Storefront](./assets/recaptcha-storefront.png)<!-- zoom -->

>[!NOTE]
>
>Le type reCAPTCHA que vous choisissez doit correspondre au type associé à la clé API de votre compte reCAPTCHA Google.

>[!WARNING]
>
>Lors de l’utilisation de reCAPTCHA version 3, un utilisateur authentique avec un score faible ne peut pas continuer. Pour la version 2, un utilisateur authentique avec un score faible reçoit un défi. Réfléchissez soigneusement si les utilisateurs authentiques avec un score faible doivent avoir la possibilité de résoudre un défi (version 2) ou être bloqués (version 3).

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--|--|--|
| [!UICONTROL Enable for Customer Login] | Site internet | Spécifie le type de reCAPTCHA utilisé lorsque les clients [se connectent](../../customers/customer-sign-in.md) à leurs comptes. Options :<br/>**`No`**- (par défaut) Ne valide pas la demande de connexion.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Nécessite que l&#39;utilisateur coche la case _Je ne suis pas un robot_.<br />**`Invisible reCAPTCHA v2`**- Valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions en fonction du score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Forgot Password] | Site internet | Indique le type de reCAPTCHA utilisé lorsque les clients demandent une [réinitialisation de mot de passe](../../customers/password-reset.md). Options : <br/>**`No`**- (par défaut) ne valide pas la demande de réinitialisation du mot de passe.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Nécessite que l&#39;utilisateur coche la case _Je ne suis pas un robot_.<br />**`Invisible reCAPTCHA v2`**- Valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions en fonction du score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Create New Customer Account] | Site internet | Indique le type de reCAPTCHA utilisé lorsque le client s’inscrit pour un [nouveau compte](../../customers/account-create.md). Options :<br/>**`No`**- (par défaut) Ne valide pas la demande de compte.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Nécessite que l&#39;utilisateur coche la case _Je ne suis pas un robot_.<br />**`Invisible reCAPTCHA v2`**- Valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions en fonction du score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Edit Customer Account] | Site internet | Spécifie le type de reCAPTCHA utilisé lorsque le client modifie ses [informations de compte](../../customers/account-dashboard-account-information.md). Options :<br/>**`No`**- (par défaut) Ne valide pas la demande de compte.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Nécessite que l&#39;utilisateur coche la case _Je ne suis pas un robot_.<br />**`Invisible reCAPTCHA v2`**- Valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions en fonction du score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Create New Company Account] | Site internet | ![Adobe Commerce B2B](../../assets/b2b.svg) (disponible avec Adobe Commerce B2B uniquement) Spécifie le type de reCAPTCHA utilisé lors de la création d’un [compte société](../../b2b/account-company-create.md). Options :<br/>**`No`**- (par défaut) Ne valide pas la demande de compte.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Nécessite que l&#39;utilisateur coche la case _Je ne suis pas un robot_.<br />**`Invisible reCAPTCHA v2`**- Valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions en fonction du score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Contact Us] | Site internet | Indique le type de reCAPTCHA utilisé pour envoyer un message à partir de la page [Nous contacter](../../getting-started/store-details.md#contact-us-form) de votre boutique. Options : <br/>**`No`**- (par défaut) ne valide pas la demande de message.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Nécessite que l&#39;utilisateur coche la case _Je ne suis pas un robot_.<br />**`Invisible reCAPTCHA v2`**- Valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions en fonction du score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Product Review] | Site internet | Spécifie le type de reCAPTCHA utilisé lorsque les clients soumettent une [révision produit](../../merchandising-promotions/product-reviews.md). Options : <br/>**`No`**- (par défaut) ne valide pas la demande de révision du produit.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Nécessite que l&#39;utilisateur coche la case _Je ne suis pas un robot_.<br />**`Invisible reCAPTCHA v2`**- Valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions en fonction du score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Newsletter Subscription] | Site internet | Indique le type de reCAPTCHA invisible utilisé lorsque les clients s’abonnent à une [newsletter](../../merchandising-promotions/newsletter-subscribers.md). Options : <br/>**`No`**- (par défaut) ne valide pas la demande d’abonnement à la newsletter.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Nécessite que l&#39;utilisateur coche la case _Je ne suis pas un robot_.<br />**`Invisible reCAPTCHA v2`**- Valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions en fonction du score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Gift Card] | Site internet | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Spécifie le type de reCAPTCHA utilisé lorsque les clients saisissent un code [carte cadeau](../../catalog/product-gift-card-create.md). Options : <br/>**`No`**- (par défaut) Ne valide pas l’envoi du code de carte cadeau.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Nécessite que l&#39;utilisateur coche la case _Je ne suis pas un robot_.<br />**`Invisible reCAPTCHA v2`**- Valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions en fonction du score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Invitation Create Account] | Site internet | Spécifie le type de reCAPTCHA utilisé lorsque les clients envoient un code de création de compte [invitation](../../merchandising-promotions/invitations.md). Options : <br/>**`No`**- (par défaut) ne valide pas l’envoi de l’e-mail d’invitation.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Nécessite que l&#39;utilisateur coche la case _Je ne suis pas un robot_.<br />**`Invisible reCAPTCHA v2`**- Valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions en fonction du score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Send to Friend] | Site internet | Indique le type de reCAPTCHA utilisé lorsque les clients [partagent un produit](../../stores-purchase/email-a-friend.md) avec un ami. Options : <br/>**`No`**- (par défaut) ne valide pas l’envoi de l’e-mail.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Nécessite que l&#39;utilisateur coche la case _Je ne suis pas un robot_.<br />**`Invisible reCAPTCHA v2`**- Valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions en fonction du score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Wishlist Sharing] | Site internet | Indique le type de reCAPTCHA utilisé lorsque les clients [partagent une liste de souhaits](../../stores-purchase/wishlist-storefront.md#share-the-wish-list). Options : <br/>**`No`**- (par défaut) ne valide pas le message et l’envoi de l’e-mail.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Nécessite que l&#39;utilisateur coche la case _Je ne suis pas un robot_.<br />**`Invisible reCAPTCHA v2`**- Valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions en fonction du score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Coupon Codes] | Site internet | Spécifie le type de reCAPTCHA utilisé lorsque les clients saisissent un [code coupon](../../merchandising-promotions/price-rules-cart-coupon.md). Options : <br/>**`No`**- (par défaut) ne valide pas l’envoi du code de coupon.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Nécessite que l&#39;utilisateur coche la case _Je ne suis pas un robot_.<br />**`Invisible reCAPTCHA v2`**- Valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions en fonction du score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for PayPal Payflow Pro payment form] | Site internet | Spécifie le type de reCAPTCHA utilisé lorsque les clients paient pour un achat avec [PayPal Payflow Pro](../../stores-purchase/paypal-payflow-pro.md). Options : <br/>**`No`**- (par défaut) ne valide pas la demande de réinitialisation du mot de passe.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Nécessite que l&#39;utilisateur coche la case _Je ne suis pas un robot_.<br />**`Invisible reCAPTCHA v2`**- Valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions en fonction du score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |

{style="table-layout:auto"}
