---
title: '[!DNL AR Viewer] pour Adobe Commerce'
description: Découvrez comment  [!DNL AR Viewer] peut bénéficier à votre instance Adobe Commerce et comment intégrer et configurer l’extension avec succès.
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# [!DNL AR Viewer] pour Adobe Commerce

La réalité augmentée (AR) décrit les expériences utilisateur qui ajoutent des éléments 2D ou 3D à la vue en direct à partir de la caméra d’un appareil de manière à ce que ces éléments apparaissent dans le monde réel.

L’extension [!DNL AR Viewer] pour Adobe Commerce optimise une expérience transparente conçue pour afficher des graphiques 3D rendus pour l’utilisateur.

Les informations de ce guide fournissent un aperçu de l’expérience d’intégration de [!DNL AR Viewer] dans Adobe Commerce et des avantages de [!DNL AR Viewer] pour l’utilisateur, ainsi que des bonnes pratiques à suivre le long de ce parcours.

Développé par Pixar, [Universal Scene Description (USD)](https://openusd.org/release/index.html){target=_blank} est le premier logiciel open source qui peut échanger des scènes 3D de manière robuste et évolutive, qui peuvent être composées de nombreuses ressources, sources et animations différentes, tout en favorisant des workflows collaboratifs de grande qualité. Cet USD est utilisé dans les fichiers `.USDZ`. Ce fichier `.USDZ` diffuse du contenu AR et 3D sur les appareils de l’utilisateur.

>[!NOTE]
>
> [!DNL AR Viewer] ne prend en charge que `.USDZ` fichiers.

## [!DNL AR Viewer] requis

[!DNL AR Viewer] est compatible avec [!DNL Magento Open Source] et Adobe Commerce. Voir [Stratégie de cycle de vie](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank} pour plus d’informations sur les versions prises en charge.

Voir [Installation de l’ [!DNL AR Viewer] extension](../catalog/ar-viewer-setup.md) pour plus d’informations.

Pour utiliser [!DNL AR Viewer], les éléments suivants doivent être disponibles pour votre instance :

* PHP 8.1.0
* Adobe Commerce version 2.4.4 et ultérieure
* Magento Open Source (CE) version 2.4.x

## Limites de compatibilité

[!DNL AR Viewer] limitations de compatibilité existantes :

* `.USDZ` uniquement : cette fonctionnalité prend uniquement en charge les fichiers `.USDZ`.
* `qr-code` : `endroid/qr-code` version 4.5 requise.
* `Catalog module` : `magento/module-catalog` version 104.0.0 requise.
