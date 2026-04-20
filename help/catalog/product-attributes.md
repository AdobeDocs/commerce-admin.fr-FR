---
title: Présentation des attributs de produit
description: Découvrez les attributs du produit et leur utilisation pour décrire les caractéristiques spécifiques d’un produit.
exl-id: e15770ee-fb71-43f0-8c26-e8029935799a
feature: Catalog Management, Products
source-git-commit: 837da039e03db94014056fbb4e945c47fa37b7c1
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 0%

---

# Présentation des attributs de produit

Les attributs sont les blocs de construction de votre catalogue de produits et décrivent les caractéristiques spécifiques d’un produit. Les attributs de produit peuvent être organisés en [jeux d’attributs](attribute-sets.md), qui sont ensuite utilisés comme modèles pour créer des produits.

Les attributs déterminent le type de contrôle d’entrée utilisé pour les options de produit et fournissent des informations supplémentaires pour les pages de produit. Ils sont également utilisés comme paramètres de recherche et critères pour la navigation par couches, les rapports de comparaison de produits et les promotions. Vous pouvez créer autant d’attributs et de jeux d’attributs que nécessaire pour décrire les produits de votre catalogue. Outre les attributs que vous pouvez créer, les attributs du système, tels que le prix, sont intégrés à la plateforme Commerce de base et ne peuvent pas être modifiés.

![Création d’un attribut lors de la modification d’un produit](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

Appliquez les bonnes pratiques décrites dans les sections suivantes lorsque vous planifiez et créez des attributs de produit.

## Noms d’attributs

Définissez des conventions de dénomination des attributs cohérentes, y compris la casse et la ponctuation. Par exemple, `Color:Green` et `Color:green` peuvent être considérés comme deux valeurs d’attribut différentes par des systèmes différents. Ce bruit dans les données peut affecter les règles métier, les résultats de recherche et les filtres de données pour les applications qui font correspondre les produits aux règles.

## Utilisation des attributs

Tenez compte de la manière dont les attributs doivent être utilisés lors de l’attribution de propriétés et de valeurs. Identifiez les attributs utilisés comme libellés pour la présentation, tels que le nom, l’image, le prix et la description du produit, ainsi que les attributs utilisés pour la saisie des données. Tenez compte de la manière dont les attributs sont représentés sur différentes pages du site et de la manière dont ils apparaissent sur les pages de catégories, les pages de détails de produits, les grilles de catégories et les curseurs de miniatures.

## Couleur

Les descriptions de couleurs ad hoc peuvent poser un problème du point de vue des opérations de base de données. Les noms de couleurs tels que « Azure Skies » ou « Robin Egg Blue » sont très attrayants, mais peuvent ne pas renvoyer les meilleurs résultats lorsqu’ils sont utilisés comme critères de recherche ou si le merchandising exige que vous spécifiiez `Color_Family:Blue`. Tenez compte de la manière dont les couleurs sont représentées dans les résultats de recherche et la navigation par couches, et établissez des directives pour les besoins de votre entreprise. Ensuite, assurez-vous d’être cohérent lors de l’attribution des valeurs d’attribut de couleur dans votre catalogue.

## Gestion des variations

Utilisez les [options de configuration](product-configurations.md) et [produits configurables](product-create-configurable.md) pour gérer les variations de vos offres de produits. Ces fonctionnalités permettent de classer les produits plus facilement, de créer des règles de prix de panier et des règles de catégories dynamiques, ainsi que de proposer une sélection d’options avec divers types de saisie de texte, de sélection et de date.

## Recherche pondérée

Les attributs de produit activés pour la [recherche catalogue](search.md) peuvent être affectés d’un poids afin de leur donner une valeur plus élevée dans les résultats de recherche. Les attributs ayant un poids supérieur sont renvoyés avant ceux ayant un poids inférieur. Prenons l’exemple de deux attributs du système, _couleur_ avec un poids de recherche de 3 et _description_ avec un poids de recherche de 1. Une recherche du mot _rouge_ renvoie une liste de produits avec une valeur d’attribut de couleur de `red`, mais ne renvoie pas de produits avec des descriptions contenant le mot _rouge_. Dans cet exemple, le poids défini de l’attribut `color` est supérieur à celui de l’attribut `description`.

## Propriétés non utilisées

Supprimez les propriétés de produit inutilisées pour une meilleure structuration et une indexation plus rapide.


>[!NOTE]
>
>Pour plus d’informations sur l’optimisation de la configuration des attributs de produit en termes de performances, consultez [Bonnes pratiques de gestion des catalogues](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/planning/catalog-management#product-attributes) dans le _guide d’implémentation_.
