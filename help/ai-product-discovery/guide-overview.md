---
title: Découverte de produits par l’IA
description: Découvrez comment l’enrichissement du catalogue [!DNL Adobe Commerce] et l’enrichissement PDP permettent de combler les lacunes dans les données structurées du produit et dans la copie ciblée sur l’acheteur pour la découverte de produits par IA.
role: Admin, User, Leader
source-git-commit: f2cf82dad7ec3c86a3b9a0a5635556ac2e77dd05
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%
---
# Découverte de produits par l’IA

La découverte de produits est la manière dont les acheteurs trouvent et évaluent des produits qui répondent à leurs besoins. Dans les outils d’IA conversationnelle tels que [!DNL ChatGPT] et [!DNL Gemini], les acheteurs peuvent décrire ce qu’ils veulent dans le langage courant et utiliser les réponses générées par l’IA pour explorer et comparer des produits. L’utilité de ces réponses dépend en partie de la capacité des agents de l’IA à accéder aux données pertinentes sur les produits et à les interpréter.

## À qui s’adresse ce guide {#who-this-guide-is-for}

- Les spécialistes du marketing et du marchandisage numériques qui souhaitent que les données sur les produits soient précises et utiles pour la découverte de produits assistée par l’IA.
- Les marchandiseurs qui ont besoin d’une méthode contrôlée pour enrichir des produits sélectionnés ou préparer une copie pour une campagne.
- Administrateurs [!DNL Adobe Commerce] responsables des données de catalogue, des services et de l’accès administrateur.

## Importance de la découverte de produits

Les acheteurs décrivent souvent un besoin, une utilisation ou une préférence plutôt que de rechercher un nom de produit ou un attribut technique exact. Pour faire correspondre ces requêtes aux produits pertinents, les agents d’IA ont besoin d’informations sur les produits qui sont à la fois structurées et significatives pour les acheteurs.

Lorsque les enregistrements des produits sont incomplets, incohérents ou axés uniquement sur les spécifications techniques, les agents peuvent avoir des difficultés à comprendre quels produits correspondent à l’intention de l’acheteur. Les acheteurs peuvent manquer des produits pertinents et les commerçants peuvent avoir besoin de passer du temps à corriger et à enrichir manuellement le contenu du catalogue.

En outre, les requêtes d’acheteurs sans marque créent de nouvelles opportunités de découverte de produit. Lorsque les acheteurs décrivent leurs besoins sans spécifier de marque, les surfaces d’IA affichent les produits pertinents sur les marques concurrentes en fonction de la manière dont ces produits correspondent à l’intention de l’acheteur. Pour les commerçants, cela crée une occasion d&#39;atteindre de nouveaux clients qui ne connaissent pas nécessairement leur marque, ce qui accroît la visibilité du produit au-delà de la notoriété de la marque existante.

Cependant, il existe des défis liés à la découverte de produits sur les surfaces d’IA, tels que des lacunes dans votre catalogue qui peuvent limiter la découverte de produits assistée par IA.

[!DNL Adobe Commerce] résout ces problèmes d’écart de catalogue en fournissant deux workflows d’enrichissement complémentaires : enrichissement des pages des détails du produit et enrichissement des catalogues. Ces deux enrichissements améliorent la manière dont les agents d’IA accèdent aux produits, les comprennent et les font correspondre au contenu de l’acheteur. Ils sont accessibles dans le menu _Admin_ > **Découverte de produit** de l’IA.

## Les faits relatifs aux produits sont difficiles à accéder et à interpréter.

Les informations sur les produits sont souvent réparties entre les attributs, les variantes, les options, les catégories et d’autres champs du catalogue. Bien que ces informations puissent être disponibles pour les acheteurs sur le storefront, elles ne sont pas toujours accessibles ou faciles à interpréter par les robots d&#39;exploration d’IA. Les détails des produits présentés par le biais de contenu généré dynamiquement, de composants dépendants de JavaScript, d’assistants d’achats interactifs, de pop-ups ou de pages liées peuvent être difficiles à récupérer par les robots d&#39;exploration.

