---
title: Authentification à deux facteurs (2FA)
description: Découvrez la prise en charge de l’authentification à deux facteurs pour garantir la sécurité de votre système et de vos données.
exl-id: d9eb3dd6-4a7b-411a-ac08-0441803cd59a
role: Admin
feature: Configuration, Security, User Account
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 0%

---

# Authentification à deux facteurs (2FA)

Commerce _Admin_ pour votre installation d’Adobe Commerce ou de Magento Open Source permet d’accéder à votre boutique, à vos commandes et aux données de vos clients. Pour empêcher tout accès non autorisé à vos données, tous les utilisateurs qui tentent de se connecter à l’_Admin_ doivent effectuer un processus d’authentification pour vérifier leur identité.

>[!NOTE]
>
>Cette implémentation de l’authentification à deux facteurs (2FA) s’applique uniquement à l’_administrateur_ et n’est pas disponible pour les comptes clients. L’authentification à deux facteurs qui protège votre compte Commerce dispose d’une configuration distincte. Pour en savoir plus, rendez-vous sur [Sécuriser votre compte Commerce](../getting-started/commerce-account-secure.md).

L’authentification à deux facteurs est largement utilisée et il est courant de générer des codes d’accès pour différents sites web sur la même application. Cette authentification supplémentaire permet de s’assurer que vous seul pouvez vous connecter à votre compte utilisateur. Si vous perdez votre mot de passe ou qu’un robot le devine, l’authentification à deux facteurs ajoute une couche de protection. Par exemple, vous pouvez utiliser l’authentificateur Google pour générer des codes pour l’administrateur de votre boutique, votre compte Commerce et votre compte Google.

![Configuration de la sécurité iphone - 2FA](./assets/google-authenticator-iphone.png){width="300"}

Adobe Commerce prend en charge les méthodes 2FA de plusieurs fournisseurs. Certains nécessitent l’installation d’une application qui génère un mot de passe à usage unique (OTP) que les utilisateurs saisissent lors de la connexion pour vérifier leur identité. Les périphériques de second facteur universel (U2F) ressemblent à un porte-clés et génèrent une clé unique pour vérifier l’identité. D&#39;autres périphériques vérifient l&#39;identité lorsqu&#39;ils sont insérés dans un port USB. En tant qu’administrateur de magasin, vous pouvez avoir besoin d’une ou de plusieurs des méthodes 2FA disponibles pour vérifier l’identité de l’utilisateur. Votre configuration 2FA s’applique à tous les sites web et magasins associés à l’installation d’Adobe Commerce.

La première fois qu’un utilisateur se connecte à l’_Admin_, il doit configurer chaque méthode [2FA](../configuration-reference/security/2fa.md) dont vous avez besoin et vérifier son identité à l’aide de l’application ou de l’appareil associé. Après cette configuration initiale, l’utilisateur doit s’authentifier à l’aide de l’une des méthodes configurées chaque fois qu’il se connecte. Les informations 2FA de chaque utilisateur sont enregistrées dans son compte _Admin_ et peuvent être [réinitialisées](security-two-factor-authentication-manage.md) si nécessaire. Pour en savoir plus sur le processus de connexion, rendez-vous sur [_Admin_ Connexion](../getting-started/admin-signin.md).

>[!NOTE]
>
>Les magasins qui ont activé l’authentification Adobe Identity Management Services (IMS) ont désactivé Adobe Commerce et Magento Open Source 2FA natifs. Les utilisateurs administrateurs connectés à leur instance Commerce avec leurs informations d’identification Adobe n’ont pas besoin de s’authentifier à nouveau pour de nombreuses tâches d’administration. L’authentification est gérée par Adobe IMS lorsque l’utilisateur administrateur se connecte à sa session en cours. Voir [Présentation de l’intégration du service Adobe Identity Management (IMS)](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html?lang=fr).

