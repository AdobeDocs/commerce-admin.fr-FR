---
title: Préparation du HIPAA sur Adobe Commerce
description: Découvrez comment ajouter le module Adobe Commerce compatible avec HIPAA et obtenir des fonctionnalités et fonctionnalités supplémentaires qui vous permettent de respecter vos obligations HIPAA.
feature: Security, Compliance
hide: true
hidefromtoc: true
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: 10b01db562777ef2fcc224177d7a83c0a6fc90e7
workflow-type: tm+mt
source-wordcount: '1472'
ht-degree: 0%

---

# Préparation du HIPAA sur Adobe Commerce

>[!IMPORTANT]
>
>**Clause de non-responsabilité**<br/>
>Ces informations ont pour but d’aider les clients Adobe à répondre à leurs questions concernant les services prêts pour le HIPAA d’Adobe. Il ne s&#39;agit pas d&#39;un avis juridique. Les commerçants doivent consulter leur propre service juridique pour comprendre leurs obligations en vertu de la HIPAA et l’utilisation et la configuration appropriées des produits d’Adobe.

## Loi sur la transférabilité et la responsabilité de l&#39;assurance-maladie (HIPAA)

La Health Insurance Porability and Accountability Act (HIPAA) est la loi fédérale clé sur la protection de la vie privée dans le domaine de la santé aux États-Unis. Elle est appliquée par le département américain de la Santé et des Services de l&#39;homme (HHS). Le HIPAA s’applique à _Entités couvertes_ (comme les prestataires de soins de santé, les assureurs et les chambres de compensation) et _Business Associates_ (telles que les entités qui fournissent des services aux entités couvertes). Les exigences HIPAA sont définies sur trois règles distinctes : règle de confidentialité, règle de sécurité et règle de notification d’infraction. Adobe fait office d’associé commercial pour certains produits, qui sont classés par Adobe &quot;Services prêts pour le HIPAA&quot;. Les données réglementées en vertu du HIPAA sont appelées _Protection des informations sanitaires_ ou l’intégrité physique. (2) se rapporte à la santé ou à la condition physique ou mentale passée ou future d&#39;un individu, à la prestation de soins à un individu, ou au paiement passé, présent ou futur de la prestation de soins à un individu, et (3) identifie l&#39;individu ou l&#39;élément auquel il existe une base raisonnable de croire les informations peuvent être utilisées pour identifier l’individu. Les règles de confidentialité et de sécurité du HIPAA exigent qu’une entité couverte obtienne des garanties écrites d’un associé sous la forme d’un accord d’association d’affaires, ou BAA, exigeant de l’associé de l’entreprise qu’il protège la vie privée et la sécurité de l’IIP de l’entité couverte.

## Prêt pour Adobe Commerce HIPAA

Les fonctionnalités et fonctionnalités supplémentaires compatibles avec Adobe Commerce HIPAA permettent aux commerçants de se conformer à leurs obligations HIPAA respectives. Vous pouvez installer Adobe Commerce compatible avec les HIPAA (`magento/hipaa-ee`) à votre Adobe Commerce sur l’infrastructure cloud. Certaines fonctionnalités doivent également être désactivées pour être conformes à HIPAA.

*Ces documents sont destinés à titre d’information uniquement. La fourniture de ces informations n&#39;autorise pas le destinataire à bénéficier de droits contractuels ou autres. Bien que des efforts aient été faits pour assurer l&#39;exactitude des informations à la date de leur transmission, aucune indication n&#39;est faite que ces informations sont exactes et complètes, et l&#39;Adobe n&#39;a aucune obligation de les mettre à jour au fur et à mesure que la loi ou les produits de l&#39;Adobe changent. En outre, ce document ne doit être distribué à aucune autre personne que le destinataire prévu sans le consentement écrit de l’Adobe.*

## Configuration requise

La préparation à la HIPAA sur Adobe Commerce requiert le même système qu’Adobe Commerce avec les exigences supplémentaires :

- Adobe Commerce version 2.4.6-p3 ou ultérieure (non bêta)
- Adobe Commerce sur l’infrastructure cloud ou Adobe Commerce sur Managed Services
- Dernière version de `magento/hipaa-ee` extension

## Installation

