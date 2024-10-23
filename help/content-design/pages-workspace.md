---
title: Contrôles de l’espace de travail de page
description: Découvrez les outils de l’espace de travail utilisés pour localiser et mettre à jour les pages de contenu.
exl-id: c53e3e70-9f88-46ec-b44d-133a2ff5d0d5
feature: Page Content, Admin Workspace
source-git-commit: fc8ebeeae56378967e95bda9bbf898c469b3a4c0
workflow-type: tm+mt
source-wordcount: '1356'
ht-degree: 0%

---

# Contrôles de l’espace de travail de page

L’espace de travail des pages comprend des outils pour vous aider à trouver rapidement les pages dont vous avez besoin et des commandes pour effectuer une maintenance périodique sur une ou plusieurs pages. Vous pouvez également rapidement mettre à jour les propriétés de page à partir de la grille.

![Grille de pages](./assets/pages-grid.png){width="700" zoomable="yes"}

## Mise à jour rapide des propriétés de page

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.
1. Cliquez sur n’importe quelle ligne de la grille.

   ![Les propriétés de page sont modifiables dans la grille Pages](./assets/page-grid-properties-update.png){width="600" zoomable="yes"}

   Pour sélectionner plusieurs enregistrements, cochez la case de chaque ligne à mettre à jour.

1. Mettez à jour l’une des propriétés suivantes :

   - **[!UICONTROL Title]**
   - **[!UICONTROL URL Key]**
   - **[!UICONTROL Status]**
   - **[!UICONTROL Layout]**

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

## Contrôles Workspace

| Contrôle | Description |
|--- |--- |
| [!UICONTROL Add New Page] | Ajoute une page. |
| [!UICONTROL Search] | Lance une recherche catalogue en fonction des filtres actuels. |
| [!UICONTROL Actions] | Répertorie toutes les actions qui peuvent être appliquées aux éléments sélectionnés de la liste. Pour appliquer une action à une ou plusieurs pages, cochez la case dans la première colonne de chaque enregistrement soumis à l’action. Options : `Delete` / `Disable` / `Enable` / `Edit` |
| [!UICONTROL Select] | Le contrôle dans l&#39;en-tête de la première colonne peut être utilisé pour sélectionner plusieurs enregistrements comme cible d&#39;action. Cochez la case dans la première colonne de chaque enregistrement que vous souhaitez sélectionner. Options : `Select All` / `Deselect All` |
| [!UICONTROL Save Edits] | Applique l’action en cours aux enregistrements sélectionnés. |
| [!UICONTROL Edit] | Ouvre l’enregistrement en mode d’édition. Vous pouvez effectuer la même opération en cliquant n’importe où sur la ligne. |

{style="table-layout:auto"}

## Colonnes

| Colonne | Description |
|--- |--- |
| [!UICONTROL Select] | La case à cocher de la première colonne permet de sélectionner plusieurs enregistrements. Options : `Select All` / `Deselect All` |
| [!UICONTROL ID] | L’ID est un nombre incrémenté attribué à chaque page. |
| [!UICONTROL Title] | Titre qui apparaît en haut de la page. |
| [!UICONTROL URL Key] | La clé URL est similaire à un nom de fichier et identifie la page dans l’URL. |
| [!UICONTROL Layout] | Détermine si la page s’affiche avec des encadrés à droite ou à gauche de la zone de contenu principale. Options : `1 column` / `2 columns with left bar` / `2 columns with right bar` / `3 columns` / `Empty` |
| [!UICONTROL Store View] | Utilisé pour associer la page à une vue de magasin spécifique. |
| [!UICONTROL Status] | Indique si la page est en ligne ou hors ligne. Options : `Enabled` / `Disabled` |
| [!UICONTROL Created] | Date à laquelle la page a été créée. |
| [!UICONTROL Modified] | Date de dernière modification de la page. |
| [!UICONTROL Action] | Les actions qui peuvent être appliquées à un enregistrement individuel incluent :<br/>**[!UICONTROL Edit]**- Ouvre la page en mode d’édition.<br/>**[!UICONTROL Delete]** - Supprime la page.<br/>**[!UICONTROL View]**- Affiche la page en mode aperçu. |

{style="table-layout:auto"}

## Autres colonnes

| Colonne | Description |
|--- |--- |
| [!UICONTROL Custom design from/to] | Indique les dates de début et de fin auxquelles la conception sélectionnée est appliquée à la page. ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement). |
| [!UICONTROL Custom Theme] | Applique un thème personnalisé à la page. |
| [!UICONTROL Custom Layout] | Détermine la disposition personnalisée de la page. |
| [!UICONTROL Meta Title] | Métadonnées du titre de la page |
| [!UICONTROL Meta Keywords] | Mots-clés méta pour la page |
| [!UICONTROL Meta Description] | La méta-description de la page |

