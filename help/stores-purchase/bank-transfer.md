---
title: Virements bancaires
description: Découvrez comment configurer des virements bancaires en tant que méthode de paiement hors ligne sur votre boutique.
exl-id: 34b2163c-2edd-4741-b002-3d8fb561fc78
feature: Payments
TQID: https://experienceleague.adobe.com/uIYk-S9M8nsKxo3O71N1z25Y-K5WaYOOAM26k9HLVoQ
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 0%

---

# Virements bancaires

Adobe Commerce et Magento Open Source vous permettent d’accepter des paiements transférés depuis un compte bancaire client et déposés sur votre compte bancaire commercial.

**_Pour configurer des paiements par virement bancaire:_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Payment Methods]**.

1. Sous _Autres modes de paiement_, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Bank Transfer Payment]** .

   ![Paiement par virement bancaire](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Si nécessaire, décochez d’abord la case **[!UICONTROL Use system value]** pour modifier ces paramètres.

1. Pour activer les transferts bancaires, définissez **[!UICONTROL Enabled]** sur `Yes`.

1. Par **[!UICONTROL Title]**, saisissez un titre qui identifie le mode de paiement par virement bancaire lors du passage en caisse.

1. Définissez **[!UICONTROL New Order Status]** sur `Pending` jusqu&#39;à ce que le paiement soit autorisé.

1. Définissez **[!UICONTROL Payment from Applicable Countries]** sur l’une des options suivantes :

   - `All Allowed Countries` - Les clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiés dans la configuration de votre boutique peuvent utiliser ce mode de paiement.

   - `Specific Countries` - Une fois cette option sélectionnée, la liste des _[!UICONTROL Payment from Specific Countries]_s’affiche. Pour sélectionner plusieurs pays, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et cliquez sur chaque option.

1. Saisissez les **[!UICONTROL Instructions]** que vos clients doivent suivre pour configurer un virement bancaire.

   Selon le pays où se trouve votre banque et les exigences de celle-ci, vous pouvez inclure les informations suivantes :

   - Nom du compte bancaire
   - Numéro de compte bancaire
   - Code d&#39;acheminement bancaire
   - Nom de la banque
   - Adresse de la banque

1. Définissez **[!UICONTROL Minimum Order Total]** et **[!UICONTROL Maximum Order Total]** sur les montants requis pour pouvoir utiliser ce mode de paiement.

   >[!NOTE]
   >
   >Une commande est qualifiée si le total est compris entre les valeurs totales minimales ou maximales ou s’il correspond exactement à ces valeurs.

1. Par **[!UICONTROL Sort Order]**, saisissez un nombre qui détermine la position de cet article dans la liste des modes de paiement affichée lors du passage en caisse.

   Ce nombre est relatif aux autres modes de paiement. (`0` = premier, `1` = deuxième, `2` = troisième, etc.)

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
