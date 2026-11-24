---
title: Enrichissement du catalogue
description: Utilisez l’enrichissement du catalogue [!DNL Adobe Commerce] pour examiner la copie de produit suggérée par l’IA, créer des tâches d’enrichissement et déployer des mises à jour approuvées pour la découverte de LLM et d’IA.
role: Admin, User, Leader
recommendations: noCatalog
touch: true
badgePaas or on-premises: label="Cloud or on-premises only" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed Cloud or on-premises infrastructure) and on-premises projects only."
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
source-git-commit: b2a1abb72839717a7249e9a34b13266b8e384189
workflow-type: tm+mt
source-wordcount: '1976'
ht-degree: 0%
---
# Enrichissement du catalogue

L’enrichissement du catalogue est une fonctionnalité native de [!DNL Adobe Commerce] qui vous permet d’améliorer les noms de produit et les descriptions longues afin que votre catalogue soit représenté plus précisément lorsque les acheteurs utilisent des LLM et des assistants d’IA pour la recherche et la découverte de produits.

## Fonctionnement {#how-it-works}

Votre catalogue de produits [!DNL Adobe Commerce] est le système d&#39;enregistrement des données de produits : noms, descriptions, attributs, prix et inventaire. [!DNL Adobe Commerce] connecte les données de catalogue actives aux expériences Adobe AI. À partir de là, l’agent de catalogue peut identifier les lacunes dans les noms de produits et les descriptions longues, proposer des améliorations et écrire les modifications approuvées dans Commerce afin que vous puissiez les examiner dans l’administration Commerce.

Avec l’enrichissement de catalogue, vous pouvez :

- Identifiez les lacunes et les incohérences dans les noms de produits et les descriptions longues qui affectent la façon dont les LLM interprètent vos produits.
- Examen des améliorations suggérées avec contexte à l&#39;appui, y compris les justifications et les comparaisons avant et après.
- Appliquez les mises à jour approuvées directement au catalogue Commerce afin que l’administrateur, le storefront et les autres canaux qui lisent ces champs restent alignés.

Comme les noms de produit et les descriptions longues résident dans Commerce, l’amélioration de la copie peut bénéficier à chaque canal qui utilise ces données de produit. L’avantage dépend de la façon dont vos systèmes sont actualisés et du moment où ils le sont.

| Direction | Objectif |
| --- | --- |
| Catalogue Commerce -> analyse | Les signaux de trafic de catalogue et Agentic révèlent des opportunités de suggestions d’enrichissement. |
| Enrichissement -> Catalogue Commerce | Après approbation d’une mise à jour, les modifications apportées au nom et à la description du produit sont enregistrées dans le catalogue Commerce afin que l’administrateur et le storefront reflètent les valeurs optimisées. |

### Accéder à l’enrichissement du catalogue

Avant de commencer, passez en revue les [conditions préalables à la découverte de produit par l’IA](prerequisites.md) spécifiques au déploiement. Une fois la configuration de votre plateforme Commerce terminée, accédez à **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]** dans l’administration.

![Tableau De Bord D’Enrichissement Du Catalogue](assets/catalog-enrich-dashboard.png){zoomable="yes"}

L’espace de travail Enrichissement du catalogue comprend les onglets **[!UICONTROL Optimizations]**, **[!UICONTROL Brand governance]** et **[!UICONTROL Settings]**.

- Utilisez l’onglet **[!UICONTROL Optimizations]** pour consulter les signaux de découverte basés sur le trafic d’agent et gérer les tâches d’enrichissement.
- Utilisez l’onglet **[!UICONTROL Brand Governance]** pour [définir les exigences](brand-governance.md) pour les noms et descriptions de produits générés par [!DNL Commerce Catalog Agent].
- Utilisez l’onglet **[!UICONTROL Settings]** pour [connecter votre instance Commerce](settings.md) à la découverte de produit IA.

L’extension partagée active également l’enrichissement PDP, qui dispose d’un workflow distinct pour exposer les faits de produit structurés aux agents d’IA. Voir [enrichissement de la page des détails du produit](pdp-enrichment.md).

## Deux chemins d’accès pour les enrichissements de catalogue

Il existe deux chemins pour recevoir les enrichissements du catalogue :

