---
title: Étendue du site, du magasin et de l’affichage
description: Découvrez la hiérarchie de sites web, de magasins et d’affichages de magasins que vous pouvez utiliser pour offrir des expériences d’achat à vos clients.
exl-id: 80fc1b73-c869-4f1c-b1a1-d61823b91d83
feature: System, Site Management
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Étendue du site, du magasin et de l’affichage

Chaque installation d’Adobe Commerce et de Magento Open Source comporte une [hiérarchie](../stores-purchase/stores.md) de sites web, de magasins et de vues de magasin. Le terme _scope_ détermine où s’applique une entité de base de données dans la hiérarchie (un produit, un attribut ou une catégorie, par exemple), un élément de contenu ou un paramètre de configuration. Les sites web, les magasins et les vues de magasin ont des relations parents/enfants de type un à plusieurs. Une seule installation peut comporter plusieurs sites web, et chaque site web peut avoir plusieurs magasins et vues de magasin.

>[!NOTE]
>
>Pour en savoir plus, voir [Plusieurs sites Web ou magasins](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html?lang=fr) dans la documentation destinée aux développeurs [!DNL Commerce].

## Sites web

Les installations commencent par un seul [site web](../stores-purchase/stores.md#add-websites), appelé _site web principal_ par défaut. Vous pouvez également configurer plusieurs sites web pour une seule installation, chacun ayant son adresse IP et son domaine.

## Magasins

Un seul site web peut avoir plusieurs [magasins](../stores-purchase/stores.md#add-stores), chacun disposant de son propre menu principal. Les magasins partagent le catalogue de produits, mais peuvent avoir une sélection de produits et une conception différentes. Tous les magasins situés sous le même site web partagent les droits d’administrateur et de passage en caisse.

## Vues du magasin

Chaque magasin disponible pour les clients est présenté selon une _[vue](../stores-purchase/store-views.md)_ spécifique. Au départ, un magasin n’a qu’une seule vue par défaut. D’autres vues de magasin peuvent être ajoutées pour prendre en charge différentes langues ou à d’autres fins. Les clients peuvent utiliser le sélecteur de langue dans l’en-tête pour modifier la vue du magasin.

Lorsque vous utilisez des sites web, des magasins et des vues de magasin, tenez compte des points suivants :

- Les instances Commerce ont un modèle en cascade : site web → global → magasin → vue magasin.
- Chaque site web possède au moins une vue de magasin et de magasin par défaut.
- Chaque vue de magasin peut avoir une URL de base différente.
- La fonction principale d’un site web est la configuration de fonctionnalités de niveau supérieur.
- La fonction principale d’un magasin est la configuration de catégorie racine.
- La principale fonction d’une vue de magasin est les informations de traduction et la configuration des symboles de devise.

## Paramètres de portée

Si votre installation Adobe Commerce ou Magento Open Source comporte une hiérarchie de sites web, de magasins ou d’affichages, vous pouvez définir le contexte, ou la _portée_ d’un paramètre de configuration. Le contexte de nombreuses entités de base de données peut également se voir attribuer une portée spécifique afin de déterminer comment elles sont utilisées dans la hiérarchie de magasin. Pour en savoir plus, voir [Portée du produit](../catalog/introduction.md#product-scope) et [Étendue du prix](../catalog/catalog-price-scope.md).

Certains paramètres de configuration, tels que le code postal, ont une portée globale, car la même valeur est utilisée dans tout le système. La portée de [site web](../stores-purchase/stores.md#add-websites) s’applique à tous les magasins sous ce niveau de la hiérarchie, y compris tous les magasins et leurs vues. Tout élément ayant une portée de [vue de magasin](../stores-purchase/store-views.md) peut être défini différemment pour chaque vue de magasin, qui est généralement utilisée pour prendre en charge plusieurs langues. Pour remplacer les valeurs par défaut des paramètres de configuration, voir [Définition de la portée](../configuration-reference/scope-change.md#set-the-scope).

À moins que le magasin ne s’exécute dans le [mode de magasin unique](#single-store-mode), la portée de chaque paramètre de configuration s’affiche en petit texte sous le libellé du champ. Si votre installation comprend plusieurs sites web, magasins ou vues, choisissez la [vue de magasin](../stores-purchase/store-views.md) où les paramètres s’appliquent avant d’apporter des modifications.

![Hiérarchie des sites Web, des magasins et des vues de magasin](./assets/scope-multisite.svg){width="550"}

| Portée | Description |
|--- |--- |
| [!UICONTROL Global] | Paramètres à l’échelle du système et ressources disponibles tout au long de l’installation. |
| [!UICONTROL Website] | Paramètres et ressources limités au site web actuel. Chaque site web comporte un magasin par défaut. |
| [!UICONTROL Store] | Paramètres et ressources limités au magasin actuel. Chaque magasin possède une catégorie racine par défaut (menu principal) et une vue de magasin par défaut. |
| [!UICONTROL Store View] | Paramètre et ressources limités à la vue de magasin actuelle. |

{style="table-layout:auto"}

## Mode magasin unique

Si votre installation Commerce ne dispose que d’une seule vue de magasin et de magasin, vous pouvez simplifier l’affichage en désactivant toutes les options de vue de magasin et tous les indicateurs de portée. Le mode de magasin unique est remplacé si vous [ajoutez d’autres vues de magasin](../stores-purchase/store-views.md) ultérieurement.

![Portée - vue unique](./assets/scope-single-view.svg){width="550"}

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Sous **[!UICONTROL General]**, faites défiler la page vers le bas et développez la section **[!UICONTROL Single-Store Mode]**.

1. Définissez **[!UICONTROL Enable Single-Store Mode]** sur `Yes`.

   ![Configuration générale - Activer le mode Boutique unique](./assets/general-single-store-mode.png){width="400"}

1. Cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous êtes invité à actualiser le cache, procédez comme suit :

   - Cliquez sur le lien **[!UICONTROL Cache Management]** dans le message système en haut de la page.

     ![&#x200B; Message système - Gestion du cache](../catalog/assets/msg-cache-management.png){width="600" zoomable="yes"}

   - Cochez la case **[!UICONTROL Page Cache]** .

   - Avec **[!UICONTROL Actions]** défini sur `Refresh`, cliquez sur **[!UICONTROL Submit]**
