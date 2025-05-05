---
title: Préparation du HIPAA pour Adobe Commerce
description: Découvrez comment ajouter l’extension Adobe Commerce HIPAA-Ready et obtenir des fonctionnalités supplémentaires qui vous permettent de respecter vos obligations HIPAA.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '2392'
ht-degree: 1%

---

# Préparation du HIPAA pour Adobe Commerce

>[!IMPORTANT]
>
>**Clause de non-responsabilité**<br/>
>Ces informations sont destinées à aider les clients Adobe à répondre à leurs questions concernant les services conformes à la norme HIPAA d’Adobe. Il ne s&#39;agit pas d&#39;un avis juridique. Les commerçants doivent consulter leur propre service juridique pour connaître leurs obligations en vertu de la loi HIPAA ainsi que l’utilisation et la configuration appropriées des produits Adobe.

>[!BEGINSHADEBOX]

**Health Insurance Portability and Accountability Act (HIPAA) (loi sur la responsabilité et la portabilité de l’assurance maladie)**

La Health Insurance Portability and Accountability Act (HIPAA) est la principale loi fédérale sur la confidentialité des soins de santé aux États-Unis et est appliquée par le Department of Health and Human Services (HHS) des États-Unis. La loi HIPAA s’applique aux _entités couvertes_ (telles que les prestataires de soins de santé, les assureurs et les chambres de compensation) et aux _entreprises associées_ (telles que les entités qui fournissent des services aux entités couvertes). Les exigences de la loi HIPAA sont définies selon trois règles distinctes : règle de confidentialité, règle de sécurité et règle de notification de violation. Adobe agit en tant qu’associé commercial pour certains produits, qu’Adobe classe comme « services conformes à la norme HIPAA ». Les données réglementées par la loi HIPAA sont appelées _informations de santé protégées_ ou ISP. Les ISP sont un sous-ensemble d&#39;informations sur la santé qui (1) est créé ou reçu par un prestataire de soins de santé, un régime de soins de santé ou un centre d&#39;échange de soins de santé, (2) se rapporte à la santé ou à l&#39;état physique ou mental passé, présent ou futur d&#39;une personne, à la prestation de soins de santé à une personne, ou au paiement passé, présent ou futur de la prestation de soins de santé à une personne, et (3) identifie la personne ou à l&#39;égard duquel il existe une base raisonnable de croire que les informations peuvent être utilisées pour identifier la personne. Les règles de confidentialité et de sécurité de la loi HIPAA exigent qu&#39;une entité couverte obtienne des assurances écrites de la part d&#39;un associé commercial sous la forme d&#39;un accord d&#39;associé commercial, ou BAA, exigeant de l&#39;associé commercial qu&#39;il protège la confidentialité et la sécurité des ISP de l&#39;entité couverte. Pour plus d’informations, voir [Produits et services HIPAA et Adobe](https://www.adobe.com/trust/compliance/hipaa-ready.html) dans le Centre de gestion de la confidentialité d’Adobe.

>[!ENDSHADEBOX]

## Adobe Commerce conforme à la norme HIPAA

L’extension Adobe Commerce HIPAA-Ready ajoute des fonctionnalités supplémentaires aux installations d’Adobe Commerce qui permettent aux commerçants de respecter leurs obligations HIPAA respectives.

