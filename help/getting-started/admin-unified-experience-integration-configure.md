---
title: Configuration de l’intégration Experience Cloud pour l’administrateur Commerce
description: Découvrez comment configurer un projet Commerce pour activer l’accès administrateur via Experience Cloud.
hide: false
hidefromtoc: false
feature: Integration
role: Admin, Leader
exl-id: b2522d25-8255-4219-98b5-4b764430dea2
source-git-commit: 8278d725a7377b865c118b86a57702cd2be43238
workflow-type: tm+mt
source-wordcount: '1011'
ht-degree: 0%

---

# Configuration de l’intégration Experience Cloud avec l’administrateur Commerce

Commencez avec l’intégration de l’Experience Cloud avec Commerce Admin en configurant l’application Commerce pour utiliser les extensions Commerce Admin Unified Experience et Commerce Events.


## Conditions préalables

- Adobe Commerce doit être configuré pour utiliser l’ [authentification Adobe IMS](../getting-started/adobe-ims-config.md)
- Approvisionnement des comptes et autorisations : les administrateurs doivent disposer d’un [profil d’entreprise Adobe](https://helpx.adobe.com/fr/enterprise/kb/introducing-adobe-profiles.html#:~:text=Adobe%20profiles%20help%20you%20manage,under%20the%20same%20email%20address) avec accès aux ressources suivantes pour configurer l’intégration Experience Cloud :
   - [Adobe Admin Console](https://helpx.adobe.com/fr/enterprise/admin-guide.html) : ajoutez et gérez des comptes utilisateurs et développeurs d’Adobes pour l’organisation.
   - [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/getting-started/) : accès développeur ou administrateur système pour créer des projets App Builder et générer les informations d’identification de connexion et la configuration de projet afin d’utiliser le service Adobe I/O Events
   - [Commerce sur le projet d’infrastructure cloud](https://experienceleague.adobe.com/docs/commerce-cloud-service/start/onboarding.html?lang=fr#get-started-with-the-project-web-interface) : installez les modules requis et configurez le serveur d’applications Commerce à l’aide de l’interface de ligne de commande Adobe Commerce.
   - [Administrateur Commerce](https://experienceleague.adobe.com/docs/commerce-admin/start/guide-overview.html?lang=fr) : mettez à jour la configuration du magasin et gérez les comptes utilisateur Commerce

## Présentation de la configuration

Activez l’intégration en effectuant les tâches suivantes :

1. [Vérifiez la configuration de l’environnement et de l’application Commerce](#check-the-commerce-environment-and-application-configuration).

1. [Activez l’extension Commerce Admin Unified Experience](#enable-the-commerce-admin-unified-experience-extension).

1. [Configuration des événements d’Adobe I/O pour Commerce](#set-up-adobe-io-events).

1. [Testez l’intégration](#test-the-integration).

## Vérification de la configuration de l’environnement et de l’application Commerce

Avant de configurer l’intégration de l’Experience Cloud, vérifiez que votre projet et votre application Commerce répondent aux exigences.

1. Sur votre poste de travail local, modifiez le répertoire du projet pour votre projet Commerce.

1. Consultez la branche d’environnement pour que l’instance s’intègre à Experience Cloud.

1. Vérifiez qu’Adobe IMS est activé.

   - Utilisez l’ [ URL d’accès SSH](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html?lang=fr) pour que l’environnement se connecte au serveur d’applications Commerce.

   - Dans la ligne de commande, utilisez l’interface de ligne de commande Adobe Commerce pour vérifier l’état du module IMS.

     ```bash
     bin/magento admin:adobe-ims:status
     ```

   Si le module n’est pas activé, [activez-le à l’aide de l’organisation et des informations d’identification pour le projet d’intégration IMS](../getting-started/adobe-ims-config.md#step-3-enable-the-adminadobeims-module).

1. Vérifiez que l’utilisateur administrateur peut se connecter à l’administrateur Commerce à l’aide de son Adobe ID.

   - Accédez à l’URL d’administration de Commerce.

   - Si vous êtes connecté, déconnectez-vous.

   - Assurez-vous que l’utilisateur administrateur est redirigé pour se connecter à l’aide de son Adobe ID.

     ![Connexion Adobe Commerce à l’aide d’Adobe ID](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

1. Dans le répertoire du projet cloud sur votre poste de travail local, vérifiez que l’extension Commerce Admin Unified Experience est installée.

   ```bash
   composer show *unified-experience*
   ```

   Si l’extension est installée, le compositeur renvoie le nom et la description de l’extension.

   ```
   magento/module-unified-experience <version> Commerce module responsible for integration with Adobe Experience Cloud
   ```

   Si l’extension n’est pas installée, utilisez le compositeur pour l’installer. Ensuite, validez les modifications et redéployez l’environnement cloud.

   ```
   composer require magento/module-unified-experience
   composer update
   ```

## Activation de l’expérience Commerce Admin Unifié

Activez l’extension Commerce Admin Unified Experience (Expérience unifiée d’administration de), puis connectez-vous via Experience Cloud.

>[!NOTE]
>
>Ces instructions indiquent comment un administrateur de projet Commerce Cloud peut activer l’extension à l’aide de l’interface de ligne de commande d’Adobe Commerce. Les utilisateurs administrateurs de Commerce peuvent également activer l’extension en mettant à jour les [paramètres de configuration du magasin Commerce](admin-unified-experience-integration-manage.md#from-the-commerce-admin).

1. Dans le répertoire racine de votre environnement de projet Cloud sur votre poste de travail local, utilisez l’[outil d’interface de ligne de commande magento-cloud](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/dev-tools/cloud-cli/cloud-cli-overview.html?lang=fr) pour vous connecter au serveur d’applications Commerce.

   ```bash
   magento-cloud ssh
   ```

1. Activez l’extension `magento/module-unified-experience` à l’aide de l’interface de ligne de commande Adobe Commerce :

   ```bash
   bin/magento config:set admin/unified_experience/enabled 1
   Admin Unified Experience integration is enabled
   ```

1. Effacez le cache.

   ```bash
   bin/magento cache:clean
   ```

## Configuration des événements d’Adobe I/O pour Commerce

Lorsque l’intégration Experience Cloud est activée, le service Adobe I/O Events envoie les données d’événement Commerce à l’Experience Cloud pour gérer l’accès administrateur aux projets Commerce. La configuration du service nécessite l’activation de l’extension Adobe I/O Events pour Commerce (`magento/commerce-eventing`) et la configuration du service Adobe I/O Events dans l’administrateur.

### Activation des événements Commerce

Activez l’extension Commerce Events (`magento/commerce-eventing`) pour envoyer des données d’événement personnalisé de l’application Commerce au service Adobe I/O Events.

>[!NOTE]
>
>Pour Commerce 2.4.6 et versions ultérieures, l’extension Commerce Events est installée par défaut. Pour les projets Commerce avec Commerce 2.4.5, utilisez d’abord le compositeur pour [installer l’extension](https://developer.adobe.com/commerce/extensibility/events/installation/#install-adobe-io-modules-on-commerce), puis activez-la.

1. Depuis votre environnement de développement de projet Commerce local, ajoutez la configuration suivante au fichier `.magento.env.yaml`.

   ```yaml
   stage:
     global:
       ENABLE_EVENTING: true
     deploy:
       CRON_CONSUMERS_RUNNER:
         cron_run: true
         max_messages: 0
         consumers: []
   ```

1. Ajoutez, validez et déployez le `.magento.env.yaml file` mis à jour dans l’environnement cloud.

>[!TIP]
>
>Pour plus d’informations sur la configuration et la gestion des variables d’environnement à l’aide du fichier `.magento.env.yaml`, voir [ Configuration des variables d’environnement pour le déploiement](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/configure-env-yaml.html?lang=fr).

### Configuration de l’intégration des événements Commerce

Configurez l’intégration des événements Commerce en effectuant les tâches suivantes. Pour obtenir des instructions détaillées, reportez-vous à la documentation du développeur [Événements d’Adobe I/O pour Commerce](https://developer.adobe.com/commerce/extensibility/events/project-setup/) .

1. [Créez un projet App Builder](https://developer.adobe.com/commerce/extensibility/events/project-setup/) pour recevoir les données d’événement de l’instance Commerce.

   Vous avez besoin des informations d’identification et des données de configuration du projet App Builder pour configurer l’intégration dans Commerce Admin.

1. Configurez Adobe Commerce pour utiliser les événements Adobe I/O.

   - [ Mettez à jour les paramètres de configuration de magasin pour le service Adobe I/O Events ](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#begin-configuring-events-on-commerce).

   - [Configurez un fournisseur d’événements pour envoyer des événements Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#create-an-event-provider-and-complete-the-commerce-configuration).

1. [Mettez à jour le projet App Builder pour recevoir les données d’événement de l’instance Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#subscribe-and-register-events).

   Ne vous abonnez pas aux événements de l’instance Commerce ou ne vous en abonnez pas. L’enregistrement de l’événement est transmis au projet App Builder lorsque vous configurez le fournisseur d’événements pour l’application Commerce.

   Après la connexion du fournisseur d’événements au projet App Builder, abonnez-vous à l’événement `observer.uex_commerce_instance_update` et enregistrez les modifications.

1. Pour établir la connexion, envoyez un événement au consommateur via le fournisseur d’événements.

   - À partir de la ligne de commande du répertoire de projet cloud local, [utilisez SSH pour vous connecter au serveur d’applications Commerce](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html?lang=fr#connect-to-a-remote-environment).

     ```bash
     magento-cloud ssh
     ```

   - Envoyez des données d’événement en vérifiant l’état de l’extension Admin Unified Experience à l’aide de l’interface de ligne de commande d’Adobe Commerce.

     ```bash
     bin/magento bin/magento admin:uex:status
     ```

### Test de l’intégration

Vérifiez qu’un administrateur Commerce peut se connecter à l’Experience Cloud pour afficher les projets Commerce disponibles et accéder à l’Admin et à Storefront pour chaque projet.

1. [Connectez-vous à Experience Cloud](https://experiencecloud.adobe.com/library) à l’aide de l’Adobe ID et de l’organisation associés à l’instance Commerce.

   ![Accès aux projets Commerce à partir de la page d’accueil de l’Experience Cloud](./assets/admin-uex-home-page.png){width="600" zoomable="yes"}

1. Affichez les projets Commerce disponibles en sélectionnant **[!UICONTROL Commerce]**.

   ![Espace de travail Commerce Projects pour l’Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="600" zoomable="yes"}

1. Ouvrez l’administrateur d’une instance en sélectionnant **[!UICONTROL Open]**.

   ![Vue d’administration Commerce avec intégration de l’Experience Cloud activée](./assets/admin-dashboard.png){width="600" zoomable="yes"}

1. Vérifiez que vous pouvez effectuer les tâches d’administration comme prévu.

   Les workflows de l’administrateur Commerce doivent suivre le même processus. Si vous rencontrez des modifications ou des erreurs de workflow après l’activation de l’intégration de l’Experience Cloud, contactez votre administrateur système Commerce ou [ envoyez un ticket d’assistance à l’Adobe ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=fr#submit-ticket).

Une fois l’intégration de l’Experience Cloud configurée, vérifiez que les comptes d’administrateur sont configurés correctement pour accéder aux projets Commerce via Experience Cloud. Voir [Gérer les utilisateurs administrateurs](/help/getting-started/admin-unified-experience-integration-manage.md#manage-admin-user-accounts).
