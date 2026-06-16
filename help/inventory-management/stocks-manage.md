---
title: Gérer le stock
description: Découvrez comment le stock est utilisé pour représenter un inventaire virtuel et agrégé de produits pour les sources de vos canaux de vente.
exl-id: 076b1325-2de4-46d3-9976-d900bd2cef47
TQID: https://experienceleague.adobe.com/IeG1bA1etAjxiDjSWY83GLNugllHT1mUrZBde45Ha8g
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
source-wordcount: 524
ht-degree: 0%

---

# Gestion des stocks

Stock représente un inventaire virtuel et agrégé de produits pour les sources de vos canaux de vente (sites web). Selon la configuration de votre site, le stock peut être affecté à un ou plusieurs canaux de vente. Un seul stock peut être affecté à chaque canal de vente, et un seul stock peut être affecté à plusieurs canaux de vente. Grâce au stock, vous pouvez modifier la hiérarchisation des sources utilisées lorsque les commandes passent par un canal de vente.

Commencez avec un Stock par défaut qui ne peut pas être supprimé ou désactivé. Vous pouvez ajouter des canaux de vente supplémentaires au stock uniquement. La seule source affectée est le Source par défaut. Ce stock est utilisé par les commerçants à source unique, les intégrations tierces et les produits importés.

Les canaux de vente représentent les entités qui vendent votre stock. Par défaut, [!DNL Commerce] fournit les sites web de votre boutique en tant que canaux de vente. Les canaux de vente peuvent être étendus pour prendre en charge d’autres canaux tels que les groupes de clients B2B et les vues de magasin. Chaque canal de vente ne peut être associé qu’à un seul Stock.

- **Assistance Sales Channel** - Les canaux de vente incluent actuellement des sites web prêts à l’emploi. Vous pouvez étendre les canaux de vente pour inclure des options personnalisées telles que les groupes de clients B2B et les vues de magasin. Chaque canal de vente ne peut être affecté qu’à un seul stock. Un seul stock peut être affecté à plusieurs canaux de vente.
- **Mapper aux sources** - Une ou plusieurs sources activées ou désactivées peuvent être attribuées à chaque stock, calculant l’inventaire virtuel agrégé par produit.
- **Exécution prioritaire des commandes** - L’algorithme de priorité prêt à l’emploi de l’algorithme de sélection Source utilise la liste source du stock, du haut vers le bas, lors de l’exécution des commandes.

Le diagramme suivant permet de définir le fonctionnement d’un stock par rapport aux sources et aux canaux de vente pour un marchand de bicyclette.

![Diagramme illustrant, par exemple, les stocks d’un magasin](assets/diagram-stock.png){width="600" zoomable="yes"}

## Exemples de stocks pour un VTT et magasin

Tous les magasins commencent par un Stock par défaut. Il doit rester `Enabled` pour les raisons suivantes :

- Il est utilisé lors de l’importation de nouveaux produits, attribuant automatiquement les produits à la source et au stock par défaut pour un accès immédiat aux [!DNL Inventory Management].
- Vous ne pouvez pas ajouter d’autres sources à ce stock au-delà du Source par défaut.
- Il est requis et utilisé par les commerçants à source unique, les produits groupés et les produits groupés.

Pour les commerçants multi-sources, créez et configurez des stocks pour mieux les adapter à vos magasins et exécuter vos commandes. Lorsque vous affectez un nouveau stock à un canal de vente, tout stock préexistant de ce canal de vente n’est pas affecté.

Dans le cas d’une installation multi-magasin, le Stock par défaut est initialement affecté au [Site web principal](../stores-purchase/stores.md#add-websites){target="_blank"} et au magasin par défaut. Le stock et les quantités corrects s’affichent pour les produits activés et désactivés dans la vue de grille **[!UICONTROL Products]**.

![Gérer les stocks](assets/inventory-stock.png){width="600" zoomable="yes"}

## Barre de boutons

| Bouton | Description |
|--|--|
| [!UICONTROL Add New Stock] | Ouvre le formulaire _[!UICONTROL New Stock]_&#x200B;utilisé pour entrer un nouveau stock de stock pour mapper le stock au canal de vente. |

## Gérer les descriptions des colonnes de stock

| Colonne | Description |
|--|--|
| [!UICONTROL ID] | Identifiant numérique unique généré pour l’entrée de stock. |
| [!UICONTROL Name] | Nom unique qui identifie le stock d’inventaire. |
| [!UICONTROL Sales Channels] | Définit la portée du stock en affectant le stock à des sites web spécifiques en tant que _canaux de vente_. |
| [!UICONTROL Assigned sources] | Origines affectées au stock qui fournit toutes les quantités de produit. |
| [!UICONTROL Action] | **[!UICONTROL Edit]** - Ouvre l&#39;enregistrement du stock en mode d&#39;édition. |
