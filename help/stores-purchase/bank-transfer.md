---
title: Transferts bancaires
description: Découvrez comment configurer les transferts bancaires en tant que méthode de paiement hors ligne sur votre boutique.
exl-id: 34b2163c-2edd-4741-b002-3d8fb561fc78
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# Transferts bancaires

Adobe Commerce et Magento Open Source vous permettent d’accepter un paiement transféré depuis un compte bancaire client et déposé sur votre compte bancaire marchand.

**_Pour configurer les paiements de transfert bancaire :_**

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Payment Methods]**.

1. Sous _Autres méthodes de paiement_, développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) de **[!UICONTROL Bank Transfer Payment]**.

   ![Paiement de transfert de banque](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Si nécessaire, décochez d’abord la case **[!UICONTROL Use system value]** pour modifier ces paramètres.

1. Pour activer les transferts bancaires, définissez **[!UICONTROL Enabled]** sur `Yes`.

1. Pour **[!UICONTROL Title]**, saisissez un titre qui identifie le mode de paiement de transfert bancaire lors du passage en caisse.

1. Définissez **[!UICONTROL New Order Status]** sur `Pending` jusqu’à ce que le paiement soit autorisé.

1. Définissez **[!UICONTROL Payment from Applicable Countries]** sur l’une des options suivantes :

   - `All Allowed Countries` - Les clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiés dans votre configuration de magasin peuvent utiliser ce mode de paiement.

   - `Specific Countries` - Une fois cette option sélectionnée, la liste _[!UICONTROL Payment from Specific Countries]_s’affiche. Pour sélectionner plusieurs pays, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

1. Saisissez le **[!UICONTROL Instructions]** que vos clients doivent suivre pour configurer un transfert bancaire.

   Selon le pays où se trouve votre banque et les exigences de celle-ci, vous pouvez inclure les informations suivantes :

   - Nom du compte bancaire
   - Numéro de compte bancaire
   - Code de routage bancaire
   - Nom de la banque
   - Adresse bancaire

1. Définissez **[!UICONTROL Minimum Order Total]** et **[!UICONTROL Maximum Order Total]** sur les montants requis pour pouvoir utiliser ce mode de paiement.

   >[!NOTE]
   >
   >Une commande est admissible si le total est compris entre, ou correspond exactement, les valeurs totales minimales ou maximales.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre qui détermine la position de cet élément dans la liste des méthodes de paiement affichées lors du passage en caisse.

   Ce nombre est relatif aux autres modes de paiement. (`0` = premier, `1` = deuxième, `2` = troisième, etc.)

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
