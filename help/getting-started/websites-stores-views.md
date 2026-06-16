---
title: Site, magasin et portée d’affichage
description: Découvrez la hiérarchie des sites web, des boutiques et des affichages de boutique que vous pouvez utiliser pour offrir des expériences d’achat à vos clients.
exl-id: 80fc1b73-c869-4f1c-b1a1-d61823b91d83
feature: System, Site Management
TQID: https://experienceleague.adobe.com/S8E0BsK2lZqb82QMhyXOIEVUrXWy1X2h943tvF3sMzM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 687
ht-degree: 0%

---

# Site, magasin et portée d’affichage

Chaque installation d’Adobe Commerce et de Magento Open Source comporte une [hiérarchie](../stores-purchase/stores.md) de sites web, de boutiques et de vues de boutique. Le terme _portée_ détermine l’emplacement dans la hiérarchie d’une entité de base de données (produit, attribut ou catégorie, par exemple) d’un élément de contenu ou d’un paramètre de configuration. Les sites web, les boutiques et les affichages de boutique ont des relations parent/enfant de un à plusieurs. Une seule installation peut comporter plusieurs sites web, et chaque site web peut avoir plusieurs magasins et vues de magasin.

>[!NOTE]
>
>Pour en savoir plus, consultez la section [Plusieurs sites web ou magasins](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) dans la documentation destinée aux développeurs [!DNL Commerce].

## Sites web

Les installations commencent par un seul [site web](../stores-purchase/stores.md#add-websites), appelé par défaut _site web principal_. Vous pouvez également configurer plusieurs sites web pour une seule installation, chacun ayant sa propre adresse IP et son propre domaine.

## Magasins

Un seul site web peut comporter plusieurs [boutiques](../stores-purchase/stores.md#add-stores), chacune disposant de son propre menu principal. Les magasins partagent le catalogue de produits, mais peuvent avoir une sélection différente de produits et de conception. Tous les magasins d’un même site web partagent les options Administration et Passage en caisse.

## Vues de la boutique

Chaque magasin disponible pour les clients est présenté selon une _[vue](../stores-purchase/store-views.md)_ spécifique. Au départ, un magasin possède une vue par défaut unique. Il est possible d’ajouter d’autres vues de magasin pour prendre en charge différentes langues ou à d’autres fins. Les clients peuvent utiliser le sélecteur de langue dans l’en-tête pour modifier la vue du magasin.

Lorsque vous utilisez des sites web, des boutiques et des affichages de boutique, gardez à l’esprit les points suivants :

- Les instances Commerce ont un modèle en cascade : site web global → magasin → vue magasin → magasin.
- Chaque site web comporte au moins un magasin et une vue de magasin par défaut.
- Chaque vue de magasin peut avoir une URL de base différente.
- La fonction principale d’un site web est la configuration des fonctionnalités de niveau supérieur.
- La fonction principale d’un magasin est la configuration de catégorie racine.
- La fonction principale d’une vue de magasin est la configuration des informations de traduction et des symboles de devise.

## Paramètres de l’étendue

Si votre installation Adobe Commerce ou Magento Open Source comporte une hiérarchie de sites web, de boutiques ou de vues, vous pouvez définir le contexte ou la _portée_ d’un paramètre de configuration. Le contexte de nombreuses entités de base de données peut également se voir attribuer une portée spécifique afin de déterminer son utilisation dans la hiérarchie du magasin. Pour en savoir plus, voir [Périmètre du produit](../catalog/introduction.md#product-scope) et [Périmètre du prix](../catalog/catalog-price-scope.md).

Certains paramètres de configuration, tels que le code postal, ont une portée globale, car la même valeur est utilisée dans l’ensemble du système. La portée [site web](../stores-purchase/stores.md#add-websites) s’applique à tous les magasins situés sous ce niveau dans la hiérarchie, y compris tous les magasins et leurs vues. Tout élément avec la portée de [vue du magasin](../stores-purchase/store-views.md) peut être défini différemment pour chaque vue du magasin, qui est généralement utilisée pour prendre en charge plusieurs langues. Pour remplacer les valeurs par défaut des paramètres de configuration, voir [Définir la portée](../configuration-reference/scope-change.md#set-the-scope).

À moins que le magasin ne s’exécute en [mode magasin unique](#single-store-mode), la portée de chaque paramètre de configuration s’affiche en petit texte sous le libellé du champ. Si votre installation comprend plusieurs sites web, boutiques ou vues, choisissez la vue [store](../stores-purchase/store-views.md) où les paramètres s’appliquent avant d’apporter des modifications.

![Hiérarchie des sites web, des boutiques et des vues de boutique](./assets/scope-multisite.svg){width="550"}

| Portée | Description |
|--- |--- |
| [!UICONTROL Global] | Paramètres et ressources à l’échelle du système disponibles tout au long de l’installation. |
| [!UICONTROL Website] | Paramètres et ressources limités au site Web actuel. Chaque site web comporte un magasin par défaut. |
| [!UICONTROL Store] | Paramètres et ressources limités au magasin actuel. Chaque magasin possède une catégorie racine par défaut (menu principal) et une vue de magasin par défaut. |
| [!UICONTROL Store View] | Paramètres et ressources limités à l’affichage actuel du magasin. |

{style="table-layout:auto"}

## Mode magasin unique

Si votre installation Commerce ne comporte qu’une seule vue de magasin et d’étendue, vous pouvez simplifier l’affichage en désactivant toutes les options de vue de magasin et tous les indicateurs d’étendue. Le mode de magasin unique est remplacé si vous [ajoutez d’autres vues de magasin](../stores-purchase/store-views.md) ultérieurement.

![Portée - vue unique](./assets/scope-single-view.svg){width="550"}

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Sous **[!UICONTROL General]**, faites défiler la page vers le bas et développez la section **[!UICONTROL Single-Store Mode]** .

1. Définissez **[!UICONTROL Enable Single-Store Mode]** sur `Yes`.

   ![Configuration générale - Activation du mode à magasin unique](./assets/general-single-store-mode.png){width="400"}

1. Cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous êtes invité à actualiser le cache, procédez comme suit :

   - Cliquez sur le lien **[!UICONTROL Cache Management]** dans le message système en haut de la page.

     ![Message système - gestion du cache](../catalog/assets/msg-cache-management.png){width="600" zoomable="yes"}

   - Cochez la case **[!UICONTROL Page Cache]** .

   - Lorsque **[!UICONTROL Actions]** est défini sur `Refresh`, cliquez sur **[!UICONTROL Submit]**
