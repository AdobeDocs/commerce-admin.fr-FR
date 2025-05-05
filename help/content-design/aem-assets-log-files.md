---
title: Configurer la rotation du journal
description: Configurez la rotation de journal pour l’intégration AEM Assets pour Commerce.
feature: CMS, Media, Integration
source-git-commit: 9e1f80d24eed078b5b28ae2d102c3f3df457081d
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# Configuration de Experience Manager Assets

L’intégration AEM Assets pour Commerce fournit les fichiers journaux suivants :

- `/var/log/aem-assets-integration.log`
- `/var/log/aem-assets-integration-errors.log`

Demandez à votre administrateur système de vérifier le planning de rotation des fichiers journaux pour ces journaux afin d’éviter qu’ils ne deviennent trop volumineux. Dans certains environnements, les fichiers journaux subissent une rotation automatique, mais dans d’autres, vous devez configurer manuellement la rotation des journaux. Pour plus d’informations, consultez les rubriques suivantes :

- Pour les installations sur site d’Adobe Commerce, demandez à votre administrateur système de configurer la [rotation des journaux](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html?lang=fr#server-settings).
- Pour les projets d’infrastructure cloud d’Adobe Commerce, voir [Afficher et gérer les journaux](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/test/log-locations.html?lang=fr).


