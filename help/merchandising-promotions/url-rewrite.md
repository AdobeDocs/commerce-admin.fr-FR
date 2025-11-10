---
title: Réécritures d’URL
description: Découvrez les réécritures d’URL et utilisez l’outil de réécriture d’URL de Commerce pour modifier les URL associées à un produit, une catégorie ou une page CMS.
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 2f2db4926ff92adfa27692eeca872c1765fd31d6
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# Réécritures d’URL

>[!TIP]
>
>Pour Adobe Commerce as a Cloud Service, consultez les [directives SEO](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/) de la documentation du Storefront Commerce

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

>[!VIDEO](https://video.tv.adobe.com/v/343751?quality=12&learn=on)

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

    http://www.example.com/catalog/category/id/6

**URL destinée aux clients :**

    http://www.example.com/peripherals/keyboard.html

#### Changement d’image de marque du produit ou optimisation des URL

Lorsque vous renommez un produit ou que vous souhaitez améliorer son URL pour l’optimisation du moteur de recherche, créez une redirection pour conserver les liens existants :

**URL d’origine :**

    http://www.example.com/peripherals/keyboard.html

**Nouvelle URL optimisée :**

    http://www.example.com/ergonomic-keyboard.html

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

    http://www.yourdomain.com/magento/index.php/storeview/url-identifier

**URL avec réécriture du serveur Web**

    http://www.yourdomain.com/magento/storeview/url-identifier

#### Activez ou désactivez les réécritures du serveur Web :

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche où **[!UICONTROL General]** est développé, choisissez **[!UICONTROL Web]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Search Engine Optimization]** .

   ![Configuration générale - Optimisation du moteur de recherche web](../configuration-reference/general/assets/web-search-engine-optimization.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Use Web Server Rewrites]** sur vos préférences.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

### Spécifier des URL canoniques

À des fins d’optimisation du moteur de recherche (SEO), chacune de vos pages web ne doit avoir qu’une seule URL distincte.

Si une seule page est accessible par plusieurs URL ou si vous disposez de pages différentes avec du contenu similaire, Google considère qu’il s’agit de versions en double de la même page. Google choisit une URL comme version canonique et l’analyse, de même que toutes les autres URL, sont considérées comme des URL en double et sont analysées moins souvent.

Si vous n’indiquez pas explicitement à Google quelle URL est canonique, cette dernière fait le choix pour vous ou peut les considérer toutes les deux comme ayant le même poids. Cela peut entraîner un comportement indésirable et risque d’entraîner un budget d’analyse inefficace et des backlinks distribués faibles.

Selon la configuration de votre site web, l’index peut contenir plusieurs versions de votre site, par exemple :

    https://www.example.com
    https://www.example.com/
    http://www.example.com
    https://example.com
    https://www.example.com/index.html

Pour spécifier une page canonique, consultez la documentation de Google Search Central [&#128279;](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls).
