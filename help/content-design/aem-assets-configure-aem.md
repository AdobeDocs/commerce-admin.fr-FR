---
title: Configuration de Experience Manager Assets
description: Ajoutez les métadonnées de ressource requises pour permettre à l’intégration AEM Assets pour Commerce de synchroniser les ressources entre les projets Adobe Commerce et Experience Manager Assets.
feature: CMS, Media, Integration
source-git-commit: d91ba86b77ef91e849d1737628b575f2309376b8
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# Configuration de Experience Manager Assets

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Pour gérer les ressources multimédias de votre magasin à l’aide de l’intégration AEM Assets pour Commerce, votre projet AEM Assets nécessite l’ajout de certaines métadonnées afin de vous assurer que vous pouvez facilement rechercher et gérer des ressources Commerce. Ces métadonnées facilitent également la synchronisation des ressources entre Adobe Commerce et Experience Manager Assets. Après avoir défini les champs de métadonnées, le mappage initial de ces champs se produit automatiquement la première fois qu’une ressource Commerce est partagée avec Experience Manager Assets.

Pour l’intégration, vous configurez deux types de métadonnées :

- **[Le ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-profiles)** permet d’appliquer des métadonnées par défaut aux ressources d’un dossier. Toutes les ressources du dossier héritent des métadonnées par défaut configurées dans le profil.

- **[Schéma de métadonnées](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-schemas)** définit la mise en page de la page des propriétés et l’ensemble des champs qui peuvent être utilisés comme propriétés de métadonnées sur une ressource AEM.

## Configuration des métadonnées

Pour l’intégration initiale, ajoutez les métadonnées Commerce suivantes à un profil de métadonnées AEM Assets et à un schéma de métadonnées.

| Type de champ | Libellé | Propriété | Valeur par défaut |
|------ | ------- | ---------- | ------------- |
| Texte | **Existe-t-il dans Adobe Commerce ?** | `./jcr:content/metadata/commerce:isCommerce` | oui |
| Texte à plusieurs valeurs | **SKU** | `./jcr:content/metadata/commerce:skus` | none |
| Texte à plusieurs valeurs | **Positions** | `./jcr:content/metadata/commerce:positions` | none |
| Texte à plusieurs valeurs | **Rôles** | `./jcr:content/metadata/commerce:roles` | none |


### Ajout de champs Commerce à un profil de métadonnées

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

1. Ajoutez les [champs de métadonnées](#configure-metadata) au formulaire.

   ![AEM l’administrateur de l’auteur ajoute des champs de métadonnées au profil](./assets/aem-edit-metadata-profile-fields.png){width="600" zoomable="yes"}

1. Enregistrez la mise à jour.

1. Appliquez le profil de métadonnées `Commerce integration` au dossier dans lequel les ressources Commerce sont stockées.

   1. Sur la page [!UICONTROL  Metadata Profiles], sélectionnez le profil d’intégration Commerce.

   1. Dans le menu Action, sélectionnez **[!UICONTROL Apply Metadata Profiles to Folder(s)]**.

   1. Sélectionnez le dossier contenant les ressources Commerce.

      Créez un dossier Commerce s’il n’existe pas.

   1. Cliquez sur **[!UICONTROL Apply]**.

### Ajout de champs Commerce à un formulaire de schéma de métadonnées

1. Dans le panneau d’administration du contenu de l’auteur AEM pour Assets, ouvrez **[!UICONTROL Metadata Schemas]** ([!UICONTROL Manage metadata schema forms]).

   ![AEM de l’administrateur de l’auteur de mettre à jour le schéma de métadonnées](./assets/aem-assets-manage-metadata-schema.png){width="600" zoomable="yes"}

1. **[!UICONTROL Create]** : schéma de métadonnées pour Commerce.

   ![AEM de l’administrateur de l’auteur de mettre à jour le schéma de métadonnées](./assets/aem-assets-create-metadata-schema.png){width="600" zoomable="yes"}

1. Sur le [!UICONTROL Metadata Schema Form], créez les champs `Does Commerce exist?` et `Commerce mappings` et mappez les propriétés.

1. Cliquez sur **[!UICONTROL Save]**.


## Publish d’une ressource

Après avoir configuré les métadonnées AEM et le profil de schéma pour les ressources Commerce, créez la première ressource Commerce à mapper les champs de métadonnées Commerce.

1. Depuis l’Experience Manager, accédez à [!UICONTROL Assets > Files] et sélectionnez le dossier **Commerce**.

1. Téléchargez une image pour un projet Commerce en faisant glisser le fichier vers le dossier ou en cliquant sur **[!UICONTROL Add Assets]**.

1. Vérifiez la configuration des métadonnées : **isCommerce** est défini sur `true` et que la propriété `commerce:skus` est définie sur le SKU du produit Commerce associé à l’image.

1. Approuvez la ressource.


## Ajout d’une ressource au dossier Commerce

Créez au moins une ressource dans le dossier Commerce AEM Assets à laquelle les attributs de métadonnées Commerce sont affectés.

Cette ressource est nécessaire pour configurer la synchronisation entre votre instance Commerce et AEM Assets.

## Mappage des métadonnées des ressources

Les métadonnées sont mises en correspondance lorsqu’une ressource Commerce est publiée pour la première fois.  de Commerce pour la première fois. Les ressources multimédia qui comportent des champs intégrés ou personnalisés sont automatiquement associées aux champs spécifiés lors de leur premier envoi à Experience Manager Assets.

Avant de commencer le mappage des ressources, effectuez les tâches suivantes :

- [Installation et configuration de l’intégration AEM Assets pour Commerce](aem-assets-configure-commerce.md)
- [Activation de la synchronisation des ressources pour le transfert de ressources entre l’environnement de projet Adobe Commerce et l’environnement de projet AEM Assets](aem-assets-setup-synchronization.md)
