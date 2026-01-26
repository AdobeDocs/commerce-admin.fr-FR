---
title: Votre compte utilisateur d’administrateur
description: Découvrez votre compte d’administrateur et comment utiliser l’authentification à deux facteurs pour vous connecter à l’administrateur.
exl-id: ad576533-5914-49d1-8e73-3f59c55543a5
feature: Admin Workspace, User Account
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 0%

---

# Votre compte d’administrateur

Le compte administrateur principal a été initialement configuré lors de l’installation et peut contenir des informations initiales d’espace réservé ou des informations d’exemples de données. Le propriétaire désigné de ce compte peut personnaliser le nom d’utilisateur et le mot de passe et mettre à jour le prénom, le nom et l’adresse e-mail à tout moment. Ce compte, un _super utilisateur_ avec toutes les autorisations par défaut, crée généralement les comptes utilisateur d’administration nécessaires à l’entreprise.

- Voir [Créer un utilisateur](../systems/permissions-users-all.md#create-a-user) pour plus d’informations sur l’ajout ou la modification d’utilisateurs.

- Voir [Autorisations](../systems/permissions.md) et [Rôles utilisateur](../systems/permissions-user-roles.md) pour plus d’informations sur les rôles administrateur et utilisateur.

{{ims-admin-note}}

## Connexion administrateur

Le [!DNL Commerce] _Admin_ est protégé par plusieurs couches de mesures de sécurité pour empêcher tout accès non autorisé à vos données de magasin, de commande et de client. La première fois que vous vous connectez à l’_Admin_, vous devez saisir votre nom d’utilisateur et votre mot de passe et configurer l’[authentification à deux facteurs](../systems/security-two-factor-authentication.md) (2FA).

Selon la configuration de votre boutique, il peut y avoir un défi [CAPTCHA](../systems/security-google-recaptcha.md) à résoudre, comme saisir une série de caractères au clavier, résoudre un puzzle ou cliquer sur une série d’images avec un thème commun. Ces tests sont conçus pour vous identifier en tant qu’humain, plutôt qu’en tant que robot automatisé.

Pour plus de sécurité, vous pouvez déterminer les parties du _Administrateur_ auxquelles chaque utilisateur a [autorisation](../systems/permissions.md) d’accéder et également limiter le nombre [ tentatives de connexion](../configuration-reference/advanced/admin.md). Par défaut, après six tentatives, le compte est verrouillé et l’utilisateur ou l’utilisatrice doit attendre quelques minutes avant de réessayer. [Comptes verrouillés](../systems/permissions-users-all.md#locked-users) peuvent également être réinitialisés à partir de l’_Admin_.

>[!NOTE]
>
>La première fois que vous vous connectez à l’_Admin_, vous êtes invité à _Autoriser la collecte de données d’utilisation par l’administrateur_. Voir [Collecte de données d’utilisation](admin.md#usage-data-collection) pour plus d’informations.

![Connexion administrateur](./assets/admin-login.png){width="400"}

### Étape 1 : configurer l’authentification à deux facteurs

Avant de pouvoir vous connecter à l’_Admin_ de votre boutique, vous devez disposer d’une solution d’authentification à deux facteurs configurée et prête à l’emploi. Pour en savoir plus sur le processus d’authentification utilisé par chaque solution, voir [Utilisation de l’authentification à deux facteurs](../systems/security-two-factor-authentication-use.md). Par défaut, [!DNL Commerce] prend en charge [Google Authenticator](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&hl=en_US).

Demandez à votre administrateur système [!DNL Commerce] quelles solutions 2FA sont prises en charge pour le magasin. Ensuite, effectuez la configuration de votre solution 2FA préférée conformément aux instructions du fournisseur.

### Étape 2 : Se connecter à l’administrateur

1. Saisissez l’URL _Admin_ spécifiée lors de l’installation du [!DNL Commerce].

   L’URL _Admin_ par défaut ressemble à `https://www.yourdomain.com/your-custom-admin-domain`.

   >[!NOTE]
   >
   >Bien que cette documentation utilise `admin` comme URL de base dans la plupart des exemples, il est recommandé de choisir une URL [personnalisée](../stores-purchase/store-urls.md) unique et difficile à deviner, pour l’_administrateur_ de votre boutique.

   Vous pouvez ajouter un signet pour la page ou enregistrer un raccourci sur votre bureau pour un accès plus facile.

1. Saisissez votre _et votre_ **[!UICONTROL Username]** Admin **[!UICONTROL Password]**.

1. (Facultatif) Si un CAPTCHA est activé pour votre boutique, suivez les instructions à l’écran pour résoudre le problème.

   Pour en savoir plus, voir [CAPTCHA](../systems/security-captcha.md) et [reCAPTCHA](../systems/security-google-recaptcha.md).

1. Cliquez sur **[!UICONTROL Sign in]**.

   Si c’est la première fois que vous vous connectez au compte _Admin_ à partir du compte , vous devriez recevoir un e-mail avec un lien vers les instructions de configuration.

### Étape 3 : terminer la configuration 2FA

L’exemple suivant montre comment associer votre compte _Admin_ à l’authentificateur Google.

1. Lorsque le code QR apparaît, utilisez l’une des méthodes suivantes pour capturer le code et associer l’authentificateur Google à votre compte _Admin_.

   ![Configurer l’authentificateur Google](./assets/admin-login-google-auth-setup.png){width="400"}

   - Capturer le code QR à l’aide d’un téléphone intelligent

     Sur votre téléphone intelligent, lancez l’authentificateur Google. Appuyez sur le _signe plus_ (+) dans le coin supérieur droit de l’application. Ensuite, au bas de l’écran, appuyez sur **[!UICONTROL Scan Barcode]** et prenez une photo du code QR.

   - Capturer le code QR à partir du navigateur

     Si Google Authenticator est installé en tant qu’extension dans votre navigateur, cliquez sur l’icône **Authenticator** de la barre d’outils et capturez la page.

   - Saisir manuellement le code QR

     Copiez la chaîne de texte sous le code QR. Lancez l’authentificateur Google à l’aide de votre téléphone intelligent ou de votre navigateur, puis cliquez sur le signe plus (+). Choisissez ensuite **[!UICONTROL Manual Entry]**. Sous **[!UICONTROL Account]**, saisissez l’adresse e-mail associée à votre compte _Admin_ et collez la chaîne de code QR dans le champ **[!UICONTROL Key]** .

1. Pour vous connecter à l’_Admin_ avec l’authentification à deux facteurs, saisissez le code à six chiffres généré par l’authentificateur Google dans le champ **[!UICONTROL Authenticator code]**, puis cliquez sur **[!UICONTROL Confirm]**.

   ![Saisissez le code d’authentification](./assets/admin-login-2fa-google.png){width="400"}

## Réinitialiser votre mot de passe

La réutilisation des quatre derniers mots de passe attribués au compte n’est pas autorisée.

1. Saisissez le **[!UICONTROL Email Address]** associé au compte _Admin_.

   ![ Mot de passe oublié ](./assets/admin-sign-in-forgot-password.png){width="400"}

1. Cliquez sur **[!UICONTROL Retrieve Password]**.

   Si un compte est associé à l’adresse e-mail, un e-mail est envoyé pour réinitialiser votre mot de passe.

   >[!NOTE]
   >
   >Un mot de passe _Admin_ doit comporter au moins sept caractères, des lettres et des chiffres. Voir [Configuration d’_Admin_ Security](../systems/security-admin.md) pour plus d’informations sur les options de mot de passe.

## Déconnectez-vous de l’administrateur

1. Dans le coin supérieur droit, cliquez sur l’icône _Compte_ (![Compte](../assets/icon-admin-user.png)).

1. Cliquez sur **[!UICONTROL Sign Out]**.

   ![Se déconnecter](./assets/admin-sign-out.png){width="700" zoomable="yes"}

La page _[!UICONTROL Sign In]_affiche un message indiquant que vous êtes déconnecté. Déconnectez-vous du_ Administrateur _chaque fois que vous laissez votre ordinateur sans surveillance.

## Modifier les informations du compte

1. Cliquez sur l’icône _Compte_ (![Icône de compte](../assets/icon-admin-user.png)).

1. Cliquez sur **[!UICONTROL Account Setting]**.

   ![Informations sur le compte](./assets/admin-account-information.png){width="700" zoomable="yes"}

1. Apportez les modifications nécessaires aux informations de votre compte.

   Si vous modifiez vos identifiants de connexion, veillez à les stocker dans un emplacement sécurisé.

1. Entrez votre mot de passe de compte actuel.

1. Cliquez sur **[!UICONTROL Save Account]**.

## Autoriser plusieurs connexions d’administrateur

Admin permet d’accéder à la gestion des fonctionnalités de commandes, de clients, de produits, d’expédition et de paiements. La configuration par défaut est définie pour interdire les connexions multiples pour un compte utilisateur administrateur en tant que bonne pratique en matière de sécurité. Cependant, vous pouvez modifier ce paramètre pour permettre aux utilisateurs administrateurs d’être connectés à partir de plusieurs appareils afin de s’adapter à vos workflows d’entreprise.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de navigation de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Admin]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Security]** .

1. Pour **Partage de compte d’administrateur**, sélectionnez `Yes`.

   ![Autoriser le partage de compte d’administrateur](./assets/multiple-admin-login.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Config]**.

## Définissez les noms de connexion des utilisateurs administrateurs en respectant la casse

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de navigation de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Admin]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Security]** .

