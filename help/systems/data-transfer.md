---
title: Transfert de données
description: Découvrez la prise en charge du transfert de données, y compris la validation des données.
exl-id: 5057e398-c458-42e9-8ec0-bf116a667a3c
feature: System, Data Import/Export
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# Transferts de données

Utilisez les outils d&#39;import et d&#39;export pour gérer plusieurs enregistrements en une seule opération. Vous pouvez importer de nouveaux éléments ainsi que mettre à jour, remplacer et supprimer des ensembles de produits existants.

Par exemple, vous pouvez ajouter de nouveaux produits à votre inventaire, mettre à jour les données sur les produits et les prix avancés, et remplacer un ensemble de produits existants par de nouveaux produits. Les outils d’importation et d’exportation permettent de gérer plus efficacement les catalogues de produits volumineux, car vous pouvez exporter les données, les modifier dans une feuille de calcul et les importer dans votre magasin au lieu d’effectuer plusieurs opérations dans l’administration.


>[!NOTE]
>
>Adobe Commerce prend également en charge l’exportation des données SaaS pour transférer les données de produit du serveur Commerce vers les services SaaS. L’exportation des données SaaS est intégrée aux services SaaS Commerce, notamment aux [Product Recommendations](https://experienceleague.adobe.com/docs/commerce/product-recommendations/overview.html), [Live Search](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview) et [Catalog Service](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/guide-overview). Pour plus d&#39;informations, consultez le [Guide d&#39;exportation de données SaaS](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview).

## Validation des données

Toutes les données doivent passer la validation pour garantir la qualité, la précision et l’intégrité des valeurs avant de les importer dans le magasin. La validation commence lorsque vous cliquez sur **[!UICONTROL Check Data]**. Au cours du processus, toutes les entités du fichier d’importation sont vérifiées pour les éléments suivants :

- **Attributs** - Les noms des en-têtes de colonne sont vérifiés afin de s’assurer qu’ils correspondent aux attributs correspondants dans la base de données système. La valeur de chaque attribut est vérifiée pour s’assurer qu’elle répond aux exigences du type de données (décimal, entier, varchar, texte et datetime).
- **Données complexes** - Les valeurs qui proviennent d’un ensemble défini, comme une liste déroulante ou un type d’entrée à sélection multiple, sont vérifiées pour s’assurer que les valeurs existent dans l’ensemble défini.
- **Données de service** - Les valeurs des colonnes de données de service sont vérifiées afin de s’assurer que les propriétés ou les valeurs de données complexes sont cohérentes avec ce qui est déjà défini dans la base de données système.
- **Valeurs requises** - Pour les nouvelles entités, la présence de valeurs d’attribut requises dans le fichier est vérifiée. Pour les entités existantes, il n’est pas nécessaire de vérifier à nouveau l’existence des valeurs d’attribut requises.
- **Séparateurs** - Bien que les séparateurs ne soient pas visibles dans une feuille de calcul, les valeurs de données d’un fichier CSV sont séparées par des virgules et les valeurs de texte sont placées entre guillemets doubles. Pendant le processus de validation, la mise en forme des séparateurs et de chaque ensemble de guillemets qui encadrent les chaînes de caractères est vérifiée.

Les résultats de la validation s’affichent dans la section Résultats de la validation et incluent les informations suivantes :

- Le nombre d’entités vérifiées
- Nombre de lignes non valides
- Nombre d’erreurs détectées

Si les données sont valides, un message _Succès de l’importation_ s’affiche.

![Message système - Le fichier est valide](./assets/data-import-validation-message.png){width="500" zoomable="yes"}

Si la validation échoue, lisez la description de chaque erreur et corrigez le problème dans le fichier CSV. Par exemple, si une ligne contient un SKU non valide, le processus d’importation s’arrête et cette ligne ainsi que toutes les lignes suivantes ne sont pas importées. Après avoir correctement résolu le problème, importez à nouveau les données. Si de nombreuses erreurs se produisent, plusieurs tentatives de validation peuvent être nécessaires.

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
