---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Catalog]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Catalog] &gt; [!UICONTROL Catalog] de l’administrateur Commerce.
exl-id: fc25ae80-aaa7-42c4-bba2-f03d3caa7970
feature: Configuration, Catalog Management
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '3233'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Catalog]

{{config}}

## [!UICONTROL Product Fields Auto-Generation]

![Génération automatique des champs de produit](./assets/catalog-product-fields-auto-generation.png)<!-- zoom -->

<!-- [Product Fields Auto-Generation](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/product-workspace#default-field-values) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Mask for SKU] | Global | Détermine la valeur par défaut du champ SKU en fonction des valeurs d’espace réservé provenant d’autres champs et de tout texte supplémentaire saisi. Espace réservé par défaut : <br/>Nom du produit - `{{name}}` |
| [!UICONTROL Mask for Meta Title] | Global | Détermine la valeur par défaut du champ Meta Title en fonction des valeurs d’espace réservé provenant d’autres champs et de tout texte supplémentaire saisi. Espace réservé par défaut : <br/>Nom du produit - `{{name}}` |
| [!UICONTROL Mask for Meta Keywords] | Global | Détermine la valeur par défaut du champ _Meta Keywords_ en fonction des valeurs d’espace réservé provenant d’autres champs et de tout texte supplémentaire saisi. Espace réservé par défaut : <br/>Nom du produit - `{{name}}` |
| [!UICONTROL Mask for Meta Description] | Global | Détermine la valeur par défaut du champ Meta-Description en fonction des valeurs d’espace réservé provenant d’autres champs et de tout texte supplémentaire saisi. Espace réservé par défaut : <br/>Nom du produit - `{{name}}` <br/>Description - `{{description}}` |

{style="table-layout:auto"}

## [!UICONTROL Product Reviews]

![Révisions de produits](./assets/catalog-product-reviews.png)<!-- zoom -->

<!-- [Product Reviews](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/product-reviews/product-reviews) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Affichage en magasin | Permet la consultation de produits. Options : `Yes` / `No` |
| [!UICONTROL Allow Guests to Write Reviews] | Site Web | Détermine si les clients doivent ouvrir un compte avec votre boutique pour pouvoir écrire des révisions de produit. |

{style="table-layout:auto"}

## [!UICONTROL Storefront]

![Storefront](./assets/catalog-storefront.png)<!-- zoom -->

<!-- [Storefront](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/catalog/navigation/navigation-product-listings) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL List Mode] | Affichage en magasin | Détermine le format de la liste des résultats de recherche. Options : <br/>**`Grid Only`**- Formate la liste en tant que grille de lignes et de colonnes. Chaque produit apparaît dans une seule cellule de la grille.<br/>**`List Only`** - Formate la liste avec chaque produit sur une ligne distincte. <br/>**`Grid (default / List)`**- Par défaut, les produits apparaissent en mode Grille et peuvent être basculés en mode Liste.<br/>**`List (default / Grid)`** - Par défaut, les produits apparaissent en mode Liste et peuvent être basculés en mode Grille. |
| [!UICONTROL Products per Page on Grid Allowed Values] | Affichage en magasin | Détermine le nombre de produits affichés en mode Grille. Pour sélectionner plusieurs options, saisissez plusieurs valeurs séparées par des virgules. |
| [!UICONTROL Products per Page on Grid Default Value] | Affichage en magasin | Détermine le nombre de produits affichés par page par défaut en mode Grille. |
| [!UICONTROL Products per Page on List Allowed Values] | Affichage en magasin | Détermine le nombre de produits affichés en mode Liste. Pour sélectionner plusieurs options, saisissez plusieurs valeurs séparées par des virgules. |
| [!UICONTROL Products per Page on List Default Value] | Affichage en magasin | Détermine le nombre de produits affichés par page, en mode Liste, par défaut. |
| Tri par liste de produits | Affichage en magasin | Détermine l’ordre de tri de la liste des résultats de la recherche. La sélection des options est déterminée par les paramètres d’affichage de la catégorie et les attributs disponibles définis sur `Used for Sorting in Product Listing`. La valeur par défaut est `Use All Available Attributes` et inclut généralement la meilleure valeur, le nom, le prix. Ce paramètre ne s’applique pas au [!DNL Live Search] [ ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling) Widget de page de liste de produits. |
| [!UICONTROL Allow All Products per Page] | Affichage en magasin | Si celle-ci est définie sur `Yes`, l’option `ALL` est incluse dans le contrôle &quot;Afficher par page&quot;. |
| [!UICONTROL Remember Category Pagination] | Global | Si celle-ci est définie sur `Yes`, les valeurs de pagination de catégorie actuelles sont enregistrées lorsque les clients naviguent d’une catégorie à une autre dans les [listes de produits](../../catalog/navigation-product-listings.md). L’enregistrement de la valeur utilise davantage de stockage du cache et peut affecter la manière dont les pages sont indexées par les moteurs de recherche. Options : `Yes` / `No` (par défaut) |
| [!UICONTROL Use Flat Catalog Category] | Global | Active la [structure de catégorie plate](../../catalog/catalog-flat.md) (non recommandée). Options : `Yes` / `No` |
| [!UICONTROL Use Flat Catalog Product] | Global | Active la structure de produit plate. (non recommandé) Options : `Yes` / `No` |
| [!UICONTROL Swatches per Product] | Affichage en magasin | Détermine le nombre d’échantillons disponibles pour chaque produit. Valeur par défaut : `16` |
| [!UICONTROL Show Swatches in Product List] | Affichage en magasin | Détermine si les échantillons apparaissent dans la liste de produits. Options : `Yes` / `No` |
| [!UICONTROL Show Swatch Tooltip] | Affichage en magasin | Détermine si l’info-bulle d’échantillon s’affiche. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Product Alerts]

