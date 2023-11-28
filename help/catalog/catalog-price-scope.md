---
title: Étendue du prix
description: Découvrez la portée utilisée pour les prix des produits, qui peuvent être configurés pour s’appliquer au niveau global ou au niveau du site web.
exl-id: 3726b16b-4ed5-4286-a7fd-69ed6677f87a
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 0%

---

# Étendue du prix

La portée de la variable [monnaie de base](../stores-purchase/currency-configuration.md) qui est utilisé pour les prix des produits peut être configuré pour s’appliquer au niveau global ou au niveau du site web. S’il est appliqué au niveau global, le même prix est utilisé dans toute la hiérarchie du magasin. S’il est appliqué au niveau du site web, le même produit peut être disponible à des prix différents dans les magasins associés à différents sites web. Par défaut, la portée de la tarification des produits est globale.

Différents facteurs peuvent avoir une incidence sur le prix d’un même produit à un endroit et non à un autre. Par exemple, il peut y avoir des coûts de distribution supplémentaires pour le produit, ainsi que d’autres considérations qui affectent le prix des produits vendus dans un magasin spécifique. Le diagramme suivant illustre une installation multisite avec la devise de base définie au niveau du site web. Les magasins et les vues de magasin associées à chaque site web reflètent la tarification du produit définie au niveau du site web.

![B2B pour Adobe Commerce](../assets/b2b.svg) Si vous utilisez des catalogues partagés, reportez-vous également à [Définition de la tarification et de la structure du catalogue partagées](../b2b/catalog-shared-pricing-structure.md) dans le _Guide B2B pour Adobe Commerce_.

![Diagramme d&#39;étendue des prix](./assets/catalog-price-scope.svg){width="550"}

## Configurer la portée du prix

1. Sur le _Administration_ , accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en-dessous.

1. Faites défiler l’écran vers le bas jusqu’à **[!UICONTROL Price]** section et définition **[!UICONTROL Catalog Price Scope]** à l’une des options suivantes :

   - `Global`
   - `Website`

   Le paramètre de portée que vous choisissez apparaît sous les champs de prix de votre catalogue.

   ![Étendue du prix du catalogue](./assets/catalog-price.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

## Utiliser la portée pour configurer les prix des produits

Le commerce n’autorise pas la définition d’un prix de produit pour chaque magasin. Mais vous pouvez modifier le prix par site web :

1. Sur le _Administration_ , accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en-dessous.

1. Dans le **[!UICONTROL Price]** , définissez la portée du prix sur `Website` plutôt que global.

1. Définissez le prix en ouvrant la page de modification du produit, en sélectionnant le périmètre dans le coin supérieur gauche, puis en entrant un nouveau prix par site web.
