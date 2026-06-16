---
title: Structure des comptes d'entreprise
description: Découvrez les structures d’entreprise et comment un administrateur d’entreprise peut les définir pour prendre en charge leurs workflows et politiques métier.
exl-id: 4724b208-b6ac-4de5-9a4c-bc4d68402506
feature: B2B, Companies
role: Admin
TQID: https://experienceleague.adobe.com/d4VWp0S-Z6BfOPBAI80LeB62GUXYax0obDztcm-VOYw
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffa
subfeature_v2: id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 710
ht-degree: 1%

---

# Structure des comptes d&#39;entreprise

Un compte d’entreprise peut être configuré pour refléter la structure de l’entreprise. Au départ, la structure de l’entreprise comprend uniquement l’administrateur ou l’administratrice de l’entreprise, mais peut être étendue pour inclure des équipes d’utilisateurs et utilisatrices. Les utilisateurs peuvent être associés à des équipes ou organisés dans une hiérarchie de divisions et de subdivisions au sein de la société.

![Structure d’entreprise avec divisions](./assets/company-structure-diagram.svg){width="500"}

Dans le tableau de bord du compte de l’administrateur de l’entreprise sur le storefront, la structure de l’entreprise est représentée sous la forme d’une arborescence et se compose initialement uniquement de l’administrateur de l’entreprise.

![Structure de l’entreprise avec l’administrateur d’entreprise](./assets/company-structure-tree-admin.png){width="700" zoomable="yes"}

Pour les commerçants, la structure complète de l’entreprise est reflétée dans les grilles _Entreprises_ et _Clients_ au sein de l’administration. La grille Sociétés répertorie toutes les sociétés, quel que soit leur statut.

![Grille des sociétés](./assets/companies-grid.png){width="700" zoomable="yes"}

L&#39;exemple suivant illustre la grille [!UICONTROL Customers] avec les comptes d&#39;administration initiaux de chaque société.

