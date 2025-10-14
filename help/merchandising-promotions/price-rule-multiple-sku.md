---
title: Règle de prix du catalogue avec plusieurs SKU
description: Découvrez comment appliquer une règle de prix de catalogue unique à plusieurs SKU.
exl-id: 99023460-0501-45cd-8990-5f2b9ed7b4a2
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# Règle de prix du catalogue avec plusieurs SKU

Une règle de prix de catalogue unique peut être appliquée à plusieurs SKU, ce qui permet de créer diverses promotions en fonction d’un produit, d’une marque ou d’une catégorie. Lors de la création de cette règle, vous souhaitez définir des conditions qui correspondent aux SKU sélectionnés. Lors de la création de la règle, vous pouvez facilement parcourir et sélectionner des SKU dans la grille.

## Étape 1. Vérification des propriétés storefront de l’attribut de produit

Avant de commencer, assurez-vous que les [Propriétés Storefront](../catalog/attribute-product-create.md#step-4-describe-the-storefront-properties) de l’attribut `sku` sont définies sur `Use in Promo Rules`.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Dans le filtre de recherche situé en haut de la colonne _[!UICONTROL Attribute Code]_, saisissez `sku` et cliquez sur **[!UICONTROL Search]**.

1. Cliquez pour ouvrir l’attribut `sku` en mode d’édition.

1. Dans le panneau de gauche, cliquez sur **[!UICONTROL Storefront Properties]** et assurez-vous que **[!UICONTROL Use for Promo Rule Conditions]** est défini sur `Yes`.

1. Si vous avez modifié la valeur de la propriété, cliquez sur **[!UICONTROL Save Attribute]**.

## Étape 2. Appliquer une règle de prix à plusieurs SKU

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**.

1. Effectuez l’une des opérations suivantes :

   - Suivez les instructions pour créer une [règle de prix de catalogue](price-rules-catalog.md).
   - Ouvrez une règle de prix de catalogue existante.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) et procédez comme suit :**[!UICONTROL Conditions]**

   - Dans la première ligne, définissez le premier paramètre sur `ANY`.

     ![Condition de règle de prix du catalogue - ANY](./assets/multiple-skus-condition1.png){width="600" zoomable="yes"}

   - Cliquez sur _Ajouter_ (![Ajouter une icône](../assets/icon-add-green-circle.png)) au début de la ligne suivante et, dans la liste sous **[!UICONTROL Product Attribute]**, cliquez sur `SKU`.

     ![Condition de règle de prix du catalogue - SKU est l’un des &#x200B;](./assets/multiple-skus-condition1a.png){width="600" zoomable="yes"}

   - Pour la comparaison, vous disposez d’options. Si vous souhaitez en trouver au moins une dans une liste de SKU, `select is one of`. Si vous souhaitez localiser un groupe de SKU que vous devez tous trouver pour appliquer, sélectionnez `is`. Nous vous recommandons de sélectionner `is one of`.

     ![Condition de règle de prix du catalogue - SKU est l’un des &#x200B;](./assets/multiple-skus-condition1b.png){width="600" zoomable="yes"}

   - Pour remplir la condition, cliquez sur le lien plus (**...**) et cliquez sur l’icône _Sélecteur_ (![Icône Liste](../assets/icon-list-chooser.png)) pour la liste des produits disponibles.

     ![Condition de règle de prix du catalogue - plusieurs SKU](./assets/multiple-skus-condition2b.png){width="600" zoomable="yes"}

   - Parcourez, filtrez ou recherchez les SKU à ajouter. Dans la liste, cochez la case de chaque produit à inclure.

   - Cliquez sur **[!UICONTROL Save and Apply]** pour ajouter les SKU à la condition.

     ![Condition de règle de prix du catalogue - plusieurs SKU](./assets/multiple-skus-condition2.png){width="600" zoomable="yes"}

1. Renseignez la règle, y compris les [actions](price-rules-catalog.md) à effectuer lorsque les conditions sont remplies.

1. Une fois la règle terminée, cliquez sur **[!UICONTROL Save]**.

{{new-price-rule}}
