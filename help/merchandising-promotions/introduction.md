---
title: Présentation du marchandisage et des promotions Commerce
description: Découvrez les outils Commerce permettant de créer des promotions ciblées et des opportunités d’engagement client.
exl-id: 8e55ac42-aeef-4f97-b1e8-9b2db354e5e6
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 0%

---

# Présentation du marchandisage et des promotions Commerce

Ciblez des promotions et créez des opportunités d’engagement client, et transformez les acheteurs en acheteurs. Gérez les relations client en prenant en charge les activités après achat et en offrant des remises spéciales aux clients réguliers. Découvrez les bonnes pratiques et les techniques pour prendre en charge vos initiatives d’optimisation pour les moteurs de recherche.

## Marchandisage

_Marchandisage_ est un terme utilisé dans la vente au détail pour décrire l’art et la science de l’élaboration du plan de plancher et de la présentation des produits. Vous pourriez penser au [navigation par catégorie](../catalog/navigation-top.md) comme plan de base du magasin, et la présentation dynamique des produits comme conditions que vous pouvez appliquer à la liste des produits dans le magasin. Vous pouvez également mettre en oeuvre des programmes qui génèrent davantage de ventes de produits :

- [Marchandisage visuel](visual-merchandiser.md) - Ensemble d’outils avancés qui vous permet de positionner des produits et d’appliquer des conditions qui déterminent quels produits apparaissent dans la liste de catégories.

- [Enregistrements de cadeaux](gift-registries.md) - Donnez à vos clients la possibilité de créer des registres de cadeaux pour les occasions spéciales et d’inviter leurs amis et leur famille à acheter leurs cadeaux dans le registre des cadeaux.

- [Récompenses et fidélité](rewards-loyalty.md) - Utilisez un système de points pour mettre en oeuvre des programmes uniques qui favorisent l’engagement des clients et la fidélisation de leurs clients. Vous pouvez attribuer des points pour un large éventail d’activités de transaction et de client et contrôler l’attribution, l’équilibre et l’expiration des points.

- [Ventes et événements privés](events-private-sales.md) - Utilisez votre base de clients existante pour générer du buzz et de nouveaux prospects, ou pour décharger l’inventaire excédentaire par le biais de ventes privées et d’autres événements de catalogue.

>[!TIP]
>
>Pour en savoir plus sur Product Recommendations et sur la manière dont ils peuvent vous donner les informations et le contrôle dont vous avez besoin pour créer la meilleure expérience pour vos acheteurs, voir la section [Guide de l’utilisateur de Recommendations produit](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html).

## Promotions

Dans Adobe Commerce, utilisez les fonctionnalités de promotion pour configurer les relations entre les produits et utilisez les règles de prix pour déclencher des remises selon diverses conditions. Vous pouvez utiliser des règles de prix pour offrir des avantages aux clients, tels que :

- Envoyer un coupon à vos meilleurs clients pour une remise sur un produit spécifique
- Offrir la livraison gratuite pour les achats d’un certain montant
- Planification d’une promotion pour une période spécifique

Une règle est un ensemble de conditions (une ou plusieurs) qui appliquent des changements de prix à des produits lorsqu’un ou tous sont satisfaits. Chaque règle peut avoir plusieurs conditions, en s’appliquant lorsque toutes ou n’importe quelle (une ou plusieurs, mais pas toutes) instructions sont vraies ou fausses.

### Conditions

Les conditions sont des instructions qui affinent la liste des produits et des situations pour l’application de la règle. Les attributs et options des conditions diffèrent entre les types de règles disponibles. Lorsqu’elle est remplie, l’action est effectuée, par exemple les remises, l’achat-un-get-one (BOGO) et d’autres options. Les règles peuvent être aussi simples ou complexes que nécessaire pour répondre aux besoins de votre entreprise, proposer des remises et des promotions saisonnières et saisir des opportunités d’une année sur l’autre. Par exemple, vous pouvez ajouter quelques options supplémentaires pour les jours fériés tout en proposant une livraison gratuite toute l’année lorsque le sous-total des paniers est élevé.

>[!NOTE]
>
>Si vous souhaitez définir une condition basée sur un attribut de produit spécifique, **[!UICONTROL Use for Promo Rule Conditions]** doit être défini sur `Yes` pour l’attribut dans votre [Propriétés Storefront](../catalog/attribute-product-create.md).


### Règles de prix

Pour [règles de prix du catalogue](price-rules-catalog.md), vous créez des conditions basées sur [ensembles d’attributs](../catalog/attribute-sets.md) dans votre catalogue, les fonctions de comparaison et les attributs sélectionnés. Vous créez les conditions comme des phrases en sélectionnant quelques instructions. Vous pouvez, par exemple, créer deux règles de prix pour appliquer des remises aux vêtements pour enfants et aux vêtements pour homme/femme en fonction de la catégorie.

