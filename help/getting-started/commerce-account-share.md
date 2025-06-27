---
title: 'Partager un  [!DNL Commerce] '
description: Découvrez comment accorder un accès limité à votre compte  [!DNL Commerce]  d’autres titulaires  [!DNL Commerce]  compte.
exl-id: adc4fed4-89f4-4b0c-811c-fcf6f94dbc22
feature: User Account
source-git-commit: 0ed338044734ac95bd3421c162b01043de49bf77
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 0%

---

# Partage d’un compte [!DNL Commerce]

Votre compte [!DNL Commerce] contient des informations que vous pouvez mettre à la disposition d’employés et de fournisseurs de services de confiance qui vous aident à gérer votre site. En tant que titulaire de compte principal, vous êtes autorisé à accorder un accès limité aux autres titulaires de compte [!DNL Commerce]. L’accès partagé peut être révoqué, mais ne peut pas être transféré d’un utilisateur à un autre.

L’équipe d’assistance [!DNL Commerce] n’a pas accès au compte et ne peut pas configurer d’accès partagé pour vous. Seul le titulaire du compte principal disposant des autorisations appropriées peut configurer l’accès partagé. Lorsque vous partagez l’accès au compte, toutes les informations sensibles, telles que votre historique de facturation ou les informations de carte de crédit, restent protégées et ne sont jamais disponibles pour les autres utilisateurs.

>[!NOTE]
>
>Toutes les actions entreprises par les utilisateurs disposant d’un accès partagé relèvent de la seule responsabilité du titulaire du compte principal. Adobe n’est pas responsable des actions entreprises par les utilisateurs et utilisatrices ayant un accès partagé à votre compte.

![Paramètres d’accès partagé](./assets/shared-access.png){width="600" zoomable="yes"}

## Configuration d’un compte partagé

