---
title: Gestion des index
description: Découvrez la gestion des index, y compris les actions qui déclenchent la réindexation et les bonnes pratiques.
exl-id: cbb249a2-b957-44fe-bf81-df795a8fd5d1
feature: System, Configuration
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '1279'
ht-degree: 0%

---

# Gestion des index

Adobe Commerce et Magento Open Source se réindexent automatiquement chaque fois qu’un ou plusieurs éléments sont modifiés. Les actions qui déclenchent la réindexation incluent les modifications de prix, la création de règles de prix de catalogue ou de panier, l’ajout de nouvelles catégories, etc. Pour optimiser les performances, Commerce accumule les données dans des tables spéciales à l’aide d’indexeurs. À mesure que les données changent, les tables indexées doivent être mises à jour ou réindexées. Commerce se réindexe en tant que processus en arrière-plan et votre boutique reste accessible pendant les processus.

La réindexation des données accélère le traitement et réduit le temps d’attente du client. Par exemple, si vous modifiez le prix d’un article de 4,99 $ à 3,99 $, Commerce réindexe les données pour afficher le changement de prix dans le magasin. Sans indexation, Commerce devrait calculer le prix de chaque produit à la volée ; gérer les règles de prix des paniers, les prix des bundles, les remises, les prix de niveau, etc. Le chargement du prix d’un produit peut prendre plus de temps que le client n’est prêt à attendre.

Les indexeurs peuvent être définis pour se mettre à jour à l’enregistrement ou selon le calendrier. Tous les index peuvent utiliser l’une de ces options, à l’exception de la grille client qui ne prend en charge que lors de l’enregistrement. Lors de l’indexation lors de l’enregistrement, Commerce lance une réindexation sur les actions d’enregistrement. La page Gestion des index termine la mise à jour et vide le cache, le message de réindexation s’affichant dans une minute ou deux. Lors d’une réindexation selon un planning, une réindexation s’exécute selon un planning sous la forme d’une tâche cron. Un message système s’affiche si une [tâche cron](cron.md) n’est pas disponible pour mettre à jour les indexeurs qui deviennent non valides. Votre boutique reste accessible pendant les processus de réindexation.

