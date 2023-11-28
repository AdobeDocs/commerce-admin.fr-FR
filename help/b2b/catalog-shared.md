---
title: Présentation du catalogue partagé
description: Découvrez les catalogues partagés fournis par B2B pour Adobe Commerce et comment les utiliser pour gérer des catalogues protégés avec une tarification personnalisée pour différents comptes d’entreprise.
exl-id: cf7c9099-9b7d-407b-adb9-06a4815624ee
feature: B2B, Companies, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 0%

---

# Présentation du catalogue partagé

B2B pour Adobe Commerce vous permet de gérer _shared_ catalogues avec tarifs personnalisés pour différentes entreprises. En plus de la norme, _primary_, catalogue de produits, il permet aux clients d’accéder à deux types de catalogues partagés avec différentes structures de tarification.

Si la variable [Fonctionnalité Catalogue partagé](enable-basic-features.md) est activé dans la configuration, le catalogue principal d’origine reste visible depuis l’administrateur, mais seul le catalogue partagé public par défaut (général) est visible depuis le storefront. En outre, il est possible de créer des catalogues personnalisés qui ne sont visibles que par les membres de certains [société](account-companies.md) comptes.

Pour le `Default (General)` catalogue partagé public, vous devez attribuer des produits pour afficher le catalogue sur le storefront. Par défaut, il est vide et ne contient aucun produit.

>[!NOTE]
>
>**[Version 1.3.0 B2B](release-notes.md#b2b-v130) et plus tard** — Lorsque vous créez un catalogue partagé, chaque [autorisation de catégorie](../catalog/category-permissions.md) pour que le catalogue soit défini sur _[!UICONTROL Allow for the Display Product Prices]_et_[!UICONTROL Add to Cart]_ pour les groupes de clients auxquels cet accès est affecté dans les paramètres d’autorisation du catalogue. Auparavant, ces paramètres étaient automatiquement définis sur `Deny` même lorsque les autorisations de catalogue étaient définies sur `Allow`.

>[!IMPORTANT]
>
>Toutes les [paramètres d’autorisation de groupe](../configuration-reference/catalog/catalog.md#category-permissions) sont ignorées par **_all_** catégories du catalogue lorsque la variable **_[!UICONTROL Shared Catalog]_** est activée. [!UICONTROL Shared Catalog] contrôle entièrement toutes les autorisations de catégorie dans le catalogue lorsqu’il est activé.

La variable _[!UICONTROL Shared Catalogs]_donne accès aux outils utilisés pour gérer vos catalogues partagés. La page est similaire à la norme [Espace de travail d’administration](../getting-started/admin-workspace.md), avec filtres et contrôles d’action. La grille répertorie tous les catalogues partagés, y compris le catalogue partagé public par défaut et tous les catalogues personnalisés que vous avez configurés.

![Catalogues partagés](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

## Accédez au [!UICONTROL Shared Catalogs] page

Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

## Contrôles des actions

La variable [contrôles d’actions](../getting-started/admin-actions-control.md) dans le coin supérieur gauche, vous pouvez utiliser avec le contrôle des actions en masse pour supprimer les catalogues partagés sélectionnés qui ne sont plus nécessaires. Dans la grille, la variable _[!UICONTROL Actions]_contient la sélection complète des outils de gestion des catalogues partagés.

![Actions du catalogue partagées](./assets/shared-catalog-grid-action-column-controls.png){width="350"}

| Contrôle | Description |
|------|-----------|
| [[!UICONTROL Set Pricing and Structure]](catalog-shared-pricing-structure.md) | Détermine la sélection de produits et la tarification personnalisée disponibles dans le catalogue partagé. |
| [[!UICONTROL Assign Companies]](catalog-shared-assign-companies.md) | Détermine quelles entreprises peuvent accéder à un catalogue partagé. |
| [[!UICONTROL General Settings]](catalog-shared-manage.md) | Détermine les informations détaillées du catalogue, notamment le nom, le type de catalogue, la classe fiscale du client et la description. |
| [!UICONTROL Delete] | Supprime les catalogues partagés sélectionnés. |

{style="table-layout:auto"}

## Descriptions des colonnes

| En-tête | Description |
|--- |--- |
| [!UICONTROL Select] | Sélection des enregistrements de catalogue partagés pour l’application d’une action. Le contrôle de l’en-tête peut être utilisé pour sélectionner tous les enregistrements de catalogue partagés de la grille ou les désélectionner. Pour sélectionner un catalogue partagé individuel, cochez la case . |
| [!UICONTROL ID] | Identifiant numérique unique attribué en séquence lors de la création du catalogue. |
| [!UICONTROL Name] | Nom du catalogue partagé. Par défaut, le catalogue partagé par défaut (Général) est disponible. |
| [!UICONTROL Type] | Identifie le type de catalogue partagé comme suit : <br/>**[!UICONTROL Public]**- Le catalogue partagé public par défaut est créé automatiquement lorsque B2B pour Adobe Commerce est installé. Il est initialement affecté à la fonction `General` et `Not Logged In` groupes de clients et est visible par les invités et les clients individuels connectés qui ne sont pas associés à une entreprise. Le système ne prend en charge qu’un seul catalogue partagé public à la fois.<br/>**[!UICONTROL Custom]** - Un catalogue partagé personnalisé contient des tarifs visibles uniquement par les associés connectés des comptes de société affectés. Vous pouvez créer autant de catalogues partagés personnalisés que nécessaire. |
| [!UICONTROL Customer Tax Class] | Classe fiscale affectée au groupe de clients correspondant. Cette colonne n&#39;apparaît pas dans la grille par défaut, mais elle peut être ajoutée en modifiant la mise en page des colonnes. |
| [!UICONTROL Created At] | Date et heure de création du catalogue partagé. |
| [!UICONTROL Created By] | Prénom et nom de l’administrateur de magasin qui a créé le catalogue partagé. |
| [!UICONTROL Action] | Répertorie les actions à appliquer aux catalogues sélectionnés. Options : `Set Pricing and Structure` / `Assign Companies` / `General Settings` / `Delete` |

{style="table-layout:auto"}
