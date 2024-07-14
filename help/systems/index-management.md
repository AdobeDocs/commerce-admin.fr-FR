---
title: Gestion des index
description: Découvrez la gestion des index, notamment les actions qui déclenchent la réindexation et les bonnes pratiques.
exl-id: cbb249a2-b957-44fe-bf81-df795a8fd5d1
feature: System, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1281'
ht-degree: 0%

---

# Gestion des index

Adobe Commerce et Magento Open Source réindexent automatiquement chaque fois qu’un ou plusieurs éléments changent. Les actions qui déclenchent la réindexation incluent les modifications de prix, la création de règles de prix de catalogue ou de panier, l’ajout de nouvelles catégories, etc. Pour optimiser les performances, Commerce accumule les données dans des tables spéciales à l’aide d’indexeurs. Au fur et à mesure que les données changent, les tables indexées doivent être mises à jour ou réindexées. Commerce effectue des réindex en tant que processus d’arrière-plan et votre magasin reste accessible pendant les processus.

La réindexation des données accélère le traitement et réduit le temps d’attente du client. Si, par exemple, vous faites passer le prix d’un article de 4,99 € à 3,99 €, Commerce réindexe les données afin d’afficher la modification du prix dans le magasin. Sans indexation, Commerce devra calculer le prix de chaque produit à la volée ; gérer les règles de prix du panier, le prix du lot, les remises, le niveau de prix, etc. Le chargement du prix d’un produit peut prendre plus de temps que ce que le client est prêt à attendre.

Les indexeurs peuvent être définis pour une mise à jour à l’enregistrement ou selon un calendrier. Tous les index peuvent utiliser l’une ou l’autre des options, à l’exception de la grille client qui ne prend en charge que lors de l’enregistrement. Lors de l’indexation lors de l’enregistrement, Commerce lance une réindexation lors des actions d’enregistrement. La page Gestion des index termine la mise à jour et vide le cache, le message de réindexation s’affichant dans un délai d’une minute ou deux. Lors de la réindexation sur un planning, une réindexation s’exécute selon un planning en tant que tâche cron. Un message système s’affiche si une [tâche cron](cron.md) n’est pas disponible pour mettre à jour les indexeurs qui deviennent non valides. Votre magasin reste accessible pendant les processus de réindexation.

