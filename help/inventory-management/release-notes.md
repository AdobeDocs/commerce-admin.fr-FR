---
title: '[!DNL Inventory Management] notes de mise à jour'
description: Consultez les notes de mise à jour pour plus d’informations sur toutes les [!DNL Inventory Management] versions.
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '3361'
ht-degree: 0%

---

# [!DNL Inventory Management] notes de mise à jour

Ces notes de mise à jour décrivent les versions de [!DNL Inventory Management] et incluent :

![Nouveau](../assets/new.svg) Nouvelles fonctionnalités
![Correction d’un problème](../assets/fix.svg) Correctifs et améliorations
![Problème connu](../assets/bug.svg) Problèmes connus

[!DNL Inventory Management] est un projet spécial d’ingénierie communautaire Magento Open Source ouvert aux contributeurs. Pour participer et contribuer, voir [Projet GitHub](https://github.com/magento/inventory) référentiel et [wiki](https://github.com/magento/inventory/wiki) pour commencer. Pour discuter du projet, rejoignez le [Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) channel ([auto-inscription](https://opensource.magento.com/slack)).

[Calendrier des versions](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html){target="_blank"} pour les versions prises en charge et compatibles.

## v1.2.6

[!DNL Inventory Management] 1.2.6 (version du module : `magento/inventory-metapackage = 1.2.6`) est pris en charge avec la version 2.4.6 et compatible avec la version 2.4.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![Correction d’un problème](../assets/fix.svg) Le storefront affiche désormais les produits composites (configurables, groupés et regroupés) en tant que produits en stock lorsque les produits enfants qui ont été vendus sont réintroduits en stock. Auparavant, le storefront indiquait que le produit composite était en rupture de stock dans ces conditions. <!-- ACP2E-1106-->

![Correction d’un problème](../assets/fix.svg) Les options de produit configurables s’affichent désormais comme prévu en rupture de stock sur le storefront si l’option a été créée avec une quantité définie sur 0 et **[!UICONTROL Display out-of-stock products]** est activée. <!-- ACP2E-1148-->

![Correction d’un problème](../assets/fix.svg) Les caches de page de catégorie ne sont plus invalidés lorsque la quantité en stock change et que le produit est toujours en stock. Adobe Commerce charge désormais les pages à partir du cache au lieu de les régénérer lorsque la quantité de produits (et rien d’autre) sur la page de catégorie de storefront change. <!-- ACP2E-118-->

![Correction d’un problème](../assets/fix.svg) Le nombre de produits de la liste de catégories est désormais correct lors de l’utilisation du stock en mode source unique avec la variable **[!UICONTROL Display Out-Of-Stock Products]** activée. Adobe Commerce vérifie désormais si un produit est vendable lors du comptage. <!-- ACP2E-1033-->

![Correction d’un problème](../assets/fix.svg) Les règles de prix du panier pour la diffusion en magasin fonctionnent désormais comme prévu lorsque le stock est activé. Auparavant, les remises générées par des règles de prix de panier n’étaient pas appliquées dans ces conditions. <!-- ACP2E-1015-->

![Correction d’un problème](../assets/fix.svg) La mise à jour de l’inventaire des produits en mode planifié n’efface plus tous les caches. Auparavant, l’indexeur d’inventaire effacait tous les caches de configuration. <!-- ACP2E-1003-->

![Correction d’un problème](../assets/fix.svg) La valeur de la variable **[!UICONTROL Allow Multiple Boxes for Shipping]** pour un produit dans l’inventaire avancé est désormais enregistré comme prévu. <!-- ACP2E-992-->

![Correction d’un problème](../assets/fix.svg) Adobe Commerce émet désormais une compensation exacte après un avis de crédit de remboursement partiel pour une commande passée avec une reprise en magasin. Auparavant, une réservation incorrecte enregistrée dans la variable `inventory_reservation` tableau lorsqu’un utilisateur administrateur a créé une note de crédit sans sélectionner la variable **[!UICONTROL Return to Stock]** . <!-- ACP2E-979-->

![Correction d’un problème](../assets/fix.svg) Adobe Commerce n’affiche plus les produits configurables en rupture de stock sur le storefront lorsque l’une de ses variantes a été manuellement remise en stock dans les déploiements mettant en oeuvre un inventaire multi-source. <!-- ACP2E-952-->

![Correction d’un problème](../assets/fix.svg) Position de la colonne sur la grille de produit (**[!UICONTROL Catalog]** > **[!UICONTROL Products]**) ne revient plus à sa position précédente une fois la page rechargée dans les déploiements avec plusieurs sources d’inventaire configurées. <!-- ACP2E-925-->

![Correction d’un problème](../assets/fix.svg) La quantité d’actions est maintenant correcte après l’émission d’une note de crédit pour un produit virtuel lorsque la variable **[!UICONTROL Back to stock]** n’est pas sélectionnée. <!-- ACP2E-908-->

![Correction d’un problème](../assets/fix.svg) Vous pouvez désormais enregistrer des catégories avec tri automatique de produits et portée affectée à un stock autre que le stock par défaut. Auparavant, Adobe Commerce n’enregistrait pas la catégorie et affichait cette erreur : `Something went wrong while saving the category`. <!-- ACP2E-859-->

![Correction d’un problème](../assets/fix.svg) Le statut du stock de produit configurable est maintenant mis à jour comme prévu lors de la création du produit avec toutes les variations configurables en rupture de stock. <!-- ACP2E-813-->

![Correction d’un problème](../assets/fix.svg) L’outil d’analyse d’incohérence des réservations fonctionne désormais correctement avec les commandes partiellement expédiées qui contiennent des produits configurables, groupés et regroupés. Les types de produits composites sont maintenant analysés. Auparavant, les annulations et les remboursements n’étaient enregistrés que pour les produits parents, et non pour les articles de commande de sous-produits des produits configurables et de regroupement de lots. <!-- ACP2E-924-->

![Correction d’un problème](../assets/fix.svg) Adobe Commerce n’affiche plus d’erreur lorsqu’un utilisateur administrateur tente d’affecter 200 sources d’inventaire ou plus à un stock ou à un produit. <!-- ACP2E-1180-->

![Correction d’un problème](../assets/fix.svg) Adobe Commerce prend désormais en charge la création d’une note de crédit pour une commande à partir de laquelle un produit a été supprimé. Auparavant, les commerçants ne pouvaient pas créer d’avoir lorsque les produits avaient été supprimés de la commande après la création d’une facture. L&#39;application affichait cette erreur : `Following products with requested skus were not found: s00001`. t. <!-- ACP2E-1138-->

![Correction d’un problème](../assets/fix.svg) Les magasins sont désormais filtrés en fonction d’identifiants de magasin uniques et multiples. La variable `event` Le code d’attribut de produit a été ajouté à la liste des codes d’attribut réservés. Auparavant, le rapport Faible stock générait une exception lorsque le module Inventaire était installé. <!-- ACP2E-1017-->

![Correction d’un problème](../assets/fix.svg) Les filtres de navigation en couches fonctionnent désormais comme prévu et les produits en rupture de stock sont désormais ajoutés à la liste de produits de la catégorie storefront. La nouvelle `is_out_of_stock` l’attribut de tri utilise le mappeur de champ dynamique Elasticsearch pour la collection de produits storefront. <!-- ACP2E-748-->

![Correction d’un problème](../assets/fix.svg) L’état du stock de produit composite (regroupement, regroupé et configurable) est mis à jour comme prévu lorsque l’état du stock de produit enfant est modifié par un REST. `POST /rest/V1/inventory/source-items` appelez . <!-- ACP2E-1209-->

## v1.2.5

[!DNL Inventory Management] 1.2.5 (version du module : `magento/inventory-metapackage = 1.2.5`) est pris en charge avec la version 2.4.5 et compatible avec la version 2.4.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![Correction d’un problème](../assets/fix.svg) L’état du stock par défaut des produits groupés et groupés est désormais mis à jour comme prévu lorsqu’un commerçant crée une expédition à partir de l’administrateur. Auparavant, l’état de ces produits restait inchangé après la création d’une expédition. <!--- ACP2E-418-->

![Correction d’un problème](../assets/fix.svg) Les produits configurables sont désormais remis en stock lorsque l’une des conditions suivantes est remplie : 1. Le produit parent a au moins un enfant enregistré en stock. 2. Le produit configurable lui-même a été mis à jour et défini comme **en stock** et avaient au moins un enfant en stock. <!--- ACP2E-443-->

![Correction d’un problème](../assets/fix.svg) Les modifications du stock implémentées par le biais de l’API REST sont désormais répercutées comme prévu sur les pages des détails du produit. Le cache des produits du catalogue est maintenant nettoyé après comparaison des états des stocks actuels et précédents. Auparavant, l’omission de la fonction de rappel entraînait une évaluation incorrecte des modifications d’état du stock, qui ne déclenchaient pas le nettoyage du cache nécessaire. Par conséquent, le storefront ne reflétait pas les modifications d’inventaire. <!--- ACP2E-161-->

![Correction d’un problème](../assets/fix.svg) Les produits qui sont attribués au stock par défaut et qui étaient auparavant en rupture de stock sont désormais visibles sur le storefront après la mise à jour de l’élément source à l’aide de `/V1/inventory/source-items`. Auparavant, ce point de terminaison de l’API REST définissait le mauvais `stock_status`. <!--- ACP2E-562-->

![Correction d’un problème](../assets/fix.svg) Annulation de l’affectation des sources d’inventaire par le biais d’une action en bloc (**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**) fonctionne désormais comme prévu lorsque les sources contiennent des SKU qui sont des doublons, à l’exception d’un zéro au début (par exemple, `01234` et `1234`). Auparavant, l’application n’annulait pas l’affectation des sources d’inventaire et générait une erreur. <!--- ACP2E-2641-->

![Correction d’un problème](../assets/fix.svg) L’état du stock de produit est désormais toujours **en stock** sur le storefront lorsque des commandes en arrière-plan infinies sont activées et que le produit est affecté à un stock personnalisé, quelle que soit la quantité en arrière-plan. Auparavant, les produits étaient en rupture de stock, même lorsque les commandes antérieures étaient activées. <!--- ACP2E-664-->

![Correction d’un problème](../assets/fix.svg) Le stock de produit parent et enfant configurable est désormais mis à jour correctement une fois l’élément source mis à jour avec `POST /V1/inventory/source-items`. Une fois le produit enfant mis à jour via l’API, un nouveau module externe Inventaire pour les vérifications de stock par défaut et met à jour la quantité et l’état configurables du produit. <!--- ACP2E-442-->

![Correction d’un problème](../assets/fix.svg) Les produits groupés en rupture de stock ne sont plus répertoriés sur la page Catégorie storefront. <!--- ACP2E-2082-->

![Correction d’un problème](../assets/fix.svg) Correction du nom du module dans `CatalogInventory` `composer.json`. <!--- ACP2E-2914-->

![Correction d’un problème](../assets/fix.svg) L’état de la commande précédente est désormais correctement représenté dans l’administrateur après avoir passé une commande avec un produit de quantité nulle dans un déploiement multi-source/stock. [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![Correction d’un problème](../assets/fix.svg) Les produits groupés en rupture de stock ne s’affichent plus sur la page Catégorie storefront lorsque le produit groupé est mis à jour à partir de la section stocks. <!--- ACP2E-2012-->

![Correction d’un problème](../assets/fix.svg) Les problèmes de compatibilité avec PHP 7.4 sont résolus. <!--- AC-3192-->

![Correction d’un problème](../assets/fix.svg) Les performances des opérations d’enregistrement qui incluent des produits de lot contenant de nombreuses options (plusieurs 100) sont améliorées. Auparavant, l’enregistrement de ces produits groupés volumineux prenait plusieurs minutes et entraînait parfois des dépassements de délai dans les déploiements pour lesquels les services d’inventaire étaient activés. [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![Correction d’un problème](../assets/fix.svg) L’outil d’action en bloc de produit (**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**) fonctionne désormais comme prévu lors de l’attribution d’une source de stock à plusieurs produits lorsque les SKU sont dupliqués, à l’exception d’un noeud `0` (par exemple, `01234` et `1234`). Auparavant, une source d’inventaire était affectée à un seul produit. [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![Correction d’un problème](../assets/fix.svg) La variable `ProductInterface.only_x_left_in_stock` renvoie désormais 0 si l’inventaire est 0. Auparavant, il renvoyait la valeur null. [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![Correction d’un problème](../assets/fix.svg) Vous pouvez désormais éditer le stock par défaut à partir de l&#39;Administrateur. **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**. Auparavant, une erreur JavaScript s’affichait dans la console lorsque vous tentiez d’ajouter ou de supprimer des sources du stock par défaut, bien que vous puissiez affecter des sites web au stock par défaut. <!--- ACP2E-545-->

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-274--> Le nombre de produits de la liste de catégories est désormais correct lors de l’utilisation du mode de stock source unique avec la variable **[!UICONTROL Display Out-Of-Stock Products]** activée. Un nouveau module externe utilise désormais `AreProductsSalableInterface` et `StockConfigurationInterface` pour déterminer le nombre total de produits. Auparavant, la liste de produits de catégorie renvoyait une quantité de produits incorrecte.

![Correction d’un problème](../assets/fix.svg) <!--- ACP2E-322--> Les produits configurables sont désormais déplacés vers la dernière position de la liste de produits après la mise à jour du stock lors de la **[!UICONTROL Move out of stock to the bottom]** est activé. Une nouvelle requête de base de données personnalisée est implémentée pour annuler l’ordre de tri des index Elasticsearch, sans tenir compte de l’ordre de tri activé par l’administrateur. Auparavant, les produits configurables et leurs produits enfants n’étaient pas déplacés vers le bas de la liste lorsque ce paramètre était activé.

## v1.2.4

Inventory management 1.2.4 (version de module : `magento/inventory-metapackage = 1.2.4`) est pris en charge avec la version 2.4.4 et compatible avec la version 2.4.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![Correction d’un problème](../assets/fix.svg) Commerce affiche désormais une valeur de quantité vendable exacte pour tous les produits dans la vue Admin product list. Auparavant, il affichait une valeur vide pour la quantité vendable de produits en stock avec des SKU contenant des caractères spéciaux. <!--- MC-41936-->

![Correction d’un problème](../assets/fix.svg) Les performances des actions de panier et de passage en caisse ont été améliorées, par exemple l’ajout de produits au panier dans les déploiements avec de nombreuses sources d’inventaire (environ 10 000). <!--- MC-42570-->

![Correction d’un problème](../assets/fix.svg) La variable `bin/magento inventory:reservation:list-inconsistencies` la commande gère désormais correctement les commandes avec des envois partiels, même si les réservations sont ignorées de la base de données et que le cache a été effacé. Auparavant, lorsque cette commande était exécutée avec un cache pré-effacé, Commerce affichait l’erreur suivante : `Area code is not set`. <!--- MC-42142-->

![Correction d’un problème](../assets/fix.svg) L’indexation incrémentielle des produits enfants groupés n’entraîne plus l’indexation incorrecte des autres produits groupés lors du partage des enfants. <!--- MC-41963-->

![Correction d’un problème](../assets/fix.svg) La page de catégorie de vitrine affiche désormais le nombre de produits correct après la suppression d’un produit d’une catégorie par API. Auparavant, le nombre de produits de la page de catégorie était incorrect jusqu’à la réindexation. <!--- MC-42287-->

![Correction d’un problème](../assets/fix.svg) Les produits configurables peuvent désormais être renvoyés en stock lors de la création d’une note de crédit lorsque la variable **[!UICONTROL Manage Stock]** est désactivée. Auparavant, Commerce n’affichait pas la variable **Retour au stock** de la page de création de l’avoir de crédit lorsque cette option était désactivée. <!--- MC-42002-->

![Correction d’un problème](../assets/fix.svg) La gestion du stock de plus de 10 000 articles a été améliorée. Auparavant, les problèmes de performances empêchaient parfois les commerçants de modifier le stock dans l’administrateur avant de lancer leur site web. <!--- MC-42643-->

![Correction d’un problème](../assets/fix.svg) La variable **[!UICONTROL User Roles]** dans Admin est mise à jour afin de fournir aux administrateurs des autorisations restreintes d’accès à la configuration des méthodes de diffusion. La variable _Méthodes de livraison_ a été renommée en _[!UICONTROL Delivery methods]_, et_[!UICONTROL In-Store Pickup]_ est déplacé sous le _[!UICONTROL Delivery methods]_. [GitHub-30053](https://github.com/magento/magento2/issues/30053)  <!--- MC-41545-->

![Correction d’un problème](../assets/fix.svg) Adobe Commerce ne crée plus de réservation de produit en double après la mise à jour d’un avoir de crédit par l’API. <!--- MC-41757-->

![Correction d’un problème](../assets/fix.svg) Basculer du _[!UICONTROL Pick up in Store]_à l’onglet_[!UICONTROL Shipping]_ dans le workflow de passage en caisse ne déclenche plus d’erreur JavaScript lorsque seule la diffusion de la collecte en magasin est disponible. <!--- MC-42808-->

![Correction d’un problème](../assets/fix.svg) La quantité de produit pouvant être vendue et la quantité de produit en stock sont désormais synchronisées correctement. Auparavant, la compensation des réservations de stock n’était pas recréée pour les commandes annulées. <!--- MC-42485-->

![Correction d’un problème](../assets/fix.svg) Les performances du programme de validation sont optimisées pour empêcher l’ajout d’une nouvelle source au produit enfant d’un produit regroupé avec un type d’envoi. `Ship Together`. <!--- MC-43039-->

## 1.2.3

[!DNL Inventory Management] 1.2.3 (version du module : `magento/inventory-metapackage = 1.2.3`) est pris en charge avec la version 2.4.3 et compatible avec la version 2.4.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![Correction d’un problème](../assets/fix.svg) Correction de plusieurs problèmes liés à la visibilité du produit composite sur le front-end.

![Correction d’un problème](../assets/fix.svg) Amélioration des performances de gestion des pages de panier avec la quantité minimale requise.

![Correction d’un problème](../assets/fix.svg) Plusieurs correctifs visent à résoudre les problèmes liés à la création de sources, aux articles en rupture de stock, à l’approvisionnement en stock, au tri des sources allouées, à la diffusion en magasin et aux commandes d’inventaire.

![Correction d’un problème](../assets/fix.svg) [!DNL Commerce] prend désormais en charge les codes postaux canadiens à trois chiffres pour la livraison en magasin. Les codes à six chiffres ne sont pas pris en charge en raison des restrictions définies par `geonames.org`.

![Correction d’un problème](../assets/fix.svg) L’administrateur affiche désormais la quantité correcte de stock par défaut pour les produits désactivés sur la page **Produits** et la grille **Modifier le produit** pour les déploiements multi-magasin.

![Correction d’un problème](../assets/fix.svg) [!DNL Commerce] actualise maintenant le cache des produits de catégorie lorsqu’un produit de lot revient en stock.

## 1.2.2

[!DNL Inventory Management] 1.2.2 (version du module : `magento/inventory-metapackage = 1.2.2`) est pris en charge avec la version 2.4.2 et compatible avec la version 2.4.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![Correction d’un problème](../assets/fix.svg) Correction de plusieurs problèmes liés à la visibilité du produit composite sur le front-end.

![Correction d’un problème](../assets/fix.svg) Amélioration des performances des pages de panier lors de la mise à jour de la quantité sur B2B.

![Correction d’un problème](../assets/fix.svg) Plusieurs correctifs visent à résoudre les problèmes liés à la récupération en magasin, aux mises à jour en masse et au seuil de stock.

![Nouveau](../assets/new.svg) **Tests fonctionnels.** Ajout de nouveaux tests fonctionnels et de correctifs pour les tests existants afin de les rendre plus stables.

## 1.2.1

[!DNL Inventory Management] 1.2.1 (version du module : `magento/inventory-metapackage = 1.2.1`) est pris en charge avec la version 2.4.1 et compatible avec la version 2.4.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![Correction d’un problème](../assets/fix.svg) Correction d’un problème connu lié au `inventory_cleanup_reservations` tâche cron et résolution d’un problème lié à la fonctionnalité de récupération en magasin pour les produits en bundle. Cette mise à jour inclut également des améliorations générales pour le calcul des stocks, la prise en charge des produits en bundle et la fonctionnalité de backorder.

![Nouveau](../assets/new.svg) **Tests fonctionnels.** Nouveaux tests fonctionnels afin de fournir une couverture supplémentaire pour la fonctionnalité de prise en charge en magasin.

## 1.2.0

[!DNL Inventory Management] 1.2.0 (version du module : `magento/inventory-metapackage = 1.2.0`) est pris en charge avec la version 2.4.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![Correction d’un problème](../assets/fix.svg) De nombreux correctifs permettent de résoudre des problèmes liés à l’attribution de sources, à la prise en charge de fonctionnalités d’environnement évolutive et à la compatibilité avec PHP 7.4, MySQL 8 et PHPUNIT 9.

![Nouveau](../assets/new.svg) **Méthode de remise en magasin.** Ajout d’une option permettant aux utilisateurs de sélectionner une source à utiliser comme emplacement de récupération lors du passage en caisse. Voir [Diffusion en magasin](../stores-purchase/shipping-in-store-delivery.md) dans le _Guide d’expérience des ventes et des achats_.

![Nouveau](../assets/new.svg) **Prise en charge des produits en bundle pour le mode multi-source.** L’inventaire prend en charge tous les types de produits avec plusieurs sources.

![Nouveau](../assets/new.svg) **Réindexation asynchrone des stocks.** Ajout de la possibilité de réindexer de manière asynchrone le stock et d’améliorer les performances de plusieurs scénarios critiques.

![Nouveau](../assets/new.svg) **Interfaces en masse.** Introduction de nouvelles interfaces en bloc pour le contrôle de la salabilité : `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`, `\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`.

![Nouveau](../assets/new.svg) **Couverture accrue des tests.** Les nouvelles fonctionnalités sont couvertes par des tests automatisés, notamment une couverture étendue pour les problèmes détectés et résolus.

![Problème connu](../assets/bug.svg) **Problème connu.** L&#39;absence de `object_id` dans les métadonnées de réservations, empêche le `inventory_cleanup_reservations` la tâche cron ne fonctionne pas correctement. Ce problème a été introduit dans [magento/inventory#3046](https://github.com/magento/inventory/pull/3046).

**Solution :** Exécutez les requêtes MySQL suivantes pour nettoyer manuellement les réservations :

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6

[!DNL Inventory Management] 1.1.6 (version du module : `inventory-composer-metapackage = 1.1.6`) est pris en charge avec la version 2.3.6 et compatible avec les versions 2.3.5, 2.3.4, 2.3.3, 2.3.2, 2.3.1 et 2.3.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![Correction d’un problème](../assets/fix.svg) Correctifs afin de résoudre les problèmes liés aux commandes en arrière-plan, aux notes de crédit, à la grille de rapport de faible stock, aux correctifs liés à l’outil d’interface de ligne de commande &quot;résoudre les incohérences&quot; et aux améliorations générales.

![Nouveau](../assets/new.svg) **Réindexation asynchrone des stocks.** Ajout de la possibilité de réindexer de manière asynchrone le stock et d’améliorer les performances de plusieurs scénarios critiques.

## 1.1.5

[!DNL Inventory Management] 1.1.5 (version du module : `inventory-composer-metapackage = 1.1.5`) est pris en charge avec la version 2.3.5 et compatible avec les versions 2.3.4, 2.3.3, 2.3.2, 2.3.1 et 2.3.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code de l’Magento Open Source.

![Nouveau](../assets/new.svg) **Mettez à jour l’inventaire une fois que le SKU du produit a été modifié.** Ajout d’un nouveau paramètre de configuration pour passer au nouveau comportement : &quot;Synchroniser avec le catalogue&quot;.

![Nouveau](../assets/new.svg) **Tests fonctionnels.** Introduction de nouveaux tests fonctionnels pour éliminer l’écart de couverture des tests. Correction de plusieurs problèmes pour rendre les tests plus stables et fiables).

![Problème connu](../assets/bug.svg) Correctifs afin d’éviter les ventes excessives de produits, la visibilité des produits &quot;en rupture de stock&quot; sur le storefront, de nombreux correctifs pour la prise en charge évolutive de l’environnement et les améliorations de l’interface utilisateur.

## 1.1.4

[!DNL Inventory Management] 1.1.4 (version du module : `inventory-composer-metapackage = 1.1.4`) est pris en charge avec la version 2.3.4 et compatible avec les versions 2.3.3, 2.3.2, 2.3.1 et 2.3.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![Correction d’un problème ](../assets/fix.svg)**Amélioration des performances.** Ajout d’une logique de regroupement pour la commande d’interface de ligne de commande des réservations d’inventaire afin de réduire l’utilisation de la mémoire et d’éviter les cas où le processus est bloqué sans réponse.

![Nouveau ](../assets/new.svg)**Couverture accrue des tests.** Nouveaux tests fonctionnels. Presque tous les scénarios d’inventaire manuel sont couverts par des tests automatisés.

![Problème connu](../assets/bug.svg) Nombreux correctifs destinés à résoudre les problèmes liés aux avoirs, aux produits regroupés et aux actions de masse des sources et des stocks.

## 1.1.3

[!DNL Inventory Management] 1.1.3 (version du module : `inventory-composer-metapackage = 1.1.3`) est pris en charge avec la version 2.3.3 et compatible avec les versions 2.3.2, 2.3.1 et 2.3.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![Correction d’un problème ](../assets/fix.svg)**Amélioration de l’intégration avec les fonctionnalités Adobe Commerce et B2B.** [!DNL Inventory Management] fonctionne désormais correctement avec les fonctionnalités suivantes pour les sites web qui utilisent des sources d’inventaire et des stocks autres que ceux par défaut :

- Commande par SKU (Adobe Commerce)
- Ordre rapide (B2B)
- Listes de demandes (B2B)

![Nouveau ](../assets/new.svg)**Amélioration des performances.** Les performances de navigation du catalogue Storefront ont été améliorées pour les sites web exécutant le stock et la source de stock par défaut.

![Nouveau ](../assets/new.svg)**Couverture accrue des tests.** La couverture des tests fonctionnels et d’intégration automatisés a considérablement augmenté.

## 1.1.2

[!DNL Inventory Management] 1.1.2 (version du module : `inventory-composer-metapackage = 1.1.2`) est pris en charge avec la version 2.3.2 et compatible avec les versions 2.3.1 et 2.3.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![Correction d’un problème](../assets/fix.svg) Ajout `source_code` à la réponse de la GET `/V1/shipments` Point de terminaison REST. <!-- https://github.com/magento/inventory/pull/2142 -->

![Correction d’un problème](../assets/fix.svg) Correction d’un problème afin d’effacer correctement les réservations et de mettre à jour les quantités de produits après l’émission d’une note de crédit pour une commande non expédiée. Lorsque vous sélectionnez l’option pour <!-- https://github.com/magento/inventory/pull/2179 -->

![Correction d’un problème](../assets/fix.svg) Correction d’un problème afin d’enregistrer correctement la quantité pour les enfants de produits configurables lors de la saisie de quantités lors de la création du produit. <!-- https://github.com/magento/inventory/pull/2158 -->

Nouveaux modules pour [!DNL Inventory Management] 1.1.2 La version bêta comprend :

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![Nouveau](../assets/new.svg) **Ajout d’un point de terminaison de transfert de stock partiel en bloc** - Les points de terminaison de transfert en bloc actuels déplacent toutes les quantités attribuées d’une origine vers une source de destination. La nouvelle `/rest/V1/inventory/bulk-partial-source-transfer` endpoint permet aux marchands de transférer le stock partiel de la source vers la source en tant qu’opération en bloc. Pour transférer une quantité spécifique, saisissez une requête au point de terminaison avec la variable `sku`, `qty`, `origin_source_code`, et `destination_source_code`. Les transferts vérifient que la source est affectée à la variable `sku`, il existe suffisamment de quantité pour le transfert, etc. Voir [Actions massives d’inventaire](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"} dans la documentation de l’API REST. <!-- https://github.com/magento/inventory/pull/2117 -->

![Nouveau](../assets/new.svg) **Ajout de l’interface de ligne de commande de réservation** - Les nouvelles commandes vous donnent des options pour détecter et résoudre les incohérences de réservation. Lorsque des commandes sont envoyées et que le statut est modifié, [!DNL Inventory Management] génère les réservations initiales et les mises à jour par le biais des réservations de compensation. Ces commandes renvoient une liste des incohérences détectées par l’ID de commande, le SKU et l’ID de stock et créent des réservations à résoudre. Voir [Référence de ligne de commande](cli.md) pour plus d’informations. <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![Nouveau](../assets/new.svg) **Améliorations des performances des sources et des options SSA** - Le tri et la sélection des sources lors de l&#39;expédition ont causé une dégradation des performances pour les stocks ayant un grand nombre de sources. Cette version offre des performances considérablement améliorées pour répertorier et trier les sources disponibles lors de l’examen et de la sélection d’options SSA dans les envois. <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![Nouveau](../assets/new.svg) **Ajout de la prise en charge de GraphQL pour Inventory management** - Cette version installe une nouvelle `magento/module-inventory-graph-ql` module . GraphQL [Attributs ProductInterface](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"} inclut désormais la variable `only_x_left_in_stock` et `stock_status` Attributs pour [!DNL Inventory Management] la prise en charge. <!-- https://github.com/magento/inventory/pull/2124 -->

![Nouveau](../assets/new.svg) **Interface utilisateur simplifiée pour les sources affectées** - Le tableau Sources affectées dans les pages de produit simplifie le contenu pour des mises à jour plus simples et des performances accrues lors de l’affichage de nombreuses sources. Toutes les sources sont répertoriées par nom de source (survolez la variable `source_code`).

![Nouveau](../assets/new.svg) **Exporter le service Stock agrégé** - Cette version fournit un nouveau service de stock agrégé à l’exportation (en conservant les réservations dans le système) pour prendre en charge les Sales Channel externes, tels qu’Amazon, eBay et les publicités commerciales Google.  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

[!DNL Inventory Management] 1.1.0 (version du module : `inventory-composer-metapackage = 1.1.0`) est pris en charge et compatible avec la version 2.3.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source. [!DNL Inventory Management] La version 1.1.1 est publiée uniquement sous la forme d’une mise à jour de nom de module, prise en charge pour la version 2.3.1 et compatible avec la version 2.3.0 d’Adobe Commerce, Adobe Commerce sur l’infrastructure cloud et la base de code du Magento Open Source.

![Correction d’un problème](../assets/fix.svg) **Ajout de la prise en charge des modes Elasticsearch unique et multi-source.** — Vous pouvez désormais configurer et utiliser Elasticsearch avec des stocks personnalisés. Voir [Configuration du service Elasticsearch](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html){target="_blank"} pour obtenir des informations sur l’installation. <!-- PR https://github.com/magento/inventory/pull/1943 -->

![Correction d’un problème](../assets/fix.svg) Résolution de problèmes de performances avec le stock par défaut afin d’améliorer considérablement les performances avec de nombreuses opérations. Les améliorations améliorent les performances pour le mode source unique, le transfert du stock vers la source, les pages Catégorie de vitrine et les calculs des quantités commercialisables.

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![Correction d’un problème](../assets/fix.svg) Résolution de problèmes liés à l’état En rupture de stock et au transfert en masse du stock vers le stock pour les produits configurables et regroupés. La sélection des produits parents et l’exécution d’actions en bloc n’ont aucune incidence sur l’état du produit. Si le produit parent était En stock, il reste En stock.

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![Nouveau](../assets/new.svg) **Algorithme de priorité des distances** — L’algorithme Priorité des distances est un nouvel algorithme d’usine de sélection de sources pour les recommandations d’expédition à distance. Cet algorithme compare l’emplacement de l’adresse de destination de livraison aux emplacements sources afin de déterminer la source la plus proche pour effectuer les envois. La distance peut être déterminée soit par la distance physique, soit par le temps passé d’un emplacement à un autre, en utilisant des données de localisation du géocode importées, soit par les directions de Google (conduite, marche ou vélo).

![Nouveau](../assets/new.svg) **Liste de quantité source étendue** — Les vendeurs avec un grand nombre de sources peuvent facilement survoler et afficher toutes les sources par produit via la grille de produits. Chaque produit affiche au moins cinq sources et quantités correspondantes. Lorsque vous pointez sur les sources, vous pouvez faire défiler la liste complète des sources et des quantités actuelles.

![Problème connu](../assets/bug.svg) Problème connu avec Magento Open Source et Adobe Commerce v2.3.1 - La migration asynchrone des données entre les sources rencontre des problèmes en raison des modifications des API asynchrones avec des noms de rubrique reflétant les noms de classe et de méthode PHP. Utilisation d’opérations synchrones, définition **[!UICONTROL Run asynchronously]** to `No`, est recommandé.
