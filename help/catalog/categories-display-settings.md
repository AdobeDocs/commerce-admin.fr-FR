---
title: Catégories - Paramètres d’affichage
description: Découvrez comment utiliser les paramètres de [!UICONTROL Display] pour définir quels éléments de contenu apparaissent sur une page de catégorie et l’ordre dans lequel les produits apparaissent.
exl-id: bb3a1b00-ba56-4113-8208-860963612333
feature: Catalog Management, Categories, Page Content
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# Catégories - Paramètres d’affichage

Les paramètres d’affichage déterminent quels éléments de contenu apparaissent sur une page de catégorie et l’ordre dans lequel les produits apparaissent. Vous pouvez activer les blocs CMS, définir le statut d’ancrage de la catégorie et gérer les options de tri à partir de l’onglet _[!UICONTROL Display Settings]_. Pour obtenir des exemples de la manière dont les catégories sont reflétées dans le storefront, voir [Navigation dans le catalogue](navigation.md).

![Paramètres d’affichage des catégories](./assets/category-display-settings.png){width="600" zoomable="yes"}

| Champ | Description |
|--- |--- |
| [!UICONTROL Display Mode] | Détermine les éléments de contenu affichés sur la page de catégorie. Options : `Products Only` / `Static Block Only` / `Static Block and Products` |
| [!UICONTROL Anchor] | Lorsque la valeur est définie sur `Yes`, affiche les produits des sous-catégories de la catégorie même s’ils n’ont pas été explicitement ajoutés à la catégorie, et active l’affichage de la section _[!UICONTROL filter by attribute]_&#x200B;dans la navigation superposée. Options : `Yes` / `No` |
| [!UICONTROL Available Product Listing Sort By] | (Obligatoire) Les valeurs par défaut sont `Position`, `Name` et `Price`. Pour personnaliser l’option de tri, décochez la case **[!UICONTROL Use All Available Attributes]** et sélectionnez les attributs à utiliser. Vous pouvez définir et ajouter des attributs selon vos besoins. Ce paramètre ne s’applique pas au [!DNL Live Search] [widget de page de liste de produits](https://experienceleague.adobe.com/fr/docs/commerce/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Default Product Listing Sort By] | (Obligatoire) Pour définir l’option de _[!UICONTROL Sort By]_&#x200B;par défaut, décochez la case **[!UICONTROL Use Config Settings]**&#x200B;et sélectionnez un attribut. Ce paramètre ne s’applique pas au [!DNL Live Search] [widget de page de liste de produits](https://experienceleague.adobe.com/fr/docs/commerce/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Layered Navigation Price Step] | Par défaut, Commerce affiche la plage de prix par incréments de 10, 100 et 1 000, selon les produits de la liste. Pour modifier la plage d&#39;étapes de prix, décochez la case **[!UICONTROL Use Config Settings]**. |

{style="table-layout:auto"}