1. Définissez le champ **[!UICONTROL Login is Case Sensitive]** sur `Yes`.

1. Cliquez sur **[!UICONTROL Save Config]**.


## Conserver un accès sécurisé à l’administrateur

Pour assurer la sécurité de votre administrateur, effectuez des audits réguliers des utilisateurs et des rôles disposant d’un accès administrateur.

En outre, pensez à [mettre à jour la configuration de l’URL de base d’administration](https://experienceleague.adobe.com/en/docs/commerce-admin/config/advanced/admin#admin-base-url) pour remplacer le point d’entrée de `/admin` par défaut par un chemin d’accès personnalisé. La configuration d’un chemin personnalisé offre les avantages de sécurité suivants :

**Sécurité renforcée** : le chemin d’accès « admin » par défaut est largement connu et souvent ciblé par des acteurs malveillants qui tentent des attaques par force brute. En la modifiant à une valeur personnalisée unique, vous réduisez considérablement le risque de tentatives d’accès non autorisées.

**Vulnérabilité réduite** : les robots automatisés recherchent fréquemment des chemins d’accès courants tels que « admin » pour exploiter les vulnérabilités. Un chemin personnalisé rend plus difficile, pour ces robots, la localisation de votre page de connexion d’administrateur, réduisant ainsi la probabilité d’attaques.

**Confidentialité améliorée** : un chemin d’administration personnalisé ajoute une couche d’obscurité supplémentaire, ce qui rend plus difficile, pour les attaquant potentiels, l’identification et le ciblage de votre page de connexion d’administrateur.

**Conformité aux bonnes pratiques** : le respect des bonnes pratiques de sécurité, telles que la personnalisation du chemin d’accès de l’administrateur, illustre une approche proactive de la protection de votre site d’e-commerce et des données des clients.

>[!NOTE]
>
>Si une violation est suspectée, veillez à supprimer tous les utilisateurs administrateurs inconnus, à réinitialiser tous les mots de passe administrateur et à consulter le [plan d’action de sécurité](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security) pour d’autres étapes.
