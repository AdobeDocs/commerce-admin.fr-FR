---
title: Gestion des index
description: Découvrez la gestion des index, notamment les actions qui déclenchent la réindexation et les bonnes pratiques.
exl-id: cbb249a2-b957-44fe-bf81-df795a8fd5d1
feature: System, Configuration
source-git-commit: 55b0672984ce8cdb853daf024299919beaf7ce0b
workflow-type: tm+mt
source-wordcount: '1308'
ht-degree: 0%

---

# Gestion des index

Adobe Commerce et Magento Open Source réindexent automatiquement chaque fois qu’un ou plusieurs éléments changent. Les actions qui déclenchent la réindexation incluent les modifications de prix, la création de règles de prix de catalogue ou de panier, l’ajout de nouvelles catégories, etc. Pour optimiser les performances, Commerce accumule les données dans des tables spéciales à l’aide d’indexeurs. Au fur et à mesure que les données changent, les tables indexées doivent être mises à jour ou réindexées. Commerce procède à des réindex en tant que processus d’arrière-plan et votre magasin reste accessible pendant les processus.

La réindexation des données accélère le traitement et réduit le temps d’attente du client. Si, par exemple, vous faites passer le prix d’un article de 4,99 € à 3,99 €, Commerce réindexe les données afin d’afficher la modification du prix dans le magasin. Sans indexation, Commerce devrait calculer le prix de chaque produit à la volée ; gérer les règles de prix du panier, le prix du lot, les remises, le niveau de prix, etc. Le chargement du prix d’un produit peut prendre plus de temps que ce que le client est prêt à attendre.

Les indexeurs peuvent être définis pour une mise à jour à l’enregistrement ou selon un calendrier. Tous les index peuvent utiliser l’une ou l’autre des options, à l’exception de la grille client qui ne prend en charge que lors de l’enregistrement. Lors de l’indexation à l’enregistrement, Commerce lance une réindexation sur les actions d’enregistrement. La page Gestion des index termine la mise à jour et vide le cache, le message de réindexation s’affichant dans un délai d’une minute ou deux. Lors de la réindexation sur un planning, une réindexation s’exécute selon un planning en tant que tâche cron. Un message système s’affiche si un [tâche cron](cron.md) n’est pas disponible pour mettre à jour les indexeurs qui deviennent invalides. Votre magasin reste accessible pendant les processus de réindexation.

