---
title: '[!UICONTROL Services] > ACO Catalog View Sync'
description: Passez en revue les paramètres de configuration sur la page [!UICONTROL ACO Catalog View Sync] de [!UICONTROL Services] &gt ; de l’administrateur Commerce.
feature: Configuration, Security
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9ec73be87dd329dc04e7b133885fcc156f4ffcb6
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 3%
---
# [!UICONTROL Services] > [!UICONTROL ACO Catalog View Sync]

Utilisez ces paramètres pour contrôler la manière dont le [!DNL Adobe Commerce Optimizer Connector for B2B] synchronise les configurations de catalogue partagé B2B (vue de catalogue, politique, catalogue des prix et clé) dans [!DNL Adobe Commerce Optimizer] et la manière dont il résout les différences de configuration entre les deux systèmes. Voir [Surveillance de l’état de synchronisation des vues du catalogue](../../systems/catalog-view-sync-status.md) pour surveiller les résultats de ces paramètres.

{{config}}

## [!UICONTROL Deletion]

![Suppression](./assets/aco-catalog-view-sync-configuration.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
| --- | --- | --- |
| [!UICONTROL Deletion Grace Period (days)] | Global | Période de conservation des données de catalogue partagées. Indique le nombre de jours pendant lesquels les vues de catalogue partagé, les politiques et les métadonnées d’un catalogue partagé supprimé sont conservées avant d’être supprimées définitivement. La valeur par défaut est de 7 jours. Définissez sur `0` pour effectuer immédiatement la suppression définitive. |

{style="table-layout:auto"}

## [!UICONTROL Creation]

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
| --- | --- | --- |
| [!UICONTROL Creation Grace Period (days)] | Global | Nombre de jours pendant lesquels une vue de catalogue nouvellement enregistrée peut attendre que la [!DNL Adobe Commerce Optimizer Connector for B2B] termine sa première synchronisation de la vue de catalogue, de la politique, du catalogue de prix et des configurations de clés, tandis que son statut est signalé comme [!UICONTROL Pending]. Si la période de grâce expire sans une synchronisation réussie, le statut passe à [!UICONTROL Failed]. Valeur par défaut : `1` |

{style="table-layout:auto"}

## [!UICONTROL Drift Reconciler]

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
| --- | --- | --- |
| [!UICONTROL Enabled] | Global | Exécute le réconciliateur de dérive planifié pour détecter et signaler les différences entre la vue de catalogue projetée à partir de [!DNL Adobe Commerce] et la configuration de la vue de catalogue dans [!DNL Adobe Commerce Optimizer]. Si `automatically repair drift` est activé, il tentera également de corriger les écarts réparables. |
| [!UICONTROL Automatically Repair Drift] | Global | Lorsqu’il est défini sur `Yes`, le réconciliateur de dérive planifié met à jour la configuration [!DNL Adobe Commerce Optimizer] pour qu’elle corresponde à la [!DNL Adobe Commerce] et resynchronise la configuration. Lorsqu’elle est définie sur `No`, l’exécution détecte et signale uniquement la dérive. Les entités [!DNL Adobe Commerce Optimizer] orphelines sont toujours signalées, mais ne sont jamais automatiquement supprimées. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
> - [Vue Catalogue ACO](./aco-catalog-view.md) — Configurer des jetons d&#39;accès pour les lectures storefront d&#39;une vue Catalogue
> - [Surveillance de l’état de synchronisation de la vue du catalogue](../../systems/catalog-view-sync-status.md) — Surveillez l’intégrité de la synchronisation et réconciliez la dérive à l’aide de ces paramètres
> - [Gestion des clés d&#39;accès restreintes](../../systems/restricted-access-keys.md) — Gérez les clés d&#39;accès affectées aux vues de catalogue synchronisées
