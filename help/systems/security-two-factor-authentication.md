---
title: Authentification à deux facteurs (2FA)
description: Découvrez la prise en charge de l’authentification à deux facteurs pour garantir la sécurité de votre système et de vos données.
exl-id: d9eb3dd6-4a7b-411a-ac08-0441803cd59a
role: Admin
feature: Configuration, Security, User Account
source-git-commit: b31ed0e76df67a486012d8ec4997d9f19e17d371
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 0%

---

# Authentification à deux facteurs (2FA)

Le _Admin_ de Commerce pour votre installation Adobe Commerce ou Magento Open Source permet d’accéder à votre boutique, à vos commandes et à vos données client. Pour empêcher un accès non autorisé à vos données, tous les utilisateurs qui tentent de se connecter à l’ _Admin_ doivent terminer un processus d’authentification pour vérifier leur identité.

>[!NOTE]
>
>Cette mise en oeuvre de l’authentification à deux facteurs (2FA) s’applique uniquement à l’ _administrateur_ et n’est pas disponible pour les comptes clients. L’authentification à deux facteurs qui protège votre compte Commerce comporte une configuration distincte. Pour en savoir plus, accédez à [Sécuriser votre compte Commerce](../getting-started/commerce-account-secure.md).

L’authentification à deux facteurs est largement utilisée et il est courant de générer des codes d’accès pour différents sites web sur la même application. Cette authentification supplémentaire garantit que seul vous pouvez vous connecter à votre compte utilisateur. Si vous perdez votre mot de passe ou si un robot l’anticipe, l’authentification à deux facteurs ajoute une couche de protection. Par exemple, vous pouvez utiliser l’authentificateur Google pour générer des codes destinés à l’administrateur de votre boutique, de votre compte Commerce et de votre compte Google.

![ Iphone de configuration de sécurité - 2FA](./assets/google-authenticator-iphone.png){width="300"}

Adobe Commerce prend en charge les méthodes 2FA de plusieurs fournisseurs. Certains nécessitent l’installation d’une application qui génère un mot de passe unique (OTP) que les utilisateurs saisissent lors de leur connexion pour vérifier leur identité. Les appareils de second facteur universel (U2F) ressemblent à un robot clé et génèrent une clé unique pour vérifier l’identité. D’autres périphériques vérifient l’identité lorsqu’ils sont insérés dans un port USB. En tant qu’administrateur de magasin, vous pouvez avoir besoin d’une ou de plusieurs des méthodes 2FA disponibles pour vérifier l’identité de l’utilisateur. Votre configuration 2FA s’applique à tous les sites web et magasins associés à l’installation Adobe Commerce.

La première fois qu’un utilisateur se connecte à l’_Admin_, il doit configurer chaque méthode [2FA](../configuration-reference/security/2fa.md) dont vous avez besoin et vérifier son identité à l’aide de l’application ou de l’appareil associé. Après cette configuration initiale, l’utilisateur doit s’authentifier à l’aide de l’une des méthodes configurées à chaque connexion. Les informations 2FA de chaque utilisateur sont enregistrées dans son compte _Admin_ et peuvent être [reset](security-two-factor-authentication-manage.md) si nécessaire. Pour en savoir plus sur le processus de connexion, accédez à [_Admin_ Se connecter](../getting-started/admin-signin.md).

