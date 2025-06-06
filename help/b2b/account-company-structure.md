---
title: Structure du compte d’entreprise
description: Découvrez les structures de l’entreprise et comment un administrateur de l’entreprise peut les définir pour prendre en charge leurs processus et stratégies d’entreprise.
exl-id: 4724b208-b6ac-4de5-9a4c-bc4d68402506
feature: B2B, Companies
role: Admin
source-git-commit: fec72b792cf3149c05803874795c45f9f4e28673
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---

# Structure du compte d’entreprise

Un compte d’entreprise peut être configuré pour refléter la structure de l’entreprise. Au départ, la structure de l’entreprise inclut uniquement l’administrateur de l’entreprise, mais peut être développée pour inclure des équipes d’utilisateurs. Les utilisateurs peuvent être associés à des équipes ou organisés au sein d’une hiérarchie de divisions et de subdivisions au sein de l’entreprise.

![Structure de l’entreprise avec des divisions](./assets/company-structure-diagram.svg){width="500"}

Dans le tableau de bord du compte de l’administrateur de l’entreprise sur le storefront, la structure de l’entreprise est représentée sous la forme d’une arborescence et se compose initialement uniquement de l’administrateur de l’entreprise.

![Structure de l’entreprise avec administrateur de l’entreprise](./assets/company-structure-tree-admin.png){width="700" zoomable="yes"}

Pour les commerçants, la structure complète de l’entreprise est reflétée dans les grilles _Entreprises_ et _Clients_ au sein de l’administrateur. La grille Entreprises répertorie toutes les entreprises, quel que soit leur statut.

![Grille d’entreprises](./assets/companies-grid.png){width="700" zoomable="yes"}

L’exemple suivant montre la grille [!UICONTROL Customers] avec les comptes administrateur de société initiaux pour chaque entreprise.

