---
title: Gestion des comptes utilisateur d’administration
description: Découvrez comment créer des comptes utilisateur d’administration et affecter des rôles pour accorder des autorisations aux fonctions d’administration.
exl-id: 65cca7a8-3d44-4c8c-a758-c0de03d53e11
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
source-git-commit: ad75c77ada34c4d66b1a58a666edadd44d054e17
workflow-type: tm+mt
source-wordcount: '1012'
ht-degree: 0%

---

# Gestion des comptes utilisateur d’administration

Lors de la première installation de votre boutique, un compte administrateur par défaut est créé avec les informations de connexion qui vous donnent un accès administratif complet. Il est recommandé de créer un autre compte utilisateur disposant d’un accès administrateur complet. De cette façon, vous pouvez utiliser un compte pour vos activités administratives quotidiennes et réserver l’autre en tant que compte « Super administrateur ». Cela peut s’avérer utile si vous oubliez vos informations d’identification standard ou si elles deviennent inutilisables.

Si d’autres membres de l’équipe ou fournisseurs de services ont besoin d’un accès, vous pouvez créer des comptes d’utilisateurs individuels pour eux et leur attribuer un accès restreint en fonction de leurs besoins professionnels spécifiques. Pour limiter les sites web ou les magasins auxquels les utilisateurs peuvent accéder dans l’administration, vous devez d’abord [créer un rôle](permissions-user-roles.md) avec une portée limitée et en sélectionnant uniquement les ressources nécessaires. Vous pouvez ensuite affecter le rôle à un compte utilisateur spécifique. Les utilisateurs administrateurs affectés à un rôle restreint peuvent afficher et modifier les données uniquement pour les sites web ou magasins associés au rôle, mais ne peuvent pas modifier les données ou paramètres globaux.

>[!NOTE]
>
>Les commerçants Adobe Commerce qui disposent d’une Adobe ID et souhaitent une connexion rationalisée aux produits Adobe Commerce et Adobe Business peuvent intégrer l’authentification Commerce au workflow d’authentification Adobe IMS. Une fois cette intégration activée pour votre boutique Commerce, chaque utilisateur administrateur doit utiliser ses informations d’identification Adobe, et non ses informations d’identification Commerce, pour se connecter. Voir [Présentation de l’intégration du service Adobe Identity Management (IMS)](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html?lang=fr).

Pour les utilisateurs et utilisatrices ou les rôles temporaires, vous pouvez également définir une date d’expiration pour le compte utilisateur.

<!--  update this to a better info-graphic ![User types for your Admin](./assets/merchant-admin-users.png) -->

## Création d’un utilisateur

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New User]**.

   Pour modifier un utilisateur existant, cliquez sur un nom d’utilisateur dans la grille. Vous pouvez modifier les sections _[!UICONTROL User Info]_&#x200B;et&#x200B;_[!UICONTROL User Role]_ selon vos besoins.

1. Dans la section _[!UICONTROL Account Information]_, procédez comme suit :

   ![Informations sur le compte utilisateur](./assets/permissions-user-new.png){width="600" zoomable="yes"}

   - Saisissez le **[!UICONTROL User Name]** du compte .

     Le nom d’utilisateur doit être facile à mémoriser. Elle n’est pas sensible à la casse. Par exemple, si le nom d’utilisateur est `John`, il peut également se connecter en tant que `john`.

   - Renseignez les informations suivantes :

      - **[!UICONTROL First Name]**
      - **[!UICONTROL Last Name]**
      - **[!UICONTROL Email address]**

     Chaque compte utilisateur doit avoir une adresse e-mail unique.

   - Saisissez un **[!UICONTROL Password]** pour le compte.

     >[!NOTE]
     >
     >Un mot de passe administrateur doit comporter au moins sept caractères et inclure des lettres et des chiffres. Pour obtenir des options de mot de passe supplémentaires, voir [Configuration d’Admin Security](security-admin.md).

   - Par **[!UICONTROL Password Confirmation]**, saisissez à nouveau le mot de passe pour vous assurer qu’il a été saisi correctement.

   - Si votre magasin comporte plusieurs langues, définissez **[!UICONTROL Interface Locale]** sur la langue à utiliser pour l’interface d’administration.

1. Définissez **[!UICONTROL This Account is]** sur `Active`.

1. Cliquez sur l’icône de calendrier pour définir la **[!UICONTROL Expiration Date]** du compte d’utilisateur.

   La définition d’une date d’expiration est utile lorsqu’un utilisateur ou un rôle est temporaire. Après la date d’expiration, le statut du compte d’utilisateur passe à `Inactive` et peut être mis à jour si nécessaire.

1. Sous _[!UICONTROL Current User Identity Verification]_, saisissez le mot de passe de votre compte utilisateur.

>[!IMPORTANT]
>
>Une fois la section _[!UICONTROL Account Information]_&#x200B;terminée, vous pouvez enregistrer l’utilisateur. Le nouvel utilisateur s’affiche dans la grille de&#x200B;_[!UICONTROL Users]_, mais le nom d’utilisateur ne peut pas se connecter tant qu’un rôle n’a pas été attribué.

## Attribuer un rôle d’utilisateur