![Grille des clients avec les comptes d’administration de la société](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

Après avoir créé le compte, l’administrateur ou l’administratrice d’entreprise peut définir une structure d’entreprise avec des [équipes](account-company-structure.md), configurer les [utilisateurs de l’entreprise](account-company-users.md) et établir des [rôles et autorisations](account-company-roles-permissions.md) pour chacun.

>[!NOTE]
>
>Lorsqu’un utilisateur d’entreprise est ajouté, il est d’abord ajouté à la structure racine de l’entreprise, puis subordonné à l’administrateur de l’entreprise. Si l’administrateur ou l’administratrice de l’entreprise exerce plusieurs rôles au sein de l’entreprise, créez des comptes utilisateur d’entreprise distincts avec une adresse électronique différente pour chaque rôle.

## Icônes de structure de l’entreprise

| Icon | Description |
| ---- | ----------------- |
| ![Icône Administrateur d’entreprise](./assets/company-icon-admin.png) | Représente l&#39;administrateur de la société dans la structure de la société. |
| ![ Icône Équipe ](./assets/company-icon-team.png) | Représente une équipe dans la structure de l&#39;entreprise. |
| ![Icône Utilisateur](./assets/company-icon-user.png) | Représente un utilisateur dans la structure de l’entreprise. |
| ![ Icône Déplacer ](./assets/company-icon-move.png) | Déplace une équipe vers un autre poste de la structure de l&#39;entreprise. |
| ![Icône d’extension](./assets/company-icon-expand.png) | Développe une équipe dans la structure de l&#39;entreprise. |
| ![Icône Réduire ](./assets/company-icon-collapse.png) | Réduit une équipe dans la structure de l&#39;entreprise. |

{style="table-layout:auto"}

## Créer des équipes d’entreprise

La structure d&#39;un compte d&#39;entreprise doit refléter l&#39;organisation d&#39;achat, qu&#39;il s&#39;agisse d&#39;une organisation simple et plate ou d&#39;une organisation complexe avec différentes équipes pour chaque subdivision et division de l&#39;entreprise.

Si le magasin est [configuré](enable-basic-features.md) pour permettre aux sociétés de gérer leurs propres comptes, la configuration de la structure de la société est l’une des premières tâches qu’un administrateur de la société doit effectuer après la validation du compte. Dans le compte d’entreprise, la structure de l’entreprise est représentée sous la forme d’une arborescence, l’administrateur de l’entreprise étant en haut.

![Structure d’entreprise avec équipes](./assets/company-structure-teams-diagram.svg){width="450"}

1. L’administrateur de l’entreprise se connecte à son compte.

1. Dans le panneau de gauche, sélectionne **[!UICONTROL Company Structure]**.

1. Sous **[!UICONTROL Business Structure]**, clique sur **[!UICONTROL Add Team]** et effectue les opérations suivantes :

   - Entre les **[!UICONTROL Team Title]** et les **[!UICONTROL Description]**.

     Le titre d’équipe peut être tout élément représentant la structure de la société, telle qu’une équipe, un bureau ou une division au sein de la société

     ![Ajouter une équipe](./assets/company-structure-add-team.png){width="700" zoomable="yes"}

   - Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

   - Crée autant d’équipes que nécessaire.

1. Pour créer une hiérarchie d’équipes, l’administrateur effectue les opérations suivantes :

   - Sélectionne l&#39;équipe parente, puis cliquez sur **[!UICONTROL Add Team]**.

     ![Structure d’entreprise avec divisions](./assets/company-structure-northwest-division.png){width="600" zoomable="yes"}

   - Entre les **[!UICONTROL Team Title]** et les **[!UICONTROL Description]**.

   - Effectue un clic sur **[!UICONTROL Save]**.

1. Répète ces étapes pour créer autant d’équipes, ou de divisions et de subdivisions que nécessaire.

   ![Structure d&#39;entreprise avec divisions et subdivisions](./assets/company-structure-divisions.png){width="600" zoomable="yes"}

## Déplacer une équipe

Lorsque l&#39;administrateur de la société travaille avec la structure de la société, il peut faire glisser des équipes ou des divisions vers d&#39;autres emplacements de la structure.

1. L’administrateur d’entreprise localise l’équipe à déplacer.

1. Clique et fait glisser l’équipe vers un nouveau poste dans la structure de l’entreprise.

## Supprimer une équipe

>[!NOTE]
>
>Avant de supprimer une équipe, il est recommandé de s’assurer que la bonne équipe est sélectionnée (les équipes supprimées ne peuvent pas être restaurées).

1. L&#39;administrateur de l&#39;entreprise sélectionne l&#39;équipe à supprimer.

1. Effectue un clic sur **[!UICONTROL Delete Selected]**.

1. Lorsque vous êtes invité à confirmer, cliquez sur **[!UICONTROL Delete]**.

## Développer ou réduire la structure de l’équipe

Lorsque l’administrateur de l’entreprise travaille avec la structure de l’entreprise, il peut réduire ou développer l’arborescence :

- Clics **[!UICONTROL Collapse All]** ou **[!UICONTROL Expand All]**.

- Clique sur ![Icône développée](../assets/icon-display-collapse.png) pour réduire une équipe ou ![Icône réduite](../assets/icon-display-expand.png) pour développer une équipe.

## Affectation d’utilisateurs à des équipes

Lorsque des équipes et des utilisateurs sont ajoutés pour la première fois à la [structure de l’entreprise](account-company-structure.md), ils sont placés au même niveau sous l’administration de l’entreprise.

![Structure de l’entreprise avec les utilisateurs et les équipes](./assets/company-users-added.png){width="700" zoomable="yes"}

| Contrôle | Description |
|--- |--- |
| [!UICONTROL Collapse All / Expand All] | Réduit ou développe l’arborescence de la structure d’entreprise |
| [!UICONTROL Add User] | Crée un utilisateur sous l&#39;équipe actuelle |
| [!UICONTROL Add Team] | Crée une équipe |
| [!UICONTROL Edit Selected / Remove from Structure] | Modifie les informations utilisateur ou supprime des utilisateurs de l’arborescence métier. Pour plus d’informations, voir [Gestion des comptes utilisateur d’entreprise](account-company-users.md). |

{style="table-layout:auto"}

1. Dans le panneau de gauche, l’administrateur de l’entreprise choisit **[!UICONTROL Company Structure]**.

1. Pour affecter un utilisateur à une équipe existante, il ou elle fait glisser (![icône Déplacer](../assets/icon-move.png)) l’utilisateur ou l’utilisatrice sous l’équipe appropriée.

   ![Affectations d’équipe](./assets/company-structure-teams-users-assigned.png){width="700" zoomable="yes"}
