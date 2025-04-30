---
title: Configuration de l’intégration
description: Découvrez comment connecter vos projets Adobe Commerce et Experience Manager Assets pour activer la synchronisation des ressources entre ces deux systèmes.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: f01ba239d885d96285186e35361a8d40f2f68e4e
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# Configuration de l’intégration

Configurez l’intégration en connectant Commerce à l’instance AEM Assets et en sélectionnant la stratégie correspondante pour la synchronisation des ressources.

Après avoir identifié le projet AEM Assets, sélectionnez la règle correspondante pour synchroniser les ressources entre Adobe Commerce et AEM Assets.

- **[!UICONTROL Match by product SKU]** : règle par défaut qui associe le SKU dans les métadonnées de ressource au [SKU de produit Commerce](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/glossary#sku) pour s’assurer que les ressources sont associées aux produits appropriés.

- **[!UICONTROL Custom match]** : règle de correspondance pour les scénarios plus complexes ou pour les besoins spécifiques de l&#39;entreprise qui nécessitent une logique de correspondance personnalisée. L’implémentation d’une correspondance personnalisée nécessite le développement d’un code personnalisé dans Adobe Developer App Builder pour définir la manière dont les ressources sont associées aux produits. Plus de détails bientôt disponibles...

Pour la configuration initiale, utilisez la règle par défaut *Correspondance par sku de produit*.

## Conditions préalables

- [Installation du package AEM Assets](aem-assets-configure-aem.md)

- [Installez les packages Adobe Commerce](aem-assets-configure-commerce.md) pour ajouter l’extension et générer les informations d’identification et les connexions requises pour utiliser l’extension.

- Créez un ticket d’assistance pour demander l’activation de l’intégration AEM Assets for Commerce. Dans le ticket, incluez les **[!UICONTROL Program ID]**, **[!UICONTROL Environment ID]** et **[!UICONTROL IMS Org ID]** de l’environnement de création AEM Assets auquel vous souhaitez vous connecter à Commerce.

- Fournissez les **[!UICONTROL Asset Selector IMS Client ID]**. Voir [ImsAuthProps](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/asset-selector-integration/integrate-asset-selector-adobe-app) dans la documentation du *sélecteur AEM Assets*.

## Configurer la connexion

1. Obtenez l’identifiant de projet et d’environnement [AEM Assets Authoring Environment](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start).

   1. Ouvrez la console AEM Sites et sélectionnez **[!UICONTROL Assets]**.

   1. Copiez et enregistrez les identifiants de projet et d’environnement à partir de l’URL <br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`
1. Ouvrez la configuration de l’intégration AEM Assets à partir de l’Administration Commerce.

   1. Accédez à **[!UICONTROL Store]** > Configuration > **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]**.

      ![L’intégration AEM Assets active l’intégration](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. Saisissez les **[!UICONTROL Program ID]** et **[!UICONTROL Environment ID]** de l’environnement AEM Assets.

   Modifiez les valeurs de configuration en supprimant la sélection de *[!UICONTROL Use system value]*.

1. Saisissez le **[!UICONTROL Asset Selector IMS Client ID]**.

   L’[identifiant du client IMS du sélecteur de ressources](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/asset-selector-integration/integrate-asset-selector-adobe-app#ims-auth-props) est requis par la [!UICONTROL Assets Selector], une fonctionnalité d’AEM Assets qui permet aux utilisateurs d’incorporer des ressources visuelles directement dans les pages de produits Commerce.

1. Sélectionnez les [[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment) permettant d’authentifier les requêtes entre Commerce et le service de correspondance des ressources.

1. Définissez **[!UICONTROL Integration enabled]** sur `Yes` pour permettre à Commerce d’accepter les mises à jour entrantes en provenance d’AEM Assets.

   Après avoir activé l’intégration, des options de configuration supplémentaires sont disponibles pour spécifier les critères de correspondance des ressources.

1. Définir la règle de correspondance pour la synchronisation des ressources.

   1. Sélectionnez **[!UICONTROL Match by product SKU]** ou **[!UICONTROL Custom match (Requires App Builder)]**.

   1. Ajoutez le [nom du champ de métadonnées AEM Assets](aem-assets-configure-aem.md#configure-metadata) défini pour les SKU de produit Commerce dans le champ **[!UICONTROL Match by product SKU attribute name]** , `commerce:skus` exemple.

1. Sélectionnez **[!UICONTROL Save Config]** pour appliquer des mises à jour et lancer la synchronisation des ressources.

   La mise à jour de la configuration déclenche le processus de synchronisation initial, ce qui permet à Commerce d’accepter les mises à jour entrantes provenant d’AEM Assets. Le temps nécessaire à la synchronisation dépend du volume de ressources et de configurations spécifiques. L’intégration tire parti de processus automatisés afin de réduire le temps nécessaire à la synchronisation.

### Configuration de l’URL du domaine personnalisé

Si un commerçant définit un [Nom de domaine personnalisé](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/custom-domain-names/add-custom-domain-name){target=_blank} dans son tableau de bord AEM, il est nécessaire d’ajouter cette **URL de domaine personnalisé** dans Commerce, afin que l’intégration AEM Assets puisse l’utiliser.

1. Accédez à **[!UICONTROL Store]** > Configuration > **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]**.

   ![L’intégration AEM Assets active l’intégration](assets/aem-assets-view.png){width="600" zoomable="yes"}

1. Ajoutez l’**URL de domaine personnalisé** au champ **[!UICONTROL Asset Custom Domain]** .

1. Cliquez sur **[!UICONTROL Save Config]** pour appliquer les mises à jour et lancer la synchronisation des ressources.

## Étape suivante

[Utilisation d’AEM Assets avec Commerce](aem-assets-manage.md)
