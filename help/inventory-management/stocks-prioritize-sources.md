---
title: Hiérarchiser les sources de stock pour un stock
description: Découvrez comment organiser les sources de haut en bas dans la priorité, qui est utilisée lors de la détermination des déductions d'expédition et de stock.
exl-id: 16db3ee3-ce99-40dd-b1a3-fcb145b1298f
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/oPgeuN3-Il-yf3zpG2r4PNAmNbf-4gmz5-GFngM3-Ng
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
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
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 210
ht-degree: 0%

---

# Hiérarchiser les sources d’un stock

Après avoir ajouté [sources](sources-manage.md) au [stock](stocks-manage.md), organisez ces sources de haut en bas en priorité pour exécuter les commandes. L&#39;algorithme Source Selection Algorithm (SSA) fournit un algorithme Priorité en utilisant cet ordre lors de la détermination des déductions d&#39;expédition et de stock.

La priorité d&#39;origine des stocks n&#39;influence pas les origines affectées lors de la modification des stocks de produits.

Dans cet exemple, le stock britannique a des sources affectées dans le désordre pour un magasin et deux entrepôts à Londres et un entrepôt à Berlin.

![Ordre de Source avant hiérarchisation](assets/inventory-priority-before.png){width="350" zoomable="yes"}

Le marchand préfère que les envois soient prioritaires à partir du plus grand entrepôt de Berlin, puis de l&#39;entrepôt de Londres, de l&#39;emplacement de débordement de Londres, et enfin du storefront de Londres. Pour modifier l’ordre, les entrées sont glissées-déposées dans l’ordre souhaité.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stocks]**.

1. Ouvrez le stock en mode _Modifier_.

1. Développez l’onglet _[!UICONTROL Sources]_, si nécessaire.

1. Utilisez l’icône ![Trier](assets/icon-sort.png) pour faire glisser les sources et les déposer dans une priorité allant du haut (première) au bas (dernière).

   Cette commande est importante lors de l’expédition des commandes. SSA recommande les expéditions en fonction de l&#39;ordre des sources

1. Cliquez sur **[!UICONTROL Save & Continue]** pour enregistrer les modifications.

![Ordre de Source après la hiérarchisation](assets/inventory-stock-priority-after.png){width="350" zoomable="yes"}
