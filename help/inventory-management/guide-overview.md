---
title: Guide [!DNL Inventory Management]
description: Guide de l’administrateur et de l’interface  [!DNL Inventory Management]  ligne de commande pour les stocks, les sources, les quantités, la configuration, les commandes et les expéditions dans Adobe Commerce et Magento Open Source.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
TQID: https://experienceleague.adobe.com/AFaKjUXrfZOMSYWjcW-dyD9OBMlQj6PkILIQiuT8YJU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: a3817847081e56272e3677dede02d992e760a2d4
workflow-type: tm+mt
source-wordcount: 327
ht-degree: 1%

---

# Vue d’ensemble des [!DNL Inventory Management]

Ce guide est destiné aux administrateurs qui gèrent le stock à plusieurs emplacements dans Adobe Commerce et Magento Open Source. Il fournit des procédures de configuration et de gestion pour le module [!DNL Inventory Management] et suppose une compréhension de base des fonctionnalités de base de la [!DNL Commerce].

Utilisez le **Admin** pour les tâches de configuration, de création de rapports et d’inventaire quotidien. Utilisez l’**interface de ligne de commande** pour l’installation, les mises à niveau et la configuration du serveur principal.

Ce guide couvre les sujets suivants :

| Objet | Description |
| ------- | ----------- |
| [Introduction](introduction.md) | Fonctionnalités, terminologie et adaptation de [!DNL Inventory Management] à votre boutique. |
| [Notes de mise à jour](release-notes.md) | Historique de publication des modules et problèmes connus. |
| [Principes de base des stocks](sources-stocks.md) | Concepts relatifs aux [stocks et origines](sources-stocks.md), [sélection et réservations de la source](selection-reservations.md), [statut de commande et de réservation](order-status.md) et [types de produits](product-types.md). |
| Prise en main | [Mises à niveau de &#x200B;](migrate.md), [installation et mises à jour](install-update.md), [types d&#39;approvisionnement des commerçants](merchant-sourcing.md) et [restructuration des stocks](expand-restructure.md). |
| [&#x200B; Configuration &#x200B;](configuration.md) | Paramètres globaux, de produit et d&#39;algorithme pour l&#39;affichage et l&#39;expédition du storefront. |
| [Gérer les sources](sources-manage.md) | Créer et gérer des emplacements d&#39;exécution. |
| [Gérer les stocks](stocks-manage.md) | Mappez les sources aux canaux de vente. |
| [Gérer les quantités](quantities-manage.md) | Affecter et mettre à jour des quantités de produits par source. |
| [Gérer les commandes et les expéditions](shipments.md) | Exécutez les commandes et gérez les expéditions à partir du stock. |
| [Référence de l’interface de ligne de commande](cli.md) | Tâches d’inventaire et de configuration de ligne de commande. |

{style="table-layout:auto"}

## Informations sur le développeur

Accédez à des ressources avancées pour les API, la personnalisation et l’architecture des modules. Voir [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) dans la documentation destinée aux développeurs d’API REST pour obtenir des détails techniques sur les API et la personnalisation des algorithmes.

## Documentation de Commerce

Consultez les guides des commerçants, du cloud et des développeurs pour obtenir de l’aide sur chaque aspect d’Adobe Commerce. Utilisez ces ressources pour tout besoin de configuration ou de gestion.

{{docs-links}}

## Dépannage et assistance

Utilisez les articles d’assistance et les systèmes de ticket pour résoudre rapidement les problèmes d’inventaire. Obtenez de l’aide supplémentaire pour l’état des stocks ou la gestion des produits.

Si vous avez besoin d’informations ou si vous avez des questions qui ne sont pas abordées dans ce guide, utilisez les ressources suivantes :

- [Statut de stock incorrect après l’installation de l’inventaire](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-29910)
- [Tickets d’assistance](https://experienceleague.adobe.com/fr/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-help-center-user-guide#support-case) : envoyez un ticket pour recevoir de l’aide supplémentaire.
