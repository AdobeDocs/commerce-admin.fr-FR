---
title: '[!DNL Commerce] mises à niveau'
description: Découvrez comment les mises à niveau d’Adobe Commerce et de Magento Open Source affectent les configurations de catalogue et de  [!DNL Inventory Management] .
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
source-git-commit: 392d8550741fe6fca3ea1301575c9ebb5e2483bd
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# [!DNL Commerce] mises à niveau

Si vous avez utilisé l’inventaire source unique dans une version précédente, ces informations fournissent des détails sur les nouvelles fonctionnalités et les modifications apportées à votre catalogue et à vos configurations d’inventaire existants.

[!DNL Inventory Management] pour Adobe Commerce et Magento Open Source comprend des fonctionnalités, des améliorations et une assistance aux développeurs qui améliorent et mettent à jour la gestion de tous les stocks de produits et en ajoutent de nouvelles. Toutes les fonctionnalités sont disponibles clé en main, y compris l’ algorithme de sélection de Source et l’ extraction simultanée pour faire correspondre les quantités de commandes aux sources et l’exécution des commandes. Selon vos sites web, magasins et types de commerçant, vous pouvez créer des sources et des stocks supplémentaires, attribuer des montants de stock, etc. Pour obtenir des informations complètes, voir [Inventory management](introduction.md).

Lorsque vous installez Magento Open Source 2.4.x ou Adobe Commerce 2.4.x, les modifications initiales suivantes se produisent :

- [Inventory management](enable.md) active au niveau du magasin ou du produit global. L’option Gérer les stocks permet ou désactive le suivi des quantités d’inventaire, le calcul des quantités agrégées pouvant être vendues et la gestion des réservations pour le suivi des achats jusqu’à la facture et l’envoi. Vous pouvez désactiver cette option pour utiliser un ERP et d’autres services tiers pour gérer les stocks, les commandes et les envois. Pour plus d’informations, voir [!DNL Inventory Management] Modules ci-dessous.

- Un [Source par défaut](sources-manage.md) et un [Stock par défaut](stocks-manage.md) ont été ajoutés au système. Ne désactivez ni ne supprimez ces valeurs par défaut. [!DNL Commerce] attribue ces valeurs par défaut aux produits existants et nouvellement importés.

  >[!IMPORTANT]
  >
  >L’utilisation du stock par défaut et du Source par défaut est fortement déconseillée car ils font partie du module `CatalogInventory`, qui est désormais obsolète. Il est recommandé de créer et d’utiliser plutôt des sources et des stocks personnalisés.

   - Les stocks fournissent une quantité vendable virtuelle agrégée avec des réservations pour effectuer le suivi des paniers et des commandes, ce qui garantit un passage en caisse simultané.

   - Tous les produits existants de votre catalogue sont affectés au Source par défaut. Tant que vous n’ajoutez pas de nouvelles sources, l’interface du produit ne change pas. Si vous n’envoyez que des produits d’un emplacement, il n’existe aucune autre différence pour les sources. Vous pouvez créer des [sources](sources-add.md) et [ attribuer des quantités](quantities-manage.md) par emplacement d’expédition.

   - Vous pouvez configurer une source comme emplacement de collecte et [attribuer des quantités](quantities-manage.md) à cette source.

   - Votre site web est affecté au stock par défaut. Vous pouvez créer des [stocks](stocks-add.md) personnalisés pour connecter les canaux de vente (sites web) et les sources (emplacements).

- Des [options de configuration](configuration.md) supplémentaires sont ajoutées à vos produits et à votre boutique globale. Certaines options de configuration existantes reçoivent des options et des comportements mis à jour :

   - Notifier pour la quantité ci-dessous envoie des notifications et déduit de la quantité vendable.

   - Le seuil en rupture de stock prend en charge les montants positifs, nuls et négatifs. Lorsque les commandes d’arrière-plan sont activées, les montants positifs sont ignorés, considérés comme nuls (ou infinis).

   - Les commandes d’arrière-plan prennent en charge des valeurs nulles (infinies) et négatives. Lorsqu’elle est activée, l’option Notifier pour la quantité inférieure ne déduit pas de la quantité vendable.

- Les nouvelles réserves effectuent le suivi des ventes potentielles, en convertissant en déductions de quantité lorsque la commande est expédiée. Vous n’avez jamais directement accès à ou n’avez jamais créé de réservation. [!DNL Commerce] crée et gère des réservations en coulisses par le biais de commandes, d’envois et de relevés de crédit.

- [Les commandes et envois](shipments.md) comprennent de nouvelles fonctionnalités pour recommander des envois à l’aide de l’algorithme de sélection Source et prennent en charge les envois partiels provenant de plusieurs sources pour répondre à une commande.

- Les nouvelles [fonctions d’import/export](inventory-import-export.md) vous permettent d’ajouter en masse des sources, de mettre à jour les quantités d’inventaire et de définir l’état du stock (en/hors stock) pour tous les SKU de votre catalogue. Ces fonctionnalités vous permettent de modifier une source, une source sélectionnée ou toutes.

- De nouvelles options en bloc par le biais de la page Grille de produits prennent en charge [l&#39;attribution et l&#39;annulation de l&#39;attribution des sources](bulk-assignment.md), et [le transfert de l&#39;inventaire à la source](inventory-transfer.md).

- [!DNL Inventory Management] prend en charge les catalogues B2B. Actuellement, tous les produits B2B doivent être affectés au Source par défaut et au Stock par défaut.

## [!DNL Commerce Order Management] et [!DNL Inventory Management]

[Commerce Order Management (MCOM)][1] n’est pas compatible avec [!DNL Inventory Management]. Une fois installés, les modules MCOM offrent toutes les fonctionnalités de gestion d’inventaire à [!DNL Commerce], y compris la gestion multi-source et unique, les stocks, les réservations, etc. Les modules [!DNL Inventory Management] sont désactivés par défaut.

MCOM fournit des fonctionnalités et des services complets pour la gestion avancée des commandes omnicanal, l’inventaire global et le multi-approvisionnement, l’exécution du stockage vers l’entrepôt et un service client centralisé. Pour obtenir la liste complète des fonctionnalités, consultez la [liste des fonctionnalités MCOM][2].

[!DNL Inventory Management] étend les fonctionnalités [!DNL Commerce] existantes avec des options supplémentaires pour effectuer le suivi des commandes en cours, de l’inventaire disponible, de l’inventaire disponible pour un stock et des API pour le développement d’extensions.

## [!DNL Inventory Management] modules

Vous pouvez désactiver les modules [!DNL Inventory Management] pour :

- Accélérez la mise à niveau des commerçants actuellement sur Adobe Commerce ou Magento Open Source 2.0/2.1/2.2/2.3 et migrez vers la version 2.4.x.

- Utilisez des modules personnalisés ou tiers de gestion des stocks et des commandes.

- Utilisez [!DNL Order Management System] pour la gestion des stocks. Le connecteur actuel ne prend pas en charge les interfaces [!DNL Inventory Management]. Pour les commerçants OMS effectuant une mise à niveau vers Adobe Commerce 2.4.0, ils doivent désactiver ces modules.

Pour plus d’informations, voir [Installation et mise à jour](install-update.md).

[1]: https://commerce-docs.github.io/oms-documentation-archive/
[2]: https://commerce-docs.github.io/oms-documentation-archive/getting-started/feature-list/
