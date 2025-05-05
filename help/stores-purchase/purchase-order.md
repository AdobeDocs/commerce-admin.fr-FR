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

Un _bon de commande_ (bon de commande) permet aux clients commerciaux de payer pour les achats autorisés en référençant le numéro du bon de commande. La commande est autorisée et émise à l’avance par la société qui effectue l’achat. Lors du passage en caisse, le client choisit le bon de commande comme mode de paiement. A réception de votre facture, l&#39;entreprise traite le paiement dans le système de leurs comptes créditeurs et paie l&#39;achat.

Avant d&#39;accepter un paiement par commande, vérifiez toujours la solvabilité du client commercial.

**_Pour configurer le paiement par bon de commande :_**

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Payment Methods]**.

1. Sous _[!UICONTROL Other Payment Methods]_, développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Purchase Order]**.

   ![Bon de commande](../configuration-reference/sales/assets/payment-methods-purchase-order.png){width="600" zoomable="yes"}

   Pour une description détaillée de chacun de ces paramètres de configuration, voir [Bon de commande](../configuration-reference/sales/payment-methods.md#purchase-order) dans le _Guide de référence de configuration_.

   >[!NOTE]
   >
   >Si nécessaire, décochez d’abord la case **[!UICONTROL Use system value]** pour modifier ces paramètres.

1. Pour activer ce mode de paiement, définissez **[!UICONTROL Enabled]** sur `Yes`.

1. Pour **[!UICONTROL Title]**, saisissez un titre qui identifie ce mode de paiement lors du passage en caisse.

1. Définissez **[!UICONTROL New Order Status]** sur `Pending` jusqu’à ce que le paiement soit autorisé.

1. Définissez **[!UICONTROL Payment from Applicable Countries]** sur l’une des options suivantes :

   - `All Allowed Countries` - Les clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiés dans votre configuration de magasin peuvent utiliser ce mode de paiement.
   - `Specific Countries` - Une fois cette option sélectionnée, la liste _[!UICONTROL Payment from Specific Countries]_&#x200B;s’affiche. Pour sélectionner plusieurs pays, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

1. Définissez **[!UICONTROL Minimum Order Total]** et **[!UICONTROL Maximum Order Total]** sur les montants requis pour bénéficier de ce mode de paiement.

   >[!NOTE]
   >
   >Une commande est admissible si le total est compris entre, ou correspond exactement, les valeurs totales minimales ou maximales.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre qui détermine la position de cet élément dans la liste des méthodes de paiement affichées lors du passage en caisse.

   Ce nombre est relatif aux autres modes de paiement. (`0` = premier, `1` = deuxième, `2` = troisième, etc.)

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
