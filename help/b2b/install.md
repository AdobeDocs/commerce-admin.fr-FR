---
title: Installation de l’extension  [!DNL Adobe Commerce B2B]
description: Découvrez comment installer le métapackage  [!DNL Adobe Commerce B2B] .
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: be36742aa1214e7e8e7f343051336cd3635099f4
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---


# Installation de l’extension [!DNL Adobe Commerce B2B]

L’extension Adobe Commerce B2B, `magento/extension-b2b` est disponible pour toutes les versions prises en charge d’Adobe Commerce. Il est installé après l’installation d’Adobe Commerce.


## Conditions

- [Adobe Commerce](https://business.adobe.com/products/magento/magento-commerce.html), toutes les versions prises en charge
- PHP 8.1 / 8.2 / 8.3
- [!DNL Composer]

## Plateformes prises en charge

- Adobe Commerce sur l’infrastructure cloud (ECE)
- Adobe Commerce sur site (EE)

## Etapes d&#39;installation

>[!BEGINSHADEBOX]

**Conditions préalables**

- Accédez à [repo.magento.com](https://repo.magento.com/) pour télécharger l’extension. Pour la génération des clés et l’obtention des droits nécessaires, voir [Obtention de vos clés d’authentification](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

  Enregistrez les clés d’authentification pour l’installation en les définissant globalement dans votre répertoire [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home). Ou enregistrez-les dans un fichier [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) dans le répertoire racine de l’application Adobe Commerce.

- [Version prise en charge de l’extension B2B](https://experienceleague.adobe.com/en/docs/commerce-operations/release/product-availability) - Déterminez la version la plus récente de l’extension B2B prise en charge sur la version déployée d’Adobe Commerce.

- Consultez les notes de mise à jour pour obtenir les informations les plus récentes sur la compatibilité des versions, les mises à jour ou les modifications susceptibles d’affecter les exigences d’installation ou de mise à niveau.

   - [Notes de mise à jour B2B](release-notes.md)
   - [Notes de mise à jour d’Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-operations/release/versions)

>[!ENDSHADEBOX]

Installez l’extension B2B (`magento/b2b-extension`) à l’aide du compositeur. L’extension est un métapaquage de compositeur qui inclut la collection de modules qui activent les fonctionnalités B2B pour une instance Adobe Commerce. Pour obtenir la liste des modules inclus, voir [Packages B2B](packages.md).

>[!BEGINTABS]

>[!TAB Infrastructure cloud]

>[!TIP]
>
>Lors de l’installation d’Adobe Commerce B2B sur l’infrastructure cloud, Adobe vous recommande de déployer votre application Adobe Commerce dans un environnement d’intégration ou d’évaluation avant de commencer.

Adobe recommande de travailler dans une branche de développement lors de l’ajout de l’extension B2B à votre projet. Si vous ne disposez pas d’une branche, voir [Création d’une branche pour le développement](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches). Lors de l’installation de l’extension B2B, le nom de l’extension `Magento_B2b` est automatiquement inséré dans le fichier `app/etc/config.php`. Il n’est pas nécessaire de modifier directement le fichier.

**Pour installer l’extension B2B** :

1. Sur votre poste de travail local, modifiez le répertoire de votre projet.

1. Créez ou extrayez une branche de développement.

1. Ajoutez l’extension B2B à la section `require` du fichier `composer.json`.

   ```bash
   composer require magento/extension-b2b --no-update
   ```

1. Mettez à jour les dépendances du projet.

   ```bash
   composer update
   ```

1. Ajout, validation et modification du code push.

   ```bash
   git add -A
   ```

   ```bash
   git commit -m "Install the B2B extension."
   ```

   ```bash
   git push origin <branch-name>
   ```

   >[!NOTE]
   >
   >La publication de mises à jour dans l’environnement cloud lance le processus de déploiement cloud de Commerce pour appliquer les modifications. Vérifiez l’état du déploiement à partir du [log de déploiement](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process). Si vous rencontrez des erreurs de déploiement, reportez-vous à la section [Récupération de l’échec du composant](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment).

1. Une fois la création et le déploiement terminés, utilisez SSH pour vous connecter à l’environnement distant et vérifier que l’extension B2B est installée et activée.

   ```bash
   bin/magento module:status Magento_B2b
   ```

   Un nom d’extension utilise le format : `<VendorName>_<ComponentName>`.

   Exemple de réponse :

   ```terminal
   Magento_B2b : Module is enabled
   ```

>[!TAB Sur site]

1. Dans le répertoire racine de l’application Adobe Commerce, mettez à jour `composer.json` pour ajouter les dépendances de l’extension B2B :

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   Si une erreur se produit, par exemple :

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Vérifiez l’orthographe du module, votre contrainte de version et que le module est disponible et correspond à votre exigence de stabilité minimale (stable).

1. Si vous y êtes invité, saisissez vos [clés d&#39;authentification](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

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
   >En mode de production, vous pouvez recevoir un message à `Please rerun Magento compile command`. Renseignez les commandes pour terminer l&#39;installation. Adobe Commerce ne vous invite pas à exécuter la commande compile en mode Développeur.

>[!ENDTABS]

Une fois l’installation terminée, configurez et démarrez les consommateurs de messages.

## Consommateurs de messages

L’extension Adobe Commerce B2B utilise MySQL pour la gestion de la file d’attente des messages. Le tableau suivant répertorie les consommateurs de messages qui prennent en charge les fonctionnalités B2B. Après avoir installé l’extension, démarrez le message des consommateurs pour les fonctionnalités B2B requises pour votre vitrine Commerce.

| Consommation | Description |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | Met à jour le prix de chaque produit dans un catalogue partagé. Obligatoire lorsque l’option [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) est activée dans les paramètres de configuration du système d’administration. |
| `sharedCatalogUpdateCategoryPermissions` | Met à jour les catégories affectées à une catégorie de catalogue partagée. Obligatoire lorsque l’option [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) est activée dans les paramètres de configuration du système d’administration. |
| `negotiableQuotePriceUpdate` | Met à jour les prix des devis négociables. Obligatoire lorsque l’option [**[!UICONTROL Quotes]**](quotes.md) est activée dans les paramètres de configuration du système d’administration. |
| `purchaseorder.toorder` | Convertit la commande d’achat en commande. Obligatoire lorsque l’option [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) est activée dans les paramètres de configuration du système d’administration. |
| `purchaseorder.transactional.email` | Envoyez des e-mails de commande. Obligatoire lorsque l’option [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) est activée dans les paramètres de configuration du système d’administration. |
| `purchaseorder.validation` | Valide la commande d’achat par rapport aux [règles d’approbation](account-dashboard-approval-rules.md) appropriées. Obligatoire lorsque l’option [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) est activée dans les paramètres de configuration du système d’administration. |
| `quoteItemCleaner` | Supprime les prix invalides ou inactifs lorsqu’un produit est supprimé du catalogue ou du panier. Obligatoire lorsque l’option [**[!UICONTROL Quotes]**](quotes.md) est activée dans les paramètres de configuration du système d’administration. |
| `inventoryQtyCounter` | Corrige de manière asynchrone l’index de stock après le passage d’une commande ou la suppression d’un produit. Obligatoire lorsque l’option [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) est activée pour Inventory management dans les paramètres de configuration de l’administrateur. Voir [Bonnes pratiques de performances](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/configuration#deferred-stock-update). |
| `async.operations.all` | Crée des messages pour chaque tâche individuelle d’une [opération en masse](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/), comme importer ou exporter des articles, modifier les prix à grande échelle et affecter des produits à un entrepôt. Obligatoire lorsque l’option [**Admin - Opérations en bloc**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) pour [!DNL Inventory Management] est définie sur **Exécuter de manière asynchrone** dans les paramètres de configuration du système d’administration. |

{style="table-layout:auto"}

>[!NOTE]
>
>Pour obtenir la liste de tous les consommateurs de messages Adobe Commerce, reportez-vous à la section [Consommateurs de file d’attente de messages](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/consumers) du _Guide de configuration_.

### Configuration des consommateurs de messages

Empêchez d’éventuels problèmes ou retards de traitement en ajoutant les paramètres suivants lorsque vous [démarrez les consommateurs de messages](#start-message-consumers) pour les fonctionnalités B2B.

- `--max-messages <value>` : spécifie le nombre maximal de messages que chaque consommateur doit traiter avant de s’arrêter (par défaut = 10 000). Bien qu’Adobe ne le recommande pas, vous pouvez utiliser 0 pour empêcher le consommateur de s’arrêter. La bonne pratique pour une application PHP est de redémarrer des processus de longue durée afin d’éviter toute fuite de mémoire.

- `--batch-size <value>` — Permet de limiter les ressources système consommées par les consommateurs (processeur, mémoire). L’utilisation de lots plus petits réduit l’utilisation des ressources et ralentit donc le traitement.  Si spécifié, les messages d’une file d’attente sont consommés par lots de `<value>` chacun. Cette option s’applique uniquement au consommateur par lots. Si `--batch-size` n’est pas défini, le consommateur de lots reçoit tous les messages disponibles dans une file d’attente.

Pour plus d’informations sur les options de configuration supplémentaires, voir [Specific-configuration](https://experienceleague.adobe.com//en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#specific-configuration).

### Démarrez le message aux consommateurs

Pour activer des opérations asynchrones pour les fonctionnalités B2B, vous devez démarrer plusieurs consommateurs de messages.

1. Répertorier les consommateurs de messages disponibles :

   ```bash
   bin/magento queue:consumers:list
   ```

   La commande renvoie les consommateurs de messages disponibles, y compris tous les [consommateurs de messages B2B](#message-consumers).

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
>Pour l’exécuter en arrière-plan, ajoutez `&` à la commande, revenez à une invite et continuez à exécuter les commandes. Par exemple : `bin/magento queue:consumers:start sharedCatalogUpdatePrice &`.

Pour plus d’informations, voir [Gestion des files d’attente de messages](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues) dans le _Guide de configuration_.

### Ajout des consommateurs de messages à cron

Vous pouvez automatiser la planification de l’exécution pour les consommateurs de messages `SharedCatalogUpdateCategoryPermissions` et `SharedCatalogUpdatePrice` en ajoutant la planification au fichier de configuration cron [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#process-management).

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

Vous pouvez également configurer des plannings pour les consommateurs de messages à partir des [paramètres de configuration de magasin](../systems/cron.md) dans l’administrateur.

## Activation des fonctionnalités B2B dans l’administration

Après avoir installé l’extension Adobe Commerce B2B et démarré les consommateurs de messages, vous devez également [activer les fonctionnalités B2B dans l’Admin](enable-basic-features.md).

