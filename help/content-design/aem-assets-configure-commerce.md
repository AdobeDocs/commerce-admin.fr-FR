---
title: Installation et configuration de l’intégration Experience Manager Assets
description: "Découvrez comment installer et configurer le  [!DNL AEM Assets Integration for Adobe Commerce]"
feature: CMS, Media
source-git-commit: 65a4339f0f6d4e9eb280ce90d6173caf671fde0f
workflow-type: tm+mt
source-wordcount: '1261'
ht-degree: 0%

---

# Installation et configuration de l’intégration AEM Assets pour Commerce

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Installez et configurez l’intégration AEM Assets pour Commerce en ajoutant l’extension à l’application Commerce, en vous connectant aux services SaaS Commerce, au service Événements d’Adobe I/O et en vous connectant au SaaS Commerce.

## Configuration requise

**Exigences logicielles**

- Adobe Commerce 2.4.5+
- PHP 8.1, 8.2, 8.3
- Compositeur : 2.x

**Configuration requise**

- Adobe Commerce doit être configuré pour utiliser l’ [authentification Adobe IMS](/help/getting-started/adobe-ims-config.md).
- Approvisionnement et autorisations des comptes
   - [Administrateur de projet cloud Commerce](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access) : installez les extensions requises et configurez le serveur d’applications Commerce à partir de l’administrateur ou de la ligne de commande.
   - [Administrateur Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/start/guide-overview) : mettez à jour la configuration du magasin et gérez les comptes utilisateur Commerce

## Présentation de la configuration

Activez l’intégration en effectuant les tâches suivantes :

