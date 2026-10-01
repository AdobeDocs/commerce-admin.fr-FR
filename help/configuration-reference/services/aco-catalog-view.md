---
title: '[!UICONTROL Services] &gt ; vue Catalogue ACO'
description: Examinez et mettez à jour les paramètres de configuration Adobe Commerce Optimizer sur la page [!UICONTROL ACO Catalog View] > [!UICONTROL Services] de Commerce Admin.
feature: Configuration, Security
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
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
source-git-commit: b32c28afffe75b3f684f0fef81bd61e9cdcb485a
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 3%
---
# [!UICONTROL Services] > [!UICONTROL ACO Catalog View]

Utilisez ces paramètres pour contrôler les jetons d’accès émis par le [!DNL Adobe Commerce Optimizer Connector for B2B]. Les storefronts utilisent ces jetons pour s’authentifier sur les vues de catalogue privé Commerce Optimizer renseignées avec des données synchronisées à partir de catalogues partagés personnalisés configurés dans l’administrateur.

{{config}}

![Administrateur Adobe Commerce affichant les paramètres de jeton d’accès de la vue Catalogue ACO, avec une TTL de 3 600 secondes et l’émission de jeton activée.](./assets/aco-catalog-view-access-token-config.png)<!-- zoom -->

## [!UICONTROL Access Token Configuration]

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
| --- | --- | --- |
| [!UICONTROL Token TTL (seconds)] | Global | Nombre de secondes pendant lesquelles un jeton d’accès reste valide après avoir été généré. Ce paramètre est en lecture seule dans la portée par défaut. Les valeurs configurées sur le site web ou dans la portée de l’affichage du magasin sont ignorées. Valeur par défaut : 3 600 secondes. |
| [!UICONTROL Issue Access Tokens] | Affichage de la boutique | Contrôle si le storefront peut obtenir un jeton d’accès pour une vue de catalogue. Lorsque la valeur est définie sur `No`, `Company.catalogViewContext` renvoie l’ID de vue de catalogue mais aucun jeton d’accès, de sorte que les storefronts ne peuvent pas s’authentifier pour lire [!DNL Adobe Commerce Optimizer] vues de catalogue privées synchronisées à partir d’Adobe Commerce. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
> - [Synchronisation des vues de catalogue ACO](./aco-catalog-view-sync.md) — Configurez la manière dont les vues de catalogue sont synchronisées dans [!DNL Adobe Commerce Optimizer]
> - [Surveillance de l&#39;état de synchronisation de la vue catalogue](../../systems/catalog-view-sync-status.md) — Surveillez l&#39;intégrité de la synchronisation et réconciliez la dérive
