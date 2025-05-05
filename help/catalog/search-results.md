---
title: Résultats de la recherche
description: Découvrez comment configurer la manière dont vos produits correspondent aux critères de recherche saisis dans la zone de recherche rapide ou le formulaire de recherche avancée.
exl-id: c721fb3b-ee31-4d2b-b4ea-9ae2c80aa800
feature: Catalog Management, Search
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 0%

---

# Résultats de la recherche

>[!NOTE]
>
>Cette page décrit les fonctionnalités de recherche standard qui peuvent être différentes de la [recherche en direct](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=fr).

La liste _Résultats de la recherche_ comprend tous les produits qui correspondent aux critères de recherche saisis dans la zone de recherche rapide ou le formulaire de recherche avancée. Chaque liste de produits du catalogue comporte essentiellement les mêmes contrôles. La seule différence est que l’une est le résultat d’une requête de recherche et l’autre est le résultat de [ navigation](navigation.md).

Les résultats peuvent être formatés sous la forme d’une grille ou d’une liste et triés en fonction d’une sélection d’attributs. Des contrôles de pagination s’affichent s’il y a plus de produits que nécessaire sur la page. Utilisez ces commandes pour passer d&#39;une page à l&#39;autre. Le nombre d’enregistrements par page est déterminé par la configuration du catalogue frontal. Pour plus d’informations, voir [Liste des produits](navigation-product-listings.md).

Avec **Elasticsearch** :

- Il n’existe aucune prise en charge prête à l’emploi pour la recherche par suffixe . Par exemple, la recherche par SKU peut ne pas renvoyer le résultat attendu si le mot-clé contient uniquement la partie de fin du SKU.
- Il existe une prise en charge prête à l’emploi de la recherche par préfixe (recherche partielle par mot-clé) pour les attributs de produit `name` et `sku` uniquement. Tous les autres attributs de produit sont recherchés par le mot-clé entier, avec la correspondance exacte.
- Les résultats de recherche pour les attributs de produit `name` et `sku` sont basés sur la pertinence, et non sur la correspondance exacte. Les correspondances les plus pertinentes, telles qu’une correspondance exacte _Nom du produit_ ou _SKU_, sont répertoriées en premier. Pour rechercher une correspondance exacte, le client peut utiliser des guillemets doubles dans la requête de recherche. Par exemple, une requête de recherche `WSH12-32-Red` peut renvoyer plusieurs produits, triés par pertinence. Cependant, une requête de recherche `"WSH12-32-Red"` renvoie un seul produit avec le `sku` correspondant **_exactement_**.

![Résultats de recherche avec contrôles de pagination](./assets/storefront-search-results-shorts.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>En raison de l’annonce de fin de prise en charge d’Elasticsearch 7 en août 2023, il est recommandé à tous les clients Adobe Commerce de migrer vers le moteur de recherche OpenSearch 2.x. Pour plus d’informations sur la migration de votre moteur de recherche pendant la mise à niveau du produit, voir [Migration vers OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html?lang=fr) dans le _Guide de mise à niveau_.

## Mappage de mots-clés pour étendre les résultats de recherche

Cette technique utilise un attribut pour créer une association par mot-clé entre deux produits afin qu’une recherche de l’un ou l’autre produit renvoie des résultats pour les deux produits. Vous pouvez utiliser le mappage de mots-clés pour promouvoir un produit dans les résultats de recherche là où il n’apparaîtrait pas autrement.

![Résultats de recherche avec mappage de mots-clés](./assets/storefront-search-results-extended.png){width="700" zoomable="yes"}

L’exemple suivant utilise le mappage de mots-clés basé sur le SKU. Lorsque l’un des SKU est saisi dans la zone de recherche, les deux produits apparaissent dans les résultats. Les SKU des produits configurables suivants sont mappés, plutôt que les SKU des variations de produit :

- Veste coupe-vent Montana (MJ03)
- Chaz Kangaroo Hoodie (MH01)

### Étape 1 : créer un attribut

1. Dans la liste _[!UICONTROL Products]_, ouvrez le `Montana Wind Jacket` (MJ03) en mode d’édition.
1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Attribute]**.
1. Sur la page _Sélectionner un attribut_, cliquez sur **[!UICONTROL Create New Attribute]**.
1. Renseignez les propriétés d’attribut comme suit :

   **[!UICONTROL Attribute Properties]**

   - [!UICONTROL Attribute Label] - `Search Keywords`
   - [!UICONTROL Catalog Input Type for Store Owner] - `Text Field`

   **[!UICONTROL Advanced Attribute Properties]**

   - [!UICONTROL Add to Column Options] - `Yes` (par défaut)
   - [!UICONTROL Use in Filter Options] - `Yes` (par défaut)

   **[!UICONTROL Storefront Properties]**

   - [!UICONTROL Use in Search] - `Yes`
   - [!UICONTROL Visible on Catalog Pages in the Storefront] - `No`
   - [!UICONTROL Used in Product Listings] - `No`

