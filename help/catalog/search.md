---
title: Présentation de la recherche catalogue
description: Découvrez les outils de recherche rapide et de recherche avancée que les clients peuvent utiliser pour localiser des produits sur le storefront.
exl-id: a796fa48-212a-47c7-ab6e-98edd4d040f4
feature: Catalog Management, Search
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# Présentation de la recherche catalogue

>[!TIP]
>
>[[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) offre une expérience de recherche rapide, super pertinente et intuitive. Elle est disponible pour Adobe Commerce sans frais supplémentaires. Cette section décrit les fonctionnalités de recherche standard qui peuvent différer de [!DNL Live Search].

Les recherches montrent que les personnes qui utilisent la recherche sont plus susceptibles de faire un achat que les clients qui ne dépendent que de la navigation. En fait, selon certaines études, les personnes qui utilisent la recherche ont presque deux fois plus de chances de faire un achat.

Les sections suivantes décrivent les fonctionnalités de base de la recherche catalogue. Pour plus d’informations sur la configuration et la personnalisation des fonctionnalités de recherche de catalogue natives, voir :

- [Configuration de la recherche catalogue](search-configuration.md)
- [Résultats de la recherche](search-results.md)
- [Gestion des termes de recherche](search-terms.md)

>[!NOTE]
>
>La fonctionnalité de recherche native dans Commerce fournit des résultats de recherche de correspondance exacte. while [!DNL Live Search], un module facultatif disponible pour l’installation et l’activation dans Adobe Commerce, est implémenté différemment et le résultat n’est pas limité à la chaîne de recherche exacte. Par exemple, où dix produits sont étiquetés numériquement pour _Omega_: une recherche de `Omega 1` entraîne une correspondance unique pour _Omega 1_ avec la fonctionnalité de recherche native. Mais la même chaîne de recherche optimisée par la recherche en direct donne une correspondance pour plusieurs éléments, _Omega 1_ et _Omega 10_.

## Recherche rapide

>[!NOTE]
>
>When [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html) est installé, la zone de recherche renvoie &quot;search as you type&quot; (rechercher lorsque vous saisissez), ce qui génère une fenêtre contextuelle.

La zone de recherche dans l’en-tête de la boutique permet aux visiteurs de trouver des produits dans votre catalogue. Le texte de recherche peut être le nom complet ou partiel du produit ou tout autre mot ou expression décrivant le produit. Les termes de recherche que les utilisateurs utilisent pour trouver des produits peuvent être gérés à partir de l’administrateur.

1. Pour **[!UICONTROL Search]**, le client saisit les premières lettres de ce qu’il souhaite trouver.

   Toutes les correspondances du catalogue apparaissent ci-dessous, avec le nombre de résultats trouvés.

1. Le client appuie sur la touche Entrée ou clique sur un résultat dans la liste des produits correspondants.

   ![Rechercher](./assets/storefront-search-box.png){width="700" zoomable="yes"}

## Recherche avancée

>[!NOTE]
>
>La fonctionnalité de recherche de formulaire avancée décrite ici ne s’applique pas à [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

La recherche avancée permet aux acheteurs de rechercher le catalogue en fonction des valeurs saisies dans un formulaire. Comme le formulaire contient plusieurs champs, une seule recherche peut inclure plusieurs paramètres. Le résultat est une liste de tous les produits du catalogue qui correspondent aux critères. Un lien vers la recherche avancée se trouve dans le pied de page de votre boutique.

![Recherche avancée](./assets/storefront-search-advanced.png){width="700" zoomable="yes"}

Chaque champ du formulaire correspond à un attribut de votre catalogue de produits. Pour ajouter un champ, définissez les propriétés front-end de l’attribut sur `Include in Advanced Search`. Il est recommandé d’inclure uniquement les champs que les clients sont les plus susceptibles d’utiliser pour trouver un produit, car trop de champs ralentit la recherche.

1. Dans le pied de page du magasin, le client clique sur **[!UICONTROL Advanced Search]**.

1. Dans le _Recherche avancée_ , ajoute des valeurs complètes ou partielles dans autant de champs que nécessaire.

1. Clics **[!UICONTROL Search]** pour afficher les résultats.

   ![Résultats de la recherche](./assets/storefront-search-advanced-results-modify.png){width="700" zoomable="yes"}

1. S’il ne voit pas ce qu’il recherche dans les résultats de recherche, le client clique **[!UICONTROL Modify your search]** et tente une autre combinaison de critères.
