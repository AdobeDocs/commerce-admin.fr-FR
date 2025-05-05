---
title: Gestion des termes de recherche
description: Découvrez comment gérer les termes de recherche de votre boutique pour rediriger les clients à l’aide de termes mal orthographiés ou alternatifs.
exl-id: e21ece58-2bc2-49ef-96d3-3be930e09f94
feature: Catalog Management, Search
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '1166'
ht-degree: 0%

---

# Gestion des termes de recherche

La [page de destination](../content-design/pages.md) d’un terme de recherche peut être une page de contenu, une page de catégorie, une page de détails du produit ou même une page d’un autre site.

Utilisez des termes de recherche pour capturer les fautes d’orthographe courantes et les rediriger vers la page appropriée. Par exemple, si vous vendez des meubles de patio en fer forgé, vous savez que beaucoup de gens écrivent mal le terme _fer à barre_, ou même _fer pourri_. Vous pouvez saisir chaque mot mal orthographié comme terme de recherche et en faire des synonymes pour _fer forgé_. Même si le mot est mal orthographié, la recherche est dirigée vers la page pour le fer forgé.

Vous pouvez également découvrir ce que vos clients recherchent en examinant les termes de recherche qu’ils utilisent pour trouver des produits dans votre magasin. Si un nombre suffisant de personnes recherchent un produit qui ne figure pas dans votre catalogue, cela peut indiquer une opportunité de vente. En attendant, plutôt que de les laisser les mains vides, vous pouvez les rediriger vers un autre produit de votre catalogue.

## Ajouter des termes de recherche

Au fur et à mesure que vous apprenez de nouveaux mots que les utilisateurs utilisent pour effectuer des recherches dans votre magasin, vous pouvez les ajouter à votre liste de termes de recherche pour diriger les utilisateurs vers les produits qui correspondent le mieux à votre catalogue.

![Grille Termes de recherche](./assets/search-terms.png){width="700" zoomable="yes"}

| Colonne | Description |
|--- |--- |
| [!UICONTROL Search Query] | Requête utilisée pour effectuer la recherche. |
| [!UICONTROL Store] | Magasin dans lequel la requête a été appliquée. |
| [!UICONTROL Results] | Nombre de résultats trouvés par requête. |
| [!UICONTROL Uses] | Nombre d’utilisateurs. |
| [!UICONTROL Redirect URL] | URL de la page cible vers laquelle l’utilisateur a été redirigé après avoir effectué la recherche. |
| [!UICONTROL Suggested Terms] | Détermine si le résultat de la requête affiche les termes suggérés. |
| [!UICONTROL Actions] | Ouvre le produit en mode d&#39;édition. |

{style="table-layout:auto"}

>[!NOTE]
>
>Le nombre de résultats est mis à jour chaque fois qu’un acheteur exécute une recherche à l’aide de cette requête de recherche. Il n’est pas mis à jour si l’un des produits est modifié ou supprimé.

### Ajouter un terme de recherche

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Terms]**.

1. Cliquez sur **[!UICONTROL Add New Search Term]**.

   ![Informations générales sur les termes de recherche](./assets/search-terms-information.png){width="600" zoomable="yes"}

1. Sous _[!UICONTROL General Information]_&#x200B;dans la zone de **[!UICONTROL Search Query]**, saisissez le mot ou l’expression à ajouter en tant que nouveau terme de recherche.

1. Si votre boutique est disponible dans plusieurs langues, choisissez la vue de **[!UICONTROL Store]** applicable.

1. Pour rediriger les résultats de la recherche vers une autre page de votre boutique ou vers un autre site web, saisissez l’URL complète de la page cible dans le champ **[!UICONTROL Redirect URL]** .

1. Si vous souhaitez que ce terme puisse être utilisé comme suggestion chaque fois qu’une recherche ne renvoie aucun résultat, définissez **[!UICONTROL Display in Suggested Terms]** sur `Yes`.

1. Cliquez ensuite sur **[!UICONTROL Save Search]**.

## Modification d’un terme de recherche

