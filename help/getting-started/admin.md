---
title: Qu’est-ce que l’administrateur ?
description: Découvrez l [!DNL Commerce] Admin, l’endroit où les commerçants configurent des produits et des promotions, gèrent les commandes et effectuent d’autres tâches administratives.
exl-id: 065cf14f-80e7-4695-8922-c761a2191d72
TQID: https://experienceleague.adobe.com/A0DuYohA907-EHXQ6fyy2Sz83Y6cFZ7PDY5SmtBa14Y
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: bd989d82-1e15-4534-88db-f1f51dd77ffaid: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: cc72dcf1-72e1-48cc-b434-e7c27d62d67cid: d095671a-1355-40aa-8b5f-06c33c68080bid: d3cdead0-685a-4489-9250-4bb709942f66id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 324
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
