---
title: Présentation des attributs de produit
description: Découvrez les attributs de produit et leur utilisation pour décrire les caractéristiques spécifiques d’un produit.
exl-id: e15770ee-fb71-43f0-8c26-e8029935799a
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# Présentation des attributs de produit

Les attributs sont les blocs de création de votre catalogue de produits et décrivent les caractéristiques spécifiques d’un produit. Les attributs de produit peuvent être organisés en [ensembles d’attributs](attribute-sets.md), qui sont ensuite utilisées comme modèles pour créer des produits.

Les attributs déterminent le type de contrôle d’entrée utilisé pour les options de produit et fournissent des informations supplémentaires pour les pages de produit. Elles servent également de paramètres et de critères de recherche pour la navigation superposée, les rapports de comparaison de produits et les promotions. Vous pouvez créer autant d’attributs et de jeux d’attributs que nécessaire pour décrire les produits de votre catalogue. Outre les attributs que vous pouvez créer, les attributs système, tels que le prix, sont intégrés à la plateforme Commerce principale et ne peuvent pas être modifiés.

![Création d’un attribut lors de la modification d’un produit](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

Appliquez les bonnes pratiques décrites dans les sections suivantes lorsque vous planifiez et créez des attributs de produit.

## Noms d’attributs

Définissez des conventions d’attribution de noms cohérentes, notamment la casse et la ponctuation des lettres. Par exemple : `Color:Green` et `Color:green` peut être considéré comme deux valeurs d’attribut différentes par différents systèmes. Ce bruit dans les données peut affecter les règles métier, les résultats de recherche et les filtres de données pour les applications qui correspondent aux produits aux règles.

## Utilisation des attributs

Tenez compte de la manière dont les attributs doivent être utilisés lors de l’attribution de propriétés et de valeurs. Identifiez les attributs utilisés comme libellés pour la présentation, tels qu’un nom, une image, un prix et une description du produit, ainsi que les attributs utilisés pour la saisie des données. Tenez compte de la manière dont les attributs sont représentés sur différentes pages du site et de leur apparence sur les pages de catégories, les pages de détails du produit, les grilles de catégories et les curseur de miniature.

## Couleur

Les descriptions de couleurs ad hoc peuvent poser problème du point de vue des opérations de base de données. Les noms de couleurs tels que &quot;Ciels Azure&quot; ou &quot;Ciels rouges&quot; ont un grand attrait, mais peuvent ne pas renvoyer les meilleurs résultats lorsqu’ils sont utilisés comme critères de recherche, ou si le marchandisage nécessite de spécifier `Color_Family:Blue`. Tenez compte de la représentation des couleurs dans les résultats de recherche et dans la navigation par couches, et établissez des directives en fonction des besoins de votre entreprise. Soyez ensuite cohérent lors de l’attribution des valeurs d’attribut de couleur dans votre catalogue.

## Gestion des variations

Utiliser le produit [options de configuration](product-configurations.md) et [produits configurables](product-create-configurable.md) pour gérer les variations de vos offres de produits. Ces fonctionnalités permettent de classer plus facilement les produits, de créer des règles de prix de panier et des règles de catégories dynamiques, et d’offrir une sélection d’options avec différents types de saisie de texte, de sélection et de date.

## Recherche pondérée

Attributs de produit activés pour [recherche catalogue](search.md) peut se voir attribuer un poids afin de leur donner une valeur plus élevée dans les résultats de recherche. Les attributs ayant un poids supérieur sont renvoyés avant ceux ayant un poids inférieur. Prenons l’exemple de deux attributs dans le système : _color_ avec un poids de recherche de 3 et _description_ avec un poids de recherche de 1. Recherche du mot _red_ renvoie une liste de produits avec une valeur d’attribut de couleur de `red`, mais ne renvoie pas les produits contenant des descriptions contenant le mot _red_. Dans cet exemple, la variable `color` a un poids défini supérieur à celui de l’attribut `description` attribut.

## Propriétés non utilisées

Supprimez les propriétés de produit inutilisées pour une meilleure structure et une indexation plus rapide.
