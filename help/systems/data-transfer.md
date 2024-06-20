---
title: Transfert de données
description: Découvrez la prise en charge du transfert de données, y compris la validation des données.
exl-id: 5057e398-c458-42e9-8ec0-bf116a667a3c
feature: System, Data Import/Export
source-git-commit: ae3bb3463df13c30ce34739bb6e476d3f7422671
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# Transferts de données

Utilisez les outils d&#39;import et d&#39;export pour gérer plusieurs enregistrements en une seule opération. Vous pouvez importer de nouveaux éléments ainsi que mettre à jour, remplacer et supprimer des ensembles de produits existants.

Par exemple, vous pouvez ajouter de nouveaux produits à votre inventaire, mettre à jour les données de produit et les données de prix avancées, et remplacer un ensemble de produits existants par de nouveaux produits. Les outils d’importation et d’exportation permettent de gérer plus efficacement les catalogues de produits volumineux, car vous pouvez exporter les données, les modifier dans une feuille de calcul et les réimporter dans votre boutique au lieu d’effectuer plusieurs opérations dans l’administrateur.

Outre les outils d’import et d’export, Adobe Commerce dispose de processus tels que [Exportation des données SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview) qui exportent les données de produit du serveur Commerce vers les services SaaS. L’exportation des données SaaS est intégrée aux services SaaS de Commerce, y compris [Recommendations de produit](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/overview.html), [Recherche en direct](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview), [Service de catalogue](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/guide-overview), et [Indexation des prix SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/price-indexer/price-indexing).

## Validation des données

Toutes les données doivent être validées pour garantir la qualité, la précision et l’intégrité des valeurs avant de les importer dans le magasin. La validation commence lorsque vous cliquez sur **[!UICONTROL Check Data]**. Pendant le processus, toutes les entités du fichier d&#39;import sont vérifiées pour les éléments suivants :

- **Attributs** - Les noms des en-têtes de colonne sont vérifiés pour s’assurer qu’ils correspondent aux attributs correspondants dans la base de données système. La valeur de chaque attribut est vérifiée afin de s’assurer qu’il répond aux exigences du type de données (décimal, entier, varchar, texte et date-heure).
- **Données complexes** - Les valeurs qui proviennent d’un jeu défini, comme une liste déroulante ou plusieurs types d’entrée de sélection, sont vérifiées afin de s’assurer que les valeurs existent dans l’ensemble défini.
- **Données du service** - Les valeurs des colonnes de données de service sont vérifiées afin de s’assurer que les propriétés ou les valeurs de données complexes sont cohérentes avec ce qui est déjà défini dans la base de données système.
- **Valeurs requises** - Pour les nouvelles entités, la présence des valeurs d’attribut requises dans le fichier est vérifiée. Pour les entités existantes, il n’est pas nécessaire de vérifier à nouveau l’existence des valeurs d’attribut requises.
- **Séparateurs** - Bien que les séparateurs ne soient pas visibles dans une feuille de calcul, les valeurs de données d’un fichier CSV sont séparées par des virgules et les valeurs de texte sont entourées de guillemets doubles. Pendant le processus de validation, la mise en forme des séparateurs et de chaque ensemble de guillemets encadrant des chaînes de caractères est vérifiée.

Les résultats de la validation apparaissent dans la section Résultats de la validation et incluent les informations suivantes :

- Le nombre d&#39;entités vérifiées
- Nombre de lignes non valides
- Le nombre d’erreurs trouvées

Si les données sont valides, une _Réussite de l’importation_ s’affiche.

![Message système - fichier valide](./assets/data-import-validation-message.png){width="500" zoomable="yes"}

Si la validation échoue, lisez la description de chaque erreur et corrigez le problème dans le fichier CSV. Par exemple, si une ligne contient un SKU non valide, le processus d’importation s’arrête et cette ligne n’est pas importée, toutes les lignes suivantes. Après avoir correctement résolu le problème, réimportez les données. Si de nombreuses erreurs sont rencontrées, plusieurs tentatives de validation peuvent être nécessaires.

### Messages de validation des données

#### Validation

- `Product with specified SKU not found in rows: 1`
- `URL key for specified store already exists`
- `'7z' file extension is not supported`
- `TXT file extension is not supported`

#### Erreurs

- `Wrong field type. Type in the imported file %decimal%, expected type is %text%.`
- `Value is not allowed. Attribute value does not exist in the system.`
- `Field %column name% is required.Wrong value separator is used.`
- `Wrong encoding used. Supported character encoding is UTF-8 and Windows-1252.`
- `Imported file does not contain SKU field.`
- `SKU does not exist in the system.`
- `Column name %column name% is invalid. Should start with a letter. Alphanumeric.`
- `Imported file does not contain a header.`
- `%website name% website does not exist in the system.`
- `%storeview name% storeview does not exist in the system.`
- `Imported attribute %attribute name% does not exist in the system.`
- `Imported resource (image) could not be downloaded from external resource due to timeout or access permissions.`
- `Imported resource (image) does not exist in the local media storage.`
- `Product creation error displayed to the user equal to the one seen during manual product save.`
- `Advanced Price creation error displayed to the user equal to the one seen during the manual product save.`
- `Customer creation error displayed to the user equal to the one seen during the manual customer save.`
