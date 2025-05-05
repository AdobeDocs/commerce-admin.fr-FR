---
title: Licence d’une image Adobe Stock
description: Pour garantir un accès légal et éliminer le filigrane Adobe Stock, autorisez vos images Adobe Stock sous licence.
exl-id: a2d6b7b8-e9ac-4f3e-bcd1-05e2bb74b6c2
feature: CMS, Media
source-git-commit: 0d072ecdba696383bd33b88b64d751736429f2f6
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---

# Licence d’une image Adobe Stock

Les ressources Adobe Stock que vous souhaitez utiliser pour vos boutiques Adobe Commerce et Magento Open Source de production doivent être sous licence. Cette licence vous garantit un accès légal à l’image et élimine le filigrane Adobe Stock présent sur tous les [aperçus d’image](./adobe-stock-save-preview.md). Pour acquérir sous licence des images ou enregistrer des images déjà sous licence, vous devez être connecté à votre compte Adobe.

Le nouveau [[!DNL Media Gallery]](media-gallery.md) offre une intégration directe à Adobe Stock, ce qui facilite la licence de vos images directement à partir de la page de la galerie.

>[!BEGINSHADEBOX]

**Conditions préalables**

La fonctionnalité de licence Adobe Stock n’est disponible que si l’ [intégration Adobe Stock](./adobe-stock.md) est installée et configurée. L&#39;obtention de licences [Adobe Stock][adobe-stock] nécessite un forfait Adobe Stock payant et un [compte d&#39;Adobe][adobe-signin].

>[!ENDSHADEBOX]

## Licence d&#39;une image à partir du nouvel [!DNL Media Gallery]

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Suivez les étapes de la section [Utilisation d’images Adobe Stock](./adobe-stock-manage.md) pour vous connecter et enregistrer les images d’aperçu dans le [stockage multimédia](./media-storage.md).

   ![Image de prévisualisation enregistrée](./assets/adobe-stock-gallery-unlicensed.png){width="600" zoomable="yes"}

1. Cliquez sur les trois points sous l’image (![Icône de menu Ressource](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}), puis cliquez sur **[!UICONTROL License]**.

   ![Actions d’image Adobe Stock](./assets/adobe-stock-gallery-image-actions.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Si vous n’êtes pas connecté, le formulaire de connexion s’affiche. Pour plus d’informations sur la connexion, voir [Utilisation d’images Adobe Stock](./adobe-stock-manage.md).

1. Dans la boîte de dialogue de confirmation de licence, cliquez sur **[!UICONTROL Confirm]** pour accorder une licence à l’image.

   ![Confirmation de licence](./assets/adobe-stock-gallery-license-confirm.png){width="350" zoomable="yes"}

   >[!NOTE]
   >
   >Vous devez disposer des [crédits Adobe Stock][stock-credits] disponibles dans votre compte pour obtenir une licence pour l’image.

## Licence d’une image à partir du stockage multimédia standard

1. [Accédez à la grille de recherche Adobe Stock][access-search].

1. Pour [afficher les détails de l’image][view-details], cliquez sur une image dans la grille de recherche dans l’ordre.

1. Selon l’état actuel des licences de l’image, effectuez l’une des opérations suivantes :

   - Si l’image est déjà sous licence, cliquez sur **[!UICONTROL Save]**.

   - Si l’image n’est pas _sous licence_, cliquez sur **[!UICONTROL License and Save]**.

     >[!NOTE]
     >
     >Vous devez disposer des [crédits Adobe Stock][stock-credits] disponibles dans votre compte pour obtenir une licence pour l’image.

   Cette action vous invite à spécifier un nom de fichier utilisé pour enregistrer l’image dans le [stockage multimédia](./media-storage.md). Un nom de fichier par défaut est fourni, mais vous pouvez le personnaliser selon vos préférences.

   ![Enregistrer l’image sous licence Adobe Stock](./assets/adobe-stock-save-licensed.png){width="550" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Confirm]**.

   La page redirige vers le stockage de médias et l’aperçu enregistré s’affiche.

[access-search]: adobe-stock-manage.md#access-the-adobe-stock-search-grid
[view-details]: adobe-stock-manage.md#view-image-details
[stock-credits]: https://helpx.adobe.com/fr/stock/help/credit-packs.html
[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/fr/manage-account/using/access-adobe-id-account.html
