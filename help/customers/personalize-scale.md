---
title: Personnalisation à grande échelle
description: Découvrez les fonctionnalités d’Adobe Commerce qui vous permettent de créer une expérience personnalisée pour vos acheteurs.
feature: Customers, Storefront, Personalization
source-git-commit: a4eeda918adcb74ad5e7008b80eff703fa15e878
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 0%

---

# Personnalisation à grande échelle

&#x200B; personnalisation à grande échelle permet aux entreprises de personnaliser l’expérience d’achat pour chaque point de contact client en fonction du contexte immédiat et du comportement observé précédemment. L’objectif est de présenter à chaque fois l’expérience la plus pertinente et personnalisée possible.

Pour comprendre les avantages de la diffusion d’une expérience d’achat personnalisée, téléchargez la [_Prise en main de la personnalisation à l’échelle_](https://business.adobe.com/resources/reports/getting-started-with-personalization-at-scale.html) rapport.

Pour créer une expérience d’achat personnalisée, vous devez connaître le type de données nécessaires pour comprendre le contexte du client. De là, vous découvrez les fonctionnalités d’Adobe Commerce qui utilisent ces données pour déverrouiller les informations sur les clients dont vous avez besoin pour créer l’expérience d’achat personnalisée.

L’image suivante illustre les concepts impliqués dans la personnalisation de l’expérience d’achat :

![Création d’un pipeline de personnalisation](assets/personalization-journey.png){width="700" zoomable="yes"}

Cet article traite plus en détail chacun des concepts ci-dessus.

## Comment personnaliser l’expérience d’achat

La personnalisation réussie commence avec le contexte client. Dans cette section, vous découvrirez les types de données disponibles pour vous aider à créer le contexte client.

### Données Storefront

Les données Storefront, également appelées données comportementales ou de navigateur, peuvent révéler des informations sur la manière dont vos acheteurs interagissent avec votre site. Par exemple :

- Quels produits et catégories intéressent le plus mes acheteurs ?
- Dans quel type de requêteurs mes acheteurs sont-ils les plus actifs ?
- Mes acheteurs ajoutent-ils des produits au panier avant de les abandonner ?
- Mes acheteurs utilisent-ils un navigateur de bureau ou mobile ?

Les événements storefront suivants capturent des données qui peuvent vous aider à répondre à ces questions :

- [pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [productPageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [addToCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [signIn](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [signOut](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [startCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [createRequestList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [addToRequestList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [removeFromRequestList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)

### Données du back office

Les données de back-office, également appelées données côté serveur, peuvent révéler des informations sur le cycle de vie de la commande. Par exemple :

- Certains produits sont-ils achetés plus fréquemment en fonction de la saison ?
- Mes acheteurs renvoient-ils des produits ?
- Comment calculer la valeur client sur la durée de vie ?

Les événements back-office suivants capturent des données qui peuvent vous aider à répondre à ces questions :

- [orderPlaced](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderItemsReturnedInitiated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderCancelled](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)

### Profil client et données de segment

Les données de profil client peuvent fournir des informations sur les acheteurs et les segments pour lesquels ils sont qualifiés. Par exemple :

- Nom
- Genre
- Adresse
- État de fidélité
- Numéro de téléphone
- Adresse e-mail
- État de fidélité
- Numéro de téléphone
- Adresse e-mail
- Eligibilité aux mises à niveau
- Acheteurs sur plusieurs canaux
- Perspectives pour les nouveaux produits
- Membres de la fidélité Gold, Silver ou bronze

Les événements de profil suivants capturent des données qui peuvent vous aider à répondre à ces questions :

- [Enregistrement de profil](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-profilerecord)
- [accountCreated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [accountUpdated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [accountDeleted](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)

Les données de storefront, back-office et de profil constituent la base du contexte client et de commande de Commerce, ce qui vous permet de connaître les produits que vos clients consultent et, en fin de compte, effectuent un achat. Vous pouvez ensuite cibler leurs intérêts et personnaliser leur expérience. Dans la section suivante, vous découvrirez les types d’expériences personnalisées que vous pouvez interagir avec vos clients.

## Types d’expériences personnalisées

Les données contextuelles des clients et des commandes dans Commerce alimentent les types d’expériences personnalisées suivants :

| Expérience | Description |
|---|---|
| **Découverte de produit** | Contient les services de marchandisage qui sont [déployé en tant que SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas). Il s’agit de fonctionnalités qui vous permettent d’utiliser des données comportementales, des attributs de produit et des niveaux d’inventaire pour personnaliser automatiquement la découverte de produits dans les résultats de recherche, les recommandations de produits et les pages de navigation. Ces fonctionnalités sont toutes utilisées [ADOBE SENSEI AI](https://business.adobe.com/products/sensei/adobe-sensei.html). |
| **Contenu du site** | Fait référence à la possibilité de déployer des blocs de contenu dynamique personnalisés en fonction de la navigation actuelle des clients sur votre site. |
| **Offres et campagnes** | Permet de déployer du contenu promotionnel personnalisé basé sur des données de segment. |
| **Mesure** | Utilise des informations sur les données pour mieux comprendre votre entreprise, notamment les recettes, les performances des canaux et des marchandises, les promotions, etc. |

Dans les deux sections suivantes, vous découvrirez comment utiliser ces données pour créer des expériences personnalisées dans [Adobe Experience Platform](#using-commerce-data-in-adobe-experience-platform) et dans [fonctionnalités commerciales natives](#using-commerce-data-in-native-commerce-features).

## Utilisation des données Commerce dans Adobe Experience Platform

Pour créer une expérience personnalisée pour vos acheteurs sur tous les canaux, envoyez vos données Commerce au réseau Edge Experience Platform à l’aide de la variable [[!DNL Data Connection]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview) extension .

![Flux de données vers le serveur Experience Platform](assets/commerce-edge.png){width="700" zoomable="yes"}

Dans l’image ci-dessus, vos données de vitrine, de back-office et de profil client sont envoyées au serveur Edge Experience Platform à l’aide d’un SDK, d’une API et d’un connecteur source. Vous n’avez pas besoin de comprendre pleinement le fonctionnement de ces pièces, car l’extension gère la complexité du partage de données pour vous. Lorsque les données d’événement se trouvent à la périphérie, vous pouvez extraire ces données dans d’autres applications Experience Platform.

Le tableau suivant met en évidence certaines des applications Experience Platform disponibles et la manière dont ces applications utilisent vos données Commerce.

| Expérience | Application | Utilisation des données commerciales |
|---|---|---|
| **Contenu du site** | [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview) | Les données Adobe Commerce alimentent des profils client unifiés, Real-Time CDP regroupant les données de sources différentes (ERP, CRM, CMS, POS) en profils uniques. Real-Time CDP peut également créer des segments basés sur des règles et sur l’IA à utiliser ensuite dans l’ensemble de vos solutions marketing. Vous pouvez également utiliser les audiences Real-Time CDP pour personnaliser les blocs de contenu, les promotions et les règles de produit associées. Voir [[!DNL Audience Activation]](../customers/audience-activation.md) pour en savoir plus &#x200B; |
|  | [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro) | Les données Adobe Commerce peuvent être activées dans Adobe [!DNL Target] pour tester, optimiser et créer des landing pages dynamiques. Vous pouvez personnaliser l’ordre dans lequel le contenu est affiché sur une page, tel que les descriptions, les spécifications, les révisions et les produits recommandés en fonction des données de commerce envoyées. |
| **Offres et campagnes** | [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started) | Les données comportementales et de back-office d’Adobe Commerce peuvent servir de déclencheur pour les parcours omnicanal personnalisés, y compris les campagnes par e-mail, les SMS, les notifications push, etc. &#x200B; |
| **Mesure** | [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview) et [Client [!DNL Journey Analytics]](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) | Commerce envoie les données de storefront et back-office à Customer [!DNL Journey Analytics] (et uniquement les données storefront à Adobe) [!DNL Analytics]) pour permettre des analyses plus riches au-delà des mesures de base d’Adobe Commerce Intelligence, telles que les recettes, les marchandises et les promotions. &#x200B; |

Pour en savoir plus sur la manière d’envoyer vos données Commerce à l’Experience Platform, voir [Connexion aux données](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview).

## Utilisation des données Commerce dans des fonctionnalités commerciales natives

Dans la section suivante, vous découvrirez comment utiliser les fonctionnalités commerciales natives, telles que le Recommendations de produit et la recherche en direct, pour créer une expérience d’achat personnalisée. Vous découvrirez également une fonctionnalité appelée [!DNL Audience Activation], qui utilise les données d’un produit disponible dans l’Experience Platform appelé Real-Time CDP, comme indiqué [précédemment](#using-commerce-data-in-adobe-experience-platform). Bien que Real-Time CDP ne soit pas native de Commerce, ses informations peuvent être ingérées dans Commerce par le biais de la variable [[!DNL Audience Activation]](../customers/audience-activation.md) extension .

Le tableau suivant met en évidence les fonctionnalités de Commerce disponibles pour transformer les données contextuelles client et commande de Commerce en informations exploitables.

| Expérience | Fonctionnalité | Description |
|---|---|---|
| **Découverte de produit** | [Recherche en direct](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/guide-overview) | Utilise des algorithmes de classement AI pour personnaliser et optimiser les résultats de recherche en fonction des actions comportementales sur site d’un acheteur, ce qui renforce la pertinence et la conversion de la recherche. |
|  | [Recommendations de produit](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview) | Affiche des recommandations de produits optimisées par l’IA en fonction du comportement des acheteurs, des tendances, de la similarité de produits, etc. Lorsqu’elles sont combinées à votre catalogue Adobe Commerce, les recommandations de produits offrent une expérience hautement attrayante, pertinente et personnalisée. |
|  | [Marchandisage des catégories](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-admin/category-merch) | Accessible depuis l’administrateur de la recherche en direct, le marchandisage par catégorie utilise l’IA pour réorganiser automatiquement la séquence de produits sur chaque page de catégorie afin d’améliorer la pertinence et la conversion pour chaque acheteur. Vous pouvez créer et gérer des règles optimisées par l’IA afin d’organiser automatiquement le séquencement des produits sur les pages de catégories en fonction des actions d’acheteur et des affinités. |
| **Contenu du site** | [Blocs dynamiques reposant sur des fonctionnalités commerciales natives](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) | Permet de diffuser du contenu personnalisé du site en fonction de la logique configurée dans les règles de prix et les segments client. |
|  | [Blocs dynamiques informés des audiences Real-Time CDP](../customers/audience-activation.md) | Permet aux commerçants de diffuser du contenu personnalisé sur le site en fonction des audiences configurées dans Real-Time CDP. |
| **Offres et campagnes** | [Règles de prix du panier](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart) | Vous permet d’appliquer des remises à des articles du panier en fonction d’un ensemble de conditions. |
|  | [Blocs dynamiques reposant sur des fonctionnalités commerciales natives](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) | Permet d’afficher des promotions de bannières personnalisées en fonction des segments de clients configurés nativement dans Commerce. |
|  | [Blocs dynamiques informés des audiences Real-Time CDP](../customers/audience-activation.md) | Permet d&#39;afficher des promotions personnalisées en fonction des audiences configurées dans Real-Time CDP. |
| **Mesure** | [Adobe Commerce Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) | (Anciennement connu sous le nom de Magento Business Intelligence) est une plateforme cloud qui fournit des informations sur les bonnes pratiques pour vous aider à prendre des décisions basées sur les données et à prendre des mesures claires et éclairées. Adobe Commerce Intelligence peut analyser vos données pour vous aider à répondre à des questions sur la croissance des commandes, le comportement des clients et l’efficacité des stratégies promotionnelles. |
