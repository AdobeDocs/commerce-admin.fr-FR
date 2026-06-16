---
title: Passage en caisse du sous-total zéro
description: Découvrez comment configurer un sous-total nul en tant que méthode de paiement hors ligne sur votre boutique.
exl-id: c14ce289-8292-41d9-a448-f493c784f35c
feature: Checkout, Configuration
TQID: https://experienceleague.adobe.com/WCWo0jvFkqHnwLX7QnAcJ1vDs66sdrtpba5hoxd-JKc
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 347
ht-degree: 0%

---

# Passage en caisse du sous-total zéro

_Passage en caisse du sous-total zéro_ peut être utilisé pour les commandes dont le sous-total est égal à zéro et qui sont taxées après application d’une remise. Par exemple, un passage en caisse avec un sous-total nul peut être utilisé dans les situations suivantes :

- Une réduction couvre le prix total de l&#39;achat, sans frais supplémentaires pour l&#39;expédition.

- Le client ajoute un produit [téléchargeable](../catalog/product-create-downloadable.md) ou [virtuel](../catalog/product-create-virtual.md) au panier et le prix est égal à zéro.

- Le prix d&#39;un produit [simple](../catalog/product-create-simple.md) est nul, et la méthode [livraison gratuite](shipping-free.md) est disponible.

- Un [code de coupon](../merchandising-promotions/price-rules-cart-coupon.md) couvre le prix complet des produits et de l&#39;expédition.

Pour gagner du temps, aucun sous-total des commandes peut être défini pour la facturation automatique.

**_Pour configurer l’extraction de zéro sous-total:_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Payment Methods]**.

1. Sous _[!UICONTROL Other Payment Methods]_, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Zero Subtotal Checkout]**.

   ![Passage En Caisse Du Sous-Total Zéro](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Si nécessaire, décochez d’abord la case **[!UICONTROL Use system value]** pour modifier ces paramètres.

1. Pour activer le passage en caisse du sous-total zéro, définissez **[!UICONTROL Enabled]** sur `Yes`.

1. Par **[!UICONTROL Title]**, saisissez un titre qui identifie la méthode du sous-total nul lors du passage en caisse.

1. Si les commandes attendent généralement leur approbation, acceptez le **[!UICONTROL New Order Status]** par défaut comme `Pending"` jusqu’à ce que la commande soit approuvée.

   Si vous préférez, vous pouvez utiliser le statut `Processing` ou `Suspected Fraud` pour les nouvelles commandes avec ce mode de paiement.

1. Définissez **[!UICONTROL Automatically Invoice All Items]** sur `Yes` si vous souhaitez facturer automatiquement tous les articles dont le solde est nul.

   Cette option n’est disponible que si l’option **[!UICONTROL New Order Status]** est définie sur `Processing`.

   >[!NOTE]
   >
   >Si _[!UICONTROL New Order Status]_est défini sur `Processing` et_[!UICONTROL Automatically Invoice All Items]_ sur `No`, vous devez également attribuer **[!UICONTROL Order Status]** = `Processing` pour le mappage **[!UICONTROL Order State]** = `Pending` et **[!UICONTROL Default Status]** = `No` sur la page [Order Status](order-status.md#custom-order-status).

1. Définissez **[!UICONTROL Payment from Applicable Countries]** sur l’une des options suivantes :

   - `All Allowed Countries` - Les clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiés dans la configuration de votre boutique peuvent utiliser ce mode de paiement.
   - `Specific Countries` - Une fois cette option sélectionnée, la liste des _[!UICONTROL Payment from Specific Countries]_s’affiche. Pour sélectionner plusieurs pays, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et cliquez sur chaque option.

1. Par **[!UICONTROL Sort Order]**, saisissez un nombre qui détermine la position de cet article dans la liste des modes de paiement affichée lors du passage en caisse.

   Ce nombre est relatif aux autres modes de paiement. (`0` = premier, `1` = deuxième, `2` = troisième, etc.)

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
