---
title: Référence des attributs de données de produit
description: Utilisez cette référence d’attributs de données de produit lorsque vous utilisez l’importation et l’exportation de données de produit.
exl-id: 9ffa4d1f-cbf8-4a08-bb79-33f21e698a74
feature: Products, Attributes
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '2469'
ht-degree: 2%

---

# Référence des attributs de données de produit

Le tableau suivant répertorie les attributs d’une exportation de produit type, dans l’ordre par défaut dans lequel ils apparaissent. Chaque attribut est représenté dans le fichier CSV sous la forme d’une colonne et les enregistrements de produit sont représentés par des lignes. Les colonnes qui commencent par un trait de soulignement contiennent des données de service telles que des propriétés ou des valeurs d’option pour les données complexes. Vous pouvez [export](data-export.md) un produit de votre catalogue pour voir comment chaque attribut est représenté dans les données.

Les exemples de données sont installés dans l’installation utilisée pour exporter ces données. Deux sites web et plusieurs vues de magasin sont disponibles. Bien que cette liste contienne toutes les colonnes généralement exportées, la variable `sku` est la seule valeur requise. Pour importer des données, vous pouvez inclure uniquement les colonnes avec modifications. La variable `sku` doit être la première colonne, mais l’ordre du reste des attributs n’a pas d’importance.

## Structure de fichier CSV de produit simple

