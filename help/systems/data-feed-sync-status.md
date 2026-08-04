---
title: Surveillance du statut de synchronisation des flux de données dans Commerce
description: Suivre les exportations. Diagnostiquer les problèmes de synchronisation pour  [!DNL Catalog Service],  [!DNL Live Search],  [!DNL Product Recommendations] et  [!DNL Adobe Commerce Optimizer Connector].
feature: Products, Customers, Data Import/Export
role: Admin
level: Beginner
exl-id: 4e1b9da0-450c-4488-8693-1938a948e792
TQID: https://experienceleague.adobe.com/Y8vYxKS-8iX-bCLSJpAiJOItWlJk348bSMWfk1Cgpbg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 424b379815ffbf818c2490d0195bf0bf7dd51ab7
workflow-type: tm+mt
source-wordcount: 1664
ht-degree: 0%

---


# Surveillance du statut de synchronisation des flux de données

La page [!UICONTROL Data Feed Sync Status] permet aux administrateurs et administratrices Commerce de surveiller l’intégrité des exportations pour les flux de données de produits et de catégories dans la zone Admin.

## Audience et disponibilité {#audience}

La page Statut de la synchronisation des flux de données est disponible sans frais supplémentaires pour les commerçants Commerce disposant d’une licence active pour l’un des services suivants :

- [[!DNL Product Recommendations v6.0.0]](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview)
- [[!DNL Live Search v4.1.0]](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview)
- [[!DNL Catalog Service v1.17]](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/guide-overview)
- [[!DNL Adobe Commerce Optimizer Connector]](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/overview)

La page Statut de la synchronisation des flux de données est disponible automatiquement dans les configurations de service Commerce prises en charge. Dans Adobe Commerce sur les déploiements d’infrastructure cloud et sur site, si la page est manquante après l’activation d’un service ou d’un connecteur éligible, suivez les instructions d’installation manuelle ci-dessous. N’utilisez pas la procédure d’installation du compositeur pour les expériences SaaS gérées par le produit.

## Accès à la page du statut de synchronisation {#access-data-feed-sync-status-page}

Dans la zone d’administration, accédez à **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Feed Sync Status]**.

![Page Statut de synchronisation des flux de données résumant l’activité d’exportation des flux de données](assets/data-feed-sync-status.png){width="600" zoomable="yes"}