1. Avant de commencer, obtenez les informations suivantes à partir du compte [!DNL Commerce] du **nouveau bénéficiaire de l’accès partagé** :

   - L’utilisateur doit déjà s’être enregistré pour un compte sur account.adobe.com et être connecté via account.magento.com. Voir [Création d’un compte Commerce](https://experienceleague.adobe.com/fr/docs/commerce-admin/start/commerce-account/commerce-account-create#create-a-commerce-account) pour plus d’informations.
   - Le `MAGE ID/Account ID (MAG00XXXXXXX)` s’affiche dans le coin supérieur gauche de l’onglet _[!UICONTROL Magento]_, juste au-dessus du lien **Déconnexion**.
   - Adresse `Email` associée au compte.

1. Connectez-vous à votre [[!DNL Commerce]  compte ](commerce-account-create.md).

1. Dans le panneau de navigation de gauche, cliquez sur **[!UICONTROL Shared Access]**.

1. Cliquez sur **[!UICONTROL Add New User]**.

   ![Ajouter un nouvel utilisateur](./assets/shared-access-add.png){width="600" zoomable="yes"}

1. Sous [!UICONTROL _New User Information]_, procédez comme suit :

   - Saisissez le **[!UICONTROL Account ID]** du compte [!DNL Commerce] du nouvel utilisateur.
   - Saisissez l’adresse **[!UICONTROL Email]** associée au compte [!DNL Commerce] du nouvel utilisateur.

   ![Informations sur le nouvel utilisateur](./assets/shared-new-user.png){width="600"}

1. Sous _[!UICONTROL Shared Information]_, procédez comme suit :

   - Pour identifier le compte partagé, saisissez un **[!UICONTROL Share Name]**. Ce nom est destiné à une référence interne et n’est visible que par vous et la personne avec laquelle vous partagez votre compte.

     Il est recommandé d’utiliser le nom de votre organisation comme [!UICONTROL Share Name]. N’utilisez pas un nom commençant par `CLOUD SHARED ACCESS FROM MAG XYX`.
   - Si vous souhaitez partager vos coordonnées personnelles avec le nouvel utilisateur, saisissez **[!UICONTROL Your Email]** et **[!UICONTROL Your Phone]**.

1. Sous _[!UICONTROL Grant Account Permissions]_, cochez la case de chaque produit et service [!DNL Commerce] que vous souhaitez partager.

   ![Accorder les autorisations de compte](./assets/shared-permissions.png){width="600"}

1. Cliquez sur **[!UICONTROL Create Shared Access]**.

   Les informations sur le nouvel utilisateur apparaissent dans la section _[!UICONTROL Manage Permissions]_&#x200B;de la page Accès partagé et une invitation par e-mail contenant des instructions pour accéder au compte partagé est envoyée au nouvel utilisateur.

   ![Gestion des autorisations d’accès partagé](./assets/shared-manage-permissions.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Il n’est pas nécessaire de partager l’accès au _[!UICONTROL Security Tool]_- Tout utilisateur disposant d’un ID MAGE peut configurer l’outil d’analyse de sécurité avec son propre compte. Ils ont juste besoin des privilèges nécessaires pour apporter des modifications au site et vérifier la propriété du domaine à l’aide de l’une des [méthodes requises](https://experienceleague.adobe.com/fr/docs/commerce-admin/systems/security/security-scan)).

## Accès à un compte partagé

Les instructions suivantes sont écrites du point de vue d’un utilisateur partagé qui reçoit une invitation à accéder à un compte partagé.

1. Lorsque vous recevez une invitation à accéder à un compte partagé, suivez les instructions contenues dans l’e-mail pour vous connecter à votre propre compte [!DNL Commerce].

   Le panneau de navigation de gauche de votre compte comporte un nouvel onglet _[!UICONTROL Shared with me]_. Le contrôle&#x200B;_[!UICONTROL Switch Accounts]_ situé dans le coin supérieur droit propose des options relatives au `My Account` et au nom du compte partagé.

   ![Partagé avec moi](./assets/shared-with-me.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >   Si vous ne voyez pas le contrôle de _[!UICONTROL Switch Accounts]_, contactez le titulaire du compte principal et confirmez qu’il a saisi vos [informations de compte](#set-up-a-shared-account) correctes.


1. Pour accéder au compte partagé, définissez **[!UICONTROL Switch Accounts]** sur le nom du compte partagé.

   ![Passer au compte partagé](./assets/shared-switch.png){width="600" zoomable="yes"}

   Le compte partagé affiche un message de bienvenue et des informations de contact. Le panneau de navigation de gauche comprend uniquement les éléments que vous êtes autorisé à utiliser.

1. Pour connecter le compte partagé au Centre d’aide, cliquez sur **[!UICONTROL Support]** dans le panneau de navigation de gauche du compte partagé.

   ![Assistance](./assets/shared-support.png){width="600" zoomable="yes"}

   Vous pouvez utiliser le [Centre d’aide Adobe Commerce](https://experienceleague.adobe.com/fr/docs/commerce-knowledge-base/kb/overview) à partir du compte partagé pour rechercher des articles et des informations de dépannage, rechercher des correctifs pour les problèmes connus et créer des tickets d’assistance.

   >[!NOTE]
   >
   >Après avoir reçu l’accès partagé, pour [soumettre un cas d’assistance](https://experienceleague.adobe.com/fr/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) sur Experience League, veillez d’abord à sélectionner le nom de l’organisation qui se termine par « ([!DNL Commerce]) » dans la colonne de gauche.

1. Pour revenir à votre propre compte, cliquez sur **Précédent** dans les commandes de votre navigateur et définissez **[!UICONTROL Switch Accounts]** sur `My Account`.

## Révoquer l’accès partagé

1. Connectez-vous à votre compte Commerce.

1. Dans le panneau de navigation de gauche, cliquez sur **[!UICONTROL Shared Access]**.

1. Recherchez le compte à révoquer sous _[!UICONTROL Managing Users & Permissions]_&#x200B;et cliquez sur **[!UICONTROL Delete]**.

   >[!NOTE]
   >
   > Si **[!UICONTROL Delete]** n’est pas affiché, vérifiez si le **[!UICONTROL Share Name]** contient le modèle de dénomination `Cloud Shared Access from MAG0XYZ`. Si le compte possède ce modèle de dénomination [ et ne peut pas être supprimé](https://experienceleague.adobe.com/fr/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#remove-cloud-shared-access-users), c’est parce que l’accès partagé a été créé par une API et non directement à partir du compte [Commerce](https://account.magento.com/).
   > 
   > S’il ne peut pas être supprimé, demandez simplement au propriétaire du compte de modifier le compte d’accès partagé et, sous Accorder des autorisations de compte, décochez chaque élément. Après cette mise à jour, l’utilisateur ne pourra plus accéder aux ressources du compte.
   > ![image](https://git.corp.adobe.com/AdobeDocs/commerce-admin.en/assets/38345/55f383e5-89c7-4832-bada-f765b522f4b5)
   >
   > En outre, assurez-vous que les utilisateurs sont supprimés du projet afin qu’ils ne reçoivent plus de notifications par e-mail : [Les anciens membres de l’équipe reçoivent des e-mails de notification dans le cloud Adobe Commerce](https://experienceleague.adobe.com/fr/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails)


1. Lorsque vous êtes invité à confirmer, cliquez sur **[!UICONTROL Delete User]**.

>[!NOTE]
>
>Dans cette interface, vous ne pouvez pas supprimer les utilisateurs dotés du nom de partage _Cloud Shared Access from MAG[XYZ]_. Voir [Comment supprimer des utilisateurs ayant obtenu un accès partagé via un projet cloud ?](https://experienceleague.adobe.com/fr/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#remove-cloud-shared-access-users).

## Lectures connexes

[Résolution des problèmes d&#39;accès partagé](https://experienceleague.adobe.com/fr/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/shared-access-troubleshooting)

