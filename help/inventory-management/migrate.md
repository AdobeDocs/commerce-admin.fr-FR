---
title: Mises à niveau de [!DNL Commerce]
description: Découvrez comment les mises à niveau d’Adobe Commerce et de Magento Open Source affectent les catalogues et  [!DNL Inventory Management]  configurations.
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# Mises à niveau de [!DNL Commerce]

Si vous avez utilisé un inventaire à source unique dans une version précédente, ces informations fournissent des détails sur les nouvelles fonctionnalités et les modifications apportées à vos configurations de catalogue et d’inventaire existantes.

[!DNL Inventory Management] pour Adobe Commerce et Magento Open Source comprend des fonctionnalités, des améliorations et une assistance développeur qui améliore et met à jour la gestion des stocks de produits et ajoute de nouvelles fonctionnalités. Toutes les fonctionnalités sont prêtes à l&#39;emploi, y compris l&#39;algorithme de sélection Source et le passage en caisse simultané pour faire correspondre les quantités de commande aux origines et à l&#39;exécution des commandes. Selon vos sites Web, vos magasins et votre type de commerçant, vous pouvez créer des stocks et des sources supplémentaires, affecter des quantités en stock, etc. Pour plus d’informations, voir [Inventory management](introduction.md).

Lorsque vous installez Magento Open Source 2.4.x ou Adobe Commerce 2.4.x, les modifications initiales suivantes se produisent :

- [Inventory management](enable.md) s’active au niveau du magasin global ou du produit. L’option Gérer les stocks permet ou désactive le suivi des quantités en stock, les calculs des quantités à vendre agrégées et la gestion des réservations pour le suivi des achats jusqu’à la facturation et l’expédition. Vous pouvez désactiver cette option pour utiliser un ERP et d’autres services tiers pour gérer les stocks, les commandes et les expéditions. Pour plus d’informations, consultez la section Modules [!DNL Inventory Management] ci-dessous.

- Un [Source par défaut](sources-manage.md) et un [Stock par défaut](stocks-manage.md) s’ajoutent au système. Ne désactivez pas et ne supprimez pas ces valeurs par défaut. [!DNL Commerce] attribue les produits existants et nouvellement importés à ces valeurs par défaut.

  >[!IMPORTANT]
  >
  >L’utilisation du Stock par défaut et du Source par défaut est fortement déconseillée, car ils font partie du module `CatalogInventory`, qui est désormais obsolète. Il est recommandé de créer et d’utiliser plutôt des stocks et des sources personnalisés.

   - Les stocks fournissent une quantité vendable virtuelle agrégée avec des réservations pour suivre les paniers et les commandes, assurant ainsi un passage en caisse simultané.

   - Tous les produits existants de votre catalogue sont affectés au Source par défaut. Tant que vous n’ajoutez pas de nouvelles sources, l’interface du produit ne change pas. Si vous expédiez uniquement des produits à partir d’un seul emplacement, il n’existe aucune autre différence pour les sources. Vous pouvez créer des [sources](sources-add.md) et [affecter des quantités](quantities-manage.md) personnalisées par lieu d&#39;expédition.

   - Vous pouvez configurer une source comme emplacement de prélèvement et [attribuer des quantités](quantities-manage.md) pour cette source.

   - Votre site Web affecte au Stock par défaut. Vous pouvez créer des [stocks](stocks-add.md) personnalisés pour connecter les canaux de vente (sites web) et les sources (emplacements).

- Ajoutez des [options de configuration](configuration.md) supplémentaires à vos produits et à votre boutique globale. Certaines options de configuration existantes reçoivent des options et des comportements mis à jour :

   - Notifier pour la quantité ci-dessous envoie des notifications et déduit de la quantité commercialisable.

   - Le seuil de rupture de stock prend en charge les montants positifs, nuls et négatifs. Lorsque les reliquats sont activés, les montants positifs sont ignorés, considérés comme nuls (ou infinis).

   - Les reliquats prennent en charge les montants nuls (infinis) et négatifs. Lorsqu&#39;elle est activée, l&#39;option Notifier pour la quantité ci-dessous ne déduit pas de la quantité commercialisable.

- Les nouvelles réservations effectuent le suivi des ventes potentielles, en les convertissant en déductions de quantité lors de l&#39;expédition de la commande. Vous ne pouvez jamais accéder directement aux réservations ou les créer. [!DNL Commerce] crée et gère les réservations en arrière-plan par le biais de commandes, d’expéditions et d’avoirs.

- [Commandes et expéditions](shipments.md) comprend de nouvelles fonctionnalités pour recommander des expéditions à l’aide de l’algorithme de sélection Source et prendre en charge les expéditions partielles provenant de plusieurs sources pour exécuter une commande.

- De nouvelles [fonctions d’importation/exportation](inventory-import-export.md) vous permettent d’ajouter en masse des sources, de mettre à jour les quantités en stock et de définir le statut du stock (en stock ou en rupture de stock) pour tous les SKU de votre catalogue. Ces fonctions vous permettent de modifier une ou plusieurs sources, sélectionnées ou toutes les sources.

- Les nouvelles options en bloc via la page Grille de produits prennent en charge les [&#x200B; en bloc &#x200B;](bulk-assignment.md)affectation et annulation de l’affectation de sources et [&#x200B; transfert de l’inventaire vers la source](inventory-transfer.md).

- [!DNL Inventory Management] prend en charge les catalogues B2B. Actuellement, tous les produits B2B doivent être affectés au Source par défaut et au Stock par défaut.

## [!DNL Commerce Order Management] et [!DNL Inventory Management]

[Commerce Order Management (MCOM)](https://commerce-docs.github.io/oms-documentation-archive/) n&#39;est pas compatible avec le [!DNL Inventory Management]. Une fois installés, les modules MCOM fournissent toutes les fonctionnalités de gestion des stocks aux [!DNL Commerce], y compris la gestion de sources uniques et multiples, les stocks, les réservations, etc. Les modules [!DNL Inventory Management] sont désactivés par défaut.

MCOM fournit des fonctionnalités et des services complets pour la gestion avancée des commandes omnicanal, l&#39;inventaire mondial et le multi-sourcing, l&#39;exécution magasin à entrepôt et le service client centralisé. Pour obtenir la liste complète des fonctionnalités, reportez-vous à la [liste des fonctionnalités MCOM](https://commerce-docs.github.io/oms-documentation-archive/getting-started/feature-list/).

[!DNL Inventory Management] étend les fonctionnalités de [!DNL Commerce] existantes avec des options supplémentaires pour effectuer le suivi des commandes en cours de traitement, du stock disponible, du stock disponible pour un stock et des API pour le développement d’extensions.

## Modules [!DNL Inventory Management]

Vous pouvez désactiver [!DNL Inventory Management] modules pour :

- Accélérez la mise à niveau des commerçants actuellement sous Adobe Commerce ou Magento Open Source 2.0/2.1/2.2/2.3 et la migration vers la version 2.4.x.

- Utilisez des modules d’inventaire et de gestion des commandes personnalisés ou tiers.

- Utilisez des [!DNL Order Management System] pour la gestion des stocks. Le connecteur actuel ne prend pas en charge les interfaces [!DNL Inventory Management]. Les commerçants OMS effectuant une mise à niveau vers Adobe Commerce 2.4.0 doivent désactiver ces modules.

Pour plus d’informations, voir [Installation et mise à jour](install-update.md).
