---
title: Gestion des entreprises
description: Rationalisation de l’administration et de la gestion des organisations B2B avec des modèles opérationnels complexes.
feature: B2B, Companies, Storefront
role: Admin
hide: false
hidefromtoc: false
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Gestion des entreprises

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponible uniquement pour les participants au programme Beta"}

La gestion des entreprises simplifie les opérations commerciales pour les entreprises aux structures organisationnelles complexes. Les utilisateurs administrateurs peuvent créer une hiérarchie d’entreprise pour refléter une organisation B2B en affectant des sociétés à la société mère désignée. Cette affectation permet à l’administrateur de la société mère d’afficher et de gérer les entreprises au sein de l’organisation.

Exécutez les tâches de gestion de l’entreprise à partir de la vue *[!UICONTROL Companies]*. Depuis l’administrateur, accédez à **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![Grille de gestion des entreprises B2B](./assets/companies-grid-view.png){width="700" zoomable="yes"}

Dans la colonne *[!UICONTROL Companies grid]*, la colonne *[!UICONTROL Company Type]* indique si une entreprise est gérée dans le cadre d’une organisation ou dans le cadre d’une entreprise distincte.

- `Parent` est une entreprise à laquelle une ou plusieurs sociétés sont affectées. Une société mère ne peut pas être affectée en tant qu’enfant d’une autre société.

- `Child` est une entreprise qui a été affectée à une organisation. Une société ne peut être affectée qu’à une seule société mère.

- `Company` représente une seule société. Une seule société peut faire partie d’une organisation en en en faisant une société mère ou en l’affectant à une société mère existante.

Lorsque vous modifiez une société mère ou fille, développez *[!UICONTROL Company Hierarchy]* pour afficher toutes les entreprises de l’organisation. Un indicateur `Current` indique la société que vous êtes en train de modifier.

![Grille hiérarchique de l’entreprise B2B](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}


## Afficher et configurer le [!UICONTROL Company Hierarchy]

Lors de la création initiale de l’entreprise, la grille [!UICONTROL Company Hierarchy] est vide. Il est également vide si la société est une seule société.

![Grille hiérarchique d’entreprise B2B](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

Pour les sociétés parentes, les utilisateurs administrateurs disposant des autorisations appropriées peuvent effectuer les tâches suivantes :

- Créez la hiérarchie de l’entreprise en créant une organisation parente ou en mettant à jour une organisation existante.
- Gérez une organisation existante pour ajouter ou supprimer des entreprises.

Pour plus d’informations, voir [Gestion de la hiérarchie de l’entreprise](assign-companies.md).
