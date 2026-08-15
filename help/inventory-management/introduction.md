---
title: Présentation de  [!DNL Inventory Management]
description: Découvrez comment utiliser  [!DNL Inventory Management] pour [!DNL Commerce] gérer les stocks entre les sources et les stocks, calculer les quantités vendables, suivre les réservations et prendre en charge l’exécution des commandes. Utilisez l’Administration pour configurer les paramètres et générer des rapports, ainsi que l’interface de ligne de commande pour les modifications de configuration et en arrière-plan.
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
TQID: https://experienceleague.adobe.com/7v-G-DZEki7y-4HSmq-rJxsmu6vih26jRYYCRRUF-XY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
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
source-git-commit: 125a49f740639bce0ced8063074ca43d627c0eac
workflow-type: tm+mt
source-wordcount: 371
ht-degree: 0%

---

# Présentation de [!DNL Inventory Management]

[!DNL Inventory Management] pour [!DNL Commerce] aide les commerçants à gérer les stocks sur un ou plusieurs sites web et emplacements de produits physiques ou virtuels. Il fournit des outils dans l’interface d’administration et de ligne de commande pour configurer l’inventaire, suivre le stock disponible et agréger les quantités vendables, protéger l’inventaire lors du passage en caisse et prendre en charge l’exécution des commandes. Vous pouvez utiliser des [!DNL Inventory Management] pour un réseau à source unique ou multi-sources qui comprend des entrepôts, des magasins, des lieux de retrait, des chargeurs directs et d&#39;autres lieux de livraison.

## Méthodes d’utilisation de [!DNL Inventory Management]

- **Admin :** permet de définir des options d’inventaire et de générer des rapports d’inventaire.
- **Interface de ligne de commande :** exécutez les commandes de configuration et appliquez les modifications d’inventaire en arrière-plan.
- **Portée de la configuration :** configurer les paramètres d’inventaire globalement, par source ou par produit.

## Fonctionnalités clés

[!DNL Inventory Management] fonctionnalités incluent :

- Différentes configurations pour les commerçants dont le stock provient d’une ou de plusieurs sources
- Stocks pour le suivi des quantités vendables agrégées dans les sources affectées
- Protection des passages en caisse simultanés
- Algorithmes de correspondance d’expédition qui prennent en charge les recommandations d’exécution basées sur la distance ou la priorité

>[!NOTE]
>
>Ces fonctionnalités ont été développées dans le cadre du projet [&#128279;](https://github.com/magento/inventory) (anciennement MSI) par le biais du programme d&#39;ingénierie communautaire.<br/>
>
>Le module [!DNL Inventory Management] est installé avec Magento Open Source et Adobe Commerce, toutes les fonctionnalités étant activées par défaut. Pour plus d’informations sur les modifications incluses dans les versions de module, voir [&#x200B; Notes de mise à jour &#x200B;](release-notes.md).

## Terminologie de base

Il est important de comprendre les termes suivants lorsque vous travaillez avec [!DNL Inventory Management] :

[!UICONTROL Sources] représentent des emplacements physiques où sont stockés et expédiés les produits disponibles. Voir [Stocks et sources](sources-stocks.md) pour obtenir des exemples et des diagrammes. (N’importe quel emplacement peut être désigné comme source de produits virtuels.)

[!UICONTROL Stocks] mapper un canal de vente (actuellement limité aux sites web) aux emplacements source et au stock disponible. Un stock peut correspondre à plusieurs canaux de vente, mais un canal de vente ne peut être affecté qu’à un seul stock.

[!UICONTROL Aggregate Salable Quantity] est le stock virtuel total qui peut être vendu par l&#39;intermédiaire d&#39;un canal de vente. Le montant est calculé pour toutes les sources affectées à un stock.

[!UICONTROL Reservations] effectuer le suivi des déductions de la quantité vendable lorsque les clients ajoutent des produits au panier et passent en caisse. Lorsqu&#39;une commande est expédiée, la réservation efface et déduit les montants expédiés de quantités de stock d&#39;origine spécifiques.
