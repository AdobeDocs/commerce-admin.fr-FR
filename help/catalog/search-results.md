---
title: Résultats de la recherche
description: Découvrez comment configurer la façon dont vos produits correspondent aux critères de recherche saisis dans la zone Recherche rapide ou dans le formulaire Recherche avancée.
exl-id: c721fb3b-ee31-4d2b-b4ea-9ae2c80aa800
feature: Catalog Management, Search
source-git-commit: 4b2e1dd87a39c9be1adc49d867e44d306a969854
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 0%

---

# Résultats de la recherche

>[!NOTE]
>
>Cette page décrit les fonctionnalités de recherche standard qui peuvent différer de [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

La liste _Résultats de la recherche_ comprend tous les produits qui correspondent aux critères de recherche saisis dans la zone Recherche rapide ou dans le formulaire Recherche avancée. Chaque liste de produits du catalogue possède essentiellement les mêmes contrôles. La seule différence est que l’une est le résultat d’une requête de recherche, et l’autre différence est le résultat de [navigation](navigation.md).

Les résultats peuvent être formatés sous la forme d’une grille ou d’une liste et triés selon une sélection d’attributs. Les contrôles de pagination s’affichent s’il existe plus de produits que de produits adaptés sur la page. Utilisez ces commandes pour passer d’une page à l’autre. Le nombre d’enregistrements par page est déterminé par la configuration du champ de catalogue frontal. Pour plus d’informations, voir [Listes de produits](navigation-product-listings.md).

Avec **Elasticsearch** :

- Il n’existe pas de prise en charge prête à l’emploi de la recherche par le suffixe. Par exemple, la recherche par SKU peut ne pas renvoyer le résultat attendu si le mot-clé contient uniquement la partie de fin de la SKU.
- La recherche par préfixe (recherche par mot-clé partielle) pour les attributs de produit `name` et `sku` est prise en charge par défaut. Tous les autres attributs de produit sont recherchés par l’ensemble du mot-clé, avec la correspondance exacte.
- Les résultats de recherche des attributs de produit `name` et `sku` sont basés sur la pertinence, et non sur une correspondance exacte. Les correspondances les plus pertinentes, telles qu’un _Nom du produit_ ou _SKU_ correspondant exactement, sont répertoriées en premier. Pour rechercher une correspondance exacte, le client peut utiliser des guillemets doubles dans la requête de recherche. Par exemple, une requête de recherche `WSH12-32-Red` peut renvoyer plusieurs produits, triés selon la pertinence. Mais une requête de recherche `"WSH12-32-Red"` ne renvoie qu’un seul produit avec le **_exact_** correspondant à `sku`.

![Résultats de la recherche avec commandes de pagination](./assets/storefront-search-results-shorts.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>En raison de l’annonce de fin de prise en charge de 7 Elasticsearch pour août 2023, il est recommandé à tous les clients Adobe Commerce de migrer vers le moteur de recherche OpenSearch 2.x. Pour plus d’informations sur la migration de votre moteur de recherche lors de la mise à niveau du produit, voir [Migration vers OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) dans le _Guide de mise à niveau_.

## Mappage de mots-clés pour étendre les résultats de recherche

Cette technique utilise un attribut pour créer une association basée sur des mots-clés entre deux produits, de sorte qu’une recherche de l’un ou l’autre des produits renvoie des résultats pour les deux produits. Vous pouvez utiliser le mappage de mots-clés pour promouvoir un produit dans les résultats de recherche où il n’apparaîtrait pas autrement.

![Résultats de la recherche avec mappage de mots-clés](./assets/storefront-search-results-extended.png){width="700" zoomable="yes"}

L’exemple suivant utilise le mappage des mots-clés en fonction du SKU. Lorsque l’une ou l’autre des SKU est saisie dans la zone de recherche, les deux produits apparaissent dans les résultats. Les SKU des produits configurables suivants sont mappés, plutôt que les SKU des variantes de produits :

- Vent de Montana (MJ03)
- Chaz Kangaroo Hoodie (MH01)

### Étape 1 : création d’un attribut

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

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Attribute]**.

   L’attribut est ajouté au jeu d’attributs du produit.

### Étape 2 : mapper le premier produit

1. Sur la page des paramètres du produit, faites défiler l’écran vers le bas et développez la section _[!UICONTROL Attributes]_.
1. Dans le champ **[!UICONTROL Search Keywords]** , saisissez le SKU `MH01` à mapper à ce produit.

   Vous pouvez saisir plusieurs SKU séparés par un espace dans le champ Mots-clés de recherche . Dans cet exemple, un seul est renseigné.

   ![Section Attributs avec mot-clé de recherche](./assets/search-keywords-attribute.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.
1. Accédez à **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**et actualisez le **[!UICONTROL Page Cache]**.

### Étape 3 : mapper le deuxième produit

1. Dans la liste _[!UICONTROL Products]_, ouvrez le `Chaz Kangaroo Hoodie` (MH01) en mode d’édition.
1. Faites défiler l’écran vers le bas et développez la section **[!UICONTROL Attributes]**.
1. Dans le champ **[!UICONTROL Search Keywords]** , saisissez le SKU de l’autre produit, `MJ03`.
1. Cliquez sur **[!UICONTROL Save]**.
1. Accédez à **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**et actualisez le **[!UICONTROL Page Cache]**.

### Étape 4 : testez-la dans le storefront

1. Accédez au storefront et saisissez `MJ03` dans la zone _Recherche rapide_.
1. Vérifiez que les deux produits sont renvoyés dans la liste des résultats de recherche.

## Recherche pondérée

Les attributs de produit activés pour la recherche catalogue peuvent se voir attribuer un poids afin de leur donner une valeur plus élevée dans les résultats de recherche. Les attributs ayant un poids supérieur sont renvoyés avant les attributs ayant un poids inférieur. Par exemple, si le système comporte deux attributs, _color_ avec un poids de recherche de 3 et _description_ avec un poids de recherche de 1. Une recherche sur le mot _red_ renvoie une liste de produits avec une valeur d’attribut de couleur `red` en haut des résultats de recherche et renvoie les produits avec des descriptions qui contiennent le mot _red_ en bas des résultats de recherche. Dans cet exemple, l’attribut `color` a un poids défini plus important que l’attribut `description`.

>[!IMPORTANT]
>
>Le tri par pertinence est affecté par **_plusieurs_** critères et relations entre eux **_en même temps_**. [!UICONTROL Search Weight] n’est qu’un de ces critères. Cela signifie que parfois les attributs ayant un poids de recherche inférieur peuvent toujours avoir plus de pertinence que les attributs ayant un poids de recherche supérieur. D’autres critères peuvent inclure le nombre de correspondances dans un attribut donné, la position du terme recherché et la structure de texte globale avant et après un terme recherché.

**_Pour définir les propriétés de poids de recherche d’un attribut :_**

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Recherchez l’attribut dans la liste et ouvrez-le en mode d’édition.

1. Dans le panneau de gauche, sélectionnez **[!UICONTROL Storefront Properties]** et procédez comme suit :

   - Pour inclure l’attribut dans les requêtes de recherche, définissez **[!UICONTROL Use in Search]** sur `Yes`.

   - Pour établir la valeur de recherche de l’attribut, définissez **[!UICONTROL Search Weight]** sur un nombre compris entre 1 et 10, où `10` a la priorité la plus élevée. Si aucune valeur n’est entrée, tous les attributs correspondent par défaut à un poids de recherche de `1`.

   ![Poids de recherche](./assets/search-weight.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Attribute]**.
