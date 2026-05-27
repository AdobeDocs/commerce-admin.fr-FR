---
title: Rôles d’entreprise B2B et autorisations de storefront
description: Découvrez comment attribuer des rôles et des autorisations de storefront B2B aux utilisateurs de l’entreprise dans Adobe Commerce. Définissez l'accès aux ventes, commandes, devis et autres ressources.
solution: Commerce
feature: B2B, Companies, Roles/Permissions
feature-set: Commerce
role: Admin
level: Intermediate
exl-id: 9fe20d6a-2c9c-4618-a395-805d64dcf0de
source-git-commit: d3c5f0da47bfd951431213050546e865c6ab35ec
workflow-type: tm+mt
source-wordcount: '1196'
ht-degree: 1%

---

# Rôles et autorisations de l’entreprise

Vous configurez des rôles pour les utilisateurs de l&#39;entreprise avec différents niveaux d&#39;autorisation pour accéder aux informations de vente et aux ressources. Par défaut, l’administrateur ou l’administratrice d’entreprise est un *super utilisateur* avec des autorisations complètes. La page [ Accès refusé ](../content-design/pages.md#access-denied) s’affiche si l’utilisateur n’est pas autorisé à y accéder.

![Page Rôles et autorisations avec le rôle par défaut](./assets/company-roles-permissions.png){width="700" zoomable="yes"}

Le système dispose d’un rôle d’utilisateur par défaut prédéfini, que vous pouvez utiliser *en l’état* ou modifier en fonction de vos besoins. Vous pouvez créer autant de rôles que nécessaire pour faire correspondre la structure de votre entreprise et vos responsabilités organisationnelles, par exemple :

- **Utilisateur par défaut** — L&#39;utilisateur par défaut dispose d&#39;un accès complet aux activités liées aux ventes et aux devis, ainsi que d&#39;un accès en lecture seule au profil de la société et aux informations de crédit.

- **Acheteur principal** — Un acheteur principal peut avoir accès à toutes les ressources de ventes et de devis, ainsi qu&#39;aux autorisations en lecture seule du profil de l&#39;entreprise, des utilisateurs et des équipes, des informations de paiement et du crédit de l&#39;entreprise.

- **Acheteur assistant** — Un acheteur assistant peut être autorisé à passer une commande à l&#39;aide de **[!UICONTROL Checkout with quote]** et à afficher les commandes, les devis et les informations dans le profil de la société.

## Gestion des rôles et des autorisations

Gérez les rôles de l’entreprise à partir du compte storefront de l’administrateur de l’entreprise.

**Pour ouvrir Rôles et autorisations :**

1. Connectez-vous au storefront en tant qu’administrateur d’entreprise.

1. Dans le panneau de gauche, sélectionnez **[!UICONTROL Roles and Permissions]**.

1. Effectuez l’une des tâches suivantes.

### Créer un rôle

1. Cliquez sur **[!UICONTROL Add New Role]**.

   ![Ajouter un nouveau rôle](./assets/company-roles-permissions-add-storefront.png){width="600" zoomable="yes"}

1. Saisissez un **[!UICONTROL Role Name]** descriptif.

1. Sous **[!UICONTROL Role Permissions]**, effectuez l’une des opérations suivantes :

   - Cochez la case de chaque ressource ou activité à laquelle les utilisateurs affectés au rôle ont l’autorisation d’accéder.

   - Cochez la case **[!UICONTROL All]** et décochez la case de chaque ressource ou activité à laquelle les utilisateurs et utilisatrices affectés au rôle n’ont pas l’autorisation d’accéder.

1. Cliquez sur **[!UICONTROL Save Role]**.

1. Répétez ces étapes pour créer autant de rôles que nécessaire.

### Modifier un rôle

1. Recherchez le rôle à modifier et cliquez sur **[!UICONTROL Edit]** dans la colonne **[!UICONTROL Actions]** .

1. Apportez les modifications nécessaires aux paramètres de nom et d’autorisation.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Role]**.

### Dupliquer un rôle

1. Recherchez le rôle à dupliquer et cliquez sur **[!UICONTROL Duplicate]** dans la colonne **[!UICONTROL Actions]** .

1. Apportez les modifications nécessaires aux paramètres de nom et d’autorisation.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Role]**.

### Supprimer un rôle

1. Dans la liste des rôles, recherchez le rôle à supprimer.

   Seuls les rôles sans utilisateurs affectés peuvent être supprimés.

1. Cliquez sur **[!UICONTROL Delete]** dans la colonne **[!UICONTROL Actions]** .

