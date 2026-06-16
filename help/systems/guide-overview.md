---
title: Guide des systèmes d’administration
description: Découvrez les bonnes pratiques de sécurité pour protéger votre boutique Commerce et gérer les autorisations. Apprenez également comment importer et exporter des données, gérer les intégrations et les extensions, et prendre en charge la maintenance de routine.
exl-id: 9d22571e-9e09-4d1a-ba55-a889f094158d
TQID: https://experienceleague.adobe.com/TMdBCvfpmoU6cWCqaC8W4JJpIiyt4tXY7Lun7-p-rHA
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: bd989d82-1e15-4534-88db-f1f51dd77ffaid: c32adafa-ed01-4b31-997e-2413013911b0id: cc250cf1-34eb-4863-80d0-d170d45ea067id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d095671a-1355-40aa-8b5f-06c33c68080bid: ebde5b41-29c9-4f5e-9ef6-1197e85409e3id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 430
ht-degree: 6%

---

# Guide des systèmes d’administration Adobe Commerce

Ce guide est destiné aux administrateurs système et aux intégrateurs qui travaillent dans Adobe Commerce et Magento Open Source Admin. Il fournit des informations détaillées sur la sécurité des administrateurs, les opérations de maintenance et les ressources à l’échelle du système qui prennent en charge les activités de plusieurs fonctions organisationnelles pour votre entreprise d’e-commerce. Il suppose une compréhension de base de la configuration et des fonctionnalités de base de Commerce.

Ce guide couvre les sujets suivants :

| Objet | Description |
| ------- | ----------- |
| [Introduction](introduction.md) | Présentation des systèmes et des fonctions d’intégration dans une instance Commerce. |
| [Menu système](system-menu.md) | Utilisez le menu [!UICONTROL System] pour accéder aux outils d’import et d’export de données, de gestion des index et du cache système, de gestion des comptes d’utilisateurs et des autorisations, de sauvegardes, de notifications système et de variables personnalisées. |
| [Comptes et autorisations d’administrateur](permissions.md) | Gérez les comptes utilisateur des administrateurs et les rôles utilisés pour accorder l’accès aux fonctions de magasin. |
| [ Variables ](variables-predefined.md) | Les variables facilitent la personnalisation des modèles d’e-mail et de newsletter, ainsi que d’autres types de contenu qui prennent en charge votre site et l’expérience client. |
| [Modèles d’e-mail](email-templates.md) | Les modèles d’e-mail définissent la disposition, le contenu et la mise en forme des messages automatisés envoyés depuis votre boutique. Ils sont appelés e-mails transactionnels , car chacun est associé à un type de transaction ou d’événement spécifique. |
| [Transfert de données ](data-transfer.md) | <ul><li>Les outils d’import et d’export vous permettent de gérer plusieurs enregistrements en une seule opération. Vous pouvez non seulement importer de nouveaux éléments, mais également mettre à jour, remplacer et supprimer des ensembles de produits existants.</li><li>Affichez le statut de synchronisation des données pour les entités transférées vers les services Commerce connectés à partir du [[!UICONTROL Data Management Dashboard]](data-dashboard.md).</li><li>Surveillez le statut de synchronisation pour l’exportation des flux de données vers les services SaaS Commerce à partir de la page [[!UICONTROL Data Export Feed Sync Status]](data-feed-sync-status.md) .</li></ul> |
| [Journaux d’actions](action-log.md) | Pour Adobe Commerce, les journaux d’actions capturent chaque modification apportée par un utilisateur administrateur qui travaille dans votre boutique. Vous pouvez ainsi suivre toutes les modifications apportées à votre boutique. |
| Outils | [!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."} Les administrateurs système disposent d’un ensemble d’outils : les [ outils d’assistance](support.md) sont conçus pour identifier les problèmes connus de votre système. Les outils système fournissent un support opérationnel pour effectuer la gestion de routine [index](index-management.md) et [cache](cache-management.md), [sauvegarder le système](backups.md), gérer les [opérations planifiées](data-scheduled-import-export.md) et utiliser un assortiment d’outils de développement [](developer-tools.md). |
| [ Intégrations ](integrations.md) | Déterminez l’emplacement des informations d’identification OAuth et fournissez les URL de redirection pour les intégrations tierces. |
| [Sécurité](security.md) | Découvrez les outils disponibles pour sécuriser votre boutique et vos données, ainsi que les directives d’un plan d’action de sécurité si vous détectez une compromission. |

{style="table-layout:auto"}

## Documentation disponible

{{docs-links}}
