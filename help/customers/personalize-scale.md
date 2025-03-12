---
title: Créez des expériences attrayantes et personnalisées à grande échelle
description: Découvrez les fonctionnalités d’Adobe  [!DNL Commerce]  vous permettent de créer une expérience personnalisée pour vos clientes et clients.
feature: Customers, Storefront, Personalization
exl-id: 9546e1b8-796b-4694-8396-773a2b0e9c12
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '1808'
ht-degree: 0%

---

# Créez des expériences attrayantes et personnalisées à grande échelle

Adobe [!DNL Commerce] vous offre une boîte à outils puissante pour personnaliser chaque point de contact client, ce qui dynamise l’engagement, la conversion et le chiffre d’affaires des acheteurs.

Dans cet article, vous apprendrez :

- Qu’est-ce que la personnalisation ?
- De quelles données ai-je besoin pour effectuer la personnalisation ?
- Comment Adobe [!DNL Commerce] déverrouille-t-il la personnalisation ?
- Cas d’utilisation de la personnalisation disponibles

## Qu’est-ce que la personnalisation ?

Personalization signifie personnaliser les aspects de l’expérience d’achat de chaque client pour répondre à ses besoins, son contexte et ses préférences uniques. Personalization ne se limite pas au contenu du site ou à la recommandation de produits adaptés, mais englobe tous les points de contact du parcours client, notamment :

- **Campagnes et communications** - Diffuser des messages pertinents et cohérents via des campagnes et des communications
- **Découverte de produits** - Présenter les bons produits aux bons clients au bon moment
- **Promotions et offres** - Ciblez les promotions et les offres pour inciter chaque client à convertir son contenu
- **Expériences de contenu** - Adaptation du contenu du site pour qu’il semble extrêmement pertinent pour chaque client et son parcours

![ Types de Personalization ](assets/types-personalization.png){width="700" zoomable="yes"}

Bien que ces types d’expériences personnalisées puissent sembler réalisables pour un petit sous-ensemble de clients et clientes, la personnalisation à l’échelle pour des milliers ou des millions de clients et clientes sur chaque point de contact et canal, le tout en temps réel peut sembler impossible. Dans les sections suivantes, vous découvrirez comment Adobe [!DNL Commerce] et Adobe Experience Cloud peuvent vous aider.

## De quelles données ai-je besoin pour effectuer la personnalisation ?

Une personnalisation efficace nécessite un contexte ou des signaux qui fournissent des informations sur les clients qui peuvent ensuite être utilisées pour modifier leur expérience. Le tableau suivant présente les différents types de données et le rôle que joue Adobe [!DNL Commerce] dans la prise en charge de la collecte et de l’activation de ces données.

