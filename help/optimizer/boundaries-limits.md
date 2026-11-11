---
title: Limites et limites des services de marchandisage
description: Découvrez les limites de licence et les limites système de Adobe Commerce Optimizer. Planifiez la capacité, suivez l’utilisation et évitez la latence et le ralentissement lorsque vous dépassez les limites.
role: Admin, Developer
hide: true
badgeSaas: label="SaaS uniquement" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique aux instances Adobe Commerce as a Cloud Service configurées avec le CCDM uniquement (infrastructure SaaS gérée par Adobe)."
autotag-review: '2026-11-02T18:48:38.168Z'
TQID: 'https://experienceleague.adobe.com/KoRp--G2sMvv-Hr7KiHriZrFmtEm0BhGoGWVQQK-ofE'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: 8d0b446f-5b16-5a10-b272-01143504a11c
    internal-label: System
  - id: d3b92bef-63fa-5031-a925-d04d9362d616
    internal-label: Saas
source-git-commit: 71df9ad673f2e7dff802e4b26d8e169c42d9c063
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 1%
---

# Limites et limites des services de marchandisage avec le modèle de données de catalogue composable (CCDM)

Les services de marchandisage Adobe Commerce avec CCDM appliquent des limites de licence et des limites système qui définissent la capacité que votre projet peut utiliser :

- **Limites de licence** : en fonction de la capacité achetée ; peut être augmentée en achetant des packages supplémentaires.
- **Limites du système** : limites fixes qui protègent les ressources système et garantissent des performances fiables pour tous les utilisateurs.

Votre utilisation doit respecter ces limites. Leur dépassement peut entraîner une latence accrue et un ralentissement des demandes.

## Demander une capacité supplémentaire

