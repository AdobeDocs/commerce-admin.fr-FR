---
title: Stockage de média
description: Découvrez comment le stockage multimédia vous permet d’organiser les fichiers multimédias Commerce stockés sur le serveur et d’y accéder.
exl-id: 5cf1bb20-d747-4a12-8558-e167c229efe8
feature: Page Content, Media
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 0%

---

# Stockage de média

Le stockage des médias vous permet d’organiser les fichiers multimédias stockés sur le serveur et d’y accéder. Le chemin d’accès à l’emplacement des fichiers est déterminé par la configuration [URL de base](../stores-purchase/store-urls.md). Les fichiers du stockage multimédia sont accessibles à partir de l’éditeur lors de l’utilisation de pages et de blocs statiques. En règle générale, le stockage des médias se trouve dans le système de fichiers sur le même serveur que les fichiers de programme [!DNL Commerce].

Vous pouvez également gérer les fichiers multimédias dans une [base de données](media-storage-database.md), sur un serveur distinct ou sur un [réseau de diffusion de contenu](media-storage-content-delivery-network.md). L’utilisation d’un autre stockage présente l’avantage de minimiser l’effort de synchronisation des médias. Les performances de synchronisation sont particulièrement affectées lorsque plusieurs instances du système sont déployées sur différents serveurs qui doivent accéder aux mêmes images, fichiers CSS et autres fichiers multimédias.

L’éditeur peut être configuré pour utiliser des URL statiques ou [URL Dynamic Media](../catalog/catalog-urls.md#configure-catalog-media-url-format) pour le contenu du catalogue dans les descriptions de catégories ou de produits.

Stockage ![[!DNL Commerce] Media](./assets/media-storage.png){width="650" zoomable="yes"}

## Ajouter des fichiers au stockage multimédia

Les deux premières étapes sont identiques à celles de l’insertion d’une image.

1. Dans la barre d’outils [éditeur](editor.md), cliquez sur l’icône _Insérer une image_.

   ![ Icône Insérer une image ](./assets/editor-toolbar-image-button.png){width="700" zoomable="yes"}

   Cette action ouvre la boîte de dialogue _[!UICONTROL Insert/edit image]_.

1. Après _[!UICONTROL Source]_, cliquez sur l’icône_ Rechercher _(![icône Rechercher](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}).

1. Dans l’arborescence de répertoire sur la gauche, effectuez l’une des opérations suivantes :

   - Accédez au dossier dans lequel vous souhaitez enregistrer l’image chargée.

   - Accédez à l’emplacement où vous souhaitez créer un dossier et cliquez sur **Créer un dossier**.

     Pour ajouter un dossier, saisissez son nom et cliquez sur **[!UICONTROL OK]**.

1. Pour ajouter un ou plusieurs fichiers au stockage multimédia, vous pouvez télécharger les fichiers à partir de votre système ou utiliser l’[intégration Adobe Stock](adobe-stock.md) :

   Pour charger des fichiers à partir de votre système, cliquez sur **[!UICONTROL Choose Files]** et procédez comme suit :

   - Dans le répertoire de votre ordinateur local, accédez à l’emplacement des images.

   - Sélectionnez chaque image à charger.

   - Cliquez sur **[!UICONTROL Open]**.

   Pour utiliser des ressources d’Adobe Stock à l’aide de l’intégration [](adobe-stock.md) :

   - Cliquez sur **[!UICONTROL Search Adobe Stock]**.

   - Ajoutez un aperçu ou une image sous licence à partir d’Adobe Stock (voir [ Utilisation d’images Adobe Stock](adobe-stock-manage.md)).

Les images sont chargées dans le dossier Stockage multimédia actuel sur le serveur.

Stockage ![[!DNL Commerce] Media](./assets/media-storage.png){width="650" zoomable="yes"}

## Insertion d’une image à partir du stockage multimédia

Ouvrez la page ou le bloc à modifier. Utilisez ensuite l’une des méthodes suivantes pour insérer une image à partir de l’espace de stockage multimédia :

### Méthode 1 : mode WYSIWYG

1. Dans la barre d’outils [éditeur](editor.md), cliquez sur l’icône _Insérer une image_.

1. Après _[!UICONTROL Source]_, cliquez sur l’icône_ Rechercher _(![icône Rechercher](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}).

   ![Sélection de l’icône de recherche](./assets/editor-dialog-insert-image.png){width="250" zoomable="yes"}

1. Dans l’arborescence de gauche, accédez au dossier dans lequel l’image est stockée.

1. Sélectionnez la mosaïque de l’image et cliquez sur **[!UICONTROL Add Selected]**.

### Méthode 2 : mode HTML

1. Placez le curseur dans le code à l’endroit où la balise `<img>` doit être insérée.

1. Cliquez sur **[!UICONTROL Insert Image]**.

   ![Insérer une image (mode HTML)](./assets/editor-html-mode-insert-image.png){width="600" zoomable="yes"}
