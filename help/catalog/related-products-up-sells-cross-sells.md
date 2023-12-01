---
title: Paramètres du produit - [!UICONTROL Related Products, Up-Sells, and Cross-Sells]
description: Pour un produit, la variable [!UICONTROL Related Products, Up-Sells, and Cross-Sells] les paramètres définissent des blocs promotionnels simples sur la page produit qui mettent en évidence une sélection de produits supplémentaires.
exl-id: 5bd65fad-4e55-40db-8702-10c366261565
feature: Catalog Management, Products, Page Content
source-git-commit: f6d52b1a3c8dd411ad3aa7c6027e964f9d49d608
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# Paramètres du produit - [!UICONTROL Related Products, Up-Sells, and Cross-Sells]

Utilisez la variable _[!UICONTROL Related Products, Up-Sells, and Cross-Sells]_pour configurer des blocs promotionnels simples qui présentent une sélection de produits supplémentaires pouvant intéresser le client. Pour plus d’informations, voir [Relations entre les produits](../merchandising-promotions/product-relationships.md).

![Produits associés, ventes consécutives et ventes croisées](./assets/product-related-up-sell-cross-sell.png){width="600" zoomable="yes"}

Chaque bloc est constitué d&#39;une liste de produits appartenant à une option spécifique.

| Champ | Description |
|--- |--- |
| [!UICONTROL ID] | Identifiant numérique unique attribué à l’entité de produit. |
| [!UICONTROL Thumbnail] | Image miniature du produit. |
| [!UICONTROL Name] | Nom du produit. |
| [!UICONTROL Status] | Indique l’état du produit. Options : `Enabled` / `Disabled`. Les produits désactivés ne s’affichent pas dans les blocs du front-end. |
| [!UICONTROL Attribute Set] | Nom du jeu d’attributs utilisé comme modèle pour le produit. |
| [!UICONTROL SKU] | Unité de gestion des stocks unique affectée au produit. |
| [!UICONTROL Price] | Prix unitaire du produit. |
| [!UICONTROL Action] | Options : `Remove`. Supprime un produit du bloc. |

{style="table-layout:auto"}

>[!TIP]
>
>![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) **Recommendations produit optimisé par Adobe Sensei** simplifie le processus de définition des relations entre les produits en utilisant l’intelligence artificielle et des algorithmes d’apprentissage automatique afin d’effectuer une analyse approfondie des données agrégées sur les visiteurs. Ces données, lorsqu’elles sont combinées à votre catalogue Adobe Commerce, génèrent des expériences hautement attrayantes, pertinentes et personnalisées pour l’acheteur.
><br/>
>Pour plus d’informations sur l’utilisation de cette extension développée par l’Adobe comme alternative aux recommandations de produits configurées manuellement et aux ventes incitatives, voir la section _[Guide Recommendations du produit](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html)_.

## Produits associés

Les produits associés sont destinés à être achetés en plus de l’article que le client consulte. Le client peut placer l’article dans le panier en cliquant simplement sur la case à cocher. L’emplacement de la variable _Produits associés_ varie en fonction du thème défini et de la mise en page. Dans l’exemple ci-dessous, la variable _Produits associés_ s’affiche au bas du _Consultation produit_ page. Avec une mise en page à deux colonnes, la variable _Produits associés_ s’affiche souvent dans la barre latérale droite.

![Produits associés](./assets/storefront-product-related-products.png){width="600" zoomable="yes"}

Pour configurer les produits associés :

1. Ouvrez le produit en mode d’édition.

1. Faire défiler vers le bas et développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** .

1. Cliquez sur **[!UICONTROL Add Related Products]**.

1. Utilisez la variable [contrôles de filtre](../getting-started/admin-grid-controls.md) pour trouver les produits que vous voulez.

1. Dans la liste, cochez la case d’un produit que vous souhaitez afficher comme produit associé.

   ![Produits associés](./assets/products-related-add.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Add Selected Products]**.

## Valeurs nues

Les produits de vente incitative sont des articles que votre client peut préférer au lieu du produit actuellement considéré. Un article proposé en tant que vente incitative peut être de meilleure qualité, plus populaire ou avoir une meilleure marge bénéficiaire. Les produits de vente incitative apparaissent sur la page de produits sous un en-tête tel que _Les produits suivants peuvent également vous intéresser :_.

![Vente en amont](./assets/storefront-product-upsell.png){width="600" zoomable="yes"}

Pour sélectionner des produits de vente incitative :

1. Ouvrez le produit en mode d’édition.

1. Faire défiler vers le bas et développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** .

1. Cliquez sur **[!UICONTROL Add Up-Sell Products]**.

1. Utilisez la variable [contrôles de filtre](../getting-started/admin-grid-controls.md) pour trouver les produits que vous voulez.

1. Dans la liste, cochez la case d’un produit que vous souhaitez présenter comme un produit de vente incitative.

   ![Vente de produits](./assets/product-up-sell-add.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Add Selected Products]**.

>[!NOTE]
>
>Le produit du lot parent s’affiche toujours automatiquement sous la forme d’un produit de vente incitative pour tous ses produits enfants.

## Ventes croisées

Les articles de ventes croisées sont similaires aux achats impulsifs positionnés à côté de la caisse dans la ligne de passage en caisse. Les produits proposés sous la forme d’une vente croisée apparaissent sur la page du panier, juste avant que le client ne commence le processus de passage en caisse.

>[!NOTE]
>
>Pour afficher ou masquer les articles de ventes croisées par vue de magasin, reportez-vous à la section [Passage en caisse > Panier](../configuration-reference/sales/checkout.md) option appelée _[!UICONTROL Show Cross-sell Items]_dans le panier. Vous pouvez masquer les ventes croisées lors de ventes spécifiques ou pour les tests A/B dans une vue de magasin.

![Ventes croisées dans le panier](./assets/storefront-cart-cross-sells.png){width="600" zoomable="yes"}

**_Pour sélectionner des produits de vente croisée :_**

1. Ouvrez le produit en mode d’édition.

1. Faire défiler vers le bas et développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** .

1. Cliquez sur **[!UICONTROL Add Cross-Sell Products]**.

1. Utilisez la variable [contrôles de filtre](../getting-started/admin-grid-controls.md) pour trouver les produits que vous voulez.

1. Dans la liste, cochez la case d’un produit que vous souhaitez présenter comme un produit de vente croisée.

   ![Produits de vente croisée](./assets/product-cross-sell-add.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Add Selected Products]**.
