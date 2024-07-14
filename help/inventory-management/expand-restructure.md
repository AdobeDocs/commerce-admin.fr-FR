---
title: Agrandir et restructurer l'inventaire
description: Découvrez comment vous développer pour devenir un commerçant multi-source ou réduire à un marchand à source unique.
exl-id: 880474e3-6533-4b2f-adf7-4312787ff736
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# Agrandir et restructurer l&#39;inventaire

À mesure que votre entreprise se développe et change, [!DNL Inventory Management] prend en charge vos besoins. Vous pouvez vous développer en tant que commerçant multi-source ou vous réduire facilement à un marchand à source unique.

## Développez-le pour plusieurs sources.

Les commerçants à source unique peuvent ajouter de nouveaux magasins, entrepôts, débardeurs, etc. L&#39;extension ne nécessite que quelques ajouts et mises à jour de stock pour être étendue au multi-sourcing :

1. Ajoutez des [sources personnalisées](sources-add.md) pour chaque nouvel emplacement.

   Vous utilisez uniquement le Source par défaut pour les produits groupés.

1. Ajoutez des [stocks personnalisés](stocks-add.md) si nécessaire pour vos nouvelles sources.

   Par exemple, vous pouvez créer des stocks par site web, pays, région ou autre méthode. Vous pouvez affecter des sources à vos stocks personnalisés. Vous utilisez uniquement le stock par défaut pour les produits en bundle.

1. Mettez à jour les [affectations source et les quantités](quantities-manage.md) pour vos produits.

   Vous pouvez également utiliser les fonctionnalités [Mass Actions Tool](bulk-assignment.md) et [Import-Export](inventory-import-export.md) pour ajouter rapidement des sources et des données de produit.

## Restructuration en source unique

Pour les marchands multi-sources qui souhaitent réduire les ventes en ligne à un seul emplacement pour l’expédition, modifiez vos sources, stocks et quantités à mettre à jour :

1. Désactivez les [sources personnalisées](sources-disable.md).

1. Transférez l’inventaire des produits vers votre Source par défaut.

   Il est recommandé d’utiliser des actions de masse. Voir [Transfert de l’inventaire vers Source](inventory-transfer.md).

1. Affectez tous les sites Web à [Default Stock](stocks-manage.md).
