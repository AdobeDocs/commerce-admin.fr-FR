---
title: Configuration de l’authentification à deux facteurs pour les comptes utilisateur
description: Découvrez comment configurer l’authentification à deux facteurs lors de la connexion initiale de l’administrateur et authentifier votre identité à l’aide d’une application d’appareil prise en charge.
exl-id: 1ea7f09e-4753-40fa-b9d4-376ba5d8f58f
role: Admin, User
feature: Configuration, Security, User Account
source-git-commit: dc6e5fc7c0996af30bae6374cd7c9879902b9235
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 0%

---

# Configuration de l’authentification à deux facteurs pour les comptes utilisateurs

Ces instructions montrent comment configurer l’authentification à deux facteurs lors de votre connexion initiale à Adobe Commerce ou Magento Open Source et comment authentifier votre identité à l’aide des applications et appareils suivants.

Pour obtenir des instructions complètes, voir [Admin Login](../getting-started/admin-signin.md).

>[!NOTE]
>
>Les magasins qui ont activé [!DNL Adobe Identity Management Services] l’authentification (IMS) ont Adobe natif Commerce et Magento Open Source 2FA désactivés. Les utilisateurs administrateurs connectés à leur instance Commerce avec leurs informations d’identification Adobe n’ont pas besoin de se réauthentifier pour de nombreuses tâches d’administration. Authentication est gérée par Adobe IMS lorsque l’utilisateur Admin se connecte à sa session en cours. Voir [[!DNL Adobe Identity Management Service] (IMS) Vue d’ensemble](../getting-started/adobe-ims-integration-overview.md) de l’intégration.

## [!DNL Google Authenticator]

### Étape 1 : configurer [!DNL Google Authenticator]

1. Saisissez les informations d’identification de votre compte et connectez-vous à l’adresse _Admin_. Un nouvel écran d’authentification s’affiche avec un code QR.

1. Ouvrez l’application **[!UICONTROL Google Authenticator]** sur votre appareil mobile.

1. Cliquez sur le signe plus ( **+** ) pour ajouter une entrée et mettre en ligne la zone rouge avec le code QR à scanner avec la caméra sur votre smartphone.

1. Lorsque votre téléphone reconnaît le code QR et ajoute une entrée, saisissez ce code à 6 chiffres dans le champ de **[!UICONTROL Authenticator code]** _Admin_.

1. Cliquez ensuite sur **[!UICONTROL Confirm]**.

   ![Code QR de l’authentificateur Google](./assets/storefront-2fa-google-qrcode.png){width="300"}

### Étape 2 : Se connecter avec [!DNL Google Authenticator]

1. Saisissez les informations d’identification de votre compte et connectez-vous au Commerce _Admin_.

   ![Authentificateur Google - connexion](./assets/storefront-2fa-google-code.png){width="300"}

1. Ouvrez [!DNL Google Authenticator] sur votre appareil mobile.

1. À l’invite, saisissez le code d’authentification à six chiffres.

1. Pour enregistrer l’authentification pour les prochaines connexions, cochez la case **[!UICONTROL Trust this device, do not ask again]** .

1. Cliquez ensuite sur **[!UICONTROL Confirm]**.

## [!DNL Duo Security]

