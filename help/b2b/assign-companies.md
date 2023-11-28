---
title: Gestion de la hiérarchie de l’entreprise
description: Créez et gérez des hiérarchies d’entreprises pour prendre en charge les organisations B2B avec des modèles opérationnels complexes.
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 10b01db562777ef2fcc224177d7a83c0a6fc90e7
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Gérer les [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponible uniquement pour les participants au programme bêta"}

Les administrateurs peuvent créer un [!UICONTROL Company Hierarchy] en attribuant des sociétés liées à une société mère désignée, qui est la société en haut de la hiérarchie organisationnelle.

Créer une société mère en modifiant une société qui n’a pas été affectée à une entreprise existante [!UICONTROL Company Hierarchy]et assigner des sociétés associées.

![Grille de hiérarchie de l’entreprise](./assets/company-detail-view.png){width="700"}

Une fois qu’une société a été affectée à une hiérarchie, la variable [!UICONTROL Company type] dans la colonne **Entreprises** grid identifie la société comme `Parent` ou  `Child` société.  Si la variable [!UICONTROL Company Type] is `Company`, la société ne fait pas partie de la hiérarchie de la société et peut devenir une société mère ou être affectée à une société mère existante.

>[!NOTE]
>
>Pour plus d’informations sur la variable [!UICONTROL Company Hierarchy] grille, voir [Hiérarchie des entreprises](account-company-create.md#company-hierarchy) description des champs.

Dans l’administrateur, vous gérez les affectations d’entreprise en modifiant une société, puis en utilisant la variable [!UICONTROL Company Hierarchy] de la [!UICONTROL Company] pour affecter ou annuler l’affectation d’entreprises.

## Affecter des sociétés à une société mère

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Grille des entreprises](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Dans la grille Entreprises , ouvrez la page des détails de la société pour créer les affectations.

   - Pour affecter des sociétés supplémentaires à une société mère existante, sélectionnez l’option **[!UICONTROL Edit]** action pour la société mère.
   - Pour créer une société mère, sélectionnez la variable **[!UICONTROL Edit]** action de la société désignée comme parent.

     Vous ne pouvez pas créer de société mère à partir d’une société mère ou d’une société enfant existante.

   ![Nouvelle entreprise](./assets/company-update.png){width="700" zoomable="yes"}

1. Sur la page Détails de l’entreprise, développez la variable **[!UICONTROL Company Hierarchy]** , puis sélectionnez **[!UICONTROL Assign Companies]**.

   ![Nouvelle entreprise](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

   Lorsque vous développez cette vue, vous pouvez voir les affectations de société existantes, le cas échéant. La société mère apparaît toujours au-dessus de _[!UICONTROL Company Hierarchy]_d’une grille `current company indicator` affiché dans la ligne de l’entreprise en cours d’édition.

1. Les entreprises disponibles pour affectation sont répertoriées dans la grille. Sélectionnez les entreprises à affecter, puis cliquez sur **[!UICONTROL Assign Selected Companies]**.

1. Vous pouvez **Tout sélectionner sur cette page** ou un élément de ligne d’entreprise spécifique, puis cliquez sur **[!UICONTROL Assign Selected Companies]**.

   ![Nouvelle entreprise](./assets/assign-selected-companies.png){width="700" zoomable="yes"}

1. Lorsque vous y êtes invité, effectuez l’affectation de la société en sélectionnant **[!UICONTROL Assign]**.

## Annulation de l’affectation d’entreprises à une société mère

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Grille des entreprises](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Sur la page Entreprises , ouvrez la page des détails de la société mère en sélectionnant **[!UICONTROL Edit]** action.

   ![Nouvelle entreprise](./assets/company-update.png){width="700" zoomable="yes"}

1. Affichez la liste des entreprises affectées en développant la variable **[!UICONTROL Company Hierarchy]** menu déroulant.

1. Dans la grille de hiérarchie de l’entreprise, annulez l’affectation d’une entreprise en sélectionnant l’option **[!UICONTROL Select]** action de la société, puis choisissez **[!UICONTROL Unassign from parent]**.

   ![Nouvelle entreprise](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

1. Lorsque vous y êtes invité, supprimez la société affectée de la hiérarchie en sélectionnant **[!UICONTROL Unassign]**.
