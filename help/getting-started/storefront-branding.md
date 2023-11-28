---
title: Marque Storefront
description: Découvrez comment modifier les éléments qui définissent l’identité de marque de votre magasin.
exl-id: 91630717-9da7-4d2f-a0d8-adb794a30ee1
feature: Storefront
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '1285'
ht-degree: 0%

---

# Marque Storefront

Une des premières choses que vous voulez faire est de [modifier le logo ;](#upload-your-logo) dans l’en-tête et [télécharger une favicon](#add-a-favicon) pour le navigateur. Ensuite, vous devriez [ajouter votre message de bienvenue](#change-the-welcome-message) et [mettre à jour la notification de copyright](#change-the-copyright-notice) dans le pied de page. Ces tâches sont quelques éléments de conception simples dont vous pouvez vous occuper immédiatement. Lorsque votre magasin est en cours de développement, vous pouvez [activation de l’avis de démonstration du magasin](#set-the-store-demo-notice), puis supprimez-le lorsque vous êtes prêt à le lancer.

![Éléments de marque Storefront](./assets/storefront-home-page-branding.png){width="600" zoomable="yes"}

## Télécharger votre logo

La taille et l’emplacement du logo dans l’en-tête sont déterminés par le thème de magasin. Votre logo peut être enregistré en tant que type de fichier GIF, PNG ou JPG (JPEG) et téléchargé depuis l’administrateur de votre boutique.

![Logo dans l’en-tête](./assets/storefront-header-logo.png){width="600"}

L’image du logo se trouve à l’emplacement suivant sur le serveur. Tout fichier image portant le nom `logo.svg` est utilisé comme logo de thème par défaut.

Chemin complet - `app/design/frontend/[vendor]/[theme]/web/images/logo.svg`

Chemin relatif -  `images/logo.svg`

Si vous ne connaissez pas la taille du logo ou des autres images utilisées dans votre thème, ouvrez la page dans un navigateur, cliquez avec le bouton droit de la souris sur l’image et examinez l’élément.

>[!NOTE]
>
>Outre le logo dans l’en-tête, votre logo s’affiche également sur [modèles d&#39;email](../systems/email-templates.md#prepare-your-email-logo) et [factures PDF](../stores-purchase/sales-documents.md) et d’autres documents de vente. Les logos utilisés pour les modèles d&#39;email et les factures ont des tailles différentes et doivent être téléchargés séparément.

Formats de fichiers de logo pris en charge :

| Format du fichier | Description |
|--- |--- |
| PNG | (Graphiques réseau mobiles) Cette nouvelle alternative au format de GIF prend en charge jusqu’à 16 millions de couleurs (24 bits). Le format de compression sans perte produit une image bitmap de haute qualité avec du texte clair, mais un fichier plus volumineux que certains formats. Le format PNG prend en charge les calques transparents et est conçu pour l’affichage en ligne et la diffusion en continu. |
| GIF | (Format d’échange graphique) Format bitmap plus ancien et largement pris en charge, limité à 256 couleurs (8 bits). Le format de GIF prend en charge l’animation simple et les calques transparents. |
| JPG (JPEG) | (Groupe d’experts photographiques interarmées) Format bitmap compressé utilisé par la plupart des appareils photo numériques. La compression avec perte entraîne une perte de données, qui est parfois perceptible sous la forme de zones floues dans le texte. |

{style="table-layout:auto"}

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

   ![Page de configuration de conception](./assets/design-configuration.png){width="700"}

1. Recherchez la vue de magasin à configurer, puis cliquez sur **[!UICONTROL Edit]** dans le _[!UICONTROL Action]_colonne .

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Header]** .

   ![Paramètres d’en-tête](./assets/configuration-header.png){width="600"}

1. Pour charger un nouveau logo, cliquez sur **[!UICONTROL Upload]** et sélectionnez le fichier sur votre système.

1. Saisissez le **[!UICONTROL Logo Image Width]** et **[!UICONTROL Logo Image Height]** en pixels.

1. Pour **[!UICONTROL Logo Image Alt]**, saisissez le texte à afficher lorsque quelqu’un survole l’image.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Configuration]**.