![Alertes produit](./assets/catalog-product-alerts.png)<!-- zoom -->

<!-- [Product Alerts](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/product-alerts/alert-setup) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Allow Alerts When Product Price Changes] | Affichage en magasin | Détermine si des alertes par e-mail sont disponibles pour les changements de prix du produit. Options : `Yes` / `No` |
| [!UICONTROL Price Alert Email Template] | Affichage en magasin | Identifie le modèle utilisé pour les alertes par e-mail de changement de prix de produit. Modèle par défaut : `Product price alert` |
| [!UICONTROL Allow Alert When Product Comes Back in Stock] | Site Web | Détermine si les clients peuvent choisir de recevoir une alerte lorsque le produit revient en stock. Options : `Yes` / `No` |
| [!UICONTROL Stock Alert Email Template] | Affichage en magasin | Identifie le modèle utilisé pour les notifications par e-mail d’alerte de stock. Modèle par défaut : `Product stock alert` |
| [!UICONTROL Alert Email Sender] | Affichage en magasin | Détermine le contact de magasin qui apparaît comme expéditeur du message d’alerte du produit. Options : `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email` |

{style="table-layout:auto"}

## [!UICONTROL Product Alerts Run Settings]

![Paramètres d’exécution des alertes de produit](./assets/catalog-product-alerts-run-settings.png)<!-- zoom -->

