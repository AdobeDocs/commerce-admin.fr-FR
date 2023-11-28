---
title: '[!DNL Google Content Experiments]'
description: Découvrez comment utiliser [!DNL Google Content Experiments] pour configurer un test A/B des produits de commerce, des catégories ou des pages de contenu.
exl-id: ae03bc5a-de84-4dad-932e-e79e509feebe
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# [!DNL Google Content Experiments]

L’exemple suivant montre comment configurer un test A/B de produits, de catégories ou de pages de contenu à l’aide d’expériences de contenu Google Analytics. Nous vous recommandons de garder deux onglets de navigateur ouverts lors de l’utilisation des instructions, car vous devez faire des allers-retours entre l’administrateur Commerce et votre [!DNL Google Analytics] compte .

>[!NOTE]
>
>[!DNL Google Content Experiments] a été abandonné et est programmé pour être remplacé par [Google Optimization](https://support.google.com/optimize/answer/7084762?hl=en).

## Étape 1. Activation des expériences de contenu (Commerce)

1. Connectez-vous à l’administrateur de votre installation Commerce.

1. Suivez les instructions pour activer [Google Analytics](google-analytics.md) avec des expériences de contenu dans la configuration Commerce.

   ![Configuration des ventes - API Google - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

## Étape 2. Configuration des variations (Commerce)

Créez plusieurs variantes d’un même produit, d’une même catégorie ou d’une même page.

- Chaque variation doit avoir une valeur unique. [Clé URL](../catalog/catalog-urls.md).
- Chaque variation doit avoir le même [vue de magasin](../getting-started/websites-stores-views.md#scope-settings) sélectionné.

Vous pouvez créer jusqu’à dix variantes de chaque entité que vous souhaitez tester. Pour les produits, utilisez [Enregistrer et dupliquer](../catalog/product-workspace.md) pour gagner du temps.

## Étape 3. Configuration de l’expérience (Google)

>[!NOTE]
>
>Pour créer une expérience, vous devez disposer des autorisations appropriées pour le compte Google.

1. Ouvrez un autre onglet du navigateur et connectez-vous à [Google Analytics][2] compte .

   Si nécessaire, accédez au **[!UICONTROL Account]** et **[!UICONTROL Property]**.

1. Dans la barre latérale gauche, choisissez **[!UICONTROL Admin]** et utilisez l’une des méthodes suivantes :

   **Méthode 1 :** Choisir une vue existante

   Dans l’en-tête de la fonction _[!UICONTROL View]_, cliquez sur la flèche vers le bas, puis sélectionnez la vue qui doit fournir les données de l’expérience.

   **Méthode 2 :** Création d’une vue de création de rapports

   - Dans l’en-tête de la fonction _Affichage_ colonne, cliquez sur **[!UICONTROL Create View]** et procédez comme suit :

      - Identifiez l’emplacement de l’expérience comme suit : `Website` ou `Mobile app`.

      - Saisissez un texte descriptif. **[!UICONTROL Reporting View Name]**.

      - Spécifiez la variable **[!UICONTROL Reporting Time Zone]**.

   - Lorsque vous avez terminé, cliquez sur **[!UICONTROL Create View]** puis cliquez sur la flèche Précédent pour revenir à la page précédente.

1. Dans le panneau de gauche, sous _[!UICONTROL Reports]_, choisissez **[!UICONTROL Behavior]**>**[!UICONTROL Experiments]**.

1. Cliquez sur **[!UICONTROL Create experiment]** et procédez comme suit :

   - Indiquez le pourcentage du trafic à rediriger.

   - Spécifiez la variable **[!UICONTROL Original Page URL]** et les URL de chaque **[!UICONTROL page variation]** que vous voulez tester.

   - Renseignez les autres options.

1. Lorsque l’expérience est configurée, cliquez sur **[!UICONTROL Manually Insert the Code]** et copiez le fragment de code.

## Étape 4. Coller le fragment de code (Commerce)

1. Revenez à l’ administrateur de votre installation Commerce et ouvrez la version d’origine du produit, de la catégorie ou de la page en mode d’édition.

1. Développez l’objet **[!UICONTROL View Optimization]** pour le produit, la catégorie ou la page.

1. Collez le fragment de code que vous avez copié à partir de Google Analytics dans le **[!UICONTROL Experiment Code]** zone de texte.

   >[!NOTE]
   >
   >Ne collez le fragment de code dans aucune des variations.

   ![Optimisation des vues de produit](../catalog/assets/product-view-optimization.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

## Étape 5 : Examinez et démarrez l’expérience (Google)

1. Revenez à votre [Google Analytics][2] compte .

1. Vérifiez les paramètres de l’expérience.

1. Si vous êtes prêt à commencer, cliquez sur **[!UICONTROL Start Experiment]**.

   Sinon, cliquez sur **[!UICONTROL Save for Later]**.


[2]: https://analytics.google.com/
