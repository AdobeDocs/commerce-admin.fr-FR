---
title: Fichiers de données CSV
description: Découvrez la structure utilisée dans le fichier CSV pour prendre en charge l’importation et l’exportation de données.
exl-id: 86e362af-2af7-4557-ac49-1efad2f0e976
feature: Products, Customers, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# Fichiers de données CSV

Le format de fichier CSV (valeurs séparées par des virgules) est utilisé comme base des opérations de transfert de données et est pris en charge par toutes les applications de tableur et de base de données. Les types de fichiers suivants sont pris en charge pour l’importation et l’exportation :

- Importation : `CSV` et `ZIP` (fichier CSV compressé)
- Export : `CSV`

>[!IMPORTANT]
>
>Il est recommandé d’utiliser un programme qui prend en charge le codage UTF-8, comme Notepad++, pour modifier les fichiers CSV. Microsoft® Excel insère des caractères supplémentaires dans l’en-tête de colonne du fichier CSV, ce qui peut empêcher l’importation des données dans Commerce. Si vous utilisez Mac, vous pouvez enregistrer vos données au format CSV (Windows).

Les fichiers CSV ont une structure spécifique qui doit correspondre à la base de données. Chaque en-tête de colonne correspond au Code d’attribut du champ représenté par la colonne. Pour vous assurer que Commerce peut lire les en-têtes de colonne, commencez par exporter les données de votre magasin sous la forme d’un fichier CSV. Vous pouvez ensuite modifier les données et les réimporter dans Commerce.

Si vous ouvrez un fichier CSV exporté dans un éditeur de texte, les valeurs sont séparées par des virgules et plusieurs valeurs sont entourées de guillemets doubles. Lors de l’importation, vous pouvez spécifier un caractère de séparateur personnalisé, bien qu’une virgule soit la valeur par défaut.

## Structure CSV du produit

Une exportation complète de la base de données de produits contient des informations sur chaque produit du catalogue et sur les relations entre celui-ci. Chaque enregistrement comporte une sélection fixe de colonnes qui correspond aux attributs du catalogue, bien que l’ordre des attributs soit ignoré pendant le processus d’importation.

La première ligne du tableau contient les noms de chaque attribut, qui sont utilisés comme en-têtes de colonne. Les lignes restantes décrivent les enregistrements de produit individuels. Toute ligne commençant par une valeur dans la colonne SKU constitue le début d’un nouvel enregistrement de produit. Un seul produit peut inclure plusieurs lignes contenant des informations sur plusieurs images ou options de produit. La ligne suivante comportant une valeur dans la colonne SKU commence un nouveau produit.

La colonne Catégorie contient un chemin d’accès pour chaque catégorie à laquelle le produit est affecté. Le chemin d’accès inclut la catégorie racine, suivie d’une barre oblique (`/`) entre chaque niveau. Par défaut, la virgule `,` est utilisée pour séparer les différents chemins de catégorie. (Vous pouvez spécifier un autre caractère de séparateur avec l’option _[!UICONTROL Multiple value separator]_.) Par exemple :

`Default Category/Gear,Default Category/Gear/Bags`

Pour importer des données, vous devez inclure uniquement le SKU et les colonnes contenant des modifications. Toutes les colonnes vides sont ignorées pendant le processus d’importation. Il n’est pas possible d’ajouter des attributs pendant le processus d’importation. Vous ne pouvez inclure que les attributs existants.

Pour une description détaillée de chaque attribut de produit, voir [Structure de fichier CSV de produit](data-attributes-product.md).

| Nom de la colonne | Description |
| ----------- | ----------- |
| `_<name>` | Les en-têtes de colonne commençant par un trait de soulignement contiennent des propriétés d’entité de service ou des données complexes. Les colonnes de service ne sont pas des attributs de produit. |
| `<attribute_name>` | Les en-têtes de colonne avec un code d’attribut ou un nom de champ identifient la colonne de données. Une colonne peut représenter un attribut système ou un attribut créé par l’administrateur du magasin. |

{style="table-layout:auto"}

## Structure CSV du client

Le fichier CSV des clients contient les informations sur les clients de la base de données et possède la structure suivante :

La première ligne du tableau contient les noms des colonnes d’attributs (qui sont identiques aux codes d’attributs). Il existe deux types de noms de colonne, comme illustré dans le tableau suivant. D’autres lignes contiennent des valeurs d’attribut, des données de service et des données complexes. Chaque ligne avec des valeurs non vides dans les colonnes `email` et `_website` commence la description du client suivant. Chaque ligne peut représenter les données du client avec ou sans données d’adresse, ou les données d’adresse uniquement. Si une ligne ne contient que les données d’adresse, les valeurs des colonnes relatives au profil du client sont ignorées et peuvent être vides.

Pour ajouter ou remplacer plusieurs adresses pour un client, ajoutez une ligne pour chaque nouvelle adresse avec des données client vides et les données d’adresse nouvelles ou mises à jour sous la ligne de données client.

Pour une description détaillée de chaque attribut du client, voir [Structure de fichier CSV client](data-attributes-customer.md).

| Nom de la colonne | Description |
| ----------- | ----------- |
| `_<name>` | Les en-têtes de colonne commençant par un trait de soulignement contiennent des propriétés d’entité de service ou des données complexes. Les colonnes du service ne sont pas des attributs du client. |
| `<attribute name>` | Les noms des colonnes avec les valeurs des attributs créés par le système et les attributs créés par l’administrateur du magasin. |

{style="table-layout:auto"}
