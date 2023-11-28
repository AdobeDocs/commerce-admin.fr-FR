---
title: '[!UICONTROL My Requisition Lists]'
description: Découvrez l’expérience client pour les listes de demandes d’achat, disponible dans le tableau de bord de leur compte.
exl-id: ed1b41aa-9c36-49f8-80f2-ad0eb151b7a5
feature: B2B, Companies
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# [!UICONTROL My Requisition Lists]

La principale raison pour laquelle vous conservez une liste de demandes d’achat est de faciliter la réorganisation des produits. Les clients autorisés peuvent facilement réorganiser les éléments d’une liste de demandes d’acquisition en les ajoutant au panier, puis les déplacer ou les copier d’une liste à une autre.

![Mes listes de demandes](./assets/account-dashboard-my-requisition-lists.png){width="700" zoomable="yes"}

## Ouvrir une liste de demandes

1. Dans le tableau de bord de leur compte, le client choisit **[!UICONTROL My Requisition Lists]**.

1. Localise la liste des demandes qu’ils souhaitent ouvrir et clique sur **[!UICONTROL View]** et effectuez l’une des opérations suivantes :

### Ajout de produits au panier

1. Le client effectue l’une des opérations suivantes pour sélectionner les produits à ajouter :

   - Coche la case de chaque élément.
   - Clics **[!UICONTROL Select All]**.

1. entre dans la variable **[!UICONTROL Qty]** à ajouter au panier.

1. Pour modifier les options d’un produit, procédez comme suit :

   - Dans l’élément de ligne, cliquez sur le bouton _Modifier_ (![Icône Crayon](../assets/icon-edit-pencil.png)).
   - Modifie toutes les options nécessaires.
   - Clics **[!UICONTROL Update Requisition List]**.

1. Clics **[!UICONTROL Add to Cart]**.

   ![Détails de la liste de demandes](./assets/requisition-list-view.png){width="700" zoomable="yes"}

### Copier des éléments dans une autre liste

1. Le client sélectionne la case à cocher de chaque élément à déplacer.

1. Clics **[!UICONTROL Copy Selected]** et effectue l’une des opérations suivantes :

   - Choisit une liste de commandes existante.
   - Clics **[!UICONTROL Create New Requisition List]**.

### Exporter une liste

1. Le client ouvre la liste des demandes à exporter.

1. Cliquez sur le bouton **[!UICONTROL Export]** lien.

Adobe Commerce génère et télécharge une liste CSV avec `sku` et `qty` valeurs.

### Déplacer des éléments vers une autre liste

1. Le client sélectionne la case à cocher de chaque élément à déplacer.

1. Clics **[!UICONTROL Move Selected]** et effectuez l’une des opérations suivantes :

   - Choisit une liste de commandes existante.
   - Clics **[!UICONTROL Create New Requisition List]**.

### Imprimer une liste

1. Dans le coin supérieur droit de la liste, le client clique sur **[!UICONTROL Print]**.

1. Vérifie le périphérique de sortie et clique **[!UICONTROL Print]**.

   ![Liste des demandes d’impression](./assets/requisition-list-print.png){width="500" zoomable="yes"}

### Modification des options de produit

Pour modifier les options de produit dans la liste, le client effectue les opérations suivantes :

1. Cliquez sur le bouton _Crayon_ (![Icône Crayon](../assets/icon-edit-pencil.png)) pour ouvrir la page du produit.

1. Modifie toutes les options nécessaires.

1. Clics **[!UICONTROL Update Requisition List]**.

   ![Mettre à jour la liste des demandes](./assets/requisition-list-update.png){width="700" zoomable="yes"}

Un produit de la liste des demandes peut être modifié dans les cas suivants :

- Le produit a **[!UICONTROL all options set]** (lorsqu’il s’agit d’une [produit configuré](../catalog/product-create-configurable.md) dans la liste des demandes).

  Le produit est **[!UICONTROL added to this Requisition List]**.

- Le produit est [un produit simple avec des options](../catalog/settings-advanced-custom-options.md)

- La modification est autorisée pour le type de produit.

### Supprimer des éléments

1. Le client sélectionne la case à cocher de chaque élément à supprimer.

1. Clics **[!UICONTROL Remove Selected]**.

1. Lorsque vous êtes invité à confirmer l’opération, cliquez sur **[!UICONTROL Delete]**.

### Renommer une liste

1. Après le titre de la liste, le client clique sur **[!UICONTROL Rename]**.

1. Entre dans une **[!UICONTROL Requisition List Name]**.

1. Clics **[!UICONTROL Save]**.

   ![Renommer la liste des demandes](./assets/requisition-list-rename.png){width="300"}


### Supprimer une liste de demandes

1. Le client ouvre la liste des demandes à supprimer.

1. Clics **[!UICONTROL Delete Requisition List]**.

1. Lorsque vous êtes invité à confirmer l’opération, cliquez sur **[!UICONTROL Delete]**.

>[!NOTE]
>
>Cette action ne peut pas être annulée.

## Actions

| Action | Description |
|--- |--- |
| [!UICONTROL Rename] | Permet de renommer la liste des demandes et de mettre à jour la description. |
| [!UICONTROL Export] | Exporte la liste des demandes d’acquisition dans un fichier CSV. |
| [!UICONTROL Print] | Imprime la liste des demandes en cours. |
| [!UICONTROL Select] | Gère les sélections d’éléments qui doivent faire l’objet d’une action. <br/>**[!UICONTROL Select All]**- Sélectionne tous les éléments de la liste des demandes d’acquisition.<br/>**[!UICONTROL Remove Selected]** - Supprime tous les éléments sélectionnés de la liste des demandes. <br/>**[!UICONTROL Copy Selected]**- Copie tous les éléments sélectionnés dans une autre liste de demandes d’acquisition. |
| [!UICONTROL Add to Cart] | Ajoute les éléments sélectionnés au panier. |
| [!UICONTROL Update List] | Recalcule le sous-total pour refléter un changement de quantité. |
| [!UICONTROL Delete Requisition List] | Supprime la liste des demandes du compte de l’utilisateur de la société. |

{style="table-layout:auto"}
