---
title: '[!UICONTROL General] > [!UICONTROL B2B Features]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL B2B Features] de [!UICONTROL General] &gt ; de l’administrateur Commerce.
exl-id: fc07a067-b92a-49c7-8512-2dfcc1c6ba0c
feature: Configuration, B2B
TQID: https://experienceleague.adobe.com/s9-xEtVsEhdegXaObYrfbu-tSvvcqlXVagEw4QJejlk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 347
ht-degree: 1%

---

# [!UICONTROL General] > [!UICONTROL B2B Features]

{{b2b-feature}}

{{config}}

>[!TIP]
>
>Avec l’installation et l’activation d’Adobe Commerce B2B, l’expérience d’achat peut être personnalisée avec des fonctionnalités spécifiques à l’entreprise. Adobe Commerce B2B est une solution intégrée qui prend en charge les modèles B2B et B2C. Pour plus d’informations sur les fonctionnalités B2B, consultez le [_Guide de l’utilisateur Adobe Commerce B2B_](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=fr).

## [!UICONTROL B2B Features]

![Fonctionnalités B2B](./assets/b2b-features.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Company]](../../b2b/account-companies.md) | Site internet | Lorsque cette option est activée, elle permet aux clients de gérer l’affectation de leur entreprise à partir du tableau de bord de leur compte et active également les fonctionnalités Catalogue partagé et Devis B2B par défaut. Options : `Yes` / `No` |
| [[!UICONTROL Enable Quick Order]](../../b2b/quick-order.md) | Site internet | Lorsqu’elle est activée, permet aux clients et aux invités de passer rapidement des commandes en fonction du SKU ou du nom du produit. Options : `Yes` / `No` |
| [[!UICONTROL Enable Requisition List]](../../b2b/configure-requisition-lists.md) | Site internet | Lorsque cette option est activée, permet aux clients de créer et de gérer des listes de demandes d&#39;approvisionnement à partir du tableau de bord de leur compte. |

{style="table-layout:auto"}

![Fonctionnalités B2B avec les sociétés et les catalogues partagés activées](./assets/b2b-features-company-enabled.png)<!-- zoom -->

Lorsque la fonction Société est activée, des champs supplémentaires sont disponibles pour le catalogue partagé et le devis B2B.

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Shared Catalog]](../../b2b/catalog-shared.md) | Site internet | Lorsque cette option est activée, elle permet de créer des catalogues organisés avec une tarification personnalisée disponible globalement ou limitée à des sociétés spécifiques. Options : `Yes` / `No` |
| [!UICONTROL Enable Shared Catalog direct products price assigning] | Site internet | Lorsque le champ _[!UICONTROL Enable Shared Catalog]_&#x200B;est défini sur `Yes`, cette option est disponible. Lorsque cette option est activée, seuls les produits affectés à un catalogue partagé sont stockés dans l’indice des prix. Les produits qui ne sont pas affectés au catalogue partagé ne sont pas affichés sur le storefront. Options : `Yes` / `No` |
| [[!UICONTROL Enable B2B Quote]](../../b2b/configure-quotes.md) | Site internet | Lorsque cette option est activée, elle permet aux acheteurs de la société de soumettre une demande de devis à partir du panier. Options : `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Default B2B Payment Methods]

![Configuration B2B - paramètres de mode de paiement par défaut](./assets/b2b-features-default-payment-methods.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|------- |----------------------------------------------------------------------- |------------ |
| [!UICONTROL Applicable Payment Methods] | Global | Détermine la sélection des modes de paiement disponibles pour les acheteurs B2B. Options : `All Payment Methods` / `Specific Payment Methods` |
| [!UICONTROL Payment Methods] | Global | Spécifie chaque mode de paiement disponible pour les acheteurs B2B. |

{style="table-layout:auto"}

### [!UICONTROL Default B2B Shipping Methods]

![Configuration B2B - Modes d’expédition par défaut](./assets/b2b-features-shipping-methods.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|------- |----------------------------------------------------------------------- |------------ |
| [!UICONTROL Applicable Shipping Methods] | Global | Détermine la sélection des méthodes d&#39;expédition disponibles par défaut pour les acheteurs B2B. Options : `All Shipping Methods` / `Specific Shipping Methods` |
| [!UICONTROL Shipping Methods] | Global | Spécifie chaque méthode d&#39;expédition disponible par défaut pour les acheteurs B2B. <br/>**_Remarque:_** vous pouvez également limiter les modes d’expédition pour un [compte de société](../../b2b/account-companies.md) spécifique. |

{style="table-layout:auto"}

## [!UICONTROL Order Approval Configuration]

![Fonctionnalités B2B - Configuration de l’approbation de commande](./assets/b2b-features-order-approval.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Purchase Orders]](../../stores-purchase/purchase-order.md) | Site internet | Lorsque cette option est activée, les entreprises peuvent créer des commandes fournisseur. Options : `Yes` / `No` |

{style="table-layout:auto"}


