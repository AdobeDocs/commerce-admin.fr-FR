---
title: Authentification à deux facteurs (2FA)
description: Découvrez la prise en charge de l’authentification à deux facteurs pour garantir la sécurité de votre système et de vos données.
exl-id: d9eb3dd6-4a7b-411a-ac08-0441803cd59a
role: Admin
feature: Configuration, Security, User Account
source-git-commit: c391a3eef8be0dd45cc8a499b63bcb0fc32640aa
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 0%

---

# Authentification à deux facteurs (2FA)

Commerce _Administration_ pour votre installation Adobe Commerce ou Magento Open Source, permet d’accéder à votre boutique, à vos commandes et à vos données client. Pour empêcher tout accès non autorisé à vos données, tous les utilisateurs qui tentent de se connecter au _Administration_ doit terminer un processus d’authentification pour vérifier leur identité.

>[!NOTE]
>
>Cette implémentation de l’authentification à deux facteurs (2FA) s’applique à la variable _Administration_ uniquement et n’est pas disponible pour les comptes clients. L’authentification à deux facteurs qui protège votre compte Commerce comporte une configuration distincte. Pour en savoir plus, accédez à [Sécurisation de votre compte Commerce](../getting-started/commerce-account-secure.md).

L’authentification à deux facteurs est largement utilisée et il est courant de générer des codes d’accès pour différents sites web sur la même application. Cette authentification supplémentaire garantit que seul vous pouvez vous connecter à votre compte utilisateur. Si vous perdez votre mot de passe ou si un robot l’anticipe, l’authentification à deux facteurs ajoute une couche de protection. Par exemple, vous pouvez utiliser l’authentificateur Google pour générer des codes destinés à l’administrateur de votre boutique, de votre compte Commerce et de votre compte Google.

![Iphone de configuration de sécurité - 2FA](./assets/google-authenticator-iphone.png){width="300"}

Adobe Commerce prend en charge les méthodes 2FA de plusieurs fournisseurs. Certains nécessitent l’installation d’une application qui génère un mot de passe unique (OTP) que les utilisateurs saisissent lors de leur connexion pour vérifier leur identité. Les appareils de second facteur universel (U2F) ressemblent à un robot clé et génèrent une clé unique pour vérifier l’identité. D’autres périphériques vérifient l’identité lorsqu’ils sont insérés dans un port USB. En tant qu’administrateur de magasin, vous pouvez avoir besoin d’une ou de plusieurs des méthodes 2FA disponibles pour vérifier l’identité de l’utilisateur. Votre configuration 2FA s’applique à tous les sites web et magasins associés à l’installation Adobe Commerce.

La première fois qu’un utilisateur se connecte à la variable _Administration_, ils doivent configurer chaque [2FA](../configuration-reference/security/2fa.md) , selon vos besoins, et vérifiez leur identité à l’aide de l’application ou de l’appareil associé. Après cette configuration initiale, l’utilisateur doit s’authentifier à l’aide de l’une des méthodes configurées à chaque connexion. Les informations 2FA de chaque utilisateur sont enregistrées dans leur _Administration_ et peut être [reset](security-two-factor-authentication-manage.md) si nécessaire. Pour en savoir plus sur le processus de connexion, accédez à [_Administration_ Se connecter](../getting-started/admin-signin.md).

>[!NOTE]
>
>Les magasins qui ont activé l’authentification Adobe Identity Management Services (IMS) ont désactivé Adobe Commerce et Magento Open Source 2FA natifs. Les utilisateurs administrateurs connectés à leur instance Commerce avec leurs informations d’identification d’Adobe n’ont pas besoin de se réauthentifier pour de nombreuses tâches d’administration. L’authentification est gérée par Adobe IMS lorsque l’utilisateur administrateur se connecte à sa session en cours. Voir [Présentation de l’intégration d’Adobe Identity Management Service (IMS)](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

Vous pouvez le voir [démonstration vidéo](https://video.tv.adobe.com/v/339104?quality=12&learn=on) pour un aperçu de l’authentification à deux facteurs dans l’Admin.

## Configuration de vos fournisseurs 2FA requis

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Security]** et choisissez **[!UICONTROL 2FA]**.

1. Dans le _[!UICONTROL General]_, sélectionnez les fournisseurs à utiliser.

   | Fournisseur | Fonction |
   |--- |--- |
   | [!UICONTROL Google Authenticator] | Génère un mot de passe unique dans l’application pour l’authentification des utilisateurs. |
   | [!UICONTROL Duo Security] | Fournit des SMS et des notifications push. |
   | [!UICONTROL Authy] | Génère un code à six chiffres dépendant du temps et fournit une protection ou un jeton SMS ou d’appel Voix 2FA. |
   | [!UICONTROL U2F Devices (Yubikey and others)] | Utilise un appareil physique à authentifier, tel que [[!DNL YubiKey]](https://www.yubico.com/). |

   Pour sélectionner plusieurs méthodes, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque élément.

1. Définissez les paramètres de chaque méthode 2FA requise.

   ![Configuration de la sécurité - 2FA](../configuration-reference/security/assets/2fa-general.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

   La première fois que les utilisateurs se connectent au _Administration_, ils doivent configurer chaque méthode 2FA requise. Après cette configuration initiale, ils doivent s’authentifier à l’aide de l’une des méthodes configurées chaque fois qu’ils se connectent.

## Paramètres du fournisseur 2FA

Définissez les paramètres de chaque méthode 2FA dont vous avez besoin.

### Google

Pour modifier la durée de disponibilité du mot de passe unique (OTP) lors de la connexion, effacez la variable **[!UICONTROL Use system value]** . Saisissez ensuite le nombre de secondes pour le **[!UICONTROL OTP Window]** pour être valide.

>[!NOTE]
>
>Dans Adobe Commerce 2.4.7 et versions ultérieures, le paramètre de configuration de fenêtre OTP contrôle la durée (en secondes) pendant laquelle le système accepte le mot de passe unique (OTP) d’un administrateur après expiration. Cette valeur doit être inférieure à 30 secondes. Le paramètre système par défaut est `1`.<br><br> Dans la version 2.4.6, le paramètre de fenêtre OTP détermine le nombre de codes OTP passés et futurs qui restent valides. Une valeur de `1` indique que le code OTP actuel plus un code dans le passé et un code dans le futur restent valides à tout moment.

### [!DNL Duo Security]

Saisissez les informations d’identification suivantes à partir de votre compte Duo Security :

- Clé d’intégration
- Clé secrète
- Nom d’hôte API

![Configuration de la sécurité - Duo](../configuration-reference/security/assets/2fa-duo-security.png){width="600" zoomable="yes"}

### [!DNL Authy]

1. Saisissez la clé API de votre [!DNL Authy] compte .

1. Pour modifier le message par défaut qui s’affiche lors de l’authentification, effacez la **[!UICONTROL Use system value]** . Ensuite, saisissez la variable **[!UICONTROL OneTouch Message]** que vous voulez voir apparaître.

   ![Configuration de la sécurité - Authentification](../configuration-reference/security/assets/2fa-authy.png){width="600" zoomable="yes"}

### Périphériques U2F ([!DNL Yubikey] et autres)

Le domaine du magasin est utilisé par défaut lors du processus d’authentification. Pour utiliser un domaine personnalisé pour les défis d’authentification, effacez la variable **[!UICONTROL Use system value]** . Ensuite, saisissez la variable **[!UICONTROL WebAPi Challenge Domain]**.

![Configuration de la sécurité - Périphériques U2F](../configuration-reference/security/assets/2fa-u2f-key.png){width="600" zoomable="yes"}