![Grille des clients avec comptes d’administrateur de l’entreprise](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

Après la création du compte, l’administrateur de l’entreprise peut définir une structure d’entreprise avec [équipes](account-company-structure.md), configurer les [utilisateurs de l’entreprise](account-company-users.md) et établir des [rôles et autorisations](account-company-roles-permissions.md) pour chacun d’eux.

>[!NOTE]
>
>Lorsqu’un utilisateur d’entreprise est ajouté, il est initialement ajouté à la structure racine de l’entreprise, sous la supervision de l’administrateur de l’entreprise. Si l’administrateur de l’entreprise remplit plusieurs rôles au sein de l’entreprise, créez des comptes utilisateurs de l’entreprise distincts avec une adresse électronique différente pour chaque rôle.

## Icônes de structure de l’entreprise

| Icône | Description |
| ---- | ----------------- |
| ![Icône de l’administrateur de l’entreprise](./assets/company-icon-admin.png) | Représente l’administrateur de l’entreprise dans la structure de l’entreprise. |
| ![Icône Équipe](./assets/company-icon-team.png) | Représente une équipe dans la structure de l’entreprise. |
| ![Icône de l’utilisateur](./assets/company-icon-user.png) | Représente un utilisateur dans la structure de l’entreprise. |
| ![Icône Déplacer](./assets/company-icon-move.png) | Déplace une équipe vers un autre poste de la structure de l’entreprise. |
| ![Icône d’extension](./assets/company-icon-expand.png) | Développe une équipe dans la structure de l’entreprise. |
| ![Icône Réduire](./assets/company-icon-collapse.png) | Réduit une équipe dans la structure de l’entreprise. |

{style="table-layout:auto"}

## Création d’équipes d’entreprise

La structure d’un compte de société doit refléter l’organisation d’achat, qu’il s’agisse d’une organisation simple et plate ou d’une organisation complexe avec des équipes différentes pour chaque division et division de la société.

Si le magasin est [configuré](enable-basic-features.md) pour permettre aux entreprises de gérer leurs propres comptes, la configuration de la structure de l’entreprise est l’une des premières tâches à accomplir par un administrateur de l’entreprise une fois le compte approuvé. Dans le compte de l’entreprise, la structure de l’entreprise est représentée sous la forme d’une arborescence dont l’administrateur est situé en haut.

![Structure de l’entreprise avec équipes](./assets/company-structure-teams-diagram.svg){width="450"}

1. L’administrateur de la société se connecte à son compte.

1. Dans le panneau de gauche, choisissez **[!UICONTROL Company Structure]**.

1. Sous **[!UICONTROL Business Structure]**, clique sur **[!UICONTROL Add Team]** et effectue les opérations suivantes :

   - Entrez les **[!UICONTROL Team Title]** et **[!UICONTROL Description]**.

     Le Titre de l’équipe peut être tout ce qui représente la structure de l’entreprise, telle qu’une équipe, un bureau ou une division au sein de l’entreprise.

     ![Ajouter une équipe](./assets/company-structure-add-team.png){width="700" zoomable="yes"}

   - Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

   - Crée autant d’équipes que nécessaire.

1. Pour créer une hiérarchie d’équipes, l’administrateur effectue les opérations suivantes :

   - Sélectionne l’équipe parente, puis cliquez sur **[!UICONTROL Add Team]**.

     ![Structure de l’entreprise avec des divisions](./assets/company-structure-northwest-division.png){width="600" zoomable="yes"}

   - Entrez les **[!UICONTROL Team Title]** et **[!UICONTROL Description]**.

   - Clics **[!UICONTROL Save]**.

1. Répète ces étapes pour créer autant d’équipes, de divisions et de subdivisions que nécessaire.

   ![Structure de l’entreprise avec des divisions et des subdivisions](./assets/company-structure-divisions.png){width="600" zoomable="yes"}

## Déplacer une équipe

Comme l’administrateur de l’entreprise travaille avec la structure de l’entreprise, il peut faire glisser des équipes ou des divisions vers d’autres emplacements de la structure.

1. L’administrateur de l’entreprise localise l’équipe à déplacer.

1. Clique et fait glisser l’équipe vers un nouveau poste dans la structure de l’entreprise.

## Suppression d’une équipe

>[!NOTE]
>
>Avant de supprimer une équipe, il est recommandé de s’assurer que la bonne équipe est sélectionnée ; les équipes supprimées ne peuvent pas être restaurées.

1. L&#39;administrateur de l&#39;entreprise sélectionne l&#39;équipe à supprimer.

1. Clics **[!UICONTROL Delete Selected]**.

1. Lorsque vous êtes invité à confirmer l’opération, cliquez sur **[!UICONTROL Delete]**.

## Développer ou réduire la structure de l’équipe

Lorsque l’administrateur de l’entreprise travaille avec la structure de l’entreprise, il peut réduire ou développer l’arborescence :

- Cliquez sur **[!UICONTROL Collapse All]** ou **[!UICONTROL Expand All]**.

- Cliquez sur ![Icône développée](../assets/icon-display-collapse.png) pour réduire une équipe ou sur ![Icône réduite](../assets/icon-display-expand.png) pour développer une équipe.

## Affecter des utilisateurs à des équipes

Lorsque des équipes et des utilisateurs sont ajoutés pour la première fois à la [structure de l’entreprise](account-company-structure.md), ils sont placés au même niveau sous l’administrateur de l’entreprise.

![Structure de l’entreprise avec utilisateurs et équipes](./assets/company-users-added.png){width="700" zoomable="yes"}

| Contrôle | Description |
|--- |--- |
| [!UICONTROL Collapse All / Expand All] | Réduit ou développe l’arborescence de la structure d’entreprise |
| [!UICONTROL Add User] | Crée un utilisateur sous l’équipe actuelle |
| [!UICONTROL Add Team] | Crée une équipe |
| [!UICONTROL Edit Selected / Remove from Structure] | Modifie les informations utilisateur ou supprime les utilisateurs de l’arborescence de l’entreprise. Pour plus d’informations, voir [Gestion des comptes utilisateurs de l’entreprise](account-company-users.md). |

{style="table-layout:auto"}

1. Dans le panneau de gauche, l’administrateur de l’entreprise choisit **[!UICONTROL Company Structure]**.

1. Pour affecter un utilisateur à une équipe existante, il fait glisser (![Icône Déplacer](../assets/icon-move.png)) l’utilisateur sous l’équipe appropriée.

   ![Affectations d’équipe](./assets/company-structure-teams-users-assigned.png){width="700" zoomable="yes"}
