---
title: Archiver les commandes
description: Découvrez comment configurer l’archive des commandes pour améliorer les performances et rationaliser Commerce pour votre organisation.
exl-id: 12025591-bfe2-4f44-9358-a38ea4493b5c
feature: Orders, Configuration
TQID: https://experienceleague.adobe.com/Zl8qJPnr8JcSSyIHewPH-GFKBkweyAmh7So9u7vHDSk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 750
ht-degree: 0%

---

# Archiver les commandes

{{ee-feature}}

L’archivage régulier des commandes améliore les performances et libère votre espace de travail des informations inutiles, ce qui vous permet de vous concentrer sur votre activité actuelle. Les factures, les livraisons et les avoirs peuvent être archivés automatiquement ou manuellement et peuvent être consultés à tout moment.

>[!NOTE]
>
>L’option _[!UICONTROL Archive]_apparaît dans le menu [[!UICONTROL Sales] uniquement lorsque ](sales-menu.md)’archivage est [ activé](../configuration-reference/sales/sales.md).

## Configuration de l’archive des commandes

Votre boutique peut être configurée pour archiver les commandes, les factures, les livraisons et les avoirs après un nombre défini de jours. Vous pouvez déplacer les commandes et les documents associés vers l&#39;archive ou les restaurer à leur état précédent. Les commandes archivées ne sont pas supprimées et restent disponibles auprès de l’administrateur. Les données archivées peuvent être exportées dans un fichier CSV et ouvertes dans une feuille de calcul. Lorsqu’elle est activée, l’action _Archiver_ s’affiche en haut de l’espace de travail.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez la section **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales]** en dessous.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]** .

   ![Paramètres de configuration de l&#39;archivage des commandes, factures, expéditions, avoirs](../configuration-reference/sales/assets/sales-orders-invoices-shipments-credit-memos-archiving.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Enable Archiving]** sur `Yes`.

   >[!NOTE]
   >
   >Si vous décidez par la suite de désactiver l’archivage, tous les ordres archivés sont restaurés à l’état précédent.

1. Définissez **[!UICONTROL Archive Orders Purchased]** sur le nombre de jours à attendre avant l&#39;archivage des commandes terminées.

   Par défaut, les commandes sont archivées 30 jours après l’achat.

1. Dans la liste **[!UICONTROL Order Statuses to be Archived]**, sélectionnez chaque statut de commande à utiliser pour identifier les commandes à archiver.

   Pour sélectionner plusieurs éléments, maintenez la touche Ctrl (Windows) ou Commande (Mac) enfoncée tout en cliquant sur chaque élément.

1. Cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous y êtes invité, actualisez tout cache non valide.

## Affichage des documents archivés

1. Dans le menu _[!UICONTROL Sales]_sous_[!UICONTROL Archive]_, choisissez l’une des options suivantes :

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. Pour afficher les détails, cliquez sur un document archivé de la liste.

## Appliquer une action à un document archivé

Sélectionnez chaque document à cibler par l’action et choisissez l’une des **[!UICONTROL Actions]** suivantes :

- `Cancel`
- `Hold`
- `Unhold`
- `Print`
- `Move to Orders Management`

## Archiver manuellement des documents

1. Sélectionnez le type de document à archiver parmi les options suivantes :

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. Cochez la case de chaque élément à archiver.

1. Dans le coin supérieur droit, définissez **[!UICONTROL Actions]** sur `Move to Archive`.

1. Cliquez sur **[!UICONTROL Submit]** pour archiver les documents sélectionnés.

## Restaurer des documents archivés

1. Choisissez le type de document à restaurer.

1. Sélectionnez des documents à l’aide de l’une des options suivantes :

   - Pour sélectionner tous les documents visibles, dans le coin supérieur gauche, cliquez sur **[!UICONTROL Select Visible]**.

   - Cochez manuellement la case de chaque document à restaurer.

1. Dans le coin supérieur droit, définissez **[!UICONTROL Action]** sur `Move to Orders Management`.

1. Cliquez sur **[!UICONTROL Submit]** pour restaurer les documents.

## Exporter des documents archivés

1. Choisissez le type de document que vous souhaitez exporter.

1. Dans le menu supérieur droit, définissez **[!UICONTROL Export to:]** sur l’une des valeurs suivantes :

   - `CSV`
   - `Excel`

1. Cliquez sur **[!UICONTROL Export]**.

Votre boutique peut être configurée pour archiver les commandes, les factures, les livraisons et les avoirs après un nombre défini de jours. Vous pouvez déplacer les commandes et les documents associés vers l&#39;archive ou les restaurer à leur état précédent. Les commandes archivées ne sont pas supprimées et restent disponibles auprès de l’administrateur. Les données archivées peuvent être exportées dans un fichier CSV et ouvertes dans une feuille de calcul. Lorsqu’elle est activée, la commande _[!UICONTROL Archive]_s’affiche en haut de l’espace de travail.

## Archiver les commandes manuellement

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Pour sélectionner l&#39;ordre dans la grille, cochez la case située dans la première colonne.

1. Définissez le contrôle **[!UICONTROL Actions]** sur `Move to Archive` et recherchez le message indiquant que la commande a été archivée.

   ![Déplacer les commandes sélectionnées vers le ](./assets/order-move-to-archive.png){width="700" zoomable="yes"} d&#39;archivage

>[!TIP]
>
>Pour spécifier une liste des statuts de commande pouvant être archivés, voir [Configurer l’archivage des commandes](#configure-the-order-archive).

## Afficher une commande archivée

1. Ouvrez la vue d’archive à l’aide de l’une des méthodes suivantes :

   - Dans la barre de boutons située au-dessus de la grille de _[!UICONTROL Orders]_, cliquez sur **[!UICONTROL Go to Archive]**.

   - Dans la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Archive]_>**[!UICONTROL Orders]**.

   >[!NOTE]
   >
   >Tout comme la page Commandes , le titre de la page Commandes archivées est _[!UICONTROL Orders]_. La seule différence notable est l’option à_[!UICONTROL Return to Orders Management]_ dans la barre de boutons. L’URL de la page indique également que vous vous trouvez dans l’archive de commandes.

1. Dans la colonne _Action_, cliquez sur **[!UICONTROL View]**.

   ![Afficher une commande archivée](./assets/order-archived-view.png){width="600" zoomable="yes"}

## Restaurer une commande archivée

>[!NOTE]
>
>Une commande restaurée à partir d’une commande archivée est archivée à nouveau en fonction du nombre de jours configuré dans le paramètre [!UICONTROL Archive Orders Purchased] (voir [Configurer l’archivage des commandes](#configure-the-order-archive)). Le nombre de jours est calculé par rapport à la date de [!UICONTROL Updated At] de la commande, qui est modifiée lorsque la commande est déplacée de l&#39;archive.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Dans la barre de boutons, cliquez sur **[!UICONTROL Go to Archive]**.

1. Recherchez l’enregistrement à restaurer et cliquez sur la case à cocher pour le sélectionner.

   ![Sélectionner l’ordre de restauration](./assets/order-archived-select-to-restore.png){width="600" zoomable="yes"}

1. Définissez la valeur du contrôle de **[!UICONTROL Actions]** sur `Move to Order Management`.

Recherchez le message indiquant que la commande archivée a été supprimée de l’archive.

## Exporter la commande archivée

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Dans le menu d’actions, cliquez sur **[!UICONTROL Export]** et sélectionnez le format souhaité.
