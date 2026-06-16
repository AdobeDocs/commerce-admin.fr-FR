---
title: Fichiers de données CSV
description: Découvrez la structure utilisée dans le fichier CSV pour prendre en charge l’importation et l’exportation de données.
exl-id: 86e362af-2af7-4557-ac49-1efad2f0e976
feature: Products, Customers, Data Import/Export
TQID: https://experienceleague.adobe.com/qeKpxnrPVwIX4MgrHlQRMEVQDOZjFvG3Es39rDwNgx4
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 718
ht-degree: 0%

---

# Fichiers de données CSV

Le format de fichier CSV (valeurs séparées par des virgules) est utilisé comme base des opérations de transfert de données et est pris en charge par toutes les tableurs et bases de données. Les types de fichiers suivants sont pris en charge pour l’importation et l’exportation :

- Importer : `CSV` et `ZIP` (un fichier CSV compressé)
- Exportation : `CSV`

>[!IMPORTANT]
>
>Il est recommandé d’utiliser un programme qui prend en charge le codage UTF-8, tel que le Bloc-notes++, pour modifier les fichiers CSV. ® Excel insère des caractères supplémentaires dans l’en-tête de colonne du fichier CSV, ce qui peut empêcher la réimportation des données dans Commerce. Si vous travaillez sur le Mac, vous pouvez enregistrer vos données au format CSV (Windows).

Les fichiers CSV ont une structure spécifique qui doit correspondre à la base de données. Chaque en-tête de colonne correspond au code d’attribut du champ représenté par la colonne. Pour que les en-têtes des colonnes puissent être lus par Commerce, exportez d’abord les données de votre magasin sous la forme d’un fichier CSV. Vous pouvez ensuite modifier les données et les réimporter dans Commerce.

Si vous ouvrez un fichier CSV exporté dans un éditeur de texte, les valeurs sont séparées par des virgules et plusieurs valeurs sont placées entre guillemets. Lors de l’importation, vous pouvez spécifier un caractère de séparation personnalisé, bien qu’une virgule soit la valeur par défaut.

## Structure CSV du produit

Une exportation complète de la base de données de produits contient des informations sur chaque produit du catalogue et sur les relations entre eux. Chaque enregistrement comporte une sélection fixe de colonnes qui correspond aux attributs du catalogue, bien que l’ordre des attributs soit ignoré pendant le processus d’importation.

La première ligne du tableau contient les noms de chaque attribut, utilisés comme en-têtes de colonne. Les lignes restantes décrivent les enregistrements de produits individuels. Toute ligne commençant par une valeur dans la colonne SKU marque le début d’un nouvel enregistrement de produit. Un seul produit peut inclure plusieurs lignes contenant des informations sur plusieurs images ou options de produit. La ligne suivante qui contient une valeur dans la colonne SKU commence un nouveau produit.

La colonne Catégorie contient un chemin d’accès pour chaque catégorie à laquelle le produit est affecté. Le chemin d’accès inclut la catégorie racine, suivie d’une barre oblique (`/`) entre chaque niveau. Par défaut, la virgule `,` est utilisée pour séparer les chemins d’accès aux catégories. (Vous pouvez spécifier un autre caractère séparateur avec l’option _[!UICONTROL Multiple value separator]_.) Par exemple :

`Default Category/Gear,Default Category/Gear/Bags`

Pour importer des données, vous ne devez inclure que le SKU et les colonnes avec des modifications. Toutes les colonnes vides sont ignorées pendant le processus d’importation. Il n’est pas possible d’ajouter des attributs pendant le processus d’importation. Vous ne pouvez inclure que des attributs existants.

Pour obtenir une description détaillée de chaque attribut de produit, voir [Structure de fichier CSV du produit](data-attributes-product.md).

| Nom de la colonne | Description |
| ----------- | ----------- |
| `_<name>` | Les en-têtes de colonne commençant par un trait de soulignement contiennent des propriétés d’entité de service ou des données complexes. Les colonnes de service ne sont pas des attributs de produit. |
| `<attribute_name>` | Les en-têtes de colonne avec un code d’attribut ou un nom de champ identifient la colonne de données. Une colonne peut représenter un attribut système ou un attribut créé par l’administrateur du magasin. |

{style="table-layout:auto"}

## Structure CSV du client

Le fichier CSV client contient des informations client de la base de données et présente la structure suivante :

La première ligne du tableau contient les noms des colonnes d’attributs (qui sont identiques aux codes d’attribut). Il existe deux types de noms de colonne, comme illustré dans le tableau suivant. D’autres lignes contiennent des valeurs d’attribut, des données de service et des données complexes. Chaque ligne contenant des valeurs non vides dans les colonnes `email` et `_website` lance la description du client suivant. Chaque ligne peut représenter les données client avec ou sans données d’adresse, ou les données d’adresse uniquement. Si une ligne contient uniquement les données d’adresse, les valeurs des colonnes liées au profil client sont ignorées et peuvent être vides.

Pour ajouter ou remplacer plusieurs adresses pour un client, ajoutez une ligne pour chaque nouvelle adresse avec des données client vides et les données d’adresse nouvelles ou mises à jour sous la ligne de données client.

Pour obtenir une description détaillée de chaque attribut du client, voir [Structure de fichier CSV du client](data-attributes-customer.md).

| Nom de la colonne | Description |
| ----------- | ----------- |
| `_<name>` | Les en-têtes de colonne commençant par un trait de soulignement contiennent des propriétés d’entité de service ou des données complexes. Les colonnes de service ne sont pas des attributs de client. |
| `<attribute name>` | Noms des colonnes avec des valeurs d’attributs créés par le système et d’attributs créés par l’administrateur du magasin. |

{style="table-layout:auto"}
