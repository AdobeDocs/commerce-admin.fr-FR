---
title: Configurer la rotation du journal
description: Configurez la rotation de journal pour l’intégration AEM Assets pour Commerce.
feature: CMS, Media, Integration
exl-id: f735d086-048c-4555-bc58-ac6736c281b0
source-git-commit: c71fd243d809e2b86c5c8e781d527892965838ae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Configuration de Experience Manager Assets

L’intégration AEM Assets pour Commerce fournit les fichiers journaux suivants dans votre instance Commerce :

- `/var/log/aem-assets-integration.log`
- `/var/log/aem-assets-integration-errors.log`

Demandez à votre administrateur système de vérifier le planning de rotation des fichiers journaux pour ces journaux afin d’éviter qu’ils ne deviennent trop volumineux. Dans certains environnements, les fichiers journaux subissent une rotation automatique, mais dans d’autres, vous devez configurer manuellement la rotation des journaux. Pour plus d’informations, consultez les rubriques suivantes :

- Pour les installations sur site d’Adobe Commerce, demandez à votre administrateur système de configurer la [rotation des journaux](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html#server-settings).
- Pour les projets d’infrastructure cloud d’Adobe Commerce, voir [Afficher et gérer les journaux](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/test/log-locations.html).
