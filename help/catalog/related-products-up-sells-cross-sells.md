---
title: Paramètres du produit - [!UICONTROL Related Products, Up-Sells, and Cross-Sells]
description: Pour un produit, les paramètres de [!UICONTROL Related Products, Up-Sells, and Cross-Sells] définissent des blocs promotionnels simples sur la page du produit qui mettent en évidence une sélection de produits supplémentaires.
exl-id: 5bd65fad-4e55-40db-8702-10c366261565
feature: Catalog Management, Products, Page Content
TQID: https://experienceleague.adobe.com/J3CJ88ZZGgyukX9EwMHPtkdygTOAhbd41So4GurqEvA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 602
ht-degree: 0%

---

# Paramètres du produit - [!UICONTROL Related Products, Up-Sells, and Cross-Sells]

Utilisez la section _[!UICONTROL Related Products, Up-Sells, and Cross-Sells]_&#x200B;pour configurer des blocs promotionnels simples qui présentent une sélection de produits supplémentaires susceptibles d’intéresser le client. Pour plus d’informations, voir [Relations produit](../merchandising-promotions/product-relationships.md).

![Produits connexes, ventes incitatives et ventes croisées](./assets/product-related-up-sell-cross-sell.png){width="600" zoomable="yes"}

Chaque bloc est constitué d’une liste de produits appartenant à une option spécifique.

| Champ | Description |
|--- |--- |
| [!UICONTROL ID] | Identifiant numérique unique attribué à l’entité de produit. |
| [!UICONTROL Thumbnail] | Image miniature du produit. |
| [!UICONTROL Name] | Nom du produit. |
| [!UICONTROL Status] | Indique le statut du produit. Options : `Enabled` / `Disabled`. Les produits désactivés ne s’affichent pas dans les blocs sur le front-end. |
| [!UICONTROL Attribute Set] | Nom du jeu d’attributs utilisé comme modèle pour le produit. |
| [!UICONTROL SKU] | Unité de gestion des stocks unique affectée au produit. |
| [!UICONTROL Price] | Prix unitaire du produit. |
| [!UICONTROL Action] | Options : `Remove`. Supprime un produit du bloc. |

{style="table-layout:auto"}

>[!TIP]
>
>![](../assets/adobe-logo.svg) (Adobe Commerce uniquement) **Recommandations de produits optimisées par Adobe AI** simplifie le processus de définition des relations de produit en utilisant l’intelligence artificielle et des algorithmes de machine learning pour effectuer une analyse approfondie des données agrégées du visiteur. Ces données, lorsqu’elles sont combinées à votre catalogue Adobe Commerce, génèrent des expériences très attrayantes, pertinentes et personnalisées pour l’acheteur.
><br/>>Pour plus d’informations sur l’utilisation de cette extension développée par Adobe comme alternative aux recommandations de produits et aux ventes incitatives configurées manuellement, consultez le _[Guide de recommandations de produits](https://experienceleague.adobe.com/docs/commerce/product-recommendations/guide-overview.html)_.

## Produits connexes

Les produits associés sont destinés à être achetés en plus de l’article que le client consulte. Le client peut placer l’article dans son panier en cochant simplement la case. L’emplacement du bloc _Produits associés_ varie en fonction du thème et de la mise en page définis. Dans l’exemple ci-dessous, le bloc _Produits associés_ s’affiche au bas de la page _Vue des produits_. Avec une disposition à deux colonnes, le bloc _Produits associés_ apparaît souvent dans la barre latérale droite.

![Produits connexes](./assets/storefront-product-related-products.png){width="600" zoomable="yes"}

Pour configurer des produits associés :

1. Ouvrez le produit en mode d’édition.

1. Faites défiler vers le bas et développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** .

1. Cliquez sur **[!UICONTROL Add Related Products]**.

1. Utilisez les [contrôles de filtre](../getting-started/admin-grid-controls.md) pour rechercher les produits de votre choix.

1. Dans la liste, cochez la case de tout produit que vous souhaitez mettre en avant en tant que produit associé.

   ![Produits connexes](./assets/products-related-add.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Add Selected Products]**.

## Ventes incitatives

Les produits de montée en gamme sont des articles que votre client pourrait préférer au produit actuellement pris en compte. Un article proposé en tant que produit de mise en vente incitative peut être de meilleure qualité, plus populaire ou présenter une meilleure marge bénéficiaire. Les produits de montée en gamme apparaissent sur la page produit sous une en-tête telle que _Vous pouvez également être intéressé par les produits suivants_.

![Vendre À Un Prix Supérieur](./assets/storefront-product-upsell.png){width="600" zoomable="yes"}

Pour sélectionner des produits de mise à niveau :

1. Ouvrez le produit en mode d’édition.

1. Faites défiler vers le bas et développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** .

1. Cliquez sur **[!UICONTROL Add Up-Sell Products]**.

1. Utilisez les [contrôles de filtre](../getting-started/admin-grid-controls.md) pour rechercher les produits de votre choix.

1. Dans la liste, cochez la case de tout produit que vous souhaitez proposer comme produit de mise à niveau.

   ![Produits de montée en gamme](./assets/product-up-sell-add.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Add Selected Products]**.

>[!NOTE]
>
>Le produit parent groupé est toujours affiché automatiquement comme produit de mise à niveau pour tous ses produits enfants.

## Ventes croisées

Les articles de vente croisée sont similaires aux achats impulsifs placés près de la caisse dans la ligne de passage en caisse. Les produits proposés en tant que vente croisée apparaissent sur la page du panier, juste avant que le client ne commence le processus de passage en caisse.

>[!NOTE]
>
>Pour afficher ou masquer les articles de ventes croisées par affichage de magasin, reportez-vous à l’option [Passer en caisse > Panier](../configuration-reference/sales/checkout.md) appelée _[!UICONTROL Show Cross-sell Items]_&#x200B;dans le panier. Vous pouvez masquer les ventes croisées lors de ventes spécifiques ou pour les tests A/B dans une vue de magasin.

![Ventes croisées dans un panier](./assets/storefront-cart-cross-sells.png){width="600" zoomable="yes"}

**_Pour sélectionner des produits de vente croisée:_**

1. Ouvrez le produit en mode d’édition.

1. Faites défiler vers le bas et développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** .

1. Cliquez sur **[!UICONTROL Add Cross-Sell Products]**.

1. Utilisez les [contrôles de filtre](../getting-started/admin-grid-controls.md) pour rechercher les produits de votre choix.

1. Dans la liste, cochez la case de tout produit que vous souhaitez proposer comme produit de vente croisée.

   ![Produits de ventes croisées](./assets/product-cross-sell-add.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Add Selected Products]**.
