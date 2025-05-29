---
title: Administrateur d’intégration de Adobe Experience Cloud pour Commerce
description: Découvrez l’extension Expérience unifiée d’administration qui intègre Commerce à Experience Cloud afin que les clients puissent accéder aux projets Commerce à partir de la page d’accueil d’Experience Cloud.
feature: Integration
exl-id: e3fb6337-c7d5-4b6f-8f4a-583697a1f2d2
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 77e7eb00e9f8d5af6361059c287707993180c4c4
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---

# Intégration de Adobe Experience Cloud pour Commerce

<table style="border:1px solid red">
<tr><td><img alt="Fonctionnalité Adobe Commerce" src="../assets/adobe-logo.svg" width="20" height="20" /> Fonctionnalité exclusive uniquement dans Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">En savoir plus</a>)</td></tr>
</table>

Intégrez des projets Adobe Commerce à Experience Cloud en activant l’extension Expérience unifiée d’administration . Lorsque l’intégration est active, les administrateurs peuvent accéder aux projets Commerce à partir de Adobe Experience Cloud.

![Accédez à Commerce à partir de la page d’accueil d’Experience Cloud](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## Afficher les projets Commerce disponibles

Les administrateurs peuvent afficher les projets Commerce auxquels ils ont accès en sélectionnant **[!UICONTROL Commerce]** sur la page d’accueil d’Experience Cloud.

Espace de travail ![Projets Commerce sur Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

Les administrateurs peuvent ouvrir l’administrateur et le storefront pour chaque projet à partir de l’espace de travail [!DNL Commerce Projects] et afficher des informations supplémentaires.

- **Instantané de la page d’accueil du storefront de Commerce** : instantané de la page d’accueil du storefront. Si un projet comporte plusieurs sites web, l’instantané affiche la page d’accueil du site par défaut.

- **[Nom du projet](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)** : identifie l&#39;environnement de projet cloud pour l&#39;instance. Le nom du projet par défaut est le [nom de la branche Git](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html) dans le projet cloud. Modifiez ou mettez à jour le nom du projet dans les [Paramètres de configuration du magasin d’expériences unifiées](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin).

- **[URL du storefront](../stores-purchase/store-urls.md)** : affiche l&#39;URL de base du site Web par défaut.

- **[Type d’environnement](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)** : les instances Commerce déployées dans un environnement de développement ou d’évaluation sont identifiées par un libellé [!UICONTROL Development] ou [!UICONTROL Staging]. Les instances qui n’ont pas de libellé sont déployées dans un environnement de production.

- **Accès administrateur Commerce**—Ouvrez l&#39;administrateur en cliquant sur **[!UICONTROL Open]**.

- **Accès au storefront** : ouvrez le storefront en sélectionnant **[!UICONTROL Open storefront]** dans le menu d&#39;options.

- **Accès rapide pour sélectionner des projets**—Sélectionnez **[!UICONTROL Add to Favorites]** dans le menu d&#39;options pour ajouter un projet à l&#39;onglet [!UICONTROL Favorites].

## Flux d’authentification

Lorsque l’intégration d’Experience Cloud est activée, les administrateurs utilisent le workflow suivant pour authentifier les projets Commerce et y accéder.

1. Connectez-vous via la page de connexion d’Experience Cloud.

   ![Page de connexion à Experience Cloud](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   Les administrateurs doivent se connecter à Experience Cloud avec le profil professionnel Adobe de l’organisation associée à l’instance Commerce. Voir [Gestion des profils Adobe](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html).

1. Sur la page d’accueil d’Experience Cloud, ouvrez le [!UICONTROL Commerce Projects workspace] en sélectionnant **[!UICONTROL Open]**.

1. Accédez à l’administration d’un projet en sélectionnant **[!UICONTROL Open]**.

1. Sur la page de connexion d’Adobe Commerce, sélectionnez **[!UICONTROL Sign in with Adobe ID]** pour terminer l’authentification et ouvrez l’interface d’administration.

   ![Page de connexion à Adobe Commerce](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Consultez [Gérer l’intégration d’Experience Cloud](admin-unified-experience-integration-manage.md) pour plus d’informations sur la manière dont le workflow d’authentification est affecté lorsque l’intégration d’Experience Cloud est activée ou désactivée.

## Conditions requises

- Adobe Commerce 2.4.5 ou version ultérieure
- Adobe Commerce sur les infrastructures cloud
- Extensions d’Adobe Commerce

   - Extension Commerce Admin Unified Experience (`magento/module-unified-experience`)

     Si le module n’est pas disponible sur l’instance Commerce, il peut être installé à l’aide du compositeur.

   - [Service Adobe I/O Events ](https://developer.adobe.com/commerce/extensibility/events/) : requis pour envoyer des données d’événement afin de gérer l’accès administrateur aux projets Commerce à partir d’Experience Cloud.

     L’intégration de Adobe I/O Events à Commerce est activée par l’extension d’événement Commerce (`magento/commerce-eventing`), disponible avec Adobe Commerce 2.4.4 et les versions ultérieures.

## Activation de l’intégration

Activez l’intégration en suivant les instructions [Configuration de l’intégration d’Experience Cloud avec Commerce Admin](admin-unified-experience-integration-configure.md).

>[!TIP]
>
>Si l’intégration Experience Cloud est déjà activée sur l’instance Commerce, consultez [Gérer l’intégration Experience Cloud](admin-unified-experience-integration-manage.md) pour plus d’informations sur la modification ou la mise à jour de la configuration, la gestion de l’accès administrateur et le dépannage.
