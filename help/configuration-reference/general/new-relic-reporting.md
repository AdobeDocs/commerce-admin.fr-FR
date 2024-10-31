---
title: '[!UICONTROL General] &gt; [!UICONTROL New Relic Reporting]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL General] &gt; [!UICONTROL New Relic Reporting] de l’administrateur Commerce.
exl-id: d6bf4810-81a3-420d-abc9-9b87c1e92551
feature: Configuration, System, Reporting
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL New Relic Reporting]

{{config}}

>[!NOTE]
>Ces options de configuration ne s’appliquent pas à Adobe Commerce sur l’infrastructure cloud.
>
>Si vous utilisez le plan Pro, New Relic est déjà [ préconfiguré et activé par défaut ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html). Si vous utilisez le plan de démarrage, vous devez effectuer les [étapes de configuration de New Relic](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment) qui font partie du processus de configuration.

## [!UICONTROL General]

![Général](./assets/new-relic-reporting-general.png)<!-- zoom -->

<!-- [General](https://experienceleague.adobe.com/en/docs/commerce-admin/start/reporting/new-relic-reporting) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable New Relic Integration] | Affichage en magasin | Détermine si votre magasin peut être utilisé avec la création de rapports [!DNL New Relic]. Options : `Yes` / `No` |
| [!UICONTROL New Relic API URL] | Affichage en magasin | URL vers laquelle les API New Relic sont déployées. Par exemple : `https://api.newrelic.com/deployments.xml` |
| URL de l’API Insights | Affichage en magasin | URL à laquelle les API Insights sont déployées. Utilisez le symbole de pourcentage (%) pour représenter votre ID de compte. Par exemple : `https://insights-collector.newrelic.com/v1/accounts/%s/events` |
| [!UICONTROL New Relic Account ID] | Affichage en magasin | L’identifiant de compte attribué à votre compte [!DNL New Relic]. |
| [!UICONTROL New Relic Application ID] | Affichage en magasin | L’ID d’application affecté à votre compte [!DNL New Relic] pour l’intégration Commerce. |
| [!UICONTROL New Relic API Key] | Affichage en magasin | Clé qui vous est affectée pour accéder à l’API [!DNL New Relic]. |
| [!UICONTROL Insights API Key] | Affichage en magasin | Clé qui vous est affectée pour accéder à Statistiques. |
| [!UICONTROL New Relic Application Name] | Affichage en magasin | Nom que vous avez attribué à votre intégration [!DNL New Relic]. |
| [!UICONTROL Send Adminhtml and Frontend as Separate Apps] | Affichage en magasin | Une option permettant d’envoyer les données de rapport collectées pour le storefront et l’administrateur en tant qu’applications distinctes à New Relic. Cette option nécessite un nom saisi pour le [!UICONTROL New Relic Application Name]. La fonctionnalité ajoute le nom de l’application avec un trait de soulignement aux données d’application collectées. Par exemple : `MyStore_Adminhtml`, `MyStore_frontend` |

{style="table-layout:auto"}

## [!UICONTROL Cron]

![Cron](./assets/new-relic-reporting-cron.png)<!-- zoom -->

<!-- Cron](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/tools/cron) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Cron] | Affichage en magasin | Détermine si les rapports [!DNL New Relic] peuvent être exécutés selon le calendrier avec [Cron](../../systems/cron.md). Options : `Yes` / `No` |

{style="table-layout:auto"}
