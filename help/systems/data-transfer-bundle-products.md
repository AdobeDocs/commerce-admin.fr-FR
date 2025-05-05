---
title: Importer des produits groupés
description: Examinez un exemple d’importation de données de produit pour un produit en regroupement.
exl-id: 52146979-9911-449b-9f14-54377e2ae9f4
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 0%

---

# Importer des produits groupés

Un produit groupé présente une sélection d’articles et permet aux clients de choisir ceux qu’ils souhaitent acheter. Tous les éléments qui constituent un lot existent dans le catalogue sous la forme [Produits simples](../catalog/product-create-simple.md) ou [Produits virtuels](../catalog/product-create-virtual.md). En règle générale, les produits du bundle sont créés et mis à jour à partir de l’administrateur. Cependant, vous pouvez également importer des données pour créer un produit groupé ou exporter des produits groupés existants, modifier les données et les réimporter dans le catalogue. Le Sprite Yoga Companion Kit est un produit fourni dans les exemples de données utilisés dans les exemples suivants.

![Produit groupé](../catalog/assets/product-bundle.png){width="700" zoomable="yes"}

## Modifier l’ordre des éléments du lot

Il existe deux manières de modifier l’ordre des éléments dans un produit en regroupement.

### Méthode 1 : glisser-déposer

Lorsque vous utilisez un produit [Bundle](../catalog/product-create-bundle.md) de l’administrateur, vous pouvez faire glisser des éléments et des sections en position.

![Éléments groupés](../catalog/assets/product-bundle-items-move.png){width="600" zoomable="yes"}

### Méthode 2 : modification des données de produit

La meilleure manière de comprendre la structure d’un produit en bundle consiste à exporter le produit et à examiner les données dans une feuille de calcul. Vous pouvez modifier l’ordre des éléments du lot en exportant le produit et en ajoutant un paramètre de position aux données de chaque élément. Les données d’élément se trouvent dans la colonne `bundle_values` du produit exporté. Lorsqu’ils sont ouverts dans une feuille de calcul, tous les éléments associés au produit se trouvent dans une seule cellule sous la forme d’une longue chaîne de texte. La colonne `bundle_values` contient les éléments suivants pour chaque élément :

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

Au cours de cette étape, le Sprite Yoga Companion Kit est exporté sous la forme d’un fichier ([CSV](data-csv.md)). Vous pouvez utiliser n’importe quel autre produit de lot que vous avez dans votre catalogue.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Sous _Paramètres d’exportation_, définissez **[!UICONTROL Entity Type]** sur `Products`.

1. Dans la liste des attributs de produit, faites défiler l’écran jusqu’à **[!UICONTROL SKU]** et saisissez le SKU du produit groupé que vous souhaitez exporter.

   Le SKU est `24-WG080` pour le produit dans cet exemple.

1. Faites défiler la page jusqu’au bas de la section et cliquez sur **[!UICONTROL Continue]**.

1. Dans la colonne _[!UICONTROL Action]_&#x200B;de la grille&#x200B;_[!UICONTROL File name]_, cliquez sur **[!UICONTROL Select]** et choisissez `Download`.

   Le fichier apparaît à l’emplacement de téléchargement utilisé par votre navigateur.

#### Etape 2 : Editer les données

1. Ouvrez le fichier CSV téléchargé dans une feuille de calcul.

1. Faites défiler l’écran jusqu’à l’extrême droite, jusqu’à ce que vous puissiez voir la colonne `bundle_values`.

   Dans les données `bundle_values`, chaque élément est séparé par une virgule et chaque élément de lot est séparé du suivant par une barre verticale. (Le dernier élément ne se termine pas par une barre verticale.) Les données de lot exportées doivent ressembler à l’exemple suivant :

   ![Valeurs groupées](./assets/product-bundle-values-export-data.png){width="600" zoomable="yes"}

1. Pour faciliter la modification, vous pouvez copier les données `bundle_values` et les coller dans un éditeur de texte. Ajoutez ensuite un saut de ligne après chaque élément afin que chaque élément soit sur une ligne distincte.

1. Après avoir modifié les données, supprimez soigneusement les sauts de ligne et collez les données modifiées dans la colonne `bundle_values`.

   Sur l’illustration suivante, un paramètre `position=[number]` est ajouté à chaque sangle de yoga pour modifier l’ordre des éléments dans la liste des magasins.

   ![Paramètre de position](./assets/product-bundle-values-position-parameter.png){width="500" zoomable="yes"}

1. Après avoir modifié les données, **[!UICONTROL Save]** le fichier CSV.

#### Étape 3 : Importer le produit mis à jour

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Sous _[!UICONTROL Import Settings]_, définissez **[!UICONTROL Entity Type]**&#x200B;sur `Products`.

1. Définissez **[!UICONTROL Import Behavior]** sur `Replace`.

   Cette option remplace les données précédentes de votre produit de lot, plutôt que d’ajouter vos modifications en tant qu’éléments supplémentaires.

1. Faites défiler l&#39;écran jusqu&#39;à la section _Fichier à importer_ et cliquez sur **[!UICONTROL Choose File]**.

1. Sélectionnez le fichier CSV que vous avez modifié.

1. Cliquez sur **[!UICONTROL Check Data]** et attendez quelques instants que les données soient vérifiées.

1. Si le fichier est valide, cliquez sur **[!UICONTROL Import]**.

1. Une fois le processus terminé, accédez à **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**&#x200B;et cliquez sur **[!UICONTROL Flush Cache Storage]**.

   Cela garantit que le produit mis à jour est immédiatement disponible dans le storefront.
