---
title: Exemple de règle de prix du panier - achetez cette get que vous recherchez
description: Examinez un exemple d’utilisation d’une règle de prix de panier pour proposer une promotion "achetez-obtenez-cela".
exl-id: 49e4f9d1-bc60-4861-baca-a23fe148d1c4
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 0%

---

# Exemple de règle de prix du panier - achetez cette get que vous recherchez

Cet exemple montre comment configurer une [règle de prix du panier](price-rules-cart.md) pour un _Achetez ceci, achetez-le gratuitement._ promotion. Le format de la remise est le suivant :

_Acheter X quantité de produit, obtenir Y quantité gratuitement_

## Étape 1. Créer une règle de prix de panier

Terminer [Étape 1](price-rules-cart.md) des instructions de règle de prix du panier pour renseigner les informations de règle.

## Étape 2. Définir les conditions

Terminer [Étape 2](price-rules-cart.md) des instructions du panier pour définir les conditions de la règle de prix. Il s’agit de la première des deux conditions qui peuvent être ajoutées à la règle et qui détermine le moment où la règle est déclenchée. Il peut être basé sur une combinaison des éléments suivants :

- Attributs de produit
- Produits
- Attributs du panier
- ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Segments de client

Si rien n’est indiqué, la règle est déclenchée pour chaque panier.

![Règle de prix du panier - condition](./assets/buy-x-get-y-condition-default.png){width="600" zoomable="yes"}

## Étape 3. Définition des actions

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Actions]** et procédez comme suit :

   - Définir **[!UICONTROL Apply]** to `Buy X get Y free (_[!UICONTROL _[!UICONTROL Discount Amount]_]_ is Y)`.

   - Définir **[!UICONTROL Discount Amount]** to `1`. Il s’agit de la quantité que le client reçoit gratuitement.

   - Pour limiter le nombre de remises qui peuvent être appliquées lorsque la condition est remplie, saisissez le nombre dans la variable **[!UICONTROL Maximum Qty Discount is Applied To]** champ . Ce calcul est effectué à l’aide de cette méthode [formule](#maximum-quantity-discount).

   - Pour **[!UICONTROL Discount Qty Step (Buy X)]**, saisissez la quantité que le client doit acheter pour bénéficier de la remise. Dans cet exemple, le client doit en acheter trois.

   - Si vous souhaitez empêcher l’application d’autres remises à l’achat, définissez **[!UICONTROL Discard subsequent rules]** to `Yes`.

   ![Règle de prix du panier - achat de 3 billets 1 gratuit](./assets/buy-3-get-1-actions.png){width="600" zoomable="yes"}

1. Pour appliquer la règle uniquement à des éléments spécifiques du panier, remplissez la condition afin de décrire les éléments du panier et/ou les attributs de produit requis pour la promotion.

   L’exemple suivant utilise le SKU pour appliquer la règle à toutes les variantes associées d’un produit configurable.

   ![Règle de prix du panier - condition pour les articles de panier](./assets/buy-3-get-1-actions-condition.png){width="600" zoomable="yes"}

1. À inclure **[!UICONTROL Free Shipping]**, choisissez `For matching items only`.

1. Cliquez sur **[!UICONTROL Save and Continue Edit]** et exécutez le reste de la règle selon les besoins.

## Étape 4. Renseignez le libellé

Terminer [Étape 4](price-rules-cart.md) des instructions de la règle de prix du panier pour saisir le libellé qui apparaît lors du passage en caisse.

## Étape 5 : enregistrer et tester la règle

{{new-price-rule}}

1. Une fois la règle terminée, cliquez sur **[!UICONTROL Save Rule]**.

1. Testez la règle pour vous assurer qu’elle fonctionne correctement.

## Variations

Buy X Get Y Free est traité comme une action unique, avec une _total des lignes_ dépendance. Tous les éléments doivent provenir du même SKU pour pouvoir bénéficier de la promotion. Par exemple :

Achetez X quantité de produit de la catégorie A, obtenez Y quantité du même produit gratuitement.

Pour limiter le produit gratuit aux catégories A, B et C, définissez l’action comme suit :

Si TOUTES ces conditions sont TRUE : Catégorie est l’une des catégories A, B, C

Pour limiter les éléments gratuits de n’importe quelle catégorie (A, B ou C) et recevoir Y des SKU (D123, E123 ou F123), définissez l’action comme suit :

Si TOUTES ces conditions sont TRUE : SKU est un D123, E123, F123

## Remise quantitative maximale

Utilisez la formule suivante pour déterminer la valeur correcte de la remise maximale sur la qualité :

Formule = `(X+Y) * (M/Y)`
Où
`X` = nombre d’articles achetés
`Y` = nombre d’éléments gratuits
`M` = Nombre maximal d’articles libres autorisés

Par exemple :

Achetez cinq et obtenez deux articles gratuits avec un maximum de quatre articles gratuits.

    Où
    X = 5
    Y = 2
    M = 4
    Remise sur la quantité maximale = (5+2)*(4/2)=(7)*(2)=14

Achetez cinq et obtenez trois articles gratuits avec neuf articles gratuits.

    Où
    X = 5
    Y = 3
    M = 9
    Remise sur la quantité maximale = (5+3)*(9/3)=24

Achetez 20 et obtenez deux articles gratuits avec un maximum de 20 articles gratuits.

    Où
    X = 20
    Y = 2
    M = 20
    Remise sur la qualité maximale = (20+2)*(20/2)=(22)*(10)=220
