---
title: Sécurisez votre compte  [!DNL Commerce]
description: Découvrez comment utiliser l'authentification à deux facteurs pour sécuriser votre compte  [!DNL Commerce] .
exl-id: 4847b5cb-a93a-40d0-8c31-c30afa27c0ce
feature: User Account
source-git-commit: fff3464c9da50927bbe9773a17b0f6858360d788
workflow-type: tm+mt
source-wordcount: '1687'
ht-degree: 0%

---

# Sécurisez votre compte [!DNL Commerce]

L’authentification à deux facteurs (TFA ou 2FA) est une couche de sécurité supplémentaire pour mieux protéger votre compte [!DNL Commerce] contre tout accès non autorisé. Pour terminer le processus de connexion, TFA a besoin d’un _second facteur_ en plus des informations d’identification d’utilisateur et de mot de passe standard. Ce second facteur prend la forme de codes de vérification temporaires générés en continu par une application TFA installée sur votre appareil mobile et associée à votre compte [!DNL Commerce].

Lorsque TFA est activé, votre compte est plus sécurisé. Un utilisateur non autorisé ne peut pas se connecter à moins qu’il ne dispose à la fois de vos informations d’identification d’utilisateur et de mot de passe (premier facteur) et d’un code de vérification valide de l’application TFA sur votre appareil personnel (second facteur).

>[!NOTE]
>
>L’authentification à deux facteurs qui protège l’_administrateur_ de votre boutique a une configuration distincte. Pour en savoir plus, voir [Authentification à deux facteurs](../systems/security-two-factor-authentication.md).

## Avant de commencer

Pour utiliser TFA, une application TFA doit être installée sur votre appareil personnel (smartphone, tablette, ordinateur, etc.). De nombreuses options sont disponibles, mais certaines sont populaires et gratuites :

- Authentificateur Google (iOS, Android™, BlackBerry®)

- Création (iOS, Android™)

- Authentificateur Microsoft® (iOS, Android™, Windows Phone)

## Activer l’authentification à deux facteurs

1. Connectez-vous à votre [[!DNL Commerce] compte][1]{:target=&quot;_blank&quot;}.

1. Dans le volet de navigation de gauche, sélectionnez **[!UICONTROL Account Settings]**, puis **[!UICONTROL Two-factor Authentication]**.

   ![Activer TFA](./assets/2fa-enable.png){width="600" zoomable="yes"}

1. Sélectionnez **[!UICONTROL Enable]** pour lancer le processus de configuration de l’authentification à deux facteurs.

1. Saisissez le **[!UICONTROL Verification Code]** envoyé à votre email et sélectionnez **[!UICONTROL Verify Code]** pour continuer.

   ![Entrez le code de vérification](./assets/2fA-verification-code-prompt.png){width="400"}

1. Ouvrez l’application d’authentification à deux facteurs que vous avez téléchargée et installée sur votre périphérique personnel.

1. Sur le formulaire [!UICONTROL SETUP TWO-FACTOR AUTHENTICATION], utilisez le **[!UICONTROL Setup Code]** pour ajouter Adobe Commerce à votre application TFA.

   ![Ajout d’Adobe Commerce à l’application TFA](./assets/commerce-account-2fa-setup-app.png){width="400"}

   Vous pouvez ajouter le code en analysant le code QR à l’aide de l’application TFA ou en le saisissant manuellement. Ce code associe votre application TFA à votre compte [!DNL Commerce] et permet aux autorisations de générer l’application TFA afin de générer des codes de vérification pour un accès sécurisé au compte.

1. Terminez la configuration.

   - Sur le formulaire [!UICONTROL SETUP TWO FACTOR-AUTHENTICATION], saisissez le code de vérification de votre application d’authentification à deux facteurs.

   - Sélectionnez **[!UICONTROL Verify Code]**.

   >[!NOTE]
   >
   >Pour des raisons de sécurité, les codes de vérification de votre application TFA expirent et se régénèrent en permanence. **_Toujours_** utilisez le code actuellement affiché.

