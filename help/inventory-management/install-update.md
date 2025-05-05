---
title: Installer, mettre à jour et supprimer [!DNL Inventory Management]
description: Découvrez comment gérer le métapaquet  [!DNL Inventory Management] .
exl-id: d088ff35-c0e1-41c8-89fb-78180eaefbf7
level: Experienced
feature: Inventory, Install
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 0%

---

# Installation, mise à jour et suppression de [!DNL Inventory Management]

Les modules [!DNL Inventory Management] fournissent toutes les fonctionnalités et options d’inventaire pour que les commerçants utilisant une ou plusieurs sources puissent gérer les quantités de produits et les stocks pour les canaux de vente. Ces fonctionnalités sont disponibles dans les versions 2.4.x d’Adobe Commerce et de Magento Open Source.

Ces fonctionnalités et extensions ont été développées dans le cadre du projet [Inventory](https://github.com/magento/inventory) via le programme Magento Open Source Community Engineering.

[!DNL Inventory Management] s’installe dans les versions 2.3.x et 2.4.x d’Adobe Commerce et de Magento Open Source, avec toutes les fonctionnalités activées par défaut. Aucune étape supplémentaire n’est nécessaire pour activer ces fonctions d’inventaire. Les mises à niveau à partir de la version v2.1.x ou 2.2.x peuvent nécessiter des étapes supplémentaires. Voir [Mise à niveau d’Inventory management](#upgrade-inventory-management).

Il est recommandé d’effectuer l’installation conformément à la [installation sur site avec démarrage rapide](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html){target="_blank"}. Installez avec un métapaquet pour recevoir tous les modules [!DNL Inventory Management].

La ligne suivante du métapaquet `composer.json` s’installe [!DNL Inventory Management] :

```json
        magento/inventory-composer-metapackage = 1.1.3
```

Pour obtenir la liste des versions de métapaquets [!DNL Inventory Management], consultez les [notes de mise à jour](release-notes.md).

Le processus d’installation [!DNL Inventory Management] ajoute tous les modules au fichier `<Magento_installation_directory>/app/etc/config.php`. Une valeur `1` indique que le module correspondant est activé. La liste suivante de modules est ajoutée :

```php
        'Magento_Inventory' => 1,
        'Magento_InventoryAdminUi' => 1,
        'Magento_InventoryAdvancedCheckout' => 1,
        'Magento_InventoryApi' => 1,
        'Magento_InventoryBundleProduct' => 1,
        'Magento_InventoryBundleProductAdminUi' => 1,
        'Magento_InventoryCatalog' => 1,
        'Magento_InventorySales' => 1,
        'Magento_InventoryCatalogAdminUi' => 1,
        'Magento_InventoryCatalogApi' => 1,
        'Magento_InventoryCatalogSearch' => 1,
        'Magento_InventoryConfigurableProduct' => 1,
        'Magento_InventoryConfigurableProductAdminUi' => 1,
        'Magento_InventoryConfigurableProductIndexer' => 1,
        'Magento_InventoryConfiguration' => 1,
        'Magento_InventoryConfigurationApi' => 1,
        'Magento_InventoryDistanceBasedSourceSelection' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionAdminUi' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionApi' => 1,
        'Magento_InventoryElasticsearch' => 1,
        'Magento_InventoryExportStockApi' => 1,
        'Magento_InventoryIndexer' => 1,
        'Magento_InventorySalesApi' => 1,
        'Magento_InventoryGroupedProduct' => 1,
        'Magento_InventoryGroupedProductAdminUi' => 1,
        'Magento_InventoryGroupedProductIndexer' => 1,
        'Magento_InventoryImportExport' => 1,
        'Magento_InventoryCache' => 1,
        'Magento_InventoryLowQuantityNotification' => 1,
        'Magento_InventoryLowQuantityNotificationApi' => 1,
        'Magento_InventoryMultiDimensionalIndexerApi' => 1,
        'Magento_InventoryProductAlert' => 1,
        'Magento_InventoryRequisitionList' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryExportStock' => 1,
        'Magento_InventorySalesAdminUi' => 1,
        'Magento_InventorySalesFrontendUi' => 1,
        'Magento_InventorySetupFixtureGenerator' => 1,
        'Magento_InventoryShipping' => 1,
        'Magento_InventorySourceDeductionApi' => 1,
        'Magento_InventorySourceSelection' => 1,
        'Magento_InventorySourceSelectionApi' => 1,
        'Magento_InventoryLowQuantityNotificationAdminUi' => 1,
        'Magento_InventoryShippingAdminUi' => 1,
        'Magento_InventoryGraphQl' => 1,
```

## Activer les fonctionnalités [!DNL Inventory Management]

Lorsqu’elle est installée, mise à niveau ou mise à jour, l’option _[!UICONTROL Manage Stock]_&#x200B;dans l’Administration est activée par défaut. Cette option permet le suivi et la gestion des stocks, mais n’affecte pas le statut du module. Pour désactiver les modules, reportez-vous à la section suivante.

Pour plus d’informations sur les configurations, voir [ Configuration d’Inventory management ](configuration.md).

## Désactiver Inventory management

>[!IMPORTANT]
>
>L’utilisation des modules [!DNL Inventory Management] par défaut est vivement recommandée. L’autre module [!DNL CatalogInventory], qui est utilisé pour les systèmes avec des modules [!DNL Inventory Management] désactivés, est désormais obsolète. La désactivation des modules [!DNL Inventory Management] peut entraîner l’instabilité du système et divers problèmes.

Vous pouvez désactiver [!DNL Inventory Management] modules pour :

* Accélérez le processus de mise à niveau pour les commerçants effectuant la migration de 2.0.x, 2.1.x, 2.2.x ou 2.3.x vers 2.4.x.
* Utilisez des modules système d’inventaire et de gestion des commandes personnalisés ou tiers.

Pour plus d’informations sur la désactivation des modules applicables[&#128279;](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html) reportez-vous à la page Activer ou désactiver des modules du _Guide d’installation_.

Une fois l’opération terminée, le système fournit une liste de modules et de valeurs dans `<Magento_installation_directory>/app/etc/config.php`, en commençant par :

```php
   'Magento_Inventory' => 0,
   'Magento_InventoryAdminUi' => 0,
   'Magento_InventoryAdvancedCheckout' => 0,
   ...
```

>[!IMPORTANT]
>
>Si les modules de connecteur OMS sont installés, veillez à ne pas désactiver le module `Magento_InventoryMessageBus`, qui est un module de connecteur. Il est nécessaire d’utiliser le connecteur avec OMS.

## Supprimer Inventory management

>[!IMPORTANT]
>
>L’utilisation des modules [!DNL Inventory Management] par défaut est vivement recommandée. L’autre module [!DNL CatalogInventory], qui est utilisé pour les systèmes disposant de modules [!DNL Inventory Management] supprimés, est désormais obsolète. La suppression des modules [!DNL Inventory Management] peut entraîner l’instabilité du système et divers problèmes.

Si vous choisissez de ne pas utiliser la fonctionnalité [!DNL Inventory Management], vous pouvez supprimer (désinstaller) ces modules. Pour supprimer tous les modules via le fichier du compositeur, ajoutez les éléments suivants à `composer.json` :

```
"replace": {
        "magento/module-inventory": "*",
        "magento/module-inventory-admin-ui": "*",
        "magento/module-inventory-advanced-checkout": "*",
        "magento/module-inventory-api": "*",
        "magento/module-inventory-bundle-product": "*",
        "magento/module-inventory-bundle-product-admin-ui": "*",
        "magento/module-inventory-cache": "*",
        "magento/module-inventory-catalog": "*",
        "magento/module-inventory-catalog-admin-ui": "*",
        "magento/module-inventory-catalog-api": "*",
        "magento/module-inventory-catalog-search": "*",
        "magento/module-inventory-configurable-product": "*",
        "magento/module-inventory-configurable-product-admin-ui": "*",
        "magento/module-inventory-configurable-product-indexer": "*",
        "magento/module-inventory-configuration": "*",
        "magento/module-inventory-configuration-api": "*",
        "magento/module-inventory-distance-based-source-selection": "*",
        "magento/module-inventory-distance-based-source-selection-admin-ui": "*",
        "magento/module-inventory-distance-based-source-selection-api": "*",
        "magento/module-inventory-export-stock": "*",
        "magento/module-inventory-export-stock-api": "*",
        "magento/module-inventory-elasticsearch": "*",
        "magento/module-inventory-graph-ql": "*",
        "magento/module-inventory-grouped-product": "*",
        "magento/module-inventory-grouped-product-admin-ui": "*",
        "magento/module-inventory-grouped-product-indexer": "*",
        "magento/module-inventory-import-export": "*",
        "magento/module-inventory-indexer": "*",
        "magento/module-inventory-low-quantity-notification": "*",
        "magento/module-inventory-low-quantity-notification-admin-ui": "*",
        "magento/module-inventory-low-quantity-notification-api": "*",
        "magento/module-inventory-multi-dimensional-indexer-api": "*",
        "magento/module-inventory-product-alert": "*",
        "magento/module-inventory-requisition-list": "*",
        "magento/module-inventory-reservations": "*",
        "magento/module-inventory-reservations-api": "*",
        "magento/module-inventory-reservation-cli": "*",
        "magento/module-inventory-sales": "*",
        "magento/module-inventory-sales-admin-ui": "*",
        "magento/module-inventory-sales-api": "*",
        "magento/module-inventory-sales-frontend-ui": "*",
        "magento/module-inventory-setup-fixture-generator": "*",
        "magento/module-inventory-shipping": "*",
        "magento/module-inventory-shipping-admin-ui": "*",
        "magento/module-inventory-source-deduction-api": "*",
        "magento/module-inventory-source-selection": "*",
        "magento/module-inventory-source-selection-api": "*",
        "magento/module-inventory-visual-merchandiser": "*",
        "magento/module-inventory-swatches-frontend-ui": "*",
        "magento/module-inventory-quote-graph-ql": "*",
        "magento/module-inventory-in-store-pickup": "*",
        "magento/module-inventory-in-store-pickup-sales": "*",
        "magento/module-inventory-in-store-pickup-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-sales-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-api": "*",
        "magento/module-inventory-in-store-pickup-sales-api": "*",
        "magento/module-inventory-in-store-pickup-frontend": "*",
        "magento/module-inventory-in-store-pickup-shipping": "*",
        "magento/module-inventory-in-store-pickup-graph-ql": "*",
        "magento/module-inventory-in-store-pickup-shipping-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-multishipping": "*",
        "magento/module-inventory-in-store-pickup-shipping-api": "*",
        "magento/module-inventory-in-store-pickup-quote": "*",
        "magento/module-inventory-in-store-pickup-webapi-extension": "*",
        "magento/module-inventory-in-store-pickup-quote-graph-ql": "*",
        "magento/module-inventory-configurable-product-frontend-ui": "*",
        "magento/module-inventory-catalog-search-configurable-product": "*",
        "magento/module-inventory-catalog-search-bundle-product": "*",
        "magento/module-inventory-catalog-frontend-ui": "*",
        "magento/module-inventory-bundle-import-export": "*",
        "magento/module-inventory-bundle-product-indexer": "*"
    }
```

Une fois cette modification terminée, exécutez le programme d’installation du compositeur et supprimez automatiquement ces modules Inventory management.

## Mettre à niveau Inventory management

### Versions [!DNL Commerce] précédentes

Lors de la mise à niveau ou de la mise à jour d’une installation 2.1.x, 2.2.x ou 2.3.x existante vers Adobe Commerce ou Magento Open Source 2.4.x, les modules [!DNL Inventory Management] sont désactivés par défaut. Ce paramètre par défaut est une précaution permettant d’empêcher les mises à niveau non rétrocompatibles et de mieux prendre en charge Order Management (OMS).

>[!NOTE]
>
>Order Management ne prend pas en charge [!DNL Inventory Management]. Lors de la mise à niveau, les modules [!DNL Inventory Management] sont désactivés pour permettre à OMS et [!DNL Commerce] 2.3.x de fonctionner de manière transparente.


Pour activer les modules [!DNL Inventory Management] :

1. Modifiez le fichier `<Commerce_installation_directory>/app/etc/config.php`.
1. Modifiez tous les modules d&#39;inventaire de `0` à `1` pour activer.
1. Mettez à jour la base de données :

   ```bash
   bin/magento setup:upgrade
   ```

1. Nettoyez le cache :

   ```bash
   bin/magento cache:clean
   ```

Il est recommandé d&#39;utiliser les commandes [réservation incohérences](cli.md) après la mise à niveau. Lors de la mise à niveau, tous vos produits sont ajoutés au Stock par défaut. Si vous avez des commandes en attente, les commandes mettent correctement à jour votre quantité vendable et vos réservations pour les ventes et l&#39;exécution des commandes.

### Versions [!DNL Inventory Management] précédentes

Lors de la mise à niveau des versions précédentes d’[!DNL Inventory Management] vers la dernière version, suivez les étapes normales de mise à niveau des extensions.

Pour la dernière version, mettez à jour votre version de métapaquet :

```json
        magento/inventory-composer-metapackage = 1.1.3
```

Consultez les guides suivants pour plus d’informations sur les mises à niveau de Commerce :

* Guide de mise à jour de Commerce [&#128279;](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/overview.html){target="_blank"}
* [Activation ou désactivation de modules](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html){target="_blank"}
