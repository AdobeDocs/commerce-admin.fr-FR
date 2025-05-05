---
title: Créer des envois multi-sources
description: Découvrez comment les marchands multi-sources peuvent créer et envoyer des envois.
exl-id: d2995139-0fc3-4379-a4ec-b0d38ed566bb
feature: Inventory, Shipping/Delivery
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Créer des envois multi-sources

Avec [!DNL Inventory Management], envoyez un ou plusieurs envois tels que vous en disposez. Pour générer d’autres envois, répétez ces instructions à l’aide des quantités et sources recommandées ou saisies manuellement. Ces instructions expliquent comment les marchands multi-sources envoient des envois. Les marchands à source unique envoient des envois sans ces étapes supplémentaires (voir [Créer une expédition](../stores-purchase/shipments.md#create-a-shipment){target="_blank"} dans le guide d’utilisation principal).

Lors de la création d’envois, utilisez l’algorithme de sélection Source pour les recommandations calculées. Suivez et utilisez ces recommandations ou définissez les montants par source, en générant des envois personnalisés. Vous contrôlez votre inventaire sortant pour chaque commande, définissez les montants à déduire, envoyez une ou plusieurs cargaisons et effectuez un envoi en stock et en amont lorsque le stock est disponible. Pour chaque élément de ligne de la commande, saisissez un montant à déduire de la quantité source.

Vous pouvez envoyer des envois partiels vers :

- Exécuter les commandes en amont à mesure que le stock arrive

- Équilibrage des déductions de stock entre les sources

Lorsque vous saisissez des envois, les quantités de stock en main sont déduites des montants saisis. En fait, les réservations sont converties en déductions réelles sur la quantité.

## Créer une expédition

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Recherchez l’ordre et ouvrez-le en mode d’affichage.

1. Si la commande est payée et facturée et prête à être expédiée, cliquez sur **[!UICONTROL Ship]**.

1. Effectuez la sélection Source pour envoyer les produits par source :

   - Pour afficher les recommandations d’expédition, cliquez sur **[!UICONTROL Source Selection Algorithm]** et sélectionnez un algorithme.

     | Algorithme | Description |
     |--|--|
     | [Priorité Source](source-priority-algorithm.md) | Recommande les envois à partir de sources en fonction des ordres de sources attribués au stock. |
     | [Priorité de distance](distance-priority-algorithm.md) | Recommande les envois provenant de sources proches de l’adresse de livraison en fonction de la distance physique ou du délai de livraison le plus court. |

     >[!IMPORTANT]
     >
     >Lors de l’utilisation de l’algorithme Distance Priority pour l’expédition et les itinéraires et que les données ne sont pas renvoyées pour le [mode de calcul](distance-priority-algorithm.md) sélectionné (conduite, vélo ou marche) pour une expédition, l’ASS définit par défaut sur Source Priority. Il est recommandé de définir également la priorité [pour les sources par stock](stocks-prioritize-sources.md).


   - Pour **[!UICONTROL Select a Source to Ship from]**, sélectionnez une source pour envoyer une expédition.

   - Pour chaque élément de ligne, conservez le montant recommandé ou entrez un montant spécifique dans le **[!UICONTROL Qty to Deduct]**. Cette valeur indique le montant qui est déduit de l’inventaire de la source sélectionnée.

   - Cliquez sur **[!UICONTROL Proceed to Shipment]**.

     ![Sélectionnez un Source et saisissez une Quantité](assets/shipment-adobe-shipping-sources.png){width="350" zoomable="yes"}

1. Passez en revue la page _[!UICONTROL New Shipment]_&#x200B;et saisissez d’autres modifications si nécessaire.

   La section _[!UICONTROL Inventory]_&#x200B;affiche la source, l’expédition des produits, la quantité totale commandée et la quantité à envoyer.

   ![Détails du stock pour l’expédition, exemple une expédition partielle](assets/inventory-shipment-details.png){width="350" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Submit Shipment]** pour terminer.
