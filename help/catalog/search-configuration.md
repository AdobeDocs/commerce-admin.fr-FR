---
title: Configuration de la recherche catalogue
description: Découvrez comment configurer la recherche catalogue pour votre magasin.
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
source-git-commit: 279f54d41264a081166cfda7d2216172ac22cd26
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---

# Configuration de la recherche catalogue

Il existe deux variantes de la configuration de recherche catalogue. La première méthode décrit les paramètres disponibles lors de l’installation de [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html). La deuxième méthode décrit les paramètres de configuration d’Adobe Commerce natif avec [OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html){:target=&quot;_blank&quot;}.

>[!NOTE]
>
>Pour les projets d’infrastructure cloud, reportez-vous à des instructions supplémentaires dans le [_Guide de Commerce sur l’infrastructure cloud_](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/opensearch).

## Méthode 1 : Adobe Commerce avec [!DNL Live Search]

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et sélectionnez **[!UICONTROL Catalog]** sous .

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Catalog Search]** .

   ![Recherche catalogue pour la recherche en direct](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   Pour obtenir une liste détaillée de ces options, voir [Adobe Commerce avec Live Search](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search) dans la _référence de configuration_.

1. Pour limiter la longueur et le nombre de mots du texte de la requête, définissez une valeur pour **[!UICONTROL Minimal Query Length]** et **[!UICONTROL Maximum Query Length]**.

1. Pour limiter la quantité de résultats de recherche populaires à mettre en cache pour des réponses plus rapides, définissez un montant pour **[!UICONTROL Number of top search results to cache]**.

   La valeur par défaut est `100`. La saisie d’une valeur de `0` met en cache tous les termes et résultats de la recherche une seconde fois.

1. Pour modifier le nombre maximal de lignes disponibles pour les résultats renvoyés dans la [storefront pop over](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html), saisissez une valeur **[!UICONTROL Autocomplete Limit]** différente.

   La limitation du nombre de lignes améliore les performances des recherches et réduit la taille de la liste renvoyée. La valeur par défaut est de `8` lignes.

## Méthode 2 : Commerce avec OpenSearch

>[!IMPORTANT]
>
>- En raison de l’annonce de fin de prise en charge [!DNL Elasticsearch 7] pour août 2023, il est recommandé à tous les clients Adobe Commerce de migrer vers le moteur de recherche OpenSearch 2.x. Pour plus d’informations sur la migration de votre moteur de recherche lors de la mise à niveau du produit, voir [Migration vers OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) dans le _Guide de mise à niveau_.
>- Dans les versions 2.4.4 et 2.4.3-p2, tous les champs intitulés Elasticsearch s’appliquent également à OpenSearch. Lorsque la prise en charge d’Elasticsearch 8.x a été introduite dans la version 2.4.6, de nouveaux libellés ont été créés pour faire la distinction entre les configurations Elasticsearch et OpenSearch. Toutefois, les options de configuration pour les deux sont identiques.

### Étape 1 : configuration des options de recherche générales

>[!NOTE]
>
>OpenSearch et Elasticsearch ne prennent pas en charge la recherche par le suffixe. Par exemple, la recherche par SKU peut ne pas renvoyer le résultat attendu si le mot-clé contient uniquement la partie de fin de la SKU.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et sélectionnez **[!UICONTROL Catalog]** sous .

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Catalog Search]** .

   ![Paramètres du moteur de recherche](../configuration-reference/catalog/assets/catalog-search-opensearch.png){zoomable="yes"}

   Pour plus d’informations sur ces options, voir [Adobe Commerce avec recherche native](../configuration-reference/catalog/catalog.md#adobe-commerce-with-native-search) dans la _référence de configuration_.

1. Pour limiter la longueur et le nombre de mots du texte de la requête, définissez une valeur pour **[!UICONTROL Minimal Query Length]** et **[!UICONTROL Maximum Query Length]**.

   >[!IMPORTANT]
   >
   >Les valeurs définies pour cette plage minimale et maximale doivent être compatibles avec la plage correspondante définie dans la configuration de votre moteur de recherche. Par exemple, si vous définissez ces valeurs sur `2` et `300` dans Commerce, mettez à jour les valeurs correspondantes dans votre moteur de recherche.

1. Pour limiter la quantité de résultats de recherche populaires à mettre en cache pour des réponses plus rapides, définissez un montant pour **[!UICONTROL Number of top search results to cache]**.

   La valeur par défaut est `100`. La saisie d’une valeur de `0` met en cache tous les termes et résultats de la recherche une seconde fois.

1. Si vous souhaitez activer ou désactiver l’indexeur EAV de produit, définissez le **[!UICONTROL Enable EAV Indexer]**.

   Cette fonctionnalité améliore la vitesse d’indexation et limite l’indexeur de l’utilisation par des extensions tierces.

1. Pour limiter le nombre maximal de résultats de recherche à afficher pour la saisie automatique de la recherche, définissez un montant pour **[!UICONTROL Autocomplete Limit]**.

   La limitation de ce montant augmente les performances des recherches et réduit la taille de la liste affichée. La valeur par défaut est `8`.

### Étape 2 : configuration de la connexion OpenSearch

>[!IMPORTANT]
>
>Les champs **[!UICONTROL Search Engine]**, **[!UICONTROL OpenSearch Server Hostname]**, **[!UICONTROL OpenSearch Server Port]**, **[!UICONTROL OpenSearch Index Prefix]**, **[!UICONTROL Enable OpenSearch HTTP Auth]** et **[!UICONTROL OpenSearch Server Timeout]** ont été configurés lors de l’installation ou de la mise à niveau de Commerce. Ces valeurs ne doivent être modifiées que lors de la mise à niveau ou de la modification d’OpenSearch.

1. Pour **[!UICONTROL Search Engine]**, sélectionnez `OpenSearch`.

1. Pour **[!UICONTROL OpenSearch Server Hostname]**, acceptez la valeur par défaut qui a été configurée lors de l’installation de Commerce.

1. Pour **[!UICONTROL OpenSearch Server Port]**, acceptez la valeur par défaut qui a été configurée lors de l’installation de Commerce.

   Dans cet exemple, la valeur par défaut est `9200`.

1. Pour **[!UICONTROL OpenSearch Index Prefix]**, saisissez un préfixe pour identifier l’index Elasticsearch.

   La valeur par défaut est `magento2`.

1. Pour utiliser l’authentification HTTP afin de demander un nom d’utilisateur et un mot de passe pour accéder au serveur OpenSearch, définissez **[!UICONTROL Enable OpenSearch HTTP Auth]** sur `Yes`.

1. Pour **[!UICONTROL OpenSearch Server Timeout]**, saisissez le nombre de secondes avant l’expiration du système.

   La valeur par défaut est `15`.

1. Pour vérifier la configuration, cliquez sur **[!UICONTROL Test Connection]**.

### Étape 3 : configurer les suggestions et recommandations

>[!NOTE]
>
>Les suggestions et recommandations de recherche peuvent avoir une incidence sur les performances du serveur.

1. Pour proposer des recommandations, définissez **[!UICONTROL Enable Search Recommendations]** sur `Yes` et procédez comme suit :

   - Pour **[!UICONTROL Search Recommendation Count]**, saisissez le nombre de recommandations à proposer.

   - Pour afficher le nombre de résultats trouvés pour chaque recommandation, définissez **[!UICONTROL Show Results Count for Each Recommendation]** sur `Yes`.

1. Définissez **[!UICONTROL Enable Search Suggestions]** sur `Yes` et procédez comme suit :

   - Pour **[!UICONTROL Search Suggestions Count]**, saisissez le nombre de suggestions de recherche à proposer.

   - Pour afficher le nombre de résultats trouvés pour chaque suggestion, définissez **[!UICONTROL Show Results for Each Suggestion]** sur `Yes`.

### Étape 4 : configuration des termes minimum à faire correspondre

Pour contrôler le nombre minimal de termes de votre requête que les résultats de recherche doivent correspondre pour le renvoi, spécifiez une valeur pour **[!UICONTROL Minimum Terms to Match]**. La spécification de cette valeur garantit une pertinence optimale des résultats pour les acheteurs. Pour obtenir une liste des valeurs acceptées, voir [paramètre minimum_should_match](https://opensearch.org/docs/latest/query-dsl/minimum-should-match/) dans la documentation OpenSearch.

Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
