---
title: Table de référence des vues de catalogue
description: Table de référence réutilisée pour la grille des vues de catalogue
source-git-commit: bc4baccc4b40fb7ecdc7f489bfaf3c797881db88
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%
---
# Table de référence des vues de catalogue

La grille répertorie une ligne pour chaque vue de catalogue créée lorsqu’un catalogue partagé est synchronisé avec [!DNL Adobe Commerce Optimizer]. La grille est en lecture seule, à l’exception de l’action d’affectation de clé. Les vues catalogue sont créées et supprimées automatiquement lorsque le connecteur synchronise les catalogues partagés configurés dans Adobe Commerce. Si un catalogue est supprimé, il existe un [délai de grâce](/help/systems/catalog-view-sync-status.md#configure-the-deletion-grace-period) avant la suppression de la vue de catalogue et des données correspondantes.

Pour attribuer ou annuler l’attribution de clés d’accès restreint, voir [Attribuer des clés à une vue de catalogue](/help/systems/restricted-access-keys.md#assign-keys-to-a-catalog-view).

| Champ | Description |
| --- | --- |
| [!UICONTROL ACO Catalog View ID] | Identifiant de la vue de catalogue correspondante dans [!DNL Adobe Commerce Optimizer]. Voir [Synchronisation de l’affichage du catalogue - Résumé](/help/systems/catalog-view-sync-status.md#catalog-view-sync-status-summary) pour vérifier l’intégrité de la synchronisation. |
| [!UICONTROL Store View] | Vue de magasin représentée par la vue de catalogue. Voir [Vues de la boutique](/help/stores-purchase/store-views.md). |
| [!UICONTROL Access Keys] | Titres des clés d’accès restreint actuellement affectées à la vue catalogue. Voir [Gestion des clés d’accès limitées](/help/systems/restricted-access-keys.md). |
| [!UICONTROL Actions] | Sélectionnez **[!UICONTROL Edit Restricted Access Keys]** pour affecter ou annuler l’affectation de clés à la vue de catalogue. Voir [Attribuer des clés à une vue de catalogue](/help/systems/restricted-access-keys.md#assign-keys-to-a-catalog-view). |

{style="table-layout:auto"}
