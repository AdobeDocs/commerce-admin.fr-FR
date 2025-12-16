---
title: Produit configurable
description: Découvrez comment créer un produit configurable qui fournit aux acheteurs des variations à sélectionner.
exl-id: 2066fd20-5227-41e9-b213-31825a58ebd9
feature: Catalog Management, Products
source-git-commit: 6fcbcd3b7cace10f0841a46b3cd27343862b3f3b
workflow-type: tm+mt
source-wordcount: '1981'
ht-degree: 0%

---

# Produit configurable

Un produit configurable s’affiche en tant que produit unique avec des options de liste déroulante pour des variations (comme la couleur ou la taille). Chaque variation est un produit simple distinct avec son propre SKU, ce qui permet un suivi d’inventaire individuel, contrairement aux produits simples avec des options personnalisées.

**Idéal pour :** produits avec plusieurs options (couleur, taille, matériau, etc.) où vous devez effectuer le suivi des stocks pour chaque variation. La configuration initiale prend plus de temps, mais offre une meilleure évolutivité.

![Produit configurable](./assets/product-configurable.png){width="700" zoomable="yes"}

## Avant de commencer

### Liste de contrôle des conditions préalables

Avant de créer un produit configurable, vérifiez que vous disposez des éléments suivants :

1. **Jeu d’attributs** - Jeu d’attributs qui inclut des attributs de variation (comme la couleur et la taille)
1. **Attributs de variation créés** - Attributs configurés avec les paramètres ci-dessous
1. **Images du produit** - (Facultatif mais recommandé) Images pour le produit parent et chaque variation

### Exigences d’attribut

Chaque attribut utilisé pour les variations de produit doit présenter les paramètres suivants :

| Propriété | Paramètre obligatoire |
|--- |--- |
| [!UICONTROL Scope] | `Global` |
| [!UICONTROL Catalog Input Type for Store Owner] | `Dropdown`, `Visual Swatch` ou `Text Swatch` |
| [!UICONTROL Values Required] | `Yes` |

{style="table-layout:auto"}

Pour obtenir des instructions sur la création d’attributs, voir [Attributs du produit](product-attributes.md).

## Phase 1 : création de la base de produit

### Étape 1 : sélection du type de produit

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Dans le menu _[!UICONTROL Add Product]_( ![Flèche du menu](../assets/icon-menu-down-arrow-red.png){width="25"} ) dans le coin supérieur droit, choisissez **[!UICONTROL Configurable Product]**.

   ![Ajouter un produit configurable](./assets/product-add-configurable.png){width="700" zoomable="yes"}

### Étape 2 : sélection du jeu d’attributs

Le [jeu d’attributs](attribute-sets.md) détermine les champs qui apparaissent dans le formulaire de produit et les attributs disponibles pour les variations.

1. Cliquez sur le champ de jeu d’attributs en haut de la page et effectuez l’une des opérations suivantes :

   - Par **[!UICONTROL Search]**, saisissez le nom du jeu d’attributs.
   - Dans la liste, choisissez le jeu d’attributs à utiliser.

   Le formulaire est mis à jour pour refléter le jeu d’attributs sélectionné.

