---
title: '[!DNL Inventory Management] notes de mise à jour'
description: Consultez les notes de mise à jour pour plus d’informations sur toutes les versions de  [!DNL Inventory Management]  .
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: 01d8a1d50f574330f3ce7e8bf03a018f0079f5db
workflow-type: tm+mt
source-wordcount: '3445'
ht-degree: 0%

---

# Notes de mise à jour de [!DNL Inventory Management]

Ces notes de mise à jour décrivent les versions de [!DNL Inventory Management] et incluent :

![New](../assets/new.svg) Nouvelles fonctionnalités
![Problème corrigé](../assets/fix.svg) Correctifs et améliorations
![Problème connu](../assets/bug.svg) Problèmes connus

[!DNL Inventory Management] est un projet spécial d’ingénierie communautaire Magento Open Source ouvert aux contributeurs. Pour participer et contribuer, consultez le référentiel [GitHub project](https://github.com/magento/inventory) et [wiki](https://github.com/magento/inventory/wiki) pour commencer. Pour discuter du projet, rejoignez le canal [Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) ([auto-inscription](https://opensource.magento.com/slack)).

[Calendrier des versions](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html?lang=fr){target="_blank"} pour les versions prises en charge et compatibles.

## v1.2.7

Les notes de mise à jour de [!DNL Inventory Management] 1.2.7 sont incluses dans les [notes de mise à jour de base 2.4.7](https://experienceleague.adobe.com/fr/docs/commerce-operations/release/notes/adobe-commerce/2-4-7#inventory-management-1).

## v1.2.6

[!DNL Inventory Management] 1.2.6 (version de module : `magento/inventory-metapackage = 1.2.6`) est pris en charge avec la version 2.4.6 et compatible avec la version 2.4.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![Problème corrigé](../assets/fix.svg) Le storefront affiche désormais les produits composites (configurables, groupés et regroupés) en tant qu’en stock lorsque les produits enfants qui ont été vendus sont renvoyés en stock. Auparavant, le storefront indiquait que le produit composite était en rupture de stock dans ces conditions. <!-- ACP2E-1106-->

![Problème corrigé](../assets/fix.svg) Les options de produit configurables s’affichent désormais comme prévu en rupture de stock sur le storefront si l’option a été créée avec une quantité définie sur 0 et **[!UICONTROL Display out-of-stock products]** est activée. <!-- ACP2E-1148-->

![Problème corrigé](../assets/fix.svg) Les caches de page de catégorie ne sont plus invalidés lorsque la quantité de stock change et que le produit est toujours en stock. Adobe Commerce charge désormais les pages à partir du cache au lieu de les régénérer lorsque la quantité de produits (et rien d’autre) sur la page de catégorie de storefront change. <!-- ACP2E-118-->

![Problème corrigé](../assets/fix.svg) Le nombre de produits de la liste de catégories est désormais correct lors de l’utilisation de l’inventaire en mode source unique avec le paramètre **[!UICONTROL Display Out-Of-Stock Products]** activé. Adobe Commerce vérifie désormais si un produit est vendable lors du comptage. <!-- ACP2E-1033-->

![ Correction d’un problème ](../assets/fix.svg) Les règles de prix du panier pour la livraison en magasin fonctionnent désormais comme prévu lorsque le stock est activé. Auparavant, les remises générées par des règles de prix de panier n’étaient pas appliquées dans ces conditions. <!-- ACP2E-1015-->

![ Correction d’un problème ](../assets/fix.svg) La mise à jour de l’inventaire des produits en mode planifié n’efface plus tous les caches. Auparavant, l’indexeur d’inventaire effacait tous les caches de configuration. <!-- ACP2E-1003-->

![Problème corrigé](../assets/fix.svg) La valeur de l’attribut **[!UICONTROL Allow Multiple Boxes for Shipping]** d’un produit dans l’inventaire avancé est désormais enregistrée comme prévu. <!-- ACP2E-992-->

![ Correction d’un problème ](../assets/fix.svg) Adobe Commerce émet désormais une compensation de réservation exacte après un avoir de crédit de remboursement partiel pour une commande qui a été placée avec la récupération en magasin. Auparavant, une réservation incorrecte enregistrée dans la table `inventory_reservation` lorsqu’un utilisateur administrateur créait une note de crédit sans cocher la case **[!UICONTROL Return to Stock]** . <!-- ACP2E-979-->

![ Problème corrigé ](../assets/fix.svg) Adobe Commerce n’affiche plus les produits configurables en rupture de stock sur le storefront lorsque l’une de ses variations a été manuellement remontée en stock dans les déploiements mettant en oeuvre l’inventaire multi-source. <!-- ACP2E-952-->

![ Correction d’un problème ](../assets/fix.svg) La position des colonnes sur la grille de produit (**[!UICONTROL Catalog]** > **[!UICONTROL Products]**) ne revient plus à sa position précédente une fois la page rechargée dans les déploiements avec plusieurs sources d’inventaire configurées. <!-- ACP2E-925-->

![Problème corrigé](../assets/fix.svg) La quantité de stock est désormais correcte après l’émission d’une note de crédit pour un produit virtuel lorsque la case à cocher **[!UICONTROL Back to stock]** n’est pas sélectionnée. <!-- ACP2E-908-->

![Problème corrigé](../assets/fix.svg) Vous pouvez désormais enregistrer des catégories avec tri automatique des produits et une portée affectée à un stock autre que le stock par défaut. Auparavant, Adobe Commerce n&#39;enregistrait pas la catégorie et affichait cette erreur : `Something went wrong while saving the category`. <!-- ACP2E-859-->

![Problème corrigé](../assets/fix.svg) L’état du stock configurable du produit est désormais mis à jour comme prévu lors de la création du produit avec toutes les variations configurables en rupture de stock. <!-- ACP2E-813-->

![ Correction d’un problème ](../assets/fix.svg) L’outil d’analyse d’incohérence de réservation fonctionne désormais correctement avec les commandes partiellement expédiées qui contiennent des produits configurables, groupés et regroupés. Les types de produits composites sont maintenant analysés. Auparavant, les annulations et les remboursements n’étaient enregistrés que pour les produits parents, et non pour les articles de commande de sous-produits des produits configurables et de regroupement de lots. <!-- ACP2E-924-->

![Problème corrigé](../assets/fix.svg) Adobe Commerce n’affiche plus d’erreur lorsqu’un utilisateur administrateur tente d’affecter 200 sources d’inventaire ou plus à un stock ou à un produit. <!-- ACP2E-1180-->

![Problème corrigé](../assets/fix.svg) Adobe Commerce prend désormais en charge la création d’une note de crédit pour une commande à partir de laquelle un produit a été supprimé. Auparavant, les commerçants ne pouvaient pas créer d’avoir lorsque les produits avaient été supprimés de la commande après la création d’une facture. L’application a affiché cette erreur : `Following products with requested skus were not found: s00001`. t. <!-- ACP2E-1138-->

![Problème corrigé](../assets/fix.svg) Les magasins sont désormais filtrés en fonction d’identifiants de magasin uniques et multiples. Le code d’attribut de produit `event` a été ajouté à la liste des codes d’attribut réservés. Auparavant, le rapport Faible stock générait une exception lorsque le module Inventaire était installé. <!-- ACP2E-1017-->

![Problème corrigé](../assets/fix.svg) Les filtres de navigation en couches fonctionnent désormais comme prévu et les produits en rupture de stock sont désormais ajoutés à la liste des produits de catégorie de storefront. Le nouvel attribut de tri `is_out_of_stock` utilise le mappeur de champ dynamique Elasticsearch pour la collection de produits storefront. <!-- ACP2E-748-->

![Problème corrigé](../assets/fix.svg) L’état du stock du produit composite (bundle, groupé et configurable) est mis à jour comme prévu lorsque l’état du stock du produit enfant est modifié par un appel REST `POST /rest/V1/inventory/source-items` . <!-- ACP2E-1209-->

## v1.2.5

[!DNL Inventory Management] 1.2.5 (version de module : `magento/inventory-metapackage = 1.2.5`) est pris en charge avec la version 2.4.5 et compatible avec la version 2.4.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![Problème corrigé](../assets/fix.svg) L’état du stock par défaut des produits groupés et groupés est désormais mis à jour comme prévu lorsqu’un commerçant crée une expédition à partir de l’administrateur. Auparavant, l’état de ces produits restait inchangé après la création d’une expédition. <!--- ACP2E-418-->

![Problème corrigé](../assets/fix.svg) Les produits configurables sont désormais retournés en stock lorsque l’une des conditions suivantes est remplie : 1. Le produit parent a au moins un enfant enregistré en stock. 2. Le produit configurable lui-même a été mis à jour et défini sur **en stock** et a au moins un enfant en stock. <!--- ACP2E-443-->

![Problème corrigé](../assets/fix.svg) Les modifications d’inventaire implémentées via l’API REST sont désormais répercutées comme prévu sur les pages Détails du produit. Le cache des produits du catalogue est maintenant nettoyé après comparaison des états des stocks actuels et précédents. Auparavant, l’omission de la fonction de rappel entraînait une évaluation incorrecte des modifications d’état du stock, qui ne déclenchaient pas le nettoyage du cache nécessaire. Par conséquent, le storefront ne reflétait pas les modifications d’inventaire. <!--- ACP2E-161-->

![Problème corrigé](../assets/fix.svg) Les produits qui sont affectés au stock par défaut et qui étaient auparavant en rupture de stock sont désormais visibles sur le storefront après la mise à jour de l’élément source à l’aide de `/V1/inventory/source-items`. Auparavant, ce point d&#39;entrée de l&#39;API REST définissait le mauvais `stock_status`. <!--- ACP2E-562-->

![ Correction d’un problème ](../assets/fix.svg) La désaffectation des sources d’inventaire par le biais d’une action en masse (**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**) fonctionne désormais comme prévu lorsque les sources incluent des SKU qui sont des doublons, à l’exception d’un zéro au début (par exemple, `01234` et `1234`). Auparavant, l’application n’annulait pas l’affectation des sources d’inventaire et générait une erreur. <!--- ACP2E-2641-->

![Problème corrigé](../assets/fix.svg) L’état du stock de produit est désormais toujours **en stock** sur le storefront lorsque des commandes en arrière infinies sont activées et que le produit est affecté à un stock personnalisé, quelle que soit la quantité en arrière-plan. Auparavant, les produits étaient en rupture de stock, même lorsque les commandes antérieures étaient activées. <!--- ACP2E-664-->

![Problème corrigé](../assets/fix.svg) Le stock de produit parent et enfant configurable est désormais mis à jour correctement après la mise à jour de l’élément source avec `POST /V1/inventory/source-items`. Une fois le produit enfant mis à jour via l’API, un nouveau module externe Inventaire pour les vérifications de stock par défaut et met à jour la quantité et l’état configurables du produit. <!--- ACP2E-442-->

![Problème corrigé](../assets/fix.svg) Les produits groupés en rupture de stock ne sont plus répertoriés sur la page Catégorie du storefront. <!--- ACP2E-2082-->

![Correction d’un problème ](../assets/fix.svg) Correction du nom du module dans `CatalogInventory` `composer.json`. <!--- ACP2E-2914-->

![Problème corrigé](../assets/fix.svg) L’état de la commande principale est désormais correctement représenté dans l’administrateur après avoir passé une commande avec zéro quantité de produit dans un déploiement multi-source/stock. [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![Problème corrigé](../assets/fix.svg) Les produits en rupture de stock ne s’affichent plus sur la page Catégorie du storefront lorsque le produit du lot est mis à jour à partir de la section stocks. <!--- ACP2E-2012-->

![Problème corrigé](../assets/fix.svg) Les problèmes de compatibilité avec PHP 7.4 sont résolus. <!--- AC-3192-->

![Problème corrigé](../assets/fix.svg) Les performances des opérations d’enregistrement qui incluent des produits de lot contenant de nombreuses options (plusieurs 100) sont améliorées. Auparavant, l’enregistrement de ces produits groupés volumineux prenait plusieurs minutes et entraînait parfois des dépassements de délai dans les déploiements pour lesquels les services d’inventaire étaient activés. [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![Problème corrigé](../assets/fix.svg) L’outil d’action en bloc de produit (**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**) fonctionne désormais comme prévu lors de l’attribution de la source de stock à plusieurs produits lorsque les SKU sont dupliqués, à l’exception d’un `0` de début (par exemple, `01234` et `1234`). Auparavant, une source d’inventaire était affectée à un seul produit. [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![Problème corrigé](../assets/fix.svg) Le champ `ProductInterface.only_x_left_in_stock` renvoie désormais 0 si l’inventaire est 0. Auparavant, il renvoyait la valeur null. [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![Problème corrigé](../assets/fix.svg) Vous pouvez désormais modifier le stock par défaut à partir de l’administrateur **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**. Auparavant, une erreur JavaScript s’affichait dans la console lorsque vous tentiez d’ajouter ou de supprimer des sources du stock par défaut, bien que vous puissiez affecter des sites web au stock par défaut. <!--- ACP2E-545-->

![Problème corrigé ](../assets/fix.svg) <!--- ACP2E-274--> Le nombre de produits de la liste de catégories est désormais correct lors de l’utilisation du mode source unique d’inventaire avec le paramètre **[!UICONTROL Display Out-Of-Stock Products]** activé. Un nouveau module externe utilise désormais `AreProductsSalableInterface` et `StockConfigurationInterface` pour déterminer le nombre total de produits. Auparavant, la liste de produits de catégorie renvoyait une quantité de produits incorrecte.

![Problème corrigé](../assets/fix.svg) <!--- ACP2E-322--> Les produits configurables sont désormais déplacés vers la dernière position de la liste de produits après la mise à jour du stock lorsque le paramètre **[!UICONTROL Move out of stock to the bottom]** est activé. Une nouvelle requête de base de données personnalisée est implémentée pour annuler l’ordre de tri des index Elasticsearch, sans tenir compte de l’ordre de tri activé par l’administrateur. Auparavant, les produits configurables et leurs produits enfants n’étaient pas déplacés vers le bas de la liste lorsque ce paramètre était activé.

## v1.2.4

Inventory management 1.2.4 (version de module : `magento/inventory-metapackage = 1.2.4`) est pris en charge avec la version 2.4.4 et compatible avec la version 2.4.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![Problème corrigé](../assets/fix.svg) Commerce affiche désormais une valeur exacte de quantité vendable pour tous les produits en mode Liste des produits d’administration. Auparavant, il affichait une valeur vide pour la quantité vendable de produits en stock avec des SKU contenant des caractères spéciaux. <!--- MC-41936-->

![Problème corrigé](../assets/fix.svg) Les performances des actions de panier et de passage en caisse ont été améliorées, par exemple l’ajout de produits au panier dans les déploiements avec de nombreuses sources d’inventaire (environ 10 000). <!--- MC-42570-->

![Correction d’un problème](../assets/fix.svg) La commande `bin/magento inventory:reservation:list-inconsistencies` gère désormais correctement les commandes avec des envois partiels, même si les réservations sont ignorées de la base de données et que le cache a été effacé. Auparavant, lorsque cette commande était exécutée avec un cache pré-effacé, Commerce affichait l’erreur suivante : `Area code is not set`. <!--- MC-42142-->

![ Correction d’un problème ](../assets/fix.svg) L’indexation incrémentielle des produits enfants groupés n’entraîne plus l’indexation incorrecte des autres produits groupés lors du partage des enfants. <!--- MC-41963-->

![Problème corrigé](../assets/fix.svg) La page de catégorie storefront affiche désormais le nombre de produits correct après la suppression d’un produit d’une catégorie par API. Auparavant, le nombre de produits de la page de catégorie était incorrect jusqu’à la réindexation. <!--- MC-42287-->

![Problème corrigé](../assets/fix.svg) Les produits configurables peuvent désormais être renvoyés en stock lors de la création d’une note de crédit lorsque l’option **[!UICONTROL Manage Stock]** est désactivée. Auparavant, Commerce n’affichait pas la case **Revenir au stock** sur la page de création de l’avoir lorsque cette option était désactivée. <!--- MC-42002-->

![Correction d’un problème ](../assets/fix.svg) La gestion du stock qui dépasse 10 000 articles a été améliorée. Auparavant, les problèmes de performances empêchaient parfois les commerçants de modifier le stock dans l’administrateur avant de lancer leur site web. <!--- MC-42643-->

![ Correction d’un problème ](../assets/fix.svg) La page **[!UICONTROL User Roles]** de l’administrateur est mise à jour afin de fournir aux administrateurs des autorisations restreintes d’accès à la configuration des méthodes de diffusion. La section _Méthodes d’expédition_ a été renommée _[!UICONTROL Delivery methods]_&#x200B;et&#x200B;_[!UICONTROL In-Store Pickup]_ est déplacé sous la section _[!UICONTROL Delivery methods]_. [GitHub-30053](https://github.com/magento/magento2/issues/30053) <!--- MC-41545-->

![ Problème corrigé ](../assets/fix.svg) Adobe Commerce ne crée plus de réservation de produit en double après la mise à jour d’une note de crédit par l’API. <!--- MC-41757-->

![ Correction d’un problème ](../assets/fix.svg) Le passage de l’onglet _[!UICONTROL Pick up in Store]_&#x200B;à l’onglet&#x200B;_[!UICONTROL Shipping]_ dans le workflow de passage en caisse ne déclenche plus d’erreur JavaScript lorsque seule la livraison de la prise en charge en magasin est disponible. <!--- MC-42808-->

![Problème corrigé](../assets/fix.svg) La quantité de produits vendables et la quantité de produits en stock sont désormais synchronisées correctement. Auparavant, la compensation des réservations de stock n’était pas recréée pour les commandes annulées. <!--- MC-42485-->

![Problème corrigé](../assets/fix.svg) Les performances du programme de validation sont optimisées pour empêcher l’ajout d’une nouvelle source au produit enfant d’un produit groupé avec le type d’expédition `Ship Together`. <!--- MC-43039-->

## 1.2.3

[!DNL Inventory Management] 1.2.3 (version de module : `magento/inventory-metapackage = 1.2.3`) est pris en charge avec la version 2.4.3 et compatible avec la version 2.4.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![Correction d’un problème](../assets/fix.svg) Correction de plusieurs problèmes liés à la visibilité du produit composite sur l’interface.

![Correction d’un problème](../assets/fix.svg) Amélioration des performances de gestion des paniers avec la quantité minimale requise.

![ Problème corrigé ](../assets/fix.svg) : plusieurs correctifs ont été ciblés afin de résoudre les problèmes liés à la création de sources, aux articles en rupture de stock, à l’approvisionnement en stock, au tri des sources allouées, à la diffusion en magasin et aux commandes d’inventaire.

![ Correction d’un problème ](../assets/fix.svg) [!DNL Commerce] qui prend désormais en charge les codes postaux canadiens à trois chiffres pour la livraison en magasin. Les codes à six chiffres ne sont pas pris en charge en raison de limitations définies par `geonames.org`.

![Problème corrigé ](../assets/fix.svg) L’administrateur affiche désormais la quantité correcte de stock par défaut pour les produits désactivés sur la grille **Produits** et la page **Modifier le produit** pour les déploiements multi-magasins.

![Correction d’un problème ](../assets/fix.svg) [!DNL Commerce] qui actualise désormais le cache de produits de catégorie lorsqu’un produit de lot revient en stock.

## 1.2.2

[!DNL Inventory Management] 1.2.2 (version de module : `magento/inventory-metapackage = 1.2.2`) est pris en charge avec la version 2.4.2 et compatible avec la version 2.4.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![Correction d’un problème](../assets/fix.svg) Correction de plusieurs problèmes liés à la visibilité du produit composite sur l’interface.

![Correction d’un problème](../assets/fix.svg) Amélioration des performances de page de panier lors de la mise à jour de la quantité sur B2B.

![Problème corrigé](../assets/fix.svg) Plusieurs correctifs destinés à résoudre les problèmes liés à la récupération en magasin, aux mises à jour en masse et au seuil d’inventaire.

![Nouveau](../assets/new.svg) **Tests fonctionnels.** Ajout de nouveaux tests fonctionnels et de correctifs pour les tests existants afin de les rendre plus stables.

## 1.2.1

[!DNL Inventory Management] 1.2.1 (version de module : `magento/inventory-metapackage = 1.2.1`) est pris en charge avec la version 2.4.1 et compatible avec la version 2.4.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![Correction d’un problème ](../assets/fix.svg) Correction d’un problème connu lié à la tâche de cron `inventory_cleanup_reservations` et résolution d’un problème lié à la fonctionnalité de récupération en magasin pour les produits en bundle. Cette mise à jour inclut également des améliorations générales pour le calcul des stocks, la prise en charge des produits en bundle et la fonctionnalité de backorder.

![Nouveau](../assets/new.svg) **Tests fonctionnels.** Introduction de nouveaux tests fonctionnels pour fournir une couverture supplémentaire pour la fonctionnalité de prise en charge en magasin.

## 1.2.0

[!DNL Inventory Management] 1.2.0 (version de module : `magento/inventory-metapackage = 1.2.0`) est pris en charge avec la version 2.4.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![Correction d’un problème](../assets/fix.svg) De nombreux correctifs pour résoudre les problèmes d’attribution de sources, de prise en charge de fonctionnalités d’environnement évolutive et de compatibilité avec PHP 7.4, MySQL 8 et PHPUNIT 9.

![Nouveau](../assets/new.svg) **Méthode de remise en magasin.** Ajout d’une option permettant aux utilisateurs de sélectionner une source à utiliser comme emplacement de récupération lors du passage en caisse. Voir [Diffusion en magasin](../stores-purchase/shipping-in-store-delivery.md) dans le _Guide de ventes et d’achat d’expérience_.

![Nouveau](../assets/new.svg) **Prise en charge du produit groupé pour le mode multi-source.** L’inventaire prend en charge tous les types de produits avec plusieurs sources.

![Nouveau](../assets/new.svg) **Réindexation asynchrone des stocks.** Ajout de la possibilité de réindexer de manière asynchrone le stock et d’améliorer les performances de plusieurs scénarios critiques.

![Nouveau](../assets/new.svg) **Interfaces en masse.** Ajout de nouvelles interfaces en masse pour le contrôle de la salabilité : `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`, `\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`.

![Nouveau](../assets/new.svg) **Couverture de test accrue.** Les nouvelles fonctionnalités sont couvertes par des tests automatisés, y compris une couverture étendue pour les problèmes détectés et résolus.

![Problème connu](../assets/bug.svg) **Problème connu.** L’absence du champ `object_id` dans les métadonnées de réservation empêche le fonctionnement correct de la tâche cron `inventory_cleanup_reservations`. Ce problème a été introduit dans [magento/inventory#3046](https://github.com/magento/inventory/pull/3046).

**Solution :** Exécutez les requêtes MySQL suivantes pour nettoyer manuellement les réservations :

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6

[!DNL Inventory Management] 1.1.6 (version de module : `inventory-composer-metapackage = 1.1.6`) est pris en charge avec la version 2.3.6 et compatible avec les versions 2.3.5, 2.3.4, 2.3.3, 2.3.2, 2.3.1 et 2.3.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![ Correction d’un problème](../assets/fix.svg) Correctifs afin de résoudre les problèmes liés aux commandes en arrière-plan, aux notes de crédit, à la grille de rapports de faible stock, aux correctifs liés à l’outil d’interface de ligne de commande &quot;résoudre les incohérences&quot; et aux améliorations générales.

![Nouveau](../assets/new.svg) **Réindexation asynchrone des stocks.** Ajout de la possibilité de réindexer de manière asynchrone le stock et d’améliorer les performances de plusieurs scénarios critiques.

## 1.1.5

[!DNL Inventory Management] 1.1.5 (version de module : `inventory-composer-metapackage = 1.1.5`) est pris en charge avec la version 2.3.5 et compatible avec les versions 2.3.4, 2.3.3, 2.3.2, 2.3.1 et 2.3.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![Nouveau](../assets/new.svg) **Mettez à jour l’inventaire une fois le SKU du produit modifié.** Ajout d’un nouveau paramètre de configuration pour passer au nouveau comportement : &quot;Synchroniser avec le catalogue&quot;.

![Nouveau](../assets/new.svg) **Tests fonctionnels.** Ajout de nouveaux tests fonctionnels pour éliminer l’écart de couverture de test. Correction de plusieurs problèmes pour rendre les tests plus stables et fiables).

![Problème connu](../assets/bug.svg) Correctifs afin d’éviter la survente de produits, la visibilité des produits &quot;en rupture de stock&quot; sur le storefront, de nombreux correctifs pour la prise en charge évolutive de l’environnement et les améliorations de l’interface utilisateur.

## 1.1.4

[!DNL Inventory Management] 1.1.4 (version de module : `inventory-composer-metapackage = 1.1.4`) est pris en charge avec la version 2.3.4 et compatible avec les versions 2.3.3, 2.3.2, 2.3.1 et 2.3.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![ Correction d’un problème ](../assets/fix.svg)**Amélioration des performances.** Introduction d’une logique de regroupement pour la commande d’interface de ligne de commande des réservations d’inventaire afin de réduire l’utilisation de la mémoire et d’éviter les cas où le processus est bloqué sans réponse.

![Nouveau ](../assets/new.svg)**Couverture de test accrue.** Ajout de nombreux nouveaux tests fonctionnels. Presque tous les scénarios d’inventaire manuel sont couverts par des tests automatisés.

![Problème connu](../assets/bug.svg) De nombreux correctifs visent à résoudre les problèmes liés aux notes de crédit, aux produits groupés et aux actions de masse des sources et des stocks.

## 1.1.3

[!DNL Inventory Management] 1.1.3 (version de module : `inventory-composer-metapackage = 1.1.3`) est pris en charge avec la version 2.3.3 et compatible avec les versions 2.3.2, 2.3.1 et 2.3.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![ Correction d’un problème ](../assets/fix.svg)**Amélioration de l’intégration aux fonctionnalités Adobe Commerce et B2B.** [!DNL Inventory Management] fonctionne désormais correctement avec les fonctionnalités suivantes pour les sites web qui utilisent des sources d’inventaire et des stocks non par défaut :

- Commande par SKU (Adobe Commerce)
- Ordre rapide (B2B)
- Listes de demandes (B2B)

![Nouveau ](../assets/new.svg)**Amélioration des performances.** Les performances de navigation du catalogue Storefront ont été améliorées pour les sites web exécutant le stock et la source de stock par défaut.

![Nouveau ](../assets/new.svg)**Couverture de test accrue.** La couverture des tests fonctionnels et d’intégration automatisés a considérablement augmenté.

## 1.1.2

[!DNL Inventory Management] 1.1.2 (version de module : `inventory-composer-metapackage = 1.1.2`) est pris en charge avec la version 2.3.2 et compatible avec les versions 2.3.1 et 2.3.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![ Correction d’un problème ](../assets/fix.svg) ajouté `source_code` à la réponse pour le point de terminaison REST de GET `/V1/shipments`. <!-- https://github.com/magento/inventory/pull/2142 -->

![Correction d’un problème ](../assets/fix.svg) Résolution d’un problème pour effacer correctement les réservations et mettre à jour les quantités de produits après avoir émis un avis de crédit pour une commande non expédiée. Lorsque vous sélectionnez l’option <!-- https://github.com/magento/inventory/pull/2179 -->

![ Problème résolu ](../assets/fix.svg) Problème résolu afin d’enregistrer correctement la quantité pour les enfants de produits configurables lors de la saisie de quantités lors de la création du produit. <!-- https://github.com/magento/inventory/pull/2158 -->

Les nouveaux modules pour [!DNL Inventory Management] 1.1.2 Beta incluent :

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![Nouveau](../assets/new.svg) **Ajout d’un point de terminaison de transfert de stock partiel en bloc** - Les points de terminaison de transfert en masse actuels déplacent toutes les quantités attribuées d’une origine vers une source de destination. Le nouveau point d’entrée `/rest/V1/inventory/bulk-partial-source-transfer` permet aux marchands de transférer le stock partiel de la source vers la source en tant qu’opération en bloc. Pour transférer une quantité spécifique, saisissez une requête sur le point de terminaison avec `sku`, `qty`, `origin_source_code` et `destination_source_code`. Les transferts vérifient que la source est affectée à `sku`, qu’il existe suffisamment de quantité pour le transfert, etc. Voir [Actions en masse d’inventaire](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"} dans la documentation de l’API REST. <!-- https://github.com/magento/inventory/pull/2117 -->

![New](../assets/new.svg) **Ajout de l’interface de ligne de commande de réservation** - Les nouvelles commandes vous donnent des options pour détecter et résoudre les incohérences de réservation. À mesure que les commandes envoient et changent de statut, [!DNL Inventory Management] génère les réservations initiales et les mises à jour par le biais de réservations de compensation. Ces commandes renvoient une liste des incohérences détectées par l’ID de commande, le SKU et l’ID de stock et créent des réservations à résoudre. Pour plus d’informations, voir la [référence de ligne de commande](cli.md) . <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![Nouveau](../assets/new.svg) **Amélioration des performances des sources et des options de l’ASS** - Le tri et la sélection de sources lors de l’expédition ont causé une dégradation des performances pour les stocks avec un grand nombre de sources. Cette version offre des performances considérablement améliorées pour répertorier et trier les sources disponibles lors de l’examen et de la sélection d’options SSA dans les envois. <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![Nouveau](../assets/new.svg) **Ajout de la prise en charge de GraphQL pour Inventory management** - Cette version installe un nouveau module `magento/module-inventory-graph-ql`. Les [attributs ProductInterface](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"} de GraphQL incluent désormais les attributs `only_x_left_in_stock` et `stock_status` pour la prise en charge de [!DNL Inventory Management]. <!-- https://github.com/magento/inventory/pull/2124 -->

![Nouveau](../assets/new.svg) **Interface utilisateur simplifiée pour les sources affectées** - Le tableau Sources affectées dans les pages de produit offre un contenu simplifié pour des mises à jour plus simples et des performances accrues lors de l’affichage de nombreuses sources. Toutes les sources sont répertoriées par nom de source (survolez `source_code` avec la souris).

![Nouveau](../assets/new.svg) **Export Aggregated Stock Service** - Cette version fournit un nouveau service de stock agrégé d’exportation (conservant les réservations dans le système) pour prendre en charge les Sales Channel externes, tels que les publicités commerciales Amazon, eBay et Google.  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

[!DNL Inventory Management] 1.1.0 (version de module : `inventory-composer-metapackage = 1.1.0`) est pris en charge et compatible avec la version 2.3.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source. [!DNL Inventory Management] 1.1.1 est publié uniquement sous la forme d’une mise à jour de nom de package, prise en charge pour la version 2.3.1 et compatible avec la version 2.3.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![ Correction d’un problème ](../assets/fix.svg) **Ajout de la prise en charge des Elasticsearch pour les modes unique et multi-source** — Vous pouvez désormais configurer et utiliser Elasticsearch avec des stocks personnalisés. Voir [Configuration du service Elasticsearch](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html?lang=fr){target="_blank"} pour obtenir des informations sur l’installation. <!-- PR https://github.com/magento/inventory/pull/1943 -->

![Correction d’un problème ](../assets/fix.svg) Résolution de problèmes de performances avec le stock par défaut pour augmenter considérablement les performances avec de nombreuses opérations. Les améliorations améliorent les performances pour le mode source unique, le transfert du stock vers Source, les pages de catégorie de storefront et les calculs de quantité vendable.

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![ Problème résolu](../assets/fix.svg) Problèmes résolus avec l’état En rupture de stock et transfert en masse du stock vers le stock pour les produits configurables et regroupés. La sélection des produits parents et l’exécution d’actions en bloc n’ont aucune incidence sur l’état du produit. Si le produit parent était En stock, il reste En stock.

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![Nouveau](../assets/new.svg) **Algorithme de priorité des distances** — L’algorithme de priorité des distances est un nouvel algorithme de sélection Source prêt à l’emploi pour les recommandations d’expédition à distance. Cet algorithme compare l’emplacement de l’adresse de destination de livraison aux emplacements sources afin de déterminer la source la plus proche pour effectuer les envois. La distance peut être déterminée soit par la distance physique, soit par le temps passé d’un emplacement à un autre, en utilisant des données de localisation du géocode importées, soit par les directions de Google (conduite, marche ou vélo).

![Nouveau](../assets/new.svg) **Liste de quantité source étendue** — Les vendeurs avec un grand nombre de sources peuvent facilement pointer et afficher toutes les sources par produit par le biais de la grille de produits. Chaque produit affiche au moins cinq sources et quantités correspondantes. Lorsque vous pointez sur les sources, vous pouvez faire défiler la liste complète des sources et des quantités actuelles.

![Problème connu](../assets/bug.svg) Problème connu avec Magento Open Source et Adobe Commerce v2.3.1 - La migration asynchrone des données entre les sources rencontre des problèmes en raison de modifications dans les API asynchrones avec des noms de rubrique reflétant les noms de classe et de méthode PHP. Il est recommandé d’utiliser des opérations synchrones, en définissant **[!UICONTROL Run asynchronously]** sur `No`.
