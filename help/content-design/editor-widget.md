---
title: Insertion d’un widget dans l’éditeur
description: Ajoutez différents éléments de contenu à une page à l’aide de l’outil widget de l’éditeur de WYSIWYG.
exl-id: bbc5e059-06d8-4dda-89a7-6c9826b73fd3
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# Insertion d’un widget dans l’éditeur

L’outil [widget](widget-create.md) peut être utilisé pour ajouter différents éléments de contenu à la page, notamment des liens vers n’importe quelle page de contenu ou nœud de contenu, produit ou catégorie Commerce. Les liens peuvent être positionnés sur la page sous forme de bloc ou directement intégrés au contenu. Vous pouvez utiliser l’outil Widget pour créer des liens vers les types de contenu suivants :

- [Pages de contenu](pages.md)
- [Catégories de catalogue](../catalog/categories.md)
- [Catalog Products](../catalog/product-create.md)

Par défaut, les liens héritent de leur style de la feuille de style du thème.

{{$include /help/_includes/directives-caution.md}}

1. Ouvrez une page, un bloc ou un bloc dynamique en mode d’édition.

1. Accédez à la section _[!UICONTROL Content]_&#x200B;et cliquez sur n’importe quel élément prenant en charge l’éditeur.

1. Placez le curseur à l’endroit où vous souhaitez que le widget apparaisse, puis cliquez sur l’icône _Insérer un widget_.

   ![Barre d’outils de l’éditeur - Insérer un widget](./assets/editor-toolbar-widget-button.png){width="700" zoomable="yes"}

   Si Page Builder n’est pas activé et que vous préférez utiliser le code, cliquez sur **[!UICONTROL Show / Hide Editor]**. Positionnez le point d&#39;insertion dans le texte à l&#39;endroit où vous souhaitez que le widget apparaisse. Cliquez ensuite sur **[!UICONTROL Insert Widget]**.

1. Choisissez le **[!UICONTROL Widget Type]**.

   Pour plus d’informations sur ces options, voir [Types de widgets](widgets.md#widget-types). Les étapes suivantes utilisent un exemple pour insérer un lien vers un produit.

1. Pour utiliser le nom du produit, laissez le champ **[!UICONTROL Anchor Custom Text]** vide.

1. Saisissez un **[!UICONTROL Anchor Custom Title]** pour connaître les bonnes pratiques d’optimisation du moteur de recherche (SEO).

   Ce titre n’est pas visible sur la page.

1. Définissez **[!UICONTROL Template]** sur l’une des options suivantes :

   - Pour incorporer le lien dans le texte, sélectionnez `Product Link Inline Template`.

   - Pour placer le lien sur une ligne distincte, sélectionnez `Product Link Block Template`.

1. Cliquez sur **[!UICONTROL Select Product]** et procédez comme suit :

   - Dans l’arborescence, accédez à la catégorie de votre choix.

   - Dans la liste, choisissez le produit lié.

1. Cliquez sur **[!UICONTROL Insert Widget]** pour placer le lien sur la page.

   Si vous utilisez du code HTML, une [ balise de balisage ](../systems/markup-tags.md) pour le lien s’affiche en haut de la page, entre doubles accolades. Si nécessaire, utilisez _Couper et coller_ pour placer la balise de balisage dans le code où vous souhaitez que le lien apparaisse.

1. Une fois vos modifications de contenu terminées, cliquez sur **[!UICONTROL Save]**.
