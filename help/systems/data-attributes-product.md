---
title: Référence des attributs de données de produit
description: Utilisez cette référence d’attributs de données de produit lorsque vous utilisez des importations et des exportations de données de produit.
exl-id: 9ffa4d1f-cbf8-4a08-bb79-33f21e698a74
feature: Products, Attributes
source-git-commit: 976efad9fb4bb53f6f102fde534001d254cd3b9c
workflow-type: tm+mt
source-wordcount: '2496'
ht-degree: 0%

---

# Référence des attributs de données de produit

Le tableau suivant répertorie les attributs d’une exportation de produit type, dans l’ordre par défaut dans lequel ils apparaissent. Chaque attribut est représenté dans le fichier CSV sous la forme d’une colonne et les enregistrements de produit sont représentés par des lignes. Les colonnes qui commencent par un trait de soulignement contiennent des données de service telles que des propriétés ou des valeurs d’option pour des données complexes. Vous pouvez [exporter](data-export.md) un produit de votre catalogue pour voir comment chaque attribut est représenté dans les données.

L’installation utilisée pour exporter ces données dispose des données d’exemple et de deux sites web et de plusieurs vues de magasin. Bien que cette liste contienne toutes les colonnes généralement exportées, la `sku` est la seule valeur requise. Pour importer des données, vous ne pouvez inclure que les colonnes modifiées. L’`sku` doit être la première colonne, mais l’ordre du reste des attributs n’a pas d’importance.

## Structure de fichier CSV de produit simple

