---
title: Vues du catalogue
description: Découvrez les vues de catalogue et comment les créer pour organiser votre catalogue de produits par structure d’entreprise, politiques et prix.
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="SaaS uniquement" type="Positive" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique aux instances Adobe Commerce as a Cloud Service configurées avec le CCDM uniquement (infrastructure SaaS gérée par Adobe)."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 8fbcfcdeb13c452a45e872d939e129703ac5abab
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%
---

# Vues du catalogue

Une vue de catalogue définit les produits et les prix qu’un storefront peut récupérer. Dans les instances Adobe Commerce as a Cloud Service configurées avec le modèle de données de catalogue composable (CCDM), les vues de catalogue utilisent la même base de catalogue qui alimente Adobe Commerce Optimizer.

Les vues catalogue combinent des sources de catalogue, des politiques et des livres de prix pour définir le contexte de catalogue d’un storefront. Les politiques déterminent l’assortiment de produits disponible. Les règles de marchandisage contrôlent la manière dont les produits de cet assortiment sont promus et classés. Elles peuvent également s’appliquer à toutes les vues de catalogue ou être personnalisées en fonction d’une vue spécifique. Voir [Créer une règle de marchandisage](../merchandising/rules/add.md).

Commerce Foundation reste la source de vérité pour les produits et les prix. Les données de produit et de prix se synchronisent de manière unidirectionnelle avec le CCDM par le biais de l’intégration native d’Adobe Commerce as a Cloud Service, sans installation de connecteur distincte ni application App Builder. La configuration du site web, du magasin et de l’affichage du magasin reste dans Commerce Foundation, qui gère également le panier, le passage en caisse, les promotions, les clients, les commandes et les paiements.

>[!NOTE]
>
>Pour les instances configurées avec CCDM, utilisez [Commerce Admin dans l’expérience unifiée Adobe](../../getting-started/admin-unified-experience.md) pour configurer les vues et les politiques de catalogue et associer les catalogues des tarifs synchronisés aux vues de catalogue. Les instances qui utilisent le service de catalogue avec Live Search et les recommandations de produits n’ont pas accès à ces écrans de gestion de catalogue.

## Fonctionnement des vues de catalogue

Une vue de catalogue rassemble les données de catalogue et la configuration pour un contexte de storefront. Il peut être utilisé pour représenter une unité opérationnelle, une marque, une région ou une autre expérience de storefront.

- **[Les sources de catalogue](catalog-sources.md)** fournissent des données de produit pour les expériences de catalogue.
- **[Politiques](policies.md)** filtrent les données de produit pour une vue de catalogue.
- **[Les catalogues de prix](pricebooks.md)** fournissent des données de prix associées à une vue catalogue.

Les vues Catalogue ne remplacent pas la structure du site web, du magasin et de la vue du magasin dans Adobe Commerce as a Cloud Service. Commerce Foundation continue de gérer cette structure et les opérations transactionnelles.

Les données de catalogue se synchronisent de Commerce Foundation dans le CCDM. Le CCDM prend en charge les expériences de catalogue storefront et la découverte de produits. Commerce Foundation continue de gérer le panier, le passage en caisse, les promotions, les clients et les commandes.

## Avant de commencer

Avant de configurer une vue de catalogue :

- [Confirmez que l’instance Adobe Commerce as a Cloud Service utilise le CCDM](../overview.md).
- Vérifiez que les données de catalogue requises pour le storefront ont été renseignées et [synchronisées](data-sync.md).
- Identifiez la [source du catalogue](catalog-sources.md), les [politiques](policies.md) et les [tarifs](pricebooks.md) nécessaires pour le contexte du storefront.
- Déterminez si vous devez créer manuellement des vues de catalogue B2C ou passer en revue les vues de catalogue B2B générées par la synchronisation native.

>[!NOTE]
>
>Pour les implémentations B2B, la synchronisation native génère des vues de catalogue, des politiques et des tarifs à partir de la configuration B2B dans Commerce Foundation. Ne créez pas manuellement de doublons de ces structures générées automatiquement.

## Création d’une vue de catalogue pour une implémentation B2C

Utilisez ce workflow lorsque l’implémentation B2C nécessite que les vues de catalogue soient configurées manuellement.

