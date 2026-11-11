---
title: Tâches de marchandisage de catalogue par rôle
description: Recherchez des conseils sur les tâches pour les administrateurs, les développeurs et les marchandiseurs qui travaillent avec les instances Adobe Commerce as a Cloud Service configurées avec CCDM.
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="SaaS uniquement" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique aux instances Adobe Commerce as a Cloud Service configurées avec le CCDM uniquement (infrastructure SaaS gérée par Adobe)."
TQID: 'https://experienceleague.adobe.com/0PmobUkdEWspxuRSaIPL8vS1ojDDZ3gw-L-3SfPmJAg'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: cc04bd17-78d5-5120-8c3d-1b8a57e49280
    internal-label: Integration
  - id: dec06508-d41f-555a-87e8-29e8bcdfa95a
    internal-label: Recommendations
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
  - id: f37757d8-3174-5335-b977-1161792f965d
    internal-label: Personalization
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: dba482e5-29a8-4127-afa2-c4b913512ef8
    internal-label: Data and analytics
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 742236e7fdb26c56a80f66a44b0a4960210f4dac
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%
---

# Tâches de marchandisage de catalogue par rôle

Utilisez cette référence de tâche pour trouver des conseils sur la configuration des données de catalogue, l’intégration du storefront, la gestion du marchandisage et la révision des performances dans les instances Adobe Commerce as a Cloud Service configurées avec le modèle de données de catalogue composable (CCDM).

Les responsabilités varient selon la mise en œuvre. Les sections suivantes regroupent les tâches selon les rôles qui les exécutent généralement.

- Les administrateurs gèrent les produits, les prix et la configuration B2B dans Commerce Foundation.
- Les développeurs configurent l’intégration du storefront et vérifient les demandes de catalogue et la collecte de données comportementales.
- Les marchandiseurs configurent la découverte et les recommandations de produits et utilisent les rapports pour prendre des décisions éclairées en matière de marchandisage.

Les données de produit et de prix se synchronisent avec le CCDM via l’intégration native d’Adobe Commerce as a Cloud Service. Aucune installation de connecteur distincte ni application App Builder n’est requise.

## Préparer le catalogue et le storefront

Effectuez les tâches qui s’appliquent à votre implémentation. Les vues de catalogue B2C peuvent être créées manuellement. Les vues de catalogue B2B, les politiques et les tarifs sont générés à partir de la configuration B2B dans Commerce Foundation.

| Tâche | Description | Ressources |
| --- | --- | --- |
| **Configurer les produits et les prix** | Gérez les produits et les prix dans Commerce Foundation. Les données de tarification sont synchronisées avec le CCDM sous forme de livres de prix ; ne créez pas indépendamment de prix dans le CCDM. | [Liste de produits](../catalog/products-list.md), [Créer un produit](../catalog/product-create.md), [Périmètre de prix](../catalog/catalog-price-scope.md) et [Tarification avancée](../catalog/pricing-advanced.md) |
| **Configurer les vues de magasin** | Configurez les vues de magasin et les données de produit localisées requises pour votre storefront dans Commerce Foundation. | [Vues du magasin](../stores-purchase/store-views.md) |
| **Configurer des catalogues et des sociétés partagés B2B** | Pour les implémentations B2B, configurez les catalogues partagés et les relations d’entreprise dans Commerce Foundation avant de passer en revue la configuration de catalogue générée. | [Catalogues partagés](../b2b/catalog-shared.md) et [Entreprises](../b2b/account-companies.md) |
| **Configurer des vues et des politiques de catalogue B2C** | Créez des vues de catalogue et sélectionnez les politiques qui définissent l’assortiment de produits disponible. Associez les registres de prix synchronisés applicables à chaque vue. | [Vues du catalogue](./setup/catalog-view.md) |
| **Consulter les vues du catalogue B2B** | Vérifiez que la synchronisation native a généré les vues de catalogue, les politiques et les registres de prix attendus. Gérez la configuration B2B sous-jacente dans Commerce Foundation plutôt que de créer manuellement des structures en double. | [Vues du catalogue B2B](./setup/catalog-view.md#b2b-catalog-views) |
| **Configurer le storefront** | Configurez le storefront pour demander le contexte de catalogue prévu. Pour les intégrations storefront personnalisées ou autres, passez en revue les en-têtes de requête de catalogue applicables. | [Configuration du storefront](https://experienceleague.adobe.com/en/tools/commerce-storefront/setup/configuration/commerce-configuration/) |

Avant de configurer le marchandisage, vérifiez que le storefront renvoie les produits et les prix attendus. Testez l’ajout au panier, le panier et le passage en caisse pour vérifier que le prix de la transaction correspond à la configuration Commerce Foundation prévue.

## Configuration du merchandising et révision des performances

| Tâche | Description | Ressources |
| --- | --- | --- |
| **Configurer la découverte de produits** | Configurez les règles, facettes et synonymes de marchandisage. Les règles peuvent s’appliquer à toutes les vues de catalogue ou être personnalisées pour une vue spécifique. | [Présentation du marchandisage](./merchandising/overview.md) |
| **Vérifier les paramètres de recherche** | Examinez la configuration de recherche et les options de recherche sémantique disponibles pour votre mise en œuvre. | [Paramètres de marchandisage](./settings.md) et [Recherche sémantique](./setup/semantic-search.md) |
| **Configurer les recommandations** | Créez des unités de recommandation et vérifiez que le storefront collecte les données comportementales requises par la mise en œuvre. | [Présentation de Recommendations](./merchandising/recommendations/overview.md) |
| **Vérifier les performances** | Utilisez les mesures de succès et les rapports de performances de recherche pour évaluer l’activité du storefront et éclairer les décisions de marchandisage. | [Mesures de succès](./manage-results/success-metrics.md) et [Performances de recherche](./manage-results/search-performance.md) |

## Étapes suivantes

Après avoir configuré le marchandisage et examiné les performances, continuez à surveiller et à ajuster vos règles, facettes et recommandations selon les besoins pour optimiser l’expérience du storefront.
