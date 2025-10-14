---
title: Présentation des systèmes d’administration
description: Découvrez les outils et les fonctions système que l’administrateur du magasin peut utiliser pour gérer efficacement les sites, les données, les intégrations et les utilisateurs administrateurs.
exl-id: 52792a89-8f6f-4230-9a04-e193b3943410
source-git-commit: 5517bb16a8f7c8aa2f9f057df773f142302a69c7
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# Présentation des systèmes d’administration

Le Store Admin est le back-office sécurisé où les commerçants configurent les produits et les promotions, gèrent les commandes et effectuent d&#39;autres tâches administratives. Toutes les tâches de configuration de base et les opérations de gestion des magasins sont effectuées par l’administrateur. Il existe également des fonctions qui fournissent une prise en charge de plusieurs fonctionnalités de magasin que les administrateurs peuvent gérer pour leur entreprise.

## Variables et communications client

Les variables sont des informations qui peuvent être créées une seule fois et utilisées à plusieurs endroits. Votre boutique comprend de nombreuses variables prédéfinies qui peuvent être facilement utilisées pour personnaliser les modèles [e-mail](email-templates.md) et [newsletter](../merchandising-promotions/newsletter-template.md), ainsi que d’autres types de [contenu](../content-design/introduction.md#content). Vous pouvez également créer des variables personnalisées pour incorporer des informations spécifiques à vos besoins.

- [Variables prédéfinies](variables-predefined.md)
- [Variables personnalisées](variables-custom.md)

L’une des tâches à effectuer avant de lancer votre boutique consiste à examiner les modèles d’e-mail utilisés pour toutes les communications envoyées depuis votre boutique afin de s’assurer qu’ils reflètent votre marque. [&#x200B; Vous pouvez notamment personnaliser les modèles d’e-mail et de newsletter](../merchandising-promotions/newsletter-template.md) ainsi que les factures et bons de livraison PDF. Il comprend également la personnalisation du contenu avec des variables et des [&#x200B; balises de balisage &#x200B;](markup-tags.md).

## Gestion des opérations

L’administrateur prend également en charge diverses tâches permettant aux administrateurs système de gérer les utilisateurs administrateurs au sein de leur organisation et d’exploiter la boutique. Il s’agit des outils suivants :

- **Comptes utilisateur et autorisations d’administrateur** - Gérez les comptes utilisateur [Admin](permissions-users-all.md), ainsi que les [rôles et autorisations associés](permissions-user-roles.md) qui contrôlent leur accès aux sites et aux zones fonctionnelles dans l’administration.
- **Sessions d’administration et restrictions de site web** - Examinez les bonnes pratiques en matière de [sécurité](security.md) et apprenez à gérer les informations d’identification et les sessions d’administration, à implémenter CAPTCHA et à gérer les restrictions de site web.
- [!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."} **Outils système** - Effectuez des opérations de gestion de routine [index](index-management.md) et [cache](cache-management.md), [sauvegardez](backups.md) le système, gérez [opérations planifiées](data-scheduled-import-export.md) et utilisez un ensemble d’outils de développement [&#128279;](developer-tools.md).
- **Transfert de données** - Utilisez les outils [transfert de données](data-transfer.md) pour importer et exporter des données, ainsi que pour gérer les données sur les produits, les prix, les clients et les taux de taxe.
- **Intégrations** - Déterminez l’emplacement des informations d’identification OAuth et l’URL de redirection pour les [intégrations tierces](integrations.md) et identifiez les ressources d’API disponibles.
- **Journaux d’actions** - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Accédez aux enregistrements ([journaux d’actions](action-log.md)) pour les modifications apportées par les utilisateurs administrateurs travaillant dans votre boutique.
- [!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."} **Outils de support** - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) [Rapports système](support.md#access-system-reports)) sont conçus pour identifier les problèmes connus de votre système. Ils peuvent être utilisés comme ressource au cours des processus de développement et d’optimisation, et comme outil de diagnostic pour aider notre équipe d’assistance à identifier et résoudre les problèmes.
