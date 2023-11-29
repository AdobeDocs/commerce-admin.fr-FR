---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Inventory]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Catalog] &gt; [!UICONTROL Inventory] de l’administrateur Commerce.
exl-id: 80113a31-3585-4ee1-95af-31efc09389eb
feature: Configuration, Inventory
source-git-commit: 768c9fdc37127b408230983e39e98b11149713a7
workflow-type: tm+mt
source-wordcount: '1205'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Inventory]

{{config}}

>[!NOTE]
>
>[!DNL Inventory Management] pour Adobe Commerce et Magento Open Source vous donne les outils nécessaires pour gérer votre inventaire de produits. Les commerçants disposant d’un seul magasin pour plusieurs entrepôts, magasins, lieux de ramassage, expéditeurs, etc. peuvent utiliser ces fonctionnalités pour conserver les quantités à vendre et traiter les envois afin de terminer les commandes. Pour plus d’informations sur ces fonctionnalités et sur la manière dont vous pouvez les utiliser pour gérer des stocks à plusieurs emplacements, voir [_[!DNL Inventory Management] Guide de l’utilisateur _](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html).

## [!UICONTROL Stock Options]

![Options Stock](./assets/catalog-inventory-stock-options.png)<!-- zoom -->

<!-- [Stock Options](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Decrease Stock When Order is Placed] | Global | Si la variable est définie sur `Yes`, réduit la quantité en stock au moment de la commande. Avec _Gérer Stock_ activée, les réservations sont renseignées pour les produits commandés et les quantités. Options : `Yes` / `No` |
| [!UICONTROL Set Items' Status to be in Stock When Order is Cancelled] | Affichage en magasin | Si la variable est définie sur `Yes`, renvoie l’article en stock lorsque la commande est annulée. Avec _Gérer Stock_ activée, la réservation est effacée pour les produits et les quantités annulés. Options : `Yes` / `No` |
| [!UICONTROL Display Out of Stock Products] | Global | Si la variable est définie sur `Yes`, affiche les produits en rupture de stock. Si les alertes de produit sont également activées, les clients peuvent s’inscrire pour être avertis lorsque le produit est disponible. Options : `Yes` / `No` |
| [!UICONTROL Only X left Threshold] | Site Web | Définit le seuil de la variable `Only x left` message. Par exemple, s’il est défini sur 3, le message s’affiche lorsqu’un article est en stock, ou lorsqu’il y en a trois ou moins. Le message n’apparaît pas si la valeur est définie sur `0`. |
| [!UICONTROL Display products availability in Stock on Storefront] | Affichage en magasin | Si la variable est définie sur `Yes`, affiche une `In Stock` ou `Out of Stock` sur la page du produit. Options : `Yes` / `No` |
| [!UICONTROL Enable Inventory Check On Cart Load] | Global | Détermine si une vérification d’inventaire est effectuée lors du chargement d’un produit dans le panier. La désactivation de cette vérification de stock peut améliorer les performances des étapes de passage en caisse, en particulier lorsqu’il y a de nombreux articles dans le panier. Cependant, si vous ignorez la prévalidation, les clients peuvent voir _en rupture de stock_ plus tard dans le processus de passage en caisse. Options : `Yes` / `No` |
| [!UICONTROL Synchronize with Catalog] | Global | Lorsque la variable est définie sur `Yes`, les données d’inventaire sont ajustées en fonction des modifications du catalogue (telles que les suppressions de produits, les modifications de SKU de produits et les changements de type de produit) et maintiennent la cohérence entre l’inventaire et le catalogue. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Product Stock Options]

![Options d’inventaire des produits](./assets/catalog-inventory-product-stock-options.png)<!-- zoom -->

