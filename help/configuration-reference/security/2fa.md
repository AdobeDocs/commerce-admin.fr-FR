---
title: '[!UICONTROL Security] &gt; [!UICONTROL 2FA]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Security] &gt; [!UICONTROL 2FA] de l’administrateur Commerce.
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
source-git-commit: 65c15bb84b28088a6e8f06f3592600779ba033f5
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>Les magasins qui ont activé l’authentification Adobe Identity Management Services (IMS) ont désactivé l’authentification à deux facteurs native Adobe Commerce et Magento Open Source (2FA). Les utilisateurs administrateurs connectés à leur instance Adobe Commerce avec leurs informations d’identification d’Adobe n’ont pas besoin de se réauthentifier pour de nombreuses tâches d’administration. L’authentification est gérée par Adobe IMS lorsque l’utilisateur administrateur se connecte à sa session en cours. Voir [Présentation de l’intégration d’Adobe Commerce à Adobe IMS](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

{{config}}

Pour plus d’informations sur la modification de ces paramètres, voir [Authentification à deux facteurs (2FA)](../../systems/security-two-factor-authentication.md) dans le _Guide des systèmes d’administration_.

## [!UICONTROL General]

![Général](./assets/2fa-general.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Providers to use] | Global | Indique les méthodes d’authentification à deux facteurs dont vous avez besoin. Si vous sélectionnez plusieurs fournisseurs, chaque utilisateur doit configurer chaque méthode 2FA la prochaine fois qu’il se connecte. |
| [!UICONTROL Configuration Email URL for Web API] | Global | Pour les implémentations personnalisées, l’URL d’un autre lien de configuration de courrier électronique envoyé aux utilisateurs _Admin_ lors de leur première connexion. Dans le modèle de courrier électronique, utilisez l’espace réservé `:tfat` pour indiquer où le jeton est injecté. |
| [!UICONTROL Retry attempt limit for Two-Factor Authentication] | Global | Détermine le nombre de fois qu’un administrateur peut entrer dans un [!DNL one-time password (OTP)] avant que son compte ne soit temporairement désactivé. Valeur par défaut : `10` |
| [!UICONTROL Two-Factor Authentication lockout time (seconds)] | Global | Détermine la durée (en secondes) pendant laquelle un administrateur peut attendre pour entrer dans un [!DNL one-time password (OTP)] avant que son compte ne soit temporairement désactivé. Valeur par défaut : `300` |

{style="table-layout:auto"}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL OTP Window] | Global | Détermine la durée (en secondes) pendant laquelle le système accepte le [!DNL one-time-password (OTP)] d’un administrateur après expiration. Ne peut pas être supérieur à la durée de vie d’un seul HTTP (généralement 30 secondes). Valeur par défaut : `29` |

{style="table-layout:auto"}

## [!UICONTROL Duo Security]

![Duo Security](./assets/2fa-duo-security.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Integration Key] | Global | Clé d’intégration de votre compte [!DNL Duo Security]. |
| [!UICONTROL Secret Key] | Global | La clé secrète de votre compte [!DNL Duo Security]. |
| [!UICONTROL API Hostname] | Global | Nom d’hôte de l’API de votre compte [!DNL Duo Security]. |

{style="table-layout:auto"}

## [!UICONTROL Authy]

![Auteur](./assets/2fa-authy.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL API Key] | Global | Clé API de votre compte [!DNL Authy]. |
| [!UICONTROL OneTouch Message] | Global | Message qui apparaît dans l’authentificateur [!DNL Authy] lors de la connexion. Valeur par défaut : `Login request to your Magento Admin` |

{style="table-layout:auto"}

## [!UICONTROL U2F Key]

![Clé U2F](./assets/2fa-u2f-key.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL WebApi Challenge Domain] | Global | Domaine utilisé pour émettre et traiter des problèmes [!DNL WebAuthn] pour les implémentations WebAPI personnalisées. |

{style="table-layout:auto"}
