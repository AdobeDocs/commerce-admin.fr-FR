---
title: Conditions préalables à la découverte de produits par l’IA
description: Examinez les exigences relatives à l’enrichissement du catalogue et à l’enrichissement PDP, puis installez l’extension d’enrichissement partagé sur Adobe Commerce sur l’infrastructure cloud ou sur site.
role: Admin, Developer
source-git-commit: 591fca4f18862d289fb233997e8848cb4692d1e7
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%
---
# Conditions préalables

Avant d’utiliser l’enrichissement du catalogue ou l’enrichissement PDP, confirmez les exigences qui s’appliquent à chaque déploiement, puis effectuez la configuration de votre plateforme Commerce.

## Conditions requises pour tous les déploiements {#all-deployments}

| Exigence | Application | Détails |
| --- | --- | --- |
| Optimiser dans Edge | enrichissement PDP | Obligatoire. Optimiser sur Edge diffuse les données de produit enrichies aux agents d’IA. Voir le guide [Optimiser sur Edge](https://experienceleague.adobe.com/en/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn). |
| Transfert de journal | Les deux workflows | Facultatif. Active les recommandations d’enrichissement en fonction du trafic d’agent. Sans cela, vous pouvez toujours sélectionner manuellement des produits ou des pages de produits. Voir le [Guide de transfert du journal](https://experienceleague.adobe.com/en/docs/brand-visibility/using/log-forwarding/log-forwarding-overview). |
| Storefront pouvant être analysé | Enrichissement du catalogue | Obligatoire pour les recommandations basées sur les explores. Les robots orientés LLM et les robots d’agence doivent pouvoir accéder à vos pages de produits. |
| Accès à [!DNL Adobe Admin Console] | Les deux workflows | Obligatoire. Pendant la configuration, [!DNL Adobe Commerce] vérifie le statut de l’utilisateur GenAI de votre organisation. Vous avez accès à moins que votre organisation n’ait choisi de se désinscrire du client GenAI. |

<!--
TBD (SME): The Optimize at Edge guide is a Brand Visibility reference, not a Commerce setup guide. Add Commerce-specific Optimize at Edge setup instructions (this might be automated by GA).
-->

## Configuration de la plateforme Commerce {#set-up}

>[!BEGINTABS]

>[!TAB Commerce sur les infrastructures cloud ou sur site]

Pour [!DNL Adobe Commerce] sur l’infrastructure cloud ou sur site, vous installez l’extension d’enrichissement partagée, qui permet l’enrichissement du catalogue et l’enrichissement PDP.

**Avant de commencer :**

- [!DNL Adobe Commerce] 2.4.7 ou version ultérieure sur PHP 8.3 ou version ultérieure. Voir les [notes de mise à jour](release-notes.md).
- Une organisation [!DNL Adobe IMS]. Si votre organisation n’en a pas, consultez la [présentation de l’intégration d’Adobe IMS](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview). L’enrichissement du catalogue utilise le jeton d’accès IMS de l’utilisateur administrateur connecté. Le fait de se connecter uniquement avec un nom d’utilisateur et un mot de passe Commerce ne fournit pas ce jeton.
- Accès en ligne de commande au serveur d’applications Commerce et autorisation de télécharger des packages depuis `repo.magento.com`.

**Installer et vérifier :**

1. Si ni [!DNL Live Search] ni [!DNL Product Recommendations] ne sont activés, ajoutez [!DNL Catalog Service] à partir de votre répertoire de projet Commerce :

   ```bash
   composer require magento/catalog-service --no-update
   composer update magento/catalog-service
   ```

   [!DNL Catalog Service] est installé automatiquement avec [!DNL Live Search] et [!DNL Product Recommendations]. Par conséquent, ignorez cette étape si l’un des services est activé.

1. S’il n’est pas déjà configuré pour un autre service Commerce, configurez le [connecteur de services Commerce](https://experienceleague.adobe.com/en/docs/commerce/user-guides/integration-services/saas) avec des clés d’API et un espace de données SaaS.

1. Ajoutez l’extension d’enrichissement partagée :

   ```bash
   composer require magento/module-catalog-enrichment --no-update
   composer update magento/module-catalog-enrichment
   ```

1. Déployez les modifications :

   - **Infrastructure cloud :** validez et transmettez les modifications à `composer.json` et `composer.lock`.
   - **Sur site :** Mettez à niveau l&#39;application et effacez le cache :

     ```bash
     bin/magento setup:upgrade
     bin/magento cache:clean
     ```

1. Dans l’administration, accédez à **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Feed Sync Status]** et confirmez que Commerce exporte les données du catalogue.

   Le nombre d’enregistrements de produit envoyés avec succès doit correspondre aux enregistrements source, sans échec ni envoi en attente. Pour les enregistrements ayant échoué, consultez les détails de l’erreur, résolvez le problème et planifiez une resynchronisation pour les enregistrements concernés.

1. Accédez à **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Management Dashboard]** et confirmez que les données de catalogue attendues sont disponibles dans [!DNL Catalog Service].

Pour plus d’informations sur le statut et la résolution des problèmes, consultez [Surveillance du statut des flux de données](/help/systems/data-feed-sync-status.md#monitor-data-feed-status).

>[!TAB Adobe Commerce as a Cloud Service]

Pour [!DNL Adobe Commerce as a Cloud Service], l’installation de [!DNL Catalog Service], l’enrichissement du catalogue et l’enrichissement PDP sont gérés pour vous pendant l’approvisionnement du compte.

Remplissez les [conditions requises pour tous les déploiements](#all-deployments) qui s’appliquent aux workflows que vous prévoyez d’utiliser.

<!-- TBD (SME): Confirm whether merchants on Adobe Commerce as a Cloud Service should verify catalog data on the Data Management Dashboard, and whether the IMS and Admin Console requirements apply. -->

>[!ENDTABS]

## Étape suivante {#next-step}

[Configurez les paramètres d’enrichissement](settings.md) pour connecter votre instance Commerce à la découverte de produit AI.
