---
title: Exemple de règle de prix du panier - escompte avec achat minimum
description: Examinez un exemple d’utilisation d’une règle de prix de panier pour offrir une remise avec un achat minimal.
exl-id: dc06cd12-d23b-4836-9ad2-93ca60dac927
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Exemple de règle de prix du panier - escompte avec achat minimum

Les règles de prix du panier peuvent être utilisées pour offrir une remise en pourcentage basée sur un achat minimal. Dans l’exemple suivant, une remise de 25 % est appliquée à tous les achats de plus de 200,00 $ dans une catégorie spécifique. Le format de la remise est le suivant :

X % de toutes les Y (catégorie) supérieures à Z dollars

## Étape 1. Créer une règle de panier

Suivez les [instructions](price-rules-cart.md) pour créer une règle de panier.

## Étape 2. Définir les conditions

1. Faire défiler vers le bas et développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Conditions]** .

1. Cliquez sur _Ajouter_ (![Icône Ajouter](../assets/icon-add-green-circle.png)) et choisissez **[!UICONTROL Product Attribute Combination]**.

   ![Condition de règle de prix du panier - combinaison d’attributs de produit](./assets/condition1.png){width="500" zoomable="yes"}

1. Cliquez sur _Ajouter_ (![Icône Ajouter](../assets/icon-add-green-circle.png)) au début de la ligne suivante et dans la liste sous **[!UICONTROL Product Attribute]**, choisissez **[!UICONTROL Category]**.

   - Cliquez sur (**..**) _more_ pour afficher d’autres options.

     ![Condition de règle de prix du panier - Options de catégorie](./assets/condition3.png){width="600" zoomable="yes"}

   - Cliquez sur le bouton _Sélecteur_ (![Icône Liste](../assets/icon-list-chooser.png)) pour afficher les catégories disponibles. Dans l’arborescence des catégories, cochez la case de chaque catégorie à inclure. Cliquez sur l’icône représentant une coche pour accepter les sélections de catégorie.

     ![Condition de règle de prix du panier - catégorie](./assets/condition4.png){width="600" zoomable="yes"}

1. Cliquez sur _Ajouter_ (![Icône Ajouter](../assets/icon-add-green-circle.png)) au début de la ligne suivante et procédez comme suit :

   - Dans la liste sous **[!UICONTROL Cart Item Attribute]**, choisissez **[!UICONTROL Price in cart]**.

     ![Condition de règle de prix du panier - attribut article de panier](./assets/condition5.png){width="500"}

   - Cliquez sur **is** et choisissez `equals or greater than`.

   - Cliquez sur **..** et indiquez le montant que le prix du panier doit être pour remplir la condition. Par exemple, saisissez `30`.

     ![Condition de règle de prix du panier - prix du panier](./assets/condition6.png){width="500"}

1. Cliquez sur **[!UICONTROL Save and Continue Edit]**.

## Étape 3. Définition des actions

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Actions]** et procédez comme suit :

   ![Actions des règles de prix du panier](./assets/minimum-discount-actions.png){width="600" zoomable="yes"}

   - Définir **[!UICONTROL Apply]** to `Percent of product price discount`.

   - Saisissez le **[!UICONTROL Discount Amount]**. Par exemple, saisissez `10` pour une remise de 10 %.

   - Pour empêcher l’application de promotions supplémentaires à l’achat, définissez **[!UICONTROL Discard subsequent rules]** to `Yes`.

1. Cliquez sur **[!UICONTROL Save and Continue Edit]** et exécutez la règle selon vos besoins.

## Étape 4. Remplissage des étiquettes

Terminer [Étape 4](price-rules-cart.md) des instructions de règle de prix du panier pour saisir les libellés qui apparaissent lors du passage en caisse.

## Étape 5 : enregistrer et tester la règle

{{new-price-rule}}

1. Une fois la règle terminée, cliquez sur **[!UICONTROL Save Rule]**.

1. Testez la règle pour vous assurer qu’elle fonctionne correctement.
