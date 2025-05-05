---
title: Optimisation des images de la galerie multimédia
description: Découvrez comment utiliser l’optimisation des images pour vos ressources multimédias  [!DNL Commerce] .
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
source-git-commit: a93e96353f4be0e771064cdcfbdf794772386a28
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Optimisation des images de la galerie multimédia

La nouvelle [galerie de médias](media-gallery.md) offre une fonction _d’optimisation d’image_, qui améliore les performances et réduit la taille des fichiers multimédia sur le storefront. Cette optimisation est activée par défaut et peut être modifiée dans les paramètres de configuration du magasin.

## Configuration de l’optimisation des images

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** et procédez comme suit :

   - Définissez **[!UICONTROL Enable Image Optimization]** sur `Yes`.
   - Saisissez les valeurs **[!UICONTROL Maximum Width]** et **[!UICONTROL Maximum Height]** (en pixels) selon vos besoins.

## Comportement

Lorsque la fonctionnalité d’optimisation des images de la galerie multimédia est activée, une copie optimisée d’une image est automatiquement insérée dans le contenu de la [galerie multimédia](media-gallery.md) au lieu du fichier d’origine.

Lorsque les valeurs _Largeur maximale_ et _Hauteur maximale_ sont modifiées dans la configuration, elles mettent à jour toutes les images optimisées existantes qui ont été insérées précédemment.

L’optimisation des images de la galerie multimédia requiert que les clients de la file d’attente `media.gallery.renditions.update` s’exécutent pour générer à nouveau des images optimisées lorsque la configuration est modifiée. Pour plus d’informations, voir [Gestion des files d’attente de messages](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html?lang=fr) dans le _Guide de configuration_.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}
