---
title: Exemple de règle de prix du panier - Promotion de la livraison gratuite
description: Examinez un exemple d’utilisation d’une règle de prix de panier pour offrir la livraison gratuite.
exl-id: f7652254-ff01-44ff-a207-2d7cf2017517
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Exemple de règle de prix du panier - Promotion de la livraison gratuite

La livraison gratuite peut être proposée sous forme de promotion, avec ou sans [coupon](price-rules-cart-coupon.md). Un bon de livraison gratuit, ou bon, peut également être appliqué aux commandes de nettoyage des clients. La commande peut donc être facturée et expédiée pour terminer la [workflow](../stores-purchase/order-processing.md#order-workflow-and-processing).

Certaines configurations de l’opérateur de livraison vous permettent d’offrir une livraison gratuite selon une commande minimale. Pour développer cette fonctionnalité de base, vous pouvez utiliser les règles de prix du panier pour créer des conditions complexes basées sur plusieurs attributs de produit, contenus du panier et groupes de clients.

## Étape 1. Activer la livraison gratuite

1. Activer [livraison gratuite](../stores-purchase/shipping-free.md) dans votre configuration de magasin.

1. Définissez les paramètres de livraison gratuite pour tout [service carrier](../stores-purchase/carriers.md) que vous souhaitez utiliser pour la livraison gratuite.

## Étape 2. Créer une règle de prix de panier

Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

Suivez les étapes ci-dessous pour configurer le type de promotion de livraison gratuite que vous souhaitez proposer.

### Exemple 1 : livraison gratuite pour toute commande

1. Procédez comme suit : **[!UICONTROL Rule Information]** comme suit :

   - Saisissez un **[!UICONTROL Rule Name]** pour référence interne.
   - Entrez un résumé **[!UICONTROL Description]** pour décrire la règle.
   - Définir **[!UICONTROL Active]** to `Yes`.
   - Dans le **[!UICONTROL Websites]** sélectionnez chaque site sur lequel le coupon de livraison gratuit doit être disponible.
   - Sélectionnez la variable **[!UICONTROL Customer Groups]** à laquelle la règle s’applique.
   - Définir **[!UICONTROL Coupon]** à l’une des options suivantes :
      - Pour proposer une promotion de livraison gratuite sans coupon, acceptez la valeur par défaut (`No Coupon`).
      - Pour utiliser un coupon avec la règle de prix, sélectionnez `Specific Coupon`. Si nécessaire, suivez les instructions pour configurer une [coupon](price-rules-cart-coupon.md).

1. Faire défiler vers le bas et développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Actions]** et procédez comme suit :

   - Définir **[!UICONTROL Apply]** to `Percent of product price discount`.
   - Définir **[!UICONTROL Apply to Shipping Amount]** to `Yes`.
   - Définir **[!UICONTROL Free Shipping]** to `For matching items only`.

   ![Règle de prix du panier - Actions d’expédition gratuite](./assets/free-shipping-actions.png){width="600" zoomable="yes"}

### Exemple 2 : expédition gratuite pour les commandes de plus de $

1. Procédez comme suit : **[!UICONTROL General Information]** comme décrit dans l’exemple précédent.

1. Faire défiler vers le bas et développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Conditions]** .

1. Cliquez sur _Ajouter_ (![Icône Ajouter](../assets/icon-add-green-circle.png)) pour insérer une condition et procédez comme suit :

   - Dans la liste sous **[!UICONTROL Cart Attribute]**, choisissez `Subtotal`.
   - Cliquez sur **[!UICONTROL is]** et choisissez `equals or greater than`.
   - Cliquez sur **..** et saisissez une valeur de seuil pour le sous-total, telle que `100`, pour remplir la condition.

   ![Règle de prix du panier - condition](./assets/free-shipping-condition1.png){width="600" zoomable="yes"}

1. Si nécessaire, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Actions]** et procédez comme suit :

   - Définir **[!UICONTROL Apply]** to `Percent of product price discount`.
   - Définir **[!UICONTROL Apply to Shipping Amount]** to `Yes`.
   - Définir **[!UICONTROL Free Shipping]** to `For matching items only`.

## Étape 3. Remplissage des étiquettes

Terminer [Étape 4](price-rules-cart.md) des instructions de règle de prix du panier pour saisir les libellés qui apparaissent lors du passage en caisse.

## Étape 4. Enregistrer et tester la règle

{{new-price-rule}}

1. Une fois la règle terminée, cliquez sur **[!UICONTROL Save Rule]**.

1. Testez la règle pour vous assurer qu’elle fonctionne correctement.
