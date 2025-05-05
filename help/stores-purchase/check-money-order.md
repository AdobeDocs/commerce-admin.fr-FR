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

Adobe Commerce et Magento Open Source vous permettent d’accepter des paiements par chèque ou par mandat. Le mode de paiement _Check / Money Order_ est activé par défaut pour votre boutique. Vous ne pouvez accepter des chèques et des mandats émis que par des pays spécifiques, et vous pouvez affiner la configuration avec des limites minimales et maximales du total des commandes.

**_Pour configurer le paiement par chèque ou mandat :_**

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Payment Methods]**.

1. Sous _[!UICONTROL Other Payment Methods]_, développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Check / Money Order]**.

   ![Vérifier / Commande d’argent](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   Pour une description détaillée de chacun de ces paramètres de configuration, voir [Contrôle / Commande d’argent](../configuration-reference/sales/payment-methods.md#check--money-order) dans le _Guide de référence de configuration_.

   >[!NOTE]
   >
   >Si nécessaire, décochez d’abord la case **[!UICONTROL Use system value]** pour modifier ces paramètres.

1. Pour accepter le paiement par chèque ou mandat, définissez **[!UICONTROL Enabled]** sur `Yes`.

1. Pour **[!UICONTROL Title]**, saisissez un titre qui identifie le mode de paiement de chèque/mandat lors du passage en caisse.

1. Si les commandes attendent généralement l’approbation, acceptez le **[!UICONTROL New Order Status]** par défaut comme `Pending"` jusqu’à ce qu’il soit approuvé.

   Si vous préférez, vous pouvez utiliser l’état `Processing` ou `Suspected Fraud` pour les nouvelles commandes avec ce mode de paiement.

1. Définissez **[!UICONTROL Payment from Applicable Countries]** sur l’une des options suivantes :

   - `All Allowed Countries` - Les clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiés dans votre configuration de magasin peuvent utiliser ce mode de paiement.
   - `Specific Countries` - Une fois cette option sélectionnée, la liste _[!UICONTROL Payment from Specific Countries]_&#x200B;s’affiche. Pour sélectionner plusieurs pays, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

1. Pour **[!UICONTROL Make Check Payable To]**, saisissez le nom de la partie à qui la vérification doit être due.

1. Pour **[!UICONTROL Send Check To]**, saisissez l’adresse de la rue ou la boîte de bon de commande dans laquelle les vérifications sont envoyées.

1. Définissez **[!UICONTROL Minimum Order Total]** et **[!UICONTROL Maximum Order Total]** sur les montants de commande requis pour être admissible pour ce mode de paiement.

   >[!NOTE]
   >
   >Une commande est admissible si le total est compris entre, ou correspond exactement, les valeurs totales minimales ou maximales.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre qui détermine la position de cet élément dans la liste des méthodes de paiement affichées lors du passage en caisse.

   Ce nombre est relatif aux autres modes de paiement. (`0` = premier, `1` = deuxième, `2` = troisième, etc.)

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
