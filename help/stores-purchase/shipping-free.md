---
title: Livraison gratuite
description: Découvrez comment configurer une option de livraison gratuite pour votre boutique.
exl-id: 3ce69583-0f7f-4c23-b3e3-7d2502bc1bca
feature: Shipping/Delivery
TQID: https://experienceleague.adobe.com/bLvgCzOtiYjpSdTm7f0Te5fjWbiaL3mfC4DN8ONbOLs
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 395
ht-degree: 0%

---

# Livraison gratuite

_Livraison gratuite_ est l&#39;une des promotions les plus efficaces que vous pouvez offrir. Il peut être basé sur un achat minimum ou configuré comme une [règle de prix de panier](../merchandising-promotions/price-rules-cart.md) qui est appliquée lorsqu’un ensemble de conditions est rempli. Si les deux s’appliquent au même ordre, le paramètre de configuration est prioritaire sur la règle de panier.

>[!NOTE]
>
>Vérifiez la configuration de votre transporteur pour connaître les paramètres supplémentaires qui peuvent être requis pour la livraison gratuite.

## Étape 1 : Configurer la livraison gratuite

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Delivery Methods]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Free Shipping]** .

   >[!NOTE]
   >
   >Si nécessaire, décochez d’abord la case **[!UICONTROL Use system value]** pour modifier les paramètres suivants comme décrit.

1. Définissez **[!UICONTROL Enabled]** sur `Yes`.

1. Par **[!UICONTROL Title]**, saisissez un titre qui identifie la méthode d&#39;expédition gratuite lors du passage en caisse et une **[!UICONTROL Method Name]** pour la décrire.

1. Par **[!UICONTROL Minimum Order Amount]**, saisissez la valeur totale minimale éligible pour une livraison gratuite.

   >[!TIP]
   >
   >Pour utiliser la livraison gratuite avec les [tarifs du tableau](shipping-table-rate.md), faites en sorte que le _[!UICONTROL Minimum Order Amount]_soit si élevé qu&#39;il ne soit jamais atteint. L&#39;utilisation de cette valeur élevée empêche l&#39;entrée en vigueur de la livraison gratuite, sauf si elle est déclenchée par une règle de prix.

1. Définir **[!UICONTROL Include Tax to Amount]** :

   - `Yes` - Taxe incluse dans le calcul du montant minimum de la commande (Sous-total + Taxe - Remise).
   - `No` - Taxe non incluse lors du calcul du montant minimum de la commande (Sous-total - Remise).

   ![Livraison gratuite](../configuration-reference/sales/assets/delivery-methods-free-shipping.png){width="600" zoomable="yes"}

1. Par **[!UICONTROL Displayed Error Message]**, saisissez le message à afficher si la livraison gratuite n’est plus disponible.

1. Définir **[!UICONTROL Ship to Applicable Countries]** :

   - `All Allowed Countries` - Les clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiés dans la configuration de votre boutique peuvent utiliser la livraison gratuite.

   - `Specific Countries` - Après avoir choisi cette valeur, la liste des _[!UICONTROL Ship to Specific Countries]_s’affiche. Dans la liste, sélectionnez chaque pays où la livraison gratuite peut être utilisée.

1. Définir **[!UICONTROL Show Method if Not Applicable]** :

   - `Yes` - Affiche toujours la méthode d&#39;expédition gratuite, même lorsqu&#39;elle n&#39;est pas applicable.
   - `No` : affiche la méthode d’expédition gratuite uniquement lorsqu’elle est applicable.

1. Par **[!UICONTROL Sort Order]**, saisissez le numéro qui détermine la position de la livraison gratuite dans la liste des méthodes de livraison lors du passage en caisse.

   `0` = premier, `1` = deuxième, `2` = troisième, etc.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Étape 2 : activer la livraison gratuite dans la configuration du transporteur

Veillez à effectuer toute configuration requise pour chaque transporteur que vous prévoyez d&#39;utiliser pour la livraison gratuite. Par exemple, si votre [configuration de l&#39;onduleur](ups.md) est terminée, mettez à jour les paramètres suivants pour activer et configurer la livraison gratuite.

1. Dans la configuration _[!UICONTROL Delivery Methods]_, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL UPS]**.

1. Définissez **[!UICONTROL Free Method]** sur `UPS Ground` ou un autre type que vous souhaitez désigner pour une livraison gratuite.

1. Pour exiger une commande minimale pour une livraison gratuite, définissez **[!UICONTROL Enable Free Shipping Threshold]** sur `Enable`.

   Si vous choisissez d&#39;utiliser une commande minimum, saisissez le montant requis pour **[!UICONTROL Free Shipping Amount Threshold]**.

1. Cliquez sur **[!UICONTROL Save Config]**.
