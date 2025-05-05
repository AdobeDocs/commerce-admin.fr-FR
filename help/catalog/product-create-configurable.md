---
title: Produit configurable
description: Découvrez comment créer un produit configurable qui fournit aux acheteurs des variantes de sélection.
exl-id: 2066fd20-5227-41e9-b213-31825a58ebd9
feature: Catalog Management, Products
source-git-commit: ce36104913434bb71115e1a5b497f38f75fbd3c5
workflow-type: tm+mt
source-wordcount: '2506'
ht-degree: 0%

---

# Produit configurable

Un produit configurable ressemble à un produit unique avec une liste déroulante de chaque variation. Chaque élément de liste est en fait un produit simple distinct avec un SKU unique, ce qui permet de suivre l’inventaire de chaque variation de produit. Vous pouvez obtenir un effet similaire en utilisant un produit simple avec des options personnalisées, mais sans la possibilité de suivre l’inventaire pour chaque variation.

Les instructions suivantes montrent le processus de création d’un produit configurable à l’aide d’un [modèle de produit](attribute-sets.md), de champs obligatoires et de paramètres de base. Chaque champ obligatoire est marqué d’un astérisque rouge (`*`). Lorsque vous avez terminé les étapes de base, vous pouvez définir les autres paramètres du produit selon vos besoins.

![Produit configurable](./assets/product-configurable.png){width="700" zoomable="yes"}

## Partie 1 : création d’un produit configurable

Bien qu’un produit configurable utilise davantage de SKU et qu’il puisse prendre un peu plus de temps au départ à configurer, il peut vous faire gagner du temps au bout du compte. Si vous prévoyez de développer votre entreprise, le type de produit configurable est un bon choix pour les produits avec plusieurs options.

Avant de commencer, préparez un [jeu d’attributs](attribute-sets.md) qui inclut un attribut défini sur l’un des types d’entrée autorisés pour chaque variante de produit. Par exemple, le jeu d’attributs peut inclure des attributs de liste déroulante pour la couleur et la taille.

Les propriétés de chaque attribut utilisé pour une variation de produit configurable doivent comporter les paramètres suivants :

### Exigences d’attribut de variation de produit

| Propriété | Paramètre |
|--- |--- |
| [!UICONTROL Scope] | `Global` |
| [!UICONTROL Catalog Input Type for Store Owner] | Le type d’entrée de tout attribut utilisé pour une variation de produit doit être l’un des suivants : `Dropdown`, `Visual Swatch` ou `Text Swatch`. |
| [!UICONTROL Values Required] | `Yes` |

{style="table-layout:auto"}

### Etape 1 : Sélection du type de produit

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Dans le menu _[!UICONTROL Add Product]_( ![Flèche de menu](../assets/icon-menu-down-arrow-red.png){width="25"} ) dans le coin supérieur droit, choisissez **[!UICONTROL Configurable Product]**.

   ![Ajouter un produit configurable](./assets/product-add-configurable.png){width="700" zoomable="yes"}

### Étape 2 : sélection du jeu d’attributs

Le [jeu d’attributs](attribute-sets.md) détermine la sélection des champs utilisés dans le produit. Le jeu d’attributs utilisé dans l’exemple suivant comporte des attributs de couleur et de taille. Le nom de l’ensemble d’attributs est indiqué en haut de la page et est initialement défini sur `Default`.

1. Pour choisir le jeu d’attributs du produit, cliquez sur le champ en haut de la page et effectuez l’une des opérations suivantes :

   - Pour **[!UICONTROL Search]**, saisissez le nom du jeu d’attributs.
   - Dans la liste, choisissez le jeu d’attributs à utiliser.

   Le formulaire est mis à jour pour refléter la modification.