| Attribut | Description |
|--- |--- |
| `sku` | (Obligatoire) L&#39;unité de gestion des stocks est un identificateur alphanumérique unique utilisé pour effectuer le suivi des stocks. Un SKU peut comporter jusqu’à 64 caractères. Par exemple : `sku123`<br/>**_Remarque :_**&#x200B;un SKU de plus de 64 caractères entraîne l’échec de l’importation. |
| `store_view_code` | Indique les vues de magasin spécifiques où le produit est disponible. Si ce champ est vide, le produit est disponible dans la vue de magasin par défaut. Par exemple : `storeview1`, `english`, `spanish` |
| `attribute_set_code` | Attribue le produit à un jeu d’attributs ou à un modèle de produit spécifique, en fonction du type de produit. Par exemple : `default`<br><br> Une fois le produit créé, le jeu d’attributs ne peut pas être modifié à l’aide de la fonctionnalité d’importation. Cependant, vous pouvez modifier le jeu d’attributs à partir de l’Administration et réexporter le produit pour mettre à jour le fichier CSV . |
| `product_type` | Indique le type de produit. Valeurs : <br/>`simple` — Articles corporels qui sont généralement vendus en unités uniques ou en quantités fixes.<br/>`grouped` — Groupe de produits séparés vendus sous forme d&#39;ensemble.<br/>`configurable` : produit avec plusieurs options que le client doit sélectionner avant d&#39;effectuer un achat. L’inventaire peut être géré pour chaque ensemble de variations, car ils représentent un produit distinct avec un SKU distinct. Par exemple, une combinaison de couleur et de taille pour un produit configurable est associée à un SKU spécifique dans le catalogue.<br/>`virtual` — Produit non tangible qui ne nécessite pas d&#39;expédition et qui n&#39;est pas conservé en stock. Par exemple, les services, les abonnements et les abonnements.<br/>`bundle` — Ensemble personnalisable de produits simples qui sont vendus ensemble. |
| `categories` | Indique chaque catégorie affectée au produit. Catégories et sous-catégories distinctes avec une barre oblique. Pour indiquer plusieurs chemins d’accès aux catégories, séparez chaque chemin par une barre verticale \| symbole. Par exemple : `Default Category/Gear\|Default Category/Gear/Bags` |
| `product_websites` | Code de chaque site web sur lequel le produit est disponible. Un seul produit peut être attribué à plusieurs sites web ou limité à un seul. Si vous spécifiez plusieurs sites web, séparez-les par une virgule, sans espace. Par exemple : `base` ou `base,website2` |
| `name` | Le nom du produit apparaît dans toutes les listes de produits et correspond au nom que les clients utilisent pour identifier le produit. |
| `description` | La description du produit fournit des informations détaillées sur le produit et peut inclure de simples balises HTML. |
| `short_description` | L’utilisation de la brève description du produit dépend du thème. Il peut apparaître dans les listes de produits et est parfois utilisé dans les listes de flux RSS envoyées aux sites d&#39;achat. |
| `weight` | Poids du produit individuel. Le poids réel du produit est déterminé par le transporteur au moment de l&#39;expédition. |
| product_online | Détermine si le produit est disponible à la vente dans le magasin. Valeurs : <br/>`1` — (Oui) Le produit est activé et disponible à la vente.<br/>`2` — (Non) Le produit est désactivé et ne peut pas être vendu. |
| `tax_class_name` | Nom de la classe de taxe associée à ce produit. |
| `visibility` | Détermine si le produit est visible dans le catalogue et s’il est disponible pour la recherche. Valeurs : <br/>`Not Visible Individually` — Le produit n&#39;est pas inclus dans les listes de produits, bien qu&#39;il puisse être disponible comme variante d&#39;un autre produit.<br/>`Catalog` — Le produit apparaît dans toutes les listes du catalogue.<br/>`Search` : le produit est disponible pour les opérations de recherche.<br/>`Catalog, Search` — Le produit est inclus dans les listes de catalogue et peut également faire l&#39;objet de recherches. |
| `price` | Le prix auquel le produit est proposé à la vente dans votre magasin. |
| `special_price` | Prix réduit du produit au cours de la période spécifiée. |
| `special_price_from_date` | Date de début de la période pendant laquelle le prix spécial est en vigueur. |
| `special_price_to_date` | Dernière date de la période pendant laquelle le prix spécial est en vigueur. |
| `url_key` | Partie de l’URL qui identifie le produit. La valeur par défaut est basée sur le nom du produit. Par exemple : `product-name` |
| save_rewrites_history | Lorsque la valeur est `1` avec une nouvelle `url_key`, une nouvelle réécriture d’URL 301 est générée afin que l’ancienne URL soit redirigée vers la nouvelle. |
| `meta_title` | Le méta-titre s’affiche dans la barre de titre et dans l’onglet des listes du navigateur et des résultats de recherche. Le méta-titre doit être propre au produit, incorporer des mots-clés de grande valeur et comporter moins de 70 caractères. |
| `meta_keywords` | Les méta-mots-clés ne sont visibles que par les moteurs de recherche et sont ignorés par certains d’entre eux. Choisissez des mots-clés de valeur élevée, séparés par une virgule. Par exemple : `keyword1`, `keyword2`, `keyword3` |
| `meta_description` | Les méta-descriptions fournissent un bref aperçu du produit pour les listes de résultats de recherche. Idéalement, une méta-description doit comporter entre 150 et 160 caractères, bien que le champ accepte jusqu’à 255 caractères. |
| `base_image` | Chemin d’accès relatif de l’image principale sur la page du produit. Commerce stocke les fichiers en interne dans une structure de dossiers alphabétique. Vous pouvez voir l’emplacement exact de chaque image dans les données exportées. Par exemple : `/sample_data/m/b/mb01-blue-0.jpg`<br/>pour charger une nouvelle image ou écraser sur une image existante, saisissez le nom du fichier, précédé d’une barre oblique. Par exemple : `/image.jpg` |
| `base_image_label` | Libellé associé à l’image de base. |
| `small_image` | Nom de fichier de la petite image utilisée sur les pages du catalogue, précédé d’une barre oblique. Par exemple : `/image.jpg` |
| `small_image_label` | Libellé associé à la petite image. Par exemple : `Small Image 1`, `Small Image 2` |
| `thumbnail_image` | Noms de fichier de toute image miniature devant apparaître dans la galerie sur la page du produit, précédée d’une barre oblique. Par exemple : `/image.jpg` |
| `thumbnail_image_label` | Libellé associé à toutes les images miniatures. Par exemple : `Thumbnail 1`, `Thumbnail 2` |
| `created_at` | Indique la date à laquelle le produit a été créé. La date est automatiquement générée lors de la création du produit, mais peut être modifiée ultérieurement. |
| `updated_at` | Indique la date de la dernière mise à jour du produit. |
| `new_from_date` | Indique la date « de » pour les nouvelles listes de produits et détermine si le produit est présenté comme un nouveau produit. |
| `new_to_date` | Indique la date de fin des nouvelles listes de produits et détermine si le produit est présenté comme un nouveau produit. |
| `display_product_options_in` | Si le produit comporte plusieurs options, détermine où elles apparaissent sur la page du produit. Valeurs : colonne d’informations sur le produit / bloc après colonne d’informations |
| `map_price` | Prix minimum annoncé du produit. (S’affiche uniquement si MAP est activé.) |
| `msrp_price` | Prix de détail suggéré par le fabricant pour le produit. (S’affiche uniquement si MAP est activé.) |
| `map_enabled` | Détermine si le prix minimum annoncé est activé dans la configuration. Values:<br/>`1` — (Oui) MAP est activé.<br/>`0` (ou vide) — (Non) MAP n’est pas activé. |
| `gift_message_available` | Détermine si un message cadeau peut être inclus dans l&#39;achat du produit. Valeurs : <br/>`1` — (Oui) L&#39;option d&#39;inclure un message cadeau est présentée au client.<br/>`0` (ou vide) — (Non) L&#39;option d&#39;inclure un message cadeau n&#39;est pas présentée au client. |
| `custom_design` | Répertorie les thèmes disponibles qui peuvent être appliqués à la page du produit. |
| `custom_design_from` | Spécifie la date de début à laquelle le thème sélectionné est appliqué à la page produit. |
| `custom_design_to` | Spécifie la date de fin à laquelle le thème sélectionné est appliqué à la page produit. |
| `custom_layout_update` | Code XML supplémentaire appliqué en tant que mise à jour de mise en page à la page du produit. |
| `page_layout` | Détermine la mise en page de la page produit. Valeurs : <br/>`No layout updates` — Aucune modification n&#39;est apportée à la mise en page.<br/>`1 column` — Applique une mise en page d&#39;une colonne à la page produit.<br/>`2 columns with left bar` — Applique une disposition à deux colonnes avec une barre latérale gauche à la page produit.<br/>`2 columns with right bar` — Applique une disposition à deux colonnes avec une barre latérale droite à la page produit.<br/>`3 columns` — Applique une disposition en trois colonnes à la page produit.<br/>`empty` — Applique une mise en page vierge à la page du produit. |
| `product_options_container` | Si le produit comporte plusieurs options, détermine où elles apparaissent sur la page du produit. Valeurs : colonne d’informations sur le produit / bloc après colonne d’informations |
| `msrp_display_actual_price_type` | Détermine où le prix réel d&#39;un produit est visible pour le client. Valeurs : <br/>`In Cart` — Affiche le prix réel du produit dans le panier.<br/>`Before Order Confirmation` : affiche le prix réel du produit à la fin du processus de passage en caisse, juste avant la confirmation de la commande.<br/>`On Gesture` — Affiche le prix réel du produit dans une fenêtre contextuelle lorsque le client clique sur le _Cliquer pour connaître le prix_ ou _Qu&#39;est-ce que c&#39;est ?Lien_. |
| `country_of_manufacture` | Indique le pays dans lequel le produit a été fabriqué. |
| `additional_attributes` | Attributs supplémentaires créés pour le produit. Par exemple : <br/>`has_options=0,required_options=0color=Black,has_options=0,required_options=0,size_general=XS` |
| `qty` | Quantité du produit actuellement en stock. |
| `out_of_stock_qty` | Niveau de stock qui détermine si le produit est en rupture de stock. |
| `use_config_min_qty` | Détermine si la valeur par défaut de la configuration est utilisée et correspond à la case Utiliser les paramètres de configuration . Values:<br/>`1` — (Oui) Le paramètre de configuration par défaut est utilisé pour la valeur de cet attribut.<br/>`0` (ou vide) — (Non) La configuration par défaut peut être remplacée pour la valeur de cet attribut. |
| `is_qty_decimal` | Détermine si l&#39;attribut qty a une valeur décimale. Values:<br/>`1` — (Oui) La valeur de l&#39;attribut qty est une valeur décimale.<br/>`0` (ou vide) — (Non) La valeur de l&#39;attribut qty est un nombre entier (entier). |
| `allow_backorders` | Détermine si votre magasin autorise les reliquats et comment ils sont gérés. |
| `use_config_backorders` | Détermine si le paramètre de configuration par défaut pour les commandes en souffrance est utilisé et correspond au statut de la case Utiliser les paramètres de configuration . Values:<br/>`1` — (Oui) La valeur de l&#39;attribut qty est une valeur décimale.<br/>`0` (ou vide) — (Non) La valeur de l&#39;attribut qty est un nombre entier (entier). |
| `min_cart_qty` | Spécifie la quantité minimale de l&#39;article qui peut être achetée dans une seule commande. |
| `use_config_min_sale_qty` | Détermine si le paramètre de configuration par défaut pour la quantité minimale est utilisé et correspond au statut de la case Utiliser les paramètres de configuration . Valeurs : <br/>`1` — (Oui)<br/>`0` (ou vide) — (Non) |
| `max_cart_qty` | Spécifie la quantité maximale du produit qui peut être achetée dans une seule commande. |
| `use_config_max_sale_qty` | Détermine si le paramètre de configuration par défaut pour la quantité maximale est utilisé et correspond au statut de la case Utiliser les paramètres de configuration . Valeurs : <br/>`1` — (Oui)<br/>`0` (ou vide) — (Non) |
| `is_in_stock` | Indique si le produit est en stock. |
| `notify_on_stock_below` | Spécifie le niveau de stock qui déclenche une notification _rupture de stock_. |
| `use_config_notify_stock_qty` | Détermine si le paramètre de configuration par défaut est utilisé pour déclencher une notification au niveau du stock et correspond au statut de la case à cocher Utiliser les paramètres de configuration . Valeurs : <br/>`1` — (Oui)<br/>`0` (ou vide) — (Non) |
| `manage_stock` | Détermine si le contrôle de stock est utilisé pour gérer le produit. Valeurs : <br/>`1` — (Oui) Active le contrôle complet des stocks pour gérer les niveaux de stock du produit.<br/>`0` (ou vide) — (Non) Le système ne suit pas le nombre d&#39;articles actuellement en stock. |
| `use_config_manage_stock` | Détermine si le paramètre de configuration par défaut pour la gestion du stock est utilisé et correspond au statut de la case Utiliser les paramètres de configuration . Valeurs : <br/>`1` — (Oui)<br/>`0` (ou vide) — (Non) |
| `use_config_qty_increments` | Détermine si le paramètre de configuration par défaut pour les incréments de quantité est utilisé et correspond au statut de la case Utiliser les paramètres de configuration . Valeurs : <br/>`1` — (Oui)<br/>`0` (ou vide) — (Non) |
| `qty_increments` | Définit le nombre de produits qui constituent une augmentation de quantité. |
| `use_config_enable_qty_inc` | Détermine si le paramètre de configuration par défaut pour activer les incréments de quantité est utilisé et correspond au statut de la case à cocher Utiliser les paramètres de configuration . Valeurs : <br/>`1` — (Oui)<br/>`0` (ou vide) — (Non) |
| `enable_qty_increments` | Détermine si les incréments de quantité sont activés pour le produit. |
| `is_decimal_divided` | Détermine si des parties du produit peuvent être expédiées séparément. Options : `Yes` / `No` |
| `website_id` | Pour les installations comportant plusieurs sites web, identifie un site web spécifique sur lequel le produit est disponible. Si ce champ est vide, le produit est disponible sur tous les sites web. |
| `related_skus` | Répertorie le SKU de chaque produit identifié comme un produit associé. Par exemple : `24-WG080,24-UG03,24-UG01,24-UG02` |
| `related_position` | Détermine la position (ordre de tri) des SKU répertoriés en tant que Produits associés dans la colonne related_skus. Par exemple : `1,2,3,4` |
| `crosssell_skus` | Répertorie le SKU de chaque produit qui a été identifié comme une vente croisée. |
| `crosssell_position` | Détermine la position (ordre de tri) des SKU répertoriés en tant que Produits de ventes croisées dans la colonne `crosssell_skus`. |
| `upsell_skus` | Répertorie le SKU de chaque produit qui a été identifié comme une vente incitative. |
| `upsell_position` | Détermine la position (ordre de tri) des SKU répertoriés en tant que produits de mise à niveau dans la colonne `upsell_skus`. |
| `additional_images` | Noms de fichier de toute image supplémentaire à associer au produit, précédée d’une barre oblique. Par exemple : `/image.jpg` |
| `additional_image_labels` | Libellés associés à toute image supplémentaire. Par exemple : `Label 1`, `Label 2` |
| `custom_options` | Spécifie les propriétés et les valeurs affectées à chaque option personnalisée. Par exemple : <br/>`name=Color, type=drop_down, required=1, price= price_type=fixed, sku=, option_title=Black|name=Color, type=drop_down, required=1, price=, price_type=fixed, sku=, option_title=White` |

