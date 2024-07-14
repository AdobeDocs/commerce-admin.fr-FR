---
title: Ajout d’une fiche d’inventaire
description: Découvrez comment ajouter un stock et mapper des sources aux canaux de vente (sites web), en fournissant un lien direct vers les quantités vendables et les inventaires de produits.
exl-id: d0032ed7-c0d6-4654-b182-43a165e7dcf6
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# Ajouter un stock

Les stocks mappent vos sources aux canaux de vente (ou sites web), fournissant un lien direct vers les quantités et les stocks de produits vendables.

Lors de la création d’un stock personnalisé, vous attribuez des sites web et des sources. Les sources peuvent inclure des sources activées et désactivées. Par exemple, vous pouvez ajouter un entrepôt à votre stock, en vous préparant à ouvrir l’emplacement de gestion du stock et de réalisation des envois.

Après avoir ajouté des sources, vous devez donner la priorité à l’ordre des sources du haut (d’abord) vers le bas (d’abord). Cette commande affecte les recommandations lors de l’expédition de la commande.

![New Stock](assets/inventory-stock-new.png){width="600" zoomable="yes"}

## Ajouter le stock

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stock]**.

1. Cliquez sur **[!UICONTROL Add New Stock]**.

1. Développez la section ![Sélecteur d&#39;extension](../assets/icon-display-expand.png) et saisissez un **[!UICONTROL Name]** unique pour identifier le nouveau stock.**[!UICONTROL General]**

   ![Options de stock générales](assets/inventory-stock-general.png){width="350" zoomable="yes"}

1. Développez la section ![Sélecteur d&#39;extension](../assets/icon-display-expand.png) et sélectionnez l&#39;élément **[!UICONTROL Websites]** où ce stock est disponible.**[!UICONTROL Sales Channels]**

   Pour une installation multi-site, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée, puis cliquez sur chaque site web.

   >[!NOTE]
   >
   >Si vous sélectionnez un site web ou un canal de vente affecté à un autre stock, il n’est pas attribué à partir de ce stock. Tous les Sales Channel non affectés à un stock personnalisé sont affectés au stock par défaut.

   ![Options Sales Channel pour les stocks](assets/inventory-sales-channel.png){width="350" zoomable="yes"}

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) et procédez comme suit pour tout autre stock que le stock par défaut :**[!UICONTROL Sources]**

   - Cliquez sur **[!UICONTROL Assign Sources]**.

   ![Sources attribuées](assets/inventory-stock-sources.png){width="350" zoomable="yes"}

   - Cochez les cases correspondant à toutes les sources que vous souhaitez affecter au stock.

   >[!IMPORTANT]
   >
   >Si vous attribuez la même source à plusieurs stocks, cela peut entraîner une vente excessive des produits affectés à cette source.

   - Cliquez sur **[!UICONTROL Done]**.

     Les sources ajoutées s’affichent dans Sources affectées.

     ![Attribuer des sources à Stock](assets/inventory-assign-sources.png){width="600" zoomable="yes"}

1. Utilisez ![Icône Tri](assets/icon-sort.png) pour faire glisser les sources dans une priorité allant du haut (premier) au bas (dernier).

   La commande source est importante lors des commandes d’expédition.

   ![Exemple de sources attribuées](assets/inventory-stock-priority-after.png){width="600" zoomable="yes"}

1. Dans le menu _[!UICONTROL Save]_(![Flèche de menu](../assets/icon-menu-down-arrow-red.png)), choisissez **[!UICONTROL Save & Close]**.

## Descriptions des champs

| Champ | Description |
|--|--|
| **[!UICONTROL General]** | |
| [!UICONTROL Name] | Nom du stock. Par exemple : `UK Stock`, `US Stock` |
| **[!UICONTROL Sales Channels]** | |
| [!UICONTROL Websites] | Définit la [portée](../getting-started/websites-stores-views.md#scope-settings) du stock en attribuant le stock à des sites web spécifiques sous la forme de _canaux de vente_. Sélectionnez un ou plusieurs sites web par stock. Chaque site web ne peut être affecté qu’à un seul stock. |
| **[!UICONTROL Sources]** | |
| [!UICONTROL Assign Sources] | Attribue des sources d’inventaire à ce stock. Les sources personnalisées ne peuvent pas être affectées au stock par défaut. |
| [!UICONTROL Assigned Sources] | Liste des sources affectées. Faites glisser et déposez les sources à l’aide de ![Icône Tri](assets/icon-sort.png) dans un ordre de priorité pour l’exécution et l’expédition des commandes.<br/><br/>**[!UICONTROL Code]**- ID de code unique de la source.<br/>**[!UICONTROL Name]** - Nom de la description de la source.<br/>**[!UICONTROL Unassign]**- Supprimez la source affectée du stock à l’aide de l’icône ![Corbeille](../assets/icon-delete-trashcan-solid.png). |
