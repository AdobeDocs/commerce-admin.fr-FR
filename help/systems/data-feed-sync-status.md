---
title: Surveillance Du Statut De Synchronisation Des Flux De Données
description: Surveillez la synchronisation de l’exportation des données et identifiez les problèmes ou retards de traitement des flux pour  [!DNL Catalog Service],  [!DNL Live Search] et  [!DNL Product Recommendations].
feature: Products, Customers, Data Import/Export
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 15118877bb8cc533b2323819db34da0513899e25
workflow-type: tm+mt
source-wordcount: '1458'
ht-degree: 0%

---


# Surveillance Du Statut De Synchronisation Des Flux De Données

Les administrateurs Adobe Commerce peuvent surveiller le statut de synchronisation des données exportées d’Adobe Commerce vers les services Commerce connectés à l’aide de la page Statut de synchronisation des flux de données dans l’administration Commerce.

![Page Détails du statut de synchronisation des flux de données avec rapport du statut de l’élément de flux](assets/data-feed-sync-status.png)

Cette page fournit des informations en temps réel sur l’intégrité et les performances des flux d’exportation de données qui transfèrent les données de produit et de catégorie de Commerce vers des services externes tels que [!DNL Product Recommendations], [!DNL Live Search] et [!DNL Catalog Service].

La page du statut de synchronisation affiche uniquement le statut d’exportation. Un statut de réussite indique que l’exportation des données a réussi et qu’elles seront éventuellement disponibles dans les services Commerce connectés. Utilisez le [tableau de bord de la gestion des données](data-dashboard.md) pour afficher l’état réel de la synchronisation des entités.

La surveillance du statut des flux permet d’assurer la cohérence des données et de résoudre rapidement les problèmes qui surviennent pendant le processus d’exportation. Les administrateurs peuvent :

* **Afficher l’état de synchronisation** pour tous les flux de données
* **Identifier et résoudre les erreurs** lors du traitement des flux
* **Accéder aux informations détaillées sur le statut** pour les éléments de flux individuels

Le statut est suivi pour les flux suivants :

* Flux de produits
* Flux d’attributs de produit
* Flux de catégories
* Flux de remplacements de produit
* Flux des prix des produits
* Flux de variantes de produit

>[!TIP]
>
>Pour en savoir plus sur le processus de synchronisation des données, consultez la section [Synchroniser les données avec l’exportation de données SaaS](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/data-synchronization) du *Guide d’exportation de données SaaS*.

## Installation de l’extension

La page Statut du flux de données est disponible pour tous les commerçants Commerce disposant de licences actives pour les services Commerce suivants :

