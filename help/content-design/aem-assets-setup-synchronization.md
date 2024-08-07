---
title: Activation de la synchronisation des ressources
description: Découvrez comment connecter vos projets Adobe Commerce et Experience Manager Assets pour activer la synchronisation des ressources entre ces deux systèmes.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: 508e9e1d23a4b6e70ada22e2a22c0dcd401393a9
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Activation de la synchronisation des ressources

>[!BEGINSHADEBOX]

**Conditions préalables**

- [Configuration d’AEM Experience Manager Assets pour gérer les ressources Commerce](#aem-assets-configure-aem)
- [Installez et configurez l’intégration AEM Assets pour Commerce](#aem-assets-configure-commerce.md) pour ajouter l’extension et générer les informations d’identification et les connexions requises pour utiliser l’extension.

>[!ENDSHADEBOX]

Au cours de ce processus d’activation, vous enregistrez votre ID de client en fournissant l’ID de programme et d’environnement pour votre environnement de création AEM. Ces identifiants identifient le projet AEM Assets auquel vous vous connectez et fournissent les informations d’identification pour activer la communication et les workflows entre Commerce et AEM Assets.

Après avoir identifié le projet AEM ressources, vous sélectionnez la règle correspondante à utiliser pour synchroniser les ressources entre Adobe Commerce et AEM Assets.

L’intégration AEM Assets pour Commerce prend en charge deux règles correspondantes pour synchroniser des ressources entre Adobe Commerce et AEM Assets.

- **Correspondance par SKU du produit** : il s’agit de la règle de correspondance par défaut qui correspond aux ressources en fonction de l’unité de gestion des stocks (SKU) du produit. Le SKU est un identifiant unique pour chaque produit. Cette règle correspond au SKU des métadonnées de la ressource avec le SKU du produit Commerce pour s’assurer que les ressources sont associées aux produits appropriés.

- **Correspondance personnalisée** : cette règle de correspondance est destinée à des scénarios plus complexes ou à des besoins spécifiques qui nécessitent une logique de correspondance personnalisée. Pour utiliser cette règle, un code personnalisé doit être implémenté dans Adobe Developer App Builder afin de définir la manière dont les ressources sont mises en correspondance avec les produits. Plus de détails bientôt...

Pour l’intégration initiale, utilisez la règle `Match by product sku` par défaut. Si nécessaire, vous pouvez modifier la règle correspondante ultérieurement.

## Activation de l’intégration

1. Obtenez l’ID de projet et d’environnement pour votre [environnement de création AEM Assets](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start).

   1. Ouvrez la console AEM Sites et sélectionnez **[!UICONTROL Assets]**.

   1. Copiez et enregistrez les ID de projet et d’environnement à partir de l’URL :<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`|

1. Depuis l’administrateur Commerce, ouvrez la configuration Intégration AEM Assets .

   1. Sélectionnez **[!UICONTROL Store]** > Configuration > **[!UICONTROL CATALOG]** > **[!UICONTROL Catalog]**.

   1. Développez **[!UICONTROL Experience Manager Assets integration]**.

      ![L’intégration AEM Assets active l’intégration](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. Identifiez le projet Experience Manager Assets auquel se connecter en entrant les **[!UICONTROL Program ID]** et **[!UICONTROL Environment ID]**.

1. Ajoutez les informations d’identification OAUTH pour authentifier les demandes d’API entre Adobe Commerce et le service ARES en sélectionnant **[[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment)**, par exemple `Assets integration`.

1. Autoriser Commerce à accepter les mises à jour entrantes d’AEM Assets en définissant **[!UICONTROL Enable integration]** sur `Yes`.

   Après avoir activé l’intégration, vous pouvez configurer la règle de correspondance des ressources.

   ![AEM Assets Integration select asset match rule](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Définissez la règle correspondante pour la synchronisation des ressources.

   1. Sélectionnez **[!UICONTROL Match by product SKU]**.

   1. Ajoutez le [nom du champ de métadonnées AEM Assets](aem-assets-configure-aem.md#configure-metadata) défini pour les SKU de produit Commerce dans le champ **[!UICONTROL Match by product SKU attribute name]**, `commerce:skus` par exemple.

1. Appliquez la configuration et lancez le processus de synchronisation en sélectionnant **[!UICONTROL Save Config]**.
