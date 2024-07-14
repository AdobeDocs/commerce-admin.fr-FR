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

La structure de catégorie de votre catalogue est semblable à une arborescence ascendante, avec la racine en haut. Chaque section de l’arborescence peut être développée et réduite. Toutes les catégories désactivées ou masquées sont grisées. Les catégories au premier niveau (sous la [root](category-root.md)) s’affichent généralement sous la forme d’options dans le [menu principal](navigation-top.md). Vous pouvez créer autant de sous-catégories supplémentaires que nécessaire, en fonction de la profondeur maximale de menu définie dans la configuration. Les catégories peuvent être glissées-déposées vers d’autres emplacements de l’arborescence. Le numéro d’ID de catégorie apparaît entre parenthèses après le nom de la catégorie en haut de la page.

Pour un site web comportant plusieurs [magasins](../stores-purchase/stores.md#add-stores), vous pouvez créer une catégorie racine différente pour chaque magasin qui définit l’ensemble de catégories utilisées pour la [navigation supérieure](navigation-top.md).

![Arborescence de catégorie](./assets/category-selected.png){width="700" zoomable="yes"}

## Bonnes pratiques

Utilisez ces bonnes pratiques lorsque vous planifiez et créez des catégories.

### Structure de catégorie

La structure des catégories dans le menu principal peut avoir un impact sur l’expérience client et les performances. Il est recommandé d’identifier une catégorie globale de niveau supérieur et d’éviter d’avoir d’autres catégories portant le même nom. Par exemple, plutôt que d’avoir plusieurs catégories pour &quot;Enfants&quot; organisées sous différents services, comme `Clothing/Kids`, `Shoes/Kids`, `Accessories/Kids`. Il peut être plus efficace de créer la catégorie parente de niveau supérieur `Kids`, puis de créer des sous-catégories selon les besoins ci-dessous. Respectez la structure des catégories et appliquez la même approche pour tous les types de produits de votre catalogue.

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

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Définissez **[!UICONTROL Store View]** pour déterminer où la nouvelle catégorie doit être disponible.

1. Dans l&#39;arborescence des catégories, sélectionnez la catégorie parente de la nouvelle catégorie.

   Le parent est à un niveau au-dessus de la nouvelle catégorie.

   Si vous commencez à partir du début sans aucune donnée, il peut y avoir seulement deux catégories dans la liste : _Catégorie par défaut_, qui est la racine, et une _catégorie d’exemple_

1. Cliquez sur **[!UICONTROL Add Subcategory]**.

## Etape 2 : renseigner les informations de base

1. Si vous souhaitez que la catégorie soit immédiatement disponible dans le magasin, définissez **[!UICONTROL Enable Category]** sur `Yes`.

1. Pour inclure la catégorie dans la [navigation supérieure](navigation-top.md), définissez **[!UICONTROL Include in Menu]** sur `Yes`.

1. Saisissez le **[!UICONTROL Category Name]**.

   ![Informations de base sur la catégorie](./assets/catalog-categories-currently-active.png){width="500" zoomable="yes"}

1. cliquez sur **[!UICONTROL Save]** et continuez.

## Etape 3 : renseigner le contenu de la catégorie

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Content]** .

   ![Contenu de catégorie](./assets/category-content.png){width="600" zoomable="yes"}

1. Pour afficher un **[!UICONTROL Category Image]** en haut de la page, vous pouvez télécharger votre propre image ou utiliser une image qui existe dans le [stockage multimédia](../content-design/media-storage.md).

   - Pour télécharger votre propre image, cliquez sur **[!UICONTROL Upload]** et choisissez l’image que vous souhaitez représenter la catégorie.

   - Pour utiliser les images du stockage multimédia, cliquez sur **[!UICONTROL Select from Gallery]** et sélectionnez l’image à représenter dans la catégorie.

   >[!NOTE]
   >
   >Dans la galerie de médias, vous pouvez également utiliser l’ [intégration Adobe Stock](../content-design/adobe-stock.md) pour trouver une image appropriée en cliquant sur **[!UICONTROL Search Adobe Stock]**.

1. Pour **[!UICONTROL Description]**, saisissez le texte ou tout autre contenu que vous souhaitez afficher sur la page d’entrée de la catégorie.

   Pour plus d’informations, voir [Contenu de catégorie](categories-content-settings.md).

1. Pour inclure un bloc de contenu sur la page d&#39;entrée de la catégorie, choisissez le **[!UICONTROL CMS Block]** que vous souhaitez afficher.

1. cliquez sur **[!UICONTROL Save]** et continuez.

## Étape 4 : Définition des paramètres d’affichage

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Display Setting]** .

   ![Paramètres d’affichage](./assets/category-display-settings.png){width="600" zoomable="yes"}

   Pour plus d’informations sur ces options, voir Pour plus d’informations sur ces options, voir [Paramètres d’affichage](categories-display-settings.md).

1. Définissez **[!UICONTROL Display Mode]** sur l’une des options suivantes :

   - `Products Only`
   - `Static Block Only`
   - `Static Block and Products`

1. Si vous souhaitez que la page de catégorie inclut la section _`Filter by Attribute`_de la navigation superposée, définissez **[!UICONTROL Anchor]**sur `Yes`.

