---
title: Configuration de l’authentification à deux facteurs pour les comptes d’utilisateurs
description: Découvrez comment configurer une authentification à deux facteurs lors de la connexion initiale de l’administrateur et authentifier votre identité à l’aide d’une application d’appareil prise en charge.
exl-id: 1ea7f09e-4753-40fa-b9d4-376ba5d8f58f
role: Admin, User
feature: Configuration, Security, User Account
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# Configuration de l’authentification à deux facteurs pour les comptes d’utilisateurs

Ces instructions expliquent comment configurer une authentification à deux facteurs lors de votre connexion initiale à Adobe Commerce ou Magento Open Source et comment authentifier votre identité à l’aide des applications et des appareils suivants.

Pour obtenir des instructions complètes, voir [Connexion de l’administrateur](../getting-started/admin-signin.md).

>[!NOTE]
>
>Les magasins qui ont activé l’authentification [!DNL Adobe Identity Management Services] (IMS) ont natif Adobe Commerce et Magento Open Source 2FA désactivé. Les utilisateurs administrateurs connectés à leur instance Commerce avec leurs informations d’identification d’Adobe n’ont pas besoin de se réauthentifier pour de nombreuses tâches d’administration. L’authentification est gérée par Adobe IMS lorsque l’utilisateur administrateur se connecte à sa session en cours. Voir [[!DNL Adobe Identity Management Service] (IMS) Présentation de l’intégration ](../getting-started/adobe-ims-integration-overview.md).

## [!DNL Google Authenticator]

### Étape 1 : configuration de [!DNL Google Authenticator]

1. Entrez vos informations d’identification de compte et connectez-vous à _Admin_. Un nouvel écran d’authentification s’affiche avec un code QR.

1. Ouvrez l’application **[!UICONTROL Google Authenticator]** sur votre appareil mobile.

1. Cliquez sur le signe plus ( **+** ) pour ajouter une entrée et aligner la zone rouge avec le code QR à analyser avec l’appareil photo sur votre smartphone.

1. Lorsque votre téléphone reconnaît le code QR et ajoute une entrée, saisissez ce code à 6 chiffres dans le champ _Admin_ **[!UICONTROL Authenticator code]** .

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Confirm]**.

   ![Code QR de l’authentificateur Google](./assets/storefront-2fa-google-qrcode.png){width="300"}

### Étape 2 : connexion avec [!DNL Google Authenticator]

1. Entrez vos informations d’identification de compte et connectez-vous à Commerce _Admin_.

   ![Authentificateur Google - connexion](./assets/storefront-2fa-google-code.png){width="300"}

1. Ouvrez [!DNL Google Authenticator] sur votre appareil mobile.

1. Lorsque vous y êtes invité, saisissez le code d’authentification à six chiffres.

1. Pour enregistrer l’authentification pour les connexions futures, cochez la case **[!UICONTROL Trust this device, do not ask again]** .

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Confirm]**.

## [!DNL Duo Security]

