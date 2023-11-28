---
title: Paramètres du produit - [!UICONTROL Design]
description: Pour un produit, la variable [!UICONTROL Design] Les paramètres vous permettent d’appliquer un thème différent à une page de produits et de modifier la mise en page.
exl-id: 8606ddc7-ca81-4503-94e5-a8276506c0a1
feature: Catalog Management, Products, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Paramètres du produit - [!UICONTROL Design]

La variable _[!UICONTROL Design]_Les paramètres permettent d’appliquer un thème différent à la page du produit, de modifier la mise en page des colonnes, de déterminer où apparaissent les options du produit et de saisir du code XML personnalisé.

![Conception](./assets/product-design-ee.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Lorsque le même produit est affecté à plusieurs catégories avec des paramètres de conception différents pour chaque catégorie, il est recommandé de définir **[!UICONTROL Use Categories Path for Product URLs]** = `Yes` dans le [Options de configuration de l’optimisation du moteur de recherche](../configuration-reference/catalog/catalog.md#search-engine-optimization). Pour accéder à ce paramètre, accédez à  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**, développer **[!UICONTROL Catalog]**et choisissez **[!UICONTROL Catalog]**sous le panneau de gauche, puis développez l’objet **[!UICONTROL Search Engine Optimization]**sur la page.

| Champ | [Portée](../getting-started/websites-stores-views.md#scope-settings) | Description |
|---|---|----|
| [!UICONTROL Theme] | Affichage en magasin | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Permet d’appliquer un thème différent au produit. Options : (tous les thèmes disponibles) |
| [!UICONTROL Layout] | Affichage en magasin | Permet d’appliquer une [layout](../content-design/page-layout.md) à la page produit. Options : <br/>**[!UICONTROL No layout updates]**- Par défaut, les mises à jour de mise en page ne sont pas disponibles pour la page du produit.<br/>**[!UICONTROL Empty]** - Permet de définir votre propre mise en page, par exemple une page de 4 colonnes. (Nécessite une compréhension du langage XML.) <br/>**[!UICONTROL 1 column]**- Applique une mise en page à une colonne à la page du produit.<br/>**[!UICONTROL 2 columns with left bar]** - Applique une mise en page à deux colonnes avec une barre latérale gauche à la page du produit. <br/>**[!UICONTROL 2 columns with right bar]**- Applique une mise en page à deux colonnes avec une barre latérale droite à la page du produit.<br/>**[!UICONTROL 3 columns]** : applique une mise en page à trois colonnes à la page du produit. <br/>**[!UICONTROL Page -- Full Width]**- (Nécessite [[!DNL Page Builder]](../page-builder/introduction.md)) Applique la mise en page pleine largeur des pages CMS à la page du produit.<br/>**[!UICONTROL Category -- Full Width]** - (Nécessite [!DNL Page Builder]) Applique la disposition pleine largeur aux pages de catégorie à la page de produit. <br/>**[!UICONTROL Product -- Full Width]**- (Nécessite [!UICONTROL Page Builder]) Applique la mise en page pleine largeur des pages du produit à la page du produit. |
| [!UICONTROL Display Product Options In] | Affichage en magasin | Détermine l’emplacement d’affichage des options du produit sur la page du produit. Options : `Product Info Column` / `Block after Info Column` |
| [!UICONTROL Custom Layout Update] | Affichage en magasin | Utilisé pour accéder aux options permettant de mettre à jour une disposition personnalisée sur la page du produit. |

{style="table-layout:auto"}
