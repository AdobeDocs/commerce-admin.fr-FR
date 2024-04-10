---
title: Fragments de code
description: Notes et éléments visuels réutilisés pour noter une fonctionnalité ou une page s’appliquant à une édition spécifique
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# Fragments de code

## Fonctionnalité EE uniquement {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Fonctionnalité Adobe Commerce" src="../assets/adobe-logo.svg" width="20" height="20" /> Fonctionnalité exclusive uniquement dans Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">En savoir plus</a>)</td></tr>
</table>

## Fonctionnalité B2B uniquement {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Fonctionnalité B2B pour Adobe Commerce" src="../assets/b2b.svg" width="20" height="20" /> Fonctionnalité exclusive disponible uniquement avec <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=en">B2B pour Adobe Commerce</a></td></tr>
</table>

## Fonctionnalité CE uniquement {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Fonction Magento Open Source" src="../assets/open-source.svg" width="20" height="20" /> Une autre méthode est requise pour Magento Open Source (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">En savoir plus</a>)</td></tr>
</table>

## Note d’authentification de l’administrateur IMS {#ims-admin-note}

>[!NOTE]
>
>Les commerçants Adobe Commerce qui disposent d’une Adobe ID et souhaitent une connexion rationalisée aux produits Adobe Commerce et Adobe Business peuvent intégrer l’authentification Commerce Admin au workflow d’authentification Adobe IMS. Une fois cette intégration activée pour votre boutique Commerce, chaque utilisateur administrateur doit utiliser ses informations d’identification d’Adobe, et non celles de son compte Commerce, pour se connecter. Voir [Présentation de l’intégration d’Adobe Commerce à Adobe IMS](/help/getting-started/adobe-ims-integration-overview.md).

## Remarque sur les API GTag {#gtag-api-note}

>[!NOTE]
>
>À partir de la version 2.4.5, l’intégration des services Google est mise à jour afin de prendre en charge l’utilisation des API GTag. GTag est un mécanisme unifié d’intégration de la fonctionnalité Google pour les pages web. Il prend en charge les fonctionnalités et opportunités les plus récentes pour le suivi et la gestion du contenu via les services Google. Pour plus d’informations, voir [Documentation destinée aux développeurs et développeuses de Google Analytics](https://developers.google.com/analytics/devguides/collection/gtagjs).

## Note de saut automatique de réécriture d&#39;URL {#url-rewrite-skip}

>[!NOTE]
>
>Lorsque les redirections automatiques sont activées et que vous enregistrez une catégorie, toutes les réécritures de produit et de catégorie sont générées en temps réel et stockées dans des tables de réécriture par défaut. Ce processus peut entraîner des problèmes de performances importants pour les catégories comportant de nombreux produits attribués. La solution consiste à modifier cette valeur par défaut et à ignorer la génération de réécritures d’URL de catégorie/produits pour l’enregistrement de catégorie. Dans ce cas, les réécritures de produit ne sont générées que pour l’URL canonique du produit. Voir [Redirections automatiques de produits](/help/merchandising-promotions/url-redirect-product-automatic.md) pour plus d’informations.

## Remarque sur les paramètres de réécriture d&#39;URL {#url-rewrite-params}

>[!IMPORTANT]
>
>Dans le processus de redirection, tous les paramètres de GET spécifiés dans l’URL sont supprimés pour des raisons de sécurité.

## Nouvelle règle de prix {#new-price-rule}

>[!NOTE]
>
>Les règles de prix sont automatiquement traitées avec d’autres règles système. La fréquence de traitement dépend du [configuration cron](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html). Lorsque vous créez une règle de prix, prévoyez suffisamment de temps pour qu’elle entre dans le système. Lorsque vous êtes sûr qu’elle se trouve dans le système, testez la règle.

## Paramètres de configuration {#config}

Pour accéder aux paramètres de configuration du magasin, choisissez **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**à partir du_ Admin _barre latérale.

## Obsolescence de l’API UPS {#ups-api}

>[!IMPORTANT]
>
>À compter de juin 2024, les commerçants Adobe Commerce ne pourront plus effectuer de transactions avec l’intégration UPS actuelle. En effet, les API United Parcel Service (UPS) utilisées par l’intégration native d’Adobe Commerce ne prennent actuellement pas en charge le modèle de sécurité OAuth 2.0 requis. Pour en savoir plus sur cette modification, voir [_Guide de migration des clés d’accès au portail des développeurs_](https://developer.ups.com/oauth-developer-guide). <br/>
>
>Les commerçants devraient [appliquer une mise à jour de correctif qualité](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html) vers leur magasin pour migrer de l’API SOAP vers l’API RESTful, qui prend en charge les protocoles d’authentification OAuth 2.0.


## Documentation disponible {#docs-links}

| Ressource de documentation | Description |
|----------------------- | ----------- |
| [Documentation pour les commerçants Adobe Commerce 2.4](../landing/home.md) | Documentation axée sur les commerçants pour Adobe Commerce et Magento Open Source |
| [Documentation des services pour Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) | Documentation à l&#39;appui d&#39;un ensemble de services qui aident les commerçants à intégrer les composantes clés de leur entreprise à leur magasin. |
| [Guide de Commerce sur les infrastructures cloud](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | Cette section contient des procédures détaillées pour déployer Adobe Commerce sur une plateforme cloud d’hébergement automatisée et gérée. |
| [Guides opérationnels d’Adobe Commerce 2.4](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | Documentation sur les systèmes relative aux concepts, processus, outils et bonnes pratiques pour développer, déployer et gérer des projets déployés sur Adobe Commerce et les plateformes de Magento Open Source. |
| [Documentation destinée aux développeurs d’Adobe Commerce 2.4](https://developer.adobe.com/commerce/docs) | Documentation destinée aux développeurs utilisée pour créer et personnaliser Adobe Commerce ou Magento Open Source |

{style="table-layout:auto"}