![Diagramme - Exemples de règles de prix de catalogue](./assets/diagram-catalog-price-rules.png){width="500"}

[Règle de prix du panier](price-rules-cart.md) Les conditions peuvent être basées sur n’importe quelle catégorie enfant du magasin. [root](../catalog/category-root.md). Les règles de prix sont établies à l’avance et mises en oeuvre dès que les conditions requises sont remplies. Ces règles utilisent des attributs, y compris des combinaisons d’attributs de produit, comme la correspondance d’un SKU dans le panier à l’aide d’attributs de produit. Ces règles peuvent également utiliser des conditions de quantité de sélection de produits, des combinaisons de conditions pour les règles complexes et des attributs de panier tels que le sous-total.

![Diagramme - Exemples de règles de prix de panier](./assets/diagram-cart-price-rules.png){width="500"}

## Communications et SEO

Maîtriser [Optimisation du moteur de recherche (SEO)](seo-overview.md) est essentiel pour attirer des acheteurs potentiels. Découvrez l’optimisation des moteurs de recherche et affinez le contenu et la présentation de votre site afin d’améliorer la façon dont les pages sont indexées par les moteurs de recherche.

Une des tâches à effectuer avant de lancer votre boutique consiste à passer en revue les modèles d’email utilisés pour toutes les communications envoyées depuis votre boutique afin de vous assurer qu’elles reflètent votre marque. Mais vous devriez aller plus loin en développant d’autres communications qui font la promotion de votre marque et de vos produits auprès des clients existants. Vous pouvez personnaliser le contenu à l’aide de variables et de balises.

>[!NOTE]
>
>Les versions 2.4.0 à 2.4.3 d’Adobe Commerce et de Magento Open Source comprenaient l’extension dotdigital développée par les fournisseurs et utilisée pour l’intégration à dotdigital Engagement Cloud. À compter de la version 2.4.4, cette extension n’est plus fournie avec la version principale et doit être installée et mise à jour à partir du Commerce Marketplace. Le Marketplace permet également d’accéder à la documentation actuelle fournie par le développeur de l’extension.
><br><br>
>Si l’extension groupée est activée et configurée, vous devez mettre à jour votre fichier compositeur.json dans le cadre du processus de mise à niveau 2.4.4 et gérer les mises à jour de l’extension. Voir [Mettre à niveau les modules](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) dans le _Guide de mise à niveau_ pour plus d’informations.

- [Newsletters](newsletters.md) - Créer des newsletters, gérer votre liste d’abonnés, développer du contenu et diriger le trafic vers votre boutique.

- [Flux RSS](social-rss.md#rss-feeds) - Utilisez des flux RSS pour publier les informations sur vos produits sur les sites d’agrégation d’achats et les inclure même dans vos newsletters. Les clients peuvent s’abonner à vos flux RSS pour en savoir plus sur les nouveaux produits et promotions.

- [Réseaux sociaux](social-rss.md#social-networks) - Intégrez votre boutique à vos réseaux sociaux en installant une extension Marketplace ou en ajoutant un module externe à vos pages de contenu.

## Outils de marketing Google

La configuration de votre magasin est intégrée aux outils Google suivants pour vous aider à optimiser votre contenu, à analyser votre trafic et à connecter votre catalogue aux agrégateurs d’achats et aux marchés.

>[!NOTE]
>
>À compter de la version 2.4.5, l’intégration des services Google est mise à jour pour prendre en charge l’utilisation des API GTag. GTag est un mécanisme unifié d’intégration à la fonctionnalité Google pour les pages web. Il prend en charge les fonctionnalités et opportunités les plus récentes de suivi et de gestion de contenu par le biais des services Google. Pour plus d’informations, voir [Documentation destinée aux développeurs Google Analytics](https://developers.google.com/analytics/devguides/collection/gtagjs).

- [Google Analytics](google-analytics.md) - Utilisez Google Universal Analytics pour définir des dimensions et des mesures personnalisées supplémentaires pour le suivi, avec la prise en charge des interactions avec les applications mobiles et hors ligne, ainsi que l’accès aux mises à jour en cours.

- [Expériences de contenu Google](google-content-experiments.md) - Configuration d’un test A/B de produits, de catégories ou de pages de contenu à l’aide de contenu Google Analytics

- [Gestionnaire de balises de Google](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Utilisez Google Tag Manager pour gérer les nombreuses balises liées aux événements de campagne marketing.

- [Google AdWords](google-adwords.md) - Créez une campagne Google AdWords et effectuez le suivi des conversions pour votre magasin.
