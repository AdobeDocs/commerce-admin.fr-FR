---
title: Configuration de l’algorithme de priorité Source
description: Découvrez comment configurer la priorité de la source utilisée pour l’ordre des sources affectées dans votre stock afin de faire des recommandations.
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
TQID: https://experienceleague.adobe.com/TB4THYjkzbNvEbsjNzOewNtYS6JoRvLDiQQCovSMkbI
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 271
ht-degree: 0%

---

# Configuration de l’algorithme de priorité Source

Les stocks personnalisés comprennent une liste attribuée de sources à vendre et expédient les stocks de produits disponibles par l&#39;intermédiaire de votre storefront. Cet algorithme utilise l’ordre des sources affectées dans votre stock pour émettre des recommandations.

Lorsqu’il est exécuté, l’algorithme :

- Passe par l&#39;ordre configuré des sources au niveau du stock, en commençant par le haut

- Recommande une quantité à expédier et une origine par produit en fonction de l&#39;ordre dans la liste, de la quantité disponible et de la quantité commandée

- Continue dans la liste jusqu&#39;à ce que l&#39;expédition de la commande soit remplie

- Ignore les sources désactivées si elles figurent dans la liste

Pour configurer, organisez ces sources de haut en bas en priorité pour exécuter les commandes. L&#39;algorithme Source Selection Algorithm (SSA) fournit un algorithme Priorité en utilisant cet ordre lors de la détermination des déductions d&#39;expédition et de stock. Voir [ Hiérarchisation des sources pour un stock](stocks-prioritize-sources.md).

## Configurer la priorité des sources

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**.

1. Ouvrez un stock en mode d’édition et accédez à la zone de _[!UICONTROL Sources]_.

1. Cliquez sur **[!UICONTROL Assign Sources]**.

1. Dans la vue _[!UICONTROL Assign Sources]_, cochez la case correspondant à la source souhaitée, puis cliquez sur **[!UICONTROL Done]**pour affecter une source au stock.

>[!NOTE]
>
>Lors de l’utilisation de l’algorithme [Priorité de distance](distance-priority-algorithm.md) pour l’expédition, si les itinéraires et les données ne sont pas renvoyés pour le [mode de calcul](distance-priority-algorithm.md) sélectionné (conduite, bicyclette ou marche) pour une expédition, la SSA utilise par défaut la priorité Source.

![Ordre de Source après la hiérarchisation](assets/inventory-stock-priority-after.png)

| Icônes | Description |
|----------------------------------------------|----------------------------------------------------------------|
| ![glissez-déposez l’icône pour définir la priorité](assets/icon-drag-and-drop-action.png) | Utilisez pour faire glisser et déposer des sources en fonction de leur priorité. |
| ![cliquez sur icône pour annuler l’affectation d’une source](assets/icon-delete-action.png) | Annulation de l&#39;affectation d&#39;une source à un stock. |
