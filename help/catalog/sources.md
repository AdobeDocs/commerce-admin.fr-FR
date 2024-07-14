---
title: Paramètres du produit - [!UICONTROL Sources]
description: Pour un produit, les paramètres [!UICONTROL Sources] permettent d’accéder aux sources  [!DNL Inventory Management]  à partir desquelles le produit peut être distribué.
exl-id: 986f6031-0edc-4105-aa02-1c22364b3e7c
feature: Catalog Management, Products, Inventory
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Paramètres du produit - [!UICONTROL Sources]

La section _[!UICONTROL Sources]_des paramètres du produit répertorie les sources à partir desquelles le produit peut être distribué. Il est utilisé pour affecter et annuler l’affectation des sources ainsi que pour gérer la quantité et la disponibilité du produit. Cette section s’affiche uniquement si plusieurs sources sont définies pour votre magasin. Pour plus d’informations sur les sources, voir [Gérer les sources](../inventory-management/sources-manage.md).

## Attribution d’une source à un produit

1. Cliquez sur **[!UICONTROL Assign Source]**.

1. Cochez la case correspondant aux sources requises.

1. Cliquez sur **[!UICONTROL Done]**.

1. Sélectionnez **[!UICONTROL Source Item Status]** et saisissez les valeurs **[!UICONTROL Qty]** et **[!UICONTROL Notify Qty]** si nécessaire.

1. Cliquez sur **[!UICONTROL Save]** pour enregistrer les modifications.

![Affichage des sources](./assets/catalog-sources-list.png){width="600" zoomable="yes"}

## Référence de champ

| Champ | Description |
|--- |--- |
| [!UICONTROL Name] | Nom unique d’une source. |
| [!UICONTROL Source Status] | Détermine si le produit est activé ou désactivé dans le catalogue. |
| [!UICONTROL Source Item Status] | Détermine la disponibilité actuelle du produit. Options : <br />**[!UICONTROL In Stock]**- Rend le produit disponible à l’achat.<br />**[!UICONTROL Out of Stock]** - À moins que les commandes en arrière-plan ne soient activées, empêche le produit d’être disponible à l’achat et supprime la liste du catalogue. |
| [!UICONTROL Qty] | Montants des stocks disponibles pour chaque source. |
| [!UICONTROL Notify Qty] | Montant de _Notifier pour la quantité_ pour cette source spécifique si `Notify Quantity Use Default` n&#39;est pas sélectionné. |
| [!UICONTROL Notify Qty Use Default] | Indique d’utiliser le paramètre par défaut pour _Notifier pour la quantité_ dans l’inventaire avancé du produit ou le paramètre global dans la configuration du magasin. Pour plus d’informations sur les paramètres d’inventaire avancés de votre produit, voir [Configuration des options avancées du produit](../inventory-management/product-options.md). |
| [!UICONTROL Actions] | Pour une source affectée, cliquez sur **[!UICONTROL Unassign]** pour rendre la source indisponible pour le produit. Pour une source non attribuée, cliquez sur **[!UICONTROL Assign Sources]** pour rendre une source disponible pour le produit. Pour plus d’informations sur les options [!UICONTROL Assign Sources], voir [Attribution de sources par produit](../inventory-management/sources-assign-per-product.md). |

{style="table-layout:auto"}
