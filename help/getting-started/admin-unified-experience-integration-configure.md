---
title: Configuration de l’intégration Experience Cloud pour l’administrateur Commerce
description: Découvrez comment configurer un projet Commerce pour activer l’accès administrateur via Experience Cloud.
hide: false
hidefromtoc: false
feature: Integration
role: Admin, Leader
exl-id: b2522d25-8255-4219-98b5-4b764430dea2
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 0%

---

# Configuration de l’intégration d’Experience Cloud avec l’administrateur Commerce

Commencez avec l’intégration d’Experience Cloud à Commerce Admin en configurant l’application Commerce pour utiliser les extensions Commerce Admin Unified Experience et Commerce Events .


## Conditions préalables

- Adobe Commerce doit être configuré pour utiliser [l’authentification Adobe IMS](../getting-started/adobe-ims-config.md)
- Approvisionnement de compte et autorisations : les administrateurs doivent disposer d’un [profil commercial Adobe](https://helpx.adobe.com/enterprise/kb/introducing-adobe-profiles.html#:~:text=Adobe%20profiles%20help%20you%20manage,under%20the%20same%20email%20address) avec un accès aux ressources suivantes pour configurer l’intégration Experience Cloud :
   - [Adobe Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html) : ajoutez et gérez des comptes d’utilisateur et de développeur Adobe pour l’organisation.
   - [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/getting-started/)—Accès développeur ou administrateur système pour la création de projets App Builder et la génération des informations d&#39;identification de connexion et de la configuration du projet pour utiliser le service Adobe I/O Events
   - [Commerce sur un projet d’infrastructure cloud ](https://experienceleague.adobe.com/docs/commerce-cloud-service/start/onboarding.html#get-started-with-the-project-web-interface)—Installez les modules requis et configurez le serveur d’applications Commerce à l’aide de l’interface de ligne de commande Adobe Commerce
   - [Commerce Admin](https://experienceleague.adobe.com/docs/commerce-admin/start/guide-overview.html)—Mise à jour de la configuration du magasin et gestion des comptes utilisateur Commerce

## Présentation de la configuration

Activez l’intégration en effectuant les tâches suivantes :

1. [Vérifiez l’environnement Commerce et la configuration de l’application](#check-the-commerce-environment-and-application-configuration).

1. [Activez l’extension Commerce Admin Unified Experience](#enable-the-commerce-admin-unified-experience-extension).

1. [Configurer Adobe I/O Events pour Commerce](#set-up-adobe-io-events).

1. [Tester l’intégration](#test-the-integration).

## Vérifier l’environnement Commerce et la configuration de l’application

Avant de configurer l’intégration d’Experience Cloud, vérifiez que votre projet et l’application Commerce répondent aux exigences.

1. Sur votre station de travail locale, accédez au répertoire du projet Commerce.

1. Consultez la branche d’environnement pour l’instance à intégrer à Experience Cloud.

1. Vérifiez qu’Adobe IMS est activé.

   - Utilisez l’[URL d’accès SSH](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html) pour que l’environnement se connecte au serveur d’applications Commerce.

   - À partir de la ligne de commande, utilisez l’interface de ligne de commande Adobe Commerce pour vérifier l’état du module IMS.

     ```bash
     bin/magento admin:adobe-ims:status
     ```

   Si le module n’est pas activé, [activez-le à l’aide de l’organisation et des informations d’identification pour le projet d’intégration IMS](../getting-started/adobe-ims-config.md#step-3-enable-the-adminadobeims-module).

1. Vérifiez que l’utilisateur administrateur peut se connecter à l’administrateur Commerce à l’aide de son Adobe ID.

   - Accédez à l’URL d’administration Commerce.

   - Si vous êtes connecté, déconnectez-vous.

   - Vérifiez que l’utilisateur administrateur est redirigé vers pour se connecter à l’aide de son Adobe ID.

     ![Connexion à Adobe Commerce à l’aide d’Adobe ID](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

1. Dans le répertoire du projet cloud de votre station de travail locale, vérifiez que l’extension Commerce Admin Unified Experience est installée.

   ```bash
   composer show *unified-experience*
   ```

   Si l’extension est installée, Composer renvoie le nom et la description de l’extension.

   ```
   magento/module-unified-experience <version> Commerce module responsible for integration with Adobe Experience Cloud
   ```

   Si l’extension n’est pas installée, utilisez le compositeur pour l’installer. Ensuite, validez les modifications et redéployez l’environnement cloud.

   ```
   composer require magento/module-unified-experience
   composer update
   ```

## Activer l’expérience unifiée d’administration Commerce

Activez l’extension Commerce Admin Unified Experience , puis connectez-vous via Experience Cloud.

>[!NOTE]
>
>Ces instructions expliquent comment un administrateur de projet Commerce Cloud peut activer l’extension à l’aide de l’interface de ligne de commande Adobe Commerce. Les utilisateurs administrateurs de Commerce peuvent également activer l’extension en mettant à jour les paramètres de configuration de la boutique Commerce [&#128279;](admin-unified-experience-integration-manage.md#from-the-commerce-admin).

1. À partir du répertoire racine de votre environnement de projet cloud sur votre station de travail locale, utilisez l’outil [Magento-cloud CLI](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/dev-tools/cloud-cli/cloud-cli-overview.html) pour vous connecter au serveur d’applications Commerce.

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

## Configuration de Adobe I/O Events pour Commerce

Lorsque l’intégration d’Experience Cloud est activée, le service Adobe I/O Events envoie des données d’événement Commerce à Experience Cloud afin de gérer l’accès administrateur aux projets Commerce. La configuration du service nécessite l’activation de l’extension Adobe I/O Events for Commerce (`magento/commerce-eventing`) et la configuration du service Adobe I/O Events dans l’administration.

### Activer les événements Commerce

Activez l’extension Commerce Events (`magento/commerce-eventing`) pour envoyer des données d’événement personnalisées de l’application Commerce au service Adobe I/O Events.

>[!NOTE]
>
>Pour Commerce 2.4.6 et les versions ultérieures, l’extension Commerce Events est installée par défaut. Pour les projets Commerce avec Commerce 2.4.5, utilisez d’abord le compositeur pour [installer l’extension](https://developer.adobe.com/commerce/extensibility/events/installation/#install-adobe-io-modules-on-commerce), puis activez-la.

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

1. Ajoutez, validez et déployez les `.magento.env.yaml file` mises à jour dans l’environnement cloud.

>[!TIP]
>
>Pour plus d’informations sur la configuration et la gestion des variables d’environnement à l’aide du fichier `.magento.env.yaml`, voir [Configurer des variables d’environnement pour le déploiement](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/configure-env-yaml.html).

### Configuration de l’intégration des événements Commerce

Configurez l’intégration des événements Commerce en effectuant les tâches suivantes. Pour obtenir des instructions détaillées, consultez la documentation destinée aux développeurs de [Adobe I/O Events for Commerce](https://developer.adobe.com/commerce/extensibility/events/project-setup/).

1. [Créez un projet App Builder](https://developer.adobe.com/commerce/extensibility/events/project-setup/) pour recevoir des données d’événement de l’instance Commerce.

   Vous avez besoin des informations d’identification et des données de configuration du projet App Builder pour configurer l’intégration dans Commerce Admin.

1. Configurez Adobe Commerce pour utiliser Adobe I/O Events.

   - [Mettez à jour les paramètres de configuration de la boutique pour le service Adobe I/O Events](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#begin-configuring-events-on-commerce).

   - [Configurer un fournisseur d’événements pour envoyer des événements Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#create-an-event-provider-and-complete-the-commerce-configuration).

1. [Mettez à jour le projet App Builder pour recevoir des données d’événement de l’instance Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#subscribe-and-register-events).

   Ne vous inscrivez pas aux événements de l’instance Commerce et ne vous y abonnez pas. L’enregistrement de l’événement est transmis au projet App Builder lorsque vous configurez le fournisseur d’événement pour l’application Commerce.

   Après avoir connecté le fournisseur d’événements au projet App Builder, abonnez-vous à l’événement `observer.uex_commerce_instance_update` et enregistrez les modifications.

1. Pour établir la connexion, envoyez un événement au client par l’intermédiaire du fournisseur d’événements.

   - Sur la ligne de commande du répertoire du projet cloud local, [utilisez SSH pour vous connecter au serveur d’applications Commerce](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment).

     ```bash
     magento-cloud ssh
     ```

   - Envoyez des données d’événement en vérifiant le statut de l’extension Expérience unifiée d’administration à l’aide de l’interface de ligne de commande Adobe Commerce.

     ```bash
     bin/magento bin/magento admin:uex:status
     ```

### Tester l’intégration

Vérifiez qu’un administrateur Commerce peut se connecter à Experience Cloud pour afficher les projets Commerce disponibles et accéder à l’administration et au storefront pour chaque projet.

1. [Connectez-vous à Experience Cloud](https://experiencecloud.adobe.com/library) à l’aide de l’Adobe ID et de l’organisation associées à l’instance Commerce.

   ![Accédez aux projets Commerce à partir de la page d’accueil Experience Cloud](./assets/admin-uex-home-page.png){width="600" zoomable="yes"}

1. Affichez les projets Commerce disponibles en sélectionnant **[!UICONTROL Commerce]**.

   Espace de travail ![Projets Commerce pour Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="600" zoomable="yes"}

1. Ouvrez l’Administration d’une instance en sélectionnant **[!UICONTROL Open]**.

   ![Vue d’administration Commerce avec l’intégration Experience Cloud activée](./assets/admin-dashboard.png){width="600" zoomable="yes"}

1. Vérifiez que vous pouvez effectuer les tâches d’administration comme prévu.

   Les workflows de l’administrateur Commerce doivent suivre le même processus. Si des modifications ou des erreurs surviennent dans le workflow après l’activation de l’intégration Experience Cloud, contactez votre administrateur système Commerce ou [envoyez un ticket d’assistance Adobe](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket).

Après avoir configuré l’intégration d’Experience Cloud, vérifiez que les comptes d’administration sont correctement configurés pour accéder aux projets Commerce via Experience Cloud. Voir [ Gérer les utilisateurs administrateurs ](/help/getting-started/admin-unified-experience-integration-manage.md#manage-admin-user-accounts).