1. Connectez-vous à [Commerce Admin dans l’expérience unifiée](../../getting-started/admin-unified-experience.md), puis sélectionnez l’instance Adobe Commerce as a Cloud Service configurée avec CCDM.
1. Dans le volet de navigation de gauche, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Catalog Views]**.
1. Sélectionnez **[!UICONTROL Create catalog view]**.
1. Saisissez un nom pour la vue de catalogue.
1. Sélectionnez la ou les [sources du catalogue](catalog-sources.md) pour le contexte storefront.
1. Associez les [politiques](policies.md) pertinentes à la vue de catalogue.
1. Associez les tarifs appropriés à la vue catalogue en [configurant la disponibilité des tarifs](pricebooks.md).
1. Créez la vue Catalogue.

## Vues du catalogue B2B

Pour les implémentations B2B, la synchronisation native génère des vues de catalogue, des politiques et des tarifs à partir de la configuration B2B dans Commerce Foundation. Gérez le catalogue B2B sous-jacent et les relations d’entreprise dans Commerce Foundation plutôt que de créer manuellement des structures en double dans CCDM.

Pour obtenir des instructions de configuration, voir [Créer un catalogue partagé](../../b2b/catalog-shared-create.md) et [Affecter des sociétés à un catalogue partagé](../../b2b/catalog-shared-assign-companies.md).

Après avoir configuré les relations B2B :

1. Vérifiez que la [synchronisation](data-sync.md) est terminée.
2. Consultez les vues de catalogue générées, les [politiques](policies.md) et les [tarifs](pricebooks.md) dans [Commerce Admin dans Unified Experience](../../getting-started/admin-unified-experience.md).
3. Vérifiez que le storefront affiche l&#39;assortiment de produits attendu et le prix pour la société.
4. Testez l’ajout au panier, le panier et le passage en caisse pour confirmer que la disponibilité du produit et le prix des transactions correspondent à la configuration B2B prévue.

## Carnets de prix et passage en caisse

Les tarifs fournissent les données de tarification disponibles par le biais d&#39;une vue de catalogue. Dans Adobe Commerce as a Cloud Service, Commerce Foundation reste la source de vérité des prix et les données de prix sont synchronisées avec le CCDM par le biais de l’intégration native. Lors de la configuration d’une vue de catalogue, utilisez les tarifs synchronisés applicables plutôt que de créer des tarifs indépendamment dans CCDM.

Le panier et le passage en caisse utilisent les tarifs de Commerce Foundation. Vérifiez que les prix de storefront affichés correspondent aux prix de panier et de passage en caisse applicables.

## Vérification et validation d’une vue de catalogue

Après avoir configuré une vue de catalogue, vérifiez l’expérience storefront complète :

- Vérifiez que les données de catalogue prévues sont [synchronisées](data-sync.md).
- Vérifiez que la vue du catalogue est associée aux [politiques](policies.md) et [tarifs prévus](pricebooks.md).
- Vérifiez que le storefront renvoie l&#39;assortiment de produits attendu.
- Vérifiez le prix affiché par rapport au prix Commerce Foundation correspondant.
- Testez l’ajout au panier, le panier et le passage en caisse.

Pour les implémentations B2B, vérifiez également que les structures de catalogue générées par la synchronisation correspondent à la configuration d’entreprise et de catalogue prévue.

## Dépannage

### Les produits sont absents du storefront

- [Confirmez que l’instance utilise CCDM](../overview.md).
- Vérifiez que les données du catalogue ont [été synchronisées](data-sync.md).
- Vérifiez que le storefront utilise le contexte de catalogue prévu.
- Examinez les [politiques](policies.md) associées à la vue de catalogue.

### Le prix affiché est inattendu

- Confirmez que le catalogue [prix catalogue](pricebooks.md) prévu est associé à la vue.
- Vérifiez que les données de prix sont [synchronisées](data-sync.md) et cohérentes avec Commerce Foundation.

  Consultez [Classeurs de prix](pricebooks.md) pour le site web et les mappages de tarification des groupes de clients.

- Validez à nouveau le prix dans le panier et passez en caisse.

### Les écrans de catalogue CCDM ne sont pas visibles dans Commerce Admin

[Confirmez que l’instance sélectionnée utilise le CCDM](../overview.md) et que vous accédez à [Commerce Admin dans l’expérience unifiée](../../getting-started/admin-unified-experience.md). Une instance exécutant catalog services v1 ne dispose pas des écrans d’administration CCDM.

## Contenu associé

- [Prise en main d’Adobe Commerce as a Cloud Service](https://experienceleague.adobe.com/fr/docs/commerce/cloud-service/getting-started)
- [Présentation du catalogue partagé Adobe Commerce B2B](../../b2b/catalog-shared.md)
- [Notes de mise à jour d’Adobe Commerce as a Cloud Service](https://experienceleague.adobe.com/fr/docs/commerce/cloud-service/release-notes)
- [Synchronisation des catalogues](data-sync.md)