1. Dans la grille de _[!UICONTROL Search Terms]_, cliquez sur la ligne d’un enregistrement pour ouvrir le terme de recherche en mode d’édition.

1. Effectuez les modifications nécessaires.

1. Cliquez ensuite sur **[!UICONTROL Save Search]**.

## Suppression d’un terme de recherche

Il existe deux méthodes pour supprimer un terme de recherche : à partir de la grille et sur la page de modification.

**Méthode 1:** dans la grille de _[!UICONTROL Search Terms]_

1. Dans la liste, cochez la case du terme à supprimer.

1. Dans le coin supérieur gauche de la liste, définissez **[!UICONTROL Actions]** sur `Delete`.

1. Cliquez ensuite sur **[!UICONTROL Submit]**.

**Méthode 2:** sur la page _[!UICONTROL Edit a Search Term]_

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Terms]**.

1. Recherchez le terme de recherche à supprimer et ouvrez-le en mode d’édition.

1. Cliquez sur **[!UICONTROL Delete Search]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

## Termes de recherche populaires

Le lien _Termes de recherche_ situé dans le pied de page de votre boutique affiche les termes de recherche utilisés par les visiteurs de votre boutique, classés par popularité. Les termes de recherche s’affichent au format _nuage de balises_, où la taille du texte indique la popularité du terme.

Par défaut, Termes de recherche populaires est activé en tant qu’outil d’optimisation du moteur de recherche, mais n’a aucune connexion directe au processus de recherche catalogue. Comme la page des termes de recherche est indexée par les moteurs de recherche, tous les termes de la page peuvent améliorer le classement dans les moteurs de recherche et la visibilité de votre boutique. L’URL de la page Termes de recherche populaires est : `mystore.com/search/term/popular/`

![Exemple de storefront - termes de recherche populaires](./assets/store-front-search-terms-yoga-pants.png){width="600" zoomable="yes"}

