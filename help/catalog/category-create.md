---
title: Créer des catégories
description: Vous pouvez créer autant de sous-catégories supplémentaires que nécessaire, en fonction de la profondeur maximale de menu définie dans la configuration.
exl-id: 8ba5fc1a-3bf2-4a29-bbc3-709fc0ad7497
feature: Catalog Management, Categories
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 0%

---

# Créer des catégories

La structure de catégorie de votre catalogue est semblable à une arborescence ascendante, avec la racine en haut. Chaque section de l’arborescence peut être développée et réduite. Toutes les catégories désactivées ou masquées sont grisées. Les catégories au premier niveau (sous le [root](category-root.md)) apparaît généralement sous la forme d’options dans la variable [menu principal](navigation-top.md). Vous pouvez créer autant de sous-catégories supplémentaires que nécessaire, en fonction de la profondeur maximale de menu définie dans la configuration. Les catégories peuvent être glissées-déposées vers d’autres emplacements de l’arborescence. Le numéro d’ID de catégorie apparaît entre parenthèses après le nom de la catégorie en haut de la page.

Pour un site web avec plusieurs [stores](../stores-purchase/stores.md#add-stores), vous pouvez créer une catégorie racine différente pour chaque magasin qui définit le jeu de catégories utilisé pour le [navigation supérieure](navigation-top.md).

![Arborescence de catégories](./assets/category-selected.png){width="700" zoomable="yes"}

## Bonnes pratiques

Utilisez ces bonnes pratiques lorsque vous planifiez et créez des catégories.

### Structure de catégorie

La structure des catégories dans le menu principal peut avoir un impact sur l’expérience client et les performances. Il est recommandé d’identifier une catégorie globale de niveau supérieur et d’éviter d’avoir d’autres catégories portant le même nom. Par exemple, plutôt que d’avoir plusieurs catégories pour &quot;Enfants&quot; organisées sous différents services, comme `Clothing/Kids`, `Shoes/Kids`, `Accessories/Kids`. Il peut être plus efficace de rendre la catégorie parent de niveau supérieur `Kids`, puis créez des sous-catégories selon les besoins ci-dessous. Respectez la structure des catégories et appliquez la même approche pour tous les types de produits de votre catalogue.

### Règles métier et automatisation

Tenez compte de la structure de catégorie et des valeurs d’attribut disponibles lorsque vous utilisez la logique métier pour afficher des éléments similaires sur une page de catalogue ou pour configurer une promotion personnalisée, un processus automatisé ou des critères de recherche. Par exemple, si vous spécifiez &quot;polo&quot; comme catégorie parente, les résultats peuvent inclure des produits mixtes et inappropriés selon l’âge. Cependant, si vous faites correspondre une sous-catégorie spécifique de chemises de polo, les résultats sont plus étroits et susceptibles de plaire à un client spécifique. Les résultats peuvent être encore plus spécifiques lorsqu’ils sont combinés avec d’autres valeurs d’attribut qui ciblent un client spécifique. Tenez compte du nombre de produits qui doivent être filtrés et récupérés lors du référencement d’un chemin de catégorie spécifique. La différence de résultats peut être spectaculaire. Tenez compte des différents résultats renvoyés par les chemins de catégorie suivants :

- `[Category:  All Products/Shirts/Father's Day/Polos/Sale]`
- `[Category Path: Men/Shirts/Polos]`
- `[Child Category: Polos]`

Il est important de définir clairement les relations catégoriques, par exemple :

- catégorie parente
- sous-catégorie
- chemin de catégorie

Définissez également les mots-clés et attributs associés, tels que :

- disponibilité
- prix de vente
- marque
- size
- color

## Etape 1 : créer une catégorie

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Définir **[!UICONTROL Store View]** pour déterminer où se trouve la nouvelle catégorie.

1. Dans l&#39;arborescence des catégories, sélectionnez la catégorie parente de la nouvelle catégorie.

   Le parent est à un niveau au-dessus de la nouvelle catégorie.

   Si vous commencez par le début sans aucune donnée, il peut y avoir seulement deux catégories dans la liste : _Catégorie par défaut_, qui est la racine, et un _Exemple de catégorie_

1. Cliquez sur **[!UICONTROL Add Subcategory]**.

## Etape 2 : renseigner les informations de base

1. Si vous souhaitez que la catégorie soit immédiatement disponible dans le magasin, définissez **[!UICONTROL Enable Category]** to `Yes`.

1. Pour inclure la catégorie dans la variable [navigation supérieure](navigation-top.md), définit **[!UICONTROL Include in Menu]** to `Yes`.

1. Saisissez le **[!UICONTROL Category Name]**.

   ![Informations de base sur les catégories](./assets/catalog-categories-currently-active.png){width="500" zoomable="yes"}

1. click **[!UICONTROL Save]** et continuez.

## Etape 3 : renseigner le contenu de la catégorie

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Content]** .

   ![Contenu de catégorie](./assets/category-content.png){width="600" zoomable="yes"}

