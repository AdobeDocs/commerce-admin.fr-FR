---
title: Optimisation des images de Media Gallery
description: Découvrez comment utiliser l’optimisation des images pour vos ressources  [!DNL Commerce]  médias.
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
TQID: https://experienceleague.adobe.com/BTjXX6X70q2Mwm0xPNx-t429R5m93VprCHBDcYgQNpY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 211
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

L’optimisation des images de la Galerie de médias nécessite que les consommateurs de la file d’attente `media.gallery.renditions.update` s’exécutent pour régénérer des images optimisées lorsque la configuration est modifiée. Voir [&#x200B; Gestion des files d’attente de messages &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html?lang=fr) dans le _Guide de configuration_ pour plus d’informations.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}

<!-- Last updated from includes: 2024-01-30 15:43:39 -->
