---
title: Intégration de Adobe Experience Cloud pour l’administrateur Commerce
description: Découvrez l’extension Admin Experience unifiée qui intègre Commerce à Experience Cloud afin que les clients puissent accéder aux projets Commerce à partir de la page d’accueil de l’Experience Cloud.
feature: Integration
exl-id: e3fb6337-c7d5-4b6f-8f4a-583697a1f2d2
source-git-commit: 61874f3dac4f574ad393e8ae258f3d6c56c8f37e
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Intégration Adobe Experience Cloud pour Commerce

<table style="border:1px solid red">
<tr><td><img alt="Fonctionnalité Adobe Commerce" src="../assets/adobe-logo.svg" width="20" height="20" /> Fonctionnalité exclusive uniquement dans Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=fr#product-editions">En savoir plus</a>)</td></tr>
</table>

Intégrez les projets Adobe Commerce à Experience Cloud en activant l’extension Admin Unified Experience. Lorsque l’intégration est active, les administrateurs peuvent accéder aux projets Commerce à partir de Adobe Experience Cloud.

![Accéder à Commerce à partir de la page d’accueil de l’Experience Cloud](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## Affichage des projets Commerce disponibles

Les administrateurs peuvent afficher les projets Commerce auxquels ils sont autorisés à accéder en sélectionnant **[!UICONTROL Commerce]** sur la page d’accueil de l’Experience Cloud.

![Espace de travail Projets Commerce sur l’Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

Les administrateurs peuvent ouvrir l’administrateur et le storefront pour chaque projet à partir de l’espace de travail [!DNL Commerce Projects] et afficher des informations supplémentaires.

- **Instantané de la page d’accueil du storefront Commerce** : instantané de la page d’accueil du storefront. Si un projet comporte plusieurs sites web, l’instantané affiche la page d’accueil du site par défaut.

- **[Nom du projet](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html?lang=fr)** : identifie l’environnement du projet cloud pour l’instance. Le nom du projet est par défaut le [nom de la branche Git](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html?lang=fr) dans le projet cloud. Modifiez ou mettez à jour le nom du projet dans les [paramètres de configuration du magasin d’expériences unifiées](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin).

- **[URL Storefront](../stores-purchase/store-urls.md)** : affiche l’URL de base du site web par défaut.

- **[Type d’environnement](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html?lang=fr)** : les instances Commerce déployées dans un environnement de développement ou d’évaluation sont identifiées avec une étiquette [!UICONTROL Development] ou [!UICONTROL Staging]. Les instances sans libellé sont déployées dans un environnement de production.

- **Accès administrateur Commerce** : ouvrez l’administrateur en cliquant sur **[!UICONTROL Open]**.

- **Accès au storefront** : ouvrez le storefront en sélectionnant **[!UICONTROL Open storefront]** dans le menu d’options.

- **Accès rapide à la sélection de projets** : sélectionnez **[!UICONTROL Add to Favorites]** dans le menu d’options pour ajouter un projet à l’onglet [!UICONTROL Favorites].

## Flux d’authentification

Lorsque l’intégration de l’Experience Cloud est activée, les administrateurs utilisent le workflow suivant pour authentifier et accéder aux projets Commerce.

1. Connectez-vous via la page de connexion de l’Experience Cloud.

   ![Page de connexion Experience Cloud](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   Les administrateurs doivent se connecter à l’Experience Cloud avec le profil d’entreprise Adobe pour l’organisation associée à l’instance Commerce. Voir [Gestion des profils d’Adobe](https://helpx.adobe.com/fr/enterprise/using/manage-adobe-profiles.html).

1. Sur la page d’accueil de l’Experience Cloud, ouvrez le [!UICONTROL Commerce Projects workspace] en sélectionnant **[!UICONTROL Open]**.

1. Accédez à l’administrateur d’un projet en sélectionnant **[!UICONTROL Open]**.

1. Sur la page de connexion d’Adobe Commerce, sélectionnez **[!UICONTROL Sign in with Adobe ID]** pour terminer l’authentification et ouvrez l’administrateur.

   ![Page de connexion Adobe Commerce](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Voir [Gestion de l’intégration d’Experience Cloud](admin-unified-experience-integration-manage.md) pour plus d’informations sur l’impact du processus d’authentification lorsque l’intégration d’Experience Cloud est activée ou désactivée.

## Conditions

- Adobe Commerce 2.4.5 ou version ultérieure
- Adobe Commerce sur l’infrastructure cloud
- Extensions Adobe Commerce

   - Extension Commerce Admin Unified Experience (`magento/module-unified-experience`)

     Si le module n’est pas disponible sur l’instance Commerce, il peut être installé à l’aide du compositeur d’expérience.

   - [ Service d’événements d’Adobe I/O ](https://developer.adobe.com/commerce/extensibility/events/) : requis pour envoyer des données d’événement afin de gérer l’accès administrateur aux projets Commerce à partir de l’Experience Cloud.

     L’intégration des événements d’Adobe I/O avec Commerce est activée par l’extension d’événement Commerce (`magento/commerce-eventing`) disponible avec Adobe Commerce 2.4.4 et versions ultérieures.

## Activation de l’intégration

Activez l’intégration en suivant les instructions pour [Configurer l’intégration Experience Cloud avec l’administrateur Commerce](admin-unified-experience-integration-configure.md).

>[!TIP]
>
>Si l’intégration de l’Experience Cloud est déjà activée sur l’instance Commerce, voir [Gestion de l’intégration de l’Experience Cloud](admin-unified-experience-integration-manage.md) pour plus d’informations sur la modification ou la mise à jour de la configuration, la gestion de l’accès administrateur et la résolution des problèmes.
