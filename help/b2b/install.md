---
title: Installez le [!DNL Adobe Commerce B2B] extension
description: Découvrez comment installer le [!DNL Adobe Commerce B2B] métapackage.
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---


# Installez le [!DNL Adobe Commerce B2B] extension

L’extension Adobe Commerce B2B est disponible uniquement pour Adobe Commerce v2.2.0 ou version ultérieure. Il est installé après l’installation d’Adobe Commerce.

Installez la version la plus récente de l’extension B2B prise en charge sur la version déployée d’Adobe Commerce.

>[!NOTE]
>
>Ces instructions d’installation s’appliquent à Adobe Commerce déployé sur site. Pour installer l’extension B2B pour les projets Commerce déployés sur l’infrastructure cloud, voir la section [Guide de l’infrastructure Commerce Cloud](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/b2b-module.html).

## Conditions

- Adobe Commerce version 2.3.x ou ultérieure
- [Version prise en charge de l’extension B2B](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html#compatibility)
- Valide [clés d’authentification](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) pour télécharger les extensions Adobe Commerce.

  Enregistrez les clés d’authentification à installer en les définissant globalement dans votre [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) répertoire . Vous pouvez également les enregistrer dans un [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) dans le répertoire racine de l’application Adobe Commerce.

Avant d’installer ou de mettre à niveau l’extension B2B, consultez les notes de mise à jour pour obtenir les informations les plus récentes sur la compatibilité des versions, les mises à jour ou les modifications susceptibles d’affecter les exigences d’installation ou de mise à niveau.

- [Notes de mise à jour B2B](release-notes.md)
- [Notes de mise à jour d’Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html?lang=en)

## Etapes d&#39;installation

1. Dans le répertoire racine de l’application Adobe Commerce, mettez à jour la variable `composer.json` pour ajouter les dépendances de l’extension B2B :

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   Si une erreur se produit, par exemple :

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Vérifiez l’orthographe du module, votre contrainte de version et que le module est disponible et correspond à votre exigence de stabilité minimale (stable).

1. Si vous y êtes invité, saisissez [clés d’authentification](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

   Votre _clé publique_ est votre nom d’utilisateur ; votre _clé privée_ est votre mot de passe. Si vous avez stocké vos clés publique et privée dans `auth.json`, vous n’êtes pas invité à vous authentifier.

1. Exécutez les commandes suivantes une fois que le compositeur a terminé la mise à jour des modules :

   ```bash
   bin/magento setup:upgrade
   ```

   ```bash
   bin/magento setup:di:compile
   ```

   ```bash
   bin/magento setup:static-content:deploy -f
   ```

   ```bash
   bin/magento cache:clean
   ```

   >[!NOTE]
   >
   >En mode de production, vous pouvez recevoir un message à l’adresse `Please rerun Magento compile command`. Renseignez les commandes pour terminer l&#39;installation. Adobe Commerce ne vous invite pas à exécuter la commande compile en mode Développeur.

Une fois l’installation terminée, configurez et démarrez les utilisateurs de messages, y compris [spécification des paramètres pour les consommateurs de messages](#configure-message-consumers).

## Consommateurs de messages

L’extension Adobe Commerce B2B utilise MySQL pour la gestion de la file d’attente des messages. Le tableau suivant répertorie les consommateurs de messages qui prennent en charge les fonctionnalités B2B. Après avoir installé l’extension, démarrez le message des consommateurs pour les fonctionnalités B2B requises pour votre vitrine Commerce.

| Consommation | Description |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | Met à jour le prix de chaque produit dans un catalogue partagé. Obligatoire lorsque la variable [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) est activée dans les paramètres de configuration du système d’administration. |
| `sharedCatalogUpdateCategoryPermissions` | Met à jour les catégories affectées à une catégorie de catalogue partagée. Obligatoire lorsque la variable [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) est activée dans les paramètres de configuration du système d’administration. |
| `negotiableQuotePriceUpdate` | Met à jour les prix des devis négociables. Obligatoire lorsque la variable [**[!UICONTROL Quotes]**](quotes.md) est activée dans les paramètres de configuration du système d’administration. |
| `purchaseorder.toorder` | Convertit la commande d’achat en commande. Obligatoire lorsque la variable [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) est activée dans les paramètres de configuration du système d’administration. |
| `purchaseorder.transactional.email` | Envoyez des e-mails de commande. Obligatoire lorsque la variable [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) est activée dans les paramètres de configuration du système d’administration. |
| `purchaseorder.validation` | Valide le bon de commande par rapport à ce qui est pertinent [règles de validation](account-dashboard-approval-rules.md). Obligatoire lorsque la variable [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) est activée dans les paramètres de configuration du système d’administration. |
| `quoteItemCleaner` | Supprime les prix invalides ou inactifs lorsqu’un produit est supprimé du catalogue ou du panier. Obligatoire lorsque la variable [**[!UICONTROL Quotes]**](quotes.md) est activée dans les paramètres de configuration du système d’administration. |
| `inventoryQtyCounter` | Corrige de manière asynchrone l’index de stock après le passage d’une commande ou la suppression d’un produit. Obligatoire lorsque la variable [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) est activée pour Inventory management dans les paramètres de configuration de l’administrateur. Voir [Bonnes pratiques en matière de performances](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/configuration.html#deferred-stock-update). |
| `async.operations.all` | Crée des messages pour chaque tâche d’une [opération en bloc](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/), comme l’importation ou l’exportation d’articles, la modification des prix à grande échelle et l’affectation de produits à un entrepôt. Obligatoire lorsque la variable [**Opérations en bloc d’administration**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) option pour [!DNL Inventory Management] est défini sur **Exécution asynchrone** dans les paramètres de configuration du système d’administration. |

{style="table-layout:auto"}

>[!NOTE]
>
>Pour obtenir la liste de tous les consommateurs de messages Adobe Commerce, voir [Consommateurs de files d&#39;attente de messages](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/consumers.html) dans le _Guide de configuration_.

### Configuration des consommateurs de messages

Empêchez les problèmes ou les retards de traitement en ajoutant les paramètres suivants lorsque vous [Démarrez le message aux consommateurs](#start-message-consumers) pour les fonctionnalités B2B.

- `--max-messages <value>`— Indique le nombre maximal de messages que chaque consommateur doit traiter avant de s’arrêter (valeur par défaut = 10 000). Bien que nous ne le recommandions pas, vous pouvez utiliser 0 pour empêcher le consommateur de s’arrêter. La bonne pratique pour une application PHP est de redémarrer des processus de longue durée afin d’éviter toute fuite de mémoire.

- `--batch-size <value>`— Permet de limiter les ressources système consommées par les consommateurs (processeur, mémoire). L’utilisation de lots plus petits réduit l’utilisation des ressources et ralentit donc le traitement.  Si spécifié, les messages d’une file d’attente sont consommés par lots de `<value>` chacun. Cette option s’applique uniquement au consommateur par lots. If `--batch-size` n’est pas définie, le consommateur par lot reçoit tous les messages disponibles dans une file d’attente.

Pour plus d’informations sur les options de configuration supplémentaires, voir [Configuration spécifique](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#specific-configuration).

### Démarrez le message aux consommateurs

Pour activer des opérations asynchrones pour les fonctionnalités B2B, vous devez démarrer plusieurs consommateurs de messages.

1. Répertorier les consommateurs de messages disponibles :

   ```bash
   bin/magento queue:consumers:list
   ```

   La commande renvoie les consommateurs de messages disponibles, y compris tous les [Consommateurs de messages B2B](#message-consumers).

1. Démarrez chaque consommateur séparément :

   ```bash
   bin/magento queue:consumers:start [--max-messages=<value>] [--batch-size=<value>] <consumer_name>
   ```

   Par exemple :

   ```bash
   bin/magento queue:consumers:start quoteItemCleaner
   ```

>[!TIP]
>
>Pour l’exécuter en arrière-plan, ajoutez `&` à la commande , revenez à une invite et continuez à exécuter les commandes. Par exemple : `bin/magento queue:consumers:start sharedCatalogUpdatePrice &`.

Pour plus d’informations, voir [Gestion des files d’attente de messages](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) dans le _Guide de configuration_.

### Ajout des consommateurs de messages à cron

Vous avez la possibilité d’automatiser le planning d’exécution de la variable `SharedCatalogUpdateCategoryPermissions` et `SharedCatalogUpdatePrice` message aux consommateurs en ajoutant le planning au fichier de configuration cron [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#process-management).

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

Vous pouvez également configurer des planifications pour les consommateurs de messages à partir de la [Paramètres de configuration du magasin](../systems/cron.md) dans Admin.

## Activation des fonctionnalités B2B dans l’administration

Après avoir installé l’extension Adobe Commerce B2B et démarré les consommateurs de messages, vous devez également [Activation des fonctionnalités B2B dans l’administration](enable-basic-features.md).
