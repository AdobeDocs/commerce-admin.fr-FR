---
title: Autorisations de catégorie
description: Découvrez comment utiliser les catégories pour contrôler l’affichage des prix des produits, déterminer les groupes de clients qui peuvent ajouter des produits au panier et spécifier la page d’entrée.
exl-id: d80a0545-918e-4c08-9f37-4aa3cd7771f4
feature: Catalog Management, Categories, Customers, Configuration
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 0%

---

# Autorisations de catégorie

{{ee-feature}}

L’accès aux catégories peut être limité à des groupes de clients spécifiques ou restreint entièrement. Vous pouvez contrôler l’affichage des prix des produits, déterminer les groupes de clients qui peuvent ajouter des produits au panier et spécifier la page d’entrée.

>[!NOTE]
>
>Les autorisations de catégorie ont une portée globale et, lorsqu’elles sont activées, limitent l’accès à chaque catégorie en fonction de ses autorisations individuelles. Par défaut, les autorisations de catégorie ne sont pas activées.

Par exemple, si vous vendez uniquement aux clients de gros, vous pouvez permettre à n’importe qui de parcourir le catalogue, mais afficher les prix et autoriser les achats uniquement pour les acheteurs du groupe de clients _Wholesale_. Dans l’exemple suivant, seuls les utilisateurs connectés ont accès à la catégorie &quot;Collections&quot;. Pour les invités, l&#39;option &quot;Collections&quot; n&#39;apparaît pas dans le menu principal.

![Les utilisateurs connectés voient la catégorie &quot;Collections&quot;](./assets/storefront-category-permissions-logged-in.png){width="600" zoomable="yes"}

Lorsqu’elle est activée, une nouvelle section _[!UICONTROL Category Permissions]_s’affiche sur la page Catégorie , ce qui vous permet d’appliquer l’accès nécessaire pour chaque catégorie. Vous pouvez ajouter plusieurs règles d’autorisation à chaque catégorie pour différents sites web et groupes de clients.

## Étape 1 : configuration des autorisations de catégorie

