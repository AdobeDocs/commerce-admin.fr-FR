---
title: Prix du niveau d'import
description: Découvrez comment exporter des données de tarification de niveau et importer des données mises à jour.
exl-id: b19d0208-68b3-45ba-9896-318e12ff4131
feature: Products, Data Import/Export
source-git-commit: 55b0672984ce8cdb853daf024299919beaf7ce0b
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---

# Prix du niveau d&#39;import

Plutôt que de saisir manuellement les [prix de niveau](../catalog/product-price-tier.md) pour chaque produit, il peut être plus efficace d&#39;[importer](data-import.md) les données de tarification. Avant de commencer, créez un fichier d’exemple de données de prix de niveau exporté que vous pouvez utiliser comme modèle.

![Exemple de vitrine - tarification à plusieurs niveaux](./assets/storefront-tier-pricing-water-bottle.png){width="700" zoomable="yes"}

## Etape 1 : exporter les données de prix du niveau

L’exemple suivant exporte les données de niveau de prix pour un seul produit. Vous pouvez ensuite utiliser les données exportées comme modèle pour les imports en masse de données de prix de niveau. Pour en savoir plus sur l’exportation de données de tarification avancées, voir [Données de tarification avancées](data-attributes-product.md#advanced-pricing-attributes).

![Prix par niveaux de produit](./assets/price-tier-customer-group-discount.png){width="600" zoomable="yes"}

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Sous _[!UICONTROL Export Settings]_, définissez **[!UICONTROL Entity Type]**sur `Advanced Pricing`.

1. Dans la grille **[!UICONTROL Entity Attributes]**, faites défiler l’écran jusqu’aux attributs SKU et procédez comme suit :

   - Pour les prix de niveau basés sur un pourcentage de réduction, saisissez le SKU de chaque produit à exporter, séparé par une virgule.

     ![Exportation de données - SKU de produit](./assets/price-tier-export-sku.png){width="600" zoomable="yes"}

   - Pour les prix de niveau basés sur un montant fixe, saisissez le SKU de chaque produit.

   - Faites défiler l’écran vers le bas et cliquez sur **[!UICONTROL Continue]**.

1. Recherchez le fichier d’exportation à l’emplacement des téléchargements de votre navigateur web et ouvrez-le.

   ![Exemple - exportation des données de prix du niveau de remise du groupe de clients](./assets/price-tier-customer-group-discount-export.png){width="600" zoomable="yes"}

**_Données de prix de niveau exporté_**

Les colonnes suivantes sont incluses dans les données exportées :

- `sku`
- `tier_price_website`
- `tier_price_customer_group`
- `tier_price_qty`
- `tier_price`
- `tier_price_value_type`

Vous utilisez les données exportées comme modèle pour importer des données de prix de niveau.

## Etape 2 : mettre à jour les données

1. Mettez à jour les données de prix de niveau pour chaque produit, si nécessaire.

   Tous les produits sans mise à jour des prix de niveau peuvent être supprimés du fichier CSV. Il n’est pas nécessaire de réimporter des produits qui n’ont pas changé.

1. **[!UICONTROL Save]** le fichier CSV mis à jour.

>[!NOTE]
>
>La taille d’un fichier d’importation ne peut pas dépasser 2 Mo.

## Etape 3 : Importer les données mises à jour

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Sous _Paramètres d’importation_, définissez **[!UICONTROL Entity Type]** sur `Advanced Pricing`.

1. Définissez **[!UICONTROL Import Behavior]** sur `Add/Update`.

1. Sous **[!UICONTROL File to Import]**, cliquez sur **[!UICONTROL Choose File]** et sélectionnez le fichier que vous avez préparé à importer à partir de votre répertoire.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Check Data]**.

1. Si le fichier est valide, cliquez sur **[!UICONTROL Import]**.

   Dans le cas contraire, corrigez chaque problème avec les données répertoriées dans le message, puis essayez de réimporter le fichier.
