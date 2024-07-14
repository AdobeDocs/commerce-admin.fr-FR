---
title: Tableau de bord intermédiaire de contenu
description: Utilisez le tableau de bord d’évaluation du contenu pour accéder à un aperçu de toutes les campagnes actives et à venir.
exl-id: 67c18c1c-94c3-4d89-ae1e-868a465431e3
feature: Page Content, Staging
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# Tableau de bord intermédiaire de contenu

{{ee-feature}}

Le tableau de bord [!UICONTROL Content Staging] présente un aperçu de toutes les campagnes actives et à venir. Le format du tableau de bord peut être modifié d’une grille à une chronologie. Vous pouvez également utiliser des filtres pour rechercher des campagnes, personnaliser la disposition des colonnes et enregistrer différentes vues de la grille. Pour plus d’informations sur les commandes de l’espace de travail, voir [Espace de travail d’administration](../getting-started/admin-workspace.md).

![Tableau de bord intermédiaire en mode Grille](./assets/content-staging-grid-view.png){width="600" zoomable="yes"}

## Affichage du tableau de bord d’évaluation

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**.

1. Pour modifier le format du tableau de bord, définissez le contrôle **[!UICONTROL View As]** sur `list`, `Grid` ou `Timeline`.

   ![Mode Chronologie](./assets/content-staging-dashboard-timeline.png){width="600" zoomable="yes"}

   Lorsque la chronologie s’affiche, le curseur dans le coin inférieur droit permet d’ajuster l’affichage d’une à quatre semaines. Chaque colonne représente un jour.

1. Si la chronologie est affichée, faites glisser le curseur jusqu’à la position `4w` à l’extrême droite pour afficher une durée plus longue.

   ![Affichage de quatre semaines](./assets/content-staging-timeline-4-week-view.png){width="600" zoomable="yes"}

1. Pour afficher des informations générales sur la campagne, cliquez sur un élément de la page.

   - Pour ouvrir la campagne, cliquez sur **[!UICONTROL View/Edit]**.

   - Pour voir à quoi ressemble la campagne pour les clients du magasin ce jour-là, cliquez sur **[!UICONTROL Preview]**.

   ![Informations sur la campagne](./assets/content-staging-campaign-info.png){width="600" zoomable="yes"}

## Descriptions des colonnes du tableau de bord d’évaluation

| Colonne | Description |
|--- |--- |
| [!UICONTROL Status] | État de la campagne. `Active` ou `Upcoming`. |
| [!UICONTROL Update Name] | Nom de la campagne. |
| [!UICONTROL Includes] | Définit le nombre d’objets inclus dans la campagne. |
| [!UICONTROL Start Time] | Date de début de la campagne. |
| [!UICONTROL End Time] | Date à laquelle la campagne se termine. |
| [!UICONTROL Description] | Description supplémentaire de chaque opération. |
| [!UICONTROL Action] | Les actions qui peuvent être appliquées à un enregistrement individuel incluent :<br/>**[!UICONTROL View/Edit]**- Ouvre la campagne en mode d’édition.<br/>**[!UICONTROL Preview]** - Affiche la campagne en mode aperçu. |

{style="table-layout:auto"}

## Modifier une campagne

Les objets de campagne existants peuvent être modifiés à partir du tableau de bord d’évaluation, à l’exception des campagnes de règles de prix qui ne comportent pas de dates de fin.

>[!NOTE]
>
>Si une campagne contenant une règle de prix est initialement créée sans date de fin, elle ne peut pas être modifiée ultérieurement pour inclure une date de fin. Dans ce cas, il est nécessaire de créer une opération en double et de renseigner la date de fin nécessaire.

![Détails de la campagne](./assets/content-staging-dashboard-view-edit.png){width="600" zoomable="yes"}

La campagne dans cet exemple comprend deux catégories et trois produits individuels.

Suivez les étapes ci-dessous pour éditer l&#39;un des objets de cette campagne.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**.

1. Recherchez l&#39;opération dans la liste ou la chronologie affichée et ouvrez-la pour accéder aux détails :

   - Pour afficher une liste, cliquez sur **[!UICONTROL Select]**, puis sur **[!UICONTROL View/Edit]** dans la colonne _[!UICONTROL Action]_.
   - Pour un affichage de chronologie, cliquez une fois pour afficher le résumé, puis cliquez sur **[!UICONTROL View/Edit]**.

1. Mettez à jour les paramètres de la section _[!UICONTROL General]_si nécessaire.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) toute section contenant un élément à modifier.

   ![Mise à jour des produits attribués pour un élément de campagne](./assets/content-staging-campaign-edit-products.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save]**.
