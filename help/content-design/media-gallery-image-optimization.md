---
title: Optimisation des images de la galerie multimédia
description: Découvrez comment utiliser l’optimisation des images pour vos [!DNL Commerce] ressources multimédias.
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
source-git-commit: a93e96353f4be0e771064cdcfbdf794772386a28
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Optimisation des images de la galerie multimédia

La nouvelle [Galerie de médias](media-gallery.md) fournit une _optimisation des images_ qui améliore les performances et réduit la taille des fichiers multimédia sur le storefront. Cette optimisation est activée par défaut et peut être modifiée dans les paramètres de configuration du magasin.

## Configuration de l’optimisation des images

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** et procédez comme suit :

   - Définir **[!UICONTROL Enable Image Optimization]** to `Yes`.
   - Saisissez le **[!UICONTROL Maximum Width]** et **[!UICONTROL Maximum Height]** en pixels selon vos besoins.

## Comportement

Lorsque la fonctionnalité d’optimisation des images de la galerie multimédia est activée, une copie optimisée d’une image est automatiquement insérée dans le contenu à partir du [Galerie de médias](media-gallery.md) au lieu du fichier d’origine.

Lorsque la variable _Largeur maximale_ et _Hauteur maximale_ est modifiée dans la configuration, elle met à jour toutes les images optimisées existantes qui ont été insérées précédemment.

L’optimisation des images de la galerie multimédia requiert que la variable `media.gallery.renditions.update` les clients de file d’attente s’exécutent pour régénérer des images optimisées lorsque la configuration est modifiée. Voir [Gestion des files d’attente de messages](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) dans le _Guide de configuration_ pour plus d’informations.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}
