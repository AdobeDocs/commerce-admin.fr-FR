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

Le _sous-total zéro passage en caisse_ peut être utilisé pour les commandes dont le sous-total est de zéro et qui sont taxées après l’application d’une remise. Par exemple, aucun sous-total passage en caisse peut être utilisé dans les situations suivantes :

- Une remise couvre l’intégralité du prix de l’achat, sans frais supplémentaires pour l’expédition.

- Le client ajoute un produit [téléchargeable](../catalog/product-create-downloadable.md) ou [virtuel](../catalog/product-create-virtual.md) au panier, et le prix est égal à zéro.

- Le prix d’un produit [simple](../catalog/product-create-simple.md) est de zéro et la méthode [livraison gratuite](shipping-free.md) est disponible.

- Un [code de bon](../merchandising-promotions/price-rules-cart-coupon.md) couvre le prix total des produits et des frais d’expédition.

Pour gagner du temps, aucun sous-total ne peut être défini pour une facture automatique.

**_Pour configurer zéro passage en caisse de sous-total :_**

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Payment Methods]**.

1. Sous _[!UICONTROL Other Payment Methods]_, développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Zero Subtotal Checkout]**.

   ![Zéro passage en caisse sous-total](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Si nécessaire, décochez d’abord la case **[!UICONTROL Use system value]** pour modifier ces paramètres.

1. Pour activer zéro extraction de sous-total, définissez **[!UICONTROL Enabled]** sur `Yes`.

1. Pour **[!UICONTROL Title]**, saisissez un titre qui identifie la méthode de sous-total zéro lors de l’extraction.

1. Si les commandes attendent généralement leur approbation, acceptez le **[!UICONTROL New Order Status]** par défaut comme `Pending"` jusqu’à ce que la commande soit approuvée.

   Si vous préférez, vous pouvez utiliser l’état `Processing` ou `Suspected Fraud` pour les nouvelles commandes avec ce mode de paiement.

1. Définissez **[!UICONTROL Automatically Invoice All Items]** sur `Yes` si vous souhaitez facturer automatiquement tous les articles dont le solde est nul.

   Cette option est disponible uniquement si l’option **[!UICONTROL New Order Status]** est définie sur `Processing`.

   >[!NOTE]
   >
   >Si _[!UICONTROL New Order Status]_est défini sur `Processing` et_[!UICONTROL Automatically Invoice All Items]_ sur `No`, vous devez également attribuer **[!UICONTROL Order Status]** = `Processing` pour le mappage **[!UICONTROL Order State]** = `Pending` et **[!UICONTROL Default Status]** = `No` sur la page [État de la commande](order-status.md#custom-order-status).

1. Définissez **[!UICONTROL Payment from Applicable Countries]** sur l’une des options suivantes :

   - `All Allowed Countries` - Les clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiés dans votre configuration de magasin peuvent utiliser ce mode de paiement.
   - `Specific Countries` - Une fois cette option sélectionnée, la liste _[!UICONTROL Payment from Specific Countries]_s’affiche. Pour sélectionner plusieurs pays, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre qui détermine la position de cet élément dans la liste des méthodes de paiement affichées lors du passage en caisse.

   Ce nombre est relatif aux autres modes de paiement. (`0` = premier, `1` = deuxième, `2` = troisième, etc.)

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