<!-- [Product Stock Options](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Manage Stock] | Global | Détermine si vous utilisez le contrôle d’inventaire complet pour gérer les éléments de votre catalogue. Options : <br/>**Oui** - Active le contrôle complet des stocks pour suivre le nombre d’articles actuellement en stock. <br/>**Non** - Ne suit pas le nombre d’éléments actuellement en stock. |
| [!UICONTROL Backorders] | Global | Détermine la manière dont votre boutique gère les commandes en arrière-plan. Un ordre de traitement ne modifie pas l’état de traitement de la commande. Les fonds sont toujours autorisés ou capturés immédiatement lorsque la commande est passée, que le produit soit en stock ou non. Lorsque le produit est disponible, il est expédié. Options : <br/>**Aucun support** - N’accepte pas les commandes en arrière-plan lorsque le produit est en rupture de stock. <br/>**Autoriser une valeur inférieure à 0** - Accepte les commandes en arrière-plan lorsque la quantité est inférieure à zéro. <br/>**Autoriser la quantité inférieure à 0 et informer le client** - Accepte les commandes en arrière-plan lorsque la quantité est inférieure à zéro, mais avertit les clients que les commandes peuvent toujours être passées. |
| [!UICONTROL Use deferred Stock update] | Global | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine s’il faut différer la mise à jour du stock si les commandes en arrière-plan sont autorisées (la variable _Commandes précédentes_ est définie sur n’importe quel élément en dehors de la variable `No backorders` valeur par défaut). Il fonctionne pour un seul produit ou un site web entier et utilise la variable _File d’attente des tâches_ pour permettre aux indicateurs de quantité de stock de se mettre à jour de manière asynchrone une fois les commandes passées. Cette option fonctionne également avec [Placement de l’ordre asynchrone](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/high-throughput-order-processing.html#asynchronous-order-placement) en combinaison avec [Inventory management](../../inventory-management/introduction.md). |
| Quantité maximale autorisée dans le panier | Global | Détermine le nombre maximal de produits qu’il est possible d’acheter dans une seule commande. Par défaut, la quantité maximale est définie sur 10 000. |
| [!UICONTROL Out-of-Stock Threshold] | Global | Détermine le niveau de stock auquel un produit est considéré comme en rupture de stock. Options : <br/>**Montant positif** - Avec _Arrière-plan_ désactivé, saisissez un montant positif. Lorsque les commandes d’arrière-plan sont activées, ce montant est ignoré. <br/>**Zéro** - Avec _Arrière-plan_ activé, saisie `0` permet d’obtenir des commandes d’arrière-plan infinies. <br/>**Montant négatif** - Avec _Arrière-plan_ activée, nous vous recommandons de saisir un montant négatif. Le montant est ajouté à la quantité vendable. Par exemple, saisissez -50 pour autoriser les commandes jusqu’à ce montant. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Global | Détermine le montant minimum d’un article disponible à l’achat selon le groupe de clients. Par défaut, la quantité minimale est définie sur 1. Cliquez sur **[!UICONTROL Add Minimum Qty]** pour saisir une autre valeur pour un groupe de clients spécifique. |
| [!UICONTROL Notify for Quantity Below] | Global | Détermine le niveau de stock auquel la notification est envoyée indiquant que l’inventaire est tombé en dessous du seuil. |
| [!UICONTROL Enable Qty Increments] | Global | Détermine si les articles peuvent être vendus en quantité par incréments. Options : `Yes` / `No` |
| [!UICONTROL Qty Increments] | Global | Définit le nombre de produits qui constituent un incrément de quantité. |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | Global | Détermine si les éléments inclus dans les avoirs sont automatiquement renvoyés à l’inventaire. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Bulk Operations]

![Opérations d’administration en bloc](./assets/catalog-inventory-admin-bulk-operations.png)<!-- zoom -->

<!-- [Admin Bulk Operations](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

>[!NOTE]
>
>Configuration et support **gestionnaires de file d’attente asynchrones**, vous devez utiliser la ligne de commande. Cela peut nécessiter l’aide des développeurs. Voir [Démarrage des consommateurs de la file de messages](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) dans le _Guide de configuration_.

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Run asynchronously] | Global | Détermine si vous exécutez des opérations en bloc de manière asynchrone pour des actions de produits de masse, y compris [bulk](../../inventory-management/bulk-assignment.md) affecter des sources, annuler l’affectation de sources et [transférer l’inventaire vers la source](../../inventory-management/inventory-transfer.md). Elle collecte des actions en bloc jusqu’à la variable _[!UICONTROL Asynchronous batch size]_, puis exécute ces actions. Cette fonctionnalité est désactivée par défaut. Nous vous recommandons de passer en revue vos performances avec des actions en bloc avant de les activer. Options :<br/>**`Yes`**: exécute toutes les opérations en masse pour [!DNL Inventory Management] de manière asynchrone. Pour l’activer, vous devez configurer un gestionnaire de file d’attente asynchrone.<br/>**`No`**- Par défaut. N’exécute pas les opérations en bloc de manière asynchrone. |
| [!UICONTROL Asynchronous batch size] | Global | Définir **[!UICONTROL Run asynchronously]** to `Yes` pour saisir une valeur pour _[!UICONTROL Asynchronous batch size]_champ . <br/>La taille de lot par défaut est 100. Lorsque les processus en masse atteignent ce montant, ils sont exécutés. |

