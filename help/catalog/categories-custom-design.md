---
title: Catégories - Paramètres de conception
description: Découvrez comment utiliser les paramètres de [!UICONTROL Design] pour définir l’aspect d’une catégorie, de toutes les pages de produits associées et de la mise en page.
exl-id: 6dc216ac-1c52-4196-9c93-e5cad19901b5
feature: Catalog Management, Categories, Page Content
TQID: https://experienceleague.adobe.com/cRTRPl-UTfAKXY8rmtVKlnAZooVWpTCjSkVSdNHXp28
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 379
ht-degree: 0%

---

# Catégories - Paramètres de conception

La section _[!UICONTROL Design]_&#x200B;vous permet de contrôler l’aspect d’une catégorie, toutes les pages de produits associées et la mise en page. Vous pouvez personnaliser une page de catégorie et ses produits associés pour une promotion ou pour différencier la catégorie. Par exemple, vous pouvez développer une conception distinctive pour une marque ou une gamme spéciale de produits, ou appliquer une mise à jour pendant une période spécifique.

![Paramètres de conception d’une catégorie](./assets/category-design.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Lorsqu’un même produit est affecté à plusieurs catégories avec des paramètres de conception différents pour chaque catégorie, il est recommandé de définir **Utiliser le chemin d’accès aux catégories pour les URL de produit** = `Yes` dans les [options de configuration de l’optimisation du moteur de recherche](../configuration-reference/catalog/catalog.md#search-engine-optimization). Pour accéder à ce paramètre, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**, développez **[!UICONTROL Catalog]**&#x200B;et choisissez **Catalogue**&#x200B;sous dans le panneau de gauche, puis développez la section **Optimisation du moteur de recherche**&#x200B;sur la page.

| Champ | Description |
|--- |--- |
| [!UICONTROL Use Parent Category Settings] | Permet à la catégorie actuelle d&#39;hériter des paramètres de conception de la catégorie parent. Si vous utilisez cette option, tous les autres champs de la section Conception ne sont plus disponibles. Options : `Yes` / ` No` |
| [!UICONTROL Theme] | Applique un thème personnalisé à la catégorie. |
| [!UICONTROL Layout] | Applique une disposition différente à la page de catégorie. Options : <br/>**[!UICONTROL No layout updates]**- Par défaut, les mises à jour de disposition ne sont pas disponibles pour les pages de catégorie.<br/>**[!UICONTROL Empty]** - Utilisez pour définir votre propre mise en page. (Nécessite une compréhension du langage XML.) <br/>**[!UICONTROL 1 column]**- Applique une disposition d’une colonne à la page de catégorie.<br/>**[!UICONTROL 2 columns with left bar]** - Applique une disposition à deux colonnes avec une barre latérale gauche à la page de catégorie. <br/>**[!UICONTROL 2 columns with right bar]**- Applique une disposition à deux colonnes avec une barre latérale droite à la page de catégorie.<br/>**[!UICONTROL 3 columns]** - Applique une disposition à trois colonnes à la page de catégorie.<br/>**[!UICONTROL Page -- Full Width]**- (Nécessite [&#x200B; Page Builder](../page-builder/introduction.md)) Applique la mise en page pleine largeur pour les pages CMS à la page de catégorie.<br/>**[!UICONTROL Category -- Full Width]** - (Nécessite Page Builder) Applique la mise en page pleine largeur pour les pages de catégorie à la page de catégorie. <br/>**[!UICONTROL Product -- Full Width]**- (Nécessite Page Builder) Applique la disposition pleine largeur des pages de produits à la page de catégorie. |
| [!UICONTROL Custom Layout Update] | Répertorie les fichiers de mise à jour de disposition personnalisés disponibles sur le serveur. Choisissez la mise à jour de disposition personnalisée que vous souhaitez appliquer à la catégorie. |
| [!UICONTROL Apply Design to Products] | Lorsque cette option est sélectionnée, les paramètres personnalisés s’appliquent à tous les produits de la catégorie. |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Design Update]

{{ce-feature}}

La section _[!UICONTROL Scheduled Design Update]_&#x200B;détermine la plage de dates à laquelle une conception personnalisée est appliquée aux pages de catégorie.

| Champ | Description |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | Détermine la plage de dates lorsqu’une mise en page personnalisée est appliquée à la catégorie. |

![Mise à jour de conception planifiée](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}
