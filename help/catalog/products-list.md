---
title: Liste de produits
description: Découvrez la page _[!UICONTROL Products]_ dans l’Admin, où vous pouvez créer des produits et modifier des produits existants.
exl-id: 47e14f72-017f-456a-8904-6d32ef47e6f1
feature: Catalog Management, Products, Admin Workspace
source-git-commit: 8bb91b80f8ba957676c654e984deb5704b777612
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---

# Liste de produits

Tous les produits du catalogue sont accessibles à partir de la page _[!UICONTROL Products]_&#x200B;de l’administrateur, où vous pouvez créer des produits et modifier des produits existants. Pour une installation multi-site, chaque site web peut proposer une sélection différente de produits à vendre depuis le même catalogue.

La liste _[!UICONTROL Products]_&#x200B;comprend tous les produits du catalogue, indique les sites web où ils sont disponibles et s’ils sont actuellement activés pour la vente. Dans les installations Adobe Commerce B2B avec [catalogues partagés](../b2b/catalog-shared.md) activés, la grille inclut une colonne qui indique quels produits ont une remise alternative dans un catalogue partagé.

Vous pouvez parcourir la liste page par page ou rechercher des produits spécifiques. Utilisez les [contrôles](../getting-started/admin-grid-controls.md) standard pour trier et filtrer la liste, et appliquez les [actions](../getting-started/admin-actions-control.md) aux produits sélectionnés.

![Grille de produits](./assets/products-grid.png){width="700" zoomable="yes"}

## Limiter l’affichage du produit

Pour améliorer les performances des catalogues volumineux, il est recommandé de limiter le nombre de produits affichés dans la grille. Vous pouvez limiter les grilles de produits affichées pour :

- Page Produits
- Ajouter des produits connexes/à vente anticipée/à vente croisée
- Ajout de produits à un produit groupé
- Ajout de produits au groupe
- Créer une commande (administrateur)

Ce paramètre de configuration pour la limitation d’affichage du produit est désactivé par défaut. En l’activant, vous pouvez limiter le nombre de produits dans la grille à une valeur spécifique. Si elle est activée et que le nombre de produits correspondants pour l’affichage de la grille est supérieur à la limite d’enregistrement, une collection limitée d’enregistrements est renvoyée. Lorsque la limite est atteinte, le nombre total d&#39;enregistrements trouvés, le nombre d&#39;enregistrements sélectionnés et les éléments de pagination n&#39;apparaissent pas dans l&#39;en-tête de la grille.

>[!NOTE]
>
>Si vous ne souhaitez pas que votre grille de produits soit limitée, utilisez les filtres plus précisément pour produire une collection comportant moins d’éléments que le nombre spécifié dans le champ _[!UICONTROL Records Limit]_.

