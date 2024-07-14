---
title: Configuration de l’intégration d’administrateur Commerce avec l’ID
description: Suivez cette procédure facultative pour intégrer les comptes d’utilisateur administrateur Adobe Commerce à Adobe ID.
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
source-git-commit: 9a9106cde5184823755fb1f44fe7eae300442abc
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 0%

---

# Configuration de l’intégration des administrateurs Commerce avec Adobe ID

{{ee-feature}}

Cette intégration prend en charge les marchands Commerce avec les utilisateurs administrateurs disposant d’un Adobe ID et qui souhaitent rationaliser la connexion aux produits Adobe Commerce et Adobe Business. Elle est facultative et activée par instance. Seuls les workflows des utilisateurs administrateurs sont affectés lorsqu’ils sont activés. 

>[!IMPORTANT]
>
>Les utilisateurs administrateurs doivent enregistrer leurs informations d’identification d’administrateur Commerce (nom d’utilisateur et mot de passe) et leurs informations d’identification 2FA avant d’activer cette intégration. Ces informations d’identification sont nécessaires si l’intégration IMS est désactivée.

## Conditions préalables

* Adobe Commerce 2.4.5 ou version ultérieure
* Un compte Adobe.com avec accès au [Adobe Admin Console](https://adminconsole.adobe.com/).

L’administrateur qui configure cette intégration a besoin des informations d’identification suivantes lors de l’activation du module :

* ID d’organisation (obtenu à partir de [Adobe Admin Console](https://adminconsole.adobe.com/)), qui doit comporter au moins 24 caractères. L’utilisateur authentifié doit appartenir à cette organisation IMS. Pour plus d’informations sur la recherche de l’ID d’organisation, voir [Organisations en Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html).
* 2FA doit être appliqué au niveau de l’organisation dans Adobe Admin Console pour activer le module. Vérifiez les [paramètres d&#39;authentification](https://helpx.adobe.com/enterprise/using/authentication-settings.html#two-step-verification).
* ID client
* Client secret
* L’ID client et le secret client sont disponibles après la récupération des clés API à partir de [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/credentials/).

Les utilisateurs administrateurs de Commerce doivent créer un compte avec un Adobe ID pour se connecter.

## Étapes générales

* Obtention de l’identifiant de l’organisation d’Adobe à partir de [Adobe Admin Console](https://adminconsole.adobe.com/)
* Générez un nouveau projet, des clés d’API IMS et un nouveau secret à partir du [Adobe Developer Console](https://developer.adobe.com/)
* Configuration des utilisateurs Adobe Commerce dans Adobe Admin Console
* Activez le module `AdminAdobeIms`.

Une intégration réussie nécessite que tous les utilisateurs d’Adobe Commerce disposent de comptes d’utilisateurs administrateurs portant le même nom et la même adresse électronique principale. Si aucun compte utilisateur administrateur correspondant n’existe, un utilisateur disposant des autorisations requises (généralement du rôle Administrateur) doit [ créer manuellement le compte utilisateur administrateur](../systems/permissions-users-all.md#create-a-user) avec le même nom et le même courrier électronique.

## Configuration de l’intégration

Une fois les étapes suivantes terminées par un administrateur ou un développeur disposant d’un accès système, le bouton _[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_s’affiche sur la page de connexion de l’administrateur Commerce pour tous les utilisateurs administrateurs.

### Étape 1 : Obtention de l’identifiant de l’organisation d’Adobe

L’appartenance à au moins une organisation IMS est requise pour activer cette fonctionnalité. Si vous disposez d’une Adobe ID, vous appartenez par défaut à au moins une organisation Adobe. Connectez-vous à [Adobe Admin Console](https://adminconsole.adobe.com/) pour récupérer votre ID d’organisation.

### Étape 2 : générer un nouveau projet, des clés d’API IMS et un secret

Pour créer des projets pour une organisation, le compte administrateur d’Adobe de l’organisation doit disposer du rôle d’administrateur système ou de développeur. Voir le [Guide de Developer Console](https://developer.adobe.com/developer-console/docs/guides/projects/).

1. Connectez-vous à [Adobe Developer Console](https://developer.adobe.com/).
1. Accédez à l’onglet **[!UICONTROL Projects]** (adobe.io/projects) et cliquez sur **[!UICONTROL Create a new project]**.
1. Cliquez sur **[!UICONTROL Add API]** sur la page Projet nouvellement créée.
1. Sélectionnez **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]**.
1. Sélectionnez **[!UICONTROL Oauth 2.0 Web]**.
1. Spécifiez le **[!UICONTROL Redirect URI]** : `https://<hostname>/`
1. Spécifiez le **[!UICONTROL Redirect URI pattern]** : `https://<hostname>/.*`

   Échappez aux points du nom d’hôte en les précédant de `\\`. L’ajout d’un caractère générique à la fin de l’URL prend en charge la clé secrète d’administration Adobe Commerce.

1. Cliquez sur **[!UICONTROL Save configured API]**.
1. Copiez les clés [!UICONTROL Client ID] et [!UICONTROL Client Secret] du projet créé.

### Étape 3 : configuration des utilisateurs Adobe Commerce dans Adobe Admin Console

Avant d’activer l’intégration, vérifiez que chaque compte utilisateur administrateur Adobe Commerce possède un compte Adobe IMS correspondant. Les utilisateurs d’Adobe Commerce doivent appartenir à une organisation d’Adobe spécifique pour se connecter à l’aide d’Adobe ID.

>[!TIP]
>
>Vous pouvez créer plusieurs comptes d’utilisateurs en chargeant les informations utilisateur à partir d’un fichier CSV. Voir [Gestion de plusieurs utilisateurs](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html).

1. Dans le [Adobe Admin Console](https://helpx.adobe.com/fr/enterprise/using/admin-console.html), accédez à **[!UICONTROL Users]** > **[!UICONTROL Users]**.

1. Cliquez sur **[!UICONTROL Add User]**.

1. Saisissez l’adresse électronique de l’utilisateur.

   Le cas échéant, le type d’ID recommandé est automatiquement renseigné. Vous pouvez définir ce paramètre sur l’un des ID de produit de la liste, qui repose sur le plan d’achat de votre entreprise.

   Vous pouvez ajouter jusqu’à dix utilisateurs simultanément. Pour en ajouter d’autres, répétez les étapes précédentes après avoir enregistré vos modifications.

1. Cliquez sur **[!UICONTROL Save]**.

L’utilisateur est ajouté et affiché dans la liste [!UICONTROL Users].

### Étape 4 : Activation du module AdminAdobeIms

Le module `AdminAdobeIms` est responsable de l&#39;intégration Adobe Commerce/Adobe IMS. Après avoir configuré le nouveau projet et copié l’ID d’organisation, l’ID client et le secret client, vous pouvez activer le module `AdminAdobeIms`.

Saisissez `bin/magento admin:adobe-ims:enable`. Vous êtes invité à saisir les paramètres suivants. Utilisez les valeurs générées lors de la création du projet.

* ID d’organisation
* ID client
* Client secret
* 2FA activé

Adobe Commerce affiche un message indiquant si l’activation a réussi ou échoué.

Une fois cette fonctionnalité activée, vous pouvez transférer d’autres comptes utilisateurs Adobe Commerce vers des comptes Adobe IMS. Les utilisateurs d’Adobe Commerce doivent appartenir à l’organisation d’Adobe configurée pour se connecter à l’aide d’un Adobe ID.
