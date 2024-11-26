---
title: Activation de la synchronisation des ressources
description: Découvrez comment connecter vos projets Adobe Commerce et Experience Manager Assets pour activer la synchronisation des ressources entre ces deux systèmes.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: e069f0a99ed9289b22cafe06fe2f787912cbba23
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# Activation de la synchronisation des ressources

Au cours du processus d’activation, vous enregistrez l’identifiant du client pour le projet à l’aide de l’identifiant de programme et d’environnement pour votre environnement de création AEM. Ces identifiants identifient le projet AEM Assets auquel vous vous connectez et fournissent les informations d’identification pour permettre la communication entre les environnements Commerce et AEM Assets.

Après avoir identifié le projet AEM ressources, vous sélectionnez la règle correspondante pour synchroniser les ressources entre Adobe Commerce et AEM Assets.

- **[!UICONTROL Match by product SKU]** : règle par défaut qui correspond au SKU des métadonnées de la ressource avec le [SKU du produit Commerce](https://experienceleague.adobe.com/en/docs/commerce-operations/operational-playbook/glossary#sku) pour s’assurer que les ressources sont associées aux produits appropriés.

- **[!UICONTROL Custom match]** : règle correspondante pour les scénarios plus complexes ou les besoins spécifiques de l’entreprise qui nécessitent une logique de correspondance personnalisée. La mise en oeuvre de la correspondance personnalisée nécessite le développement de code personnalisé dans Adobe Developer App Builder pour définir la manière dont les ressources sont mises en correspondance avec les produits. Plus de détails bientôt...

Pour l’intégration initiale, utilisez la règle par défaut *Correspondance par SKU* du produit.

## Conditions préalables

- [Configuration d’AEM Experience Manager Assets pour gérer les ressources Commerce](#aem-assets-configure-aem)
- [Installez et configurez l’intégration AEM Assets pour Commerce](#aem-assets-configure-commerce.md) pour ajouter l’extension et générer les informations d’identification et les connexions requises pour utiliser l’extension.

## Configuration de la connexion

1. Obtenez l’ID de projet et d’environnement [Environnement de création AEM Assets](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start).

   1. Ouvrez la console AEM Sites et sélectionnez **[!UICONTROL Assets]**.

   1. Copiez et enregistrez les ID de projet et d’environnement à partir de l’URL :<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`|

1. Depuis l’administrateur Commerce, ouvrez la configuration Intégration AEM Assets .

   1. Accédez à **[!UICONTROL Store]** > Configuration > **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]**.

      ![L’intégration AEM Assets active l’intégration](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. Renseignez les environnements AEM Assets **[!UICONTROL Program ID]** et **[!UICONTROL Environment ID]**.

1. Saisissez le **[!UICONTROL Asset Selector IMS Client ID].

   L’ [identifiant IMS](../getting-started/adobe-ims-config.md) vous permet d’intégrer AEM Assets au générateur de pages.

1. Sélectionnez le [[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment)** pour authentifier les demandes entre Commerce et le service de correspondance de ressources.

1. Autoriser Commerce à accepter les mises à jour entrantes d’AEM Assets en définissant **[!UICONTROL Integration enabled]** sur `Yes`.

   Après avoir activé l’intégration, configurez la règle de correspondance des ressources.

   ![AEM Assets Integration select asset match rule](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Définissez la règle correspondante pour la synchronisation des ressources.

   1. Sélectionnez **[!UICONTROL Match by product SKU]**.

   1. Ajoutez le [nom du champ de métadonnées AEM Assets](aem-assets-configure-aem.md#configure-metadata) défini pour les SKU de produit Commerce dans le champ **[!UICONTROL Match by product SKU attribute name]**, `commerce:skus` par exemple.

   ![AEM Assets Integration select asset match rule](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Sélectionner **[!UICONTROL Save Config]** pour appliquer des mises à jour et lancer la synchronisation des ressources