| Attribut | Description |
|--- |--- |
| `sku` | (Obligatoire) L’unité de gestion des stocks est un identifiant alphanumérique unique utilisé pour effectuer le suivi du stock. Un SKU peut comporter jusqu’à 64 caractères. Par exemple : `sku123`<br/>**_Remarque :_**Un SKU de plus de 64 caractères provoque l’échec de l’importation. |
| `store_view_code` | Identifie les vues de magasin spécifiques où le produit est disponible. Si ce champ est vide, le produit est disponible dans la vue de magasin par défaut. Par exemple: `storeview1`, `english`, `spanish` |
| `attribute_set_code` | Attribue le produit à un jeu d’attributs ou à un modèle de produit spécifique, en fonction du type de produit. Une fois le produit créé, le jeu d’attributs ne peut plus être modifié. Par exemple: `default` |
| `product_type` | Indique le type de produit. Valeurs :<br/>`simple` — Éléments tangibles qui sont habituellement vendus en unités uniques ou en quantités fixes.<br/>`grouped` — Groupe de produits distincts vendus en tant qu’ensemble.<br/>`configurable` — Un produit avec plusieurs options que le client doit sélectionner avant d’effectuer un achat. Le stock peut être géré pour chaque ensemble de variations, car il représente un produit distinct avec un SKU distinct. Par exemple, une combinaison de couleur et de taille pour un produit configurable est associée à un SKU spécifique dans le catalogue.<br/>`virtual` — Produit non tangible qui ne nécessite pas d’expédition et qui n’est pas conservé dans l’inventaire. Par exemple, les services, les adhésions et les abonnements.<br/>`bundle` — Un ensemble de produits personnalisable de produits simples vendus ensemble. |
| `categories` | Indique chaque catégorie affectée au produit. Séparez les catégories et les sous-catégories par une barre oblique. Pour indiquer plusieurs chemins de catégorie, séparez chaque chemin par une barre verticale | symbole . Par exemple: `Default Category/Gear&#124;Default Category/Gear/Bags` |
| `product_websites` | Code de chaque site web sur lequel le produit est disponible. Un seul produit peut être attribué à plusieurs sites web ou limité à un seul. Si vous spécifiez plusieurs sites web, séparez-les par une virgule et sans espace. Par exemple : `base` ou `base,website2` |
| `name` | Le nom du produit apparaît dans toutes les listes de produits et est le nom que les clients utilisent pour identifier le produit. |
| `description` | La description du produit fournit des informations détaillées sur le produit et peut inclure des balises de HTML simples. |
| `short_description` | L’utilisation de la brève description du produit dépend du thème. Il peut apparaître dans les listes de produits et est parfois utilisé dans les listes de flux RSS envoyées aux sites d’achats. |
| `weight` | Le poids du produit individuel. Le poids réel du produit est déterminé par le transporteur au moment de l&#39;expédition. |
| product_online | Détermine si le produit est disponible en vente dans le magasin. Valeurs :<br/>`1` — (Oui) Le produit est activé et disponible à la vente.<br/>`2` — (Non) Le produit est désactivé et n’est pas disponible à la vente. |
| `tax_class_name` | Nom de la classe fiscale associée à ce produit. |
| `visibility` | Détermine si le produit est visible dans le catalogue et est disponible pour la recherche. Valeurs :<br/>`Not Visible Individually` — Le produit n’est pas inclus dans les listes de produits, bien qu’il puisse être disponible sous la forme d’une variante d’un autre produit.<br/>`Catalog` — Le produit apparaît dans toutes les listes de catalogues.<br/>`Search` : le produit est disponible pour les opérations de recherche.<br/>`Catalog, Search` — Le produit est inclus dans les listes de catalogues et peut également être recherché. |
| `price` | Le prix que le produit est proposé en vente dans votre boutique. |
| `special_price` | Prix réduit du produit pendant la période spécifiée. |
| `special_price_from_date` | Date de début de la période pendant laquelle le prix spécial est appliqué. |
| `special_price_to_date` | Dernière date de la période pendant laquelle le prix spécial est en vigueur. |
| `url_key` | Partie de l’URL qui identifie le produit. La valeur par défaut est basée sur le nom du produit. Par exemple: `product-name` |
| save_rewrites_history | Lorsque la valeur est fournie `1` avec une nouvelle `url_key`, une nouvelle réécriture d’URL 301 est générée afin que l’ancienne URL soit redirigée vers la nouvelle URL. |
| `meta_title` | Le méta-titre apparaît dans la barre de titre et l’onglet du navigateur et des listes de résultats de recherche. Le méta-titre doit être propre au produit, contenir des mots-clés à forte valeur ajoutée et contenir moins de 70 caractères. |
| `meta_keywords` | Les mots-clés de métadonnées sont visibles uniquement par les moteurs de recherche et sont ignorés par certains moteurs de recherche. Choisissez des mots-clés de valeur élevée, séparés par une virgule. Par exemple: `keyword1`, `keyword2`, `keyword3` |
| `meta_description` | Les métadonnées fournissent un bref aperçu du produit pour les listes de résultats de recherche. Idéalement, une méta-description doit comporter entre 150 et 160 caractères, bien que le champ accepte jusqu’à 255 caractères. |
| `base_image` | Chemin d’accès relatif de l’image principale sur la page du produit. Commerce stocke les fichiers en interne dans une structure de dossiers alphabétique. Vous pouvez voir l’emplacement exact de chaque image dans les données exportées. Par exemple : `/sample_data/m/b/mb01-blue-0.jpg`<br/>Pour charger une nouvelle image ou écraser sur une image existante, saisissez le nom du fichier, précédé d’une barre oblique. Par exemple: `/image.jpg` |
| `base_image_label` | Libellé associé à l’image de base. |
| `small_image` | Nom de fichier de la petite image utilisée sur les pages de catalogue, précédé d’une barre oblique. Par exemple: `/image.jpg` |
| `small_image_label` | libellé associé à la petite image. Par exemple: `Small Image 1`, `Small Image 2` |
| `thumbnail_image` | Les noms de fichier de toute miniature devant apparaître dans la galerie sur la page du produit, précédés d’une barre oblique. Par exemple: `/image.jpg` |
| `thumbnail_image_label` | Libellé associé à toutes les images miniatures. Par exemple: `Thumbnail 1`, `Thumbnail 2` |
| `created_at` | Indique la date de création du produit. La date est automatiquement générée lors de la création du produit, mais elle peut être modifiée ultérieurement. |
| `updated_at` | Indique la date de la dernière mise à jour du produit. |
| `new_from_date` | Indique la date &quot;à partir de&quot; pour les nouvelles listes de produits et détermine si le produit est présenté comme un nouveau produit. |
| `new_to_date` | Indique la date &quot;à&quot; pour les nouvelles listes de produits et détermine si le produit est présenté comme un nouveau produit. |
| `display_product_options_in` | Si le produit comporte plusieurs options, détermine où elles apparaissent sur la page du produit. Valeurs : colonne Infos produit / bloc après colonne Infos |
| `map_price` | Prix minimum annoncé du produit. (Apparaît uniquement si MAP est activé.) |
| `msrp_price` | Prix de détail suggéré par le fabricant pour le produit. (Apparaît uniquement si MAP est activé.) |
| `map_enabled` | Détermine si le prix publicitaire minimum est activé dans la configuration. Valeurs :<br/>`1` — (Oui) MAP est activé.<br/>`0` (ou vide) — (No) MAP n’est pas activé. |
| `gift_message_available` | Détermine si un message cadeau peut être inclus avec l’achat du produit. Valeurs :<br/>`1` — (Oui) L’option permettant d’inclure un message cadeau est présentée au client.<br/>`0` (ou vide) — (Non) L’option permettant d’inclure un message cadeau n’est pas présentée au client. |
| `custom_design` | Répertorie les thèmes disponibles qui peuvent être appliqués à la page de produits. |
| `custom_design_from` | Indique la date de début à laquelle le thème sélectionné est appliqué à la page du produit. |
| `custom_design_to` | Indique la date de fin à laquelle le thème sélectionné est appliqué à la page du produit. |
| `custom_layout_update` | Code XML supplémentaire appliqué en tant que mise en page est mis à jour vers la page du produit. |
| `page_layout` | Détermine la mise en page de la page du produit. Valeurs :<br/>`No layout updates` — Aucune modification n’est apportée à la mise en page.<br/>`1 column` — Applique une mise en page à une colonne à la page du produit.<br/>`2 columns with left bar` — Applique une mise en page à deux colonnes avec une barre latérale gauche à la page du produit.<br/>`2 columns with right bar` — Applique une mise en page à deux colonnes avec une barre latérale droite à la page du produit.<br/>`3 columns` — Applique une mise en page à trois colonnes à la page du produit.<br/>`empty` — Applique une mise en page vierge à la page du produit. |
| `product_options_container` | Si le produit comporte plusieurs options, détermine où elles apparaissent sur la page du produit. Valeurs : colonne Infos produit / bloc après colonne Infos |
| `msrp_display_actual_price_type` | Détermine où le prix réel d’un produit est visible pour le client. Valeurs :<br/>`In Cart` — Affiche le prix réel du produit dans le panier.<br/>`Before Order Confirmation` — Affiche le prix réel du produit à la fin du processus de passage en caisse, juste avant que la commande ne soit confirmée.<br/>`On Gesture` — Affiche le prix réel du produit dans une fenêtre contextuelle lorsque le client clique sur la variable _Clic pour le prix_ ou _Qu&#39;est-ce ?_ lien. |
| `country_of_manufacture` | Identifie le pays dans lequel le produit a été fabriqué. |
| `additional_attributes` | Attributs supplémentaires créés pour le produit. Par exemple: <br/>`has_options=0,required_options=0color=Black,has_options=0,required_options=0,size_general=XS` |
| `qty` | Quantité du produit actuellement en stock. |
| `out_of_stock_qty` | Niveau de stock qui détermine le produit à partir de la stock. |
| `use_config_min_qty` | Détermine si la valeur par défaut de la configuration est utilisée et correspond à la case à cocher Utiliser les paramètres de configuration . Valeurs :<br/>`1` — (Oui) Le paramètre de configuration par défaut est utilisé pour la valeur de cet attribut.<br/>`0` (ou vide) — (Non) La configuration par défaut peut être remplacée pour la valeur de cet attribut. |
| `is_qty_decimal` | Détermine si l’attribut qty a une valeur décimale. Valeurs :<br/>`1` — (Oui) La valeur de l’attribut qty est une valeur décimale.<br/>`0` (ou vide) — (Non) La valeur de l’attribut qty est un nombre entier (entier). |
| `allow_backorders` | Détermine si votre magasin autorise les commandes en arrière-plan et la manière dont elles sont gérées. |
| `use_config_backorders` | Détermine si le paramètre de configuration par défaut des commandes en arrière-plan est utilisé et correspond à l’état de la case à cocher Utiliser les paramètres de configuration . Valeurs :<br/>`1` — (Oui) La valeur de l’attribut qty est une valeur décimale.<br/>`0` (ou vide) — (Non) La valeur de l’attribut qty est un nombre entier (entier). |
| `min_cart_qty` | Indique la quantité minimale de l’article qui peut être acheté dans une seule commande. |
| `use_config_min_sale_qty` | Détermine si le paramètre de configuration par défaut pour la quantité minimale est utilisé et correspond à l’état de la case à cocher Utiliser les paramètres de configuration . Valeurs :<br/>`1` — (Oui)<br/>`0` (ou vide) — (Non) |
| `max_cart_qty` | Indique la quantité maximale de produits pouvant être achetés dans une seule commande. |
| `use_config_max_sale_qty` | Détermine si le paramètre de configuration par défaut pour la quantité maximale est utilisé et correspond à l’état de la case à cocher Utiliser les paramètres de configuration . Valeurs :<br/>`1` — (Oui)<br/>`0` (ou vide) — (Non) |
| `is_in_stock` | Indique si le produit est en stock. |
| `notify_on_stock_below` | Indique le niveau de stock qui déclenche une _en rupture de stock_ notification. |
| `use_config_notify_stock_qty` | Détermine si le paramètre de configuration par défaut est utilisé pour déclencher la notification au niveau du stock et correspond à l’état de la case à cocher Utiliser les paramètres de configuration . Valeurs :<br/>`1` — (Oui)<br/>`0` (ou vide) — (Non) |
| `manage_stock` | Détermine si le contrôle des stocks est utilisé pour gérer le produit. Valeurs :<br/>`1` — (Oui) Active le contrôle complet des stocks pour gérer les niveaux de stock du produit.<br/>`0` (ou vide) — (Non) Le système ne suit pas le nombre d’éléments actuellement en stock. |
| `use_config_manage_stock` | Détermine si le paramètre de configuration par défaut pour la gestion du stock est utilisé et correspond à l’état de la case à cocher Utiliser les paramètres de configuration . Valeurs :<br/>`1` — (Oui)<br/>`0` (ou vide) — (Non) |
| `use_config_qty_increments` | Détermine si le paramètre de configuration par défaut pour les incréments de quantité est utilisé et correspond à l’état de la case à cocher Utiliser les paramètres de configuration . Valeurs :<br/>`1` — (Oui)<br/>`0` (ou vide) — (Non) |
| `qty_increments` | Définit le nombre de produits qui constituent un incrément de quantité. |
| `use_config_enable_qty_inc` | Détermine si le paramètre de configuration par défaut pour activer les incréments de quantité est utilisé et correspond à l’état de la case à cocher Utiliser les paramètres de configuration . Valeurs :<br/>`1` — (Oui)<br/>`0` (ou vide) — (Non) |
| `enable_qty_increments` | Détermine si les incréments de quantité sont activés pour le produit. |
| `is_decimal_divided` | Détermine si des parties du produit peuvent être expédiées séparément. Options : `Yes` / `No` |
| `website_id` | Pour les installations comportant plusieurs sites web, identifie un site web spécifique sur lequel le produit est disponible. Si ce champ est vide, le produit est disponible sur tous les sites Web. |
| `related_skus` | Répertorie le SKU de chaque produit qui a été identifié comme un produit associé. Par exemple: `24-WG080,24-UG03,24-UG01,24-UG02` |
| `related_position` | Détermine la position (ordre de tri) des SKU répertoriés comme Produits associés dans la colonne related_skus . Par exemple: `1,2,3,4` |
| `crosssell_skus` | Répertorie le SKU de chaque produit identifié comme une vente croisée. |
| `crosssell_position` | Détermine la position (ordre de tri) des SKU répertoriés comme Produits de vente croisée dans la variable `crosssell_skus` colonne . |
| `upsell_skus` | Répertorie le SKU de chaque produit qui a été identifié comme une vente ascendante. |
| `upsell_position` | Détermine la position (ordre de tri) des SKU répertoriés en tant que produits de vente incitative dans la variable `upsell_skus` colonne . |
| `additional_images` | Les noms de fichier de toute image supplémentaire à associer au produit, précédés d’une barre oblique. Par exemple: `/image.jpg` |
| `additional_image_labels` | Libellés associés aux images supplémentaires. Par exemple: `Label 1`, `Label 2` |
| `custom_options` | Spécifie les propriétés et les valeurs attribuées à chaque option personnalisée. Par exemple: <br/>`name=Color, type=drop_down, required=1, price= price_type=fixed, sku=, option_title=Black|name=Color, type=drop_down, required=1, price=, price_type=fixed, sku=, option_title=White` |

