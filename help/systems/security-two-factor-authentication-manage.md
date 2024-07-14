---
title: Gestion de l’authentification à deux facteurs
description: Découvrez comment gérer l’authentification à deux facteurs et réinitialiser les authentificateurs pour les utilisateurs administrateurs.
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# Gestion de l’authentification à deux facteurs

Les utilisateurs qui ne peuvent pas se connecter à _Admin_ avec une authentification à deux facteurs (2FA) peuvent essayer de synchroniser ou de résoudre le problème. Vous pouvez également réinitialiser les authentificateurs associés au compte. Lors de la réinitialisation, l’utilisateur doit se reconnecter et reconfigurer les authentificateurs requis.

Si vous rencontrez des problèmes pour vous connecter avec 2FA, tenez compte des points suivants :

- Certaines applications mobiles incluent des options de synchronisation. Cette option reconnecte l’application et le serveur et synchronise les paramètres temporels sur le périphérique et le serveur.
- Révoquer un appareil ou réinitialiser un authentificateur peut aider les utilisateurs à se connecter.
- L’effacement du cache web et des cookies pour l’installation d’Adobe Commerce ou de Magento Open Source peut également vous aider. Les authentificateurs, comme Google, utilisent des cookies générés pour enregistrer l’accès et la durée. Effacez les cookies pour votre navigateur spécifique et stockez le domaine.
- Le blocage des cookies empêche certains authentificateurs, tels que [!DNL Google Authenticator], d’achever le processus de vérification. Ajoutez une règle à votre navigateur qui autorise les cookies pour votre installation Adobe Commerce.

Pour réinitialiser les authentificateurs à partir de la ligne de commande et obtenir des informations de dépannage plus avancées, reportez-vous à la section [Authentification à deux facteurs](https://developer.adobe.com/commerce/testing/functional-testing-framework/two-factor-authentication/) de la documentation destinée aux développeurs.

**_Pour réinitialiser les authentificateurs pour un compte d’utilisateur :_**

>[!NOTE]
>
>Pour réinitialiser les fournisseurs 2FA pour d’autres utilisateurs, vous devez être un _administrateur_ avec des autorisations `All` ou disposer d’autorisations `Custom` pour votre rôle avec [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL Two Factor Auth] et [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL All Users] sélectionnés. Pour en savoir plus, voir [Rôles utilisateur](permissions-user-roles.md).

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Sélectionnez l’utilisateur et ouvrez le compte en mode d’édition.

1. Faites défiler l’écran jusqu’à la section _[!UICONTROL Current User Identity Verification]_et saisissez votre mot de passe.

1. Dans le panneau de gauche, cliquez sur **[!UICONTROL 2FA]**.

1. Dans la section _[!UICONTROL Configuration reset]_, cliquez sur **[!UICONTROL Reset]**et **[!UICONTROL OK]**pour confirmer.

   ![Compte utilisateur - activer 2FA](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"}

   Si l’utilisateur souhaite restaurer les méthodes 2FA requises dans son compte, il doit reconfigurer chacune d’elles à partir de la page _Se connecter_.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save User]**.
