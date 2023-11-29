---
title: '[!UICONTROL General] &gt; [!UICONTROL New Relic Reporting]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL General] &gt; [!UICONTROL New Relic Reporting] de l’administrateur Commerce.
exl-id: d6bf4810-81a3-420d-abc9-9b87c1e92551
feature: Configuration, System, Reporting
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 4%

---

# [!UICONTROL General] > [!UICONTROL New Relic Reporting]

{{config}}

## [!UICONTROL General]

![Général](./assets/new-relic-reporting-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/reports/new-relic-reporting.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable New Relic Integration] | Affichage en magasin | Détermine si votre magasin peut être utilisé avec [!DNL New Relic] Création de rapports. Options : `Yes` / `No` |
| [!UICONTROL New Relic API URL] | Affichage en magasin | URL vers laquelle les API New Relic sont déployées. Par exemple: `https://api.newrelic.com/deployments.xml` |
| URL de l’API Insights | Affichage en magasin | URL à laquelle les API Insights sont déployées. Utilisez le symbole de pourcentage (%) pour représenter votre ID de compte. Par exemple: `https://insights-collector.newrelic.com/v1/accounts/%s/events` |
| [!UICONTROL New Relic Account ID] | Affichage en magasin | L’identifiant de compte attribué à votre [!DNL New Relic] compte . |
| [!UICONTROL New Relic Application ID] | Affichage en magasin | L’ID d’application attribué à votre [!DNL New Relic] compte pour l’intégration de Commerce. |
| [!UICONTROL New Relic API Key] | Affichage en magasin | La clé qui vous est attribuée pour accéder à la variable [!DNL New Relic] API. |
| [!UICONTROL Insights API Key] | Affichage en magasin | Clé qui vous est affectée pour accéder à Statistiques. |
| [!UICONTROL New Relic Application Name] | Affichage en magasin | Le nom que vous avez attribué à votre [!DNL New Relic] intégration. |
| [!UICONTROL Send Adminhtml and Frontend as Separate Apps] | Affichage en magasin | Une option permettant d’envoyer les données de rapport collectées pour le storefront et l’administrateur en tant qu’applications distinctes à New Relic. Cette option nécessite la saisie d’un nom pour la variable [!UICONTROL New Relic Application Name]. La fonctionnalité ajoute le nom de l’application avec un trait de soulignement aux données d’application collectées. Par exemple: `MyStore_Adminhtml`, `MyStore_frontend` |

{style="table-layout:auto"}

## [!UICONTROL Cron]

![Cron](./assets/new-relic-reporting-cron.png)<!-- zoom -->

<!-- Cron](https://docs.magento.com/user-guide/system/cron.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Cron] | Affichage en magasin | Détermine si [!DNL New Relic] Les rapports peuvent être exécutés selon un calendrier comportant [Cron](../../systems/cron.md). Options : `Yes` / `No` |

{style="table-layout:auto"}
