---
title: Paramètres du produit - [!UICONTROL Product Reviews]
description: Pour un produit, les paramètres [!UICONTROL Product Reviews] donnent accès aux révisions envoyées pour le produit et modifient le statut des révisions en attente.
exl-id: 9328c9f5-dcd4-4837-8902-39dc48cb8151
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/GdeAB8bT8WjR9vSGjuD-h5I3O6vYNxyaaUQYAjjy8ME
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ccaac3a13a346ce192a724efb3384ef2d612c980
workflow-type: tm+mt
source-wordcount: 212
ht-degree: 0%

---

# Paramètres du produit - [!UICONTROL Product Reviews]

La section _[!UICONTROL Product Reviews]_&#x200B;répertorie toutes les critiques soumises par les clients à propos du produit. Cette section s’affiche avec les autres informations sur les produits uniquement après le premier enregistrement d’un nouveau produit. Pour plus d’informations, voir [Avis sur le produit](../merchandising-promotions/product-reviews.md).

![Avis sur les produits](./assets/product-review.png){width="600" zoomable="yes"}

## Référence du champ

| Champ | Description |
|--- |--- |
| [!UICONTROL ID] | ID numérique unique généré pour l’entrée de révision du produit |
| [!UICONTROL Created] | Date de publication du réexamen |
| [!UICONTROL Status] | Statut de révision (`Pending`, `Approved` ou `Not Approved`) |
| [!UICONTROL Title] | Titre de la révision |
| [!UICONTROL Nickname] | Surnom de l’utilisateur qui a quitté la révision |
| [!UICONTROL Review] | Avis du client sur le produit actuel |
| [!UICONTROL Visibility] | Visibilité dans les révisions de magasin |
| [!UICONTROL Type] | Type d’utilisateur qui a quitté la révision (`Guest` ou `Customer`) |
| [!UICONTROL Product] | Nom du produit révisé |
| [!UICONTROL SKU] | Unité de gestion des stocks unique affectée au produit |
| [!UICONTROL Action] | Ouvre le produit en mode d&#39;édition |

{style="table-layout:auto"}

## Modération des critiques pour un produit spécifique

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Recherchez le produit et ouvrez-le en mode d’édition.

1. Faites défiler l’écran jusqu’à la section _[!UICONTROL Product Reviews]_.

1. Cliquez sur **[!UICONTROL Edit]** pour une révision de produit avec `Pending` statut afin d’afficher et de modifier les détails.

1. Définir le statut de la révision :

   - Pour approuver une révision en attente, sélectionnez `Approved`.
   - Pour rejeter une révision, sélectionnez `Not Approved`.
   - Vous pouvez redéfinir le statut de révision sur `Pending` à tout moment.

1. Cliquez ensuite sur **[!UICONTROL Save Review]**.

Les révisions avec les statuts `Pending` et `Not Approved` ne sont pas affichées sur le storefront.