>[!IMPORTANT]
>
>Tous les [paramètres d&#39;autorisation de groupe](../configuration-reference/catalog/catalog.md#category-permissions) existants sont ignorés par **_toutes_** catégories dans le catalogue lorsque la fonction **_[!UICONTROL Shared Catalog]_** est activée. [!UICONTROL Shared Catalog] contrôle entièrement toutes les autorisations de catégorie dans le catalogue lorsqu’il est activé.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et sélectionnez **[!UICONTROL Catalog]** sous .

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Category Permissions]** .

   ![Autorisations de catégorie](../configuration-reference/catalog/assets/catalog-category-permissions.png){width="600" zoomable="yes"}

   Pour obtenir une liste détaillée de ces options, voir [Autorisations de catégorie](../configuration-reference/catalog/catalog.md#category-permissions) dans la _référence de configuration_.

1. Définissez **[!UICONTROL Enable]** sur `Yes`.

1. Définissez les autres options en fonction de ce que vous souhaitez autoriser ou restreindre dans votre boutique (voir les sections suivantes).

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous êtes invité à mettre à jour le cache, cliquez sur le lien **[!UICONTROL Cache Management]** dans le message système et suivez les instructions pour actualiser le cache.

### [!UICONTROL Allow Browsing Category]

Cette option s’applique à toutes les catégories du [site web](../getting-started/websites-stores-views.md).

Pour permettre aux membres d’un **_groupe de clients spécifique_** de parcourir les produits de catégorie, procédez comme suit :

1. Définissez **[!UICONTROL Allow Browsing Category]** sur `Specified Customer Groups`.

1. Dans la zone **[!UICONTROL Customer Groups]**, sélectionnez chaque groupe autorisé à parcourir les produits de la catégorie.

   Pour sélectionner plusieurs groupes, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée lorsque vous cliquez sur chaque groupe.

   ![Autoriser la navigation par groupe de clients de gros](./assets/category-permissions-allow-browsing-customer-groups.png){width="600" zoomable="yes"}

Pour **_restreindre l&#39;accès et la redirection vers une landing page_**, procédez comme suit :

1. Définissez **[!UICONTROL Allow Browsing Category]** sur `No, Redirect to Landing Page`.

1. Sélectionnez le **[!UICONTROL Landing Page]** où les visiteurs sont redirigés.

   ![Rediriger vers la page d’accueil](./assets/category-permissions-browse-category-landing-page.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Bien que le paramètre _[!UICONTROL Allow Browsing Category]_s’applique à toutes les catégories du site web, vous pouvez configurer une page d’entrée différente pour chaque vue de magasin.

### [!UICONTROL Display Product Prices]

Cette option s’applique à toutes les catégories du [site web](../getting-started/websites-stores-views.md).

Pour autoriser uniquement les membres de **_groupes de clients spécifiques_** à voir le prix des produits de la catégorie, procédez comme suit :

1. Définissez **[!UICONTROL Display Product Prices]** sur `Yes, for Specified Customer Groups`.

1. Dans la zone **[!UICONTROL Customer Groups]**, sélectionnez chaque groupe autorisé à voir le prix des produits de la catégorie.

   Pour sélectionner plusieurs groupes, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée lorsque vous cliquez sur chaque groupe.)

   ![Seul le groupe de clients de gros peut voir les prix](./assets/category-permissions-price-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Allow Adding to Cart]

Cette option s’applique à toutes les catégories du [site web](../getting-started/websites-stores-views.md).

Pour autoriser uniquement les membres de **_groupes de clients spécifiques_** à placer des produits de catégorie dans le panier, procédez comme suit :

1. Définissez **[!UICONTROL Allow Adding to Cart]** sur `Yes, for Specified Customer Groups`.

1. Dans la zone **[!UICONTROL Customer Groups]**, sélectionnez chaque groupe autorisé à ajouter au panier des produits de la catégorie.

   Pour sélectionner plusieurs groupes, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée lorsque vous cliquez sur chaque groupe.

   ![ Seul un groupe de clients de vente en gros peut placer un produit dans le panier ](./assets/category-permissions-cart-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Disallow Catalog Search]

Définissez cette option pour empêcher les membres d’un groupe de clients spécifique d’utiliser la recherche catalogue. Elle s’applique à toutes les catégories du [site web](../getting-started/websites-stores-views.md).

- Pour autoriser **_uniquement les clients connectés_** à utiliser la recherche catalogue, sélectionnez `NOT LOGGED IN`.

- Pour autoriser **_uniquement des groupes de clients spécifiques_** à utiliser la recherche catalogue, sélectionnez chaque groupe à exclure de l’utilisation de la recherche de catégorie.

  Pour sélectionner plusieurs groupes, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée lorsque vous cliquez sur chaque groupe.

  ![Recherche catalogue non autorisée pour le groupe client général](./assets/category-permissions-disallow-category-search.png){width="600" zoomable="yes"}

## Étape 2 : application des autorisations de catégorie

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Dans l&#39;arborescence des catégories, sélectionnez la catégorie cible.

1. Développez le ![sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Category Permissions]** sur la page et procédez comme suit :

   - Pour créer une règle d’autorisation, cliquez sur **[!UICONTROL New Permission]**.

     ![Section Autorisations de catégorie](./assets/category-permissions-section-admin.png){width="600" zoomable="yes"}

   - Sélectionnez les **[!UICONTROL Website]** et **[!UICONTROL Customer Group]** applicables.

   - Définissez les autorisations individuelles selon vos besoins.

   >[!NOTE]
   >
   >Lorsque l’autorisation `Browsing Category` = `Deny` est définie pour n’importe quelle catégorie parente, elle n’est pas affichée sur la [piste de chemin de navigation](navigation-breadcrumb-trail.md) de la page de catégorie enfant.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

>[!NOTE]
>
>Si des autorisations **_Autoriser_** sont définies pour `Root Category`, ces autorisations sont automatiquement appliquées à toutes les sous-catégories et à tous les produits dans `Catalog`. Si un produit est affecté à plusieurs catégories et qu’il dispose des autorisations **_Autoriser_** pour au moins une catégorie, il dispose automatiquement des mêmes autorisations **_Autoriser_** pour toutes les catégories attribuées.
