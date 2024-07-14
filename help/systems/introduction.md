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

Les variables sont des informations qui peuvent être créées une seule fois et utilisées à plusieurs endroits. Votre magasin comprend de nombreuses variables prédéfinies qui peuvent être facilement utilisées pour personnaliser les modèles [email](email-templates.md) et [newsletter](../merchandising-promotions/newsletter-template.md) et d’autres types de [contenu](../content-design/introduction.md#content). Vous pouvez également créer des variables personnalisées pour incorporer des informations spécifiques à vos besoins.

- [Variables prédéfinies](variables-predefined.md)
- [Variables personnalisées](variables-custom.md)

Une des tâches à effectuer avant de lancer votre boutique consiste à passer en revue les modèles d’email utilisés pour toutes les communications envoyées depuis votre boutique afin de vous assurer qu’elles reflètent votre marque. Cela inclut la personnalisation des modèles d’email et de newsletter [, ainsi que des factures PDF et des bordereaux d’emballage. ](../merchandising-promotions/newsletter-template.md) Il comprend également la personnalisation du contenu avec des variables et des [balises de balisage](markup-tags.md).

## Gestion des opérations

L’administrateur prend également en charge diverses tâches permettant aux administrateurs système de gérer les utilisateurs administrateurs au sein de leur entreprise et d’exploiter le magasin. Il s’agit notamment des outils suivants :

- **Comptes utilisateur et autorisations d’administrateur** - Gérez les [ comptes d’utilisateur ](permissions-users-all.md) de l’administrateur, ainsi que les [ rôles et autorisations associés ](permissions-user-roles.md) qui contrôlent leur accès aux sites et aux zones fonctionnelles dans l’administrateur.
- **Sessions d’administrateur et restrictions du site web** - Passez en revue les bonnes pratiques [security](security.md), découvrez comment gérer les sessions d’administrateur et les informations d’identification, mettre en oeuvre CAPTCHA et gérer les restrictions du site web.
- **Outils système** - Exécutez la routine [index](index-management.md) et les [opérations de gestion du cache](cache-management.md), [sauvegarder](backups.md) le système, gérer les [opérations planifiées](data-scheduled-import-export.md) et utiliser un assortiment de [outils de développement](developer-tools.md).
- **Transfert de données** - Utilisez les outils de [ transfert de données](data-transfer.md) pour importer et exporter des données, ainsi que pour gérer les données sur les produits, les prix, les clients et les taux d’imposition.
- **Intégrations** - Définissez l’emplacement des informations d’identification OAuth et l’URL de redirection pour les [intégrations tierces](integrations.md) et identifiez les ressources d’API disponibles.
- **Logs d’action** - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Accédez aux enregistrements ([journaux d’action](action-log.md)) pour les modifications effectuées par les utilisateurs administrateurs travaillant dans votre boutique.
- **Outils d’assistance** - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Les outils d’assistance ([Collecteur de données](support.md#data-collector) et [Rapports système](support.md#access-system-reports)) sont conçus pour identifier les problèmes connus de votre système. Ils peuvent être utilisés comme ressource au cours des processus de développement et d’optimisation, et comme outil de diagnostic pour aider notre équipe d’assistance à identifier et résoudre les problèmes.
