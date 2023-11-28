---
title: Intégration de Adobe Experience Cloud pour l’administrateur Commerce
description: Découvrez l’extension Admin Unified Experience qui intègre Commerce à Experience Cloud afin que les clients puissent accéder aux projets Commerce à partir de la page d’accueil de l’Experience Cloud.
feature: Integration
exl-id: e3fb6337-c7d5-4b6f-8f4a-583697a1f2d2
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# Intégration de Adobe Experience Cloud pour Commerce

{{ee-feature}}

{{$include /help/_includes/admin-unified-experience-beta-note.md}}

Intégrez les projets Adobe Commerce à Experience Cloud en activant l’extension Admin Unified Experience. Lorsque l’intégration est active, les administrateurs peuvent accéder aux projets Commerce à partir de Adobe Experience Cloud.

![Accès à Commerce à partir de la page d’accueil de l’Experience Cloud](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## Affichage des projets Commerce disponibles

Les administrateurs peuvent afficher les projets Commerce auxquels ils sont autorisés à accéder en sélectionnant **[!UICONTROL Commerce]** de la page d’accueil de l’Experience Cloud.

![Espace de travail des projets de commerce sur Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

Les administrateurs peuvent ouvrir l’administrateur et le storefront pour chaque projet à partir de la [!DNL Commerce Projects] workspace et afficher des informations supplémentaires.

- **Instantané de la page d’accueil du storefront Commerce**—Instantané de la page d’accueil du storefront. Si un projet comporte plusieurs sites web, l’instantané affiche la page d’accueil du site par défaut.

- **[Nom du projet](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**: identifie l’environnement de projet cloud de l’instance. Par défaut, le nom du projet correspond à la valeur [Nom de la branche Git](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html) dans le projet cloud. Modifiez ou mettez à jour le nom du projet dans la variable [Paramètres de configuration d’Experience Store unifiés](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin).

- **[URL de storefront](../stores-purchase/store-urls.md)**: affiche l’URL de base du site web par défaut.

- **[Type d’environnement](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**: les instances de commerce déployées dans un environnement de développement ou d’évaluation sont identifiées par un [!UICONTROL Development] ou [!UICONTROL Staging] libellé. Les instances sans libellé sont déployées dans un environnement de production.

- **Accès administrateur de commerce**: ouvrez l’administrateur en cliquant sur **[!UICONTROL Open]**.

- **Accès à Storefront**: ouvrez le storefront en sélectionnant **[!UICONTROL Open storefront]** dans le menu options.

- **Accès rapide à la sélection de projets**—Select **[!UICONTROL Add to Favorites]** dans le menu options pour ajouter un projet à la [!UICONTROL Favorites] .

## Flux d’authentification

Lorsque l’intégration de l’Experience Cloud est activée, les administrateurs utilisent le workflow suivant pour authentifier et accéder aux projets Commerce.

1. Connectez-vous via la page de connexion de l’Experience Cloud.

   ![Page de connexion Experience Cloud](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   Les administrateurs doivent se connecter à l’Experience Cloud avec le profil d’entreprise Adobe pour l’organisation associée à l’instance Commerce. Voir [Gestion des profils d’Adobe](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html).

1. Sur la page d’accueil de l’Experience Cloud, ouvrez le [!UICONTROL Commerce Projects workspace] en sélectionnant **[!UICONTROL Open]**.

1. Accédez à l’administrateur d’un projet en sélectionnant **[!UICONTROL Open]**.

1. Sur la page de connexion d’Adobe Commerce, sélectionnez **[!UICONTROL Sign in with Adobe ID]** pour terminer l’authentification et ouvrir l’administrateur.

   ![Page de connexion Adobe Commerce](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Voir [Gestion de l’intégration des Experience Cloud](admin-unified-experience-integration-manage.md) pour plus d’informations sur l’impact du workflow d’authentification lorsque l’intégration Experience Cloud est activée ou désactivée.

## Conditions

- Adobe Commerce 2.4.5 ou version ultérieure
- Adobe Commerce sur l’infrastructure cloud
- Extensions Adobe Commerce

   - Extension Expérience unifiée de l’administrateur Commerce (`magento/module-unified-experience`)

     Si le module n’est pas disponible sur l’instance Commerce, il peut être installé à l’aide du compositeur.

   - [Service Adobe I/O Events](https://developer.adobe.com/commerce/extensibility/events/): obligatoire pour envoyer des données d’événement afin de gérer l’accès administrateur aux projets Commerce à partir d’un Experience Cloud.

     L’intégration des événements d’Adobe I/O avec Commerce est activée par l’extension Événement de commerce (`magento/commerce-eventing`) qui est disponible avec Adobe Commerce 2.4.4 et versions ultérieures.

## Activation de l’intégration

Activez l’intégration en suivant les instructions pour [Configuration de l’intégration Experience Cloud avec l’administrateur Commerce](admin-unified-experience-integration-configure.md).

>[!TIP]
>
>Si l’intégration de l’Experience Cloud est déjà activée sur l’instance Commerce, voir [Gestion de l’intégration des Experience Cloud](admin-unified-experience-integration-manage.md) pour plus d’informations sur la modification ou la mise à jour de la configuration, la gestion de l’accès administrateur et la résolution des problèmes.
