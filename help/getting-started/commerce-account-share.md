---
title: Partager une [!DNL Commerce] account
description: Découvrez comment accorder un accès limité à votre [!DNL Commerce] compte autre [!DNL Commerce] titulaires de compte.
exl-id: adc4fed4-89f4-4b0c-811c-fcf6f94dbc22
feature: User Account
source-git-commit: ec634ebedd43b8bbc6b4a3e5079035b055740f2d
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---

# Partager une [!DNL Commerce] account

Votre [!DNL Commerce] Ce compte contient des informations que vous pouvez mettre à la disposition des employés et des fournisseurs de services de confiance qui vous aident à gérer votre site. En tant que titulaire principal du compte, vous avez le pouvoir d’accorder un accès limité à d’autres [!DNL Commerce] titulaires de compte. L’accès partagé peut être révoqué, mais ne peut pas être transféré d’un utilisateur à un autre.

La variable [!DNL Commerce] L’équipe d’assistance n’a pas accès au compte et ne peut pas configurer l’accès partagé pour vous. Seul le titulaire du compte principal disposant des autorisations appropriées peut configurer l’accès partagé. Lorsque vous partagez l’accès à votre compte, toutes les informations sensibles, telles que l’historique de facturation ou les informations de carte de crédit, restent protégées et ne sont jamais accessibles à d’autres utilisateurs.

>[!NOTE]
>
>Toutes les actions entreprises par les utilisateurs disposant d&#39;un accès partagé sont de la seule responsabilité du titulaire du compte principal. Adobe n’est responsable d’aucune action entreprise par les utilisateurs qui ont partagé l’accès à votre compte.

![Paramètres d’accès partagé](./assets/shared-access.png){width="600" zoomable="yes"}

## Configuration d’un compte partagé

1. Avant de commencer, obtenez les informations suivantes à partir de la [!DNL Commerce] du compte **nouveau titulaire d’accès partagé**:

   - L’utilisateur doit avoir déjà été enregistré pour un compte à l’adresse account.adobe.com et être connecté via account.magento.com.
   - La variable `MAGE ID/Account ID (MAG00XXXXXXX)` s’affiche dans le coin supérieur gauche de la _[!UICONTROL Magento]_, juste au-dessus de l’onglet **Déconnexion**lien.
   - La variable `Email` adresse associée au compte.

1. Connectez-vous à [[!DNL Commerce] account](commerce-account-create.md).

1. Dans le panneau de navigation de gauche, cliquez sur **[!UICONTROL Shared Access]**.

1. Cliquez sur **[!UICONTROL Add New User]**.

   ![Ajouter un nouvel utilisateur](./assets/shared-access-add.png){width="600" zoomable="yes"}

1. Sous [!UICONTROL _New User Information]_, procédez comme suit :

   - Saisissez le **[!UICONTROL Account ID]** du nouvel utilisateur [!DNL Commerce] compte .
   - Saisissez le **[!UICONTROL Email]** adresse associée au nouvel utilisateur [!DNL Commerce] compte .

   ![Informations sur les nouveaux utilisateurs](./assets/shared-new-user.png){width="600"}

1. Sous _[!UICONTROL Shared Information]_, procédez comme suit :

   - Pour identifier le compte partagé, saisissez une **[!UICONTROL Share Name]**. Ce nom est à titre de référence interne et n’est visible que pour vous et la personne avec laquelle vous partagez votre compte.

     Il est recommandé d’utiliser le nom de votre organisation comme [!UICONTROL Share Name]. N’utilisez pas de nom commençant par `CLOUD SHARED ACCESS FROM MAG XYX`.
   - Si vous souhaitez partager vos coordonnées personnelles avec le nouvel utilisateur, saisissez **[!UICONTROL Your Email]** et **[!UICONTROL Your Phone]**.

1. Sous _[!UICONTROL Grant Account Permissions]_, cochez la case de chaque [!DNL Commerce] produit et service que vous souhaitez partager.

   ![Octroi des autorisations de compte](./assets/shared-permissions.png){width="600"}

