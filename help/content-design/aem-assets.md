---
title: Intégration Experience Manager Assets pour Commerce
description: Découvrez comment intégrer Experience Manager Assets à votre instance  [!DNL Commerce] pour accéder à d’innombrables ressources multimédias à utiliser dans votre boutique.
feature: CMS, Media, Configuration, Integration
source-git-commit: 8588973f265c6bd3dfdd41e574f27f653cc9da0e
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# Intégration Experience Manager Assets pour Commerce

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

L’intégration entre Commerce et Adobe Experience Manager (AEM) Assets combine les puissantes fonctionnalités d’AEM as a Digital Asset Management (DAM) avec Adobe Commerce pour améliorer les expériences de commerce électronique. Cette intégration tire parti AEM puissantes fonctionnalités de gestion des ressources pour offrir un moyen transparent, évolutif et efficace de gérer et de diffuser des ressources sur les vitrines commerciales.

**Fonctionnalités clés**

- **Gestion centralisée des ressources**

   - **AEM Assets as a Single Source of Truth** - AEM Assets sert de référentiel central pour toutes les ressources numériques, en s’assurant que toutes les plateformes de commerce électronique ont accès à des ressources approuvées et de marque.

   - **Gestion des ressources en bloc** : grâce à l’AEM de puissantes fonctionnalités de gestion des ressources, les entreprises peuvent gérer efficacement d’importants volumes de ressources. Cela permet aux marketeurs et aux marchandiseurs de mapper efficacement de grands ensembles d’images pour de nouvelles lignes de produits.

- **Expériences Commerce personnalisées** - À l’aide des services GenAI dans AEM, les entreprises peuvent générer des millions de variations de produits pour les expériences de commerce électronique personnalisées. Les marketeurs et les marchandiseurs peuvent utiliser ces images pour créer des vitrines dynamiques pour les lancements de produits et les campagnes saisonnières, ce qui améliore l’engagement et améliore les taux de conversion.

- **Correspondance automatisée de ressources** : l’intégration comprend un service de moteur de règles qui associe automatiquement les ressources d’ AEM aux produits dans Adobe Commerce en fonction de SKU ou d’autres attributs clés. Le service garantit que les dernières ressources et variations de produit sont toujours disponibles sur les vitrines de commerce électronique. Elle réduit également l’effort manuel requis pour gérer les ressources, ce qui permet de gagner du temps pour des activités plus stratégiques.

- **Processus rationalisés**
   - **Activez et configurez l’intégration à partir de l’administrateur Commerce**. Les administrateurs et les développeurs peuvent installer et configurer l’intégration à partir d’Adobe Commerce à l’aide d’outils et de processus familiers.
   - **Mises à jour dynamiques** - Tenez les images du produit à jour avec les dernières modifications apportées au système de gestion des ressources. Ces mises à jour automatisées garantissent que les vitrines commerciales disposent toujours des informations sur les produits les plus récentes.
   - **Gestion efficace du catalogue** : simplifie la maintenance du catalogue de produits en automatisant le nettoyage et l’actualisation des ressources.

## Intégration de Commerce et Experience Manager Assets

>[!BEGINSHADEBOX]

**Conditions préalables**

- Adobe Commerce doit être configuré avec l’ [intégration de Commerce Admin avec Adobe ID](/help/getting-started/adobe-ims-config.md) avec un ID d’organisation attribué.
- Experience Manager Assets doit être affecté en tant que produit au même ID d’organisation.
- L’utilisateur configurant l’intégration doit disposer d’un compte dans la même organisation avec les droits d’administration pour accéder à Adobe Commerce et Experience Manager Assets.

>[!ENDSHADEBOX]

Activation de l’intégration de Commerce avec Experience Manager Assets en procédant comme suit :

1. [Configuration de votre projet Experience Manager Assets pour gérer des ressources Commerce](aem-assets-configure-aem.md)

1. [Installation de l’extension Experience Manager Assets Integration et configuration d’Adobe Commerce](aem-assets-configure-commerce.md)

1. [Configuration des services de synchronisation](aem-assets-setup-synchronization.md)
