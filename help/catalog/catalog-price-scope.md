---
title: Périmètre du prix
description: Découvrez la portée utilisée pour les prix des produits, qui peut être configurée pour s’appliquer au niveau mondial ou au niveau du site web.
exl-id: 3726b16b-4ed5-4286-a7fd-69ed6677f87a
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/4tNRviXPzBubIpyAn9vgUs8BaILjJ6BEdV4yj5ngz6Y
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 376
ht-degree: 0%

---

# Périmètre du prix

La portée de la [devise de base](../stores-purchase/currency-configuration.md) utilisée pour les prix des produits peut être configurée pour s’appliquer au niveau global ou au niveau du site web. Si le prix est appliqué au niveau global, le même prix est utilisé dans toute la hiérarchie du magasin. S’il est appliqué au niveau du site web, le même produit peut être disponible à des prix différents dans des magasins associés à différents sites web. Par défaut, la portée de la tarification des produits est globale.

Différents facteurs peuvent influer sur le prix d&#39;un même produit à un endroit et pas à un autre. Par exemple, il peut y avoir des coûts de distribution supplémentaires pour le produit et d’autres considérations qui affectent le prix des produits vendus dans un magasin spécifique. Le diagramme suivant illustre une installation multisite avec la devise de base définie au niveau du site web. Les magasins et les affichages de magasin associés à chaque site web reflètent le prix du produit défini au niveau du site web.

![Adobe Commerce B2B](../assets/b2b.svg) Si vous utilisez des catalogues partagés, reportez-vous également à la section [Définir la tarification et la structure des catalogues partagés](../b2b/catalog-shared-pricing-structure.md) dans le _Guide Adobe Commerce B2B_.

![Diagramme de la portée des prix](./assets/catalog-price-scope.svg){width="550"}

## Configurer la portée des prix

1. Dans le menu _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en dessous.

1. Faites défiler jusqu’à la section **[!UICONTROL Price]** et définissez **[!UICONTROL Catalog Price Scope]** sur l’une des options suivantes :

   - `Global`
   - `Website`

   Le paramètre d’étendue que vous choisissez s’affiche sous les champs de prix de votre catalogue.

   ![Périmètre du prix du catalogue](./assets/catalog-price.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Utiliser la portée pour configurer les prix des produits

Commerce ne permet pas de définir un prix de produit pour chaque magasin. Mais vous pouvez modifier le prix par site web :

1. Dans le menu _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en dessous.

1. Dans l’onglet **[!UICONTROL Price]** , définissez la portée du prix sur `Website` au lieu de `Global`.

1. Définissez le prix en ouvrant la page de modification du produit, en sélectionnant la portée dans le coin supérieur gauche, puis en saisissant un nouveau prix par site web.

Dans de rares cas, lorsque la portée des prix est définie sur `Global`, la base de données Commerce peut toujours avoir des prix différents au niveau du site web. Cela peut être dû à des problèmes de synchronisation en dehors de Commerce. Dans ces cas, le commerçant doit effectuer un nettoyage des prix au niveau du magasin et exécuter une synchronisation des catalogues avec les services Commerce.