---
title: Ajouter un stock
description: Découvrez comment ajouter un stock et mapper des sources aux canaux de vente (sites web), en fournissant un lien direct vers les quantités à vendre et les inventaires de produits.
exl-id: d0032ed7-c0d6-4654-b182-43a165e7dcf6
TQID: https://experienceleague.adobe.com/oP-H4hvUmNunTl-hThx4ytzC6qOXa1PhK4P1omwFBUg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 409
ht-degree: 0%

---

# Ajouter un stock

Les stocks mappent vos sources aux canaux de vente (ou sites web), fournissant un lien direct aux quantités à vendre et aux inventaires de produits.

Lors de la création d’un stock personnalisé, vous affectez des sites web et des sources. Les sources peuvent inclure des sources activées et désactivées. Par exemple, vous pouvez ajouter un entrepôt à votre stock, vous préparer à ouvrir l&#39;emplacement pour gérer les stocks et terminer les expéditions.

Après avoir ajouté des sources, vous devez donner la priorité à l’ordre des sources, du haut (premier) au bas (dernier). Cette commande affecte les recommandations lors de l&#39;expédition de la commande.

![Nouveau stock](assets/inventory-stock-new.png){width="600" zoomable="yes"}

## Ajouter le stock d’inventaire

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stock]**.

1. Cliquez sur **[!UICONTROL Add New Stock]**.

1. Développez ![Sélecteur de développement](../assets/icon-display-expand.png) la section **[!UICONTROL General]** et saisissez un **[!UICONTROL Name]** unique pour identifier le nouveau stock.

   ![Options générales sur actions](assets/inventory-stock-general.png){width="350" zoomable="yes"}

1. Développez ![Sélecteur de développement](../assets/icon-display-expand.png) la section **[!UICONTROL Sales Channels]** et sélectionnez le **[!UICONTROL Websites]** où ce stock est disponible.

   Pour une installation multisite, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et cliquez sur chaque site Web.

   >[!NOTE]
   >
   >Si vous sélectionnez un site web ou un canal de vente affecté à un autre stock, l’affectation de ce stock est annulée. Tous les canaux de vente qui ne sont pas affectés à un stock personnalisé sont affectés au stock par défaut.

   ![Options des canaux de vente pour les stocks](assets/inventory-sales-channel.png){width="350" zoomable="yes"}

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Sources]** et procédez comme suit pour tout stock autre que le stock par défaut :

   - Cliquez sur **[!UICONTROL Assign Sources]**.

   ![Sources affectées](assets/inventory-stock-sources.png){width="350" zoomable="yes"}

   - Cochez les cases correspondant à toutes les sources que vous souhaitez affecter au stock.

   >[!IMPORTANT]
   >
   >Si vous affectez la même source à plusieurs stocks, cela peut entraîner une survente des produits affectés à cette source.

   - Cliquez sur **[!UICONTROL Done]**.

     Les sources ajoutées s’affichent dans Sources affectées.

     ![Affecter des sources au stock](assets/inventory-assign-sources.png){width="600" zoomable="yes"}

1. Utilisez l’icône ![Trier](assets/icon-sort.png) pour faire glisser les sources et les déposer dans une priorité allant du haut (première) au bas (dernière).

   La commande source est importante lors de l&#39;expédition des commandes.

   ![Exemple de sources affectées](assets/inventory-stock-priority-after.png){width="600" zoomable="yes"}

1. Dans le menu _[!UICONTROL Save]_(![flèche du menu](../assets/icon-menu-down-arrow-red.png)), choisissez **[!UICONTROL Save & Close]**.

## Descriptions des champs

| Champ | Description |
|--|--|
| **[!UICONTROL General]** | |
| [!UICONTROL Name] | Nom du stock. Par exemple : `UK Stock`, `US Stock` |
| **[!UICONTROL Sales Channels]** | |
| [!UICONTROL Websites] | Définit la [portée](../getting-started/websites-stores-views.md#scope-settings) du stock en affectant le stock à des sites web spécifiques en tant que _canaux de vente_. Sélectionnez un ou plusieurs sites web par stock. Chaque site web ne peut être affecté qu&#39;à un seul stock. |
| **[!UICONTROL Sources]** | |
| [!UICONTROL Assign Sources] | Attribue des origines de stock à ce stock. Les sources personnalisées ne peuvent pas être affectées au stock par défaut. |
| [!UICONTROL Assigned Sources] | Liste des sources attribuées. Faites glisser et déposez les sources à l’aide de l’icône ![Trier](assets/icon-sort.png) dans un ordre de priorité pour l’exécution des commandes et l’expédition.<br/><br/>**[!UICONTROL Code]**- ID de code unique pour la source.<br/>**[!UICONTROL Name]** - Description du nom de la source.<br/>**[!UICONTROL Unassign]**- Supprimez la source affectée du stock à l’aide de ![icône Corbeille](../assets/icon-delete-trashcan-solid.png). |
