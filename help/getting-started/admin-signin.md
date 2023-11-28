---
title: Votre compte utilisateur administrateur
description: Découvrez votre compte d’administrateur et comment utiliser l’authentification à deux facteurs pour vous connecter à l’administrateur.
exl-id: ad576533-5914-49d1-8e73-3f59c55543a5
feature: Admin Workspace, User Account
source-git-commit: fff3464c9da50927bbe9773a17b0f6858360d788
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 0%

---

# Votre compte administrateur

Le compte administrateur principal a été initialement configuré pendant l’installation et peut contenir des informations initiales sur l’espace réservé ou des exemples de données. Le propriétaire désigné de ce compte peut personnaliser le nom d’utilisateur et le mot de passe et mettre à jour le prénom, le nom et l’adresse électronique à tout moment. Ce compte, une _super-utilisateur_ avec toutes les autorisations par défaut, crée généralement les comptes d’utilisateurs administrateurs nécessaires à l’entreprise.

- Voir [Création d’un utilisateur](../systems/permissions-users-all.md#create-a-user) pour plus d’informations sur l’ajout ou la modification d’utilisateurs.

- Voir [Autorisations](../systems/permissions.md) et [Rôles utilisateur](../systems/permissions-user-roles.md) pour plus d’informations sur les rôles administrateur et utilisateur.

{{ims-admin-note}}

## Connexion d’administrateur

La variable [!DNL Commerce] _Administration_ est protégé par plusieurs couches de mesures de sécurité afin d’empêcher tout accès non autorisé aux données de votre boutique, de vos commandes et de vos clients. La première fois que vous vous connectez au _Administration_, vous devez saisir votre nom d’utilisateur et votre mot de passe et configurer la variable [authentification à deux facteurs](../systems/security-two-factor-authentication.md) (2FA).

Selon la configuration de votre boutique, une [CAPTCHA](../systems/security-google-recaptcha.md) difficulté à résoudre, par exemple la saisie d’une série de caractères de clavier, la résolution d’un puzzle ou le clic sur une série d’images avec un thème commun. Ces tests sont conçus pour vous identifier en tant qu’humain, plutôt qu’en tant que robot automatisé.

Pour plus de sécurité, vous pouvez déterminer les parties de la variable _Administration_ chaque utilisateur possède [autorisation](../systems/permissions.md) pour accéder à et limiter également le nombre de [tentatives de connexion](../configuration-reference/advanced/admin.md). Par défaut, après six tentatives, le compte est verrouillé et l’utilisateur doit attendre quelques minutes avant de réessayer. [Comptes verrouillés](../systems/permissions-users-all.md#locked-users) peut également être réinitialisé à partir de la fonction _Administration_.

>[!NOTE]
>
>La première fois que vous vous connectez au _Administration_, vous êtes invité à _Autorisation de la collecte des données d’utilisation des administrateurs_. Voir [Collecte de données d’utilisation](admin.md#usage-data-collection) pour plus d’informations.

![Connexion de l’administrateur](./assets/admin-login.png){width="400"}

### Étape 1 : configuration de l’authentification à deux facteurs

Avant de vous connecter au _Administration_ de votre boutique, vous devez disposer d’une solution d’authentification à deux facteurs configurée et prête à l’emploi. Pour en savoir plus sur le processus d’authentification utilisé par chaque solution, voir [Utilisation de l’authentification à deux facteurs](../systems/security-two-factor-authentication-use.md). Par défaut, [!DNL Commerce] prend [Authentificateur Google][1].

Demandez à votre [!DNL Commerce] administrateur système qui prend en charge les solutions 2FA pour le magasin. Ensuite, effectuez la configuration de votre solution 2FA préférée en fonction des instructions du fournisseur.

### Étape 2 : connexion à l’administrateur

1. Saisissez le _Administration_ URL spécifiée lors de la [!DNL Commerce] installation.

   Par défaut _Administration_ L’URL ressemble à `https://www.yourdomain.com/your-custom-admin-domain`.

   >[!NOTE]
   >
   >Cette documentation utilise `admin` comme URL de base dans la plupart des exemples, il est recommandé de choisir un fichier unique et difficile à deviner. [URL personnalisée](../stores-purchase/store-urls.md) pour le _Administration_ de votre magasin.

   Vous pouvez ajouter un signet pour la page ou enregistrer un raccourci sur votre bureau pour un accès facile.

1. Saisissez votre _Administration_ **[!UICONTROL Username]** et **[!UICONTROL Password]**.

1. (Facultatif) Si un CAPTCHA est activé pour votre magasin, suivez les instructions à l’écran pour résoudre le problème.

   Pour en savoir plus, voir [CAPTCHA](../systems/security-captcha.md) et [reCAPTCHA](../systems/security-google-recaptcha.md).

1. Cliquez sur **[!UICONTROL Sign in]**.

   S’il s’agit de la première fois que vous vous connectez à la variable _Administration_ à partir du compte , vous devriez recevoir un courrier électronique contenant un lien vers les instructions de configuration.

### Étape 3 : achèvement de la configuration 2FA

L’exemple suivant montre comment associer vos _Administration_ compte avec l’authentificateur Google.

1. Lorsque le code QR apparaît, utilisez l’une des méthodes suivantes pour capturer le code et associer l’authentificateur Google à votre _Administration_ compte .

   ![Configuration de l’authentificateur Google](./assets/admin-login-google-auth-setup.png){width="400"}

   - Capture du code QR à l’aide d’un smartphone

     Sur votre smartphone, lancez l’authentificateur Google. Appuyez sur le bouton _symbole plus_ (+) dans le coin supérieur droit de l’application. Ensuite, au bas de l’écran, appuyez sur **[!UICONTROL Scan Barcode]** et prenez une photo du code QR.

   - Capture du code QR à partir du navigateur

     Si l’authentificateur Google est installé en tant qu’extension dans votre navigateur, cliquez sur le bouton **Authentificateur** dans la barre d’outils, puis capturez la page.

   - Saisie manuelle du code QR

     Copiez la chaîne de texte sous le code QR. Lancez l’authentificateur Google avec votre smartphone ou navigateur, puis cliquez sur le signe plus (+). Sélectionnez ensuite **[!UICONTROL Manual Entry]**. Sous **[!UICONTROL Account]**, saisissez l’adresse électronique associée à votre _Administration_ et collez la chaîne de code QR dans la variable **[!UICONTROL Key]** champ .

1. Pour vous connecter au _Administration_ avec une authentification à deux facteurs, saisissez le code à six chiffres généré par l’authentificateur Google dans la variable **[!UICONTROL Authenticator code]** puis cliquez sur **[!UICONTROL Confirm]**.

   ![Saisissez le code de l’authentificateur.](./assets/admin-login-2fa-google.png){width="400"}

## Réinitialisation de votre mot de passe

La réutilisation des quatre derniers mots de passe affectés au compte n’est pas autorisée.

1. Saisissez le **[!UICONTROL Email Address]** qui est associé à la variable _Administration_ compte .

   ![Mot de passe oublié](./assets/admin-sign-in-forgot-password.png){width="400"}

1. Cliquez sur **[!UICONTROL Retrieve Password]**.

   Si un compte est associé à l’adresse électronique, un courrier électronique est envoyé pour réinitialiser votre mot de passe.

   >[!NOTE]
   >
   >Un _Administration_ le mot de passe doit comporter au moins sept caractères et contenir à la fois des lettres et des chiffres. Voir [Configuration _Administration_ Sécurité](../systems/security-admin.md) pour plus d’informations sur les options de mot de passe.

## Déconnexion de l’administrateur

1. Dans le coin supérieur droit, cliquez sur le bouton _Compte_ (![Compte](../assets/icon-admin-user.png)).

1. Cliquez sur **[!UICONTROL Sign Out]**.

   ![Se déconnecter](./assets/admin-sign-out.png){width="700" zoomable="yes"}

La variable _[!UICONTROL Sign In]_affiche un message indiquant que vous êtes déconnecté. Déconnectez-vous de_ Administration _chaque fois que vous laissez votre ordinateur sans surveillance.

## Modifier les informations du compte

1. Cliquez sur le bouton _Compte_ (![Icône Compte](../assets/icon-admin-user.png)).

1. Cliquez sur **[!UICONTROL Account Setting]**.

   ![Informations du compte](./assets/admin-account-information.png){width="700" zoomable="yes"}

1. Apportez les modifications nécessaires aux informations de votre compte.

   Si vous modifiez vos informations de connexion, assurez-vous de les stocker dans un emplacement sécurisé.

1. Saisissez le mot de passe de votre compte actuel.

1. Cliquez sur **[!UICONTROL Save Account]**.

## Autorisation de plusieurs connexions d’administrateur

L’administrateur permet de gérer les commandes, les clients, les produits, les frais d’expédition et les fonctionnalités de paiements. La configuration par défaut est définie pour interdire plusieurs connexions pour un compte d’utilisateur administrateur en tant que bonne pratique de sécurité. Cependant, vous pouvez modifier ce paramètre pour permettre aux utilisateurs administrateurs d’être connectés à partir de plusieurs appareils en fonction des workflows de votre entreprise.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de navigation de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Admin]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Security]** .

1. Pour **Partage des comptes d’administrateur**, sélectionnez `Yes`.

   ![Autorisation du partage des comptes d’administrateur](./assets/multiple-admin-login.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Config]**.

## Définir les noms de connexion des utilisateurs administrateurs en fonction de la casse

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de navigation de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Admin]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Security]** .

1. Définissez la variable **[!UICONTROL Login is Case Sensitive]** champ à `Yes`.

1. Cliquez sur **[!UICONTROL Save Config]**.

[1]: https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&amp;hl=en_US
