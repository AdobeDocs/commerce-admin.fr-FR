---
title: Commandes
description: Découvrez l’espace de travail Commandes et les fonctionnalités de recherche utilisées pour localiser les commandes dans l’Administration.
exl-id: 6ec8b8c7-97c4-446e-9420-e36e72e90237
feature: Orders, Admin Workspace
source-git-commit: c60f0af09fb1af08deea49216aff340eea59f1b4
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 1%

---

# Commandes

La grille _Commandes_ répertorie toutes les commandes actuelles et suit leur progression et [statut de la commande](order-status.md) tout au long du [workflow](order-processing.md). Pour comprendre facilement le processus de base, une commande devient une [facture](invoices.md) et une facture devient une [expédition](shipments.md). La grille représente la première étape du processus et c&#39;est là que vous pouvez [mettre à jour](order-update.md) les commandes existantes et créer des commandes.

En règle générale, les commandes sont créées lorsque les clients terminent le processus de passage en caisse à partir du storefront. Cependant, si un client a besoin d’aide, vous pouvez également accéder à son [panier](shopping-assisted-cart-manage.md) ou [créer une commande](customer-account-create-order.md) à partir de la grille _Commandes_ ou directement à partir de son compte client.

## Espace de travail Commandes

L&#39;espace de travail Commandes répertorie toutes les commandes actuelles et vous permet de modifier les commandes existantes et de [créer](customer-account-create-order.md) des commandes. Chaque ligne de la grille représente une commande client et chaque colonne représente un attribut ou un champ de données. Utilisez les [contrôles](../getting-started/admin-grid-controls.md) standard pour trier et filtrer la liste, rechercher des commandes et appliquer des [actions](../getting-started/admin-actions-control.md) aux commandes sélectionnées. Utilisez les onglets situés au-dessus des contrôles de pagination pour filtrer la liste, modifier la vue par défaut, modifier et réorganiser les colonnes et exporter les données.

![Grille Commandes](./assets/orders-grid.png){width="700" zoomable="yes"}

### Disposition Grille

La sélection des colonnes et leur ordre dans la grille peuvent être modifiés en fonction de vos préférences. La nouvelle disposition peut être enregistrée en tant que grille _vue_. Par défaut, seules neuf des 20 colonnes disponibles sont incluses dans la grille.

![Colonnes de grille de commande](./assets/order-grid-columns.png){width="600" zoomable="yes"}

#### Modifier la sélection des colonnes

Dans le coin supérieur droit, cliquez sur le contrôle _Colonnes_ ( ![Paramètres des colonnes](../assets/icon-columns.png) ) et procédez comme suit :

- Cochez la case de n’importe quelle colonne à ajouter à la grille.
- Décochez la case de toute colonne que vous souhaitez supprimer de la grille.

#### Réinitialiser la sélection des colonnes

1. Cliquez sur le contrôle _Colonnes_ ( ![Paramètres des colonnes](../assets/icon-columns.png) ).

