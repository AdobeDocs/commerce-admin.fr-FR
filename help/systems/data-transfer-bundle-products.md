---
title: Importer des produits groupés
description: Examinez un exemple d’importation de données de produit pour un produit en regroupement.
exl-id: 52146979-9911-449b-9f14-54377e2ae9f4
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%

---

# Importer des produits groupés

Un produit groupé présente une sélection d’articles et permet aux clients de choisir ceux qu’ils souhaitent acheter. Tous les éléments qui constituent un lot existent dans le catalogue comme suit : [Produits simples](../catalog/product-create-simple.md) ou [Produits virtuels](../catalog/product-create-virtual.md). En règle générale, les produits du bundle sont créés et mis à jour à partir de l’administrateur. Cependant, vous pouvez également importer des données pour créer un produit groupé ou exporter des produits groupés existants, modifier les données et les réimporter dans le catalogue. Le Sprite Yoga Companion Kit est un produit fourni dans les exemples de données utilisés dans les exemples suivants.

![Produit groupé](../catalog/assets/product-bundle.png){width="700" zoomable="yes"}

## Modifier l’ordre des éléments du lot

Il existe deux manières de modifier l’ordre des éléments dans un produit en regroupement.

### Méthode 1 : glisser-déposer

Lorsque vous utilisez une [Bundle](../catalog/product-create-bundle.md) à partir de l’administrateur, vous pouvez faire glisser des éléments et des sections et les positionner.

![Éléments groupés](../catalog/assets/product-bundle-items-move.png){width="600" zoomable="yes"}

### Méthode 2 : modification des données de produit

La meilleure manière de comprendre la structure d’un produit en bundle consiste à exporter le produit et à examiner les données dans une feuille de calcul. Vous pouvez modifier l’ordre des éléments du lot en exportant le produit et en ajoutant un paramètre de position aux données de chaque élément. Les données d’élément se trouvent dans la variable `bundle_values` de la colonne du produit exporté. Lorsqu’ils sont ouverts dans une feuille de calcul, tous les éléments associés au produit se trouvent dans une seule cellule sous la forme d’une longue chaîne de texte. La variable `bundle_values` contient les éléments suivants pour chaque élément :

- Nom de la section d’élément
- Contrôle d’entrée
- Indicateur d’élément requis
- SKU
- Couleur
- Prix
- Indicateur d’option par défaut
- Quantité par défaut
- Type de prix
- Indicateur de quantité modifiable

#### Étape 1 : exporter le produit du lot

Au cours de cette étape, le kit Sprite Yoga Companion est exporté sous la forme ([CSV](data-csv.md) fichier . Vous pouvez utiliser n’importe quel autre produit de lot que vous avez dans votre catalogue.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Sous _Paramètres d’exportation_, définit **[!UICONTROL Entity Type]** to `Products`.

1. Dans la liste des attributs de produit, faites défiler l’écran jusqu’à **[!UICONTROL SKU]** et saisissez le SKU du produit du lot que vous souhaitez exporter.

   Le SKU est `24-WG080` pour le produit dans cet exemple.

1. Faites défiler la page vers le bas de la section et cliquez sur **[!UICONTROL Continue]**.

1. Dans le _[!UICONTROL Action]_de la colonne_[!UICONTROL File name]_ grille, cliquez sur **[!UICONTROL Select]** et choisissez `Download`.

   Le fichier apparaît à l’emplacement de téléchargement utilisé par votre navigateur.

#### Etape 2 : Editer les données

1. Ouvrez le fichier CSV téléchargé dans une feuille de calcul.

1. Faites défiler l’écran jusqu’à l’extrême droite, jusqu’à ce que vous puissiez voir le `bundle_values` colonne .

   Dans le `bundle_values` data, chaque élément est séparé par une virgule et chaque élément de lot est séparé du suivant par une barre verticale. (Le dernier élément ne se termine pas par une barre verticale.) Les données de lot exportées doivent ressembler à l’exemple suivant :

   ![Valeurs groupées](./assets/product-bundle-values-export-data.png){width="600" zoomable="yes"}

1. Pour faciliter la modification, vous pouvez copier la variable `bundle_values` et collez-la dans un éditeur de texte. Ajoutez ensuite un saut de ligne après chaque élément, de sorte que chaque élément se trouve sur une ligne distincte.

1. Après avoir modifié les données, supprimez soigneusement les sauts de ligne et collez-les à nouveau dans le `bundle_values` colonne .

   Sur l’illustration suivante, une `position=[number]` est ajouté à chaque sangle de yoga pour modifier l’ordre des éléments dans la liste des magasins.

   ![Paramètre de position](./assets/product-bundle-values-position-parameter.png){width="500" zoomable="yes"}

1. Après avoir modifié les données, **[!UICONTROL Save]** fichier CSV.

#### Étape 3 : Importer le produit mis à jour

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Sous _[!UICONTROL Import Settings]_, définit **[!UICONTROL Entity Type]**to `Products`.

1. Définir **[!UICONTROL Import Behavior]** to `Replace`.

   Cette option remplace les données précédentes de votre produit de lot, plutôt que d’ajouter vos modifications en tant qu’éléments supplémentaires.

1. Faites défiler l’écran vers le bas jusqu’à _Fichier à importer_ et cliquez sur **[!UICONTROL Choose File]**.

1. Sélectionnez le fichier CSV que vous avez modifié.

1. Cliquez sur **[!UICONTROL Check Data]** et patientez quelques instants pour que les données soient vérifiées.

1. Si le fichier est valide, cliquez sur **[!UICONTROL Import]**.

1. Une fois le processus terminé, accédez à **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**et cliquez sur **[!UICONTROL Flush Cache Storage]**.

   Cela garantit que le produit mis à jour est immédiatement disponible dans le storefront.
