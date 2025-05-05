---
title: Configuration de la recherche catalogue
description: Découvrez comment configurer la recherche catalogue pour votre boutique.
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 0%

---

# Configuration de la recherche catalogue

Il existe deux variantes de la configuration de la recherche catalogue . La première méthode décrit les paramètres disponibles lors de l’installation de [Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=fr). La deuxième méthode décrit les paramètres de configuration d’Adobe Commerce natif avec [OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html?lang=fr){:target="_blank"}.

>[!NOTE]
>
>Pour les projets d’infrastructure cloud, consultez les instructions supplémentaires dans le guide [_Commerce sur les infrastructures cloud_](https://experienceleague.adobe.com/fr/docs/commerce-cloud-service/user-guide/configure/service/opensearch).

## Méthode 1 : Adobe Commerce avec [!DNL Live Search]

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en dessous.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Catalog Search]** .

   ![Recherche catalogue pour Live Search](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   Pour obtenir une liste détaillée de ces options, consultez [Adobe Commerce avec recherche en direct](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search) dans la _Référence de configuration_.

1. Pour limiter la longueur et le nombre de mots du texte de la requête de recherche, définissez une valeur pour **[!UICONTROL Minimal Query Length]** et **[!UICONTROL Maximum Query Length]**.

1. Pour limiter la quantité de résultats de recherche populaires à mettre en cache pour des réponses plus rapides, définissez une quantité de **[!UICONTROL Number of top search results to cache]**.

   La valeur par défaut est `100`. La saisie d’une valeur `0` met en cache tous les termes et résultats de recherche lorsqu’elle est effectuée une seconde fois.

1. Pour modifier le nombre maximal de lignes disponibles pour les résultats renvoyés dans la fenêtre contextuelle [storefront](https://experienceleague.adobe.com/docs/commerce/live-search/live-search-storefront/quick-tour.html?lang=fr), saisissez une autre valeur de **[!UICONTROL Autocomplete Limit]**.

   Limiter le nombre de lignes améliore les performances des recherches et réduit la taille de la liste renvoyée. La valeur par défaut est `8` lignes.

## Méthode 2 : Commerce avec OpenSearch

>[!IMPORTANT]
>
>- En raison de l’annonce de fin de prise en charge [!DNL Elasticsearch 7] d’août 2023, il est recommandé à tous les clients Adobe Commerce de migrer vers le moteur de recherche OpenSearch 2.x. Pour plus d’informations sur la migration de votre moteur de recherche pendant la mise à niveau du produit, voir [Migration vers OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html?lang=fr) dans le _Guide de mise à niveau_.
>- Dans les versions 2.4.4 et 2.4.3-p2, tous les champs libellés Elasticsearch s’appliquent également à OpenSearch. Lorsque la prise en charge d’Elasticsearch 8.x a été introduite dans la version 2.4.6, de nouveaux libellés ont été créés pour faire la distinction entre les configurations Elasticsearch et OpenSearch. Toutefois, les options de configuration pour les deux sont identiques.

### Étape 1 : Configurer les options de recherche générales

>[!NOTE]
>
>Avec OpenSearch et Elasticsearch, il n’existe aucune prise en charge prête à l’emploi de la recherche par suffixe . Par exemple, la recherche par SKU peut ne pas renvoyer le résultat attendu si le mot-clé contient uniquement la partie de fin du SKU.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en dessous.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Catalog Search]** .

   ![Paramètres du moteur de recherche](../configuration-reference/catalog/assets/catalog-search-opensearch.png){zoomable="yes"}

   Pour plus d’informations sur ces options, consultez [Adobe Commerce avec recherche native](../configuration-reference/catalog/catalog.md#adobe-commerce-with-native-search) dans la _Référence de configuration_.

1. Pour limiter la longueur et le nombre de mots du texte de la requête de recherche, définissez une valeur pour **[!UICONTROL Minimal Query Length]** et **[!UICONTROL Maximum Query Length]**.

   >[!IMPORTANT]
   >
   >La valeur définie pour cette plage minimale et maximale doit être compatible avec la plage correspondante définie dans votre configuration de moteur de recherche. Par exemple, si vous définissez ces valeurs sur `2` et `300` dans Commerce, mettez à jour les valeurs correspondantes dans votre moteur de recherche.

1. Pour limiter la quantité de résultats de recherche populaires à mettre en cache pour des réponses plus rapides, définissez une quantité de **[!UICONTROL Number of top search results to cache]**.

   La valeur par défaut est `100`. La saisie d’une valeur `0` met en cache tous les termes et résultats de recherche lorsqu’elle est effectuée une seconde fois.

1. Si vous souhaitez activer ou désactiver l’indexeur AEP du produit, définissez la **[!UICONTROL Enable EAV Indexer]** .

   Cette fonctionnalité améliore la vitesse d’indexation et limite l’utilisation de l’indexeur par les extensions tierces.

1. Pour limiter le nombre maximal de résultats de recherche à afficher pour la saisie semi-automatique de la recherche, définissez un montant pour **[!UICONTROL Autocomplete Limit]**.

   Limiter ce nombre améliore les performances des recherches et réduit la taille de la liste affichée. La valeur par défaut est `8`.

### Étape 2 : Configurer la connexion OpenSearch

>[!IMPORTANT]
>
>Les champs **[!UICONTROL Search Engine]**, **[!UICONTROL OpenSearch Server Hostname]**, **[!UICONTROL OpenSearch Server Port]**, **[!UICONTROL OpenSearch Index Prefix]**, **[!UICONTROL Enable OpenSearch HTTP Auth]** et **[!UICONTROL OpenSearch Server Timeout]** ont été configurés lors de l’installation ou de la mise à niveau de Commerce. Ces valeurs ne doivent être modifiées que lors de la mise à niveau ou de la modification d’OpenSearch.

1. Par **[!UICONTROL Search Engine]**, sélectionnez `OpenSearch`.

1. Par **[!UICONTROL OpenSearch Server Hostname]**, acceptez la valeur par défaut configurée lors de l’installation de Commerce.

1. Par **[!UICONTROL OpenSearch Server Port]**, acceptez la valeur par défaut configurée lors de l’installation de Commerce.

   Dans cet exemple, la valeur par défaut est `9200`.

1. Par **[!UICONTROL OpenSearch Index Prefix]**, saisissez un préfixe pour identifier l’index Elasticsearch.

   La valeur par défaut est `magento2`.

1. Pour utiliser l’authentification HTTP afin d’inviter un nom d’utilisateur et un mot de passe à accéder au serveur OpenSearch, définissez **[!UICONTROL Enable OpenSearch HTTP Auth]** sur `Yes`.

1. Par **[!UICONTROL OpenSearch Server Timeout]**, saisissez le nombre de secondes avant l’expiration du système.

   La valeur par défaut est `15`.

1. Pour vérifier la configuration, cliquez sur **[!UICONTROL Test Connection]**.

### Étape 3 : configuration des suggestions et des recommandations

>[!NOTE]
>
>Les suggestions et recommandations de recherche peuvent avoir une incidence sur les performances du serveur.

1. Pour proposer des recommandations, définissez **[!UICONTROL Enable Search Recommendations]** sur `Yes` et procédez comme suit :

   - Par **[!UICONTROL Search Recommendation Count]**, saisissez le nombre de recommandations à offrir.

   - Pour afficher le nombre de résultats trouvés pour chaque recommandation, définissez **[!UICONTROL Show Results Count for Each Recommendation]** sur `Yes`.

1. Définissez **[!UICONTROL Enable Search Suggestions]** sur `Yes` et procédez comme suit :

   - Par **[!UICONTROL Search Suggestions Count]**, saisissez le nombre de suggestions de recherche à proposer.

   - Pour afficher le nombre de résultats trouvés pour chaque suggestion, définissez **[!UICONTROL Show Results for Each Suggestion]** sur `Yes`.

### Étape 4 : Configurer les conditions minimales à faire correspondre

Pour contrôler le nombre minimum de termes de votre requête que les résultats de la recherche doivent correspondre pour le retour, spécifiez une valeur pour **[!UICONTROL Minimum Terms to Match]**. La spécification de cette valeur garantit une pertinence optimale des résultats pour les acheteurs. Pour obtenir la liste des valeurs acceptées, voir le paramètre [minimum_should_match](https://opensearch.org/docs/latest/query-dsl/minimum-should-match/) dans la documentation d’OpenSearch.

Cliquez ensuite sur **[!UICONTROL Save Config]**.
