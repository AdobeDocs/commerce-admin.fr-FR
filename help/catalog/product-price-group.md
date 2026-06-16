---
title: Tarification du groupe
description: Découvrez comment utiliser la tarification de groupe pour définir les prix des articles à prix réduit en fonction des groupes de clients de votre boutique.
exl-id: bc5be23f-64eb-47c3-beda-01168abfbf96
feature: Catalog Management, Products, Customers
TQID: https://experienceleague.adobe.com/OCeX5pLtUzWdwOW5W8qpI4DCeab2PTAVi5xF8HUr91A
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fcid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 333
ht-degree: 0%

---

# Tarification du groupe

Vous pouvez utiliser les paramètres de configuration du produit dans l’Administration pour définir les prix des articles à prix réduit en fonction des groupes de clients de votre boutique. Ce modèle de tarification stratégique est appelé _tarification de groupe_.

Le prix réduit d’un produit peut être proposé aux membres d’un groupe de clients spécifique lorsque l’acheteur est connecté à son compte. Le prix du groupe de clients est affiché sur la page des produits avec le prix normal afin qu’un acheteur puisse facilement comparer les prix et agir en conséquence. Après avoir ajouté le produit au panier, le prix normal est remplacé par le prix de groupe en fonction du groupe de clients.

La tarification des groupes de clients est un composant de la [tarification échelonnée](product-price-tier.md) et est définie de la même manière. La seule différence est que les prix du groupe de clients ont une quantité de 1.

![Remise groupe client](./assets/storefront-price-group.png){width="600" zoomable="yes"}

## Avantages de l’utilisation de la tarification de groupe

- Convient aux acheteurs en gros

- Incitation pour les clients à mettre à niveau leur groupe de clients afin de bénéficier de remises

- Campagnes marketing ciblées

- Établir la confiance et la crédibilité en récompensant les clients fidèles

## Configurer un prix de groupe

1. Ouvrez le produit en mode d’édition.

1. Sous le champ _[!UICONTROL Price]_, cliquez sur **[!UICONTROL Advanced Pricing]**.

1. Dans la section _[!UICONTROL Customer Group Price]_, cliquez sur **[!UICONTROL Add]**.

   Si votre boutique inclut [Adobe Commerce B2B](../b2b/introduction.md) et a activé [catalogues partagés](../b2b/catalog-shared.md), cette section est intitulée _[!UICONTROL Catalog and Tier Price]_.

   ![Tarification avancée](./assets/product-price-group.png){width="600" zoomable="yes"}

1. Configurez le prix de groupe :

   - Dans le cas d’une installation multisite, choisissez le **[!UICONTROL Website]** auquel le prix de groupe s’applique.

   - Choisissez le **[!UICONTROL Customer Group]** qui recevra la remise.

   - Saisissez un **[!UICONTROL Quantity]** de `1`.

   - Par **[!UICONTROL Price]**, définissez le type de tarification et le montant :

      - `Fixed` - Saisissez le prix du produit escompté.

      - `Discount` - Entrez le prix réduit en pourcentage du prix du produit.

     ![Tarification du groupe client](./assets/product-price-group-discount.png){width="600" zoomable="yes"}

1. Pour ajouter un autre prix de groupe, cliquez sur **[!UICONTROL Add]** et répétez l’étape précédente.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Done]** puis sur **[!UICONTROL Save]**.

>[!NOTE]
>
>Le prix du produit **_final_** est calculé comme étant le prix pertinent **_minimum_** selon la formule suivante : <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Prix fixe_** les options personnalisables du produit ne sont _pas_ affectées par les règles Prix du groupe, Prix de niveau, Prix spécial ou Prix catalogue.
