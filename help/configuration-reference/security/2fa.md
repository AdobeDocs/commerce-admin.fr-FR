---
title: '[!UICONTROL Security] &gt; [!UICONTROL 2FA]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Security] &gt; [!UICONTROL 2FA] de l’administrateur Commerce.
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '280'
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
| [!UICONTROL Configuration Email URL for Web API] | Global | Pour les implémentations personnalisées, URL d’un autre lien de configuration de courrier électronique envoyé à _Administration_ utilisateurs lors de leur première connexion. Dans le modèle de courrier électronique, utilisez l’espace réservé. `:tfat` pour indiquer l’endroit où le jeton est injecté. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL OTP Window] | Global | Durée de vie, en secondes, de chaque mot de passe unique (OTP) généré par l’authentificateur Google. Valeur par défaut : `30` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Duo Security]

![Duo Security](./assets/2fa-duo-security.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Integration Key] | Global | La clé d’intégration de votre [!DNL Duo Security] compte . |
| [!UICONTROL Secret Key] | Global | La clé secrète de votre [!DNL Duo Security] compte . |
| [!UICONTROL API Hostname] | Global | Le nom d’hôte de l’API de [!DNL Duo Security] compte . |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Authy]

![Création](./assets/2fa-authy.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL API Key] | Global | La clé API de votre [!DNL Authy] compte . |
| [!UICONTROL OneTouch Message] | Global | Le message qui apparaît dans la [!DNL Authy] authentificateur lors de la connexion. Valeur par défaut : `Login request to your Magento Admin` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL U2F Key]

![Clé U2F](./assets/2fa-u2f-key.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL WebApi Challenge Domain] | Global | Domaine utilisé pour émettre et traiter [!DNL WebAuthn] défis pour les implémentations WebAPI personnalisées. |

{:style=&quot;table-layout:auto&quot;}
