---
title: Gestion de la hiérarchie de l’entreprise
description: Découvrez comment gérer des organisations B2B avec des modèles opérationnels complexes en créant des hiérarchies d’entreprise
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# Gérer les [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponible uniquement pour les participants au programme bêta"}

Les administrateurs peuvent créer un [!UICONTROL Company Hierarchy] en attribuant des sociétés liées à une société mère désignée, qui est la société au sommet de l’organisation. Si la variable [!UICONTROL Company Type] is `Company`, la société ne fait pas partie d’une organisation et peut devenir une société mère ou être affectée à une société mère existante.

Dans l’administrateur, vous gérez les affectations de l’entreprise en modifiant une société, puis en mettant à jour la variable [!UICONTROL Company Hierarchy] configuration pour affecter ou annuler l’affectation d’entreprises.

![Grille de hiérarchie de l’entreprise](./assets/company-detail-hierarchy-current-flag.png){width="700"}

>[!NOTE]
>
>Pour plus d’informations sur la variable [!UICONTROL Company Hierarchy] grille, voir [Hiérarchie des entreprises](account-company-create.md#company-hierarchy) description des champs.

## Affectation de sociétés à une organisation

1. Dans la _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Grille des entreprises](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Dans le [!UICONTROL Companies] , ouvrez la page des détails de l’entreprise pour créer les affectations.

   - Pour affecter des sociétés supplémentaires à une société mère existante, sélectionnez l’option **[!UICONTROL Edit]** action pour la société mère.
   - Pour créer une société mère, sélectionnez la variable **[!UICONTROL Edit]** action de la société à désigner comme parent.

     Vous ne pouvez pas créer une société mère à partir d’une société mère ou d’une société enfant existante.

1. Sur la page des détails de l’entreprise, développez **[!UICONTROL Company Hierarchy]**.

   ![Grille de hiérarchie de l’entreprise](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

   La grille affiche les affectations d’entreprise existantes, le cas échéant. La société mère est toujours positionnée en haut de la page [!UICONTROL Company Hierarchy] grid. La variable `[!UICONTROL Current]` indique la société en cours de modification.

1. Ajoutez des entreprises à l’organisation parente.

   - Effectuez un choix parmi une liste de sociétés disponibles en sélectionnant **[!UICONTROL Assign Companies]**.

   - **Tout sélectionner sur cette page** ou sélectionnez un ou plusieurs éléments de ligne d’entreprise spécifiques.

   - Sélectionner **[!UICONTROL Assign Selected Companies]**.

   - Effectuez l’affectation de la société en sélectionnant **[!UICONTROL Assign]**.

     ![Affecter des entreprises à l’organisation](./assets/assign-selected-companies-hierarchy.png){width="675" zoomable="yes"}

## Annulation de l’affectation d’entreprises à une société mère

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Grille des entreprises](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Dans le [!UICONTROL Companies] grille, ouvrez la page des détails de la société mère en sélectionnant **[!UICONTROL Edit]**.

1. Affichez la liste des entreprises affectées en développant **[!UICONTROL Company Hierarchy]**.

1. Dans la [!UICONTROL Company Hierarchy] grille, annulez l’affectation d’une société à l’aide de la fonction **[!UICONTROL Select]** contrôle d’action à choisir **[!UICONTROL Unassign from parent]**.

   ![Annulation de l’affectation d’entreprises à une organisation parente](./assets/company-hierarchy-grid-unassign.png){width="700" zoomable="yes"}

1. Lorsque vous y êtes invité, supprimez la société affectée de la hiérarchie en sélectionnant **[!UICONTROL Unassign]**.
