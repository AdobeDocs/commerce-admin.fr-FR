---
title: Guide d’Inventory management [!DNL Inventory Management] Guide'
description: Informations complètes sur [!DNL Inventory Management] pour les administrateurs Adobe Commerce et Magento Open Source, y compris la migration et la configuration.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# [!DNL Inventory Management] Présentation du guide

Ce guide est destiné aux administrateurs d’Adobe Commerce et de Magento Open Source. Il fournit des informations détaillées sur l’activation de ce module, notamment sur la configuration et la gestion de ses fonctionnalités. Cela suppose une compréhension de base du coeur [!DNL Commerce] configuration et fonctionnalité.

[!DNL Inventory Management] comporte deux zones pour les administrateurs :

- L’administrateur : utilisez cette zone pour accéder à l’interface utilisateur de configuration et aux rapports.
- L’interface de ligne de commande : utilisez cet outil pour exécuter les tâches d’installation et de configuration du serveur principal.

Ce guide couvre :

| Objet | Description |
| ------- | ----------- |
| [Introduction](introduction.md) | Présentation de la variable [!DNL Inventory Management] fonctionnalités que vous pouvez utiliser pour gérer des stocks à plusieurs emplacements afin que votre boutique Commerce reflète fidèlement l’inventaire physique. |
| [Notes de mise à jour](release-notes.md) | Consultez les notes de mise à jour pour plus d’informations sur toutes les [!DNL Inventory Management] versions. |
| Principes de base du stock | Découvrez les principes de base de la gestion des stocks : [Stocks et sources](sources-stocks.md), [sélection et réservations de sources](selection-reservations.md), [statut de commande et de réservation](order-status.md), et [types de produits](product-types.md) |
| Prise en main | En savoir plus sur les [!DNL Inventory Management] et comment il s’intègre à votre instance Commerce et aux opérations de magasin : [Mises à niveau de Commerce](migrate.md), [installation et mise à jour du module](install-update.md), [types d’approvisionnement commercial](merchant-sourcing.md), et [Modifications de la structure d&#39;approvisionnement](expand-restructure.md) |
| [Configuration](configuration.md) | En savoir plus sur la configuration de [!DNL Inventory Management] options qui déterminent la disponibilité de la source, les produits de vitrine et l’expédition des commandes. |
| [Gestion des sources](sources-manage.md) | Découvrez les sources et comment elles définissent les emplacements physiques où l’inventaire des produits est géré et expédié pour l’exécution des commandes, ou où les services sont disponibles. |
| [Gérer les stocks](stocks-manage.md) | Découvrez comment le stock est utilisé pour représenter un inventaire virtuel et agrégé de produits pour les sources de vos canaux de vente. |
| [Gestion des quantités](quantities-manage.md) | Découvrez comment attribuer des sources et des quantités pour de nouveaux produits ou modifier des produits existants. |
| [Gestion des commandes et des envois](shipments.md) | En savoir plus sur les [!DNL Inventory Management] fonctionnalités et options pour gérer les quantités d’inventaire tout au long du processus d’expédition. |
| [Référence de ligne de commande](cli.md) | En savoir plus sur les commandes fournies par le [!DNL Inventory Management] pour gérer les données d’inventaire et les paramètres de configuration. |

{style="table-layout:auto"}

## Informations sur les développeurs

Voir [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) dans la documentation destinée aux développeurs pour plus d’informations sur l’architecture des modules, les API et la personnalisation des algorithmes.

## Documentation sur Commerce

{{docs-links}}

## Résolution des problèmes et assistance

Si vous avez besoin d’informations ou si vous avez des questions qui ne sont pas abordées dans ce guide, utilisez les ressources suivantes :

- [Incohérences de réservation à grand nombre](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-30112-magento-patch-large-number-reservation-inconsistencies.html)
- [Problèmes d’incohérence de l’inventaire](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33281-magento-patch-inventory-inconsistency-issues.html)
- [Échantillons dont l’inventaire n’a pas atteint &quot;0&quot;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-17/mdva-34850-swatches-not-strike-through-inventory-reaches-0.html)
- [Etat du stock incorrect après l’installation du stock](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [tickets d’assistance](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket): soumettez un ticket pour recevoir de l’aide supplémentaire.
