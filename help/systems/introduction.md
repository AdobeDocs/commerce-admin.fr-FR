---
title: Présentation des systèmes d’administration
description: Découvrez les outils et fonctions système que l’administrateur du magasin peut utiliser pour gérer efficacement les sites, les données, les intégrations et les utilisateurs administrateurs.
exl-id: 52792a89-8f6f-4230-9a04-e193b3943410
source-git-commit: 46564240e7f76cf2a691c209b36d530763ba4f01
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Présentation des systèmes d’administration

L’administrateur du magasin est le back-office sécurisé où les commerçants configurent des produits et des promotions, gèrent des commandes et effectuent d’autres tâches administratives. Toutes les tâches de configuration de base et les opérations de gestion de magasin sont effectuées à partir de l’administrateur. Il existe également des fonctions qui prennent en charge plusieurs fonctionnalités de magasin que les administrateurs peuvent gérer pour leurs entreprises.

## Variables et communications client

Les variables sont des informations qui peuvent être créées une seule fois et utilisées à plusieurs endroits. Votre magasin comprend de nombreuses variables prédéfinies qui peuvent être facilement utilisées pour personnaliser [email](email-templates.md) et [newsletter](../merchandising-promotions/newsletter-template.md) modèles et autres types de [content](../content-design/introduction.md#content). Vous pouvez également créer des variables personnalisées pour incorporer des informations spécifiques à vos besoins.

- [Variables prédéfinies](variables-predefined.md)
- [Variables personnalisées](variables-custom.md)

Une des tâches à effectuer avant de lancer votre boutique consiste à passer en revue les modèles d’email utilisés pour toutes les communications envoyées depuis votre boutique afin de vous assurer qu’elles reflètent votre marque. Cela inclut la personnalisation des emails et [modèles de newsletter](../merchandising-promotions/newsletter-template.md), et les factures et bordereaux d’emballage des PDF. Il comprend également la personnalisation du contenu avec des variables et [balises marketing](markup-tags.md).

## Gestion des opérations

L’administrateur prend également en charge diverses tâches permettant aux administrateurs système de gérer les utilisateurs administrateurs au sein de leur entreprise et d’exploiter le magasin. Il s’agit notamment des outils suivants :

- **Comptes utilisateur et autorisations de l’administrateur** - Gérer l’administrateur [comptes utilisateur](permissions-users-all.md), ainsi que la variable [rôles et autorisations](permissions-user-roles.md) qui contrôlent leur accès aux sites et aux zones fonctionnelles dans l’administrateur.
- **Sessions d’administration et restrictions du site web** - Révision [sécurité](security.md) bonnes pratiques, découvrez comment gérer les sessions d’administration et les informations d’identification, mettre en oeuvre CAPTCHA et gérer les restrictions des sites web.
- **Outils système** - Effectuer une routine [index](index-management.md) et [cache](cache-management.md) les opérations de gestion, [sauvegarde](backups.md) le système, gérer [opérations planifiées](data-scheduled-import-export.md), et utilisez un assortiment de [outils de développement](developer-tools.md).
- **Transfert de données** - Utilisez la variable [transfert de données](data-transfer.md) des outils permettant d’importer et d’exporter des données, ainsi que de gérer les données sur les produits, les prix, les clients et les taux d’imposition.
- **Intégrations** - Définition de l’emplacement des informations d’identification OAuth et de l’URL de redirection pour [intégrations tierces](integrations.md)et identifier les ressources d’API disponibles.
- **Logs d’action** - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Accéder aux enregistrements ([journaux d’action](action-log.md)) pour les modifications apportées par les utilisateurs administrateurs travaillant dans votre magasin.
- **Outils d’assistance** - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Les outils de support ([Collecteur de données](support.md#data-collector) et [Rapports système](support.md#access-system-reports)) sont conçues pour identifier les problèmes connus de votre système. Ils peuvent être utilisés comme ressource au cours des processus de développement et d’optimisation, et comme outil de diagnostic pour aider notre équipe d’assistance à identifier et résoudre les problèmes.
