---
title: Autorisations de catégorie
description: Découvrez comment utiliser les catégories pour contrôler l’affichage des prix des produits, déterminer les groupes de clients qui peuvent ajouter des produits au panier et spécifier la page d’entrée.
exl-id: d80a0545-918e-4c08-9f37-4aa3cd7771f4
feature: Catalog Management, Categories, Customers, Configuration
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# Autorisations de catégorie

{{ee-feature}}

L’accès aux catégories peut être limité à des groupes de clients spécifiques ou restreint entièrement. Vous pouvez contrôler l’affichage des prix des produits, déterminer les groupes de clients qui peuvent ajouter des produits au panier et spécifier la page d’entrée.

>[!NOTE]
>
>Les autorisations de catégorie ont une portée globale et, lorsqu’elles sont activées, limitent l’accès à chaque catégorie en fonction de ses autorisations individuelles. Par défaut, les autorisations de catégorie ne sont pas activées.

Par exemple, si vous vendez uniquement aux clients de gros, vous pouvez permettre à n’importe qui de parcourir le catalogue, mais afficher les prix et autoriser les achats uniquement pour les acheteurs dans la variable _Vente en gros_ groupe de clients. Dans l’exemple suivant, seuls les utilisateurs connectés ont accès à la catégorie &quot;Collections&quot;. Pour les invités, l&#39;option &quot;Collections&quot; n&#39;apparaît pas dans le menu principal.

![Les utilisateurs connectés voient la catégorie Collections](./assets/storefront-category-permissions-logged-in.png){width="600" zoomable="yes"}

Lorsqu’elle est activée, une nouvelle _[!UICONTROL Category Permissions]_s’affiche sur la page Catégorie qui vous permet d’appliquer l’accès nécessaire pour chaque catégorie. Vous pouvez ajouter plusieurs règles d’autorisation à chaque catégorie pour différents sites web et groupes de clients.

## Étape 1 : configuration des autorisations de catégorie