1. Pour les options **[!UICONTROL Available Product Listing Sort By]**, sélectionnez une ou plusieurs des valeurs disponibles pour que les clients puissent trier la liste. Ce paramètre ne s’applique pas au [!DNL Live Search] [ ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling) Widget de page de liste de produits.

   Par défaut, toutes les valeurs disponibles sont incluses. Décochez la case **[!UICONTROL Use All]** pour modifier les sélections. Par exemple, les valeurs peuvent inclure :

   - `Position`
   - `Product Name`
   - `Price`

1. Pour définir l’ordre de tri par défaut pour la catégorie, choisissez la valeur **[!UICONTROL Default Product Listing Sort By]**. Ce paramètre ne s’applique pas au [!DNL Live Search] [ ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling) Widget de page de liste de produits.

1. Pour modifier le paramètre de navigation par défaut [price step](navigation-layered.md#configure-price-navigation) , procédez comme suit :

   - Décochez la case **[!UICONTROL Use Config Settings]** .

   - Saisissez la valeur à utiliser comme étape de prix incrémentielle pour la navigation par couches.

1. Cliquez sur **[!UICONTROL Save]** et continuez.

## Étape 5 : Définition des paramètres d’optimisation du moteur de recherche

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Search Engine Optimization Settings]** .

   ![Optimisation du moteur de recherche](./assets/categories-search-engine-optimization.png){width="600" zoomable="yes"}

   Pour plus d’informations sur ces options, voir [Optimisation du moteur de recherche](categories-search-engine-optimization.md).

1. Renseignez les [métadonnées](../merchandising-promotions/meta-data.md) suivantes pour la catégorie :

   - [!UICONTROL Meta Title]
   - [!UICONTROL Meta Keywords]
   - [!UICONTROL Meta Description]

1. Cliquez sur **[!UICONTROL Save]** et continuez.

## Etape 6 : Sélection des produits dans la catégorie

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Products in Category]** .

   ![Produits dans la catégorie](./assets/category-products-in-category.png){width="600" zoomable="yes"}

   Pour plus d’informations sur ces options, voir [Produits dans la catégorie](categories-product-assignments.md).

1. Si nécessaire, utilisez les [filtres](../getting-started/admin-grid-controls.md) pour rechercher les produits.

   Pour afficher tous les enregistrements qui ne sont pas encore inclus dans la catégorie, définissez le programme de sélection des enregistrements dans la première colonne sur `No` et cliquez sur **[!UICONTROL Search]**.

1. Dans la première colonne, cochez la case correspondant à chaque produit à inclure dans la catégorie.

1. Cliquez sur **[!UICONTROL Save]** et continuez.

## Étape 7 : définition des autorisations de catégorie

{{ee-feature}}

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Category Permissions]** .

1. Pour une installation multi-site, sélectionnez l’ **[!UICONTROL Website]** où les autorisations de catégorie s’appliquent.

1. Sélectionnez l’ **[!UICONTROL Customer Group]** où s’appliquent les autorisations de catégorie.

   ![Adobe Commerce B2B](../assets/b2b.svg) ([Adobe Commerce B2B](../b2b/introduction.md) uniquement) Si nécessaire, vous pouvez choisir un **[!UICONTROL Shared Catalog]** à la place.

1. Définissez les autorisations suivantes selon vos besoins :

   - [!UICONTROL Browsing Category]
   - [!UICONTROL Display Product Prices]
   - [!UICONTROL Add to Cart]

1. Pour ajouter une autre règle d’autorisation, cliquez sur **[!UICONTROL New Permission]** et répétez le processus.

   ![ Autorisations de catégorie ](./assets/category-create-permissions.png){width="600" zoomable="yes"}

## Étape 8 : Définition des paramètres de conception

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Design]** .

1. Définissez les paramètres de conception selon vos besoins :

   - ([Adobe Commerce B2B](../b2b/introduction.md) uniquement) Pour appliquer les paramètres de conception de catégorie parente à cette catégorie, définissez **[!UICONTROL Use Parent Category Settings]** sur `Yes`.

   - Pour modifier la conception des pages de catégorie, choisissez le **[!UICONTROL Theme]** que vous souhaitez appliquer.

   - Pour modifier la mise en page des colonnes des pages de catégorie, choisissez le **[!UICONTROL Layout]** à appliquer.

   - Pour entrer du code personnalisé, saisissez un code XML valide dans la zone **[!UICONTROL Layout Update XML]**.

   - Pour utiliser la même conception pour les pages de produit, définissez **[!UICONTROL Apply Design to Products]** sur `Yes`.

   ![Paramètres de conception](./assets/category-design.png){width="600" zoomable="yes"}

1. ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Pour planifier la mise à jour de la conception pour une période spécifique, procédez comme suit :

   - Développez la section _[!UICONTROL Schedule Design Update]_.

   - Utilisez le calendrier (![Icône Calendrier](../assets/icon-calendar.png)) pour choisir les dates **[!UICONTROL from]** et **[!UICONTROL to]** de mise à jour de planification.

   ![Mise à jour de conception planifiée](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.