| Types de données | Données Storefront (Événements Comportementaux) | Données de back-office (événements côté serveur) | Profil client et données de segment |
|---|---|---|---|
| **Définition** | Clics ou actions des clients sur votre site. | Informations sur le cycle de vie et détails de chaque commande (passée et actuelle). | Qui sont vos acheteurs et pour quels segments se qualifient-ils ? |
| **Événements capturés par Adobe Commerce** | [pageView](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#pageview)<br>[productPageView](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events)<br>[searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#searchrequestsent)<br>[searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#searchresponsereceived)<br>[addToCart](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#addtocart)<br>[openCart](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#opencart)<br>[signIn](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#signin)<br>[signOut](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#signout)<br>[startCheckout](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#startcheckout)<br>[completeCheckout](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#completecheckout)<br>[createRequisitionList](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#createrequisitionlist)<br>[addToRequisitionList](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#addtorequisitionlist)<br>[removeFromRequisitionList](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#removefromrequisitionlist) | **Statut de la commande**:<br>[orderPlaced](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#orderplaced)<br>[orderItemsReturnInitiated](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#orderitemsreturnedinitiated)<br>[orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#orderitemsshipped)<br>[orderCancelled](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#ordercancelled)<br>[**Order history**](https://experienceleague.adobe.com/en/docs/commerce/data-connection/fundamentals/connect-data#send-historical-order-data):<br>- SKU, Nom, Quantité de prix, Remise<br>- Catégorie de produits<br>- Montant du paiement, Type, Devise<br>- Mode d&#39;expédition et Montant<br>- ID de remboursement, Montant, Devise<br>- Motif de retour, Condition, Résolution<br>- Adresse<br>- E-mail | [**Enregistrement de profil**](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-profilerecord) : (nom, genre, adresse, statut de fidélité, numéro de téléphone, adresse électronique)<br>**statut du compte**:<br>[accountCreated](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#accountcreated)<br>[accountUpdated](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#accountupdated)<br>[accountDeleted](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice#accountdeleted) |

Grâce à toutes ces données [!DNL Commerce] propriétaires riches, vous êtes prêt à cibler et à personnaliser l’expérience de chaque acheteur. Dans la section suivante, découvrez comment [!DNL Commerce] et Adobe Experience Cloud vous aident à créer des expériences personnalisées et des cas d’utilisation que vous pouvez activer.

## Comment Adobe [!DNL Commerce] renforce-t-il la personnalisation ?

Le partage de données [!DNL Commerce] d’Adobe vous permet de collecter et de partager les types de données du tableau précédent avec d’autres produits Adobe Experience Cloud afin d’alimenter des profils client et des audiences unifiés, des campagnes personnalisées ainsi que des analyses et des informations complètes.

![Flux de données vers Experience Platform Edge](assets/commerce-edge.png){width="700" zoomable="yes"}

Le partage de données [!DNL Commerce] d’Adobe comprend deux composants clés :

1. [Connexion aux données](https://experienceleague.adobe.com/en/docs/commerce/data-connection/overview) : partagez les données de storefront, de back-office et de profil client d’Adobe [!DNL Commerce] vers le réseau Edge de Adobe Experience Platform pour les utiliser dans les applications Adobe Experience Cloud, notamment :

   - [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview) : regroupez les données client provenant de plusieurs sources (ERP, CRM, POS) en profils unifiés et créez des segments basés sur des règles ou sur l’IA.
   - [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started) : lancez des parcours omnicanal personnalisés, y compris des campagnes par e-mail, des SMS, des notifications push, etc.
   - [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) et [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview) : obtenez des informations sur le client et l’entreprise.
   - [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro) : testez et optimisez le contenu, les produits recommandés, les offres, la navigation, etc.

1. [[!DNL Audience Activation]](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) : utilisez les audiences [!DNL Real-Time CDP] pour personnaliser les blocs de contenu dynamique, les promotions et les règles de produit associées sur votre site [!DNL Commerce] Adobe.

### Expériences de storefront personnalisées sur n’importe quel canal, à grande échelle

Adobe [!DNL Commerce] peut tirer parti d’une vitrine haute performance, appelée [Edge Delivery Services](https://experienceleague.adobe.com/developer/commerce/storefront/), pour offrir des expériences personnalisées sur tous vos canaux, avec les fonctionnalités d’IA au cœur, et la vitesse comme base.

Avec Edge Delivery Services, vous pouvez :

- **Créer du contenu personnalisé** : utilisez la création basée sur des documents, l’expérimentation native avec des variations de texte et d’image de l’IA générative pour personnaliser l’expérience à grande échelle. Utilisez la création de contenu Assets et Generative AI pour produire des images de produit et de marketing à grande échelle.

- **Générer des variations** : permet aux auteurs de contenu d’utiliser l’IA générative pour créer d’importants volumes de [variations de contenu et d’image](https://experienceleague.adobe.com/en/docs/experience-manager-learn/sites/generative-ai/generate-variations) personnalisés et pilotés par l’IA avec Adobe Firefly.

- **Déploiement via le storefront Edge Delivery Services** : contenu sur les fonctionnalités Edge et Commerce optimisé par des composants déroulants, pour créer des expériences d’achat personnalisées pour vos audiences.

- **Commerce et Adobe Experience Manager Assets** : création et variations de ressources de produit Generative AI à grande échelle. Créez, diffusez et surveillez la diffusion de contenu sur n’importe quel canal.

![Pages déroulantes : Détails du produit](assets/drop-in.png){width="700" zoomable="yes"}

### Personalization prêt à l’emploi : prise en main des fonctionnalités natives d’Adobe [!DNL Commerce]

Adobe [!DNL Commerce] offre une personnalisation puissante avec ses fonctionnalités natives prêtes à l’emploi. Le tableau suivant décrit [!DNL Commerce] fonctionnalités que vous pouvez activer immédiatement pour commencer à utiliser votre parcours de personnalisation.

| Catégorie | Fonctionnalités |
|---|---|
| Découverte de produits personnalisée | [[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview) : personnalisez et optimisez les résultats de recherche en fonction des actions comportementales et des affinités sur site d’un acheteur avec la recherche optimisée par l’IA.<br>[Marchandisage intelligent de catégorie](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-admin/category-merch) : classement de produits piloté par l’IA sur les pages de catégorie en fonction des actions comportementales et des affinités sur site d’un acheteur.<br>[Recommandations de produits](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview) : recommandations de produits optimisées par l’IA basées sur le comportement, les tendances et les affinités de l’acheteur.<br>[Règles de produits associés](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) : définissez des règles personnalisées pour afficher les produits de votre catalogue afin de stimuler les ventes croisées et les ventes incitatives. |
| Contenu de site personnalisé | [Blocs de contenu dynamique](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) : affichez des blocs de contenu personnalisés, par exemple des bannières, en fonction des segments de clientèle dans Adobe Commerce. |
| Offres et promotions personnalisées | [Règles de prix du panier](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart) : appliquez des remises aux articles du panier en fonction d’un ensemble de conditions, y compris les segments de clients dans Adobe [!DNL Commerce]. |
| Informations et mesure | [Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) : découvrez comment fonctionnent vos stratégies de personnalisation et comment elles s’améliorent au fil du temps. |

## Principaux cas d’utilisation de la personnalisation

Les clients Adobe [!DNL Commerce] utilisent des fonctionnalités prêtes à l’emploi et partagent des données avec Adobe Experience Cloud pour divers cas d’utilisation. Les sections suivantes mettent en évidence les principaux cas d’utilisation et décrivent leur implémentation à l’aide des applications Adobe [!DNL Commerce] uniquement ou [!DNL Commerce] plus Experience Cloud.

### Campagnes et communications personnalisées

| Cas D’Utilisation | Solution |
|---|---|
| **Panier et navigation abandonnés** - Envoyez un e-mail ou une notification de réengagement personnalisé lorsqu’un client abandonne son panier ou sa session de navigation après avoir démontré un engagement élevé | **Adobe [!DNL Commerce] uniquement**:<br>[Rappels par e-mail](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules)<br>**Adobe [!DNL Commerce] avec Adobe Journey Optimizer**:<br>[!DNL Commerce] les données servent de déclencheur pour un parcours d’abandon omnicanal. Personnalisez ce parcours en fonction des attributs du client, de ce qu’il a abandonné, d’autres comportements d’achat et des achats précédents.<br>Commerce avec Adobe Journey Optimizer et Real-Time CDP : personnalisez les campagnes d’abandon en fonction des profils client unifiés et des audiences gérées de manière centralisée, par exemple en créant une audience à taux d’abandon élevé. |
| **Création d’audience centralisée** - Créez des audiences basées sur des règles ou sur l’IA en fonction du comportement sur site, des achats précédents, des attributs de profil, des affinités de catégorie, du statut de fidélité, de la valeur du client, etc | **Adobe [!DNL Commerce] uniquement**:<br>Collectez des informations sur le profil client lorsque [!DNL Commerce] clients créent des comptes. Créez des [segments de clients](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/segments/customer-segments) et des groupes de clients basés sur des règles pour personnaliser le contenu et les promotions.<br>**[!DNL Commerce] Adobe avec Adobe Real-Time CDP**:<br> [Profils unifiés](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home) issus de l’ensemble des sources de données et des canaux ; audiences basées sur des règles ou optimisées par l’IA. |
| **Offre personnalisée par e-mail/SMS basée sur le comportement de l’acheteur** - Envoyez des offres personnalisées aux clients par e-mail ciblé en fonction de leurs achats précédents et de leur comportement d’acheteur, par exemple, envoyez une offre pour des produits ou des catégories que les clients ont consultés ou avec lesquels ils ont interagi. | **Adobe [!DNL Commerce] uniquement**:<br>Exporter des données à utiliser avec les solutions d’automatisation du marketing.<br>**Les [!DNL Commerce] Adobe avec Adobe Journey Optimizer et Real-Time CDP**:<br>[!DNL Commerce] servent de déclencheur pour les offres par e-mail ou SMS et fournissent des signaux (comportements d’acheteur) sur lesquels effectuer une personnalisation. Real-Time CDP n’est pas obligatoire, mais en règle générale, ces offres et campagnes sont créées autour des audiences, qui sont créées et gérées dans Real-Time CDP. |
| **Produits/marques compatibles avec les ventes croisées ou les ventes incitatives** - Si un client achète un produit ou une marque compatible ou indique une forte affinité pour un autre produit ou une autre marque, envoyez une campagne (e-mail/SMS) pour stimuler la conversion des ventes croisées. | **Adobe [!DNL Commerce] uniquement**:<br>Utilisez Adobe [!DNL Commerce] [Recommandations de produits](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview) pour recommander des produits spécifiques sur le site. Vous pouvez également utiliser [Règles de produits associés](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) pour suggérer d&#39;autres produits.<br>**[!DNL Commerce] avec [!DNL Target]**:<br>Adobe [!DNL Target] dispose également d’un moteur de recommandation de produit intégré doté de puissantes fonctionnalités telles que l’affinité catégorielle. Vous pouvez l’utiliser pour des ventes croisées ou des ventes incitatives.<br>**[!DNL Commerce] avec Adobe Journey Optimizer**:<br>utilisez [!DNL Target] ou [!DNL Commerce] pour déterminer les produits à recommander, puis diffusez via Adobe Journey Optimizer. |

### Expériences de site personnalisées

| Cas D’Utilisation | Solution |
|---|---|
| **Contenu de site personnalisé** - Personnalisez les bannières de site et d’autres contenus de page en fonction des actions de l’acheteur, telles que la navigation dans les produits et les affinités entre les catégories. Déployez le contenu le mieux adapté en fonction des résultats des tests A/B ou des objectifs commerciaux. | **Adobe [!DNL Commerce] uniquement**:<br>Déployer des [blocs de contenu dynamique](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) spécifiques au segment.<br>**[!DNL Commerce] avec Real-Time CDP **:<br>Utilisez [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) pour déployer des blocs de contenu dynamique spécifiques à une audience qui répondent aux actions en temps réel et aux données de profil client unifiées, tout en gérant de manière centralisée les profils et les audiences dans Real-Time CDP.<br>**[!DNL Commerce] avec[!DNL Target]**:<br>personnalisez chaque partie de l’expérience du site, y compris le contenu, les éléments de navigation, les dispositions de pages complètes, etc. à l’aide des données de [!DNL Commerce] Adobe dans Adobe [!DNL Target]. Contenu du test A/B, sélectionner et déployer automatiquement le contenu gagnant pour chaque client.<br>**[!DNL Commerce] avec AEM Assets **:<br>Stockez tout votre contenu dans Adobe Experience Manager Assets. Accédez à ce contenu de manière native à partir d’Adobe Commerce. Utilisez l’IA générative pour créer des variations de contenu à personnaliser en fonction des différents segments ou audiences. |
| **Offre personnalisée sur site en fonction du comportement** - Personnalisez les promotions en fonction des actions de l’acheteur, telles que la navigation dans les produits et les affinités entre les catégories. Déployez la meilleure offre suivante en fonction des résultats des tests A/B ou des objectifs commerciaux. | **Adobe [!DNL Commerce] uniquement**:<br>Déployez un catalogue spécifique au segment et [règles de prix de panier](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart).<br>**Adobe [!DNL Commerce] avec Real-Time CDP**:<br>Utilisez [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) pour déployer des offres spécifiques à une audience, tout en gérant de manière centralisée les profils/audiences dans Real-Time CDP.<br>**Commerce avec[!DNL Target]** : utilisez Offer Decisioning pour déterminer l’offre à déployer, effectuer des tests A/B ou définir des objectifs commerciaux pour guider les offres déployées dans Adobe Commerce. |

### Analytics et insights

| Cas D’Utilisation | Solution |
|---|---|
| **Comportement des clients par canal** - Comprenez les nuances de la façon dont les clients s’engagent dans chaque canal (web, en personne, application, autre) pour affecter les stratégies marketing pour chaque canal. Comprenez l’entonnoir d’achat et les faiblesses de l’expérience client. | **Adobe [!DNL Commerce] uniquement** :<br>[Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) fournit des analyses enrichies sur le canal de [!DNL Commerce] numérique, mais pas sur plusieurs canaux ni sur des éléments plus larges du parcours client.<br>**[!DNL Commerce] d’Adobe avec Customer Journey Analytics**:<br>[!DNL Commerce] les tableaux de bord de données des flux de données pour obtenir des détails complets sur toutes les étapes de l’expérience client (sur l’ensemble des canaux). Comprenez tous les points de contact et l’entonnoir plus large afin d’identifier les points faibles du parcours client susceptibles d’entraîner une baisse de la clientèle. |
| **Tendances d’achat** - Comprenez les comportements d’achat sur une période spécifique (par exemple, analyse du panier d’achat, analyse des produits) pour identifier les tendances, le caractère saisonnier et optimiser le marketing en fonction des modèles d’achat historiques. | **Adobe [!DNL Commerce] uniquement** :<br>[Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) fournit des analyses enrichies sur le canal de [!DNL Commerce] numérique, mais pas sur plusieurs canaux ni sur des éléments plus larges du parcours client.<br>**[!DNL Commerce] d’Adobe avec Customer Journey Analytics**:<br>[!DNL Commerce] les tableaux de bord de données des flux de données pour obtenir des détails complets sur toutes les étapes de l’expérience client (sur l’ensemble des canaux). Comprenez tous les points de contact et l’entonnoir plus large afin d’identifier les points faibles du parcours client susceptibles d’entraîner une baisse de la clientèle. |

## Exemples De Cas D’Utilisation

- Découvrez comment utiliser Adobe Journey Optimizer pour [envoyer un email de panier abandonné](https://experienceleague.adobe.com/en/docs/commerce/data-connection/use-cases/using-ajo).
- Découvrez comment [créer une audience dans Real-Time CDP](https://experienceleague.adobe.com/en/docs/commerce/data-connection/use-cases/create-audience) pour informer une règle de prix de panier dans Adobe [!DNL Commerce].
