---
title: URL rewrites
description: Découvrez les réécritures d’URL et l’utilisation de l’outil de réécriture d’URL de Commerce pour modifier les URL associées à un produit, à une catégorie ou à une page CMS.
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---

# URL rewrites

L’outil de réécriture d’URL vous permet de modifier toute URL associée à un produit, une catégorie ou une page CMS. Lorsque la réécriture prend effet, tous les liens pointant vers l’URL précédente sont redirigés vers la nouvelle adresse.

>[!NOTE]
>
>Pour mettre à jour les réécritures d’URL pour plusieurs ou tous les produits simultanément, reportez-vous à la section [Plusieurs réécritures d’URL](url-rewrite-product.md#multiple-url-rewrites).

Les termes _rewrite_ et _rediriger_ sont souvent interchangeables, mais font référence à des processus légèrement différents. Une réécriture d’URL modifie la manière dont une URL apparaît dans le navigateur. Une redirection d’URL met à jour l’URL stockée sur le serveur. Une redirection d’URL peut être temporaire ou permanente. Votre boutique utilise des réécritures et des redirections d’URL pour vous permettre de modifier facilement la clé d’URL d’un produit, d’une catégorie ou d’une page et de conserver les liens existants.

Par défaut, [redirections d’URL automatiques](url-redirect-product-automatic.md) sont activés pour votre boutique et la variable **Créer une redirection permanente pour l’ancienne URL** est cochée sous le champ Clé URL de chaque produit.

{{url-rewrite-skip}}

{{url-rewrite-params}}

![Optimisation du moteur de recherche - Création d’une redirection d’URL permanente](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

## URL canoniques

À des fins d’optimisation pour les moteurs de recherche, il est judicieux que chacune de vos pages web ne comporte qu’une seule URL distincte.

Si vous disposez d’une seule page accessible par plusieurs URL ou différentes pages avec un contenu similaire, Google la considère comme des versions dupliquées de la même page. Google choisit une URL comme version canonique et analyse celle-ci, et toutes les autres URL sont considérées comme des URL en double et sont analysées moins souvent.

Si vous n’indiquez pas explicitement à Google quelle URL est canonique, cela vous donne le choix, ou vous pouvez les considérer tous les deux de même poids. Cela pourrait conduire à des comportements indésirables et courir le risque d&#39;un budget d&#39;analyse inefficace et de liens de redirection peu efficaces.

Selon la configuration de votre site web, il peut y avoir plusieurs versions de votre site dans l’index, notamment :

    https://www.example.com
    https://www.example.com/
    http://www.example.com
    https://example.com
    https://www.example.com/index.html

Pour définir une page canonique, voir [Documentation de Google Search Central](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls).

## Configuration des réécritures d’URL

L’activation du serveur web Apache Rewrites fait partie de la configuration initiale de Commerce. Commerce utilise régulièrement des réécritures d’URL pour supprimer le nom de fichier. `index.php` qui s’affiche normalement dans l’URL juste après le dossier racine. Lorsque Web Server Rewrites est activé, le système réécrit chaque URL à omettre. `index.php`. La réécriture supprime les mots qui n’ont aucune valeur pour les moteurs de recherche ou les clients et n’ont aucune incidence sur les performances ou le classement du site.

URL sans réécriture de serveur web

    http://www.yourdomain.com/magento/index.php/storeview/url-identifier

URL avec réécriture du serveur web

    http://www.yourdomain.com/magento/storeview/url-identifier

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche où **[!UICONTROL General]** est développé, choisissez **[!UICONTROL Web]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Search Engine Optimization]** .

   ![Configuration générale - optimisation du moteur de recherche web](../configuration-reference/general/assets/web-search-engine-optimization.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Use Web Server Rewrites]** selon vos préférences.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

## Créer des réécritures d’URL

Vous pouvez utiliser l’outil de réécriture d’URL pour créer des réécritures de produit et de catégorie, ainsi que des réécritures personnalisées pour n’importe quelle page de votre magasin. Lorsque la réécriture prend effet, tout lien existant pointant vers l’URL précédente est facilement redirigé vers la nouvelle adresse.

Les réécritures d’URL peuvent être utilisées pour ajouter des mots-clés à forte valeur ajoutée afin d’améliorer la façon dont le produit est indexé par les moteurs de recherche. Vous pouvez également utiliser des réécritures pour créer des URL supplémentaires pour une modification saisonnière temporaire ou définitive. Les réécritures peuvent être créées pour n’importe quel chemin valide, y compris les pages de contenu CMS. En interne, le système référence toujours les produits et les catégories selon leur identifiant. Quelle que soit la fréquence à laquelle l’URL change, l’ID reste le même. Vous pouvez utiliser une réécriture d’URL de plusieurs façons :

URL système

    http://www.example.com/catalog/category/id/6

URL d’origine

    http://www.example.com/peripherals/keyboard.html

URL du produit redirigé

    http://www.example.com/ergonomic-keyboard.html

URL de catégorie supplémentaires

    http://www.example.com/all-on-sale.html
    http://www.example.com/save-now/spring-sale

![URL réécrit la grille](./assets/url-rewrites.png){width="700" zoomable="yes"}

Commerce propose les types de réécriture d’URL suivants :

* [Réécritures de produit](url-rewrite-product.md)
* [Réécritures de catégorie](url-rewrite-category.md)
* [Réécritures de page CMS](url-rewrite-cms-page.md)
* [Réécritures personnalisées](url-rewrite-custom.md)

## Démo de réécriture d’URL

Regardez cette vidéo pour en savoir plus sur la gestion des réécritures d’URL :

>[!VIDEO](https://video.tv.adobe.com/v/343751?quality=12&learn=on)
