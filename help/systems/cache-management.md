---
title: Gestion du cache
description: Découvrez comment utiliser les outils de gestion du cache, qui permettent d’améliorer facilement les performances de votre site.
exl-id: c87f85ca-81b9-4cbf-9817-3d779397eefd
feature: Cache, System
source-git-commit: fdf04be69754d0209772d9ceb244e3808f3b61d3
workflow-type: tm+mt
source-wordcount: '1821'
ht-degree: 0%

---

# Gestion du cache

Le système de gestion du cache d’Adobe Commerce et de Magento Open Source permet d’améliorer facilement les performances de votre site. Lorsqu’un cache nécessite une actualisation, une notification s’affiche avec un lien vers la variable [!UICONTROL Cache Management] pour terminer l’actualisation.

![Enregistrement de l’attribut de produit - message de mise à jour du cache](./assets/product-attribute-save-msg-update-cache.png){width="500"}

La variable _[!UICONTROL Cache Management]_La page affiche l’état de chaque cache principal et de la balise qui lui est associée. Les grands boutons situés dans le coin supérieur droit peuvent être utilisés pour vider le cache ou le stockage du cache tout compris. Au bas de la page, des boutons supplémentaires vous permettent de vider le cache des images du produit du catalogue et le cache des images JavaScript/CSS.

>[!IMPORTANT]
>
>Lorsque les entités de catalogue sont modifiées, elles peuvent affecter d’autres pages et invalider simultanément plusieurs caches. Lorsque vous passez en revue la page de gestion du cache, vous pouvez voir des éléments non valides qui doivent être actualisés alors qu’ils étaient _**non modifié directement**_. Par exemple, cette invalidation se produit lorsque vous modifiez un produit du catalogue affecté à une catégorie ou lorsque vous modifiez une règle de produit associée.

Après avoir vidé le cache, actualisez toujours votre navigateur pour vous assurer que vous pouvez voir les fichiers les plus récents. L’effacement du cache de Commerce n’efface pas le cache de votre navigateur web. Vous devrez peut-être vider le cache du navigateur pour afficher le contenu mis à jour.

Des informations techniques supplémentaires sur la mise en cache d’Adobe Commerce sont disponibles dans la section [Présentation du cache](https://developer.adobe.com/commerce/frontend-core/guide/caching/){:target=&quot;_blank&quot;} dans la variable _Guide de développement de Commerce Frontend_.

Accédez au _[!UICONTROL Cache Management]_en effectuant l’une des opérations suivantes :

- Cliquez sur le bouton **[!UICONTROL Cache Management]** dans le message situé au-dessus de l’espace de travail.
- Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

![Gestion du cache](./assets/cache-management-invalid.png){width="700" zoomable="yes"}

## Bonnes pratiques relatives à la mise en cache

La réindexation et la mise en cache ont des objectifs différents dans Commerce. [Index](index-management.md) suivre les informations de la base de données pour augmenter les performances de recherche, récupérer plus rapidement les données pour les storefronts, etc. ; Les caches enregistrent les données chargées, les images, les formats et autres afin d’améliorer les performances de chargement et d’accès au storefront.

- Effacez toujours le cache après l’installation des extensions/modules. Vous pouvez installer une ou plusieurs extensions, puis vider le cache.
- Videz le cache après l’installation de Commerce. Pour les nouvelles installations, vous devez également réindexer.
- Videz le cache après la mise à niveau d’une version d’Open Source ou de Commerce vers une autre.
- Lors de la purge des caches, prenez en compte le type de cache et planifiez la purge en périodes creuses. Par exemple, choisissez une heure lorsque peu de clients utilisent le site, par exemple tard le soir ou tôt le matin. L’effacement des types de cache lors de la demande maximale peut augmenter la charge sur l’administrateur et entraîner la fermeture du site jusqu’à la fin de l’opération.
- When [réindexation](index-management.md), vous n’avez pas besoin de vider le cache.

## Ressources de rôle de gestion du cache

Vous pouvez affecter l’accès à des actions de maintenance du cache spécifiques aux utilisateurs par rôle, y compris des options d’affichage, de basculement et de vidage des caches. Adobe recommande d’activer les actions de vidage uniquement pour les utilisateurs de niveau administrateur. L’accès à toutes les fonctionnalités de gestion du cache peut avoir un impact sur les performances de votre vitrine.

![Ressources de rôle - Gestion du cache](./assets/permissions-role-resources-cache-management.png){width="600" zoomable="yes"}

Pour plus d’informations sur l’affectation de ressources pour accorder l’accès aux comptes d’utilisateurs administrateurs, voir [Ressources de rôle](permissions-user-roles.md#role-resources). Les ressources suivantes contrôlent l’accès aux outils de gestion du cache :

- [!UICONTROL Clean Cache Actions]

   - [!UICONTROL Flush Cache Storage]
   - [!UICONTROL Flush Magento Cache]

- [!UICONTROL Cache Type Management]

   - [!UICONTROL Toggle Cache Type]
   - [!UICONTROL Refresh Cache Type]

- [!UICONTROL Additional Cache Management]

   - [!UICONTROL Catalog Images Cache]
   - [!UICONTROL Flush Js/Css]
   - [!UICONTROL Flush Static Files]

## Actualisation de caches spécifiques

1. Pour que chaque cache soit actualisé, cochez la case au début de la ligne.

1. Définir **[!UICONTROL Actions]** to `Refresh` et cliquez sur **[!UICONTROL Submit]**.

## Effectuer une actualisation de l’action de masse

1. Pour sélectionner un groupe de caches, définissez **[!UICONTROL Mass Actions]** à l’une des options suivantes :

   - `Select All`
   - `Select Visible`

1. Cochez la case correspondant à chaque cache à actualiser.

1. Définir **[!UICONTROL Actions]** to `Refresh` et cliquez sur **[!UICONTROL Submit]**.

## Videz le cache de l’image du produit

1. Sous _[!UICONTROL Additional Cache Management]_, cliquez sur **[!UICONTROL Flush Catalog Images Cache]**pour effacer les fichiers image de produit prégénérés.

   La variable `Image cache was cleaned` s’affiche en haut de l’espace de travail.

1. Effacez le cache de votre navigateur.

## Videz le cache JavaScript/CSS

1. Sous _[!UICONTROL Additional Cache Management]_, effacez les fichiers JavaScript et CSS fusionnés en un seul fichier en cliquant sur **[!UICONTROL Flush JavaScript/CSS Cache]**.

   La variable `The JavaScript/CSS cache has been cleaned` s’affiche en haut de l’espace de travail.

1. Effacez le cache de votre navigateur.

## Purge à l’aide de la ligne de commande

Les administrateurs système et les développeurs ayant accès au serveur d’applications Commerce peuvent également gérer la configuration du cache et du cache à partir de la ligne de commande à l’aide de l’interface de ligne de commande Commerce. Voir [Gestion du cache](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/manage-cache#clean-and-flush-cache-types){:target=&quot;_blank&quot;} dans la variable _Guide de configuration_.

## Contrôles

| Contrôle | Description |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Mass Actions] | Coche la case de plusieurs caches. Options : <br/>**[!UICONTROL Select All]**— Coche la case de tous les caches.<br/>** Tout désélectionner **— Efface la case de tous les caches.<br/>**[!UICONTROL Select Visible]** — Coche la case de tous les caches visibles. <br/>**[!UICONTROL Unselect Visible]**— Efface la case à cocher de tous les caches visibles. |
| [!UICONTROL Actions] | Détermine l’action à appliquer à tous les caches sélectionnés. Options : <br/>**[!UICONTROL Enable]**— Active tous les caches sélectionnés.<br/>**[!UICONTROL Disable]** — Désactive tous les caches sélectionnés. <br/>**[!UICONTROL Refresh]**— Actualise tous les caches sélectionnés. |
| [!UICONTROL Submit] | Applique l’action à tous les caches sélectionnés. |

{style="table-layout:auto"}

### Boutons

| Bouton | Description |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Flush Magento Cache] | Supprime tous les éléments du cache Commerce par défaut (`var/cache`), en fonction de leurs balises Commerce associées. |
| [!UICONTROL Flush Cache Storage] | Supprime tous les éléments du cache, quelle que soit la balise Commerce. Si votre système utilise un autre emplacement de cache, tous les fichiers mis en cache utilisés par d’autres applications sont supprimés dans le processus. |
| [!UICONTROL Flush Catalog Images Cache] | Supprime toutes les images de catalogue automatiquement redimensionnées et filigrane stockées dans `media/catalog/product/cache`. Si les images récemment chargées ne sont pas reflétées dans le catalogue, essayez de vider le catalogue et d’actualiser votre navigateur. |
| [!UICONTROL Flush JavaScript/CSS Cache] | Supprime la copie fusionnée des fichiers JavaScript et CSS du cache. Si les modifications récentes apportées à la feuille de style ou au code JavaScript ne sont pas répercutées dans le magasin, essayez de vider le cache JavaScript/CSS et d’actualiser votre navigateur. |
| [!UICONTROL Flush Static Files Cache] | Supprime les fichiers d’affichage prétraités et les fichiers statiques. |

{style="table-layout:auto"}

### Caches

La variable [!UICONTROL Cache Management] La page répertorie les types de cache que vous pouvez gérer à partir de l’administrateur avec leur état actuel. Cette section décrit les types de cache par défaut pris en charge par Adobe Commerce. La variable _Balise de cache_ et _Identifiant du cache_ Les colonnes décrivent les valeurs utilisées dans le code de l’application Commerce :

- `cache_type_id` définit l’identifiant unique d’un type de cache.

- `%CACHE_TYPE_TAG%` définit la balise unique à utiliser dans l’application de plage de type cache.

Les développeurs et les intégrateurs de système utilisent ces valeurs pour configurer et gérer la mise en cache lors de la personnalisation ou de l’intégration à Adobe Commerce, par exemple pour le développement d’intégrations à l’aide des API GraphQL. La variable `cache type id` est également utilisé pour la gestion du cache à partir de la ligne de commande du serveur d’applications à l’aide de l’interface de ligne de commande de Commerce. Par exemple : ` bin/magento cache:status config` affiche l’état actuel du cache de configuration.

>[!NOTE]
>
>Les développeurs et les intégrateurs système peuvent personnaliser et étendre le système de gestion du cache de Commerce pour prendre en charge les modules et intégrations personnalisés. Pour plus d’informations, voir [Configuration de la mise en cache](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cache/caching-overview) dans le _Guide de configuration d’Adobe Commerce_.

<!-- prettier-ignore -->

#### Détails de la liste cache

| Cache | Description | Balise de cache | Identifiant du cache |
|-------|------------|----------|----------|
| [!UICONTROL Configuration] | Commerce collecte la configuration XML de tous les modules, la fusionne et enregistre le résultat fusionné dans le cache.<br>**[!UICONTROL System]**-  `config.xml`,`local.xml`<br>**[!UICONTROL Module]** - `config.xml`<br><br>Ce cache contient également des paramètres spécifiques au magasin stockés dans le système de fichiers et la base de données. Nettoyez ou videz ce type de cache après avoir modifié les fichiers de configuration. | `CONFIG` | `config` |
| [!UICONTROL Layouts] | Mises en page compilées, c’est-à-dire les composants de mise en page de tous les composants. Nettoyez ou videz ce type de cache après avoir modifié les fichiers de mise en page. | `LAYOUT_GENERAL_CACHE_TAG` | `layout` |
| [!UICONTROL Blocks HTML output] | Fragments de page par bloc de HTML. Nettoyez ou videz ce type de cache après avoir modifié la couche d’affichage. | `BLOCK_HTML` | `block_html` |
| [!UICONTROL Collections Data] | Fichiers de données de collecte qui stockent les résultats des requêtes de base de données. Si nécessaire, Commerce nettoie automatiquement ce cache, mais les développeurs tiers peuvent placer n’importe quelle donnée dans n’importe quel segment du cache. Nettoyez ou videz ce type de cache si votre module personnalisé utilise une logique qui entraîne des entrées de cache que Commerce ne peut pas nettoyer. | `COLLECTION_DATA` | `collections` |
| [!UICONTROL Reflections] | Efface les données de réflexion de l’interface d’API, généralement générées lors de l’exécution. | `REFLECTION` | `reflection` |
| `Database DDL operations` | Schéma de la base de données. Si nécessaire, Commerce nettoie automatiquement ce cache, mais les développeurs tiers peuvent placer n’importe quelle donnée dans n’importe quel segment du cache. Nettoyez ou videz ce type de cache après avoir apporté des modifications personnalisées au schéma de base de données. (En d’autres termes, il s’agit de mises à jour que Commerce ne s’auto-définit pas.) L’utilisation de la configuration magento est une méthode permettant de mettre automatiquement à jour le schéma de base de données.:db-schema:commande upgrade. | `DB_DDL` | `db_ddl` |
| [!UICONTROL Compiled Config] | Résultats de la compilation de code. | `COMPILED_CONFIG` | `compiled_config` |
| [!UICONTROL Webhooks Response Cache] | Met en cache les réponses aux demandes webhook. Pour plus d’informations, voir [Guide de webhooks](https://developer.adobe.com/commerce/extensibility/webhooks/release-notes/#enhancements-2) dans la documentation destinée aux développeurs Commerce. | `WEBHOOKS_RESPONSE` | `webhooks_response` |
| [!UICONTROL EAV types and attributes] | Met en cache la déclaration des types d’entité pour les métadonnées liées aux attributs de valeur d’attribut d’entité (EAV). Les attributs incluent les libellés de magasin, les liens vers le code PHP associé, le rendu des attributs, les paramètres de recherche, etc. En règle générale, vous n’avez pas besoin de nettoyer ou de vider ce type de cache. | `EAV` | `eav` |
| [!UICONTROL Customer Notification] | Notifications temporaires qui apparaissent dans l’interface utilisateur. | `CUSTOMER_NOTIFICATION` | `customer_notification` |
| [!UICONTROL GraphQL Query Resolver Results] | Met en cache les résultats des programmes de résolution de requêtes GraphQL pour les entités client, page CMS, bloc CMS et galerie de médias de produits. Conservez ce cache activé pour améliorer les performances de GraphQL. | `GRAPHQL_QUERY_RESOLVER_RESULT` | `graphql_query_resolver_result` |
| [!UICONTROL Integrations Configuration] | Fichier de configuration d’intégration. Nettoyez ou videz ce cache après avoir modifié ou ajouté des intégrations. | `INTEGRATION` | `config_integration` |
| [!UICONTROL Integrations API Configuration] | Configuration des API d’intégration compilée pour les intégrations de magasin. | `INTEGRATION_API_CONFIG` | `config_integration_api` |
| [!UICONTROL Admin UI SDK Cache] | Met en cache les personnalisations à l’administrateur. Voir [Configuration et test de l’administrateur](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/configuration/) dans le _Guide du SDK de l’interface utilisateur d’administration_. | `ADMIN_UI_SDK` | `admin_ui_sdk` |
| [!UICONTROL Page Cache] | Mise en cache complète des pages. | `FPC` | `full_page` |
| [!UICONTROL Target Rule] | Index de règle Target | `TARGET_RULE` | `target_rule` |
| [!UICONTROL Web Services Configuration] | Mise en cache de la structure de l’API Web. | `WEBSERVICE` | `config_webservice` |
| [!UICONTROL Translations] | Fichiers de traduction. | `TRANSLATE` | `translate` |

{style="table-layout:auto"}

## Mise en cache pleine page

Adobe Commerce et Magento Open Source utilisent la mise en cache de la page entière sur le serveur pour afficher rapidement les pages de catégorie, de produit et de CMS. La mise en cache de la page entière améliore le temps de réponse et réduit la charge sur le serveur. Sans mise en cache, il se peut que chaque page doive exécuter des blocs de code et récupérer des informations de la base de données. Toutefois, avec la mise en cache de la page entière activée, une page entièrement générée peut être lue directement à partir du cache.

>[!NOTE]
>
>Il est recommandé de : [Cache de vernis](https://varnish-cache.org/){:target=&quot;_blank&quot;} ne peut être utilisé que dans un environnement de production.

Le contenu mis en cache peut être utilisé pour traiter les demandes provenant de types de visites similaires. Par conséquent, les pages présentées à un visiteur occasionnel peuvent différer des pages affichées à un client. Pour la mise en cache, chaque visite est de trois types :

- `Non-sessioned` - Au cours d’une visite sans session, l’acheteur consulte les pages, mais n’interagit pas avec le magasin. Le système met en cache le contenu de chaque page vue et les diffuse à d’autres acheteurs non sessions.
- `Sessioned` - Au cours d’une visite de session, un ID de session est attribué aux acheteurs qui interagissent avec le magasin. Les interactions incluent des activités telles que la comparaison de produits ou l’ajout de produits au panier. Les pages mises en cache qui sont générées au cours de la session sont utilisées uniquement par cet acheteur au cours de la session.
- `Customer` - Les sessions client sont créées pour les clients qui se connectent et font leurs achats à l’aide de leur compte enregistré. Au cours de la session, les clients peuvent recevoir des offres spéciales, des promotions et des prix en fonction du groupe de clients qui leur est assigné.

Pour obtenir des informations techniques, voir [Configuration et utilisation du vernis](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/varnish/config-varnish.html){:target=&quot;_blank&quot;} et [Utilisation de Redis pour la page Commerce et le cache par défaut](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-pg-cache.html){:target=&quot;_blank&quot;} dans la variable _Guide de configuration_.

**_Pour configurer le cache de la page entière :_**

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Full Page Cache]** .

   ![Configuration avancée - cache de la page entière](../configuration-reference/advanced/assets/system-full-page-cache.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Caching Application]** à l’une des options suivantes :

   - `Built-in Application`
   - `Varnish Caching`

1. Pour définir le délai d’expiration du cache de la page, saisissez la variable **[!UICONTROL TTL for public content]**. (La valeur par défaut est `86400`)

1. Pour spécifier le nombre maximal de [poignées de mise en page](https://developer.adobe.com/commerce/frontend-core/guide/layouts/#layout-handles) pour traiter sur le [`{BASE-URL}/page_cache/block/esi`](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/use-varnish-esi.html) Point de terminaison HTTP, saisissez la variable **[!UICONTROL Handles param size]**. La limitation de la taille peut améliorer la sécurité et les performances. (La valeur par défaut est `100`)

1. Si vous utilisez le vernis, renseignez la variable **[!UICONTROL Varnish Configuration]** , comme suit :

   - **[!UICONTROL Access list]** - Entrez les adresses IP qui peuvent purger la configuration de vernis pour générer un fichier de configuration. Séparez plusieurs entrées par une virgule. La valeur par défaut est `localhost`.

   - **[!UICONTROL Backend host]** - Entrez l’adresse IP de l’hôte principal qui génère les fichiers de configuration. La valeur par défaut est `localhost`.

   - **[!UICONTROL Backend port]** - Identifiez le port principal utilisé pour générer les fichiers de configuration. La valeur par défaut est : `8080`.

   - **[!UICONTROL Grace period]** - Indiquez le nombre de secondes à utiliser comme période de grâce pour générer les fichiers de configuration. Voir [Configuration du vernis avancé](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/config-varnish-advanced.html) dans le _Guide de configuration_.

   - Pour exporter la configuration en tant que `varnish.vcl` , cliquez sur le bouton correspondant à la version de vernis que vous utilisez.

   ![Configuration avancée - vernis de cache pleine page](../configuration-reference/advanced/assets/system-full-page-cache-varnish.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.
