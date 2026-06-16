---
title: Le  [!DNL Media Gallery]
description: Utilisez la Galerie de médias pour organiser et gérer vos fichiers multimédias sur le serveur.
exl-id: bf730e46-70f3-405c-88cf-62d0a3e8634f
feature: Page Content, Media
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
TQID: https://experienceleague.adobe.com/PL80USg-GVh-vlWwoYCuWRzJdO-FzHDFmFSDjxhavo8
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
source-wordcount: 352
ht-degree: 0%

---

# Le [!DNL Media Gallery]

Avec Adobe Commerce ou Magento Open Source 2.4, les commerçants peuvent utiliser le nouveau [!DNL Media Gallery] _amélioré_ pour organiser et gérer leurs fichiers multimédias sur le serveur. Cette nouvelle [!DNL Media Gallery] contient les mêmes fonctionnalités que le stockage multimédia existant, mais comprend une interface utilisateur améliorée et une intégration plus étroite avec [Adobe Stock](https://stock.adobe.com).

![Images affichées dans la grille Galerie de médias](./assets/media-gallery-grid.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Les images de produit ajoutées à la section de produit [&#128279;](../catalog/product-image.md#upload-an-image) ne sont pas gérées par le [!DNL Media Gallery]. _[!UICONTROL Images and Videos]_&#x200B;Seules les images utilisées dans les champs de la section Produit&#x200B;_[!UICONTROL Content]_ sont affichées et filtrées dans la nouvelle [!DNL Media Gallery].

## Activer la nouvelle [!DNL Media Gallery]

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery]**.

   ![Configuration avancée - [!DNL Media Gallery]](./assets/system-media-gallery.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Enable Old Media Gallery]** sur `No`.

1. Cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous y êtes invité, cliquez sur le lien **[!UICONTROL Cache Management]** dans le message système et actualisez le cache non valide.

   Le menu [[!UICONTROL Content] affiche désormais &#x200B;](/help/content-design/content-menu.md) nouvelle option de _[!UICONTROL Media Gallery]_.

>[!NOTE]
>
>La fonctionnalité complète des nouvelles [!DNL Media Gallery] nécessite le démarrage des clients de file d’attente `media.gallery.synchronization` et `media.content.synchronization` pour la synchronisation initiale. Voir [&#x200B; Gestion des files d’attente de messages &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) dans le _Guide de configuration_ pour plus d’informations.

## Accéder au nouveau [!DNL Media Gallery]

Le nouveau [!DNL Media Gallery] est accessible à partir du menu Contenu ou lorsque vous [ajoutez ou modifiez une page](/help/content-design/page-add.md). Vous pouvez également y accéder lorsque vous [créez ou modifiez une catégorie](/help/catalog/category-create.md) ou lorsque vous [insérez des images à l’aide de l’éditeur de contenu](/help/content-design/editor-insert-image.md).

Pour accéder au nouveau [!UICONTROL Media Gallery] via le menu [!UICONTROL Content] :

- Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

Pour accéder à la nouvelle Galerie de médias lorsque vous ajoutez ou modifiez une page :

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Cliquez sur **[!UICONTROL Add a New Page]**.

   Si vous souhaitez modifier une page existante, vous pouvez utiliser la colonne _[!UICONTROL Action]_&#x200B;pour cliquer sur **[!UICONTROL Select]**&#x200B;et choisir **[!UICONTROL Edit]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Content]** et procédez comme suit :

   - Si le [Page Builder est activé](../page-builder/setup.md), développez le panneau **[!UICONTROL Media]** et faites glisser un espace réservé **[!UICONTROL Image]** vers le conteneur cible. Cliquez ensuite sur **[!UICONTROL Select from Gallery]**.

     ![Faire glisser l’image vers l’étape](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

   - Si l&#39;éditeur [WYSIWYG est activé](/help/content-design/editor.md) cliquez sur **[!UICONTROL Show/Hide Editor]**, puis sur **[!UICONTROL Insert Image]**.

## [!DNL Media Gallery] de démonstration

Pour en savoir plus sur le [!DNL Media Gallery], regardez cette vidéo :

>[!VIDEO](https://video.tv.adobe.com/v/343785?quality=12&learn=on)
