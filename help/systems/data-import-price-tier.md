---
title: Importer les prix de niveau
description: Découvrez comment exporter des données de tarification de niveau et importer des données mises à jour.
exl-id: b19d0208-68b3-45ba-9896-318e12ff4131
feature: Products, Data Import/Export
TQID: https://experienceleague.adobe.com/8eyWhVu-RtuzEYG81xOyqsEFdbz0s7evB-UGepUGCNw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 346
ht-degree: 0%

---

# Importer les prix de niveau

Plutôt que de saisir manuellement les [prix de niveau](../catalog/product-price-tier.md) pour chaque produit, il peut être plus efficace d’[importer](data-import.md) les données de prix. Avant de commencer, créez un exemple de fichier de données de prix de niveau exportées que vous pouvez utiliser comme modèle.

![Exemple de storefront - tarification échelonnée](./assets/storefront-tier-pricing-water-bottle.png){width="700" zoomable="yes"}

## Étape 1 : Exporter les données de prix de niveau

L’exemple suivant exporte les données de tarification de niveau pour un seul produit. Vous pouvez ensuite utiliser les données exportées comme modèle pour les importations en bloc de données de prix de niveau . Pour en savoir plus sur l&#39;exportation de données de tarification avancée, voir [Données de tarification avancée](data-attributes-product.md#advanced-pricing-attributes).

![Tarification échelonnée du produit](./assets/price-tier-customer-group-discount.png){width="600" zoomable="yes"}

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Sous _[!UICONTROL Export Settings]_, définissez **[!UICONTROL Entity Type]**&#x200B;sur `Advanced Pricing`.

1. Dans la grille de **[!UICONTROL Entity Attributes]**, faites défiler l’écran jusqu’aux attributs de SKU et procédez comme suit :

   - Pour les prix de niveau basés sur un pourcentage de remise, saisissez le SKU de chaque produit à exporter, séparé par une virgule.

     ![Exportation de données - SKU du produit](./assets/price-tier-export-sku.png){width="600" zoomable="yes"}

   - Pour les prix de niveau basés sur un montant fixe, saisissez le SKU de chaque produit.

   - Faites défiler vers le bas et cliquez sur **[!UICONTROL Continue]**.

1. Recherchez le fichier d’exportation à l’emplacement de téléchargement de votre navigateur web et ouvrez le fichier.

   ![Exemple - données de prix de niveau de remise du groupe client exportées](./assets/price-tier-customer-group-discount-export.png){width="600" zoomable="yes"}

**_Données de prix de niveau exportées_**

Les colonnes suivantes sont incluses dans les données exportées :

- `sku`
- `tier_price_website`
- `tier_price_customer_group`
- `tier_price_qty`
- `tier_price`
- `tier_price_value_type`

Vous utilisez les données exportées comme modèle pour importer les données de prix de niveau .

## Etape 2 : Mise à jour des données

1. Mettez à jour les données de prix de niveau pour chaque produit, si nécessaire.

   Tous les produits sans mise à jour des prix du niveau peuvent être supprimés du fichier CSV. Il n’est pas nécessaire de réimporter des produits qui n’ont pas été modifiés.

1. **[!UICONTROL Save]** le fichier CSV mis à jour.

>[!NOTE]
>
>La taille d’un fichier d’importation ne peut pas dépasser 2 Mo.

## Étape 3 : importer les données mises à jour

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Sous _Paramètres d’importation_, définissez **[!UICONTROL Entity Type]** sur `Advanced Pricing`.

1. Définissez **[!UICONTROL Import Behavior]** sur `Add/Update`.

1. Sous **[!UICONTROL File to Import]**, cliquez sur **[!UICONTROL Choose File]** et sélectionnez le fichier que vous souhaitez importer depuis votre répertoire .

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Check Data]**.

1. Si le fichier est valide, cliquez sur **[!UICONTROL Import]**.

   Sinon, corrigez chaque problème avec les données répertoriées dans le message, puis réessayez d’importer le fichier.