1. Si vous souhaitez ajouter un autre attribut au jeu d’attributs, cliquez sur **[!UICONTROL Add Attribute]** et suivez les instructions de la section [Ajout d’un attribut](product-attributes-add.md).

   ![Choisir le modèle](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

### Étape 3 : Définissez les paramètres requis

1. Saisissez le produit **[!UICONTROL Product Name]**.

1. Acceptez la valeur par défaut **[!UICONTROL SKU]** basée sur le nom du produit ou saisissez-en une autre.

1. Saisissez le produit **[!UICONTROL Price]**.

1. Comme le produit n’est pas encore prêt à être publié, définissez **[!UICONTROL Enable Product]** sur `No`.

1. cliquez sur **[!UICONTROL Save]** et continuez.

   Lorsque le produit est enregistré, le programme de sélection [Affichage magasin](introduction.md#product-scope) s’affiche dans le coin supérieur gauche.

1. Sélectionnez l’ **[!UICONTROL Store View]** où le produit doit être disponible.

   ![Choisir la vue de magasin](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### Étape 4 : définition des paramètres de base

1. Définissez **[!UICONTROL Tax Class]** sur l’une des options suivantes :

   - `None`
   - `Taxable Goods`

1. L’ **[!UICONTROL Quantity]** est déterminé par les variations de produit, vous pouvez donc le laisser vide.

1. Laissez le **[!UICONTROL Stock Status]** tel quel.

   L’état du stock d’un produit configurable est déterminé par chaque configuration associée. Comme le produit a été enregistré sans entrer de quantité, **[!UICONTROL Stock Status]** est défini sur `Out of Stock`.

   >[!NOTE]
   >
   >L’ **état du stock** du produit configurable est un paramètre contrôlé **_semi-manuel_**. Elle est partiellement contrôlée par l’état des stocks de ses produits enfants. Il fait partie d’un calcul d’état du stock **_multicritère_**, qui est décrit dans la section [Configurer l’état du stock](#configure-the-stock-status) .

1. Saisissez le produit **[!UICONTROL Weight]**.

>[!NOTE]
>
>Un produit configurable doit toujours avoir un poids. Si vous sélectionnez **[!UICONTROL This item has no weight]** dans la liste déroulante, il est automatiquement remplacé par **[!UICONTROL This item has weight]** après l’enregistrement du produit.

1. Acceptez le paramètre par défaut **[!UICONTROL Visibility]** de `Catalog, Search`.

1. Pour afficher le produit dans la liste de [nouveaux produits](../content-design/widget-new-products-list.md), cochez la case **[!UICONTROL Set Product as New]** .

1. Pour attribuer des catégories au produit, cliquez sur la zone **[!UICONTROL Select…]** et effectuez l’une des opérations suivantes :

   **Choisissez une catégorie existante** :

   - Commencez à taper dans la zone jusqu’à ce que vous trouviez une correspondance.

   - Cochez la case de la catégorie à attribuer.

   ![Sélectionnez une ou plusieurs catégories pour le produit du lot](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **Créer une catégorie** :

   - Cliquez sur **[!UICONTROL New Category]**.

   - Saisissez le **[!UICONTROL Category Name]** et choisissez le **[!UICONTROL Parent Category]**, qui détermine sa position dans la structure de menus.

   s - Cliquez sur **[!UICONTROL Create Category]**.

1. Sélectionnez le **[!UICONTROL Country of Manufacture]**.

   Il peut y avoir des attributs supplémentaires utilisés pour décrire le produit. La sélection varie en fonction de l’ensemble d’attributs. Vous pouvez la terminer ultérieurement.

### Étape 5 : enregistrer et continuer

C&#39;est le bon moment pour sauver votre travail. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]**. Dans la série d’étapes suivante, vous allez définir les configurations de chaque variante du produit.

## Partie 2 : ajout de configurations

L’exemple suivant montre comment ajouter des configurations pour trois couleurs et trois tailles. En tout, neuf produits simples sont créés avec des SKU uniques pour couvrir chaque combinaison possible de variations. Par défaut, le nom du produit et le SKU de chaque variation sont basés sur la valeur d’attribut et soit sur le nom du produit parent, soit sur le SKU.

La barre de progression située en haut de la page indique où vous vous trouvez dans le processus et vous guide tout au long de chaque étape.

### Étape 1 : Sélection des attributs

1. Continuez depuis la partie supérieure, faites défiler l’écran jusqu’à la section _[!UICONTROL Configurations]_&#x200B;et cliquez sur **[!UICONTROL Create Configurations]**.

   ![Configurations](./assets/product-configurable-create-configurations.png){width="600" zoomable="yes"}

1. Cochez la case de chaque attribut que vous souhaitez inclure comme configuration.

   Dans cet exemple, `color` et `size` sont sélectionnés.

   ![Sélectionner des attributs](./assets/product-create-configurable-step1.png){width="600" zoomable="yes"}

   La liste inclut tous les attributs du jeu d’attributs qui peuvent être utilisés dans un produit configurable.

1. Si vous souhaitez ajouter un attribut, cliquez sur **[!UICONTROL Create New Attribute]** et procédez comme suit :

   - Renseignez les propriétés d’attribut.

   - Cliquez sur **[!UICONTROL Save Attribute]**.

   - Cochez la case correspondant à l’attribut .

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Next]**.

### Etape 2 : saisie des valeurs d&#39;attribut

1. Pour chaque attribut, cochez la case des valeurs qui s’appliquent au produit.

   ![Valeurs d’attribut](./assets/product-create-configurable-step2.png){width="600" zoomable="yes"}

1. Pour réorganiser les attributs, appuyez sur l’icône _Réorganiser_ ( ![Icône Ordre de tri](../assets/icon-sort-order.png) ) et déplacez la section vers une nouvelle position.

   L’ordre détermine la position des listes déroulantes sur la page du produit.

1. Dans la barre de progression, cliquez sur **[!UICONTROL Next]**.

### Étape 3 : configuration des images, du prix et de la quantité

Cette étape détermine les images, le prix et la quantité de chaque configuration. Les options disponibles sont les mêmes pour chacune d’elles et vous pouvez en choisir une seule. Vous pouvez appliquer le même paramètre à tous les SKU, appliquer un paramètre unique à chaque SKU ou ignorer les paramètres pour l’instant.

Choisissez les options de configuration qui s&#39;appliquent.

Utilisez l’une des méthodes suivantes pour configurer le **[!UICONTROL images]** :

**Méthode 1 :** appliquer un seul jeu d’images à tous les SKU

1. Sélectionnez **[!UICONTROL Apply single set of images to all SKUs]**.

1. Accédez à chaque image à inclure dans la galerie de produits ou faites-la glisser sur la zone.

![Utiliser les mêmes images pour tous les SKU](./assets/product-configurations-images-apply-single-set.png){width="600" zoomable="yes"}

**Méthode 2 :** appliquer des images uniques pour chaque SKU

Comme l’image du produit parent est déjà téléchargée, vous pouvez utiliser cette option pour télécharger une image de chaque couleur. Vous pouvez ajouter une autre image qui apparaît dans le panier lorsque quelqu’un achète l’article dans une couleur spécifique.

1. Sélectionnez **[!UICONTROL Apply unique images by attribute to each SKU]**.

1. Sélectionnez les **[!UICONTROL Attribute]** illustrés par les images, par exemple `color`.

1. Pour chaque valeur d’attribut, accédez aux images que vous souhaitez utiliser pour cette configuration ou faites-les glisser vers la zone.

   Si vous faites glisser l’image vers une zone de valeur, elle apparaît également dans les sections des autres valeurs. Si vous souhaitez supprimer une image, cliquez sur l’icône _Corbeille_ (![Icône Corbeille](../assets/icon-delete-trashcan-solid.png)).

   ![Images uniques par SKU](./assets/product-configurable-create-configurations-add-images-unique.png){width="600" zoomable="yes"}

Utilisez l’une des méthodes suivantes pour configurer le **[!UICONTROL prices]** :

>[!NOTE]
>
>Un produit configurable n’a pas son propre prix dans le catalogue. Le prix configurable du produit est dérivé de ses [!UICONTROL In Stock] produits enfants.

**Méthode 1 :** Appliquez le même prix à tous les SKU

1. Si le prix est le même pour toutes les variations, sélectionnez **[!UICONTROL Apply single price to all SKUs]**.

1. Saisissez le **[!UICONTROL Price]**.

   ![Même prix par SKU](./assets/product-configurable-create-configurations-price-all-skus.png){width="600" zoomable="yes"}

**Méthode 2 :** appliquer un prix différent pour chaque SKU

1. Si le prix varie pour chaque ou pour certaines variantes du produit, sélectionnez **[!UICONTROL Apply unique prices by attribute to each SKU]**.

1. Sélectionnez le **[!UICONTROL Attribute]** qui est la base de la différence de prix.

1. Saisissez le **[!UICONTROL Price]** pour chaque valeur d’attribut.

   Dans cet exemple, la taille XL coûte plus cher.

   ![Prix unique par SKU](./assets/product-configurable-create-configurations-price-unique.png){width="600" zoomable="yes"}

Utilisez l’une des méthodes suivantes pour configurer le **[!UICONTROL Quantity]** :

**Méthode 1 :** Appliquez la même quantité à tous les SKU

Si la quantité est la même pour tous les SKU, sélectionnez **[!UICONTROL Apply single quantity to each SKU]** et indiquez la quantité.

_Marchands à source unique_ - Saisissez le **[!UICONTROL Quantity]**.

_Commerçants multi-Source utilisant [Inventory management](../inventory-management/introduction.md)_ - Attribuez des sources et ajoutez des quantités pour toutes les variantes de produits générées :

1. Sélectionnez l’option **[!UICONTROL Apply single quantity to each SKU]** .

1. Pour ajouter une source, cliquez sur **[!UICONTROL Assign Sources]**.

1. Recherchez une source à ajouter. Cochez la case en regard des sources que vous souhaitez ajouter au produit.

1. Saisissez un montant de stock disponible par source.

   ![Quantité unique pour tous les SKU, attribuer la source](./assets/inventory-configure-product-quantity.png){width="600" zoomable="yes"}

**Méthode 2 :** appliquer une quantité différente par attribut

_Marchands à source unique_ - Saisissez le **[!UICONTROL Quantity]**.

_Commerçants multi-Source utilisant [Inventory management](../inventory-management/introduction.md)_ - Attribuez des sources et ajoutez des quantités pour toutes les variantes de produits générées :

1. Si la quantité est différente pour chaque SKU, sélectionnez **[!UICONTROL Apply unique quantity by attribute to each SKU]**.

1. Saisissez le **[!UICONTROL Quantity]** pour chacun d’eux.

   ![Quantités différentes par attribut](./assets/product-configurations-quantity-different.png){width="600" zoomable="yes"}

Lorsque la configuration des images, du prix et de la quantité est terminée, cliquez sur **[!UICONTROL Next]** dans le coin supérieur droit.

### Étape 4 : Génération des configurations de produit

Patientez quelques instants pour que la liste de produits s’affiche et effectuez l’une des opérations suivantes :

- Si les configurations vous conviennent, cliquez sur **[!UICONTROL Generate Products]**.

- Pour apporter des corrections, cliquez sur **[!UICONTROL Back]**.

![Résumé de la révision avant de générer des variations de produit](./assets/product-create-configurable-summary.png){width="600" zoomable="yes"}

Les variations de produit actuelles apparaissent au bas de la section _Configuration_.

![Configurations actuelles](./assets/product-create-configurable-generated.png){width="600" zoomable="yes"}

### Étape 5 : Ajout d’images de produit

1. Faites défiler l’écran vers le bas et développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur _[!UICONTROL Images and Videos]_.

1. Cliquez sur la mosaïque _Appareil photo_ et accédez à l’image principale que vous souhaitez utiliser pour le produit configurable.

Pour plus d’informations, voir [Images et vidéo](product-images-and-video.md).

### Étape 6 : renseigner les informations sur le produit

Faites défiler l’écran vers le bas et renseignez les informations des sections suivantes selon vos besoins :

- [Contenu](product-content.md)

- [Produits associés, ventes consécutives et ventes croisées](related-products-up-sells-cross-sells.md)

- [Optimisation du moteur de recherche](product-search-engine-optimization.md)

- [Options personnalisables](settings-advanced-custom-options.md)

- [Produits sur les sites web](settings-basic-websites.md)

- [Conception](settings-advanced-design.md)

- [Options de cadeau](product-gift-options.md)

### Étape 7 : Publish du produit

1. Si vous êtes prêt à publier le produit dans le catalogue, définissez **[!UICONTROL Enable Product]** sur `Yes` et effectuez l’une des opérations suivantes :

   - **Méthode 1 :** Enregistrer et prévisualiser

      - Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]**.

      - Pour afficher le produit dans votre boutique, sélectionnez **[!UICONTROL Customer View]** dans le menu _Admin_ ( ![Flèche de menu](../assets/icon-menu-down-arrow-black.png) ).

     Le magasin s’ouvre dans un nouvel onglet du navigateur.

     ![Affichage client](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Méthode 2 :** Enregistrer et fermer

     Dans le menu _[!UICONTROL Save]_( ![Flèche de menu](../assets/icon-menu-down-arrow-red.png){width="25"} ), choisissez **[!UICONTROL Save & Close]**.

### Étape 8 : configuration des miniatures de panier

Si vous disposez d’une image différente pour chaque variation, vous pouvez définir la configuration de manière à utiliser l’image correcte pour la miniature du panier.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et sélectionnez **[!UICONTROL Checkout]** sous .

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur _[!UICONTROL Shopping Cart]_.

1. Définissez **[!UICONTROL Configurable Product Image]** sur `Product Thumbnail Itself`.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

   ![Panier - image de produit configurable](./assets/config-checkout-configurable-product.png){width="600" zoomable="yes"}

## Configuration de l’état du stock

L’état du stock configurable d’un produit est différent de l’état du stock du produit simple, où il est une représentation directe de la disponibilité du produit. Pour un produit configurable, l’état du stock fait partie du calcul de l’état du stock **_multi-critères_**.

### Vue d’ensemble

Les principes principaux des relations d’état des stocks sont les suivants :

- Lorsque vous modifiez le **[!UICONTROL Stock Status]** du produit configurable en tant que `Out of Stock` et cliquez sur **[!UICONTROL Save]**, il est **_non contrôlé_** par les statuts de ses produits enfants. Il s’affiche toujours sous la forme `Out of Stock` dans l’administrateur et sur le storefront.

- Lorsque vous définissez le **[!UICONTROL Stock Status]** du produit configurable sur `In Stock` et cliquez sur **[!UICONTROL Save]**, il est **_partiellement contrôlé_** par les statuts de ses produits enfants, qui sont reflétés dans l’Admin et sur le storefront.

### Description détaillée

L’ _état du stock_ du produit configurable est partiellement contrôlé par l’état du stock de ses produits enfants et selon les calculs d’état du stock **_à plusieurs critères_** suivants :

#### Avec source/stock par défaut uniquement :

- Si le statut du produit configurable Stock est **_défini manuellement_** sur `Out of Stock` par un utilisateur administrateur, un import de fichier ou un appel API, il reste défini sur `Out of Stock` sur les instances **_Admin_** et **_Storefront_** jusqu’à ce qu’il soit **_manuellement_** modifié en `In stock` par un utilisateur administrateur, un import de fichier ou un appel API. Il ne peut pas être contrôlé par l’état des stocks de ses produits enfants.

- Si le statut du stock de produit configurable est **_manuellement_** défini sur `In Stock` par un utilisateur administrateur, un import de fichier ou un appel API, son état du stock est **_automatiquement_** contrôlé par l’état du stock de ses produits enfants sur les **_Admin_** et **_Storefront_**.

>[!NOTE]
>
>Les stocks et les sources personnalisés font partie de l’extension [Inventory management](../inventory-management/sources-stocks.md) et il est vivement recommandé d’utiliser cet outil exclusivement pour gérer le stock et la source. Les fonctions source et stock par défaut font partie du module `CatalogInventory`, qui est désormais obsolète.

#### Avec au moins une source/un stock personnalisé :

- Si la valeur de statut Stock du produit configurable est **_manuellement_** définie sur `Out of Stock` par un utilisateur administrateur, un import de fichier ou un appel API, elle reste définie sur `Out of Stock` sur les instances **_Admin_** et **_Storefront_** jusqu’à ce qu’elle soit **_manuellement_** modifiée sur `In Stock` par un utilisateur administrateur, un import de fichier ou un appel API. Il **_ne peut pas_** être contrôlé par l’état de stock de ses produits enfants.

- Si la valeur de statut Stock du produit configurable est **_manuellement_** définie sur `In Stock` par un utilisateur administrateur, un import de fichier ou un appel API, son état de stock est **_automatiquement_** contrôlé par l’état de stock de ses produits enfants sur **_Storefront_** uniquement.

- Si la valeur de statut Stock du produit configurable est **_définie manuellement_** sur `In Stock` par un utilisateur administrateur, un import de fichier ou un appel API, elle reste définie sur `In Stock` dans l’ **_Admin_** jusqu’à ce qu’elle soit **_manuellement_** remplacée par `Out of Stock` par un utilisateur administrateur, un import de fichier ou un appel API. Il **_ne peut pas_** être contrôlé par l’état de stock de ses produits enfants.

## Les choses à retenir

- Un produit configurable permet à l’acheteur de choisir des options dans une liste déroulante, plusieurs sélections, un échantillon visuel et des types d’entrée d’échantillon de texte. Chaque option est un produit simple et distinct.

- [État du stock](../inventory-management/sources-stocks.md) pour un produit configurable est un paramètre contrôlé semi-manuellement. Il diffère de l’état du stock du produit simple, où il représente directement la disponibilité du produit. Pour un produit configurable, l’état du stock fait partie du calcul de l’état du stock à plusieurs critères.

- Les produits enfants configurables peuvent être des produits simples ou virtuels **sans options personnalisées**. Pour que les produits enfants personnalisés soient virtuels, vous devez sélectionner `Тhis item has no weight` pour le paramètre **[!UICONTROL Weight]** de chacun d’eux.

- Tous les produits enfants sont attribués et non attribués à partir du produit configurable **_global_** pour tous les sites web, magasins et vues de magasin en même temps.

- Un produit configurable n’a pas son propre prix dans le catalogue. Le prix configurable du produit est dérivé de ses [!UICONTROL In Stock] produits enfants.

- Les attributs utilisés pour les variations de produit doivent avoir une portée globale et le client doit être tenu de choisir une valeur. Les attributs de variation de produit doivent être inclus dans le jeu d’attributs utilisé comme modèle pour le produit configurable.

- L’ensemble d’attributs utilisé comme modèle pour un produit configurable doit inclure les attributs qui contiennent les valeurs nécessaires pour chaque variante de produit.

- L’image miniature du panier peut être définie pour afficher l’image à partir de l’enregistrement de produit configurable ou de la variation de produit.

- [Les attributs Swatch](swatches.md#create-swatches-for-products) peuvent être configurés pour ne pas afficher les images de produit simples correspondantes lorsque l’échantillon est sélectionné en définissant la valeur de l’option **[!UICONTROL Update Product Preview Image]** sur `No` sur la page de modification des attributs dans l’administrateur.

- Le thème contrôle le comportement de la galerie d’images lorsqu’un utilisateur bascule entre les configurations de produit. Le comportement par défaut du thème _Vierge_ consiste à remplacer les images de produit configurables parentes par la variation de produit sélectionnée. Pour le thème Luma, le comportement par défaut consiste à ajouter les images de variation de produit sélectionnées en préfixe aux images de produit configurables parentes.
