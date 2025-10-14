---
title: URL de catalogue et de produit
description: Découvrez les types de format d’URL de vos produits de catalogue et comment les configurer.
exl-id: 47405dc6-9b5e-4ca8-87eb-5a222de40793
feature: Catalog Management, Products, Search, Categories
source-git-commit: 1edab49fd8d52a1b7414eb207a21c5c03200e75e
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 0%

---

# URL de catalogue et de produit

Les URL que vous affectez aux produits et aux catégories jouent un rôle majeur dans la détermination de la qualité de l’indexation de votre site par les moteurs de recherche. Avant de commencer à créer votre catalogue, tenez compte des options disponibles. Pour afficher le format d’URL actuel, accédez au storefront et à n’importe quel produit de votre catalogue. Le format de l’URL dépend des paramètres de configuration et de la méthode actuellement utilisés pour rechercher la page.

## Formats des URL

### URL dynamique

Une URL dynamique est créée _à la volée_ et peut inclure une chaîne de requête avec des variables pour l’ID de produit, l’ordre de tri et la page sur laquelle la requête a été effectuée. Lorsqu’un client recherche un produit dans votre boutique, l’URL qui en résulte peut se présenter comme suit :

- `http://mystore.com/catalogsearch/result/?q=racer+back`
- `http://mystore.com/women/tops-women.html?style_general=135`

### URL statique

Une URL statique est une adresse fixe pour une page spécifique. Une URL statique peut être affichée dans un format compatible avec les moteurs de recherche ou qui fait référence aux produits et aux catégories par identifiant. Ces URL incluent des mots que les utilisateurs peuvent utiliser pour rechercher un produit et qui nécessitent des réécritures du serveur web pour être activées. Les fichiers avec des URL statiques sont généralement utilisés pour les pages de produits et de catégories, les pages de contenu et les ressources de [thème](../content-design/theme-assets.md).

- `http://mystore.com/antonia-racer-tank.html`

## Composants d’URL

### Clé de l’URL

La clé URL est la partie d’une URL statique qui décrit le produit ou la catégorie. Lorsque vous créez un produit ou une catégorie, une clé d’URL initiale est automatiquement générée en fonction du nom. Pour modifier la clé URL, reportez-vous à la section [Optimisation du moteur de recherche](product-search-engine-optimization.md) des informations sur le produit.

>[!NOTE]
>
>Par défaut, les caractères spéciaux accentués sont automatiquement remplacés par leurs versions standard non accentuées dans la clé d’URL. Par exemple, `ñ` est automatiquement remplacé par `n`. Ce comportement peut être désactivé en définissant l’option de configuration _[!UICONTROL Search Engine Optimization: Apply transliteration for product URL]_&#x200B;sur `No`. Voir [&#x200B; Configuration des URL de catalogue &#x200B;](#configure-catalog-urls).

La clé de l’URL doit comporter des caractères minuscules séparés par des tirets sans fin. Les tirets ne sont pas autorisés au début ou à la fin de la clé URL. Une clé d’URL bien conçue et « adaptée aux moteurs de recherche » peut inclure le nom du produit et des mots-clés afin d’améliorer la manière dont elle est indexée par les moteurs de recherche. La clé URL peut être configurée pour créer une redirection automatique en cas de modification de la clé URL.

>[!NOTE]
>
>Pour étendre les personnalisations d’URL, telles que les URL localisées, consultez [Réécritures d’URL](../merchandising-promotions/url-rewrite.md) pour plus d’informations.

### Suffixe HTML

Votre catalogue peut être configuré pour inclure ou exclure le suffixe dans le cadre des URL de catégories et de produits. Il existe différentes raisons pour lesquelles les utilisateurs peuvent choisir d’utiliser ou d’omettre le suffixe . Certains pensent que le suffixe n’a plus aucune utilité et que les pages sans suffixe sont indexées plus efficacement par les moteurs de recherche. Cependant, votre entreprise peut disposer d’un format normalisé pour les URL qui nécessite un suffixe.

