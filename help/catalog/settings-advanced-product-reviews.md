---
title: Paramètres du produit - [!UICONTROL Product Reviews]
description: Pour un produit, les paramètres [!UICONTROL Product Reviews] permettent d’accéder aux révisions envoyées pour le produit et de modifier l’état des révisions en attente.
exl-id: 9328c9f5-dcd4-4837-8902-39dc48cb8151
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Paramètres du produit - [!UICONTROL Product Reviews]

La section _[!UICONTROL Product Reviews]_répertorie toutes les révisions que les clients ont envoyées sur le produit. Cette section s’affiche avec les autres informations sur les produits uniquement après la première sauvegarde d’un nouveau produit. Pour plus d’informations, voir [Product Review](../merchandising-promotions/product-reviews.md).

![Révisions de produits](./assets/product-review.png){width="600" zoomable="yes"}

## Référence de champ

| Champ | Description |
|--- |--- |
| [!UICONTROL ID] | Identifiant numérique unique généré pour l’entrée de révision de produit. |
| [!UICONTROL Created] | Date de publication de la révision |
| [!UICONTROL Status] | État de révision (`Pending`, `Approved` ou `Not Approved`) |
| [!UICONTROL Title] | Titre de la révision |
| [!UICONTROL Nickname] | Le surnom de l’utilisateur qui a quitté la révision |
| [!UICONTROL Review] | Examen par le client du produit actuel |
| [!UICONTROL Visibility] | Visibilité dans les révisions de magasin |
| [!UICONTROL Type] | Type d’utilisateur ayant quitté la révision (`Guest` ou `Customer`) |
| [!UICONTROL Product] | Nom du produit révisé |
| [!UICONTROL SKU] | Unité de gestion des stocks unique affectée au produit |
| [!UICONTROL Action] | Ouvre le produit en mode édition. |

{style="table-layout:auto"}

## Modération des révisions pour un produit spécifique

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Recherchez le produit et ouvrez-le en mode d’édition.

1. Accédez à la section _[!UICONTROL Product Reviews]_.

1. Cliquez sur **[!UICONTROL Edit]** pour une révision de produit avec l’état `Pending` afin d’afficher et de modifier les détails.

1. Définir l’état de révision :

   - Pour approuver une révision en attente, sélectionnez `Approved`.
   - Pour rejeter une révision, sélectionnez `Not Approved`.
   - Vous pouvez à tout moment restaurer l’état de révision en `Pending`.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Review]**.

Les révisions avec les états `Pending` et `Not Approved` ne s’affichent pas sur le storefront.
