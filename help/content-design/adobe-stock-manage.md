---
title: Utilisation des images Adobe Stock
description: Améliorez vos pages de boutique avec des images provenant d’Adobe Stock.
exl-id: 8f7d6f0a-511f-4f4b-821d-10a06e18041e
feature: CMS, Media
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '1013'
ht-degree: 0%

---

# Utilisation des images Adobe Stock

Les images [Adobe Stock](https://stock.adobe.com) peuvent être utilisées à la place du chargement de votre propre contenu d’image. Un cas d’utilisation courant consiste à charger et à placer du contenu d’image lors de la création d’une page.

Le [[!DNL Media Gallery]](media-gallery.md) offre une intégration directe à Adobe Stock, ce qui facilite l’obtention de licences pour vos images directement depuis la page de la galerie.

## Accès à la grille de recherche d’Adobe Stock

Le panneau de recherche Adobe Stock est accessible lorsque vous [ajoutez ou modifiez une page](page-add.md), lorsque vous [créez ou modifiez une catégorie](../catalog/category-create.md) ou lorsque vous [insérez des images via l’éditeur de contenu](editor-insert-image.md).

**_Pour rechercher des ressources Adobe Stock et ajouter une image système à une page, procédez comme suit_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Cliquez sur **[!UICONTROL Add a New Page]**.

   Si vous souhaitez modifier une page existante, vous pouvez utiliser la colonne _[!UICONTROL Action]_&#x200B;pour cliquer sur **[!UICONTROL Select]**&#x200B;et choisir **[!UICONTROL Edit]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Content]** et procédez comme suit :

   - Si l&#39;éditeur [WYSIWYG est activé](editor.md) cliquez sur **[!UICONTROL Show/Hide Editor]**, puis sur **[!UICONTROL Insert Image]**.

   - Si le [Page Builder est activé](../page-builder/setup.md), développez le panneau **[!UICONTROL Media]** et faites glisser un espace réservé **[!UICONTROL Image]** vers le conteneur cible. Cliquez ensuite sur **[!UICONTROL Select from Gallery]**.

     ![Glisser une image vers l’étape Page Builder](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Search Adobe Stock]**.

**_Pour rechercher des ressources Adobe Stock et ajouter une image système à une catégorie, procédez comme suit_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Cliquez sur **[!UICONTROL Add Root Category]** ou **[!UICONTROL Add Subcategory]**.

   Si vous souhaitez ajouter l’image à une catégorie existante, cliquez sur le nom de la catégorie dans la liste de gauche.

1. Développez la section **[!UICONTROL Content]**, puis sous _[!UICONTROL Category Image]_&#x200B;cliquez sur **[!UICONTROL Select from Gallery]**.

1. Cliquez sur **[!UICONTROL Search Adobe Stock]**.

Pour rechercher des ressources Adobe Stock et ajouter une image système à partir de l’éditeur WYSIWYG :

1. cliquez sur **[!UICONTROL Show/Hide Editor]**.

1. Cliquez sur **[!UICONTROL Insert Image]**.

1. Cliquez sur **[!UICONTROL Search Adobe Stock]**.

   ![Résultats de la recherche Adobe Stock](./assets/adobe-stock-search-grid.png){width="600" zoomable="yes"}

## Filtrer et rechercher des ressources Adobe Stock

La [grille de recherche Adobe Stock](#access-the-adobe-stock-search-grid) fournit des fonctionnalités d’interrogation et de filtrage pour vous aider à trouver l’image parfaite pour vos magasins de [!DNL Commerce].

Par défaut, les résultats de recherche affichés proviennent d’une galerie de quelques centaines de résultats organisée par Adobe Stock. Lorsque vous effectuez votre propre recherche par mot-clé, vous recherchez les millions de ressources disponibles via Adobe Stock.

### Recherche de ressources Adobe Stock par mots-clés

1. [Accédez à la grille de recherche Adobe Stock](#access-the-adobe-stock-search-grid).

1. Saisissez votre mot-clé dans le champ de saisie **[!UICONTROL Search by keyword]** en haut à gauche et cliquez sur la loupe ou appuyez sur **Entrée**.

   ![Résultats de la recherche Adobe Stock pour le mot-clé « mango »](./assets/adobe-stock-search-keyword.png){width="600" zoomable="yes"}

### Filtrage des ressources Adobe Stock

1. [Exécutez une recherche par mot-clé des ressources Adobe Stock](#search-for-adobe-stock-assets-by-keywords).

1. Cliquez sur **[!UICONTROL Filters]**.

   Plusieurs filtres sont disponibles pour affiner les résultats de votre recherche :

   | Filtre | Description |
   |---|---|
   | [!UICONTROL Subcategory] | Filtrez les images **Photos** ou **Illustrations** |
   | [!UICONTROL Orientation] | Filtrer les images par taille, forme et aspect |
   | [!UICONTROL Color] | Utilisation d’une palette de couleurs pour filtrer les images par couleur |
   | [!UICONTROL Price] | Filtrer les images en fonction de leur coût |
   | [!UICONTROL Safe search] | Activer ou désactiver la recherche sécurisée |
   | [!UICONTROL Isolated Assets] | Limitez l’affichage aux _ressources isolées_, où les objets s’affichent seuls sur un arrière-plan solide |

   {style="table-layout:auto"}

   ![Filtres de recherche Adobe Stock](./assets/adobe-stock-filters.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Apply Filters]**.

   La grille des résultats de la recherche est mise à jour avec votre recherche affinée.

## Afficher les détails de l’image

Chaque image contient des détails disponibles pour l’affichage. D’autres actions spécifiques à l’image, telles que [enregistrement d’aperçus d’image](adobe-stock-save-preview.md) ou [enregistrement (et éventuellement licence) d’images](adobe-stock-license-image.md), sont disponibles via cette vue détaillée.

1. [Accédez à la grille de recherche Adobe Stock](#access-the-adobe-stock-search-grid).

1. Cliquez sur une image dans les résultats de la recherche.

   D’autres détails sur l’image s’affichent, tels que :

   - Une version plus grande de l’image
   - Métadonnées d’image, telles que _[!UICONTROL Dimensions]_,_[!UICONTROL File type]_, _[!UICONTROL Category]_,_[!UICONTROL File]_ et _Mots-clés_
   - Images associées, telles que des images de la même _série_ ou _modèle_
   - Boutons d’action, tels que [[!UICONTROL Save Preview]](adobe-stock-save-preview.md) et [[!UICONTROL Save (and optionally license) Image]](adobe-stock-license-image.md)

     ![Détails de l’image Adobe Stock](./assets/adobe-stock-image-details.png){width="600" zoomable="yes"}

## Connectez-vous à votre compte Adobe

Pour obtenir un accès complet à une image et éliminer le filigrane Adobe Stock, vous devez vous [connecter à l’aide d’un compte Adobe](https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html) et acheter des crédits pour acquérir des droits d’utilisation d’une image.

1. [Accédez à la grille de recherche Adobe Stock](#access-the-adobe-stock-search-grid).

1. Cliquez sur **[!UICONTROL Sign In]** en haut à droite.

   Une nouvelle fenêtre de navigateur vous guide tout au long du processus de connexion à [Adobe](https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html).

   Une fois le processus de connexion terminé, l’état sous licence des images s’affiche dans les résultats de recherche sous forme de libellé.

   ![Connexion à Adobe](./assets/adobe-stock-account-login.png){width="600" zoomable="yes"}

### Afficher l’état sous licence des résultats de recherche

[Connectez-vous à votre compte Adobe](#log-in-to-your-adobe-account).

Toutes les images sous licence associées à votre compte Adobe comportent un libellé qui permet d’identifier clairement les images sous licence.

![Résultats de la recherche Adobe Stock avec des images sous licence](./assets/adobe-stock-licensed-images.png){width="600" zoomable="yes"}

### Enregistrer les images dans le stockage multimédia

Les images recherchées à l’aide de l’intégration d’Adobe Stock peuvent être enregistrées dans le [!DNL Commerce] [stockage multimédia](media-storage.md) pour une réutilisation facile dans votre banque de [!DNL Commerce].

Vous pouvez enregistrer deux types d’images : un [aperçu d’image](adobe-stock-save-preview.md) ou une [image sous licence](adobe-stock-license-image.md).

#### Enregistrement d’un aperçu d’image

Un aperçu d’image est une version en filigrane d’une ressource Adobe Stock. Les aperçus d’images sont gratuits et sont un bon moyen de tester différentes images avant de décider d’acheter une licence pour des images spécifiques et de les utiliser dans vos magasins de production.

1. [Accédez à la grille de recherche Adobe Stock](#access-the-adobe-stock-search-grid).

1. Pour [afficher les détails de l’image](#view-image-details), cliquez sur une image dans la grille de recherche.

1. Cliquez sur **[!UICONTROL Save Preview]**.

   Cette action affiche une invite vous demandant de spécifier un nom de fichier utilisé pour enregistrer l’image dans l’espace de stockage multimédia. Un nom de fichier par défaut est fourni, mais vous pouvez personnaliser le nom en fonction de vos préférences.

   ![Enregistrer l’image d’aperçu Adobe Stock](./assets/adobe-stock-save-preview.png){width="500" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Confirm]**.

   La page redirige vers l’espace de stockage multimédia et l’aperçu que vous avez enregistré s’affiche.

#### Enregistrer une image sous licence

Les ressources Adobe Stock que vous souhaitez utiliser pour vos magasins de [!DNL Commerce] de production doivent disposer d’une licence. L’octroi de licence vous garantit un accès légal à l’image et vous permet d’éliminer le filigrane Adobe Stock présent dans tous les [aperçus d’image](adobe-stock-save-preview.md). Pour acquérir des images sous licence ou enregistrer des images déjà sous licence, vous devez être connecté à votre compte Adobe.

1. [Connectez-vous à votre compte Adobe](#log-in-to-your-adobe-account).

1. Pour [afficher les détails de l’image](#view-image-details), cliquez sur une image dans la grille de recherche.

1. Selon le statut de licence actuel de l’image, effectuez l’une des opérations suivantes :

   - Si l’image est déjà sous licence, cliquez sur **[!UICONTROL Save]**.

   - Si l’image n’est _pas_ sous licence, cliquez sur **[!UICONTROL License and Save]**.

     >[!NOTE]
     >
     >Vous devez disposer de [crédits Adobe Stock disponibles](https://helpx.adobe.com/stock/help/credit-packs.html) sur votre compte pour obtenir la licence de l’image.

   Cette action affiche une invite vous demandant de spécifier un nom de fichier utilisé pour enregistrer l’image dans le [espace de stockage multimédia](media-storage.md). Un nom de fichier par défaut est fourni, mais vous pouvez personnaliser le nom en fonction de vos préférences.

1. Cliquez sur **[!UICONTROL Confirm]**.

   La page redirige vers l’espace de stockage multimédia et l’aperçu que vous avez enregistré s’affiche.
