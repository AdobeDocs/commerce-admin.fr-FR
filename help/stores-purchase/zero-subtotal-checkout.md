---
title: Aucun sous-total passage en caisse
description: Découvrez comment configurer un sous-total nul comme mode de paiement hors ligne sur votre boutique.
exl-id: c14ce289-8292-41d9-a448-f493c784f35c
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Aucun sous-total passage en caisse

_Aucun sous-total passage en caisse_ peut être utilisé pour les commandes dont le sous-total est nul après application d’une remise. Par exemple, aucun sous-total passage en caisse peut être utilisé dans les situations suivantes :

- Une remise couvre l’intégralité du prix de l’achat, sans frais supplémentaires pour l’expédition.

- Le client ajoute une [téléchargeable](../catalog/product-create-downloadable.md) ou [virtual](../catalog/product-create-virtual.md) produit dans le panier, et le prix est égal à zéro.

- Le prix d’un [simple](../catalog/product-create-simple.md) le produit est nul et la variable [livraison gratuite](shipping-free.md) est disponible.

- A [code de coupon](../merchandising-promotions/price-rules-cart-coupon.md) couvre le prix total des produits et de l’expédition.

Pour gagner du temps, aucun sous-total ne peut être défini pour une facture automatique.

**_Pour configurer zéro passage en caisse sous-total :_**

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Payment Methods]**.

1. Sous _[!UICONTROL Other Payment Methods]_, développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Zero Subtotal Checkout]**.

   ![Achat de sous-total nul](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Si nécessaire, effacez d’abord la variable **[!UICONTROL Use system value]** pour modifier ces paramètres.

1. Pour activer zéro passage en caisse de sous-total, définissez **[!UICONTROL Enabled]** to `Yes`.

1. Pour **[!UICONTROL Title]**, saisissez un titre qui identifie la méthode de sous-total zéro lors de l’extraction.

1. Si les commandes attendent généralement leur approbation, acceptez la valeur par défaut **[!UICONTROL New Order Status]** as `Pending"` jusqu’à ce que la commande soit approuvée.

   Si vous préférez, vous pouvez utiliser la variable `Processing` ou `Suspected Fraud` statut des nouvelles commandes avec ce mode de paiement.

1. Définir **[!UICONTROL Automatically Invoice All Items]** to `Yes` si vous souhaitez facturer automatiquement tous les articles dont le solde est nul.

   Cette option est disponible uniquement si la variable **[!UICONTROL New Order Status]** est définie sur `Processing`.

   >[!NOTE]
   >
   >If _[!UICONTROL New Order Status]_est défini sur `Processing` et_[!UICONTROL Automatically Invoice All Items]_ est défini sur `No`, vous devez également affecter **[!UICONTROL Order Status]** = `Processing` pour le **[!UICONTROL Order State]** = `Pending` et **[!UICONTROL Default Status]** = `No` sur le [État de la commande](order-status.md#custom-order-status) page.

1. Définir **[!UICONTROL Payment from Applicable Countries]** à l’une des options suivantes :

   - `All Allowed Countries` - Clients de tous les [pays](../getting-started/store-details.md#country-options) spécifié dans votre configuration de magasin peut utiliser ce mode de paiement.
   - `Specific Countries` - Après avoir choisi cette option, la variable _[!UICONTROL Payment from Specific Countries]_s’affiche. Pour sélectionner plusieurs pays, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre qui détermine la position de cet élément dans la liste des méthodes de paiement affichées lors du passage en caisse.

   Ce nombre est relatif aux autres modes de paiement. (`0` = first, `1` = second, `2` = troisième, etc.)

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.
