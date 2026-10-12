---
title: Promotions Cadeau gratuit
description: Découvrez comment configurer une promotion de cadeau gratuite avec des règles de prix de panier pour offrir un cadeau gratuit lorsqu’un ensemble de conditions est rempli.
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
TQID: 'https://experienceleague.adobe.com/FR-q4Qj-ZDDzmfEKSvSj-BlwsM7ro-BqAE1yCppTaXE'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 58c984c2-e237-5c50-9718-500e40d1e82c
    internal-label: Merchandising
  - id: a507b1ed-4937-53da-97ae-57d36bd5b9e0
    internal-label: Price Rules
  - id: df8eaa0e-dd74-553a-8ad5-28129f8e8d3d
    internal-label: Shopping Cart
  - id: 04d3134c-2afb-5bd7-ac14-e19fa935e848
    internal-label: Shipping/Delivery
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%
---

# Promotion cadeau gratuit

La promotion *Cadeau gratuit* vous permet de définir une [ règle de prix de panier](price-rules-cart.md) qui ajoute un article gratuit au panier dans des conditions spécifiques.

>[!NOTE]
>
>Cette fonctionnalité n’est pas prise en charge sur les storefronts Luma. Il est accessible via [](https://developer.adobe.com/commerce/webapi/graphql/schema/cart/mutations/select-free-gift/) et disponible sur les storefronts Edge Delivery Services (EDS).

## Créer une promotion cadeau gratuite

Cette section décrit comment créer une promotion cadeau gratuite en utilisant le format suivant :

**Achetez X produit, obtenez Y produit gratuitement**

1. [Créez une règle de prix de panier](price-rules-cart.md#step-1-add-a-rule) avec une promotion cadeau gratuite.

1. [Décrivez les conditions](price-rules-cart.md#step-2-describe-the-conditions) des instructions du panier pour définir les conditions de la règle de prix. Il s’agit de la première de plusieurs conditions qui peuvent être ajoutées à la règle et qui déterminent à quel moment la règle est déclenchée. Elle peut être basée sur une combinaison des éléments suivants :

   - Attributs de produit
   - Produits
   - Attributs de panier
   - Segments clients Adobe Commerce

   Si rien n’est indiqué, la règle est déclenchée pour chaque panier.

   ![Règle de prix du panier - Conditions](./assets/conditions.png){width="600" zoomable="yes"}

1. Définissez les actions de la règle de prix de panier :

   1. Développez  (../assets/icon-display-expand.png) la section **[!UICONTROL Actions]** et saisissez les informations suivantes :

   - Définissez **[!UICONTROL Apply]** sur `Free Gift`.
   - Dans **[!UICONTROL Gift SKU(s)]**, sélectionnez un ou plusieurs SKU que le client peut choisir comme cadeau gratuit.
   - Définissez **[!UICONTROL Free Gift Discount Type]** sur **[!UICONTROL Price Based]** ou **[!UICONTROL Discount Based]**.
   - Dans **[!UICONTROL Gift Qty]**, entrez la quantité du cadeau offert au client. Par exemple, saisissez `2` si vous souhaitez que le client reçoive deux articles gratuits.
   - Pour empêcher l&#39;application d&#39;autres remises, **[!UICONTROL Discard subsequent rules]** sur `Yes`.

   1. Cliquez sur **[!UICONTROL Save and Continue Edit]** et effectuez le reste de la règle selon vos besoins.

1. [Complétez le libellé](price-rules-cart.md) des instructions de la règle de prix du panier pour saisir le libellé qui s’affiche lors du passage en caisse.

![Règle de prix du panier - Étiquette cadeau gratuite](./assets/free-gift-promotion-label.png){width="600" zoomable="yes"}

{{new-price-rule}}

1. Une fois la règle terminée, cliquez sur **[!UICONTROL Save Rule]**.

## Variations

Vous pouvez personnaliser les règles de prix du panier de différentes manières. La fonction Cadeau gratuit peut être configurée avec deux types de remises différents :

- **Basé sur le prix** : un article de ligne cadeau est ajouté au prix de `0`.
- **Basé sur la remise** : une remise complète est appliquée à l’élément de ligne du cadeau.
