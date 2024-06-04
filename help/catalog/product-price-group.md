---
title: Tarifs des groupes
description: Découvrez comment utiliser la tarification par groupe pour définir les prix des articles à prix réduit en fonction des groupes de clients de votre boutique.
exl-id: bc5be23f-64eb-47c3-beda-01168abfbf96
feature: Catalog Management, Products, Customers
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 0%

---

# Tarifs des groupes

Vous pouvez utiliser les paramètres de configuration de produit dans l’Admin pour définir les prix des articles à prix réduit en fonction des groupes de clients de votre boutique. Ce modèle de tarification stratégique est appelé _tarif de groupe_.

Le prix réduit de n’importe quel produit peut être offert aux membres d’un groupe de clients spécifique lorsque l’acheteur est connecté à son compte. Le prix du groupe de clients s’affiche sur la page du produit avec le prix normal afin qu’un acheteur puisse facilement comparer les prix et agir en conséquence. Après avoir ajouté le produit dans le panier, le prix normal est remplacé par le prix du groupe en fonction de leur groupe de clients.

La tarification pour les groupes de clients est un composant de [tarification échelonnée](product-price-tier.md) et est défini de la même manière. La seule différence est que les prix des groupes de clients ont une quantité de 1.

![Réduction sur le groupe de clients](./assets/storefront-price-group.png){width="600" zoomable="yes"}

## Avantages du prix de groupe

- Convient aux acheteurs en gros

- Incitez les clients à mettre à niveau leur groupe de clients pour bénéficier de remises

- Campagnes marketing ciblées

- Renforcer la confiance et la crédibilité en récompensant les clients fidèles

## Configurer un prix de groupe

1. Ouvrez le produit en mode d’édition.

1. Sous la section _[!UICONTROL Price]_champ, cliquez sur **[!UICONTROL Advanced Pricing]**.

1. Dans le _[!UICONTROL Customer Group Price]_, cliquez sur **[!UICONTROL Add]**.

   Si votre boutique comprend [Adobe Commerce B2B](../b2b/introduction.md) et possède [catalogues partagés](../b2b/catalog-shared.md) activée, cette section est intitulée _[!UICONTROL Catalog and Tier Price]_.

   ![Tarifs avancés](./assets/product-price-group.png){width="600" zoomable="yes"}

1. Configurez le prix du groupe :

   - Pour une installation multi-site, choisissez la méthode **[!UICONTROL Website]** lorsque le prix de groupe s&#39;applique.

   - Choisissez la **[!UICONTROL Customer Group]** c&#39;est-à-dire recevoir la remise.

   - Saisissez un **[!UICONTROL Quantity]** de `1`.

   - Pour **[!UICONTROL Price]**, définissez le type de prix et le montant :

      - `Fixed` - Saisissez le prix du produit escompté.

      - `Discount` - Saisissez le prix escompté en pourcentage du prix du produit.

     ![Tarifs des groupes clients](./assets/product-price-group-discount.png){width="600" zoomable="yes"}

1. Pour ajouter un autre prix de groupe, cliquez sur **[!UICONTROL Add]** et répétez l’étape précédente.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Done]** puis **[!UICONTROL Save]**.

>[!NOTE]
>
>La variable **_final_** le prix du produit est calculé comme suit : **_minimum_** prix pertinent, selon la formule suivante : <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Prix fixe_** les options personnalisables du produit sont _not_ affectés par les règles de prix de groupe, de prix de niveau, de prix spécial ou de prix de catalogue ;
