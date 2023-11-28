---
title: Paramètres du produit - [!UICONTROL Product Reviews]
description: Pour un produit, la variable [!UICONTROL Product Reviews] Les paramètres permettent d’accéder aux révisions envoyées pour le produit et de modifier l’état des révisions en attente.
exl-id: 9328c9f5-dcd4-4837-8902-39dc48cb8151
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Paramètres du produit - [!UICONTROL Product Reviews]

La variable _[!UICONTROL Product Reviews]_Cette section répertorie toutes les révisions que les clients ont soumises au sujet du produit. Cette section s’affiche avec les autres informations sur les produits uniquement après la première sauvegarde d’un nouveau produit. Pour plus d’informations, voir [Révisions de produit](../merchandising-promotions/product-reviews.md).

![Révisions de produit](./assets/product-review.png){width="600" zoomable="yes"}

## Référence de champ

| Champ | Description |
|--- |--- |
| [!UICONTROL ID] | Identifiant numérique unique généré pour l’entrée de révision de produit. |
| [!UICONTROL Created] | Date de publication de la révision |
| [!UICONTROL Status] | État de révision (`Pending`, `Approved`, ou `Not Approved`) |
| [!UICONTROL Title] | Titre de la révision |
| [!UICONTROL Nickname] | Le surnom de l’utilisateur qui a quitté la révision |
| [!UICONTROL Review] | Examen par le client du produit actuel |
| [!UICONTROL Visibility] | Visibilité dans les révisions de magasin |
| [!UICONTROL Type] | Type d’utilisateur qui a quitté la révision (`Guest` ou `Customer`) |
| [!UICONTROL Product] | Nom du produit révisé |
| [!UICONTROL SKU] | Unité de gestion des stocks unique affectée au produit |
| [!UICONTROL Action] | Ouvre le produit en mode édition. |

{style="table-layout:auto"}

## Modération des révisions pour un produit spécifique

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Recherchez le produit et ouvrez-le en mode d’édition.

1. Faites défiler l’écran jusqu’à _[!UICONTROL Product Reviews]_.

1. Cliquez sur **[!UICONTROL Edit]** pour une révision de produit avec `Pending` pour afficher et modifier les détails.

1. Définir l’état de révision :

   - Pour approuver une révision en attente, sélectionnez `Approved`.
   - Pour rejeter une révision, sélectionnez `Not Approved`.
   - Vous pouvez rétablir l’état de révision sur `Pending` à tout moment.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Review]**.

Révisions avec la fonction `Pending` et `Not Approved` les statuts ne s’affichent pas sur le storefront.