1. Enregistrez le **[!UICONTROL Recovery Codes]** présenté dans un endroit sûr et accessible.

   ![Stocker les codes de récupération](./assets/commerce-account-2fa-store-recovery-codes.png){width="400"}

   Si vous ne pouvez pas fournir de code de vérification lorsque vous vous connectez à votre compte [!DNL Commerce], vous devez utiliser un code de récupération pour récupérer l’accès au compte.

   Chaque code de récupération ne peut être utilisé qu’une seule fois, mais vous pouvez [en générer](#generate-new-recovery-codes) de nouveaux. Les codes de récupération respectent la casse.

1. Cochez la case de confirmation et sélectionnez **[!UICONTROL Submit]** pour continuer.

1. Pour vous assurer que vous pouvez récupérer l’accès à votre compte, saisissez un **[!UICONTROL Recovery Email]**.

   Cette adresse électronique est nécessaire si vous ne pouvez pas générer de code de vérification à partir de votre application d’authentification à deux facteurs et que vous n’avez pas accès à un code de récupération prégénéré inutilisé.

   Une fois toutes les 24 heures, vous pouvez générer et envoyer un code de récupération temporaire à votre adresse électronique de récupération désignée. Utilisez ce code pour récupérer l’accès au compte.

   >[!IMPORTANT]
   >
   >Maintenez l’accès à votre compte de messagerie de récupération. Sinon, vous ne pouvez pas utiliser les codes de récupération temporaires envoyés à ce compte.

   ![Définir l’email de récupération](./assets/commerce-account-2fa-set-recovery-email.png){width="400"}

1. Cochez la case de confirmation et sélectionnez **[!UICONTROL Submit]** pour terminer le processus de configuration de l’authentification à deux facteurs.

   - Une notification est envoyée à l’adresse électronique associée à votre compte [!DNL Commerce] pour confirmer que vous avez activé l’authentification à deux facteurs.

   - Une notification est envoyée à votre compte de messagerie de récupération pour confirmer la configuration.

>[!TIP]
>
>Si vous perdez votre périphérique personnel ou en obtenez un nouveau, vous pouvez [modifier votre application d’authentification à deux facteurs](#change-your-two-factor-authentication-application) et générer de nouveaux codes de récupération.

## Connexion à l’aide d’un code de vérification

1. Accédez au [!DNL Commerce] [compte login][1]{:target=&quot;_blank&quot;}.

1. Saisissez votre nom d’utilisateur et votre mot de passe, puis sélectionnez **[!UICONTROL Login]**.

1. Saisissez le **[!UICONTROL Verification Code]** affiché dans votre application d’authentification à deux facteurs lorsque vous y êtes invité.

   ![Entrer le code de vérification](./assets/commerce-account-2fa-login-verification-code.png){width="600"}

1. Sélectionnez **[!UICONTROL Submit]** pour terminer le processus de connexion.

## Connexion à l’aide d’un code de récupération

1. Accédez au [!DNL Commerce] [compte login][1]{:target=&quot;_blank&quot;}.

1. Saisissez votre nom d’utilisateur et votre mot de passe, puis sélectionnez **[!UICONTROL Login]**.

1. Sélectionnez **[!UICONTROL Use recovery code]** pour contourner l’invite de code de vérification.

1. Saisissez un **[!UICONTROL Recovery Code]** inutilisé lorsque vous y êtes invité.

   ![Entrer le code de récupération](./assets/2fa-recovery-code.png){width="600"}

1. Sélectionnez **[!UICONTROL Submit]** pour terminer le processus de connexion.

## Connectez-vous à l’aide de votre email de récupération

1. Connectez-vous à votre [[!DNL Commerce] compte][1]{:target=&quot;_blank&quot;}.

1. Saisissez votre nom d’utilisateur et votre mot de passe, puis sélectionnez **[!UICONTROL Login]**.

1. Sélectionnez **[!UICONTROL Use recovery code]** pour contourner l’invite de code de vérification.

1. Pour obtenir un code de récupération temporaire par courrier électronique, cliquez sur le lien **[!UICONTROL recovery email]** .

   ![Utiliser l’email de récupération](./assets/2fa-recovery-email.png){width="600"}

1. Ouvrez votre compte de courrier électronique de récupération pour obtenir le code temporaire, puis saisissez le code dans les champs désignés.

1. Sélectionnez **[!UICONTROL Submit]** pour terminer le processus de connexion.

Après avoir utilisé un code de récupération temporaire pour accéder à votre compte, [générez de nouveaux codes de récupération](#generate-new-recovery-codes) et enregistrez-les afin d’éviter d’autres problèmes d’accès au compte.

## Afficher vos codes de récupération

1. Accédez au [!DNL Commerce] [compte login][1]{:target=&quot;_blank&quot;}.

1. Saisissez votre nom d’utilisateur et votre mot de passe, puis sélectionnez **[!UICONTROL Login]**.

1. Procédez à la connexion à l’aide de l’une des méthodes d’authentification à deux facteurs décrites précédemment.

1. Dans le volet de navigation de gauche, sélectionnez **[!UICONTROL Account Settings]**, puis **[!UICONTROL Two-factor Authentication]**.

   ![2FA settings](./assets/commerce-account-2fa-manage.png){width="600" zoomable="yes"}

1. Pour afficher vos codes de récupération prégénérés, sélectionnez **Afficher les codes de récupération**.

1. Saisissez le **[!UICONTROL Verification Code]** envoyé à votre email et sélectionnez **[!UICONTROL Verify Code]** pour continuer.

   ![Entrer le code de vérification](./assets/2fA-verification-code-prompt.png){width="400"}

1. Enregistrez les **codes de récupération** présentés dans un endroit sûr et accessible.

   Si vous ne pouvez pas fournir de code de vérification pour vous connecter à votre compte [!DNL Commerce], l’utilisation d’un code de récupération est le seul moyen de récupérer l’accès au compte.

   Chaque code de récupération est utilisé une seule fois, mais vous pouvez toujours [générer](#generate-new-recovery-codes) de nouveaux codes. Les codes de récupération respectent la casse.

   ![Afficher les codes de récupération](./assets/2fa-view-recovery.png){width="400"}

1. Cochez la case de confirmation et sélectionnez **[!UICONTROL Submit]** pour fermer la boîte de dialogue.

## Générer de nouveaux codes de récupération

1. Accédez au [!DNL Commerce] [compte login][1]{:target=&quot;_blank&quot;}.

1. Saisissez votre nom d’utilisateur et votre mot de passe, puis sélectionnez **[!UICONTROL Login]**.

1. Procédez à la connexion à l’aide de l’une des méthodes d’authentification à deux facteurs décrites précédemment.

1. Dans le volet de navigation de gauche, sélectionnez **[!UICONTROL Account Settings]**, puis **[!UICONTROL Two-factor Authentication]**.

1. Pour générer de nouveaux codes de récupération prégénérés, sélectionnez **Générer de nouveaux codes de récupération**.

1. Saisissez le **[!UICONTROL Verification Code]** envoyé à votre email et sélectionnez **[!UICONTROL Verify Code]** pour continuer.

1. Enregistrez les **codes de récupération** présentés dans un endroit sûr et accessible.

   Si vous ne pouvez pas fournir de code de vérification lorsque vous vous connectez à votre compte [!DNL Commerce], l’utilisation d’un code de récupération est le seul moyen de récupérer l’accès au compte.

   Tous les codes de récupération générés précédemment sont désormais rendus non valides et doivent être ignorés (seul l’ensemble actuel de codes de récupération générés est fonctionnel). Les codes de récupération respectent la casse.

1. Cochez la case de confirmation et sélectionnez **[!UICONTROL Submit]** pour fermer la boîte de dialogue.

## Modification de l’email de récupération

1. Accédez au [!DNL Commerce] [compte login][1]{:target=&quot;_blank&quot;}.

1. Saisissez votre nom d’utilisateur et votre mot de passe, puis sélectionnez **[!UICONTROL Login]**.

1. Procédez à la connexion à l’aide de l’une des méthodes d’authentification à deux facteurs décrites précédemment.

1. Dans le volet de navigation de gauche, sélectionnez **[!UICONTROL Account Settings]**, puis **[!UICONTROL Two-factor Authentication]**.

1. Sélectionnez **Modifier l’e-mail de récupération** pour modifier l’e-mail de récupération dans le fichier de votre compte.

1. Saisissez le **[!UICONTROL Verification Code]** envoyé à votre email et sélectionnez **[!UICONTROL Verify Code]** pour continuer.

1. Pour vous assurer que vous pouvez récupérer l’accès à votre compte, saisissez un **email de récupération**.

   Cette adresse électronique est nécessaire si vous ne pouvez pas générer de code de vérification à partir de votre application d’authentification à deux facteurs et que vous n’avez pas accès à un code de récupération prégénéré inutilisé.

   Une fois toutes les 24 heures, vous pouvez générer et envoyer un code de récupération temporaire à votre adresse électronique de récupération désignée. Vous pouvez utiliser ce code pour récupérer l’accès au compte.

   >[!IMPORTANT]
   >
   >Maintenez l’accès à votre compte de messagerie de récupération. Sinon, vous ne pouvez pas utiliser les codes de récupération temporaires envoyés à ce compte.

1. Cochez la case de confirmation et sélectionnez **[!UICONTROL Submit]** pour fermer la boîte de dialogue.

   Le système envoie une notification par courrier électronique à l’adresse électronique de récupération que vous avez désignée pour confirmer que cette adresse électronique spécifique figure dans le fichier en tant qu’adresse électronique de récupération pour réception des codes de récupération temporaires.

## Modification de votre application d’authentification à deux facteurs

1. Accédez au [!DNL Commerce] [compte login][1]{:target=&quot;_blank&quot;}.

1. Saisissez votre nom d’utilisateur et votre mot de passe, puis sélectionnez **[!UICONTROL Login]**.

1. Procédez à la connexion à l’aide de l’une des méthodes d’authentification à deux facteurs décrites précédemment.

1. Dans le volet de navigation de gauche, sélectionnez **[!UICONTROL Account Settings]**, puis **[!UICONTROL Two-factor Authentication]**.

1. Sélectionnez **Modifier l’application TFA** pour utiliser une autre application TFA avec votre compte magento.com.

1. Saisissez le **[!UICONTROL Verification Code]** envoyé à votre email et sélectionnez **[!UICONTROL Verify Code]** pour continuer.

1. Ouvrez l’application d’authentification à deux facteurs sur votre périphérique personnel.

1. Saisissez le **code de configuration** dans votre application d’authentification à deux facteurs.

   Vous pouvez ajouter le code en analysant le code QR à l’aide de l’application TFA ou en le saisissant manuellement. Ce code associe votre application TFA à votre compte [!DNL Commerce] et permet aux autorisations de l’application TFA de générer des codes de vérification pour un accès sécurisé au compte.

   >[!NOTE]
   >
   >Pour des raisons de sécurité, les codes de vérification de votre application TFA expirent et se régénèrent en permanence. **_Toujours_** utilisez le code actuellement affiché.

1. Maintenant que votre application TFA est associée à votre compte [!DNL Commerce], saisissez le **[!UICONTROL Verification Code]** affiché dans votre application TFA et sélectionnez **[!UICONTROL Verify Code]** pour continuer.

1. Enregistrez les **codes de récupération** présentés dans un endroit sûr et accessible.

   Si vous ne pouvez pas fournir de code de vérification lorsque vous vous connectez à votre compte [!DNL Commerce], le seul moyen de récupérer l’accès au compte est d’utiliser un code de récupération.

   Chaque code de récupération est utilisé une seule fois, mais vous pouvez toujours [générer](#generate-new-recovery-codes) de nouveaux codes. Les codes de récupération respectent la casse. Les codes de récupération respectent la casse.

1. Cochez la case pour confirmer et sélectionnez **[!UICONTROL Submit]** pour continuer.

1. Pour vous assurer que vous pouvez récupérer l’accès à votre compte, saisissez un **email de récupération**.

   Cette adresse électronique est nécessaire si vous ne pouvez pas générer de code de vérification à partir de votre application d’authentification à deux facteurs et que vous n’avez pas accès à un code de récupération prégénéré inutilisé.

   Une fois toutes les 24 heures, vous pouvez générer et envoyer un code de récupération temporaire à votre adresse électronique de récupération désignée. Utilisez ce code pour récupérer l’accès au compte.

   >[!IMPORTANT]
   >
   >Maintenez l’accès à votre compte de messagerie de récupération. Sinon, vous ne pouvez pas utiliser les codes de récupération temporaires envoyés à ce compte.

1. Cochez la case de confirmation et sélectionnez **[!UICONTROL Submit]** pour terminer le processus de configuration de l’authentification à deux facteurs.

   Une notification électronique est envoyée à l’adresse électronique de récupération que vous avez désignée pour confirmer que cette adresse électronique spécifique figure dans le fichier en tant qu’adresse électronique de récupération pour réception d’un code de récupération temporaire.

## Désactivation de l’authentification à deux facteurs

>[!IMPORTANT]
>
>Si votre stratégie de sécurité organisationnelle nécessite une authentification à plusieurs facteurs sur les comptes Adobe Commerce, vous ne pouvez pas désactiver l’authentification à deux facteurs.

1. Accédez au [!DNL Commerce] [compte login][1]{:target=&quot;_blank&quot;}.

1. Saisissez votre nom d’utilisateur et votre mot de passe, puis sélectionnez **[!UICONTROL Login]**.

1. Procédez à la connexion à l’aide de l’une des méthodes d’authentification à deux facteurs décrites précédemment.

1. Dans le volet de navigation de gauche, sélectionnez **[!UICONTROL Account Settings]** et **[!UICONTROL Two-factor Authentication]** sous .

1. Sélectionnez **[!UICONTROL Disable]** pour lancer le processus de désactivation TFA.

1. Saisissez le **[!UICONTROL Verification Code]** envoyé à votre email et sélectionnez **[!UICONTROL Verify Code]** pour continuer.

1. Cochez la case de confirmation et sélectionnez **[!UICONTROL Submit]** pour terminer la désactivation de l’authentification à deux facteurs.

   Le système envoie une confirmation par courrier électronique indiquant que TFA a été désactivé sur votre compte [!DNL Commerce].

   ![Désactiver TFA](./assets/2fa-disable.png){width="400"}

[1]: https://account.magento.com/customer/account/login
