---
title: Gérer le stock
description: Découvrez comment le stock est utilisé pour représenter un inventaire virtuel et agrégé de produits pour les sources de vos canaux de vente.
exl-id: 076b1325-2de4-46d3-9976-d900bd2cef47
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Gérer le stock

Stock représente un inventaire virtuel et agrégé de produits pour les sources de vos canaux de vente (sites web). Selon la configuration de votre site, le stock peut être affecté à un ou plusieurs canaux de vente. Un seul stock peut être affecté à chaque canal de vente et un seul stock peut être affecté à plusieurs canaux de vente. Grâce au stock, vous pouvez modifier la priorité des sources utilisées lorsque les commandes arrivent par le biais d&#39;un canal de vente.

Vous commencez avec un Stock par défaut qui ne peut pas être supprimé ou désactivé. Vous pouvez ajouter des canaux de vente supplémentaires au stock uniquement. La seule source affectée est la source par défaut. Ce stock est utilisé par les marchands à source unique, les intégrations tierces et les produits importés.

Les Sales Channel représentent les entités qui vendent votre stock. Par défaut, [!DNL Commerce] fournit vos sites web de magasin en tant que canaux de vente ; Les canaux de vente peuvent être étendus afin de prendre en charge d’autres canaux, tels que les groupes de clients B2B et les vues de magasin. Chaque canal de vente ne peut être associé qu’à un seul Stock.

- **Prise en charge des Sales Channel** - Les canaux de vente incluent actuellement des sites web prêts à l’emploi. Vous pouvez étendre les canaux de vente afin d’inclure des options personnalisées telles que les groupes de clients B2B et les vues de magasin. Un seul stock peut être affecté à chaque canal de vente. Un seul stock peut être affecté à plusieurs canaux de vente.
- **Mapper aux sources** - Une ou plusieurs sources activées ou désactivées peuvent être affectées à chaque stock, en calculant l’inventaire agrégé virtuel par produit.
- **Exécution des commandes prioritaires** - L’algorithme Priorité prêt à l’emploi de l’algorithme de sélection de la source utilise la liste source du stock de haut en bas lors de l’exécution des commandes.

Le diagramme suivant permet de définir le fonctionnement d’un stock par rapport aux sources et aux Sales Channel pour un vendeur de vélos.

![Diagramme par exemple les stocks pour un magasin](assets/diagram-stock.png){width="600" zoomable="yes"}

## Exemples de stocks pour un VTT et un magasin

Tous les magasins commencent par un Stock par défaut. Elle doit rester `Enabled` pour les raisons suivantes :

- Il est utilisé lors de l’import de nouveaux produits, en attribuant automatiquement les produits à la source et au stock par défaut pour un accès immédiat à [!DNL Inventory Management].
- Vous ne pouvez pas ajouter à ce stock des sources supplémentaires au-delà de la source par défaut.
- Elle est requise et utilisée par les marchands à source unique, les produits groupés et les produits regroupés.

Pour les commerçants multi-sources, créez et configurez des stocks afin qu’ils s’adaptent le mieux à vos magasins et à l’exécution des commandes. Lorsque vous attribuez un nouveau stock à un canal de vente, tout stock préexistant de ce canal de vente n’est plus attribué.

Dans le cas d’une installation multi-magasin, le stock par défaut est initialement attribué à la variable [Site web principal](../stores-purchase/stores.md#add-websites){target="_blank"} et magasin par défaut. Le stock et les quantités corrects s’affichent pour les produits activés et désactivés dans le **[!UICONTROL Products]** vue grid.

![Gérer Stock](assets/inventory-stock.png){width="600" zoomable="yes"}

## Barre de boutons

| Bouton | Description |
|--|--|
| [!UICONTROL Add New Stock] | Ouvre la _[!UICONTROL New Stock]_formulaire utilisé pour saisir un nouveau stock de stock afin de mapper le stock au canal des ventes. |

## Gestion des descriptions des colonnes Stock

| Colonne | Description |
|--|--|
| [!UICONTROL ID] | Identifiant numérique unique généré pour la saisie de stock. |
| [!UICONTROL Name] | Nom unique qui identifie le stock de stock. |
| [!UICONTROL Sales Channels] | Définit la portée du stock en attribuant le stock à des sites web spécifiques en tant que _canaux de vente_. |
| [!UICONTROL Assigned sources] | Sources affectées au stock qui fournissent toutes les quantités de produits. |
| [!UICONTROL Action] | **[!UICONTROL Edit]** - Ouvre l’enregistrement de stock de stock de stock en mode d’édition. |