**_Pour configurer la limitation de l’affichage des produits :_**

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Admin]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) de **[!UICONTROL Admin Grids]** et procédez comme suit :

   - Définissez **[!UICONTROL Limit Number of Products in Grid]** sur `Yes`.

   - (Facultatif) Saisissez une valeur dans le champ **[!UICONTROL Records Limit]** pour limiter le nombre de produits dans la grille à une valeur spécifique. La valeur minimale par défaut est `20000`.

   ![Paramètres de configuration des grilles d’administration](../configuration-reference/advanced/assets/admin-admin-grids.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

## Contrôles de page

| Contrôle | Description |
|--- |--- |
| [!UICONTROL Add Product] | Lance le processus de création d’un produit simple. Pour choisir un type de produit spécifique, cliquez sur la flèche vers le bas. Options : [[!UICONTROL Simple Product]](product-create-simple.md) / [[!UICONTROL Configurable Product]](product-create-configurable.md) / [[!UICONTROL Grouped Product]](product-create-grouped.md) / [[!UICONTROL Virtual Product]](product-create-virtual.md) / [[!UICONTROL Bundle Product]](product-create-bundle.md) / [[!UICONTROL Downloadable Product]](product-create-downloadable.md) / [[!UICONTROL Gift Card]](product-gift-card-create.md) |
| [!UICONTROL Actions] | Répertorie toutes les actions qui peuvent être appliquées aux produits sélectionnés de la liste. Pour appliquer une action à un produit ou à un groupe de produits, cochez la case dans la première colonne de chaque produit. Options : `Delete` / `Change Status` / `Update Attributes` / `Assign Inventory Source` / `Unassign Inventory Source` / `Transfer Inventory To Source` |
| [!UICONTROL Filters] | Lance une recherche catalogue en fonction des filtres actuels. |
| [!UICONTROL Default View] | Indique la disposition actuelle des colonnes de la grille. Si des colonnes de grille sont enregistrées, vous pouvez en choisir une autre. |
| [!UICONTROL Columns] | Répertorie toutes les actions qui peuvent être appliquées aux produits sélectionnés de la liste. Pour appliquer une action à un produit ou à un groupe de produits, cochez la case dans la première colonne de chaque produit. |
| [!UICONTROL Search by keyword] | La zone de recherche, située dans le coin supérieur gauche, est utilisée pour rechercher des produits par mot-clé. |
| [!UICONTROL Edit] | Ouvre le produit en mode d’édition. Vous pouvez effectuer la même opération en cliquant n’importe où sur la ligne. |

{style="table-layout:auto"}

## Colonnes par défaut

| Colonne | Description |
|--- |--- |
| (Case à cocher) | Sélection de plusieurs enregistrements à soumettre à une action. La case à cocher dans la première colonne de chaque enregistrement sélectionné est marquée. Options : <br/>**[!UICONTROL Select All]**- Sélectionne tous les enregistrements trouvés qui correspondent aux paramètres de filtre actuels.<br/>**[!UICONTROL Select All on This Page]** - Sélectionne uniquement les enregistrements trouvés sur la page active qui correspondent aux paramètres de filtre. |
| [!UICONTROL ID] | Numéro séquentiel unique attribué lorsqu’un nouveau produit est enregistré pour la première fois. |
| [!UICONTROL Thumbnail] | Affiche une miniature de l’image du produit principal. |
| [!UICONTROL Name] | Nom du produit. |
| [!UICONTROL Type] | Type de produit. |
| [!UICONTROL Attribute Set] | Nom du jeu d’attributs utilisé comme modèle pour le produit. |
| [!UICONTROL SKU] | Unité de gestion des stocks unique affectée au produit. |
| [!UICONTROL Price] | Prix unitaire du produit. |
| [!UICONTROL Quantity] | La quantité en stock. |
| [!UICONTROL Salable Quantity] | La somme de toutes les unités disponibles de ce produit. |
| [!UICONTROL Visibility] | Indique l’emplacement de visibilité du produit dans le catalogue. Options : `Not Visible Individually` / `Catalog` / `Search` / `Catalog, Search` |
| [!UICONTROL Status] | Indique le statut du produit. Options : `Enabled` et `Disabled` |
| [!UICONTROL Websites] | Indique les sites web sur lesquels le produit est disponible. |
| [!UICONTROL Action] | Ouvre le produit en mode Édition . |
| [!UICONTROL Shared Catalog] | ![Adobe Commerce B2B](../assets/b2b.svg) (Disponible avec [Adobe Commerce B2B](./b2b/../introduction.md) uniquement) Indique les catalogues partagés qui contiennent une tarification personnalisée pour le produit. |

{style="table-layout:auto"}

## Autres colonnes

| Colonne | Description |
|--- |--- |
| [!UICONTROL Short Description] | Brève description du produit. |
| [!UICONTROL Special Price From Date] | La première date de la promotion spéciale de prix. |
| [!UICONTROL Special Price To Date] | Dernière date de la promotion spéciale de prix. |
| [!UICONTROL Cost] | Le coût réel de l’article. |
| [!UICONTROL Manufacturer] | Le fabricant du produit. |
| [!UICONTROL Meta Keywords] | Métadonnées des mots-clés pour le produit. |
| [!UICONTROL Color] | Couleur du produit. |
| [!UICONTROL Set Product as New from Date] | La première date du produit défini en tant que nouvelle promotion. |
| [!UICONTROL Set Product as New to Date] | Dernière date du produit défini en tant que nouvelle promotion. |
| [!UICONTROL Active From / To] | Les dates de début et de fin du produit. |
| [!UICONTROL Layout] | Disposition du produit. |
| [!UICONTROL Minimum Advertised Price] | Prix minimum annoncé du produit. |
| [!UICONTROL Allow Gift Message] | Message cadeau aux clients qui achètent une carte-cadeau. |
| [!UICONTROL Special Price] | Prix spécial du produit. |
| [!UICONTROL Weight] | Le poids du produit. |
| [!UICONTROL Meta Title] | Métadonnées du produit. |
| [!UICONTROL Meta Description] | Description des métadonnées du produit. |
| [!UICONTROL Country of Manufacture] | Le pays de fabrication. |
| [!UICONTROL New Theme] | Application d’un thème personnalisé au produit |
| [!UICONTROL URL Key] | Clé URL du produit. |
| [!UICONTROL Tax Class] | Classe fiscale du produit. |
| [!UICONTROL Allow Gift Message] | Affiche la disponibilité de l’option de message cadeau pour le produit. |

{style="table-layout:auto"}