>[!IMPORTANT]
>
>Toutes les [paramètres d’autorisation de groupe](../configuration-reference/catalog/catalog.md#category-permissions) sont ignorées par **_all_** catégories du catalogue lorsque la variable **_[!UICONTROL Shared Catalog]_** est activée. [!UICONTROL Shared Catalog] contrôle entièrement toutes les autorisations de catégorie dans le catalogue lorsqu’il est activé.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en-dessous.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Category Permissions]** .

   ![Autorisations de catégorie](../configuration-reference/catalog/assets/catalog-category-permissions.png){width="600" zoomable="yes"}

   Pour obtenir la liste détaillée de ces options, voir [Autorisations de catégorie](../configuration-reference/catalog/catalog.md#category-permissions) dans le _Référence de configuration_.

1. Définir **[!UICONTROL Enable]** to `Yes`.

1. Définissez les autres options en fonction de ce que vous souhaitez autoriser ou restreindre dans votre boutique (voir les sections suivantes).

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous y êtes invité, cliquez sur le bouton **[!UICONTROL Cache Management]** dans le message système et suivez les instructions pour actualiser le cache.

### [!UICONTROL Allow Browsing Category]

Cette option s’applique à toutes les catégories de la [site web](../getting-started/websites-stores-views.md).

Pour autoriser les membres d’une **_groupe de clients spécifique_** pour parcourir les produits de catégorie, procédez comme suit :

1. Définir **[!UICONTROL Allow Browsing Category]** to `Specified Customer Groups`.

1. Dans le **[!UICONTROL Customer Groups]** sélectionnez chaque groupe autorisé à parcourir les produits de la catégorie.

   Pour sélectionner plusieurs groupes, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée lorsque vous cliquez sur chaque groupe.

   ![Autoriser la navigation par groupe de clients de gros](./assets/category-permissions-allow-browsing-customer-groups.png){width="600" zoomable="yes"}

À **_restreindre l&#39;accès et la redirection vers une landing page ;_**, procédez comme suit :

1. Définir **[!UICONTROL Allow Browsing Category]** to `No, Redirect to Landing Page`.

1. Choisissez la **[!UICONTROL Landing Page]** où les visiteurs sont redirigés.

   ![Rediriger vers la page d’accueil](./assets/category-permissions-browse-category-landing-page.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Bien que la variable _[!UICONTROL Allow Browsing Category]_s’applique à toutes les catégories du site web, vous pouvez configurer une page d’entrée différente pour chaque vue de magasin.

### [!UICONTROL Display Product Prices]

Cette option s’applique à toutes les catégories de la [site web](../getting-started/websites-stores-views.md).

Pour n’autoriser que les membres de **_groupes de clients spécifiques_** pour connaître le prix des produits de la catégorie, procédez comme suit :

1. Définir **[!UICONTROL Display Product Prices]** to `Yes, for Specified Customer Groups`.

1. Dans le **[!UICONTROL Customer Groups]** sélectionnez chaque groupe autorisé à voir le prix des produits de la catégorie.

   Pour sélectionner plusieurs groupes, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée lorsque vous cliquez sur chaque groupe.)

   ![Seul un groupe de clients de vente en gros peut voir les prix](./assets/category-permissions-price-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Allow Adding to Cart]

Cette option s’applique à toutes les catégories de la [site web](../getting-started/websites-stores-views.md).

Pour n’autoriser que les membres de **_groupes de clients spécifiques_** pour placer des produits de catégorie dans le panier, procédez comme suit :

1. Définir **[!UICONTROL Allow Adding to Cart]** to `Yes, for Specified Customer Groups`.

1. Dans le **[!UICONTROL Customer Groups]** sélectionnez chaque groupe autorisé à ajouter au panier des produits de la catégorie.

   Pour sélectionner plusieurs groupes, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée lorsque vous cliquez sur chaque groupe.

   ![Seul un groupe de clients de vente en gros peut placer un produit dans le panier.](./assets/category-permissions-cart-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Disallow Catalog Search]

Définissez cette option pour empêcher les membres d’un groupe de clients spécifique d’utiliser la recherche catalogue. Il s’applique à toutes les catégories de la variable [site web](../getting-started/websites-stores-views.md).

- Pour autoriser **_uniquement les clients connectés ;_** pour utiliser la recherche catalogue, sélectionnez `NOT LOGGED IN`.

- Pour autoriser **_groupes de clients spécifiques_** pour utiliser la recherche catalogue, sélectionnez chaque groupe à exclure de l’utilisation de la recherche par catégorie.

  Pour sélectionner plusieurs groupes, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée lorsque vous cliquez sur chaque groupe.

  ![Recherche catalogue non autorisée pour le groupe de clients Général](./assets/category-permissions-disallow-category-search.png){width="600" zoomable="yes"}

## Étape 2 : application des autorisations de catégorie

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Dans l&#39;arborescence des catégories, sélectionnez la catégorie cible.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Category Permissions]** sur la page et procédez comme suit :

   - Pour créer une règle d’autorisations, cliquez sur **[!UICONTROL New Permission]**.

     ![Section Autorisations de catégorie](./assets/category-permissions-section-admin.png){width="600" zoomable="yes"}

   - Choisissez le **[!UICONTROL Website]** et **[!UICONTROL Customer Group]**.

   - Définissez les autorisations individuelles selon vos besoins.

   >[!NOTE]
   >
   >When `Browsing Category` = `Deny` L’autorisation est définie pour n’importe quelle catégorie parente ; elle n’est pas affichée sur la page [Chemin de navigation](navigation-breadcrumb-trail.md) sur la page de catégorie enfant.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

>[!NOTE]
>
>Si **_Autoriser_** les autorisations sont définies pour la variable `Root Category`, ces autorisations sont alors automatiquement appliquées à toutes les sous-catégories et à tous les produits de la variable `Catalog`. Si un produit est affecté à plusieurs catégories et qu’il comporte la variable **_Autoriser_** autorisations pour au moins une catégorie, elle possède automatiquement la même **_Autoriser_** autorisations pour toutes les catégories affectées.
