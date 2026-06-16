---
title: '[!DNL AR Viewer] pour Adobe Commerce'
description: Découvrez comment le  [!DNL AR Viewer]  peut bénéficier à votre instance Adobe Commerce et comment intégrer et configurer l’extension avec succès.
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
TQID: https://experienceleague.adobe.com/ofebqdDS0exPDKJMLB-mpE0eVjRKT5ck91Fm2-7CVjA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a09a5a04-e30b-4d55-b031-38e6f5ec86db
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 247
ht-degree: 0%

---

# [!DNL AR Viewer] pour Adobe Commerce

La réalité augmentée (RA) décrit les expériences utilisateur qui ajoutent des éléments 2D ou 3D à la vue en direct à partir de la caméra d’un appareil d’une manière qui donne l’impression que ces éléments habitent le monde réel.

L’extension [!DNL AR Viewer] for Adobe Commerce offre une expérience transparente conçue pour afficher des graphiques 3D rendus à l’utilisateur.

Les informations contenues dans ce guide donnent un aperçu de l’expérience d’intégration des [!DNL AR Viewer] dans Adobe Commerce et des avantages de l’[!DNL AR Viewer] pour l’utilisateur, ainsi que des bonnes pratiques à suivre dans ce parcours.

Développé par Pixar, [Universal Scene Description (USD)](https://openusd.org/release/index.html){target=_blank} est le premier logiciel open source qui peut interchanger de manière robuste et évolutive des scènes 3D qui peuvent être composées de nombreuses ressources, sources et animations différentes, tout en favorisant des workflows hautement collaboratifs. Cet USD est utilisé dans les fichiers `.USDZ`. Ce fichier `.USDZ` diffuse du contenu AR et 3D sur les appareils de l’utilisateur.

>[!NOTE]
>
> Le [!DNL AR Viewer] ne prend en charge que les fichiers `.USDZ`.

## [!DNL AR Viewer] requises

Le [!DNL AR Viewer] est compatible avec [!DNL Magento Open Source] et Adobe Commerce. Consultez [Politique de cycle de vie](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html?lang=fr){target=_blank} pour plus d’informations sur les versions prises en charge.

Voir [Installer l’extension [!DNL AR Viewer]  pour plus d’informations](../catalog/ar-viewer-setup.md).

Pour utiliser [!DNL AR Viewer], les éléments suivants doivent être disponibles pour votre instance :

* PHP 8.1.0
* Adobe Commerce version 2.4.4 et ultérieure
* Magento Open Source (CE) version 2.4.x

## Limites de compatibilité

[!DNL AR Viewer] limites de compatibilité existantes :

* `.USDZ` uniquement : cette fonctionnalité ne prend en charge que les fichiers `.USDZ`.
* `qr-code` : nécessite `endroid/qr-code` version 4.5.
* `Catalog module` : nécessite `magento/module-catalog` version 104.0.0.
