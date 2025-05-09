---
title: Gérer les quantités d'inventaire
description: Découvrez comment attribuer des sources et des quantités pour de nouveaux produits ou modifier des produits existants.
exl-id: b3d4a4c0-725a-4e62-854f-efb6a5709f73
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Gérer les quantités d&#39;inventaire

Les informations suivantes expliquent comment attribuer des sources et des quantités pour de nouveaux produits ou modifier des produits existants.

Lors de la création de produits, affectez des sources et des quantités lors de la création de produits. Voir [Création d’un produit](../catalog/product-create.md) pour obtenir des instructions complètes. Ces pages contiennent des informations à source unique et multi-source pour les sources et les quantités par source.

Lors de l’accès initial à un [!DNL Commerce] mis à niveau avec [!DNL Inventory Management], tous les produits et toutes les quantités sont attribués au Source par défaut. Lors de l’importation de nouveaux produits via le fichier .csv , ils sont également affectés au Source par défaut.

Les marchands à source unique et multi-source peuvent mettre à jour les sources, les quantités d’inventaire et les seuils par produit ou en bloc.

- Les marchands à source unique peuvent mettre à jour les quantités de produits pour le Source par défaut. Cette quantité correspond au nombre total de produits disponibles à la vente.

- Les négociants multi-sources peuvent attribuer plusieurs sources et quantités par produit pour chaque emplacement (entrepôts, magasins, expéditeurs, etc.). Il est recommandé d’ajouter des sources avant de définir les quantités d’inventaire des produits.

Lors de l’ajout de sources et de quantités à vos produits, vous pouvez afficher les montants par le biais de la grille de produits. Si vous disposez d’un grand nombre de sources, passez la souris sur le _[!UICONTROL Quantity per Source]_&#x200B;pour afficher la liste complète et déroulante des sources avec les quantités actuelles.

![Quantités de produits par source](assets/inventory-product-quantity.png){width="600" zoomable="yes"}

Vous disposez des options suivantes pour affecter un inventaire aux produits :

- [Attribution de sources par produit](sources-assign-per-product.md) - Affectez manuellement des sources par produit dans votre catalogue.

- [Attribution de quantités par produit](quantities-assign-per-product.md) - Ajoutez des quantités de stock disponibles à vos produits par source. Ces informations sont spécifiques aux marchands multisource.

- [Affectation et annulation de l’attribution en bloc de sources](bulk-assignment.md) - Affectez des sources à des produits sélectionnés en tant qu’action de masse. Utilisez l’option [Transférer l’inventaire vers Source](inventory-transfer.md) si vous souhaitez transférer l’inventaire et supprimer la source.

- [Transfert de l’inventaire vers Source](inventory-transfer.md) - Transfert en masse de tous les stocks d’une source d’origine vers une source de destination.

- [Importation et exportation de quantités](inventory-import-export.md) - Utilisez les fonctionnalités d’importation et d’exportation pour mettre à jour plusieurs SKU de produits avec des sources et des quantités d’inventaire.
