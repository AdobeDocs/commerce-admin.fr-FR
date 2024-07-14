---
title: "Guide Inventory management [!DNL Inventory Management] Guide"
description: Informations complètes sur  [!DNL Inventory Management] pour les administrateurs Adobe Commerce et Magento Open Source, y compris la migration et la configuration.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# [!DNL Inventory Management] Guide - Aperçu

Ce guide est destiné aux administrateurs d’Adobe Commerce et de Magento Open Source. Il fournit des informations détaillées sur l’activation de ce module, notamment sur la configuration et la gestion de ses fonctionnalités. Cela suppose une compréhension de base de la configuration et des fonctionnalités de base de [!DNL Commerce].

[!DNL Inventory Management] comporte deux zones pour les administrateurs :

- L’administrateur : utilisez cette zone pour accéder à l’interface utilisateur de configuration et aux rapports.
- L’interface de ligne de commande : utilisez cet outil pour exécuter les tâches d’installation et de configuration du serveur principal.

Ce guide couvre :

| Objet | Description |
| ------- | ----------- |
| [Introduction](introduction.md) | Présentation des fonctionnalités [!DNL Inventory Management] que vous pouvez utiliser pour gérer le stock à plusieurs emplacements afin que votre magasin Commerce reflète fidèlement l’inventaire physique. |
| [Notes de mise à jour](release-notes.md) | Consultez les notes de mise à jour pour plus d’informations sur toutes les versions de [!DNL Inventory Management] . |
| Principes de base du stock | Découvrez les principes de base de la gestion des stocks : [Stocks et sources](sources-stocks.md), [sélection et réservation de sources](selection-reservations.md), [statut de commande et de réservation](order-status.md) et [types de produits](product-types.md). |
| Prise en main | Découvrez le module [!DNL Inventory Management] et sa fonction dans vos opérations d’instance et de magasin Commerce : [Mises à niveau de Commerce](migrate.md), [installation et mise à jour de module ](install-update.md), [types d’approvisionnement marchand](merchant-sourcing.md) et [changements de structure d’approvisionnement](expand-restructure.md) |
| [Configuration](configuration.md) | Découvrez la configuration des options [!DNL Inventory Management] qui déterminent la disponibilité de la source, les produits storefront et l’expédition de commandes. |
| [Gérer les sources](sources-manage.md) | Découvrez les sources et comment elles définissent les emplacements physiques où l’inventaire des produits est géré et expédié pour l’exécution des commandes, ou où les services sont disponibles. |
| [Gérer les stocks](stocks-manage.md) | Découvrez comment le stock est utilisé pour représenter un inventaire virtuel et agrégé de produits pour les sources de vos canaux de vente. |
| [Gérer les quantités](quantities-manage.md) | Découvrez comment attribuer des sources et des quantités pour de nouveaux produits ou modifier des produits existants. |
| [Gérer les commandes et les envois](shipments.md) | Découvrez les fonctionnalités et options supplémentaires [!DNL Inventory Management] pour gérer les quantités d&#39;inventaire par le biais du processus d&#39;envoi. |
| [Référence de ligne de commande](cli.md) | Découvrez les commandes fournies par le module [!DNL Inventory Management] pour gérer les données d’inventaire et les paramètres de configuration. |

{style="table-layout:auto"}

## Informations sur les développeurs

Voir [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) dans la documentation destinée aux développeurs pour plus d’informations sur l’architecture des modules, les API et la personnalisation des algorithmes.

## Documentation Commerce

{{docs-links}}

## Résolution des problèmes et assistance

Si vous avez besoin d’informations ou si vous avez des questions qui ne sont pas abordées dans ce guide, utilisez les ressources suivantes :

- [Incohérences de réservation de grand nombre](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-30112-magento-patch-large-number-reservation-inconsistencies.html)
- [ Problèmes d’incohérence de l’inventaire](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33281-magento-patch-inventory-inconsistency-issues.html)
- [Échantillons dont l’inventaire n’atteint pas &quot;0&quot;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-17/mdva-34850-swatches-not-strike-through-inventory-reaches-0.html)
- [État du stock incorrect après l’installation du stock](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [tickets d’assistance](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket) : envoyez un ticket pour recevoir une aide supplémentaire.
