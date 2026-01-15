---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Shipping Settings]'
description: Vérifiez les paramètres de configuration sur la page de [!UICONTROL Sales] d’[!UICONTROL Shipping Settings] &gt; de l’administrateur Commerce.
exl-id: d7d46946-f8c9-4714-96c3-2173e28f7bfa
feature: Configuration, Shipping/Delivery
source-git-commit: 528e57df775b53b6137e1542ad0583c60d2f47ff
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Shipping Settings]

{{config}}

Pour plus d’informations sur la modification de ces paramètres, voir [Paramètres d’expédition](../../stores-purchase/shipping-settings.md) dans le _Guide des magasins et de l’expérience d’achat_.

## [!UICONTROL Origin]

![Origine](./assets/shipping-settings-origin.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Country] | Site internet | Pays d’origine. |
| [!UICONTROL Region/State] | Site internet | Région ou État du point d’origine. |
| [!UICONTROL ZIP/Postal Code] | Site internet | Code postal du point d’origine. |
| [!UICONTROL City] | Site internet | Ville du point d’origine. |
| [!UICONTROL Street Address] | Site internet | Adresse postale du point d’origine. |
| [!UICONTROL Street Address Line 2] | Site internet | Une ligne supplémentaire pour l’adresse postale du point d’origine, si nécessaire. |

{style="table-layout:auto"}

## [!UICONTROL Shipping Policy Parameters]

![Paramètres de la stratégie d&#39;expédition](./assets/shipping-settings-shipping-policy-parameters.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Apply Custom Shipping Policy] | Site internet | Détermine si votre politique d&#39;expédition s&#39;affiche lors du passage en caisse. Options : `Yes` / `No` |
| [!UICONTROL Shipping Policy] | Affichage de la boutique | Contient votre politique d’expédition sous forme de texte. |

{style="table-layout:auto"}

## [!UICONTROL Shipment Tracking URLs]

[!BADGE SaaS uniquement]{type=Positive url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce as a Cloud Service (infrastructure SaaS gérée par Adobe)."}

[!BADGE &#x200B; Sandbox &#x200B;]{type=Caution tooltip="Les éléments répertoriés ne sont actuellement disponibles que dans les environnements Sandbox. Adobe commence par rendre les nouvelles versions disponibles dans les environnements Sandbox afin que vous disposiez du temps nécessaire pour tester les modifications à venir avant que la version ne soit disponible dans les environnements de production."}

![Paramètres de la stratégie d&#39;expédition](./assets/shipping-settings-shipment-tracking-urls.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Custom Tracking URLs] | Affichage de la boutique | Détermine si les numéros de suivi des expéditions envoyés dans les e-mails des acheteurs sont des liens ou du texte brut. La valeur par défaut de `No` indique que les nombres sont en texte brut. Options : `Yes` / `No` |
| [!UICONTROL USPS Tracking URL] | Affichage de la boutique | Modèle d’URL pour les expéditions du service postal des États-Unis. |
| [!UICONTROL UPS Tracking URL] | Affichage de la boutique | Modèle d&#39;URL pour les expéditions United Parcel Service. |
| [!UICONTROL FedEx Tracking URL] | Affichage de la boutique | Modèle d&#39;URL pour les expéditions Federal Express. |
| [!UICONTROL DHL Tracking URL] | Affichage de la boutique | Modèle d&#39;URL pour les expéditions DHL Express. |

{style="table-layout:auto"}
