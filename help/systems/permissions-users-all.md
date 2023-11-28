---
title: Gestion des comptes d’utilisateurs administrateur
description: Découvrez comment créer des comptes d’utilisateurs administrateurs et affecter des rôles pour accorder des autorisations aux fonctions d’administration.
exl-id: 65cca7a8-3d44-4c8c-a758-c0de03d53e11
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# Gestion des comptes d’utilisateurs administrateur

Lorsque votre boutique est installée pour la première fois, un compte administrateur par défaut est créé avec les informations de connexion qui vous donnent un accès administrateur complet. Il est recommandé de créer un autre compte utilisateur avec un accès administrateur complet. Ainsi, vous pouvez utiliser un compte pour vos activités administratives quotidiennes et réserver l’autre comme compte &quot;Super administrateur&quot;. Cela peut s’avérer utile si vous oubliez vos informations d’identification normales, ou si elles deviennent d’une manière ou d’une autre inutilisables.

Si d’autres membres de votre équipe ou fournisseurs de services doivent y avoir accès, vous pouvez créer un compte d’utilisateur distinct pour chacun d’eux et attribuer un accès restreint en fonction des besoins de leur entreprise. Pour limiter les sites web ou les magasins auxquels les utilisateurs peuvent accéder dans l’administrateur, vous devez d’abord [créer un rôle](permissions-user-roles.md) avec une portée limitée et uniquement les ressources nécessaires sélectionnées. Vous pouvez ensuite affecter le rôle à un compte d’utilisateur spécifique. Les utilisateurs administrateurs affectés à un rôle restreint peuvent afficher et modifier des données uniquement pour les sites web ou les magasins associés au rôle, mais ne peuvent pas modifier de paramètres ou de données globaux.

>[!NOTE]
>
>Les marchands Adobe Commerce qui disposent d’un Adobe ID et souhaitent une connexion simplifiée à Adobe Commerce et aux produits d’entreprise Adobe peuvent intégrer l’authentification Commerce au workflow d’authentification Adobe IMS. Une fois cette intégration activée pour votre boutique Commerce, chaque utilisateur administrateur doit utiliser ses informations d’identification d’Adobe (et non ses informations d’identification Commerce) pour se connecter. Voir [Présentation de l’intégration d’Adobe Identity Management Service (IMS)](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

Pour les utilisateurs ou les rôles temporaires, vous pouvez également définir une date d’expiration pour le compte d’utilisateur.

<!--  update this to a better info-graphic ![User types for your Admin](./assets/merchant-admin-users.png) -->

## Création d’un utilisateur

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New User]**.

   Pour modifier un utilisateur existant, cliquez sur un nom d’utilisateur dans la grille. Vous pouvez modifier le _[!UICONTROL User Info]_et_[!UICONTROL User Role]_ le cas échéant.

1. Dans le _[!UICONTROL Account Information]_, procédez comme suit :

   ![Informations du compte utilisateur](./assets/permissions-user-new.png){width="600" zoomable="yes"}

   - Saisissez le **[!UICONTROL User Name]** pour compte.

     Le nom d’utilisateur doit être facile à mémoriser. Il n’est pas sensible à la casse. Par exemple, si le nom d’utilisateur est `John`, ils peuvent également se connecter en tant que `john`.

   - Renseignez les informations suivantes :

      - **[!UICONTROL First Name]**
      - **[!UICONTROL Last Name]**
      - **[!UICONTROL Email address]**

     Chaque compte utilisateur doit disposer d’une adresse électronique unique.

   - Saisissez un **[!UICONTROL Password]** pour le compte .

     >[!NOTE]
     >
     >Un mot de passe administrateur doit comporter au moins sept caractères et contenir à la fois des lettres et des chiffres. Pour accéder à d’autres options de mot de passe, voir [Configuration de la sécurité d’administration](security-admin.md).

   - Pour **[!UICONTROL Password Confirmation]**, saisissez à nouveau le mot de passe pour vous assurer qu’il a été correctement saisi.

   - Si votre boutique comporte plusieurs langues, définissez **[!UICONTROL Interface Locale]** dans la langue à utiliser pour l’interface d’administration.

1. Définir **[!UICONTROL This Account is]** to `Active`.

1. Cliquez sur l’icône de calendrier pour définir la variable **[!UICONTROL Expiration Date]** pour le compte utilisateur.

   La définition d’une date d’expiration s’avère utile lorsqu’un utilisateur ou un rôle est temporaire. Après la date d’expiration, l’état du compte utilisateur passe à `Inactive` et peuvent être mis à jour, si nécessaire.

1. Sous _[!UICONTROL Current User Identity Verification]_, saisissez le mot de passe de votre compte d’utilisateur.

>[!IMPORTANT]
>
>Avec la variable _[!UICONTROL Account Information]_, vous pouvez enregistrer l’utilisateur. Le nouvel utilisateur s’affiche dans la variable_[!UICONTROL Users]_ , mais le nom d’utilisateur ne peut pas se connecter tant qu’un rôle n’a pas été attribué.

## Attribution d’un rôle d’utilisateur