Même lorsque ces informations sont accessibles, elles peuvent ne pas être structurées de manière à ce que les agents d’IA puissent les interpréter de manière fiable. Par conséquent, les agents d’IA peuvent ne pas bien comprendre les fonctionnalités d’un produit, les options disponibles et les capacités de celui-ci, ce qui limite leur capacité à adapter précisément les produits aux besoins des acheteurs.

### Mise à disposition des faits structurés avec l’enrichissement de la page des détails du produit

L’enrichissement PDP crée une payload de données structurée contenant des informations pertinentes sur les produits, notamment les attributs, les variantes, les options, les puces de fonctionnalités, les relations entre les catégories, le prix et la disponibilité. Les agents d’IA disposent ainsi d’une compréhension plus complète et plus structurée des fonctionnalités et des configurations disponibles d’un produit.

Grâce à la technologie [Optimize at Edge](#prerequisites), les informations enrichies sur les produits sont rendues directement accessibles aux robots d&#39;exploration d’IA sans qu’il soit nécessaire de modifier le storefront visible par l’utilisateur. Les commerçants peuvent améliorer la manière dont les informations sur les produits sont présentées aux agents d’IA sans modifier la disposition des storefront, introduire de nouveaux composants destinés aux acheteurs ou nécessiter un développement storefront personnalisé.

Voir [enrichissement de la page des détails du produit](pdp-enrichment.md).

## Le catalogue de produits ne reflète pas l’intention de l’acheteur

Les acheteurs décrivent de plus en plus leurs besoins, problèmes et cas d’utilisation prévus en langage naturel plutôt que de rechercher des noms de produits ou des spécifications techniques spécifiques. Cependant, les noms et descriptions de produits se concentrent souvent sur les attributs techniques sans communiquer clairement les avantages, les cas d’utilisation ou les problèmes réels qu’un produit résout.

Cela crée un écart entre la façon dont les acheteurs expriment leurs besoins et la façon dont les produits sont décrits dans le catalogue. Sans contenu clair du produit axé sur l’acheteur, les agents de l’IA peuvent avoir du mal à interpréter la valeur et la pertinence d’un produit par rapport à l’intention d’un acheteur, risquant d’ignorer les produits appropriés au profit d’alternatives dont les descriptions s’alignent plus clairement sur les besoins de l’acheteur.

### Optimiser le contenu du catalogue de produits avec l’intention de l’acheteur en utilisant l’enrichissement du catalogue

L’enrichissement du catalogue transforme les attributs techniques des produits et les informations de catalogue existantes en noms et descriptions de produits axés sur les acheteurs qui communiquent clairement les avantages, les fonctionnalités et les cas d’utilisation réels d’un produit. Les noms et descriptions des produits sont parmi les sources d’informations les plus influentes utilisées par les surfaces d’IA pour comprendre les fonctionnalités des produits et déterminer leur pertinence par rapport à l’intention de l’acheteur.

En connectant les spécifications techniques des produits aux besoins et problèmes décrits par les acheteurs en langage naturel, l’enrichissement du catalogue aide les agents de l’IA à mieux comprendre la valeur d’un produit, à réduire l’ambiguïté dans l’interprétation de ses fonctionnalités et à faire correspondre plus précisément les produits pertinents au souhait de l’acheteur.

Les commerçants peuvent examiner et approuver les améliorations suggérées avant de les appliquer directement à leur catalogue de produits Adobe Commerce. Cela permet de s’assurer que les vitrines et les canaux de vente alimentés par le catalogue peuvent communiquer de manière cohérente les mêmes informations enrichies et axées sur la valeur aux acheteurs à travers les points de contact.

Voir [Enrichissement du catalogue](catalog-enrichment.md).

#### Règles de gouvernance des marques

Les règles de gouvernance de marque vous permettent de définir les exigences en matière de copie de produit pour l’enrichissement du catalogue, y compris la longueur, les expressions, le ton et la casse. Ces règles s’appliquent uniquement à l’enrichissement du catalogue, et non à l’enrichissement PDP.

Voir [Créer des règles de marque d’enrichissement de catalogue](brand-governance.md).
