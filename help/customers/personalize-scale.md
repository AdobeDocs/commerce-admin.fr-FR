---
title: Créer des expériences personnalisées et attrayantes à l’échelle
description: Découvrez les fonctionnalités d’Adobe [!DNL Commerce] qui vous permettent de créer une expérience personnalisée pour vos acheteurs.
feature: Customers, Storefront, Personalization
exl-id: 9546e1b8-796b-4694-8396-773a2b0e9c12
source-git-commit: 728a1fdb413009a00377cd8205dde93cd4feadc8
workflow-type: tm+mt
source-wordcount: '1808'
ht-degree: 0%

---

# Créer des expériences personnalisées et attrayantes à l’échelle

Adobe [!DNL Commerce] offre une boîte à outils puissante pour personnaliser chaque point de contact client, ce qui stimule l’engagement des acheteurs, la conversion et les recettes.

Dans cet article, vous apprenez :

- Qu’est-ce que la personnalisation ?
- De quelles données ai-je besoin pour obtenir une personnalisation ?
- Comment l&#39;Adobe [!DNL Commerce] déverrouille-t-il la personnalisation ?
- Cas d’utilisation de la personnalisation disponibles

## Qu’est-ce que la personnalisation ?

Personalization consiste à personnaliser les aspects de l’expérience d’achat de chaque client en fonction de ses besoins, de son contexte et de ses préférences. Personalization ne se limite pas au contenu du site ou à la recommandation de produits adaptés, mais englobe tous les points de contact du parcours client, notamment :

- **Campagnes et communications** - Diffuser des messages pertinents et cohérents par le biais de campagnes et de communications
- **Découverte de produit** - Affichage des produits appropriés aux bons clients aux bons moments
- **Promotions et offres** - Ciblage des promotions et des offres pour pousser chaque client à convertir
- **Expériences de contenu** - Personnaliser le contenu du site pour qu’il se sente hyper-pertinent pour chaque client et son parcours

![Types de Personalization](assets/types-personalization.png){width="700" zoomable="yes"}

Bien que ces types d’expériences personnalisées puissent sembler réalisables pour un petit sous-ensemble de clients, personnalisation à grande échelle pour des milliers ou des millions de clients sur chaque point de contact et canal, le tout en temps réel peut se révéler impossible. Dans les sections suivantes, vous découvrirez comment Adobe [!DNL Commerce] et Adobe Experience Cloud peuvent vous aider.

## De quelles données ai-je besoin pour obtenir une personnalisation ?

Une personnalisation efficace nécessite un contexte ou des signaux qui fournissent des informations sur les clients qui peuvent ensuite être utilisées pour modifier leur expérience. Le tableau suivant fournit les différents types de données et le rôle que l’Adobe [!DNL Commerce] joue dans la prise en charge de la collecte et de l’activation de ces données.

