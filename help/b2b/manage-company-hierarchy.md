---
title: Gestion de la hiérarchie de l’entreprise
description: Créez et gérez des hiérarchies d’entreprises pour prendre en charge les organisations B2B avec des modèles opérationnels complexes.
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 6b06f52eb4ee8ca136a1c60fd6dc04a9ac96bbfa
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# Gérer les [!UICONTROL Company Hierarchy]

Les administrateurs peuvent créer un [!UICONTROL Company Hierarchy] en affectant les sociétés associées à une société mère désignée, qui est la société en haut de la hiérarchie de l’organisation.

À partir de l’administrateur, créez une société mère en modifiant une société (`[!UICONTROL Company Type] = Company`) individuelle et en affectant les sociétés associées dans la configuration [!UICONTROL Company Hierarchy].

![Grille de hiérarchie de l’entreprise](./assets/company-hierarchy-grid.png){width="700"}


>[!NOTE]
>
>Pour plus d’informations sur la grille [!UICONTROL Company Hierarchy], voir la description des champs [Hiérarchie de l’entreprise](account-company-create.md#company-hierarchy).

Gérez les affectations de l’entreprise en modifiant une société mère et en utilisant la grille *[!UICONTROL Company Hierarchy]* pour ajouter ou supprimer des entreprises. Utilisez le contrôle *[!UICONTROL Actions]* pour gérer la [configuration avancée des paramètres](#change-company-settings) pour les entreprises de l’entreprise.

## Affecter des sociétés à une société mère

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Grille d’entreprises](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Dans la grille [!UICONTROL Companies], ouvrez la page des détails de l’entreprise pour créer les affectations.

   - Pour affecter des sociétés supplémentaires à une société mère existante, sélectionnez l’action **[!UICONTROL Edit]** pour la société mère.
   - Pour créer une société mère, sélectionnez l’action **[!UICONTROL Edit]** pour la société désignée comme parent.

     Vous ne pouvez pas créer de société mère à partir d’une société mère ou d’une société enfant existante.

1. Sur la page Détails de la société, développez **[!UICONTROL Company Hierarchy]**, puis sélectionnez **[!UICONTROL Assign Companies]**.

   ![Créer une société mère](./assets/company-hierarchy-grid.png){width="675" zoomable="yes"}

1. Dans la liste des sociétés disponibles, sélectionnez les sociétés à affecter, puis sélectionnez **[!UICONTROL Assign Selected Companies]**.

   ![Sélectionner les entreprises à attribuer](./assets/company-hierarchy-select-companies-assign.png){width="675" zoomable="yes"}

1. Lorsque vous y êtes invité, effectuez l’affectation de la société en sélectionnant **[!UICONTROL Assign]**.

## Annulation de l’affectation d’entreprises à une société mère

1. Sur la page Entreprises , ouvrez la page des détails de la société mère en sélectionnant l’action **[!UICONTROL Edit]**.

   ![Page des détails de la société parente](./assets/company-update.png){width="700" zoomable="yes"}

1. Affichez la liste des sociétés affectées en développant **[!UICONTROL Company Hierarchy]**.

1. Supprimez la société de l’organisation.

   - Dans la colonne [!UICONTROL Action] de la société à supprimer, **[!UICONTROL Select]** > **[!UICONTROL Unassign from parent]**.

     ![Supprimer une société d&#39;une organisation](./assets/company-hierarchy-grid-unassign.png){width="640" zoomable="yes"}

   - Lorsque vous y êtes invité, supprimez la société affectée de la hiérarchie en sélectionnant **[!UICONTROL Unassign]**.

## Gestion des paramètres d’entreprise d’une entreprise

Mettez à jour la configuration [Paramètres avancés](account-company-create.md#advanced-settings) pour qu’une organisation applique la configuration parent à toutes les entreprises enfants ou applique les mêmes paramètres à certaines entreprises de l’organisation.

Au cours du processus de mise à jour, les valeurs de configuration initiales par défaut correspondent aux valeurs actuelles configurées pour la société mère. Vous devez modifier au moins un paramètre pour mettre à jour la configuration pour certaines entreprises.

**Modification de la configuration Paramètres avancés de plusieurs entreprises**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Dans la grille [!UICONTROL Companies], modifiez la société mère en sélectionnant **[!UICONTROL Edit]** dans la colonne **[!UICONTROL Action]**.

1. Sur la page des détails de la société parente, développez la section **[!UICONTROL Company Hierarchy]** pour afficher les entreprises incluses dans l’organisation.

1. Sélectionnez les sociétés à configurer.

   ![Sélectionner des entreprises dans la hiérarchie de l’entreprise](assets/company-hierarchy-select-companies.png){width="675" zoomable="yes"}

1. Dans la commande **[!UICONTROL Actions]** située au-dessus de la grille, sélectionnez **[!UICONTROL Change company settings]**.

   ![Modification des paramètres de l’entreprise pour la hiérarchie de l’entreprise](assets/company-hierarchy-change-company-settings-action.png){width="675" zoomable="yes"}

1. Modifiez la configuration des paramètres.

   - Sur la page [!UICONTROL Change company settings], recherchez le paramètre de configuration à modifier.

   - Cochez la case **[!UICONTROL Change]** pour activer le paramètre.

   - Mettez à jour la valeur selon vos besoins.

     ![Modification des paramètres de la société pour plusieurs entreprises](assets/company-hierarchy-change-settings-config.png){width="575" zoomable="yes"}

1. Après la mise à jour de la configuration, sélectionnez **[!UICONTROL Apply Changes]**.

1. Lorsque vous y êtes invité, sélectionnez **[!UICONTROL Change settings]** pour mettre à jour la configuration des entreprises sélectionnées.

>[!TIP]
>
>Gérez la configuration des paramètres avancés d’une seule entreprise en modifiant l’élément de ligne de l’entreprise.
