---
title: Étendue de la configuration
description: Découvrez comment définir la portée des paramètres de configuration dans l’administrateur Commerce.
exl-id: b7b87ac5-dc7d-472f-af24-52b4d12e46c5
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 0%

---

# Étendue de la configuration

Le sélecteur de vue de magasin situé dans le coin supérieur gauche de nombreuses pages de configuration filtre l’affichage de la page pour une portée spécifique et définit la valeur de certaines entités utilisées par Commerce. Il répertorie chaque niveau de la hiérarchie par nom et est utilisé pour remplacer la portée par un autre niveau. Tous les paramètres représentant la portée actuelle sont grisés. Dès lors, seuls ceux représentant le paramètre de portée actuel sont disponibles. La portée est initialement définie sur _Default Config_. Pour les utilisateurs administrateurs disposant d’un accès limité, la liste des vues de magasin disponibles inclut uniquement celles auxquelles l’utilisateur dispose de l’ [autorisation](../systems/permissions.md) d’accès.

| Niveau | Description |
|--- |--- |
| [!UICONTROL Default Config] | Configuration système par défaut. |
| [!UICONTROL Main Website] | Nom du site web en haut de la hiérarchie. |
| [!UICONTROL Main Website Store] | Nom du magasin par défaut associé au site web parent. |
| [!UICONTROL Default Store View] | Nom de la vue de magasin par défaut associée au magasin parent. |
| [!UICONTROL Stores Configuration] | Accède à la grille Magasins et revient à sélectionner [!UICONTROL Stores] > [!UICONTROL All Stores] dans la barre latérale d’administration. |

{style="table-layout:auto"}

![Coches Utiliser la valeur système sélectionnées](./assets/store-view-control.png){width="700" zoomable="yes"}

## [!UICONTROL Use system value]

La case à cocher _[!UICONTROL Use System Value]_&#x200B;située à droite de nombreux paramètres de configuration est utilisée pour appliquer ou remplacer la valeur de champ par défaut dans la portée de configuration actuelle. La valeur du champ par défaut ne peut pas être modifiée lorsque la case à cocher est cochée. Pour modifier la valeur, décochez la case et saisissez la nouvelle valeur. Vous êtes invité à confirmer la modification de la valeur système.

Le libellé de la case à cocher change en fonction de la portée actuelle et fait toujours référence au niveau parent qui est une étape de la hiérarchie de la portée. Le niveau parent étant un conteneur pour tous les éléments situés en dessous de ce niveau, le paramètre de portée du niveau parent est hérité, sauf s’il est remplacé.

## Options de valeur par défaut

| Case à cocher | Description |
|--- |--- |
| [!UICONTROL Use system value] | Cette case à cocher s’affiche lorsque la portée de configuration est définie sur `Default Config`. |
| [!UICONTROL Use Default] | Cette case à cocher s’affiche lorsque la portée de configuration est définie sur Principal `Website` et fait référence au magasin par défaut affecté au site web. |
| [!UICONTROL Use Website] | Cette case à cocher s’affiche lorsque la portée de configuration est définie sur une vue de magasin spécifique. Lorsqu’elle est sélectionnée, elle utilise le paramètre du site Web parent associé à la vue de magasin. Dans ce cas, le niveau de la boutique est ignoré, car il est entendu qu’il s’applique à la boutique par défaut associée au site web. |

{style="table-layout:auto"}

## Définition de la portée

Avant d’effectuer un paramètre de configuration qui s’applique uniquement à une vue de site web, de magasin ou de magasin spécifique, procédez comme suit :

1. Dans la barre latérale _Admin_, effectuez l’une des opérations suivantes :

   - Pour la plupart des paramètres de configuration, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - Pour [ paramètres de conception ](../content-design/configuration.md), accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**. Ensuite, dans la grille, sélectionnez la vue de magasin appropriée.

