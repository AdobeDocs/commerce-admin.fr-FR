---
title: Produits récemment consultés ou comparés
description: Découvrez comment configurer les blocs de contenu storefront pour les produits récemment consultés et comparés.
exl-id: a4580835-68c2-4eb0-825e-0939eeab921b
feature: Products, Storefront
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
TQID: 'https://experienceleague.adobe.com/YeayJ1RkE6Muq0wNnd6KAQmmZcyjTQrSZOqEltlj8T8'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 0%
---
# Produits récemment consultés ou comparés

Les blocs _Récemment consultés et Récemment comparés_ s’affichent généralement dans la barre latérale droite d’une page de catalogue. Le nombre de produits répertoriés dans chaque peut être configuré pour chaque site web, magasin ou vue de magasin.

**_Pour configurer les produits récemment consultés et comparés:_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en dessous.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Recently Viewed/Compared Products]** .

   ![Configuration du catalogue - produits récemment consultés/comparés](../configuration-reference/catalog/assets/catalog-recently-viewed-and-compared-products.png){width="600" zoomable="yes"}

   Pour obtenir une description détaillée de chacun de ces paramètres de configuration, consultez [Produits récemment consultés/comparés](../configuration-reference/catalog/catalog.md#recently-viewedcompared-products) dans le _Guide de référence de configuration_.

1. Définissez des **[!UICONTROL Synchronize widget products with backend storage]** pour synchroniser les informations sur le widget du produit, telles que l’ID du produit, avec la disponibilité actuelle du stockage du produit dans la base de données et réutilisez ces informations sur différents appareils.

1. Définissez **[!UICONTROL Show for Current]** sur la vue du site web, du magasin ou du magasin où s’applique la configuration.

1. Par **[!UICONTROL Default Recently Viewed Products Count]**, saisissez le nombre de produits récemment consultés qui apparaîtront dans la liste.

1. Par **[!UICONTROL Default Recently Compared Products Count]**, saisissez le nombre de produits récemment comparés à afficher dans la liste.

1. Par **[!UICONTROL Lifetime of products in Recently Viewed Widget]**, saisissez une plage horaire en secondes, supérieure à zéro.

   Ce paramètre détermine la durée d’affichage des produits consultés dans la liste récemment consultée.

1. Par **[!UICONTROL Lifetime of products in Recently Compared Widget]**, saisissez une plage horaire en secondes, supérieure à zéro.

   Ce paramètre détermine la durée d’affichage des produits comparés dans la liste récemment comparée.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
