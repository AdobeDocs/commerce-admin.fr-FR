---
title: Gestion des catalogues partagés
description: Découvrez les informations et les outils disponibles sur la page Catalogues partagés.
exl-id: a01ac292-240d-42e7-b4c9-2982f293c521
feature: B2B, Companies, Catalog Management
TQID: https://experienceleague.adobe.com/q2dtQ-y3ByGhtMNp68-3lN-PqZJ-1mRX4BMCu0lfB54
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
last-update: 2026-10-01
source-git-commit: 82862dcdd7667b46cfe7bd08863926ae5bafd24b
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 0%
---
# Gestion des catalogues partagés

La page _[!UICONTROL Shared Catalogs]_donne accès aux outils nécessaires à la gestion de vos catalogues partagés, notamment la sélection de produits, la tarification personnalisée, les autorisations de catégorie et les détails de catalogue. La page est similaire à l’espace de travail d’administration standard, avec des filtres et des commandes d’action. La grille répertorie tous les catalogues partagés, y compris le catalogue public partagé par défaut et tous les catalogues personnalisés que vous avez configurés.

Si l’extension [!DNL Adobe Commerce Optimizer Connector for B2B] est installée, la page permet également d’accéder aux vues de catalogue [!DNL Adobe Commerce Optimizer] créées lorsque le connecteur synchronise les données de chaque catalogue partagé avec [!DNL Adobe Commerce Optimizer], ainsi qu’aux clés d’accès restreintes qui sécurisent les vues de catalogue pour les expériences de storefront B2B.

## Mettre à jour la sélection de produits