>[!NOTE]
> Les marchands Adobe Commerce utilisant la recherche en direct, le service de catalogue ou le Recommendations de produits ont la possibilité d’utiliser un [indexeur de prix SaaS](https://experienceleague.adobe.com/docs/commerce-merchant-services/price-indexer/index.html).

Lorsqu’une réindexation est nécessaire, une notification s’affiche en haut de la page. L’index et le message s’effacent en fonction du mode de réindexation et des actions potentielles que vous effectuez. Pour plus d’informations sur l’indexation, consultez la section [Comment l’application implémente l’indexation](https://developer.adobe.com/commerce/php/development/components/indexing/#how-the-application-implements-indexing) du _Guide du développeur PHP_.

![Gestion des index - actions](./assets/index-management.png){width="700" zoomable="yes"}

- La gestion des index présente une présentation légèrement différente pour les catalogues de produits plats.
- Pour éviter des problèmes lorsque plusieurs utilisateurs administrateurs mettent à jour des objets qui déclenchent une réindexation automatique, il est recommandé de définir tous les indexeurs pour qu’ils s’exécutent selon le calendrier comme [tâches cron](cron.md). Sinon, chaque fois qu’un objet est enregistré, tout objet avec des interdépendances peut provoquer un blocage. Les symptômes d’un blocage incluent une utilisation élevée du processeur et des erreurs MySQL. Il est recommandé d’utiliser l’indexation planifiée.
- ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Par défaut, les actions d’administration, telles que la réindexation, sont consignées par le système et peuvent être visualisées dans le [rapport Journaux d’action](action-log-report.md). La journalisation des actions peut être configurée dans la [journalisation des actions d’administration](action-log.md) des paramètres d’administration avancés de votre magasin.

## Bonnes pratiques relatives à la réindexation

La réindexation et la mise en cache ont des objectifs différents dans Commerce. Les index effectuent le suivi des informations de base de données pour optimiser les performances de recherche, accélérer la récupération des données pour les vitrines, etc. [Les caches](cache-management.md) enregistrent les données chargées, les images, les formats et autres afin d’améliorer les performances de chargement et d’accès au storefront.

- En règle générale, vous souhaitez réindexer lors de la mise à jour des données dans Commerce.
- Si vous disposez d’un grand magasin ou de plusieurs magasins, vous pouvez définir des indexeurs tels que catégorie et produits sur des tâches cron planifiées en raison de la possibilité de réindexer la boucle. Vous pouvez définir la réindexation selon un planning aux heures creuses.
- Lors de la réindexation, il n’est pas nécessaire d’effectuer également un vidage du cache.
- Pour les nouvelles installations Commerce, vous devez vider le cache et réindexer.
- Le vidage des caches et la réindexation ne vident pas le cache du navigateur Web de votre ordinateur. Effacez le cache du navigateur après avoir terminé les mises à jour de votre storefront.

## Modification du mode d’index

>[!IMPORTANT]
>
>Pour les magasins qui utilisent [Adobe Commerce B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html) et qui ont défini Elasticsearch comme indexeur de texte intégral (`catalogsearch_fulltext`) : l’index de texte intégral doit être réexécuté après toute modification des autorisations en bloc ou lorsque l’indexeur d’autorisations est en mode &quot;Planifié&quot;.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Index Management]**.

1. Cochez la case correspondant à chaque indexeur que vous souhaitez modifier.

1. Définissez **[!UICONTROL Actions]** sur l’une des options suivantes :

   - `Update on Save`
   - `Update by Schedule`
   - `Invalidate index`

   >[!IMPORTANT]
   >
   >La grille client ne peut être réindexée qu’à l’aide de `Update on Save`. Cet index ne prend **_pas_** en charge `Update by Schedule`.

1. Cliquez sur **[!UICONTROL Submit]** pour appliquer la modification à chaque indexeur sélectionné.

   **Colonnes de gestion des index**

   | Colonne | Description |
   | ------ |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | [!UICONTROL Indexer] | Nom de l’indexeur. |
   | [!UICONTROL Description] | Description de l’indexeur. |
   | [!UICONTROL Mode] | Indique le mode de mise à jour actuel pour chaque indexeur. Options : <br/>**[!UICONTROL Update on Save]**- L’index est défini pour se mettre à jour chaque fois qu’une modification d’entité est enregistrée. Ces entités comprennent les produits, les catégories et les clients. Une fois l’action d’enregistrement terminée, une série d’étapes commence à capturer les modifications et à mettre à jour l’index. La page Gestion des index met à jour et vide le message de réindexation dans un délai d’une minute ou deux.<br/>**[!UICONTROL Update on Schedule]** - L’index est défini pour une mise à jour planifiée conformément à une [tâche cron](cron.md). La tâche cron inclut l’intervalle de planification de la réindexation, en écrivant des mises à jour à l’index lors de l’exécution. |
   | [!UICONTROL Schedule Status] | Affiche les mises à jour de l’état du planning. |
   | [!UICONTROL Status] | Affiche l’un des éléments suivants : <br/>**[!UICONTROL Ready]**— L’index est à jour.<br/>**[!UICONTROL Suspended]** - La réindexation est suspendue. <br/>**[!UICONTROL Processing]**- La réindexation est en cours d’exécution.<br/>**[!UICONTROL Reindex Required]** - Une modification a été apportée qui nécessite une réindexation, mais les indexeurs ne peuvent pas être mis à jour automatiquement. Vérifiez si [cron](cron.md) est disponible et configuré correctement. |
   | [!UICONTROL Updated] | Indique la date et l’heure de la dernière mise à jour d’un index. |

   {style="table-layout:auto"}

## Réindexation à l’aide de la ligne de commande

Commerce fournit des options de réindexation supplémentaires à l’aide de la ligne de commande. Pour obtenir des détails complets et des options de commande, voir [Reindex](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html#reindex){:target=&quot;blank&quot;} dans le _Guide de configuration_.

## Événements de déclencheur d’index

## Réindexation des déclencheurs

| Type d’index | Réindexation des événements |
| ---------- | ---------------- |
| [!UICONTROL Product Prices] | Ajouter un groupe de clients<br/>Modifier les paramètres de configuration |
| [!UICONTROL Flat catalog product data] | Ajouter un magasin<br/>Ajouter un groupe de magasin<br/>Ajouter, modifier ou supprimer un attribut (pour la recherche et le filtrage) |
| [!UICONTROL Flat catalog category data] | Ajouter un magasin<br/>Ajouter un groupe de magasin<br/>Ajouter, modifier ou supprimer un attribut (pour la recherche et le filtrage) |
| [!UICONTROL Catalog category/product index] | Ajouter, modifier ou supprimer des produits (uniques, en masse et importation)<br/>Changer les relations produit-catégorie<br/>Ajouter, modifier ou supprimer des catégories<br/>Ajouter ou supprimer des magasins<br/>Supprimer des groupes de magasins<br/>Supprimer des sites web |
| [!UICONTROL Catalog search index] | Ajouter, modifier ou supprimer des produits (uniques, en masse et importation)<br/>Ajouter ou supprimer des magasins<br/>Supprimer des groupes de magasins<br/>Supprimer des sites web |
| [!UICONTROL Stock status index] | Modifiez les paramètres de configuration du stock. |
| [!UICONTROL Category permissions index] | Ajouter un magasin<br/>Ajouter un groupe de magasin<br/>Ajouter, supprimer ou mettre à jour un attribut (pour la recherche et le filtrage) |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>L’utilisation d’un catalogue plat n’est plus recommandée comme bonne pratique. L’utilisation continue de cette fonctionnalité provoque une dégradation des performances et d’autres problèmes d’indexation. Pour plus d’informations, voir [Utilisation du catalogue plat](../catalog/catalog-flat.md) .

## Actions et contrôles d’index

| Action | Résultat | Contrôles |
| ------ | ------ | -------- |
| Création d&#39;un magasin, d&#39;un nouveau groupe de clients ou de toute action répertoriée dans `Actions that Cause a Full Reindex` | Réindexation complète | La réindexation complète est effectuée selon le planning déterminé par votre tâche Adobe Commerce ou Magento Open Source cron. |
| Chargement en masse d’éléments (import/export Commerce, requête SQL directe et toute autre méthode qui ajoute, modifie ou supprime directement des données) | Réindexation partielle (seuls les éléments modifiés sont réindexés) | À la fréquence déterminée par votre tâche cron Commerce. |
| Modification de la portée (par exemple, de globale à site web) | Réindexation partielle (seuls les éléments modifiés sont réindexés) | À la fréquence déterminée par votre tâche cron Commerce. |

{style="table-layout:auto"}

## Événements qui déclenchent une réindexation complète

| Indexer | Événement |
| ------- | ----- |
| [!UICONTROL Catalog Category Flat Indexer] | Créez un magasin web<br/>Créez une vue de magasin web<br/>Créez ou supprimez un attribut qui est l’un des suivants :<br/>- Recherchable ou visible dans une recherche avancée<br/>- Filtrable<br/>- Filtrable dans la recherche<br/>- Utilisé pour trier<br/>Modifiez un attribut existant comme l’un des précédents.<br/>Activer les options de vitrine de catégorie plate |
| [!UICONTROL Catalog Product Flat Indexer] | Créez un magasin web<br>Créez une vue de magasin web<br/>Créez ou supprimez un attribut qui est l’un des suivants :<br/>- Recherchable ou visible dans une recherche avancée<br>- Filtrable<br>- Filtrable dans la recherche<br/>- Utilisé pour trier <br/>Modifiez un attribut existant comme l’un des précédents.<br/>Activer les options de vitrine de catégorie plate |
| [!UICONTROL Stock status indexer] | Lorsque les _options d’inventaire catalogue_ suivantes changent dans la configuration système :<br/>`Stock Options` - Afficher les produits en rupture de stock<br/>`Product Stock Options` - Gérer les stocks |
| [!UICONTROL Price Indexer] | Ajout d’un groupe de clients<br/> Lorsque l’une des options d’inventaire catalogue suivantes change dans la configuration du système :<br/>`Stock Options` - Afficher les produits en rupture de stock<br/>`Product Stock Options` - Gérer les stocks<br/>`Price` - Portée du prix du catalogue |
| [!UICONTROL Category or Product Indexer] | Créer ou supprimer une vue de magasin<br/>Supprimer un magasin<br/>Supprimer un site web |

{style="table-layout:auto"}
