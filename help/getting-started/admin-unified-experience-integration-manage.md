---
title: Gestion de l’intégration Experience Cloud
description: Découvrez comment gérer l’intégration d’Experience Cloud et résoudre les problèmes
hide: false
hidefromtoc: false
feature: Integration
exl-id: 451bf2e1-7c38-40be-a7c1-aaf0fe9f486c
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 0%

---

# Gestion de l’intégration Experience Cloud

Après l’activation initiale, gérez le statut de l’intégration Experience Cloud en activant ou en désactivant l’extension Commerce Admin Unified Experience.

- Si l’extension Commerce Admin Unified Experience est activée et que les comptes d’administration sont [correctement configurés](#manage-admin-user-accounts), les administrateurs et administratrices Commerce peuvent afficher les projets Commerce disponibles et y accéder à partir de Adobe Experience Cloud. Les administrateurs peuvent toujours accéder à des projets individuels à l’aide de l’URL d’administration pour l’environnement de projet Commerce.

- Si l’extension Commerce Admin Unified Experience est désactivée, l’accès via Experience Cloud est désactivé. Les administrateurs doivent se connecter à des projets individuels à l’aide de l’URL d’administration pour l’environnement de projet Commerce.

>[!WARNING]
>
>Si l’intégration du service Adobe Identity Management (IMS) est désactivée, l’intégration d’Experience Cloud est automatiquement désactivée.

## Gérer l’intégration à partir de l’administrateur

1. Dans l’Administration de Commerce, ouvrez le menu Configuration de la boutique en sélectionnant **[!UICONTROL Stores]** dans le menu de navigation de gauche, puis sélectionnez **[!UICONTROL Configuration]**.

1. Dans le menu Configuration , sélectionnez **[!UICONTROL Advanced > Admin]**, puis développez le **[!UICONTROL Unified Experience option]** .

   ![Configuration de magasin d’administration pour l’intégration d’Experience Cloud](./assets/admin-uex-manage-settings.png){width="600" zoomable="yes"}

1. Activez ou désactivez l’intégration en sélectionnant la valeur **[!UICONTROL Enable]**.

1. Modifiez le nom du projet qui s’affiche dans l’espace de travail Projets Commerce en ajoutant ou en mettant à jour la valeur **[!UICONTROL Project Name]**.

1. Enregistrez la configuration.

1. Effacez le cache.

## Gérer l’intégration à l’aide de l’interface de ligne de commande d’Adobe Commerce

Les administrateurs système Commerce disposant d’un accès administrateur au projet cloud Commerce peuvent utiliser les commandes de l’interface de ligne de commande Adobe Commerce pour gérer l’intégration d’Experience Cloud.

1. Connectez-vous au projet cloud à partir de votre environnement de développement local.

   ```bash
   magento-cloud login
   ```

1. Dans le répertoire racine de votre environnement de projet cloud, connectez-vous au serveur d’applications Commerce.

   ```bash
   ssh magento-cloud
   ```

1. Vérifiez le statut de l’extension Admin Unified Experience :

   ```bash
   bin/magento admin:uex:status
   ```

1. Modifiez le statut de l’extension pour désactiver l’intégration

   - **Activer**—`bin/magento config:set admin/unified_experience/enabled 1`

   - **Désactiver**—`bin/magento config:set admin/unified_experience/enabled 0`

## Gestion des comptes utilisateur d’administration

Tous les utilisateurs administrateurs de Commerce doivent disposer d’un compte administrateur sur l’instance Commerce et d’un compte utilisateur Adobe (Adobe ID) pour accéder aux produits et services Adobe. Les deux comptes doivent être associés à la même adresse e-mail.

- **Compte d’administrateur Commerce**—[Gérez les utilisateurs Commerce Admin](../systems/permissions-users-all.md) à partir de l’administrateur de l’instance Commerce. Le rôle Administrateur doit être attribué aux comptes utilisateur des administrateurs Commerce.

  Les administrateurs système du projet Commerce peuvent utiliser [SSH pour se connecter à l’environnement distant](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html?lang=fr#connect-to-a-remote-environment) et utiliser le `admin:user:create` de l’interface de ligne de commande Commerce et les commandes `admin:user:unlock` pour ajouter ou déverrouiller des comptes utilisateur d’administration.

- **Compte utilisateur Adobe**—Un administrateur de l&#39;organisation Adobe associée à l&#39;instance Commerce doit se connecter au Adobe Admin Console et ajouter l&#39;Adobe ID de chaque administrateur Commerce à l&#39;organisation. Ensuite, ils doivent attribuer des droits et des autorisations de produit pour accéder à l’application Commerce. Voir [ Configuration des utilisateurs d’Adobe Commerce dans Adobe Admin Console](adobe-ims-config.md#step-4-configure-adobe-commerce-users-in-the-adobe-admin-console).

Les administrateurs qui gèrent la configuration pour l’intégration d’Experience Cloud à partir de Adobe Developer Console doivent disposer d’un compte utilisateur Adobe avec un accès d’administrateur système ou de développeur.

>[!NOTE]
>
>Un Adobe ID est un compte créé via Adobe qui est nécessaire pour accéder aux produits et services via Experience Cloud. Les administrateurs Commerce qui ne disposent pas d’Adobe ID peuvent [créer un compte gratuit](https://helpx.adobe.com/fr/manage-account/using/create-update-adobe-id.html) utiliser la même adresse e-mail que celle qu’ils utilisent pour se connecter à l’administrateur Commerce.
