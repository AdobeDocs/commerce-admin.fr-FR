---
title: '[!DNL New Relic] de rapports'
description: Découvrez les rapports  [!DNL New Relic]  disponibles pour les comptes d’Adobe Commerce sur les infrastructures cloud, qui incluent le logiciel pour le service New Relic APM.
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: c406add80981387305755221f21624dad475e63f
workflow-type: tm+mt
source-wordcount: '1399'
ht-degree: 0%

---

# [!DNL New Relic] de rapports

[New Relic][1] est un service d’analyse logicielle qui vous aide à analyser et à améliorer les interactions entre les applications. Les comptes d’Adobe Commerce sur les infrastructures cloud incluent le logiciel pour le service [!DNL New Relic APM]. Pour plus d’informations, consultez la section [Services New Relic][4] dans le guide _Commerce sur les infrastructures cloud_.

## Étape 1 : S’inscrire à un compte [!DNL New Relic]

1. Rendez-vous sur le site Web [[!DNL New Relic]][1] et inscrivez-vous à un compte.

   Vous pouvez également créer un compte d’évaluation gratuit.

1. Suivez les instructions sur le site. Lorsque vous y êtes invité, sélectionnez d’abord le produit à installer.

1. Lorsque vous vous trouvez dans votre compte , recherchez les informations d’identification suivantes, requises pour terminer la configuration de Commerce :

   | Option | Description |
   | ------ | ----------- |
   | ID de compte | Dans le tableau de bord de votre compte [!DNL New Relic], l’ID de compte est le numéro dans l’URL après : `/accounts` |
   | ID de l’application | Dans le tableau de bord de votre compte [!DNL New Relic], cliquez sur **[!UICONTROL New Relic APM]**. Dans le menu, choisissez **[!UICONTROL Applications]**. Choisissez ensuite votre application. L’ID de l’application est le numéro dans l’URL après : `/applications/` |
   | Clé API New Relic | Dans le tableau de bord de votre compte [!DNL New Relic], cliquez sur **[!UICONTROL Account Settings]**. Dans le menu de gauche, sous Intégrations, choisissez **[!UICONTROL Data Sharing]**. Vous pouvez créer, régénérer ou supprimer votre clé API à partir de cette page. |
   | Clé API Insights | Dans le tableau de bord de votre compte [!DNL New Relic], cliquez sur **[!UICONTROL Insights]**. Dans le menu de gauche, sous Administration, choisissez **[!UICONTROL API Keys]**. Vos clés API Insights apparaissent sur cette page. Si nécessaire, cliquez sur le signe plus (**+**) en regard de Insérer des clés pour générer une clé. |

   {style="table-layout:auto"}

## Étape 2 : installer l’agent [!DNL New Relic] sur votre serveur

Pour utiliser [!DNL New Relic APM Pro] pour collecter et transmettre des données, l&#39;agent PHP doit être installé sur votre serveur.

1. Lorsque vous êtes invité à choisir un agent web, cliquez sur **PHP**.

1. Pour configurer l&#39;agent PHP sur votre serveur, suivez les instructions.

   Si vous avez besoin d&#39;aide, voir [New Relic pour PHP][3].

1. Vérifiez que cron est en cours d’exécution sur votre serveur.

   Pour en savoir plus, consultez [Configuration et exécution de cron][5] dans la documentation destinée aux développeurs.

## Étape 3 : Configurer votre boutique

>[!NOTE]
>Ces options de configuration ne s’appliquent pas à Adobe Commerce sur les infrastructures cloud.
>
>Si vous êtes sur le plan Pro, New Relic est déjà [préconfiguré et activé par défaut](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html). Si vous êtes dans le plan de démarrage, vous devez suivre les [étapes de configuration de New Relic](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment) qui font partie du processus de configuration.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de navigation de gauche où **[!UICONTROL General]** est développé, choisissez **[!UICONTROL New Relic Reporting]** et procédez comme suit :

   ![Configuration des rapports New Relic](./assets/new-relic-reporting-general.png){width="600"}

   * Définissez **[!UICONTROL Enable New Relic Integration]** sur `Yes`.

   * Dans la **[!UICONTROL Insights API URL]**, remplacez le symbole de pourcentage (`%`) par votre identifiant de compte New Relic.

   * Saisissez votre **[!UICONTROL New Relic Account ID]**.

   * Saisissez votre **[!UICONTROL New Relic Application ID]**.

   * Saisissez votre **[!UICONTROL New Relic API Key]**.

   * Saisissez votre **[!UICONTROL Insights API Key]**.