>[!NOTE]
> Les marchands Adobe Commerce utilisant la recherche en direct, le service de catalogue ou le Recommendations de produits ont la possibilité d’utiliser une [Indexeur de prix SaaS](https://experienceleague.adobe.com/docs/commerce-merchant-services/price-indexer/index.html).

Lorsqu’une réindexation est nécessaire, une notification s’affiche en haut de la page. L’index et le message s’effacent en fonction du mode de réindexation et des actions potentielles que vous effectuez. Pour plus d’informations sur l’indexation , voir la section [Comment l’application met en oeuvre l’indexation](https://developer.adobe.com/commerce/php/development/components/indexing/#how-the-application-implements-indexing) dans le _Guide du développeur PHP_.

![Gestion des index - actions](./assets/index-management.png){width="700" zoomable="yes"}

- La gestion des index présente une présentation légèrement différente pour les catalogues de produits plats.
- Pour éviter des problèmes lorsque plusieurs utilisateurs administrateurs mettent à jour des objets qui déclenchent une réindexation automatique, il est recommandé de définir tous les indexeurs pour qu’ils s’exécutent selon le calendrier [tâches cron](cron.md). Sinon, chaque fois qu’un objet est enregistré, tout objet avec des interdépendances peut provoquer un blocage. Les symptômes d’un blocage incluent une utilisation élevée du processeur et des erreurs MySQL. Il est recommandé d’utiliser l’indexation planifiée.
- ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Par défaut, les actions de l’administrateur, telles que la réindexation, sont consignées par le système et peuvent être visualisées dans la variable [Rapport Journaux d’action](action-log-report.md). La journalisation de l’action peut être configurée dans le [Journalisation des actions d’administration](action-log.md) dans les paramètres d’administration avancés de votre boutique.

## Bonnes pratiques relatives à la réindexation

La réindexation et la mise en cache ont des objectifs différents dans Commerce. Les index effectuent le suivi des informations de base de données pour optimiser les performances de recherche, accélérer la récupération des données pour les vitrines, etc. [Caches](cache-management.md) enregistrez les données chargées, les images, les formats et autres afin d’optimiser les performances de chargement et d’accès au storefront.

- En règle générale, vous souhaitez réindexer lors de la mise à jour des données dans Commerce.
- Si vous disposez d’un grand magasin ou de plusieurs magasins, vous pouvez définir des indexeurs tels que catégorie et produits sur des tâches cron planifiées en raison de la possibilité de réindexer la boucle. Vous pouvez définir la réindexation selon un planning aux heures creuses.
- Lors de la réindexation, il n’est pas nécessaire d’effectuer également un vidage du cache.
- Pour les nouvelles installations Commerce, vous devez vider le cache et réindexer.
- Le vidage des caches et la réindexation ne vident pas le cache du navigateur Web de votre ordinateur. Effacez le cache du navigateur après avoir terminé les mises à jour de votre storefront.

## Modification du mode d’index

>[!IMPORTANT]
>
>Pour les magasins qui utilisent [B2B pour Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html) et ont défini Elasticsearch comme texte intégral (`catalogsearch_fulltext`) indexeur : l’index de texte intégral doit être réexécuté après toute modification des autorisations en bloc ou lorsque l’indexeur &quot;autorisations&quot; est en mode &quot;Planifié&quot;.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Index Management]**.

1. Cochez la case correspondant à chaque indexeur que vous souhaitez modifier.

1. Définir **[!UICONTROL Actions]** à l’une des options suivantes :

   - `Update on Save`
   - `Update by Schedule`
   - `Invalidate index`

   >[!IMPORTANT]
   >
   >La grille client ne peut être réindexée qu’à l’aide de `Update on Save`. Cet index effectue les actions suivantes : **_not_** support `Update by Schedule`.

1. Cliquez sur **[!UICONTROL Submit]** pour appliquer la modification à chaque indexeur sélectionné.

   **Colonnes de gestion des index**

   | Colonne | Description |
   | ------ | ----------- |
   | [!UICONTROL Indexer] | Nom de l’indexeur. |
   | [!UICONTROL Description] | Description de l’indexeur. |
   | [!UICONTROL Mode] | Indique le mode de mise à jour actuel pour chaque indexeur. Options : <br/>**[!UICONTROL Update on Save]**- L’index est défini pour se mettre à jour chaque fois qu’une modification d’entité est enregistrée. Ces entités comprennent les produits, les catégories et les clients. Une fois l’action d’enregistrement terminée, une série d’étapes commence à capturer les modifications et à mettre à jour l’index. La page Gestion des index met à jour et vide le message de réindexation dans un délai d’une minute ou deux.<br/>**[!UICONTROL Update on Schedule]** - L’index est défini pour une mise à jour planifiée selon une [tâche cron](cron.md). La tâche cron inclut l’intervalle de planification de la réindexation, en écrivant des mises à jour à l’index lors de l’exécution. |
   | [!UICONTROL Schedule Status] | Affiche les mises à jour de l’état du planning. |
   | [!UICONTROL Status] | Affiche l’une des options suivantes : <br/>**[!UICONTROL Ready]**— L&#39;index est à jour.<br/>**[!UICONTROL Scheduled]** - La réindexation est planifiée. <br/>**[!UICONTROL Running]**- La réindexation est en cours d’exécution.<br/>**[!UICONTROL Reindex Required]** - Une modification a été apportée qui nécessite une réindexation, mais les indexeurs ne peuvent pas être mis à jour automatiquement. Vérifiez si [cron](cron.md) est disponible et configuré correctement. |
   | [!UICONTROL Updated] | Indique la date et l’heure de la dernière mise à jour d’un index. |

   {style="table-layout:auto"}

## Réindexation à l’aide de la ligne de commande

Commerce fournit des options de réindexation supplémentaires à l’aide de la ligne de commande. Pour obtenir des détails complets et des options de commande, voir [Reindex](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html#reindex){:target=&quot;blank&quot;} dans la variable _Guide de configuration_.

## Événements de déclencheur d’index

## Réindexation des déclencheurs

| Type d’index | Réindexation des événements |
| ---------- | ---------------- |
| [!UICONTROL Product Prices] | Ajouter un groupe de clients<br/>Modification des paramètres de configuration |
| [!UICONTROL Flat catalog product data] | Ajouter un magasin<br/>Ajouter un groupe de magasin<br/>Ajouter, modifier ou supprimer un attribut (pour la recherche et le filtrage) |
| [!UICONTROL Flat catalog category data] | Ajouter un magasin<br/>Ajouter un groupe de magasin<br/>Ajouter, modifier ou supprimer un attribut (pour la recherche et le filtrage) |
| [!UICONTROL Catalog category/product index] | Ajouter, modifier ou supprimer des produits (uniques, en masse et importation)<br/>Modification des relations produit-à-catégorie<br/>Ajout, modification ou suppression de catégories<br/>Ajout ou suppression de magasins<br/>Suppression de groupes de magasin<br/>Suppression de sites web |
| [!UICONTROL Catalog search index] | Ajouter, modifier ou supprimer des produits (uniques, en masse et importation)<br/>Ajout ou suppression de magasins<br/>Suppression de groupes de magasin<br/>Suppression de sites web |
| [!UICONTROL Stock status index] | Modifiez les paramètres de configuration du stock. |
| [!UICONTROL Category permissions index] | Ajouter un magasin<br/>Ajouter un groupe de magasin<br/>Ajouter, supprimer ou mettre à jour un attribut (pour la recherche et le filtrage) |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>L’utilisation d’un catalogue plat n’est plus recommandée comme bonne pratique. L’utilisation continue de cette fonctionnalité provoque une dégradation des performances et d’autres problèmes d’indexation. Voir [Utiliser le produit Catalogue plat](../catalog/catalog-flat.md) pour plus d’informations.

## Actions et contrôles d’index

| Action | Résultat | Contrôles |
| ------ | ------ | -------- |
| Création d’un magasin, d’un nouveau groupe de clients ou de toute action répertoriée dans `Actions that Cause a Full Reindex` | Réindexation complète | La réindexation complète est effectuée selon le planning déterminé par votre tâche Adobe Commerce ou Magento Open Source cron. |
| Chargement en masse d’éléments (import/export de commerce, requête SQL directe et toute autre méthode qui ajoute, modifie ou supprime directement des données) | Réindexation partielle (seuls les éléments modifiés sont réindexés) | À la fréquence déterminée par votre tâche de cron Commerce. |
| Modification de la portée (par exemple, de globale à site web) | Réindexation partielle (seuls les éléments modifiés sont réindexés) | À la fréquence déterminée par votre tâche de cron Commerce. |

{style="table-layout:auto"}

## Événements qui déclenchent une réindexation complète

| Indexer | Événement |
| ------- | ----- |
| [!UICONTROL Catalog Category Flat Indexer] | Création d’un magasin web<br/>Création d’une vue de boutique Web<br/>Créez ou supprimez un attribut de l’une des manières suivantes :<br/>- Recherchables ou visibles dans la recherche avancée<br/>- Filtrable<br/>- Filtrable dans la recherche<br/>- Utilisé pour le tri<br/>Modifiez un attribut existant comme l’un des attributs précédents.<br/>Activation des options de vitrine de catégorie plate |
| [!UICONTROL Catalog Product Flat Indexer] | Création d’un magasin web<br>Création d’une vue de boutique Web<br/>Créez ou supprimez un attribut de l’une des manières suivantes :<br/>- Recherchables ou visibles dans la recherche avancée<br>- Filtrable<br>- Filtrable dans la recherche<br/>- Utilisé pour le tri <br/>Modifiez un attribut existant comme l’un des attributs précédents.<br/>Activation des options de vitrine de catégorie plate |
| [!UICONTROL Stock status indexer] | Lorsque la variable _Options d’inventaire catalogue_ modification de la configuration du système :<br/>`Stock Options` - Produits en rupture de stock<br/>`Product Stock Options` - Gestion des stocks |
| [!UICONTROL Price Indexer] | Ajout d’un groupe de clients<br/>Lorsque l’une des options suivantes de l’inventaire catalogue change dans la configuration du système :<br/>`Stock Options` - Produits en rupture de stock<br/>`Product Stock Options` - Gestion des stocks<br/>`Price` - Périmètre du prix du catalogue |
| [!UICONTROL Category or Product Indexer] | Création ou suppression d’une vue de magasin<br/>Suppression d’un magasin<br/>Suppression d’un site web |

{style="table-layout:auto"}
