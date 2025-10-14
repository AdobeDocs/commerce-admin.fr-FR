---
title: 'Installation de l’extension  [!DNL Adobe Commerce B2B] '
description: Découvrez comment installer le métapaquet  [!DNL Adobe Commerce B2B] .
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 25964363ca5c4ec849e231d4eccb5f60b682a499
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 0%

---


# Installation de l’extension [!DNL Adobe Commerce B2B]

L’extension Adobe Commerce B2B, `magento/extension-b2b`, est disponible pour toutes les versions prises en charge d’Adobe Commerce. Il est installé après l’installation d’Adobe Commerce.


## Conditions requises

- [Adobe Commerce](https://business.adobe.com/products/magento/magento-commerce.html), toutes les versions prises en charge
- PHP 8.1, 8.2 et 8.3 (nécessite B2B 1.5.0)
- [!DNL Composer]

>[!IMPORTANT]
>
>Adobe Commerce B2B version 1.4.2+ n&#39;est pas compatible avec PHP 8.3. Si vous mettez à niveau l’instance Commerce vers Commerce version 2.4.7+, assurez-vous que la version PHP installée sur l’instance est PHP 8.2 pour conserver la compatibilité avec B2B 1.4.2+.

## Plateformes prises en charge

- Adobe Commerce sur les infrastructures cloud (ECE)
- Adobe Commerce On-Premise (EE)

## Etapes d&#39;installation

>[!BEGINSHADEBOX]

**Conditions préalables**

- Accédez à [repo.magento.com](https://repo.magento.com/) pour télécharger l’extension. Pour la génération des clés et l’obtention des droits nécessaires, voir [&#x200B; Obtenir vos clés d’authentification &#x200B;](https://experienceleague.adobe.com/fr/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

  Enregistrez les clés d’authentification pour l’installation en les définissant globalement dans votre répertoire [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home). Vous pouvez également les enregistrer dans un fichier [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) dans le répertoire racine de l’application Adobe Commerce.

- [Version prise en charge de l’extension B2B](https://experienceleague.adobe.com/fr/docs/commerce-operations/release/product-availability)-Déterminez la version la plus récente de l’extension B2B prise en charge sur la version Adobe Commerce déployée.

- Consultez les notes de mise à jour pour obtenir les informations les plus récentes sur la compatibilité des versions, les mises à jour ou les modifications pouvant affecter les exigences d’installation ou de mise à niveau.

   - [Notes De Mise À Jour B2B](release-notes.md)
   - [Notes De Mise À Jour D’Adobe Commerce](https://experienceleague.adobe.com/fr/docs/commerce-operations/release/versions)

>[!ENDSHADEBOX]

Installez l’extension B2B (`magento/b2b-extension`) à l’aide du compositeur. L’extension est un métapaquet de compositeur qui inclut la collection de modules qui activent les fonctionnalités B2B pour une instance Adobe Commerce. Pour obtenir la liste des modules inclus, voir [Packages B2B](packages.md).

>[!BEGINTABS]

>[!TAB Infrastructure cloud]

>[!TIP]
>
>Lors de l’installation d’Adobe Commerce B2B sur une infrastructure cloud, Adobe vous recommande de déployer votre application Adobe Commerce dans un environnement d’intégration ou d’évaluation avant de commencer.

Adobe recommande de travailler dans une branche de développement lors de l’ajout de l’extension B2B à votre projet. Si vous ne disposez pas d’une branche, voir [Créer une branche pour le développement](https://experienceleague.adobe.com/fr/docs/commerce-cloud-service/user-guide/develop/cli-branches). Lors de l’installation de l’extension B2B, le nom de l’extension `Magento_B2b` est automatiquement inséré dans le fichier `app/etc/config.php`. Il n’est pas nécessaire de modifier directement le fichier.

**Pour installer l’extension B2B** :

1. Sur votre station de travail locale, accédez au répertoire du projet.

1. Créez ou extrayez une branche de développement.

1. Ajoutez l’extension B2B à la section `require` du fichier `composer.json`.

   ```bash
   composer require magento/extension-b2b --no-update
   ```

1. Mettez à jour les dépendances du projet.

   ```bash
   composer update
   ```

1. Ajout, validation et modifications de code push.

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
   >L’envoi de mises à jour à l’environnement cloud lance le processus de déploiement cloud de Commerce pour appliquer les modifications. Vérifiez le statut du déploiement dans le [journal de déploiement](https://experienceleague.adobe.com/fr/docs/commerce-cloud-service/user-guide/develop/deploy/process). Si vous rencontrez des erreurs de déploiement, reportez-vous à la section [Récupération après une défaillance de composant](https://experienceleague.adobe.com/fr/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment).

1. Une fois la création et le déploiement terminés, utilisez SSH pour vous connecter à l’environnement distant et vérifier que l’extension B2B est installée et activée.

   ```bash
   bin/magento module:status Magento_B2b
   ```

   Un nom d’extension utilise le format suivant : `<VendorName>_<ComponentName>`.

   Exemple de réponse :

   ```
   Magento_B2b : Module is enabled
   ```

>[!TAB Sur site]

1. Dans le répertoire racine de l’application Adobe Commerce, mettez à jour le `composer.json` pour ajouter les dépendances de l’extension B2B :

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   Si une erreur se produit, par exemple :

   ```
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Vérifiez l’orthographe du package, votre contrainte de version, et assurez-vous que le package est disponible et correspond à vos exigences de stabilité minimale (stable).

1. Si vous y êtes invité, saisissez vos [&#x200B; clés d’authentification &#x200B;](https://experienceleague.adobe.com/fr/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

   Votre _clé publique_ est votre nom d’utilisateur ; votre _clé privée_ est votre mot de passe. Si vous avez stocké vos clés publiques et privées dans `auth.json`, vous n’êtes pas invité à vous authentifier.

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
   >En mode Production , il se peut que vous receviez un message à `Please rerun Magento compile command`. Saisissez les commandes pour terminer l’installation. Adobe Commerce ne vous invite pas à exécuter la commande compiler en mode Développeur.

>[!ENDTABS]

Une fois l’installation terminée, configurez et démarrez les consommateurs de messages.

## Consommateurs de messages

L’extension Adobe Commerce B2B utilise MySQL pour la gestion des files d’attente de messages. Le tableau suivant répertorie les consommateurs de messages qui prennent en charge les fonctionnalités B2B. Après avoir installé l’extension, démarrez les consommateurs de messages pour les fonctionnalités B2B requises pour votre storefront Commerce.

| Consommateur | Description |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | Met à jour le prix de chaque produit dans un catalogue partagé. Obligatoire lorsque l’option [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) est activée dans les paramètres de configuration du système d’administration. |
| `sharedCatalogUpdateCategoryPermissions` | Met à jour les catégories affectées à une catégorie de catalogue partagé. Obligatoire lorsque l’option [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) est activée dans les paramètres de configuration du système d’administration. |
| `negotiableQuotePriceUpdate` | Met à jour les prix des devis négociables. Obligatoire lorsque l’option [**[!UICONTROL Quotes]**](quotes.md) est activée dans les paramètres de configuration du système d’administration. |
| `purchaseorder.toorder` | Convertit une commande fournisseur en commande. Obligatoire lorsque l’option [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) est activée dans les paramètres de configuration du système d’administration. |
| `purchaseorder.transactional.email` | Envoyez des e-mails de bon de commande. Obligatoire lorsque l’option [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) est activée dans les paramètres de configuration du système d’administration. |
| `purchaseorder.validation` | Valide la commande fournisseur par rapport aux [règles d&#39;approbation](account-dashboard-approval-rules.md) pertinentes. Obligatoire lorsque l’option [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) est activée dans les paramètres de configuration du système d’administration. |
| `quoteItemCleaner` | Supprime les devis non valides ou inactifs lorsqu&#39;un produit est supprimé du catalogue ou du panier. Obligatoire lorsque l’option [**[!UICONTROL Quotes]**](quotes.md) est activée dans les paramètres de configuration du système d’administration. |
| `inventoryQtyCounter` | Corrige l’index de stock de manière asynchrone après la passation d’une commande ou la suppression d’un produit. Obligatoire lorsque l’option [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) est activée pour Inventory management dans les paramètres de configuration d’administration. Voir [&#x200B; Bonnes pratiques en matière de performances &#x200B;](https://experienceleague.adobe.com/fr/docs/commerce-operations/performance-best-practices/configuration#deferred-stock-update). |
| `async.operations.all` | Crée des messages pour chaque tâche individuelle d&#39;une [opération en bloc](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/) telle que l&#39;importation ou l&#39;exportation d&#39;articles, la modification des prix à grande échelle et l&#39;affectation de produits à un entrepôt. Obligatoire lorsque l’option [**Opérations en bloc d’administration**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) pour [!DNL Inventory Management] est définie sur **Exécuter de manière asynchrone** dans les paramètres de configuration du système d’administration. |

{style="table-layout:auto"}

>[!NOTE]
>
>Pour obtenir la liste de tous les consommateurs de messages d’Adobe Commerce, voir [Consommateurs de files d’attente de messages](https://experienceleague.adobe.com/fr/docs/commerce-operations/configuration-guide/message-queues/consumers) dans le _Guide de configuration_.

### Configuration des consommateurs de messages

Empêchez d’éventuels problèmes ou retards de traitement en ajoutant les paramètres suivants lorsque vous [démarrez les consommateurs de messages](#start-message-consumers) pour les fonctionnalités B2B.

- `--max-messages <value>` : indique le nombre maximal de messages que chaque client doit traiter avant de s&#39;arrêter (par défaut = 10000). Bien qu’Adobe ne le recommande pas, vous pouvez utiliser la valeur 0 pour empêcher le client de s’arrêter. La bonne pratique pour une application PHP est de redémarrer les processus de longue durée pour éviter les fuites de mémoire.

- `--batch-size <value>` : permet de limiter les ressources système consommées par les consommateurs (CPU, mémoire). L’utilisation de lots plus petits réduit l’utilisation des ressources et, par conséquent, ralentit le traitement.  Si spécifié, les messages d&#39;une file d&#39;attente sont consommés par lots de `<value>` chacun. Cette option s’applique uniquement au client par lots. Si `--batch-size` n’est pas défini, le client par lots reçoit tous les messages disponibles dans une file d’attente.

Pour plus d’informations sur les options de configuration supplémentaires, voir [Configuration spécifique](https://experienceleague.adobe.com//en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues?lang=fr#specific-configuration).

### Démarrer les consommateurs de messages

Pour activer les opérations asynchrones pour les fonctionnalités B2B, vous devez démarrer plusieurs consommateurs de messages.

1. Répertoriez les consommateurs de messages disponibles :

   ```bash
   bin/magento queue:consumers:list
   ```

   La commande renvoie les consommateurs de messages disponibles, y compris tous les consommateurs [B2B](#message-consumers).

1. Démarrez chaque client séparément :

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

Pour plus d’informations, voir [Gérer les files d’attente de messages](https://experienceleague.adobe.com/fr/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues) dans le _Guide de configuration_.

### Ajouter des consommateurs de messages à cron

Vous pouvez automatiser le planning d’exécution des consommateurs de messages `SharedCatalogUpdateCategoryPermissions` et `SharedCatalogUpdatePrice` en ajoutant le planning au fichier de configuration cron [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/fr/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#process-management).

```
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

Vous pouvez également configurer des plannings pour les consommateurs de messages à partir des [paramètres de configuration de la boutique](../systems/cron.md) dans Admin.

## Activer les fonctionnalités B2B dans l’administration

Après avoir installé l’extension B2B d’Adobe Commerce et démarré les consommateurs de messages, vous devez également [activer les fonctionnalités B2B dans l’administration](enable-basic-features.md).

