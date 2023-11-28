---
title: Ajout de clients à un compte d’entreprise
description: Découvrez comment ajouter un client existant à un compte d’entreprise.
exl-id: ee2f9c27-37d6-4997-8285-1c4c84f8d04c
feature: B2B, Companies, Customers
role: Admin, User
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# Ajout de clients à un compte d’entreprise

Lorsqu’il est activé dans la configuration, l’administrateur de l’entreprise ajoute des utilisateurs à l’entreprise. Cependant, l’affectation d’entreprise d’un profil client peut également être effectuée ou modifiée à partir de l’administrateur.

>[!NOTE]
>
>Si une personne possède déjà un compte personnel dans votre boutique et qu’elle se rend ensuite au travail pour une entreprise, n’attribuez pas son compte personnel à la société. Créez plutôt un compte utilisateur de société pour la personne qui possède une adresse électronique de société.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Recherchez le client dans la grille, puis cliquez sur **[!UICONTROL Edit]** dans le _[!UICONTROL Action]_colonne .

1. Dans le panneau de gauche, choisissez **[!UICONTROL Account Information]**.

1. Cliquez sur **[!UICONTROL Associate to Company]** et saisissez les premières lettres du nom de la société dans la zone de saisie.

   Le système génère une liste de toutes les correspondances possibles.

   ![Associer à la société](./assets/company-assign-customer-account.png){width="600"}

1. Dans la liste, sélectionnez la société à laquelle vous souhaitez affecter le client, puis cliquez sur **[!UICONTROL Done]**.

1. Si le client a déjà été affecté à une autre société, cliquez sur **[!UICONTROL Confirm]**.

   Le client est réaffecté au groupe de clients (ou [catalogue partagé](catalog-shared.md)) de la société et ajouté à ses [structure de l&#39;entreprise](account-company-structure.md).

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Customer]**.

   Les colonnes suivantes sont mises à jour dans la variable [Clients](../customers/customers-all.md) grid :

   - La variable _[!UICONTROL Group]_change le nom du groupe de clients (ou du catalogue partagé) affecté à la société.
   - La variable _[!UICONTROL Company]_affiche le nom de la société à laquelle le profil client est désormais associé.
