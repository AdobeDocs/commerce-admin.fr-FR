---
title: Présentation d’Inventory management
description: Découvrez comment utiliser [!DNL Inventory Management] des fonctionnalités permettant de gérer le stock à plusieurs emplacements afin que votre [!DNL Commerce] le magasin reflète fidèlement l’inventaire physique.
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Présentation d’Inventory management

[!DNL Inventory Management] pour [!DNL Commerce] vous donne les outils nécessaires pour gérer votre inventaire de produits. Les commerçants disposant d’un seul magasin pour plusieurs entrepôts, magasins, lieux de ramassage, expéditeurs, etc. peuvent utiliser ces fonctionnalités pour conserver les quantités à vendre et traiter les envois afin de terminer les commandes. Vous pouvez suivre les quantités de vos stocks, fournir aux clients des quantités de stock vendables précises pour tous vos sites web et les envoyer en fonction des recommandations en fonction de la distance ou de la priorité. Vous pouvez également configurer globalement vos configurations de produit préférées (pour tous les magasins et produits), par source et par produit. Ces fonctionnalités s’étendent à votre entreprise, ce qui vous permet de travailler depuis un seul entrepôt ou un réseau d’expédition complexe avec quelques paramètres supplémentaires.

[!DNL Inventory Management] les fonctionnalités incluent :

- Différentes configurations pour les commerçants dont l’inventaire provient d’une source unique et de plusieurs sources
- Stocks pour effectuer le suivi des quantités agrégées disponibles par le biais de sources affectées
- Protection des passages en caisse simultanés
- Algorithmes de correspondance des envois

>[!NOTE]
>
>Ces fonctionnalités ont été développées dans le cadre de la [Inventory management](https://github.com/magento/inventory) (anciennement MSI) par l’intermédiaire du programme d’ingénierie communautaire.<br/>
>
>La variable [!DNL Inventory Management] est installé avec Magento Open Source et Adobe Commerce, avec toutes les fonctionnalités activées par défaut. Pour plus d’informations sur les modifications incluses dans les versions de module, voir [Notes de mise à jour](release-notes.md).

## Terminologie de base

Il est important de comprendre les termes suivants lorsque vous utilisez [!DNL Inventory Management]:

[!UICONTROL **Sources**] représentent des emplacements physiques qui stockent et livrent les produits disponibles. Il peut s&#39;agir d&#39;entrepôts, de magasins en briques et de mortiers, de centres de distribution et d&#39;expéditeurs. (N’importe quel emplacement peut être désigné comme source des produits virtuels.)

[!UICONTROL **Stocks**] mapper un canal de vente (actuellement limité aux sites web) aux emplacements sources et à l’inventaire disponible. Un stock peut correspondre à plusieurs canaux de vente, mais un canal de vente ne peut être affecté qu’à un seul stock.

[!UICONTROL **Quantité vendue agrégée**] est l’inventaire virtuel total qui peut être vendu via un canal de vente. Le montant est calculé sur l&#39;ensemble des sources affectées à un stock.

[!UICONTROL **Réservations**] effectuer le suivi des déductions de la quantité vendue lorsque les clients ajoutent des produits au panier et effectuent le passage en caisse. Lorsqu’une commande est expédiée, la réservation efface et déduit les quantités expédiées des quantités d’inventaire source spécifiques.
