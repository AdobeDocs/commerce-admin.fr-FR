---
title: Catégories - Paramètres d’affichage
description: Découvrez comment utiliser les paramètres [!UICONTROL Display] pour définir les éléments de contenu qui apparaissent sur une page de catégorie et l’ordre dans lequel les produits apparaissent.
exl-id: bb3a1b00-ba56-4113-8208-860963612333
feature: Catalog Management, Categories, Page Content
source-git-commit: a47e744cf4cc5163ca2ba0718ccb78eb65a7d404
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# Catégories - Paramètres d’affichage

Les paramètres d’affichage déterminent les éléments de contenu qui apparaissent sur une page de catégorie et l’ordre dans lequel les produits apparaissent. Vous pouvez activer les blocs CMS, définir l’état d’ancrage de la catégorie et gérer les options de tri à partir de l’onglet _[!UICONTROL Display Settings]_. Pour des exemples de la façon dont les catégories sont reflétées dans le storefront, voir [Navigation dans un catalogue](navigation.md).

![Paramètres d’affichage des catégories](./assets/category-display-settings.png){width="600" zoomable="yes"}

| Champ | Description |
|--- |--- |
| [!UICONTROL Display Mode] | Détermine les éléments de contenu affichés sur la page de catégorie. Options : `Products Only` / `Static Block Only` / `Static Block and Products` |
| [!UICONTROL Anchor] | Lorsqu’elle est définie sur `Yes`, affiche les produits des sous-catégories de la catégorie même s’ils n’ont pas été explicitement ajoutés à la catégorie et active l’affichage de la section _[!UICONTROL filter by attribute]_dans la navigation par couche. Options : `Yes` / `No` |
| [!UICONTROL Available Product Listing Sort By] | (Obligatoire) Les valeurs par défaut sont `Position`, `Name` et `Price`. Pour personnaliser l’option de tri, décochez la case **[!UICONTROL Use All Available Attributes]** et sélectionnez les attributs à utiliser. Vous pouvez définir et ajouter des attributs selon vos besoins. Ce paramètre ne s’applique pas au [!DNL Live Search] [ ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling) Widget de page de liste de produits. |
| [!UICONTROL Default Product Listing Sort By] | (Obligatoire) Pour définir l’option _[!UICONTROL Sort By]_par défaut, décochez la case **[!UICONTROL Use Config Settings]**et sélectionnez un attribut. Ce paramètre ne s’applique pas au [!DNL Live Search] [ ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling) Widget de page de liste de produits. |
| [!UICONTROL Layered Navigation Price Step] | Par défaut, Commerce affiche la gamme de prix par incréments de 10, 100 et 1000, selon les produits de la liste. Pour modifier la plage Price Step, désélectionnez la case **[!UICONTROL Use Config Settings]** . |

{style="table-layout:auto"}
