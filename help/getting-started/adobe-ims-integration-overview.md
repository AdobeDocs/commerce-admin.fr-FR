---
title: Présentation de l’intégration d’Adobe Identity Management Service (IMS)
description: Introduit l’intégration facultative de la connexion de l’administrateur Adobe Commerce avec Adobe IMS.
exl-id: 106d731c-a541-4a19-a38c-221e80740508
feature: Identity Management
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# Présentation de l’intégration d’Adobe Identity Management Service (IMS)

{{ee-feature}}

Les utilisateurs administrateurs Adobe Commerce qui disposent d’un compte Adobe peuvent désormais utiliser leur Adobe ID pour se connecter à Adobe Commerce. Adobe Identity Management Service (IMS) est une fonctionnalité de gestion des identités basée sur OAuth 2.0 d’Adobe qui prend en charge l’authentification. L’intégration de l’authentification de l’administrateur Commerce dans le workflow d’authentification IMS d’Adobe Business Product peut rationaliser le processus d’authentification pour les utilisateurs qui travaillent avec d’autres produits Adobe. Cette intégration est facultative et activée sur une base par instance. Seuls les workflows des utilisateurs administrateurs sont affectés lorsque cette intégration est activée. 

Les modules requis pour l’intégration IMS de l’administrateur Commerce sont inclus dans le package `adobe-ims-metapackage`, qui est fourni avec les versions principales d’Adobe Commerce.

Pour mettre en oeuvre cette intégration, voir [Configuration de l’intégration d’administrateur Commerce avec IMS](./adobe-ims-config.md).

## Modifications apportées aux processus et à l’interface d’administration après l’intégration à IMS

Lorsque cette intégration est activée, les utilisateurs administrateurs de Commerce subissent des modifications dans le processus de connexion et d’authentification de l’administrateur Commerce par défaut, car ils effectuent des tâches routinières dans l’administrateur qui nécessitent une réauthentification, comme la création d’un utilisateur administrateur. L’application de l’authentification à deux facteurs (2FA) au niveau de l’organisation Adobe est requise pour l’activation des modules. La connexion d’administrateur par défaut et la connexion 2FA sont désactivées, et le bouton _[!UICONTROL Sign In with Adobe ID]_&#x200B;remplace la connexion d’administrateur par défaut dans le formulaire. Les droits sont toujours gérés par l’administrateur.

## Comment l’intégration de l’administrateur à IMS affecte les mots de passe Commerce

Les déploiements Commerce qui ont été intégrés à Adobe IMS nécessitent un compte Adobe ID ayant accès à l’organisation Adobe IMS configurée pour l’application Commerce pendant le processus d’activation IMS.  Lorsque l’intégration IMS est activée, les utilisateurs administrateurs s’authentifient via la page de connexion à l’Adobe à l’aide de leurs informations d’identification d’Adobe. Les mots de passe et noms d’utilisateur Commerce des utilisateurs administrateurs ne sont plus utilisés pour l’authentification tant que l’intégration Adobe IMS est activée.

Si l’intégration IMS est désactivée, les utilisateurs administrateurs doivent à nouveau s’authentifier via Adobe Commerce à l’aide de leur nom d’utilisateur et mot de passe Commerce. Les utilisateurs administrateurs doivent enregistrer leurs informations d’identification d’administrateur Commerce (nom d’utilisateur et mot de passe) et leurs informations d’identification 2FA avant d’activer cette intégration.

Certains composants principaux impliqués dans l’authentification de l’utilisateur nécessitent toujours un mot de passe non nul. Pour répondre à cette exigence, Commerce crée des mots de passe aléatoires pour les utilisateurs administrateurs nouvellement créés dans la table `admin_user`.

Les comptes utilisateur et les autorisations de rôle pour l’application Commerce sont toujours gérés à partir de l’administrateur Commerce.


## Génération de jetons API web avec les informations d’identification IMS

Les API d’administration de Commerce sont affectées lorsque l’authentification d’administrateur avec Adobe IMS est activée dans une instance Commerce. Les utilisateurs administrateurs ne peuvent plus utiliser les informations d’identification émises par l’instance Commerce. Il s’agit des informations d’identification requises pour se connecter à l’administrateur et obtenir des jetons d’accès que les services peuvent utiliser pour envoyer des requêtes aux API REST et SOAP de l’administrateur.

Une fois l’intégration Adobe IMS activée, les utilisateurs administrateurs doivent utiliser les [jetons OAuth Adobe IMS](https://developer.adobe.com/developer-console/docs/guides/authentication/OAuthIntegration/) pour les points de terminaison de l’API Adobe Commerce nécessitant une authentification. Les solutions clientes obtiennent les jetons dynamiquement pour l’utilisation de l’API web. Ce mécanisme d’authentification est activé pour les zones REST et SOAP API web dans le cadre de la configuration de cette intégration.

Voir [Authentification basée sur les jetons](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-token/) pour un aperçu de la manière dont les API web utilisent les jetons d’accès Commerce, y compris les jetons d’accès IMS.

## Gestion de session Commerce et jetons d’accès Adobe IMS

Les jetons d’accès contiennent à la fois les informations d’identification de l’utilisateur et les informations de session de connexion. Une fois qu’un utilisateur a été authentifié et qu’une session a commencé, ces deux variables sont ajoutées à la session de l’utilisateur :

`token_last_check_time`. Identifie l’heure actuelle et est utilisé par le module externe `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin`.

`adobe_access_token` — Identifie la valeur `ACCESS_TOKEN` reçue lors de l’autorisation.

Le module externe `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` vérifie si `token_last_check_time` a été mis à jour il y a 10 minutes. Si `token_last_check_time` a été vérifié il y a dix minutes, le workflow d’authentification lance un appel API à IMS pour valider le jeton d’accès, et la session se poursuit. Si le jeton d’accès est valide, la valeur `token_last_check_time` est mise à jour à l’heure actuelle. Si le jeton n’est pas valide, la session est arrêtée.

## Fichiers importants

`adminAdobeIms` - Fournit une implémentation de la connexion administrateur basée sur le module `AdobeImsApi`.

`admin_adobe_ims_webapi` - Conserve un enregistrement de tous les jetons d’accès validés. Lorsqu’un jeton est validé ou invalidé, un enregistrement de son état est conservé dans ce tableau.

`adobeIms` - Implémente toute la logique commerciale liée à l’intégration avec Adobe IMS (conservée pour empêcher les incompatibilités ascendantes).

`adobeImsApi` - Déclare les interfaces qui prennent en charge l’intégration à Adobe IMS.

`adminadobe-ims.log` - Fichier journal des erreurs.

## Activation de l’intégration

Le métaphorage Adobe IMS est installé avec Adobe Commerce 2.4.5 et versions ultérieures, mais doit être configuré pour être utilisé. Il étend le module `AdobeIms` pour prendre en charge le module qui active la logique d’authentification (`AdminAdobeIms`).

Pour plus d’informations sur l’activation de l’intégration, voir [Configuration de l’intégration d’administration Commerce avec Adobe IMS](./adobe-ims-config.md).
