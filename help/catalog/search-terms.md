---
title: Gestion des termes de recherche
description: Découvrez comment gérer les termes de recherche pour que votre boutique redirige les clients à l’aide de termes mal orthographiés ou alternatifs.
exl-id: e21ece58-2bc2-49ef-96d3-3be930e09f94
feature: Catalog Management, Search
source-git-commit: 6126943f20f33d52085018ca634159918833efc9
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 0%

---

# Gestion des termes de recherche

La variable [landing page](../content-design/pages.md) pour un terme de recherche, il peut s’agir d’une page de contenu, d’une page de catégorie, d’une page des détails d’un produit ou même d’une page sur un autre site.

Utilisez les termes de recherche pour capturer les fautes d’orthographe courantes et les rediriger vers la page appropriée. Par exemple, si vous vendez des meubles de terrasse en fer forgé, vous savez que beaucoup de gens orthographient le terme comme _barre_, ou même _fer pourri_. Vous pouvez saisir chaque mot mal orthographié comme terme de recherche et en faire des synonymes pour _fer forgé_. Même si le mot est mal orthographié, la recherche est dirigée vers la page pour le fer forgé.

Vous pouvez également découvrir ce que recherchent vos clients en examinant les termes de recherche qu’ils utilisent pour trouver des produits dans votre boutique. Si suffisamment de personnes recherchent un produit qui ne figure pas dans votre catalogue, cela peut indiquer une opportunité de vente. Pendant ce temps, plutôt que de les laisser vides, vous pouvez les rediriger vers un autre produit de votre catalogue.

## Ajout de termes de recherche

À mesure que vous découvrez les nouveaux mots que les visiteurs utilisent pour effectuer des recherches dans votre boutique, vous pouvez les ajouter à votre liste de termes de recherche afin d’orienter les personnes vers les produits qui correspondent le mieux à votre catalogue.

![Grille Termes de recherche](./assets/search-terms.png){width="700" zoomable="yes"}

| Colonne | Description |
|--- |--- |
| [!UICONTROL Search Query] | Requête utilisée pour effectuer la recherche. |
| [!UICONTROL Store] | Magasin dans lequel la requête de recherche a été appliquée. |
| [!UICONTROL Results] | Nombre de résultats trouvés par requête. |
| [!UICONTROL Uses] | Nombre d’utilisations. |
| [!UICONTROL Redirect URL] | URL de la page cible vers laquelle l’utilisateur a été redirigé après avoir effectué la recherche. |
| [!UICONTROL Suggested Terms] | Détermine si le résultat de la requête affiche les termes suggérés. |
| [!UICONTROL Actions] | Ouvre le produit en mode d’édition. |

{style="table-layout:auto"}

>[!NOTE]
>
>Le nombre de résultats est mis à jour chaque fois qu’un acheteur exécute une recherche à l’aide de cette requête de recherche. Elle n’est pas mise à jour si l’un des produits est modifié ou supprimé.

### Ajout d’un terme de recherche

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Terms]**.

1. Cliquez sur **[!UICONTROL Add New Search Term]**.

   ![Informations générales sur les termes de recherche](./assets/search-terms-information.png){width="600" zoomable="yes"}

1. Sous _[!UICONTROL General Information]_dans le **[!UICONTROL Search Query]**, saisissez le mot ou l’expression à ajouter comme nouveau terme de recherche.

1. Si votre boutique est disponible en plusieurs langues, choisissez la **[!UICONTROL Store]** vue.

1. Pour rediriger les résultats de la recherche vers une autre page de votre boutique ou vers un autre site web, saisissez l’URL complète de la page cible dans la variable **[!UICONTROL Redirect URL]** champ .

1. Si vous souhaitez que ce terme puisse être utilisé comme suggestion lorsqu’une recherche ne renvoie aucun résultat, définissez **[!UICONTROL Display in Suggested Terms]** to `Yes`.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Search]**.

## Modification d’un terme de recherche

1. Dans le _[!UICONTROL Search Terms]_grille, cliquez sur la ligne d’un enregistrement pour ouvrir le terme de recherche en mode d’édition.

1. Effectuez les modifications nécessaires.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Search]**.

## Suppression d’un terme de recherche

Il existe deux méthodes pour supprimer un terme de recherche : la grille et la page d’édition.

**Méthode 1 :** Dans le _[!UICONTROL Search Terms]_grid

1. Dans la liste, cochez la case du terme à supprimer.

1. Dans le coin supérieur gauche de la liste, définissez **[!UICONTROL Actions]** to `Delete`.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Submit]**.

**Méthode 2 :** Sur le _[!UICONTROL Edit a Search Term]_page

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Terms]**.

1. Recherchez le terme de recherche à supprimer et ouvrez-le en mode d’édition.

1. Cliquez sur **[!UICONTROL Delete Search]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

## Termes de recherche populaires

La variable _Termes de recherche_ dans le pied de page de votre boutique affiche les termes de recherche utilisés par les visiteurs de votre boutique, classés par popularité. Les termes de recherche apparaissent dans un _nuage de balises_ format, où la taille du texte indique la popularité du terme.

Par défaut, les termes de recherche populaire sont activés en tant qu’outil d’optimisation du moteur de recherche, mais n’ont aucune connexion directe au processus de recherche catalogue. La page Termes de recherche étant indexée par les moteurs de recherche, tous les termes de la page peuvent améliorer le classement de votre moteur de recherche et la visibilité de votre boutique. L’URL de la page Termes de recherche populaires est la suivante : `mystore.com/search/term/popular/`

![Exemple de storefront - termes de recherche courants](./assets/store-front-search-terms-yoga-pants.png){width="600" zoomable="yes"}

