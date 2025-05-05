---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Catalog]'
description: Vérifiez les paramètres de configuration sur la page de [!UICONTROL Catalog] d’[!UICONTROL Catalog] &gt; de l’administrateur Commerce.
exl-id: fc25ae80-aaa7-42c4-bba2-f03d3caa7970
feature: Configuration, Catalog Management
source-git-commit: 20f97d6ab391b7f5675d6790ab2ec5d24e9dda21
workflow-type: tm+mt
source-wordcount: '3261'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Catalog]

{{config}}

## [!UICONTROL Product Fields Auto-Generation]

![Génération automatique des champs de produit](./assets/catalog-product-fields-auto-generation.png)<!-- zoom -->

<!-- [Product Fields Auto-Generation](https://experienceleague.adobe.com/fr/docs/commerce-admin/catalog/products/product-workspace#default-field-values) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Mask for SKU] | Global | Détermine la valeur par défaut du champ SKU en fonction des valeurs d’espace réservé d’autres champs et de tout texte supplémentaire saisi. Espace réservé par défaut : <br/>Nom du produit - `{{name}}` |
| [!UICONTROL Mask for Meta Title] | Global | Détermine la valeur par défaut du champ Méta-titre en fonction des valeurs d’espace réservé d’autres champs et de tout texte supplémentaire saisi. Espace réservé par défaut : <br/>Nom du produit - `{{name}}` |
| [!UICONTROL Mask for Meta Keywords] | Global | Détermine la valeur par défaut du champ _Mots-clés méta_ en fonction des valeurs d’espace réservé d’autres champs et de tout texte supplémentaire saisi. Espace réservé par défaut : <br/>Nom du produit - `{{name}}` |
| [!UICONTROL Mask for Meta Description] | Global | Détermine la valeur par défaut du champ Méta-description en fonction des valeurs d’espace réservé d’autres champs et de tout texte supplémentaire saisi. Espace réservé par défaut : <br/>Nom du produit - `{{name}}` <br/>Description - `{{description}}` |

{style="table-layout:auto"}

## [!UICONTROL Product Reviews]

![Avis sur les produits](./assets/catalog-product-reviews.png)<!-- zoom -->

<!-- [Product Reviews](https://experienceleague.adobe.com/fr/docs/commerce-admin/marketing/merchandising/product-reviews/product-reviews) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Affichage de la boutique | Permet des révisions de produit. Options : `Yes` / `No` |
| [!UICONTROL Allow Guests to Write Reviews] | Site internet | Détermine si les clients doivent ouvrir un compte dans votre boutique pour pouvoir rédiger des avis sur les produits. |

{style="table-layout:auto"}

## [!UICONTROL Storefront]

![Storefront](./assets/catalog-storefront.png)<!-- zoom -->

<!-- [Storefront](https://experienceleague.adobe.com/fr/docs/commerce-admin/catalog/catalog/navigation/navigation-product-listings) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL List Mode] | Affichage de la boutique | Détermine le format de la liste des résultats de recherche. Options : <br/>**`Grid Only`**- Met en forme la liste sous la forme d’une grille de lignes et de colonnes. Chaque produit apparaît dans une seule cellule de la grille.<br/>**`List Only`** - Met en forme la liste avec chaque produit sur une ligne distincte. <br/>**`Grid (default / List)`**- Par défaut, les produits s’affichent dans la vue Grille et peuvent être basculés dans la vue Liste.<br/>**`List (default / Grid)`** - Par défaut, les produits apparaissent dans la vue Liste et peuvent être basculés en vue Grille. |
| [!UICONTROL Products per Page on Grid Allowed Values] | Affichage de la boutique | Détermine le nombre de produits affichés dans la vue Grille. Pour proposer une sélection d’options, saisissez plusieurs valeurs séparées par des virgules. |
| [!UICONTROL Products per Page on Grid Default Value] | Affichage de la boutique | Détermine le nombre de produits affichés par défaut par page dans la vue Grille. |
| [!UICONTROL Products per Page on List Allowed Values] | Affichage de la boutique | Détermine le nombre de produits affichés dans la vue Liste. Pour proposer une sélection d’options, saisissez plusieurs valeurs séparées par des virgules. |
| [!UICONTROL Products per Page on List Default Value] | Affichage de la boutique | Détermine le nombre de produits affichés par défaut par page, dans la vue Liste. |
| Liste des produits Trier par | Affichage de la boutique | Détermine l’ordre de tri de la liste des résultats de recherche. La sélection des options est déterminée par les paramètres d’affichage de la catégorie et les attributs disponibles définis pour être `Used for Sorting in Product Listing`. La valeur par défaut est définie sur `Use All Available Attributes` et inclut généralement Meilleure valeur, Nom, Prix. Ce paramètre ne s’applique pas au [!DNL Live Search] [widget de page de liste de produits](https://experienceleague.adobe.com/fr/docs/commerce/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Allow All Products per Page] | Affichage de la boutique | S’il est défini sur `Yes`, inclut l’option `ALL` dans le contrôle « Afficher par page ». |
| [!UICONTROL Remember Category Pagination] | Global | Si elles sont définies sur `Yes`, les valeurs actuelles de pagination de catégorie sont enregistrées lorsque les clients passent d’une catégorie à une autre dans [listes de produits](../../catalog/navigation-product-listings.md). L’enregistrement de la valeur utilise davantage d’espace de stockage en cache et peut affecter la manière dont les pages sont indexées par les moteurs de recherche. Options : `Yes` / `No` (par défaut) |
| [!UICONTROL Use Flat Catalog Category] | Global | Active la [structure de catégories plate](../../catalog/catalog-flat.md) (non recommandée). Options : `Yes` / `No` |
| [!UICONTROL Use Flat Catalog Product] | Global | Active la structure produit plate. (non recommandé) Options : `Yes` / `No` |
| [!UICONTROL Swatches per Product] | Affichage de la boutique | Détermine le nombre d’échantillons disponibles pour chaque produit. Valeur par défaut : `16` |
| [!UICONTROL Show Swatches in Product List] | Affichage de la boutique | Détermine si les échantillons apparaissent dans la liste de produits. Options : `Yes` / `No` |
| [!UICONTROL Show Swatch Tooltip] | Affichage de la boutique | Détermine si l’info-bulle de l’échantillon s’affiche. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Product Alerts]

![Alertes de produit](./assets/catalog-product-alerts.png)<!-- zoom -->

<!-- [Product Alerts](https://experienceleague.adobe.com/fr/docs/commerce-admin/inventory/configuration/product-alerts/alert-setup) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Allow Alerts When Product Price Changes] | Affichage de la boutique | Détermine si des alertes par e-mail sont disponibles pour les modifications du prix du produit. Options : `Yes` / `No` |
| [!UICONTROL Price Alert Email Template] | Affichage de la boutique | Identifie le modèle utilisé pour les alertes par e-mail de modification du prix des produits. Modèle par défaut : `Product price alert` |
| [!UICONTROL Allow Alert When Product Comes Back in Stock] | Site internet | Détermine si les clients peuvent choisir de recevoir une alerte lorsque le produit sera de nouveau en stock. Options : `Yes` / `No` |
| [!UICONTROL Stock Alert Email Template] | Affichage de la boutique | Identifie le modèle utilisé pour les notifications par e-mail d’alerte de stock. Modèle par défaut : `Product stock alert` |
| [!UICONTROL Alert Email Sender] | Affichage de la boutique | Détermine le contact du magasin qui apparaît comme expéditeur de l’e-mail d’alerte de produit. Options : `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email` |

{style="table-layout:auto"}

## [!UICONTROL Product Alerts Run Settings]

![Paramètres d’exécution des alertes de produit](./assets/catalog-product-alerts-run-settings.png)<!-- zoom -->

<!-- [Product Alerts Run Settings](https://experienceleague.adobe.com/fr/docs/commerce-admin/inventory/configuration/product-alerts/alert-setup) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Frequency] | Global | Choisissez la fréquence d’envoi des alertes de produits. Options : `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Start Time] | Global | Choisissez l’heure à laquelle le processus d’alerte des produits commence. Cette heure doit être postérieure à toute mise à jour des prix ou des stocks. |
| [!UICONTROL Error Email Recipient] | Global | Identifiez l’adresse e-mail de la personne (généralement un administrateur de magasin) qui doit recevoir une notification par e-mail en cas d’erreur dans le processus d’alerte du produit. |
| [!UICONTROL Error Email Sender] | Global | Sélectionnez le rôle auquel l’e-mail est `from`. |
| [!UICONTROL Error Email Template] | Global | Sélectionnez le modèle d’e-mail à utiliser pour les notifications d’erreur d’alerte de produit. |

{style="table-layout:auto"}

## [!UICONTROL Product Image Placeholders]

![Espaces réservés d’image de produit](./assets/catalog-product-image-placeholders.png)<!-- zoom -->

<!-- [Product Image Placeholders](https://experienceleague.adobe.com/fr/docs/commerce-admin/catalog/products/digital-assets/product-image-config#image-placeholders) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Base Image] | Affichage de la boutique | Identifie le fichier d’espace réservé choisi pour l’image de base. |
| [!UICONTROL Small Image] | Affichage de la boutique | Identifie le fichier d’espace réservé choisi pour la petite image. |
| [!UICONTROL Swatch] | Affichage de la boutique | Identifie le fichier d’espace réservé choisi pour l’échantillon. |
| [!UICONTROL Thumbnail] | Affichage de la boutique | Identifie le fichier d’espace réservé choisi pour la miniature. |
| [!UICONTROL Choose File] |  | Permet d’accéder au fichier et de le charger en tant qu’image d’espace réservé pour le type. |

{style="table-layout:auto"}

## [!UICONTROL Recently Viewed/Compared Products]

![Produits récemment consultés/comparés](./assets/catalog-recently-viewed-and-compared-products.png)<!-- zoom -->

<!-- Recently Viewed/Compared Products](https://experienceleague.adobe.com/fr/docs/commerce-admin/stores-sales/shopper-tools/products-viewed-compared) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Synchronize widget products with backend storage] | Global | Détermine la synchronisation des informations du widget de produit, telles que l’ID de produit, avec la base de données. Cela permet de réutiliser des informations sur d’autres appareils. |
| [!UICONTROL Show for Current] | Site internet | Limite les produits affichés sur le site web actuel. Options : `Website` / `Store` / `Store View` |
| [!UICONTROL Default Recently Viewed Products Count] | Affichage de la boutique | Détermine le nombre maximal de produits récemment consultés qui apparaissent dans la liste. |
| [!UICONTROL Default Recently Compared Products Count] | Affichage de la boutique | Détermine le nombre maximal de produits récemment comparés qui apparaissent dans la liste. |
| [!UICONTROL Lifetime of products in Recently Viewed Widget] | Global | Détermine la durée pendant laquelle, en secondes, les produits consultés sont affichés dans la liste récemment consultée. |
| [!UICONTROL Lifetime of products in Recently Compared Widget] | Global | Détermine la durée d&#39;affichage, en secondes, des produits comparés dans la liste récemment comparée. |

{style="table-layout:auto"}

## [!UICONTROL Product Video]

![Vidéos produit](./assets/catalog-product-video.png)<!-- zoom -->

<!-- [Product Videos](https://experienceleague.adobe.com/fr/docs/commerce-admin/catalog/products/digital-assets/product-video) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL YouTube API key] | Affichage de la boutique | Indique la clé API requise pour se connecter au serveur YouTube. |
| [!UICONTROL Autostart base video] | Affichage de la boutique | Pour démarrer automatiquement la vidéo après le chargement de la page, définissez sur `Yes`. |
| [!UICONTROL Show related video] | Affichage de la boutique | Pour afficher les vidéos associées, définissez sur `Yes`. |
| [!UICONTROL Auto restart video] | Affichage de la boutique | Pour activer la vidéo de relecture automatique, définissez sur `Yes`. |

{style="table-layout:auto"}

## [!UICONTROL Price]

![Prix](./assets/catalog-price.png)<!-- zoom -->

<!--Price](https://experienceleague.adobe.com/fr/docs/commerce-admin/catalog/products/pricing/catalog-price-scope) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Catalog Price Scope] | Global | Détermine la portée de la devise de base. Options : `Global` / `Website` |
| [!UICONTROL Default Product Price] | Global | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Définit le prix par défaut du produit, le cas échéant. |

{style="table-layout:auto"}

## [!UICONTROL Layered Navigation]

>[!NOTE]
>
>La configuration de recherche standard décrite dans cette section diffère pour [Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=fr).

<!-- [Layered Navigation - Automatic (equalize price ranges)](https://experienceleague.adobe.com/fr/docs/commerce-admin/catalog/catalog/navigation/navigation-layered#configure-layered-navigation) -->

![Navigation à plusieurs niveaux - Automatique (égalisation des plages de prix)](./assets/layered-navigation-equalize-price-range.png)<!-- zoom -->

![Navigation superposée - Automatique (égalisation du nombre de produits)](./assets/layered-navigation-equalize-product-counts.png)<!-- zoom -->

![Navigation par couches - Manuelle](./assets/layered-navigation-manual.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Display Product Count] | Affichage de la boutique | Détermine si le nombre de produits apparaît après chaque attribut, plage de prix et catégorie. Options : `Yes` / `No` |
| [!UICONTROL Price Navigation Step Calculation] | Affichage de la boutique | Détermine la méthode utilisée pour déterminer l’[étape de navigation des prix](../../catalog/navigation-layered.md#configure-price-navigation)). Options : <br/>`Automatic (equalize price ranges)` - Base le calcul sur la gamme de prix des produits du groupe. <br/>`Automatic (equalize product counts)` - Base le calcul sur le nombre de produits dans le groupe. Établit un seuil pour le nombre minimal de produits du groupe, afin d&#39;éviter qu&#39;ils ne soient divisés en groupes plus petits. <br/>`Manual` - Utilise la limite de division que vous entrez pour les intervalles de prix. |
| [!UICONTROL Default Price Navigation Step] | Affichage de la boutique | Détermine le nombre de produits inclus dans chaque étape. |
| [!UICONTROL Maximum Number of Price Intervals] | Affichage de la boutique | Définit une limite pour le nombre d’intervalles de prix qui apparaissent dans la navigation superposée. |

{style="table-layout:auto"}

## [!UICONTROL Category Permissions]

{{ee-feature}}

![Autorisations de catégorie](./assets/catalog-category-permissions.png)<!-- zoom -->

<!-- [Category Permissions](https://experienceleague.adobe.com/fr/docs/commerce-admin/catalog/categories/category-permissions) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable] | Global | Active les restrictions de catégorie. Par défaut, l’utilisation de cette fonctionnalité limite toutes les catégories. Options : `Yes` / `No` |
| [!UICONTROL Allow Browsing Category] | Site internet | Détermine qui est autorisé à parcourir les catégories. Options : <br/>`Yes, for Everyone` - Permet à tous les visiteurs et clients de parcourir la catégorie. <br/>`Yes, for Specified Customer Groups` - Permet uniquement aux membres des groupes de clients sélectionnés de parcourir la catégorie. <br/>`No, Redirect to Landing Page` - Refuse l’accès à la catégorie et redirige vers la page sélectionnée. |
| [!UICONTROL Display Product Prices] | Site internet | Contrôle l&#39;affichage des prix des produits pour la catégorie. Options : <br/>`Yes, for Everyone` - Permet à tout le monde de voir le prix des produits dans la catégorie. <br/>`Yes, for Specified Customer Groups` - Permet uniquement aux membres des groupes de clients sélectionnés d’afficher le prix des produits de la catégorie. <br/>`No` - Désactive l&#39;affichage des prix des produits pour la catégorie. |
| [!UICONTROL Allow Adding to Cart] | Site internet | Détermine qui peut acheter des produits de la catégorie. Options : <br/>`Yes, for Everyone` - Permet à chacun de placer des produits de la catégorie dans son panier. <br/>`Yes, for Specified Customer Groups` - Permet uniquement aux membres des groupes de clients sélectionnés de placer des produits de la catégorie dans leur panier. <br/>`No` - Ne permet à personne de placer des produits de la catégorie dans son panier. |
| [!UICONTROL Disallow Catalog Search by] | Site internet | Identifie les groupes de clients qui ne sont pas autorisés à rechercher des produits dans la catégorie. |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Optimization]

![Optimisation du moteur de recherche](./assets/catalog-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization](https://experienceleague.adobe.com/fr/docs/commerce-admin/catalog/products/settings/product-search-engine-optimization) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Popular Search Terms] | Affichage de la boutique | Détermine si _Termes de recherche populaires_ est implémenté dans le magasin. Ce paramètre ne s’applique pas aux magasins qui utilisent [Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=fr). Options : `Enable` / `Disable` |
| [!UICONTROL Product URL Suffix] | Affichage de la boutique | Détermine si un suffixe, tel que html ou htm, est appliqué aux URL de produit. Si vous utilisez cette option, n’incluez pas de point avant le suffixe , car il est appliqué automatiquement. |
| [!UICONTROL Category URL Suffix] | Affichage de la boutique | Détermine si un suffixe, tel que html ou htm, est appliqué aux URL de catégorie. Si vous utilisez cette option, n’incluez pas de point avant le suffixe , car il est appliqué automatiquement. |
| [!UICONTROL Use Categories Path for Product URLs] | Affichage de la boutique | Détermine si les chemins d’accès aux catégories sont inclus dans les URL de produit sur le storefront. Cela peut entraîner le pointage de plusieurs URL vers la même page, ce qui peut avoir un impact sur le classement de la recherche. Pour en savoir plus, voir [Balise de métadonnées canonique](../../merchandising-promotions/meta-data.md#canonical-meta-tag). |
| [!UICONTROL Create Permanent Redirect for URLs if URL Key Changed] | Affichage de la boutique | Détermine si une redirection permanente est créée automatiquement chaque fois qu’une clé d’URL change. Lorsqu’elle est implémentée, la case à cocher Créer une redirection personnalisée pour l’ancienne URL située sous le champ Clé d’URL de produit est sélectionnée par défaut. Options : `Yes` / `No` |
| [!UICONTROL Generate "category/product" URL Rewrites] | Global | Détermine si Adobe Commerce génère des données et les enregistre dans des tables de réécriture lorsqu’un utilisateur enregistre une catégorie qui contient de nombreux produits affectés.  <br/><br/>La modification de cette option n’affecte pas la manière dont les URL de produit sont résolues dans Adobe Commerce, car le système résout automatiquement les URL de produit, quel que soit ce paramètre. <br/><br/>Options : `Yes` / `No` <br/><br/>**_Important :_**&#x200B;l’enregistrement de ces données générées dans un tableau de réécritures d’URL peut dégrader les performances. Pour plus d’informations, consultez [Redirections automatiques de produit](../../merchandising-promotions/url-redirect-product-automatic.md). |
| [!UICONTROL Apply transliteration for product URL] | Affichage de la boutique | Détermine si la translittération est appliquée lors de la création ou de la mise à jour des URL de produit. Options : `Yes` / `No`. La valeur par défaut est définie sur `Yes`. <br/><br/>Pour certains cas d’utilisation, vous devez désactiver la translittération. Par exemple, si vous utilisez une boutique en ligne en chinois, les bonnes pratiques d’optimisation du moteur de recherche recommandent que les URL des produits correspondent au nom du produit. La définition de l’option sur `No` permet d’utiliser des caractères chinois dans les URL de produit au lieu d’un équivalent ASCII. |
| [!UICONTROL Page Title Separator] | Affichage de la boutique | Identifie le caractère qui sépare le nom de catégorie et la sous-catégorie dans la barre de titre du navigateur. |
| [!UICONTROL Use Canonical Link Meta Tag for Categories] | Affichage de la boutique | S’il existe plusieurs URL pointant vers la même page de catégorie, cette option utilise une balise meta canonique pour identifier l’URL de catégorie que les moteurs de recherche doivent indexer. L’URL inclut un nom complet pour la catégorie à l’aide de la balise meta . Cela réduit le contenu en double et améliore l’optimisation du moteur de recherche. Options : `Yes` / `No` |
| [!UICONTROL Use Canonical Link Meta Tag for Products] | Affichage de la boutique | S’il existe plusieurs URL pointant vers la même page de produit, cette option utilise une balise meta canonique pour identifier l’URL du produit que les moteurs de recherche doivent indexer. L’URL inclut un nom complet du produit à l’aide de la balise meta . Cela réduit le contenu en double et améliore l’optimisation du moteur de recherche. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Category Top Navigation]

![Navigation supérieure de catégorie](./assets/catalog-category-top-navigation.png)<!-- zoom -->

<!-- Category Top Navigation](https://experienceleague.adobe.com/fr/docs/commerce-admin/catalog/catalog/navigation/navigation-top) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Maximal Depth] | Global | Détermine le nombre de niveaux de sous-catégorie dans la barre de navigation supérieure. La valeur par défaut de `0` ne limite pas le nombre de niveaux. |

{style="table-layout:auto"}

## [!UICONTROL Catalog Search]

Vous pouvez configurer la recherche catalogue à l’aide de services de moteur de recherche [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=fr) ou tiers pris en charge par Adobe Commerce. Suivez les instructions relatives à votre installation.

### Adobe Commerce avec [!DNL Live Search]

Lors de l’installation de Live Search, la recherche catalogue inclut les paramètres de configuration suivants :

![Recherche catalogue pour Live Search](./assets/catalog-search-live-search.png)<!-- zoom -->

<!-- [Catalog Search for Live Search](https://experienceleague.adobe.com/fr/docs/commerce-admin/catalog/catalog/search/search-configuration) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Minimal Query Length] | Affichage de la boutique | Nombre minimum de caractères autorisés dans une recherche catalogue. La valeur définie pour cette option doit être compatible avec la plage correspondante définie dans les configurations de votre moteur de recherche Elasticsearch. Par exemple, si vous définissez cette valeur sur `2` dans Adobe Commerce, mettez à jour la valeur dans votre moteur de recherche. |
| [!UICONTROL Maximum Query Length] | Affichage de la boutique | Nombre maximal de caractères autorisés dans une recherche catalogue. La valeur définie pour cette option doit être compatible avec la plage correspondante définie dans les configurations de votre moteur de recherche Elasticsearch. Par exemple, si vous définissez cette valeur sur 300 dans Adobe Commerce, mettez à jour la valeur dans votre moteur de recherche. |
| [!UICONTROL Number of top search results to cache] | Affichage de la boutique | Nombre de termes et résultats de recherche populaires à mettre en cache pour des réponses plus rapides. La saisie d’une valeur `0` met en cache tous les termes et résultats de recherche lorsqu’elle est effectuée une seconde fois. Valeur par défaut : `100` |
| [!UICONTROL Autocomplete Limit] | Affichage de la boutique | Détermine le nombre maximal de lignes disponibles dans la page [fenêtre contextuelle storefront]. La valeur par défaut peut être modifiée lors de l’installation de Live Search et mise à jour ultérieurement en modifiant ce paramètre de configuration. Valeur par défaut : `8` |

{style="table-layout:auto"}

### Moteurs de recherche tiers

Adobe Commerce prend en charge OpenSearch et Elasticsearch. Les versions 2.3.7-p3, 2.4.3-p2 et 2.4.4 d’Adobe Commerce et ultérieures prennent en charge le service OpenSearch. Elasticsearch 7.11 et versions ultérieures ne sont pas pris en charge sur Adobe Commerce dans les projets d’infrastructure cloud. Elasticsearch est toujours pris en charge pour les installations sur site.

>[!IMPORTANT]
>
>- En raison de l’annonce de fin de prise en charge d’Elasticsearch 7 en août 2023, Adobe recommande à tous les clients Adobe Commerce de migrer vers le moteur de recherche OpenSearch 2.x. Pour plus d’informations sur la migration de votre moteur de recherche lors d’une mise à niveau, voir [Migration vers OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html?lang=fr) dans le _Guide de mise à niveau_.
>- Dans les versions 2.4.4 et 2.4.3-p2, tous les champs libellés Elasticsearch s’appliquent également à OpenSearch. Lorsque la prise en charge d’Elasticsearch 8.x a été introduite dans la version 2.4.6, de nouveaux libellés ont été créés pour faire la distinction entre les configurations Elasticsearch et OpenSearch. Toutefois, les options de configuration pour les deux sont identiques.

![Options de configuration de la recherche catalogue](./assets/catalog-search-opensearch.png){zoomable="yes"}

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Minimal Query Length] | Affichage de la boutique | Nombre minimum de caractères autorisés dans une recherche catalogue. La valeur définie pour cette option doit être compatible avec la plage correspondante définie dans votre configuration OpenSearch ou Elasticsearch. Par exemple, si vous définissez cette valeur sur `2` dans Adobe Commerce, vous devez également mettre à jour la valeur dans la configuration de votre moteur de recherche. Valeur par défaut : `3` |
| [!UICONTROL Maximum Query Length] | Affichage de la boutique | Nombre maximal de caractères autorisés dans une recherche catalogue. La valeur définie pour cette option doit être compatible avec la plage correspondante définie dans votre configuration OpenSearch ou Elasticsearch. Par exemple, si vous définissez cette valeur sur `300` dans Adobe Commerce, vous devez mettre à jour la valeur dans la configuration de votre moteur de recherche. Valeur par défaut : `128` |
| [!UICONTROL Number of top search results to cache] | Affichage de la boutique | Nombre de termes et résultats de recherche populaires à mettre en cache pour des réponses plus rapides. La saisie d’une valeur `0` met en cache tous les termes et résultats de recherche lorsqu’elle est effectuée une seconde fois. Valeur par défaut : `100` |
| [!UICONTROL Enable EAV Indexer] | Global | Détermine s’il faut activer ou désactiver l’indexeur AEM du produit. Cette fonctionnalité améliore la vitesse d’indexation et limite l’utilisation de l’indexeur par les extensions tierces. Option par défaut : `Yes` pour activé |
| [!UICONTROL Autocomplete Limit] | Affichage de la boutique | Nombre maximal de requêtes de recherche à afficher sous le champ de recherche pour la saisie semi-automatique. Limiter ce nombre améliore les performances des recherches et réduit la taille de la liste affichée. Valeur par défaut : `8` |
| Moteur de recherche | Global | Identifie le moteur de recherche requis pour traiter les demandes de données de catalogue. Les options de configuration du moteur de recherche sont identiques pour OpenSearch et Elasticsearch. Options : `OpenSearch` ou `Elasticsearch` |
| [!UICONTROL OpenSearch Server Hostname] | Global | Indique le nom du serveur hôte OpenSearch ou Elasticsearch. |
| [!UICONTROL OpenSearch Server Port] | Global | Indique le numéro de port du serveur utilisé par OpenSearch ou Elasticsearch. Valeur par défaut : `9200` |
| [!UICONTROL OpenSearch Index Prefix] | Global | Attribue un préfixe pour identifier l’index OpenSearch ou Elasticsearch. Valeur par défaut : `magento2` |
| [!UICONTROL Enable OpenSearch HTTP Auth] | Global | Si cette option est activée, utilise l’authentification HTTP pour demander un nom d’utilisateur et un mot de passe avant d’accéder au serveur OpenSearch ou Elasticsearch. Options : `Yes` / `No` |
| [!UICONTROL OpenSearch HTTP Username] | Global | Lorsque l’option _Activer l’authentification HTTP Elasticsearch_ est définie sur `Yes`, indique le nom d’utilisateur pour l’authentification OpenSearch ou HTTP Elasticsearch. |
| [!UICONTROL OpenSearch HTTP Password] | Global | Lorsque _Activer l’authentification HTTP Elasticsearch_ est défini sur `Yes`, indique le mot de passe de l’authentification OpenSearch ou HTTP Elasticsearch. |
| [!UICONTROL OpenSearch Server Timeout] | Global | Détermine le nombre de secondes avant l’expiration d’une requête au serveur OpenSearch ou Elasticsearch. Valeur par défaut : `15` |
| [!UICONTROL Test Connection] |  | Valide la connexion OpenSearch ou Elasticsearch. |
| [!UICONTROL Enable Search Recommendations] | Affichage de la boutique | Détermine si des recommandations de recherche sont proposées lorsqu’une recherche ne renvoie aucun résultat et s’affichent sous la section `Related search terms` de la page des résultats de recherche. Options : `Yes` / `No` <br/>Lorsque ce paramètre est défini sur Oui, des options supplémentaires s’affichent pour les _[!UICONTROL Search Recommendations Count]_&#x200B;et les&#x200B;_[!UICONTROL Shows Results Count for Each Recommendation]_. |
| [!UICONTROL Search Recommendations Count] | Affichage de la boutique | Indique le nombre de termes de recherche proposés en tant que recommandations. Par défaut, cinq sont affichés au maximum. |
| [!UICONTROL Show Results Count for Each Recommendation] | Affichage de la boutique | Lorsqu’il est défini sur `Yes`, le nombre de produits trouvés pour la recommandation de recherche proposée est indiqué entre parenthèses. Options : `Yes` / `No` |
| [!UICONTROL Enable Search Suggestions] | Affichage de la boutique | Détermine si des suggestions de recherche s’affichent pour les fautes d’orthographe courantes. Lorsque cette option est activée, des suggestions de recherche sont proposées pour toute requête qui ne renvoie aucun résultat et qui s’affiche sous la section `Did you mean` de la page **Résultats de la recherche**. Les suggestions de recherche peuvent avoir un impact sur les performances de la recherche. Lorsque ce paramètre est défini sur `Yes`, des options supplémentaires s’affichent pour Activer les recommandations de recherche et les champs associés. Options : `Yes` / `No` |
| [!UICONTROL Search Suggestions Count] | Affichage de la boutique | Détermine le nombre de suggestions de recherche proposées. Par exemple : `2` |
| [!UICONTROL Show Results Count for Each Suggestion] | Affichage de la boutique | Détermine si le nombre de résultats de recherche s’affiche pour chaque suggestion. Selon le thème, le nombre apparaît généralement entre crochets après la suggestion. Options : `Yes` / `No` |
| [!UICONTROL Minimum Terms to Match] | Affichage de la boutique | Spécifie une valeur qui correspond au nombre de termes de votre requête auxquels les résultats de recherche doivent correspondre pour être renvoyés. Cela garantit une pertinence optimale des résultats pour les acheteurs. Les valeurs de pourcentage sont corrélées à un nombre. Si nécessaire, elles sont arrondies à l’unité inférieure et utilisées comme nombre minimum de termes à faire correspondre dans votre requête. La valeur peut être un nombre entier négatif ou positif, un pourcentage négatif ou positif, une combinaison des deux combinaisons ou plusieurs combinaisons. Pour en savoir plus, consultez le paramètre [minimum_should_match](https://opensearch.org/docs/latest/query-dsl/minimum-should-match/) dans la documentation d’OpenSearch. |

## [!UICONTROL Downloadable Product Options]

![Options de produit téléchargeables](./assets/catalog-downloadable-product-options.png)<!-- zoom -->

<!-- [Downloadable Product Options](https://experienceleague.adobe.com/fr/docs/commerce-admin/catalog/products/types/product-create-downloadable#configure-the-download-options) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Order Item Status to Enable Downloads] | Site internet | Détermine le statut requis pour qu’une commande soit téléchargée. Options : `Pending` / `Invoiced` |
| [!UICONTROL Default Maximum Number of Downloads] | Site internet | Détermine le nombre de téléchargements disponibles par défaut pour un client. |
| [!UICONTROL Shareable] | Site internet | Détermine si les clients doivent se connecter à leur compte pour accéder au lien de téléchargement. Options : <br/>**Oui** - Permet d’envoyer le lien par e-mail, qui peut ensuite être partagé avec d’autres personnes. <br/>**Non** - Nécessite que les clients se connectent à leur compte pour accéder au lien de téléchargement. |
| [!UICONTROL Default Sample Title] | Affichage de la boutique | Titre par défaut de tous les fichiers d’exemple. |
| [!UICONTROL Default Link Title] | Affichage de la boutique | Le lien par défaut pour tous les titres téléchargeables. |
| [!UICONTROL Opens Links in New Window] | Site internet | Détermine si le lien de téléchargement s’ouvre dans une nouvelle fenêtre du navigateur. Options : `Yes` / `No` |
| [!UICONTROL Use Content Disposition] | Affichage de la boutique | Détermine la manière dont le lien vers le contenu téléchargeable est diffusé, sous la forme d’une pièce jointe d’e-mail ou d’un lien intégré dans une fenêtre de navigateur. Options : <br/>**`Attachment`**- le lien de téléchargement est fourni sous la forme d’une pièce jointe à votre courrier électronique.<br/>**`Inline`** - Le lien de téléchargement est fourni sous la forme d’un lien intégré sur une page web. |
| [!UICONTROL Disable Guest Checkout if Cart Contains Downloadable Items] | Site internet | Détermine si les invités qui achètent des produits téléchargeables doivent s’inscrire à un compte et se connecter pour terminer le processus de passage en caisse. Options : <br/>**`Yes`**- Si le panier contient des produits téléchargeables, le client doit soit s’inscrire à un compte, soit se connecter à un compte existant pour terminer l’achat.<br/>**`No`** - Le lien de téléchargement est fourni sous la forme d’un lien intégré dans le corps de l’e-mail.  <br/> _&#x200B;**Remarque :**&#x200B;_ passage en caisse des invités n’est disponible que pour les produits de téléchargement si l’option Partageable est définie sur `Yes`. |

{style="table-layout:auto"}

## [!UICONTROL Date & Time Custom Options]

![Options personnalisées de date et heure](./assets/catalog-date-time-custom-options.png)<!-- zoom -->

<!-- Date & Time Custom Options](https://experienceleague.adobe.com/fr/docs/commerce-admin/catalog/product-attributes/attributes-input-types#date-and-time-options) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Use JavaScript Calendar] | Affichage de la boutique | Détermine si le calendrier JavaScript est utilisé comme contrôle d’entrée pour les champs de date. Options : `Yes` / `No` <br/>Si cette option est définie sur `No`, une liste déroulante distincte s’affiche pour chaque partie du champ de date. |
| [!UICONTROL Date Fields Order] | Affichage de la boutique | Définit l’ordre des trois champs de date. Options : `Day` / `Month` / `Year` |
| [!UICONTROL Time Format] | Affichage de la boutique | Définit le format de l’heure sur une horloge de 12 ou 24 heures. Options : `12h AM/PM` / `24h` |
| [!UICONTROL Year Range] | Affichage de la boutique | Définit la plage de début et de fin des années qui apparaissent dans le champ _Année_. La valeur doit être saisie au format AAAA. |

{style="table-layout:auto"}

## [!UICONTROL Catalog Events]

{{ee-feature}}

![Événements de catalogue](./assets/catalog-events.png)<!-- zoom -->

<!-- [Catalog Events](https://experienceleague.adobe.com/fr/docs/commerce-admin/marketing/promotions/events/events-private-sales) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Catalog Events Functionality] | Site internet | Détermine si le module Événements est activé. |
| [!UICONTROL Enable Catalog Event Widget on Frontend] | Affichage de la boutique | Détermine si le widget d’événement est disponible dans le storefront. Il s’agit d’un bloc statique contenant des informations sur les événements de votre site. |
| [!UICONTROL Number of Events to be Displayed in the Event Slider Widget] | Affichage de la boutique | Détermine le nombre d’événements qui apparaissent dans le widget de curseur d’événement sur les pages de catégorie. Pour remplacer, utilisez la variable `limit="x"` . |
| [!UICONTROL Events to Scroll per Click in Event Slider Widget] | Affichage de la boutique | Détermine le nombre d’événements qui apparaissent dans le widget de curseur d’événement sur les pages CMS, telles que la page d’accueil. Pour remplacer, utilisez la variable `scroll="x"` . |

{style="table-layout:auto"}

## [!UICONTROL Rule-Based Product Relations]

{{ee-feature}}

![Relations de produit basées sur des règles](./assets/catalog-rule-based-product-relations.png)<!-- zoom -->

<!-- [Rule-Based Product Relations](https://experienceleague.adobe.com/fr/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Maximum Number of Products in Related Products List] | Global | Détermine le nombre maximal de produits pouvant apparaître dans la liste _Produits associés_. |
| [!UICONTROL Show Related Products] | Global | Détermine quelle liste de produits associés apparaît dans le magasin. Il peut s’agir de la liste sélectionnée manuellement dans les informations sur le produit, de la liste générée en réponse à une règle de relation de produit ou d’une combinaison des deux. Options : `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Related Products List] | Global | Détermine l&#39;ordre dans lequel les produits de la liste _Produits associés_ s&#39;affichent. Options : `Do not rotate` / `Shuffle` |
| [!UICONTROL Maximum Number of Products in Cross-Sell Product List] | Global | Détermine le nombre maximal de produits pouvant apparaître dans la liste de ventes croisées. |
| [!UICONTROL Show Cross-Sell Products] | Global | Détermine la liste des produits de vente croisée qui apparaît dans le magasin. Il peut s’agir de la liste sélectionnée manuellement dans les informations sur le produit, de la liste générée en réponse à une règle de relation de produit ou d’une combinaison des deux. Options : `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Cross-Sell Products List] | Global | Détermine l’ordre dans lequel les produits de la liste de ventes croisées s’affichent. Options : ne pas faire pivoter/mélanger |
| [!UICONTROL Maximum Number of Products in Upsell Product List] | Global | Détermine le nombre maximal de produits pouvant apparaître dans la liste _Produits de mise à niveau_. |
| [!UICONTROL Show Upsell Products] | Global | Détermine la liste des produits de mise à niveau qui apparaît dans le magasin. Il peut s’agir de la liste sélectionnée manuellement dans les informations sur le produit, de la liste générée en réponse à une règle de relation de produit ou d’une combinaison des deux. Options : `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Upsell Product List] | Global | Détermine l’ordre dans lequel les produits de la liste de produits de montée en gamme s’affichent. Options : `Do not rotate` / `Shuffle` |

{style="table-layout:auto"}
