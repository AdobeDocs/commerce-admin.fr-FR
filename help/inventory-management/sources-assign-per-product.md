---
title: Affecter des sources d'inventaire par produit
description: Découvrez comment affecter une source d’inventaire à un produit.
exl-id: 7e47be25-633e-4f5d-bb61-0d9e79b6dbad
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/Wjx3w6Z-oNALxNRHw65BZDeCzka3BQvtg-m4a9kp-Y8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 0%

---

# Attribuer des sources par produit

Avant de modifier les quantités et les paramètres, vous devez affecter des [sources](sources-manage.md) aux produits.

{{$include /help/_includes/unassign-source.md}}

## Affectation de sources à un produit

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Ouvrez un produit en mode _Modifier_.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Sources]** .

   Cette section vous permet de modifier l&#39;origine, de mettre à jour les quantités en stock, etc.

   >[!NOTE]
   >
   >Actuellement, seuls les produits simples, configurables, virtuels, téléchargeables et groupés prennent en charge plusieurs sources. Les produits groupés peuvent être créés et gérés uniquement avec le Source et le Stock par défaut.

   ![Section Sources de produit](assets/inventory-product-sources-before.png){width="600" zoomable="yes"}

1. Pour ajouter une source, cliquez sur **[!UICONTROL Assign Sources]**.

1. Sur la page _[!UICONTROL Assign Sources]_, cochez la case en regard de chaque source que vous souhaitez affecter au produit.

   ![Produit - Attribuer des sources](assets/inventory-product-assign-sources.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Done]** pour ajouter les sources.

1. Effectuez l’une des opérations suivantes pour enregistrer :

   - Cliquez sur **[!UICONTROL Save]**.
   - Dans le menu _[!UICONTROL Save]_(![flèche du menu](../assets/icon-menu-down-arrow-red.png)), choisissez **[!UICONTROL Save & Close]**.

Après avoir affecté des origines, mettez à jour la [quantité en stock](quantities-assign-per-product.md) pour chaque origine de produit.

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