**_Pour configurer les termes de recherche courants :_**

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en-dessous.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Search Engine Optimization]** .

   ![Configuration du catalogue - optimisation du moteur de recherche](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   Pour obtenir la liste détaillée de ces options, voir [Optimisation du moteur de recherche](../configuration-reference/catalog/catalog.md#search-engine-optimization) dans le _Référence de configuration_.

1. Définir **[!UICONTROL Popular Search Terms]** selon les besoins.

   Si nécessaire, effacez la variable **[!UICONTROL Use system value]** pour modifier ce paramètre.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Vous pouvez configurer la mise en cache des [recherches de catalogue](search-configuration.md).

## Recherche de synonymes

Un moyen d’améliorer l’efficacité de la variable [recherche catalogue](search-configuration.md) est d’inclure des termes différents que les utilisateurs peuvent utiliser pour décrire le même élément. Vous ne voulez pas perdre une vente juste parce que quelqu&#39;un cherche une _sofa_, et votre produit est répertorié en tant que _canapé_. Vous pouvez capturer un plus large éventail de termes de recherche en saisissant _sofa_, _davenport_, et _loveseat_ comme synonymes de _canapé_ et dirigez-les vers la même page d’entrée.

Adobe Commerce prend en charge deux solutions de gestion des synonymes différentes :

- Recherche en direct [Synonymes](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/synonyms/synonyms.html) Cette fonctionnalité est disponible pour les installations Adobe Commerce où la recherche en direct est installée.
- La fonctionnalité Synonymes de recherche standard (décrite dans cette page) est disponible en standard pour toutes les installations Adobe Commerce.

>[!NOTE]
>
>La fonction d’usine Synonymes de recherche standard prend en charge `name` et `sku` attributs de produit **_only_**.

![Exemple de storefront : résultats de recherche avec des synonymes](./assets/storefront-search-results-synonyms.png){width="700" zoomable="yes"}

### Créer un groupe de synonymes

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Synonyms]**.

   La variable _[!UICONTROL Search Synonyms]_grid apparaît. Si c’est la première fois que vous utilisez des synonymes de recherche, la grille est vide.

   ![Rechercher une grille de synonymes](./assets/search-synonyms-grid-empty.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL New Synonym Group]**.

   ![Nouveau groupe de synonymes de recherche](./assets/search-synonym-group-new.png){width="700" zoomable="yes"}

1. Définir **[!UICONTROL Scope]** aux vues des magasins dans lesquelles les synonymes s’appliquent.

1. Saisissez chaque synonyme dans le groupe, séparé par une virgule. Choisissez des mots que les utilisateurs peuvent utiliser comme critères de recherche. Par exemple :

   - `sweatshirt, sweat shirt, hoodie, fleece`
   - `cell phone, mobile phone, smart phone`
   - `couch, sofa, davenport`
   - `wrought iron, rot iron, rod iron`

1. Pour fusionner ces synonymes en un groupe avec d’autres qui ont la même portée, sélectionnez la variable **[!UICONTROL Merge existing synonyms]** .

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Synonym Group]**.

### Modification d’un groupe de synonymes

1. Dans le _[!UICONTROL Search Synonyms]_grille, cliquez sur la ligne d’un enregistrement pour ouvrir le groupe de synonymes en mode d’édition.

1. Effectuez les modifications nécessaires.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Synonym Group]**.

### Suppression d’un groupe de synonymes

Il existe deux méthodes pour supprimer un groupe de synonymes : à partir de la grille et sur la page d’édition.

**Méthode 1 :** Dans la grille Synonymes de recherche

1. Dans le _[!UICONTROL Search Synonyms]_grid, cochez la case du groupe à supprimer.

1. Dans le coin supérieur gauche de la liste, définissez **[!UICONTROL Actions]** to `Delete`.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Submit]**.

**Méthode 2 :** Sur la page Modifier un groupe de synchronisation

1. Dans la grille Search Synonymes , cliquez sur la ligne d’un enregistrement pour ouvrir le groupe de synonymes en mode d’édition.

1. Cliquez sur **[!UICONTROL Delete Synonym Group]**.

1. Lorsque vous y êtes invité, confirmez la suppression du groupe.

## Rapport Termes de recherche

Le rapport Termes de recherche indique le nombre de résultats pour chaque terme et le nombre de fois (accès) où le terme a été utilisé. Les données du rapport peuvent être filtrées par terme, par magasin, par résultats et par accès, puis exportées pour une analyse plus approfondie.

### Afficher le rapport

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Search Terms]**.

1. Utilisez les contrôles pour filtrer le rapport selon vos besoins.

   ![Rapport Termes de recherche](./assets/search-terms-report.png){width="700" zoomable="yes"}

## Exporter le rapport

1. Pour **[!UICONTROL Export to]**, choisissez un format d&#39;export :

   - `CSV` : fichier de valeurs séparées par des virgules contenant des données de texte brut
   - `Excel XML` - Un format de données de feuille de calcul XML

1. Cliquez sur **[!UICONTROL Export]**.

   Le fichier généré est automatiquement enregistré dans le dossier désigné pour les téléchargements.

### Colonnes de rapport

| Colonne | Description |
|--- |--- |
| [!UICONTROL ID] | Identifiant numérique unique généré pour la saisie de terme de recherche. |
| [!UICONTROL Search Query] | Requête utilisée pour effectuer la recherche |
| [!UICONTROL Store] | Magasin dans lequel la requête de recherche a été appliquée |
| [!UICONTROL Results] | Nombre de résultats |
| [!UICONTROL Hits] | Nombre d’utilisations |

{style="table-layout:auto"}
