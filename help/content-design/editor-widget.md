---
title: Insertion d’un widget dans l’éditeur
description: Ajoutez divers éléments de contenu à une page à l’aide de l’outil de widget dans l’éditeur WYSIWYG.
exl-id: bbc5e059-06d8-4dda-89a7-6c9826b73fd3
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# Insertion d’un widget dans l’éditeur

L’outil [widget](widget-create.md) peut être utilisé pour ajouter divers éléments de contenu à la page, y compris des liens vers une page de contenu Commerce, un noeud, un produit ou une catégorie. Les liens peuvent être positionnés sur la page au format bloc ou incorporés directement dans le contenu. Vous pouvez utiliser l’outil Widget pour créer des liens vers les types de contenu suivants :

- [Pages de contenu](pages.md)
- [Catégories de catalogue](../catalog/categories.md)
- [Produits de catalogue](../catalog/product-create.md)

Par défaut, les liens héritent de leur style à partir de la feuille de style du thème.

{{$include /help/_includes/directives-caution.md}}

1. Ouvrez une page, un bloc ou un bloc dynamique en mode d’édition.

1. Accédez à la section _[!UICONTROL Content]_et cliquez sur un élément prenant en charge l’éditeur.

1. Placez le curseur à l’endroit où vous souhaitez que le widget s’affiche, puis cliquez sur l’icône _Insérer le widget_ .

   ![Barre d’outils de l’éditeur - Insérer un widget](./assets/editor-toolbar-widget-button.png){width="700" zoomable="yes"}

   Si le Créateur de pages n’est pas activé et que vous préférez travailler avec le code, cliquez sur **[!UICONTROL Show / Hide Editor]**. Placez le point d’insertion dans le texte à l’endroit où vous souhaitez que le widget s’affiche. Cliquez ensuite sur **[!UICONTROL Insert Widget]**.

1. Sélectionnez le **[!UICONTROL Widget Type]**.

   Pour plus d’informations sur ces options, voir [Types de widgets](widgets.md#widget-types). Les étapes suivantes utilisent un exemple d’insertion d’un lien vers un produit.

1. Pour utiliser le nom du produit, laissez le champ **[!UICONTROL Anchor Custom Text]** vide.

1. Saisissez un **[!UICONTROL Anchor Custom Title]** pour la bonne pratique SEO.

   Ce titre n’est pas visible sur la page.

1. Définissez **[!UICONTROL Template]** sur l’une des options suivantes :

   - Pour incorporer le lien dans du texte, sélectionnez `Product Link Inline Template`.

   - Pour placer le lien sur une ligne distincte, sélectionnez `Product Link Block Template`.

1. Cliquez sur **[!UICONTROL Select Product]** et procédez comme suit :

   - Dans l’arborescence, accédez à la catégorie de votre choix.

   - Dans la liste, choisissez le produit associé.

1. Cliquez sur **[!UICONTROL Insert Widget]** pour placer le lien sur la page.

   Si vous utilisez du code d’HTML, une [balise de balisage](../systems/markup-tags.md) pour le lien apparaît en haut de la page, entre accolades doubles. Si nécessaire, utilisez _Couper et Coller_ pour positionner la balise de balisage dans le code où vous souhaitez que le lien s’affiche.

1. Une fois vos modifications de contenu terminées, cliquez sur **[!UICONTROL Save]**.