<!-- [Product Alerts Run Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/product-alerts/alert-setup) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Frequency] | Global | Sélectionnez la fréquence d’envoi des alertes de produit. Options : `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Start Time] | Global | Sélectionnez l’heure de début du processus d’alerte du produit. Cette fois doit être effectuée après toute mise à jour de prix ou d’inventaire. |
| [!UICONTROL Error Email Recipient] | Global | Identifiez l’adresse électronique de la personne (normalement un administrateur de magasin) qui doit recevoir une notification par e-mail lorsqu’une erreur se produit dans le processus d’alerte du produit. |
| [!UICONTROL Error Email Sender] | Global | Sélectionnez le rôle `from` de l’email. |
| [!UICONTROL Error Email Template] | Global | Sélectionnez le modèle de courrier électronique à utiliser pour les notifications d’erreur d’alerte de produit. |

{style="table-layout:auto"}

## [!UICONTROL Product Image Placeholders]

![Espace réservé de l’image du produit](./assets/catalog-product-image-placeholders.png)<!-- zoom -->

<!-- [Product Image Placeholders](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/digital-assets/product-image-config#image-placeholders) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Base Image] | Affichage en magasin | Identifie le fichier d’espace réservé choisi pour l’image de base. |
| [!UICONTROL Small Image] | Affichage en magasin | Identifie le fichier d’espace réservé choisi pour la petite image. |
| [!UICONTROL Swatch] | Affichage en magasin | Identifie le fichier d’espace réservé choisi pour l’échantillon. |
| [!UICONTROL Thumbnail] | Affichage en magasin | Identifie le fichier d’espace réservé choisi pour la miniature. |
| [!UICONTROL Choose File] |  | Accède au fichier et le télécharge en tant qu’image d’espace réservé pour le type . |

{style="table-layout:auto"}

## [!UICONTROL Recently Viewed/Compared Products]

![Produits récemment consultés/comparés](./assets/catalog-recently-viewed-and-compared-products.png)<!-- zoom -->

<!-- Recently Viewed/Compared Products](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/shopper-tools/products-viewed-compared) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Synchronize widget products with backend storage] | Global | Détermine la synchronisation des informations du widget de produit, telles que l’ID du produit, avec la base de données. Cela permet de réutiliser les informations sur d’autres périphériques. |
| [!UICONTROL Show for Current] | Site Web | Limite les produits affichés au site web actuel. Options : `Website` / `Store` / `Store View` |
| [!UICONTROL Default Recently Viewed Products Count] | Affichage en magasin | Détermine le nombre maximal de produits récemment consultés qui apparaissent dans la liste. |
| [!UICONTROL Default Recently Compared Products Count] | Affichage en magasin | Détermine le nombre maximal de produits récemment comparés qui apparaissent dans la liste. |
| [!UICONTROL Lifetime of products in Recently Viewed Widget] | Global | Détermine la durée, en secondes, pendant laquelle les produits consultés s’affichent dans la liste récemment affichée. |
| [!UICONTROL Lifetime of products in Recently Compared Widget] | Global | Détermine la durée, en secondes, d’affichage des produits comparés dans la liste récemment comparée. |

{style="table-layout:auto"}

## [!UICONTROL Product Video]

![Vidéos produit](./assets/catalog-product-video.png)<!-- zoom -->

<!-- [Product Videos](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/digital-assets/product-video) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL YouTube API key] | Affichage en magasin | Indique la clé d’API requise pour la connexion au serveur YouTube. |
| [!UICONTROL Autostart base video] | Affichage en magasin | Pour démarrer automatiquement la vidéo après le chargement de la page, définissez sur `Yes`. |
| [!UICONTROL Show related video] | Affichage en magasin | Pour afficher les vidéos connexes, définissez sur `Yes`. |
| [!UICONTROL Auto restart video] | Affichage en magasin | Pour activer la relecture automatique de la vidéo, définissez sur `Yes`. |

{style="table-layout:auto"}

## [!UICONTROL Price]

![Price](./assets/catalog-price.png)<!-- zoom -->

<!--Price](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/pricing/catalog-price-scope) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Catalog Price Scope] | Global | Détermine la portée de la devise de base. Options : `Global` / `Website` |
| [!UICONTROL Default Product Price] | Global | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Définit le prix par défaut du produit, le cas échéant. |

{style="table-layout:auto"}

## [!UICONTROL Layered Navigation]

>[!NOTE]
>
>La configuration de recherche standard décrite dans cette section diffère pour [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

<!-- [Layered Navigation - Automatic (equalize price ranges)](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/catalog/navigation/navigation-layered#configure-layered-navigation) -->

![Navigation par couches - Automatique (égaliser les plages de prix)](./assets/layered-navigation-equalize-price-range.png)<!-- zoom -->

![Navigation par couches - Automatique (égaliser le nombre de produits)](./assets/layered-navigation-equalize-product-counts.png)<!-- zoom -->

![Navigation par couches - Manuel](./assets/layered-navigation-manual.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Display Product Count] | Affichage en magasin | Détermine si le nombre de produits apparaît après chaque attribut, plage de prix et catégorie. Options : `Yes` / `No` |
| [!UICONTROL Price Navigation Step Calculation] | Affichage en magasin | Détermine la méthode utilisée pour déterminer l’ [étape de navigation par prix](../../catalog/navigation-layered.md#configure-price-navigation)). Options : <br/>`Automatic (equalize price ranges)` - Base le calcul sur la plage de prix des produits du groupe. <br/>`Automatic (equalize product counts)` - Base le calcul sur le nombre de produits du groupe. Établit un seuil pour le nombre minimum de produits dans le groupe, afin de les empêcher d’être divisés en groupes plus petits. <br/>`Manual` - Utilise la limite de division que vous saisissez pour les intervalles de prix. |
| [!UICONTROL Default Price Navigation Step] | Affichage en magasin | Détermine le nombre de produits inclus dans chaque étape. |
| [!UICONTROL Maximum Number of Price Intervals] | Affichage en magasin | Définit une limite pour le nombre d’intervalles de prix qui apparaissent dans la navigation par couches. |

{style="table-layout:auto"}

## [!UICONTROL Category Permissions]

{{ee-feature}}

![Autorisations de catégorie](./assets/catalog-category-permissions.png)<!-- zoom -->

<!-- [Category Permissions](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/categories/category-permissions) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable] | Global | Active les restrictions de catégorie. Par défaut, l’utilisation de cette fonctionnalité limite toutes les catégories. Options : `Yes` / `No` |
| [!UICONTROL Allow Browsing Category] | Site Web | Détermine qui est autorisé à parcourir les catégories. Options : <br/>`Yes, for Everyone` - Permet à tous les visiteurs et clients de parcourir la catégorie. <br/>`Yes, for Specified Customer Groups` - Permet uniquement aux membres des groupes de clients sélectionnés de parcourir la catégorie. <br/>`No, Redirect to Landing Page` : refuse l’accès à la catégorie et la redirige vers la page sélectionnée. |
| [!UICONTROL Display Product Prices] | Site Web | Contrôle l’affichage des prix des produits pour la catégorie. Options : <br/>`Yes, for Everyone` - Permet à tous de voir le prix des produits de la catégorie. <br/>`Yes, for Specified Customer Groups` - Permet uniquement aux membres de groupes de clients sélectionnés de voir le prix des produits de la catégorie. <br/>`No` - Désactive l’affichage des prix des produits pour la catégorie. |
| [!UICONTROL Allow Adding to Cart] | Site Web | Détermine qui peut acheter des produits de la catégorie. Options : <br/>`Yes, for Everyone` - Permet à tous de placer des produits de la catégorie dans leur panier. <br/>`Yes, for Specified Customer Groups` - Permet uniquement aux membres des groupes de clients sélectionnés de placer des produits de la catégorie dans leur panier. <br/>`No` - Ne permet à personne de placer des produits de la catégorie dans son panier. |
| [!UICONTROL Disallow Catalog Search by] | Site Web | Identifie les groupes de clients qui ne sont pas autorisés à rechercher des produits dans la catégorie. |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Optimization]

![Optimisation du moteur de recherche](./assets/catalog-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/settings/product-search-engine-optimization) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Popular Search Terms] | Affichage en magasin | Détermine si les _termes de recherche populaires_ sont implémentés dans le magasin. Ce paramètre ne s’applique pas aux magasins qui utilisent [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html). Options : `Enable` / `Disable` |
| [!UICONTROL Product URL Suffix] | Affichage en magasin | Détermine si un suffixe, tel que html ou htm, est appliqué aux URL de produit. En cas d’utilisation, n’insérez pas de point avant le suffixe, car celui-ci est appliqué automatiquement. |
| [!UICONTROL Category URL Suffix] | Affichage en magasin | Détermine si un suffixe, tel que html ou htm, est appliqué aux URL de catégorie. En cas d’utilisation, n’insérez pas de point avant le suffixe, car celui-ci est appliqué automatiquement. |
| [!UICONTROL Use Categories Path for Product URLs] | Affichage en magasin | Détermine si les chemins de catégorie sont inclus dans les URL de produit. Ce faisant, plusieurs URL peuvent pointer vers la même page, ce qui peut avoir une incidence sur le classement de recherche. Pour en savoir plus, voir [Méta canonique ](../../merchandising-promotions/meta-data.md#canonical-meta-tag). |
| [!UICONTROL Create Permanent Redirect for URLs if URL Key Changed] | Affichage en magasin | Détermine si une redirection permanente est créée automatiquement chaque fois qu’une clé d’URL change. Lorsqu’elle est implémentée, la case à cocher Créer une redirection personnalisée pour l’ancienne URL située sous le champ Clé URL du produit est sélectionnée par défaut. Options : `Yes` / `No` |
| [!UICONTROL Generate "category/product" URL Rewrites] | Global | Détermine si Adobe Commerce génère des données et les enregistre dans les tableaux de réécriture lorsqu’un utilisateur enregistre une catégorie contenant de nombreux produits attribués. Options : `Yes` / `No` <br/><br/>**_Important :_**L’enregistrement de ces données générées dans une table de réécritures d’URL peut dégrader les performances. Pour plus d’informations, voir [Redirections automatiques des produits](../../merchandising-promotions/url-redirect-product-automatic.md) . |
| [!UICONTROL Apply transliteration for product URL] | Affichage en magasin | Détermine si la translittération est appliquée lors de la création ou de la mise à jour des URL de produit. Options : `Yes` / `No`. La valeur par défaut est `Yes`. <br/><br/>Pour certains cas d’utilisation, désactivez la translittération. Par exemple, si vous gérez une boutique en ligne en chinois, les bonnes pratiques d’optimisation pour les moteurs de recherche recommandent que les URL de produit correspondent au nom du produit. La définition de l’option sur `No` permet d’utiliser des caractères chinois dans les URL de produit au lieu d’un équivalent ASCII. |
| [!UICONTROL Page Title Separator] | Affichage en magasin | Identifie le caractère qui sépare le nom de la catégorie et la sous-catégorie dans la barre de titre du navigateur. |
| [!UICONTROL Use Canonical Link Meta Tag for Categories] | Affichage en magasin | Si plusieurs URL pointent vers la même page de catégorie, cette option utilise une méta-balise canonique pour identifier l’URL de catégorie que les moteurs de recherche doivent indexer. L’URL contient un nom complet pour la catégorie à l’aide de la balise meta . Cela réduit la duplication du contenu et améliore l’optimisation du moteur de recherche. Options : `Yes` / `No` |
| [!UICONTROL Use Canonical Link Meta Tag for Products] | Affichage en magasin | Si plusieurs URL pointent vers la même page de produit, cette option utilise une méta-balise canonique pour identifier l’URL de produit que les moteurs de recherche doivent indexer. L’URL inclut un nom complet du produit à l’aide de la balise meta . Cela réduit la duplication du contenu et améliore l’optimisation du moteur de recherche. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Category Top Navigation]

![Navigation supérieure des catégories](./assets/catalog-category-top-navigation.png)<!-- zoom -->

<!-- Category Top Navigation](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/catalog/navigation/navigation-top) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Maximal Depth] | Global | Détermine le nombre de niveaux de sous-catégorie dans la navigation supérieure. La valeur par défaut `0` ne limite pas le nombre de niveaux. |

{style="table-layout:auto"}

## [!UICONTROL Catalog Search]

Vous pouvez configurer la recherche catalogue à l’aide de [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) ou de services de moteur de recherche tiers pris en charge par Adobe Commerce. Suivez les instructions de votre installation.

### Adobe Commerce avec [!DNL Live Search]

Lorsque la recherche en direct est installée, la recherche catalogue inclut les paramètres de configuration suivants :

![Recherche catalogue pour la recherche en direct](./assets/catalog-search-live-search.png)<!-- zoom -->

<!-- [Catalog Search for Live Search](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/catalog/search/search-configuration) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Minimal Query Length] | Affichage en magasin | Nombre minimum de caractères autorisés dans une recherche catalogue. Les valeurs définies pour cette option doivent être compatibles avec la plage correspondante définie dans les configurations de votre moteur de recherche Elasticsearch. Par exemple, si vous définissez cette valeur sur `2` dans Adobe Commerce, mettez à jour la valeur dans votre moteur de recherche. |
| [!UICONTROL Maximum Query Length] | Affichage en magasin | Nombre maximal de caractères autorisés dans une recherche catalogue. Les valeurs définies pour cette option doivent être compatibles avec la plage correspondante définie dans les configurations de votre moteur de recherche Elasticsearch. Par exemple, si vous définissez cette valeur sur 300 dans Adobe Commerce, mettez à jour la valeur dans votre moteur de recherche. |
| [!UICONTROL Number of top search results to cache] | Affichage en magasin | Nombre de termes de recherche et de résultats courants à mettre en cache pour des réponses plus rapides. La saisie d’une valeur de `0` met en cache tous les termes et résultats de la recherche une seconde fois. Valeur par défaut : `100` |
| [!UICONTROL Autocomplete Limit] | Affichage en magasin | Détermine le nombre maximal de lignes disponibles dans la page [storefront popover]. La valeur par défaut peut être modifiée lors de l’installation de Live Search et mise à jour ultérieurement en modifiant ce paramètre de configuration. Valeur par défaut : `8` |

{style="table-layout:auto"}

### Moteurs de recherche tiers

Adobe Commerce prend en charge OpenSearch et Elasticsearch. Les versions 2.3.7-p3, 2.4.3-p2 et 2.4.4 et ultérieures d’Adobe Commerce prennent en charge le service OpenSearch. Elasticsearch 7.11 et versions ultérieures ne sont pas pris en charge sur Adobe Commerce dans les projets d’infrastructure cloud. Elasticsearch est toujours pris en charge pour les installations sur site.

>[!IMPORTANT]
>
>- En raison de l’annonce de fin de prise en charge de 7 Elasticsearch pour août 2023, Adobe recommande à tous les clients Adobe Commerce de migrer vers le moteur de recherche OpenSearch 2.x. Pour plus d’informations sur la migration de votre moteur de recherche lors d’une mise à niveau, voir [Migration vers OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) dans le _Guide de mise à niveau_.
>- Dans les versions 2.4.4 et 2.4.3-p2, tous les champs intitulés Elasticsearch s’appliquent également à OpenSearch. Lorsque la prise en charge d’Elasticsearch 8.x a été introduite dans la version 2.4.6, de nouveaux libellés ont été créés pour faire la distinction entre les configurations Elasticsearch et OpenSearch. Toutefois, les options de configuration pour les deux sont identiques.

![Options de configuration de la recherche catalogue](./assets/catalog-search-opensearch.png){zoomable="yes"}

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Minimal Query Length] | Affichage en magasin | Nombre minimum de caractères autorisés dans une recherche catalogue. La valeur définie pour cette option doit être compatible avec la plage correspondante définie dans votre configuration OpenSearch ou Elasticsearch. Par exemple, si vous définissez cette valeur sur `2` dans Adobe Commerce, vous devez également mettre à jour la valeur dans la configuration de votre moteur de recherche. Valeur par défaut : `3` |
| [!UICONTROL Maximum Query Length] | Affichage en magasin | Nombre maximal de caractères autorisés dans une recherche catalogue. La valeur définie pour cette option doit être compatible avec la plage correspondante définie dans votre configuration OpenSearch ou Elasticsearch. Par exemple, si vous définissez cette valeur sur `300` dans Adobe Commerce, vous devez mettre à jour la valeur dans la configuration de votre moteur de recherche. Valeur par défaut : `128` |
| [!UICONTROL Number of top search results to cache] | Affichage en magasin | Nombre de termes de recherche et de résultats courants à mettre en cache pour des réponses plus rapides. La saisie d’une valeur de `0` met en cache tous les termes et résultats de la recherche une seconde fois. Valeur par défaut : `100` |
| [!UICONTROL Enable EAV Indexer] | Global | Détermine s’il faut activer ou désactiver l’indexeur EAV de produit. Cette fonctionnalité améliore la vitesse d’indexation et limite l’indexeur de l’utilisation par des extensions tierces. Option par défaut : `Yes` pour activée |
| [!UICONTROL Autocomplete Limit] | Affichage en magasin | Nombre maximal de requêtes de recherche à afficher sous le champ de recherche pour la saisie automatique de la recherche. La limitation de ce montant augmente les performances des recherches et réduit la taille de la liste affichée. Valeur par défaut : `8` |
| Moteur de recherche | Global | Identifie le moteur de recherche requis pour traiter les demandes de données de catalogue. Les options de configuration du moteur de recherche sont les mêmes pour OpenSearch et Elasticsearch. Options : `OpenSearch` ou `Elasticsearch` |
| [!UICONTROL OpenSearch Server Hostname] | Global | Spécifie le nom du serveur hôte OpenSearch ou Elasticsearch. |
| [!UICONTROL OpenSearch Server Port] | Global | Indique le numéro de port du serveur utilisé par OpenSearch ou Elasticsearch. Valeur par défaut : `9200` |
| [!UICONTROL OpenSearch Index Prefix] | Global | Attribue un préfixe pour identifier l’index OpenSearch ou Elasticsearch. Valeur par défaut : `magento2` |
| [!UICONTROL Enable OpenSearch HTTP Auth] | Global | S’il est activé, utilise l’authentification HTTP pour demander un nom d’utilisateur et un mot de passe avant d’accéder au serveur OpenSearch ou Elasticsearch. Options : `Yes` / `No` |
| [!UICONTROL OpenSearch HTTP Username] | Global | Lorsque l’option _Activer l’authentification HTTP Elasticsearch_ est définie sur `Yes`, spécifie le nom d’utilisateur pour l’authentification HTTP OpenSearch ou Elasticsearch. |
| [!UICONTROL OpenSearch HTTP Password] | Global | Lorsque l’option _Activer l’authentification HTTP Elasticsearch_ est définie sur `Yes`, indique le mot de passe de l’authentification HTTP OpenSearch ou Elasticsearch. |
| [!UICONTROL OpenSearch Server Timeout] | Global | Détermine le nombre de secondes avant l’expiration d’une requête au serveur OpenSearch ou Elasticsearch. Valeur par défaut : `15` |
| [!UICONTROL Test Connection] |  | Valide la connexion OpenSearch ou Elasticsearch. |
| [!UICONTROL Enable Search Recommendations] | Affichage en magasin | Détermine si des recommandations de recherche sont proposées lorsqu’une recherche ne renvoie aucun résultat et apparaissent sous la section `Related search terms` de la page des résultats de recherche. Options : `Yes` / `No` <br/> Lorsque cette option est définie sur Oui, d’autres options s’affichent pour _[!UICONTROL Search Recommendations Count]_et_[!UICONTROL Shows Results Count for Each Recommendation]_. |
| [!UICONTROL Search Recommendations Count] | Affichage en magasin | Indique le nombre de termes de recherche proposés comme recommandations. Par défaut, cinq au maximum s’affichent. |
| [!UICONTROL Show Results Count for Each Recommendation] | Affichage en magasin | Lorsque la valeur est définie sur `Yes`, le nombre de produits trouvés pour la recommandation de recherche proposée est indiqué entre parenthèses. Options : `Yes` / `No` |
| [!UICONTROL Enable Search Suggestions] | Affichage en magasin | Détermine si les suggestions de recherche s’affichent pour les fautes d’orthographe courantes. Lorsque cette option est activée, des suggestions de recherche sont proposées pour toute requête qui ne renvoie aucun résultat et apparaissent sous la section `Did you mean` de la page **Résultats de la recherche**. Les suggestions de recherche peuvent avoir un impact sur les performances de la recherche. Lorsque la variable est définie sur `Yes`, d’autres options s’affichent pour l’option Activer le Recommendations de recherche et les champs associés. Options : `Yes` / `No` |
| [!UICONTROL Search Suggestions Count] | Affichage en magasin | Détermine le nombre de suggestions de recherche proposées. Par exemple : `2` |
| [!UICONTROL Show Results Count for Each Suggestion] | Affichage en magasin | Détermine si le nombre de résultats de recherche s’affiche pour chaque suggestion. Selon le thème, le nombre apparaît généralement entre crochets après la suggestion. Options : `Yes` / `No` |
| [!UICONTROL Minimum Terms to Match] | Affichage en magasin | Indique une valeur qui correspond au nombre de termes de votre requête que les résultats de la recherche doivent correspondre pour être renvoyés. Cela garantit une pertinence optimale des résultats pour les acheteurs. Les valeurs en pourcentage correspondent à un nombre. Si nécessaire, arrondies et utilisées comme nombre minimum de termes à faire correspondre dans votre requête. La valeur peut être un entier négatif ou positif, un pourcentage négatif ou positif, une combinaison des deux combinaisons ou plusieurs combinaisons. Pour en savoir plus, voir [paramètre minimum_should_match](https://opensearch.org/docs/latest/query-dsl/minimum-should-match/) dans la documentation OpenSearch. |

## [!UICONTROL Downloadable Product Options]

![Options de produit téléchargeables](./assets/catalog-downloadable-product-options.png)<!-- zoom -->

<!-- [Downloadable Product Options](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/types/product-create-downloadable#configure-the-download-options) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Order Item Status to Enable Downloads] | Site Web | Détermine l’état d’une commande avant que les téléchargements ne soient disponibles. Options : `Pending` / `Invoiced` |
| [!UICONTROL Default Maximum Number of Downloads] | Site Web | Détermine le nombre par défaut de téléchargements disponibles pour un client. |
| [!UICONTROL Shareable] | Site Web | Détermine si les clients doivent se connecter à leurs comptes pour accéder au lien de téléchargement. Options : <br/>**Oui** - Permet l’envoi du lien par courrier électronique, qui peut ensuite être partagé avec d’autres personnes. <br/>**Non** - Nécessite que les clients se connectent à leurs comptes pour accéder au lien de téléchargement. |
| [!UICONTROL Default Sample Title] | Affichage en magasin | Titre par défaut de tous les fichiers d’exemple. |
| [!UICONTROL Default Link Title] | Affichage en magasin | Lien par défaut pour tous les titres téléchargeables. |
| [!UICONTROL Opens Links in New Window] | Site Web | Détermine si le lien de téléchargement s’ouvre dans une nouvelle fenêtre du navigateur. Options : `Yes` / `No` |
| [!UICONTROL Use Content Disposition] | Affichage en magasin | Détermine le mode de diffusion du lien vers le contenu téléchargeable, sous la forme d’une pièce jointe à un email ou d’un lien intégré dans une fenêtre de navigateur. Options : <br/>**`Attachment`**- Le lien de téléchargement est remis en tant que pièce jointe à un email.<br/>**`Inline`** - Le lien de téléchargement est diffusé sous la forme d’un lien intégré sur une page web. |
| [!UICONTROL Disable Guest Checkout if Cart Contains Downloadable Items] | Site Web | Détermine si les invités qui achètent des produits téléchargeables doivent s’enregistrer pour un compte et se connecter pour terminer le processus de passage en caisse. Options : <br/>**`Yes`**- Si le panier contient des produits téléchargeables, l’invité doit s’enregistrer pour un compte ou se connecter à un compte existant pour terminer l’achat.<br/>**`No`** - Le lien de téléchargement est diffusé sous la forme d’un lien intégré dans le corps du message électronique.  <br/> _**Remarque :**_ Le passage en caisse des invités n’est disponible que pour les produits de téléchargement si le paramètre Partable est défini sur `Yes`. |

{style="table-layout:auto"}

## [!UICONTROL Date & Time Custom Options]

![Options personnalisées Date et heure](./assets/catalog-date-time-custom-options.png)<!-- zoom -->

<!-- Date & Time Custom Options](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/product-attributes/attributes-input-types#date-and-time-options) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Use JavaScript Calendar] | Affichage en magasin | Détermine si le calendrier JavaScript est utilisé comme contrôle d’entrée pour les champs de date. Options : `Yes` / `No` <br/>Si la valeur est définie sur `No`, une liste déroulante distincte s’affiche pour chaque partie du champ de date. |
| [!UICONTROL Date Fields Order] | Affichage en magasin | Définit l’ordre des trois champs de date. Options : `Day` / `Month` / `Year` |
| [!UICONTROL Time Format] | Affichage en magasin | Définit le format d’heure sur une horloge de 12 ou 24 heures. Options : `12h AM/PM` / `24h` |
| [!UICONTROL Year Range] | Affichage en magasin | Définit la période de début et de fin des années qui apparaissent dans le champ _Year_. La valeur doit être saisie au format AAAA. |

{style="table-layout:auto"}

## [!UICONTROL Catalog Events]

{{ee-feature}}

![Événements de catalogue](./assets/catalog-events.png)<!-- zoom -->

<!-- [Catalog Events](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/events/events-private-sales) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Catalog Events Functionality] | Site Web | Détermine si le module Événements est activé. |
| [!UICONTROL Enable Catalog Event Widget on Frontend] | Affichage en magasin | Détermine si le widget d’événement est disponible dans le storefront. Il s’agit d’un bloc statique contenant des informations sur les événements de votre site. |
| [!UICONTROL Number of Events to be Displayed in the Event Slider Widget] | Affichage en magasin | Détermine le nombre d’événements qui apparaissent dans le widget du curseur d’événement sur les pages de catégorie. Pour remplacer, utilisez la variable `limit="x"`. |
| [!UICONTROL Events to Scroll per Click in Event Slider Widget] | Affichage en magasin | Détermine le nombre d’événements qui apparaissent dans le widget du curseur des événements sur les pages CMS, telles que la page d’accueil. Pour remplacer, utilisez la variable `scroll="x"`. |

{style="table-layout:auto"}

## [!UICONTROL Rule-Based Product Relations]

{{ee-feature}}

![Relations produit basées sur des règles](./assets/catalog-rule-based-product-relations.png)<!-- zoom -->

<!-- [Rule-Based Product Relations](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Maximum Number of Products in Related Products List] | Global | Détermine le nombre maximal de produits pouvant apparaître dans la liste _Produits associés_. |
| [!UICONTROL Show Related Products] | Global | Détermine la liste des produits associés qui apparaît dans le magasin. Il peut s’agir de la liste sélectionnée manuellement dans les Informations sur le produit, de la liste générée en réponse à une règle de relation avec le produit ou d’une combinaison des deux. Options : `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Related Products List] | Global | Détermine l’ordre dans lequel les produits de la liste _Produits associés_ apparaissent. Options : `Do not rotate` / `Shuffle` |
| [!UICONTROL Maximum Number of Products in Cross-Sell Product List] | Global | Détermine le nombre maximal de produits pouvant apparaître dans la liste de ventes croisées. |
| [!UICONTROL Show Cross-Sell Products] | Global | Détermine la liste des produits de vente croisée qui apparaît dans le magasin. Il peut s’agir de la liste sélectionnée manuellement dans les Informations sur le produit, de la liste générée en réponse à une règle de relation avec le produit ou d’une combinaison des deux. Options : `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Cross-Sell Products List] | Global | Détermine l’ordre dans lequel apparaissent les produits dans la liste des produits vendus. Options : ne pas faire pivoter/mélanger |
| [!UICONTROL Maximum Number of Products in Upsell Product List] | Global | Détermine le nombre maximal de produits pouvant apparaître dans la liste _produits de vente incitative_. |
| [!UICONTROL Show Upsell Products] | Global | Détermine la liste des produits de vente incitative qui apparaît dans le magasin. Il peut s’agir de la liste sélectionnée manuellement dans les Informations sur le produit, de la liste générée en réponse à une règle de relation avec le produit ou d’une combinaison des deux. Options : `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Upsell Product List] | Global | Détermine l’ordre dans lequel les produits de la liste de produits de mise à niveau apparaissent. Options : `Do not rotate` / `Shuffle` |

{style="table-layout:auto"}