>[!NOTE]
>
> Cette page indique uniquement le statut d’exportation. Un statut de réussite signifie que les données ont bien été exportées ; il ne confirme pas que les données sont disponibles dans les services connectés. Voir [Confirmer les données dans les services connectés](#confirm-data-in-connected-services) pour plus d’informations.

## Flux d’exportation disponibles

La liste des flux d’exportation disponibles que vous pouvez gérer à partir de la page État de la synchronisation des données dépend des services Commerce connectés.

- **Pour les [!DNL Adobe Commerce on Cloud, On Premises, and Commerce as a Cloud Service] avec les services Commerce configurés :** consultez [Flux pris en charge](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/reference/feed-table-reference#supported-feeds) dans le Guide d’exportation des données _SaaS_.

- **Pour les déploiements sur le cloud ou On-Premise d’Adobe Commerce configurés avec le [!DNL Adobe Commerce Optimizer Connector] :** consultez [Flux pris en charge](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/reference/connector-reference#supported-feeds) dans le _Guide du connecteur Adobe Commerce Optimizer_.


## Résumé du statut de synchronisation des flux de données {#data-feed-sync-status-summary}

La grille de résumé répertorie chaque flux et son nombre d’exportations.

| Champ | Description |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Nom du flux** | Indexeur de flux pour une entité ou une partie d’une entité (produit, prix du produit). |
| **Enregistrements** | Nombre d’enregistrements Commerce nécessitant une synchronisation. Peut dépasser le nombre de grilles d’administration parce que les éléments de flux sont inclus dans la portée (par exemple, le code Vue de la boutique). |
| **Enregistrements envoyés avec succès** | Nombre d’éléments de flux envoyés avec succès de Commerce au point d’entrée de service configuré. Cela ne confirme pas l’ingestion en aval ou la disponibilité du catalogue. Si des erreurs de synchronisation se sont produites, ce nombre peut être inférieur au nombre d’enregistrements sources. |
| **Enregistrements ayant échoué** | Nombre d’enregistrements qui n’ont pas pu être envoyés aux services Commerce connectés. |
| **Action** | Sélectionnez **[!UICONTROL Details]** pour afficher l’activité de synchronisation d’un flux. |

## Détails du statut de synchronisation des flux de données {#data-feed-sync-status-details}

Dans la page de résumé, sélectionnez un nom de flux ou sélectionnez **[!UICONTROL Details]** pour afficher le statut d’exportation de chaque élément de flux :

![Page Détails du statut de synchronisation des flux de données avec rapport du statut de l’élément de flux](assets/data-feed-sync-status-details.png){width="600" zoomable="yes"}

| Champ | Description |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **ID d’élément de flux** | Identifiant généré automatiquement et utilisé à des fins système |
| **Identifiant de l’entité** | Identifiant unique de l’entité source (ID de produit, ID de catégorie, etc.) |
| **Identifiants de flux** | Identifiants uniques pour l’élément de flux. Par exemple, le SKU et le code d’affichage de la boutique pour le flux de produits. Les valeurs varient selon le flux. |
| **Statut de l’exportation** | [état de synchronisation](#export-status-types) de l’élément de flux, avec des indicateurs codés par couleur |
| **Date de la dernière synchronisation** | Date et heure de la dernière tentative d’exportation ou d’envoi depuis Commerce. Cet horodatage ne confirme pas la disponibilité en aval. |
| **L’Entité Est-Elle Supprimée ?** | Indique si l’entité a été supprimée dans Adobe Commerce. Les éléments supprimés ne s’affichent que si la synchronisation a échoué. |
| **ID de requête** | ID unique de la requête de synchronisation. Fournissez-le à l’assistance lors du dépannage des mises à jour d’entités. |
| **Erreur** | Informations détaillées sur les erreurs lors des échecs de synchronisation |

Vous pouvez gérer la vue à l&#39;aide des commandes suivantes :

- [!UICONTROL Mass Action] de planifier la resynchronisation des éléments de flux sélectionnés
- [!UICONTROL Filters] et [!UICONTROL Columns]
- [!UICONTROL Default View] de créer et d’enregistrer une vue filtrée, et de basculer entre les vues

### Indicateurs d’intégrité des flux {#feed-health-indicators}

| **Indicateur** | **Description** |
| ------------- | --------------- |
| Statut de l’indexeur | <ul><li>**Prêt** : l’indexeur est à jour. Aucune réindexation requise.</li><li>**Réindexation requise** : données Source modifiées. Exécutez une réindexation pour capturer les modifications récentes.</li><li>**Traitement** : l’indexation est en cours.</li></ul> |
| Liste d&#39;attente du journal des modifications | <ul><li>**Tous synchronisés** : aucune modification en attente à traiter.</li><li>**Éléments dans la liste d&#39;attente** : nombre de modifications en attente de traitement. Une liste d’attente de plus de 1 000 éléments peut indiquer des problèmes de performances.</li></ul> |
| Mode indexeur | <ul><li>**Mode de planification** (recommandé) : l’indexeur s’exécute selon le calendrier, ce qui réduit le risque de perte de données.</li><li>**Mise à jour lors de l’enregistrement** (temps réel) : affiché comme un avertissement sur la page. Le mode temps réel n’est pas attendu et augmente le risque de perte de données en cas de forte charge.</li></ul> |

>[!TIP]
>
> Pour en savoir plus sur le traitement des index, consultez la rubrique [Gestion des index](index-management.md).

### Types de statut d&#39;export {#export-status-types}

| **Statut** | **Description** | **Action requise** |
| ----------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------------ |
| **Soumis au service** | L’élément de flux a été envoyé avec succès depuis Commerce pour le traitement en aval. | Aucune |
| **Échec, va réessayer** | Échec de l&#39;envoi, mais le système tentera de le renvoyer. | Surveiller la résolution |
| **Échec, requiert votre attention** | Échec en raison d&#39;une erreur d&#39;application ou de données. | Examiner et résoudre le problème dans la colonne [!UICONTROL Error] |
| **En attente d’envoi** | Modifications détectées dans le journal des modifications, mais pas encore traitées. | État de traitement normal |

## Surveillance du statut des flux de données

Lorsque vous mettez à jour des entités liées à des produits et à des catégories dans la base de données Commerce, les données sont transférées vers les services Commerce en fonction de la configuration de votre flux. Vous pouvez surveiller l’activité d’exportation et son statut actuel à partir de la page de résumé de la [!UICONTROL Data Feed Sync Status].

>[!IMPORTANT]
>
> Le temps nécessaire à la synchronisation des données varie en fonction de la taille de votre catalogue, du volume de données mises à jour et des performances du service externe.

Lorsque le nombre d’envois réussis correspond au nombre source d’un flux et qu’aucun élément n’est en attente d’envoi ou n’a échoué, Commerce a terminé l’exportation de ce flux. Utilisez le tableau de bord approprié pour [confirmer la disponibilité en aval](#confirm-data-in-connected-services).

>[!NOTE]
>
> Adobe fournit également des outils d’interface de ligne de commande et des journaux système que les développeurs et les intégrateurs système peuvent utiliser pour gérer et suivre les opérations de synchronisation. Pour plus d&#39;informations, consultez le [Guide d&#39;exportation de données SaaS](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview).

### Gérer les exportations ayant échoué {#manage-failed-exports}

Pour passer en revue les exportations ayant échoué et planifier une resynchronisation :

1. Sur la page de résumé, recherchez le flux avec les enregistrements ayant échoué.
1. Sélectionnez **[!UICONTROL Details]**.
1. Vérifiez les messages d’erreur dans la colonne [!UICONTROL Error] .
1. Sélectionnez les enregistrements à resynchroniser à l’aide des cases à cocher.
1. Dans le menu [!UICONTROL Mass Action], sélectionnez **[!UICONTROL Schedule Resync]**, sélectionnez **[!UICONTROL Submit]** et confirmez l’opération.
1. Surveillez les modifications de statut dans la page de détails.

Le système réessaye automatiquement certains échecs.

#### Quand resynchroniser manuellement {#resync-feed-items}

Resynchronisez manuellement dans ces cas :

- Des erreurs d’authentification ou d’autorisation (codes d’état 401 ou 403) persistent
- Correction de problèmes de format des données qui provoquaient des erreurs de payload
- Configuration de service externe ou points d’entrée modifiés
- Des personnalisations affectant l’exportation des données ont été déployées.

### Confirmer les données dans les services connectés {#confirm-data-in-connected-services}

Pour vérifier la synchronisation de bout en bout une fois les exportations terminées, utilisez l’une des méthodes suivantes. Pour connaître les limites du statut d’exportation sur cette page, reportez-vous à la [remarque ci-dessus](#export-status-scope).

- **[!DNL Adobe Commerce as a Cloud Service]avec les services Commerce :** vérifiez le [tableau de bord de gestion des données](data-dashboard.md) applicable pour confirmer la disponibilité en aval.
- **Adobe Commerce sur le cloud ou On-premise avec Adobe Commerce Optimizer Connector** : vérifiez d’abord le statut d’exportation de l’administrateur Commerce, puis vérifiez la page [Synchronisation des données](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/data-sync) dans [!DNL Commerce Optimizer Studio]
- **[!DNL Adobe Commerce Optimizer] (autonome) :** données ne sont pas exportées à partir du serveur principal Commerce. Utilisez la [page Synchronisation des données](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/data-sync) dans [!DNL Commerce Optimizer Studio] pour confirmer la disponibilité des données.

>[!TIP]
>
> Pour en savoir plus sur le processus de synchronisation des données, consultez la section [Synchroniser les données avec l’exportation de données SaaS](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/data-synchronization/data-sync-manage#view-and-manage-the-synchronization-process) du *Guide d’exportation de données SaaS*.

## Bonnes pratiques {#best-practices}

- Consultez quotidiennement la page de résumé pour les flux présentant des taux d’échec élevés.
- Consultez chaque semaine les détails des flux critiques, tels que les produits et les prix.
- Suivez les tendances de succès des exportations chaque mois pour identifier les problèmes récurrents.

## Résolution des problèmes courants {#troubleshoot-common-issues}

| Problème | Symptômes | Que faire |
| ---------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Taux d’échec élevés | De nombreux enregistrements affichent le statut *Échec, nécessite une attention* | <ul><li>Vérifier le statut et la configuration du service externe</li><li>Vérifier les messages d’erreur pour les modèles de la colonne [!UICONTROL Error]</li><li>Une fois le problème sous-jacent résolu, consultez [Gérer et resynchroniser les exportations en échec](#manage-failed-exports)</li><li>Contactez le support technique externe si nécessaire</li></ul> |
| Performances d’exportation lentes | Liste d&#39;attente élevée pour les modifications ou mises à jour de statut lentes | <ul><li>Vérifiez [indicateurs d’intégrité des flux](#feed-health-indicators) l’indexeur et le statut de la liste d’attente</li><li>Réexécutez l’indexation si **Réindexation requise** s’affiche.</li><li>Surveiller les temps de réponse du service externe</li><li>Planifier des exportations pendant les heures creuses lorsque cela est possible</li><li>Examen des ressources et des performances du système</li></ul> |
| Échecs d&#39;authentification | Codes d’état 401 ou 403 dans la colonne [!UICONTROL Error] | <ul><li>Vérification des informations d’identification et des jetons d’API</li><li>Vérifier les autorisations du compte de service externe</li><li>Renouveler les jetons expirés ou contacter votre fournisseur de services</li><li>Une fois les informations d’identification restaurées, [resynchronisez les enregistrements concernés](#manage-failed-exports)</li></ul> |
| Page de statut de synchronisation des flux de données manquants | **[!UICONTROL Data Feed Sync Status]** n’est pas répertorié sous **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** après l’activation d’un service connecté | <ul><li>Pour Commerce as a Cloud Service, vérifiez qu’un service éligible est activé (voir [&#x200B; Audience et disponibilité &#x200B;](#audience)).</li><li>Pour Commerce sur le cloud ou On-premise uniquement, [Installez l’extension manuellement](#install-the-extension)</li></ul> |

Adobe Commerce sur les infrastructures cloud ou sur site : vérifiez qu’un service éligible ou le connecteur Adobe Commerce Optimizer est activé ; si la page est toujours manquante, suivez les instructions d’installation manuelle.
ACCS ou Adobe Commerce Optimizer : n’installez pas le module manuellement, utilisez l’expérience de synchronisation gérée par le produit ou contactez l’équipe d’assistance technique appropriée.

## Installation de l’extension {#install-the-extension}

Une installation manuelle est requise pour les déploiements Adobe Commerce sur le cloud ou sur site uniquement si la page [!UICONTROL Data Feed Sync Status] est manquante dans la zone d’administration après l’activation d’un service éligible. Voir [&#x200B; Audience et disponibilité &#x200B;](#audience).

### Conditions préalables

- Adobe Commerce 2.4.4+. Pour connaître la configuration requise, voir [Configuration requise](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/system-requirements).
- [Extension Adobe Commerce Data Export](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/reference/manage-extension), version 103.4.15 ou ultérieure
- Clés d’authentification avec l’autorisation de télécharger le package requis à partir du référentiel Adobe Commerce. Pour créer des clés d’authentification et obtenir l’accès au package nécessaire, voir [&#x200B; Obtenir vos clés d’authentification &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys). Pour les installations cloud, consultez le guide [Commerce sur les infrastructures cloud](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/authentication-keys).
- Accès à la ligne de commande du serveur applicatif Adobe Commerce.

### Etapes d&#39;installation

Ajoutez le module `magento/module-data-exporter-status` à l’aide du compositeur :

```shell
composer require magento/module-data-exporter-status
```

Pour obtenir des instructions d’installation détaillées, consultez les guides suivants :

- [Installation de l’extension pour Adobe Commerce sur une infrastructure cloud](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure-store/extensions)
- [Installation de l’extension sur Adobe Commerce On-premise](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/tutorials/extensions)

>[!MORELIKETHIS]
>
> - [Tableau de bord de gestion des données](data-dashboard.md)
> - [Guide d&#39;exportation de données SaaS](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview)