>[!NOTE]
> Les commerçants Adobe Commerce qui utilisent Live Search, Catalog Service ou Product Recommendations ont la possibilité d’utiliser un indexeur de prix [SaaS](https://experienceleague.adobe.com/docs/commerce/price-indexer/index.html).

Lorsqu’une réindexation est nécessaire, une notification s’affiche en haut de la page. L’index et le message sont effacés en fonction du mode de réindexation et des actions potentielles que vous effectuez. Pour plus d’informations sur l’indexation , consultez le [Comment l’application implémente l’indexation](https://developer.adobe.com/commerce/php/development/components/indexing/#how-the-application-implements-indexing) dans le _Guide de développement de PHP_.

![Gestion des index - actions](./assets/index-management.png){width="700" zoomable="yes"}

- La gestion des index présente une présentation légèrement différente pour les catalogues de produits plats.
- Pour éviter des problèmes lorsque plusieurs utilisateurs administrateurs mettent à jour des objets qui déclenchent une réindexation automatique, il est recommandé de définir tous les indexeurs pour qu’ils s’exécutent selon le calendrier en tant que [ tâches cron ](cron.md). Dans le cas contraire, chaque fois qu’un objet est enregistré, tout objet ayant des interdépendances peut entraîner un blocage. Les symptômes d’un blocage incluent une utilisation élevée de CPU et des erreurs MySQL. Il est recommandé d’utiliser l’indexation planifiée.
- ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Par défaut, les actions d’administration, telles que la réindexation, sont consignées par le système et peuvent être consultées dans le [rapport des journaux d’actions](action-log-report.md). La journalisation des actions peut être configurée dans l’[Journalisation des actions d’administration](action-log.md) dans les paramètres d’administration avancés de votre boutique.

## Bonnes pratiques relatives à la réindexation

La réindexation et la mise en cache ont des objectifs différents dans Commerce. Les index effectuent le suivi des informations de la base de données pour améliorer les performances de recherche, accélérer la récupération des données pour les vitrines, etc. [Caches](cache-management.md) enregistrez les données chargées, les images, les formats, etc. pour améliorer les performances de chargement et d’accès au storefront.

- En règle générale, vous souhaitez effectuer une réindexation lors de la mise à jour des données dans Commerce.
- Si vous disposez d’un ou de plusieurs magasins, vous pouvez définir des indexeurs tels que les catégories et les produits sur des tâches cron planifiées en raison de la possibilité d’une boucle de réindexation. Vous pouvez définir la réindexation selon un calendrier en dehors des heures de pointe.
- Lors de la réindexation, vous n’avez pas besoin d’effectuer également un vidage du cache.
- Pour les nouvelles installations de Commerce, vous devez vider le cache et procéder à la réindexation.
- Le vidage des caches et la réindexation ne vident pas le cache du navigateur web de votre ordinateur. Effacez la mémoire cache du navigateur après avoir effectué les mises à jour de votre storefront.

## Modification du mode d’index

>[!IMPORTANT]
>
>Pour les magasins qui utilisent [Adobe Commerce B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=fr) et ont défini Elasticsearch comme indexeur de texte intégral (`catalogsearch_fulltext`) : l’index de texte intégral doit être réexécuté après toute modification des autorisations en bloc ou lorsque l’indexeur d’autorisations est en mode « Planifié ».

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Index Management]**.

1. Cochez la case correspondant à chaque indexeur à modifier.

1. Définissez **[!UICONTROL Actions]** sur l’une des options suivantes :

   - `Update on Save`
   - `Update by Schedule`
   - `Invalidate index`

   >[!IMPORTANT]
   >
   >La grille client ne peut être réindexée qu’à l’aide de `Update on Save`. Cet index ne prend **_pas_** en charge les `Update by Schedule`.

1. Cliquez sur **[!UICONTROL Submit]** pour appliquer la modification à chaque indexeur sélectionné.

   **Colonnes de gestion des index**

   | Colonne | Description |
   | ------ |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | [!UICONTROL Indexer] | Nom du moteur d’indexation. |
   | [!UICONTROL Description] | Description de l’indexeur. |
   | [!UICONTROL Mode] | Indique le mode de mise à jour actuel pour chaque indexeur. Options : <br/>**[!UICONTROL Update on Save]**- L’index est défini pour être mis à jour chaque fois qu’une modification d’entité est enregistrée. Ces entités comprennent les produits, les catégories et les clients. Une fois l’action d’enregistrement terminée, une série d’étapes commence à capturer les modifications et à mettre à jour l’index. La page Gestion des index met à jour et vide le message de réindexation dans une minute ou deux.<br/>**[!UICONTROL Update on Schedule]** - L’index est défini pour se mettre à jour selon le calendrier selon une [tâche cron](cron.md). La tâche cron inclut l’intervalle de planification pour la réindexation, l’écriture de mises à jour dans l’index lors de l’exécution. |
   | [!UICONTROL Schedule Status] | Affiche les mises à jour du statut du planning. |
   | [!UICONTROL Status] | Affiche l&#39;un des éléments suivants : <br/>**[!UICONTROL Ready]**— L&#39;index est à jour.<br/>**[!UICONTROL Suspended]** - La réindexation est suspendue. <br/>**[!UICONTROL Processing]**- La réindexation est en cours d’exécution.<br/>**[!UICONTROL Reindex Required]** - Une modification a été apportée qui nécessite une réindexation, mais les indexeurs ne peuvent pas être mis à jour automatiquement. Vérifiez si [cron](cron.md) est disponible et configuré correctement. |
   | [!UICONTROL Updated] | Indique la date et l’heure de la dernière mise à jour d’un index. |

   {style="table-layout:auto"}

## Réindexation à l’aide de la ligne de commande

Commerce fournit des options de réindexation supplémentaires à l’aide de la ligne de commande. Pour plus d’informations et d’options de commande, consultez [Réindexation](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html?lang=fr#reindex){:target="blank"} dans le _Guide de configuration_.

## Événements de déclenchement d’index

## Déclencheurs de réindexation

| Type d’index | Événement de réindexation |
| ---------- | ---------------- |
| [!UICONTROL Product Prices] | Ajouter un groupe de clients<br/>Modifier les paramètres de configuration |
| [!UICONTROL Flat catalog product data] | Ajouter un magasin<br/>Ajouter un groupe de magasins<br/>Ajouter, modifier ou supprimer un attribut (pour la recherche et le filtrage) |
| [!UICONTROL Flat catalog category data] | Ajouter un magasin<br/>Ajouter un groupe de magasins<br/>Ajouter, modifier ou supprimer un attribut (pour la recherche et le filtrage) |
| [!UICONTROL Catalog category/product index] | Ajouter, modifier ou supprimer des produits (uniques, en masse et d’importation)<br/>Modifier les relations produit à catégorie<br/>Ajouter, modifier ou supprimer des catégories<br/>Ajouter ou supprimer des magasins<br/>Supprimer des groupes de magasins<br/>Supprimer des sites web |
| [!UICONTROL Catalog search index] | Ajouter, modifier ou supprimer des produits (uniques, en masse et d’importation)<br/>Ajouter ou supprimer des magasins<br/>Supprimer des groupes de magasins<br/>Supprimer des sites web |
| [!UICONTROL Stock status index] | Modifier les paramètres de configuration de l&#39;inventaire. |
| [!UICONTROL Category permissions index] | Ajouter un magasin<br/>Ajouter un groupe de magasins<br/>Ajouter, supprimer ou mettre à jour l’attribut (pour la recherche et le filtrage) |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>L’utilisation d’un catalogue plat n’est plus recommandée. L’utilisation continue de cette fonctionnalité peut entraîner une dégradation des performances et d’autres problèmes d’indexation. Pour plus d’informations, consultez la section [Utilisation d’un produit de catalogue plat](../catalog/catalog-flat.md).

## Actions et commandes d’index

| Action | Résultat | Contrôles |
| ------ | ------ | -------- |
| Création d’un magasin, d’un groupe de clients ou de toute action répertoriée dans `Actions that Cause a Full Reindex` | Réindexation complète | La réindexation complète est effectuée selon le planning déterminé par votre tâche cron Adobe Commerce ou Magento Open Source. |
| Chargement en masse d’éléments (import/export Commerce, requête SQL directe et toute autre méthode qui ajoute, modifie ou supprime directement des données) | Réindexation partielle (seuls les éléments modifiés sont réindexés) | À la fréquence déterminée par votre tâche cron Commerce. |
| Modification de la portée (par exemple, de global à site web) | Réindexation partielle (seuls les éléments modifiés sont réindexés) | À la fréquence déterminée par votre tâche cron Commerce. |

{style="table-layout:auto"}

## Événements déclenchant une réindexation complète

| Indexeur | Événement |
| ------- | ----- |
| [!UICONTROL Catalog Category Flat Indexer] | Créez un magasin web<br/>Créez un affichage de magasin web<br/>Créez ou supprimez un attribut qui est l’un des éléments suivants :<br/>- consultable ou visible dans la recherche avancée<br/>- filtrable<br/>- filtrable dans la recherche<br/>- utilisé pour le tri<br/>Modifiez un attribut existant pour qu’il corresponde à l’un des précédents.<br/>Activer les options de storefront de catégorie plate |
| [!UICONTROL Catalog Product Flat Indexer] | Créez un magasin web<br>Créez un affichage de magasin web<br/>Créez ou supprimez un attribut qui est l’un des éléments suivants :<br/>- consultable ou visible dans la recherche avancée<br>- filtrable<br>- filtrable dans la recherche<br/>- utilisé pour le tri <br/>modifiez un attribut existant pour qu’il corresponde à l’un des précédents.<br/>Activer les options de storefront de catégorie plate |
| [!UICONTROL Stock status indexer] | Lorsque les options suivantes _Inventaire des catalogues_ changent dans la configuration du système :<br/>`Stock Options` - Afficher les produits en rupture de stock<br/>`Product Stock Options` - Gérer les stocks |
| [!UICONTROL Price Indexer] | Ajout d’un groupe de clients.<br/>Lorsque l’une des options d’inventaire des catalogues suivantes change dans la configuration du système :<br/>`Stock Options` - Afficher les produits en rupture de stock<br/>`Product Stock Options` - Gérer les stocks<br/>`Price` - Périmètre du prix du catalogue |
| [!UICONTROL Category or Product Indexer] | Créer ou supprimer une vue de magasin<br/>Supprimer un magasin<br/>Supprimer un site web |

{style="table-layout:auto"}