## Ajout d’une favicon

_Favicon_ est court pour _icône préférée_ et fait référence à la petite icône de l’onglet de chaque page du navigateur. Selon le navigateur, l’icône favicon s’affiche également dans la barre d’adresse, juste avant l’URL.

Une favicon fait généralement 16 x 16 pixels ou 32 x 32 pixels de taille. [!DNL Commerce] accepte les types de fichiers ICO, PNG, APNG, GIF et JPG (JPEG), bien que tous les navigateurs ne prennent pas en charge ces formats. Le format de fichier le plus souvent pris en charge pour une favicon est ICO. Vous pouvez utiliser d’autres types de fichiers image, mais le format peut ne pas être pris en charge par tous les navigateurs. Il existe de nombreux outils gratuits en ligne que vous pouvez utiliser pour générer une image ICO ou convertir une image dans ce format.

![Favicon dans l’onglet du navigateur](./assets/storefront-favicon.png){width="600"}

[!DNL Commerce] prend en charge les formats de fichiers suivants en tant que favicon :

| Format du fichier | Description |
|--- |--- |
| ICO | Ce format de fichier image est conçu pour les images d’icônes d’ordinateur de petite taille. Principalement utilisé sous Microsoft® Windows OS, le format ICO peut contenir des images de 256 x 256 pixels et 16 millions de couleurs (24 bits) avec 8 bits de transparence. |
| PNG | (Graphiques réseau mobiles) Cette nouvelle alternative au format de GIF prend en charge jusqu’à 16 millions de couleurs (24 bits). Le format de compression sans perte produit une image bitmap de haute qualité avec du texte clair, mais un fichier plus volumineux que certains formats. Le format PNG prend en charge les calques transparents et est conçu pour l’affichage en ligne et la diffusion en continu. |
| APNG | (Animated Portable Network Graphics) Format de fichier similaire au format PNG qui prend en charge l’animation simple. |
| GIF | (Format d’échange graphique) Format bitmap plus ancien et largement pris en charge, limité à 256 couleurs (8 bits). Le format de GIF prend en charge l’animation simple et les calques transparents. |
| JPG (JPEG) | (Groupe d’experts photographiques interarmées) Format bitmap compressé utilisé par la plupart des appareils photo numériques. La compression avec perte entraîne une perte de données, qui est parfois perceptible sous la forme de zones floues dans le texte. |

{style="table-layout:auto"}

### Étape 1 : création d’une favicon

1. A l’aide de l’éditeur d’image de votre choix, créez une image graphique de votre logo 16 x 16 ou 32 x 32.

1. (Facultatif) Utilisez l’un des outils en ligne disponibles pour convertir le fichier au format .ico et enregistrer le fichier sur votre ordinateur.

### Étape 2 : téléchargement de la favicon vers votre boutique

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Dans la grille, recherchez la vue de magasin que vous souhaitez configurer, puis cliquez sur **[!UICONTROL Edit]** dans le _[!UICONTROL Action]_colonne .

1. Sous _[!UICONTROL Other Settings]_, développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL HTML Head]**.

   ![Paramètres d’en-tête de HTML](./assets/configuration-html-head.png){width="600"}

1. Si vous souhaitez supprimer l’icône de favicon actuelle, cliquez sur le bouton _Supprimer_ (![Icône Corbeille](../assets/icon-delete-trashcan.png)) dans le coin inférieur gauche de l’image.

1. Cliquez sur **[!UICONTROL Upload]** et ouvrez le fichier favicon que vous avez préparé.

   ![favicon téléchargé](./assets/favicon-upload.png){width="400"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Configuration]**.

### Étape 3 : Actualisation du cache

1. Lorsque vous êtes invité à actualiser le cache, cliquez sur le **[!UICONTROL Cache Management]** dans le message en haut de l’espace de travail.

1. Dans la liste, sélectionnez le **[!UICONTROL Page Cache]** de la case à cocher marquée `Invalidated`.

