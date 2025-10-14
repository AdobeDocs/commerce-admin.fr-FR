---
title: Archiver les commandes
description: Découvrez comment configurer l’archive de commandes afin d’améliorer les performances et de rationaliser Commerce pour votre organisation.
exl-id: 12025591-bfe2-4f44-9358-a38ea4493b5c
feature: Orders, Configuration
source-git-commit: 47f170f1a1dd1c236b99c2e7139bb119368abf47
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# Archiver les commandes

{{ee-feature}}

L’archivage des commandes améliore régulièrement les performances et évite à votre espace de travail d’avoir à fournir des informations superflues, afin que vous puissiez vous concentrer sur l’activité actuelle. Les factures, les envois et les notes de crédit peuvent être archivés automatiquement ou manuellement et peuvent être affichés à tout moment.

>[!NOTE]
>
>L’option _[!UICONTROL Archive]_&#x200B;apparaît dans le menu [[!UICONTROL Sales] &#x200B;](sales-menu.md) uniquement lorsque l’archivage est [activé](../configuration-reference/sales/sales.md).

## Configuration de l’archive de commande

Votre boutique peut être configurée pour archiver des commandes, des factures, des envois et des notes de crédit après un nombre défini de jours. Vous pouvez déplacer les commandes et les documents associés dans l’archive ou les restaurer à leur état précédent. Les commandes archivées ne sont pas supprimées et restent disponibles auprès de l’administrateur. Les données archivées peuvent être exportées dans un fichier CSV et ouvertes dans une feuille de calcul. Lorsque cette option est activée, l’action _Archiver_ s’affiche en haut de l’espace de travail.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez la section **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales]** en dessous.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]** .

   ![Commandes, factures, envois, paramètres de configuration de l’archivage des notes de crédit](../configuration-reference/sales/assets/sales-orders-invoices-shipments-credit-memos-archiving.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Enable Archiving]** sur `Yes`.

   >[!NOTE]
   >
   >Si vous décidez par la suite de désactiver l’archivage, toutes les commandes archivées sont restaurées à l’état précédent.

1. Définissez **[!UICONTROL Archive Orders Purchased]** sur le nombre de jours à attendre avant que les commandes terminées ne soient archivées.

   Par défaut, les commandes sont archivées 30 jours après l’achat.

1. Dans la liste **[!UICONTROL Order Statuses to be Archived]**, sélectionnez chaque état de commande à utiliser pour identifier les commandes à archiver.

   Pour sélectionner plusieurs éléments, maintenez la touche Ctrl (Windows) ou Commande (Mac) enfoncée lorsque vous cliquez sur chaque élément.

1. Cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous y êtes invité, actualisez le cache non valide.

## Affichage des documents archivés

1. Dans le menu _[!UICONTROL Sales]_&#x200B;sous&#x200B;_[!UICONTROL Archive]_, sélectionnez l’une des options suivantes :

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. Pour afficher les détails, cliquez sur un document archivé dans la liste.

## Application d’une action à un document archivé

Sélectionnez chaque document pour être la cible de l’action et choisissez l’une des **[!UICONTROL Actions]** suivantes :

- `Cancel`
- `Hold`
- `Unhold`
- `Print`
- `Move to Orders Management`

## Archivage manuel de documents

1. Sélectionnez le type de document à archiver à partir des éléments suivants :

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. Cochez la case de chaque élément que vous souhaitez archiver.

1. Dans le coin supérieur droit, définissez **[!UICONTROL Actions]** sur `Move to Archive`.

1. Cliquez sur **[!UICONTROL Submit]** pour archiver les documents sélectionnés.

## Restaurer des documents archivés

1. Sélectionnez le type de document à restaurer.

1. Sélectionnez des documents à l’aide de l’une des options suivantes :

   - Pour sélectionner tous les documents visibles, dans le coin supérieur gauche, cliquez sur **[!UICONTROL Select Visible]**.

   - Cochez manuellement la case de chaque document à restaurer.

1. Dans le coin supérieur droit, définissez **[!UICONTROL Action]** sur `Move to Orders Management`.

1. Cliquez sur **[!UICONTROL Submit]** pour restaurer les documents.

## Exporter des documents archivés

1. Sélectionnez le type de document à exporter.

1. Dans le menu supérieur droit, définissez **[!UICONTROL Export to:]** sur l’une des valeurs suivantes :

   - `CSV`
   - `Excel`

1. Cliquez sur **[!UICONTROL Export]**.

Votre boutique peut être configurée pour archiver des commandes, des factures, des envois et des notes de crédit après un nombre défini de jours. Vous pouvez déplacer les commandes et les documents associés dans l’archive ou les restaurer à leur état précédent. Les commandes archivées ne sont pas supprimées et restent disponibles auprès de l’administrateur. Les données archivées peuvent être exportées dans un fichier CSV et ouvertes dans une feuille de calcul. Lorsque cette option est activée, la commande _[!UICONTROL Archive]_&#x200B;s’affiche en haut de l’espace de travail.

## Archivage manuel des commandes

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Pour sélectionner l’ordre dans la grille, cochez la case dans la première colonne.

1. Définissez le contrôle **[!UICONTROL Actions]** sur `Move to Archive` et recherchez le message que la commande a été archivée.

   ![Déplacement des commandes sélectionnées vers l’archive &#x200B;](./assets/order-move-to-archive.png){width="700" zoomable="yes"}

>[!TIP]
>
>Pour spécifier une liste des états de commande pouvant être archivés, voir [Configuration de l’archive de commande](#configure-the-order-archive).

## Affichage d’un ordre archivé

1. Ouvrez la vue d’archivage à l’aide de l’une des méthodes suivantes :

   - Dans la barre de boutons située au-dessus de la grille _[!UICONTROL Orders]_, cliquez sur **[!UICONTROL Go to Archive]**.

   - Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Archive]_>**[!UICONTROL Orders]**.

   >[!NOTE]
   >
   >Comme la page Commandes, le titre de la page des commandes archivées est _[!UICONTROL Orders]_. La seule différence notable est l’option de la barre de boutons sur&#x200B;_[!UICONTROL Return to Orders Management]_. L’URL de la page indique également que vous vous trouvez dans l’archive de commande.

1. Dans la colonne _Action_, cliquez sur **[!UICONTROL View]**.

   ![Afficher une commande archivée](./assets/order-archived-view.png){width="600" zoomable="yes"}

## Restaurer un ordre archivé

>[!NOTE]
>
>Une commande restaurée à partir d’un ordre archivé est de nouveau archivée en fonction du nombre de jours configuré dans le paramètre [!UICONTROL Archive Orders Purchased] (voir [Configuration de l’archive de commande](#configure-the-order-archive)). Le nombre de jours est calculé par rapport à la date [!UICONTROL Updated At] de la commande, qui est modifiée lorsque la commande est déplacée de l’archive.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Dans la barre de boutons, cliquez sur **[!UICONTROL Go to Archive]**.

1. Recherchez l&#39;enregistrement à restaurer et cochez la case pour le sélectionner.

   ![Sélectionner l’ordre à restaurer](./assets/order-archived-select-to-restore.png){width="600" zoomable="yes"}

1. Définissez la valeur de contrôle **[!UICONTROL Actions]** sur `Move to Order Management`.

Recherchez le message indiquant que l’ordre archivé a été supprimé de l’archive.

## Exporter l’ordre archivé

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Dans le menu d’actions, cliquez sur **[!UICONTROL Export]** et sélectionnez le format souhaité.