{style="table-layout:auto"}

## Données de service pour les variations de produit

| Attribut | Description | S’applique à |
|--- |--- | --- |
| `_super_products_sku` | SKU généré pour une variation de produit configurable. Par exemple : WB03-XS-Green | Produits configurables |
| `_super_attribute_code` | Le code d’attribut d’une variation de produit configurable. Par exemple : couleur | Produits configurables |
| `_super_attribute_option` | La valeur d’une variation de produit configurable. Par exemple : vert | Produits configurables |
| `_super_attribute_price_corr` | Ajustement de prix associé à une variation de produit configurable. | Produits configurables |
| `_associated_sku` | SKU d’un produit associé à un produit groupé. | Produits regroupés <br/>Produits groupés |
| `_associated_default_qty` | Détermine la quantité du produit associé qui est incluse. | Produits configurables<br/>Produits regroupés<br/>Produits groupés |
| `_associated_position` | Détermine la position du produit associé lorsqu’il est répertorié avec d’autres produits associés. | Produits configurables<br/>Produits regroupés<br/>Produits groupés |

{style="table-layout:auto"}

## Attributs de données de produit complexes

Le terme données complexes fait référence aux données associées à plusieurs options de produit. Les types de produits suivants utilisent des données provenant de produits distincts pour créer des variantes de produits et plusieurs options.

