---
title: Activer la synchronisation des ressources
description: Découvrez comment connecter vos projets Adobe Commerce et Experience Manager Assets pour activer la synchronisation des ressources entre ces deux systèmes.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: e9b3ede8945de0a6ed0cdb02e5675d736764d3e4
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# Activer la synchronisation des ressources

Pendant le processus d’activation, vous enregistrez l’identifiant client pour le projet à l’aide du programme et de l’identifiant d’environnement pour votre environnement de création AEM. Ces identifiants identifient le projet AEM Assets auquel vous vous connectez et fournissent les informations d’identification pour permettre la communication entre les environnements Commerce et AEM Assets.

Après avoir identifié le projet de ressources AEM, sélectionnez la règle correspondante pour synchroniser les ressources entre Adobe Commerce et AEM Assets.

- **[!UICONTROL Match by product SKU]** : règle par défaut qui associe le SKU dans les métadonnées de ressource au [SKU de produit Commerce](https://experienceleague.adobe.com/en/docs/commerce-operations/operational-playbook/glossary#sku) pour s’assurer que les ressources sont associées aux produits appropriés.

- **[!UICONTROL Custom match]** : règle de correspondance pour les scénarios plus complexes ou pour les besoins spécifiques de l&#39;entreprise qui nécessitent une logique de correspondance personnalisée. L’implémentation d’une correspondance personnalisée nécessite le développement d’un code personnalisé dans Adobe Developer App Builder pour définir la manière dont les ressources sont associées aux produits. Plus de détails bientôt disponibles...

Pour l’intégration initiale, utilisez la règle par défaut *Correspondre par SKU de produit*.

## Conditions préalables

- [Configuration d’AEM Experience Manager Assets pour gérer les ressources Commerce](#aem-assets-configure-aem)

- [Installez et configurez l’intégration AEM Assets pour Commerce](#aem-assets-configure-commerce.md) pour ajouter l’extension et générer les informations d’identification et les connexions requises pour utiliser l’extension.

- Créez un ticket d’assistance pour demander l’activation de l’intégration AEM Assets. Vous devez fournir les **[!UICONTROL Program ID]**, **[!UICONTROL Environment ID]** et **[!UICONTROL IMS Org ID]**.

  >[!TIP]
  >
  > (Facultatif) Fournissez l’**[!UICONTROL Asset Selector IMS Client ID]** si elle est disponible.

## Configurer la connexion

1. Obtenez l’identifiant de projet et d’environnement [AEM Assets Authoring Environment](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start).

   1. Ouvrez la console AEM Sites et sélectionnez **[!UICONTROL Assets]**.

   1. Copiez et enregistrez les identifiants de projet et d’environnement à partir de l’URL <br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`|.

1. Ouvrez la configuration de l’intégration AEM Assets à partir de l’Administration Commerce.

   1. Accédez à **[!UICONTROL Store]** > Configuration > **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]**.

      ![L’intégration AEM Assets active l’intégration](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. Saisissez les **[!UICONTROL Program ID]** et **[!UICONTROL Environment ID]** de l’environnement AEM Assets.

1. Saisissez la **[!UICONTROL Asset Selector IMS Client ID]** si elle est disponible.

   L’[ID IMS](../getting-started/adobe-ims-config.md) est requis par la [[!UICONTROL Assets Selector]](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/overview-asset-selector) qui sélectionne des images pour les catégories et/ou les [!DNL Page Builder].

1. Sélectionnez les [[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment) permettant d’authentifier les requêtes entre Commerce et le service de correspondance des ressources.

1. Autorisez Commerce à accepter les mises à jour entrantes en provenance d’AEM Assets en définissant **[!UICONTROL Integration enabled]** sur `Yes`.

   Après avoir activé l’intégration, configurez la règle de correspondance des ressources.

   ![Règle de correspondance de ressource sélectionnée pour l’intégration d’AEM Assets](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Définir la règle de correspondance pour la synchronisation des ressources.

   1. Sélectionnez **[!UICONTROL Match by product SKU]**.

   1. Ajoutez le [nom du champ de métadonnées AEM Assets](aem-assets-configure-aem.md#configure-metadata) défini pour les SKU de produit Commerce dans le champ **[!UICONTROL Match by product SKU attribute name]** , `commerce:skus` exemple.

   ![Règle de correspondance de ressource sélectionnée pour l’intégration d’AEM Assets](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Sélectionnez **[!UICONTROL Save Config]** pour appliquer des mises à jour et lancer la synchronisation des ressources