1. Lorsque vous êtes invité à confirmer, cliquez sur **[!UICONTROL OK]**.

## Actions de liste de rôles {#actions}

| Action | Description |
| --- | --- |
| [!UICONTROL Duplicate] | Crée une copie du rôle sélectionné. Le nom du rôle en double a `- Duplicated` ajouté à la fin. |
| [!UICONTROL Edit] | Modifie le nom et le jeu d’autorisations. |
| [!UICONTROL Delete] | Supprime le rôle. Seuls les rôles sans utilisateurs affectés peuvent être supprimés. |

{style="table-layout:auto"}

## Autorisations des rôles

Les fonctionnalités B2B sont bloquées par des **autorisations** (ressources ACL). Lorsqu’un utilisateur d’entreprise ouvre une page ou exécute une action sur le storefront, l’application vérifie si son rôle inclut l’autorisation requise.

Les administrateurs et administratrices d’entreprise peuvent mettre à jour la configuration des autorisations pour un rôle en sélectionnant **[!UICONTROL Edit]**, puis en sélectionnant ou en effaçant les autorisations dans la liste de **[!UICONTROL Role Permissions]**.

![Liste des rôles et des autorisations](./assets/role-permissions-list.png){width="700" zoomable="yes"}

Affectez ces ressources lorsque vous **créez ou modifiez un rôle d’entreprise** dans le compte d’entreprise. Les utilisateurs autorisés à gérer des rôles peuvent ouvrir le formulaire de rôle et définir l’arborescence des autorisations.

Les autorisations de rôle sont organisées dans une arborescence, avec des options principales et des options subordonnées. La sélection d&#39;une option principale sélectionne automatiquement toutes les options subordonnées. L&#39;effacement d&#39;une option principale efface automatiquement toutes les options subordonnées. Vous pouvez également sélectionner ou effacer les options subordonnées individuellement.

### Toutes les autorisations

| Libellé de l’autorisation | Description |
| --- | --- |
| Tous | Nœud racine pour les autorisations **all** affectées à ce rôle de storefront. |

### Autorisations de vente

| Libellé de l’autorisation | Description |
| --- | --- |
| Ventes | Parent pour la visibilité du passage en caisse et de la commande pour les utilisateurs de l’entreprise. |
| Autoriser l’extraction | Passez des commandes au passage en caisse. |
| Utiliser la méthode de paiement en compte | Utilisez **Payer sur le compte** (crédit d’entreprise) au moment de passer en caisse lorsque cela est disponible. |
| Afficher les commandes | Affichez les commandes de l’utilisateur. |
| Afficher les commandes des utilisateurs subordonnés | Afficher les commandes passées par les utilisateurs sous cet utilisateur dans la hiérarchie. |

### Autorisations de devis

Nœud parent dans l’arborescence des autorisations de la société : **Quotes**.

| Libellé de l’autorisation | Description |
| --- | --- |
| Citations | Parent pour les actions de devis négociables du storefront. |
| Afficher (guillemets) | Afficher les devis négociables. |
| Demander, Modifier, Supprimer | Demandez de nouveaux devis, modifiez des devis et supprimez des devis en fonction des règles métier. |
| Passer en caisse avec devis | Effectuez le passage en caisse à l’aide d’un devis approuvé. |
| Gérer les devis des utilisateurs subordonnés | Parent pour les actions sur les devis des subordonnés. |
| Afficher (devis des subordonnés) | Afficher les devis des subordonnés. |
| Modifier (guillemets des subordonnés) | Modifier les citations des subordonnés. |
| Supprimer (guillemets des subordonnés) | Supprimez les guillemets des subordonnés. |

### Modèles de devis

Nœud parent : **Modèles de devis** (sous **Devis** dans l’arborescence de la société).

| Libellé de l’autorisation | Description |
| --- | --- |
| Modèles de devis | Fonctionnalités du modèle de devis parent sur le storefront. |
| Affichage (modèles) | Afficher les modèles de devis. |
| Demander, Modifier, Supprimer | Créer, mettre à jour, annuler et gérer des modèles de devis. |
| Générer des devis à partir de modèles | Générer des devis négociables à partir de modèles. |
| Gérer les modèles de devis des utilisateurs subordonnés | Parent pour les actions de modèle subordonnées. |
| Afficher (modèles des subordonnés) | Afficher les modèles de devis des subordonnés. |
| Modifier (modèles des subordonnés) | Modifier les modèles de devis des subordonnés. |
| Supprimer (modèles des subordonnés) | Supprimer les modèles de devis des subordonnés. |

