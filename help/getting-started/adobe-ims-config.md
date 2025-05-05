---
title: Configuration de l’intégration d’administration Commerce avec l’ID
description: Suivez cette procédure facultative pour intégrer les connexions du compte utilisateur d’administrateur Adobe Commerce à Adobe ID.
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 0%

---

# Configuration de l’intégration d’administration Commerce à Adobe ID

{{ee-feature}}

Cette intégration prend en charge les commerçants Commerce avec les utilisateurs administrateurs disposant d’une Adobe ID et souhaitant rationaliser la connexion aux produits Adobe Commerce et Adobe Business. Elle est facultative et activée sur une base par instance. Seuls les workflows utilisateur administrateur sont affectés lorsqu’ils sont activés. 

>[!IMPORTANT]
>
>Les utilisateurs administrateurs doivent enregistrer leurs informations d’identification d’administrateur Commerce (nom d’utilisateur et mot de passe) et 2FA avant d’activer cette intégration. Ces informations d’identification sont nécessaires si l’intégration IMS est désactivée.

## Conditions préalables

* Adobe Commerce 2.4.5 ou version ultérieure
* Un compte Adobe.com avec accès à [Adobe Admin Console](https://adminconsole.adobe.com/).

L’administrateur qui configure cette intégration a besoin des informations d’identification suivantes pendant l’activation du module :

* Identifiant de l&#39;organisation (obtenu à partir de [Adobe Admin Console](https://adminconsole.adobe.com/)), qui doit comporter au moins 24 caractères. L’utilisateur authentifié doit appartenir à cette organisation IMS. Pour plus d’informations sur la recherche de votre ID d’organisation, voir [ Organisations dans Experience Cloud ](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html).
* 2FA doit être appliqué au niveau de l’organisation dans Adobe Admin Console pour activer le module. Cochez la case [Paramètres d’authentification](https://helpx.adobe.com/enterprise/using/authentication-settings.html#two-step-verification).
* Identifiant client
* Secret client
* L’ID client et le secret client sont disponibles après la récupération des clés API du [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/credentials/).

Les utilisateurs administrateurs de Commerce doivent créer un compte avec un Adobe ID pour se connecter.

## Étapes générales

* Obtention de l’ID d’organisation Adobe à partir de [Adobe Admin Console](https://adminconsole.adobe.com/)
* Générez un nouveau projet, des clés d’API IMS et un secret à partir du [Adobe Developer Console](https://developer.adobe.com/)
* Configuration des utilisateurs d’Adobe Commerce dans Adobe Admin Console
* Activez le module `AdminAdobeIms` .

Pour une intégration réussie, tous les utilisateurs d’Adobe Commerce doivent disposer de comptes utilisateur d’administration portant le même nom et la même adresse e-mail principale. S’il n’existe pas de compte utilisateur Administrateur correspondant, un utilisateur disposant des autorisations requises (généralement avec le rôle Administrateur ) doit [créer manuellement le compte utilisateur Administrateur](../systems/permissions-users-all.md#create-a-user) avec le même nom et la même adresse e-mail.

## Configuration de l’intégration

Une fois les étapes suivantes effectuées par un administrateur ou un développeur disposant d’un accès système, le bouton _[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_s’affiche sur la page de connexion d’administrateur Commerce pour tous les utilisateurs administrateurs.

### Étape 1 : obtention de l’ID d’organisation Adobe

Pour activer cette fonctionnalité, vous devez être membre d’au moins une organisation IMS. Si vous disposez d’une Adobe ID, vous appartenez par défaut à au moins une organisation Adobe. Connectez-vous à [Adobe Admin Console](https://adminconsole.adobe.com/) pour récupérer votre ID d’organisation.

### Étape 2 : générer un nouveau projet, des clés API IMS et un secret

Pour créer des projets pour une organisation, le compte Administrateur Adobe de l’organisation doit disposer du rôle d’administrateur système ou de développeur. Voir le Guide de Developer Console [](https://developer.adobe.com/developer-console/docs/guides/projects/).

1. Connectez-vous à [Adobe Developer Console](https://developer.adobe.com/).
1. Accédez à l’onglet **[!UICONTROL Projects]** (adobe.io/projects) et cliquez sur **[!UICONTROL Create a new project]**.
1. Cliquez sur **[!UICONTROL Add API]** sur la page Projet nouvellement créée.
1. Sélectionnez **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]**.
1. Sélectionnez **[!UICONTROL Oauth 2.0 Web]**.
1. Spécifiez le **[!UICONTROL Redirect URI]** : `https://<commerce_base_url>/`
1. Spécifiez le **[!UICONTROL Redirect URI pattern]** : `https://<commerce_base_url>/.*`

   Évitez les points du nom d’hôte en les faisant précéder de `\\`. L’ajout d’un caractère générique à la fin de l’URL prend en charge la clé secrète d’administration Adobe Commerce.

1. Cliquez sur **[!UICONTROL Save configured API]**.
1. Copiez les clés [!UICONTROL Client ID] et [!UICONTROL Client Secret] du projet créé.

### Étape 3 : configuration des utilisateurs d’Adobe Commerce dans Adobe Admin Console

Avant d’activer l’intégration, vérifiez que chaque compte utilisateur administrateur Adobe Commerce possède un compte Adobe IMS correspondant. Les utilisateurs d’Adobe Commerce doivent appartenir à une organisation Adobe spécifique pour se connecter à l’aide d’un Adobe ID.

>[!TIP]
>
>Vous pouvez créer plusieurs comptes utilisateur en chargeant les informations utilisateur à partir d’un fichier CSV. Voir [Gérer plusieurs utilisateurs](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html).

1. Dans [Adobe Admin Console](https://helpx.adobe.com/fr/enterprise/using/admin-console.html), accédez à **[!UICONTROL Users]** > **[!UICONTROL Users]**.

1. Cliquez sur **[!UICONTROL Add User]**.

1. Saisissez l’adresse e-mail de l’utilisateur.

   Le cas échéant, le type d’identifiant recommandé est renseigné automatiquement. Vous pouvez modifier ce paramètre sur l’un des ID de produit de la liste, qui est basé sur le plan d’achat de votre entreprise.

   Vous pouvez ajouter jusqu’à dix utilisateurs à la fois. Pour en ajouter d’autres, répétez les étapes précédentes après avoir enregistré vos modifications.

1. Cliquez sur **[!UICONTROL Save]**.

L’utilisateur est ajouté et affiché dans la liste des [!UICONTROL Users].

### Étape 4 : activer le module AdminAdobeIms

Le module `AdminAdobeIms` est responsable de l’intégration Adobe Commerce/Adobe IMS. Après avoir configuré le nouveau projet et copié votre identifiant d’organisation, votre identifiant client et votre secret client, vous pouvez activer le module `AdminAdobeIms`.

Saisissez `bin/magento admin:adobe-ims:enable`. Vous êtes invité à saisir les paramètres suivants. Utilisez les valeurs générées lors de la création du projet.

* Identifiant de l’organisation
* Identifiant client
* Secret client
* 2FA activé

Adobe Commerce affiche un message qui indique si l’activation a réussi ou échoué.

Une fois cette fonctionnalité activée, vous pouvez effectuer la transition d’autres comptes d’utilisateur Adobe Commerce vers des comptes Adobe IMS. Les utilisateurs d’Adobe Commerce doivent appartenir à l’organisation Adobe configurée pour se connecter à l’aide d’un Adobe ID.