- **Trafic agentic** - Ce type d’enrichissement démarre automatiquement 24 à 48 heures après la configuration de l’instance Commerce et affiche les résultats dans l’onglet **Optimisations**.
- **Gestionnaire d’enrichissement** - Les commerçants configurent ces enrichissements lorsqu’ils cliquent sur le bouton **[!UICONTROL Create enrichment]** et sélectionnent manuellement les SKU à enrichir. En savoir plus sur le [gestionnaire d’enrichissement](#create-an-enrichment-job).

### Vérifier et appliquer l’enrichissement du catalogue {#review-and-apply}

Une fois que l’enrichissement du catalogue est activé et configuré, utilisez l’onglet **[!UICONTROL Optimizations]** pour consulter les informations sur le trafic de recherche et d’agent et gérer les tâches d’enrichissement.

### Vérifier le trafic mensuel de l’agent

Chaque audit de trafic mensuel par un agent identifie les SKU à trafic élevé et met à disposition un lot recommandé. Les optimisations pour la révision sont automatiquement générées pour les SKU à trafic élevé d’agents. Ces optimisations sont générées automatiquement en fonction de votre règle de gouvernance « Par défaut ». Les cartes mensuelles affichent le nombre de produits, les visites d’agents AI et le statut de la tâche. Le trafic d’agents et les lots auto-sélectionnés utilisent le même workflow de sélection de règles, de confirmation, d’exécution, de révision et de déploiement.

### Tâches de révision nécessitant une attention particulière

La section **[!UICONTROL Needs your attention]** met en évidence les tâches nécessitant une action, y compris les tâches terminées prêtes à être révisées. Ouvrez une tâche terminée pour examiner ses modifications de produit proposées avant le déploiement.

### Rechercher des tâches

Le tableau **[!UICONTROL All jobs]** répertorie chaque ID de tâche, nom, origine, nombre de SKU, règle utilisée, heure de début et statut. Les origines indiquent si un lot a été auto-sélectionné ou recommandé à partir du trafic d’agent. Suivre le statut de traitement comme **[!UICONTROL Queued]**, **[!UICONTROL Running]**, **[!UICONTROL Completed]** ou **[!UICONTROL Failed]**. Dans l’espace de travail Optimisations , ces tâches peuvent également apparaître sous la forme **[!UICONTROL Generating]** pendant leur exécution, **[!UICONTROL Ready to review]** une fois la génération terminée et **[!UICONTROL Deployed]** une fois les modifications approuvées déployées. Vous pouvez exécuter plusieurs tâches simultanément. Réessayer un traitement ayant échoué avec **[!UICONTROL Retry]**.

### Création d’une tâche d’enrichissement

**Pour créer un enrichissement de catalogue :**

![Créer Un Enrichissement De Catalogue](./assets/create-cat-enrich.png){zoomable="yes"}

1. Dans **[!UICONTROL Optimizations]**, cliquez sur **[!UICONTROL Create enrichment]**.
1. Saisissez un **nom de l’enrichissement**, par exemple « Black Friday 2026 ».
1. Sélectionnez la **catégorie**, par exemple « Café ».
1. Sélectionnez le **Jeu d’attributs**, par exemple « Accessoires ».
1. Sélectionnez le **type de produit**, par exemple « Produit simple ».
1. Sélectionnez la **gamme de prix**.
1. Cliquez sur **[!UICONTROL Apply filters]**.

   Vous pouvez prévisualiser les produits qui correspondent à vos critères d’enrichissement et cliquer sur **Personnaliser** pour étendre la portée des produits que vous souhaitez enrichir.

1. Cliquez sur **[!DNL Next]** et prévisualisez la [règle de gouvernance](brand-governance.md) appliquée à votre enrichissement.
1. Cliquez sur **[!DNL Next]** pour confirmer les produits spécifiques que vous souhaitez enrichir.
1. Cliquez sur **[!DNL Run enrichment]**.

   La tâche d’enrichissement s’exécute et s’affiche dans le tableau Optimisations . Une fois l’exécution terminée, vous pouvez [examiner et déployer](#review-deploy-catalog) les optimisations.

### Vérification et déploiement d’une tâche d’enrichissement {#review-deploy-catalog}

Ouvrez une tâche d’enrichissement.

![Liste des URL d’enrichissement de catalogue](./assets/catalog-enrich-urls.png){zoomable="yes"}

Le tableau **URL avec suggestions** répertorie tous les produits avec des opportunités d’enrichissement. Pour chaque produit, vous pouvez :

- **Développez la ligne** pour afficher l’analyse de l’IA et l’enrichissement proposé.
- **Modifiez** le nom ou la description du produit proposé avant l&#39;application, afin de vous conformer aux directives de votre marque en matière de voix et de marchandisage.
- **Déployez l’optimisation** pour les produits que vous souhaitez enrichir et publiez-la directement dans votre catalogue Adobe Commerce.
- **Marquer comme corrigé** une fois l&#39;enrichissement vérifié et appliqué.
- **Ignorer** les suggestions qui ne sont pas pertinentes pour votre stratégie de catalogue.

Les suggestions sont organisées en trois vues : **Suggestions actuelles**, **Suggestions fixes** et **Suggestions ignorées**. Une fois qu’un enrichissement est appliqué, il passe aux Suggestions fixes avec un statut **Appliqué** et une action **Afficher dans le catalogue** pour vérifier la mise à jour dans Adobe Commerce. Les enrichissements appliqués peuvent être restaurés à tout moment, en restaurant le nom et la description d’origine du produit.

## Vérifier l’enrichissement dans l’administrateur {#verify-in-admin}

**Pour vérifier l&#39;enrichissement appliqué du catalogue :**

1. Accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]** dans l’administration Commerce.
1. Utilisez des filtres et le sélecteur **[!UICONTROL Store View]** selon vos besoins (par exemple, **[!UICONTROL Default Store View]**).
1. Recherchez le SKU.
1. Ouvrez le produit en mode d’édition.

   Le formulaire de produit affiche le nom et/ou la description enrichis du produit.

   ![Nom De Produit Enrichi](./assets/enriched-product-name.png){zoomable="yes"}

1. Facultatif : sélectionnez **[!UICONTROL Override Catalog Agent provided Product Name]** si vous souhaitez conserver un nom saisi manuellement à la place.

   Les remplacements manuels affectent la manière dont les suggestions restent synchronisées avec le catalogue. Pour plus d&#39;informations, voir [Remplacement manuel dans l&#39;administrateur](#manual-override-in-the-admin).

1. Développez la section **[!UICONTROL Content]** et recherchez le champ de description.

   La description enrichie s’affiche lorsque vous appliquez des modifications de description.

   ![Enrichir La Description Du Produit](./assets/enrich-product-description.png){zoomable="yes"}

1. Facultatif : sélectionnez **[!UICONTROL Override Catalog Agent provided Description]** si vous souhaitez conserver une description saisie manuellement à la place.

Les remplacements manuels affectent la manière dont les suggestions restent synchronisées avec le catalogue. Pour plus d&#39;informations, voir [Remplacement manuel dans l&#39;administrateur](#manual-override-in-the-admin).

## Vérifier l’enrichissement sur le storefront {#verify-storefront}

**Pour vérifier l&#39;enrichissement sur le storefront :**

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

Si le processus externe envoie une nouvelle valeur qui n’est pas une répétition du texte de préenrichissement, Commerce respecte la nouvelle valeur de catalogue. Par exemple, le changement de nom de « Red Shoes » en « Iconic Red Shoes » remplace la valeur enrichie. La suggestion d’enrichissement associée est généralement marquée comme *Obsolète*, car le catalogue dynamique ne correspond plus au contexte de la suggestion.

### Remplacement manuel dans l’administrateur {#manual-override-in-the-admin}

Si vous modifiez manuellement le nom ou la description du produit dans l’administration [!DNL Adobe Commerce] :

- La valeur Admin est sélectionnée en tant que système d’enregistrement pour cette modification manuelle.
- La suggestion d’enrichissement est marquée comme *Obsolète*.
- Le workflow de suggestions revient au statut d’origine de cet élément afin que vous puissiez réinitialiser ou accepter une nouvelle suggestion si l’analyse s’exécute à nouveau.

Ces règles vous aident à savoir si l’enrichissement du catalogue, les flux d’ingestion ou les modifications administratives font autorité lorsque plusieurs canaux touchent le même SKU.

## Limites et considérations {#limits}

- L’enrichissement s’applique uniquement aux noms de produit et aux descriptions longues. Elle ne modifie pas la mise en page des détails du produit, les widgets ou tout autre contenu de storefront au niveau de la page.
- La taille des catalogues et le nombre élevé d’URL peuvent avoir une incidence sur la rapidité avec laquelle l’analyse est terminée et le nombre de suggestions qui s’affichent en même temps.
- Des suggestions pertinentes supposent que les robots LLM peuvent accéder aux URL des produits qui vous intéressent. Les règles robotisées, l’authentification, le blocage géographique et une personnalisation poussée peuvent réduire la couverture.

## Bonnes pratiques {#best-practices}

- Documentez la propriété du système pour le nom et la description du produit afin que les tâches PIM ou de flux n’entrent pas involontairement en conflit avec l’enrichissement du catalogue.
- Coordonnez-vous avec les équipes d’optimisation du moteur de recherche et de marque avant d’appliquer des titres ou des descriptions en bloc.
- resynchronisez ou analysez-les après des importations de catalogues majeures afin que les suggestions reflètent l’état actuel du catalogue.

## Exemples

Les exemples suivants montrent comment l’enrichissement du catalogue transforme les attributs techniques bruts en une copie de produit narrative axée sur l’acheteur que les gestionnaires de contenu peuvent utiliser pour répondre aux questions d’achat.

### Exemple : produit café avec des attributs techniques

Un catalogue de retailer de café stocke uniquement les spécifications techniques d’un produit de grain de café torréfié moyen : variété de grain, région d’origine, méthode de traitement, niveau de torréfaction et plage d’altitude. Ces champs décrivent le produit, mais ne communiquent pas sa valeur à un acheteur, de sorte qu&#39;un assistant d&#39;IA a peu de choses à gérer pour répondre à une question comme « quel café a une saveur lisse et peu acide ? »

L’enrichissement du catalogue lit les attributs techniques et les raisons de l’interaction pour déduire des caractéristiques pertinentes pour l’acheteur :

| Attribut technique | Caractéristique déduite | Raisonnement |
| --- | --- | --- |
| Procédé au miel, rôti Medium | Faible acidité | Le mucilage des fruits laissé sur la fève pendant le traitement du miel supprime l&#39;acidité, et le rôti moyen décompose les composés acides résiduels. |
| Processus de miel, Arabica, Medium Roast | Arôme noisette | Les sucres de fruits du mucilage se combinent avec les notes naturelles de noix d&#39;Arabica, amplifiées au rôti moyen. |
| Procédé au miel, Arabica | Sensation de bouche riche et crémeuse | Les huiles absorbées à partir du mucilage pendant le séchage ajoutent viscosité et corps. |
| Processus de miel, Altitude 900-1200m | Sous-tons caramel | Les haricots plus denses et de haute altitude développent des sucres plus complexes, raffinés par la transformation du miel. |

L’enrichissement du catalogue applique ces caractéristiques déduites à la copie du produit :

- **Avant** : « Medium Roast Coffee Beans - Arabica, Brazil Minas Gerais, Miel Process, 900-1200m »
- **Après** : « Les haricots Arabica cultivés à 900-1200 m dans le Minas Gerais au Brésil, traités au miel et grillés à point, développent une sensation en bouche naturellement douce et crémeuse avec un caractère de noisette distinct, des nuances de caramel et une faible acidité. Un café de spécialité cohérent et accessible que l’on peut déguster à jamais. »

Le nom et la description mis à jour sont enregistrés directement dans le catalogue Commerce. De ce fait, le storefront, les flux LLM et les autres canaux qui lisent ces champs reflètent la même copie enrichie.

### Exemple : configuration de meubles modulaires

Un retailer de meubles vend un canapé modulaire en section où la description du produit répertorie uniquement les codes de configuration et le nom du tissu, par exemple `6 Standard Seats + 6 Standard Sides in Sapphire Navy Corded Velvet`. Ce raccourci est compréhensible pour un client régulier, mais il donne à un assistant d’IA peu de contexte sur le fonctionnement du produit ou sur ce qui le rend durable ou confortable.

L’enrichissement du catalogue développe les attributs de configuration et de fabric dans une description narrative qui explique ce que fait chaque composant et pourquoi il est important pour un acheteur :

- **Avant** : « 6 sièges standard + 6 côtés standard en velours à cordon Sapphire Navy »
- **Après** : « Cette configuration comprend 6 ensembles d&#39;inserts de siège standard et 6 inserts latéraux standard qui fonctionnent de manière interchangeable comme des bras ou des dossiers, formant les blocs de construction modulaires de votre disposition. Chaque siège est doté d&#39;une mousse standard avec trois couches haute densité conçues pour préserver la portance et résister à l&#39;affaissement. La housse de velours à cordon Sapphire Navy est aussi durable que luxueuse, avec des cordons texturés qui créent une brillance subtile et une sensation douce et moelleuse. Les couvertures sont cousues à la main pour un look précis et sur mesure et sont lavables en machine et modifiables, afin que votre section puisse évoluer avec votre espace. »

Comme la description enrichie est réécrite dans le catalogue Commerce, elle est disponible pour les robots d’IA qui explorent à la page des détails du produit ainsi que pour tout canal ou flux en aval qui consomme les données du catalogue du produit, sans modifier la mise en page ou la conception que les acheteurs voient sur la page.
