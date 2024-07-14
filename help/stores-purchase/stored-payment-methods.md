---
title: Méthodes de paiement stockées
description: Découvrez comment les clients peuvent utiliser les méthodes de paiement stockées sur votre vitrine Commerce.
exl-id: 5e264f84-1891-4ee9-8ebe-55ac9c93ab8c
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Méthodes de paiement stockées

Les clients qui ont accès à un coffre sécurisé pour stocker des informations de paiement peuvent accélérer leur passage en caisse sans saisir à chaque fois leurs informations de carte de crédit. Si l’option [Achat instantané](checkout-instant-purchase.md) est activée, les clients peuvent ignorer le processus de paiement en deux étapes et passer la commande à partir de la page du produit.

Un mode de paiement prenant en charge un coffre sécurisé, tel que [Braintree](braintree.md), est requis. Lorsqu’un coffre sécurisé est activé dans la configuration du mode de paiement, les clients ont la possibilité, lors de leur passage en caisse, d’enregistrer leurs informations de carte de crédit comme méthode de paiement stockée. Les clients peuvent gérer les modes de paiement stockés à partir du tableau de bord de leur compte.

![Méthodes de paiement stockées](./assets/customer-account-stored-payment-methods.png){width="700" zoomable="yes"}

## Ajout du mode de paiement stocké au passage en caisse

1. Depuis le storefront, le client accède à la page de détails du produit.

1. Ajoute un produit au panier.

1. Passe à la page de passage en caisse.

1. Exécute l’étape _Expédition_.

1. Sélectionne le mode de paiement **[!UICONTROL Braintree Credit Card]**.

1. Remplit les données de carte de crédit.

1. Sélectionne la case à cocher **[!UICONTROL Save for later use]**.

1. Clics **[!UICONTROL Place Order]**.

Le mode de paiement enregistré est ensuite affiché dans l’onglet _[!UICONTROL Stored Payment Methods]_du tableau de bord du client.

## Supprimer un mode de paiement stocké

Les méthodes de paiement stockées précédemment ajoutées ne peuvent pas être modifiées par le client, elles ne peuvent être supprimées que. Cette action ne peut pas être annulée.

1. Dans la barre latérale de leur compte, le client sélectionne **[!UICONTROL Stored Payment Methods]**.

1. Recherche l’entrée du mode de paiement à supprimer.

1. Clics **[!UICONTROL Delete]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.