Les services prêts pour l’HIPAA d’Adobe sont techniquement un métapaquet de compositeur `magento/hipaa-ee` qui contient des liens vers des modules spéciaux. Ce module se trouve dans le référentiel [repo.magento.com](https://repo.magento.com).

1. Pour pouvoir installer `magento/hipaa-ee` métapaquage, vous devez y avoir accès. Pour la génération des clés et l&#39;obtention des droits nécessaires, reportez-vous à la section [Obtention des clés d’authentification](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html?lang=en).

1. Vérifiez l’environnement dans lequel vous allez installer le module et assurez-vous qu’il respecte la configuration [configuration requise](#system-requirements).

1. Ajouter le métappackage `magento/hipaa-ee` à la configuration du compositeur.

   La méthode la plus simple consiste à utiliser l’interface de ligne de commande du compositeur. Par exemple :

   ```shell
   composer require magento/hipaa-ee
   ```

1. Si Adobe Commerce n’est pas encore installé, vous pouvez démarrer l’installation (suivez le [Instructions d’installation](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html?lang=en)).

   Si Adobe Commerce est déjà installé, exécutez après le téléchargement des modules. `bin/magento setup:upgrade` puis suivez les recommandations.

   ```shell
   bin/magento setup:upgrade
   ```

   Lorsque cette commande est en cours d’exécution, les modules nouvellement téléchargés sont activés et les scripts permettant de les installer sont lancés. Pour en savoir plus sur la gestion des modules, voir [Activation ou désactivation des modules](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html?lang=en).

1. Une fois le processus d’installation ou de mise à jour terminé, vérifiez si la variable `Hipaa*` les modules appropriés ont été inclus.

   Exécutez la commande :

   ```shell
   bin/magento module:status
   ```

   Si le package du compositeur HIPAA a été correctement ajouté, les modules HIPAA s’affichent dans la sortie de la commande. Par exemple :

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
   <truncated for brevity>
   ```

   Tous les modules dotés du préfixe `Magento_Hipaa` doit se trouver dans la section modules activés .

## Améliorations des fonctionnalités pour la préparation à la HIPAA

La variable `magento/hipaa-ee` Le module introduit quelques modifications et améliorations au produit Commerce de base. Les sections suivantes fournissent des détails sur ces modifications et sur la manière dont elles modifient le produit de base.

### Journaux des actions

La journalisation d’audit est une exigence HIPAA. Dans Adobe Commerce, la variable [Journaux des actions](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) enregistre chaque modification effectuée par un utilisateur administrateur qui travaille dans votre boutique. Pour répondre aux exigences de l’HIPAA concernant le journal d’audit, des modifications sont apportées à la fonctionnalité afin d’enregistrer toutes les actions des utilisateurs administrateurs et des clients effectuées via l’interface utilisateur d’administration et par le biais d’appels API.

#### Rapport Journaux d’actions

La variable _Journaux des actions_ grille de rapport (**[!UICONTROL System]** > Journaux d’actions > Rapport) est modifié pour prendre en compte les actions des clients effectuées par le biais de l’interface utilisateur d’administration et de l’API.

1. Deux colonnes supplémentaires :
   - ***Source***: affiche l’emplacement où l’action a été effectuée.\
     Valeurs : `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***Type de client***: affiche le type de client.\
     Valeurs : client | Admin | Intégration


2. Renommer ***Nom d’utilisateur*** to ***Identifiant du client***
   - ***Identifiant du client***: affiche l’identifiant de connexion de l’utilisateur qui a exécuté l’action.\
     Valeurs :
      - un e-mail si le type de client est Client ;
      - un nom d’utilisateur si le type de client est Admin ;
      - un nom si le type de client est Intégration ;

3. Renommer ***Nom complet de l’action*** to ***Cible***
   - ***Cible***: affiche le nom de l’action.\
     Valeurs :
      - un point de terminaison si la source est une API REST ou une API SOAP ;
      - un nom de requête/mutation si l’API GraphQL
      - Nom de l’action dans l’interface utilisateur d’administration ou l’interface utilisateur client.

#### Configuration des actions d’administration pour la journalisation

Cette fonction n’est pas disponible, car toutes les actions doivent être enregistrées par défaut.

### Fonctionnalités d’importation/exportation

Les améliorations apportées aux fonctions d’importation/exportation visent à améliorer l’expérience administrative et à améliorer la visibilité des actions des utilisateurs.

>[!NOTE]
>
>Ces ***Les améliorations ne modifient pas la logique de base Import/Export***; au lieu de cela, ils étendent les fonctionnalités afin d’offrir une journalisation plus complète et une attribution de données améliorée. La fonctionnalité fondamentale d&#39;import/export reste inchangée. Les utilisateurs peuvent continuer à utiliser les fonctionnalités et les workflows existants sans interruption.

#### Journalisation des actions administratives

L’une des principales améliorations des fonctionnalités d’importation/exportation est la journalisation améliorée des actions administratives. Cela permet de mieux comprendre les activités liées à l’import/export de données, ce qui contribue à améliorer le suivi et la vérification. Les actions suivantes sont désormais consignées et répercutées dans la variable **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**grid :

| Type | Actions |
| ---- | ------- |
| Importer | <ul><li>Un utilisateur administrateur exécute un import<li>Un utilisateur administrateur télécharge un fichier importé.<li>Un utilisateur administrateur télécharge un fichier d’erreur<ul/> |
| Exporter | <ul><li>Requêtes d’utilisateur administrateur<li>Un utilisateur administrateur télécharge un fichier exporté.<ul/> |
| Imports/exports planifiés | <ul><li>Exportation des plannings d’utilisateur administrateur<li>Un utilisateur administrateur modifie une exportation planifiée.<li>Un utilisateur administrateur exécute une exportation planifiée.<li>Un utilisateur administrateur supprime une exportation planifiée<li>Un utilisateur administrateur planifie un import<li>Un utilisateur administrateur modifie un import planifié.<li>Un utilisateur administrateur exécute un import planifié<li>Un utilisateur administrateur supprime un import planifié<li>Un utilisateur administrateur exécute une suppression en bloc des opérations d’importation/exportation.<ul/> |

### Améliorations de l’affichage et amélioration du filtrage/tri

Pour permettre aux utilisateurs administrateurs de disposer de grilles plus informatives, plusieurs améliorations ont été apportées à l’affichage des données ainsi qu’aux fonctionnalités de filtrage et de tri :

#### Historique d&#39;import ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- Filtrage activé pour toutes les colonnes, à l’exception de **[!UICONTROL Imported File]**, **[!UICONTROL Error File]**, **[!UICONTROL Execution Time]**, et **[!UICONTROL Summary]**.

#### Exporter ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- Ajout d’une **[!UICONTROL ID]** colonne .
- Ajout d’une **[!UICONTROL Requested At]** column (_date et heure auxquelles l’exportation a été demandée_).
- Ajout d’une **[!UICONTROL User]** column (_nom d’utilisateur d’un administrateur qui a effectué la requête._).
- Suppression d’un **[!UICONTROL Action]** colonne .
- Déplacement de la variable **[!UICONTROL Download]** lien vers un **[!UICONTROL File name]** column (_comme la grille Import History_).
- Désactivation de l’action responsable de la suppression d’un fichier exporté (_pour améliorer le suivi_).
- Activation du tri pour toutes les colonnes, sauf **[!UICONTROL File name]**.
- Activation du filtrage pour toutes les colonnes.

#### Imports/exports planifiés ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- Ajout d’une **[!UICONTROL ID]** colonne .
- Ajout d’une **[!UICONTROL Scheduled At]** column (_date et heure auxquelles l’importation ou l’exportation a été planifiée_).
- Ajout d’une **[!UICONTROL User]** column (_nom d’utilisateur d’un utilisateur administrateur qui a planifié l’import/export_).

## Fonctionnalités désactivées pour la préparation à la HIPAA

### Services SaaS

Aucun des services SaaS proposés pour Adobe Commerce n’est disponible dans le cadre de l’offre de préparation HIPAA. Cela inclut, sans s’y limiter :

- Recherche en direct
- Mesh de l’API
- App Builder
- Service de catalogue

### Dépôt d’invités désactivé par défaut

- Le passage en caisse des invités présente un risque potentiel pour divers aspects de l’HIPAA, y compris l’abattage, le contrôle d’accès, l’hygiène et la traçabilité des PHI, et potentiellement plus encore.
- Le passage en caisse des invités est désactivé par défaut dans le module de préparation HIPAA, mais mes commerçants peuvent être activés à leurs risques et périls.

### Fonction de newsletter désactivée par défaut

- La fonction de newsletter est désactivée par défaut pour empêcher l’utilisation de l’information PHI dans un contexte marketing, mais peut être activée par le commerçant à ses risques et périls.

### Désactivation par défaut du paramètre du service de création de rapports avancés

Le paramètre du service de création de rapports avancés est désactivé par défaut pour empêcher l’utilisation de l’API pour l’analyse et la création de rapports, mais il peut être activé par le commerçant à ses risques et périls.