### Approbations de commande

Nœud parent : **Validations de commande**. Les autorisations de commande fournisseur et de règle d’approbation sont imbriquées sous cette branche de l’arborescence.

### Commandes fournisseur

| Libellé de l’autorisation | Description |
| --- | --- |
| Approbations de commande | Parent pour les fonctions de commande fournisseur et d&#39;approbation. |
| Afficher mes commandes fournisseur | Afficher les commandes fournisseur créées par cet utilisateur. |
| Afficher pour les subordonnés | Afficher les commandes fournisseur pour les utilisateurs situés sous cet utilisateur dans la hiérarchie. |
| Afficher pour toutes les entreprises | Afficher les commandes fournisseur dans l&#39;ensemble de la société. |
| Approuver automatiquement les commandes d&#39;achat créées dans ce rôle | Approuver automatiquement les commandes fournisseur créées par les utilisateurs de ce rôle lorsque les règles le permettent. |

### Règles de bon de commande

| Libellé de l’autorisation | Description |
| --- | --- |
| Approuver les commandes fournisseur sans autre approbation | Approuver des commandes fournisseur même lorsque d&#39;autres approbations sont normalement requises (selon les règles d&#39;approbation). |
| Afficher les règles d&#39;approbation | Afficher les règles d&#39;approbation de commande fournisseur. |
| Créer, modifier et supprimer | Créer, modifier et supprimer des règles d’approbation. |

### Profil d&#39;entreprise et contacts

Autorisations de storefront pour les sections de profil d’entreprise. Les entrées imbriquées **Modifier** s’appliquent uniquement sous l’autorisation **Afficher** au-dessus d’elles dans l’arborescence des rôles.

| Libellé de l’autorisation | Description |
| --- | --- |
| Profil d&#39;entreprise | Accédez aux zones de profil de l’entreprise en tant que groupe. |
| Informations sur le compte (affichage) | Affichez les informations sur le compte de la société. |
| Modifier | Modifiez les informations du compte de la société (sous Informations du compte). |
| Adresse Légale (Vue) | Afficher l&#39;adresse légale de la société. |
| Modifier | Modifiez l&#39;adresse légale de la société (sous Adresse légale). |
| Contacts (affichage) | Afficher les contacts d’entreprise. |
| Informations de paiement (affichage) | Affichez les informations de paiement sur le profil de la société. |
| Informations d&#39;expédition (voir) | Affichez les informations d&#39;expédition sur le profil de la société. |

## Gestion des utilisateurs de l’entreprise

| Libellé de l’autorisation | Description |
| --- | --- |
| Gestion des utilisateurs de l’entreprise | Parent pour les rôles et pour les utilisateurs ou les équipes. |
| Affichage des rôles et des autorisations | Affichez les rôles de l’entreprise et leurs autorisations. |
| Gestion des rôles et des autorisations | Créez ou modifiez des rôles et attribuez des autorisations. |
| Affichage des utilisateurs et des équipes | Affichez les utilisateurs et les équipes de l’entreprise. |
| Gestion des utilisateurs et des équipes | Ajouter, modifier ou supprimer des utilisateurs et des équipes. |

## Crédit d’entreprise

| Libellé de l’autorisation | Description |
| --- | --- |
| Crédit d&#39;entreprise | Accédez à la zone de crédit de la société. |
| Afficher (historique de crédit) | Afficher l&#39;historique de crédit de la société et les informations de solde associées. |

## Attribuer un rôle à un utilisateur d’entreprise

Après avoir défini les rôles dont vous avez besoin, attribuez un rôle à chaque utilisateur de la société.

**Pour attribuer un rôle, procédez comme suit**

1. Connectez-vous au storefront en tant qu’administrateur d’entreprise.

1. Dans le panneau de gauche, sélectionnez **[!UICONTROL Company Users]**.

   ![Utilisateurs de l’entreprise](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Recherchez l’utilisateur dans la liste, puis cliquez sur **[!UICONTROL Edit]**.

1. Sélectionnez la **[!UICONTROL User Role]** appropriée pour l’utilisateur.

   ![Modifier l’utilisateur - choisir un rôle d’utilisateur](./assets/company-user-assign-role.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>- [Gérer les utilisateurs de l’entreprise](account-company-users.md)
>- [Structure de compte d’entreprise](account-company-structure.md)
>- [Rôle d’administrateur d’entreprise](account-company-admin.md)
>- [Gérer les entreprises](manage-companies.md)
>- [Activer les fonctionnalités B2B](enable-basic-features.md)
