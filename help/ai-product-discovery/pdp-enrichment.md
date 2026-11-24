---
title: Enrichissement de la page des détails du produit
description: Utilisez l’enrichissement de page des détails du produit [!DNL Adobe Commerce] pour examiner la copie de produit suggérée par l’IA, créer des tâches d’enrichissement et déployer des mises à jour approuvées pour la découverte de LLM et d’IA.
role: Admin, User, Leader
recommendations: noCatalog
touch: true
badgePaas or on-premises: label="Cloud or on-premises only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed Cloud or on-premises infrastructure) and on-premises projects only."
autotag-review: '2026-06-23T17:36:07.142Z'
TQID: 'https://experienceleague.adobe.com/cjHuva7PP7UzP-yVhe0rkDzHgAYjfSdYEx3g5gorxwk'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c32adafa-ed01-4b31-997e-2413013911b0
    internal-label: Integrations
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9e234eb68fe34171d9e5cf95e8cdab5c31825492
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 0%
---

# Enrichissement de la page des détails du produit

L’enrichissement de la page des détails du produit (PDP) optimise l’explorabilité des LLM sur chaque PDP avec des données de produit structurées sans apporter de modifications à votre expérience humaine visible. Cette fonctionnalité lit à travers votre catalogue de produits afin de créer une payload de données structurées pour chaque PDP qui est facilement lisible et analysable par les LLM.

## Fonctionnement {#how-it-works}

Votre catalogue Adobe Commerce contient des informations sur les produits, telles que les attributs, les variantes, les catégories, les prix et la disponibilité. Dans une tâche d’enrichissement PDP, vous sélectionnez les pages de produits et les groupes de faits de catalogue à mettre à la disposition des agents d’IA. Les informations sont organisées pour les agents sans modifier l’expérience du storefront.

Avec l’enrichissement PDP, vous pouvez :

- Choisissez des produits activés spécifiques qui ont des pages de produits actives.
- Consultez un résumé des pages et des faits sélectionnés avant d’enregistrer ou d’exécuter la tâche.
- Prévisualisez les informations sur les produits incluses dans l’enrichissement.

| Direction | Objectif |
| --- | --- |
| Catalogue Commerce -> tâche d’enrichissement | Sélectionnez les pages de produits actives et les faits du catalogue à inclure. |
| Tâche d’enrichissement -> Agents d’IA | Rendre les informations sur les produits existantes sélectionnées disponibles dans un formulaire structuré. Le storefront visible par l&#39;homme ne change pas. |

## Accéder à l’enrichissement du PDP

Avant de commencer, passez en revue les [conditions préalables à la découverte de produit par l’IA](prerequisites.md) spécifiques au déploiement. Une fois la configuration de votre plateforme Commerce terminée, ouvrez **[!UICONTROL AI Product Discovery]** dans l’Administration et sélectionnez **[!UICONTROL Product Details Page Enrichment]**.

## Deux chemins d’enrichissement du PDP

Il existe deux chemins pour recevoir des enrichissements PDP :