{style="table-layout:auto"}

## Recherche de page

La zone de recherche située en haut à gauche de la grille _[!UICONTROL Pages]_peut être utilisée pour rechercher des pages spécifiques par mot-clé. Pour une recherche plus avancée, vous pouvez [filtrer](../getting-started/admin-grid-controls.md) la recherche selon plusieurs paramètres.

### Recherche par mot-clé

1. Saisissez un terme de recherche dans la zone de recherche de page.

1. Pour afficher les résultats, cliquez sur l’icône Rechercher (![Icône Loupe](../assets/icon-magnify-search.png)) .

   Les résultats incluent toutes les pages qui contiennent le mot-clé.

### Filtrage des résultats de la recherche

1. Si nécessaire, cliquez sur **[!UICONTROL Clear All]** pour effacer les critères de recherche précédents.

1. Pour afficher la sélection des filtres de recherche, cliquez sur le **[!UICONTROL Filters]** !Onglet ([Icône Entonnoir](../assets/icon-filter-search.png)).

1. Complétez autant de filtres que nécessaire pour décrire les pages que vous souhaitez trouver.

1. Cliquez sur **[!UICONTROL Apply Filters]** pour afficher les résultats.

### Filtres de recherche

| Filtrer | Description |
|--- |--- |
| [!UICONTROL ID] | Filtrez la recherche par identifiant d’enregistrement de page. |
| [!UICONTROL Title] | Filtrez la recherche en fonction du titre de la page. |
| [!UICONTROL URL Key] | Filtrez la recherche par clé URL. |
| [!UICONTROL Created] | Vous pouvez filtrer la recherche par date de création de la page. |
| [!UICONTROL Modified] | Filtrez la recherche selon la date de dernière modification de la page. |
| [!UICONTROL Store View] | Filtrez la recherche en fonction de la vue de magasin. Options : `All available` / `Store Views` |
| [!UICONTROL Layout] | Filtrez la recherche en fonction de la mise en page. Options : `1 column` / `2 columns with left bar` / `2 columns with right bar` / `3 columns` / `Empty` |
| [!UICONTROL Status] | Filtrez la recherche sur l’état de la page. Options : `Disabled` / `Published` |
| [!UICONTROL Custom design from / to] | Vous pouvez filtrer la recherche par date de début et de fin lorsque la conception sélectionnée est appliquée à la page. ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement). |
| [!UICONTROL Asset] | Filtrage de la recherche par ressources de titre de page |
| [!UICONTROL Custom Layout] | Filtrez la recherche selon une disposition personnalisée. Options : `1 column` / `2 columns with left bar` / `2 columns with right bar` / `3 columns` / `Empty` / `Page -- Full Width` / `Category -- Full Width` / `Product -- Full Width` |
| [!UICONTROL Custom Theme] | Filtrez la recherche selon un thème personnalisé. Options par défaut : `Magento Blank` / `Magento Luma` |
| [!UICONTROL Meta Keywords] | Filtrez la recherche en fonction des méta-mots-clés de la page. |
| [!UICONTROL Meta Title] | Filtrez la recherche en fonction du méta-titre de la page. |
| [!UICONTROL Meta Description] | Filtrez la recherche en fonction de la méta-description de la page. |

{style="table-layout:auto"}

### Outils de recherche

| Outil | Description |
|--- |--- |
| [!UICONTROL Apply Filters] | Applique tous les filtres aux résultats de la recherche. |
| [!UICONTROL Cancel] | Annule la recherche en cours. |
| [!UICONTROL Clear All] | Efface tous les filtres de recherche. |

{style="table-layout:auto"}

## Actions de page

Les pages peuvent être modifiées, désactivées, activées et supprimées. Pour appliquer une action à une page, cochez la case dans la première colonne. Pour sélectionner ou désélectionner toutes les pages, utilisez la commande de sélection située en haut de la colonne.

![Actions de page](./assets/pages-select.png){width="400" zoomable="yes"}

### Action unique

Utilisez la colonne _[!UICONTROL Action]_à l’extrême droite pour appliquer l’une des actions suivantes à une page individuelle :

- [!UICONTROL Edit] : ouvre la page en mode d’édition
- [!UICONTROL Delete] - supprime la page (confirmation requise)
- [!UICONTROL View] : ouvre une page directement sur le storefront

![Actions de page unique](./assets/page-grid-actions.png){width="600" zoomable="yes"}

### Actions en masse

Appliquez simultanément l’une des actions suivantes à plusieurs pages sélectionnées à l’aide du sélecteur _[!UICONTROL Action]_situé dans le coin supérieur gauche :

