---
title: Scénarios de message Stock
description: Découvrez la combinaison des paramètres de configuration qui contrôlent les messages de disponibilité du stock sur les pages de produits et dans les listes de produits sur les pages de catalogue.
exl-id: 63114305-e695-445b-91cd-9e0fb2729ec4
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/9kPHtr75C7PkM9vD-2-AeG8JnAfKAao0GKEH9MhkBbU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
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
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 353
ht-degree: 1%

---

# Scénarios de message Stock

Vous pouvez utiliser une combinaison de paramètres de configuration pour contrôler les messages de disponibilité du stock sur les pages de produits et dans les listes de produits sur les pages de catalogue.

![Produit groupé avec un message de « rupture de stock »](assets/storefront-out-of-stock-message.png){width="600" zoomable="yes"}

## Messages de stock de page de produit

Plusieurs variantes de messages sont disponibles pour la page produit, selon la combinaison des paramètres Gérer les stocks et Disponibilité des stocks .

### Exemple 1 : afficher le message de disponibilité

#### Scénario 1

Cette combinaison de paramètres entraîne l’affichage du message de disponibilité sur la page produit, en fonction de la disponibilité du stock de chaque produit.

| Options sur actions | Paramètre | Message |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` | |
| [!UICONTROL Manage Stock] | `Yes` | |
| [!UICONTROL Stock Availability] | `In Stock` | _[!UICONTROL Availability: In Stock]_ |
| | `Out of Stock` | _[!UICONTROL Availability: Out of Stock]_ |

#### Scénario 2

Lorsque le stock n’est pas géré pour un produit, cette combinaison de paramètres peut être utilisée pour afficher le message de disponibilité sur la page du produit.

| Options sur actions | Paramètre | Message |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` |  |
| [!UICONTROL Manage Stock] | `No` | _[!UICONTROL Availability: In Stock]_ |

### Exemple 2 : masquage du message de disponibilité

#### Scénario 1

Cette combinaison de paramètres de configuration et de produit empêche l’affichage du message de disponibilité sur la page du produit.

| Options sur actions | Paramètre | Message |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |
| [!UICONTROL Manage Stock] | `Yes` |  |
| [!UICONTROL Stock Availability] | `In Stock` | Aucune |
|  | `Out of Stock` | Aucune |

#### Scénario 2

Lorsque le stock n’est pas géré pour un produit, cette combinaison de paramètres de configuration et de produit empêche l’affichage du message de disponibilité sur la page du produit.

| Options sur actions | Paramètre | Message |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |
| [!UICONTROL Manage Stock] | `No` | Aucune |

## Messages de stock de page de catalogue

Les options d’affichage suivantes sont possibles pour les listes de catégories et de résultats de recherche, selon la disponibilité du produit et les paramètres de configuration.

![&#x200B; Message de rupture de stock sur la page Catégorie &#x200B;](assets/storefront-out-of-stock-catalog-page.png){width="600" zoomable="yes"}

### Exemple 1 : afficher le produit avec le message « En rupture de stock »

Cette combinaison de paramètres de configuration inclut les produits en rupture de stock dans les listes de catégories et de résultats de recherche, et affiche un message de rupture de stock.

| Options sur actions | Paramètre | Message |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `Yes` |  |
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` | _[!UICONTROL Out of stock]_ |
| [!UICONTROL Display Out of Stock Products] | `Yes` |  |
| [!UICONTROL Display product availability in stock in the frontend] | `No` | Aucune |

### Exemple 2 : affichage du produit sans message « En rupture de stock »

Cette combinaison de paramètres de configuration inclut les produits en rupture de stock dans les listes de catégories et de résultats de recherche, mais n’affiche pas de message.

| Options sur actions | Paramètre | Message |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `Yes` | Aucune |
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |

### Exemple 3 : masquer le produit jusqu’à sa remise en stock

Ce paramètre de configuration omet entièrement les produits en rupture de stock des listes de catégories et de résultats de recherche, jusqu’à ce qu’ils soient de nouveau en stock.

| Options sur actions | Paramètre | Message |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `No` | Aucune |