- **Trafic agentic** - Ce type d’enrichissement démarre automatiquement 24 à 48 heures après la configuration de l’instance Commerce et affiche les résultats dans l’onglet **Optimisations**.
- **Gestionnaire d’enrichissement** - Ces enrichissements sont configurés par le commerçant lorsqu’il clique sur le bouton **[!UICONTROL Create enrichment]** et sélectionne manuellement les SKU à enrichir. En savoir plus sur le [gestionnaire d’enrichissement](#create-an-enrichment-job).

## Vérifier l’activité d’enrichissement PDP

La page d’enrichissement PDP s’ouvre sur l’onglet **[!UICONTROL Optimizations]**. Utilisez le tableau de bord pour passer en revue la couverture d’enrichissement, l’activité de tâche et les tâches nécessitant votre attention. Utilisez l’onglet **[!UICONTROL Settings]** pour [lier](settings.md) votre instance Commerce à la découverte de produit IA.

### Rechercher les tâches nécessitant une attention particulière

La section **[!UICONTROL Needs your attention]** met en évidence les tâches nécessitant une action. Une carte peut afficher le nom de la tâche, la manière dont les produits ont été sélectionnés, le nombre de pages de produits, le statut de la tâche et la progression. Utilisez l’action disponible sur une carte pour poursuivre le traitement.

### Rechercher dans toutes les tâches

Utilisez le tableau pour rechercher et suivre les tâches. Rechercher par détails de tâche ou filtrer par statut, y compris **[!UICONTROL Generating]**, **[!UICONTROL Ready to review]**, **[!UICONTROL Deployed]**, **[!UICONTROL Queued]** ou **[!UICONTROL Failed]**. Le tableau répertorie l’identifiant, le nom, l’origine, le nombre de pages de produits, la date de début, le statut et les actions disponibles de chaque traitement.

## Création d’une tâche d’enrichissement

Dans cette section, vous apprendrez à créer un enrichissement de page des détails du produit.

![Créer un enrichissement PDP](./assets/create-cat-enrich.png)

1. Dans **[!UICONTROL Optimizations]**, cliquez sur **[!UICONTROL Create enrichment]**.
1. Saisissez un **nom de l’enrichissement**, par exemple « Black Friday 2026 ».
1. Sélectionnez la **catégorie**, par exemple « Café ».
1. Sélectionnez le **Jeu d’attributs**, par exemple « Accessoires ».
1. Sélectionnez le **type de produit**, par exemple « Produit simple ».
1. Sélectionnez la **gamme de prix**.
1. Cliquez sur **[!UICONTROL Apply filters]**.

   Vous pouvez prévisualiser les produits qui correspondent à vos critères d’enrichissement et cliquer sur **Personnaliser** pour étendre la portée des produits que vous souhaitez enrichir.

1. Cliquez sur **[!DNL Next]** pour confirmer les produits spécifiques que vous souhaitez enrichir.
1. Cliquez sur **[!DNL Run enrichment]**.

   La tâche d’enrichissement s’exécute et s’affiche dans la table **Optimisations**. Une fois l’exécution terminée, vous pouvez [examiner et déployer](#review-and-deploy-an-enrichment-job) les optimisations.

### Vérification d’une tâche d’enrichissement {#review-and-deploy-an-enrichment-job}

Ouvrez une tâche d’enrichissement.

![Liste des URL d’enrichissement PDP](./assets/pdp-enrich-urls.png)

Le tableau **URL avec suggestions** répertorie tous les produits avec des opportunités d’enrichissement. Pour chaque produit, vous pouvez :

- **Développez la ligne** pour afficher l’analyse de l’IA et l’enrichissement proposé.
- **Modifiez** le nom ou la description du produit proposé avant l&#39;application, afin de vous conformer aux directives de votre marque en matière de voix et de marchandisage.
- **Déployez l’optimisation** pour les produits que vous souhaitez enrichir et publiez-la directement sur votre storefront Adobe Commerce.
- **Marquer comme corrigé** une fois l&#39;enrichissement vérifié et appliqué.
- **Ignorer** les suggestions qui ne sont pas pertinentes pour votre stratégie de catalogue.

Les suggestions sont organisées en trois vues : **Suggestions actuelles**, **Suggestions fixes** et **Suggestions ignorées**. Une fois qu’un enrichissement est appliqué, il passe à **Suggestions fixes** avec un statut de **Appliqué**. Les enrichissements appliqués peuvent être restaurés à tout moment.

### Déployer l’optimisation

Une fois que vous avez examiné les suggestions et sélectionné les pages de produits à optimiser, cliquez sur **Déployer des optimisations** pour publier l’enrichissement à l’aide d’Optimiser sur Edge. Une boîte de dialogue de confirmation **Déployer sur Edge** affiche les URL de produit sélectionnées, le type d’optimisation et l’enrichissement appliqué. Après le déploiement, un écran de confirmation confirme quelles pages de produits ont été optimisées avec succès.

L’optimisation est fournie exclusivement aux agents utilisateurs de l’IA via l’[Optimiser sur Edge](https://experienceleague.adobe.com/en/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn). Les visiteurs humains continuent à voir votre expérience de storefront existante exactement comme auparavant, sans modifications de la conception de votre PDP, des performances de la page ou de l’expérience de votre marque.

## Limites et considérations {#limits}

- Seuls les produits activés avec une page de produits en ligne peuvent être sélectionnés.
- L’enrichissement organise les faits déjà présents dans le catalogue ; il n’ajoute pas de nouvelles informations sur les produits.
- Le workflow d’enrichissement PDP ne modifie pas le storefront.
- Les tâches d’enrichissement PDP et les tâches d’enrichissement de catalogue ont des objectifs et des workflows différents.
- L’optimisation du PDP utilise [Optimiser dans Edge](https://experienceleague.adobe.com/en/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn) .

## Bonnes pratiques {#best-practices}

- Utilisez des noms de tâche clairs qui identifient le groupe de produits ou la campagne.
- Prévisualisez les faits inclus dans la tâche et confirmez qu’ils sont exacts et appropriés pour les agents d’IA.
- Vérifiez si les produits ont déjà été enrichis avant de décider de les ignorer ou de les remplacer.
- Coordonnez la synchronisation des catalogues et la propriété des faits de produit avec les équipes responsables de ces enregistrements.

## Exemple : enrichissement d’un produit avec des variantes et des spécifications

Une page produit contient souvent plus d’informations de catalogue que les agents d’IA ne peuvent en lire. Par exemple, un marchand vend une botte de randonnée imperméable. Les options de taille, de largeur et de couleur se trouvent dans un sélecteur de variante qui se charge avec JavaScript. Les matériaux, l’imperméabilisation et les instructions d’entretien se trouvent dans un onglet Détails réduit et le guide d’ajustement s’ouvre dans un pop-up. Un acheteur peut accéder à toutes ces fonctionnalités, mais un robot d&#39;exploration d’IA qui lit la page telle qu’elle se charge en premier ne peut voir que le nom, le prix et une brève description du produit.

Lorsque la tâche d’enrichissement s’exécute sur ce produit, elle prend toutes les données du catalogue du produit, y compris ses attributs et chaque variante, et les regroupe dans un format structuré que les agents d’IA peuvent lire. Un assistant d’IA peut alors répondre à des questions du type « Cette botte est-elle disponible dans un format large de la taille 11 ? » ou « Est-il complètement étanche ? » à partir des données de catalogue propres au commerçant.

La tâche d’enrichissement utilise uniquement les informations qui existent déjà dans le catalogue. Cela ne crée pas de nouveaux faits de produit et ne modifie pas la page produit que les acheteurs voient.