{style="table-layout:auto"}

## Données de service pour les variations de produit

| Attribut | Description | Application |
|--- |--- | --- |
| `_super_products_sku` | SKU généré pour une variation de produit configurable. Par exemple : WB03-XS-Green | Produits configurables |
| `_super_attribute_code` | Code d’attribut d’une variation de produit configurable. Par exemple : color | Produits configurables |
| `_super_attribute_option` | Valeur d’une variation de produit configurable. Par exemple : vert | Produits configurables |
| `_super_attribute_price_corr` | Ajustement de prix associé à une variation de produit configurable. | Produits configurables |
| `_associated_sku` | SKU d’un produit associé à un produit regroupé. | Produits groupés <br/>Produits groupés |
| `_associated_default_qty` | Détermine la quantité du produit associé inclus. | Produits configurables<br/>produits groupés<br/>produits groupés |
| `_associated_position` | Détermine la position du produit associé lorsqu&#39;il est répertorié avec d&#39;autres produits associés. | Produits configurables<br/>produits groupés<br/>produits groupés |

{style="table-layout:auto"}

## Attributs de données de produit complexes

Le terme données complexes fait référence aux données associées à plusieurs options de produit. Les types de produits suivants utilisent des données provenant de produits distincts pour créer des variations de produit et plusieurs options.

