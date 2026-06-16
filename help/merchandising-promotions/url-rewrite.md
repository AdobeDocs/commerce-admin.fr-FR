---
title: Réécritures d’URL
description: Découvrez les réécritures d’URL et utilisez l’outil de réécriture d’URL de Commerce pour modifier les URL associées à un produit, une catégorie ou une page CMS.
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
TQID: https://experienceleague.adobe.com/fuILlBHCevV6rfQT-PUiuBPBgWkFXDbFofgde8O5BCM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 940
ht-degree: 0%

---

# Réécritures d’URL

>[!TIP]
>
>Pour Adobe Commerce as a Cloud Service, consultez les [directives SEO](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/?lang=fr) de la documentation du Storefront Commerce

L’outil Réécritures d’URL permet de modifier toute URL associée à un produit, une catégorie ou une page CMS. Lorsque vous créez une réécriture d’URL, Commerce crée automatiquement une redirection permanente (301) afin que tous les liens pointant vers l’ancienne URL soient redirigés vers la nouvelle adresse.

>[!NOTE]
>
>Pour mettre à jour les réécritures d’URL pour plusieurs produits ou tous les produits simultanément, reportez-vous à [Réécritures d’URL multiples](url-rewrite-product.md#multiple-url-rewrites).

>[!BEGINSHADEBOX « Comprendre les réécritures et les redirections »]

Les termes _réécriture_ et _redirection_ sont souvent utilisés de manière interchangeable, mais il s’agit de deux opérations différentes :

* **Réécriture d’URL** — Processus côté serveur qui mappe en interne une URL à une autre sans modifier ce qui apparaît dans la barre d’adresse du navigateur. Lorsqu’un visiteur demande une URL, le serveur la traite en tant qu’URL différente en arrière-plan, mais le navigateur continue d’afficher l’URL d’origine.

* **Redirection d&#39;URL** — Envoie une réponse HTTP au navigateur pour lui demander d&#39;accéder à une autre URL. La barre d’adresse du navigateur se met à jour pour afficher la nouvelle URL. Les redirections peuvent être temporaires (302) ou permanentes (301).

>[!ENDSHADEBOX]

## Fonctionnement de l’outil de réécriture

Dans Adobe Commerce, l’outil de réécriture d’URL crée des redirections permanentes (301) par défaut afin de conserver la valeur d’optimisation du moteur de recherche lorsque vous modifiez la clé d’URL d’un produit, d’une catégorie ou d’une page. Ce comportement garantit que les liens existants continuent à fonctionner et que les classements des moteurs de recherche sont conservés.

Par défaut, les [redirections d’URL automatiques](url-redirect-product-automatic.md) sont activées pour votre boutique et la case à cocher **Créer une redirection permanente pour l’ancienne URL** est sélectionnée sous le champ Clé d’URL de chaque produit.

{{url-rewrite-skip}}

![Optimisation du moteur de recherche - Créer une redirection URL permanente](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

{{url-rewrite-params}}

## Démonstration des réécritures d&#39;URL

Regardez la vidéo suivante pour en savoir plus sur la gestion des réécritures d’URL :

>[!VIDEO](https://video.tv.adobe.com/v/3410124?captions=fre_fr&quality=12&learn=on)

## Créer des réécritures d’URL

Utilisez l’outil de réécriture d’URL pour créer des redirections de produits et de catégories, ainsi que des redirections personnalisées pour n’importe quelle page de votre boutique. Lorsque la configuration de réécriture d’URL est appliquée, tous les liens existants pointant vers l’URL précédente sont facilement redirigés vers la nouvelle adresse.

Vous pouvez créer des réécritures d’URL dans :

* Ajoutez des mots-clés de grande valeur pour améliorer la façon dont le produit est indexé par les moteurs de recherche.

* Ajoutez des URL supplémentaires pour un changement saisonnier temporaire ou un changement permanent.

* Ajoutez un chemin d’accès valide pour une page, y compris les pages de contenu CMS. Par exemple, vous pouvez créer une URL pour créer une URL plus conviviale pour l’utilisateur ou l’utilisatrice ou pour l’optimisation du moteur de recherche (SEO) sur un système qui référence toujours les produits et les catégories par leur identifiant interne.

Les réécritures d’URL que vous créez peuvent rediriger vers des catégories existantes ou des pages personnalisées sans modifier la structure de votre site, ce qui facilite la création d’URL mémorisables pour les campagnes marketing.

![L’URL réécrit la grille](./assets/url-rewrites.png){width="700" zoomable="yes"}

Commerce propose les types de réécriture d’URL suivants :

* [Réécritures de produit](url-rewrite-product.md)
* [Réécritures de catégorie](url-rewrite-category.md)
* [Réécritures de page CMS](url-rewrite-cms-page.md)
* [Réécritures personnalisées](url-rewrite-custom.md)

### Cas d’utilisation et exemples

Les réécritures d’URL sont généralement utilisées dans les cas suivants :

#### Modification d’une URL de système interne en URL compatible avec l’optimisation du moteur de recherche

Commerce utilise des URL basées sur des ID en interne, mais vous pouvez créer des URL compatibles avec les moteurs de recherche pour les clients :

**URL système (interne) :**

    

**URL destinée aux clients :**

    

#### Changement d’image de marque du produit ou optimisation des URL

Lorsque vous renommez un produit ou que vous souhaitez améliorer son URL pour l’optimisation du moteur de recherche, créez une redirection pour conserver les liens existants :

**URL d’origine :**

    

**Nouvelle URL optimisée :**

    

L’outil Réécritures crée automatiquement une redirection 301 de l’ancienne URL vers la nouvelle, afin que les clients et les moteurs de recherche soient redirigés de manière transparente vers la bonne page.

#### Pages de destination promotionnelles

Créez des URL personnalisées temporaires ou permanentes pour les campagnes marketing :

**URL promotionnelles :**

    http://www.example.com/all-on-sale.html
    http://www.example.com/save-now/spring-sale

## Configuration supplémentaire de la gestion des URL

Les sections suivantes décrivent comment configurer les réécritures de serveur web et les URL canoniques pour Commerce.

### Configurer les réécritures du serveur web

>[!NOTE]
>
>Cette section décrit la réécriture d’URL au niveau du serveur web, qui est différente de la fonctionnalité de l’outil de réécriture d’URL. Les réécritures de serveur web gèrent le formatage technique des URL (comme la suppression de `index.php`), tandis que l’outil de réécriture d’URL gère les redirections pour les modifications de contenu.

L’activation des réécritures du serveur web fait partie de la configuration Commerce initiale et est généralement configurée lors de l’installation. Lorsqu’il est activé, le serveur web (Apache ou Nginx) supprime automatiquement le nom de fichier `index.php` des URL, créant des adresses plus propres et plus compatibles avec l’optimisation du moteur de recherche (SEO).
L’exemple suivant montre comment les URL apparaissent avec et sans les réécritures du serveur web activées :

**URL sans réécriture du serveur Web**

    

**URL avec réécriture du serveur Web**

    

#### Activez ou désactivez les réécritures du serveur Web :

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche où **[!UICONTROL General]** est développé, choisissez **[!UICONTROL Web]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Search Engine Optimization]** .

   ![Configuration générale - Optimisation du moteur de recherche web](../configuration-reference/general/assets/web-search-engine-optimization.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Use Web Server Rewrites]** sur vos préférences.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

### Spécifier des URL canoniques

À des fins d’optimisation du moteur de recherche (SEO), chacune de vos pages web ne doit avoir qu’une seule URL distincte.

Si une seule page est accessible par plusieurs URL ou si vous disposez de pages différentes avec du contenu similaire, Google considère qu’il s’agit de versions en double de la même page. Google choisit une URL comme version canonique et l’explore. Toutes les autres URL sont considérées comme des URL en double et sont moins souvent explorées.

Si vous n’indiquez pas explicitement à Google quelle URL est canonique, cette dernière fait le choix pour vous ou peut les considérer toutes les deux comme ayant le même poids. Cela peut entraîner un comportement indésirable et risque d’entraîner un budget d’explore inefficace et de faibles backlinks distribués.

Selon la configuration de votre site web, l’index peut contenir plusieurs versions de votre site, par exemple :

    https://www.example.com
    https://www.example.com/
    http://www.example.com
    https://example.com
    https://www.example.com/index.html

Pour spécifier une page canonique, consultez la documentation de Google Search Central [&#128279;](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls).