1. Par **[!UICONTROL New Relic Application Name]**, saisissez un nom pour identifier la configuration à des fins de référence interne.

1. (Facultatif) Par **[!UICONTROL Send Adminhtml and Frontend as Separate Apps]**, sélectionnez `Yes` pour envoyer les données collectées pour le storefront et l’administrateur sous la forme d’applications distinctes vers New Relic.

   Cette option nécessite la saisie d’un nom pour le **[!UICONTROL New Relic Application Name]**.

   >[!NOTE]
   >
   >L’activation de cette fonctionnalité réduit le nombre d’alertes de [!DNL New Relic] faussement positives et permet une surveillance et des alertes configurées strictement pour les performances frontales. New Relic reçoit des fichiers de données d’application distincts avec les noms d’application ajoutés à `Adminhtml` et frontend . Par exemple : `MyStore_Adminhtml`

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Étape 4 : activer Cron pour la création de rapports [!DNL New Relic]

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Cron]** .

   ![Configuration New Relic Cron](./assets/new-relic-reporting-cron.png){width="600"}

1. Définissez **[!UICONTROL Enable Cron]** sur `Yes`.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## [!DNL New Relic] des requêtes

[!DNL New Relic Insights] données sont basées sur des instructions écrites en [!DNL New Relic Query Language] (NRQL) et sur les paramètres personnalisés que vous pouvez inclure. Les données peuvent être renvoyées à partir de requêtes ad hoc ou par des requêtes enregistrées dans votre tableau de bord. Pour en savoir plus, consultez la [Référence NRQL][6] dans la documentation [!DNL New Relic].

### Événements d’administration

#### Utilisateurs administrateurs actifs

Renvoie le nombre d’utilisateurs administrateurs actifs.

    SELECT uniqueCount(AdminId)
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; DEPUIS 15 minutes

#### Utilisateurs administrateurs actuellement actifs

Renvoie les noms des utilisateurs administrateurs actifs.

    SELECT uniques(AdminName)
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; DEPUIS 15 minutes

#### Activité Administrateur récente

Renvoie le nombre d’actions Admin récentes.

    SELECT count(AdminId)
    FROM Transaction
    WHERE appName =&#39;&lt;your_app_name>&#39; FACET AdminName DEPUIS 1 jour

#### Dernière activité Admin

Renvoie des informations détaillées sur les récentes actions d’administration, y compris le nom d’utilisateur, la durée et le nom de l’application administrateur.

    SELECT AdminName, duration, name
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; AND AdminName IS NOT NULL
    AND AdminName != LIMITE &#39;N/A&#39; DE 50

### Événements cron

#### Nombre de catégories

Renvoie le nombre d&#39;événements d&#39;application par catégorie pendant la période spécifiée.

    SELECT average(CatalogCategoryCount)
    FROM Cron
    WHERE CatalogCategoryCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 minutes

#### Nombre actuel de catalogues

Renvoie le nombre moyen d&#39;événements d&#39;application dans le catalogue par catégorie pendant la période spécifiée.

    SELECT average(CatalogCategoryCount)
    FROM Cron
    WHERE CatalogCategoryCount IS NOT NULL
    AND CatalogCategoryCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; FROM 2 minutes ago LIMIT 1

#### Produits actifs

Renvoie le nombre d&#39;événements d&#39;application par produit pendant la période spécifiée.

    SELECT average(CatalogProductActiveCount)
    FROM Cron
    WHERE CatalogProductActiveCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 minutes

#### Nombre de produits actifs

Renvoie le nombre moyen d&#39;événements d&#39;application actifs par produit pendant la période spécifiée.

    SELECT average(CatalogProductActiveCount)
    FROM Cron
    WHERE CatalogProductActiveCount IS NOT NULL
    AND CatalogProductActiveCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; FROM 2 minutes ago LIMIT 1

#### Produits configurables

Renvoie le nombre moyen d’événements d’application pour les produits configurables au cours de la période spécifiée.

    SELECT average(CatalogProductConfigurableCount)
    FROM Cron
    WHERE CatalogProductConfigurableCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 minutes

#### Nombre de produits configurables

