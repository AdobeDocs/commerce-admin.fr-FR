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

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponible uniquement pour les participants au programme Beta"}

Les administrateurs peuvent créer un [!UICONTROL Company Hierarchy] en affectant des sociétés associées à une société mère désignée, qui est la société au sommet de l’organisation. Si [!UICONTROL Company Type] est `Company`, la société ne fait pas partie d’une organisation et peut devenir une société mère ou être affectée à une société mère existante.

Dans l’administrateur, vous gérez les affectations de l’entreprise en modifiant une société, puis en mettant à jour la configuration [!UICONTROL Company Hierarchy] pour affecter ou annuler l’affectation des entreprises.

![Grille de hiérarchie de l’entreprise](./assets/company-detail-hierarchy-current-flag.png){width="700"}

>[!NOTE]
>
>Pour plus d’informations sur la grille [!UICONTROL Company Hierarchy], voir la description des champs [Hiérarchie de l’entreprise](account-company-create.md#company-hierarchy).

## Affectation de sociétés à une organisation

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Grille d’entreprises](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Dans la grille [!UICONTROL Companies], ouvrez la page des détails de l’entreprise pour créer les affectations.

   - Pour affecter des sociétés supplémentaires à une société mère existante, sélectionnez l’action **[!UICONTROL Edit]** pour la société mère.
   - Pour créer une société mère, sélectionnez l’action **[!UICONTROL Edit]** que la société doit désigner comme parent.

     Vous ne pouvez pas créer une société mère à partir d’une société mère ou d’une société enfant existante.

1. Sur la page des détails de la société, développez **[!UICONTROL Company Hierarchy]**.

   ![Grille de hiérarchie de l’entreprise](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

   La grille affiche les affectations d’entreprise existantes, le cas échéant. La société mère est toujours positionnée en haut de la grille [!UICONTROL Company Hierarchy]. L’indicateur `[!UICONTROL Current]` indique la société en cours de modification.

1. Ajoutez des entreprises à l’organisation parente.

   - Choisissez parmi une liste de sociétés disponibles en sélectionnant **[!UICONTROL Assign Companies]**.

   - **Sélectionnez Tout sur cette page** ou sélectionnez un ou plusieurs éléments de ligne d’entreprise spécifiques.

   - Sélectionnez **[!UICONTROL Assign Selected Companies]**.

   - Effectuez l’affectation de la société en sélectionnant **[!UICONTROL Assign]**.

     ![Affecter des entreprises à l’organisation](./assets/assign-selected-companies-hierarchy.png){width="675" zoomable="yes"}

## Annulation de l’affectation d’entreprises à une société mère

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Grille d’entreprises](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Dans la grille [!UICONTROL Companies], ouvrez la page des détails de la société mère en sélectionnant **[!UICONTROL Edit]**.

1. Affichez la liste des sociétés affectées en développant **[!UICONTROL Company Hierarchy]**.

1. Dans la grille [!UICONTROL Company Hierarchy], annulez l’affectation d’une société à l’aide du contrôle d’action **[!UICONTROL Select]** pour choisir **[!UICONTROL Unassign from parent]**.

   ![Annulation de l’affectation des entreprises à une organisation parente](./assets/company-hierarchy-grid-unassign.png){width="700" zoomable="yes"}

1. Lorsque vous y êtes invité, supprimez la société affectée de la hiérarchie en sélectionnant **[!UICONTROL Unassign]**.
