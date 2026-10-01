---
title: '[!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys]'
description: Passez en revue les paramètres de configuration sur la page [!UICONTROL ACO Restricted Access Keys] de [!UICONTROL Services] &gt ; de l’administrateur Commerce.
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
source-wordcount: '182'
ht-degree: 4%
---
# [!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys]

Utilisez ce paramètre pour contrôler la période d’expiration par défaut que le [!DNL Adobe Commerce Optimizer Connector for B2B] applique aux clés d’accès restreint qu’il approvisionne pour les vues de catalogue partagées B2B. Pour créer, attribuer et supprimer ces clés, voir [Gestion des clés d’accès restreint](../../systems/restricted-access-keys.md).

{{config}}

## [!UICONTROL Provisioning]

![Approvisionnement](./assets/optimizer-restricted-access-key-config.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
| --- | --- | --- |
| [!UICONTROL Default key expiry (days)] | Global | Période de validité des clés d’accès restreint nouvellement configurées. [!DNL Adobe Commerce Optimizer] nécessite une date d&#39;expiration d&#39;au moins une minute dans le futur sur chaque clé et exclut les clés expirées des lectures de passerelle, de sorte qu&#39;une valeur d&#39;au moins un jour est toujours appliquée. Valeur par défaut : `36500` |

{style="table-layout:auto"}

>[!NOTE]
>
>La période d’expiration par défaut est longue, car la rotation automatique des clés n’est pas encore disponible. Voir [ Sélection et rotation des clés ](../../systems/restricted-access-keys.md#key-selection-and-rotation).

>[!MORELIKETHIS]
>
> - [Vue catalogue ACO](./aco-catalog-view.md) — Configurer des jetons d’accès storefront pour les vues catalogue
> - [Gestion des clés d&#39;accès restreint](../../systems/restricted-access-keys.md) — Créez, attribuez et supprimez des clés d&#39;accès restreint
> - [Surveillance de l’état de synchronisation de la vue Catalogue](../../systems/catalog-view-sync-status.md) — Surveillez les clés arrivant à expiration
