---
title: Paramètres du produit - [!UICONTROL Search Engine Optimization]
description: Pour un produit, les paramètres [!UICONTROL Search Engine Optimization] définissent la clé d’URL et les métadonnées utilisées par les moteurs de recherche pour indexer le produit.
exl-id: 78888094-759c-4e45-afcd-65858ee76159
feature: Catalog Management, Products, Search
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# Paramètres du produit - [!UICONTROL Search Engine Optimization]

_L’optimisation du moteur de recherche_ est une pratique consistant à affiner le contenu et la présentation d’un site afin d’améliorer la manière dont les pages sont indexées par les moteurs de recherche.

Les paramètres _[!UICONTROL Search Engine Optimization]_d’un produit spécifient les champs [URL Key](catalog-urls.md) et [meta data](../merchandising-promotions/meta-data.md) utilisés par les moteurs de recherche pour indexer le produit. Bien que certains moteurs de recherche ignorent les méta-mots-clés, d’autres moteurs de recherche continuent de les utiliser. La [bonne pratique d’optimisation pour les moteurs de recherche](../merchandising-promotions/seo-overview.md) actuelle consiste à incorporer des mots-clés à valeur élevée dans le méta-titre et dans la méta-description.

La valeur par défaut de chaque champ de métadonnées peut être générée automatiquement en fonction des valeurs spécifiées dans la configuration. Chaque champ contient un espace réservé qui est remplacé par une valeur réelle. Pour plus d’informations, voir [Génération automatique des champs de produit](../configuration-reference/catalog/catalog.md#uicontrol-product-fields-auto-generation).

## Renseignez les champs d’optimisation du moteur de recherche

1. Ouvrez le produit en mode d’édition.

1. Faites défiler l’écran vers le bas et développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur _[!UICONTROL Search Engine Optimization]_.

![Optimisation du moteur de recherche](./assets/product-search-engine-optimization.png){width="600" zoomable="yes"}


1. Saisissez le **[!UICONTROL URL Key]** (facultatif).

   La clé d’URL par défaut est basée sur le nom du produit. Vous pouvez utiliser la valeur par défaut ou la modifier selon vos besoins. Pour plus d’informations, voir [URL de catalogue](catalog-urls.md).

1. Saisissez le **[!UICONTROL Meta Title]** (facultatif).

   Le titre du méta est le texte qui s’affiche en haut de la fenêtre du navigateur. Vous pouvez utiliser la valeur par défaut, qui est basée sur le nom du produit, ou la modifier selon vos besoins.

1. Ajoutez le **[!UICONTROL Meta Keywords]** (facultatif).

   Les méta-mots-clés sont plus utilisés par certains moteurs de recherche que par d’autres. Il est recommandé de saisir quelques mots-clés à forte valeur ajoutée pour améliorer la visibilité du produit.

1. Saisissez le **[!UICONTROL Meta Description]**.

   La méta-description est le texte qui apparaît dans les listes de résultats de recherche. Pour de meilleurs résultats, saisissez une description comprise entre 150 et 160 caractères.

## Référence de champ

| Champ | [Portée](../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |------------------|
| [!UICONTROL URL Key] | Affichage en magasin | Détermine l’adresse en ligne du produit. La clé URL est ajoutée à l’URL de base du magasin et apparaît dans la barre d’adresse d’un navigateur. Commerce crée initialement une URL _compatible avec les moteurs de recherche_ basée sur le nom du produit. La clé URL doit être composée de tous les caractères minuscules, avec des tirets non alignés à la fin entre ces caractères et non des espaces. N’incluez pas de suffixe tel que `.html` dans la clé d’URL, car il est géré dans la configuration. |
| [!UICONTROL Meta Title] | Affichage en magasin | Le titre apparaît dans la barre de titre et dans l’onglet de votre navigateur et est également utilisé comme titre sur la page de résultats d’un moteur de recherche (SERP). Le titre du méta doit être propre à la page et contenir moins de 70 caractères. Valeur générée automatiquement : `{{name}}` |
| [!UICONTROL Meta Keywords] | Affichage en magasin | Mots-clés pertinents pour le produit. Pensez à utiliser des mots-clés que les clients peuvent utiliser pour trouver le produit. Valeur générée automatiquement : `{{name}}` |
| [!UICONTROL Meta Description] | Affichage en magasin | La méta-description fournit un bref aperçu de la page pour les listes de résultats de recherche. La longueur idéale est comprise entre 150 et 160 caractères, avec un maximum de 255 caractères. Bien que invisible pour le client, certains moteurs de recherche incluent la méta-description sur la page des résultats de recherche. Valeur générée automatiquement : `{{name}} {{description}}` |

{style="table-layout:auto"}
