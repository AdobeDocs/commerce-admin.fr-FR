---
title: Règle de prix de catalogue avec plusieurs SKU
description: Découvrez comment appliquer une règle de prix de catalogue unique à plusieurs SKU.
exl-id: 99023460-0501-45cd-8990-5f2b9ed7b4a2
feature: Merchandising, Price Rules, Catalog Management
TQID: https://experienceleague.adobe.com/nChe-8VA4V0nrC46PbeKyh7DB4Ta-0lpcezMV3uHEw0
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 367
ht-degree: 0%

---

# Règle de prix de catalogue avec plusieurs SKU

Une seule règle de prix de catalogue peut être appliquée à plusieurs SKU, ce qui permet de créer différentes promotions basées sur un produit, une marque ou une catégorie. Lors de la création de cette règle, vous devez définir des conditions correspondant aux SKU sélectionnés. Lors de la création de la règle, vous pouvez facilement parcourir et sélectionner des SKU à partir de la grille.

## Étape 1. Vérifier les propriétés storefront de l’attribut de produit

Avant de commencer, assurez-vous que les [Propriétés du storefront](../catalog/attribute-product-create.md#step-4-describe-the-storefront-properties) de l’attribut `sku` sont définies sur `Use in Promo Rules`.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Dans le filtre de recherche en haut de la colonne _[!UICONTROL Attribute Code]_, saisissez `sku` et cliquez sur **[!UICONTROL Search]**.

1. Cliquez pour ouvrir l’attribut `sku` en mode d’édition.

1. Dans le panneau de gauche, cliquez sur **[!UICONTROL Storefront Properties]** et assurez-vous que **[!UICONTROL Use for Promo Rule Conditions]** est défini sur `Yes`.

1. Si vous avez modifié la valeur de la propriété, cliquez sur **[!UICONTROL Save Attribute]**.

## Étape 2. Appliquer une règle de prix à plusieurs SKU

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**.

1. Effectuez l’une des opérations suivantes :

   - Suivez les instructions pour créer une [&#x200B; règle de prix de catalogue &#x200B;](price-rules-catalog.md).
   - Ouvrez une règle de prix de catalogue existante.

1. Développez ![Sélecteur de développement](../assets/icon-display-expand.png) la section **[!UICONTROL Conditions]**, puis procédez comme suit :

   - Dans la première ligne, définissez le premier paramètre sur `ANY`.

     ![Condition de règle de prix de catalogue - ANY](./assets/multiple-skus-condition1.png){width="600" zoomable="yes"}

   - Cliquez sur _Ajouter_ (![icône Ajouter](../assets/icon-add-green-circle.png)) au début de la ligne suivante et dans la liste sous **[!UICONTROL Product Attribute]**, cliquez sur `SKU`.

     ![Condition de règle de prix de catalogue - SKU est l’une des suivantes &#x200B;](./assets/multiple-skus-condition1a.png){width="600" zoomable="yes"}

   - Pour la comparaison, vous disposez d’options. Si vous souhaitez en localiser au moins un à partir d’une liste de SKU, `select is one of`. Si vous souhaitez localiser un groupe de SKU qui doivent tous être appliqués, sélectionnez `is`. Nous vous recommandons de sélectionner `is one of`.

     ![Condition de règle de prix de catalogue - SKU est l’une des suivantes &#x200B;](./assets/multiple-skus-condition1b.png){width="600" zoomable="yes"}

   - Pour remplir la condition, cliquez sur le lien Plus (**...**) et cliquez sur l’icône _Sélecteur_ (![Icône de liste](../assets/icon-list-chooser.png)) pour afficher la liste des produits disponibles.

     ![Condition de règle de prix de catalogue - plusieurs SKU](./assets/multiple-skus-condition2b.png){width="600" zoomable="yes"}

   - Parcourez, filtrez ou recherchez les SKU à ajouter. Dans la liste, cochez la case de chaque produit à inclure.

   - Cliquez sur **[!UICONTROL Save and Apply]** pour ajouter les SKU à la condition.

     ![Condition de règle de prix de catalogue - plusieurs SKU](./assets/multiple-skus-condition2.png){width="600" zoomable="yes"}

1. Renseignez la règle, y compris les [actions](price-rules-catalog.md) à entreprendre une fois les conditions remplies.

1. Une fois la règle terminée, cliquez sur **[!UICONTROL Save]**.

{{new-price-rule}}