- [Configurable](../catalog/product-create-configurable.md)
- [Regroupé](../catalog/product-create-grouped.md)
- [Bundle](../catalog/product-create-bundle.md)

Si vous exportez un produit configurable, vous trouverez les attributs standard qui constituent un produit simple, ainsi que les attributs supplémentaires nécessaires à la gestion des données complexes.

![Produit configurable - données exportées](./assets/data-exported-configurable-product.png){width="600" zoomable="yes"}

### Produits configurables

| Attribut | Description |
|--- |--- |
| `configurable_variation_labels` | Étiquettes qui identifient les variations de produit. Par exemple : `Choose Color:` ou `Choose Size:` |
| `configurable_variations` | Décrit les valeurs associées à une variation de produit. Par exemple: `sku=sku-red xs,color=red,size=xs,price=10.99,display=1,image=/pub/media/import/image1.png|sku=sku-red-m,color=red,size=m,price=20.88,display=1,image=/pub/media/import/image2.png` |

{style="table-layout:auto"}

### Produits regroupés

| Attribut | Description |
|--- |--- |
| `associated_skus` | Identifie les SKU des produits individuels qui constituent le groupe. |

{style="table-layout:auto"}

### Lot de produits

| Attribut | Description |
|--- |--- |
| `bundle_price_type` | Détermine si le prix d’un élément de lot est fixe ou dynamique. |
| `bundle_sku_type` | Détermine si chaque élément se voit attribuer une variable, un SKU dynamique ou si un SKU fixe est utilisé pour le lot. Options : fixes / dynamiques |
| `bundle_weight_type` | Détermine si le poids d’un élément de lot est variable ou fixe. |
| `bundle_values` | Décrit la valeur d’apprentissage associée à une option de lot. Par exemple: `name=Bundle Option One,type=dropdown; required=1, sku=sku-option2,price=10, price_type=fixed` |