1. Pour réinitialiser les colonnes de la grille, cliquez sur **[!UICONTROL Reset]**.

   La mise en page de la grille est modifiée pour n’afficher que les [colonnes par défaut](#column-descriptions).

#### Déplacer une colonne

1. Cliquez et maintenez l’en-tête de la colonne enfoncé.

1. Faites glisser la colonne vers sa nouvelle position et relâchez-la.

#### Enregistrer une vue de grille

1. Cliquez sur la commande **[!UICONTROL View]** ( ![Icône Œil](../assets/icon-view-eye.png) ).

1. Cliquez sur **[!UICONTROL Save Current View]**.

1. Saisissez un **[!UICONTROL name]** pour la vue.

1. Pour enregistrer toutes les modifications, cliquez sur la flèche ( ![Icône de flèche](../assets/icon-arrow-save.png) ).

   Le nom de la vue apparaît désormais comme vue actuelle.

#### Modifier la vue

Cliquez sur la commande **[!UICONTROL View]** ( ![Icône Œil](../assets/icon-view-eye.png) ). Effectuez ensuite l’une des opérations suivantes :

- Pour utiliser une autre vue, cliquez sur son nom.

- Pour modifier le nom d’une vue, cliquez sur l’icône _Modifier_ ( ![icône de crayon](../assets/icon-edit-pencil.png) ) et mettez à jour le nom.

### Contrôles Workspace

| Contrôle | Description |
|--- |--- |
| [!UICONTROL Create New Order] | Crée une commande. Voir [Création d&#39;une commande](customer-account-create-order.md) pour plus d&#39;informations. |
| [!UICONTROL Go to Archive] | Affiche la liste des commandes archivées. |
| [!UICONTROL Search] | Lance une recherche de commandes en fonction des filtres actuels. |
| [!UICONTROL Filters] | Définit un ensemble de paramètres de recherche utilisés pour filtrer les enregistrements qui apparaissent dans la grille. |
| [!UICONTROL Default View] | Détermine la disposition de colonne par défaut de la grille. |
| [!UICONTROL Columns] | Détermine la sélection des colonnes et leur ordre dans la grille. La disposition des colonnes peut être modifiée et enregistrée en tant que _vue_. Par défaut, seules certaines des colonnes sont incluses dans la grille. |
| [!UICONTROL Export] | Exporte les enregistrements sélectionnés au format CSV ou XML Excel. |

{style="table-layout:auto"}

### Actions

Pour appliquer une action à des commandes spécifiques, cochez la case située dans la première colonne de chaque commande. Pour sélectionner ou désélectionner toutes les commandes, utilisez le contrôle en haut de la colonne.

![Actions de commande](./assets/orders-action.png){width="600" zoomable="yes"}

| Contrôle | Description |
|--- |--- |
| [!UICONTROL Actions] | Répertorie toutes les actions pouvant être appliquées aux commandes sélectionnées. Pour appliquer une action à une commande ou à un groupe de commandes, cochez la case située dans la première colonne de chaque commande. <br/>Actions de commande : `Cancel` / `Hold` / `Unhold` / `Print Invoices` / `Print Packing Slips` / `Print Credit Memos` / `Print All` / `Print Shipping Labels` / `Move to Archive` ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) |
| [!UICONTROL Mass Actions] | Peut être utilisé pour sélectionner plusieurs enregistrements comme cible de l’action. Cochez la case située dans la première colonne de chaque enregistrement soumis à l&#39;action. Options : `Select All` / `Unselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL Submit] | Applique l&#39;action en cours aux enregistrements de commande sélectionnés. |
| [!UICONTROL Edit] | Ouvre la commande en mode d&#39;édition. |

{style="table-layout:auto"}

### Descriptions des colonnes

| Colonne | Description |
|--- |--- |
| [!UICONTROL Select] | Cochez les cases des guillemets qui feront l&#39;objet d&#39;une action ou utilisez la commande de sélection dans l&#39;en-tête de colonne. Options : Tout sélectionner / Tout désélectionner |
| [!UICONTROL ID] | Numéro séquentiel unique attribué lors du premier enregistrement d’une nouvelle commande. |
| [!UICONTROL Purchase Point] | Identifie la vue du magasin dans laquelle la commande a été passée. |
| [!UICONTROL Purchase Date] | Date et heure auxquelles la commande a été passée. Il est toujours affiché selon le fuseau horaire par défaut. |
| [!UICONTROL Bill-to Name] | Nom de la personne responsable du paiement de la commande. |
| [!UICONTROL Ship-to Name] | Nom de la personne à qui la commande doit être expédiée. |
| [!UICONTROL Grand Total (Base)] | Total général de la commande. |
| [!UICONTROL Grand Total (Purchased)] | Total général des produits achetés dans la commande. |
| [!UICONTROL Status] | Statut actuel de la commande. |
| [!UICONTROL Action] | _[!UICONTROL View]_ouvre la commande en mode d’édition. |
| [!UICONTROL Allocated sources] | Les sources allouées à cet ordre spécifique. |

{style="table-layout:auto"}

Colonnes supplémentaires disponibles :

| Colonne | Description |
|--- |--- |
| [!UICONTROL Billing Address] | Adresse de facturation du client qui a passé la commande. |
| [!UICONTROL Shipping Address] | Adresse à laquelle la commande doit être expédiée. |
| [!UICONTROL Shipping Information] | Méthode à utiliser pour expédier la commande. |
| [!UICONTROL Customer Email] | Adresse e-mail de la personne qui a passé la commande. |
| [!UICONTROL Customer Group] | Groupe de clients auquel est affectée la personne qui a passé la commande. |
| [!UICONTROL Subtotal] | Sous-total de la commande, sans expédition ni manutention, ni taxe. |
| [!UICONTROL Shipping and Handling] | Montant facturé pour l&#39;expédition et la manutention. |
| [!UICONTROL Customer Name] | Prénom et nom du client qui a passé la commande. |
| [!UICONTROL Payment Method] | Mode de paiement à utiliser pour la commande. |
| [!UICONTROL Total Refunded] | Tout montant de la commande qui doit être remboursé au client. |
| [!UICONTROL Refunded to Store Credit] | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Tout montant de la commande qui doit être remboursé au crédit de la boutique du client. |
| [!UICONTROL Company Name] | ![Adobe Commerce B2B](../assets/b2b.svg) (disponible avec Adobe Commerce B2B) Nom de la [société](../b2b/account-companies.md) qui a passé la commande. |

{style="table-layout:auto"}

## Recherche de commande

La zone de recherche située dans le coin supérieur gauche de la grille Commandes permet de rechercher des commandes spécifiques par mot-clé ou en filtrant les enregistrements de commandes dans la grille.

![Résultats de la recherche](./assets/order-search.png){width="600" zoomable="yes"}

### Rechercher une correspondance

1. Saisissez un terme de recherche dans la zone de recherche de la page.

1. Pour afficher les résultats, cliquez sur _Rechercher_ ( ![Icône Loupe](../assets/icon-magnify-search.png) ).

### Filtrer la recherche

1. Pour afficher la sélection des filtres de recherche, cliquez sur l’onglet _Filtres_ ( ![icône Funnel](../assets/icon-filter-search.png) ).

   ![Filtres de commande](./assets/order-search-filter.png){width="600" zoomable="yes"}

1. Renseignez autant de filtres que vous le souhaitez pour décrire les commandes que vous souhaitez rechercher.

1. Cliquez sur **[!UICONTROL Apply Filters]** pour afficher les résultats.

### Filtres de recherche

| Filtre | Description |
|--- |--- |
| [!UICONTROL Purchase Date] | Filtre la recherche en fonction de la date d’achat. Pour rechercher des commandes dans une plage de dates, saisissez les dates **[!UICONTROL from]** et **[!UICONTROL to]**. |
| [!UICONTROL ID] | Filtre la recherche en fonction de l’identifiant de commande. |
| [!UICONTROL Grand Total (Base)] | Filtre la recherche en fonction du total général de chaque commande, qui inclut tous les crédits appliqués à la commande. |
| [!UICONTROL Grand Total (Purchased)] | Filtre la recherche en fonction du total général des articles achetés dans chaque commande. |
| [!UICONTROL Bill-to Name] | Filtre la recherche en fonction du nom de la personne responsable du paiement de la commande. |
| [!UICONTROL Ship-to Name] | Filtre la recherche en fonction du nom de la personne à laquelle chaque commande est envoyée . |
| [!UICONTROL Purchase Point] | Filtre la recherche par site web, magasin ou vue de magasin où la commande a été passée. |
| [!UICONTROL Status] | Filtre la recherche en fonction du statut de la commande. Options : `Canceled` / `Closed` / `Complete` / `Suspected Fraud` / `On Hold` / `Payment Review` / `PayPal Canceled Reversal` /` PayPal Reversed` /` Pending` / `Pending Payment` / `Pending PayPal` / `Processing` |
| [!UICONTROL Braintree Transaction Source] | Filtre la recherche selon la source de la transaction. |

{style="table-layout:auto"}

### Outils de recherche

| Outil | Description |
|--- |--- |
| [!UICONTROL Apply Filters] | Applique tous les filtres aux résultats de la recherche. |
| [!UICONTROL Cancel] | Annule la recherche en cours. |
| [!UICONTROL Clear All] | Efface tous les filtres de recherche. |

{style="table-layout:auto"}

