---
title: Présentation de la gestion des catalogues
description: Découvrez le fonctionnement du catalogue et de la portée du produit dans la gestion des catalogues.
exl-id: 3c58fc1c-d7a3-4f51-8a78-6bf2fd0dbeee
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---

# Présentation de la gestion des catalogues

Adobe Commerce et Magento Open Source utilisent le terme _catalogue_ pour faire référence à la base de données de produits dans son ensemble.

L’un des domaines les plus importants dans la création et la gestion de votre boutique est la création de produits et de catégories. L’administrateur fournit plusieurs outils que vous utilisez pour la configuration initiale de votre magasin, ainsi que pour la maintenance de votre magasin et l’optimisation de votre entreprise.

>[!TIP]
>
>Inventory management pour Adobe Commerce et Magento Open Source vous donne les outils nécessaires pour gérer votre inventaire de produits. Les commerçants disposant d’un seul magasin pour plusieurs entrepôts, magasins, lieux de ramassage, expéditeurs, etc. peuvent utiliser ces fonctionnalités pour conserver les quantités à vendre et traiter les envois afin de terminer les commandes. Pour plus d’informations sur ces fonctionnalités et sur la manière dont vous pouvez les utiliser pour gérer des stocks à plusieurs emplacements, voir [Guide de l’utilisateur d’Inventory management](../inventory-management/introduction.md).

## Portée du catalogue

L’accès aux données du catalogue est déterminé par plusieurs facteurs, dont la variable [scope](../getting-started/websites-stores-views.md#scope-settings) , la configuration du catalogue et la variable [catégorie racine](category-root.md) qui est affecté au magasin. Le catalogue comprend les produits activés et disponibles à la vente, ainsi que les produits qui ne sont actuellement pas proposés à la vente.

En vente, le terme _catalogue_ fait généralement référence à une sélection organisée de produits disponibles à la vente. Par exemple, un magasin peut avoir un &quot;catalogue de printemps&quot; et un &quot;catalogue d’automne&quot;.

Comme la table des matières d’un catalogue imprimé, le menu principal de votre boutique — ou _navigation supérieure_ — classe les produits par catégorie pour faciliter la recherche de ce qu’ils veulent par les clients. Le menu principal repose sur un _catégorie racine_, qui est un conteneur pour le menu affecté au magasin. Comme les options de menu spécifiques sont définies au niveau de l’affichage en magasin, chaque vue peut avoir un menu principal différent basé sur la même catégorie racine. Dans chaque menu, vous pouvez proposer une sélection de produits adaptés au magasin.

![Diagramme hiérarchique du catalogue](./assets/catalog-hierarchy-scope.svg){width="550"}

## Portée du produit

Pour les installations comportant plusieurs sites web, magasins et vues, la variable [scope](../getting-started/websites-stores-views.md#scope-settings) détermine où les produits sont disponibles pour la vente et les informations sur les produits disponibles pour chaque consultation de magasin. Au départ, tous les produits que vous créez sont publiés sur le site web, le magasin et la vue de magasin par défaut.

![diagramme de magasin multi-site](./assets/scope-multisite.svg){width="550"}

Si vous n’avez qu’un seul magasin avec la vue par défaut, vous pouvez exécuter votre magasin dans [mode magasin unique](../getting-started/websites-stores-views.md#single-store-mode) pour masquer les paramètres de portée. Cependant, si votre boutique comporte plusieurs vues, un indicateur de portée s’affiche sous le nom de chaque champ.

- Pour modifier les informations sur un produit pour une vue spécifique, utilisez le _Affichage en magasin_ dans le coin supérieur gauche pour choisir la vue. Des contrôles supplémentaires sont disponibles pour tout champ pouvant être modifié au niveau de l’affichage du magasin.

- Pour définir la portée d’un produit dans une installation multi-site, voir la section [Produit sur les sites web](settings-basic-websites.md) de la section des informations sur les produits.

La modification d’un produit pour une vue de magasin est semblable à l’ajout d’une couche d’informations sur le produit spécifique à la vue.

Vous pouvez uniquement modifier ou attribuer des produits pour le site pour lequel vous disposez des autorisations, et non pour tous les sites où le produit est affecté.

Bien que la variable _Espagnol_ la vue de magasin est sélectionnée dans l’exemple suivant. les informations sur les produits apparaissent toujours dans la langue d’origine de la vue de magasin par défaut. Pour traduire les informations sur le produit, vous devez passer à la section _Espagnol_ afficher le magasin et traduire les champs de texte, tels que le titre du produit, la description et les métadonnées ; Pour plus d’informations, voir [Localisation des produits](../stores-purchase/store-localize.md#localize-products).

## Modification d’un produit pour une autre vue

>[!NOTE]
>
>La variable _Toutes les vues de magasin_ est désactivée pour les utilisateurs administrateurs qui sont limités à une portée spécifique lorsque le produit est également publié en dehors de la portée autorisée. La première plage disponible pour modification est sélectionnée par défaut, car les utilisateurs à accès limité ne peuvent pas effectuer de _global_ actions ou actions qui affectent les portées auxquelles ils n’ont pas accès.

1. Dans le coin supérieur gauche, définissez **[!UICONTROL Store View]** à la vue spécifique à modifier.

1. Pour confirmer le changement de portée, cliquez sur **[!UICONTROL OK]**.

1. Mettez à jour le champ avec la nouvelle valeur pour la vue de magasin.

   Une case à cocher s’affiche sous n’importe quel champ pouvant être modifié pour la vue de magasin. Pour remplacer la valeur par défaut, désélectionnez l’option **Utiliser la valeur par défaut** .

   ![Traduction du nom du produit pour la vue de magasin en espagnol](./assets/product-translate-field-french.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

1. Dans le coin supérieur gauche, définissez la variable **[!UICONTROL Store View]** sélectionnez à nouveau la valeur par défaut.

1. Pour vérifier la modification dans votre magasin, procédez comme suit :

   - Dans le coin supérieur droit, cliquez sur le bouton _Administration_ Flèche de menu et choisissez **[!UICONTROL Customer View]**.

     ![Vue client](./assets/product-admin-menu-customer-view.png){width="600" zoomable="yes"}

   - Dans le coin supérieur droit du magasin, définissez la variable **[!UICONTROL Language Chooser]** dans la vue store du produit que vous avez modifié et recherchez le produit que vous avez modifié pour l’affichage.

     ![Sélecteur de langue](./assets/storefront-language-chooser.png){width="700" zoomable="yes"}