1. Cliquez ensuite sur **[!UICONTROL Save Attribute]**.

   L’attribut est ajouté au jeu d’attributs du produit.

### Étape 2 : Mapper le premier produit

1. Sur la page des paramètres du produit, faites défiler la page vers le bas et développez la section _[!UICONTROL Attributes]_.
1. Dans le champ **[!UICONTROL Search Keywords]** , saisissez le `MH01` de SKU à mapper à ce produit.

   Vous pouvez saisir plusieurs SKU séparées par un espace dans le champ Mots-clés de recherche . Dans cet exemple, un seul est saisi.

   ![Section Attributs avec mot-clé de recherche](./assets/search-keywords-attribute.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save]**.
1. Accédez à **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**&#x200B;et actualisez le **[!UICONTROL Page Cache]**.

### Étape 3 : Mapper le deuxième produit

1. Dans la liste _[!UICONTROL Products]_, ouvrez le `Chaz Kangaroo Hoodie` (MH01) en mode d&#39;édition.
1. Faites défiler vers le bas et développez la section **[!UICONTROL Attributes]** .
1. Dans le champ **[!UICONTROL Search Keywords]** , saisissez le SKU de l’autre produit, `MJ03`.
1. Cliquez sur **[!UICONTROL Save]**.
1. Accédez à **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**&#x200B;et actualisez le **[!UICONTROL Page Cache]**.

### Étape 4 : Testez-la dans le storefront

1. Accédez au storefront et saisissez `MJ03` dans la zone _Recherche rapide_.
1. Vérifiez que les deux produits sont renvoyés dans la liste des résultats de recherche.

## Recherche pondérée

Un poids peut être attribué aux attributs de produit activés pour la recherche catalogue afin de leur donner une valeur plus élevée dans les résultats de recherche. Les attributs ayant un poids supérieur sont renvoyés avant les attributs ayant un poids inférieur. Par exemple, s’il existe deux attributs dans le système, _color_ avec un poids de recherche de 3 et _description_ avec un poids de recherche de 1. Une recherche du mot _rouge_ renvoie une liste de produits avec une valeur d’attribut de couleur de `red` en haut des résultats de recherche et renvoie les produits avec des descriptions contenant le mot _rouge_ en bas des résultats de recherche. Dans cet exemple, le poids défini de l’attribut `color` est supérieur à celui de l’attribut `description`.

>[!IMPORTANT]
>
>Le tri par pertinence est affecté par **_plusieurs_** critères et relations entre eux **_en même temps_**. [!UICONTROL Search Weight] n&#39;est qu&#39;un de ces critères. Cela signifie que parfois les attributs ayant un poids de recherche inférieur peuvent toujours avoir plus de pertinence que les attributs ayant un poids de recherche supérieur. D’autres critères peuvent inclure le nombre de correspondances dans un attribut donné, la position du terme de recherche trouvé et la structure textuelle globale avant et après un terme de recherche.

**_Pour définir les propriétés de poids de recherche d’un attribut, procédez comme suit_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Recherchez l’attribut dans la liste et ouvrez-le en mode d’édition.

1. Dans le panneau de gauche, choisissez **[!UICONTROL Storefront Properties]** et procédez comme suit :

   - Pour inclure l’attribut dans les requêtes de recherche, définissez **[!UICONTROL Use in Search]** sur `Yes`.

   - Pour établir la valeur de recherche de l’attribut, définissez **[!UICONTROL Search Weight]** sur un nombre compris entre 1 et 10, où `10` a la priorité la plus élevée. Si aucune valeur n’est saisie, tous les attributs ont par défaut un poids de recherche de `1`.

   ![Rechercher poids](./assets/search-weight.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save Attribute]**.
