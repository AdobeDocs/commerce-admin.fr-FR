---
title: Ajout d’utilisateurs à un compte d’entreprise
description: Découvrez comment ajouter un client existant à un compte d’entreprise.
exl-id: ee2f9c27-37d6-4997-8285-1c4c84f8d04c
feature: B2B, Companies, Customers
role: Admin, User
source-git-commit: 99285b700b91e0072340a2231c39a8050818fd17
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 0%

---

# Ajout d’utilisateurs à un compte d’entreprise

Lorsqu’il est activé dans la configuration, l’administrateur de l’entreprise ajoute et gère les utilisateurs de l’entreprise à partir du storefront. Cependant, les comptes utilisateurs de l’entreprise peuvent également être ajoutés et gérés à partir de l’administrateur.

Si nécessaire, vous pouvez affecter un utilisateur à plusieurs entreprises. Par exemple, si les acheteurs B2B prennent en charge plusieurs entreprises, vous pouvez ajouter leurs comptes d’utilisateurs à toutes les entreprises avec lesquelles ils font affaire. Sur le storefront, les acheteurs affectés à plusieurs entreprises peuvent basculer entre les comptes d’entreprise en sélectionnant dans le menu *[!UICONTROL Company]* des entreprises disponibles.

![Associer à la société](./assets/company-assign-multi-switcher.png){width="700"}

>[!NOTE]
>
>Si une personne possède déjà un compte personnel dans votre boutique et qu’elle se rend ensuite au travail pour une entreprise, n’attribuez pas son compte personnel à la société. Créez plutôt un compte utilisateur de société pour la personne qui possède une adresse électronique de société.

## Ajout d’un utilisateur d’entreprise

Lorsque vous ajoutez un utilisateur de société, la première société que vous associez au compte utilisateur est la société par défaut.

1. Dans la barre latérale Admin, accédez à **[!UICONTROL Customers > All Customers]**.

1. Cliquez sur **[!UICONTROL Add new customer]**.

1. Configurez le nouveau compte.

   1. Spécifiez l’état initial du compte en définissant le bouton d’activation/désactivation **[!UICONTROL Customer Active]**.

      Activez-la pour activer immédiatement le compte ou désactivez-la pour créer un compte inactif.

   1. Sélectionnez la portée du site web dans la liste **[!UICONTROL Associate to Website]**.

   1. Cliquez sur **[!UICONTROL Associate to Company]** pour afficher les sociétés disponibles.

      ![Associer à la société](./assets/company-assign-customer-account.png){width="675"}

      Si nécessaire, filtrez la liste en saisissant les premières lettres du nom de l’entreprise dans la zone de saisie.

   1. Dans la liste, sélectionnez une ou plusieurs entreprises auxquelles vous souhaitez affecter le client, puis cliquez sur **[!UICONTROL Done]**.

      Les utilisateurs de l’entreprise sont automatiquement ajoutés au groupe de clients (ou [catalogue partagé](catalog-shared.md)) pour chaque société associée à leur compte.

   1. Saisissez les informations de compte utilisateur requises : **[!UICONTROL First Name]**, **[!UICONTROL Last Name]** et **[!UICONTROL Email]**.

   1. Autoriser les représentants commerciaux à se connecter au storefront au nom du client en activant **[!UICONTROL Allow remote shopping assistance]**.

   1. Appliquez les modifications en cliquant sur **[!UICONTROL Save Customer]**.

      ![Grille client avec affectations de société](./assets/company-assign-user-assignments.png){width="675"}

[!UICONTROL Customers grid] affiche une ligne distincte pour chaque entreprise à laquelle l’utilisateur est affecté. Les colonnes suivantes sont mises à jour.

- La colonne _[!UICONTROL Customer Type]_se met à jour pour afficher le rôle attribué à l’utilisateur.

  S’il s’agit de la première fois que le client est assigné à une entreprise, la colonne _[!UICONTROL Customer Type]_est mise à jour de_[!UICONTROL Individual user]_ vers _[!UICONTROL Company User]_.

- La colonne _[!UICONTROL Group]_change le nom du groupe de clients (ou du catalogue partagé) affecté à la société.

- La colonne _[!UICONTROL Company]_affiche le nom de la société à laquelle le profil client est désormais associé.

## Affectation d’un utilisateur à un ou plusieurs comptes d’entreprise

Lorsque vous affectez un nouvel utilisateur, la première société que vous associez au compte utilisateur est la société par défaut.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Recherchez le client dans la grille et cliquez sur **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_.

1. Dans le panneau de gauche, choisissez **[!UICONTROL Account Information]**.

1. Dans la liste **[!UICONTROL Associate to Company]**, sélectionnez une ou plusieurs entreprises à affecter à l’utilisateur de la société et cliquez sur **[!UICONTROL Done]**.

1. Appliquez les modifications en cliquant sur **[!UICONTROL Save Customer]**.

## Suppression d’une affectation de société d’un compte d’utilisateur

La suppression d’une société d’un profil d’utilisateur révoque l’accès de l’utilisateur à cette société. Les données utilisateur restent accessibles dans l’administrateur. Si vous supprimez toutes les affectations d’entreprise, le _[!UICONTROL Customer Type]_se transforme en *[!UICONTROL Individual user]*désactivant les fonctionnalités B2B du compte.

1. Dans la grille Client de l’Admin, modifiez le profil client à mettre à jour.

1. Dans la section *[!UICONTROL Account Information] , supprimez une société affectée du champ **[!UICONTROL Associate to Company]** en cliquant sur le **[!UICONTROL X]** dans le libellé du nom de la société.

1. Appliquez les modifications en cliquant sur **[!UICONTROL Save Customer]**.

>[!NOTE]
>
>Si un utilisateur de la société est désigné comme administrateur de la société, vous ne pouvez pas associer cet utilisateur à l’entreprise tant que vous n’avez pas mis à jour le compte de la société pour affecter un nouvel administrateur de société.