- [Paramétrable](../catalog/product-create-configurable.md)
- [Regroupé](../catalog/product-create-grouped.md)
- [Bundle](../catalog/product-create-bundle.md)

Si vous exportez un produit configurable, vous y trouverez les attributs standard qui constituent un produit simple, ainsi que les attributs supplémentaires nécessaires à la gestion de données complexes.

![Produit configurable - données exportées](./assets/data-exported-configurable-product.png){width="600" zoomable="yes"}

### Produits configurables

| Attribut | Description |
|--- |--- |
| `configurable_variation_labels` | Étiquettes qui identifient les variations de produit. Par exemple : `Choose Color:` ou `Choose Size:` |
| `configurable_variations` | Décrit les valeurs associées à une variation de produit. Par exemple : `sku=sku-red xs,color=red,size=xs,price=10.99,display=1,image=/pub/media/import/image1.png|sku=sku-red-m,color=red,size=m,price=20.88,display=1,image=/pub/media/import/image2.png` |

{style="table-layout:auto"}

### Produits groupés

| Attribut | Description |
|--- |--- |
| `associated_skus` | Identifie les SKU des produits individuels qui constituent le groupe. |

{style="table-layout:auto"}

### Lots de produits

| Attribut | Description |
|--- |--- |
| `bundle_price_type` | Détermine si le prix d&#39;un article groupé est fixe ou dynamique. |
| `bundle_sku_type` | Détermine si chaque élément se voit attribuer une variable, un SKU dynamique ou si un SKU fixe est utilisé pour le lot. Options : Fixe/Dynamique |
| `bundle_weight_type` | Détermine si le poids d&#39;un élément groupé est variable ou fixe. |
| `bundle_values` | Décrit la valeur d’apprentissage associée à une option de lot. Par exemple : `name=Bundle Option One,type=dropdown; required=1, sku=sku-option2,price=10, price_type=fixed` |

