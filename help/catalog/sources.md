---
title: Paramètres du produit - [!UICONTROL Sources]
description: Pour un produit, les paramètres de [!UICONTROL Sources] permettent d’accéder aux sources  [!DNL Inventory Management]  à partir desquelles le produit peut être distribué.
exl-id: 986f6031-0edc-4105-aa02-1c22364b3e7c
feature: Catalog Management, Products, Inventory
TQID: https://experienceleague.adobe.com/7LFF4ufXyKtJwUp4DiNDdnRMhFRsM1tX8Z2TlPt1Kso
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ccaac3a13a346ce192a724efb3384ef2d612c980
workflow-type: tm+mt
source-wordcount: 259
ht-degree: 1%

---

# Paramètres du produit - [!UICONTROL Sources]

La section _[!UICONTROL Sources]_&#x200B;des paramètres du produit répertorie les sources à partir desquelles le produit peut être distribué. Il permet d’affecter et d’annuler l’affectation des sources, ainsi que de gérer la quantité et la disponibilité du produit. Cette section s’affiche uniquement si plusieurs sources sont définies pour votre boutique. Pour plus d’informations sur les sources, voir [Gérer les sources](../inventory-management/sources-manage.md).

## Attribution d’une source à un produit

1. Cliquez sur **[!UICONTROL Assign Source]**.

1. Cochez la case correspondant aux sources requises.

1. Cliquez sur **[!UICONTROL Done]**.

1. Sélectionnez **[!UICONTROL Source Item Status]** et saisissez les valeurs **[!UICONTROL Qty]** et **[!UICONTROL Notify Qty]** selon vos besoins.

1. Cliquez sur **[!UICONTROL Save]** pour enregistrer les modifications.

![Vue Sources](./assets/catalog-sources-list.png){width="600" zoomable="yes"}

## Référence du champ

| Champ | Description |
|--- |--- |
| [!UICONTROL Name] | Nom unique d’une source. |
| [!UICONTROL Source Status] | Détermine si le produit est activé ou désactivé dans le catalogue. |
| [!UICONTROL Source Item Status] | Détermine la disponibilité actuelle du produit. Options :<br />**[!UICONTROL In Stock]**- Rend le produit disponible à l’achat.<br />**[!UICONTROL Out of Stock]** - Sauf si les commandes en souffrance sont activées, empêche l&#39;achat du produit et supprime la liste du catalogue. |
| [!UICONTROL Qty] | Montant du stock disponible pour chaque origine. |
| [!UICONTROL Notify Qty] | Montant de l&#39;option _Notifier pour la quantité_ pour cette origine spécifique si `Notify Quantity Use Default` n&#39;est pas sélectionnée. |
| [!UICONTROL Notify Qty Use Default] | Indique d&#39;utiliser le paramètre par défaut _Notifier pour la quantité_ dans le stock avancé du produit ou le paramètre global dans la configuration du magasin. Pour plus d&#39;informations sur les paramètres d&#39;inventaire avancés de votre produit, voir [Configurer les options avancées du produit](../inventory-management/product-options.md). |
| [!UICONTROL Actions] | Pour une source affectée, cliquez sur **[!UICONTROL Unassign]** pour que la source ne soit pas disponible pour le produit. Pour une source non affectée, cliquez sur **[!UICONTROL Assign Sources]** pour rendre une source disponible pour le produit. Pour plus d’informations sur [!UICONTROL Assign Sources] options, voir [Attribution de sources par produit](../inventory-management/sources-assign-per-product.md). |

{style="table-layout:auto"}

