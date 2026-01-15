---
title: '[!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Admin Panel]'
description: Vérifiez les paramètres de configuration sur la page de [!UICONTROL Security] d’[!UICONTROL Google reCAPTCHA Admin Panel] &gt; de l’administrateur Commerce.
exl-id: e4e6771a-487a-43ee-8b98-6acee4599aaf
feature: Configuration, Security
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 6fe5ffb6f529f95e32bb12a55ae16100f4d1bbbb
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Admin Panel]

>[!IMPORTANT]
>
>Avant de pouvoir configurer Google reCAPTCHA, vous devez vous assurer que votre fichier `PHP.ini` inclut le paramètre suivant : `allow_url_fopen = 1`. Cela peut nécessiter l’aide d’un développeur. Voir [Paramètres PHP requis](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html?lang=fr) dans le _Guide d&#39;installation_.

{{config}}

Pour plus d&#39;informations sur la modification de ces paramètres, consultez [Google reCAPTCHA](../../systems/security-google-recaptcha.md) dans le _Guide des systèmes d&#39;administration_.

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2 (« Je ne suis pas un robot »)](./assets/recaptcha-admin-v2-not-robot.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--|--|--|
| [!UICONTROL Google API Website Key] | Global | Clé de site web créée lors de l’enregistrement de votre compte reCAPTCHA Google. |
| [!UICONTROL Google API Secret Key] | Global | Clé secrète associée à votre compte Google reCAPTCHA. |
| [!UICONTROL Size] | Global | Taille de la zone reCAPTCHA de Google qui s’affiche lors de la connexion. Options : `Normal` (par défaut) / `Compact` |
| [!UICONTROL Theme] | Global | Détermine le style de la zone reCAPTCHA Google. Options : `Light Theme` (par défaut) / `Dark Theme` |
| [!UICONTROL Language Code] | Global | Code [&#x200B; à deux caractères](https://developers.google.com/recaptcha/docs/language) qui spécifie la langue utilisée pour le texte et la messagerie reCAPTCHA de Google. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 invisible](./assets/recaptcha-admin-v2-invisible.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--|--|--|
| [!UICONTROL Google API Website Key] | Global | Clé de site web créée lors de l’enregistrement de votre compte reCAPTCHA Google. |
| [!UICONTROL Google API Secret Key] | Global | Clé secrète associée à votre compte Google reCAPTCHA. |
| [!UICONTROL Invisible Badge Position] | Global | Position du badge reCAPTCHA invisible sur chaque page. Options : `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Global | Détermine le style de la zone reCAPTCHA Google. Options : `Light Theme` (par défaut) / `Dark Theme` |
| [!UICONTROL Language Code] | Global | Code [&#x200B; à deux caractères](https://developers.google.com/recaptcha/docs/language) qui spécifie la langue utilisée pour le texte et la messagerie reCAPTCHA de Google. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3 invisible](./assets/recaptcha-admin-v3-invisible.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--|--|--|
| [!UICONTROL Google API Website Key] | Global | Clé de site web créée lors de l’enregistrement de votre compte reCAPTCHA Google. |
| [!UICONTROL Google API Secret Key] | Global | Clé secrète associée à votre compte Google reCAPTCHA. |
| [!UICONTROL Minimum Score Threshold] | Global | Score minimal qui identifie une interaction utilisateur comme un risque potentiel, où 1,0 est une interaction utilisateur type et 0,0 est probablement un robot. Valeur par défaut : `0.5` |
| [!UICONTROL Invisible Badge Position] | Global | Position du badge reCAPTCHA invisible sur chaque page. Options : `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Global | Détermine le style de la zone reCAPTCHA Google. Options : `Light Theme` (par défaut) / `Dark Theme` |
| [!UICONTROL Language Code] | Global | Code [&#x200B; à deux caractères](https://developers.google.com/recaptcha/docs/language) qui spécifie la langue utilisée pour le texte et la messagerie reCAPTCHA de Google. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Failure Messages]

![Messages d’échec](./assets/recaptcha-admin-failure-messages.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | Global | Message affiché dans l’Administration en cas d’échec de la vérification. Texte par défaut : `reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | Global | Le message qui s’affiche dans Admin si reCAPTCHA ne parvient pas à renvoyer un résultat de vérification. Texte par défaut : `Something went wrong with reCAPTCHA. Please contact the store owner.` |

{style="table-layout:auto"}

## [!UICONTROL Admin Panel]

![Panneau d’administration](./assets/recaptcha-admin-panel.png)<!-- zoom -->

>[!NOTE]
>
>Le type reCAPTCHA que vous choisissez doit correspondre au type associé à la clé API de votre compte reCAPTCHA Google.

>[!WARNING]
>
>Lors de l’utilisation de reCAPTCHA version 3, un utilisateur authentique avec un score faible ne peut pas continuer. Pour la version 2, un utilisateur authentique avec un score faible reçoit un défi. Réfléchissez soigneusement si les utilisateurs authentiques avec un score faible doivent avoir la possibilité de résoudre un défi (version 2) ou être bloqués (version 3).

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--|--|--|
| [!UICONTROL Enable for Login] | Global | Détermine le type de reCAPTCHA activé pour le [login administrateur](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html?lang=fr). Options : <br/>**`No`**- (par défaut) ne valide pas le nom d’utilisateur de l’administrateur.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Nécessite que l&#39;utilisateur coche la case _Je ne suis pas un robot_.<br />**`Invisible reCAPTCHA v2`**- Valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions en fonction du score.<br/>**`Invisible reCAPTCHA v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |
| [!UICONTROL Enable for Forgot Password] | Global | Détermine le type de reCAPTCHA activé pour demander une [réinitialisation du mot de passe administrateur](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html?lang=fr#reset-your-password). Options : <br/>**`No`**- (par défaut) ne valide pas la demande de réinitialisation du mot de passe.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Nécessite que l&#39;utilisateur coche la case _Je ne suis pas un robot_.<br />**`Invisible reCAPTCHA v2`**- Valide le comportement de l’utilisateur en arrière-plan sans nécessiter d’interactions en fonction du score.<br/>**`Invisible reCaptcha v3`** - (Recommandé) Valide le comportement de l’utilisateur en arrière-plan en fonction du score d’interaction. |

{style="table-layout:auto"}
