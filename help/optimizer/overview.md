---
title: Présentation des services de marchandisage
description: Découvrez les outils de configuration de catalogue, de marchandisage, de création de rapports et de surveillance pour les instances Adobe Commerce as a Cloud Service configurées avec le CCDM.
recommendations: noCatalog
badgeSaas: label="SaaS uniquement" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique aux instances Adobe Commerce as a Cloud Service configurées avec le CCDM uniquement (infrastructure SaaS gérée par Adobe)."
exl-id: f9516d4c-fbae-4db2-a1a9-cda3684a8122
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: a6a5a899ba60097bd6baf2a5de14063a0af2f313
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%
---
# Présentation des services de marchandisage avec CCDM

Les instances Adobe Commerce as a Cloud Service configurées avec le modèle de données de catalogue composable (CCDM) fournissent des outils de configuration de catalogue, de marchandisage, de création de rapports et de surveillance dans l’[administration Commerce dans l’expérience unifiée Adobe](../getting-started/admin-unified-experience.md). Le CCDM est la même base de catalogue qui alimente Adobe Commerce Optimizer.

Grâce aux services de marchandisage, vous pouvez :

- Utilisez les données de catalogue de votre instance Adobe Commerce as a Cloud Service pour prendre en charge les expériences storefront.
- Configurez les vues et stratégies de catalogue pour définir des assortiments de produits storefront.
- Appliquez des règles de marchandisage à toutes les vues de catalogue ou adaptez-les à une vue spécifique.
- Configurez les recommandations de produits, les facettes de recherche et les synonymes.
- Examinez les performances du storefront grâce aux mesures de succès et aux rapports de performances de recherche.
- Surveillez la synchronisation des catalogues et les événements storefront capturés.

Commerce Foundation reste la source de vérité pour les produits et les prix et continue à gérer le panier, le passage en caisse et d’autres opérations transactionnelles.

## Aperçu rapide

>[!BEGINTABS]

>[!TAB Configuration du catalogue]

Configurez le contexte de catalogue disponible pour un storefront.

- **Vues de catalogue**—Combinez les sources de catalogue, les politiques et les livres de prix pour définir les produits et les prix qu&#39;un storefront peut récupérer. Voir [Vues du catalogue](./setup/catalog-view.md).
- **Calques de catalogue** : remplacez les attributs de produit sélectionnés sans modifier les données source. Lors de l’utilisation d’AEM Assets pour les images de produit, le calque AEM-Assets est appliqué au moyen des visuels de produit. Voir [Calques de catalogue](./setup/catalog-layer.md).
- **Vues de catalogue privé** : activez la protection du catalogue pour exiger un jeton signé valide lors de la récupération des données d’une vue du catalogue. Voir [Vues de catalogue privé](./setup/private-catalog-view.md).

>[!TAB Politiques]

Les politiques filtrent les produits disponibles par le biais d’une vue de catalogue en fonction des attributs de produit. Par exemple, une politique peut limiter un assortiment à une marque ou une catégorie de produits particulière.

Les politiques déterminent l’assortiment de produits disponible. Ils ne remplacent pas la protection du catalogue, qui contrôle l’accès à une vue de catalogue privée.

>[!TAB Marchandisage]

Configurez la manière dont les acheteurs découvrent des produits et dont les produits sont promus dans l’assortiment disponible.

- **Opportunités** : passez en revue les performances des produits, le comportement des acheteurs et les tendances de recherche pour identifier les domaines à améliorer en matière de marchandisage.
- **Recommandations** : créez et gérez des unités de recommandation dans Commerce Admin. Les recommandations utilisent des données de catalogue et un comportement d’acheteur agrégé pour suggérer des produits pertinents, tels que « Les clients qui ont consulté ce produit ont également consulté ».
- **Règles de marchandisage** : contrôlez la manière dont les produits sont promus et classés. Les règles peuvent s’appliquer à toutes les vues de catalogue ou être personnalisées pour une vue spécifique. Voir [Créer une règle de marchandisage](https://experienceleague.adobe.com/en/docs/commerce/optimizer/merchandising/rules/add#create-a-rule).
- **Facettes** : configurez les filtres que les acheteurs utilisent pour limiter les résultats des produits en fonction d’attributs tels que la marque, la taille ou le prix.
- **Synonymes** : associez des termes de recherche équivalents pour aider les acheteurs à trouver des produits utilisant des mots différents pour le même concept.
- **Paramètres** : configurez les options de recherche et de marchandisage, y compris les facettes de prix, la langue et la recherche avancée.

Les politiques déterminent quels produits sont disponibles par le biais d’une vue de catalogue. Les règles de marchandisage contrôlent la manière dont les produits de cet assortiment sont promus et classés.

Pour plus d&#39;informations sur la façon dont les résultats de recherche sont associés et classés, consultez [Correspondance de recherche et classement](./manage-results/search-relevance-matching.md).

>[!TAB Rapports]

Utilisez les rapports pour examiner l’activité du storefront et éclairer les décisions de marchandisage.

- **Mesures de succès**—Examinez le chiffre d’affaires, la conversion, l’engagement, l’acquisition et le taux de rebond en fonction de l’activité du storefront.
- **Performances de la recherche** : passez en revue les termes de recherche utilisés par les acheteurs et leurs performances afin d’identifier les domaines dans lesquels la découverte de produits doit être affinée.

La création de rapports dépend des données d’activité du storefront collectées par la mise en œuvre.

>[!TAB Configuration du système]

Surveillez la synchronisation des catalogues et la collecte d’événements storefront pour étudier les problèmes de disponibilité des données et d’implémentation.

- **Synchronisation du catalogue** : vérifiez l’état de synchronisation des données de catalogue transférées depuis Commerce Foundation.
- **Événements** : passez en revue les événements storefront capturés utilisés par la découverte de produits, les recommandations et les rapports. Utilisez la page Événements pour vérifier la collecte de données comportementales et rechercher les événements manquants ou inattendus.

>[!ENDTABS]
<!--
Watch the following video for a high-level overview of [!DNL Adobe Commerce Optimizer]:

>[!VIDEO](https://video.tv.adobe.com/v/3450226)
-->

## Confirmer qu’une instance utilise le CCDM

1. Connectez-vous à Commerce Admin via Unified Shell et sélectionnez l’instance Adobe Commerce as a Cloud Service prévue.
1. Vérifiez que les pages de marchandisage du CCDM, telles que les vues de catalogue et les politiques, sont disponibles dans la navigation de l’instance.
1. Si ces pages ne sont pas disponibles, vérifiez que vous avez sélectionné l’instance appropriée et que vous utilisez Unified Shell.

   Contactez l’assistance Adobe ou l’équipe d’approvisionnement de Commerce pour vérifier le statut d’approvisionnement du CCDM de l’instance.

Le statut Prêt de l’instance confirme qu’elle est approvisionnée, mais ne confirme pas en soi qu’elle utilise le CCDM.

