---
title: Préparation du HIPAA sur Adobe Commerce
description: Découvrez comment ajouter l’extension Adobe Commerce HIPAA-Ready et obtenir des fonctionnalités supplémentaires qui vous permettent de respecter vos obligations HIPAA.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: cbcdaf8f5c531ba10a95e9455a5ebc28bd61c3b5
workflow-type: tm+mt
source-wordcount: '1597'
ht-degree: 1%

---

# Préparation du HIPAA sur Adobe Commerce

>[!IMPORTANT]
>
>**Clause de non-responsabilité légale**<br/>
>Ces informations ont pour but d’aider les clients Adobe à répondre à leurs questions concernant les services prêts pour le HIPAA d’Adobe. Il ne s&#39;agit pas d&#39;un avis juridique. Les commerçants doivent consulter leur propre service juridique pour comprendre leurs obligations en vertu de la HIPAA et l’utilisation et la configuration appropriées des produits d’Adobe.

>[!BEGINSHADEBOX]

**Loi sur la transférabilité et la responsabilité de l&#39;assurance-maladie (HIPAA)**

La Health Insurance Porability and Accountability Act (HIPAA) est la loi fédérale clé sur la protection de la vie privée dans le domaine de la santé aux États-Unis. Elle est appliquée par le département américain de la Santé et des Services de l&#39;homme (HHS). La loi HIPAA s’applique aux _entités couvertes_ (comme les prestataires de soins de santé, les assureurs et les chambres de compensation) et aux _Business Associates_ (telles que les entités qui fournissent des services aux entités couvertes). Les exigences HIPAA sont définies sur trois règles distinctes : règle de confidentialité, règle de sécurité et règle de notification d’infraction. Adobe fait office d’associé commercial pour certains produits, qui sont classés par Adobe &quot;Services prêts pour le HIPAA&quot;. Les données réglementées en vertu de l’HIPAA sont appelées _Information sanitaire protégée_ ou PHI. (2) se rapporte à la santé ou à la condition physique ou mentale passée ou future d&#39;un individu, à la prestation de soins à un individu, ou au paiement passé, présent ou futur de la prestation de soins à un individu, et (3) identifie l&#39;individu ou l&#39;élément auquel il existe une base raisonnable de croire les informations peuvent être utilisées pour identifier l’individu. Les règles de confidentialité et de sécurité du HIPAA exigent qu’une entité couverte obtienne des garanties écrites d’un associé sous la forme d’un accord d’association d’affaires, ou BAA, exigeant de l’associé de l’entreprise qu’il protège la vie privée et la sécurité de l’IIP de l’entité couverte. Pour plus d’informations, voir [HIPAA et Adobe Products and Services](https://www.adobe.com/trust/compliance/hipaa-ready.html) dans le Centre de gestion de l’Adobe.

>[!ENDSHADEBOX]

## Prêt pour Adobe Commerce HIPAA

L’extension Adobe Commerce compatible avec le HIPAA ajoute des fonctionnalités supplémentaires aux installations Adobe Commerce qui permettent aux commerçants de respecter leurs obligations HIPAA respectives.

