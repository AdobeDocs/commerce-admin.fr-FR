---
title: Enrichissement du catalogue
description: Utilisez la fonctionnalité native d’enrichissement du catalogue d’Adobe Commerce pour examiner et appliquer les améliorations suggérées par l’IA aux noms de produit et aux descriptions longues pour la gestion du cycle de vie des documents et la découverte assistée par l’IA.
role: Admin, User, Leader
recommendations: noCatalog
hide: true
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
autotag-review: '2026-06-23T17:36:07.142Z'
TQID: 'https://experienceleague.adobe.com/cjHuva7PP7UzP-yVhe0rkDzHgAYjfSdYEx3g5gorxwk'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c32adafa-ed01-4b31-997e-2413013911b0
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 69e598995a3f7fbbb23c4cde3bc28334ef2feafe
workflow-type: tm+mt
source-wordcount: 1649
ht-degree: 0%

---

# Enrichissement du catalogue

L’enrichissement du catalogue est une fonctionnalité de [!DNL Adobe Commerce] native qui vous permet d’améliorer les noms de produit et les descriptions longues afin que votre catalogue soit représenté plus précisément lorsque les acheteurs utilisent des outils LLM et des assistants d’IA pour la recherche et la découverte de produits.

>[!NOTE]
>
>L’enrichissement des catalogues s’effectue à l’aide de [!DNL Commerce Catalog Agent] et [!DNL Adobe LLM Optimizer] en coulisses. Vous utilisez l’enrichissement dans le cadre de votre workflow de catalogue Commerce. Vous ne gérez pas une intégration LLM Optimizer distincte pour appliquer les mises à jour de nom et de description approuvées. Pour une surveillance et une optimisation LLM plus larges en dehors de Commerce, consultez la documentation du produit [LLM Optimizer](https://experienceleague.adobe.com/fr/docs/llm-optimizer/using/home).

## Fonctionnement {#how-it-works}

Votre catalogue de produits [!DNL Adobe Commerce] est le système d’enregistrement des données de produits : noms, descriptions, attributs, tarification et inventaire. [!DNL Adobe Commerce] MCP (Model Context Protocol) de Storefront connecte les données de catalogue actives aux expériences Adobe AI. À partir de là, l’agent de catalogue peut identifier les lacunes dans les noms de produits et les descriptions longues, proposer des améliorations et écrire les modifications approuvées dans Commerce afin que vous puissiez les examiner dans l’administration Commerce.

Avec l’enrichissement de catalogue, vous pouvez :

- Identifiez les lacunes et les incohérences dans les noms de produits et les descriptions longues qui affectent la façon dont les LLM interprètent vos produits.
- Examen des améliorations suggérées avec contexte à l&#39;appui, y compris les justifications et les comparaisons avant et après.
- Appliquez les mises à jour approuvées directement au catalogue Commerce afin que l’administrateur, le storefront et les autres canaux qui lisent ces champs restent alignés.

Comme les noms de produit et les descriptions longues résident dans Commerce, l’amélioration de la copie peut bénéficier à chaque canal qui utilise ces données de produit. L’avantage dépend de la façon dont vos systèmes sont actualisés et du moment où ils le sont.

| Direction | Objectif |
| --- | --- |
| Catalogue Commerce -> analyse | Les signaux de catalogue et d’URL fournissent des suggestions d’enrichissement. |
| Enrichissement -> Catalogue Commerce | Après approbation d’une mise à jour, les modifications apportées au nom et à la description du produit sont enregistrées dans le catalogue Commerce afin que l’administrateur et le storefront reflètent les valeurs optimisées. |

## À qui cela s&#39;adresse-t-il {#who-this-is-for}

- Les marketeurs et les marketeurs qui souhaitent que les données sur les produits soient exactes et cohérentes dans les réponses pilotées par LLM
- Les spécialistes du marketing numérique et les marketeurs qui ont besoin d’un moyen contrôlé d’améliorer la copie de catalogue à grande échelle.
- Les administrateurs Commerce qui possèdent l’intégrité du catalogue, les processus d’administration et les intégrations (API, CSV, PIM) qui alimentent les attributs de produit.

## Conditions préalables {#prerequisites}

Les conditions préalables suivantes s’appliquent lorsque vous avez accès à l’enrichissement du catalogue.

- Votre storefront peut être exploré par des robots orientés LLM et agentiques où une couverture d’explore est requise pour les suggestions tenant compte du catalogue.
- Les services Commerce requis et la connectivité du catalogue sont activés et sains. Voir [Activer l’enrichissement du catalogue](#enable-catalog-enrichment) pour en savoir plus.
- [IMS est configuré](https://experienceleague.adobe.com/fr/docs/core-services/interface/administration/organizations).
- Vous avez accès à [&#128279;](https://helpx.adobe.com/fr/business/enterprise/plan-your-deployment/basic-concepts/admin-console.html).

> Si vous ne disposez pas d’une organisation IMS, contactez votre équipe de compte Adobe pour en configurer une.

## Activer l’enrichissement du catalogue {#enable-catalog-enrichment}

Contactez votre administrateur Commerce ou votre partenaire d’implémentation pour vous assurer des points suivants avant de vérifier ou d’appliquer les suggestions :

### Installation de l’enrichissement du catalogue et des extensions des services de catalogue

1. Installez l’extension d’enrichissement de catalogue dans votre instance Commerce en exécutant la commande suivante :

   ```bash
   composer require magento/module-catalog-enrichment --no-update
   composer update magento/module-catalog-enrichment
   ```

1. Si vous n’avez pas encore installé les services de catalogue, [faites-le](https://experienceleague.adobe.com/fr/docs/commerce/catalog-service/installation#install-the-catalog-service-extension).

   **[!UICONTROL Catalog enrichment]** est désormais disponible dans votre instance Commerce.

### Accéder à l’enrichissement du catalogue

Une fois que vous avez installé l’enrichissement de catalogue et les extensions de services de catalogue, la fonctionnalité d’enrichissement de catalogue est disponible dans l’Administration sous **[!UICONTROL Catalog]** > **[!UICONTROL Catalog Enrichment]**.

![Enrichissement du catalogue](./assets/catalog-enrichment-menu.png)

### Configuration de l’enrichissement du catalogue

Configurez l’enrichissement du catalogue dans l’onglet **[!UICONTROL Settings]** afin que [!DNL Commerce Catalog Agent] puissiez vous connecter à votre environnement de [!DNL Adobe Commerce] et obtenir des suggestions de surfaces dans l’administration Commerce.

1. Dans Admin, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Catalog Enrichment]**.
1. Dans la liste **[!UICONTROL Scope]** en haut de la page, sélectionnez la vue de magasin à configurer ou laissez-**[!UICONTROL All Store Views]** pour gérer les paramètres entre les vues de magasin.
1. Ouvrez l’onglet **[!UICONTROL Settings]** .
1. Dans **[!UICONTROL Commerce Configuration]**, développez le panneau d’affichage du magasin intitulé avec son URL.

   Fournissez les détails de votre environnement [!DNL Adobe Commerce] pour activer le service Catalog LLM Optimizer et les workflows d’audit.

   Configuration de ![Commerce dans l’onglet Paramètres d’enrichissement du catalogue &#x200B;](./assets/catalog-enrichment-commerce-config.png)

1. Saisissez les informations de connexion requises pour la vue du magasin.

   - **[!UICONTROL Store View URL]** : URL correspondant à la vue du magasin (par exemple, `https://brand.example.com/fr/`).
   - **[!UICONTROL Environment ID]** : identifiant unique de l’environnement [!DNL Adobe Commerce] auquel la connexion accède.
   - **[!UICONTROL Website Code]**, **[!UICONTROL Store Code]** et **[!UICONTROL Store View Code]** : codes d’affichage du site web, du magasin et du magasin pour le site web Commerce. Ces valeurs doivent correspondre aux codes de votre administrateur Commerce.

1. Facultatif : saisissez **[!UICONTROL Host Name]** et **[!UICONTROL API Key]** si votre environnement les requiert.

   - **[!UICONTROL Host Name]** : nom d’hôte de votre instance [!DNL Adobe Commerce].
   - **[!UICONTROL API Key]** : clé d’authentification utilisée pour accéder en toute sécurité aux API [!DNL Adobe Commerce]. Cliquez sur **[!UICONTROL Copy]** en regard du champ si vous devez copier la clé ailleurs.

1. Cliquez sur **[!UICONTROL Save]**.

Après l’enregistrement, attendez la fin de toute tâche de synchronisation ou de validation initiale avant de vous fier aux résultats du catalogue ou de l’audit pour cette vue de magasin. L’affichage des suggestions de produits sur la page **[!UICONTROL Catalog Enrichment]** peut prendre jusqu’à 24 heures.

Pour supprimer une configuration de vue de magasin, développez cette entrée et cliquez sur **[!UICONTROL Delete]**.

#### Descriptions des champs {#commerce-connection-fields}

Les champs obligatoires sont marqués d’un astérisque (*) sur le formulaire **[!UICONTROL Commerce Configuration]**.

| Champ | Obligatoire | Description |
| --- | --- | --- |
| URL de la vue Boutique | Oui | URL correspondant à la vue du magasin (par exemple, `https://brand.example.com/fr/`). |
| Identifiant de l’environnement | Oui | Identifiant unique de l’environnement [!DNL Adobe Commerce] auquel la connexion accède. |
| Code du site web | Oui | Code du site web du site web Commerce. |
| Code de magasin | Oui | Code de magasin du site web Commerce. |
| Code d’affichage du magasin | Oui | Affichage de la boutique du site web de Commerce. |
| Nom d’hôte | Non | Nom d’hôte de votre instance [!DNL Adobe Commerce]. |
| Clé API | Non | Clé d’authentification utilisée pour accéder en toute sécurité aux API [!DNL Adobe Commerce]. Traitez-le comme n’importe quelles informations d’identification de production. |

### Vérifier et appliquer l’enrichissement du catalogue {#review-and-apply}

Une fois l’enrichissement du catalogue activé et configuré, des suggestions de produits s’affichent dans l’onglet **[!UICONTROL Agentic Opportunities]** . À partir de là, vous pouvez examiner les suggestions et appliquer les mises à jour approuvées aux noms de produit et aux descriptions longues de votre catalogue Commerce.

L’enrichissement du catalogue utilise les vues de workflow suivantes :

- **[!UICONTROL Current Suggestions]** : éléments nouveaux ou actifs à vérifier.
- **[!UICONTROL Fixed Suggestions]** : éléments déjà appliqués ou résolus.
- **[!UICONTROL Ignored Suggestions]** : éléments que vous avez intentionnellement exclus de l’action.

![Enrichissement du catalogue](./assets/agentic-opportunities.png)

### Déployer les suggestions approuvées {#review-deploy-catalog}

Pour déployer des suggestions approuvées :

1. Sélectionnez **[!UICONTROL Current Suggestions]**.
1. Cliquez sur le contrôle de développement de la ligne URL ou SKU pour afficher les mises à jour proposées du nom et de la description du produit.
1. Examinez la suggestion et vérifiez qu’elle correspond à votre stratégie de marchandisage et d’optimisation pour les moteurs de recherche.

Vous pouvez modifier une suggestion avant de la déployer ou la déplacer vers **[!UICONTROL Ignored Suggestions]** si elle ne correspond pas à votre stratégie.

1. Sélectionnez la ligne de l’URL ou du SKU à mettre à jour.
1. Cliquez sur **[!UICONTROL Deploy optimizations]** et confirmez.

Les modifications de nom et de description approuvées sont enregistrées dans votre catalogue [!DNL Adobe Commerce] comme les autres mises à jour de produits.

>[!IMPORTANT]
>
>Traiter chaque mise à jour appliquée comme une modification du catalogue de production. Utilisez vos pratiques normales de contrôle des modifications, d’évaluation et d’assurance qualité. Appliquez les mises à jour uniquement après que les parties prenantes du merchandising et du SEO se sont mises d’accord sur la copie finale.

Après avoir appliqué une mise à jour, les suggestions sont déplacées vers les **[!UICONTROL Fixed Suggestions]** avec un statut **Marqué comme fixe**.

## Vérifier l’enrichissement dans l’administrateur {#verify-in-admin}

**Pour vérifier l’enrichissement du catalogue appliqué :**

1. Accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]** dans l’Administration Commerce.
1. Utilisez des filtres et le sélecteur de **[!UICONTROL Store View]** selon vos besoins (par exemple, **[!UICONTROL Default Store View]**).
1. Recherchez le SKU.
1. Ouvrez le produit en mode d’édition.

   Le formulaire de produit affiche le nom et/ou la description enrichis du produit.

   ![Nom de produit enrichi](./assets/enriched-product-name.png)

1. Facultatif : sélectionnez **[!UICONTROL Override Catalog Agent provided Product Name]** si vous souhaitez conserver un nom saisi manuellement à la place.

   Les remplacements manuels affectent la manière dont les suggestions restent synchronisées avec le catalogue. Pour plus d’informations, voir [Remplacement manuel dans l’administrateur](#manual-override-in-the-admin).

1. Développez la section **[!UICONTROL Content]** et recherchez le champ de description .

   La description enrichie s’affiche lorsque vous appliquez des modifications de description.

   ![Enrichir la description du produit](./assets/enrich-product-description.png)

1. Facultatif : sélectionnez **[!UICONTROL Override Catalog Agent provided Description]** si vous souhaitez conserver une description saisie manuellement à la place.

Les remplacements manuels affectent la manière dont les suggestions restent synchronisées avec le catalogue. Pour plus d’informations, voir [Remplacement manuel dans l’administrateur](#manual-override-in-the-admin).

## Vérifier l’enrichissement sur le storefront {#verify-storefront}

**Pour vérifier l’enrichissement sur le storefront :**

1. Recherchez le SKU sur votre storefront.
1. Ouvrez la page du produit.
1. Vérifiez que le nom et la description du produit correspondent à ce que vous avez approuvé.

   Les enrichissements peuvent prendre un certain temps avant d’apparaître sur votre storefront.

1. Vérifiez que les régions qui affichent la description longue correspondent à ce que vous avez approuvé.
1. Facultatif : confirmez les canaux en aval qui consomment les mêmes attributs de catalogue, le cas échéant en fonction de votre déploiement.

## Remplacements, ingestion et suggestions obsolètes {#overrides-ingestion}

Après la mise à jour du nom ou de la description d’un produit par l’enrichissement du catalogue, d’autres systèmes d’ingestion peuvent modifier les mêmes champs. Par exemple, les appels API REST, les imports de fichiers CSV et les flux PIM.

### Valeur d’origine réingérée {#original-value-reingested}

Si un processus externe écrit le nom ou la description d’origine (la valeur qui existait avant l’application de l’enrichissement), Commerce continue à honorer la valeur enrichie de ce champ conformément aux règles d’enrichissement du catalogue. La suggestion peut ne pas revenir automatiquement sur la base de cette seule ingestion.

### Nouvelle valeur réingérée {#new-value-reingested}

Si le processus externe envoie une nouvelle valeur qui n’est pas une répétition du texte de préenrichissement, Commerce respecte la nouvelle valeur de catalogue. Par exemple, le changement de nom de « Red Shoes » en « Iconic Red Shoes » remplace la valeur enrichie. La suggestion d’enrichissement associée est généralement marquée comme *obsolète* car le catalogue dynamique ne correspond plus au contexte de la suggestion.

### Remplacement manuel dans l’administrateur {#manual-override-in-the-admin}

Si vous modifiez manuellement le nom ou la description du produit dans l’administration [!DNL Adobe Commerce] :

- La valeur Admin est sélectionnée en tant que système d’enregistrement pour cette modification manuelle.
- La suggestion d’enrichissement est marquée *Obsolète*.
- Le workflow de suggestions revient au statut d’origine de cet élément afin que vous puissiez réinitialiser ou accepter une nouvelle suggestion si l’analyse s’exécute à nouveau.

Ces règles vous aident à savoir si l’enrichissement du catalogue, les flux d’ingestion ou les modifications administratives font autorité lorsque plusieurs canaux touchent le même SKU.

## Limites et considérations {#limits}

- L’enrichissement s’applique uniquement aux noms de produit et aux descriptions longues. Elle ne modifie pas la disposition du PDP, les widgets ou tout autre contenu de storefront au niveau de la page.
- La taille des catalogues et le nombre élevé d’URL peuvent avoir une incidence sur la rapidité avec laquelle l’analyse est terminée et le nombre de suggestions qui s’affichent en même temps.
- Des suggestions pertinentes supposent que les robots LLM peuvent accéder aux URL des produits qui vous intéressent. Les règles robotisées, l’authentification, le blocage géographique et une personnalisation poussée peuvent réduire la couverture.

## Bonnes pratiques {#best-practices}

- Documentez la propriété du système pour le nom et la description du produit afin que les tâches PIM ou de flux n’entrent pas involontairement en conflit avec l’enrichissement du catalogue.
- Coordonnez-vous avec les équipes d’optimisation du moteur de recherche et de marque avant d’appliquer des titres ou des descriptions en bloc.
- resynchronisez ou analysez-les après des importations de catalogues majeures afin que les suggestions reflètent l’état actuel du catalogue.

<!--## Examples This section will provide examples of what enrichment before/after looks like:-->
