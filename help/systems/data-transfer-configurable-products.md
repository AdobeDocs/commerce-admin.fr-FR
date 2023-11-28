---
title: Importation de produits configurables
description: Examinez un exemple d’importation de données de produit pour un produit configurable.
exl-id: bb8b2a6d-867e-4ab2-bdfd-98a01d79c457
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '943'
ht-degree: 0%

---

# Importation de produits configurables

La meilleure façon de comprendre la structure des données de produit configurables consiste à exporter un produit configurable et ses variantes, puis à examiner les données dans une feuille de calcul.

Dans l’exemple suivant, vous ajoutez un ensemble de variations de produit pour une nouvelle taille dans chaque couleur. Tout d’abord, vous exportez le produit configurable et vous examinez la structure des données. Vous mettez ensuite les données à jour et les importez à nouveau dans le catalogue. Si vous ne souhaitez pas poursuivre l’exportation des données, vous pouvez télécharger le fichier CSV utilisé dans l’exemple.

![Exemple de storefront - attributs de taille et de couleur](./assets/storefront-hoodie-new-size.png){width="700" zoomable="yes"}

## Étape 1 : vérification des paramètres et des valeurs d’attribut

1. Avant de commencer, assurez-vous que les attributs utilisés pour les variations de produit possèdent les paramètres de propriété requis.

   - [**[!UICONTROL Scope]**](../getting-started/websites-stores-views.md#scope-settings) - `Global`
   - [**[!UICONTROL Catalog Input Type for Store Owner]**](data-attributes-product.md) - Le type d’entrée de tout attribut utilisé pour une variation de produit doit être l’un des suivants :

      - `Dropdown`
      - `Visual Swatch`
      - `Text Swatch`
      - `Multi-Select`

   - **[!UICONTROL Values Required]** - `Yes`

1. Si vous ajoutez une taille ou une couleur, ou apportez toute autre modification à un attribut existant, veillez à mettre à jour l’attribut avec la nouvelle valeur.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Recherchez l’attribut dans la liste et ouvrez-le en mode d’édition.

1. Ajoutez la nouvelle valeur à l’attribut .

   Dans l’exemple suivant, une nouvelle taille est ajoutée à une nuance de texte.

   ![Attribut de produit - ajouter une nouvelle valeur](./assets/data-transfer-configurable-product-add-new-attribute-value.png){width="500" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Attribute]**.

1. Si vous ajoutez un attribut, suivez les instructions pour [création de l’attribut](../catalog/attribute-product-create.md) avant de commencer.

## Etape 2 : exporter le produit configurable

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Recherchez le produit configurable à exporter :

   - Cliquez sur **[!UICONTROL Filters]**.
   - Définir **[!UICONTROL Type]** to `Configurable Product` et cliquez sur **[!UICONTROL Apply Filters]**.
   - Sélectionnez le produit configurable que vous souhaitez utiliser pour votre export test et notez le **[!UICONTROL SKU]**.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

   ![Paramètres d’exportation des données](./assets/data-transfer-export-settings.png){width="600" zoomable="yes"}

1. Sous _[!UICONTROL Export Setting]s_, procédez comme suit :

   - Définir **[!UICONTROL Entity Type]** to `Products`.

   - Définir **[!UICONTROL Export File Format]** to `CSV`.

1. Sous _[!UICONTROL Entity Attributes]_, faites défiler l’écran vers le bas ou utilisez le filtre de libellé d’attribut pour localiser la variable **[!UICONTROL SKU]**Attribuez et procédez comme suit :

   - Saisissez le SKU du produit configurable que vous avez choisi d’exporter, puis cliquez sur **[!UICONTROL Continue]**.

     ![SKU d’exportation de données](./assets/data-transfer-export-sku.png){width="600" zoomable="yes"}

   - Recherchez le fichier à l’emplacement de téléchargement de votre navigateur web et ouvrez-le sous forme de feuille de calcul.

     Le fichier CSV comporte une ligne distincte pour chaque variante de produit simple et une ligne pour le produit configurable. La variable `product_type column` affiche plusieurs variantes de produits simples associées à un produit configurable.

     ![Exemple de données - produit configurable avec variations](./assets/data-transfer-csv-configurable-product.png){width="600" zoomable="yes"}

   - Faites défiler la page jusqu’à l’extrémité droite de la feuille de calcul pour trouver les colonnes suivantes.

      - `configurable_variations` - Définit la relation de type &quot;un à plusieurs&quot; entre l’enregistrement de produit configurable et chaque variation.
      - `configurable_variation_labels` - Définit le libellé qui identifie chaque variation.

     Dans cet exemple, les données se trouvent dans les colonnes CG et CH. Selon le nombre de variations, la chaîne de données de la variable `configurable_variations` peut être longue. Les données sont utilisées comme index pour les variations de produit associées et présentent la structure suivante :

     ```text
     sku={{SKU_VALUE}},attribute1={{VALUE}},attribute2={{VALUE}}| sku={{SKU_VALUE}},attribute1={{VALUE}},attribute2={{VALUE}}
     ```

     Chaque SKU est séparé par une barre verticale (|) et les attributs sont séparés par une virgule. La valeur de chaque attribut est représentée par le code de l’attribut, plutôt que par le libellé de l’attribut. Voici comment les données réelles apparaissent :

     ```text
     sku=MH01-XS-Black,size=XS,color=Black|sku=MH01-XS-Gray,size=XS,color=Gray|sku=MH01-XS-Orange,size=XS,color=Orange</pre>
     ```

1. Lorsque vous comprenez la structure des données de produit configurables, vous pouvez modifier les données ou ajouter de nouvelles variations directement au fichier CSV.

   Pour en savoir plus, voir [Données complexes](data-attributes-product.md#complex-product-data-attributes).

## Etape 3 : Editer les données

Dans l’exemple suivant, l’ensemble de tailles XL est copié et collé dans la feuille de calcul afin de créer un ensemble de variations de produit pour une nouvelle taille dans chaque couleur.

1. Copiez l’ensemble de variations de produit que vous souhaitez utiliser comme modèle pour les nouveaux produits.

   ![Données exportées - Copie de variations de produit](./assets/data-transfer-export-configurable-copy-rows.png){width="600" zoomable="yes"}

1. Insérez les enregistrements de lignes copiés dans la feuille de calcul.

   Vous disposez désormais de deux ensembles identiques de variations de produit simples.

   ![Données CSV - Ajout de variations de produit](./assets/data-transfer-export-configurable-copy-rows.png){width="600" zoomable="yes"}

1. Mettez à jour les données dans les colonnes suivantes des nouvelles variations, si nécessaire.

   - `sku`
   - `name`
   - `url_key`
   - `additional_attributes`

   Pour cet exemple, tous les `XL` les références sont remplacées par `XXL`.

1. Mettez à jour les informations dans le `product_variations` de l’enregistrement de produit configurable, de sorte que les nouvelles variations soient incluses dans le produit configurable.

   Sur la ligne contenant l’enregistrement de produit configurable, cliquez sur la cellule contenant le `product_variations` data. Ensuite, dans la barre de formule, copiez le dernier ensemble de paramètres, en commençant par le symbole de barre verticale.

   ![données product_variations](./assets/data-transfer-export-configurable-product-product-variations-data.png){width="600" zoomable="yes"}

1. Collez les paramètres à la fin des données et modifiez-les selon les besoins pour les nouvelles variations.

   Dans cet exemple, la variable `sku` et `size` Les paramètres sont mis à jour pour la nouvelle taille XXL.

1. Avant que les données ne soient réimportées dans le catalogue, supprimez les lignes qui n’ont pas été modifiées.

   Dans cet exemple, seules les trois nouvelles variations de la nouvelle taille et de la ligne avec le produit configurable mis à jour sont réimportées dans le catalogue. Les autres lignes peuvent être supprimées du fichier CSV. Veillez toutefois à ne pas supprimer la ligne d’en-tête avec les libellés de colonne.

   ![Données CSV à importer](./assets/data-transfer-csv-configurable-product-data-ready-to-import.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save]** fichier CSV.

   Les données sont prêtes à être importées dans le catalogue.

   >[!NOTE]
   >
   >La taille d’un fichier d’importation ne peut pas dépasser 2 Mo.

## Étape 4 : Importer les données mises à jour

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Sous _[!UICONTROL Import Settings]_, définit **[!UICONTROL Entity Type]**to `Products`.

1. Sous _[!UICONTROL Import Behavior]_, définit **[!UICONTROL Import Behavior]**to `Add/Update`.

   ![Comportement d’importation de données](./assets/data-transfer-configurable-product-import-behavior.png){width="600" zoomable="yes"}

1. Sous _[!UICONTROL File to Import]_, cliquez sur **[!UICONTROL Choose File]**et accédez au fichier CSV que vous avez préparé pour l’importation, puis sélectionnez le fichier.

   ![Fichier d’importation de données](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Check Data]**.

1. Si le fichier est valide, cliquez sur **[!UICONTROL Import]**.

   Sinon, corrigez les problèmes détectés dans les données et réessayez.

   ![Message système - fichier valide](./assets/data-transfer-configurable-product-import-validation-results.png){width="600" zoomable="yes"}

1. Une fois l’importation terminée, cliquez sur **[!UICONTROL Cache Management]** dans le message en haut de la page et actualisez tous les caches non valides.

   Les nouvelles variations de produit sont désormais disponibles dans le catalogue à partir de l’administrateur et dans le storefront. Dans cet exemple, le sweat à capuche est désormais disponible en taille XXL pour toutes les couleurs.
