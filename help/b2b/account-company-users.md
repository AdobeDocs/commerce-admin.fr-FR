---
title: Gestion des comptes d’utilisateurs de l’entreprise
description: Découvrez les comptes d’utilisateurs de l’entreprise et leur fonctionnement dans le compte d’entreprise associé.
exl-id: 36b55f61-e579-4eb8-8f67-0156221d378e
feature: B2B, Companies, User Account, Storefront
role: Admin, User
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Gestion des comptes d’utilisateurs de l’entreprise

Les utilisateurs de la société sont affectés par l’administrateur de la société et sont visibles à partir de l’administrateur dans la grille _[!UICONTROL Customers]_par type de client,_[!UICONTROL Company User]_. Ces personnes sont généralement des acheteurs disposant de différents niveaux de permission d’accéder aux services et aux ressources des magasins.

L’administrateur de l’entreprise commence par configurer la [structure de l’entreprise](account-company-structure.md), puis effectue les tâches suivantes, si nécessaire :

- Créer des utilisateurs d’entreprise et affecter des utilisateurs à des équipes

- Définition des rôles et des autorisations et affectation d’utilisateurs à des rôles

>[!IMPORTANT]
>
>Les utilisateurs de l’entreprise peuvent uniquement être ajoutés, modifiés ou supprimés par l’administrateur de l’entreprise. La suppression ne peut pas être annulée car l’utilisateur est supprimé de la structure de l’entreprise.

## Ajout d’utilisateurs d’entreprise

1. Depuis le storefront, l’administrateur de la société se connecte à son compte.

1. Dans le panneau de gauche, choisissez **[!UICONTROL Company Users]**.

   ![Utilisateurs de l’entreprise](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Clique sur **[!UICONTROL Add New User]** et effectue les opérations suivantes :

   - Saisissez le **[!UICONTROL Job Title]** du nouvel utilisateur.

   - Choisit le **[!UICONTROL User Role]** approprié si les rôles et les autorisations sont définis. Sinon, ils peuvent renvoyer ultérieurement pour affecter le rôle.

     ![Ajouter un nouvel utilisateur](./assets/company-structure-users-add.png){width="700" zoomable="yes"}

   - Remplit les champs restants selon les besoins de l’utilisateur :

      - **[!UICONTROL First Name]** et **[!UICONTROL Last Name]**
      - **[!UICONTROL Email]**
      - **[!UICONTROL Phone Number]**

   Par défaut, le **[!UICONTROL Status]** du compte est `Active`.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

1. Répète le processus pour créer autant d’utilisateurs de l’entreprise que nécessaire.

   Les nouveaux utilisateurs apparaissent dans la liste Utilisateurs de l’entreprise , avec l’administrateur de l’entreprise.

Pour gagner du temps lors de leur première commande, l’administrateur de la société peut rappeler à chaque utilisateur de la société d’ajouter l’adresse de facturation et de livraison par défaut à son [carnet d’adresses](../customers/account-dashboard-address-book.md).

## Modifier les utilisateurs de l’entreprise

1. Depuis le storefront, l’administrateur de la société se connecte à son compte.

1. Dans le panneau de gauche, choisissez **[!UICONTROL Company Users]**.

1. Recherche l’enregistrement de l’utilisateur à mettre à jour et clique sur **[!UICONTROL Edit]**.

1. Effectue les modifications nécessaires.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

## Suppression d’un utilisateur d’entreprise

1. Depuis le storefront, l’administrateur de la société se connecte à son compte.

1. Dans le panneau de gauche, choisissez **[!UICONTROL Company Structure]**.

1. Sélectionne l’utilisateur de l’entreprise dans la structure de l’entreprise.

1. Clics **[!UICONTROL Delete Selected]**.

   ![Supprimer l’utilisateur](./assets/company-structure-delete-user.png){width="600" zoomable="yes"}

1. Lorsque vous êtes invité à confirmer l’opération, cliquez sur **[!UICONTROL Delete]**.

Dans l’administrateur, l’utilisateur de la société reste répertorié dans la grille [Customers](../customers/customers-all.md), mais avec le statut `Inactive`.

## Descriptions des champs

| Champ | Description |
|--------------|---------------|
| [!UICONTROL Job Title] | Fonction de l’utilisateur de la société. |
| [!UICONTROL User Role] | [role](account-company-roles-permissions.md) attribué à l’utilisateur de la société. Options : `Default User` / (autres rôles) |
| [!UICONTROL First Name] | Prénom de l’utilisateur de la société. |
| [!UICONTROL Last Name] | Nom de l’utilisateur de la société. |
| [!UICONTROL Email] | Adresse électronique de l’utilisateur de la société. |
| [!UICONTROL Phone Number] | Numéro de téléphone de l’utilisateur de la société. |
| [!UICONTROL Status] | État du compte utilisateur de l’entreprise. Options : `Active` / `Inactive` |

{style="table-layout:auto"}
