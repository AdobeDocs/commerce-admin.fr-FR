---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Inventory]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Catalog] &gt; [!UICONTROL Inventory] de l’administrateur Commerce.
exl-id: 80113a31-3585-4ee1-95af-31efc09389eb
feature: Configuration, Inventory
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Inventory]

{{config}}

>[!NOTE]
>
>[!DNL Inventory Management] pour Adobe Commerce et Magento Open Source vous donne les outils nécessaires pour gérer votre inventaire de produits. Les commerçants disposant d’un seul magasin pour plusieurs entrepôts, magasins, lieux de ramassage, expéditeurs, etc. peuvent utiliser ces fonctionnalités pour conserver les quantités à vendre et traiter les envois afin de terminer les commandes. Pour plus d’informations sur ces fonctionnalités et sur leur utilisation pour gérer des stocks à plusieurs emplacements, consultez le [_[!DNL Inventory Management] Guide de l’utilisateur _](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html).

## [!UICONTROL Stock Options]

![Options Stock](./assets/catalog-inventory-stock-options.png)<!-- zoom -->

<!-- [Stock Options](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/global-options) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Decrease Stock When Order is Placed] | Global | Si celle-ci est définie sur `Yes`, la quantité en stock est réduite lors de la commande. Lorsque _Gérer les stocks_ est activé, les réservations sont renseignées pour les produits et les quantités commandés. Options : `Yes` / `No` |
| [!UICONTROL Set Items' Status to be in Stock When Order is Cancelled] | Affichage en magasin | Si celle-ci est définie sur `Yes`, renvoie l’article en stock lorsque la commande est annulée. Si l’option _Gérer le stock_ est activée, la réservation est effacée pour les produits et les quantités annulés. Options : `Yes` / `No` |
| [!UICONTROL Display Out of Stock Products] | Global | S’il est défini sur `Yes`, affiche les produits en rupture de stock. Si les alertes de produit sont également activées, les clients peuvent s’inscrire pour être avertis lorsque le produit est disponible. Options : `Yes` / `No` |
| [!UICONTROL Only X left Threshold] | Site Web | Définit le seuil pour le message `Only x left`. Par exemple, s’il est défini sur 3, le message s’affiche lorsqu’un article est en stock, ou lorsqu’il y en a trois ou moins. Le message n’apparaît pas si la valeur est définie sur `0`. |
| [!UICONTROL Display products availability in Stock on Storefront] | Affichage en magasin | S’il est défini sur `Yes`, affiche un message `In Stock` ou `Out of Stock` sur la page du produit. Options : `Yes` / `No` |
| [!UICONTROL Enable Inventory Check On Cart Load] | Global | Détermine si une vérification d’inventaire est effectuée lors du chargement d’un produit dans le panier. La désactivation de cette vérification de stock peut améliorer les performances des étapes de passage en caisse, en particulier lorsqu’il y a de nombreux articles dans le panier. Cependant, si vous ignorez la prévalidation, les clients peuvent voir des erreurs _out of stock_ plus tard dans le processus de passage en caisse. Options : `Yes` / `No` |
| [!UICONTROL Synchronize with Catalog] | Global | Lorsqu’elle est définie sur `Yes`, les données d’inventaire sont ajustées en fonction des modifications du catalogue (telles que les suppressions de produits, les modifications de SKU de produits et les modifications de type de produit) et conservent la cohérence entre l’inventaire et le catalogue. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Product Stock Options]

![Options Stock de produits](./assets/catalog-inventory-product-stock-options.png)<!-- zoom -->