L’extension Adobe Commerce HIPAA-Ready `magento/hipaa-ee` est disponible pour Adobe Commerce sur les infrastructures cloud ou les projets Adobe Managed Services. Le processus d’installation conforme à la norme HIPAA d’Adobe Commerce désactive certains services et fonctionnalités natifs pour les mettre en conformité avec les exigences de la norme HIPAA. Voir [Services et fonctionnalités désactivés](#disabled-services-and-features).

>[!NOTE]
>
>Seuls les commerçants qui ont acheté le module complémentaire de soins de santé pour Adobe Commerce ont accès aux fonctionnalités conformes à la loi HIPAA.

*Ces documents sont fournis uniquement à titre d’information. La fourniture de ces informations ne confère au destinataire aucun droit contractuel ou autre. Bien que des efforts aient été faits pour assurer l&#39;exactitude des renseignements à la date où ils ont été fournis, aucune déclaration n&#39;est faite selon laquelle ces renseignements sont exacts et complets. Adobe n’engage aucune obligation de mettre à jour ces informations à mesure que la loi ou les produits Adobe évoluent. En outre, ce document ne doit être distribué à aucune autre partie que le destinataire prévu sans le consentement écrit d’Adobe.*

## Configuration requise

Le tableau suivant montre la compatibilité entre les versions d’Adobe Commerce et l’extension conforme à la loi HIPAA :

| Adobe Commerce | Pris en charge | Remarques |
|----------------|-----------|-------|
| 2.4.7-p4 - 2.4.7-p5 | 1.2.0 | La prise en charge d’ 2.4.7-p4 nécessite un [correctif](https://experienceleague.adobe.com/fr/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/hotfix-for-hipaa-package-1-2-0-compatibility-with-adobe-commerce-2-4-7-p4) |
| 2.4.6-p9 - 2.4.6-p10 | 1.2.0 | |
| 2.4.6-p8 | 1.1.0 | La prise en charge des [services de données](#adobe-commerce-services) a été introduite dans la version 1.1.0 |
| 2.4.6-p3 - 2.4.6-p7 | 1.0.0 | |

>[!IMPORTANT]
>
>- L’extension conforme à la loi HIPAA n’est disponible que pour Adobe Commerce sur les projets cloud ou Adobe Commerce Managed Services.
>- L’extension est disponible en tant que métapaquet Compositeur depuis `repo.magento.com`.
>- L’accès aux fonctionnalités conformes à la loi HIPAA nécessite le module complémentaire de soins de santé pour Adobe Commerce.
>- les versions bêta d’Adobe Commerce ne sont pas prises en charge.

## Installation

**Prérequis**

>[!BEGINSHADEBOX]

- Adobe a configuré votre compte Adobe Commerce pour accéder à l’extension conforme à la loi HIPAA.
- Accédez à [repo.magento.com](https://repo.magento.com) pour installer l’extension. Pour la génération des clés et l’obtention des droits nécessaires, voir [ Obtenir vos clés d’authentification ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html?lang=fr).

>[!ENDSHADEBOX]

Installez la dernière version de l’extension Adobe HIPAA-Ready Services (`magento/hipaa-ee`) sur une instance qui exécute Adobe Commerce versions 2.4.7-p5 ou 2.4.6-p3 à 2.4.6-p8. L’extension est fournie en tant que métapaquet de compositeur à partir du référentiel [repo.magento.com](https://repo.magento.com). Le métapaquet comprend l’ensemble des modules qui activent les fonctionnalités HIPAA pour une instance Adobe Commerce.

>[!NOTE]
>
>Pour vous assurer que les données d’événement de back-office envoyées à Experience Platform sont conformes à la loi HIPAA, consultez le guide [Data Connection extension guide](https://experienceleague.adobe.com/fr/docs/commerce/data-connection/fundamentals/install#install-the-data-services-hipaa-extension).

1. Sur votre station de travail locale, accédez au répertoire du projet d’infrastructure cloud d’Adobe Commerce.

   >[!NOTE]
   >
   >Pour plus d’informations sur la gestion locale des environnements de projet Commerce, voir [Gestion des branches avec l’interface de ligne de commande](https://experienceleague.adobe.com/fr/docs/commerce-cloud-service/user-guide/develop/cli-branches) dans le _Guide d’utilisation d’Adobe Commerce sur les infrastructures cloud_.

1. Extrayez la branche d’environnement pour effectuer la mise à jour à l’aide de l’interface de ligne de commande Adobe Commerce Cloud.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Ajoutez le `magento/hipaa-ee` de métapaquet à la configuration du compositeur à l’aide de l’interface de ligne de commande du compositeur.

   ```shell
   composer require "magento/hipaa-ee" --no-update
   ```

1. Mettez à jour les dépendances de package.

   ```shell
   composer update "magento/hipaa-ee"
   ```

1. Ajoutez, validez et envoyez le code mis à jour à l’environnement cloud.

   ```shell
   git add -A
   git commit -m "Add HIPAA-Ready Services modules"
   git push origin <branch-name>
   ```

   L’envoi des mises à jour lance le processus de déploiement cloud de [Commerce](https://experienceleague.adobe.com/fr/docs/commerce-cloud-service/user-guide/develop/deploy/process) pour appliquer les modifications. Vérifiez le statut du déploiement dans le [journal de déploiement](https://experienceleague.adobe.com/fr/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

### Vérification de l’installation

Une fois les mises à jour déployées, vérifiez que l’extension `Hipaa*` est installée

1. Utilisez SSH pour vous connecter à l’environnement cloud distant.

   ```shell
   magento-cloud ssh
   ```

1. À partir de la ligne de commande, utilisez l’interface de ligne de commande Adobe Commerce pour vérifier le statut du module.

   ```shell
   bin/magento module:status
   ```

1. Vérifiez que les modules HIPAA sont inclus dans la liste des modules activés :

   ```text
   List of enabled modules:
   <truncated for brevity>
   Magento_HipaaAnalytics
   Magento_HipaaCheckout
   Magento_HipaaLogging
   Magento_HipaaScheduledImportExport
   Magento_HipaaAdminLogging
   Magento_HipaaCustomerLogging
   Magento_HipaaNewsletter
   Magento_HipaaImportExport
   Magento_HipaaApiLogging
   Magento_HipaaSales
   Magento_HipaaCustomer
   <truncated for brevity>
   ```

   Tous les modules dotés du préfixe `Magento_Hipaa` doivent se trouver dans la section Modules activés .

## Améliorations des fonctionnalités pour la conformité à la norme HIPAA

L’extension `magento/hipaa-ee` apporte des modifications et des améliorations au produit Commerce de base. Les sections suivantes fournissent des détails sur ces modifications et sur la manière dont elles modifient le produit de base.

### Journaux d’action

La journalisation d’audit est une exigence de la loi HIPAA. Dans Adobe Commerce, la fonctionnalité [Journaux d’action](../../systems/action-log.md) enregistre chaque modification apportée par un utilisateur administrateur qui travaille dans votre boutique. Pour répondre aux exigences de la loi HIPAA pour le journal d’audit, la fonctionnalité a été mise à jour afin d’enregistrer toutes les actions des utilisateurs administrateurs et des clients effectuées via l’interface utilisateur d’administration et les appels API.

Les journaux d’actions capturent également des événements lorsque les services Adobe accèdent aux données de votre boutique. Vous pouvez identifier ces événements en filtrant sur l’action « Données envoyées en dehors » dans le rapport Journaux d’actions .

#### Rapport Journaux d’action

La grille de rapport _Journaux d’actions_ (**[!UICONTROL System]** > Journaux d’actions > Rapport) est modifiée pour s’adapter aux actions du client effectuées via l’interface utilisateur d’administration et l’API.

1. Ajout de deux colonnes :
   - ***Source*** : affiche l’emplacement où l’action a été effectuée.
Valeurs : `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***Type de client*** : affiche le type de client.
Valeurs : client | Admin | Intégration

2. Colonne ***Nom d’utilisateur*** renommée ***Identifiant client***
   - ***Identifiant client*** : affiche l’ID de connexion de l’utilisateur qui a exécuté l’action.
Valeurs :
      - un e-mail si le type de client est Client ;
      - un nom d’utilisateur si le type de client est Admin.
      - un nom si le type de client est Intégration.

3. Colonne ***Nom complet de l’action*** renommée ***Target***
   - ***Target*** : affiche le nom de l’action.
Valeurs :
      - un point d’entrée si Source est une API REST ou une API SOAP
      - une requête ou un nom de mutation si une API GraphQL
      - Nom d’action d’une interface utilisateur d’administration ou d’une interface utilisateur client.

#### Configuration des actions d’administration pour la journalisation

Cette fonctionnalité n’est pas disponible, car toutes les actions doivent être enregistrées par défaut.

### HIPAA - Restriction des résultats de recherche de clients

La fonctionnalité de restriction des résultats de recherche client HIPAA d’Adobe Commerce assure la conformité aux réglementations HIPAA en limitant l’accès aux informations de santé protégées (ISP) et aux informations d’identification personnelle (PII). Cette fonctionnalité limite la possibilité de rechercher et d’afficher des enregistrements de clients en fonction des rôles utilisateur, de sorte que seuls les utilisateurs autorisés puissent accéder à ces informations.

#### Fonctionnalités clés

- **Restrictions de recherche** : les utilisateurs ne disposant pas des rôles nécessaires ne peuvent pas rechercher ni afficher les enregistrements de clients.
- **Recherche d’accès obligatoire** : contrairement au comportement par défaut d’Adobe Commerce, il n’est pas possible d’afficher les informations client sans effectuer de recherche. Ainsi, les utilisateurs doivent connaître les détails spécifiques d’un client pour localiser leurs informations.
- **Résultats de recherche limités** : les résultats de recherche correspondant aux critères sont limités à 10 enregistrements, ce qui garantit que seul un nombre gérable d’enregistrements est affiché à la fois.
- **Nombre minimum de filtres** : les utilisateurs doivent appliquer au moins trois filtres (e-mail, nom de famille et état, par exemple) pour effectuer une recherche, en veillant à ce que les recherches soient spécifiques et ciblées.
- **Notifications de filtre** : lorsque les restrictions de recherche sont activées, les utilisateurs sont avertis d’appliquer des filtres pour affiner les résultats de leur recherche.

#### Configuration

La configuration permettant de limiter le nombre de clients dans les résultats de la recherche se trouve dans le panneau d’administration sous **[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Advanced]** > **[!UICONTROL Admin]** > **[!UICONTROL Admin Grids]**. Cette configuration est activée par défaut lors de l’installation de l’extension `hipaa-ee`.

- **Limiter le nombre de clients dans la grille** : ce paramètre permet d’activer ou de désactiver la limitation du nombre de clients affichés dans les résultats de la recherche dans la grille.
- **Limite des résultats de recherche dans la grille du client** : ce paramètre spécifie le nombre maximal d’enregistrements client pouvant être affichés dans les résultats de recherche dans la grille.

#### Zones fonctionnelles affectées

Les grilles Clients de la page Créer une commande d’administration (**[!UICONTROL Sales]** > **[!UICONTROL Orders]** > **[!UICONTROL Create New Order]**) et de la page Clients (**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**) sont affectées par la fonctionnalité de restriction des résultats de recherche.

- Les filtres sont ouverts par défaut.
- Les utilisateurs doivent appliquer au moins trois filtres pour effectuer une recherche.
- Par défaut, les résultats de recherche sont limités à 10 enregistrements.
- S’il existe d’autres enregistrements correspondant aux critères de recherche, les notifications informeront les utilisateurs et utilisatrices de la limite de résultats et de la nécessité d’affiner leur recherche.
- La pagination de grille n’est pas disponible.
- Les résultats de recherche précédents et les filtres appliqués ne sont pas enregistrés lorsque vous quittez la page.

La fonctionnalité de restriction des résultats de recherche s’applique également à l’API REST pour la recherche de clients (`/V1/customers/search`).

- Si aucun filtre n’est appliqué ou si les filtres sont insuffisants, l’API renvoie un message d’erreur indiquant que le nombre de filtres requis est nécessaire pour effectuer une recherche.
- Lorsque suffisamment de filtres sont appliqués par les utilisateurs autorisés, l’API renvoie des résultats dans la limite spécifiée.
- Lorsque les résultats sont limités, un message est ajouté à la réponse indiquant le nombre total d’enregistrements trouvés et la limite actuellement appliquée.

### Importer et exporter des fonctionnalités

Les améliorations apportées aux fonctionnalités d’import et d’export visent à améliorer l’expérience administrative et à offrir une meilleure visibilité sur les actions des utilisateurs et utilisatrices.

>[!NOTE]
>
>Ces ***améliorations ne modifient pas la logique principale d’import et d’export*** mais étendent plutôt la fonctionnalité pour offrir une journalisation plus complète et une attribution des données améliorée. Les fonctionnalités fondamentales de l’import et de l’export restent inchangées. Les utilisateurs peuvent continuer à utiliser les fonctionnalités et les workflows existants sans aucune interruption.

#### Journalisation des actions administratives

L’une des améliorations clés des fonctionnalités d’importation et d’exportation réside dans la journalisation améliorée des actions administratives. Cette amélioration permet d’approfondir les activités associées à l’import et à l’export de données, contribuant ainsi à l’amélioration du suivi et de l’auditabilité. Les actions suivantes sont désormais consignées et reflétées dans la grille **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**:

| Type | Actions |
| ---- | ------- |
| Importer | <ul><li>Un utilisateur administrateur exécute une importation<li>Un utilisateur administrateur télécharge un fichier importé<li>Un utilisateur administrateur télécharge un fichier d’erreur<ul/> |
| Exporter | <ul><li>Un utilisateur administrateur demande<li>Un utilisateur administrateur télécharge un fichier exporté<ul/> |
| Imports/exports planifiés | <ul><li>Un utilisateur administrateur planifie l’exportation.<li>Un utilisateur administrateur modifie une exportation planifiée<li>Un utilisateur administrateur exécute une exportation planifiée<li>Un utilisateur administrateur supprime une exportation planifiée<li>Un utilisateur administrateur planifie une importation<li>Un utilisateur administrateur modifie une importation planifiée<li>Un utilisateur administrateur exécute une importation planifiée<li>Un utilisateur administrateur supprime une importation planifiée<li>Un utilisateur administrateur exécute une suppression en bloc des opérations d’importation/exportation.<ul/> |

### Améliorations de l’affichage et amélioration du filtrage et du tri

Pour offrir aux utilisateurs administrateurs des grilles plus informatives, le service HIPAA-Ready apporte plusieurs améliorations à l’affichage, au filtrage et au tri des données.

#### Historique des imports ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- Filtrage activé pour toutes les colonnes, à l’exception de **[!UICONTROL Imported File]**, **[!UICONTROL Error File]**, **[!UICONTROL Execution Time]** et **[!UICONTROL Summary]**.

#### Exporter ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- Ajout d’une colonne **[!UICONTROL ID]**.
- Ajout d&#39;une colonne **[!UICONTROL Requested At]** (_date et heure de la demande d&#39;export_).
- Ajout d’une colonne **[!UICONTROL User]** (_nom d’utilisateur de l’administrateur qui a effectué la demande_).
- Suppression d’une colonne **[!UICONTROL Action]**.
- Déplacement du lien **[!UICONTROL Download]** vers une colonne **[!UICONTROL File name]** (_comme la grille Historique des imports_).
- Désactivation de l&#39;action de suppression d&#39;un fichier exporté (_pour améliorer le tracking_)
- Tri activé pour toutes les colonnes sauf **[!UICONTROL File name]**.
- Filtrage activé pour toutes les colonnes.

#### Imports et exports planifiés ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- Ajout d’une colonne **[!UICONTROL ID]**.
- Ajout d’une colonne **[!UICONTROL Scheduled At]** (la _date et heure auxquelles l’importation ou l’exportation a été planifiée_).
- Ajout d’une colonne **[!UICONTROL User]** (le _nom d’utilisateur d’un utilisateur administrateur qui a planifié l’importation ou l’exportation_).

## Services et outils conformes à la loi HIPAA

Cette section décrit les services Adobe conformes à la loi HIPAA disponibles avec l’offre HIPAA pour Adobe Commerce. Il décrit également les outils que vous pouvez utiliser pour surveiller les contrôles clés de sécurité et de conformité de votre magasin.

| Service | Production | Évaluation | staging_for_support | Développement |
|---------------------------------------|------------|---------|---------------------|-------------|
| Adobe Commerce avec module complémentaire Healthcare | Oui | Oui | Oui | Non |
| SendGrid | Non | Non | Non | Non |
| AWS Simple Email Service | Oui | Oui | Oui | Non |

### Services Adobe Commerce

Le tableau suivant répertorie les services Adobe Commerce disponibles pour l’offre conforme à la loi HIPAA. Ces services comprennent, sans s’y limiter :

| Service | Hors production | Production |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|------------|
| [Adobe Developer App Builder](https://developer.adobe.com/app-builder/docs/overview/) | Oui | Oui |
| [ Maillage API pour Adobe Developer App Builder ](https://developer.adobe.com/graphql-mesh-gateway/) | Oui | Oui |
| [Exportation de données SaaS](https://experienceleague.adobe.com/fr/docs/commerce/saas-data-export/overview) | Oui | Oui |
| [Recherche en direct](https://experienceleague.adobe.com/fr/docs/commerce/live-search/overview) | Non | Non |
| [Recommandations de produits](https://experienceleague.adobe.com/fr/docs/commerce/product-recommendations/overview) | Non | Non |
| [ Services de paiement ](https://experienceleague.adobe.com/fr/docs/commerce/payment-services/guide-overview) | Non | Non |
| [Événements Back Office De Connexion Aux Données](https://experienceleague.adobe.com/fr/docs/commerce/data-connection/event-forwarding/events-backoffice) | Oui | Oui |
| [Événements de storefront de connexion de données](https://experienceleague.adobe.com/fr/docs/commerce/data-connection/event-forwarding/events#storefront-events) | Non | Non |
| [Audience Activation](https://experienceleague.adobe.com/fr/docs/commerce-admin/customers/audience-activation) | Non | Non |

### Outils

L’outil [Security Scan Tool](../../systems/security-scan.md) pour Adobe Commerce vous permet de surveiller votre boutique pour vous assurer que tous les contrôles de sécurité requis sont activés et opérationnels. Outre les contrôles de sécurité standard, Adobe a amélioré l’outil afin d’afficher les contrôles spécifiques à la loi HIPAA pour les clients qui utilisent l’offre HIPAA pour Adobe Commerce. Les contrôles HIPAA de l’outil d’analyse de sécurité sont conçus pour garantir les éléments suivants :

- Les modules d’audit ne sont pas désactivés
- L’authentification à deux facteurs (2FA) n’est pas désactivée
- Les fonctionnalités marketing sont désactivées
- Toutes les extensions installées correspondent à une liste autorisée prédéfinie
- Aucun service Adobe non pris en charge n’est installé.

Vous pouvez [configurer l’outil](../../systems/security-scan.md#run-a-security-scan) pour vous envoyer des notifications par e-mail avec les détails des analyses planifiées ou [afficher manuellement les rapports](https://experienceleague.adobe.com/fr/docs/commerce-cloud-service/user-guide/launch/overview#to-review-the-report).

## Disabled features

Pour se conformer aux exigences de la loi HIPAA, certaines fonctionnalités prises en charge par Adobe Commerce ne sont pas disponibles ou sont désactivées par défaut. Les commerçants ont la possibilité de réactiver ou d&#39;utiliser ces fonctionnalités à leurs propres risques.

Les fonctionnalités suivantes sont désactivées par défaut dans le module de préparation à la loi HIPAA. Les commerçants peuvent activer l&#39;une de ces fonctionnalités à leurs propres risques.

- **[E-mail transactionnel](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html?lang=fr)**—SendGrid est désactivé par défaut, car le service n&#39;est pas conforme à la loi HIPAA. Adobe Commerce propose une option d’intégration que vous pouvez utiliser avec votre propre compte [AWS Simple Email Service](https://docs.aws.amazon.com/ses/). Pour plus d’informations sur la configuration, contactez votre gestionnaire de compte technique client ou l’assistance Adobe Commerce.

- **[Passage en caisse des invités](../../stores-purchase/checkout-guest.md)** : cette fonctionnalité présente un risque potentiel pour divers aspects de la loi HIPAA, notamment la journalisation, le contrôle d’accès, l’hygiène et la traçabilité des ISP, et potentiellement plus encore.

- **[Fonction Newsletter](../../merchandising-promotions/newsletters.md)** : cette fonction est désactivée pour empêcher l&#39;utilisation des ISP dans un contexte marketing.

- **[Paramètre du service de création de rapports avancée](../../getting-started/business-intelligence.md)** : ce paramètre de configuration est désactivé pour empêcher l&#39;utilisation des ISP pour l&#39;analyse et la création de rapports.
