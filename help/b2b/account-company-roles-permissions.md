---
title: Rôles et autorisations de l’entreprise
description: Découvrez les rôles et les autorisations qu’un administrateur de l’entreprise peut appliquer aux utilisateurs de l’entreprise, ce qui vous permet d’accéder à différents niveaux aux informations et aux ressources de la commande.
exl-id: 9fe20d6a-2c9c-4618-a395-805d64dcf0de
feature: B2B, Companies, Roles/Permissions
role: Admin
source-git-commit: bad59798a1a6d97826dc421fe8614ef511e067bd
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# Rôles et autorisations de l’entreprise

Les rôles des utilisateurs de l’entreprise sont configurés avec différents niveaux d’autorisation pour accéder aux informations et ressources commerciales. Par défaut, l’administrateur de l’entreprise est un _super-utilisateur_ avec des autorisations complètes. La page [Accès refusé](../content-design/pages.md#access-denied) s’affiche si l’utilisateur n’est pas autorisé à accéder à la page.

![Page Rôles et autorisations avec rôle par défaut](./assets/company-roles-permissions.png){width="700" zoomable="yes"}

Le système dispose d’un rôle d’utilisateur par défaut prédéfini, que vous pouvez utiliser _en l’état_ ou modifier en fonction de vos besoins. Vous pouvez créer autant de rôles que nécessaire pour correspondre à la structure de votre entreprise et aux responsabilités organisationnelles, comme dans l’exemple suivant :

- **Utilisateur par défaut** : l’utilisateur par défaut a un accès complet aux activités liées aux ventes et aux devis, ainsi qu’un accès en lecture seule aux informations de profil et de crédit de la société.

- **Acheteur principal** : un acheteur principal peut avoir accès à toutes les ressources de ventes et de devis, ainsi qu’à des autorisations d’affichage uniquement sur le profil de l’entreprise, les informations de paiement et le crédit de l’entreprise.

- **Acheteur assistant** : un acheteur assistant peut avoir la permission de passer une commande à l’aide de l’option _Passage en caisse avec devis_ et d’afficher les commandes, devis et informations dans le profil de la société.

## Gestion des rôles et des autorisations

1. L’administrateur de la société se connecte à son compte de magasin.

1. Dans le panneau de gauche, choisissez **[!UICONTROL Roles and Permissions]**.

1. Effectue l’une des tâches suivantes.

### Création d’un rôle

1. Clics **[!UICONTROL Add New Role]**.

   ![Ajouter un nouveau rôle](./assets/company-roles-permissions-add-storefront.png){width="600" zoomable="yes"}

1. Saisissez un **[!UICONTROL Role Name]** descriptif.

1. Sous _[!UICONTROL Role Permissions]_, effectuez l’une des opérations suivantes :

   - Coche la case de chaque ressource ou activité à laquelle les utilisateurs auxquels le rôle a été attribué et à laquelle ils ont accès.

   - Sélectionne la case à cocher **[!UICONTROL All]** et efface la case à cocher de chaque ressource ou activité à laquelle les utilisateurs affectés au rôle ne sont pas autorisés à accéder.

1. Clics **[!UICONTROL Save Role]**.

1. Crée autant de rôles que nécessaire en répétant ces étapes.

### Modification d’un rôle

1. Pour que le rôle soit modifié, l’administrateur de l’entreprise clique sur **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Actions]_.

1. Apporte les modifications nécessaires aux paramètres de nom et d’autorisation.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Role]**.

### Dupliquer un rôle

1. Pour que le rôle soit dupliqué, l’administrateur de l’entreprise clique sur **[!UICONTROL Duplicate]** dans la colonne _[!UICONTROL Actions]_.

1. Apporte les modifications nécessaires aux paramètres de nom et d’autorisation.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Role]**.

### Suppression d’un rôle

1. L’administrateur de la société trouve le rôle à supprimer dans la liste des rôles.

   Seuls les rôles sans utilisateurs affectés peuvent être supprimés.

1. Cliquez sur **[!UICONTROL Delete]** dans la colonne _[!UICONTROL Actions]_.

1. Lorsque vous êtes invité à confirmer l’opération, cliquez sur **[!UICONTROL OK]**.

## Actions

| Action | Description |
|-----------| ----------- |
| [!UICONTROL Duplicate] | Crée une copie du rôle sélectionné. `- Duplicated` a été ajouté à la fin au nom du rôle en double. |
| [!UICONTROL Edit] | Modifiez le nom et/ou le jeu d’autorisations. |
| [!UICONTROL Delete] | Supprimez le rôle. Seuls les rôles sans utilisateurs affectés peuvent être supprimés. |

{style="table-layout:auto"}

## Autorisations de rôle

Les administrateurs d’entreprise peuvent mettre à jour la configuration des autorisations pour un rôle en sélectionnant [!UICONTROL Edit action], puis en sélectionnant ou en supprimant des autorisations dans la liste **Autorisations de rôle**.

![ Liste des rôles et autorisations](./assets/role-permissions-list.png){width="700" zoomable="yes"}

## Attribution d’un rôle à un utilisateur de société

Après avoir défini les rôles nécessaires, l’administrateur de l’entreprise attribue un rôle à chaque utilisateur de l’entreprise.

1. Se connecte à son compte d’entreprise en tant qu’administrateur de l’entreprise.

1. Dans le panneau de gauche, choisissez **[!UICONTROL Company Users]**.

   ![Utilisateurs de l’entreprise](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Recherche l’utilisateur dans la liste et clique sur **[!UICONTROL Edit]**.

1. Choisit le **[!UICONTROL User Role]** approprié pour l’utilisateur.

   ![Modifier l’utilisateur - choisissez un rôle d’utilisateur](./assets/company-user-assign-role.png){width="700" zoomable="yes"}

1. Clics **[!UICONTROL Save]**.