{style="table-layout:auto"}

## [!UICONTROL Inventory Indexer Settings]

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Stock/Source reindex strategy] | Global | Détermine la stratégie utilisée pour la réindexation des stocks/sources. Options : `Synchronous` / `Asynchronous` (un gestionnaire de file d’attente asynchrone doit être configuré pour le mode asynchrone) |

{style="table-layout:auto"}

>[!NOTE]
>
> En raison des dépendances des mises à jour de stock pour les activités liées aux commandes, l’indexeur d’inventaire est également déclenché lors de l’enregistrement du produit, quelle que soit la variable `Synchronous` ou `Asynchronous` .


## [!UICONTROL Distance Provider for Distance Based SSA]

![Fournisseurs de distance pour l’ASS basée sur les distances](./assets/catalog-inventory-distance-provider.png)<!-- zoom -->

<!-- [Distance Providers for Distance Based SSA](https://docs.magento.com/user-guide/catalog/inventory-configure-distance-priority.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Provider] | Global | Détermine le fournisseur à utiliser pour l’algorithme de sélection de la source de priorité des distances. Cette fonction est activée par défaut. Options : <br/>**`Google MAP`**- Utilise les services Google pour calculer la distance et l’heure entre l’adresse de destination de l’expédition et les emplacements sources (adresse et coordonnées GPS). Cette option nécessite une clé API Google et peut entraîner des frais via Google.<br/>**`Offline Calculation`** - Calcule la distance à l’aide d’une base de données incorporée afin de déterminer la source la plus proche de l’adresse de destination de livraison. Pour utiliser cette option, vous pouvez avoir besoin de l’aide du développeur pour télécharger initialement le contenu de l’emplacement de la base de données pour tous les pays vers lesquels vous envoyez à l’aide d’une ligne de commande. |

{style="table-layout:auto"}

## [!UICONTROL Google Distance Provider]

![Fournisseur de distance Google](./assets/catalog-inventory-distance-provider-settings.png)<!-- zoom -->

<!-- [Google Distance Provider](https://docs.magento.com/user-guide/catalog/inventory-configure-distance-priority.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Google API key] | Global | Saisissez la clé d’API Google pour le fournisseur Google MAP. La clé provient de la fonction [!DNL Google Maps Platform] et doivent avoir [!DNL Geocoding API] et [!DNL Distance Matrix API] activée. Pour plus d’informations, voir [Configuration de l’algorithme de priorité des distances](../../inventory-management/distance-priority-algorithm.md#configure-the-distance-priority-algorithm) dans le _Guide Inventory management_. |
| [!UICONTROL Computation mode] | Global | Détermine les directions et les chemins pour calculer la distance entre l’adresse d’expédition et toutes les sources affectées au stock. Par défaut, les calculs utilisent le mode de conduite. Options : <br/>**`Driving`**- Paramètre par défaut, demande des instructions de conduite standard à l’aide du réseau routier.<br/>**`Walking`** - Demande des instructions de marche en utilisant des chemins piétonniers et des trottoirs (le cas échéant). <br/>**`Bicycling`**- Demande des instructions cyclables en utilisant des pistes cyclables et des rues de choix (actuellement disponibles uniquement aux États-Unis et dans certaines villes canadiennes). |
| [!UICONTROL Value] | Global | Indique les éléments à calculer et à renvoyer pour la distance et l’heure des emplacements sources à l’adresse de destination de livraison. L’algorithme de priorité des distances recommande la source avec la distance ou le temps le plus court jusqu’à l’adresse de destination de livraison, qui fournit des envois plus rapides et éventuellement moins chers. Options : <br/>**`Distance`**- Renvoie la distance entre les points en mesures (kilomètres et mètres) ou impériales (kilomètres et pieds).<br/>**`Time to Destination`** - Renvoie le temps nécessaire pour voyager des emplacements sources vers l’adresse d’expédition en heures et minutes. |

{style="table-layout:auto"}
