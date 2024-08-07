---
title: Import et export d'inventaire
description: Utilisez les fonctionnalités natives d'import et d'export avec les options  [!DNL Inventory Management] étendues pour mettre à jour les sources et les quantités par SKU.
exl-id: cb2d2e0d-aef8-4b18-b013-9a7b0ab448bd
feature: Inventory, Data Import/Export
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# Import et export d&#39;inventaire

Pour les catalogues comportant de nombreux produits, utilisez les fonctionnalités natives d’import et d’export avec les options [!DNL Inventory Management] étendues pour mettre à jour les sources et les quantités par SKU. Grâce à ces options, vous pouvez ajouter de nouvelles sources et mettre à jour les quantités d’inventaire pour l’ensemble ou une source spécifique. Par exemple, vous pouvez exporter des produits pour une source en Allemagne sans affecter les informations sur les produits pour des sources en France, en Angleterre ou aux États-Unis.

- [!DNL Commerce] affecte automatiquement le Source par défaut à vos produits lors de la mise à niveau de [!DNL Commerce] ou de l&#39;import de nouveaux produits. Si vous importez des produits auxquels une source personnalisée est affectée, le Source par défaut est toujours ajouté avec une quantité de 0. Pour mettre à jour les sources et les quantités, suivez ces instructions d&#39;import.

- Les marchands à source unique utilisent l’importation pour mettre à jour uniquement les quantités de produits. Tous les produits existants et ajoutés sont affectés à la Source par défaut.

- Les négociants multi-sources utilisent l’importation pour ajouter plusieurs sources et quantités par ligne par SKU.

Pour importer des mises à jour, commencez par exporter un fichier CSV pour une ou toutes les sources. Modifiez le fichier CSV et ajoutez une ligne par SKU pour chaque source et quantité. Vous avez besoin du code source lors de l&#39;ajout d&#39;une source et de l&#39;ajout de quantités de stock. Vous ne pouvez pas ajouter ni mettre à jour des stocks à l&#39;aide des fonctionnalités d&#39;import-export.

## Contenu du fichier CSV

Le fichier export-import contient les informations suivantes en fonction de la source :

- `source_code` - Code des sources dans [!DNL Commerce]. Il existe une ligne pour chaque source et chaque SKU.
- `sku` - SKU du produit dans [!DNL Commerce]. Le SKU doit correspondre à un produit de votre magasin pour mettre à jour correctement les données [!DNL Inventory Management].
- `status` - 0 pour rupture de stock. 1 pour En stock. Cette valeur doit être de 1 pour acheter du stock à partir de cette source.
- `quantity` - La quantité totale d’inventaire disponible pour ce SKU et cette source.

Utilisez un fichier CSV pour mettre rapidement à jour plusieurs produits et sources affectées afin de mettre à jour et de corriger les éventuelles inexactitudes dans les enregistrements d’inventaire plutôt qu’une par une dans l’interface de l’application. Pour un fichier de base, exportez d’abord et mettez-le à jour selon les besoins.

![Exemple de fichier CSV pour l’importation - Exporter les données d’inventaire](assets/inventory-import-export-data.png){width="600" zoomable="yes"}

## Exportation des données de produit pour toutes les sources

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Pour **[!UICONTROL Entity Type]**, choisissez `Stock Sources`.

   L’exportation extrait uniquement les données des produits avec un SKU.

1. Cliquez sur **[!UICONTROL Continue]**.

   Le fichier génère et télécharge pour s’ouvrir et modifier.

Après la mise à jour des quantités d’inventaire et des données de produit, réimportez le fichier dans [!DNL Commerce].

![Exporter des sources de stock pour les données et les sources de produits](assets/inventory-export-stock-sources.png){width="350" zoomable="yes"}

## Exportation des données de produit pour une source spécifique

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Pour **[!UICONTROL Entity Type]**, choisissez `Stock Sources`.

   L’exportation extrait uniquement les données des produits avec un SKU.

1. Utilisez le **[!UICONTROL Entity Attributes]** pour filtrer les produits exportés pour une source spécifique.

   Pour `source_code`, saisissez le code de la source dans le champ de filtre.

1. Cliquez sur **[!UICONTROL Continue]**.

   Le fichier génère et télécharge pour s’ouvrir et modifier.

Après la mise à jour des quantités d’inventaire et des données de produit, réimportez le fichier dans [!DNL Commerce].

## Importation des données de produit

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Pour **[!UICONTROL Entity Type]**, choisissez `Stock Sources`.

   L’exportation extrait uniquement les données des produits avec un SKU.

1. Sélectionnez des configurations pour le **[!UICONTROL Import Behavior]**.

1. Sélectionnez le fichier .csv à importer.

1. Cliquez sur **[!UICONTROL Check Data]** et effectuez l’importation.

![Importer des données de produit et des sources](assets/inventory-import-sources.png){width="600" zoomable="yes"}