1. Dans le panneau de gauche, cliquez sur **[!UICONTROL User Role]**.

   La grille répertorie tous les rôles d’utilisateur existants. Pour un nouveau magasin, _[!UICONTROL Administrators]_est le seul rôle disponible.

   ![Administration - ajout d’un nouveau rôle d’utilisateur](./assets/permissions-user-roles.png){width="600" zoomable="yes"}

1. Dans le _[!UICONTROL Assigned]_, sélectionnez un rôle utilisateur.

   Vous pouvez [afficher ou définir des rôles utilisateur supplémentaires ;](permissions-user-roles.md). Une fois qu’un rôle est défini, vous devez modifier le compte d’utilisateur pour affecter le nouveau rôle.

## Vérifier ou réinitialiser des fournisseurs 2FA

1. Ouvrez le compte d’utilisateur administrateur.

1. Dans le panneau de gauche, cliquez sur **[!UICONTROL 2FA]**.

   ![Administration - ajout d’un nouveau rôle d’utilisateur](./assets/permissions-user-2fa.png){width="600" zoomable="yes"}

1. Vérification des solutions 2FA disponibles pour _Administration_ utilisateurs et conseillent à chaque utilisateur d’installer les solutions qu’il souhaite utiliser avant de se connecter.

   L’authentification par une seule solution 2FA est requise pour se connecter à _Administration_.

1. Si l’utilisateur doit réinstaller la solution 2FA, vous pouvez réinitialiser la configuration 2FA actuelle.

   Pour ce faire, l’utilisateur doit répéter le processus de configuration avant de pouvoir se reconnecter. Par exemple, l’utilisateur peut disposer d’un nouveau smartphone et doit réinstaller l’authentificateur Google. Pour effacer la configuration 2FA actuelle de l’utilisateur, cliquez sur **[!UICONTROL Reset (Provider)]** pour chaque solution à effacer. Lorsque vous y êtes invité, cliquez sur **[!UICONTROL OK]** pour confirmer.

   L’utilisateur reçoit un courrier électronique contenant un lien vers [configuration de 2FA](security-two-factor-authentication.md). Le lien ne peut être utilisé qu’une seule fois. Si l’utilisateur tente de se connecter plusieurs fois, un nouveau lien est envoyé après chaque tentative.

1. Cliquez sur **[!UICONTROL Save User]**.

1. Lorsque vous y êtes invité, saisissez votre mot de passe pour confirmer votre identité, puis cliquez de nouveau sur **[!UICONTROL Save User]**.

   La variable _[!UICONTROL Users]_s’ouvre et répertorie tous les utilisateurs.

## Supprimer un utilisateur administrateur

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Localisez le compte utilisateur à l’aide de filtres au-dessus de la grille, puis cliquez sur le nom de l’utilisateur.

1. Lorsque vous y êtes invité, saisissez votre mot de passe pour confirmer votre identité.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Delete User]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

## Mot de passe oublié et réinitialisation des emails

La configuration du modèle de courrier électronique d’administrateur détermine les courriers électroniques envoyés lorsque les utilisateurs oublient et réinitialisent leurs mots de passe. Cette configuration spécifie le contact du magasin qui apparaît comme expéditeur du message et la durée de validité du lien de récupération du mot de passe.

**_Pour configurer les modèles de courrier électronique d’administrateur :_**

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Setting]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Admin]**.

1. Développer ![basculer d&#39;extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Admin User Emails]** .

   ![Configuration avancée - Paramètres du modèle de courrier électronique d’administration](../configuration-reference/advanced/assets/admin-admin-user-emails.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Forgot Password Email Template]** au modèle envoyé lorsqu’un utilisateur administrateur oublie ses mots de passe.

1. Définir **[!UICONTROL Forgot and Reset Email Sender]** au contact du magasin qui apparaît comme expéditeur du message.

1. Définir **[!UICONTROL User Notification Template]** au modèle de courrier électronique utilisé par défaut pour les notifications admin.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

## Utilisateurs verrouillés

Pour la sécurité de votre entreprise, les comptes d’utilisateurs sont verrouillés par défaut après six tentatives infructueuses de [connexion](../getting-started/admin-signin.md) à l’administrateur. Tout compte d’utilisateur actuellement verrouillé s’affiche dans la grille Utilisateurs verrouillés . Un compte peut être déverrouillé par tout autre utilisateur disposant de toutes les autorisations d’administrateur.

D’autres mesures de sécurité des mots de passe peuvent être mises en oeuvre dans la variable [Administration avancée](../configuration-reference/advanced/admin.md#security) configuration. Voir [Sécurité d’administration](security-admin.md).

![Alerte d’écran de connexion : le compte est temporairement désactivé](./assets/admin-login-locked-out-message.png){width="300"}

**_Pour déverrouiller un compte administrateur :_**

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL Locked Users]**.

1. Dans la grille, cochez la case du compte verrouillé.

   ![Autorisations - comptes utilisateur verrouillés](./assets/permissions-locked-users-grid.png){width="600" zoomable="yes"}

1. Dans le coin supérieur gauche, définissez **[!UICONTROL Actions]** to `Unlock`.

1. Cliquez sur **[!UICONTROL Submit]** pour déverrouiller le compte.