[!DNL Duo] offre une version d’évaluation gratuite et des frais en fonction du nombre d’utilisateurs associés au compte. Suivez leurs [instructions pour configurer votre compte et télécharger l’application](https://duo.com/product/multi-factor-authentication-mfa/duo-mobile-app).

### Étape 1 : Configuration [!DNL Duo Security]

1. Saisissez les informations d’identification de votre compte et connectez-vous à l’administrateur __.

1. Lorsque la page Configuration s’affiche [!DNL Duo] , cliquez **[!UICONTROL Get Started]** et procédez comme suit :

   ![Exemple de vitrine - Configuration Duo](./assets/storefront-2fa-duo-setup-options.png){width="300"}

1. Sélectionnez votre option. Vous pouvez choisir Touch ID, Duo Mobile, Clé de sécurité ou Numéro de téléphone. Cet exemple illustre l’option Duo Mobile ou Numéro de téléphone.

1. A l&#39;invite, entrez votre numéro de téléphone et cliquez sur **[!UICONTROL Continue]**.

   Confirmez le propriétaire en envoyant et en vérifiant le mot de passe sur le numéro de téléphone.

1. Lorsque vous êtes invité à installer [!DNL Duo Mobile] pour votre type de téléphone, cliquez sur **[!UICONTROL I have Duo Mobile]**.

1. Ouvrez [!DNL Duo Mobile] et scannez le code QR pour synchroniser l’authentificateur avec Adobe Commerce. Une coche apparaît une fois l’activation terminée.

1. Vous pouvez ajouter d’autres appareils (si nécessaire) ou les ignorer. Votre configuration est maintenant terminée et vous pouvez vous connecter avec Duo.

   ![Actions de vérification Duo](./assets/storefront-2fa-duo-setup-complete.png){width="300"}

### Étape 2 : Se connecter avec [!DNL Duo Security]

L’exemple suivant illustre les options de `Ask me to choose an authenticator method` :

1. Lorsque vous y êtes invité, saisissez vos informations d’identification _Admin_ pour vous connecter.

   ![Duo - connexion](./assets/storefront-2fa-duo-auth.png){width="300"}

1. Choisissez Se connecter avec Duo pour recevoir une notification push sur l’application Duo Mobile, connectez-vous avec Touch ID ou utilisez une autre option que vous avez configurée lors de la configuration.

1. Approuvez la demande de l’application Duo / de l’ID tactile / du message texte et vous serez correctement connecté.

   ![Duo - connexion](./assets/storefront-2fa-duo-success.png){width="300"}

## [!DNL Authy]

[!DNL Authy] offre son application et son service gratuitement aux utilisateurs. Suivez leurs instructions pour télécharger et configurer l’application pour votre appareil ou navigateur. Pour en savoir plus, consultez la [[!DNL Authy] documentation](https://authy.com/features/setup/).

### Étape 1 : Configuration d’Authy

1. Saisissez les informations d’identification de votre compte et connectez-vous à l’adresse _Admin_.

   ![[!DNL Authy] enregistrement](./assets/storefront-2fa-authy-auth.png){width="300"}

1. Lorsque vous êtes invité à vous enregistrer auprès de l’auteur, procédez comme suit :

   - Sélectionnez votre pays.

   - Saisissez votre numéro de téléphone.

   - Sélectionnez le **[!UICONTROL Verification method]** : `SMS` ou `Call Me`

   Cliquez sur **[!UICONTROL Continue]**. Un message est envoyé à votre téléphone par SMS ou par appel.

1. Saisissez le code de vérification que vous recevez et cliquez sur **[!UICONTROL Verify]**.

1. Cliquez ensuite sur **[!UICONTROL Confirm]**.

   ![[!DNL Authy] code de vérification](./assets/storefront-2fa-authy-verify.png){width="300"}

### Étape 2 : Se connecter avec [!DNL Authy]

1. Saisissez les informations d’identification de votre compte et connectez-vous à l’administrateur __.

   ![[!DNL Authy] - connexion](./assets/storefront-2fa-authy-access.png){width="300"}

1. Sélectionnez l’une des méthodes d’authentification suivantes :

   - `Use one touch` — Envoie une alerte à votre application [!DNL Authy]. Dans l’application, acceptez l’accès.
   - `Use authy token` — Invite à saisir un code de votre [!DNL Authy] application.

1. Si vous ne parvenez pas à vous connecter, choisissez la méthode que vous souhaitez utiliser pour recevoir le code. Ensuite, entrez le code que vous recevez pour accéder à l’administrateur __.

   L’application inclut ces méthodes d’urgence supplémentaires.

   - `Send me a code via SMS` — Un SMS texte est envoyé à l’appareil mobile configuré.
   - `Send me a code via phone call` — L’utilisateur reçoit un appel téléphonique avec un code.

   Votre compte est vérifié et s’ouvre.

## U2F ([!DNL Yubikey] et autres appareils)

Suivez les instructions du fournisseur de solution pour configurer votre appareil U2F. Pour plus d’informations, consultez la documentation du fournisseur, par exemple [[!DNL YubiKey]](https://support.yubico.com/hc/en-us/articles/360013790339-Getting-Started-with-Your-YubiKey) par [!UICONTROL Yubico].

1. Saisissez les informations d’identification de votre compte et connectez-vous à l’adresse _Admin_.

   Accès à la clé ![U2F](./assets/storefront-2fa-u2f.png){width="300"}

1. Appuyez sur la touche.

   L’authentification se déclenche immédiatement et ouvre l’_Admin_.

1. Insérez le **[!UICONTROL U2F key]** dans un port USB de votre ordinateur.
