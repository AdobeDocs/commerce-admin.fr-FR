---
title: Réécritures d’URL
description: Découvrez les réécritures d’URL et utilisez l’outil de réécriture d’URL de Commerce pour modifier les URL associées à un produit, une catégorie ou une page CMS.
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# Réécritures d’URL

L’outil de réécriture d’URL vous permet de modifier toute URL associée à un produit, une catégorie ou une page CMS. Lorsque la réécriture prend effet, tous les liens renvoyant à l’URL précédente sont redirigés vers la nouvelle adresse.

>[!NOTE]
>
>Pour mettre à jour les réécritures d’URL pour plusieurs produits ou tous les produits simultanément, reportez-vous à [Réécritures d’URL multiples](url-rewrite-product.md#multiple-url-rewrites).

Les termes _réécriture_ et _redirection_ sont souvent utilisés de manière interchangeable, mais font référence à des processus légèrement différents. Une réécriture d’URL modifie la manière dont une URL apparaît dans le navigateur. Une redirection d’URL met à jour l’URL stockée sur le serveur. Une redirection d’URL peut être temporaire ou permanente. Votre boutique utilise des réécritures d’URL et des redirections pour vous permettre de modifier facilement la clé d’URL d’un produit, d’une catégorie ou d’une page et de conserver les liens existants.

Par défaut, les [redirections d’URL automatiques](url-redirect-product-automatic.md) sont activées pour votre boutique et la case à cocher **Créer une redirection permanente pour l’ancienne URL** est sélectionnée sous le champ Clé d’URL de chaque produit.

{{url-rewrite-skip}}

{{url-rewrite-params}}

![Optimisation du moteur de recherche - Créer une redirection URL permanente](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

## URL canoniques

À des fins d’optimisation du moteur de recherche (SEO), il est préférable que chacune de vos pages web ait une seule URL distincte.

Si une seule page est accessible par plusieurs URL ou si vous disposez de pages différentes avec du contenu similaire, Google considère qu’il s’agit de versions en double de la même page. Google choisit une URL comme version canonique et l’analyse. Toutes les autres URL sont considérées comme des URL en double et sont analysées moins souvent.

Si vous n’indiquez pas explicitement à Google quelle URL est canonique, cette dernière fait le choix pour vous ou peut les considérer toutes les deux comme ayant le même poids. Cela peut entraîner un comportement indésirable et risque d’entraîner un budget d’analyse inefficace et des liens rétroactifs mal distribués.

Selon la configuration de votre site web, l’index peut contenir plusieurs versions de votre site, notamment :

    https://www.example.com
    https://www.example.com/
    http://www.example.com
    https://example.com
    https://www.example.com/index.html

Pour spécifier une page canonique, consultez la documentation de Google Search Central [&#128279;](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls).

## Configuration des réécritures d’URL

L’activation des réécritures Apache du serveur web fait partie de la configuration Commerce initiale. Commerce utilise régulièrement les réécritures d’URL pour supprimer le nom de fichier `index.php` qui apparaît normalement dans l’URL juste après le dossier racine. Lorsque les réécritures du serveur web sont activées, le système réécrit chaque URL pour omettre `index.php`. La réécriture supprime les mots qui ne transmettent rien de valeur aux moteurs de recherche ou aux clients et n’a aucun impact sur les performances ou le classement du site.

URL sans réécriture du serveur Web

    http://www.yourdomain.com/magento/index.php/storeview/url-identifier

URL avec réécriture du serveur Web

    http://www.yourdomain.com/magento/storeview/url-identifier

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche où **[!UICONTROL General]** est développé, choisissez **[!UICONTROL Web]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Search Engine Optimization]** .

   ![Configuration générale - Optimisation du moteur de recherche web](../configuration-reference/general/assets/web-search-engine-optimization.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Use Web Server Rewrites]** sur vos préférences.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Créer des réécritures d’URL

Vous pouvez utiliser l’outil de réécriture d’URL pour créer des réécritures de produit et de catégorie, ainsi que des réécritures personnalisées pour n’importe quelle page de votre boutique. Lorsque la réécriture prend effet, tous les liens existants pointant vers l’URL précédente sont redirigés de manière transparente vers la nouvelle adresse.

Les réécritures d’URL peuvent être utilisées pour ajouter des mots-clés à forte valeur ajoutée afin d’améliorer la manière dont le produit est indexé par les moteurs de recherche. Vous pouvez également utiliser des réécritures pour créer des URL supplémentaires en cas de modification saisonnière temporaire ou permanente. Les réécritures peuvent être créées pour n’importe quel chemin d’accès valide, y compris les pages de contenu CMS. En interne, le système référence toujours les produits et les catégories par leur identifiant. Quelle que soit la fréquence de modification de l’URL, l’identifiant reste le même. Voici quelques façons d’utiliser une réécriture d’URL :

URL système

    http://www.example.com/catalog/category/id/6

URL d’origine

    http://www.example.com/peripherals/keyboard.html

URL du produit redirigée

    http://www.example.com/ergonomic-keyboard.html

Autres URL de catégorie

    http://www.example.com/all-on-sale.html
    http://www.example.com/save-now/spring-sale

![L’URL réécrit la grille](./assets/url-rewrites.png){width="700" zoomable="yes"}

Commerce propose les types de réécriture d’URL suivants :

* [Réécritures de produit](url-rewrite-product.md)
* [Réécritures de catégorie](url-rewrite-category.md)
* [Réécritures de page CMS](url-rewrite-cms-page.md)
* [Réécritures personnalisées](url-rewrite-custom.md)

## Démonstration des réécritures d&#39;URL

Regardez cette vidéo pour en savoir plus sur la gestion des réécritures d’URL :

>[!VIDEO](https://video.tv.adobe.com/v/3410124?quality=12&learn=on&captions=fre_fr)
