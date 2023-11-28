---
title: URL Dynamic Media
description: Découvrez comment utiliser une URL de média dynamique comme référence relative à une image ou à une autre ressource multimédia.
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
source-git-commit: d3b9b4cd0d12f8d5feb2bad0bf601970f9ee1a36
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# URL Dynamic Media

Une URL de média dynamique est une référence relative à une image ou à une autre ressource multimédia. Lorsque cette option est activée, les URL Dynamic Media peuvent être utilisées pour créer des liens directs vers des ressources sur votre serveur ou vers des fichiers stockés sur un [réseau de diffusion de contenu](media-storage-content-delivery-network.md). L’utilisation d’URL Dynamic Media peut avoir un impact sur les performances du catalogue et sur la variable [éditeur](editor.md#configure-the-editor) peut être configuré pour utiliser des URL de média statique ou dynamique.

Comme pour tout [balises marketing](../systems/markup-tags.md), la directive est entourée d’accolades doubles. Le format d’une URL de média dynamique se présente comme suit :

`\{\{media url="path/to/image.jpg"}}`

Les directives d’URL dynamiques sont traitées à partir du contenu de HTML enregistré lorsque la page est rendue sur le storefront. Chaque fois que la page est rendue, le contenu est analysé pour `\{\{media url="..."}}` et chaque directive est remplacée par l’URL du média correspondant.

{{$include /help/_includes/directives-caution.md}}

## Configuration d’URL de médias statiques

Par défaut, les images insérées dans le catalogue à partir de l&#39;éditeur WYSIWYG ont des URL relatives et dynamiques. Si vous préférez utiliser une URL statique, vous pouvez modifier le paramètre de configuration.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, sous _[!UICONTROL General]_, choisissez **[!UICONTROL Content Management]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL WYSIWYG Options]** .

   ![Options WYSIWYG](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]** à l’une des options suivantes :

   - `Yes` : utilise des URL statiques pour le contenu multimédia inséré avec l’éditeur WYSIWYG. Les URL statiques sont absolues et cassées si la variable [URL de base](../stores-purchase/store-urls.md) des modifications du magasin.

   - `No` - (Par défaut) utilise des URL dynamiques pour le contenu multimédia inséré avec l’éditeur WYSIWYG, en fonction de la variable `\{\{media url="..."}}` de . Les URL dynamiques sont relatives et ne rompent pas si l’URL de base du magasin change.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.
