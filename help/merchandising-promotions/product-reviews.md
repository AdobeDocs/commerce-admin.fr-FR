---
title: Examens de produits
description: Découvrez comment les évaluations de produits peuvent améliorer votre boutique et apporter plus de crédibilité à vos produits.
exl-id: 82f96b24-626f-4b2d-be42-3d655d08dfda
feature: Merchandising, Products
TQID: 'https://experienceleague.adobe.com/GVmMoMMhnS4nHjCoa-6ylW8ah5-itrJKXiK9GKrdHd8'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 58c984c2-e237-5c50-9718-500e40d1e82c
    internal-label: Merchandising
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 560b0b1584040e8d840645328cdea5e51bdca640
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 0%
---
# Examens de produits

Les évaluations de produits aident à créer un sentiment de communauté et sont considérées comme plus crédibles que tout ce que l&#39;argent de la publicité peut acheter. En fait, certains moteurs de recherche donnent aux sites qui ont publié des avis sur des produits un rang supérieur à ceux qui n&#39;en ont pas publié. Pour ceux qui trouvent votre site en recherchant un produit spécifique, une revue de produit est essentiellement la page de destination de votre boutique. Les évaluations de produits aident les gens à trouver votre magasin, à maintenir leur engagement et mènent souvent à des ventes.

Commerce comprend une fonctionnalité native de révision des produits que vous pouvez gérer à partir de l’administration. Vous pouvez également utiliser une extension du [Commerce Marketplace](../getting-started/commerce-marketplace.md) pour utiliser un système de gestion des révisions hébergé.

