---
title: Prix de niveau
description: Découvrez comment utiliser le niveau de prix pour offrir une remise quantitative à partir d’une liste de produits ou d’une page de produits.
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Prix de niveau

Le prix de niveau vous permet d’offrir une remise quantitative sur une liste de produits ou une page de produits dans le storefront. La remise peut être appliquée à une vue de magasin spécifique, à un groupe de clients ou à un catalogue partagé.

Si vous avez de nombreux produits à mettre à jour, il est plus efficace d’importer les modifications de prix du niveau, plutôt que de les saisir individuellement. Pour plus d’informations, voir [Prix du niveau d&#39;import](../systems/data-import-price-tier.md).

![Prix de niveau sur une page de produits storefront](./assets/product-price-tier-storefront.png){width="700" zoomable="yes"}

La page produit calcule la remise sur la quantité et affiche un message tel que :

`Buy 6 for $5.95 each and save 15%`

Les prix dans la vitrine sont prioritaires de la quantité la plus élevée à la quantité la plus faible. Si vous avez un prix de niveau pour la quantité `5` et un pour `10`et qu’un client ajoute cinq, six, sept, huit ou neuf articles au panier, il reçoit le prix réduit de la quantité `5` niveau. Lorsque le client ajoute le dixième élément, le prix réduit spécifié pour la quantité `10` le niveau remplace le niveau pour une quantité de `5`, et le prix escompté pour `10` s’applique.

## Ajout d’un niveau de prix pour un produit

1. Ouvrez le produit en mode d’édition.

1. Sous la section _[!UICONTROL Price]_champ, cliquez sur **[!UICONTROL Advanced Pricing]**.

1. Dans le _[!UICONTROL Tier Price]_, cliquez sur **[!UICONTROL Add]**.

   Si vous créez un niveau de plusieurs prix, cliquez sur **[!UICONTROL Add]** pour chaque niveau supplémentaire, afin que vous puissiez travailler tous les niveaux en même temps. Chaque niveau du groupe possède le même site web et groupe de clients ou une affectation de catalogue partagée, mais une quantité et un prix différents.

## Configuration du niveau de prix

1. Si votre boutique comporte plusieurs sites web, choisissez la variable **[!UICONTROL Website]** pour laquelle le niveau de prix s’applique.

1. Si nécessaire, limitez la disponibilité du niveau de tarification en sélectionnant le **[!UICONTROL Customer Group]** ou **[!UICONTROL Shared Catalog]** (![B2B pour Adobe Commerce](../assets/b2b.svg) Disponible avec [B2B pour Adobe Commerce](./b2b/../introduction.md) uniquement).

1. Pour **[!UICONTROL Qty]**, indiquez la quantité qui doit être commandée pour recevoir la remise.

   - **Méthode 1 :** Saisir le prix comme montant fixe

     Définir **[!UICONTROL Price]** to `Fixed` et indiquez le prix ajusté d’une unité à ce niveau.

     ![Prix de niveau en tant que montant fixe](./assets/product-price-tier-fixed.png){width="600" zoomable="yes"}

   - **Méthode 2 :** Entrer le prix en pourcentage

     Définir **[!UICONTROL Price]** to `Discount` et indiquez le prix actualisé en pourcentage par rapport au prix de base du produit.

     Par exemple, pour une remise de 15 %, entrez le nombre `15`. (Le prix est conservé avec deux décimales, telles que `15.00`.)

     >[!NOTE]
     >
     >Pour obtenir le prix escompté, le pourcentage défini est calculé par rapport à la valeur définie dans la variable _[!UICONTROL Price]_ , et non le champ _[!UICONTROL Special Price]_ champ .

     ![Prix de niveau en pourcentage](./assets/product-price-tier-discount.png){width="600" zoomable="yes"}

## Effectuer le paramétrage des prix

1. Pour ajouter un autre ensemble de tarifs de niveau pour un autre site web ou groupe de clients, répétez les étapes précédentes.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Done]** puis **[!UICONTROL Save]**.

>[!NOTE]
>
>La variable **_final_** le prix du produit est calculé comme suit : **_minimum_** prix pertinent, selon la formule suivante : <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Prix fixe_** les options personnalisables du produit sont _not_ affectés par les règles de prix de groupe, de prix de niveau, de prix spécial ou de prix de catalogue ;