Vous pouvez regarder cette [vidéo de démonstration](https://video.tv.adobe.com/v/339104?quality=12&learn=on) pour un aperçu de l’authentification à deux facteurs dans l’interface d’administration.

## Configurer les fournisseurs 2FA requis

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Security]** et choisissez **[!UICONTROL 2FA]**.

1. Dans la section _[!UICONTROL General]_, sélectionnez les fournisseurs à utiliser.

   | Fournisseur | Fonction |
   |--- |--- |
   | [!UICONTROL Google Authenticator] | Génère un mot de passe à usage unique dans l’application pour l’authentification des utilisateurs. |
   | [!UICONTROL Duo Security] | Fournit des SMS et des notifications push. |
   | [!UICONTROL Authy] | Génère un code à six chiffres dépendant du temps et fournit une protection ou un jeton SMS ou d’appel vocal 2FA. |
   | [!UICONTROL U2F Devices (Yubikey and others)] | Utilise un appareil physique pour l’authentification, tel que [[!DNL YubiKey]](https://www.yubico.com/). |

   Pour sélectionner plusieurs méthodes, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et cliquez sur chaque élément.

1. Renseignez les [paramètres](../configuration-reference/security/2fa.md) pour chaque méthode 2FA requise.

   ![Configuration de la sécurité - 2FA](../configuration-reference/security/assets/2fa-general.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

   La première fois que les utilisateurs se connectent à l’_Admin_, ils doivent configurer chaque méthode 2FA requise. Après cette configuration initiale, ils doivent s’authentifier à l’aide de l’une des méthodes configurées chaque fois qu’ils se connectent.

## Paramètres du fournisseur 2FA

Définissez les paramètres de chaque méthode 2FA dont vous avez besoin.

### Google

Pour modifier la durée pendant laquelle le mot de passe à usage unique (OTP) est disponible lors de la connexion, décochez la case **[!UICONTROL Use system value]**. Saisissez ensuite le nombre de secondes pendant lesquelles vous souhaitez que le **[!UICONTROL OTP Window]** soit valide.

![&#x200B; Configuration de la sécurité - Google &#x200B;](../configuration-reference/security/assets/2fa-google.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Dans Adobe Commerce version 2.4.7 et ultérieure, le paramètre de configuration de la fenêtre du mot de passe à usage unique contrôle la durée (en secondes) pendant laquelle le système accepte le mot de passe à usage unique (OTP) d’un administrateur après son expiration. Cette valeur doit être inférieure à 30 secondes. Le paramètre système par défaut est `29`.<br><br> Dans la version 2.4.6, le paramètre de fenêtre OTP détermine le nombre de codes OTP passés et futurs qui restent valides. Une valeur `1` indique que le code OTP actuel plus un code dans le passé et un code dans le futur restent valides à un moment donné.

### [!DNL Duo Security]

Saisissez les informations d’identification suivantes à partir de votre compte Duo Security :

- Identifiant client
- Secret client
- Clé d’intégration
- Clé secret
- Nom d’hôte de l’API

![Configuration de la sécurité - Duo](../configuration-reference/security/assets/2fa-duo-security.png){width="600" zoomable="yes"}

### [!DNL Authy]

1. Saisissez la clé API de votre compte [!DNL Authy].

1. Pour modifier le message par défaut qui s’affiche lors de l’authentification, décochez la case **[!UICONTROL Use system value]** . Ensuite, saisissez le **[!UICONTROL OneTouch Message]** que vous souhaitez afficher.

   ![Configuration de la sécurité - Authentifier](../configuration-reference/security/assets/2fa-authy.png){width="600" zoomable="yes"}

### Dispositifs U2F ([!DNL Yubikey] et autres)

Le domaine de magasin est utilisé par défaut pendant le processus d’authentification. Pour utiliser un domaine personnalisé pour les défis d’authentification, décochez la case **[!UICONTROL Use system value]** . Saisissez ensuite le **[!UICONTROL WebAPi Challenge Domain]**.

![Configuration de la sécurité - Appareils U2F](../configuration-reference/security/assets/2fa-u2f-key.png){width="600" zoomable="yes"}