[!DNL Duo] offre un essai gratuit et des frais en fonction du nombre d’utilisateurs associés au compte. Suivez leurs [ instructions pour configurer votre compte et télécharger l’application ](https://duo.com/product/multi-factor-authentication-mfa/duo-mobile-app).

### Étape 1 : configuration de [!DNL Duo Security]

1. Entrez vos informations d’identification de compte et connectez-vous à _Admin_.

1. Lorsque la page de configuration [!DNL Duo] s’affiche, cliquez sur **[!UICONTROL Start setup]** et procédez comme suit :

   ![Exemple de storefront - Duo setup](./assets/storefront-2fa-duo-user1.png){width="300"}

1. Sélectionnez votre appareil.

1. Lorsque vous y êtes invité, saisissez votre numéro de téléphone et cliquez sur **[!UICONTROL Continue]**.

   Cet exemple demande votre numéro de téléphone, car nous utilisons un appareil mobile.

1. Lorsque vous êtes invité à installer [!DNL Duo Mobile] pour votre type de téléphone, cliquez sur **[!UICONTROL I have Duo Mobile]**.

1. Ouvrez [!DNL Duo Mobile] et analysez le code QR pour synchroniser l’authentificateur avec Adobe Commerce. Une coche s’affiche lorsque l’activation est terminée.

1. Pour configurer vos paramètres pour l’appareil, choisissez l’action que vous souhaitez effectuer lorsque vous vous connectez.

   - `Ask me to choose an authenticator method` — Permet à l’utilisateur de sélectionner lors de la connexion et de l’authentification dans le _Admin_.
   - `Automatically send this device a Duo Push` — Envoie un message à votre appareil pour accepter ou refuser l’accès.
   - `Automatically call this device` — Appelle et fournit un code de passe à saisir pour l’accès.

   ![ Actions de vérification de duo](./assets/storefront-2fa-duo-user7.png){width="300"}

### Étape 2 : connexion avec [!DNL Duo Security]

L’exemple suivant illustre les options pour `Ask me to choose an authenticator method` :

1. Lorsque vous y êtes invité, saisissez vos informations d’identification _Admin_ pour vous connecter.

   ![ Duo - connexion](./assets/storefront-2fa-duo-auth.png){width="300"}

1. Sélectionnez la méthode à utiliser pour l’authentification :

   - `Send Me a Push` — Cliquez pour recevoir une notification push vers [!DNL Duo Mobile]. Acceptez de vous authentifier.
   - `Call Me` — Cliquez sur cette option, recevez un appel avec un code et saisissez le code de passe.
   - `Enter a Passcode` — Cliquez sur cette option pour recevoir et saisir un code de passe.

1. Complétez la notification push ou le code pour vous connecter entièrement à l’ _Admin_.

## [!DNL Authy]

[!DNL Authy] offre gratuitement son application et son service aux utilisateurs. Suivez leurs instructions pour télécharger et configurer l’application pour votre appareil ou navigateur. Pour en savoir plus, consultez la [[!DNL Authy] documentation](https://authy.com/features/setup/).

### Étape 1 : configuration de l’authentification

1. Entrez vos informations d’identification de compte et connectez-vous à _Admin_.

   ![[!DNL Authy] registration](./assets/storefront-2fa-authy-auth.png){width="300"}

1. Lorsque vous êtes invité à vous enregistrer auprès de l’instance d’auteur, procédez comme suit :

   - Sélectionnez votre pays.

   - Saisissez votre numéro de téléphone.

   - Sélectionnez le **[!UICONTROL Verification method]** : `SMS` ou `Call Me`

   Cliquez sur **[!UICONTROL Continue]**. Un message est envoyé à votre téléphone par SMS ou par un appel.

1. Saisissez le code de vérification que vous recevez, puis cliquez sur **[!UICONTROL Verify]**.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Confirm]**.

   ![[!DNL Authy] code de vérification](./assets/storefront-2fa-authy-verify.png){width="300"}

### Étape 2 : connexion avec [!DNL Authy]

1. Entrez vos informations d’identification de compte et connectez-vous à _Admin_.

   ![[!DNL Authy] - signature](./assets/storefront-2fa-authy-access.png){width="300"}

1. Choisissez l’une des méthodes suivantes pour vous authentifier :

   - `Use one touch` — Envoie une alerte à votre application [!DNL Authy]. Dans l’application, acceptez l’accès.
   - `Use authy token` — Indique de saisir un code à partir de votre application [!DNL Authy].

1. Si vous rencontrez des difficultés pour vous connecter, choisissez la méthode à utiliser pour recevoir le code. Saisissez ensuite le code que vous recevez pour accéder à l’ _Admin_.

   L’application inclut ces méthodes d’urgence supplémentaires.

   - `Send me a code via SMS` — Un SMS est envoyé au périphérique mobile configuré.
   - `Send me a code via phone call` : l’utilisateur reçoit un appel téléphonique avec un code.

   Votre compte est vérifié et ouvert.

## U2F ([!DNL Yubikey] et autres appareils)

Suivez les instructions du fournisseur de solution pour configurer votre appareil U2F. Pour plus d’informations, consultez la documentation du fournisseur, par exemple [[!DNL YubiKey]](https://support.yubico.com/hc/en-us/articles/360013790339-Getting-Started-with-Your-YubiKey) par [!UICONTROL Yubico].

1. Entrez vos informations d’identification de compte et connectez-vous à _Admin_.

   ![Accès à la clé U2F](./assets/storefront-2fa-u2f.png){width="300"}

1. Appuyez sur le bouton de la touche.

   L’authentification déclenche et ouvre immédiatement le _Admin_.

1. Insérez le **[!UICONTROL U2F key]** dans un port USB de votre ordinateur.
