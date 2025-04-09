---
title: Qu’est-ce que l’administrateur ?
description: Découvrez l [!DNL Commerce] Admin, l’endroit où les commerçants configurent des produits et des promotions, gèrent les commandes et effectuent d’autres tâches administratives.
exl-id: 065cf14f-80e7-4695-8922-c761a2191d72
source-git-commit: a6b293dca673808bbc7f37cb468c6e316fddb735
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---


# Qu’est-ce que l’administrateur ?

Votre boutique _Admin_ est le back-office protégé par mot de passe où vous, en tant que commerçant, configurez des produits et des promotions, gérez les commandes et effectuez d&#39;autres tâches administratives. Toutes les tâches de configuration de base et les opérations de gestion de magasin sont effectuées à partir de l’_Admin_.

Pour plus de sécurité, la connexion _Admin_ est protégée par [authentification à deux facteurs](../systems/security-two-factor-authentication.md) et peut être configurée pour nécessiter un [CAPTCHA](../systems/security-captcha.md). Pour en savoir plus, accédez à [Configuration d’Admin Security](../systems/security-admin.md).

![Barre latérale et tableau de bord administrateur](./assets/admin-dashboard.png){width="700" zoomable="yes"}

Vos informations d’identification [de connexion](admin-signin.md) initiales ont été configurées lors de l’installation d’Adobe Commerce ou de Magento Open Source. Si vous oubliez votre mot de passe, un mot de passe temporaire peut être envoyé à l’adresse e-mail associée au compte. Pour renforcer la sécurité, configurez votre boutique pour qu’elle exige un nom d’utilisateur sensible à la casse et un mot de passe fort.

Outre le compte utilisateur administrateur par défaut, votre entreprise peut créer autant de comptes [comptes supplémentaires](../systems/permissions-users-all.md) dont vous avez besoin pour gérer le magasin et prendre en charge les comptes clients. Chaque compte peut être associé à un [rôle](../systems/permissions-user-roles.md) et à un niveau d’accès spécifiques, en fonction des besoins de l _entreprise_. L’adresse e-mail associée à chaque compte utilisateur administrateur doit être unique.

{{ims-admin-note}}

## Collecte des données d’utilisation

La première fois que vous vous connectez à _Admin_, vous êtes invité à accorder à Adobe l’autorisation de collecter des données d’utilisation pour tous les utilisateurs administrateurs. En permettant à l’administrateur de collecter des données d’utilisation, vous aidez Adobe à améliorer son expérience d’utilisation d’Adobe Commerce Admin et des produits et services associés.

![Autoriser la collecte de données d&#39;utilisation par l&#39;administrateur](./assets/admin-usage-data.png){width="600"}

Les utilisateurs individuels ne sont pas identifiés dans les données d’utilisation. Vos paramètres de collecte de données peuvent être modifiés à tout moment à partir de la configuration [Utilisation par l’administrateur](../configuration-reference/advanced/admin.md#admin-usage).

Pour Adobe Commerce, autoriser la collecte de données active également le _conseil intégré au produit_, qui est conçu pour apporter du contenu interactif à l’_administrateur_. Il fournit de l’aide, des info-bulles, des guides détaillés, des informations d’intégration, des annonces de fonctionnalités, etc.
