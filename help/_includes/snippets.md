---
title: Extraits de code
description: Remarques réutilisées et éléments visuels pour noter une fonctionnalité ou une page s’appliquant à une édition spécifique
source-git-commit: 1f84bf9ab20aeccacf56eab396b2778140964d17
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%

---

# Extraits de code

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
<tr><td><img alt="Fonctionnalité Magento Open Source" src="../assets/open-source.svg" width="20" height="20" /> Une autre méthode est requise pour Magento Open Source (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">En savoir plus</a>)</td></tr>
</table>

## Mises à jour de la version bêta 1 {#beta-updates}

>[!NOTE]
>
>[!BADGE 2.4.7-beta1]{type=Informative url="https://experienceleague.adobe.com/docs/commerce-operations/release/notes/adobe-commerce/2-4-7.html" tooltip="Disponible dans la version 2.4.7-beta1 uniquement"}[notes de mise à jour](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/adobe-commerce/2-4-7.html) pour obtenir des informations détaillées sur les modifications.

## Mises à jour de la version bêta 2 {#beta2-updates}

>[!NOTE]
>
[!BADGE 2.4.7-beta2]{type=Informative url="https://experienceleague.adobe.com/docs/commerce-operations/release/notes/adobe-commerce/2-4-7.html" tooltip="Disponible dans la version 2.4.7-beta2 uniquement"}[notes de mise à jour](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/adobe-commerce/2-4-7.html) pour obtenir des informations détaillées sur les modifications.

## Mise à jour de la version bêta 2 et des correctifs {#beta2-patches-updates}

>[!NOTE]
>
[!BADGE 2.4.6-p3]{type=Informative tooltip="Mises à jour dans 2.4.6-p3"}[!BADGE 2.4.7-beta2]{type=Informative tooltip="Mises à jour dans la version 2.4.7-bêta2"}[2.4.7-beta2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/adobe-commerce/2-4-7.html) et [2.4.6-p3](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p3.html) versions qui apportent des améliorations à la fonctionnalité décrite. Si vous utilisez l’une de ces versions ou celles-ci, consultez les notes de mise à jour.

## Note d&#39;authentification de l&#39;administrateur IMS {#ims-admin-note}

>[!NOTE]
>
Les marchands Adobe Commerce qui disposent d’un Adobe ID et souhaitent une connexion simplifiée à Adobe Commerce et aux produits d’entreprise Adobe peuvent intégrer l’authentification Admin Commerce au workflow d’authentification Adobe IMS. Une fois cette intégration activée pour votre boutique Commerce, chaque utilisateur administrateur doit utiliser ses informations d’identification d’Adobe (et non ses informations d’identification de compte Commerce) pour se connecter. Voir [Présentation de l’intégration d’Adobe Commerce à Adobe IMS](/help/getting-started/adobe-ims-integration-overview.md).

## Note sur les API GTag {#gtag-api-note}

>[!NOTE]
>
À compter de la version 2.4.5, l’intégration des services Google est mise à jour pour prendre en charge l’utilisation des API GTag. GTag est un mécanisme unifié d’intégration à la fonctionnalité Google pour les pages web. Il prend en charge les fonctionnalités et opportunités les plus récentes de suivi et de gestion de contenu par le biais des services Google. Pour plus d’informations, voir [Documentation destinée aux développeurs Google Analytics](https://developers.google.com/analytics/devguides/collection/gtagjs).

## note de saut automatique de réécriture d’URL {#url-rewrite-skip}

>[!NOTE]
>
Lorsque les redirections automatiques sont activées et que vous enregistrez une catégorie, toutes les réécritures de produit et de catégorie sont générées en temps réel et stockées dans les tables de réécriture par défaut. Ce processus pourrait entraîner des problèmes de performances significatifs pour les catégories comportant de nombreux produits attribués. La solution consiste à modifier cette valeur par défaut et à ignorer la génération de réécritures d’URL de catégorie/produits pour l’enregistrement de catégorie. Dans ce cas, les réécritures de produit sont générées uniquement pour l’URL canonique du produit. Voir [Redirections automatiques de produits](/help/merchandising-promotions/url-redirect-product-automatic.md) pour plus d’informations.

## note sur les paramètres de réécriture d’URL {#url-rewrite-params}

>[!IMPORTANT]
>
Dans le processus de redirection, tous les paramètres de GET indiqués dans l&#39;URL sont supprimés pour des raisons de sécurité.

## Nouvelle règle de prix {#new-price-rule}

>[!NOTE]
>
Les règles de prix sont automatiquement traitées avec d’autres règles système. La fréquence de traitement dépend de la [configuration cron](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html). Lorsque vous créez une règle de prix, laissez suffisamment de temps pour qu’elle entre dans le système. Lorsque vous êtes certain qu’il se trouve dans le système, testez la règle.

## Paramètres de configuration {#config}

Pour accéder aux paramètres de configuration du magasin, choisissez **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**de la_ Administration _barre latérale.

## Dépréciation de l’API UPS {#ups-api}

>[!IMPORTANT]
>
À compter de juin 2024, les marchands Adobe Commerce ne pourront plus traiter avec l’intégration UPS actuelle. En effet, les API UPS (United Parcel Service) utilisées par l’intégration native d’Adobe Commerce ne prennent actuellement pas en charge le modèle de sécurité OAuth 2.0 requis. Pour en savoir plus sur ce changement, reportez-vous à la section [_Guide de migration de la clé d’accès à Developer Portal_](https://developer.ups.com/oauth-developer-guide). <br/>
>
Les vendeurs doivent [appliquer une mise à jour de correctif de qualité ;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html) à leur magasin pour migrer de l’API SOAP vers l’API RESTful, qui prend en charge les protocoles d’authentification OAuth 2.0.


## Documentation disponible {#docs-links}

| Ressource de documentation | Description |
|----------------------- | ----------- |
| [Documentation du marché Adobe Commerce 2.4](../landing/home.md) | Documentation axée sur le marché pour Adobe Commerce et Magento Open Source |
| [Documentation des services pour Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) | Documentation pour prendre en charge un ensemble de services qui aident les marchands à intégrer les composants clés de leur entreprise à leur magasin. |
| [Guide de Commerce sur les infrastructures cloud](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | Procédures détaillées pour déployer Adobe Commerce sur une plateforme cloud automatisée et gérée. |
| [Guides opérationnels Adobe Commerce 2.4](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | Documentation système sur les concepts, processus, outils et bonnes pratiques permettant de développer, déployer et gérer des projets déployés sur des plateformes Adobe Commerce et Magento Open Source. |
| [Documentation destinée aux développeurs Adobe Commerce 2.4](https://developer.adobe.com/commerce/docs) | Documentation destinée aux développeurs utilisée pour créer et personnaliser Adobe Commerce ou Magento Open Source |

{style="table-layout:auto"}
