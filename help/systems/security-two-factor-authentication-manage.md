---
title: Gestion de l’authentification à deux facteurs
description: Découvrez comment gérer l’authentification à deux facteurs et réinitialiser les authentificateurs pour les utilisateurs administrateurs.
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# Gestion de l’authentification à deux facteurs

Les utilisateurs qui ne parviennent pas à se connecter à l’_Admin_ avec l’authentification à deux facteurs (2FA) peuvent essayer de synchroniser ou de résoudre le problème. Vous pouvez également réinitialiser les authentificateurs associés au compte. Une fois réinitialisé, l’utilisateur doit se reconnecter et reconfigurer les authentificateurs requis.

Si vous rencontrez des problèmes pour vous connecter avec 2FA, tenez compte des points suivants :

- Certaines applications mobiles incluent des options de synchronisation. Cette option reconnecte l’application et le serveur, et synchronise les paramètres de l’heure sur l’appareil et le serveur.
- La révocation d’un appareil ou la réinitialisation d’un authentificateur peut aider les utilisateurs à se connecter.
- L’effacement du cache web et des cookies pour l’installation d’Adobe Commerce ou de Magento Open Source peut également être utile. Les authentificateurs, comme Google, utilisent des cookies générés pour enregistrer l’accès et la durée. Effacez les cookies pour votre navigateur et votre domaine de magasin spécifiques.
- Le blocage des cookies empêche certains authentificateurs, tels que [!DNL Google Authenticator], de terminer le processus de vérification. Ajoutez à votre navigateur une règle qui autorise les cookies pour votre installation d’Adobe Commerce.

Pour réinitialiser les authentificateurs à partir de la ligne de commande et obtenir des informations de dépannage plus avancées, consultez la section [Authentification à deux facteurs](https://developer.adobe.com/commerce/testing/functional-testing-framework/two-factor-authentication/) dans la documentation du développeur.

**_Pour réinitialiser les authentificateurs d’un compte utilisateur :_**

>[!NOTE]
>
>Pour réinitialiser les fournisseurs 2FA pour d’autres utilisateurs, vous devez être un _administrateur_ avec des autorisations `All` ou disposer d’autorisations `Custom` pour votre rôle avec [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL Two Factor Auth] et [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL All Users] sélectionné. Pour en savoir plus, voir [Rôles utilisateur](permissions-user-roles.md).

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Sélectionnez l’utilisateur et ouvrez le compte en mode d’édition.

1. Faites défiler l’écran jusqu’à la section _[!UICONTROL Current User Identity Verification]_et saisissez votre mot de passe.

1. Dans le panneau de gauche, cliquez sur **[!UICONTROL 2FA]**.

1. Dans la section _[!UICONTROL Configuration reset]_, cliquez sur **[!UICONTROL Reset]**et **[!UICONTROL OK]**pour confirmer.

   ![Compte utilisateur - Activer 2FA](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"}

   Si l’utilisateur souhaite restaurer les méthodes 2FA requises dans son compte, il doit reconfigurer chacune d’elles à partir de la page _Connexion_.

1. Cliquez ensuite sur **[!UICONTROL Save User]**.
