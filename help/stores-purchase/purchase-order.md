---
title: Commandes
description: Découvrez comment configurer les commandes d’achat en tant que méthode de paiement hors ligne sur votre boutique.
exl-id: 493c1b59-2155-449f-a08a-eb1aa2af9b3e
feature: Purchase Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Commandes

A _commande_ (PO) permet aux clients commerciaux de payer pour les achats autorisés en référençant le numéro du bon de commande. La commande est autorisée et émise à l’avance par la société qui effectue l’achat. Lors du passage en caisse, le client choisit le bon de commande comme mode de paiement. A réception de votre facture, l&#39;entreprise traite le paiement dans le système de leurs comptes créditeurs et paie l&#39;achat.

Avant d&#39;accepter un paiement par commande, vérifiez toujours la solvabilité du client commercial.

**_Pour configurer le paiement par bon de commande :_**

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Payment Methods]**.

1. Sous _[!UICONTROL Other Payment Methods]_, développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Purchase Order]**.

   ![Bon de commande](../configuration-reference/sales/assets/payment-methods-purchase-order.png){width="600" zoomable="yes"}

   Pour une description détaillée de chacun de ces paramètres de configuration, voir [Bon de commande](../configuration-reference/sales/payment-methods.md#purchase-order) dans le _Guide de référence de configuration_.

   >[!NOTE]
   >
   >Si nécessaire, effacez d’abord la variable **[!UICONTROL Use system value]** pour modifier ces paramètres.

1. Pour activer ce mode de paiement, définissez **[!UICONTROL Enabled]** to `Yes`.

1. Pour **[!UICONTROL Title]**, saisissez un titre qui identifie ce mode de paiement lors du passage en caisse.

1. Définir **[!UICONTROL New Order Status]** to `Pending` jusqu’à ce que le paiement soit autorisé.

1. Définir **[!UICONTROL Payment from Applicable Countries]** à l’une des options suivantes :

   - `All Allowed Countries` - Clients de tous les [pays](../getting-started/store-details.md#country-options) spécifié dans votre configuration de magasin peut utiliser ce mode de paiement.
   - `Specific Countries` - Après avoir choisi cette option, la variable _[!UICONTROL Payment from Specific Countries]_s’affiche. Pour sélectionner plusieurs pays, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

1. Définir **[!UICONTROL Minimum Order Total]** et **[!UICONTROL Maximum Order Total]** aux montants requis pour bénéficier de ce mode de paiement.

   >[!NOTE]
   >
   >Une commande est admissible si le total est compris entre, ou correspond exactement, les valeurs totales minimales ou maximales.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre qui détermine la position de cet élément dans la liste des méthodes de paiement affichées lors du passage en caisse.

   Ce nombre est relatif aux autres modes de paiement. (`0` = first, `1` = second, `2` = troisième, etc.)

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.
