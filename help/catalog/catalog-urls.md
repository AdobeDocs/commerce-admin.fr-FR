---
title: URL de catalogue et de produit
description: Découvrez les types de format d’URL de vos produits de catalogue et comment les configurer.
exl-id: 47405dc6-9b5e-4ca8-87eb-5a222de40793
feature: Catalog Management, Products, Search, Categories
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 0%

---

# URL de catalogue et de produit

Les URL que vous affectez aux produits et aux catégories jouent un rôle majeur pour déterminer la façon dont votre site est indexé par les moteurs de recherche. Avant de commencer à créer votre catalogue, prenez en compte les options disponibles. Pour afficher le format d’URL actuel, accédez au storefront et accédez à n’importe quel produit de votre catalogue. Le format de l’URL dépend des paramètres de configuration et de la méthode utilisés pour trouver la page.

## Formats d’URL

### URL dynamique

Une URL dynamique est créée. _à la volée_ et peut inclure une chaîne de requête avec des variables pour l’ID de produit, l’ordre de tri et la page sur laquelle la demande a été effectuée. Lorsqu’un client recherche un produit dans votre boutique, l’URL qui en résulte peut ressembler à ceci :

- `http://mystore.com/catalogsearch/result/?q=racer+back`
- `http://mystore.com/women/tops-women.html?style_general=135`

### URL statique

Une URL statique est une adresse fixe pour une page spécifique. Une URL statique peut être affichée dans un format compatible avec le moteur de recherche ou dans un format qui référence les produits et les catégories par identifiant. Ces URL contiennent des mots que les utilisateurs peuvent utiliser pour rechercher un produit et nécessitent que les réécritures de serveur web soient activées. Les fichiers avec des URL statiques sont généralement utilisés pour les pages de produits et de catégories, les pages de contenu et les [ressources de thème](../content-design/theme-assets.md).

- `http://mystore.com/antonia-racer-tank.html`

## Composants d’URL

### Clé URL

La clé URL fait partie d’une URL statique qui décrit le produit ou la catégorie. Lorsque vous créez un produit ou une catégorie, une clé URL initiale est automatiquement générée, en fonction du nom. Pour modifier la clé d’URL, voir la section [Optimisation du moteur de recherche](product-search-engine-optimization.md) de la section des informations sur les produits.

>[!NOTE]
>
>Les caractères spéciaux accentués sont automatiquement remplacés par leurs versions régulières non accentuées dans la clé URL. Par exemple : `ñ` est automatiquement remplacé par `n`.

La clé URL doit être composée de caractères minuscules avec des tirets non alignés à la fin entre ces caractères et séparés par des mots. Les tirets ne sont pas autorisés au début ou à la fin de la clé URL. Une clé URL bien conçue et &quot;compatible avec les moteurs de recherche&quot; peut inclure le nom du produit et les mots-clés pour améliorer son indexation par les moteurs de recherche. La clé URL peut être configurée pour créer une redirection automatique en cas de modification de la clé URL.

>[!NOTE]
>
>Pour étendre les personnalisations des URL, telles que les URL localisées, voir [URL Rewrites](../merchandising-promotions/url-rewrite.md) pour plus d’informations.

### Suffixe de HTML

Votre catalogue peut être configuré pour inclure ou exclure le suffixe dans les URL de catégorie et de produit. Il existe différentes raisons pour lesquelles les utilisateurs peuvent choisir d’utiliser ou d’omettre le suffixe. Certains pensent que le suffixe n’est plus utile et que les pages sans suffixe sont indexées plus efficacement par les moteurs de recherche. Cependant, votre société peut avoir un format normalisé pour les URL qui nécessitent un suffixe.

Étant donné que le suffixe est contrôlé par la configuration système, vous ne devez jamais le saisir directement dans la clé URL d’une catégorie ou d’un produit. (Cela entraîne un double suffixe à la fin de l’URL.) Que vous décidiez d’utiliser ou non le suffixe, soyez cohérent et utilisez le même paramètre pour toutes vos pages de produits et de catégories. Voici des exemples d’URL avec et sans suffixe.

#### URL avec suffixe de HTML

- `http://mystore.com/helena-hooded-fleece.html`
- `http://mystore.com/helena-hooded-fleece.htm`

#### URL sans suffixe de HTML

- `http://mystore.com/helena-hooded-fleece`

### Chemin de la catégorie

Vous pouvez configurer l’URL pour inclure ou exclure le chemin de catégorie. Par défaut, le chemin de catégorie est inclus dans toutes les pages de catégories et de produits. Les exemples suivants montrent la même URL de produit avec et sans le chemin de catégorie.

#### URL avec chemin de catégorie

- `http://mystore.com/women/tops-women/hoodies-and-sweatshirts-women/helena-hooded-fleece.html`

#### URL sans chemin de catégorie

- `http://mystore.com/helena-hooded-fleece.html`

Pour empêcher les moteurs de recherche d’indexer plusieurs URL menant au même contenu, vous pouvez exclure le chemin de catégorie de l’URL. Une autre méthode consiste à utiliser une méta-balise canonique pour indiquer aux moteurs de recherche quelles URL indexer et lesquelles ignorer. Par défaut, Commerce n’inclut pas le chemin de catégorie dans les URL de produit.

## Configuration des URL de catalogue

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en-dessous.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Search Engine Optimizations]** et définissez les options suivantes :

   - Définir **[!UICONTROL Product URL Suffix]** to `html` ou `htm`. Saisissez le suffixe sans point, car il est automatiquement appliqué.

   - Définir **[!UICONTROL Category URL Suffix]** to `html` ou `htm`. Saisissez le suffixe sans point, car il est automatiquement appliqué.

   - Définir **[!UICONTROL Use Categories Path for Product URLs]** selon vos préférences.

   ![Optimisation du moteur de recherche](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   Pour obtenir la liste détaillée de ces options, voir [Optimisation du moteur de recherche](../configuration-reference/catalog/catalog.md#search-engine-optimization) dans le _Référence de configuration_.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous y êtes invité, cliquez sur l’icône **[!UICONTROL Cache Management]** dans le message système et actualisez le cache non valide.

   ![Actualiser le cache](./assets/msg-cache-management.png){width="450" zoomable="yes"}

   Pour plus d’informations sur ces options, voir [Actualisation des caches](../systems/cache-management.md#refresh-specific-caches).

## Configuration du format d’URL de média de catalogue

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL General]** et choisissez **[!UICONTROL Web]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Url Options]** et définissez les options suivantes :

![Web > Options générales](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

| Champ | [Portée](../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Add Store Code to URLs] | Global | Si les réécritures du serveur web sont activées, l’activation de ce paramètre insère le code de magasin de la vue actuelle dans l’URL. Options : `Yes` / `No` |
| [!UICONTROL Auto-redirect to Base URL] | Global | (Pour les configurations à une seule boutique) En cas de lien rompu sur votre site, le trafic est redirigé vers l’URL de base plutôt que vers une page comportant un message &quot;404 Page introuvable&quot;. Options : `No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br /><br />**_Important !_**N’utilisez pas la redirection automatique vers l’URL de base pour les configurations multi-magasin. |
| [!UICONTROL Catalog media URL format] | Global | Définit le format d’URL affecté aux produits et aux catégories. Options : <br />**[!UICONTROL Unique hash per image variant (Legacy mode)]**- Définit le nom de fichier converti en tant que valeur de hachage unique.<br />**[!UICONTROL Image optimization based on query parameters]** - Définitions [optimisation des images](../content-design/media-gallery-image-optimization.md) en fonction des paramètres de requête. |

{style="table-layout:auto"}