>[!NOTE]
>
>Les versions 2.4.0 à 2.4.3 d’Adobe Commerce et de Magento Open Source incluaient l’extension Yotpo développée par le fournisseur. À compter de la version 2.4.4, cette extension n’est plus fournie avec la version de base et doit être installée et mise à jour à partir de Commerce Marketplace. La Marketplace permet également d’accéder à la documentation actuelle fournie par le développeur d’extensions.
><br><br>
>Si l’extension groupée est activée et configurée, vous devez mettre à jour votre fichier composer.json dans le cadre du processus de mise à niveau vers la version 2.4.4 et pour gérer les mises à jour d’extension à l’avenir. Voir [Mettre à niveau les modules](https://experienceleague.adobe.com/en/docs/commerce-operations/upgrade-guide/modules/upgrade) dans le _Guide de mise à niveau_ pour plus d&#39;informations.

## Évaluations de produits sur le storefront

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

>[!NOTE]
>
>Cette section décrit les révisions de produits pour le storefront Luma dans Adobe Commerce sur les infrastructures cloud et Adobe Commerce On-Premise. Adobe Commerce as a Cloud Service n’inclut pas le storefront Luma. Par conséquent, l’activation de révisions de produit dans l’administration n’ajoute pas de fonctionnalités de révision à votre storefront. Au lieu de cela, vous devez utiliser la requête GraphQL [`reviews`](https://developer.adobe.com/commerce/webapi/graphql/schema/products/queries/reviews) pour récupérer les révisions et la mutation [`createProductReview`](https://developer.adobe.com/commerce/webapi/graphql/schema/products/mutations/create-review) pour créer des révisions.

Lorsque la fonction native Product Reviews est activée, les clients peuvent rédiger des avis sur n’importe quel produit de votre catalogue. Vous pouvez rédiger des avis depuis la page produit en cliquant sur :

- **Ajoutez votre évaluation** pour les produits ayant des évaluations existantes.

- **Soyez le premier à évaluer ce produit** pour les produits sans évaluation existante.

L’onglet [!UICONTROL Reviews] répertorie toutes les révisions en cours et le formulaire utilisé pour envoyer une révision.

Votre configuration détermine si les clients doivent ouvrir un compte dans votre boutique avant d’écrire des avis sur les produits ou s’ils peuvent envoyer des avis en tant qu’invités. Le fait d’obliger les réviseurs à ouvrir un compte empêche les envois anonymes et améliore la qualité des révisions.

![Exemple de storefront - Ajouter votre évaluation](./assets/storefront-review-this-product.png){width="700" zoomable="yes"}

Le nombre d’étoiles indique la note de satisfaction du produit. Les visiteurs peuvent cliquer sur le lien pour lire les avis et écrire les leurs. À titre d’incitation, les clients peuvent recevoir des points de récompense pour avoir envoyé une révision. Lorsqu’une révision est soumise, elle est envoyée à l’administrateur pour modération. Une fois approuvée, la révision est publiée dans votre boutique.

![Exemple de storefront - Onglet Révisions](./assets/storefront-reviews-tab.png){width="700" zoomable="yes"}

### [!UICONTROL My Product Reviews]

La section _[!UICONTROL My Product Reviews]_du tableau de bord du compte client répertorie tous les avis soumis par le client et dont la publication a été approuvée. Chaque résumé de révision comprend la date à laquelle la révision a été soumise, des liens vers la page du produit et des détails de révision.

![Mes évaluations de produits](./assets/account-dashboard-my-product-reviews.png){width="700" zoomable="yes"}

1. Dans la barre latérale de son compte, le client choisit **[!UICONTROL My Product Reviews]**.

1. Pour afficher la révision complète, cliquez sur **[!UICONTROL See Details]**.

   ![Consulter les détails](./assets/account-dashboard-my-product-reviews-details.png){width="700" zoomable="yes"}

## Activer les fonctionnalités de révision de produit

La fonction Révisions des produits Commerce est activée par défaut dans Adobe Commerce sur les infrastructures cloud et Adobe Commerce On-Premise. Elle est désactivée par défaut dans Adobe Commerce as a Cloud Service.

>[!NOTE]
>
>Pour modifier les valeurs par défaut de ces champs, vous devez d&#39;abord décocher les cases **[!UICONTROL Use system value]**.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et sélectionnez **[!UICONTROL Catalog]** sous-jacent.

1. Développez le sélecteur d’extension ![](../assets/icon-display-expand.png) dans la section **[!UICONTROL Product Reviews]**.

   ![Configuration du catalogue - Examens de produits Commerce](../configuration-reference/catalog/assets/catalog-product-reviews.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Enabled]** sur `Yes`.

   Ce paramètre permet de passer en revue les produits.

1. Définir **[!UICONTROL Allow Guests to Write Reviews]** sur `Yes`.

   Ce paramètre détermine si les clients doivent ouvrir un compte dans votre boutique pour pouvoir rédiger des avis sur des produits.

1. Une fois terminé, cliquez sur **[!UICONTROL Save Config]**.

## Créer des évaluations personnalisées

Grâce aux révisions de produit Commerce, les clients peuvent attribuer des évaluations lorsqu’ils soumettent une révision de produit. Les évaluations par défaut sont la qualité, le prix et la valeur. En outre, vous pouvez ajouter vos propres évaluations personnalisées. La moyenne des notes 5 étoiles qui apparaissent sur les pages du catalogue est calculée pour chaque produit.

![Exemple de storefront - évaluations personnalisées](./assets/attribute-custom-ratings-review.png){width="700" zoomable="yes"}

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Rating]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Rating]**.

   ![Administrateur - Évaluations](./assets/product-reviews-rating.png){width="700" zoomable="yes"}

1. Dans la section _[!UICONTROL Rating Title]_, saisissez **[!UICONTROL Default Value]**pour la nouvelle évaluation.

   Le cas échéant, saisissez également la traduction pour chaque vue de magasin.

   ![Paramètres du titre de la note](./assets/product-rating-title.png){width="600" zoomable="yes"}

1. Dans la section _Visibilité de l’évaluation_, définissez **[!UICONTROL Visibility In]** sur l’affichage du magasin où l’évaluation doit être utilisée.

   Pour sélectionner plusieurs vues de magasin, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et cliquez sur chaque élément.

   >[!NOTE]
   >
   >Les évaluations ne sont pas visibles, sauf si elles sont affectées à une vue de magasin.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre pour déterminer l&#39;ordre de cette évaluation lorsqu&#39;elle est répertoriée avec d&#39;autres.

1. Si vous souhaitez afficher votre évaluation sur le storefront, cochez la case **[!UICONTROL Is Active]**.

   ![Paramètres de visibilité des évaluations](./assets/product-rating-visibility.png){width="600" zoomable="yes"}

1. Une fois terminé, cliquez sur **[!UICONTROL Save Rating]**.

   L’évaluation moyenne de toutes les évaluations s’affiche pour chaque produit sur la page de la grille de produits du catalogue.

   ![Page De Catalogue](./assets/catalog-rating-page.png){width="700" zoomable="yes"}
