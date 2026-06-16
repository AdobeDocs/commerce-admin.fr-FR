---
title: Modes de paiement stockés
description: Découvrez comment les clients peuvent utiliser des modes de paiement stockés sur votre storefront Commerce.
exl-id: 5e264f84-1891-4ee9-8ebe-55ac9c93ab8c
feature: Payments
TQID: https://experienceleague.adobe.com/dYEYXgEIp83AKhHepfDQVNR9YBUQGbJ7B2zu8UTM-I4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
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
source-wordcount: 226
ht-degree: 0%

---

# Modes de paiement stockés

Les clients qui ont accès à un coffre sécurisé pour stocker les informations de paiement peuvent passer rapidement en caisse sans saisir leurs informations de carte de crédit à chaque fois. Si l’option [Achat instantané](checkout-instant-purchase.md) est activée, les clients peuvent contourner le processus de passage en caisse en deux étapes et passer la commande à partir de la page du produit.

Un mode de paiement prenant en charge un coffre sécurisé, tel que [&#128279;](braintree.md), est requis. Lorsqu’un coffre sécurisé est activé dans la configuration du mode de paiement, les clients ont la possibilité, lors du passage en caisse, d’enregistrer leurs informations de carte de crédit en tant que mode de paiement stocké. Les clients peuvent gérer les modes de paiement stockés à partir du tableau de bord de leur compte.

![Modes de paiement stockés](./assets/customer-account-stored-payment-methods.png){width="700" zoomable="yes"}

## Ajouter un mode de paiement stocké lors du passage en caisse

1. Depuis le storefront, le client accède à la page des détails du produit.

1. Ajoute un produit au panier.

1. Accède à la page de passage en caisse.

1. Termine l’étape _Expédition_.

1. Sélectionne le mode de paiement **[!UICONTROL Braintree Credit Card]**.

1. Renseigne les données de carte de crédit.

1. Sélectionne la case à cocher **[!UICONTROL Save for later use]**.

1. Effectue un clic sur **[!UICONTROL Place Order]**.

Le mode de paiement enregistré est alors affiché dans l’onglet _[!UICONTROL Stored Payment Methods]_&#x200B;du tableau de bord du client.

## Supprimer un mode de paiement stocké

Les modes de paiement stockés précédemment ajoutés ne peuvent pas être modifiés par le client, ils peuvent uniquement être supprimés. Cette action est irréversible.

1. Dans la barre latérale de son compte, le client sélectionne **[!UICONTROL Stored Payment Methods]**.

1. Recherche l&#39;écriture de mode de paiement à supprimer.

1. Effectue un clic sur **[!UICONTROL Delete]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.