1. Cliquez sur **[!UICONTROL Create Shared Access]**.

   Les informations sur le nouvel utilisateur apparaissent dans la variable _[!UICONTROL Manage Permissions]_de la page Accès partagé et une invitation par courrier électronique contenant des instructions pour accéder au compte partagé est envoyée au nouvel utilisateur.

   ![Gestion des autorisations pour l’accès partagé](./assets/shared-manage-permissions.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Il n’est pas nécessaire de partager l’accès au _[!UICONTROL Security Tool]_- Tout utilisateur disposant d’un MAGE ID peut configurer l’outil d’analyse de sécurité avec son propre compte. Ils ont simplement besoin des privilèges nécessaires pour apporter des modifications au site et vérifier la propriété du domaine à l’aide de l’une des [Méthodes requises](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security-scan)).

## Accès à un compte partagé

Les instructions suivantes sont écrites du point de vue d’un utilisateur partagé qui reçoit une invitation à un compte partagé.

1. Lorsque vous recevez une invitation à accéder à un compte partagé, suivez les instructions contenues dans le courrier électronique pour vous connecter. [!DNL Commerce] compte .

   Le panneau de navigation de gauche de votre compte comporte un nouveau _[!UICONTROL Shared with me]_. La variable_[!UICONTROL Switch Accounts]_ Le contrôle dans le coin supérieur droit comporte des options pour `My Account` et le nom du compte partagé.

   ![Partagé avec moi](./assets/shared-with-me.png){width="600" zoomable="yes"}

1. Pour accéder au compte partagé, définissez **[!UICONTROL Switch Accounts]** au nom du compte partagé.

   ![Passez au compte partagé](./assets/shared-switch.png){width="600" zoomable="yes"}

   Le compte partagé affiche un message de bienvenue et des coordonnées. Le panneau de navigation de gauche comprend uniquement les éléments que vous êtes autorisé à utiliser.

1. Pour connecter le compte partagé au centre d’aide, cliquez sur **[!UICONTROL Support]** dans le panneau de navigation de gauche du compte partagé.

   ![Assistance](./assets/shared-support.png){width="600" zoomable="yes"}

   Vous pouvez utiliser la variable [Centre d’aide Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview.html) du compte partagé pour rechercher des articles et des informations de dépannage, rechercher des correctifs pour les problèmes connus et créer des tickets d’assistance.

   >[!NOTE]
   >
   >Après avoir reçu l’accès partagé, l’utilisateur doit se connecter à son [[!DNL Commerce] account](https://account.magento.com/customer/account/login), accédez à _Accès partagé_, puis cliquez sur le bouton **[!UICONTROL Support]** . Cette action n’est nécessaire que pour s’assurer que la variable [Base de connaissances du support Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview.html) est correctement configuré via la fonction `SSO` appelez .

1. Pour revenir à votre propre compte, cliquez sur **Précédent** dans les commandes de votre navigateur et définissez **[!UICONTROL Switch Accounts]** to `My Account`.

## Révoquer l’accès partagé

1. Connectez-vous à votre compte Commerce.

1. Dans le panneau de navigation de gauche, cliquez sur **[!UICONTROL Shared Access]**.

1. Recherche du compte à révoquer sous _[!UICONTROL Managing Users & Permissions]_et cliquez sur **[!UICONTROL Delete]**.

   >[!NOTE]
   >
   > If  **[!UICONTROL Delete]** n’est pas affiché, vérifiez si la variable **[!UICONTROL Share Name]** commence par `Cloud Shared Access from MAG XYZ`. Vous ne pouvez pas supprimer de comptes avec cette [modèle de dénomination](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#remove-cloud-shared-access-users).
   > 
   > Si tel est le cas, demandez au propriétaire du compte de modifier le compte Accès partagé afin d’effacer les autorisations du compte. Après cette mise à jour, l’utilisateur ne peut plus accéder aux ressources du compte.
   >
   > En outre, assurez-vous que les utilisateurs sont supprimés du projet afin qu’ils ne reçoivent plus de notifications par courrier électronique : [Les anciens membres de l’équipe reçoivent des e-mails de notification cloud Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails.html)


1. Lorsque vous y êtes invité, cliquez sur **[!UICONTROL Delete User]**.

>[!NOTE]
>
>Vous ne pouvez pas supprimer les utilisateurs dont le nom du partage est _Accès partagé dans le cloud à partir de MAG[XYZ]_ dans cette interface. Voir [Comment supprimer les utilisateurs auxquels un accès partagé a été accordé via un projet Cloud ?](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#remove-cloud-shared-access-users).
