---
title: Opérations
description: Recommandations pour migrer vers une offre conforme à la loi HIPAA et utiliser l’environnement d’évaluation secondaire à des fins de dépannage.
exl-id: 058b43de-1cee-4557-b2e3-87ee7422bf9b
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: cedbc2c5c885b7051fef3b0ef01522282b8bb973
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Opérations

{{ee-feature}}

Utilisez ces instructions pour en savoir plus sur la migration vers l’offre conforme à la loi HIPAA pour Adobe Commerce et sur l’utilisation de l’environnement `staging_for_support` à des fins de dépannage.

## Migration

Les clients effectuant la migration d’une offre Commerce non conforme à la loi HIPAA vers une offre conforme à la loi HIPAA doivent respecter les directives suivantes :

1. **Supprimer les espaces de données existants** : avant la migration, tous les espaces de données existants doivent être supprimés pour éviter le mélange de données sensibles et non sensibles dans la couche SaaS Adobe Commerce. Créez un ticket d’assistance pour supprimer vos espaces de données.
1. **Configuration d’un nouvel environnement** : la configuration de [Commerce Services Connector](https://experienceleague.adobe.com/en/docs/commerce/user-guides/integration-services/saas) dans la nouvelle instance Commerce HIPAA ne doit être configurée qu’une fois les espaces de données supprimés. Le nouvel environnement SaaS HIPAA ne doit être utilisé qu’une fois les anciens espaces de données supprimés. La configuration de Commerce Services Connector déclenche automatiquement la création de nouveaux espaces de données SaaS.
1. **Stratégie de migration** : la suppression des espaces de données SaaS est un processus irréversible qui supprime toutes les données de votre catalogue et les configurations associées. Une stratégie de migration doit être en place si vous souhaitez transférer l’une de vos anciennes données ou configurations. Cette stratégie est la responsabilité du commerçant. Un ticket d’assistance pour la suppression des espaces de données existants ne doit être créé qu’après la sauvegarde des données de migration (le cas échéant).

>[!NOTE]
>Pour supprimer des espaces de données existants, les clients doivent créer un ticket d’assistance Adobe Commerce intitulé « Migration HIPAA : supprimer les espaces de données SaaS », fournir leurs `MAGEID` et indiquer les identifiants de projet SaaS qui doivent être supprimés.

## Résolution des problèmes avec l’assistance Adobe Commerce

L’offre conforme à la norme HIPAA d’Adobe Commerce comprend un environnement `staging_for_support` supplémentaire que l’équipe d’assistance d’Adobe Commerce peut utiliser à des fins de dépannage.

Les clients doivent s’assurer que `staging_for_support` environnement :

- Ne contient aucune donnée sensible, comme, mais sans s’y limiter, les informations de santé protégées (ISP).
- Ne doit pas être utilisé pour des activités de production.
- Ne pas donner un nom différent de `staging_for_support` pour éviter toute confusion.
- est tenu à jour avec le code et la configuration de l’environnement de production afin de s’assurer que le dépannage est effectué dans un environnement aussi proche que possible de la production.

## Services Commerce

- **Services Commerce non conformes à la loi HIPAA** : les clients ne doivent pas utiliser les services Adobe Commerce, tels que Live Search, Product Recommendations, Payment Services, Sales Channels ou Commerce Intelligence, car ils ne sont pas conformes à la loi HIPAA. Les clients ne doivent utiliser que les [services conformes à la norme HIPAA](overview.md).

- **Connexion aux données** : seul le collecteur back-office de l’extension [Connexion aux données](https://experienceleague.adobe.com/en/docs/commerce/data-connection/overview) est conforme à la norme HIPAA. Les clients ne doivent pas envoyer de PHI à des services de connexion de données non conformes à la loi HIPAA, tels que les événements de storefront et Audience Activation. Les clients doivent s’assurer que la collecte de données storefront est désactivée.

- **Service de catalogue** : par défaut, [Service de catalogue](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/overview) ne traite pas les informations d’identification personnelles, de sorte qu’il n’entre pas dans le cadre de l’audit de conformité à la loi HIPAA. Il est de la responsabilité des clients de s’assurer qu’ils utilisent ce service en fonction de leur propre évaluation des cas d’utilisation et en consultation avec le service juridique. Les clients ne doivent pas non plus utiliser le service de catalogue par le biais du service fédéré afin d’éviter le risque de transmettre des ISP à des services non conformes à la loi HIPAA.

- **Exportation de données SaaS** : le service [Exportation de données SaaS](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview) doit être configuré pour envoyer des données uniquement pour les composants conformes à la loi HIPAA dans Adobe Commerce.