<!-- [Product Stock Options](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/global-options) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Manage Stock] | Global | Détermine si vous utilisez le contrôle d’inventaire complet pour gérer les éléments de votre catalogue. Options : <br/>**Oui** - Active le contrôle de stock complet pour suivre le nombre d’articles actuellement en stock. <br/>**Non** - Ne suit pas le nombre d’éléments actuellement en stock. |
| [!UICONTROL Backorders] | Global | Détermine la manière dont votre boutique gère les commandes en arrière-plan. Un ordre de traitement ne modifie pas l’état de traitement de la commande. Les fonds sont toujours autorisés ou capturés immédiatement lorsque la commande est passée, que le produit soit en stock ou non. Lorsque le produit est disponible, il est expédié. Options : <br/>**sans commandes arrière** - N’accepte pas les commandes arrière lorsque le produit est en rupture de stock. <br/>**Autoriser la quantité inférieure à 0** - Accepte les commandes en arrière-plan lorsque la quantité est inférieure à zéro. <br/>**Allow Qty Below 0 and Notify Customer** - Accepte les commandes en arrière-plan lorsque la quantité est inférieure à zéro, mais avertit les clients que des commandes peuvent toujours être passées. |
| [!UICONTROL Use deferred Stock update] | Global | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine s’il faut différer la mise à jour du stock si les commandes en arrière-plan sont autorisées (l’option _Commandes en arrière_ est définie sur autre chose que la valeur par défaut `No backorders`). Il fonctionne pour un seul produit ou un site web entier et utilise le mécanisme _File d’attente des tâches_ pour permettre la mise à jour asynchrone des indicateurs de quantité d’inventaire après le passage des commandes. Cette option fonctionne également avec [Placement de commande asynchrone](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/high-throughput-order-processing.html#asynchronous-order-placement) en combinaison avec [Inventory management](../../inventory-management/introduction.md). |
| Quantité maximale autorisée dans le panier | Global | Détermine le nombre maximal de produits qu’il est possible d’acheter dans une seule commande. Par défaut, la quantité maximale est définie sur 10 000. |
| [!UICONTROL Out-of-Stock Threshold] | Global | Détermine le niveau de stock auquel un produit est considéré comme en rupture de stock. Options : <br/>**Montant positif** - Si _Bordures_ est désactivé, saisissez un montant positif. Lorsque les commandes d’arrière-plan sont activées, ce montant est ignoré. <br/>**Zéro** - Avec _Backorders_ activés, la saisie de `0` permet d’obtenir des commandes d’arrière-plan infinies. <br/>**Montant négatif** - Avec _Backorders_ activés, nous vous recommandons de saisir un montant négatif. Le montant est ajouté à la quantité vendable. Par exemple, saisissez -50 pour autoriser les commandes jusqu’à ce montant. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Global | Détermine le montant minimum d’un article disponible à l’achat selon le groupe de clients. Par défaut, la quantité minimale est définie sur 1. Cliquez sur **[!UICONTROL Add Minimum Qty]** pour saisir une autre valeur pour un groupe de clients spécifique. |
| [!UICONTROL Notify for Quantity Below] | Global | Détermine le niveau de stock auquel la notification est envoyée indiquant que l’inventaire est tombé en dessous du seuil. |
| [!UICONTROL Enable Qty Increments] | Global | Détermine si les articles peuvent être vendus en quantité par incréments. Options : `Yes` / `No` |
| [!UICONTROL Qty Increments] | Global | Définit le nombre de produits qui constituent un incrément de quantité. |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | Global | Détermine si les éléments inclus dans les avoirs sont automatiquement renvoyés à l’inventaire. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Bulk Operations]

![Opérations d’administration en bloc](./assets/catalog-inventory-admin-bulk-operations.png)<!-- zoom -->

<!-- [Admin Bulk Operations](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/global-options) -->

>[!NOTE]
>
>Pour configurer et prendre en charge les **gestionnaires de file d’attente asynchrones**, vous devez utiliser la ligne de commande. Cela peut nécessiter l’aide des développeurs. Voir [Démarrage des consommateurs de la file d’attente de messages](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) dans le _Guide de configuration_.

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Run asynchronously] | Global | Détermine si vous exécutez des opérations en bloc de manière asynchrone pour des actions de produits de masse, y compris [bulk](../../inventory-management/bulk-assignment.md) , attribuez des sources, annulez l’affectation des sources et [transférez l’inventaire à la source](../../inventory-management/inventory-transfer.md). Il collecte les actions en masse jusqu’à _[!UICONTROL Asynchronous batch size]_, puis exécute ces actions. Cette fonctionnalité est désactivée par défaut. Nous vous recommandons de passer en revue vos performances avec des actions en bloc avant de les activer. Options :<br/>**`Yes`**- Exécute toutes les opérations en masse pour [!DNL Inventory Management] de manière asynchrone. Pour l’activer, vous devez configurer un gestionnaire de file d’attente asynchrone.<br/>**`No`**- Valeur par défaut. N’exécute pas les opérations en bloc de manière asynchrone. |
| [!UICONTROL Asynchronous batch size] | Global | Définissez **[!UICONTROL Run asynchronously]** sur `Yes` pour saisir une valeur pour le champ _[!UICONTROL Asynchronous batch size]_. <br/>La taille de lot par défaut est 100. Lorsque les processus en masse atteignent ce montant, ils sont exécutés. |

