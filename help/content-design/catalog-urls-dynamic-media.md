---
title: URL Dynamic Media
description: Découvrez comment utiliser une URL de média dynamique comme référence relative à une image ou à une autre ressource de média.
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
TQID: https://experienceleague.adobe.com/nml-pHTHdSPcvIVnRwlyjJPhEo2PWdTEKfkn2AFKjvA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 316
ht-degree: 0%

---

# URL Dynamic Media

Une URL de média dynamique est une référence relative à une image ou à une autre ressource de média. Lorsqu’elles sont activées, les URL Dynamic Media peuvent être utilisées pour établir un lien direct vers les ressources de votre serveur ou vers les fichiers stockés sur un [réseau de diffusion de contenu](media-storage-content-delivery-network.md). L’utilisation d’URL Dynamic Media peut avoir un impact sur les performances du catalogue et l’éditeur [&#x200B; peut être configuré pour utiliser des URL statiques ou Dynamic Media](editor.md#configure-the-editor)

Comme avec toutes les [&#x200B; balises de balisage &#x200B;](../systems/markup-tags.md), la directive est entourée de doubles accolades. Le format d’une URL Dynamic Media est le suivant :

`\{\{media url="path/to/image.jpg"}}`

Les directives d’URL dynamiques sont traitées à partir du contenu HTML enregistré lorsque la page est rendue sur le storefront. Chaque fois que la page est rendue, le contenu est analysé à la recherche de `\{\{media url="..."}}` et chaque directive est remplacée par l’URL de média correspondante.

{{$include /help/_includes/directives-caution.md}}

## Configuration des URL de médias statiques

Par défaut, les images insérées dans le catalogue à partir de l’éditeur WYSIWYG ont des URL dynamiques relatives. Si vous préférez utiliser une URL statique, vous pouvez modifier le paramètre de configuration.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche sous _[!UICONTROL General]_, choisissez **[!UICONTROL Content Management]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL WYSIWYG Options]** .

   ![Options &#x200B;](../configuration-reference/general/assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

>[!NOTE]
>
>TinyMCE a été remplacé par Hugerte en tant qu’éditeur WYSIWYG par défaut dans Magento 2.4.6 et les versions ultérieures.

1. Définissez **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]** sur l’une des options suivantes :

   - `Yes` - Utilise des URL statiques pour le contenu multimédia inséré avec l’éditeur WYSIWYG. Les URL statiques sont absolues et interrompues si l’[URL de base](../stores-purchase/store-urls.md) du magasin change.

   - `No` : (par défaut) utilise des URL dynamiques pour le contenu multimédia inséré avec l’éditeur WYSIWYG, en fonction de la directive `\{\{media url="..."}}`. Les URL dynamiques sont relatives et ne sont pas rompues si l’URL de base du magasin change.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
