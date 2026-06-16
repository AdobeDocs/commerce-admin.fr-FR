---
title: Augmenter et restructurer l'inventaire
description: Découvrez comment vous agrandir pour devenir un commerçant multi-sources ou réduire votre activité à un commerçant mono-source.
exl-id: 880474e3-6533-4b2f-adf7-4312787ff736
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/w4TV-BQrg0RzlHn4DVSdHFPD2M5CF11wA7I5OyA7jsY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
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
source-wordcount: 219
ht-degree: 0%

---

# Augmenter et restructurer l&#39;inventaire

Au fur et à mesure que votre entreprise se développe et change, [!DNL Inventory Management] répond à vos besoins. Vous pouvez évoluer vers un commerçant multi-sources ou réduire votre activité à un commerçant mono-source en toute facilité.

## Développer vers multi-source

Les commerçants à source unique peuvent ajouter de nouveaux magasins, entrepôts, chargeurs directs, etc. L’extension ne nécessite que quelques ajouts et mises à jour de stock pour évoluer vers le multi-sourcing :

1. Ajoutez [sources personnalisées](sources-add.md) pour chaque nouvel emplacement.

   Vous utilisez uniquement le Source par défaut pour les produits groupés.

1. Ajoutez [des stocks personnalisés](stocks-add.md) selon vos besoins pour vos nouvelles sources.

   Par exemple, vous pouvez créer des stocks par site web, pays, paramètre régional ou autre méthode. Vous pouvez affecter des sources à vos stocks personnalisés. Vous utilisez uniquement le Stock par défaut pour les produits groupés.

1. Mettez à jour [affectations d&#39;origine et quantités](quantities-manage.md) pour vos produits.

   Vous pouvez également utiliser l’outil [Actions en masse](bulk-assignment.md) et la fonctionnalité [Import-Export](inventory-import-export.md) pour ajouter rapidement des sources et des données de produit.

## Restructuration vers une source unique

Pour les commerçants multi-sources qui souhaitent réduire les ventes en ligne à un seul emplacement pour l’expédition, modifiez vos sources, vos stocks et vos quantités pour mettre à jour :

1. Désactivez [&#x200B; sources personnalisées &#x200B;](sources-disable.md).

1. Transférez l’inventaire des produits vers votre Source par défaut.

   Il est recommandé d’utiliser des actions en masse. Voir [Transfert de l’inventaire vers Source](inventory-transfer.md).

1. Affectez tous les sites web au [&#x200B; Stock par défaut &#x200B;](stocks-manage.md).