L’extension Adobe Commerce Prêt pour HIPAA `magento/hipaa-ee` est disponible pour Adobe Commerce sur l’infrastructure cloud ou les projets Managed Services Adobe. Le processus d’installation prêt pour l’HIPAA d’Adobe Commerce désactive certains services et fonctionnalités natifs pour se conformer aux exigences HIPAA. Voir [Services et fonctionnalités désactivés](#disabled-services-and-features).

>[!NOTE]
>
>L’accès aux fonctionnalités prêtes pour l’HIPAA est disponible uniquement pour les commerçants qui ont acheté le module complémentaire de soins de santé pour Adobe Commerce.

*Ces documents sont destinés à titre d’information uniquement. La fourniture de ces informations n&#39;autorise pas le destinataire à bénéficier de droits contractuels ou autres. Bien que des efforts aient été faits pour assurer l&#39;exactitude des informations à la date à laquelle elles ont été fournies, il n&#39;est pas établi que ces informations sont exactes et complètes. Adobe n&#39;a aucune obligation de mettre à jour ces informations à mesure que la loi ou les produits de l&#39;Adobe changent. En outre, ce document ne doit pas être distribué à une autre partie que le destinataire prévu sans le consentement écrit de l’Adobe.*

## Configuration requise

Adobe Commerce doit être déployé sur Adobe Commerce sur l’infrastructure cloud ou Adobe Commerce Managed Services avec la version 2.4.6-p3 - 2.4.6-p8 (pas de version bêta).

## Installation

**Condition préalable requise**

>[!BEGINSHADEBOX]

- Adobe a configuré votre compte Adobe Commerce pour accéder à l’extension Prêt pour HIPAA.
- Accédez à [repo.magento.com](https://repo.magento.com) pour installer l’extension. Pour la génération des clés et l’obtention des droits nécessaires, voir [Obtention de vos clés d’authentification](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

>[!ENDSHADEBOX]

Installez la dernière version de l’extension des services prêts pour l’HIPAA d’Adobe (`magento/hipaa-ee`) sur une instance exécutant Adobe Commerce version 2.4.6-p3 - 2.4.6-p8. L’extension est fournie en tant que métapaquet compositeur à partir du référentiel [repo.magento.com](https://repo.magento.com). Le métapaquage comprend la collection de modules qui activent les fonctionnalités HIPAA pour une instance Adobe Commerce.

1. Sur votre poste de travail local, modifiez le répertoire du projet pour votre projet Adobe Commerce sur l’infrastructure cloud.

   >[!NOTE]
   >
   >Pour plus d’informations sur la gestion locale des environnements de projet Commerce, voir [Gestion des branches avec l’interface de ligne de commande](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) dans le _Guide de l’utilisateur d’Adobe Commerce on Cloud Infrastructure_.

1. Extrayez la branche d’environnement à mettre à jour à l’aide de l’interface de ligne de commande de Adobe Commerce Cloud.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Ajoutez le métappackage `magento/hipaa-ee` à la configuration du compositeur à l’aide de l’interface de ligne de commande du compositeur.

   ```shell
   composer require "magento/hipaa-ee" --no-update
   ```

1. Mettez à jour les dépendances de package.

   ```shell
   composer update "magento/hipaa-ee"
   ```

1. Ajoutez, validez et envoyez le code mis à jour vers l’environnement cloud.

   ```shell
   git add -A
   git commit -m "Add HIPAA-Ready Services modules"
   git push origin <branch-name>
   ```

   La publication des mises à jour déclenche le [processus de déploiement cloud de Commerce](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) pour appliquer les modifications. Vérifiez l’état du déploiement à partir du [log de déploiement](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

### Vérification de l’installation

Une fois les mises à jour déployées, vérifiez que l’extension `Hipaa*` est installée.

1. Utilisez SSH pour vous connecter à l’environnement cloud distant.

   ```shell
   magento-cloud ssh
   ```

1. Dans la ligne de commande, utilisez l’interface de ligne de commande Adobe Commerce pour vérifier l’état du module.

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
   <truncated for brevity>
   ```

   Tous les modules dotés du préfixe `Magento_Hipaa` doivent se trouver dans la section modules activés .

## Améliorations des fonctionnalités pour la préparation à la HIPAA

L’extension `magento/hipaa-ee` introduit quelques modifications et améliorations au produit Commerce de base. Les sections suivantes fournissent des détails sur ces modifications et sur la manière dont elles modifient le produit de base.

### Journaux des actions

La journalisation d’audit est une exigence HIPAA. Dans Adobe Commerce, la fonctionnalité [Journaux d’action](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) enregistre chaque modification effectuée par un utilisateur administrateur qui travaille dans votre boutique. Pour répondre aux exigences de l’HIPAA relatives au journal d’audit, la fonctionnalité a été mise à jour afin d’enregistrer toutes les actions des utilisateurs administrateurs et des clients effectuées via l’interface utilisateur d’administration et par le biais d’appels API.

#### Rapport Journaux d’actions

La grille de rapport _Journaux d’action_ (**[!UICONTROL System]** > Journaux d’action > Rapport) est modifiée pour prendre en compte les actions des clients effectuées par le biais de l’interface utilisateur d’administration et de l’API.

1. Ajout de deux colonnes :
   - ***Source*** : affiche l’emplacement où l’action a été effectuée.
Valeurs : `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***Type de client*** : affiche le type de client.
Valeurs : client | Administration | Intégration

2. La colonne ***Nom d’utilisateur*** a été renommée ***Identifiant du client***.
   - ***Identifiant du client*** : affiche l’identifiant de connexion de l’utilisateur qui a exécuté l’action.
Valeurs :
      - un e-mail si le type de client est Client ;
      - un nom d’utilisateur si le type de client est Admin ;
      - un nom si le type de client est Intégration ;

3. La colonne ***Full Action Name*** a été renommée ***Target***
   - ***Target*** : affiche le nom de l’action.
Valeurs :
      - un point de terminaison si Source est une API REST ou une API SOAP
      - un nom de requête ou de mutation si une API GraphQL
      - nom d’action dans une interface utilisateur d’administration ou l’interface utilisateur client.

#### Configuration des actions d’administration pour la journalisation

Cette fonction n’est pas disponible, car toutes les actions doivent être enregistrées par défaut.

### Fonctionnalités d’import et d’export

Les améliorations apportées aux fonctions d’importation et d’exportation visent à améliorer l’expérience administrative et à améliorer la visibilité des actions des utilisateurs.

>[!NOTE]
>
>Ces ***améliorations ne modifient pas la logique de base Import et Export*** ; elles étendent plutôt la fonctionnalité pour offrir une journalisation plus complète et une attribution de données améliorée. Les fonctionnalités fondamentales de l&#39;import et de l&#39;export restent inchangées. Les utilisateurs peuvent continuer à utiliser les fonctionnalités et les workflows existants sans interruption.

#### Journalisation des actions administratives

L’une des principales améliorations des fonctionnalités d’importation et d’exportation est la journalisation améliorée des actions administratives. Cette amélioration offre la possibilité de mieux comprendre les activités liées à l’import et à l’export de données, ce qui contribue à améliorer le suivi et la vérification. Les actions suivantes sont maintenant consignées et répercutées dans la grille **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**:

| Type | Actions |
| ---- | ------- |
| Importer | <ul><li>Un utilisateur administrateur exécute un import<li>Un utilisateur administrateur télécharge un fichier importé.<li>Un utilisateur administrateur télécharge un fichier d’erreur<ul/> |
| Exporter | <ul><li>Requêtes d’utilisateur administrateur<li>Un utilisateur administrateur télécharge un fichier exporté.<ul/> |
| Imports/exports planifiés | <ul><li>Exportation des plannings d’utilisateur administrateur<li>Un utilisateur administrateur modifie une exportation planifiée.<li>Un utilisateur administrateur exécute une exportation planifiée.<li>Un utilisateur administrateur supprime une exportation planifiée<li>Un utilisateur administrateur planifie un import<li>Un utilisateur administrateur modifie un import planifié.<li>Un utilisateur administrateur exécute un import planifié<li>Un utilisateur administrateur supprime un import planifié<li>Un utilisateur administrateur exécute une suppression en bloc des opérations d’importation/exportation.<ul/> |

### Améliorations de l’affichage et amélioration du filtrage et du tri

Pour offrir aux utilisateurs administrateurs des grilles plus informatives, le service Prêt pour HIPAA propose plusieurs améliorations pour afficher, filtrer et trier les données.

#### Historique des imports ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- Activation du filtrage de toutes les colonnes à l’exception de **[!UICONTROL Imported File]**, **[!UICONTROL Error File]**, **[!UICONTROL Execution Time]** et **[!UICONTROL Summary]**.

#### Exporter ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- Ajout d’une colonne **[!UICONTROL ID]**.
- Ajout d’une colonne **[!UICONTROL Requested At]** (_date et heure auxquelles l’exportation a été demandée_).
- Ajout d’une colonne **[!UICONTROL User]** (_nom d’utilisateur d’un administrateur qui a effectué la requête_).
- Suppression d’une colonne **[!UICONTROL Action]**.
- Déplacement du lien **[!UICONTROL Download]** vers une colonne **[!UICONTROL File name]** (_comme la grille Import History_).
- Désactivation de l’action responsable de la suppression d’un fichier exporté (_pour améliorer le suivi_).
- Activation du tri pour toutes les colonnes à l’exception de **[!UICONTROL File name]**.
- Activation du filtrage pour toutes les colonnes.

#### Imports et exports planifiés ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- Ajout d’une colonne **[!UICONTROL ID]**.
- Ajout d&#39;une colonne **[!UICONTROL Scheduled At]** (la _date et l&#39;heure auxquelles l&#39;import ou l&#39;export a été planifié_).
- Ajout d’une colonne **[!UICONTROL User]** (nom d’utilisateur _d’un utilisateur administrateur qui a planifié l’importation ou l’exportation_).

## Services et fonctionnalités désactivés

Pour se conformer aux exigences de la HIPAA, certains services et fonctionnalités pris en charge par Adobe Commerce ne sont pas disponibles ou désactivés par défaut. Les commerçants ont la possibilité de réactiver ou d’utiliser ces services et fonctionnalités à leurs risques et périls.

### Services

- **Services Adobe Commerce** : aucun des services Adobe Commerce ou des services d’extensibilité n’est disponible sous l’offre de préparation HIPAA. Ces services comprennent, entre autres :

   - Recherche en direct
   - Mesh de l’API
   - App Builder

- **Email transactionnel**—[SendGrid](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html) est désactivé par défaut, car le service n’est pas prêt pour HIPAA. Adobe Commerce fournit une option d’intégration que vous pouvez utiliser avec votre propre compte [AWS Simple Email Service](https://docs.aws.amazon.com/ses/). Pour obtenir des informations sur la configuration, contactez votre gestionnaire de compte technique client ou l’assistance d’Adobe Commerce.

### Fonctionnalités désactivées par défaut

Les fonctionnalités suivantes sont désactivées par défaut dans le module de préparation HIPAA. Les vendeurs peuvent activer n’importe laquelle de ces fonctionnalités à leurs risques et périls.

- **[Passage en caisse des invités](../stores-purchase/checkout-guest.md)** : cette fonctionnalité présente un risque potentiel pour divers aspects de l’HIPAA, y compris la journalisation, le contrôle d’accès, l’hygiène et la traçabilité des PHI, et potentiellement plus encore.

- **[Fonction Newsletter](../merchandising-promotions/newsletters.md)** : cette fonction est désactivée pour empêcher l’utilisation de l’API dans un contexte marketing.

- **[Paramètre du service de création de rapports avancé](../getting-started/business-intelligence.md)** : ce paramètre de configuration est désactivé pour empêcher l’utilisation de l’API pour l’analyse et la création de rapports.