* [[!DNL Product Recommendations v6.0.0+]](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview)
* [[!DNL Live Search v4.1.0+]](https://experienceleague.adobe.com/en/docs/commerce/live-search/guide-overview)
* [[!DNL Catalog Service v1.17+]](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/guide-overview) avec une licence active.

**Conditions requises**

* PHP 8.1, 8.2, 8.3 ou 8.4
* Adobe Commerce 2.4.4+
* [Extension Adobe Commerce Data Export](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/manage-extension), version 103.4.15 ou ultérieure
* Accès à [repo.magento.com](https://repo.magento.com)

  Pour générer des clés et obtenir les droits nécessaires, voir [&#x200B; Obtenir vos clés d’authentification &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys). Pour les installations cloud, consultez le guide [Commerce sur les infrastructures cloud](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/authentication-keys).

* Accès à la ligne de commande du serveur applicatif Adobe Commerce.

### Etapes d&#39;installation

Ajoutez le module `magento/module-data-exporter-status` à l’aide du compositeur :

```shell
composer require magento/module-data-exporter-status
```

Pour obtenir des instructions d’installation détaillées, consultez les guides suivants :

* [Installation de l’extension sur Adobe Commerce sur une infrastructure cloud](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure-store/extensions)

* [Installation de l’extension Adobe Commerce sur site](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/tutorials/extensions)

## Accès à la page Statut du flux de données

À partir de l’Administration Commerce, accédez à la page Statut du flux de données à partir de l’Administration Commerce sous **[!DNL System]** > Transfert de données > **[!DNL Data Feed Sync Status]**.

![Page Statut de synchronisation des flux de données résumant l’activité d’exportation des flux de données](assets/data-feed-sync-status.png)

La surveillance du statut des flux de données fournit deux interfaces :

* La [page récapitulative du statut de synchronisation des flux de données](#data-feed-sync-status-summary) qui répertorie les flux disponibles et l’état actuel
* La page [Statut de synchronisation des flux de données - Détails](#data-feed-sync-status-details) qui affiche des informations détaillées sur un flux sélectionné.

## Résumé du statut de synchronisation des flux de données

La page de synthèse du statut de synchronisation des flux fournit des informations sur l’activité d’exportation des flux de données, notamment les informations suivantes :

| Champ | Description |
|-------|-------------|
| **Nom du flux** | Nom de l’indexeur de flux responsable de la synchronisation d’une entité spécifique ou de sa partie, par exemple le produit ou le prix du produit. |
| **Enregistrements Source** | Nombre d’enregistrements disponibles à l’export depuis la base de données Commerce. Ce nombre peut être supérieur au nombre d’enregistrements affichés dans l’Administration Commerce, car chaque élément de flux appartient à une portée spécifique, telle que le code d’affichage du magasin. |
| **Enregistrements envoyés avec succès** | Nombre d’enregistrements transmis avec succès au SaaS Commerce pour un traitement ultérieur. Si des erreurs se sont produites lors de la transmission, le nombre d’enregistrements transmis avec succès aux services externes. |
| **Enregistrements ayant échoué** | Nombre d’enregistrements dont l’exportation a échoué et qui nécessitent une attention particulière. |
| **Action** | Sélectionnez **[!UICONTROL Details]** pour afficher l’activité de synchronisation d’un flux. |

## Détails du statut de synchronisation du flux de données

Dans la page de résumé du statut du flux de données , cliquez sur le nom d’un flux ou utilisez l’action [!DNL View Details] pour accéder à des informations détaillées sur les enregistrements individuels d’un flux.

![[!UICONTROL Data Feed Sync Status - Details] page avec rapport du statut des éléments de flux](assets/data-feed-sync-status-details.png)

La vue détaillée fournit les informations suivantes pour chaque élément de flux :

| Champ | Description |
|-------|-------------|
| **ID d’élément de flux** | Identifiant interne de l’enregistrement du flux |
| **Identifiant de l’entité** | L’ID de l’entité source (ID de produit, ID de catégorie, etc.) |
| **Statut de l’exportation** | [état de synchronisation](#export-status-types) de l’élément de flux. Statut actuel de la tentative d’exportation avec des indicateurs codés par couleur |
| **Date de la dernière synchronisation** | Date et heure du dernier envoi de l’enregistrement aux services Commerce |
| **L’entité est-elle supprimée ?** | Indique si l&#39;entité ou sa partie (produit ou prix de produit par exemple) a été supprimée dans Adobe Commerce. Les éléments ne s’affichent que si une erreur s’est produite lors de la synchronisation. |
| **ID de requête** | Identifiant unique de la demande de synchronisation. Fournissez cet identifiant à l’assistance lors de la résolution des problèmes de mises à jour d’entités spécifiques. |
| **Erreur** | Informations détaillées sur l’erreur si la synchronisation de l’élément de flux a échoué. |

Vous pouvez gérer la vue à l&#39;aide des commandes suivantes :

* [!DNL Mass Action] de planifier la resynchronisation des éléments de flux sélectionnés
* [!DNL Filters]
* [!DNL Default View] de créer et d’enregistrer une vue filtrée, et de basculer entre les vues
* [!DNL Columns] d’afficher et de masquer les colonnes du tableau.

### Indicateurs d’intégrité des flux

En haut de la page des détails de chaque flux, les indicateurs d’intégrité critiques indiquent l’état du système pour chaque flux :

#### Statut de l’indexeur

* **Valide** : les données sont synchronisées ; aucune réindexation n’est requise.
* **Non valide** : les données d’origine ont été modifiées. L’index doit être mis à jour.
* **Traitement** : indexation en cours.

>[!TIP]
>
>Pour en savoir plus sur le traitement des index, consultez la rubrique [Gestion des index](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/tools/index-management).

#### Liste d&#39;attente du journal des modifications

* **Tous synchronisés** : aucune modification en attente à traiter
* **Éléments dans la liste d&#39;attente** : nombre de modifications en attente de traitement

### Types de statut d&#39;export

Le système fournit des indicateurs de statut pour vous aider à identifier rapidement les problèmes :

#### Catégories de statut

| **Statut** | **Description** | **Action requise** |
|--------|-----------|-------------|
| **Soumis au service** | L’élément de flux a été exporté vers le service Commerce. | Aucune |
| **Échec, va réessayer** | Echec temporaire. Le système réessaiera automatiquement. | Surveiller la résolution |
| **Échec, requiert votre attention** | Échec en raison d&#39;une erreur d&#39;application ou de données. | Examiner et résoudre le problème dans la colonne [!DNL Error] |
| **En attente d’envoi** | En file d’attente pour l’exportation, mais pas encore traité. | État de traitement normal |

## Surveillance du statut des flux de données

Lorsque vous mettez à jour des entités liées à des produits et à des catégories dans la base de données Commerce, les données sont transférées vers les services Commerce en fonction de la configuration de votre flux. Vous pouvez surveiller ce processus en temps réel à partir de la page de résumé du statut de synchronisation des flux de données .

>[!IMPORTANT]
>
>Le temps nécessaire à la synchronisation des données varie en fonction de la taille de votre catalogue, du volume de données mises à jour et des performances du service externe.

Lorsque le nombre d’enregistrements envoyés avec succès correspond au nombre d’enregistrements sources, cela indique que la synchronisation est terminée et que toutes les données ont été transmises avec succès.

>[!NOTE]
>
>Adobe fournit également des outils d’interface de ligne de commande et des journaux système que les développeurs et les intégrateurs système peuvent utiliser pour gérer et suivre les opérations de synchronisation. Pour plus d&#39;informations, consultez le [Guide d&#39;exportation de données SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview).

### Gestion des exportations ayant échoué

Pour afficher les détails des exportations ayant échoué et prendre des mesures correctives :

1. Sur la page État de synchronisation des flux , recherchez le flux avec des enregistrements ayant échoué.
1. Cliquez sur **[!DNL Details]**.

1. Consultez les messages d’erreur pour des raisons d’échec spécifiques.

1. Utilisez des actions en masse pour planifier des opérations de resynchronisation pour les éléments ayant échoué.

### Données d’échec de resynchronisation

Vous pouvez resynchroniser manuellement les flux de données ayant échoué ou posé problème à l’aide du menu [!DNL Actions] de la page [!DNL Data Feed Sync Status - Details].

Alors que le système tente automatiquement de reproduire certains types d’échecs, une intervention manuelle peut s’avérer nécessaire dans les scénarios suivants :

* Vous constatez des erreurs d’authentification ou d’autorisation (codes d’état 401 et 403).
* Après avoir résolu les problèmes de format de données qui provoquaient des erreurs de payload.
* Suivi des mises à jour des configurations de service externes ou des points d’entrée.
* Vous déployez des personnalisations qui affectent les processus d’exportation de données.

En surveillant de manière proactive l’état des flux et en corrigeant rapidement les défaillances, vous pouvez maintenir la cohérence et la fiabilité des données dans l’ensemble de votre écosystème Commerce.

#### Resynchroniser manuellement les éléments de flux

Si vous devez resynchroniser des éléments de flux spécifiques :

1. **Sélectionner les enregistrements** : utilisez des cases à cocher pour sélectionner les enregistrements ayant échoué et nécessitant une attention particulière.
2. **Choisir une action** : sélectionnez **[!DNL Schedule Resync]** dans la liste déroulante d’actions en masse.
3. **Confirmer** : cliquez sur **[!DNL Submit]** et confirmez l’opération de resynchronisation.
4. **Surveiller les résultats** : vérifiez le message de réussite et surveillez les modifications de statut.

## Bonnes pratiques

### Surveillance régulière

1. **Contrôles quotidiens** : consultez quotidiennement la page d’aperçu des flux présentant des taux d’échec élevés
1. **Weekly Deep Dive** : examiner le statut détaillé des flux critiques (produits, prix)
1. **Analyse mensuelle** : suivez les tendances en matière de taux de réussite et de performances des exportations

### Workflow de dépannage

1. **Identifier les problèmes** : rechercher les erreurs et les nombres d’échecs élevés
1. **Vérifier l’intégrité de l’indexeur** : assurez-vous que les indexeurs sont valides et que la liste d’attente est gérable
1. **Consulter les détails de l’erreur** : cliquez sur les enregistrements ayant échoué pour afficher des messages d’erreur spécifiques
1. **Planifier la resynchronisation** : utilisez des actions en masse pour réessayer les exportations ayant échoué.
1. **Résolution du moniteur** : vérifiez que les éléments resynchronisés affichent le statut Succès

### Correction de problèmes courants

#### Taux d’échec élevés

**Symptômes** : grand nombre d’enregistrements affichant le statut « Échec, nécessite une attention particulière »

**Causes potentielles** :

* Modifications de la configuration du service externe
* Incompatibilités entre les formats de données
* Problèmes d’authentification ou d’autorisation

**Étapes de résolution** :

1. Vérifier le statut et la configuration du service externe
1. Vérifier les messages d’erreur pour les modèles
1. Vérifier les informations d’authentification
1. Contactez le support technique externe si nécessaire

#### Performances d’exportation lentes

**Symptômes** : journal des modifications volumineux, mises à jour de statut lentes

**Causes potentielles** :

* Problèmes de performances de l’indexeur
* Volume de données élevé
* Limitation de débit de service externe

**Étapes de résolution** :

1. Vérifier le statut de l’indexeur et le réexécuter s’il n’est pas valide
2. Surveiller les temps de réponse du service externe
3. Envisagez de planifier des exportations pendant les heures creuses
4. Examen des ressources et des performances du système

#### Échecs d&#39;authentification

**Symptômes** : codes d’état 401 ou 403

**Étapes de résolution** :

1. Vérification des informations d’identification et des jetons d’API
1. Vérifier les autorisations du compte de service externe
1. Renouveler les jetons d’authentification expirés
1. Contactez votre fournisseur pour les problèmes d’accès

>[!MORELIKETHIS]
>
>* [Tableau de bord de gestion des données](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/data-transfer/data-sync/data-dashboard)
>* [Guide d&#39;exportation de données SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview)