{style="table-layout:auto"}

## Attributs de tarification avancés

L’importation/exportation de prix avancés vous permet de mettre rapidement à jour les informations de tarification pour les groupes de produits et les prix de niveau. Le processus de [import](data-import.md) et [export](data-export.md) les données de prix avancées sont identiques à tout autre type d’entité. L’exemple de fichier CSV contient les prix des niveaux et des groupes pour chaque type de produit prenant en charge la tarification avancée. La modification des tarifs avancés n’a aucune incidence sur le reste de l’enregistrement du produit.

![Exemples de données d’exportation - prix avancé](./assets/data-advanced-pricing-export-sample.png){width="600" zoomable="yes"}

| Attribut | Description |
|--- |--- |
| `sku` | (Obligatoire) L’unité de gestion des stocks est un identifiant alphanumérique unique utilisé pour effectuer le suivi du stock. Un SKU peut comporter jusqu’à 64 caractères. Par exemple : `sku123`<br/>**_Remarque :_**Un SKU de plus de 64 caractères provoque l’échec de l’importation. |
| `tier_price_website` | La variable [code du site web](../stores-purchase/stores.md#add-websites) identifie chaque site web sur lequel des tarifs de niveau sont disponibles. Par exemple: `-  website1 -  All Websites [USD]` |
| `tier_price_customer` | Identifie la variable [groupes de clients](../customers/customer-groups.md) où le prix de niveau est disponible. Par exemple: `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `tier_price_customer_group` | Identifie les groupes de clients dans lesquels le niveau de prix est disponible. Par exemple: `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `tier_price_qty` | Quantité du produit qui doit être commandé pour recevoir la remise de prix de niveau. |
| `tier_price` | Prix de niveau réduit du produit. Pour [regroupement de produits](../catalog/product-create-bundle.md), le prix du niveau est calculé en pourcentage. |
| `group_price_website` | La variable [code du site web](../stores-purchase/stores.md#add-websites) de chaque site web sur lequel des tarifs de groupe sont disponibles. Si vous spécifiez plusieurs sites web, séparez-les par une virgule et sans espace. Par exemple: `-  website1 -  All Websites [USD]` |
| `group_price_customer_group` | Identifie les groupes de clients dans lesquels le prix de groupe est disponible. Par exemple: `-  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `group_price` | Prix de groupe réduit du produit. Pour [regroupement de produits](../catalog/product-create-bundle.md), le prix du groupe est calculé en pourcentage. |

{style="table-layout:auto"}