1. Définir **[!UICONTROL Actions]** to `Refresh` et cliquez sur **[!UICONTROL Submit]**.

1. Pour afficher la nouvelle favicon, revenez à votre vitrine et actualisez le navigateur.

## Modifier le message de bienvenue

Le message de bienvenue dans l’en-tête se développe afin d’inclure le nom du client connecté. Avant de lancer votre boutique, veillez à modifier la valeur par défaut. _Bienvenue_ texte pour chaque vue de magasin.

![Message de bienvenue](./assets/storefront-welcome-message.png){width="600"}

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Dans la grille, recherchez la vue de magasin que vous souhaitez configurer, puis cliquez sur **[!UICONTROL Edit]** dans le _[!UICONTROL Action]_colonne .

1. Sous _[!UICONTROL Other Settings]_, développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Header]**.

1. Pour **[!UICONTROL Welcome Text]**, saisissez le texte du message de bienvenue que vous souhaitez voir apparaître dans l’en-tête de votre boutique.

   ![Paramètres d’en-tête](./assets/configuration-header.png){width="600"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Configuration]**.

1. Lorsque vous êtes invité à mettre à jour le cache de page, cliquez sur le bouton **[!UICONTROL Cache Management]** lien situé en haut de l’espace de travail et suivez les instructions pour actualiser le cache.

## Modification de la notification de copyright

Votre boutique affiche un avis de copyright dans le pied de page de chaque page. En règle générale, la mention de copyright doit inclure l’année en cours et identifier votre société comme propriétaire légal du contenu sur le site.

![Exemple de notification de copyright](./assets/storefront-footer-copyright.png){width="600"}

La variable `&copy;` Le code de caractère est utilisé pour insérer le symbole de copyright, comme illustré dans les exemples suivants :

- Exemple de format long

  `Copyright &copy; 2013-present Luma, Inc. All rights reserved.`

- Exemple de format court

  `&copy; 2021 Luma, Inc. All rights reserved.`

**_Pour mettre à jour la notification de copyright :_**

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Dans la grille, recherchez la vue de magasin que vous souhaitez configurer, puis cliquez sur **[!UICONTROL Edit]** dans le _[!UICONTROL Action]_colonne .

1. Sous _Autres paramètres_, développer ![Sélecteur d’extension](../assets/icon-display-expand.png)la valeur **[!UICONTROL Footer]** .

   ![Paramètres de conception du pied de page](./assets/configuration-footer.png){width="600"}

1. Pour **[!UICONTROL Copyright]**, saisissez la note de copyright que vous souhaitez voir apparaître dans le pied de page de chaque page.

   Utilisez la variable `&copy;` code de caractère pour insérer un symbole de copyright.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Configuration]**.

## Définition de l’avis de démonstration du magasin

Si votre boutique est en ligne, mais qu’elle est toujours en construction, vous pouvez afficher un avis de démonstration en haut de la page pour informer les utilisateurs que la boutique n’est pas encore ouverte pour les besoins professionnels. Lorsque vous êtes prêt à _go live_, supprimez simplement le message. Cela revient à retourner le panneau suspendu dans la fenêtre à partir de _Fermé_ to _Ouvrir_. Le format de l’avis de démonstration est déterminé par le thème de votre magasin.

![Avis de démonstration de Storefront](./assets/storefront-demo-notice.png){width="600"}

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Dans la grille, recherchez la vue de magasin que vous souhaitez configurer, puis cliquez sur **[!UICONTROL Edit]** dans le _[!UICONTROL Action]_colonne .

1. Sous _[!UICONTROL Other Settings]_, développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL HTML Head]**.

   ![HTML Head](./assets/configuration-html-head.png){width="600"}

1. Faites défiler l’écran vers le bas et définissez la variable **[!UICONTROL Display Demo Store Notice]** selon vos préférences.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Configuration]**.

1. Si vous êtes invité à mettre à jour le cache, cliquez sur **[!UICONTROL Cache Management]** dans le message système et suivez les instructions pour actualiser le cache.
