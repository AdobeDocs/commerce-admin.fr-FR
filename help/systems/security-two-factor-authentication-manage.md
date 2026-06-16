---
title: Gestion de l’authentification à deux facteurs
description: Découvrez comment gérer l’authentification à deux facteurs et réinitialiser les authentificateurs pour les utilisateurs administrateurs.
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
TQID: https://experienceleague.adobe.com/aE-36667-f0E4GSXDjZZmFUkS3wa-xTLUMbVtjwS6qk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 336
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

**_Pour réinitialiser les authentificateurs d’un compte utilisateur:_**

>[!NOTE]
>
>Pour réinitialiser les fournisseurs 2FA pour d’autres utilisateurs, vous devez être un _administrateur_ avec des autorisations `All` ou disposer d’autorisations `Custom` pour votre rôle avec [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL Two Factor Auth] et [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL All Users] sélectionné. Pour en savoir plus, voir [Rôles utilisateur](permissions-user-roles.md).

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Sélectionnez l’utilisateur et ouvrez le compte en mode d’édition.

1. Faites défiler l’écran jusqu’à la section _[!UICONTROL Current User Identity Verification]_&#x200B;et saisissez votre mot de passe.

1. Dans le panneau de gauche, cliquez sur **[!UICONTROL 2FA]**.

1. Dans la section _[!UICONTROL Configuration reset]_, cliquez sur **[!UICONTROL Reset]**&#x200B;et **[!UICONTROL OK]**&#x200B;pour confirmer.

   ![Compte utilisateur - Activer 2FA](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"}

   Si l’utilisateur souhaite restaurer les méthodes 2FA requises dans son compte, il doit reconfigurer chacune d’elles à partir de la page _Connexion_.

1. Cliquez ensuite sur **[!UICONTROL Save User]**.
