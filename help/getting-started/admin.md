---
title: Qu’est-ce que l’administrateur ?
description: Découvrez l’ [!DNL Commerce] administrateur, l’emplacement où les commerçants configurent des produits et des promotions, gèrent des commandes et effectuent d’autres tâches administratives.
exl-id: 065cf14f-80e7-4695-8922-c761a2191d72
source-git-commit: b657db7e486fec591d5a6239d554376f00707e8c
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Qu’est-ce que l’administrateur ?

Votre boutique _Admin_ est le back-office protégé par mot de passe où vous, en tant que commerçant, configurez des produits et des promotions, gérez les commandes et effectuez d’autres tâches administratives. Toutes les tâches de configuration de base et les opérations de gestion de magasin sont effectuées à partir de l’ _administrateur_.

Pour plus de sécurité, la connexion _Admin_ est protégée par une [authentification à deux facteurs](../systems/security-two-factor-authentication.md) et peut être configurée pour exiger un [CAPTCHA](../systems/security-captcha.md). Pour en savoir plus, consultez la page [Configuration de la sécurité de l’administrateur](../systems/security-admin.md).

![Barre latérale et tableau de bord de l’administrateur](./assets/admin-dashboard.png){width="700" zoomable="yes"}

Vos informations d’identification [de connexion](admin-signin.md) initiales ont été configurées lors de l’installation d’Adobe Commerce ou de Magento Open Source. Si vous oubliez votre mot de passe, un mot de passe temporaire peut être envoyé à l’adresse électronique associée au compte. Pour accroître la sécurité, configurez votre boutique afin d’exiger un nom d’utilisateur sensible à la casse et un mot de passe fort.

Outre le compte d’utilisateur administrateur par défaut, votre entreprise peut créer autant de [comptes supplémentaires](../systems/permissions-users-all.md) que nécessaire pour gérer le magasin et prendre en charge les comptes clients. Chaque compte peut être associé à un [rôle](../systems/permissions-user-roles.md) spécifique et à un niveau d’accès, en fonction de la _nécessité de connaître_ de l’entreprise. L’adresse électronique associée à chaque compte utilisateur administrateur doit être unique.

{{ims-admin-note}}

## Collecte de données d’utilisation

La première fois que vous vous connectez à _Admin_, vous êtes invité à accorder l’autorisation d’Adobe pour collecter des données d’utilisation pour tous les utilisateurs administrateurs. En autorisant la collecte de données d’utilisation par l’administrateur, vous contribuez à améliorer l’expérience d’utilisation de l’administrateur Adobe Commerce, ainsi que des produits et services associés.

![ Autoriser la collecte de données d’utilisation de l’administrateur ](./assets/admin-usage-data.png){width="600"}

Les utilisateurs individuels ne sont pas identifiés dans les données d’utilisation. Le paramètre de collecte de données peut être modifié à tout moment à partir de la configuration [Utilisation de l’administrateur](../configuration-reference/advanced/admin.md#admin-usage).

Pour Adobe Commerce, l’autorisation de la collecte de données active également le _guide interne au produit_, conçu pour apporter du contenu interactif à l’_administrateur_. Il fournit de l’aide, des info-bulles, des guides de présentation, des informations d’intégration, des annonces de fonctionnalités, etc.
