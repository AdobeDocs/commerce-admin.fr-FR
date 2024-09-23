---
title: Configuration de Experience Manager Assets
description: Ajoutez les métadonnées de ressource requises pour permettre à l’intégration AEM Assets pour Commerce de synchroniser les ressources entre les projets Adobe Commerce et Experience Manager Assets.
feature: CMS, Media, Integration
exl-id: deb7c12c-5951-4491-a2bc-542e993f1f84
source-git-commit: 8a150c79c2e15ce5bd2cb2037f94c94f90b7a1df
workflow-type: tm+mt
source-wordcount: '668'
ht-degree: 0%

---

# Configuration de Experience Manager Assets

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Préparez l’environnement AEM as a Cloud Service pour gérer les ressources Commerce en mettant à jour la configuration de l’environnement et en configurant les métadonnées Assets pour identifier et gérer les ressources Commerce.

L’intégration requiert l’ajout d’un espace de noms `Commerce` personnalisé et de [métadonnées de profil](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-profiles) et [métadonnées de schéma](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-schemas) supplémentaires.

Adobe fournit un modèle de projet AEM pour ajouter les ressources de schéma de métadonnées et d’espace de noms à la configuration de l’environnement as a Cloud Service AEM Assets. Le modèle ajoute :

- Un [espace de noms personnalisé](https://github.com/ankumalh/assets-commerce/blob/main/ui.config/jcr_root/apps/commerce/config/org.apache.sling.jcr.repoinit.RepositoryInitializer~commerce-namespaces.cfg.json), `Commerce` pour identifier les propriétés liées à Commerce.

- Un type de métadonnées personnalisé `commerce:isCommerce` avec le libellé `Does it exist in Commerce?` pour baliser les ressources Commerce associées à un projet Adobe Commerce.

- Un type de métadonnées personnalisé `commerce:productmetadata` et un composant d’IU correspondant pour ajouter une propriété *[!UICONTROL Product Data]*. Les données de produit incluent les propriétés de métadonnées pour associer une ressource Commerce aux SKU du produit et pour spécifier les attributs image `role` et `position` de la ressource.

  ![Contrôle personnalisé de l’interface utilisateur des données de produit](./assets/aem-commerce-sku-metadata-fields-from-template.png){width="600" zoomable="yes"}

- Un formulaire de schéma de métadonnées avec un onglet Commerce qui comprend les champs `Does it exist in Adobe Commerce?` et `Product Data` pour baliser les ressources Commerce. Le formulaire fournit également des options pour afficher ou masquer les champs `roles` et `order` (position) de l’interface utilisateur d’AEM Assets.

  ![Onglet Commerce pour le formulaire de schéma de métadonnées AEM Assets](./assets/assets-configure-metadata-schema-form-editor.png){width="600" zoomable="yes"}

- [ exemple de ressource Commerce balisée et approuvée ](https://github.com/ankumalh/assets-commerce/blob/main/ui.content/src/main/content/jcr_root/content/dam/wknd/en/activities/hiking/equipment_6.jpg/.content.xml) `equipment_6.jpg` pour prendre en charge la synchronisation initiale des ressources. Seules les ressources Commerce approuvées peuvent être synchronisées d’AEM Assets vers Adobe Commerce.

Pour plus d’informations sur le projet Commerce-Assets AEM, voir [Readme](https://github.com/ankumalh/assets-commerce).

## Personnalisation de la configuration de l’environnement AEM Assets

>[!BEGINSHADEBOX]

**Conditions préalables**

- [Accès au programme et aux environnements AEM Assets Cloud Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/onboarding/journey/cloud-manager#access-sysadmin-bo) avec les rôles Program et Deployment Manager.

- Un [environnement de développement AEM local](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview) et une familiarité avec le processus de développement local AEM.

- Découvrez [AEM structure de projet](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) et comment déployer des packages de contenu personnalisés à l’aide de Cloud Manager.

>[!ENDSHADEBOX]

### Déployer le projet Commerce-Assets AEM dans l’environnement de création AEM Assets

1. Dans Cloud Manager, créez des environnements de production et d’évaluation pour votre projet AEM Assets, si nécessaire.

1. Configurez un pipeline de déploiement, si nécessaire.

1. A partir de GitHub, téléchargez le code standard du [projet Commerce-Assets AEM](https://github.com/ankumalh/assets-commerce).

1. A partir de votre [environnement de développement AEM local](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview), installez le code personnalisé dans votre configuration d’environnement AEM Assets sous la forme d’un package Maven, ou en copiant manuellement le code dans la configuration de projet existante.

1. Validez les modifications et poussez votre branche de développement local dans le référentiel git de Cloud Manager.

1. À partir de Cloud Manager, [ déployez votre code pour mettre à jour l&#39;environnement AEM ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/deploy-code#deploying-code-with-cloud-manager).

## Configuration d’un profil de métadonnées

Définissez des valeurs par défaut pour les métadonnées de ressources Commerce en créant un profil de métadonnées. Une fois configuré, appliquez ce profil à AEM dossiers de ressources afin d’utiliser automatiquement ces valeurs par défaut. Cette configuration facultative permet de rationaliser le traitement des ressources en réduisant les étapes manuelles.

1. Dans l’espace de travail Adobe Experience Manager, accédez à l’espace de travail Auteur de l’administration du contenu pour AEM Assets en cliquant sur l’icône Adobe Experience Manager .

   ![Création AEM Assets](./assets/aem-assets-authoring.png){width="600" zoomable="yes"}

1. Ouvrez les outils de l’administrateur en sélectionnant l’icône en forme de marteau.

   ![AEM administrateur de création gérer les profils de métadonnées](./assets/aem-manage-metadata-profiles.png){width="600" zoomable="yes"}

1. Ouvrez la page de configuration du profil en cliquant sur **[!UICONTROL Metadata Profiles]**.

1. **[!UICONTROL Create]** : profil de métadonnées pour l’intégration de Commerce.

   ![AEM Administrateur d’auteur ajoutez des profils de métadonnées ](./assets/aem-create-metadata-profile.png){width="600" zoomable="yes"}

1. Ajoutez un onglet pour les métadonnées Commerce.

   1. Sur la gauche, cliquez sur **[!UICONTROL Settings]**.

   1. Cliquez sur **[!UICONTROL +]** dans la section des onglets, puis spécifiez les **[!UICONTROL Tab Name]**, `Commerce`.

1. Ajoutez le champ `Does it exist in Commerce?` au formulaire et définissez la valeur par défaut sur `yes`.

   ![AEM l’administrateur de l’auteur ajoute des champs de métadonnées au profil](./assets/aem-edit-metadata-profile-fields.png){width="600" zoomable="yes"}

1. Enregistrez la mise à jour.

1. Appliquez le profil de métadonnées `Commerce integration` au dossier dans lequel les ressources Commerce sont stockées.

   1. Sur la page [!UICONTROL  Metadata Profiles], sélectionnez le profil d’intégration Commerce.

   1. Dans le menu Action, sélectionnez **[!UICONTROL Apply Metadata Profiles to Folder(s)]**.

   1. Sélectionnez le dossier contenant les ressources Commerce.

      Créez un dossier Commerce s’il n’existe pas.

   1. Cliquez sur **[!UICONTROL Apply]**.

>[!TIP]
>
>Vous pouvez synchroniser automatiquement les ressources Commerce lors de leur chargement dans l’environnement AEM Assets en mettant à jour le profil de métadonnées afin de définir la valeur par défaut du champ _[!UICONTROL Review Status]_sur `Approved`. Le type de propriété du champ `Review Status` est `./jcr:content/metadata/dam:status`.


## Étapes suivantes

Après la mise à jour de l’environnement AEM, configurez Adobe Commerce :

1. [Installation et configuration de l’intégration AEM Assets pour Commerce](aem-assets-configure-commerce.md)
2. [Activation de la synchronisation des ressources pour le transfert de ressources entre l’environnement de projet Adobe Commerce et l’environnement de projet AEM Assets](aem-assets-setup-synchronization.md)