1. Pour afficher un **[!UICONTROL Category Image]** dans la partie supérieure de la page, vous pouvez télécharger votre propre image ou utiliser une image qui existe dans la variable [Stockage multimédia](../content-design/media-storage.md).

   - Pour charger votre propre image, cliquez sur **[!UICONTROL Upload]** et choisissez l’image que vous souhaitez représenter la catégorie.

   - Pour utiliser des images à partir du stockage multimédia, cliquez sur **[!UICONTROL Select from Gallery]** et sélectionnez l’image que vous souhaitez représenter la catégorie.

   >[!NOTE]
   >
   >Dans la galerie de médias, vous pouvez également utiliser le [Intégration Adobe Stock](../content-design/adobe-stock.md) pour rechercher une image appropriée en cliquant sur **[!UICONTROL Search Adobe Stock]**.

1. Pour **[!UICONTROL Description]**, saisissez le texte ou tout autre contenu que vous souhaitez afficher sur la landing page de catégorie.

   Pour plus d’informations, voir [Contenu de catégorie](categories-content-settings.md).

1. Pour inclure un bloc de contenu dans la landing page de catégorie, sélectionnez l&#39;option **[!UICONTROL CMS Block]** que vous voulez voir apparaître.

1. click **[!UICONTROL Save]** et continuez.

## Étape 4 : Définition des paramètres d’affichage

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Display Setting]** .

   ![Paramètres d’affichage](./assets/category-display-settings.png){width="600" zoomable="yes"}

   Pour plus d’informations sur ces options, voir Pour plus d’informations sur ces options, voir  [Paramètres d’affichage](categories-display-settings.md).

1. Définir **[!UICONTROL Display Mode]** à l’une des options suivantes :

   - `Products Only`
   - `Static Block Only`
   - `Static Block and Products`

1. Si vous souhaitez que la page de catégorie contienne le _`Filter by Attribute`_de la navigation par couches, définie **[!UICONTROL Anchor]**to `Yes`.

1. Pour le **[!UICONTROL Available Product Listing Sort By]** , sélectionnez une ou plusieurs des valeurs disponibles pour que les clients puissent trier la liste. Ce paramètre ne s’applique pas à la variable [!DNL Live Search] [Widget de page de liste de produits](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling).

   Par défaut, toutes les valeurs disponibles sont incluses. Désélectionnez l’option **[!UICONTROL Use All]** pour modifier les sélections. Par exemple, les valeurs peuvent inclure :

   - `Position`
   - `Product Name`
   - `Price`

1. Pour définir l’ordre de tri par défaut de la catégorie, choisissez le **[!UICONTROL Default Product Listing Sort By]** . Ce paramètre ne s’applique pas à la variable [!DNL Live Search] [Widget de page de liste de produits](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling).

