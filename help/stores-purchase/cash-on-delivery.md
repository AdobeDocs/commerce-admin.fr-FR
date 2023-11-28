---
title: Encaisse lors de la diffusion (DCO)
description: Découvrez comment configurer l’argent liquide à la livraison en tant que mode de paiement hors ligne dans votre boutique.
exl-id: dcf94734-a66e-4d32-b389-b47c979ceaa9
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Encaisse lors de la diffusion (DCO)

Adobe Commerce et Magento Open Source vous permettent d’accepter _espèces à la diffusion_ (DCO) paiements pour les achats. Vous ne pouvez accepter le paiement de la DCO que de pays spécifiques et vous pouvez affiner la configuration avec des limites totales de commande minimales et maximales.

Le transporteur reçoit le paiement du client au moment de la livraison, qui vous est ensuite transféré. Vous pouvez effectuer un ajustement pour les frais facturés par le service de transport dans vos frais d&#39;expédition et de gestion.

**_Pour configurer l’encaisse sur les paiements de diffusion :_**

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Payment Methods]**.

1. Sous _Autres modes de paiement_, développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Cash On Delivery Payment]** .

   ![Paiement en espèces à la livraison](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png){width="600" zoomable="yes"}

   Pour une description détaillée de chacun de ces paramètres de configuration, voir [Paiement en espèces à la livraison](../configuration-reference/sales/payment-methods.md#cash-on-delivery-payment) dans le _Guide de référence de configuration_.

   >[!NOTE]
   >
   >Si nécessaire, effacez d’abord la variable **[!UICONTROL Use system value]** pour modifier ces paramètres.

1. Pour activer l’encaisse au moment du paiement de la diffusion, définissez **[!UICONTROL Enabled]** to `Yes`.

1. Pour **[!UICONTROL Title]**, saisissez un titre qui identifie le mode de paiement DCO lors du passage en caisse.

1. Définir **[!UICONTROL New Order Status]** to `Pending` jusqu&#39;à ce que la réception du paiement soit confirmée.

   Si vous préférez, vous pouvez utiliser la variable `Processing` ou `Suspected Fraud` statut des nouvelles commandes avec ce mode de paiement.

1. Définir **[!UICONTROL Payment from Applicable Countries]** à l’une des options suivantes :

   - `All Allowed Countries` - Clients de tous les [pays](../getting-started/store-details.md#country-options) spécifié dans votre configuration de magasin peut utiliser ce mode de paiement.
   - `Specific Countries` - Après avoir choisi cette option, la variable _[!UICONTROL Payment from Specific Countries]_s’affiche. Pour sélectionner plusieurs pays, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

1. Saisissez le **[!UICONTROL Instructions]** pour accepter l&#39;envoi d&#39;une commande de la DCO.

1. Définir **[!UICONTROL Minimum Order Total]** et **[!UICONTROL Maximum Order Total]** aux montants de commande qui doivent être admissibles au paiement de la DCO.

   >[!NOTE]
   >
   >Une commande est admissible si le total est compris entre le total de la commande ou correspond au total de la commande minimale ou maximale.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre qui détermine la position de cet élément dans la liste des méthodes de paiement affichées lors du passage en caisse.

   Ce nombre est relatif aux autres modes de paiement. (`0` = first, `1` = second, `2` = troisième, etc.)

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.
