---
title: Présentation de la recherche catalogue
description: Découvrez les outils de recherche rapide et de recherche avancée que les clients peuvent utiliser pour localiser les produits sur le storefront.
exl-id: a796fa48-212a-47c7-ab6e-98edd4d040f4
feature: Catalog Management, Search
TQID: https://experienceleague.adobe.com/PV3ZrkqHaUZw-2LFHCNKUeDcvJmkvFcuoR3ZxxURP54
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 541
ht-degree: 0%

---

# Présentation de la recherche catalogue

>[!TIP]
>
>[[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=fr) offre une expérience de recherche rapide, très pertinente et intuitive et est disponible gratuitement pour Adobe Commerce. Cette section décrit les fonctionnalités de recherche standard qui peuvent être différentes de [!DNL Live Search].

Les recherches montrent que les personnes qui utilisent la recherche sont plus susceptibles de faire un achat que les clients qui dépendent uniquement de la navigation. En fait, selon certaines études, les gens qui utilisent le référencement sont près de deux fois plus susceptibles de faire un achat.

Les sections suivantes décrivent les fonctionnalités de base de la recherche catalogue. Pour plus d’informations sur la configuration et la personnalisation des fonctionnalités de recherche catalogue native, voir :

- [Configuration de la recherche catalogue](search-configuration.md)
- [Résultats de la recherche](search-results.md)
- [Gestion des termes de recherche](search-terms.md)

>[!NOTE]
>
>La fonctionnalité de recherche native de Commerce fournit des résultats de recherche correspondant exactement. Bien que [!DNL Live Search], un module facultatif disponible pour l’installation et l’activation dans Adobe Commerce, soit implémenté différemment et que le résultat ne se limite pas à la chaîne de recherche exacte. Par exemple, lorsque vous avez dix produits étiquetés numériquement pour _Omega_ : une recherche de `Omega 1` donne une correspondance unique pour _Omega 1_ avec la fonctionnalité de recherche native. Mais la même chaîne de recherche optimisée par Live Search génère une correspondance pour plusieurs éléments, _Omega 1_ et _Omega 10_.

## Recherche rapide

>[!NOTE]
>
>Lorsque [[!DNL Live Search]](https://experienceleague.adobe.com/fr/docs/commerce/live-search/overview) est installé et que le widget [[!DNL Storefront Popover]](https://experienceleague.adobe.com/fr/docs/commerce/live-search/live-search-storefront/storefront-popover) est activé, la zone de recherche renvoie « rechercher au fur et à mesure que vous tapez » dans une fenêtre contextuelle.

La zone de recherche située dans l’en-tête du magasin permet aux visiteurs de trouver les produits de votre catalogue. Le texte de recherche peut être le nom complet ou partiel du produit ou tout autre mot ou expression qui décrit le produit. Les termes de recherche que les personnes utilisent pour trouver des produits peuvent être gérés à partir de l’administrateur.

1. Par **[!UICONTROL Search]**, le client saisit les premières lettres de ce qu’il souhaite trouver.

   Toutes les correspondances du catalogue s’affichent ci-dessous, avec le nombre de résultats trouvés.

1. Le client appuie sur la touche Entrée ou clique sur un résultat dans la liste des produits correspondants.

   ![Rechercher](./assets/storefront-search-box.png){width="700" zoomable="yes"}

## Recherche avancée

>[!NOTE]
>
>La fonctionnalité de recherche avancée de formulaires décrite ici ne s’applique pas aux [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=fr).

La recherche avancée permet aux acheteurs de rechercher dans le catalogue en fonction des valeurs saisies dans un formulaire. Comme le formulaire contient plusieurs champs, une seule recherche peut inclure plusieurs paramètres. Le résultat est une liste de tous les produits du catalogue qui correspondent aux critères. Un lien vers la Recherche avancée se trouve dans le pied de page de votre boutique.

![Recherche avancée](./assets/storefront-search-advanced.png){width="700" zoomable="yes"}

Chaque champ du formulaire correspond à un attribut de votre catalogue de produits. Pour ajouter un champ, définissez les propriétés frontend de l’attribut sur `Include in Advanced Search`. Il est recommandé d’inclure uniquement les champs que les clients sont les plus susceptibles d’utiliser pour trouver un produit, car un nombre trop élevé ralentit la recherche.

1. Dans le pied de page du magasin, le client clique sur **[!UICONTROL Advanced Search]**.

1. Dans le formulaire _Recherche avancée_, ajoute des valeurs complètes ou partielles dans autant de champs que nécessaire.

1. Clique sur **[!UICONTROL Search]** pour afficher les résultats.

   ![Résultats de la recherche](./assets/storefront-search-advanced-results-modify.png){width="700" zoomable="yes"}

1. S’il ne voit pas ce qu’il recherche dans les résultats de la recherche, le client clique sur **[!UICONTROL Modify your search]** et tente une autre combinaison de critères.
