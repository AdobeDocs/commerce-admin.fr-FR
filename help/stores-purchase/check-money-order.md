---
title: Vérifications et commandes monétaires
description: Découvrez comment configurer les commandes de paiement et de contrôle en tant que mode de paiement hors ligne sur votre boutique.
exl-id: e004f0c3-f659-4b08-a41a-88bfc05acaab
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Vérifications et commandes monétaires

Adobe Commerce et Magento Open Source vous permettent d’accepter des paiements par chèque ou par mandat. La variable _Vérifier / Commande monétaire_ le mode de paiement est activé par défaut pour votre boutique. Vous ne pouvez accepter des chèques et des mandats émis que par des pays spécifiques, et vous pouvez affiner la configuration avec des limites minimales et maximales du total des commandes.

**_Pour configurer le paiement par chèque ou par mandat :_**

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Payment Methods]**.

1. Sous _[!UICONTROL Other Payment Methods]_, développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Check / Money Order]**.

   ![Vérifier / Commande monétaire](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   Pour une description détaillée de chacun de ces paramètres de configuration, voir [Vérifier / Commande monétaire](../configuration-reference/sales/payment-methods.md#check--money-order) dans le _Guide de référence de configuration_.

   >[!NOTE]
   >
   >Si nécessaire, effacez d’abord la variable **[!UICONTROL Use system value]** pour modifier ces paramètres.

1. Pour accepter le paiement par chèque ou mandat, définissez **[!UICONTROL Enabled]** to `Yes`.

1. Pour **[!UICONTROL Title]**, saisissez un titre qui identifie le mode de paiement de la commande ou de la commande durant le passage en caisse.

1. Si les commandes attendent généralement leur approbation, acceptez la valeur par défaut **[!UICONTROL New Order Status]** as `Pending"` jusqu’à ce qu’elle soit approuvée.

   Si vous préférez, vous pouvez utiliser la variable `Processing` ou `Suspected Fraud` statut des nouvelles commandes avec ce mode de paiement.

1. Définir **[!UICONTROL Payment from Applicable Countries]** à l’une des options suivantes :

   - `All Allowed Countries` - Clients de tous les [pays](../getting-started/store-details.md#country-options) spécifié dans votre configuration de magasin peut utiliser ce mode de paiement.
   - `Specific Countries` - Après avoir choisi cette option, la variable _[!UICONTROL Payment from Specific Countries]_s’affiche. Pour sélectionner plusieurs pays, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

1. Pour **[!UICONTROL Make Check Payable To]**, saisissez le nom de la partie à qui la vérification doit être payée.

1. Pour **[!UICONTROL Send Check To]**, saisissez l’adresse de la rue ou la boîte de bon de commande dans laquelle les vérifications sont envoyées.

1. Définir **[!UICONTROL Minimum Order Total]** et **[!UICONTROL Maximum Order Total]** aux montants de commande requis pour bénéficier de ce mode de paiement.

   >[!NOTE]
   >
   >Une commande est admissible si le total est compris entre, ou correspond exactement, les valeurs totales minimales ou maximales.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre qui détermine la position de cet élément dans la liste des méthodes de paiement affichées lors du passage en caisse.

   Ce nombre est relatif aux autres modes de paiement. (`0` = first, `1` = second, `2` = troisième, etc.)

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.
