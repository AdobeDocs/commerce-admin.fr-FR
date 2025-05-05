---
title: Études de produits
description: Découvrez comment les révisions de produits peuvent améliorer votre boutique et apporter plus de crédibilité à vos produits.
exl-id: 82f96b24-626f-4b2d-be42-3d655d08dfda
feature: Merchandising, Products
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 0%

---

# Études de produits

Les avis sur les produits aident à créer un sentiment de communauté et sont considérés comme plus crédibles que n’importe quel argent publicitaire. En fait, certains moteurs de recherche donnent aux sites dont les avis sur les produits sont supérieurs à ceux qui n’en ont pas. Pour ceux qui trouvent votre site en recherchant un produit spécifique, la consultation d’un produit est essentiellement la page d’entrée de votre boutique. Les avis sur les produits aident les clients à trouver votre magasin, à rester actifs et souvent à générer des ventes.

Commerce comprend une fonctionnalité native de révisions des produits que vous pouvez gérer à partir de l’administrateur. Vous pouvez également utiliser une extension du [Commerce Marketplace](../getting-started/commerce-marketplace.md) pour utiliser un système de gestion des révisions hébergé.

>[!NOTE]
>
>Les versions 2.4.0 à 2.4.3 d’Adobe Commerce et de Magento Open Source comprenaient l’extension développée par le fournisseur Yotpo. À compter de la version 2.4.4, cette extension n’est plus fournie avec la version principale et doit être installée et mise à jour à partir du Commerce Marketplace. Le Marketplace permet également d’accéder à la documentation actuelle fournie par le développeur de l’extension.
><br><br>
>Si l’extension groupée est activée et configurée, vous devez mettre à jour votre fichier compositeur.json dans le cadre du processus de mise à niveau 2.4.4 et gérer les mises à jour de l’extension. Pour plus d’informations, voir [Mise à niveau de modules](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html?lang=fr) dans le _Guide de mise à niveau_ .

## Critiques de produits sur le storefront

Lorsque la fonction native Product Reviews est activée, les clients peuvent écrire des révisions pour n’importe quel produit de votre catalogue. Les révisions peuvent être écrites à partir de la page du produit en cliquant sur :

- **Ajoutez votre révision** pour les produits avec des révisions existantes.

- **Soyez le premier à consulter ce produit** pour les produits sans avis existant.

L’onglet [!UICONTROL Reviews] répertorie toutes les révisions en cours et le formulaire qui a été utilisé pour envoyer une révision.

Votre configuration détermine si les clients doivent ouvrir un compte avec votre boutique avant d’écrire des révisions de produit ou s’ils peuvent envoyer des révisions en tant qu’invités. L’obligation pour les réviseurs d’ouvrir un compte empêche les envois anonymes et améliore la qualité des révisions.

![Exemple de storefront - Ajouter votre révision](./assets/storefront-review-this-product.png){width="700" zoomable="yes"}

Le nombre d’étoiles indique la note de satisfaction du produit. Les visiteurs peuvent cliquer sur le lien pour lire les critiques et écrire les leurs. À titre d’incitation, les clients peuvent recevoir des points de récompense pour l’envoi d’une révision. Lorsqu’une révision est envoyée, elle est envoyée à l’administrateur pour modération. Une fois approuvée, la révision est publiée dans votre boutique.

![Exemple de storefront - Onglet Révisions](./assets/storefront-reviews-tab.png){width="700" zoomable="yes"}

### [!UICONTROL My Product Reviews]

La section _[!UICONTROL My Product Reviews]_&#x200B;du tableau de bord du compte client répertorie toutes les révisions soumises par le client et approuvées pour publication. Chaque résumé de révision comprend la date d’envoi de la révision, des liens vers la page du produit et des détails de révision.

![Mes révisions de produit](./assets/account-dashboard-my-product-reviews.png){width="700" zoomable="yes"}

1. Dans la barre latérale de leur compte, le client choisit **[!UICONTROL My Product Reviews]**.

1. Pour afficher la révision complète, cliquez sur **[!UICONTROL See Details]**.

   ![Détails de la révision](./assets/account-dashboard-my-product-reviews-details.png){width="700" zoomable="yes"}

## Activation des fonctionnalités de révision de produit

La fonction Révisions de produits Commerce est activée par défaut.

>[!NOTE]
>
>Pour définir ces champs sur `No` et désactiver les révisions des produits Commerce, vous devez cocher les cases **Utiliser la valeur système** .

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et sélectionnez **[!UICONTROL Catalog]** en dessous.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Product Reviews]** .

   ![Configuration du catalogue - Révisions de produits Commerce](../configuration-reference/catalog/assets/catalog-product-reviews.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Enabled]** sur `Yes`.

   Il s’agit du paramètre par défaut qui active les révisions de produits.

1. Définissez **[!UICONTROL Allow Guests to Write Reviews]** sur `Yes`.

   Il s’agit du paramètre par défaut qui détermine si les clients doivent ouvrir un compte avec votre boutique pour pouvoir écrire des révisions de produit.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

## Création d’évaluations personnalisées

Avec les révisions de produit Commerce, les clients peuvent attribuer des évaluations lorsqu’ils envoient une révision de produit. Les notations par défaut sont la qualité, le prix et la valeur. En outre, vous pouvez ajouter vos propres évaluations personnalisées. Les évaluations cinq étoiles qui apparaissent sur les pages du catalogue sont moyennes pour chaque produit.

![Exemple de storefront - évaluations personnalisées](./assets/attribute-custom-ratings-review.png){width="700" zoomable="yes"}

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Rating]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Rating]**.

   ![Admin - Évaluations](./assets/product-reviews-rating.png){width="700" zoomable="yes"}

1. Dans la section _[!UICONTROL Rating Title]_, saisissez le **[!UICONTROL Default Value]**&#x200B;correspondant à la nouvelle évaluation.

   Le cas échéant, saisissez également la traduction pour chaque vue de magasin.

   ![Paramètres du titre de notation](./assets/product-rating-title.png){width="600" zoomable="yes"}

1. Dans la section _Visibilité de l’évaluation_, définissez **[!UICONTROL Visibility In]** sur la vue du magasin où l’évaluation doit être utilisée.

   Pour sélectionner plusieurs vues de magasin, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque élément.

   >[!NOTE]
   >
   >Les évaluations ne sont pas visibles, sauf si elles sont affectées à une vue de magasin.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre de cette évaluation lorsqu’elle est répertoriée avec d’autres personnes.

1. Si vous souhaitez afficher votre évaluation sur le storefront, cochez la case **[!UICONTROL Is Active]** .

   ![Paramètres de visibilité de notation](./assets/product-rating-visibility.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Rating]**.

   La note moyenne de toutes les révisions s’affiche pour chaque produit sur la page de grille de produits du catalogue.

   ![Page de catalogue](./assets/catalog-rating-page.png){width="700" zoomable="yes"}