La sélection de produits dans un catalogue partagé peut être facilement mise à jour à partir de la colonne _[!UICONTROL Action]_de la grille de catalogues partagés. Les modifications que vous apportez sont visibles pour les membres de tous les comptes de société associés. Le processus est identique à la sélection de produits pour une nouvelle [structure de catalogue](catalog-shared-pricing-structure.md), sauf que la portée de la configuration ne peut pas être modifiée.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Pour le catalogue partagé dans la grille, accédez à la colonne **[!UICONTROL Action]** et sélectionnez **[!UICONTROL Set Pricing and Structure]**.

   ![Grille de catalogue partagé et menu Action](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. Suivez les instructions de l’[étape 2 : sélection des produits](catalog-shared-pricing-structure.md#step-2-choose-the-products).

   Vous pouvez ignorer le premier élément, car l’étendue d’un catalogue partagé ne peut pas être modifiée après son premier enregistrement.

Si vous utilisez un produit spécifique, la section _[!UICONTROL Products In Shared Catalog]_répertorie chaque catalogue partagé dans lequel le produit est disponible. Pour en savoir plus, voir [Ajouter des produits à un catalogue partagé](catalog-shared-product-add.md).

![Produit dans les catalogues partagés](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

## Mettre à jour la tarification personnalisée

La tarification personnalisée des produits dans un catalogue partagé peut être facilement mise à jour à partir de la colonne Action de la grille Catalogues partagés. Les modifications que vous apportez sont visibles dans le storefront pour les membres de la société ou du groupe de clients associé. Le processus est identique à la définition du prix personnalisé pour un nouveau [catalogue partagé](catalog-shared-pricing-structure.md), sauf que la portée de la configuration ne peut pas être modifiée.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Pour le catalogue partagé de la grille que vous souhaitez mettre à jour, accédez à la colonne **[!UICONTROL Action]** et sélectionnez **[!UICONTROL Set Pricing and Structure]**.

1. Sur la page _[!UICONTROL Catalog Structure]_, cliquez sur **[!UICONTROL Configure]**et effectuez l’une des opérations suivantes :

   - Dans l’indicateur de progression en haut de la page, cliquez sur **[!UICONTROL Pricing]**.
   - Dans le coin supérieur droit, cliquez sur **[!UICONTROL Next]**.

1. Suivez les instructions de l’[étape 3 : définir des prix personnalisés](catalog-shared-pricing-structure.md#step-3-set-custom-prices).

## Mettre à jour les autorisations de catégorie

Les [autorisations de catégorie](../catalog/category-permissions.md) sont automatiquement définies sur `Allow` pour les produits ajoutés à partir de l’arborescence des catégories à un catalogue partagé. Vous pouvez ensuite ajuster les autorisations ou créer des règles supplémentaires, si nécessaire.

>[!NOTE]
>
>**[Version 1.3.0 de B2B](release-notes.md#b2b-v130) et versions ultérieures** — Lorsque vous créez un catalogue partagé, chaque autorisation [de catégorie](../catalog/category-permissions.md) est définie sur `Allow` pour les _[!UICONTROL Display Product Prices]_et_[!UICONTROL Add to Cart]_ pour les groupes de clients attribués. Auparavant, ces paramètres étaient automatiquement définis sur `Deny` même lorsque les autorisations de catalogue étaient définies sur `Allow`.

>[!IMPORTANT]
>
>**_[!UICONTROL Shared Catalog]_** remplace toutes les catégories [paramètres d’autorisation de groupe](../configuration-reference/catalog/catalog.md#category-permissions) existantes pour **_toutes_** du catalogue lorsqu’elles sont activées. [!UICONTROL Shared Catalog] contrôle entièrement toutes les autorisations de catégorie du catalogue lorsqu’il est activé.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Dans l’arborescence des catégories, sélectionnez la catégorie des produits à mettre à jour.

   Pour inclure tous les produits, sélectionnez la catégorie de niveau supérieur dans l’arborescence.

1. Faites défiler vers le bas et développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Category Permissions]** .

1. Cliquez sur **[!UICONTROL New Permission]** et procédez comme suit :

   ![Nouvelle autorisation](./assets/category-permissions-new.png){width="600" zoomable="yes"}

   - Sélectionnez le **[!UICONTROL Customer Group]** correspondant au catalogue partagé et modifiez les paramètres d’autorisation si nécessaire.

     ![Règle des autorisations de catégorie](./assets/shared-catalog-category-permissions.png){width="600" zoomable="yes"}

   - Pour créer une règle d’autorisations pour un autre groupe de clients, cliquez sur **[!UICONTROL New Permissions]** et répétez le processus.

   - Pour supprimer une règle d’autorisation, cliquez sur l’icône _Supprimer_ ![Corbeille](../assets/icon-delete-trashcan-solid.png).

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

## Mettre à jour les détails du catalogue

Les informations détaillées de tout catalogue partagé peuvent être facilement mises à jour à partir de la colonne Action de la grille Catalogues partagés. Les modifications que vous apportez sont répercutées dans les comptes de société associés.

![Paramètres généraux](./assets/shared-catalog-grid-general-settings.png){width="700" zoomable="yes"}

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Pour le catalogue partagé que vous souhaitez mettre à jour, accédez à la colonne **[!UICONTROL Action]** et sélectionnez **[!UICONTROL General Settings]**.

   ![Détails du catalogue](./assets/shared-catalog-update-details.png){width="600" zoomable="yes"}

1. Mettez à jour les informations détaillées du catalogue si nécessaire.

   - La modification du nom d’un catalogue partagé modifie également le nom du groupe de clients correspondant.
   - Si vous remplacez le type de catalogue `Custom` par `Public`, le catalogue public existant est converti en catalogue personnalisé. Toutes les sociétés associées au catalogue public d’origine sont réaffectées au remplacement. Un catalogue public ne peut pas être converti en catalogue personnalisé.
   - Pour identifier la classification fiscale appliquée aux achats effectués via le catalogue partagé, sélectionnez l’[!UICONTROL Customer Tax Class].

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

## Gestion de la configuration de la vue de catalogue

Une fois l’extension [!DNL Adobe Commerce Optimizer Connector for B2B] installée, la section _[!UICONTROL Catalog Views]_d’un catalogue partagé répertorie les vues de catalogue [!DNL Adobe Commerce Optimizer] projetées à partir du catalogue partagé et vous permet de gérer les clés d’accès restreint qui les sécurisent.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Pour le catalogue partagé que vous souhaitez consulter, accédez à la colonne **[!UICONTROL Action]** et sélectionnez **[!UICONTROL General Settings]**.

1. Dans le panneau _[!UICONTROL Shared Catalog Information]_, sélectionnez **[!UICONTROL Catalog Views]**.

Pour en savoir plus sur les vues de catalogue et la modification des clés d’accès restreintes, voir [Gérer la configuration des vues de catalogue](catalog-views-manage.md).

## Référence de page de catalogue partagé

### Barre de boutons

| Bouton | Description |
| --- | --- |
| [!UICONTROL Back] | Retourne à la page Catalogues partagés sans enregistrer le nouveau catalogue partagé. |
| [!UICONTROL Delete] | Supprime le catalogue et réaffecte toutes les sociétés associées et leurs membres au catalogue public partagé. |
| [!UICONTROL Reset] | Efface le formulaire des modifications non enregistrées et restaure les informations détaillées d’origine du catalogue. |
| [!UICONTROL Duplicate] | Crée une [copie en double du catalogue](catalog-shared-create.md). Pour un catalogue personnalisé, modèle et structure de tarification de l’original, mais sans les associations d’entreprises. Si un catalogue public partagé est dupliqué, le type du catalogue dupliqué devient `custom`. Un groupe de clients correspondant est également créé et porte le même nom que le catalogue en double. Par défaut, un catalogue en double est nommé _Dupliquer de_ catalogue d’origine. |
| [!UICONTROL Save and Continue Edit] | Enregistre toutes les modifications et maintient le formulaire ouvert en mode d’édition. |
| [!UICONTROL Save] | Enregistre les modifications, ferme le formulaire et revient à la page Catalogues partagés. |

{style="table-layout:auto"}

### Détails du catalogue

| Champ | Description |
| --- | --- |
| [!UICONTROL Name] | Identifie le catalogue partagé dans l’ensemble de l’administration et dans les comptes clients où il est disponible. Le nom du catalogue doit être explicite et ne pas dépasser 32 caractères. Vous ne pouvez pas avoir deux catalogues partagés avec le même nom. Nombre maximal de caractères : 32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]** - Identifie un catalogue avec tarification personnalisée qui n&#39;est disponible que pour les sociétés spécifiques auxquelles il est affecté.<br/>**[!UICONTROL Public]**- Identifie le catalogue partagé qui est disponible pour tous les visiteurs invités et pour les clients connectés qui ne sont pas associés à une entreprise. Un catalogue public partagé « par défaut » est créé lors de l’installation d’Adobe Commerce B2B, mais doit être configuré par l’administrateur. Un seul catalogue public partagé peut exister à la fois. |
| [!UICONTROL Customer Tax Class] | Détermine la classe de taxe utilisée pour les achats effectués à partir du catalogue. Les options incluent toutes les classes de taxe disponibles. La classe de taxe est associée au groupe de clients créé ou utilisé pour le catalogue partagé. Voir [Classes d’impôts](../stores-purchase/tax-class.md). |
| [!UICONTROL Description] | Brève explication de l’utilisation du catalogue. |

{style="table-layout:auto"}

### Vues du catalogue

{{$include /help/_includes/catalog-views-reference-table.md}}