**_Pour configurer des termes de recherche populaires, procédez comme suit_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en dessous.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Search Engine Optimization]** .

   ![Configuration du catalogue - Optimisation du moteur de recherche](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   Pour obtenir la liste détaillée de ces options, voir [Optimisation du moteur de recherche](../configuration-reference/catalog/catalog.md#search-engine-optimization) dans le _Référence de configuration_.

1. Définissez **[!UICONTROL Popular Search Terms]** selon vos besoins.

   Si nécessaire, décochez la case **[!UICONTROL Use system value]** pour modifier ce paramètre.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Vous pouvez configurer plus en détail la mise en cache des recherches de catalogue [populaires](search-configuration.md).

## Rechercher des synonymes

L’une des manières d’améliorer l’efficacité de la [recherche catalogue](search-configuration.md) consiste à inclure différents termes que les utilisateurs peuvent utiliser pour décrire un même élément. Vous ne voulez pas perdre une vente juste parce que quelqu&#39;un recherche un _canapé_, et votre produit est répertorié comme un _canapé_. Vous pouvez capturer un plus large éventail de termes de recherche en saisissant _canapé_, _davenport_ et _lovesseat_ comme synonymes de _canapé_, puis en les dirigeant vers la même page de destination.

Adobe Commerce prend en charge deux solutions de gestion des synonymes différentes :

- La fonctionnalité Live Search [Synonymes](https://experienceleague.adobe.com/docs/commerce/live-search/live-search-admin/synonyms/synonyms.html?lang=fr) est disponible pour les installations d’Adobe Commerce sur lesquelles Live Search est installé.
- La fonctionnalité standard Synonymes de recherche (décrite dans cette page) est disponible par défaut pour toutes les installations d’Adobe Commerce.

>[!NOTE]
>
>La fonctionnalité standard Synonymes de recherche prend en charge les attributs de produit `name` et `sku` **_uniquement_**.

>[!IMPORTANT]
>
>La fonction de recherche de synonymes utilise uniquement une méthode de recherche de correspondance de texte intégral.

![Exemple de storefront - résultats de recherche avec synonymes](./assets/storefront-search-results-synonyms.png){width="700" zoomable="yes"}

### Créer un groupe de synonymes

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Synonyms]**.

   La grille de _[!UICONTROL Search Synonyms]_&#x200B;s’affiche. Si c’est la première fois que vous utilisez des synonymes de recherche, la grille est vide.

   ![Grille des synonymes de recherche](./assets/search-synonyms-grid-empty.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL New Synonym Group]**.

   ![Nouveau groupe de synonymes de recherche](./assets/search-synonym-group-new.png){width="700" zoomable="yes"}

1. Définissez **[!UICONTROL Scope]** sur les vues du magasin où s’appliquent les synonymes.

1. Saisissez chaque synonyme dans le groupe, en les séparant par des virgules. Choisissez des mots que les utilisateurs peuvent utiliser comme critères de recherche. Par exemple :

   - `sweatshirt, sweat shirt, hoodie, fleece`
   - `cell phone, mobile phone, smart phone`
   - `couch, sofa, davenport`
   - `wrought iron, rot iron, rod iron`

1. Pour fusionner ces synonymes dans un groupe avec d’autres qui ont la même portée, cochez la case **[!UICONTROL Merge existing synonyms]** .

1. Cliquez ensuite sur **[!UICONTROL Save Synonym Group]**.

### Modification d’un groupe de synonymes

1. Dans la grille de _[!UICONTROL Search Synonyms]_, cliquez sur la ligne d’un enregistrement pour ouvrir le groupe de synonymes en mode d’édition.

1. Effectuez les modifications nécessaires.

1. Cliquez ensuite sur **[!UICONTROL Save Synonym Group]**.

### Suppression d’un groupe de synonymes

Vous pouvez supprimer un groupe de synonymes de la grille et de la page d’édition selon deux méthodes.

**Méthode 1 :** dans la grille des synonymes de recherche

1. Dans la grille de _[!UICONTROL Search Synonyms]_, cochez la case du groupe à supprimer.

1. Dans le coin supérieur gauche de la liste, définissez **[!UICONTROL Actions]** sur `Delete`.

1. Cliquez ensuite sur **[!UICONTROL Submit]**.

**Méthode 2 :** sur la page Modifier un groupe de synonymes

1. Dans la grille Rechercher des synonymes , cliquez sur la ligne d’un enregistrement pour ouvrir le groupe de synonymes en mode d’édition.

1. Cliquez sur **[!UICONTROL Delete Synonym Group]**.

1. Lorsque vous y êtes invité, confirmez la suppression du groupe.

## Rapport Termes de recherche

Le rapport Termes de recherche affiche le nombre de résultats pour chaque terme et le nombre de fois (accès) où le terme a été utilisé. Les données du rapport peuvent être filtrées par terme, magasin, résultats et accès, puis exportées pour une analyse plus approfondie.

### Afficher le rapport

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Search Terms]**.

1. Utilisez les commandes pour filtrer le rapport selon vos besoins.

   ![Rapport Termes de recherche](./assets/search-terms-report.png){width="700" zoomable="yes"}

## Exporter le rapport

1. Par **[!UICONTROL Export to]**, choisissez un format d’exportation :

   - `CSV` - Fichier de valeurs séparées par des virgules contenant des données en texte brut
   - `Excel XML` - Format de données de feuille de calcul XML

1. Cliquez sur **[!UICONTROL Export]**.

   Le fichier généré est automatiquement enregistré dans le dossier désigné pour les téléchargements.

### Colonnes du rapport

| Colonne | Description |
|--- |--- |
| [!UICONTROL ID] | Identifiant numérique unique généré pour l’entrée du terme de recherche |
| [!UICONTROL Search Query] | Requête utilisée pour effectuer la recherche |
| [!UICONTROL Store] | Magasin dans lequel la requête de recherche a été appliquée |
| [!UICONTROL Results] | Nombre de résultats |
| [!UICONTROL Hits] | Nombre d’utilisateurs |

{style="table-layout:auto"}
