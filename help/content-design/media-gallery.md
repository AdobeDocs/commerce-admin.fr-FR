---
title: La variable [!DNL Media Gallery]
description: Utilisez la galerie de médias pour organiser et gérer vos fichiers multimédia sur le serveur.
exl-id: bf730e46-70f3-405c-88cf-62d0a3e8634f
feature: Page Content, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# La variable [!DNL Media Gallery]

Avec Adobe Commerce ou Magento Open Source 2.4, les marchands peuvent utiliser la nouvelle _amélioré_ [!DNL Media Gallery] pour organiser et gérer leurs fichiers multimédias sur le serveur. Cette nouvelle [!DNL Media Gallery] contient les mêmes fonctionnalités que le stockage multimédia existant, mais comprend une interface utilisateur améliorée et une intégration plus étroite avec [Adobe Stock][adobe-stock].

![Images affichées dans la grille Galerie de médias](./assets/media-gallery-grid.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Images de produit ajoutées au [_[!UICONTROL Images and Videos]_section produit](../catalog/product-image.md#upload-an-image) ne sont pas gérés par la variable [!DNL Media Gallery]. Seules les images utilisées dans la variable_[!UICONTROL Content]_ les champs de section de produit sont affichés et filtrés dans la nouvelle [!DNL Media Gallery].

## Activez la nouvelle [!DNL Media Gallery]

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery]**.

   ![Configuration avancée - [!DNL Media Gallery]](./assets/system-media-gallery.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Enable Old Media Gallery]** to `No`.

1. Cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous y êtes invité, cliquez sur l’icône **[!UICONTROL Cache Management]** dans le message système et actualisez le cache non valide.

   La variable [[!UICONTROL Content] menu](/help/content-design/content-menu.md) affiche désormais la nouvelle _[!UICONTROL Media Gallery]_.

>[!NOTE]
>
>Fonctionnalités complètes pour la nouvelle [!DNL Media Gallery] require `media.gallery.synchronization` et `media.content.synchronization` consommateurs de file d’attente à démarrer pour la synchronisation initiale. Voir [Gestion des files d’attente de messages](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) dans le _Guide de configuration_ pour plus d’informations.

## Accédez au nouveau [!DNL Media Gallery]

La nouvelle [!DNL Media Gallery] est accessible à partir du menu Contenu ou lorsque vous [ajout ou modification d’une page](/help/content-design/page-add.md). Vous pouvez également y accéder lorsque vous [créer ou modifier une catégorie](/help/catalog/category-create.md)ou lorsque vous [insérer des images à l’aide de l’éditeur de contenu ;](/help/content-design/editor-insert-image.md).

Pour accéder au [!UICONTROL Media Gallery] par le biais du [!UICONTROL Content] menu :

- Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

Pour accéder à la nouvelle galerie de médias lorsque vous ajoutez ou modifiez une page :

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Cliquez sur **[!UICONTROL Add a New Page]**.

   Si vous souhaitez modifier une page existante, vous pouvez utiliser la variable _[!UICONTROL Action]_colonne à cliquer **[!UICONTROL Select]**et choisissez **[!UICONTROL Edit]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Content]** et procédez comme suit :

   - Si vous avez [Créateur de pages activé](../page-builder/setup.md), développez la variable **[!UICONTROL Media]** et faites glisser un **[!UICONTROL Image]** balise d’emplacement du conteneur cible. Cliquez ensuite sur **[!UICONTROL Select from Gallery]**.

     ![Faire glisser l’image vers l’étape](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

   - Si vous avez le [Éditeur WYSIWYG activé](/help/content-design/editor.md), cliquez sur **[!UICONTROL Show/Hide Editor]** puis cliquez sur **[!UICONTROL Insert Image]**.

## [!DNL Media Gallery] demo

Pour en savoir plus sur la variable [!DNL Media Gallery], regardez cette vidéo :

>[!VIDEO](https://video.tv.adobe.com/v/343785?quality=12)

[adobe-stock]: https://stock.adobe.com

