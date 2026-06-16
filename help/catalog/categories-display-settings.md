---
title: Catégories - Paramètres d’affichage
description: Découvrez comment utiliser les paramètres de [!UICONTROL Display] pour définir quels éléments de contenu apparaissent sur une page de catégorie et l’ordre dans lequel les produits apparaissent.
exl-id: bb3a1b00-ba56-4113-8208-860963612333
feature: Catalog Management, Categories, Page Content
TQID: https://experienceleague.adobe.com/t5UfvWvJ7R-kZb5kyMwpzwI2gfs3x3g1amlfWzQcAsw
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fc
subfeature_v2: id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 247
ht-degree: 0%

---

# Catégories - Paramètres d’affichage

Les paramètres d’affichage déterminent quels éléments de contenu apparaissent sur une page de catégorie et l’ordre dans lequel les produits apparaissent. Vous pouvez activer les blocs CMS, définir le statut d’ancrage de la catégorie et gérer les options de tri à partir de l’onglet _[!UICONTROL Display Settings]_. Pour obtenir des exemples de la manière dont les catégories sont reflétées dans le storefront, voir [Navigation dans le catalogue](navigation.md).

![Paramètres d’affichage des catégories](./assets/category-display-settings.png){width="600" zoomable="yes"}

| Champ | Description |
|--- |--- |
| [!UICONTROL Display Mode] | Détermine les éléments de contenu affichés sur la page de catégorie. Options : `Products Only` / `Static Block Only` / `Static Block and Products` |
| [!UICONTROL Anchor] | Lorsque la valeur est définie sur `Yes`, affiche les produits des sous-catégories de la catégorie même s’ils n’ont pas été explicitement ajoutés à la catégorie, et active l’affichage de la section _[!UICONTROL filter by attribute]_dans la navigation superposée. Options : `Yes` / `No` |
| [!UICONTROL Available Product Listing Sort By] | (Obligatoire) Les valeurs par défaut sont `Position`, `Name` et `Price`. Pour personnaliser l’option de tri, décochez la case **[!UICONTROL Use All Available Attributes]** et sélectionnez les attributs à utiliser. Vous pouvez définir et ajouter des attributs selon vos besoins. Ce paramètre ne s’applique pas au [!DNL Live Search] [widget de page de liste de produits](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Default Product Listing Sort By] | (Obligatoire) Pour définir l’option de _[!UICONTROL Sort By]_par défaut, décochez la case **[!UICONTROL Use Config Settings]**et sélectionnez un attribut. Ce paramètre ne s’applique pas au [!DNL Live Search] [widget de page de liste de produits](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Layered Navigation Price Step] | Par défaut, Commerce affiche la plage de prix par incréments de 10, 100 et 1 000, selon les produits de la liste. Pour modifier la plage d&#39;étapes de prix, décochez la case **[!UICONTROL Use Config Settings]**. |

{style="table-layout:auto"}
