---
title: Gestion de l’intégration des Experience Cloud
description: Découvrez comment gérer l’intégration des Experience Cloud et résoudre les problèmes
hide: false
hidefromtoc: false
feature: Integration
exl-id: 451bf2e1-7c38-40be-a7c1-aaf0fe9f486c
source-git-commit: 15569794c1e66ba5a93e46206244e2951522923e
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Gestion de l’intégration des Experience Cloud

Après l’activation initiale, gérez l’état de l’intégration de l’Experience Cloud en activant ou en désactivant l’extension Commerce Admin Unified Experience.

- Si l’extension Commerce Admin Unified Experience est activée et que les comptes d’administrateur sont [ configurés correctement](#manage-admin-user-accounts), les administrateurs Commerce peuvent afficher et accéder aux projets Commerce disponibles à partir de Adobe Experience Cloud. Les administrateurs peuvent toujours accéder à des projets individuels à l’aide de l’URL d’administration de l’environnement de projet Commerce.

- Si l’extension Commerce Admin Unified Experience est désactivée, l’accès via Experience Cloud est désactivé. Les administrateurs doivent se connecter à des projets individuels à l’aide de l’URL d’administration de l’environnement de projet Commerce.

>[!WARNING]
>
>Si l’intégration d’Adobe Identity Management Service (IMS) est désactivée, l’intégration d’Experience Cloud est désactivée automatiquement.

## Gestion de l’intégration à partir de l’administrateur

1. Dans l’administrateur Commerce, ouvrez le menu Configuration de magasin en sélectionnant **[!UICONTROL Stores]** dans le menu de navigation de gauche, puis sélectionnez **[!UICONTROL Configuration]**.

1. Dans le menu Configuration, sélectionnez **[!UICONTROL Advanced > Admin]**, puis développez **[!UICONTROL Unified Experience option]**.

   ![Configuration de la boutique d’administration pour l’intégration des Experience Cloud](./assets/admin-uex-manage-settings.png){width="600" zoomable="yes"}

1. Activez ou désactivez l’intégration en sélectionnant la valeur **[!UICONTROL Enable]**.

1. Modifiez le nom du projet qui s’affiche dans l’espace de travail Projets Commerce en ajoutant ou en mettant à jour la valeur **[!UICONTROL Project Name]**.

1. Enregistrez la configuration.

1. Effacez le cache.

## Gestion de l’intégration à l’aide de l’interface de ligne de commande d’Adobe Commerce

Les administrateurs système Commerce ayant un accès administrateur au projet cloud Commerce peuvent utiliser les commandes de l’interface de ligne de commande d’Adobe Commerce pour gérer l’intégration de l’Experience Cloud.

1. Dans votre environnement de développement local, connectez-vous au projet cloud.

   ```bash
   magento-cloud login
   ```

1. Dans le répertoire racine de votre environnement de projet Cloud, connectez-vous au serveur d’applications Commerce.

   ```bash
   ssh magento-cloud
   ```

1. Vérifiez le statut de l’extension Admin Unified Experience :

   ```bash
   bin/magento admin:uex:status
   ```

1. Modifier l’état de l’extension pour désactiver l’intégration

   - **Activer**—`bin/magento config:set admin/unified_experience/enabled 1`

   - **Désactiver**—`bin/magento config:set admin/unified_experience/enabled 0`

## Gestion des comptes d’utilisateurs administrateur

Tous les utilisateurs administrateurs de Commerce doivent disposer d’un compte administrateur sur l’instance Commerce et d’un compte utilisateur d’Adobe (Adobe ID) pour accéder aux produits et services d’Adobe. Les deux comptes doivent être associés à la même adresse email.

- **Compte administrateur Commerce**—[Gérer les utilisateurs administrateurs Commerce](../systems/permissions-users-all.md) à partir de l’administrateur de l’instance Commerce. Les comptes utilisateur des administrateurs Commerce doivent se voir attribuer le rôle d’administrateur.

  Les administrateurs système du projet Commerce peuvent utiliser le protocole [SSH pour se connecter à l’environnement distant](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html?lang=fr#connect-to-a-remote-environment) et utiliser les commandes CLI `admin:user:create` et `admin:user:unlock` de Commerce pour ajouter ou déverrouiller des comptes utilisateurs Admin.

- **Compte utilisateur d’Adobe** : un administrateur de l’organisation d’Adobe associée à l’instance Commerce doit se connecter à Adobe Admin Console et ajouter l’Adobe ID pour chaque administrateur Commerce à l’organisation. Ensuite, ils doivent attribuer des droits et des autorisations sur les produits pour accéder à l’application Commerce. Voir [Configuration des utilisateurs Adobe Commerce dans Adobe Admin Console](adobe-ims-config.md#step-4-configure-adobe-commerce-users-in-the-adobe-admin-console).

Les administrateurs qui gèrent la configuration pour l’intégration des Experience Cloud à partir de Adobe Developer Console doivent disposer d’un compte utilisateur d’Adobe avec un accès Administrateur système ou Développeur.

>[!NOTE]
>
>Un Adobe ID est un compte créé par le biais d’un Adobe qui est nécessaire pour accéder aux produits et services par l’intermédiaire d’Experience Cloud. Les administrateurs Commerce qui ne disposent pas d’Adobe ID peuvent [ créer un compte gratuit ](https://helpx.adobe.com/fr/manage-account/using/create-update-adobe-id.html) à l’aide de la même adresse électronique que celle utilisée pour se connecter à l’administrateur Commerce.
