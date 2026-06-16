---
title: Commandes fournisseur
description: Découvrez comment configurer des commandes fournisseur en tant que mode de paiement hors ligne sur votre boutique.
exl-id: 493c1b59-2155-449f-a08a-eb1aa2af9b3e
feature: Purchase Orders
TQID: https://experienceleague.adobe.com/Oc2vdP-OTXwo-6cjKWFj5zPf-QJVvU8aK6OUMPko4eY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 0%

---

# Commandes fournisseur

Une _bon de commande_ (PO) permet aux clients commerciaux de payer les achats autorisés en référençant le numéro de la PO. Le bon de commande est autorisé et émis à l’avance par la société qui effectue l’achat. Lors du passage en caisse, le client choisit le bon de commande comme mode de paiement. À la réception de votre facture, la société traite le paiement dans son système de comptabilité fournisseur et paie l&#39;achat.

Avant d&#39;accepter un paiement par bon de commande, vérifiez toujours la solvabilité du client commercial.

**_Pour configurer le paiement par commande fournisseur:_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Payment Methods]**.

1. Sous _[!UICONTROL Other Payment Methods]_, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Purchase Order]**.

   ![Bon de commande](../configuration-reference/sales/assets/payment-methods-purchase-order.png){width="600" zoomable="yes"}

   Pour obtenir une description détaillée de chacun de ces paramètres de configuration, voir [Bon de commande](../configuration-reference/sales/payment-methods.md#purchase-order) dans le _Guide de référence de configuration_.

   >[!NOTE]
   >
   >Si nécessaire, décochez d’abord la case **[!UICONTROL Use system value]** pour modifier ces paramètres.

1. Pour activer ce mode de paiement, définissez **[!UICONTROL Enabled]** sur `Yes`.

1. Par **[!UICONTROL Title]**, saisissez un titre qui identifie ce mode de paiement lors du passage en caisse.

1. Définissez **[!UICONTROL New Order Status]** sur `Pending` jusqu&#39;à ce que le paiement soit autorisé.

1. Définissez **[!UICONTROL Payment from Applicable Countries]** sur l’une des options suivantes :

   - `All Allowed Countries` - Les clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiés dans la configuration de votre boutique peuvent utiliser ce mode de paiement.
   - `Specific Countries` - Une fois cette option sélectionnée, la liste des _[!UICONTROL Payment from Specific Countries]_&#x200B;s’affiche. Pour sélectionner plusieurs pays, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et cliquez sur chaque option.

1. Définissez **[!UICONTROL Minimum Order Total]** et **[!UICONTROL Maximum Order Total]** sur les montants requis pour être admissible pour ce mode de paiement.

   >[!NOTE]
   >
   >Une commande est qualifiée si le total est compris entre les valeurs totales minimales ou maximales ou s’il correspond exactement à ces valeurs.

1. Par **[!UICONTROL Sort Order]**, saisissez un nombre qui détermine la position de cet article dans la liste des modes de paiement affichée lors du passage en caisse.

   Ce nombre est relatif aux autres modes de paiement. (`0` = premier, `1` = deuxième, `2` = troisième, etc.)

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
