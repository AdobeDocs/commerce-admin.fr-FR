---
title: Paramètres du produit - [!UICONTROL Design]
description: Pour un produit, les paramètres de [!UICONTROL Design] vous permettent d’appliquer un thème différent à une page de produit et de modifier la mise en page.
exl-id: 8606ddc7-ca81-4503-94e5-a8276506c0a1
feature: Catalog Management, Products, Page Content
TQID: https://experienceleague.adobe.com/u6VzZ9TiovuSopBcBjmpQTKl3pzh3DoXXzpr8akWp-8
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fcid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ccaac3a13a346ce192a724efb3384ef2d612c980
workflow-type: tm+mt
source-wordcount: 284
ht-degree: 0%

---

# Paramètres du produit - [!UICONTROL Design]

Les paramètres _[!UICONTROL Design]_permettent d’appliquer un thème différent à la page du produit, de modifier la disposition des colonnes, de déterminer où les options du produit apparaissent et de saisir du code XML personnalisé.

![ Conception ](./assets/product-design-ee.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Lorsqu’un même produit est affecté à plusieurs catégories avec des paramètres de conception différents pour chaque catégorie, il est recommandé de définir **[!UICONTROL Use Categories Path for Product URLs]** = `Yes` dans les [options de configuration de l’optimisation du moteur de recherche](../configuration-reference/catalog/catalog.md#search-engine-optimization). Pour accéder à ce paramètre, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**, développez **[!UICONTROL Catalog]**et choisissez **[!UICONTROL Catalog]**en dessous dans le panneau de gauche, puis développez la section **[!UICONTROL Search Engine Optimization]**de la page.

| Champ | [Portée](../getting-started/websites-stores-views.md#scope-settings) | Description |
|---|---|----|
| [!UICONTROL Theme] | Affichage de la boutique | ![](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Permet d’appliquer un thème différent au produit. Options : (tous les thèmes disponibles) |
| [!UICONTROL Layout] | Affichage de la boutique | Vous permet d’appliquer une [mise en page](../content-design/page-layout.md) différente à la page du produit. Options : <br/>**[!UICONTROL No layout updates]**- Par défaut, les mises à jour de disposition ne sont pas disponibles pour la page du produit.<br/>**[!UICONTROL Empty]** - Permet de définir votre propre mise en page, par exemple une page à 4 colonnes. (Nécessite une compréhension du langage XML.) <br/>**[!UICONTROL 1 column]**- Applique une mise en page d’une colonne à la page du produit.<br/>**[!UICONTROL 2 columns with left bar]** - Applique une disposition à deux colonnes avec une barre latérale gauche à la page produit. <br/>**[!UICONTROL 2 columns with right bar]**- Applique une disposition à deux colonnes avec une barre latérale droite à la page de produit.<br/>**[!UICONTROL 3 columns]** - Applique une disposition à trois colonnes à la page produit. <br/>**[!UICONTROL Page -- Full Width]**- (Nécessite [[!DNL Page Builder]](../page-builder/introduction.md)) Applique la disposition pleine largeur des pages CMS à la page du produit.<br/>**[!UICONTROL Category -- Full Width]** - (Nécessite [!DNL Page Builder]) Applique la mise en page pleine largeur pour les pages de catégorie à la page de produit. <br/>**[!UICONTROL Product -- Full Width]**- (Nécessite [!UICONTROL Page Builder]) Applique la disposition pleine largeur des pages de produits à la page de produits. |
| [!UICONTROL Display Product Options In] | Affichage de la boutique | Détermine où les options de produit apparaissent sur la page de produit. Options : `Product Info Column` / `Block after Info Column` |
| [!UICONTROL Custom Layout Update] | Affichage de la boutique | Permet d’accéder aux options de mise à jour d’une mise en page personnalisée sur la page du produit. |

{style="table-layout:auto"}

