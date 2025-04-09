---
title: Fragments de code
description: Notes et éléments visuels réutilisés pour noter une fonctionnalité ou une page s’appliquant à une édition spécifique
source-git-commit: e82b979ee2c5f51caba6a2aa416c5f20dbce110a
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%

---

# Fragments de code

## Fonctionnalité EE uniquement {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Fonctionnalité Adobe Commerce" src="../assets/adobe-logo.svg" width="20" height="20" /> Fonctionnalité exclusive uniquement dans Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">En savoir plus</a>)</td></tr>
</table>

## Fonctionnalité B2B uniquement {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Fonctionnalité B2B d’Adobe Commerce" src="../assets/b2b.svg" width="20" height="20" /> Fonction exclusive disponible uniquement avec <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=en">Adobe Commerce B2B</a></td></tr>
</table>

## Fonctionnalité CE uniquement {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Fonctionnalité Magento Open Source" src="../assets/open-source.svg" width="20" height="20" /> Une autre méthode est requise pour Magento Open Source (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">En savoir plus</a>).</td></tr>
</table>

## Note d’authentification de l’administrateur IMS {#ims-admin-note}

>[!NOTE]
>
>Les commerçants Adobe Commerce qui disposent d’une Adobe ID et souhaitent une connexion rationalisée aux produits Adobe Commerce et Adobe Business peuvent intégrer l’authentification Commerce Admin au workflow d’authentification Adobe IMS. Une fois cette intégration activée pour votre boutique Commerce, chaque utilisateur administrateur doit utiliser ses informations d’identification Adobe, et non ses informations d’identification de compte Commerce, pour se connecter. Voir [ Intégration d’Adobe Commerce à Adobe IMS](/help/getting-started/adobe-ims-integration-overview.md).

## Remarque sur les API GTag {#gtag-api-note}

>[!NOTE]
>
>À partir de la version 2.4.5, l’intégration des services Google est mise à jour afin de prendre en charge l’utilisation des API GTag. GTag est un mécanisme unifié d’intégration de la fonctionnalité Google pour les pages web. Il prend en charge les fonctionnalités et opportunités les plus récentes pour le suivi et la gestion du contenu via les services Google. Pour plus d’informations, consultez la [documentation destinée aux développeurs de Google Analytics](https://developers.google.com/analytics/devguides/collection/gtagjs).

## Note de saut automatique de réécriture d&#39;URL {#url-rewrite-skip}

>[!NOTE]
>
>Lorsque les redirections automatiques sont activées et que vous enregistrez une catégorie, toutes les réécritures de produit et de catégorie sont générées en temps réel et stockées dans des tables de réécriture par défaut. Ce processus peut entraîner des problèmes de performances importants pour les catégories comportant de nombreux produits attribués. La solution consiste à modifier cette valeur par défaut et à ignorer la génération de réécritures d’URL de catégorie/produits pour l’enregistrement de catégorie. Dans ce cas, les réécritures de produit ne sont générées que pour l’URL de produit canonique. Pour plus d’informations, consultez [Redirections automatiques de produits](/help/merchandising-promotions/url-redirect-product-automatic.md).

## Remarque sur les paramètres de réécriture d&#39;URL {#url-rewrite-params}

>[!IMPORTANT]
>
>Dans le processus de redirection, tous les paramètres GET spécifiés dans l’URL sont supprimés pour des raisons de sécurité.

## Nouvelle règle de prix {#new-price-rule}

>[!NOTE]
>
>Les règles de prix sont automatiquement traitées avec d’autres règles système. La fréquence de traitement dépend de la configuration [cron](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html). Lorsque vous créez une règle de prix, laissez suffisamment de temps pour qu’elle entre dans le système. Lorsque vous êtes sûr qu’elle se trouve dans le système, testez la règle.

## Paramètres de configuration {#config}

Pour accéder aux paramètres de configuration du magasin, sélectionnez **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**dans la barre latérale_ Admin _.

## Obsolescence de l’API UPS {#ups-api}

>[!IMPORTANT]
>
>À compter de juin 2024, les commerçants Adobe Commerce ne pourront plus effectuer de transactions avec l’intégration UPS actuelle. En effet, les API United Parcel Service (UPS) utilisées par l’intégration native d’Adobe Commerce ne prennent actuellement pas en charge le modèle de sécurité OAuth 2.0 requis. Pour activer l’intégration, [créez une application sur la plateforme de développement UPS](https://developer.ups.com/get-started) afin d’obtenir les informations d’identification requises pour OAuth 2.0. Utilisez les nouvelles informations d’identification comme `username` et `password` dans la configuration d’expédition UPS de Commerce. Pour en savoir plus sur le changement de modèle de sécurité, voir [Developer Portal Access Key Migration Guide_](https://developer.ups.com/oauth-developer-guide). <br/>
>
>Les commerçants doivent [appliquer une mise à jour de correctif de qualité](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html) à leur magasin pour migrer de l’API SOAP vers l’API RESTful, qui prend en charge les protocoles d’authentification OAuth 2.0.


## Documentation disponible {#docs-links}

| Ressource de documentation | Description |
|----------------------- | ----------- |
| [Guides de l’utilisateur des administrateurs d’Adobe Commerce 2.4](../landing/home.md) | Documentation et ressources pour les commerçants travaillant dans l’administration. |
| [Documentation Services pour Adobe Commerce](https://experienceleague.adobe.com/docs/commerce/user-guides/home.html) | Documentation pour prendre en charge un ensemble de services de marchandisage qui aident les commerçants à intégrer les composants clés de leur entreprise à leur magasin. |
| [Guide de Commerce sur les infrastructures cloud](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | Cette section contient des procédures détaillées pour déployer Adobe Commerce sur une plateforme cloud d’hébergement automatisée et gérée. |
| [Guides opérationnels d’Adobe Commerce 2.4](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | Documentation sur les systèmes relative aux concepts, processus, outils et bonnes pratiques pour développer, déployer et gérer Adobe Commerce sur les projets Cloud et On-Premise. |
| [Documentation destinée aux développeurs d’Adobe Commerce 2.4](https://developer.adobe.com/commerce/docs) | Documentation destinée aux développeurs utilisée pour personnaliser Adobe Commerce et l’intégrer à des systèmes tiers. |

{style="table-layout:auto"}

## Compatibilité B2B {#b2b-compatibility}

>[!IMPORTANT]
>
>Adobe Commerce B2B version 1.4.2+ est compatible avec PHP 8.2. Si vous mettez à niveau l’instance Commerce vers la version 2.4.7+, assurez-vous que l’instance utilise PHP version 8.2 pour maintenir la compatibilité avec la version B2B d’Adobe Commerce. En outre, la version B2B 1.4.2+ ne prend pas en charge le [serveur d’applications GraphQL](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server).