>[!NOTE]
>
>Les magasins qui ont activé l’authentification Adobe Identity Management Services (IMS) ont désactivé Adobe Commerce et Magento Open Source 2FA natifs. Les utilisateurs administrateurs connectés à leur instance Commerce avec leurs informations d’identification d’Adobe n’ont pas besoin de se réauthentifier pour de nombreuses tâches d’administration. L’authentification est gérée par Adobe IMS lorsque l’utilisateur administrateur se connecte à sa session en cours. Voir [Présentation de l’intégration d’Adobe Identity Management Service (IMS)](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

Vous pouvez regarder cette [démonstration vidéo](https://video.tv.adobe.com/v/339104?quality=12&learn=on) pour un aperçu de l’authentification à deux facteurs dans l’administrateur.

## Configuration de vos fournisseurs 2FA requis

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Security]** et choisissez **[!UICONTROL 2FA]**.

1. Dans la section _[!UICONTROL General]_, sélectionnez les fournisseurs à utiliser.

   | Fournisseur | Fonction |
   |--- |--- |
   | [!UICONTROL Google Authenticator] | Génère un mot de passe unique dans l’application pour l’authentification des utilisateurs. |
   | [!UICONTROL Duo Security] | Fournit des SMS et des notifications push. |
   | [!UICONTROL Authy] | Génère un code à six chiffres dépendant du temps et fournit une protection ou un jeton SMS ou d’appel Voix 2FA. |
   | [!UICONTROL U2F Devices (Yubikey and others)] | Utilise un appareil physique à authentifier, tel que [[!DNL YubiKey]](https://www.yubico.com/). |

   Pour sélectionner plusieurs méthodes, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque élément.

1. Définissez les paramètres de chaque méthode 2FA requise.

   ![Configuration de la sécurité - 2FA](../configuration-reference/security/assets/2fa-general.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

   La première fois que les utilisateurs se connectent à _Admin_, ils doivent configurer chaque méthode 2FA requise. Après cette configuration initiale, ils doivent s’authentifier à l’aide de l’une des méthodes configurées chaque fois qu’ils se connectent.

## Paramètres du fournisseur 2FA

Définissez les paramètres de chaque méthode 2FA dont vous avez besoin.

### Google

Pour modifier la durée pendant laquelle le mot de passe unique (OTP) est disponible lors de la connexion, décochez la case **[!UICONTROL Use system value]** . Ensuite, saisissez le nombre de secondes que vous souhaitez que le **[!UICONTROL OTP Window]** soit valide.

![Configuration de la sécurité - Google](../configuration-reference/security/assets/2fa-google.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Dans Adobe Commerce 2.4.7 et versions ultérieures, le paramètre de configuration de fenêtre OTP contrôle la durée (en secondes) pendant laquelle le système accepte le mot de passe unique (OTP) d’un administrateur après expiration. Cette valeur doit être inférieure à 30 secondes. Le paramètre par défaut du système est `29`.<br><br> Dans la version 2.4.6, le paramètre de fenêtre OTP détermine le nombre de codes OTP passés et futurs qui restent valides. Une valeur `1` indique que le code OTP actuel plus un code dans le passé et un code dans le futur restent valides à tout moment donné.

### [!DNL Duo Security]

Saisissez les informations d’identification suivantes à partir de votre compte Duo Security :

- Clé d’intégration
- Clé secrète
- Nom d’hôte API

![Configuration de la sécurité - Duo](../configuration-reference/security/assets/2fa-duo-security.png){width="600" zoomable="yes"}

### [!DNL Authy]

1. Saisissez la clé API de votre compte [!DNL Authy].

1. Pour modifier le message par défaut qui s’affiche pendant l’authentification, décochez la case **[!UICONTROL Use system value]** . Ensuite, saisissez le **[!UICONTROL OneTouch Message]** que vous souhaitez afficher.

   ![ Configuration de sécurité - Authy](../configuration-reference/security/assets/2fa-authy.png){width="600" zoomable="yes"}

### Appareils U2F ([!DNL Yubikey] et autres)

Le domaine du magasin est utilisé par défaut lors du processus d’authentification. Pour utiliser un domaine personnalisé pour les défis d’authentification, décochez la case **[!UICONTROL Use system value]** . Ensuite, saisissez le **[!UICONTROL WebAPi Challenge Domain]**.

![Configuration de la sécurité - Périphériques U2F](../configuration-reference/security/assets/2fa-u2f-key.png){width="600" zoomable="yes"}