1. Accédez au paramètre de configuration à modifier et procédez comme suit :

   - Dans le coin supérieur gauche, définissez **[!UICONTROL Store View]** sur la vue spécifique dans laquelle s’applique la configuration. Lorsque vous êtes invité à confirmer le changement de portée, cliquez sur **[!UICONTROL OK]**.

     Une case à cocher s’affiche après chaque champ ; d’autres champs peuvent être disponibles.

   - Décochez la case **[!UICONTROL Use system value]** après tout champ que vous souhaitez modifier. Ensuite, mettez à jour la valeur de la vue.

   - Répétez cette procédure pour chaque champ qui doit être mis à jour sur la page.

   ![Définition des options Pays de la vue de magasin française](./assets/store-view-french.png){width="700" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

## Référence rapide sur la portée

| Portée | Description |
|--- |--- |
| **[!UICONTROL Global]** |  |
| Administration | Tous les sites web, magasins et vues de magasin de l’installation sont gérés à partir du même administrateur. |
| Configuration par défaut | Les paramètres globaux [configuration par défaut](../getting-started/websites-stores-views.md#scope-settings) sont utilisés par l’intermédiaire de la hiérarchie de magasin, sauf s’ils sont remplacés à un niveau inférieur. |
| Catalogue | Le terme _catalog_ fait référence à la base de données de produits dans son ensemble et est disponible tout au long de l’installation. |
| Prix du produit | Les prix des produits peuvent être configurés pour une application au niveau global ou au niveau du site web. |
| Configurations de produits | Les attributs utilisés comme options de [produit configurable](../catalog/product-create-configurable.md) doivent avoir une portée globale. |
| Clients | Les comptes clients peuvent être configurés pour une application au niveau global ou au niveau du site web. Chaque site web peut avoir un ensemble distinct de [comptes clients](../customers/customer-account-scope.md) ou partager des comptes clients avec d’autres sites web dans l’installation. |
| **[!UICONTROL Website]** |  |
| Domaine | D&#39;autres [sites web](../stores-purchase/introduction.md#store-structure) peuvent être configurés en tant que sous-domaines du domaine principal ou ont des adresses IP et des domaines dédiés distincts. |
| Clients | Les comptes clients peuvent être configurés pour une application au niveau global ou au niveau du site web. Chaque site web peut avoir un ensemble distinct de [comptes clients](../customers/customer-account-scope.md) ou partager des comptes clients avec d’autres sites web dans l’installation. |
| Devise | Chaque site web peut se voir attribuer une [devise de base](../stores-purchase/currency-configuration.md) différente. La devise de base est utilisée pour traiter toutes les transactions, bien qu’une devise d’affichage différente puisse apparaître pour le client, selon les paramètres régionaux de la vue de magasin. |
| Produits | Les produits individuels sont affectés à la hiérarchie au niveau du site web. La grille Produits répertorie tous les produits du catalogue, ainsi que les sites web sur lesquels ils sont disponibles. Le paramètre [Produit sur les sites web](../catalog/settings-basic-websites.md) identifie chaque site web sur lequel le produit est disponible. |
| Prix du produit | [Les prix des produits](../catalog/catalog-price-scope.md) peuvent être configurés pour une application au niveau global ou au niveau du site web. |
| Méthodes de paiement | [Les méthodes de paiement](../stores-purchase/payments.md) sont configurées au niveau du site web, bien que le titre et les instructions puissent être configurés pour chaque vue de magasin. |
| Passage en caisse | Le [processus de passage en caisse](../stores-purchase/checkout-process.md) a lieu au niveau du site web, bien que certaines options d’affichage puissent être configurées pour chaque vue de magasin. Tous les magasins associés à un site web ont la même [configuration de passage en caisse](../stores-purchase/checkout-process.md#checkout-options). |
| Pays autorisés | Les pays autorisés peuvent être configurés au niveau du site web. Les paramètres [pays autorisés](../getting-started/store-details.md#country-options) sont utilisés dans le passage en caisse pour limiter la provenance d’un client. |
| **[!UICONTROL Store]** |  |
| Domaine | Avec plusieurs magasins, chaque magasin peut avoir le même domaine, un sous-domaine ou des domaines distincts. Pour plus d&#39;informations, voir [Ajout de magasins](../stores-purchase/stores.md#add-stores). |
| Catégorie racine | Chaque boutique peut comporter un ensemble distinct de produits et de menus principaux, reposant sur une catégorie et des sous-catégories &quot;racine&quot;. Chaque catalogue possède une [catégorie racine](../catalog/category-root.md) affectée au niveau du magasin. |
| **[!UICONTROL Store View]** |  |
| Sous-catégories | Les [sous-catégories](../catalog/category-create.md#category-structure) qui constituent le menu principal (sous la racine) sont affectées au niveau de la vue du magasin. |
| Paramètres régionaux | Chaque vue de magasin peut se voir attribuer un [paramètre régional](../getting-started/store-details.md#locale-options) différent. La devise d’affichage, les unités de mesure et l’interface d’administration sont spécifiques aux paramètres régionaux. |
| Langues | Pour prendre en charge plusieurs langues, tout le contenu, y compris les descriptions de produit, doit être [traduit](../stores-purchase/store-localize.md#localize-products) pour chaque affichage de magasin. |
| Afficher la devise | Une [devise d’affichage](../stores-purchase/currency-configuration.md) différente peut être utilisée pour chaque vue de magasin, bien que les transactions soient traitées au niveau du site web à l’aide de la devise de base. |

{style="table-layout:auto"}