Comme le suffixe est contrôlé par la configuration du système, vous ne devez jamais le saisir directement dans la clé URL d’une catégorie ou d’un produit. (Vous obtenez ainsi un double suffixe à la fin de l’URL.) Que vous décidiez d’utiliser le suffixe ou non, restez cohérent et utilisez le même paramètre pour toutes vos pages de produits et de catégories. Voici des exemples d’URL avec et sans suffixe .

#### URL avec suffixe HTML

- `http://mystore.com/helena-hooded-fleece.html`
- `http://mystore.com/helena-hooded-fleece.htm`

#### URL sans suffixe HTML

- `http://mystore.com/helena-hooded-fleece`

### Chemin d’accès de la catégorie

Vous pouvez configurer les URL des produits pour inclure ou exclure le chemin d’accès de la catégorie en fonction de vos préférences. Par défaut, le chemin d’accès à la catégorie n’est pas inclus dans les URL de produits. Cependant, les catégories imbriquées afficheront toujours le chemin d’accès complet aux catégories dans leurs URL sur le storefront, assurant ainsi la clarté et la cohérence de la navigation par catégorie. Les exemples suivants montrent la même URL de produit avec et sans le chemin d’accès à la catégorie.

#### URL du produit avec chemin de catégorie

- `http://mystore.com/women/tops-women/hoodies-and-sweatshirts-women/helena-hooded-fleece.html`

#### URL du produit sans chemin d’accès de catégorie

- `http://mystore.com/helena-hooded-fleece.html`

Pour empêcher les moteurs de recherche d’indexer plusieurs URL menant au même contenu, vous pouvez exclure le chemin d’accès à la catégorie de l’URL. Une autre méthode consiste à utiliser une balise meta canonique pour indiquer aux moteurs de recherche les URL à indexer et celles à ignorer. Par défaut, Commerce n’inclut pas le chemin d’accès à la catégorie dans les URL de produits.

## Configuration des URL de catalogue

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en dessous.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Search Engine Optimizations]** et définissez les options suivantes :

   - Définissez **[!UICONTROL Product URL Suffix]** sur `html` ou `htm`. Saisissez le suffixe sans point, car il est appliqué automatiquement.

   - Définissez **[!UICONTROL Category URL Suffix]** sur `html` ou `htm`. Saisissez le suffixe sans point, car il est appliqué automatiquement.

   - Définissez **[!UICONTROL Use Categories Path for Product URLs]** sur vos préférences.

   ![Optimisation du moteur de recherche](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   Pour obtenir la liste détaillée de ces options, voir [Optimisation du moteur de recherche](../configuration-reference/catalog/catalog.md#search-engine-optimization) dans le _Référence de configuration_.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

1. Lorsque vous y êtes invité, cliquez sur le lien **[!UICONTROL Cache Management]** dans le message système et actualisez le cache non valide.

   ![Actualiser le cache](./assets/msg-cache-management.png){width="450" zoomable="yes"}

   Pour plus d’informations sur ces options, voir [Actualiser les caches](../systems/cache-management.md#refresh-specific-caches).

## Configuration du format d’URL de médias de catalogue

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL General]** et choisissez **[!UICONTROL Web]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Url Options]** et définissez les options suivantes :

![Web > Options générales](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

| Champ | [Portée](../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Add Store Code to URLs] | Global | Si les réécritures du serveur web sont activées, l’activation de ce paramètre insère le code de magasin de l’affichage actuel dans l’URL. Options : `Yes` / `No` |
| [!UICONTROL Auto-redirect to Base URL] | Global | (Pour les configurations à magasin unique) En cas de rupture de lien sur votre site, le trafic est redirigé vers l’URL de base plutôt que vers une page contenant un message « Page 404 introuvable ». Options : `No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br /><br />**_Important !_**&#x200B;N’utilisez pas la redirection automatique vers l’URL de base pour les configurations multi-magasin. |
| [!UICONTROL Catalog media URL format] | Global | Définit le format d’URL attribué aux produits et aux catégories. Options : <br />**[!UICONTROL Unique hash per image variant (Legacy mode)]**- Définit le nom de fichier converti comme une valeur de hachage unique.<br />**[!UICONTROL Image optimization based on query parameters]** - Définit le processus [optimisation d’image](../content-design/media-gallery-image-optimization.md) en fonction des paramètres de requête. |

{style="table-layout:auto"}