1. Si vous devez ajouter un autre attribut au jeu d’attributs, cliquez sur **[!UICONTROL Add Attribute]** et suivez les instructions de la section [Ajout d’un attribut](product-attributes-add.md).

   ![Choisir un modèle](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

### Étape 3 : saisir des informations de base

1. Saisissez le **[!UICONTROL Product Name]** du produit.

1. Acceptez le **[!UICONTROL SKU]** par défaut en fonction du nom du produit ou saisissez une autre valeur.

1. Saisissez le **[!UICONTROL Price]** du produit.

   >[!NOTE]
   >
   >Ce prix est remplacé par les prix des produits enfants. Le prix réel affiché aux clients provient des produits enfants [!UICONTROL In Stock].

1. Comme le produit n’est pas encore prêt à être publié, définissez **[!UICONTROL Enable Product]** sur `No`.

1. Cliquez sur **[!UICONTROL Save]** et continuez.

   Lorsque le produit est enregistré, le sélecteur [Vue Boutique](introduction.md#product-scope) s’affiche dans le coin supérieur gauche.

1. Choisissez le **[!UICONTROL Store View]** où le produit doit être disponible.

   ![Choisir la vue du magasin](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### Étape 4 : compléter les paramètres de base

1. Définissez **[!UICONTROL Tax Class]** sur l’une des options suivantes :

   - `None`
   - `Taxable Goods`

1. Laissez **[!UICONTROL Quantity]** vide. La quantité est déterminée par les variations du produit.

1. Laissez **[!UICONTROL Stock Status]** actif.

   L’état de stock d’un produit configurable est déterminé par ses variations associées. Comme le produit a été enregistré sans quantité, la **[!UICONTROL Stock Status]** est définie sur `Out of Stock`.

   >[!NOTE]
   >
   >Le paramètre **État du stock** d’un produit configurable est un paramètre contrôlé **_semi-manuellement_** qui dépend en partie de l’état du stock de ses produits enfants. Il fait partie d&#39;un calcul **_critères multiples_** de l&#39;état des stocks. Voir [Configuration du statut du stock](#configure-stock-status) pour plus d’informations.

1. Saisissez le **[!UICONTROL Weight]** du produit.

   >[!NOTE]
   >
   >Un produit configurable doit toujours avoir un poids. Si vous sélectionnez **[!UICONTROL This item has no weight]** dans la liste déroulante, elle devient automatiquement **[!UICONTROL This item has weight]** lorsque vous enregistrez le produit.

1. Acceptez le paramètre de **[!UICONTROL Visibility]** par défaut de `Catalog, Search`.

1. Pour mettre le produit en avant dans la liste des [nouveaux produits](../content-design/widget-new-products-list.md), cochez la case **[!UICONTROL Set Product as New]**.

1. Pour affecter des catégories au produit, cliquez sur la zone de **[!UICONTROL Select…]** et effectuez l’une des opérations suivantes :

   **Choisir une catégorie existante :**

   - Commencez à saisir dans la zone pour trouver une correspondance.

   - Cochez la case de chaque catégorie à affecter.

   ![Sélectionnez une ou plusieurs catégories pour le produit groupé](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **Créer une nouvelle catégorie :**

   - Cliquez sur **[!UICONTROL New Category]**.

   - Saisissez le **[!UICONTROL Category Name]** et choisissez le **[!UICONTROL Parent Category]** pour déterminer sa position dans la structure du menu.

   - Cliquez sur **[!UICONTROL Create Category]**.

1. Choisissez le **[!UICONTROL Country of Manufacture]**.

   D’autres attributs peuvent apparaître en fonction du jeu d’attributs. Vous pourrez les terminer ultérieurement.

### Étape 5 : Enregistrer et continuer

C’est le bon moment pour enregistrer votre travail. Cliquez sur **[!UICONTROL Save]** dans le coin supérieur droit. Au cours de la phase suivante, vous allez configurer les configurations pour chaque variation.

## Phase 2 : ajout de variations de produit

Les étapes suivantes indiquent comment ajouter des configurations pour plusieurs variations. La barre de progression en haut de la page indique votre position actuelle dans le processus.

**Exemple :** Pour une chemise de 3 couleurs et 3 tailles, vous allez créer 9 produits simples avec des SKU uniques (un pour chaque combinaison). Par défaut, le nom du produit et le SKU de chaque variation sont basés sur la valeur de l’attribut et le nom du produit parent ou le SKU.

### Étape 6 : sélection des attributs de variation

1. Faites défiler jusqu’à la section _[!UICONTROL Configurations]_&#x200B;et cliquez sur **[!UICONTROL Create Configurations]**.

   ![Configurations &#x200B;](./assets/product-configurable-create-configurations.png){width="600" zoomable="yes"}

1. Cochez la case de chaque attribut à inclure en tant que variation.

   Pour cet exemple, `color` et `size` sont sélectionnés.

   ![Sélectionner les attributs](./assets/product-create-configurable-step1.png){width="600" zoomable="yes"}

   La liste inclut tous les attributs du jeu d’attributs pouvant être utilisés dans un produit configurable.

1. Si vous devez ajouter un attribut, cliquez sur **[!UICONTROL Create New Attribute]** et procédez comme suit :

   - Renseignez les propriétés de l’attribut.

   - Cliquez sur **[!UICONTROL Save Attribute]**.

   - Cochez la case correspondant à l’attribut .

1. Cliquez sur **[!UICONTROL Next]** dans le coin supérieur droit.

### Étape 7 : sélection des valeurs d’attribut

1. Pour chaque attribut, cochez la case des valeurs qui s’appliquent au produit.

   ![Valeurs d’attribut](./assets/product-create-configurable-step2.png){width="600" zoomable="yes"}

1. Pour réorganiser les attributs, saisissez l’icône _Réorganiser_ ( ![icône Ordre de tri](../assets/icon-sort-order.png) ) et déplacez la section vers un nouvel emplacement.

   L’ordre détermine la position des listes déroulantes sur la page de produits.

1. Dans la barre de progression, cliquez sur **[!UICONTROL Next]**.

### Étape 8 : configuration des images, de la tarification et de l’inventaire

Cette étape détermine les images, le prix et la quantité pour chaque configuration. Les options disponibles sont les mêmes pour chacune d’elles. Vous pouvez appliquer le même paramètre à tous les SKU, appliquer des paramètres uniques à chaque SKU ou ignorer les paramètres pour l’instant.

#### Configuration des images

Sélectionnez l’option de configuration qui s’applique :

**Option 1 : appliquer un seul ensemble d’images à tous les SKU**

1. Sélectionnez **[!UICONTROL Apply single set of images to all SKUs]**.

1. Accédez à chaque image à inclure dans la galerie de produits ou faites glisser les images vers la zone.

![Utiliser les mêmes images pour tous les SKU](./assets/product-configurations-images-apply-single-set.png){width="600" zoomable="yes"}

**Option 2 : appliquer des images uniques pour chaque SKU**

Comme l’image du produit parent est déjà chargée, utilisez cette option pour charger des images pour chaque variation. Vous pouvez ajouter différentes images qui apparaissent dans le panier lorsqu’une personne achète une variation spécifique.

1. Sélectionnez **[!UICONTROL Apply unique images by attribute to each SKU]**.

1. Sélectionnez les **[!UICONTROL Attribute]** illustrées par les images, telles que `color`.

1. Pour chaque valeur d’attribut, accédez aux images à utiliser pour cette configuration ou faites-les glisser vers la zone.

   Si vous faites glisser une image vers une zone de valeur, elle apparaît également dans les sections pour d’autres valeurs. Pour supprimer une image, cliquez sur l’icône _Corbeille_ (![Icône Corbeille](../assets/icon-delete-trashcan-solid.png)).

   ![Images uniques par SKU](./assets/product-configurable-create-configurations-add-images-unique.png){width="600" zoomable="yes"}

#### Configurer la tarification

>[!NOTE]
>
>Un produit configurable n&#39;a pas son propre prix dans le catalogue. Le prix configurable du produit est dérivé de ses produits enfants [!UICONTROL In Stock].

Sélectionnez l’option de configuration qui s’applique :

**Option 1 : appliquer le même prix à tous les SKU**

1. Si le prix est le même pour toutes les variations, sélectionnez **[!UICONTROL Apply single price to all SKUs]**.

1. Saisissez le **[!UICONTROL Price]**.

   ![Même prix par SKU](./assets/product-configurable-create-configurations-price-all-skus.png){width="600" zoomable="yes"}

**Option 2 : appliquer un prix différent pour chaque SKU**

1. Si le prix diffère pour chacune des variations, sélectionnez **[!UICONTROL Apply unique prices by attribute to each SKU]**.

1. Sélectionnez le **[!UICONTROL Attribute]** qui est à la base de la différence de prix.

1. Saisissez le **[!UICONTROL Price]** de chaque valeur d’attribut.

   Dans cet exemple, la taille XL coûte plus cher.

   ![Prix unique par SKU](./assets/product-configurable-create-configurations-price-unique.png){width="600" zoomable="yes"}

#### Configuration de l’inventaire

Sélectionnez l’option de configuration qui s’applique :

**Option 1 : appliquer la même quantité à tous les SKU**

Si la quantité est identique pour tous les SKU, sélectionnez **[!UICONTROL Apply single quantity to each SKU]** et spécifiez la quantité.

_Marchands Source uniques :_

Saisissez le **[!UICONTROL Quantity]**.

_Marchands Multi Source utilisant [Inventory management &#x200B;](../inventory-management/introduction.md):_

Affectez des sources et ajoutez des quantités pour toutes les variantes de produit générées :

1. Sélectionnez l’option **[!UICONTROL Apply single quantity to each SKU]** .

1. Pour ajouter une source, cliquez sur **[!UICONTROL Assign Sources]**.

1. Parcourez ou recherchez une source à ajouter. Cochez la case en regard des sources du produit.

1. Entrez un montant de stock disponible par origine.

   ![Quantité unique pour tous les SKU, affecter la source](./assets/inventory-configure-product-quantity.png){width="600" zoomable="yes"}

**Option 2 : appliquer une quantité différente par attribut**

_Marchands Source uniques :_

Saisissez le **[!UICONTROL Quantity]** de chaque valeur d’attribut.

_Marchands Multi Source utilisant [Inventory management &#x200B;](../inventory-management/introduction.md):_

Affectez des sources et ajoutez des quantités pour toutes les variantes de produit générées :

1. Sélectionnez **[!UICONTROL Apply unique quantity by attribute to each SKU]**.

1. Saisissez le **[!UICONTROL Quantity]** de chaque variation.

   ![Quantités différentes par attribut](./assets/product-configurations-quantity-different.png){width="600" zoomable="yes"}

Lorsque la configuration des images, du prix et de la quantité est terminée, cliquez sur **[!UICONTROL Next]** dans le coin supérieur droit.

### Étape 9 : génération des configurations de produit

Attendez que la liste des produits s’affiche et effectuez l’une des opérations suivantes :

- Si les configurations vous conviennent, cliquez sur **[!UICONTROL Generate Products]**.

- Pour apporter des corrections, cliquez sur **[!UICONTROL Back]**.

![Consultez le résumé avant de générer des variations de produit](./assets/product-create-configurable-summary.png){width="600" zoomable="yes"}

Les variations actuelles du produit s’affichent au bas de la section _Configuration_.

![Configurations actuelles](./assets/product-create-configurable-generated.png){width="600" zoomable="yes"}

### Étape 10 : ajouter des images de produit

1. Faites défiler vers le bas et développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section _[!UICONTROL Images and Videos]_.

1. Cliquez sur la mosaïque _Appareil photo_ et accédez à l’image principale à utiliser pour le produit configurable.

Pour plus d’informations, voir [&#x200B; Images et vidéo &#x200B;](product-images-and-video.md).

### Étape 11 : Compléter les informations sur le produit

Faites défiler vers le bas et renseignez les informations des sections suivantes selon vos besoins :

- [Contenu](product-content.md)

- [Produits associés, ventes incitatives et ventes croisées](related-products-up-sells-cross-sells.md)

- [Optimisation du moteur de recherche](product-search-engine-optimization.md)

- [Options personnalisables](settings-advanced-custom-options.md)

- [Produits dans les sites web](settings-basic-websites.md)

- [Conception](settings-advanced-design.md)

- [Options de cadeau](product-gift-options.md)

## Phase 3 : publication du produit

### Étape 12 : publier le produit

1. Si vous êtes prêt à publier le produit dans le catalogue, définissez **[!UICONTROL Enable Product]** sur `Yes`.

1. Effectuez l’une des opérations suivantes :

   **Méthode 1 : enregistrer et prévisualiser**

   - Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]**.

   - Pour afficher le produit dans votre boutique, choisissez **[!UICONTROL Customer View]** dans le menu _Admin_ ( ![Flèche de menu](../assets/icon-menu-down-arrow-black.png) ).

   Le magasin s’ouvre dans un nouvel onglet du navigateur.

   ![Affichage client](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **Méthode 2 : enregistrer et fermer**

   Dans le menu _[!UICONTROL Save]_( ![flèche du menu](../assets/icon-menu-down-arrow-red.png){width="25"} ), choisissez **[!UICONTROL Save & Close]**.

## Configuration du statut du stock

Le statut de stock de produits configurable diffère du statut de stock de produits simple. Pour un produit configurable, le statut du stock fait partie d&#39;un calcul **_critères multiples_**.

### Fonctionnement de l’état des stocks

Les principes clés du comportement de l&#39;état des stocks :

| Vous Avez Défini Le Statut Sur | Résultat | Contrôlé Par Des Produits Enfants ? |
|---|---|---|
| `Out of Stock` (manuel) | Affiche toujours `Out of Stock` dans Admin et Storefront | Non - reste jusqu’à ce qu’il soit modifié manuellement en `In Stock` |
| `In Stock` (manuel) | Le statut est dynamique en fonction des produits enfants | Partiel - voir les détails ci-dessous |

{style="table-layout:auto"}

### Lorsqu’elle est définie sur « En stock »

Lorsque vous définissez manuellement le statut du stock de produit configurable sur `In Stock`, il se comporte différemment selon la configuration de votre inventaire :

**Avec source/stock par défaut uniquement :**

- **Admin et Storefront :** le statut du stock reflète automatiquement la disponibilité des produits enfants

**Avec au moins une source/stock personnalisé(e) :**

- **Storefront :** statut des stocks reflète automatiquement la disponibilité des produits enfants
- **Admin:** Reste tel `In Stock` jusqu’à ce qu’il soit modifié manuellement (non contrôlé par des produits enfants)

>[!NOTE]
>
>Les stocks et sources personnalisés font partie de l’extension [Inventory management](../inventory-management/sources-stocks.md). Il est vivement recommandé d’utiliser cet outil exclusivement pour gérer le stock et la source. Les fonctions source et stock par défaut font partie du module `CatalogInventory`, qui est désormais obsolète.

### Modifications manuelles du statut du stock

Si vous définissez manuellement le statut du stock sur `Out of Stock` (via l’action de l’utilisateur de l’administrateur, l’importation de fichier ou l’appel API), il reste `Out of Stock` sur l’administrateur et le storefront jusqu’à ce que vous le remplaciez manuellement par `In Stock`. Il n’est pas affecté par le statut du stock de produits enfants.

## Configuration du système (facultatif)

### Affichage des images de variation dans les miniatures de panier

Si vous disposez d’images différentes pour chaque variation, vous pouvez configurer le système pour afficher l’image appropriée pour la miniature du panier.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Checkout]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section _[!UICONTROL Shopping Cart]_.

1. Définissez **[!UICONTROL Configurable Product Image]** sur `Product Thumbnail Itself`.

1. Cliquez sur **[!UICONTROL Save Config]**.

   ![Panier - image de produit configurable](./assets/config-checkout-configurable-product.png){width="600" zoomable="yes"}

## Considérations principales

- **Types de variation :** les acheteurs peuvent sélectionner des options parmi les types d’entrée de liste déroulante, de sélection multiple, d’échantillon visuel et d’échantillon de texte. Chaque option est un produit simple et distinct.

- **Suivi des stocks :** contrairement aux produits simples avec des options personnalisées, les produits configurables effectuent le suivi des stocks pour chaque variation indépendamment.

- **Types de produits enfants :** les produits enfants peuvent être des produits simples ou virtuels **sans options personnalisées**. Pour rendre les produits enfants virtuels, sélectionnez `Тhis item has no weight` pour le paramètre **[!UICONTROL Weight]** de chaque enfant.

- **Affectation globale** les produits enfants sont affectés et non affectés du produit configurable **globalement** à tous les sites web, magasins et vues de magasin simultanément.

- **Tarification :** un produit configurable n’a pas son propre prix dans le catalogue. Le prix affiché provient de ses produits enfants [!UICONTROL In Stock].

- **Attributs :** les attributs de variation doivent avoir une portée globale et les clients doivent être tenus de choisir une valeur. Les attributs doivent être inclus dans le jeu d’attributs utilisé pour le produit configurable.

- **Miniatures de panier :** la miniature du panier peut afficher l’image à partir de l’enregistrement de produit configurable ou de la variation de produit. Voir [Configuration du système](#system-configuration-optional) ci-dessus.

- **Comportement de l’échantillon :** les [attributs d’échantillon](swatches.md#create-swatches-for-products) peuvent être configurés pour ne pas afficher les images de produit simples correspondantes lorsque l’échantillon est sélectionné en définissant **[!UICONTROL Update Product Preview Image]** sur `No` sur la page de modification des attributs.

- **Comportement de la galerie d’images :** le thème contrôle le comportement de la galerie d’images lorsque les utilisateurs basculent entre les configurations de produit. Le comportement par défaut du thème _Vide_ remplace les images du produit configurable parent par la variation sélectionnée. Pour le thème Luma , le comportement par défaut consiste à ajouter les images de variation sélectionnées aux images de produit configurables parentes.
