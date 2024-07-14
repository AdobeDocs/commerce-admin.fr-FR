---
title: Présentation du marchandisage visuel
description: Découvrez les outils de marchandisage visuel qui vous permettent de positionner des produits et de déterminer les produits qui apparaissent dans la liste de catégories.
exl-id: 00fe8b7f-0c33-4f06-a3cd-1f0bd18079f1
feature: Categories, Merchandising, Products
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Marchandisage visuel

{{ee-feature}}

Le _marchandiseur visuel_ est un ensemble d’outils avancés qui vous permettent de positionner des produits et d’appliquer des conditions qui déterminent quels produits apparaissent dans la liste de catégories. Le résultat peut être une sélection dynamique de produits qui s’adapte aux modifications du catalogue. Vous pouvez travailler en _mode visuel_, qui affiche chaque produit sous forme de mosaïque sur une grille, ou pour travailler à partir d’une liste de produits de la catégorie. Les mêmes outils sont disponibles dans chaque mode et vous pouvez utiliser les boutons situés dans le coin supérieur droit pour basculer entre chaque type d’affichage.

![Produits de catégorie dans la vue de mosaïque](./assets/category-products-visual-with-stock.png){width="600" zoomable="yes"}

## Accès à Visual Merchandiser

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Explorez l’arborescence des catégories et cliquez sur la catégorie à modifier.

1. Faites défiler l’écran vers le bas et développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Products in Category]** .

1. Cliquez sur le bouton _Afficher comme mosaïques_ ( ![Afficher comme mosaïques](../assets/icon-view-tiles.png) ) pour afficher les produits sous forme de grille.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Category]**.

## Modifier la position d’un produit

1. Utilisez l’ [ordre de tri](../catalog/navigation-product-listings.md) pour afficher le produit que vous souhaitez déplacer.

   - **Méthode 1 : glisser-déposer**

     Saisissez la commande _Faire glisser_ (![Faire glisser l’icône](../assets/icon-move.png)) dans le coin supérieur droit de la mosaïque du produit et placez le produit en position positionnée. Le nombre de chaque produit s’ajuste pour refléter la nouvelle position.

   - **Méthode 2 : définir la valeur de position**

     Dans le contrôleur _Position_ (![Champ de position](../assets/control-position.png)) sur la mosaïque du produit, saisissez le numéro où vous souhaitez que le produit apparaisse. Saisissez `0` pour placer le produit en haut de la liste.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Category]**.

>[!NOTE]
>
>Dans une installation propre, Adobe Commerce réserve l’ID de catégorie `2` pour le catalogue racine du magasin par défaut. Le marchandisage visuel ne peut utiliser que les catégories dont le numéro d’identification est `3` ou supérieur.

## Contrôles Workspace

| Contrôle | Description |
|--- |--- |
| ![Icône Afficher la liste](../assets/icon-view-list.png) | Afficher sous forme de liste |
| ![Icône Afficher en tant que mosaïques](../assets/icon-view-tiles.png) | Afficher sous forme de mosaïques |
| ![Bascule de correspondance par règle - no](../assets/toggle-no.png) | Correspondance par règle - non |
| ![Bascule de correspondance par règle - oui](../assets/toggle-yes.png) | Correspondance par règle - oui |
| ![Icône Déplacer](../assets/icon-move.png) | Glisser |
| ![Contrôleur de position](../assets/control-position.png) | Position |
| ![Icône Supprimer de la catégorie](../assets/icon-delete-x.png) | Supprimer de la catégorie |
| ![Éléments par contrôle de page](../assets/control-items-per-page.png) | Afficher par page |
| ![Modifier l’affichage de la page](../assets/control-page-display.png) | Aller à la page suivante / précédente |

{style="table-layout:auto"}