{style="table-layout:auto"}

## [!UICONTROL Inventory Indexer Settings]

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Stock/Source reindex strategy] | Global | Détermine la stratégie utilisée pour la réindexation des stocks/sources. Options : `Synchronous` / `Asynchronous` (un gestionnaire de file d’attente asynchrone doit être configuré pour le mode asynchrone) |

{style="table-layout:auto"}

>[!NOTE]
>
> En raison des dépendances des mises à jour d’inventaire pour les activités liées aux commandes, l’indexeur d’inventaire est également déclenché lors de l’enregistrement du produit, quel que soit le paramètre `Synchronous` ou `Asynchronous` .


## [!UICONTROL Distance Provider for Distance Based SSA]

![Fournisseurs de distance pour SSA basée sur les distances](./assets/catalog-inventory-distance-provider.png)<!-- zoom -->

<!-- [Distance Providers for Distance Based SSA](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/distance-priority-algorithm) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Provider] | Global | Détermine le fournisseur à utiliser pour l’algorithme de sélection Source de priorité des distances. Cette fonction est activée par défaut. Options : <br/>**`Google MAP`**- Utilise les services Google pour calculer la distance et l’heure entre l’adresse de destination de livraison et les emplacements source (adresse et coordonnées GPS). Cette option nécessite une clé API Google et peut entraîner des frais via Google.<br/>**`Offline Calculation`** - Calcule la distance à l’aide d’une base de données incorporée afin de déterminer la source la plus proche de l’adresse de destination de livraison. Pour utiliser cette option, vous pouvez avoir besoin de l’aide du développeur pour télécharger initialement le contenu de l’emplacement de la base de données pour tous les pays vers lesquels vous envoyez à l’aide d’une ligne de commande. |

{style="table-layout:auto"}

## [!UICONTROL Google Distance Provider]

![Fournisseur d’instances Google](./assets/catalog-inventory-distance-provider-settings.png)<!-- zoom -->

<!-- [Google Distance Provider](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/distance-priority-algorithm) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Google API key] | Global | Saisissez la clé d’API Google pour le fournisseur Google MAP. La clé provient de [!DNL Google Maps Platform] et [!DNL Geocoding API] et [!DNL Distance Matrix API] doivent être activés. Pour plus d’informations, voir [Configuration de l’algorithme de priorité des distances](../../inventory-management/distance-priority-algorithm.md#configure-the-distance-priority-algorithm) dans le _Guide d’Inventory management_. |
| [!UICONTROL Computation mode] | Global | Détermine les directions et les chemins pour calculer la distance entre l’adresse d’expédition et toutes les sources affectées au stock. Par défaut, les calculs utilisent le mode de conduite. Options : <br/>**`Driving`**- Paramètre par défaut, demande des instructions de conduite standard à l’aide du réseau routier.<br/>**`Walking`** - Demande des instructions de marche à l’aide de chemins piétons et de trottoirs (le cas échéant). <br/>**`Bicycling`**- Demande des instructions de vélo utilisant des pistes cyclables et des rues préférées (actuellement disponibles uniquement aux États-Unis et dans certaines villes canadiennes). |
| [!UICONTROL Value] | Global | Indique les éléments à calculer et à renvoyer pour la distance et l’heure des emplacements sources à l’adresse de destination de livraison. L’algorithme de priorité des distances recommande la source avec la distance ou le temps le plus court jusqu’à l’adresse de destination de livraison, qui fournit des envois plus rapides et éventuellement moins chers. Options : <br/>**`Distance`**- Renvoie la distance entre les points en mesures (kilomètres et mètres) ou impériales (kilomètres et pieds).<br/>**`Time to Destination`** - Renvoie le temps nécessaire pour voyager des emplacements source vers l’adresse d’expédition en heures et minutes. |

{style="table-layout:auto"}
