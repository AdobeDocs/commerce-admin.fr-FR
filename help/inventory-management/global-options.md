---
title: "Configurer [!DNL Inventory Management] les options globales"
description: Découvrez comment configurer les options de configuration par défaut  [!DNL Inventory Management] pour le produit et le stock de vos sites web.
exl-id: 1a8c9605-ae61-4d45-b549-64911b329203
feature: Inventory, Configuration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 0%

---

# Configuration des options globales [!DNL Inventory Management]

Configurez les options de configuration par défaut pour le produit et le stock de vos sites web. Certains de ces paramètres peuvent être remplacés par produit par [Configuration des options de produit](product-options.md). Pour configurer les paramètres de priorité des distances, voir [Configuration de l’algorithme de priorité des distances](distance-priority-algorithm.md).

## Configuration globale des options de produit et de stock

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Inventory]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) et définissez les options suivantes :**[!UICONTROL Stock Options]**

   ![Options Stock](assets/config-catalog-inventory-stock-options.png){width="600" zoomable="yes"}

   - Pour ajuster la quantité disponible lors du passage d’une commande, définissez **[!UICONTROL Decrease Stock When Order is Placed]** sur `Yes`.

   - Pour renvoyer des éléments en stock si une commande est annulée, **[!UICONTROL Set Items' Status to be in Stock When Order in Cancelled]** sur `Yes`.

   - Pour continuer à afficher dans le catalogue les produits qui ne sont plus en stock, définissez **[!UICONTROL Display Out of Stock Products]** sur `Yes`.

   - Si les [alertes de prix](alert-setup.md) sont activées, les clients peuvent s’inscrire pour être avertis lorsque le produit est de nouveau en stock.

   - Pour définir le début de l’affichage du dernier montant de stock restant sur la page de produit, saisissez un montant pour **[!UICONTROL Only X left Threshold]**.

     Le message commence à s’afficher lorsque la quantité en stock atteint le seuil. Par exemple, si la valeur est `3`, le message `Only 3 left` s’affiche lorsque la quantité en stock atteint trois. Le message s’ajuste pour refléter la quantité en stock, jusqu’à ce que la quantité atteigne zéro.

   - Pour afficher un message &quot;En stock&quot; ou &quot;En rupture de stock&quot; sur la page du produit, définissez **[!UICONTROL Display Products Availability In Stock on Storefront]** sur `Yes`.

   - Pour vérifier l’inventaire lors du chargement d’un produit dans le panier, définissez **[!UICONTROL Enable Inventory Check On Cart Load]** sur `Yes`. Lorsque cette option est désactivée, la vérification de stock est ignorée. La désactivation de cette option accélère le passage en caisse, en particulier si le panier contient de nombreux articles. Cependant, si vous ignorez la prévalidation, les clients peuvent voir des erreurs &quot;en rupture de stock&quot; plus tard dans le processus de passage en caisse.

   - Pour maintenir la cohérence entre l’inventaire et le catalogue, définissez **[!UICONTROL Synchronize with Catalog]** sur `Yes`. Lorsque cette option est activée, les données d’inventaire sont ajustées en fonction des modifications du catalogue (telles que la suppression d’un produit, la modification du SKU du produit et la modification du type de produit).

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) et définissez les options suivantes :**[!UICONTROL Product Stock Options]**

   - Pour activer la [gestion de stock](enable.md) pour votre catalogue, définissez **[!UICONTROL Manage Stock]** sur `Yes`.

     ![Options Stock de produits](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - Définissez **[!UICONTROL Backorders]** sur l’une des options suivantes :

     | Option | Description |
     | ----- | ----- |
     | `No Backorders` | [Les commandes en arrière-plan](backorders.md) ne sont pas acceptées lorsque le produit est en rupture de stock. |
     | `Allow Qty Below 0` | Les commandes en arrière-plan sont acceptées lorsque la quantité est inférieure à zéro. |
     | `Allow Qty Below 0 and Notify Customer` | Les commandes en arrière-plan sont acceptées lorsque la quantité est inférieure à zéro et que le système avertit le client que la commande peut toujours être passée. |

   - Saisissez le **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

   - Saisissez un montant pour le **[!UICONTROL Out-of-Stock Threshold]** :

     | Valeur | Description |
     | ----- |-----|
     | Montant positif | Si l’option Commandes d’arrière-plan est désactivée, saisissez un montant positif. |
     | Zéro | Lorsque les commandes d’arrière-plan sont activées, la saisie de `0` permet des commandes d’arrière-plan infinies. |
     | Montant négatif | Lorsque les commandes d’arrière-plan sont activées, il est recommandé de saisir un montant négatif. Le montant est ajouté à la quantité vendable. Par exemple, saisissez `-50` pour autoriser les commandes jusqu’à ce montant. |

   - Saisissez le **[!UICONTROL Minimum Qty Allowed in Shopping Cart]** pour le groupe et les montants sélectionnés.

   - Pour **[!UICONTROL Notify for Quantity Below]**, saisissez le niveau de stock qui déclenche la notification indiquant que l&#39;article est en rupture de stock.

   - Pour activer les incréments de quantité pour le produit, définissez **[!UICONTROL Enable Qty Increments]** sur `Yes`. Ensuite, pour **[!UICONTROL Qty Increments]**, saisissez le nombre d’articles à acheter pour répondre à la demande.

     Par exemple, un article vendu par incréments de six peut être acheté en quantités de `6`, `12`, `18`, etc.

   - Pour [!DNL Inventory Management], **[!UICONTROL Automatically Return Credit Memo Item to Stock]** est défini sur `No`. Lors de l’envoi d’une note de crédit, vous saisissez et choisissez de renvoyer le stock à des sources.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) et définissez les options suivantes :**[!UICONTROL Admin bulk operations]**

   ![Opérations d’administration en bloc](assets/config-catalog-inventory-admin-bulk-operations.png){width="600" zoomable="yes"}

   - Définissez **[!UICONTROL Run asynchronously]** pour exécuter des opérations en bloc de manière asynchrone pour des actions de produits de masse.

     Ces opérations comprennent l&#39;affectation et l&#39;annulation de l&#39;attribution des sources [&#128279;](bulk-assignment.md) en masse et le [ transfert de l&#39;inventaire vers la source](inventory-transfer.md).  Il collecte les actions en bloc jusqu’à la taille de lot asynchrone, puis exécute ces actions. Cette option est désactivée par défaut. Il est recommandé de consulter vos performances avec des actions en bloc avant d’activer .

     >[!NOTE]
     >
     >Pour configurer et prendre en charge les _gestionnaires de file d’attente asynchrones_, vous devez émettre une commande à l’aide de la ligne de commande. Cette étape peut nécessiter l’aide des développeurs. Voir [Démarrage des consommateurs de la file d’attente de messages](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) dans le _Guide de configuration_.

   - S’il est activé, définissez le **[!UICONTROL Asynchronous batch size]**. La taille de lot par défaut est 100. Lorsque les processus en masse atteignent cette valeur, le système les déclenche.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
