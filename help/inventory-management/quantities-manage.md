---
title: Gérer les quantités en stock
description: Découvrez comment attribuer des sources et des quantités pour de nouveaux produits ou modifier des produits existants.
exl-id: b3d4a4c0-725a-4e62-854f-efb6a5709f73
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/ykiHTLnzZGtJrRdp2wZvlL7YLbEb7iAiYlcbY8K7IX8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
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
source-wordcount: 325
ht-degree: 0%

---

# Gérer les quantités en stock

Les informations suivantes expliquent comment attribuer des sources et des quantités pour de nouveaux produits ou modifier des produits existants.

Lors de la création de produits, affectez des sources et des quantités. Voir [Création d’un produit](../catalog/product-create.md) pour obtenir des instructions complètes. Ces pages contiennent des informations provenant de sources uniques et multiples pour les sources et les quantités par source.

Lors du premier accès à une [!DNL Commerce] mise à niveau avec [!DNL Inventory Management], tous les produits et quantités sont affectés au Source par défaut. Lors de l’importation de nouveaux produits au moyen d’un fichier .csv, ils sont également affectés au Source par défaut.

Les commerçants à source unique et multi-sources peuvent mettre à jour les sources, les quantités en stock et les seuils par produit ou en bloc.

- Les commerçants à source unique peuvent mettre à jour les quantités de produits pour le Source par défaut. Cette quantité correspond au nombre total de produits disponibles à la vente.

- Les commerçants multi-sources peuvent attribuer plusieurs sources et quantités par produit pour chaque emplacement (entrepôts, magasins, chargeurs, etc.). Il est recommandé d&#39;ajouter des sources avant de définir les quantités en stock des produits.

Lorsque vous ajoutez des sources et des quantités à vos produits, vous pouvez afficher les montants via la grille de produits. Si vous disposez d’un grand nombre de sources, pointez sur la _[!UICONTROL Quantity per Source]_&#x200B;pour afficher la liste complète et défilable des sources avec les quantités actuelles.

![Quantités de produits par source](assets/inventory-product-quantity.png){width="600" zoomable="yes"}

Vous disposez des options suivantes pour affecter un stock aux produits :

- [Attribution de sources par produit](sources-assign-per-product.md) - Attribuez manuellement des sources par produit dans votre catalogue.

- [Affecter des quantités par produit](quantities-assign-per-product.md) - Ajoutez les montants du stock disponible à vos produits par origine. Ces informations sont spécifiques aux commerçants multi-sources.

- [Affectation et annulation d’affectation en bloc de sources](bulk-assignment.md) - Affectez des sources à des produits sélectionnés en tant qu’action en masse. Utilisez l’option [Transférer l’inventaire vers Source](inventory-transfer.md) si vous souhaitez transférer l’inventaire et supprimer l’origine.

- [Transférer les stocks vers Source](inventory-transfer.md) - Transférer en masse tous les stocks d&#39;une origine vers une destination.

- [Importation et exportation des quantités](inventory-import-export.md) - Utilisez les fonctionnalités d’importation et d’exportation pour mettre à jour plusieurs SKU de produit avec des sources et des quantités en stock.
