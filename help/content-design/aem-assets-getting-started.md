---
title: Configuration de l’intégration d’AEM Assets pour Commerce
description: Découvrez comment configurer votre environnement Experience Manager Assets afin de gérer les ressources Commerce pour votre boutique.
feature: CMS, Media, Configuration
exl-id: 699f517e-1545-4c22-aa8d-9c8d60d352af
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
TQID: https://experienceleague.adobe.com/loyCmoFINQvC-13BGzAUKmcF7gY6T2e6mV-lK-SnVxo
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 42029ed6d13cd4203c4a5d8300297315aac1abf5
workflow-type: tm+mt
source-wordcount: 298
ht-degree: 3%

---

# Configuration de l’intégration d’AEM Assets pour Commerce

L’installation de l’intégration Adobe Experience Manager Assets pour Commerce nécessite un accès administratif pour personnaliser la configuration de l’application et de l’environnement.

- Accès administratif au programme Cloud Manager dans lequel les environnements AEM Assets as a Cloud Service sont configurés.

- Accès administratif à l’environnement Adobe Commerce et possibilité de récupérer ou de générer les clés API requises pour l’authentification.

## Conditions requises pour utiliser l’intégration

Pour tirer parti de cette intégration, les entreprises doivent répondre aux exigences suivantes :

- Licences actives pour Adobe Commerce, Adobe Experience Manager Assets et [AEM Dynamic Media](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/assets/dynamic/administering-dynamic-media).

- Adobe Commerce 2.4.5+

- Adobe Experience Manager est configuré avec [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/assets/overview)

- L’utilisateur d’Adobe Commerce qui configure l’intégration doit avoir accès à l’organisation [IMS](https://experienceleague.adobe.com/fr/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) où le projet AEM Assets est configuré.

## Principaux avantages

- **Pas de frais supplémentaires** - Cette intégration est fournie gratuitement pour les commerçants qui répondent aux exigences de licence.

- **Solution Adobe officielle** : développée, conservée et entièrement prise en charge par Adobe, assurant la stabilité et l’alignement avec les améliorations futures de la plateforme.

- **Modèle d’assistance gérée par Adobe**—Adobe gère l’assistance et le dépannage, offrant ainsi une tranquillité d’esprit et une résolution rationalisée des problèmes.

## Étapes suivantes

L’activation de l’intégration de Commerce à Experience Manager Assets est un processus en trois étapes :

1. [Installez le package AEM Assets](aem-assets-configure-aem.md).
1. [Installation des packages Adobe Commerce](aem-assets-configure-aem.md).
1. [Configurez la ressource d’intégration](aem-assets-setup-synchronization.md).
