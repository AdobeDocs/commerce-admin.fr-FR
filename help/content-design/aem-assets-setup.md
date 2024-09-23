---
title: Configuration de l’intégration AEM Assets
description: Découvrez les exigences et les étapes de configuration de l’intégration entre Adobe Commerce et AEM Assets as a Cloud Service.
feature: CMS, Media, Configuration, Integration
source-git-commit: df21ea9a797a4f11d0104cf34134ced3bbabbdf4
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---


# Configuration de l’intégration AEM Assets

Activez les fonctionnalités avancées de gestion des ressources en configurant votre environnement AEM Assets et en installant et en configurant l’intégration d’AEM Assets pour Commerce.

Lorsque l’intégration est active, les administrateurs peuvent utiliser Experience Manager Assets as a Cloud Service comme source unique de vérité pour la création et la gestion des ressources, et comme outil central de gestion des ressources numériques (DAM) pour créer, gérer, organiser et distribuer des ressources pour les projets Commerce.

## Conditions

- Adobe Commerce 2.4.5+
   - PHP 8.1, 8.2, 8.3
   - Compositeur : 2.x
- Adobe Experience Manager est fourni avec [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/assets/overview)
- L’utilisateur Adobe Commerce configurant l’intégration doit avoir accès à l’ [organisation IMS](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) où le projet AEM Assets est configuré.

## Configuration de l’intégration

>[!BEGINSHADEBOX]

**Conditions préalables**

La configuration de l’intégration AEM Assets requiert un accès administratif pour personnaliser la configuration de l’application et de l’environnement.

- Accès administratif au programme Cloud Manager dans lequel les environnements as a Cloud Service AEM Assets sont configurés.
- Accès administratif à l’environnement Adobe Commerce et possibilité de récupérer ou de générer les clés API requises pour l’authentification.

>[!ENDSHADEBOX]

L’activation de l’intégration Commerce avec Experience Manager Assets est un processus en trois étapes :

1. [Configurez votre projet Experience Manager Assets pour gérer les ressources Commerce](aem-assets-configure-aem.md).

1. [Installez l’extension Experience Manager Assets Integration et configurez Adobe Commerce](aem-assets-configure-aem.md).

1. [Activer la synchronisation des ressources](aem-assets-setup-synchronization.md).
