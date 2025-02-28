---
title: Activer la synchronisation des ressources
description: Découvrez comment connecter vos projets Adobe Commerce et Experience Manager Assets pour activer la synchronisation des ressources entre ces deux systèmes.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: d8e255259e4a8b87c63a4d1c013b4c1feb2b29cb
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 0%

---

# Activer la synchronisation des ressources

Activez la synchronisation des ressources en mettant à jour la configuration de l’environnement Commerce pour connecter Commerce à l’instance AEM Assets. L’intégration permet la synchronisation des ressources entre Commerce et AEM Assets, en veillant à ce que les images du produit et les autres ressources soient toujours à jour.

Après avoir identifié le projet de ressources AEM, sélectionnez la règle correspondante pour synchroniser les ressources entre Adobe Commerce et AEM Assets.

- **[!UICONTROL Match by product SKU]** : règle par défaut qui associe le SKU dans les métadonnées de ressource au [SKU de produit Commerce](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/glossary#sku) pour s’assurer que les ressources sont associées aux produits appropriés.

- **[!UICONTROL Custom match]** : règle de correspondance pour les scénarios plus complexes ou pour les besoins spécifiques de l&#39;entreprise qui nécessitent une logique de correspondance personnalisée. L’implémentation d’une correspondance personnalisée nécessite le développement d’un code personnalisé dans Adobe Developer App Builder pour définir la manière dont les ressources sont associées aux produits. Plus de détails bientôt disponibles...

Pour l’intégration initiale, utilisez la règle par défaut *Correspondre par SKU de produit*.

## Conditions préalables

- [Configuration d’AEM Assets pour gérer les ressources Commerce](aem-assets-configure-aem.md)

- [Installez et configurez l’intégration AEM Assets pour Commerce](aem-assets-configure-commerce.md) pour ajouter l’extension et générer les informations d’identification et les connexions requises pour utiliser l’extension.

- Créez un ticket d’assistance pour demander l’activation de l’intégration AEM Assets. Vous devez fournir les **[!UICONTROL Program ID]**, **[!UICONTROL Environment ID]** et **[!UICONTROL IMS Org ID]** pour l’environnement de création AEM Assets auquel vous souhaitez vous connecter à Commerce.

  >[!TIP]
  >
  > (Facultatif) Fournissez l’**[!UICONTROL Asset Selector IMS Client ID]** si elle est disponible. Voir [ImsAuthProps](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/asset-selector-integration/integrate-asset-selector-adobe-app) dans la documentation du *sélecteur AEM Assets*.

## Configurer la connexion

1. Obtenez l’identifiant de projet et d’environnement [AEM Assets Authoring Environment](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start).

   1. Ouvrez la console AEM Sites et sélectionnez **[!UICONTROL Assets]**.

   1. Copiez et enregistrez les identifiants de projet et d’environnement à partir de l’URL <br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`
1. Ouvrez la configuration de l’intégration AEM Assets à partir de l’Administration Commerce.

   1. Accédez à **[!UICONTROL Store]** > Configuration > **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]**.

      ![L’intégration AEM Assets active l’intégration](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. Saisissez les **[!UICONTROL Program ID]** et **[!UICONTROL Environment ID]** de l’environnement AEM Assets.

   Modifiez les valeurs de configuration en supprimant la sélection de *[!UICONTROL Use system value]*.

1. Saisissez le **[!UICONTROL Asset Selector IMS Client ID]**, le cas échéant.

   L’[identifiant du client IMS du sélecteur de ressources](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/asset-selector-integration/integrate-asset-selector-adobe-app#ims-auth-props) est requis par la [!UICONTROL Assets Selector], une fonctionnalité d’AEM Assets qui permet aux utilisateurs d’incorporer des ressources visuelles directement dans les pages de produits Commerce.

1. Sélectionnez les [[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment) permettant d’authentifier les requêtes entre Commerce et le service de correspondance des ressources.

1. Définissez **[!UICONTROL Integration enabled]** sur `Yes` pour permettre à Commerce d’accepter les mises à jour entrantes en provenance d’AEM Assets.

   Après avoir activé l’intégration, des options de configuration supplémentaires sont disponibles pour spécifier les critères de correspondance des ressources.

1. Définir la règle de correspondance pour la synchronisation des ressources.

   1. Sélectionnez **[!UICONTROL Match by product SKU]** ou **[!UICONTROL Custom match (Requires App Builder)]**.

   1. Ajoutez le [nom du champ de métadonnées AEM Assets](aem-assets-configure-aem.md#configure-metadata) défini pour les SKU de produit Commerce dans le champ **[!UICONTROL Match by product SKU attribute name]** , `commerce:skus` exemple.

1. Sélectionnez **[!UICONTROL Save Config]** pour appliquer des mises à jour et lancer la synchronisation des ressources.

   La mise à jour de la configuration déclenche le processus de synchronisation initial, ce qui permet à Commerce d’accepter les mises à jour entrantes en provenance d’AEM Assets. Le temps nécessaire à la synchronisation dépend du volume de ressources et de configurations spécifiques. L’intégration tire parti de processus automatisés afin de réduire le temps nécessaire à la synchronisation.

## Étape suivante

[Utilisation d’AEM Assets avec Commerce](aem-assets-manage.md)
