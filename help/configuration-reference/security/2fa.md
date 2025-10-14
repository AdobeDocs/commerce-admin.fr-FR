---
title: '[!UICONTROL Security] &gt; [!UICONTROL 2FA]'
description: Vérifiez les paramètres de configuration sur la page de [!UICONTROL 2FA] d’[!UICONTROL Security] &gt; de l’administrateur Commerce.
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
source-git-commit: 22bfff98a9189f3020de21b31705351510dcf1be
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>Pour les magasins qui ont activé l’authentification Adobe Identity Management Services (IMS), l’authentification native Adobe Commerce et Magento Open Source à deux facteurs (2FA) est désactivée. Les utilisateurs administrateurs connectés à leur instance Adobe Commerce avec leurs informations d’identification Adobe n’ont pas besoin de s’authentifier à nouveau pour de nombreuses tâches d’administration. L’authentification est gérée par Adobe IMS lorsque l’utilisateur administrateur se connecte à sa session en cours. Voir [&#x200B; Intégration d’Adobe Commerce à Adobe IMS](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html?lang=fr).

{{config}}

Pour plus d’informations sur la modification de ces paramètres, voir [Authentification à deux facteurs (2FA)](../../systems/security-two-factor-authentication.md) dans le _Guide d’administration des systèmes_.

## [!UICONTROL General]

![Général](./assets/2fa-general.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Providers to use] | Global | Indique les méthodes d’authentification à deux facteurs dont vous avez besoin. Si vous sélectionnez plusieurs fournisseurs, chaque utilisateur doit configurer chaque méthode 2FA la prochaine fois qu’il se connecte. |
| [!UICONTROL Configuration Email URL for Web API] | Global | Pour les implémentations personnalisées, URL d’un lien de configuration d’e-mail secondaire envoyé aux utilisateurs _Admin_ lors de la première connexion. Dans le modèle de courrier électronique, utilisez l’espace réservé `:tfat` pour indiquer où le jeton est injecté. |
| [!UICONTROL Retry attempt limit for Two-Factor Authentication] | Global | Détermine combien de fois un administrateur peut entrer un avant que [!DNL one-time password (OTP)] son compte ne soit temporairement désactivé. Faire défaut: `10` |
| [!UICONTROL Two-Factor Authentication lockout time (seconds)] | Global | Détermine combien de temps (en secondes) un administrateur peut attendre pour entrer un avant que [!DNL one-time password (OTP)] son compte ne soit temporairement désactivé. Faire défaut: `300` |

{style="table-layout:auto"}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL OTP Window] | Global | Détermine la durée (en secondes) pendant laquelle le système accepte les [!DNL one-time-password (OTP)] d&#39;un administrateur après leur expiration. Ne peut pas être supérieur à la durée de vie d’un seul mot de passe à usage unique (généralement 30 secondes). Valeur par défaut : `29` |

{style="table-layout:auto"}

## [!UICONTROL Duo Security]

![Duo Security](./assets/2fa-duo-security.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Client Id] | Global | L’ID client de votre [!DNL Duo Security] compte. |
| [!UICONTROL Client Secret] | Global | Secret client de votre compte [!DNL Duo Security]. |
| [!UICONTROL Integration Key] | Global | La clé d’intégration de votre [!DNL Duo Security] compte API. |
| [!UICONTROL Secret Key] | Global | La clé secrète de votre [!DNL Duo Security] compte API. |
| [!UICONTROL API Hostname] | Global | Nom d’hôte API de votre [!DNL Duo Security] compte. |

{style="table-layout:auto"}

## [!UICONTROL Authy]

![Authy](./assets/2fa-authy.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL API Key] | Global | La clé API de votre [!DNL Authy] compte. |
| [!UICONTROL OneTouch Message] | Global | Message qui apparaît dans l’authentificateur lors de la [!DNL Authy] connexion. Faire défaut: `Login request to your Magento Admin` |

{style="table-layout:auto"}

## [!UICONTROL U2F Key]

![Clé U2F](./assets/2fa-u2f-key.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL WebApi Challenge Domain] | Global | Domaine utilisé pour émettre et traiter [!DNL WebAuthn] les défis liés aux implémentations WebAPI personnalisées. |

{style="table-layout:auto"}
