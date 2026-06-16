---
title: Chèques et mandats
description: Découvrez comment configurer les chèques et les mandats comme mode de paiement hors ligne dans votre boutique.
exl-id: e004f0c3-f659-4b08-a41a-88bfc05acaab
feature: Payments
TQID: https://experienceleague.adobe.com/mmlEdLGANV93nvet3YwYoBGZKcft1qYuA6HboQ0Buvw
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 337
ht-degree: 0%

---

# Chèques et mandats

Adobe Commerce et Magento Open Source vous permettent d’accepter des paiements par chèque ou mandat. Le mode de paiement _Chèque / Mandat_ est activé par défaut pour votre boutique. Vous pouvez accepter des chèques et des mandats uniquement de pays spécifiques et vous pouvez affiner la configuration avec des limites de total de commande minimum et maximum.

**_Pour configurer le paiement par chèque ou mandat:_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Payment Methods]**.

1. Sous _[!UICONTROL Other Payment Methods]_, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Check / Money Order]**.

   ![Chèque / Mandat](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   Pour obtenir une description détaillée de chacun de ces paramètres de configuration, consultez [Chèque / Mandat](../configuration-reference/sales/payment-methods.md#check--money-order) dans le _Guide de référence de configuration_.

   >[!NOTE]
   >
   >Si nécessaire, décochez d’abord la case **[!UICONTROL Use system value]** pour modifier ces paramètres.

1. Pour accepter un paiement par chèque ou mandat, **[!UICONTROL Enabled]** sur `Yes`.

1. Par **[!UICONTROL Title]**, saisissez un titre qui identifie le mode de paiement du chèque / du mandat lors du passage en caisse.

1. Si les commandes sont généralement en attente d&#39;approbation, acceptez le **[!UICONTROL New Order Status]** par défaut comme `Pending"` jusqu&#39;à ce qu&#39;il soit approuvé.

   Si vous préférez, vous pouvez utiliser le statut `Processing` ou `Suspected Fraud` pour les nouvelles commandes avec ce mode de paiement.

1. Définissez **[!UICONTROL Payment from Applicable Countries]** sur l’une des options suivantes :

   - `All Allowed Countries` - Les clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiés dans la configuration de votre boutique peuvent utiliser ce mode de paiement.
   - `Specific Countries` - Une fois cette option sélectionnée, la liste des _[!UICONTROL Payment from Specific Countries]_s’affiche. Pour sélectionner plusieurs pays, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et cliquez sur chaque option.

1. Par **[!UICONTROL Make Check Payable To]**, entrez le nom de la partie à qui le chèque doit être payable.

1. Par **[!UICONTROL Send Check To]**, saisissez la rue ou la boîte postale où les chèques sont envoyés.

1. Définissez **[!UICONTROL Minimum Order Total]** et **[!UICONTROL Maximum Order Total]** sur les montants de commande requis pour bénéficier de ce mode de paiement.

   >[!NOTE]
   >
   >Une commande est qualifiée si le total est compris entre les valeurs totales minimales ou maximales ou s’il correspond exactement à ces valeurs.

1. Par **[!UICONTROL Sort Order]**, saisissez un nombre qui détermine la position de cet article dans la liste des modes de paiement affichée lors du passage en caisse.

   Ce nombre est relatif aux autres modes de paiement. (`0` = premier, `1` = deuxième, `2` = troisième, etc.)

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
