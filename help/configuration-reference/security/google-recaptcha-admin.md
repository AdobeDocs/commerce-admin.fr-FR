---
title: '[!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Admin Panel]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Admin Panel] de l’administrateur Commerce.
exl-id: e4e6771a-487a-43ee-8b98-6acee4599aaf
feature: Configuration, Security
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Admin Panel]

>[!IMPORTANT]
>
>Avant de pouvoir configurer Google reCAPTCHA, vous devez vous assurer que `PHP.ini` comprend le paramètre suivant : `allow_url_fopen = 1`. Cela peut nécessiter l’aide des développeurs. Voir [Paramètres PHP requis](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) dans le _Guide d’installation_.

{{config}}

Pour plus d’informations sur la modification de ces paramètres, voir [Google reCAPTCHA](../../systems/security-google-recaptcha.md) dans le _Guide des systèmes d’administration_.

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2 (&quot;Je ne suis pas un robot&quot;)](./assets/recaptcha-admin-v2-not-robot.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--|--|--|
| [!UICONTROL Google API Website Key] | Global | Clé de site web créée lors de l’enregistrement de votre compte Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Global | Clé secrète associée à votre compte Google reCAPTCHA. |
| [!UICONTROL Size] | Global | Taille de la zone reCAPTCHA Google qui s’affiche lors de la connexion. Options : `Normal` (par défaut) / `Compact` |
| [!UICONTROL Theme] | Global | Détermine le style de la zone Google reCAPTCHA. Options : `Light Theme` (par défaut) / `Dark Theme` |
| [!UICONTROL Language Code] | Global | A [code à deux caractères](https://developers.google.com/recaptcha/docs/language) qui spécifie la langue utilisée pour le texte et la messagerie reCAPTCHA de Google. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 Invisible](./assets/recaptcha-admin-v2-invisible.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--|--|--|
| [!UICONTROL Google API Website Key] | Global | Clé de site web créée lors de l’enregistrement de votre compte Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Global | Clé secrète associée à votre compte Google reCAPTCHA. |
| [!UICONTROL Invisible Badge Position] | Global | Position du badge reCAPTCHA invisible sur chaque page. Options : `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Global | Détermine le style de la zone Google reCAPTCHA. Options : `Light Theme` (par défaut) / `Dark Theme` |
| [!UICONTROL Language Code] | Global | A [code à deux caractères](https://developers.google.com/recaptcha/docs/language) qui spécifie la langue utilisée pour le texte et la messagerie reCAPTCHA de Google. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3 Invisible](./assets/recaptcha-admin-v3-invisible.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--|--|--|
| [!UICONTROL Google API Website Key] | Global | Clé de site web créée lors de l’enregistrement de votre compte Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Global | Clé secrète associée à votre compte Google reCAPTCHA. |
| [!UICONTROL Minimum Score Threshold] | Global | Score minimum qui identifie une interaction utilisateur comme risque potentiel, où 1.0 est une interaction utilisateur type et 0.0 est probablement un bot. Valeur par défaut : `0.5` |
| [!UICONTROL Invisible Badge Position] | Global | Position du badge reCAPTCHA invisible sur chaque page. Options : `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Global | Détermine le style de la zone Google reCAPTCHA. Options : `Light Theme` (par défaut) / `Dark Theme` |
| [!UICONTROL Language Code] | Global | A [code à deux caractères](https://developers.google.com/recaptcha/docs/language) qui spécifie la langue utilisée pour le texte et la messagerie reCAPTCHA de Google. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL reCAPTCHA Failure Messages]

![Messages d’échec](./assets/recaptcha-admin-failure-messages.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | Global | Message affiché dans l’Admin en cas d’échec de la vérification. Texte par défaut : `reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | Global | Message affiché dans l’Admin si reCAPTCHA ne parvient pas à renvoyer un résultat de vérification. Texte par défaut : `Something went wrong with reCAPTCHA. Please contact the store owner.` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Admin Panel]

![Panneau d’administration](./assets/recaptcha-admin-panel.png)<!-- zoom -->

>[!NOTE]
>
>Le type reCAPTCHA que vous choisissez doit correspondre au type associé à la clé API de votre compte reCAPTCHA Google.

>[!WARNING]
>
>Lors de l’utilisation de reCAPTCHA version 3, un véritable utilisateur avec un score faible ne peut pas continuer. Pour la version 2, un véritable utilisateur avec un score faible reçoit un défi. Examinez attentivement si les utilisateurs authentiques ayant un score faible doivent avoir la possibilité de résoudre un problème (version 2) ou être bloqués (version 3).

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--|--|--|
| [!UICONTROL Enable for Login] | Global | Détermine le type de reCAPTCHA activé pour la variable [Connexion administrateur](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html). Options :<br/>**`No`**- (par défaut) Ne valide pas la connexion administrateur.<br />**`reCAPTCHA v2 ("I am not a robot")`** - L’utilisateur doit sélectionner la variable _Je ne suis pas un robot_ .<br />**`Invisible reCAPTCHA v2`**: valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions basées sur un score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Forgot Password] | Global | Détermine le type de reCAPTCHA activé pour demander une [Réinitialisation du mot de passe administrateur](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html#reset-your-password). Options :<br/>**`No`**- (par défaut) Ne valide pas la demande de réinitialisation du mot de passe.<br />**`reCAPTCHA v2 ("I am not a robot")`** - L’utilisateur doit sélectionner la variable _Je ne suis pas un robot_ .<br />**`Invisible reCAPTCHA v2`**: valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions basées sur un score.<br/>**`Invisible reCaptcha v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |

{:style=&quot;table-layout:auto&quot;}