1. Dans le panneau de gauche, cliquez sur **[!UICONTROL User Role]**.

   La grille répertorie tous les rôles utilisateur existants. Pour un nouveau magasin, _[!UICONTROL Administrators]_&#x200B;est le seul rôle disponible.

   ![Admin - add new user role](./assets/permissions-user-roles.png){width="600" zoomable="yes"}

1. Dans la colonne _[!UICONTROL Assigned]_, sélectionnez un rôle d’utilisateur.

   Vous pouvez [afficher les rôles utilisateur existants ou en définir d’autres](permissions-user-roles.md). Une fois le rôle défini, vous devez modifier le compte utilisateur pour affecter le nouveau rôle.

## Vérifier ou réinitialiser les fournisseurs 2FA

1. Ouvrez le compte utilisateur d’administration .

1. Dans le panneau de gauche, cliquez sur **[!UICONTROL 2FA]**.

   ![Admin - add new user role](./assets/permissions-user-2fa.png){width="600" zoomable="yes"}

1. Vérifiez les solutions 2FA disponibles pour les utilisateurs _Admin_ et conseillez à chaque utilisateur d’installer les solutions qu’il souhaite utiliser avant de se connecter.

   L’authentification par une seule solution 2FA est nécessaire pour se connecter à l’_Admin_.

1. Si l’utilisateur doit réinstaller la solution 2FA, vous pouvez réinitialiser la configuration 2FA actuelle.

   Pour ce faire, l’utilisateur doit répéter le processus de configuration avant de pouvoir se reconnecter. Par exemple, l’utilisateur ou l’utilisatrice peut disposer d’un nouveau téléphone intelligent et doit réinstaller l’authentificateur Google. Pour effacer la configuration 2FA actuelle de l’utilisateur, cliquez sur **[!UICONTROL Reset (Provider)]** pour chaque solution à effacer. Lorsque vous y êtes invité, cliquez sur **[!UICONTROL OK]** pour confirmer.

   L’utilisateur reçoit un courrier électronique contenant un lien [configurer 2FA](security-two-factor-authentication.md). Le lien ne peut être utilisé qu’une seule fois. Si l’utilisateur ou l’utilisatrice tente de se connecter plusieurs fois, un nouveau lien est envoyé après chaque tentative.

1. Cliquez sur **[!UICONTROL Save User]**.

1. Lorsque vous y êtes invité, saisissez votre mot de passe pour confirmer votre identité, puis cliquez de nouveau sur **[!UICONTROL Save User]**.

   La grille de _[!UICONTROL Users]_&#x200B;s’ouvre et répertorie tous les utilisateurs.

## Suppression d’un utilisateur administrateur

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Recherchez le compte utilisateur à l’aide de filtres au-dessus de la grille et cliquez sur le nom d’utilisateur.

1. Lorsque vous y êtes invité, saisissez votre mot de passe pour confirmer votre identité.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Delete User]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

## Mot de passe oublié et e-mails de réinitialisation

La configuration du modèle d’e-mail d’administrateur détermine les e-mails envoyés lorsque les utilisateurs oublient et réinitialisent leurs mots de passe. Cette configuration spécifie le contact du magasin qui apparaît comme expéditeur du message et la durée pendant laquelle le lien de récupération du mot de passe reste valide.

**_Pour configurer les modèles d’e-mail d’administration, procédez comme suit_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Setting]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Admin]**.

1. Développez ![bouton bascule d’extension](../assets/icon-display-expand.png) dans la section **[!UICONTROL Admin User Emails]** .

   ![Configuration avancée - Paramètres du modèle d’e-mail d’administration](../configuration-reference/advanced/assets/admin-admin-user-emails.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Forgot Password Email Template]** sur le modèle envoyé lorsqu’un utilisateur administrateur oublie ses mots de passe.

1. Définissez **[!UICONTROL Forgot and Reset Email Sender]** sur le contact du magasin qui apparaît comme l’expéditeur du message.

1. Définissez **[!UICONTROL User Notification Template]** sur le modèle d’e-mail utilisé par défaut pour les notifications des administrateurs.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Utilisateurs verrouillés

Pour la sécurité de votre entreprise, les comptes utilisateur sont verrouillés par défaut après six tentatives infructueuses de [connexion](../getting-started/admin-signin.md) à l’administrateur. Tout compte utilisateur actuellement verrouillé s’affiche dans la grille Utilisateurs verrouillés . Un compte peut être déverrouillé par tout autre utilisateur disposant des autorisations Administrateur complètes.

Des mesures de sécurité de mot de passe supplémentaires peuvent être mises en œuvre dans la configuration [Administration avancée](../configuration-reference/advanced/admin.md#security). Voir [Admin Security](security-admin.md).

![Alerte écran de connexion - Le compte est temporairement désactivé](./assets/admin-login-locked-out-message.png){width="300"}

**_Pour déverrouiller un compte d’administrateur, procédez comme suit_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL Locked Users]**.

1. Dans la grille, cochez la case du compte verrouillé.

   ![Autorisations - comptes utilisateur verrouillés](./assets/permissions-locked-users-grid.png){width="600" zoomable="yes"}

1. Dans le coin supérieur gauche, définissez **[!UICONTROL Actions]** sur `Unlock`.

1. Cliquez sur **[!UICONTROL Submit]** pour déverrouiller le compte.
