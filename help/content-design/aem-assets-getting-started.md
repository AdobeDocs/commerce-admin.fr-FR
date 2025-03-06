---
title: Configuration de l’intégration d’AEM Assets pour Commerce
description: Découvrez comment configurer votre environnement Experience Manager Assets afin de gérer les ressources Commerce pour votre boutique.
feature: CMS, Media, Configuration
exl-id: 699f517e-1545-4c22-aa8d-9c8d60d352af
source-git-commit: 98c40c779e1fe705cf1bd47331537bc7b7235921
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---

# Configuration de l’intégration d’AEM Assets pour Commerce

L’installation de l’intégration Adobe Experience Manager Assets pour Commerce nécessite un accès administratif pour personnaliser la configuration de l’application et de l’environnement.

- Accès administratif au programme Cloud Manager dans lequel les environnements AEM Assets as a Cloud Service sont configurés.

- Accès administratif à l’environnement Adobe Commerce et possibilité de récupérer ou de générer les clés API requises pour l’authentification.

## Conditions requises pour utiliser l’intégration

Pour tirer parti de cette intégration, les entreprises doivent répondre aux exigences suivantes :

- Licences actives pour Adobe Commerce, Adobe Experience Manager Assets et [AEM Dynamic Media](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/administering-dynamic-media).

- Adobe Commerce 2.4.5+

   - PHP 8.1, 8.2, 8.3
   - Compositeur : 2.x

- Adobe Experience Manager est configuré avec [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/assets/overview)

- L’utilisateur d’Adobe Commerce qui configure l’intégration doit avoir accès à l’organisation [IMS](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) où le projet AEM Assets est configuré.

## Principaux avantages

- **Pas de frais supplémentaires** - Cette intégration est fournie gratuitement pour les commerçants qui répondent aux exigences de licence.

- **Solution Adobe officielle** : développée, conservée et entièrement prise en charge par Adobe, assurant la stabilité et l’alignement avec les améliorations futures de la plateforme.

- **Modèle d’assistance gérée par Adobe**—Adobe gère l’assistance et le dépannage, offrant ainsi une tranquillité d’esprit et une résolution rationalisée des problèmes.

## Étapes suivantes

L’activation de l’intégration de Commerce à Experience Manager Assets est un processus en trois étapes :

1. [Installez le package AEM Assets](aem-assets-configure-aem.md).

1. [Installation des packages Adobe Commerce](aem-assets-configure-aem.md).

1. [Configurez la ressource d’intégration](aem-assets-setup-synchronization.md).