| Types de données | Données Storefront (Événements comportementaux) | Données du back-office (événements côté serveur) | Données de profil et de segment du client |
|---|---|---|---|
| **Définition** | Clics ou actions des clients sur votre site. | Informations sur le cycle de vie et détails de chaque commande (passé et actuel). | Qui sont vos acheteurs et à quels segments sont-ils qualifiés ? |
| **Événements capturés par Adobe Commerce** | [pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#pageview)<br>[productPageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)<br>[searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#searchrequestsent)<br>[searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#searchresponsereceived)<br>[addToCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtocart)<br>[openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#opencart)<br>[signIn](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#signin)<br>[signOut](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#signout)}<br>[startCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#startcheckout)<br>[completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#completecheckout)<br>[createRequestList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#createrequisitionlist)<br>[addToRequestList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtorequisitionlist)<br>[removeFromRequestList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#removefromrequisitionlist) | **État de la commande** :<br>[orderPlaced](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderplaced)<br>[orderItemsReturnedInitiated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderitemsreturnedinitiated)<br>[orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderitemsshipped)<br>[orderCancelled](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#ordercancelled)<br>[**Historique des commandes**](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/fundamentals/connect-data#send-historical-order-data) :<br>- SKU, Nom, Quantité de prix, Discount<br>- Catégorie<br> - Montant du paiement, Type, Devise<br> - Mode de livraison et Montant<br> - ID de remboursement, Montant, Devise<br> - Raison de retour, condition, résolution<br> - Adresse<br> - Email | [**Enregistrement de profil**](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-profilerecord) : (nom, genre, adresse, état de fidélité, numéro de téléphone, adresse électronique)<br>**état du compte** :<br>[compteCreated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountcreated)<br>[compteUpdated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountupdated)<br>[compteDeleted](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountdeleted) |

Avec toutes ces données [!DNL Commerce] propriétaires riches, vous êtes prêt à cibler et personnaliser l’expérience de chaque acheteur. Dans la section suivante, vous découvrirez comment [!DNL Commerce] et Adobe Experience Cloud vous aident à créer des expériences personnalisées et les cas d’utilisation que vous pouvez activer.

## Comment l&#39;Adobe [!DNL Commerce] permet-il la personnalisation ?

Adobe [!DNL Commerce] Le partage de données vous permet de collecter et de partager les types de données du tableau précédent avec d’autres produits Adobe Experience Cloud afin d’alimenter les profils et audiences client unifiés, les campagnes personnalisées et des analyses et informations riches.

![Flux de données vers le serveur Experience Platform ](assets/commerce-edge.png){width="700" zoomable="yes"}

Le partage de données d&#39;Adobe [!DNL Commerce] comprend deux composants clés :

1. [Connexion aux données](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview) : partagez les données de vitrine, de back-office et de profil client de l’Adobe [!DNL Commerce] avec le réseau Adobe Experience Platform Edge pour les utiliser dans les applications Adobe Experience Cloud, notamment :

   - [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview) : assemblez les données client de plusieurs sources (ERP, CRM, POS) en profils unifiés et créez des segments basés sur des règles ou sur l’IA.
   - [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started) : lancez des parcours omnicanal personnalisés, y compris des campagnes par e-mail, des SMS, des notifications push, etc.
   - [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) et [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview) : obtenez des informations sur le client et l’entreprise.
   - [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro) : testez et optimisez le contenu, les produits recommandés, les offres, la navigation, etc.

1. [[!DNL Audience Activation]](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) : utilisez les audiences [!DNL Real-Time CDP] pour personnaliser les blocs de contenu dynamique, les promotions et les règles de produit associées sur votre site [!DNL Commerce] d&#39;Adobe.

### Expériences Storefront personnalisées sur n’importe quel canal, à l’échelle

Adobe [!DNL Commerce] peut tirer parti d’une vitrine haute performance, appelée [Edge Delivery Services](https://experienceleague.adobe.com/developer/commerce/storefront/), pour offrir des expériences personnalisées sur tous vos canaux, avec des fonctionnalités d’IA au coeur et une vitesse de base.

Avec les Edge Delivery Services, vous pouvez :

- **Créer du contenu personnalisé** : utilisez la création basée sur des documents, l’expérimentation native avec des variations de texte et d’image Generative AI pour personnaliser l’expérience à grande échelle. Utilisez la création de contenu Assets et Generative AI pour produire des images de produit et marketing à grande échelle.

- **Générer des variations** : permet aux auteurs de contenu d’utiliser l’IA générique pour créer de grands volumes de [contenus textuels et variations d’image](https://experienceleague.adobe.com/en/docs/experience-manager-learn/sites/generative-ai/generate-variations) personnalisés pilotés par l’IA avec Adobe Firefly.

- **Déployer via Edge Delivery Services Storefront** : contenu des fonctionnalités Edge et Commerce alimentées par des composants de dépôt, pour créer des expériences Shoppable personnalisées pour vos audiences.

- **Commerce et Adobe Experience Manager Assets** : création et variations de ressources de produits d’IA générique à grande échelle. Créez, diffusez et surveillez la diffusion du contenu sur n’importe quel canal.

![Déposer : page Détails du produit](assets/drop-in.png){width="700" zoomable="yes"}

### Personalization d’usine : prise en main des fonctionnalités d’Adobe natif [!DNL Commerce]

Adobe [!DNL Commerce] offre une personnalisation puissante avec ses fonctionnalités natives prêtes à l&#39;emploi. Le tableau suivant décrit les fonctions [!DNL Commerce] que vous pouvez activer immédiatement pour commencer à utiliser votre parcours de personnalisation.

| Catégorie | Fonctionnalités |
|---|---|
| Découverte de produit personnalisée | [[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview) : personnalisez et optimisez les résultats de recherche en fonction des actions comportementales sur site d’un acheteur et des affinités avec la recherche optimisée par l’IA.<br>[Marchandisage intelligent de catégories](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-admin/category-merch) : classement de produits piloté par l’IA sur les pages de catégories en fonction des actions comportementales et des affinités sur site d’un acheteur.<br>[Recommendations produit](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview) : recommandations de produits optimisées par l’IA basées sur le comportement, les tendances et les affinités des acheteurs.<br>[Règles de produit connexes](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) : définissez des règles personnalisées pour afficher les produits de votre catalogue afin de générer des ventes croisées et incitatives. |
| Contenu du site personnalisé | [Blocs de contenu dynamique](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) : affiche des blocs de contenu personnalisé, par exemple des bannières, en fonction des segments de clients dans Adobe Commerce. |
| Offres et promotions personnalisées | [Règles de prix du panier](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart) : appliquez des remises aux articles du panier en fonction d’un ensemble de conditions, y compris les segments de clients dans l’Adobe [!DNL Commerce]. |
| Statistiques et mesures | [Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) : Comprenez le fonctionnement et l’amélioration de vos stratégies de personnalisation au fil du temps. |

## Cas d’utilisation de la personnalisation principale

Les clients Adobe [!DNL Commerce] utilisent des fonctionnalités prêtes à l’emploi et partagent des données avec Adobe Experience Cloud pour divers cas d’utilisation. Les sections suivantes mettent en évidence les principaux cas d’utilisation et décrivent comment ils sont implémentés à l’aide des applications Adobe [!DNL Commerce] uniquement ou [!DNL Commerce] plus les applications Experience Cloud.

### Campagnes personnalisées et communications

| Cas d’utilisation | Solution |
|---|---|
| **Panier et navigation abandonnés** - Diffuser un email ou une notification de réengagement personnalisé lorsqu’un client abandonne son panier ou sa session de navigation après avoir démontré un engagement élevé | **Adobe [!DNL Commerce] Seulement** : <br>[Reminders email](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules)<br>**Adobe [!DNL Commerce] avec Adobe Journey Optimizer** : <br>[!DNL Commerce] les données servent de déclencheur pour un parcours d’abandon omnicanal. Personnalisez ce parcours en fonction des attributs du client, de ce qu’il a abandonné, d’autres comportements d’achat et des achats précédents.<br>Commerce avec Adobe Journey Optimizer et Real-Time CDP : personnalisez des campagnes d’abandon basées sur des profils client unifiés et des audiences gérées de manière centralisée, par exemple en créant une audience à taux d’abandon élevé. |
| **Création d’audiences centralisée** - Créez des audiences basées sur des règles ou optimisées par l’IA en fonction du comportement sur site, des achats passés, des attributs de profil, des affinités catégorielles, de l’état de fidélité, de la valeur client, etc. | **Adobe [!DNL Commerce] Uniquement** : <br>Rassemblez les informations de profil client lorsque les clients [!DNL Commerce] créent des comptes. Créez des [ segments client](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/segments/customer-segments) basés sur des règles et des groupes de clients pour personnaliser le contenu et les promotions.<br>**Adobe [!DNL Commerce] avec Adobe Real-Time CDP**:<br> [Profils unifiés](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home) à partir de sources de données et de canaux ; audiences basées sur des règles ou optimisées par l’IA. |
| **Offre email/SMS personnalisée basée sur le comportement de l’acheteur** - Envoyer des offres personnalisées aux clients par e-mail ciblé en fonction des achats précédents et du comportement d’achat, par exemple, envoyer une offre pour les produits ou les catégories que les clients ont consultés ou engagés. | **Adobe [!DNL Commerce] Uniquement** : <br>Exporter des données à utiliser avec des solutions d’automatisation du marketing.<br>**Adobe [!DNL Commerce] avec Adobe Journey Optimizer et Real-Time CDP** : <br>[!DNL Commerce] les données servent de déclencheur pour les offres par e-mail ou par SMS et fournissent des signaux (comportements d’acheteur) à personnaliser en fonction de leurs besoins. Real-Time CDP n’est pas obligatoire, mais en règle générale, ces offres et campagnes sont créées autour des audiences, qui seraient créées et gérées dans Real-Time CDP. |
| **Produits/marques compatibles avec l’offre cross ou Upsell** - Si un client achète un produit ou une marque compatible ou indique une affinité élevée avec un autre produit ou marque, envoyez une campagne (email/SMS) pour générer une conversion de vente croisée. | **Adobe [!DNL Commerce] Seulement** : <br>Utilisez l’Adobe [!DNL Commerce] [Recommendations de produit](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview) pour recommander des produits spécifiques sur le site. Vous pouvez également utiliser [Règles de produit connexes](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) pour suggérer d’autres produits.<br>**[!DNL Commerce] avec [!DNL Target]**: <br>Adobe [!DNL Target] dispose également d’un moteur de recommandation de produit intégré avec de puissantes fonctionnalités telles que l’affinité catégorielle. Il peut être utilisé pour la vente croisée ou par upsell.<br>**[!DNL Commerce] avec Adobe Journey Optimizer** :<br>Utilisez [!DNL Target] ou [!DNL Commerce] pour déterminer les produits à recommander, puis effectuez la diffusion via Adobe Journey Optimizer. |

### Expériences personnalisées sur le site

| Cas d’utilisation | Solution |
|---|---|
| **Contenu du site personnalisé** - Personnalisez les bannières du site et tout autre contenu de page en fonction des actions de l’acheteur, telles que la navigation dans les produits et les affinités catégorielles. Déployez le contenu le mieux adapté en fonction des résultats des tests A/B ou des objectifs de l’entreprise. | **Adobe [!DNL Commerce] Uniquement** : <br>Déployez des [blocs de contenu dynamique](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) spécifiques aux segments.<br>**[!DNL Commerce] avec Real-Time CDP **: <br>Utilisez [l’Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) pour déployer des blocs de contenu dynamique spécifiques à l’audience qui répondent à des actions en temps réel et à des données de profil client unifiées, tout en gérant de manière centralisée les profils et les audiences dans Real-Time CDP.<br>**[!DNL Commerce] avec[!DNL Target]** :<br>Personnalisez chaque partie de l’expérience du site, y compris le contenu, les éléments de navigation, les mises en page complètes, etc. à l’aide des données d’Adobe [!DNL Commerce] dans l’Adobe [!DNL Target]. Contenu du test A/B, sélectionnez et déployez automatiquement le contenu gagnant pour chaque client.<br>**[!DNL Commerce] avec AEM Assets **:<br>Stockez tout votre contenu dans Adobe Experience Manager Assets. Accédez à ce contenu en mode natif depuis Adobe Commerce. Utilisez Generative AI pour créer des variations de contenu à personnaliser pour différents segments ou audiences. |
| **Offre sur site personnalisée basée sur le comportement** - Personnalisez des promotions en fonction d’actions d’achat, telles que la navigation dans les produits et les affinités catégorielles. Déployez la meilleure offre suivante en fonction des résultats des tests A/B ou des objectifs de l’entreprise. | **Adobe [!DNL Commerce] Uniquement** : <br>Déployez un catalogue spécifique au segment et [règles de prix du panier](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart).<br>**Adobe [!DNL Commerce] avec Real-Time CDP** : <br>Utilisez [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) pour déployer des offres spécifiques à l’audience, tout en gérant de manière centralisée les profils/audiences dans Real-Time CDP.<br>**Commerce avec[!DNL Target]** : utilisez l’offer decisioning pour déterminer l’offre à déployer, le test A/B ou définir des objectifs commerciaux pour guider les offres déployées dans Adobe Commerce. |

### Analytics et insights

| Cas d’utilisation | Solution |
|---|---|
| **Comportement des clients par canal** - Comprenez les nuances de la manière dont les clients interagissent dans chaque canal (web, en personne, application, autre) pour affecter les stratégies marketing pour chaque canal. Comprenez l’entonnoir du nouvel acheteur et les faiblesses de l’expérience client. | **Adobe [!DNL Commerce] Seulement** : <br>[Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) fournit des analyses riches sur le canal numérique [!DNL Commerce], mais pas sur tous les canaux ou éléments plus larges du parcours client.<br>**Adobe [!DNL Commerce] avec Customer Journey Analytics** : <br>[!DNL Commerce] les tableaux de bord de données de flux pour obtenir des détails complets sur toutes les étapes de l’expérience client (entre canaux). Comprenez chaque point de contact et l’entonnoir plus large afin d’identifier les points faibles dans le parcours client où les clients peuvent tomber. |
| **Tendances d’achat** - Comprendre les comportements d’achat sur une période spécifique (par exemple, l’analyse du panier d’achat, l’analyse des produits) pour identifier les tendances, le caractère saisonnier et optimiser le marketing en fonction des schémas d’achat historiques. | **Adobe [!DNL Commerce] Seulement** : <br>[Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) fournit des analyses riches sur le canal numérique [!DNL Commerce], mais pas sur tous les canaux ou éléments plus larges du parcours client.<br>**Adobe [!DNL Commerce] avec Customer Journey Analytics** : <br>[!DNL Commerce] les tableaux de bord de données de flux pour obtenir des détails complets sur toutes les étapes de l’expérience client (entre canaux). Comprenez chaque point de contact et l’entonnoir plus large afin d’identifier les points faibles dans le parcours client où les clients peuvent tomber. |

## Exemples de cas d’utilisation

- Découvrez comment utiliser Adobe Journey Optimizer pour [envoyer un email de panier abandonné](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/using-ajo).
- Découvrez comment [créer une audience dans Real-Time CDP](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/create-audience) pour informer une règle de prix de panier dans Adobe [!DNL Commerce].
