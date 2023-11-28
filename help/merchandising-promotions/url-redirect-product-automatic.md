---
title: Redirections automatiques
description: Découvrez comment configurer les redirections automatiques à générer chaque fois que la clé d’URL d’un produit ou d’une catégorie change dans votre boutique Commerce.
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# Redirections automatiques

Votre magasin peut être configuré pour générer automatiquement une redirection permanente chaque fois que la clé d’URL d’un produit ou d’une catégorie change. Dans la section Optimisation du moteur de recherche , la case sous la clé URL indique si les redirections permanentes sont activées. Si votre boutique est déjà configurée pour rediriger automatiquement les URL du catalogue, une redirection est une mise à jour simple de la clé URL. Le processus de création d’une redirection automatique est le même pour les produits et les catégories.

>[!NOTE]
>
>Lorsque les redirections automatiques sont activées et que vous enregistrez une catégorie, toutes les réécritures de produit et de catégorie sont générées en temps réel et stockées dans des tables de base de données par défaut. Cela peut entraîner des problèmes de performances significatifs pour les catégories comportant de nombreux produits attribués. La solution consiste à modifier cette valeur par défaut et à ignorer la génération de réécritures d’URL de catégorie/produits pour les produits enregistrés dans la catégorie. Dans ce cas, les réécritures de produit sont générées uniquement pour l’URL canonique du produit.

## Configuration des redirections automatiques

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en-dessous.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Search Engine Optimization]** .

   ![Configuration du catalogue - optimisation du moteur de recherche](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]** to `Yes`.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

## Redirection automatique des URL de produit

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Recherchez le produit dans la liste et cliquez pour ouvrir l’enregistrement.

1. Développer ![Sélecteur d’extension ](../assets/icon-display-expand.png) la valeur **[!UICONTROL Search Engine Optimization]** .

   ![Optimisation du moteur de recherche de produits - redirection permanente](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. Pour **[!UICONTROL URL Key]**, procédez comme suit :

   - Assurez-vous que la variable **[!UICONTROL Create Permanent Redirect for old URL]** est sélectionnée. Si ce n’est pas le cas, suivez les instructions pour [activation des redirections automatiques](url-rewrite.md#configure-url-rewrites).

   - Mettez à jour le **[!UICONTROL URL Key]** si nécessaire, utilisez toutes les minuscules et les tirets non alignés à la fin entre ces caractères et non des espaces.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

1. Lorsque vous êtes invité à actualiser le cache, suivez les liens contenus dans le message situé en haut de l’espace de travail.

   La redirection permanente est désormais effective pour le produit et les URL de catégorie associées.

## Redirection automatique des URL de catégorie

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Recherchez la catégorie dans l&#39;arborescence et cliquez pour ouvrir l&#39;enregistrement.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Search Engine Optimization]** .

1. Pour **[!UICONTROL URL Key]**, procédez comme suit :

   - Assurez-vous que la variable **[!UICONTROL Create Permanent Redirect for old URL]** est sélectionnée. Si ce n’est pas le cas, suivez les instructions pour [activation des redirections automatiques](url-rewrite.md#configure-url-rewrites).

   - Mettez à jour le **[!UICONTROL URL Key]** si nécessaire, utilisez toutes les minuscules et les tirets non alignés à la fin entre ces caractères et non des espaces.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

1. Lorsque vous êtes invité à actualiser le cache, suivez les liens contenus dans le message situé en haut de l’espace de travail.

   La redirection permanente est désormais effective pour la catégorie et toutes les URL de produit associées.

## Ignorer la génération des réécritures d’URL de produit pour l’enregistrement de catégorie {#skip-rewrite}

>[!WARNING]
>
>La désactivation de la génération automatique de l’URL de catégorie/produit entraîne la suppression définitive de toutes les réécritures d’URL de type de catégorie/produit existantes, qui ne peuvent pas être restaurées. Cela peut entraîner des conflits d’URL de type catégorie/produit non résolus qui nécessitent une mise à jour manuelle de la clé d’URL pour être résolus.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en-dessous.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Search Engine Optimization]** .

1. Définir **[!UICONTROL Generate "category/product" URL Rewrites]** to `No`.

1. Dans la boîte de dialogue de confirmation, cliquez sur **[!UICONTROL OK]** pour confirmer la modification et la suppression des réécritures d’URL existantes.

   ![Désactivation des réécritures d’URL de catégorie/produit - Confirmez](./assets/seo-rewrite-off.png){width="350"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.
