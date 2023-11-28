---
title: Catégories - Paramètres Contenu
description: En savoir plus sur l’utilisation de la variable [!UICONTROL Content] pour définir tout contenu supplémentaire qui s’affiche sur la page de catégorie.
exl-id: 988083e1-0993-4e08-b5e6-8b0855e56467
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# Catégories - Paramètres Contenu

La variable _[!UICONTROL Content]_détermine le contenu supplémentaire qui s’affiche sur la page de catégorie. Outre la liste des produits de catégorie, la page peut inclure une image, une description et un bloc CMS. Vous pouvez utiliser la variable [[!DNL Page Builder]](../page-builder/introduction.md) outils de contenu pour définir la description de la catégorie.

## Ajoutez la description de la catégorie dans la section [!DNL Page Builder]

1. Ouvrez la catégorie en mode d’édition.

1. Faire défiler vers le bas et développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Content]** .

   ![Contenu de catégorie](./assets/category-content.png){width="600" zoomable="yes"}

1. En haut à droite du **[!UICONTROL Description]** zone, cliquez sur **[!UICONTROL Edit with Page Builder]**.

1. Utilisez la variable [[!DNL Page Builder]](../page-builder/introduction.md) outils de contenu vers [modifier du texte existant ;](../page-builder/text.md) et ajoutez d’autres contenus (si nécessaire).

## [!DNL Page Builder] aperçu

Lorsque vous développez l’objet _Contenu_ pour une catégorie existante dans laquelle du contenu a été créé avec [!DNL Page Builder], un aperçu de la fonction **[!UICONTROL Description]** contenu tel qu’il apparaîtra dans la page de catégorie. Cliquez sur la zone de contenu pour ouvrir la [!DNL Page Builder] espace de travail, où vous pouvez effectuer les mises à jour nécessaires.

![Aperçu de la description](../page-builder/assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

Par défaut, cet aperçu du contenu est activé pour les formulaires de produit et de catégorie. Si les performances souffrent du chargement de l’aperçu, vous pouvez désactiver l’aperçu dans la variable [Configuration de la gestion de contenu](../configuration-reference/general/content-management.md#advanced-content-tools) paramètres.

## Ajoutez la description de la catégorie dans l’éditeur.

Entrez uniquement des caractères ASCII simples dans la zone de texte. Si vous collez du texte à partir d’un traitement de texte, enregistrez-le d’abord en tant que fichier .TXT simple pour supprimer tous les caractères de contrôle invisibles.

Pour plus d’informations, voir [Éditeur WYSIWYG](../content-design/editor.md).

1. Ouvrez la catégorie en mode d’édition.

1. Faire défiler vers le bas et développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Content]** .

   ![Contenu de catégorie](./assets/category-content-ce.png){width="500" zoomable="yes"}

1. Saisir la catégorie **[!UICONTROL Description]** et utilisez la fonction [barre d’outils de l’éditeur](../content-design/editor.md) au format suivant les besoins.

   Vous pouvez faire glisser le coin inférieur droit pour modifier la hauteur de la zone de texte.

## Ajouter un bloc CMS à la page de catégorie

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Dans l&#39;arborescence des catégories, sélectionnez la catégorie à modifier.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Content]** .

1. Pour **[!UICONTROL Add the CMS block]**, sélectionnez un bloc à ajouter.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Display Settings]** .

1. Définissez la variable **[!UICONTROL Display Mode]** à l’une des options suivantes :

   - `Static block only`
   - `Static block and products`

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]** et passez en revue l’affichage des blocs sur le storefront (nécessite une actualisation du cache).

## Référence des paramètres de contenu

| Paramètre | [Portée](../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Category Image] | Affichage en magasin | Indique une image pour le haut de la page de catégorie. Méthodes : <br/><br/>**[!UICONTROL Upload]**- Télécharge un fichier image de votre ordinateur local vers la galerie et l’utilise comme image de catégorie.<br/><br/>**[!UICONTROL Select from Gallery]** - Vous invite à choisir une image existante dans la galerie. <br/><br/>![Icône de caméra du générateur de pages](../assets/icon-camera.png) - Faites glisser un fichier image sur la mosaïque de l’appareil photo ou accédez à l’image et sélectionnez-le dans votre système de fichiers local. |
| [!UICONTROL Description] | Affichage en magasin | Indique une description qui s’affiche sur la page de catégorie. <br/><br/>**[!UICONTROL Edit with Page Builder]**- Ouvre la fenêtre [[!DNL Page Builder] workspace](../page-builder/workspace.md), où vous pouvez modifier la description.<br/><br/>**[!UICONTROL Show / Hide Editor]** - Active/désactive l’affichage entre l’éditeur WYSIWYG et les modes HTML. |
| [!UICONTROL Add CMS Block] | Affichage en magasin | Ajoute un [Bloc CMS](../content-design/blocks.md) sur la page de catégorie. |

{style="table-layout:auto"}
