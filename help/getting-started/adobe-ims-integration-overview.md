---
title: Présentation de l’intégration du service Adobe Identity Management (IMS)
description: Introduit l’intégration facultative de la connexion administrateur Adobe Commerce à Adobe IMS
exl-id: 106d731c-a541-4a19-a38c-221e80740508
feature: Identity Management
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 15118877bb8cc533b2323819db34da0513899e25
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 0%

---

# Présentation de l’intégration du service Adobe Identity Management (IMS)

{{ee-feature}}

Les utilisateurs administrateurs d’Adobe Commerce qui disposent d’un compte Adobe peuvent désormais utiliser leur Adobe ID pour se connecter à Adobe Commerce. Le service Adobe Identity Management (IMS) est une fonctionnalité de gestion des identités basée sur OAuth 2.0 d’Adobe qui prend en charge l’authentification. L’intégration de l’authentification Commerce Admin au workflow d’authentification IMS du produit Adobe Business peut rationaliser le processus d’authentification pour les utilisateurs qui travaillent avec d’autres produits Adobe. Cette intégration est facultative et est activée sur une base par instance. Seuls les workflows utilisateur administrateur sont affectés lorsque cette intégration est activée. 

Les modules requis pour l’intégration Commerce Admin IMS sont fournis dans `adobe-ims-metapackage`, qui est fourni avec les versions de base d’Adobe Commerce.

Pour implémenter cette intégration, consultez [Configuration de l’intégration d’administration Commerce avec IMS](./adobe-ims-config.md).

## Modifications des workflows et de l’interface d’administration après l’intégration avec IMS

Lorsque cette intégration est activée, les utilisateurs administrateurs de Commerce subissent des modifications du workflow d’authentification et de connexion par défaut d’Commerce Admin lorsqu’ils effectuent des tâches de routine dans l’administration nécessitant une réauthentification, telles que la création d’un utilisateur administrateur. L’application de l’authentification à deux facteurs (2FA) au niveau de l’organisation Adobe est requise pour l’activation du module . Les paramètres de connexion d’administrateur par défaut et 2FA sont désactivés, et le bouton _[!UICONTROL Sign In with Adobe ID]_&#x200B;remplace le formulaire de connexion d’administrateur par défaut. Les droits sont toujours gérés à partir de l’administrateur.

## Impact de l’intégration d’administration avec IMS sur les mots de passe Commerce

Les déploiements de Commerce intégrés à Adobe IMS nécessitent un compte Adobe ID ayant accès à l’organisation Adobe IMS configurée pour l’application Commerce pendant le processus d’activation IMS.  Lorsque l’intégration IMS est activée, les utilisateurs administrateurs s’authentifient via la page de connexion d’Adobe à l’aide de leurs informations d’identification Adobe. Les mots de passe et noms d’utilisateur Commerce pour les utilisateurs administrateurs ne sont plus utilisés pour l’authentification tant que l’intégration Adobe IMS est activée.

Si l’intégration IMS est désactivée, les utilisateurs administrateurs doivent s’authentifier à nouveau via Adobe Commerce à l’aide de leurs nom d’utilisateur et mot de passe Commerce. Les utilisateurs administrateurs doivent enregistrer leurs informations d’identification d’administrateur Commerce (nom d’utilisateur et mot de passe) et 2FA avant d’activer cette intégration.

Certains composants principaux impliqués dans l’authentification des utilisateurs nécessitent toujours un mot de passe non nul. Pour répondre à cette exigence, Commerce crée des mots de passe aléatoires pour les utilisateurs administrateurs nouvellement créés dans le tableau `admin_user`.

Les comptes utilisateur et les autorisations de rôle pour l’application Commerce sont toujours gérés par l’administrateur Commerce.


## Génération de jetons API Web avec les informations d’identification IMS

Les API d’administration Commerce sont affectées lorsque l’authentification de l’administrateur avec Adobe IMS est activée dans une instance Commerce. Les utilisateurs administrateurs ne peuvent plus utiliser les informations d’identification émises par l’instance Commerce. Il s’agit des informations d’identification requises pour se connecter à l’administrateur et obtenir des jetons d’accès que les services peuvent utiliser pour envoyer des requêtes aux API REST d’administration et SOAP.

Une fois l’intégration Adobe IMS activée, les utilisateurs administrateurs doivent utiliser des [jetons OAuth Adobe IMS](https://developer.adobe.com/developer-console/docs/guides/authentication/) pour les points d’entrée de l’API Adobe Commerce qui nécessitent une authentification. Les solutions clientes obtiennent les jetons de manière dynamique pour l’utilisation de l’API web. Ce mécanisme d’authentification est activé pour les zones d’API web REST et SOAP dans le cadre de la configuration de cette intégration.

Consultez [Authentification basée sur les jetons](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-token/) pour un aperçu de la manière dont les API web utilisent les jetons d’accès Commerce, y compris les jetons d’accès IMS.

## Gestion des sessions Commerce et jetons d’accès Adobe IMS

Les jetons d’accès contiennent les informations d’identification utilisateur et de connexion. Une fois qu’un utilisateur a été authentifié et qu’une session a commencé, ces deux variables sont ajoutées à la session de l’utilisateur :

`token_last_check_time`. Identifie l’heure actuelle et est utilisé par le plug-in `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin`.

`adobe_access_token` — Identifie la valeur `ACCESS_TOKEN` reçue pendant l&#39;autorisation.

Le plug-in `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` vérifie si le `token_last_check_time` a été mis à jour il y a 10 minutes. Si la `token_last_check_time` a été vérifiée il y a dix minutes, le workflow d’authentification effectue un appel API à IMS pour valider le jeton d’accès et la session se poursuit. Si le jeton d’accès est valide, la valeur `token_last_check_time` est mise à jour sur l’heure actuelle. Si le jeton n’est pas valide, la session est interrompue.

## Fichiers importants

`adminAdobeIms` - Fournit une implémentation de l’ID de connexion d’administrateur en fonction du module `AdobeImsApi`.

`admin_adobe_ims_webapi` - Conserve un enregistrement de tous les jetons d’accès validés. Lorsqu’un jeton est validé ou invalidé, un enregistrement de son statut est conservé dans ce tableau.

`adobeIms` - Implémente toute la logique commerciale liée à l’intégration avec Adobe IMS (conservée pour éviter les incompatibilités descendantes).

`adobeImsApi` : déclare les interfaces qui prennent en charge l’intégration à Adobe IMS.

`adminadobe-ims.log` - Fichier journal des erreurs.

## Activation de l’intégration

Le métapaquet Adobe IMS est installé avec Adobe Commerce 2.4.5 et versions ultérieures, mais doit être configuré pour être utilisé. Il étend le module `AdobeIms` pour prendre en charge le module qui active la logique d’authentification (`AdminAdobeIms`).

Pour plus d’informations sur l’activation de l’intégration, voir [&#x200B; Configuration de l’intégration d’administration Commerce avec Adobe IMS &#x200B;](./adobe-ims-config.md).
