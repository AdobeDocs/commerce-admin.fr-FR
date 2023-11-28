---
title: Éditeur WYSIWYG
description: Découvrez comment utiliser l’éditeur et utiliser du contenu dans une vue _What You See Is What You Get_ (WYSIWYG).
exl-id: 209ca9d6-973c-4ad9-b7cd-4fba58dbfbb8
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# Éditeur WYSIWYG

L’éditeur vous permet de saisir et de mettre en forme lorsque vous travaillez dans un _Ce Que Vous Voyez Est Ce Que Vous Obtenez_ (WYSIWYG) vue du contenu. Si vous préférez travailler directement avec le code de HTML sous-jacent, vous pouvez facilement changer de mode. L’éditeur peut être utilisé pour créer du contenu pour [pages](pages.md), [blocs](blocks.md), et [description des produits](../catalog/product-content.md). Lorsque vous travaillez sur les détails du produit, accédez à l’éditeur en cliquant sur **[!UICONTROL Show / Hide Editor]**.

>[!NOTE]
>
>TinyMCE 5 est l’éditeur WYSIWYG par défaut. Une mise à jour de la bibliothèque TinyMCE 5.10 dans Adobe Commerce et Magento Open Source 2.4.5 résout une vulnérabilité qui permettait l’exécution arbitraire de JavaScript lors de la mise à jour d’une image ou d’un lien à l’aide de certains types d’URL. TinyMCE 3 a été abandonné dans la version 2.4.0 et supprimé dans la version 2.4.3. TinyMCE 4 a été supprimé dans la version 2.4.4.

![Barre d’outils de l’éditeur](./assets/editor-toolbar.png){width="700" zoomable="yes"}

Les rubriques suivantes fournissent des informations détaillées sur l’utilisation de l’éditeur :

- [Insérer un lien](editor-insert-link.md)
- [Insertion d’une image](editor-insert-image.md)
- [Insérer un widget](editor-widget.md)
- [Insertion d’une variable](editor-insert-variable.md)

## Configuration de l’éditeur

L’éditeur WYSIWYG est activé par défaut et peut être utilisé pour modifier le contenu sur les pages et les blocs CMS, ainsi que dans les produits et les catégories. Dans la configuration, vous pouvez activer ou désactiver l’éditeur, puis choisir d’utiliser l’option statique plutôt que statique. [dynamic](../catalog/catalog-urls.md#dynamic-url), URL du contenu multimédia dans les descriptions de produit et de catégorie.

![Options WYSIWYG](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

Pour une description détaillée de toutes les options WYSIWYG, voir [Gestion de contenu](../configuration-reference/general/content-management.md) dans le _Référence de configuration_.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, sous _[!UICONTROL General]_, choisissez **[!UICONTROL Content Management]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL WYSIWYG Options]**.

1. Définir **[!UICONTROL Enable WYSIWYG Editor]** selon vos préférences.

   L’éditeur est activé par défaut.

1. Définir **[!UICONTROL Static URLs for Media Content in WYSIWYG]** à votre préférence pour tous [contenu multimédia](../catalog/catalog-urls.md#static-url) qui est saisi avec l’éditeur WYSIWYG.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.