- [!UICONTROL Delete] - supprime les pages (confirmation requise)
- [!UICONTROL Disable] - désactive les pages du storefront
- [!UICONTROL Enable] - active les pages sur le storefront
- [!UICONTROL Edit] - ouvre les colonnes sur la grille en mode d’édition (**[!UICONTROL Title]**, **[!UICONTROL URL Key]**, **[!UICONTROL Layout]** et **[!UICONTROL Status]**)

## Disposition de la grille de page

La sélection des colonnes et leur ordre dans la grille peuvent être modifiés selon vos préférences. Pour conserver la nouvelle disposition des colonnes, vous pouvez l’enregistrer en tant que vue.

### Modifier la sélection des colonnes

Dans le coin supérieur droit, cliquez sur la commande _Colonnes_ (![Icône Colonne](../assets/icon-columns.png)) et procédez comme suit :

- Cochez la case d’une colonne que vous souhaitez ajouter à la grille.

- Décochez la case de toute colonne que vous souhaitez supprimer de la grille.

### Déplacer une colonne

1. Cliquez sur l’en-tête de la colonne et maintenez-la enfoncée.

1. Faites glisser la colonne vers la nouvelle position et la nouvelle version.

### Enregistrer une vue

1. Cliquez sur la commande _View_ (![Icône OEil](../assets/icon-view-eye.png)), puis cliquez sur **[!UICONTROL Save View As]**.

1. Saisissez le nom de la vue.

1. Pour enregistrer la vue, cliquez sur la _flèche_ (![icône de flèche](../assets/icon-arrow-save.png)).

   Le nom de la vue s’affiche désormais sous la forme de la vue actuelle.

### Modification de la vue

Cliquez sur la commande _View_ (![Icône OEil](../assets/icon-view-eye.png)) et effectuez l’une des opérations suivantes :

- Choisissez la vue que vous souhaitez utiliser.

- Modifiez le nom d’une vue en cliquant sur l’icône Modifier (![Icône Crayon](../assets/icon-edit-pencil.png)) et en mettant à jour le nom.

  ![La vue enregistrée apparaît dans les commandes d’affichage avec une icône de modification](./assets/pages-default-grid-control.png){width="600" zoomable="yes"}

## Modifications planifiées

{{ee-feature}}

Les modifications de page peuvent être appliquées selon le calendrier et regroupées avec d’autres modifications de contenu. Vous pouvez créer une campagne d’après les modifications planifiées apportées à une page ou appliquer les modifications à une campagne existante. Pour plus d’informations, voir [Content Staging](content-staging.md).

Lors de la configuration des plannings pour les modifications de page et la modification des campagnes, gardez à l’esprit les points suivants :

- Toutes les mises à jour planifiées sont appliquées consécutivement, ce qui signifie que toute entité ne peut avoir qu’une seule mise à jour planifiée à un moment donné. Toute mise à jour planifiée est appliquée à toutes les vues de magasin au cours de sa période. Par conséquent, une entité ne peut pas avoir une mise à jour planifiée différente pour différentes vues de magasin en même temps. Toutes les valeurs d’attribut d’entité dans toutes les vues de magasin, qui ne sont pas affectées par la mise à jour planifiée actuelle, sont extraites des valeurs par défaut et non de la mise à jour planifiée précédente.

- Si une campagne est liée à plusieurs pages, elle ne peut être modifiée que depuis le [tableau de bord d’évaluation du contenu](content-staging-dashboard.md).

- Si une campagne active est initialement créée sans date de fin, elle ne peut pas être modifiée ultérieurement pour inclure une date de fin. Dans ce cas, il est nécessaire de créer une opération en double et de renseigner la date de fin nécessaire.

- La date de début et la date de fin de la campagne doivent être définies à l’aide du fuseau horaire d’administrateur **_default_**, converti à partir du fuseau horaire local de chaque site web. Prenons l’exemple de plusieurs sites web dans différents fuseaux horaires, mais que vous souhaitez lancer une campagne basée sur un fuseau horaire américain. Dans ce cas, vous devez planifier une mise à jour distincte pour chaque fuseau horaire local, et définir **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** convertis de chaque fuseau horaire de site web local en fuseau horaire d’administration par défaut.

- Vous pouvez planifier et prévisualiser les modifications pour les mises à jour de produit. Pour plus d’informations, voir [Planification d’une mise à jour](content-staging-scheduled-update.md).

>[!NOTE]
>
>L’onglet [!UICONTROL Custom Design Update] a été supprimé dans ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce et ne peut pas être modifié directement sur la page. Vous devez créer une mise à jour planifiée pour ces activations.

![La page d’accueil affiche les modifications planifiées dans la partie supérieure](./assets/page-scheduled-change.png){width="600" zoomable="yes"}

