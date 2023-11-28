---
title: Stockage multimédia
description: Découvrez comment le stockage des médias vous aide à organiser et à accéder aux fichiers multimédia de Commerce stockés sur le serveur.
exl-id: 5cf1bb20-d747-4a12-8558-e167c229efe8
feature: Page Content, Media
source-git-commit: 7dae6b6d387c796c5ff472293c6590fabaa83e85
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Stockage multimédia

Le stockage multimédia vous permet d’organiser et d’accéder aux fichiers multimédias stockés sur le serveur. Le chemin d’accès à l’emplacement des fichiers est déterminé par le [URL de base](../stores-purchase/store-urls.md) configuration. Les fichiers du stockage multimédia sont accessibles à partir de l’éditeur lorsque vous travaillez sur des pages et des blocs statiques. En règle générale, le stockage de médias réside dans le système de fichiers sur le même serveur que la variable [!DNL Commerce] fichiers de programme.

Vous pouvez également gérer les fichiers multimédia dans une [base](media-storage-database.md)ou sur un serveur distinct ou [réseau de diffusion de contenu](media-storage-content-delivery-network.md). L’avantage de l’utilisation d’un stockage alternatif est qu’il minimise l’effort requis pour synchroniser les médias. Les performances de synchronisation sont particulièrement affectées lorsque plusieurs instances du système sont déployées sur différents serveurs qui doivent accéder aux mêmes images, fichiers CSS et autres fichiers multimédias.

L’éditeur peut être configuré pour utiliser des [URL Dynamic Media](../catalog/catalog-urls.md#configure-catalog-media-url-format) pour le contenu du catalogue dans les descriptions de catégorie ou de produit.

![[!DNL Commerce] Stockage multimédia](./assets/media-storage.png){width="650" zoomable="yes"}

## Ajout de fichiers au stockage multimédia

Les deux premières étapes sont les mêmes que si vous insérez une image.

1. Sur le [éditeur](editor.md) , cliquez sur _Insérer une image_ Icône

   ![Icône Insérer une image](./assets/editor-toolbar-image-button.png){width="700" zoomable="yes"}

   Cette action ouvre la fenêtre _[!UICONTROL Insert/edit image]_boîte de dialogue.

1. Après _[!UICONTROL Source]_, cliquez sur le_ Rechercher _icône (![Icône Rechercher](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}).

1. Dans l’arborescence de répertoire à gauche, effectuez l’une des opérations suivantes :

   - Accédez au dossier dans lequel vous souhaitez enregistrer l’image chargée.

   - Accédez à l’emplacement où vous souhaitez créer un dossier et cliquez sur **Créer un dossier**.

     Pour ajouter un dossier, saisissez son nom, puis cliquez sur **[!UICONTROL OK]**.

1. Pour ajouter un ou plusieurs fichiers à Media Storage, vous pouvez charger les fichiers à partir de votre système ou utiliser la variable [Intégration Adobe Stock](adobe-stock.md):

   Pour charger des fichiers depuis votre système, cliquez sur **[!UICONTROL Choose Files]** et procédez comme suit :

   - Dans le répertoire de votre ordinateur local, accédez à l’emplacement des images.

   - Sélectionnez chaque image à télécharger.

   - Cliquez sur **[!UICONTROL Open]**.

   Pour utiliser des ressources d’Adobe Stock à l’aide de la méthode [integration](adobe-stock.md):

   - Cliquez sur **[!UICONTROL Search Adobe Stock]**.

   - Ajout d’un aperçu ou d’une image sous licence depuis Adobe Stock (voir [Utilisation d’images Adobe Stock](adobe-stock-manage.md)).

Les images sont téléchargées dans le dossier Media Storage actuel du serveur.

![[!DNL Commerce] Stockage multimédia](./assets/media-storage.png){width="650" zoomable="yes"}

## Insertion d’une image à partir d’un stockage multimédia

Ouvrez la page ou le bloc à modifier. Utilisez ensuite l’une des méthodes suivantes pour insérer une image à partir du stockage multimédia :

### Méthode 1 : mode WYSIWYG

1. Sur le [éditeur](editor.md) , cliquez sur _Insérer une image_ Icône

1. Après _[!UICONTROL Source]_, cliquez sur le_ Rechercher _icône (![Icône Rechercher](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}).

   ![Sélectionner l’icône de recherche](./assets/editor-dialog-insert-image.png){width="250" zoomable="yes"}

1. Dans l’arborescence de gauche, accédez au dossier dans lequel l’image est stockée.

1. Sélectionnez la mosaïque de l’image et cliquez sur **[!UICONTROL Add Selected]**.

### Méthode 2 : mode HTML

1. Placez le curseur dans le code où la fonction `<img>` est à insérer.

1. Cliquez sur **[!UICONTROL Insert Image]**.

   ![Insérer une image (mode HTML)](./assets/editor-html-mode-insert-image.png){width="600" zoomable="yes"}
