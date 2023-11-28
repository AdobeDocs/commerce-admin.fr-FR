---
title: Configuration de la recherche catalogue
description: Découvrez comment configurer la recherche catalogue pour votre magasin.
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
source-git-commit: 1f84bf9ab20aeccacf56eab396b2778140964d17
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 0%

---

# Configuration de la recherche catalogue

Il existe deux variantes de la configuration de recherche catalogue. La première méthode décrit les paramètres disponibles lors de la [Recherche en direct](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) est installé. La deuxième méthode décrit les paramètres de configuration d’Adobe Commerce natif avec [Elasticsearch][1]{:target=&quot;_blank&quot;}.

## Méthode 1 : Adobe Commerce avec [!DNL Live Search]

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en-dessous.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Catalog Search]** .

   ![Recherche catalogue pour la recherche en direct](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   Pour obtenir la liste détaillée de ces options, voir [Adobe Commerce avec la recherche en direct](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search) dans le _Référence de configuration_.

1. Pour limiter la longueur et le nombre de mots du texte de la requête, définissez une valeur pour **[!UICONTROL Minimal Query Length]** et **[!UICONTROL Maximum Query Length]**.

1. Pour limiter la quantité de résultats de recherche populaires à mettre en cache pour des réponses plus rapides, définissez un montant pour **[!UICONTROL Number of top search results to cache]**.

   La valeur par défaut est `100`. Saisir la valeur de `0` met en cache tous les termes et résultats de la recherche une seconde fois.

1. Pour modifier le nombre maximal de lignes disponibles pour les résultats renvoyés, la variable [storefront](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html), saisissez un **[!UICONTROL Autocomplete Limit]** .

   La limitation du nombre de lignes améliore les performances des recherches et réduit la taille de la liste renvoyée. La valeur par défaut est `8` lignes.

## Méthode 2 : commerce avec Elasticsearch

>[!IMPORTANT]
>
>En raison de la variable [!DNL Elasticsearch 7] annonce de fin de prise en charge pour août 2023, il est recommandé à tous les clients Adobe Commerce de migrer vers le moteur de recherche OpenSearch 2.x. Pour plus d’informations sur la migration de votre moteur de recherche lors de la mise à niveau du produit, voir [Migration vers OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) dans le _Guide de mise à niveau_.

{{beta2-updates}}

### Étape 1 : configuration des options de recherche générales

>[!NOTE]
>
>Avec Elasticsearch, il n’existe pas de prise en charge prête à l’emploi de la recherche par le suffixe. Par exemple, la recherche par SKU peut ne pas renvoyer le résultat attendu si le mot-clé contient uniquement la partie de fin de la SKU.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en-dessous.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Catalog Search]** .

   ![Paramètres des Elasticsearch](../configuration-reference/catalog/assets/catalog-search-elasticsearch.png){width="600" zoomable="yes"}

   Pour plus d’informations sur ces options, voir [Adobe Commerce avec Elasticsearch](../configuration-reference/catalog/catalog.md#adobe-commerce-with-elasticsearch) dans le _Référence de configuration_.

1. Pour limiter la longueur et le nombre de mots du texte de la requête, définissez une valeur pour **[!UICONTROL Minimal Query Length]** et **[!UICONTROL Maximum Query Length]**.

   >[!IMPORTANT]
   >
   >Les valeurs définies pour cette plage minimale et maximale doivent être compatibles avec la plage correspondante définie dans la configuration de votre moteur de recherche Elasticsearch. Par exemple, si vous définissez ces valeurs sur `2` et `300` dans Commerce, mettez à jour les valeurs correspondantes dans votre moteur de recherche.

1. Pour limiter la quantité de résultats de recherche populaires à mettre en cache pour des réponses plus rapides, définissez un montant pour **[!UICONTROL Number of top search results to cache]**.

   La valeur par défaut est `100`. Saisir la valeur de `0` met en cache tous les termes et résultats de la recherche une seconde fois.

1. Si vous souhaitez activer ou désactiver l’indexeur EAV de produit, définissez **[!UICONTROL Enable EAV Indexer]**.

   Cette fonctionnalité améliore la vitesse d’indexation et limite l’indexeur de l’utilisation par des extensions tierces.

1. Pour limiter le nombre maximal de résultats de recherche à afficher pour la saisie automatique de la recherche, définissez un montant pour **[!UICONTROL Autocomplete Limit]**.

   La limitation de ce montant augmente les performances des recherches et réduit la taille de la liste affichée. La valeur par défaut est `8`.

### Étape 2 : Configuration de la connexion Elasticsearch

>[!IMPORTANT]
>
>La variable **[!UICONTROL Search Engine]**, **[!UICONTROL Elasticsearch Server Hostname]**, **[!UICONTROL Elasticsearch Server Port]**, **[!UICONTROL Elasticsearch Index Prefix]**, **[!UICONTROL Enable Elasticsearch HTTP Auth]**, et **[!UICONTROL Elasticsearch Server Timeout]** étaient configurés lors de l’installation ou de la mise à niveau de Commerce. Ces valeurs ne doivent être modifiées que lors de la mise à niveau ou de la modification d’Elasticsearch.

1. Pour **[!UICONTROL Search Engine]**, acceptez la valeur par défaut `Elasticsearch 7`.

   Elasticsearch 7.6.x est requis pour toutes les installations Commerce.

1. Pour **[!UICONTROL Elasticsearch Server Hostname]**, acceptez la valeur par défaut qui a été configurée lors de l’installation de Commerce.

   Dans cet exemple, la valeur par défaut est `elasticsearch.internal`.

1. Pour **[!UICONTROL Elasticsearch Server Port]**, acceptez la valeur par défaut qui a été configurée lors de l’installation de Commerce.

   Dans cet exemple, la valeur par défaut est `9200`.

1. Pour **[!UICONTROL Elasticsearch Index Prefix]**, saisissez un préfixe pour identifier l’index Elasticsearch.

   La valeur par défaut est `magento2`.

1. Pour utiliser l’authentification HTTP afin de demander un nom d’utilisateur et un mot de passe pour accéder au serveur Elasticsearch, définissez **[!UICONTROL Enable Elasticsearch HTTP Auth]** to `Yes`.

1. Pour **[!UICONTROL Elasticsearch Server Timeout]**, saisissez le nombre de secondes avant l’expiration du système.

   La valeur par défaut est `15`.

1. Pour vérifier la configuration, cliquez sur **[!UICONTROL Test Connection]**.

### Étape 3 : configurer les suggestions et recommandations

>[!NOTE]
>
>Les suggestions et recommandations de recherche peuvent avoir une incidence sur les performances du serveur.

1. Pour proposer des recommandations, définissez **[!UICONTROL Enable Search Recommendations]** to `Yes` et procédez comme suit :

   - Pour **[!UICONTROL Search Recommendation Count]**, saisissez le nombre de recommandations à proposer.

   - Pour afficher le nombre de résultats trouvés pour chaque recommandation, définissez **[!UICONTROL Show Results Count for Each Recommendation]** to `Yes`.

1. Définir **[!UICONTROL Enable Search Suggestions]** to `Yes` et procédez comme suit :

   - Pour **[!UICONTROL Search Suggestions Count]**, saisissez le nombre de suggestions de recherche à proposer.

   - Pour afficher le nombre de résultats trouvés pour chaque suggestion, définissez **[!UICONTROL Show Results for Each Suggestion]** to `Yes`.

### Étape 4 : configuration des termes minimum à faire correspondre

Pour contrôler le nombre minimal de termes de votre requête que les résultats de recherche doivent correspondre au retour, spécifiez une valeur pour **[!UICONTROL Minimum Terms to Match]**. La spécification de cette valeur garantit une pertinence optimale des résultats pour les acheteurs. Pour obtenir la liste des valeurs acceptées, voir [paramètre minimum_should_match](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-minimum-should-match.html) dans la documentation de l’Elasticsearch.

Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/search/overview-search.html
