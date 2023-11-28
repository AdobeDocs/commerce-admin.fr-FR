---
title: Catégories - Paramètres de conception
description: En savoir plus sur l’utilisation de la variable [!UICONTROL Design] pour définir l’aspect d’une catégorie, toutes les pages de produits associées et la mise en page.
exl-id: 6dc216ac-1c52-4196-9c93-e5cad19901b5
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# Catégories - Paramètres de conception

La variable _[!UICONTROL Design]_vous permet de contrôler l’aspect d’une catégorie, toutes les pages de produits associées et la mise en page. Vous pouvez personnaliser une page de catégorie et ses produits associés pour une promotion ou pour différencier la catégorie. Par exemple, vous pouvez développer une conception spécifique pour une marque ou une ligne particulière de produits, ou appliquer une mise à jour pour une période spécifique.

![Paramètres de conception d’une catégorie](./assets/category-design.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Lorsque le même produit est affecté à plusieurs catégories avec des paramètres de conception différents pour chaque catégorie, il est recommandé de définir **Utilisation du chemin d’accès aux catégories pour les URL de produit** = `Yes` dans le [Options de configuration de l’optimisation du moteur de recherche](../configuration-reference/catalog/catalog.md#search-engine-optimization). Pour accéder à ce paramètre, accédez à  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**, développer **[!UICONTROL Catalog]**et choisissez **Catalogue**sous le panneau de gauche, puis développez l’objet **Optimisation du moteur de recherche**sur la page.

| Champ | Description |
|--- |--- |
| [!UICONTROL Use Parent Category Settings] | Permet à la catégorie actuelle d’hériter des paramètres de conception de la catégorie parente. En cas d’utilisation, tous les autres champs de la section Conception ne sont plus disponibles. Options : `Yes` / ` No` |
| [!UICONTROL Theme] | Applique un thème personnalisé à la catégorie. |
| [!UICONTROL Layout] | Applique une mise en page différente à la page de catégorie. Options : <br/>**[!UICONTROL No layout updates]**- Par défaut, les mises à jour de mise en page ne sont pas disponibles pour les pages de catégorie.<br/>**[!UICONTROL Empty]** - Utilisez pour définir votre propre mise en page. (Nécessite une compréhension du langage XML.) <br/>**[!UICONTROL 1 column]**: applique une mise en page à une colonne à la page des catégories.<br/>**[!UICONTROL 2 columns with left bar]** : applique une mise en page à deux colonnes avec une barre latérale gauche à la page de catégorie. <br/>**[!UICONTROL 2 columns with right bar]**: applique une mise en page à deux colonnes avec une barre latérale droite à la page de catégorie.<br/>**[!UICONTROL 3 columns]** : applique une mise en page à trois colonnes à la page de catégorie.<br/>**[!UICONTROL Page -- Full Width]**- (Nécessite [Page Builder](../page-builder/introduction.md)) Applique la disposition pleine largeur des pages CMS à la page de catégorie.<br/>**[!UICONTROL Category -- Full Width]** - (Créateur de pages requis) Applique la disposition pleine largeur des pages de catégorie à la page de catégorie. <br/>**[!UICONTROL Product -- Full Width]**- (Créateur de pages requis) Applique la disposition pleine largeur pour les pages de produit à la page de catégorie. |
| [!UICONTROL Custom Layout Update] | Répertorie les fichiers de mise à jour de mise en page personnalisée disponibles sur le serveur. Sélectionnez la mise à jour de mise en page personnalisée que vous souhaitez appliquer à la catégorie. |
| [!UICONTROL Apply Design to Products] | Lorsque cette option est sélectionnée, les paramètres personnalisés s’appliquent à tous les produits de la catégorie. |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Design Update]

{{ce-feature}}

La variable _[!UICONTROL Scheduled Design Update]_détermine la plage de dates lorsqu’une conception personnalisée est appliquée à des pages de catégorie.

| Champ | Description |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | Détermine la plage de dates lorsqu’une disposition personnalisée est appliquée à la catégorie. |

![Mise à jour de conception planifiée](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}
