---
title: '[!DNL AR Viewer] pour Adobe Commerce'
description: Découvrez comment [!DNL AR Viewer] pourrait bénéficier à votre instance Adobe Commerce et comment intégrer et configurer l’extension avec succès.
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# [!DNL AR Viewer] pour Adobe Commerce

La réalité augmentée (AR) décrit les expériences utilisateur qui ajoutent des éléments 2D ou 3D à la vue en direct à partir de la caméra d’un appareil de manière à ce que ces éléments apparaissent dans le monde réel.

La variable [!DNL AR Viewer] pour l’extension Adobe Commerce, une expérience transparente conçue pour afficher des graphiques 3D rendus pour l’utilisateur.

Les informations de ce guide fournissent un aperçu de l’expérience d’intégration pour la variable [!DNL AR Viewer] dans Adobe Commerce et comment la fonction [!DNL AR Viewer] bénéficie à l’utilisateur, ainsi que des bonnes pratiques à suivre le long de ce parcours.

Développé par Pixar, [Description de scène universelle (USD)](https://www.pixar.com/usd){target=_blank} est le premier logiciel open source qui peut échanger de manière robuste et évolutive des scènes 3D qui peuvent être composées de nombreuses ressources, sources et animations différentes, tout en favorisant des processus hautement collaboratifs. Ce USD est utilisé dans `.USDZ` fichiers . Ceci `.USDZ` diffuse du contenu AR et 3D sur les appareils de l’utilisateur.

>[!NOTE]
>
> La variable [!DNL AR Viewer] prend uniquement en charge `.USDZ` fichiers .

## [!DNL AR Viewer] conditions requises

La variable [!DNL AR Viewer] est compatible avec les deux [!DNL Magento Open Source] et Adobe Commerce. Voir [Stratégie de cycle de vie](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank} pour plus d’informations sur les versions prises en charge.

Voir [Installez le [!DNL AR Viewer] extension](../catalog/ar-viewer-setup.md) pour plus d’informations.

Pour utiliser [!DNL AR Viewer], les éléments suivants doivent être disponibles pour votre instance :

* PHP 8.1.0
* Adobe Commerce version 2.4.4 et ultérieure
* Magento Open Source (CE) version 2.4.x

## Limites de compatibilité

[!DNL AR Viewer] limitations de compatibilité existantes :

* `.USDZ` uniquement : cette fonctionnalité ne prend en charge que `.USDZ` fichiers .
* `qr-code`: nécessite `endroid/qr-code` version 4.5.
* `Catalog module`: nécessite `magento/module-catalog` version 104.0.0.
