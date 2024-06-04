---
title: Gestion des catalogues partagés
description: Découvrez les informations et les outils disponibles sur la page Catalogues partagés.
exl-id: a01ac292-240d-42e7-b4c9-2982f293c521
feature: B2B, Companies, Catalog Management
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '967'
ht-degree: 0%

---

# Gestion des catalogues partagés

La variable _[!UICONTROL Shared Catalogs]_donne accès aux outils nécessaires à la gestion de vos catalogues partagés. La page est similaire à l’espace de travail Admin standard, avec des filtres et des contrôles d’action. La grille répertorie tous les catalogues partagés, y compris le catalogue partagé public par défaut et tous les catalogues personnalisés que vous avez configurés.

## Mettre à jour la sélection de produits

La sélection de produits dans n’importe quel catalogue partagé peut être facilement mise à jour à partir du _[!UICONTROL Action]_de la grille des catalogues partagés. Les modifications que vous apportez sont visibles par les membres de tout compte d’entreprise associé. Le processus est essentiellement le même que le choix de produits pour un nouveau [structure du catalogue](catalog-shared-pricing-structure.md), sauf que la portée de la configuration ne peut pas être modifiée.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Pour le catalogue partagé dans la grille, accédez à la **[!UICONTROL Action]** et sélectionnez **[!UICONTROL Set Pricing and Structure]**.

   ![Grille de catalogue partagée et menu d’action](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. Suivez les instructions de la section [Étape 2 : Sélection des produits](catalog-shared-pricing-structure.md#step-2-choose-the-products).

   Vous pouvez ignorer le premier élément, car la portée d’un catalogue partagé ne peut pas être modifiée après son enregistrement initial.

Si vous travaillez avec un produit spécifique, la variable _[!UICONTROL Products In Shared Catalog]_répertorie chaque catalogue partagé où le produit est disponible. Pour en savoir plus, voir [Ajout de produits à un catalogue partagé](catalog-shared-product-add.md).

![Produit dans les catalogues partagés](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

## Mise à jour de la tarification personnalisée

La tarification personnalisée des produits d’un catalogue partagé peut être facilement mise à jour à partir de la colonne Action de la grille Catalogues partagés. Les modifications que vous apportez sont visibles dans le storefront aux membres de la société ou du groupe de clients associé. Le processus est essentiellement le même que la définition d’une tarification personnalisée pour un nouveau [catalogue partagé](catalog-shared-pricing-structure.md), sauf que la portée de la configuration ne peut pas être modifiée.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Pour le catalogue partagé dans la grille que vous souhaitez mettre à jour, accédez au **[!UICONTROL Action]** et sélectionnez **[!UICONTROL Set Pricing and Structure]**.

1. Sur le _[!UICONTROL Catalog Structure]_page, cliquez sur **[!UICONTROL Configure]**et effectuez l’une des opérations suivantes :

   - Dans l’indicateur de progression situé en haut de la page, cliquez sur **[!UICONTROL Pricing]**.
   - Dans le coin supérieur droit, cliquez sur **[!UICONTROL Next]**.

1. Suivez les instructions de la section [Étape 3 : définition de prix personnalisés](catalog-shared-pricing-structure.md#step-3-set-custom-prices).

## Mise à jour des autorisations de catégorie

[Autorisations de catégorie](../catalog/category-permissions.md) sont automatiquement définis sur `Allow` pour les produits ajoutés de l’arborescence des catégories à un catalogue partagé. Vous pouvez ensuite ajuster les autorisations ou créer des règles supplémentaires, si nécessaire.

>[!NOTE]
>
>**[Version 1.3.0 B2B](release-notes.md#b2b-v130) et plus tard** — Lorsque vous créez un catalogue partagé, chaque [autorisation de catégorie](../catalog/category-permissions.md) pour que le catalogue soit défini sur `Allow` pour le _[!UICONTROL Display Product Prices]_et_[!UICONTROL Add to Cart]_ pour les groupes de clients auxquels cet accès est affecté dans les paramètres d’autorisation du catalogue. Auparavant, ces paramètres étaient automatiquement définis sur `Deny` même lorsque les autorisations de catalogue étaient définies sur `Allow`.

>[!IMPORTANT]
>
>Toutes les [paramètres d’autorisation de groupe](../configuration-reference/catalog/catalog.md#category-permissions) sont ignorées par **_all_** catégories du catalogue lorsque la variable **_[!UICONTROL Shared Catalog]_** est activée. [!UICONTROL Shared Catalog] contrôle entièrement toutes les autorisations de catégorie dans le catalogue lorsqu’il est activé.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Dans l&#39;arborescence des catégories, sélectionnez la catégorie des produits que vous souhaitez mettre à jour.

   Pour inclure tous les produits, sélectionnez la catégorie de niveau supérieur dans l’arborescence.

1. Faire défiler vers le bas et développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Category Permissions]** .

1. Cliquez sur **[!UICONTROL New Permission]** et procédez comme suit :

   ![Nouvelle autorisation](./assets/category-permissions-new.png){width="600" zoomable="yes"}

   - Choisissez la **[!UICONTROL Customer Group]** qui correspond au catalogue partagé et modifiez les paramètres d’autorisation si nécessaire.

     ![Règle d’autorisations de catégorie](./assets/shared-catalog-category-permissions.png){width="600" zoomable="yes"}

   - Pour créer une règle d’autorisation pour un autre groupe de clients, cliquez sur **[!UICONTROL New Permissions]** et répétez le processus.

   - Pour supprimer une règle d’autorisation, cliquez sur le bouton _Supprimer_ ![Corbeille](../assets/icon-delete-trashcan-solid.png) Icône

1. Une fois terminé, cliquez sur **[!UICONTROL Save]**.

## Mise à jour des détails du catalogue

Les informations détaillées de tout catalogue partagé peuvent être facilement mises à jour à partir de la colonne Action de la grille Catalogues partagés. Les modifications que vous apportez sont répercutées dans les comptes d’entreprise associés.

![Paramètres généraux](./assets/shared-catalog-grid-general-settings.png){width="700" zoomable="yes"}

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Pour le catalogue partagé que vous souhaitez mettre à jour, accédez au **[!UICONTROL Action]** et sélectionnez **[!UICONTROL General Settings]**.

   ![Détails du catalogue](./assets/shared-catalog-update-details.png){width="600" zoomable="yes"}

1. Mettez à jour les informations détaillées du catalogue si nécessaire.

   - La modification du nom d’un catalogue partagé modifie également le nom du groupe de clients correspondant.
   - Modification du type de catalogue depuis `Custom` to `Public` convertit le catalogue public existant en catalogue personnalisé. Toutes les entreprises associées au catalogue public d’origine sont réaffectées au remplacement. Un catalogue public ne peut pas être converti en catalogue personnalisé.

1. Une fois terminé, cliquez sur **[!UICONTROL Save]**.

## Référence de page de catalogue partagée

### Barre de boutons

| Bouton | Description |
|--- |--- |
| [!UICONTROL Back] | Renvoie à la page Catalogues partagés sans enregistrer le nouveau catalogue partagé. |
| [!UICONTROL Delete] | Supprime le catalogue et réaffecte toutes les entreprises associées et leurs membres au catalogue partagé public. |
| [!UICONTROL Reset] | Efface le formulaire des modifications non enregistrées et restaure les informations détaillées du catalogue d’origine. |
| [!UICONTROL Duplicate] | Crée une [copie en double du catalogue](catalog-shared-create.md). Pour un catalogue personnalisé, le modèle de prix et la structure de l’original, mais sans les associations de l’entreprise. Si un catalogue partagé public est dupliqué, le type du catalogue dupliqué devient `custom`. Un groupe de clients correspondant est également créé avec le même nom que le catalogue en double. Par défaut, un catalogue en double est nommé _Dupliquer de_ le catalogue d’origine. |
| [!UICONTROL Save and Continue Edit] | Enregistre toutes les modifications et conserve le formulaire ouvert en mode d’édition. |
| [!UICONTROL Save] | Enregistre les modifications, ferme le formulaire et revient à la page Catalogues partagés . |

{style="table-layout:auto"}

### Détails du catalogue

| Champ | Description |
|--- |--- |
| [!UICONTROL Name] | Identifie le catalogue partagé dans l’ensemble de l’administrateur et dans les comptes clients où il est disponible. Le nom du catalogue doit être descriptif et ne pas dépasser 32 caractères. Vous ne pouvez pas avoir deux catalogues partagés portant le même nom. Nombre maximum de caractères : 32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]** - Identifie un catalogue dont la tarification personnalisée est disponible uniquement pour les entreprises spécifiques auxquelles il est affecté.<br/>**[!UICONTROL Public]**- Identifie le catalogue partagé disponible pour tous les visiteurs invités et les clients connectés qui ne sont pas associés à une entreprise. Un catalogue partagé public &quot;par défaut&quot; est créé lorsque Adobe Commerce B2B est installé, mais doit être configuré par l’administrateur. Un seul catalogue partagé public peut exister à la fois. |
| [!UICONTROL Customer Tax Class] | Détermine la classe de taxe utilisée pour les achats effectués à partir du catalogue. Les options incluent toutes les classes d’impôts disponibles. |
| [!UICONTROL Description] | Une brève explication de l’utilisation du catalogue. |

{style="table-layout:auto"}
