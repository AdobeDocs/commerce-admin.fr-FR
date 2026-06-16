---
title: Présentation d’Inventory management
description: Découvrez comment utiliser  [!DNL Inventory Management]  fonctionnalités pour gérer le stock à plusieurs emplacements afin que votre  [!DNL Commerce]  reflète précisément l’inventaire physique.
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
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 364
ht-degree: 0%

---

# Présentation d’Inventory management

[!DNL Inventory Management] pour [!DNL Commerce] vous donne les outils nécessaires pour gérer votre inventaire de produits. Les commerçants disposant d’un magasin unique pour plusieurs entrepôts, magasins, lieux de retrait, chargeurs, etc. peuvent utiliser ces fonctionnalités pour gérer les quantités pour les ventes et gérer les expéditions pour terminer les commandes. Vous pouvez suivre les quantités en stock, fournir des quantités de stock vendables exactes aux clients pour tous vos sites Web et les expédier selon des recommandations basées sur la distance ou la priorité. Vous pouvez également configurer vos configurations de produit préférées globalement (pour tous les magasins et produits), par source et par produit. Ces fonctionnalités évoluent avec votre entreprise, ce qui vous permet de travailler à partir d&#39;un seul entrepôt ou d&#39;un réseau d&#39;expédition complexe avec quelques paramètres supplémentaires.

[!DNL Inventory Management] fonctionnalités incluent :

- Différentes configurations pour les commerçants dont l’inventaire provient d’une seule source et de plusieurs sources
- Stocks pour le suivi des quantités agrégées disponibles par le biais de sources affectées
- Protection des passages en caisse simultanés
- Algorithmes de correspondance des expéditions

>[!NOTE]
>
>Ces fonctionnalités ont été développées dans le cadre du projet [&#128279;](https://github.com/magento/inventory) (anciennement MSI) par le biais du programme d&#39;ingénierie communautaire.<br/>
>
>Le module [!DNL Inventory Management] est installé avec Magento Open Source et Adobe Commerce, toutes les fonctionnalités étant activées par défaut. Pour plus d’informations sur les modifications incluses dans les versions de module, voir [&#x200B; Notes de mise à jour &#x200B;](release-notes.md).

## Terminologie de base

Il est important de comprendre les termes suivants lorsque vous travaillez avec [!DNL Inventory Management] :

[!UICONTROL **Sources**] représentent les emplacements physiques où sont stockés et expédiés les produits disponibles. Ces emplacements peuvent comprendre des entrepôts, des magasins physiques, des centres de distribution et des chargeurs directs. (N’importe quel emplacement peut être désigné comme source de produits virtuels.)

[!UICONTROL **Stocks**] mappez un canal de vente (actuellement limité aux sites web) aux emplacements sources et au stock disponible. Un stock peut correspondre à plusieurs canaux de vente, mais un canal de vente ne peut être affecté qu’à un seul stock.

[!UICONTROL **Quantité de vente agrégée**] est le stock virtuel total qui peut être vendu par l&#39;intermédiaire d&#39;un canal de vente. Le montant est calculé pour toutes les sources affectées à un stock.

[!UICONTROL **Réservations**] suivez les déductions de la quantité vendable lorsque les clients ajoutent des produits au panier et effectuent la commande. Lorsqu&#39;une commande est expédiée, la réservation efface et déduit les montants expédiés de quantités de stock d&#39;origine spécifiques.
