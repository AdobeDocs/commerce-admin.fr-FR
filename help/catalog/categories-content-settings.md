---
title: Catégories - Paramètres de contenu
description: Découvrez comment utiliser les paramètres de [!UICONTROL Content] pour définir tout contenu supplémentaire qui s’affiche sur la page de catégorie.
exl-id: 988083e1-0993-4e08-b5e6-8b0855e56467
feature: Catalog Management, Categories, Page Content
TQID: https://experienceleague.adobe.com/PKCKw4i-EDB10X3AU-daMiyVMT96naqRLF8vrVBp24s
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 450
ht-degree: 0%

---

# Catégories - Paramètres de contenu

Les paramètres de _[!UICONTROL Content]_&#x200B;déterminent si du contenu supplémentaire s’affiche sur la page de catégorie. Outre la liste des produits de catégorie, la page peut inclure une image, une description et un bloc CMS. Vous pouvez utiliser les outils de contenu [[!DNL Page Builder]](../page-builder/introduction.md) pour définir la description de la catégorie.

## Ajoutez la description de la catégorie dans [!DNL Page Builder]

1. Ouvrez la catégorie en mode d’édition.

1. Faites défiler vers le bas et développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Content]** .

   ![Contenu de la catégorie](./assets/category-content.png){width="600" zoomable="yes"}

1. En haut à droite de la zone de **[!UICONTROL Description]**, cliquez sur **[!UICONTROL Edit with Page Builder]**.

1. Utilisez les outils de contenu [[!DNL Page Builder]](../page-builder/introduction.md) pour [modifier tout texte existant](../page-builder/text.md) et ajouter d’autres contenus (si nécessaire).

## Aperçu [!DNL Page Builder]

Lorsque vous développez la section _Contenu_ pour une catégorie existante contenant du contenu créé avec [!DNL Page Builder], elle affiche un aperçu du contenu **[!UICONTROL Description]** tel qu’il apparaîtrait sur la page de catégorie. Cliquez sur la zone de contenu pour ouvrir l’espace de travail [!DNL Page Builder], où vous pouvez effectuer les mises à jour nécessaires.

![Aperçu de la description](../page-builder/assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

Cet aperçu du contenu est activé par défaut pour les formulaires de produits et de catégories. Si les performances pâtissent du chargement de l’aperçu, vous pouvez le désactiver dans les paramètres [Configuration de la gestion de contenu](../configuration-reference/general/content-management.md#advanced-content-tools).

## Ajouter la description de la catégorie dans l’éditeur

Saisissez uniquement des caractères ASCII simples dans la zone de texte. Si vous collez du texte à partir d’un traitement de texte, enregistrez-le d’abord en tant que fichier .TXT brut pour supprimer tous les caractères de contrôle invisibles.

Pour plus d&#39;informations, voir [Éditeur &#x200B;](../content-design/editor.md).

1. Ouvrez la catégorie en mode d’édition.

1. Faites défiler vers le bas et développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Content]** .

   ![Contenu de la catégorie](./assets/category-content-ce.png){width="500" zoomable="yes"}

1. Saisissez le **[!UICONTROL Description]** de la catégorie et utilisez la barre d’outils [éditeur](../content-design/editor.md) pour la mettre en forme selon vos besoins.

   Vous pouvez faire glisser le coin inférieur droit pour modifier la hauteur de la zone de texte.

## Ajouter un bloc CMS à la page de catégorie

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Dans l’arborescence des catégories, sélectionnez la catégorie à modifier.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Content]** .

1. Par **[!UICONTROL Add the CMS block]**, sélectionnez un bloc que vous souhaitez ajouter.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Display Settings]** .

1. Définissez la **[!UICONTROL Display Mode]** sur l’une des options suivantes :

   - `Static block only`
   - `Static block and products`

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]** et vérifiez l’affichage du bloc sur le storefront (actualisation du cache requise).

## Référence des paramètres de contenu

| Paramètre | [Portée](../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Category Image] | Affichage de la boutique | Indique une image pour le haut de la page de catégorie. Méthodes : <br/><br/>**[!UICONTROL Upload]**- Télécharge un fichier image de votre ordinateur local dans la galerie et l’utilise comme image de catégorie.<br/><br/>**[!UICONTROL Select from Gallery]** - Vous invite à choisir une image existante dans la galerie. <br/><br/>![Icône de caméra du générateur de page](../assets/icon-camera.png) - Faites glisser un fichier image vers la mosaïque de la caméra ou accédez à l’image et sélectionnez-le dans votre système de fichiers local. |
| [!UICONTROL Description] | Affichage de la boutique | Spécifie une description qui s&#39;affiche sur la page de catégorie. <br/><br/>**[!UICONTROL Edit with Page Builder]**- Ouvre l’espace de travail [[!DNL Page Builder] workspace](../page-builder/workspace.md) dans lequel vous pouvez modifier la description.<br/><br/>**[!UICONTROL Show / Hide Editor]** - Fait basculer l’affichage entre le mode éditeur de WYSIWYG et le mode HTML. |
| [!UICONTROL Add CMS Block] | Affichage de la boutique | Ajoute un bloc [CMS existant](../content-design/blocks.md) à la page de catégorie. |

{style="table-layout:auto"}
