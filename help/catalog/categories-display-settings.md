---
title: Catégories - Paramètres d’affichage
description: En savoir plus sur l’utilisation de la variable [!UICONTROL Display] pour définir les éléments de contenu qui apparaissent sur une page de catégorie et l’ordre d’affichage des produits.
exl-id: bb3a1b00-ba56-4113-8208-860963612333
feature: Catalog Management, Categories, Page Content
source-git-commit: b99212b2c6977fc788e75df4bdce608fc4998dc4
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# Catégories - Paramètres d’affichage

Les paramètres d’affichage déterminent les éléments de contenu qui apparaissent sur une page de catégorie et l’ordre dans lequel les produits apparaissent. Vous pouvez activer les blocs CMS, définir l’état d’ancrage de la catégorie et gérer les options de tri à partir du _[!UICONTROL Display Settings]_. Pour des exemples de la façon dont les catégories sont reflétées dans le storefront, voir [Navigation dans le catalogue](navigation.md).

![Paramètres d’affichage des catégories](./assets/category-display-settings.png){width="600" zoomable="yes"}

| Champ | Description |
|--- |--- |
| [!UICONTROL Display Mode] | Détermine les éléments de contenu affichés sur la page de catégorie. Options : `Products Only` / `Static Block Only` / `Static Block and Products` |
| [!UICONTROL Anchor] | Lorsque la variable est définie sur `Yes`, inclut la variable _[!UICONTROL filter by attribute]_dans la navigation par couches. Options : `Yes` / `No` |
| [!UICONTROL Available Product Listing Sort By] | (Obligatoire) Les valeurs par défaut sont les suivantes : `Position`, `Name`, et `Price`. Pour personnaliser l’option de tri, désélectionnez l’option **[!UICONTROL Use All Available Attributes]** et sélectionnez les attributs à utiliser. Vous pouvez définir et ajouter des attributs selon vos besoins. Ce paramètre ne s’applique pas à la variable [!DNL Live Search] [Widget de page de liste de produits](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Default Product Listing Sort By] | (Obligatoire) Pour définir la valeur par défaut _[!UICONTROL Sort By]_désélectionnez l’option **[!UICONTROL Use Config Settings]**et sélectionnez un attribut. Ce paramètre ne s’applique pas à la variable [!DNL Live Search] [Widget de page de liste de produits](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Layered Navigation Price Step] | Par défaut, Commerce affiche la gamme de prix par incréments de 10, 100 et 1000, selon les produits de la liste. Pour modifier la plage d’étapes de prix, désélectionnez la **[!UICONTROL Use Config Settings]** . |

{style="table-layout:auto"}