1. Pour modifier la navigation par couche par défaut [étape de prix](navigation-layered.md#configure-price-navigation) , procédez comme suit :

   - Désélectionnez l’option **[!UICONTROL Use Config Settings]** .

   - Saisissez la valeur à utiliser comme étape de prix incrémentielle pour la navigation par couches.

1. Cliquez sur **[!UICONTROL Save]** et continuez.

## Étape 5 : Définition des paramètres d’optimisation du moteur de recherche

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Search Engine Optimization Settings]** .

   ![Optimisation du moteur de recherche](./assets/categories-search-engine-optimization.png){width="600" zoomable="yes"}

   Pour plus d’informations sur ces options, voir [Optimisation du moteur de recherche](categories-search-engine-optimization.md).

1. Procédez comme suit : [métadonnées](../merchandising-promotions/meta-data.md) pour la catégorie :

   - [!UICONTROL Meta Title]
   - [!UICONTROL Meta Keywords]
   - [!UICONTROL Meta Description]

1. Cliquez sur **[!UICONTROL Save]** et continuez.

## Etape 6 : Sélection des produits dans la catégorie

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Products in Category]** .

   ![Produits dans la catégorie](./assets/category-products-in-category.png){width="600" zoomable="yes"}

   Pour plus d’informations sur ces options, voir [Produits dans la catégorie](categories-product-assignments.md).

1. Si nécessaire, utilisez la méthode [filtres](../getting-started/admin-grid-controls.md) pour trouver les produits.

   Pour afficher tous les enregistrements qui ne sont pas encore inclus dans la catégorie, définissez le sélecteur d’enregistrements dans la première colonne sur `No` et cliquez sur **[!UICONTROL Search]**.

1. Dans la première colonne, cochez la case correspondant à chaque produit à inclure dans la catégorie.

1. Cliquez sur **[!UICONTROL Save]** et continuez.

## Étape 7 : définition des autorisations de catégorie

{{ee-feature}}

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Category Permissions]** .

1. Pour une installation multi-site, choisissez la méthode **[!UICONTROL Website]** où les autorisations de catégorie s’appliquent.

1. Choisissez la **[!UICONTROL Customer Group]** où les autorisations de catégorie s’appliquent.

   ![Adobe Commerce B2B](../assets/b2b.svg) ([Adobe Commerce B2B](../b2b/introduction.md) uniquement) Si nécessaire, vous pouvez choisir un **[!UICONTROL Shared Catalog]** au lieu de .

1. Définissez les autorisations suivantes selon vos besoins :

   - [!UICONTROL Browsing Category]
   - [!UICONTROL Display Product Prices]
   - [!UICONTROL Add to Cart]

1. Pour ajouter une autre règle d’autorisation, cliquez sur **[!UICONTROL New Permission]** et répétez le processus.

   ![Autorisations de catégorie](./assets/category-create-permissions.png){width="600" zoomable="yes"}

## Étape 8 : Définition des paramètres de conception

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Design]** .

1. Définissez les paramètres de conception selon vos besoins :

   - ([Adobe Commerce B2B](../b2b/introduction.md) uniquement) Pour appliquer les paramètres de conception de catégorie parente à cette catégorie, définissez **[!UICONTROL Use Parent Category Settings]** to `Yes`.

   - Pour modifier la conception des pages de catégorie, choisissez la variable **[!UICONTROL Theme]** que vous souhaitez postuler.

   - Pour modifier la mise en page des colonnes des pages de catégories, choisissez la variable **[!UICONTROL Layout]** que vous souhaitez postuler.

   - Pour entrer du code personnalisé, saisissez un code XML valide dans la variable **[!UICONTROL Layout Update XML]** de la boîte.

   - Pour utiliser la même conception pour les pages de produits, définissez **[!UICONTROL Apply Design to Products]** to `Yes`.

   ![Paramètres de conception](./assets/category-design.png){width="600" zoomable="yes"}

1. ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Pour planifier la mise à jour de la conception pour une période spécifique, procédez comme suit :

   - Développez l’objet _[!UICONTROL Schedule Design Update]_.

   - Utilisez le calendrier (![Icône Calendrier](../assets/icon-calendar.png)) pour choisir la mise à jour de la planification **[!UICONTROL from]** et **[!UICONTROL to]** dates.

   ![Mise à jour planifiée de la conception](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.
