---
title: Notes de mise à jour de [!DNL Inventory Management]
description: Consultez les notes de mise à jour pour plus d’informations sur toutes  [!DNL Inventory Management]  versions.
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: fdc14758788fa5cd0391371ebfafb478dadec8a4
workflow-type: tm+mt
source-wordcount: '3462'
ht-degree: 0%

---

# Notes de mise à jour de [!DNL Inventory Management]

Ces notes de mise à jour décrivent les versions d’[!DNL Inventory Management] et incluent les éléments suivants :

![Nouveau](../assets/new.svg) Nouvelles fonctionnalités
![Correction d’un problème](../assets/fix.svg) Correctifs et améliorations
![Problème connu](../assets/bug.svg) Problèmes connus

[!DNL Inventory Management] est un projet spécial d’ingénierie de la communauté Magento Open Source ouvert aux contributeurs. Pour participer et contribuer, consultez le référentiel [Projet GitHub](https://github.com/magento/inventory) et le [wiki](https://github.com/magento/inventory/wiki) pour commencer. Pour discuter du projet, rejoignez le canal [Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) ([auto-inscription](https://opensource.magento.com/slack)).

[ Calendrier des versions ](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html?lang=fr){target="_blank"} pour les versions prises en charge et compatibles.

## v1.2.7

Les notes de mise à jour d’[!DNL Inventory Management] 1.2.7 sont incluses dans les notes de mise à jour d’[core 2.4.7](https://experienceleague.adobe.com/fr/docs/commerce-operations/release/notes/adobe-commerce/2-4-7#inventory-management-1).

## v1.2.6

[!DNL Inventory Management] 1.2.6 (version du module : `magento/inventory-metapackage = 1.2.6`) est pris en charge avec la version 2.4.6 et compatible avec la version 2.4.0 d’Adobe Commerce, Adobe Commerce sur les infrastructures cloud et la base de code Magento Open Source.

![Problème résolu](../assets/fix.svg) Le storefront affiche désormais les produits composites (configurables, groupés et groupés) en stock lorsque les produits enfants qui avaient été vendus sont renvoyés en stock. Auparavant, le storefront indiquait que le produit composite était en rupture de stock dans ces conditions. <!-- ACP2E-1106-->

![Problème résolu](../assets/fix.svg) Les options de produit configurables s&#39;affichent désormais comme prévu en rupture de stock sur le storefront si l&#39;option a été créée avec une quantité définie sur 0 et **[!UICONTROL Display out-of-stock products]** est activée. <!-- ACP2E-1148-->

![Problème résolu](../assets/fix.svg) Les caches de page de catégorie ne sont plus invalidés lorsque la quantité de stock change et que le produit est toujours en stock. Adobe Commerce charge désormais les pages à partir du cache au lieu de les générer de nouveau lorsque la quantité de produits (et rien d’autre) sur la page de catégorie du storefront change. <!-- ACP2E-118-->

![Problème résolu](../assets/fix.svg) Le nombre de produits de la liste de catégories est désormais correct lors de l&#39;utilisation d&#39;Inventory en mode mono-source avec le paramètre **[!UICONTROL Display Out-Of-Stock Products]** activé. Adobe Commerce vérifie désormais si un produit est commercialisable lors du comptage. <!-- ACP2E-1033-->

![Problème résolu](../assets/fix.svg) Les règles de prix du panier pour la livraison en magasin fonctionnent désormais comme prévu lorsque l’option Stock est activée. Auparavant, les remises générées par des règles de prix de panier n’étaient pas appliquées dans ces conditions. <!-- ACP2E-1015-->

![Problème résolu](../assets/fix.svg) La mise à jour de l’inventaire des produits en mode planifié n’efface plus tous les caches. Auparavant, l’indexeur d’inventaire effaçait tous les caches de configuration. <!-- ACP2E-1003-->

![Problème résolu](../assets/fix.svg) La valeur de l&#39;attribut **[!UICONTROL Allow Multiple Boxes for Shipping]** pour un produit dans Advanced Inventory est maintenant enregistrée comme prévu. <!-- ACP2E-992-->

![Problème résolu](../assets/fix.svg) Adobe Commerce émet désormais une compensation précise de réservation après un avoir de remboursement partiel pour une commande qui a été passée avec retrait en magasin. Auparavant, une réservation incorrecte était enregistrée dans la table `inventory_reservation` lorsqu&#39;un utilisateur administrateur créait un avoir sans cocher la case **[!UICONTROL Return to Stock]**. <!-- ACP2E-979-->

![Problème résolu](../assets/fix.svg) Adobe Commerce n’affiche plus les produits configurables comme étant en rupture de stock sur le storefront lorsque l’une de ses variantes a été manuellement renvoyée en stock dans des déploiements implémentant l’inventaire multi-source. <!-- ACP2E-952-->

![Problème résolu](../assets/fix.svg) La position de la colonne sur la grille de produits (**[!UICONTROL Catalog]** > **[!UICONTROL Products]**) ne revient plus à sa position précédente après le rechargement de la page dans les déploiements avec plusieurs sources d’inventaire configurées. <!-- ACP2E-925-->

![Problème résolu](../assets/fix.svg) La quantité de stock est désormais correcte après l&#39;émission d&#39;un avoir pour un produit virtuel lorsque la case à cocher **[!UICONTROL Back to stock]** n&#39;est pas sélectionnée. <!-- ACP2E-908-->

![Problème résolu](../assets/fix.svg) Vous pouvez désormais enregistrer des catégories avec un tri et une portée de produit automatiques affectés à des stocks autres que ceux par défaut. Auparavant, Adobe Commerce n’enregistrait pas la catégorie et affichait cette erreur : `Something went wrong while saving the category`. <!-- ACP2E-859-->

![Problème résolu](../assets/fix.svg) Le statut du stock de produits configurables est désormais mis à jour comme prévu lorsque le produit est créé avec toutes les variations configurables en rupture de stock. <!-- ACP2E-813-->

![Problème résolu](../assets/fix.svg) L’outil d’analyse des incohérences de réservation fonctionne désormais correctement avec les commandes partiellement expédiées qui contiennent des produits configurables, groupés et groupés. Les types de produits composites sont maintenant analysés. Auparavant, les annulations et les remboursements étaient enregistrés uniquement pour les produits parents, et non pour les articles de commande de sous-produits de produits configurables et de produits groupés à expédier ensemble. <!-- ACP2E-924-->

![Problème résolu](../assets/fix.svg) Adobe Commerce n’affiche plus d’erreur lorsqu’un utilisateur administrateur tente d’affecter 200 sources d’inventaire ou plus à un stock ou à un produit. <!-- ACP2E-1180-->

![Problème résolu](../assets/fix.svg) Adobe Commerce prend désormais en charge la création d&#39;un avoir pour une commande à partir de laquelle un produit a été supprimé. Auparavant, les commerçants ne pouvaient pas créer d&#39;avoir lorsque des produits avaient été supprimés de la commande après la création d&#39;une facture. L’application affichait cette erreur : `Following products with requested skus were not found: s00001`. t. <!-- ACP2E-1138-->

![Problème résolu](../assets/fix.svg) Les magasins sont désormais filtrés en fonction des ID de magasin uniques et multiples. Le code d’attribut de produit `event` a été ajouté à la liste des codes d’attribut réservés. Auparavant, le rapport de stock faible générait une exception lors de l&#39;installation du module Inventaire. <!-- ACP2E-1017-->

![Problème résolu](../assets/fix.svg) Les filtres de navigation superposés fonctionnent désormais comme prévu et les produits en rupture de stock sont désormais ajoutés à la liste des produits de la catégorie storefront. Le nouvel attribut de tri `is_out_of_stock` utilise le mappeur de champs dynamiques Elasticsearch pour la collection de produits storefront. <!-- ACP2E-748-->

![Problème résolu](../assets/fix.svg) Le statut du stock de produits composites (groupés, configurables et groupés) est mis à jour comme prévu lorsque le statut du stock de produits enfants est modifié par un appel de `POST /rest/V1/inventory/source-items` REST. <!-- ACP2E-1209-->

## v1.2.5

[!DNL Inventory Management] 1.2.5 (version du module : `magento/inventory-metapackage = 1.2.5`) est pris en charge avec la version 2.4.5 et compatible avec la version 2.4.0 d’Adobe Commerce, Adobe Commerce sur les infrastructures cloud et la base de code Magento Open Source.

![Problème résolu](../assets/fix.svg) Le statut de stock par défaut des produits groupés et groupés est désormais mis à jour comme prévu lorsqu&#39;un commerçant crée une expédition à partir de l&#39;administrateur. Auparavant, le statut de ces produits restait inchangé après la création d’une expédition. <!--- ACP2E-418-->

![Problème résolu](../assets/fix.svg) Les produits configurables sont désormais renvoyés en stock lorsque l’une des conditions suivantes est remplie : 1. Le produit parent a au moins un enfant enregistré en stock. 2. Le produit configurable lui-même a été mis à jour et défini comme **en stock** et avait au moins un enfant en stock. <!--- ACP2E-443-->

![Problème résolu](../assets/fix.svg) Les modifications d’inventaire implémentées via l’API REST sont désormais répercutées comme prévu sur les pages de détails du produit. Le cache des produits du catalogue est maintenant nettoyé après avoir comparé les derniers et actuels statuts de stock. Auparavant, l’omission de la fonction de rappel entraînait une évaluation incorrecte des modifications de statut du stock, ce qui ne déclenchait pas le nettoyage du cache nécessaire. Par conséquent, le storefront ne reflétait pas les modifications d&#39;inventaire. <!--- ACP2E-161-->

![Problème résolu](../assets/fix.svg) Les produits affectés au stock par défaut et précédemment en rupture de stock sont désormais visibles sur le storefront après la mise à jour de l’élément source à l’aide de `/V1/inventory/source-items`. Auparavant, ce point d’entrée de l’API REST définissait une `stock_status` incorrecte. <!--- ACP2E-562-->

![Problème résolu ](../assets/fix.svg) L’annulation de l’affectation des sources d’inventaire par le biais d’une action en masse (**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**) fonctionne désormais comme prévu lorsque les sources incluent des SKU qui sont des doublons, à l’exception d’un zéro au début (par exemple, `01234` et `1234`). Auparavant, l’application n’annulait pas l’affectation des sources d’inventaire et générait une erreur. <!--- ACP2E-2641-->

![Problème résolu](../assets/fix.svg) Le statut du stock du produit est désormais toujours **en stock** sur le storefront lorsque d&#39;innombrables commandes en souffrance sont activées et que le produit est affecté à un stock personnalisé, quelle que soit la quantité en souffrance. Auparavant, les produits étaient en rupture de stock même lorsque les commandes en souffrance étaient activées. <!--- ACP2E-664-->

![Problème résolu](../assets/fix.svg) Le stock de produits parent et enfant configurable est désormais correctement mis à jour après la mise à jour de l’élément source avec `POST /V1/inventory/source-items`. Une fois le produit enfant mis à jour via l’API, un nouveau plug-in Inventaire pour les contrôles de stock par défaut vérifie et met à jour la quantité et le statut configurables du produit. <!--- ACP2E-442-->

![Problème résolu](../assets/fix.svg) Les produits groupés en rupture de stock ne sont plus répertoriés sur la page Catégorie de storefront. <!--- ACP2E-2082-->

![Correction d’un problème](../assets/fix.svg) Correction du nom du package dans `CatalogInventory` `composer.json`. <!--- ACP2E-2914-->

![Problème résolu](../assets/fix.svg) Le statut de commande en souffrance est désormais correctement représenté dans l’administration après le passage d’une commande avec un produit en quantité nulle dans un déploiement multi-source/stock. [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![Problème résolu](../assets/fix.svg) Les produits groupés en rupture de stock ne s’affichent plus sur la page Catégorie de storefront lorsque le produit groupé est mis à jour à partir de la section Stocks. <!--- ACP2E-2012-->

![Correction d’un problème](../assets/fix.svg) Les problèmes de compatibilité avec PHP 7.4 sont résolus. <!--- AC-3192-->

![Correction d’un problème](../assets/fix.svg) Les performances des opérations d’enregistrement qui incluent des produits groupés contenant de nombreuses options (plusieurs centaines) sont améliorées. Auparavant, l’enregistrement de ces produits groupés volumineux prenait plusieurs minutes et entraînait parfois des délais d’expiration dans les déploiements avec les services d’inventaire activés. [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![Correction d’un problème](../assets/fix.svg) L’outil d’action en masse sur les produits (**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**) fonctionne désormais comme prévu lors de l’affectation d’une source de stock à plusieurs produits lorsque les SKU sont dupliqués, à l’exception d’un `0` de début (par exemple, `01234` et `1234`). Auparavant, un seul produit se voyait attribuer une source d&#39;inventaire. [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![Problème résolu](../assets/fix.svg) Le champ `ProductInterface.only_x_left_in_stock` renvoie désormais 0 si l’inventaire est égal à 0. Auparavant, elle renvoyait la valeur null. [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![Correction d’un problème](../assets/fix.svg) Vous pouvez désormais modifier le stock par défaut à partir de Admin **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**. Auparavant, une erreur JavaScript s’affichait dans la console lorsque vous tentiez d’ajouter ou de supprimer des sources du stock par défaut, bien que vous puissiez affecter des sites web au stock par défaut. <!--- ACP2E-545-->

![Problème résolu](../assets/fix.svg) <!--- ACP2E-274--> Le nombre de produits de la liste de catégories est désormais correct lors de l’utilisation du mode d’inventaire à source unique avec le paramètre **[!UICONTROL Display Out-Of-Stock Products]** activé. Un nouveau plug-in utilise désormais `AreProductsSalableInterface` et `StockConfigurationInterface` pour déterminer le nombre total de produits. Auparavant, la liste des produits de la catégorie renvoyait une quantité incorrecte de produits.

![Problème résolu](../assets/fix.svg) <!--- ACP2E-322--> les produits configurables sont désormais déplacés à la dernière position de la liste des produits après la mise à jour du stock lorsque le paramètre **[!UICONTROL Move out of stock to the bottom]** est activé. Une nouvelle requête de base de données personnalisée est implémentée pour annuler l’ordre de tri des index Elasticsearch, qui ignore l’ordre de tri activé par l’administrateur. Auparavant, les produits configurables et leurs produits enfants n’étaient pas déplacés en bas de la liste lorsque ce paramètre était activé.

## v1.2.4

Inventory management 1.2.4 (version du module : `magento/inventory-metapackage = 1.2.4`) est pris en charge avec la version 2.4.4 et compatible avec la version 2.4.0 d’Adobe Commerce, Adobe Commerce sur les infrastructures cloud et la base de code Magento Open Source.

![Problème résolu](../assets/fix.svg) Commerce affiche désormais une valeur de quantité vendable précise pour tous les produits dans la vue de liste de produits Admin. Auparavant, elle affichait une valeur vide pour la quantité vendable de produits en stock avec des SKU qui contenaient des caractères spéciaux. <!--- MC-41936-->

![Problème résolu](../assets/fix.svg) Les performances se sont améliorées pour les actions de panier et de passage en caisse telles que l’ajout de produits au panier dans les déploiements avec de nombreuses sources d’inventaire (environ 10 000). <!--- MC-42570-->

![Problème résolu](../assets/fix.svg) [!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."} La commande `bin/magento inventory:reservation:list-inconsistencies` gère désormais correctement les commandes avec des expéditions partielles, même si les réservations sont manquantes dans la base de données et que le cache a été effacé. Auparavant, lorsque cette commande était exécutée avec un cache pré-effacé, Commerce affichait l’erreur suivante : `Area code is not set`. <!--- MC-42142-->


![Problème résolu ](../assets/fix.svg) l’indexation incrémentielle des produits enfants groupés n’entraîne plus l’indexation incorrecte d’autres produits groupés lorsque les enfants sont partagés. <!--- MC-41963-->

![Problème résolu](../assets/fix.svg) La page de catégorie storefront affiche désormais le nombre correct de produits après la suppression d’un produit d’une catégorie par API. Auparavant, le nombre de produits de la page de catégorie était incorrect jusqu’à la réindexation. <!--- MC-42287-->

![Problème résolu](../assets/fix.svg) Les produits configurables peuvent désormais être retournés en stock lors de la création d&#39;un avoir lorsque l&#39;option **[!UICONTROL Manage Stock]** est désactivée. Auparavant, lorsque cette option était désactivée, Commerce n&#39;affichait pas la case à cocher **Retour au stock** sur la page de création des avoirs. <!--- MC-42002-->

![Problème résolu](../assets/fix.svg) La gestion des stocks de plus de 10 000 articles a été améliorée. Auparavant, les problèmes de performances empêchaient parfois les commerçants de modifier les stocks dans l’administrateur avant de lancer leur site web. <!--- MC-42643-->

![Correction d’un problème](../assets/fix.svg) La page **[!UICONTROL User Roles]** dans l’interface Administration est mise à jour afin de fournir aux administrateurs un accès restreint aux autorisations pour la configuration des méthodes de diffusion. La section _Modes d’expédition_ a été renommée en _[!UICONTROL Delivery methods]_&#x200B;et&#x200B;_[!UICONTROL In-Store Pickup]_ est déplacée sous la section _[!UICONTROL Delivery methods]_. [GitHub-30053](https://github.com/magento/magento2/issues/30053) <!--- MC-41545-->

![Problème résolu](../assets/fix.svg) Adobe Commerce ne crée plus de réservation de produit en double après la mise à jour d&#39;un avoir par l&#39;API. <!--- MC-41757-->

![Problème corrigé](../assets/fix.svg) Le passage de l’onglet _[!UICONTROL Pick up in Store]_&#x200B;à l’onglet&#x200B;_[!UICONTROL Shipping]_ dans le workflow de passage en caisse ne déclenche plus d’erreur JavaScript lorsque seule la diffusion en magasin Pickup est disponible. <!--- MC-42808-->

![Problème résolu](../assets/fix.svg) La quantité de produit vendable et la quantité de produit en stock sont désormais correctement synchronisées. Auparavant, la compensation de réservation de stock n&#39;était pas recréée pour les commandes annulées. <!--- MC-42485-->

![Correction d’un problème](../assets/fix.svg) Les performances du programme de validation sont optimisées pour empêcher l’ajout d’une nouvelle source au produit enfant d’un produit groupé avec le type d’expédition `Ship Together`. <!--- MC-43039-->

## 1.2.3

[!DNL Inventory Management] 1.2.3 (version du module : `magento/inventory-metapackage = 1.2.3`) est pris en charge avec la version 2.4.3 et compatible avec la version 2.4.0 d’Adobe Commerce, Adobe Commerce sur les infrastructures cloud et la base de code Magento Open Source.

![Correction d’un problème](../assets/fix.svg) Correction de plusieurs problèmes liés à la visibilité du produit composite sur le serveur frontal.

![Correction d’un problème](../assets/fix.svg) Amélioration des performances de gestion des pages du panier avec la quantité minimale requise.

![Problème résolu](../assets/fix.svg) Plusieurs correctifs ont été ciblés pour résoudre les problèmes de création de sources, d’articles en rupture de stock, d’approvisionnement en stock, de tri des sources allouées, de diffusion en magasin et de commandes d’inventaire.

![Problème résolu](../assets/fix.svg) [!DNL Commerce] prend désormais en charge les codes postaux canadiens à trois chiffres pour la livraison en magasin. Les codes à six chiffres ne sont pas pris en charge en raison des limitations définies par `geonames.org`.

![Problème résolu](../assets/fix.svg) L’administrateur affiche désormais la quantité correcte de stock par défaut pour les produits désactivés sur la grille **Produits** et la page **Modifier le produit** pour les déploiements multi-magasin.

![Problème résolu](../assets/fix.svg) [!DNL Commerce] actualise désormais le cache de produit de catégorie lorsqu’un produit groupé est de nouveau en stock.

## 1.2.2

[!DNL Inventory Management] 1.2.2 (version du module : `magento/inventory-metapackage = 1.2.2`) est pris en charge avec la version 2.4.2 et compatible avec la version 2.4.0 d’Adobe Commerce, Adobe Commerce sur les infrastructures cloud et la base de code Magento Open Source.

![Correction d’un problème](../assets/fix.svg) Correction de plusieurs problèmes liés à la visibilité du produit composite sur le serveur frontal.

![Problème résolu](../assets/fix.svg) Amélioration des performances de la page du panier lors de la mise à jour de la quantité sur B2B.

![Correction d’un problème](../assets/fix.svg) Plusieurs correctifs étaient destinés à résoudre les problèmes liés au ramassage en magasin, aux mises à jour en masse et au seuil d’inventaire.

![Nouveau](../assets/new.svg) **Tests fonctionnels.** A introduit de nouveaux tests fonctionnels et a fourni des correctifs pour les tests existants afin de les rendre plus stables.

## 1.2.1

[!DNL Inventory Management] 1.2.1 (version du module : `magento/inventory-metapackage = 1.2.1`) est pris en charge avec la version 2.4.1 et compatible avec la version 2.4.0 d’Adobe Commerce, Adobe Commerce sur les infrastructures cloud et la base de code Magento Open Source.

![Correction d’un problème](../assets/fix.svg) Correction d’un problème connu lié à la tâche cron `inventory_cleanup_reservations` et correction d’un problème lié à la fonctionnalité de ramassage en magasin pour les produits groupés. Cette mise à jour comprend également des améliorations générales au calcul des stocks, à la prise en charge des produits groupés et aux fonctionnalités de commande en souffrance.

![Nouveau](../assets/new.svg) **Tests fonctionnels.** Ajout de nouveaux tests fonctionnels pour fournir une couverture supplémentaire pour la fonctionnalité de retrait en magasin.

## 1.2.0

[!DNL Inventory Management] 1.2.0 (version du module : `magento/inventory-metapackage = 1.2.0`) est pris en charge avec la version 2.4.0 d’Adobe Commerce, Adobe Commerce sur les infrastructures cloud et la base de code Magento Open Source.

![Correction de problèmes](../assets/fix.svg) De nombreux correctifs permettent de résoudre les problèmes d&#39;affectation de source, de prise en charge des fonctionnalités d&#39;environnement évolutif et de compatibilité avec PHP 7.4, MySQL 8 et PHPUNIT 9.

![Nouvelle](../assets/new.svg) **Méthode de diffusion en magasin.** Ajout d’une option permettant aux utilisateurs de sélectionner une source à utiliser comme emplacement de retrait lors du passage en caisse. Voir [Livraison en magasin](../stores-purchase/shipping-in-store-delivery.md) dans le _Guide de l’expérience client et d’achat_.

![Nouveau](../assets/new.svg) **Prise en charge groupée du produit pour le mode multi-source.** Inventory prend en charge tous les types de produits avec plusieurs sources.

![Nouveau](../assets/new.svg) **Réindexation asynchrone des stocks.** Ajout de la possibilité de réindexer le stock de manière asynchrone et d’améliorer les performances de plusieurs scénarios critiques.

![Nouvelles](../assets/new.svg) **Interfaces en bloc.** Ajout de nouvelles interfaces en bloc pour le contrôle de la délivrabilité : `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`, `\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`.

![Nouvelle](../assets/new.svg) **Couverture de test accrue.** Les nouvelles fonctionnalités sont couvertes par des tests automatisés, y compris une couverture étendue pour les problèmes découverts et corrigés.

![Problème connu](../assets/bug.svg) **Problème connu.** L’absence du champ `object_id` dans les métadonnées de réservation empêche le bon fonctionnement de la tâche `inventory_cleanup_reservations` cron. Ce problème a été introduit dans [magento/inventory#3046](https://github.com/magento/inventory/pull/3046).

**Solution :** exécutez les requêtes MySQL suivantes pour nettoyer manuellement les réservations :

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6.

[!DNL Inventory Management] 1.1.6 (version du module : `inventory-composer-metapackage = 1.1.6`) est pris en charge avec la version 2.3.6 et compatible avec les versions 2.3.5, 2.3.4, 2.3.3, 2.3.2, 2.3.1 et 2.3.0 d’Adobe Commerce, Adobe Commerce sur les infrastructures cloud et la base de code Magento Open Source.

![Problème résolu](../assets/fix.svg) Correctifs pour résoudre les problèmes liés aux commandes en souffrance, aux avoirs, à la grille de rapports sur les stocks faibles, aux correctifs liés à l’outil de ligne de commande « résoudre les incohérences » et aux améliorations générales.

![Nouveau](../assets/new.svg) **Réindexation asynchrone des stocks.** Ajout de la possibilité de réindexer le stock de manière asynchrone et d’améliorer les performances de plusieurs scénarios critiques.

## 1,1,5

[!DNL Inventory Management] 1.1.5 (version du module : `inventory-composer-metapackage = 1.1.5`) est pris en charge avec la version 2.3.5 et compatible avec les versions 2.3.4, 2.3.3, 2.3.2, 2.3.1 et 2.3.0 d’Adobe Commerce, Adobe Commerce sur les infrastructures cloud et la base de code Magento Open Source.

![Nouveau](../assets/new.svg) **Mettre à jour l’inventaire une fois le SKU du produit modifié.** Ajout d’un nouveau paramètre de configuration pour passer au nouveau comportement : « Synchroniser avec le catalogue ».

![Nouveau](../assets/new.svg) **Tests fonctionnels.** Introduction de nouveaux tests fonctionnels pour éliminer l’écart de couverture des tests. Correction de plusieurs problèmes pour rendre les tests plus stables et fiables).

![Problème connu](../assets/bug.svg) Correctifs pour empêcher la vente excessive de produits, visibilité des produits « en rupture de stock » sur le storefront, nombreux correctifs pour la prise en charge de l’environnement évolutif et améliorations de l’interface utilisateur.

## 1.1.4

[!DNL Inventory Management] 1.1.4 (version du module : `inventory-composer-metapackage = 1.1.4`) est pris en charge avec la version 2.3.4 et compatible avec les versions 2.3.3, 2.3.2, 2.3.1 et 2.3.0 d’Adobe Commerce, Adobe Commerce sur les infrastructures cloud et la base de code Magento Open Source.

![Correction d’un problème ](../assets/fix.svg)**Amélioration des performances.** Ajout d’une logique de regroupement pour la commande de l’interface de ligne de commande de réservation d’inventaire afin de réduire l’utilisation de la mémoire et d’éviter les cas où le processus est bloqué sans réponse.

![Nouvelle ](../assets/new.svg)**Couverture de test accrue.** Introduit de nombreux nouveaux tests fonctionnels. Presque tous les scénarios d’inventaire manuels sont couverts par des tests automatisés.

![Problème connu](../assets/bug.svg) De nombreux correctifs ont été conçus pour résoudre les problèmes liés aux avoirs, aux produits groupés et aux actions de masse sur les sources et les stocks.

## 1.1.3

[!DNL Inventory Management] 1.1.3 (version du module : `inventory-composer-metapackage = 1.1.3`) est pris en charge avec la version 2.3.3 et compatible avec les versions 2.3.2, 2.3.1 et 2.3.0 d’Adobe Commerce, Adobe Commerce sur les infrastructures cloud et la base de code Magento Open Source.

![Correction d’un problème ](../assets/fix.svg)**Amélioration de l’intégration avec les fonctionnalités Adobe Commerce et B2B.** [!DNL Inventory Management] fonctionne désormais correctement avec les fonctionnalités suivantes pour les sites web utilisant des sources d’inventaire et des stocks autres que ceux par défaut :

- Classer par SKU (Adobe Commerce)
- Commande rapide (B2B)
- Listes de demandes d&#39;approvisionnement (B2B)

![Nouveau ](../assets/new.svg)**Performances accrues.** performances de navigation du catalogue Storefront sont améliorées pour les sites web exécutant le stock et la source d’inventaire par défaut.

![Nouvelle ](../assets/new.svg)**Couverture de test accrue.** La couverture des tests fonctionnels et d’intégration automatisés a considérablement augmenté.

## 1.1.2

[!DNL Inventory Management] 1.1.2 (version du module : `inventory-composer-metapackage = 1.1.2`) est pris en charge avec la version 2.3.2 et compatible avec les versions 2.3.1 et 2.3.0 d’Adobe Commerce, Adobe Commerce sur les infrastructures cloud et la base de code Magento Open Source.

![Correction d’un problème](../assets/fix.svg) Ajout d’un `source_code` à la réponse pour le point d’entrée REST GET `/V1/shipments`. <!-- https://github.com/magento/inventory/pull/2142 -->

![Problème résolu](../assets/fix.svg) Problème résolu pour effacer correctement les réservations et mettre à jour les quantités de produit après l&#39;émission d&#39;un avoir pour une commande non expédiée. Lorsque vous sélectionnez l’option à <!-- https://github.com/magento/inventory/pull/2179 -->

![Problème résolu](../assets/fix.svg) Problème résolu afin d&#39;enregistrer correctement la quantité pour les enfants de produits configurables lors de la saisie de quantités lors de la création du produit. <!-- https://github.com/magento/inventory/pull/2158 -->

Les nouveaux modules d’[!DNL Inventory Management] 1.1.2 Beta incluent :

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![Nouveau](../assets/new.svg) **Ajout d’un point d’entrée de transfert de stock partiel en bloc** - Les points d’entrée de transfert en bloc actuels déplacent toute la quantité affectée d’une origine vers une source de destination. Le nouveau point d’entrée `/rest/V1/inventory/bulk-partial-source-transfer` permet aux commerçants de transférer un stock partiel de la source vers la source sous la forme d’une opération en bloc. Pour transférer une quantité spécifique, saisissez une demande au point d&#39;entrée avec les `sku`, `qty`, `origin_source_code` et `destination_source_code`. Les transferts vérifient que l&#39;origine est affectée au `sku`, qu&#39;il existe une quantité suffisante pour le transfert, etc. Voir [Actions en masse d’inventaire](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"} dans la documentation de l’API REST. <!-- https://github.com/magento/inventory/pull/2117 -->

![Nouvelle](../assets/new.svg) **Interface de ligne de commande de réservation ajoutée** - Les nouvelles commandes vous offrent des options pour détecter et résoudre les incohérences de réservation. À mesure que les commandes envoient et modifient leur statut, [!DNL Inventory Management] génère les réservations et mises à jour initiales par le biais des réservations de rémunération. Ces commandes renvoient une liste des incohérences détectées par ID de commande, SKU et ID de stock, et créent des réservations à résoudre. Pour plus d’informations, consultez la [référence de l’interface en ligne de commande](cli.md). <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![Nouveau](../assets/new.svg) **Amélioration des performances pour les sources et options SSA** - Le tri et la sélection des sources pendant l’expédition ont entraîné une dégradation des performances pour les stocks comportant un grand nombre de sources. Cette version offre des améliorations de performances importantes pour répertorier et trier les sources disponibles lors de la révision et de la sélection des options SSA dans les expéditions. <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![Nouveau](../assets/new.svg) **Ajout de la prise en charge de GraphQL pour Inventory management** - Cette version installe un nouveau module de `magento/module-inventory-graph-ql`. Les attributs GraphQL [ProductInterface](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"} incluent désormais les attributs `only_x_left_in_stock` et `stock_status` pour la prise en charge des [!DNL Inventory Management]. <!-- https://github.com/magento/inventory/pull/2124 -->

![Nouvelle](../assets/new.svg) **IU simplifiée pour les sources affectées** - Le tableau Sources affectées dans les pages de produits présente un contenu simplifié pour des mises à jour plus faciles et des performances accrues lors de l’affichage de nombreuses sources. Toutes les sources sont répertoriées par nom de source (pointez pour `source_code`).

![Nouveau](../assets/new.svg) **Service Export Aggregated Stock** - Cette version fournit un nouveau service Export Aggregated Stock (qui conserve les réservations dans le système) pour prendre en charge les canaux de vente externes, tels que les annonces Amazon, eBay et Google Shopping.  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

[!DNL Inventory Management] 1.1.0 (version du module : `inventory-composer-metapackage = 1.1.0`) est pris en charge et compatible avec la version 2.3.0 d’Adobe Commerce, Adobe Commerce sur les infrastructures cloud et la base de code Magento Open Source. [!DNL Inventory Management] 1.1.1 est publié uniquement sous la forme d’une mise à jour du nom du package, pris en charge par la version 2.3.1 et compatible avec la version 2.3.0 d’Adobe Commerce, Adobe Commerce sur les infrastructures cloud et la base de code Magento Open Source.

![Correction d’un problème](../assets/fix.svg) **Ajout de la prise en charge d’Elasticsearch pour les modes mono et multi-sources** — Vous pouvez désormais configurer et utiliser Elasticsearch avec des stocks personnalisés. Voir [Configuration du service Elasticsearch](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html?lang=fr){target="_blank"} pour obtenir des informations sur l’installation. <!-- PR https://github.com/magento/inventory/pull/1943 -->

![Correction de problèmes](../assets/fix.svg) Résolution des problèmes de performances avec le Stock par défaut pour augmenter considérablement les performances avec de nombreuses opérations. Les améliorations augmentent les performances pour le mode à source unique, les pages Transférer l&#39;inventaire vers Source, les pages de catégorie Storefront et les calculs de quantité vendable.

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![Problème résolu](../assets/fix.svg) Problèmes résolus avec le statut En rupture de stock et le transfert d’inventaire en bloc vers les stocks pour les produits configurables et groupés. La sélection des produits parents et l’exécution d’actions en bloc n’affectent pas le statut du produit. Si le produit parent était en stock, il reste en stock.

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![Nouvel](../assets/new.svg) **Algorithme de priorité à distance** — L&#39;algorithme de priorité à distance est un nouvel algorithme de sélection Source prêt à l&#39;emploi pour les recommandations d&#39;expédition basées sur la distance. Cet algorithme compare l&#39;emplacement de l&#39;adresse de destination d&#39;expédition avec les emplacements source afin de déterminer la source la plus proche pour exécuter les expéditions. La distance peut être déterminée par la distance physique ou le temps passé à voyager d&#39;un endroit à un autre, en utilisant des données de géolocalisation importées ou des directions de Google (conduite, marche ou vélo).

![Nouvelle](../assets/new.svg) **Liste de quantité de sources étendue** — Les commerçants ayant un grand nombre de sources peuvent facilement survoler et afficher toutes les sources par produit via la grille de produits. Chaque produit affiche un minimum de cinq sources et quantités correspondantes. Lorsque vous pointez sur les sources, vous pouvez faire défiler la liste complète des sources et des quantités actuelles.

![Problème connu](../assets/bug.svg) Problème connu avec Magento Open Source et Adobe Commerce v2.3.1 : la migration asynchrone des données entre les sources rencontre des problèmes liés aux modifications apportées aux API asynchrones avec des noms de rubriques reflétant les noms de classe et de méthode PHP. Il est recommandé d’utiliser des opérations synchrones et de définir **[!UICONTROL Run asynchronously]** sur `No`.
