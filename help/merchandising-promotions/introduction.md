---
title: Présentation du merchandising et des promotions Commerce
description: Découvrez les outils Commerce pour créer des promotions ciblées et des opportunités d’engagement client.
exl-id: 8e55ac42-aeef-4f97-b1e8-9b2db354e5e6
source-git-commit: 9c25196367023a44fa76e441d485693493a4c058
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 1%

---

# Présentation du merchandising et des promotions Commerce

Ciblez les promotions et créez des opportunités d’engagement client, et transformez les acheteurs en acheteurs. Gérez les relations client en soutenant les activités après achat et en offrant des remises spéciales aux clients récurrents. Découvrez les bonnes pratiques et techniques pour prendre en charge vos initiatives d’optimisation du moteur de recherche.

## Marchandisage

_Marchandisage_ est un terme utilisé dans le commerce de détail pour décrire l&#39;art et la science de l&#39;élaboration du plan d&#39;étage et de la présentation des produits. Vous pouvez considérer la [navigation par catégorie](../catalog/navigation-top.md) comme le plan d’étage du magasin, et la présentation dynamique des produits comme les conditions que vous pouvez appliquer à l’énumération des produits du magasin. Vous pouvez également implémenter des programmes qui stimulent les ventes de produits :

- [!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."} [Marchandiseur visuel](visual-merchandiser.md) - Ensemble d’outils avancés qui vous permettent de positionner des produits et d’appliquer des conditions qui déterminent quels produits apparaissent dans la liste des catégories.

- [Registres cadeaux](gift-registries.md) - Donnez à vos clients la possibilité de créer des registres cadeaux pour des occasions spéciales et d&#39;inviter leurs amis et leur famille à acheter leurs cadeaux dans le registre des cadeaux.

- [Récompenses et fidélité](rewards-loyalty.md) - Utilisez un système de points pour mettre en œuvre des programmes uniques qui stimulent l’engagement des clients et favorisent leur fidélité. Vous pouvez accorder des points pour un large éventail de transactions et d’activités client et contrôler l’attribution, le solde et l’expiration des points.

- [Ventes et événements privés](events-private-sales.md) - Utilisez votre base de clients existante pour générer du buzz et de nouveaux prospects, ou pour écouler votre stock excédentaire par le biais de ventes privées et d’autres événements de catalogue.

>[!TIP]
>
>Pour en savoir plus sur les recommandations de produits et sur la manière dont elles peuvent vous apporter l’insight et le contrôle dont vous avez besoin pour offrir la meilleure expérience à vos acheteurs, consultez le [Guide d’utilisation des recommandations de produits](https://experienceleague.adobe.com/docs/commerce/product-recommendations/guide-overview.html).

## Promotions

Dans Adobe Commerce, utilisez les fonctionnalités de promotions pour configurer les relations de produit et utilisez les règles de prix pour déclencher des remises en fonction de diverses conditions. Vous pouvez utiliser les règles de prix pour proposer des incentives aux clients, par exemple :

- Envoyez à vos meilleurs clients un coupon pour une remise sur un produit spécifique
- Offrez la livraison gratuite pour les achats supérieurs à un certain montant
- Planifier une promotion pour une période spécifique

Une règle est un ensemble de conditions (une ou plusieurs) qui appliquent des changements de prix aux produits lorsqu’un ou tous les produits sont remplis. Chaque règle peut comporter plusieurs conditions, qui s’appliquent lorsque toutes les instructions ou une partie d’entre elles (une ou plusieurs, mais pas toutes) sont vraies ou fausses.

### Conditions

Les conditions sont des instructions qui affinent la liste des produits et des situations pour appliquer la règle. Les attributs et les options des conditions diffèrent selon les types de règles disponibles. Une fois cette condition remplie, l’action est effectuée, par exemple, des remises, des achats uniques (BOGO) et d’autres options. Les règles peuvent être aussi simples ou complexes que nécessaire pour répondre aux besoins de votre entreprise, aux remises et promotions saisonnières et aux opportunités à l’année longue. Par exemple, vous pouvez ajouter quelques options supplémentaires pour les vacances tout en fournissant la livraison gratuite toute l’année lorsque les paniers ont un sous-total élevé.

>[!NOTE]
>
>Si vous souhaitez définir une condition en fonction d’un attribut de produit spécifique, **[!UICONTROL Use for Promo Rule Conditions]** devez définir sur `Yes` pour l’attribut dans vos [Propriétés du storefront](../catalog/attribute-product-create.md).


### Règles de prix

Pour les [règles de prix de catalogue](price-rules-catalog.md), vous créez des conditions basées sur des [jeux d’attributs](../catalog/attribute-sets.md) dans votre catalogue, des fonctions de comparaison et des attributs sélectionnés. Vous créez les conditions telles que des phrases en sélectionnant quelques instructions. Par exemple, vous pouvez créer deux règles de prix pour appliquer des remises aux vêtements pour enfants et aux vêtements pour hommes/femmes en fonction de la catégorie.

![Diagramme - Exemple de règles de prix de catalogue](./assets/diagram-catalog-price-rules.png){width="500"}

[Règle de prix du panier](price-rules-cart.md) les conditions peuvent être basées sur n’importe quelle catégorie enfant du magasin [racine](../catalog/category-root.md). Les règles de prix sont établies à l’avance et entrent en vigueur dès que les conditions requises sont remplies. Ces règles utilisent des attributs, y compris des combinaisons d’attributs de produit telles que la correspondance d’un SKU dans le panier à l’aide d’attributs de produit. Ces règles peuvent également utiliser des conditions de quantité pour la sélection de produits, des combinaisons de conditions pour des règles complexes et des attributs de panier tels que le sous-total.

![Diagramme - Exemple de règles de prix de panier](./assets/diagram-cart-price-rules.png){width="500"}

## Communications et SEO

Maîtriser l’optimisation du moteur de recherche [SEO)](seo-overview.md) est essentiel pour attirer des acheteurs potentiels. Découvrez comment optimiser les moteurs de recherche et affiner le contenu et la présentation de votre site pour améliorer la manière dont les pages sont indexées par les moteurs de recherche.

L’une des tâches à effectuer avant de lancer votre boutique consiste à examiner les modèles d’e-mail utilisés pour toutes les communications envoyées depuis votre boutique afin de s’assurer qu’ils reflètent votre marque. Mais vous devriez aller plus loin en développant d’autres communications qui font la promotion de votre marque et de vos produits auprès des clients existants. Vous pouvez personnaliser le contenu avec des variables et des balises de balisage.

>[!NOTE]
>
>Les versions 2.4.0 à 2.4.3 d’Adobe Commerce et de Magento Open Source incluaient l’extension développée par le fournisseur dotdigital utilisée pour s’intégrer à dotdigital Engagement Cloud. À compter de la version 2.4.4, cette extension n’est plus fournie avec la version de base et doit être installée et mise à jour à partir de Commerce Marketplace. La Marketplace permet également d’accéder à la documentation actuelle fournie par le développeur d’extensions.
>><br><br>
>>Si l’extension groupée est activée et configurée, vous devez mettre à jour votre fichier composer.json dans le cadre du processus de mise à niveau vers la version 2.4.4 et pour gérer les mises à jour d’extension à l’avenir. Voir [Mise à niveau des modules](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) dans le _Guide de mise à niveau_ pour plus d’informations.

- [Newsletters](newsletters.md) - Produisez des newsletters, gérez votre liste d’abonnés, développez du contenu et générez du trafic vers votre boutique.

- [Flux RSS](social-rss.md#rss-feeds) - Utilisez les flux RSS pour publier des informations sur vos produits sur les sites d&#39;agrégation d&#39;achats et même les inclure dans vos newsletters. Les clients peuvent s&#39;abonner à vos flux RSS pour en savoir plus sur les nouveaux produits et les promotions.

- [Réseaux sociaux](social-rss.md#social-networks) - Intégrez votre boutique à vos réseaux sociaux en installant une extension Marketplace ou en ajoutant un plug-in à vos pages de contenu.

## Outils marketing Google

La configuration de votre boutique est intégrée aux outils Google suivants pour vous aider à optimiser votre contenu, à analyser votre trafic et à connecter votre catalogue aux agrégateurs d’achats et aux places de marché.

>[!NOTE]
>
>À partir de la version 2.4.5, l’intégration des services Google est mise à jour afin de prendre en charge l’utilisation des API GTag. GTag est un mécanisme unifié d’intégration de la fonctionnalité Google pour les pages web. Il prend en charge les fonctionnalités et opportunités les plus récentes pour le suivi et la gestion du contenu via les services Google. Pour plus d’informations, consultez la [documentation destinée aux développeurs de Google Analytics](https://developers.google.com/analytics/devguides/collection/gtagjs).

- [Google Analytics](google-analytics.md) - Utilisez Google Universal Analytics pour définir des dimensions et des mesures personnalisées supplémentaires pour le suivi, avec la prise en charge des interactions d’applications hors ligne et mobiles et l’accès aux mises à jour en cours.

- [Google Tag Manager](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Utilisez Google Tag Manager pour gérer les nombreuses balises liées aux événements de campagne marketing.

- [Google AdWords](google-adwords.md) - Créez une campagne Google AdWords et suivez les conversions pour votre boutique.