1. [Installez l’extension d’intégration AEM Assets (`aem-assets-integration`)](#install-the-aem-assets-integration-extension).
1. [Configurez le connecteur de service Commerce](#configure-the-commerce-services-connector) pour connecter votre instance Adobe Commerce et avec les services qui permettent la transmission des données entre Adobe Commerce et AEM Assets.
1. [Configuration des événements d’Adobe I/O pour Commerce](#configure-adobe-io-events-for-commerce)
1. [Obtention des informations d’authentification pour l’accès aux API](#get-authentication-credentials-for-api-access)

## Installation de l’extension AEM Assets Integration

>[!BEGINSHADEBOX]

**Condition préalable requise**

- Accédez à [repo.magento.com](https://repo.magento.com/admin/dashboard) pour installer l’extension. Pour la génération des clés et l’obtention des droits nécessaires, voir [Obtention de vos clés d’authentification](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys). Pour les installations dans le cloud, consultez le [Guide de l’infrastructure de Commerce on Cloud](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/authentication-keys)

- Accès à la ligne de commande du serveur applicatif Adobe Commerce.

>[!ENDSHADEBOX]

Installez la dernière version de l’extension d’intégration AEM Assets (`aem-assets-integration`) sur un Adobe Commerce exécutant Adobe Commerce 2.4.4 ou version ultérieure. L’intégration d’AEM Asset est diffusée en tant que métapaquet de compositeur à partir du référentiel [repo.magento.com](https://repo.magento.com/admin/dashboard).

>[!BEGINTABS]

>[!TAB Infrastructure cloud]

Utilisez cette méthode pour installer l’extension [!DNL AEM Assets Integration] pour une instance de Commerce Cloud.

1. Sur votre poste de travail local, modifiez le répertoire du projet pour votre projet Adobe Commerce sur l’infrastructure cloud.

   >[!NOTE]
   >
   >Pour plus d’informations sur la gestion locale des environnements de projet Commerce, voir [Gestion des branches avec l’interface de ligne de commande](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) dans le _Guide de l’utilisateur d’Adobe Commerce on Cloud Infrastructure_.

1. Consultez la branche d’environnement pour mettre à jour à l’aide de l’interface de ligne de commande de Adobe Commerce Cloud.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Ajoutez l’extension AEM Assets Integration for Commerce .

   ```shell
   composer require "magento/aem-assets-integration" "<version-tbd>" --no-update
   ```

1. Mettez à jour les dépendances de package.

   ```shell
   composer update "magento/aem-assets-integration"
   ```

1. Validez et poussez les modifications de code pour les fichiers `composer.json` et `composer.lock`.

1. Ajoutez, validez et poussez les modifications de code des fichiers `composer.json` et `composer.lock` dans l’environnement cloud.

   ```shell
   git add -A
   git commit -m "Install AEM Assets Integration extension for Adobe Commerce"
   git push origin <branch-name>
   ```

   La publication des mises à jour déclenche le [processus de déploiement cloud de Commerce](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) pour appliquer les modifications. Vérifiez l’état du déploiement à partir du [log de déploiement](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

>[!TAB Sur site]

Utilisez cette méthode pour installer l’extension [!DNL AEM Assets Integration] pour une instance sur site.

1. Utilisez le compositeur pour ajouter l’extension AEM Assets Integration for Commerce à votre projet :

   ```shell
   composer require "magento/aem-assets-integration" --no-update
   ```

1. Mettez à jour les dépendances et installez l’extension :

   ```shell
   composer update  "magento/aem-assets-integration"
   ```

1. Mettre à niveau Adobe Commerce :

   ```shell
   bin/magento setup:upgrade
   ```

1. Effacez le cache :

   ```shell
   bin/magento cache:clean
   ```

   >[!TIP]
   >
   >Dans certains cas, en particulier lors du déploiement en production, vous souhaiterez peut-être éviter de supprimer le code compilé, car cela peut prendre du temps. Assurez-vous de sauvegarder votre système avant d’apporter des modifications.

>[!ENDTABS]

## Configuration du connecteur Commerce Services

Commerce Services Connector permet la synchronisation et la communication des données entre l’instance Commerce, le service Asset Rule Engine et d’autres services de prise en charge.

>[!NOTE]
>
>La configuration de Commerce Services Connector est un processus unique requis pour utiliser les [services Adobe Commerce SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas#availableservices). Si vous avez déjà configuré le connecteur pour un autre service, vous pouvez afficher la configuration existante à partir de l’administrateur Commerce en sélectionnant **[!UICONTROL Systems]** > [!UICONTROL Services] > **[!UICONTROL Commerce Services Connector]**.

Pour transmettre des données entre votre instance Adobe Commerce et les services qui activent l’intégration AEM Assets, configurez le Connecteur de services Commerce avec les éléments suivants :

- Configurez votre instance Commerce avec les clés d’API de production et d’environnement de test pour l’authentification.
- Spécifiez un espace de données (identifiant SaaS) pour le stockage sécurisé dans le cloud.
- Connectez-vous à la même organisation IMS que celle que vous utilisez pour accéder à AEM Assets afin d’établir la connexion entre votre jeu de données et Adobe Experience Platform.

Pour obtenir des instructions détaillées, reportez-vous à la section [Connecteur de services Commerce](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas#organizationid).

Lorsque vous configurez Commerce Services Connector, le système génère les identifiants de projet SaaS et de base de données. Vous avez besoin de ces identifiants lors du processus d’intégration du client.

![ID de projet SaaS et d’espace de données pour l’intégration AEM Assets](assets/aem-saas-project-config.png){width="600" zoomable="yes"}

## Configuration des événements d’Adobe I/O pour Commerce

L’intégration AEM Assets utilise le service Adobe I/O Events pour envoyer des données d’événement personnalisé entre l’instance Commerce et l’Experience Cloud. Les données d’événement sont utilisées pour coordonner les workflows pour l’intégration d’AEM Assets.

>[!BEGINSHADEBOX]

**Condition préalable requise**

- Assurez-vous que RabbitMQ est activé et que vous écoutez les événements.
   - [Configuration de RabbitMQ pour Adobe Commerce sur site](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/rabbitmq)
   - [Configuration de RabbitMQ pour Adobe Commerce sur l’infrastructure cloud](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/rabbitmq)

>[!ENDSHADEBOX]

>[!NOTE]
>
>Pour plus d’informations sur les événements d’Adobe I/O pour Commerce, consultez la documentation [Événements d’Adobe I/O pour Commerce](https://developer.adobe.com/commerce/extensibility/events/) sur le site Adobe Developer.

La configuration requiert les étapes suivantes.

1. Activez la structure Commerce Eventing en configurant les événements d’Adobe I/O sur le serveur d’applications et dans l’administrateur.
1. Activez la synchronisation des données entre Adobe Commerce et AEM Assets à l’aide de l’API Assets Rules Engine Service pour configurer la connexion.
1. Activez l’intégration d’AEM Assets dans Admin.

### Activation de la structure Eventing de Commerce

Activez la structure d’événement Commerce en suivant les instructions de l’environnement dans lequel votre projet Commerce est déployé.

>[!BEGINTABS]

>[!TAB Infrastructure cloud]

1. Activez le service Adobe I/O Events dans le menu [!DNL Store Settings Configuration].

   1. Depuis l’administrateur, accédez à **[!UICONTROL Stores]** > [!UICONTROL Settings] > **[!UICONTROL Configuration]** > **[!UICONTROL Adobe Services]** > **Événements d’Adobe I/O**.

   1. Développez **[!UICONTROL Commerce events]**.

   1. Définissez **[!UICONTROL Enabled]** sur `Yes`.

      ![Configuration d’administration Commerce des événements d’Adobe I/O - activer les événements Commerce](assets/aem-enable-io-event-admin-config.png){width="600" zoomable="yes"}

      >[!NOTE]
      >
      >[Activez cron](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#check-cron-and-message-queue-configuration) afin que Commerce puisse envoyer des événements aux points de terminaison de l’API pour gérer les processus et communications pour l’intégration.

1. Mettez à jour la configuration du projet cloud.

   1. Ajoutez le fichier `app/etc/config.php` à votre référentiel de travail :

   ```shell
   git add app/etc/config.php
   ```

   1. Exécutez la commande `composer info magento/ece-tools` pour déterminer votre version des outils de l’environnement de test. Si la version est inférieure à `2002.1.13`, [mettez à jour vers la version la plus récente](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/dev-tools/ece-tools/update-package).

   1. Activez les événements dans le fichier `.magento.env.yaml` :

      ```yaml
      stage:
         global:
            ENABLE_EVENTING: true
      ```

   1. Validez et envoyez les fichiers mis à jour dans l’environnement cloud.

>[!TAB Sur site]

1. Activez le service Adobe I/O Events dans le menu [!DNL Store Settings Configuration].

   1. Depuis l’administrateur, accédez à **[!UICONTROL Stores]** > [!UICONTROL Settings] > **[!UICONTROL Configuration]** > **[!UICONTROL Adobe Services]** > **Événements d’Adobe I/O**.

   1. Développez **[!UICONTROL Commerce events]**.

   1. Définissez **[!UICONTROL Enabled]** sur `Yes`.

      ![Configuration d’administration Commerce des événements d’Adobe I/O - activer les événements Commerce](assets/aem-enable-io-event-admin-config.png){width="600" zoomable="yes"}

      >[!NOTE]
      >
      >[ Activez les tâches cron ](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#check-cron-and-message-queue-configuration) afin que Commerce puisse envoyer des événements pour gérer la communication et les workflows entre les ressources AEM et Commerce.

>[!ENDTABS]

## Obtention des informations d’authentification pour l’accès aux API

L’intégration AEM Assets pour Commerce requiert des informations d’identification d’authentification OAuth pour permettre l’accès de l’API à l’instance Commerce. Vous avez besoin de ces informations d’identification pour enregistrer le projet Commerce auprès du service Assets Rule Engine lors de l’intégration du client et pour envoyer des demandes d’API pour gérer les ressources entre Adobe Commerce et AEM Assets.

Pour générer les informations d’identification, ajoutez l’intégration à l’instance Commerce et activez-la.

### Ajout de l’intégration à l’environnement Commerce

1. Depuis l’administrateur, accédez à **Système** > Extensions > **Intégrations**, puis cliquez sur **Ajouter une nouvelle intégration**.

1. Saisissez des informations sur l’intégration.

   Dans la section **Général**, spécifiez uniquement l&#39;intégration **Nom** et **Email**. Utilisez l’e-mail d’un compte Adobe IMS avec accès à l’organisation dans laquelle Commerce et Experience Manager Assets sont déployés.

   ![Intégration AEM Assets pour la configuration d’administration Commerce](assets/aem-add-commerce-integration.png){width="600" zoomable="yes"}

1. Vérifiez votre identité en cliquant sur **Confirmer l’identité**.

   Le système vérifie votre identité en s’authentifiant auprès de l’Experience Cloud avec votre ID d’Adobe.

1. Configurez les ressources d’API.

   1. Dans le panneau de gauche, cliquez sur **[!UICONTROL API]**.
E
   1. Sélectionnez la ressource de média externe **[!UICONTROL Catalog > Inventory > Products > External Media]**.

   ![Configuration de l’intégration d’administrateur pour les ressources d’API](assets/aem-commerce-integration-api-resources.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save]**.

### Génération des informations d’identification

Sur la page Intégrations, générez les informations d’identification d’authentification OAuth en cliquant sur **Activer** pour l’intégration Assets. Vous avez besoin de ces informations d’identification pour enregistrer le projet Commerce avec le service Assets Rule Engine et pour envoyer des demandes d’API pour gérer des ressources entre Adobe Commerce et AEM Assets.

1. Sur la page Intégrations , générez les informations d’identification en cliquant sur **[!UICONTROL Activate]**.

   ![Activer la configuration Commerce pour l’intégration Assets](assets/aem-activate-commerce-integration.png){width="600" zoomable="yes"}

1. Enregistrez les informations d’identification pour la clé client et le jeton d’accès en vue d’une utilisation ultérieure.

![Informations d’identification OAuth pour authentifier les demandes d’API](./assets/aem-commerce-integration-credentials.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Done]**.

>[!NOTE]
>
>Vous pouvez également générer des informations d’identification d’authentification à l’aide des API Adobe Commerce. Pour plus d’informations sur ce processus et sur l’authentification OAuth pour Adobe Commerce, voir [Authentification OAuth](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) dans la documentation Adobe Developer.