Les limites de licence peuvent être augmentées en achetant les packages de licence décrits dans la section [Limites de licence et limites système](#license-limits-and-system-boundaries) ou en négociant une licence personnalisée pour des cas d’utilisation uniques. Contactez votre représentant de compte Adobe pour discuter de vos besoins.

Pour toute question sur les limites du système, contactez [l’assistance Adobe](https://experienceleague.adobe.com/home?lang=en#support).

## Prévention des problèmes de performances

Suivez ces bonnes pratiques pour respecter les limites et éviter les problèmes opérationnels :

- **Examinez vos limites**—Comprenez vos [limites de capacité](#license-limits-and-system-boundaries) avant de lancer de nouveaux storefronts ou de nouvelles campagnes.
- **Suivez votre utilisation** : utilisez des tableaux de bord de mesures intégrés ou des journaux CDN.

## Limites de licence et limites système

Les tableaux suivants résument les limites des licences et les limites du système par domaine de capacité et incluent des informations sur l’ajout de licences supplémentaires pour augmenter la capacité, le cas échéant.


### Catalogue

| **Fonctionnalité** | **Description** | **Affectation de base** | **Extensible ?** |
| --- | --- | --- | --- |
| Taux d’ingestion du produit | Nombre de produits créés ou mis à jour | 1K mises à jour par minute<p>100 000 mises à jour maximum par jour</p> | Oui<p>Ajouter un pack de licences :</p><ul><li>5K mises à jour par minute<br>Un maximum de 500K mises à jour par jour</li> <li>10 000 mises à jour par minute<br>Un maximum de 1 million de mises à jour par jour</li></ul><p>La capacité maximale d’ingestion des données est de 1 million de mises à jour par jour.</p> |
| Taille de la payload du produit | La quantité maximale de données autorisée lors de la création, de la mise à jour ou de l’ingestion d’informations sur les produits à l’aide de l’API | 200 KO | Non |
| Variations de catalogue | Le nombre de vues d’un catalogue disponibles pour les utilisateurs de storefront,<p>qui sont comptabilisés comme (*Nombre de vues de catalogue × Nombre de livres de prix*)</p> | 100 variations | Oui<p>Ajout d’un pack de licences de 100 variations de catalogue</p> |
| Produits dans une seule source de catalogue | SKU pris en charge dans le catalogue | 250 000 SKU | Oui<p>Ajouter un pack de licences SKU 100 000</p> |
| Variantes par produit | Le nombre de variantes de produit (taille, combinaisons de couleurs) autorisées par produit | 10K | Non |
| Sources de catalogue | Le nombre de contextes de données de catalogue (par exemple, des paramètres régionaux ou des sources de données telles que des PIM et des ERP) | 50 | Non |

{style="table-layout:auto"}

### Catalogues de prix

| **Fonctionnalité** | **Description** | **Affectation de base** | **Extensible ?** |
| --- | --- | --- | --- |
| Catalogues de prix | Nombre de répertoires de prix autorisés par instance | En fonction du nombre de [variations de catalogue](#catalog) | Oui<br>Augmenter les variations de catalogue |
| Remises par enregistrement de prix | Nombre de remises qui peuvent être appliquées à un prix de produit dans un seul catalogue de prix | 10 | Non |

{style="table-layout:auto"}

### Vues et politiques de catalogue

| **Fonctionnalité** | **Description** | **Affectation de base** | **Extensible ?** |
| --- | --- | --- | --- |
| Vues du catalogue | Nombre de sous-ensembles configurables de votre catalogue principal | En fonction du nombre de [variations de catalogue](#catalog) | Oui<br>Augmenter les variations de catalogue |
| Politiques par vue de catalogue | Nombre de filtres de données autorisés | 10 | Non |
| Valeurs d’attribut dans une politique | Nombre de caractéristiques de produit configurables pour le filtrage | 100 | Non |
| [Affectation de clé d&#39;accès restreinte](setup/private-catalog-view.md) | Nombre de clés d’accès restreint pouvant être affectées à une seule vue de catalogue | 3 | Non |
| Taille de la clé RSA (clés d’accès restreint) | Intensité de clé minimale et maximale acceptée pour une clé à accès restreint | 2 048 bits au minimum, 8 192 bits au maximum | Non |
| Clés d’accès restreintes | Délai de propagation de révocation de clé | Jusqu’à 5 minutes, en raison de la mise en cache. Les jetons signés par une clé supprimée sont refusés une fois le délai écoulé. | Sans objet |

{style="table-layout:auto"}

### Storefront de catalogue

L’allocation de base pour les fonctionnalités de storefront du catalogue est déterminée en fonction du niveau de la valeur brute (VGM). Le tableau indique l’allocation minimale pour chaque fonctionnalité.

| **Fonctionnalité** | **Description** | **Affectation de base** | **Extensible ?** |
| --- | --- | --- | --- |
| Taux de récupération des catalogues | Nombre d’appels mensuels d’une API de catalogue par un système (storefront, système de transactions, ERP ou autre) pour récupérer des données du catalogue | Basé sur le niveau GMV<p>Allocation minimale : 10M/mois</p> | Oui<p>Ajout de 1 million de requêtes par mois de packs de licences</p> |
| Requêtes de contenu | Demandes au storefront de pages vues HTML ou d’appels API JSON. Comptabilisé comme 1 page vue ou 5 appels API. | Basé sur le niveau GMV<p>Allocation minimale : 2M/mois</p> | Oui<p>Ajout d’un pack de licences de 1 million par mois</p> |
| Variantes de Storefront GenAI | Autorisation pour la génération de contenu textuel | Basé sur le niveau GMV<p>Allocation minimale : 1 K variations/mois</p> | Oui<p>Achetez les crédits IA génératifs séparément</p> |

{style="table-layout:auto"}

>[!NOTE]
>
>La génération d’images nécessite une licence [!DNL Adobe Firefly] configurée pour la même organisation IMS que [!DNL Adobe Commerce Optimizer].


### Découverte de produits

Les limites suivantes s’appliquent à la recherche de produits, aux listes et à la configuration de marchandisage du storefront.

| **Fonctionnalité** | **Description** | **Affectation de base** | **Extensible ?** |
| --- | --- | --- | --- |
| Récupération du produit | SKU maximum par requête GraphQL [!DNL Catalog Service] lors de la récupération des données de produit avec `products`, `productSearch`, `refineProduct` et `variants`. Répartissez les requêtes les plus volumineuses sur plusieurs appels. | 100 | Non |
| Attributs filtrables | Nombre de caractéristiques de produit (telles que la couleur, la taille, la marque ou le matériau) qui peuvent être activées pour la navigation superposée et les facettes | 200 | Non |
| Attributs pouvant faire l’objet d’une recherche | Nombre de caractéristiques de produit qui peuvent être indexées pour la recherche catalogue | 200 | Non |
| Attributs triables | Nombre de caractéristiques de produit disponibles en tant qu’options de tri sur les pages de recherche et de catégorie. | 50 | Non |
| Profondeur de pagination de recherche | Nombre maximal de produits accessibles par la pagination de la recherche (par exemple, page 100 × 100 produits/page). | 10K | Non |
| Facettes | Nombre d’attributs de produit filtrables (tels que la marque, la couleur, la taille et le prix) qui peuvent être configurés pour aider les acheteurs à affiner les résultats de recherche et à parcourir les catégories | 100<p>Doit être un attribut filtrable</p> | Non |
| Options par facette | Nombre de valeurs d’attribut de produit filtrables que les acheteurs peuvent sélectionner dans une facette (par exemple, « Rouge », « Bleu » pour la couleur, « Petit », « Medium » pour la taille). | 100 | Oui<p>Peut augmenter via une demande d’assistance</p> |

{style="table-layout:auto"}

### Recommendations

Les fonctionnalités suivantes sont disponibles pour les recommandations de produits. Certaines fonctionnalités disponibles dans d&#39;autres produits Adobe Commerce ne sont pas prises en charge dans [!DNL Adobe Commerce Optimizer].

| **Fonctionnalité** | **Description** | **Affectation de base** | **Extensible ?** |
| --- | --- | --- | --- |
| Unités de recommandation actives | Nombre de composants de recommandations en direct sur votre storefront (par exemple, « Les clients ont également consulté » ou « Vous pourriez également aimer ») | 50 | Non |
| Inclusions/exclusions de catégories ou d’attributs | Filtrer les produits selon un ensemble spécifique éligible aux recommandations | Non pris en charge | — |

{style="table-layout:auto"}
