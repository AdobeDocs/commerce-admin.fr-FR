---
title: Optimisation des images de Media Gallery
description: Découvrez comment utiliser l’optimisation des images pour vos ressources  [!DNL Commerce]  médias.
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# Optimisation des images de Media Gallery

La nouvelle [Galerie de médias](media-gallery.md) offre une fonctionnalité _optimisation des images_ qui améliore les performances et réduit la taille des fichiers multimédias sur le storefront. Cette optimisation est activée par défaut et peut être modifiée dans les paramètres de configuration du magasin.

## Configuration de l’optimisation des images

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** et procédez comme suit :

   - Définissez **[!UICONTROL Enable Image Optimization]** sur `Yes`.
   - Saisissez les valeurs **[!UICONTROL Maximum Width]** et **[!UICONTROL Maximum Height]** (en pixels) selon vos besoins.

## Comportement

Lorsque la fonctionnalité d’optimisation des images de la Galerie de médias est activée, une copie optimisée d’une image est automatiquement insérée dans le contenu à partir de la [Galerie de médias](media-gallery.md) au lieu du fichier d’origine.

Lorsque les valeurs _Largeur maximale_ et _Hauteur maximale_ sont modifiées dans la configuration, elle met à jour toutes les images optimisées existantes qui ont été insérées précédemment.

L’optimisation des images de la Galerie de médias nécessite que les consommateurs de la file d’attente `media.gallery.renditions.update` s’exécutent pour régénérer des images optimisées lorsque la configuration est modifiée. Voir [ Gestion des files d’attente de messages ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) dans le _Guide de configuration_ pour plus d’informations.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}