{style="table-layout:auto"}

## Attributs de tarification avancés

L&#39;importation/exportation de prix avancés vous permet de mettre rapidement à jour les informations de prix pour les groupes de produits et les prix de niveau. Le processus d&#39;[import](data-import.md) et d&#39;[export](data-export.md) des données de prix avancées est le même que pour tout autre type d&#39;entité. L’exemple de fichier CSV contient des prix de niveau et de groupe pour chaque type de produit qui prend en charge la tarification avancée. La modification du prix avancé n&#39;affecte pas le reste de l&#39;enregistrement du produit.

![Exemple de données d’exportation - Tarification avancée](./assets/data-advanced-pricing-export-sample.png){width="600" zoomable="yes"}

| Attribut | Description |
|--- |--- |
| `sku` | (Obligatoire) L&#39;unité de gestion des stocks est un identificateur alphanumérique unique utilisé pour effectuer le suivi des stocks. Un SKU peut comporter jusqu’à 64 caractères. Par exemple : `sku123`<br/>**_Remarque :_**&#x200B;un SKU de plus de 64 caractères entraîne l’échec de l’importation. |
| `tier_price_website` | Le [code du site web](../stores-purchase/stores.md#add-websites) identifie chaque site web sur lequel une tarification par niveau est disponible. Par exemple : `-  website1 -  All Websites [USD]` |
| `tier_price_customer` | Identifie les [groupes de clients](../customers/customer-groups.md) où la tarification de niveau est disponible. Par exemple : `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `tier_price_customer_group` | Identifie les groupes de clients pour lesquels une tarification de niveau est disponible. Par exemple : `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `tier_price_qty` | Quantité du produit qui doit être commandé pour recevoir la remise de prix de niveau. |
| `tier_price` | Prix de niveau réduit du produit. Pour les [produits groupés](../catalog/product-create-bundle.md), le prix du niveau est calculé en tant que pourcentage. |
| `group_price_website` | Le [code du site web](../stores-purchase/stores.md#add-websites) de chaque site web sur lequel la tarification du groupe est disponible. Si vous spécifiez plusieurs sites web, séparez-les par une virgule, sans espace. Par exemple : `-  website1 -  All Websites [USD]` |
| `group_price_customer_group` | Identifie les groupes de clients pour lesquels une tarification de groupe est disponible. Par exemple : `-  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `group_price` | Prix de groupe réduit du produit. Pour les [produits groupés](../catalog/product-create-bundle.md), le prix du groupe est calculé en tant que pourcentage. |

{style="table-layout:auto"}
