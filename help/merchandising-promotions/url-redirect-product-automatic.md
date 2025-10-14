---
title: Redirections automatiques
description: Découvrez comment configurer les redirections automatiques à générer lorsque la clé URL d’un produit ou d’une catégorie change dans votre boutique Commerce.
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# Redirections automatiques

Votre boutique peut être configurée pour générer automatiquement une redirection permanente chaque fois que la clé URL d’un produit ou d’une catégorie change. Dans la section Optimisation du moteur de recherche , la case à cocher située sous la clé URL indique si les redirections permanentes sont activées. Si votre boutique est déjà configurée pour rediriger automatiquement les URL de catalogue, une redirection consiste simplement à mettre à jour la clé d’URL. Le processus de création d’une redirection automatique est le même pour les produits et les catégories.

>[!NOTE]
>
>Lorsque les redirections automatiques sont activées et que vous enregistrez une catégorie, toutes les réécritures de produit et de catégorie sont générées en temps réel et stockées dans les tables de base de données par défaut. Cela peut entraîner des problèmes de performances importants pour les catégories comportant de nombreux produits attribués. La solution consiste à modifier cette valeur par défaut et à ignorer la génération de réécritures d’URL de catégorie/produits pour les produits lors de l’enregistrement de la catégorie. Dans ce cas, les réécritures de produit ne sont générées que pour l’URL de produit canonique.

## Configurer les redirections automatiques

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en dessous.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Search Engine Optimization]** .

   ![Configuration du catalogue - Optimisation du moteur de recherche](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]** sur `Yes`.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.


>[!NOTE]
>
> Des réécritures d’URL peuvent être générées pour la vue du magasin ou de la portée du site web. Définissez la portée de la réécriture d’URL de l’administrateur sur **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;**[!UICONTROL Catalog]**>**[!UICONTROL Catalog]**>**[!UICONTROL Search Engine Optimization]**. Sélectionnez la portée dans le champ&#x200B;_[!UICONTROL Product URL Rewrite Scope]_ .

## Rediriger automatiquement les URL de produits

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Recherchez le produit dans la liste et cliquez pour ouvrir l’enregistrement.

1. Développez ![Sélecteur d’extension &#x200B;](../assets/icon-display-expand.png) la section **[!UICONTROL Search Engine Optimization]** .

   ![Optimisation du moteur de recherche de produits - redirection permanente](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. Par **[!UICONTROL URL Key]**, procédez comme suit :

   - Assurez-vous que la case **[!UICONTROL Create Permanent Redirect for old URL]** est cochée. Dans le cas contraire, suivez les instructions pour [activer les redirections automatiques](url-rewrite.md#configure-url-rewrites).

   - Mettez à jour le **[!UICONTROL URL Key]** selon vos besoins, en utilisant tous les caractères minuscules et les traits d’union entre ces caractères au lieu des espaces.

1. Cliquez ensuite sur **[!UICONTROL Save]**.

1. Lorsque vous êtes invité à actualiser le cache, suivez les liens du message en haut de l’espace de travail.

   La redirection permanente est désormais en vigueur pour le produit et toutes les URL de catégorie associées.

## Rediriger automatiquement les URL de catégorie

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Recherchez la catégorie dans l’arborescence et cliquez pour ouvrir l’enregistrement.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Search Engine Optimization]** .

1. Par **[!UICONTROL URL Key]**, procédez comme suit :

   - Assurez-vous que la case **[!UICONTROL Create Permanent Redirect for old URL]** est cochée. Dans le cas contraire, suivez les instructions pour [activer les redirections automatiques](url-rewrite.md#configure-url-rewrites).

   - Mettez à jour le **[!UICONTROL URL Key]** selon vos besoins, en utilisant tous les caractères minuscules et les traits d’union entre ces caractères au lieu des espaces.

1. Cliquez ensuite sur **[!UICONTROL Save]**.

1. Lorsque vous êtes invité à actualiser le cache, suivez les liens du message en haut de l’espace de travail.

   La redirection permanente est désormais en vigueur pour la catégorie et toutes les URL de produit associées.

## Ignorer la génération des réécritures d’URL de produit pour l’enregistrement de catégorie {#skip-rewrite}

>[!WARNING]
>
>La désactivation de la génération automatique des réécritures d’URL de catégorie/produit entraîne la suppression définitive de toutes les réécritures d’URL de catégorie/type de produit existantes, qui ne peuvent pas être restaurées. Cela peut potentiellement entraîner des conflits d’URL de catégorie/type de produit non résolus qui nécessitent une mise à jour manuelle de la clé d’URL.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en dessous.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Search Engine Optimization]** .

1. Définissez **[!UICONTROL Generate "category/product" URL Rewrites]** sur `No`.

1. Dans la boîte de dialogue de confirmation, cliquez sur **[!UICONTROL OK]** pour confirmer la modification et la suppression des réécritures d’URL existantes.

   ![Désactiver les réécritures d’URL de catégorie/produit - Confirmer](./assets/seo-rewrite-off.png){width="350"}

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