Renvoie le nombre moyen d&#39;événements d&#39;application par produit configurable pendant la période spécifiée.

    SELECT average(CatalogProductConfigurableCount)
    FROM Cron
    WHERE CatalogProductConfigurableCount IS NOT NULL
    AND CatalogProductConfigurableCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; FROM 2 minutes ago LIMIT 1

#### Nombre de produits (tous)

Renvoie le nombre total d’événements d’application pour tous les produits.

    SELECT average(CatalogProductCount)
    FROM Cron
    WHERE CatalogProductCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 minutes

#### Nombre actuel de produits (tous)

Renvoie le nombre moyen d’événements d’application pour tous les produits au cours de la période spécifiée.

    SELECT average(CatalogProductCount)
    FROM Cron
    WHERE CatalogProductCount IS NOT NULL
    AND CatalogProductCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; FROM 2 minutes ago LIMIT 1

#### Nombre de clients

Renvoie le nombre moyen d’événements d’application par client.

    SELECT average(CustomerCount)
    FROM Cron
    WHERE CustomerCount IS NOT NULL
    AND CustomerCount > 0&lt;
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 minutes

#### Nombre actuel de clients

Renvoie le nombre moyen de clients pendant la période spécifiée.

    SELECT average(CustomerCount)
    FROM Cron
    WHERE CustomerCount IS NOT NULL
    AND CustomerCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; FROM 2 minutes ago LIMIT 1

#### Statut du module

Renvoie le nombre moyen de fois où les modules d’application sont activés, désactivés ou installés au cours de la période spécifiée.

    SELECT average(ModulesDisabled), average(ModulesEnabled), average
    (ModulesInstalled)
    FROM Cron&lt;
    WHERE appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 minutes

#### Statut actuel du module

Renvoie le nombre moyen de fois où les modules ont été activés, désactivés ou installés au cours de la période spécifiée.

    SELECT average(ModulesDisabled), average(ModulesEnabled), average
    (ModulesInstalled)
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name>&#39; DEPUIS 2 minutes LIMIT 1

#### Nombre de sites web et de magasins

Renvoie le nombre moyen d’événements d’application par site web et magasin au cours de la période spécifiée.

    SELECT average(StoreViewCount), average(WebsiteCount)
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name&gt;&#39; TIMESERIES 2 minutes

#### Nombre actuel de sites web et de magasins

Renvoie le nombre moyen d&#39;événements d&#39;application en cours au cours de la période spécifiée.

    SELECT average(StoreViewCount), average(WebsiteCount)
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name>&#39; DEPUIS 2 minutes LIMIT 1

#### Cron : toutes les données de l’événement

Renvoie toutes les données d’événement d’application.

    SELECT *
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name>&#39;

### Clients

#### Nombre de clients et clientes actifs

Renvoie le nombre de clients et clientes actifs pendant la période spécifiée.

    SELECT uniqueCount(CustomerId)
    FROM Transaction
    WHERE appName = &#39;&lt;your_app_name>&#39; DEPUIS 15 minutes

#### Clients et clientes actifs

Renvoie les noms des clients et clientes actifs pendant la période spécifiée.

    SELECT uniques(CustomerName)
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; DEPUIS 15 minutes

#### Principaux clients

Renvoie les principaux clients au cours de la période spécifiée.

    SELECT count(CustomerId)
    FROM Transaction
    WHERE appName = &#39;&lt;your_app_name>&#39; FACET CustomerName DEPUIS 1 jour

#### Activité Administrateur récente

Renvoie un nombre défini d’enregistrements d’activité récente, y compris le nom du client et la durée de sa visite.

    SELECT CustomerName, duration, name
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39;
    AND CustomerName IS NOT NULL
    AND CustomerName != LIMITE &#39;N/A&#39; DE 50

### Commandes

#### Nombre de commandes passées

Renvoie le nombre de commandes passées au cours de la période spécifiée.

    SELECT count(Order)
    FROM Transaction SINCE 1 day ago

#### Valeur totale de la commande

Renvoie le nombre total d&#39;éléments de ligne commandés au cours de la période spécifiée.

    SELECT sum(orderValue)
    FROM Transaction FROM Il y a 1 jour

#### Total des lignes commandées

Renvoie le nombre total d&#39;éléments de ligne commandés au cours de la période spécifiée.

    SELECT sum(lineItemCount)
    FROM Transaction SINCE Il y a 1 jour


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference
