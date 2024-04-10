---
title: Configuration de la recherche catalogue
description: Découvrez comment configurer la recherche catalogue pour votre boutique.
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# Configuration de la recherche catalogue

Il existe deux variantes de la configuration de la recherche catalogue . La première méthode décrit les paramètres disponibles lorsque [Recherche en direct](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) est installé. La deuxième méthode décrit les paramètres de configuration d’Adobe Commerce natif avec . [Elasticsearch][1]{:target=« _blank »}.

## Méthode 1 : Adobe Commerce avec [!DNL Live Search]

1. Le _Admin_ barre latérale, accéder à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en dessous.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) le **[!UICONTROL Catalog Search]** section.

   ![Recherche catalogue pour la recherche en direct](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   Pour obtenir une liste détaillée de ces options, voir [Adobe Commerce avec recherche en direct](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search) dans le _Référence de configuration_.

1. Pour limiter la longueur et le nombre de mots du texte de la requête de recherche, définissez une valeur pour **[!UICONTROL Minimal Query Length]** et **[!UICONTROL Maximum Query Length]**.

1. Pour limiter la quantité de résultats de recherche populaires à mettre en cache pour des réponses plus rapides, définissez un montant pour **[!UICONTROL Number of top search results to cache]**.

   La valeur par défaut est `100`. Saisir une valeur de `0` met en cache tous les termes et résultats de recherche lorsqu’ils sont saisis une deuxième fois.

1. Pour modifier le nombre maximal de lignes disponibles pour les résultats renvoyés dans le [fenêtre contextuelle de storefront](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html), saisissez un autre **[!UICONTROL Autocomplete Limit]** valeur.

   Limiter le nombre de lignes améliore les performances des recherches et réduit la taille de la liste renvoyée. La valeur par défaut est `8` lignes.

## Méthode 2 : Commerce avec Elasticsearch

>[!IMPORTANT]
>
>En raison du [!DNL Elasticsearch 7] Annonce de fin de prise en charge pour août 2023. Il est recommandé à tous les clients Adobe Commerce de migrer vers le moteur de recherche OpenSearch 2.x. Pour plus d’informations sur la migration de votre moteur de recherche pendant la mise à niveau du produit, voir [Migration vers OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) dans le _Guide de mise à niveau_.

### Étape 1 : Configurer les options de recherche générales

>[!NOTE]
>
>Avec Elasticsearch, il n’existe aucune prise en charge prête à l’emploi pour la recherche par suffixe . Par exemple, la recherche par SKU peut ne pas renvoyer le résultat attendu si le mot-clé contient uniquement la partie de fin du SKU.

1. Le _Admin_ barre latérale, accéder à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en dessous.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) le **[!UICONTROL Catalog Search]** section.

   ![Paramètres de l’Elasticsearch](../configuration-reference/catalog/assets/catalog-search-elasticsearch.png){width="600" zoomable="yes"}

   Pour plus d’informations sur ces options, voir [Adobe Commerce avec Elasticsearch](../configuration-reference/catalog/catalog.md#adobe-commerce-with-elasticsearch) dans le _Référence de configuration_.

1. Pour limiter la longueur et le nombre de mots du texte de la requête de recherche, définissez une valeur pour **[!UICONTROL Minimal Query Length]** et **[!UICONTROL Maximum Query Length]**.

   >[!IMPORTANT]
   >
   >La valeur définie pour cette plage minimale et maximale doit être compatible avec la plage correspondante définie dans la configuration de votre moteur de recherche Elasticsearch. Par exemple, si vous définissez ces valeurs sur `2` et `300` dans Commerce, mettez à jour les valeurs correspondantes dans votre moteur de recherche.

1. Pour limiter la quantité de résultats de recherche populaires à mettre en cache pour des réponses plus rapides, définissez un montant pour **[!UICONTROL Number of top search results to cache]**.

   La valeur par défaut est `100`. Saisir une valeur de `0` met en cache tous les termes et résultats de recherche lorsqu’ils sont saisis une deuxième fois.

1. Si vous souhaitez activer ou désactiver l’indexeur de l’éditeur de texte enrichi, définissez la variable **[!UICONTROL Enable EAV Indexer]**.

   Cette fonctionnalité améliore la vitesse d’indexation et limite l’utilisation de l’indexeur par les extensions tierces.

1. Pour limiter le nombre maximal de résultats de recherche à afficher pour la saisie semi-automatique de la recherche, définissez un montant pour **[!UICONTROL Autocomplete Limit]**.

   Limiter ce nombre améliore les performances des recherches et réduit la taille de la liste affichée. La valeur par défaut est `8`.

### Étape 2 : configurer la connexion Elasticsearch

>[!IMPORTANT]
>
>Le **[!UICONTROL Search Engine]**, **[!UICONTROL Elasticsearch Server Hostname]**, **[!UICONTROL Elasticsearch Server Port]**, **[!UICONTROL Elasticsearch Index Prefix]**, **[!UICONTROL Enable Elasticsearch HTTP Auth]**, et **[!UICONTROL Elasticsearch Server Timeout]** Les champs ont été configurés lors de l’installation ou de la mise à niveau de Commerce. Ces valeurs ne doivent être modifiées que lors de la mise à niveau ou de la modification d’Elasticsearch.

1. Pour **[!UICONTROL Search Engine]**, acceptez la valeur par défaut `Elasticsearch 7`.

   L’Elasticsearch 7.6.x est requis pour toutes les installations de Commerce.

1. Pour **[!UICONTROL Elasticsearch Server Hostname]**, acceptez la valeur par défaut configurée lors de l’installation de Commerce.

   Dans cet exemple, la valeur par défaut est . `elasticsearch.internal`.

1. Pour **[!UICONTROL Elasticsearch Server Port]**, acceptez la valeur par défaut configurée lors de l’installation de Commerce.

   Dans cet exemple, la valeur par défaut est . `9200`.

1. Pour **[!UICONTROL Elasticsearch Index Prefix]**, saisissez un préfixe pour identifier l’index Elasticsearch.

   La valeur par défaut est `magento2`.

1. Pour utiliser l’authentification HTTP afin d’inviter un nom d’utilisateur et un mot de passe à accéder au serveur Elasticsearch, définissez **[!UICONTROL Enable Elasticsearch HTTP Auth]** vers `Yes`.

1. Pour **[!UICONTROL Elasticsearch Server Timeout]**, saisissez le nombre de secondes avant l’expiration du système.

   La valeur par défaut est `15`.

1. Pour vérifier la configuration, cliquez sur **[!UICONTROL Test Connection]**.

### Étape 3 : configuration des suggestions et des recommandations

>[!NOTE]
>
>Les suggestions et recommandations de recherche peuvent avoir une incidence sur les performances du serveur.

1. Pour proposer des recommandations, définissez **[!UICONTROL Enable Search Recommendations]** vers `Yes` et procédez comme suit :

   - Pour **[!UICONTROL Search Recommendation Count]**, saisissez le nombre de recommandations à offrir.

   - Pour afficher le nombre de résultats trouvés pour chaque recommandation, définissez **[!UICONTROL Show Results Count for Each Recommendation]** vers `Yes`.

1. Définir **[!UICONTROL Enable Search Suggestions]** vers `Yes` et procédez comme suit :

   - Pour **[!UICONTROL Search Suggestions Count]**, saisissez le nombre de suggestions de recherche à proposer.

   - Pour afficher le nombre de résultats trouvés pour chaque suggestion, définissez **[!UICONTROL Show Results for Each Suggestion]** vers `Yes`.

### Étape 4 : Configurer les conditions minimales à faire correspondre

Pour contrôler le nombre minimum de termes de votre requête que les résultats de la recherche doivent correspondre pour le retour, spécifiez une valeur pour . **[!UICONTROL Minimum Terms to Match]**. La spécification de cette valeur garantit une pertinence optimale des résultats pour les acheteurs. Pour obtenir une liste des valeurs acceptées, voir [paramètre minimum_should_match](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-minimum-should-match.html) dans la documentation de l’Elasticsearch.

Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/search/overview-search.html
