---
title: Contre remboursement (COD)
description: Découvrez comment configurer l’option Contre remboursement comme mode de paiement hors ligne dans votre boutique.
exl-id: dcf94734-a66e-4d32-b389-b47c979ceaa9
feature: Payments
TQID: https://experienceleague.adobe.com/xKFjuGpjrF-XfVnNqWR2St8v3D4Lnr74WozkrynBbdo
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 336
ht-degree: 0%

---

# Contre remboursement (COD)

Adobe Commerce et Magento Open Source vous permettent d’accepter des paiements _contre remboursement_ (COD) pour les achats. Vous pouvez accepter le paiement contre remboursement uniquement de pays spécifiques et vous pouvez affiner la configuration avec des limites de total de commande minimum et maximum.

Le transporteur reçoit le paiement du client au moment de la livraison, qui vous est ensuite transféré. Vous pouvez effectuer un ajustement pour tous les frais facturés par le service de transporteur dans vos frais d&#39;expédition et de manutention.

**_Pour configurer les paiements contre remboursement:_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Payment Methods]**.

1. Sous _Autres modes de paiement_, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Cash On Delivery Payment]** .

   ![Paiement à la livraison](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png){width="600" zoomable="yes"}

   Pour obtenir une description détaillée de chacun de ces paramètres de configuration, consultez [Paiement à la livraison](../configuration-reference/sales/payment-methods.md#cash-on-delivery-payment) dans le _Guide de référence de configuration_.

   >[!NOTE]
   >
   >Si nécessaire, décochez d’abord la case **[!UICONTROL Use system value]** pour modifier ces paramètres.

1. Pour activer le paiement en espèces à la livraison, **[!UICONTROL Enabled]** sur `Yes`.

1. Par **[!UICONTROL Title]**, saisissez un titre qui identifie le mode de paiement du contre remboursement lors du passage en caisse.

1. Définissez **[!UICONTROL New Order Status]** sur `Pending` jusqu&#39;à ce que la réception du paiement soit confirmée.

   Si vous préférez, vous pouvez utiliser le statut `Processing` ou `Suspected Fraud` pour les nouvelles commandes avec ce mode de paiement.

1. Définissez **[!UICONTROL Payment from Applicable Countries]** sur l’une des options suivantes :

   - `All Allowed Countries` - Les clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiés dans la configuration de votre boutique peuvent utiliser ce mode de paiement.
   - `Specific Countries` - Une fois cette option sélectionnée, la liste des _[!UICONTROL Payment from Specific Countries]_s’affiche. Pour sélectionner plusieurs pays, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et cliquez sur chaque option.

1. Saisissez le **[!UICONTROL Instructions]** d&#39;acceptation de la livraison d&#39;une commande contre remboursement.

1. Définissez **[!UICONTROL Minimum Order Total]** et **[!UICONTROL Maximum Order Total]** sur les montants de commande requis pour bénéficier du paiement contre remboursement.

   >[!NOTE]
   >
   >Une commande est qualifiée si le total est compris entre le total de commande minimum ou maximum ou correspond à ce total.

1. Par **[!UICONTROL Sort Order]**, saisissez un nombre qui détermine la position de cet article dans la liste des modes de paiement affichée lors du passage en caisse.

   Ce nombre est relatif aux autres modes de paiement. (`0` = premier, `1` = deuxième, `2` = troisième, etc.)

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
