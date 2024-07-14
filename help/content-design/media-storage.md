---
title: Stockage multimédia
description: Découvrez comment le stockage des médias vous aide à organiser et à accéder aux fichiers multimédias Commerce stockés sur le serveur.
exl-id: 5cf1bb20-d747-4a12-8558-e167c229efe8
feature: Page Content, Media
source-git-commit: 7dae6b6d387c796c5ff472293c6590fabaa83e85
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Stockage multimédia

Le stockage multimédia vous permet d’organiser et d’accéder aux fichiers multimédias stockés sur le serveur. Le chemin d’accès à l’emplacement des fichiers est déterminé par la configuration [base URL](../stores-purchase/store-urls.md). Les fichiers du stockage multimédia sont accessibles à partir de l’éditeur lorsque vous travaillez sur des pages et des blocs statiques. En règle générale, le stockage multimédia réside dans le système de fichiers sur le même serveur que les fichiers de programme [!DNL Commerce].

Vous pouvez également gérer les fichiers multimédias dans une [base de données](media-storage-database.md), ou sur un serveur distinct ou sur le [réseau de diffusion de contenu](media-storage-content-delivery-network.md). L’avantage de l’utilisation d’un stockage alternatif est qu’il minimise l’effort requis pour synchroniser les médias. Les performances de synchronisation sont particulièrement affectées lorsque plusieurs instances du système sont déployées sur différents serveurs qui doivent accéder aux mêmes images, fichiers CSS et autres fichiers multimédias.

L’éditeur peut être configuré pour utiliser des [URL de média dynamique](../catalog/catalog-urls.md#configure-catalog-media-url-format) ou statiques pour le contenu d’un catalogue dans une catégorie ou des descriptions de produit.

![[!DNL Commerce] Stockage de médias](./assets/media-storage.png){width="650" zoomable="yes"}

## Ajout de fichiers au stockage multimédia

Les deux premières étapes sont les mêmes que si vous insérez une image.

1. Dans la barre d&#39;outils [editor](editor.md), cliquez sur l&#39;icône _Insérer une image_ .

   ![Icône Insérer une image](./assets/editor-toolbar-image-button.png){width="700" zoomable="yes"}

   Cette action ouvre la boîte de dialogue _[!UICONTROL Insert/edit image]_.

1. Après _[!UICONTROL Source]_, cliquez sur l&#39;icône_ Rechercher _(![Icône Rechercher](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}).

1. Dans l’arborescence de répertoire à gauche, effectuez l’une des opérations suivantes :

   - Accédez au dossier dans lequel vous souhaitez enregistrer l’image chargée.

   - Accédez à l’emplacement où vous souhaitez créer un dossier et cliquez sur **Créer un dossier**.

     Pour ajouter un dossier, saisissez le nom du dossier et cliquez sur **[!UICONTROL OK]**.

1. Pour ajouter un ou plusieurs fichiers à Media Storage, vous pouvez télécharger les fichiers à partir de votre système ou utiliser l’ [intégration Adobe Stock](adobe-stock.md) :

   Pour charger des fichiers à partir de votre système, cliquez sur **[!UICONTROL Choose Files]** et procédez comme suit :

   - Dans le répertoire de votre ordinateur local, accédez à l’emplacement des images.

   - Sélectionnez chaque image à télécharger.

   - Cliquez sur **[!UICONTROL Open]**.

   Pour utiliser des ressources d’Adobe Stock à l’aide de l’ [intégration](adobe-stock.md) :

   - Cliquez sur **[!UICONTROL Search Adobe Stock]**.

   - Ajoutez un aperçu ou une image sous licence d’Adobe Stock (voir [Utilisation d’images Adobe Stock](adobe-stock-manage.md)).

Les images sont téléchargées dans le dossier Media Storage actuel du serveur.

![[!DNL Commerce] Stockage de médias](./assets/media-storage.png){width="650" zoomable="yes"}

## Insertion d’une image à partir d’un stockage multimédia

Ouvrez la page ou le bloc à modifier. Utilisez ensuite l’une des méthodes suivantes pour insérer une image à partir du stockage multimédia :

### Méthode 1 : mode WYSIWYG

1. Dans la barre d&#39;outils [editor](editor.md), cliquez sur l&#39;icône _Insérer une image_ .

1. Après _[!UICONTROL Source]_, cliquez sur l&#39;icône_ Rechercher _(![Icône Rechercher](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}).

   ![Sélectionner l’icône de recherche](./assets/editor-dialog-insert-image.png){width="250" zoomable="yes"}

1. Dans l’arborescence de gauche, accédez au dossier dans lequel l’image est stockée.

1. Sélectionnez la mosaïque de l&#39;image et cliquez sur **[!UICONTROL Add Selected]**.

### Méthode 2 : mode HTML

1. Placez le curseur dans le code où la balise `<img>` doit être insérée.

1. Cliquez sur **[!UICONTROL Insert Image]**.

   ![Insérer une image (mode HTML)](./assets/editor-html-mode-insert-image.png){width="600" zoomable="yes"}
