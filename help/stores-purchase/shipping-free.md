---
title: Envoi gratuit
description: Découvrez comment configurer une option de livraison gratuite pour votre boutique.
exl-id: 3ce69583-0f7f-4c23-b3e3-7d2502bc1bca
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Envoi gratuit

_La livraison gratuite_ est l’une des promotions les plus efficaces que vous pouvez proposer. Elle peut être basée sur un achat minimal ou configurée en tant que [règle de prix de panier](../merchandising-promotions/price-rules-cart.md) appliquée lorsqu’un ensemble de conditions est satisfait. Si les deux s’appliquent au même ordre, le paramètre de configuration prévaut sur la règle du panier.

>[!NOTE]
>
>Vérifiez la configuration de votre fournisseur d’expédition pour connaître les paramètres supplémentaires qui peuvent être requis pour la livraison gratuite.

## Étape 1 : Configuration de la livraison gratuite

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Delivery Methods]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Free Shipping]** .

   >[!NOTE]
   >
   >Si nécessaire, désélectionnez tout d’abord la case à cocher **[!UICONTROL Use system value]** pour modifier les paramètres suivants, comme décrit.

1. Définissez **[!UICONTROL Enabled]** sur `Yes`.

1. Pour **[!UICONTROL Title]**, saisissez un titre qui identifie la méthode d’expédition gratuite lors du passage en caisse et un **[!UICONTROL Method Name]** pour la décrire.

1. Pour **[!UICONTROL Minimum Order Amount]**, saisissez la valeur totale minimale admissible pour la livraison gratuite.

   >[!TIP]
   >
   >Pour utiliser la livraison gratuite avec des [tarifs de table](shipping-table-rate.md), rendez le _[!UICONTROL Minimum Order Amount]_si élevé qu&#39;il n&#39;est jamais rempli. L’utilisation de cette valeur élevée empêche la livraison gratuite de prendre effet, sauf si elle est déclenchée par une règle de prix.

1. Définissez **[!UICONTROL Include Tax to Amount]** :

   - `Yes` - Inclut la taxe lors du calcul du montant minimum de la commande (Subtotal + Taxe - Remise).
   - `No` - N’inclut pas la taxe lors du calcul du montant de la commande minimum (sous-total - remise).

   ![Livraison gratuite](../configuration-reference/sales/assets/delivery-methods-free-shipping.png){width="600" zoomable="yes"}

1. Pour **[!UICONTROL Displayed Error Message]**, saisissez le message à afficher si la livraison gratuite devient indisponible.

1. Définissez **[!UICONTROL Ship to Applicable Countries]** :

   - `All Allowed Countries` - Les clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiés dans votre configuration de magasin peuvent utiliser la livraison gratuite.

   - `Specific Countries` - Après avoir choisi cette valeur, la liste _[!UICONTROL Ship to Specific Countries]_s’affiche. Sélectionnez chaque pays de la liste où la livraison gratuite peut être utilisée.

1. Définissez **[!UICONTROL Show Method if Not Applicable]** :

   - `Yes` - Affiche toujours la méthode d’expédition gratuite, même lorsqu’elle n’est pas applicable.
   - `No` - Affiche la méthode d’expédition gratuite uniquement le cas échéant.

1. Pour **[!UICONTROL Sort Order]**, saisissez le nombre qui détermine la position de la livraison gratuite dans la liste des méthodes de livraison lors du passage en caisse.

   `0` = premier, `1` = second, `2` = troisième, etc.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Étape 2 : activation de la livraison gratuite dans la configuration de l’opérateur

Veillez à effectuer toute configuration requise pour chaque opérateur que vous prévoyez d’utiliser pour la livraison gratuite. Par exemple, si votre [configuration UPS](ups.md) est terminée, mettez à jour les paramètres suivants pour activer et configurer la livraison gratuite.

1. Dans la configuration _[!UICONTROL Delivery Methods]_, développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL UPS]**.

1. Définissez **[!UICONTROL Free Method]** sur `UPS Ground` ou un autre type que vous souhaitez désigner pour la livraison gratuite.

1. Pour exiger une commande minimale pour la livraison gratuite, définissez **[!UICONTROL Enable Free Shipping Threshold]** sur `Enable`.

   Si vous choisissez d’utiliser une commande minimale, saisissez le montant requis pour **[!UICONTROL Free Shipping Amount Threshold]**.

1. Cliquez sur **[!UICONTROL Save Config]**.
