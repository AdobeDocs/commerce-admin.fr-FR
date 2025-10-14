---
title: Guide  [!DNL Inventory Management] ’Inventory management
description: Informations complètes sur  [!DNL Inventory Management]  pour les administrateurs Adobe Commerce et Magento Open Source, y compris la migration et la configuration.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
source-git-commit: dbc0057f02bddf681d769bdaebfaf6b526c8dbd2
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 0%

---

# Présentation du guide [!DNL Inventory Management]

Ce guide est destiné aux administrateurs travaillant pour Adobe Commerce et Magento Open Source Admin. Elle fournit des informations détaillées sur l’activation de ce module, y compris la configuration et la gestion de ses fonctionnalités. Il suppose une compréhension de base de la configuration et des fonctionnalités de base du [!DNL Commerce].

[!DNL Inventory Management] dispose de deux domaines pour l’administration :

- Administration : utilisez cette zone pour accéder à l’interface utilisateur de configuration et aux rapports.
- L’interface de ligne de commande : utilisez cet outil pour exécuter les tâches d’installation et de configuration du serveur principal.

Ce guide couvre les sujets suivants :

| Objet | Description |
| ------- | ----------- |
| [Introduction](introduction.md) | Présentation des fonctionnalités [!DNL Inventory Management] que vous pouvez utiliser pour gérer le stock à plusieurs emplacements afin que votre boutique Commerce reflète précisément l’inventaire physique. |
| [Notes de mise à jour](release-notes.md) | Consultez les notes de mise à jour pour plus d’informations sur toutes les versions de [!DNL Inventory Management]. |
| Concepts de base des stocks | Découvrez les principes de base de la gestion des stocks : [Stocks et origines](sources-stocks.md), [sélection et réservations de la source](selection-reservations.md), [statut de la commande et de la réservation](order-status.md) et [types de produits](product-types.md) |
| Prise en main | Découvrez le module [!DNL Inventory Management] et comment il s’intègre à votre instance Commerce et aux opérations de stockage : [mises à niveau de Commerce](migrate.md), [installation et mise à jour du module](install-update.md), [types de sourcing pour les commerçants](merchant-sourcing.md) et [modifications de la structure de sourcing](expand-restructure.md) |
| [&#x200B; Configuration &#x200B;](configuration.md) | Découvrez la configuration des options de [!DNL Inventory Management] qui déterminent la disponibilité de la source, les produits de storefront et l’expédition des commandes. |
| [Gérer les sources](sources-manage.md) | Découvrez les sources et comment elles définissent les emplacements physiques où le stock de produits est géré et expédié pour l&#39;exécution des commandes, ou où les services sont disponibles. |
| [Gérer les stocks](stocks-manage.md) | Découvrez comment le stock est utilisé pour représenter un inventaire virtuel et agrégé de produits pour les sources de vos canaux de vente. |
| [Gérer les quantités](quantities-manage.md) | Découvrez comment attribuer des sources et des quantités pour de nouveaux produits ou modifier des produits existants. |
| [Gérer les commandes et les expéditions](shipments.md) | Découvrez les autres fonctionnalités et options de [!DNL Inventory Management] pour gérer les quantités en stock via le processus d&#39;expédition. |
| [Référence de l’interface de ligne de commande](cli.md) | Découvrez les commandes fournies par le module [!DNL Inventory Management] pour gérer les données d’inventaire et les paramètres de configuration. |

{style="table-layout:auto"}

## Informations sur le développeur

Voir [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) dans la documentation destinée aux développeurs pour plus d’informations sur l’architecture des modules, les API et la personnalisation des algorithmes.

## Documentation de Commerce

{{docs-links}}

## Dépannage et assistance

Si vous avez besoin d’informations ou si vous avez des questions qui ne sont pas abordées dans ce guide, utilisez les ressources suivantes :

- [Statut de stock incorrect après l’installation de l’inventaire](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html?lang=fr)
- [Tickets d’assistance](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=fr#submit-ticket) : envoyez un ticket pour recevoir de l’aide supplémentaire.
