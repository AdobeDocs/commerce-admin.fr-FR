---
title: Invitations d’événement
description: Découvrez comment les clients peuvent envoyer et afficher des invitations à des événements et des ventes privées depuis le tableau de bord de leurs comptes clients.
exl-id: 6a9123a0-bdb4-4cd6-99cd-658f728aa90c
feature: Promotions/Events, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# Invitations d’événement

{{ee-feature}}

Lorsque les invitations sont activées, les clients peuvent envoyer et afficher des invitations à partir du tableau de bord de leurs comptes clients. Le courrier électronique d’invitation comprend un lien vers la page de connexion de votre magasin.

## Mes invitations

La section _[!UICONTROL My Invitations]_&#x200B;du compte client répertorie toutes les invitations envoyées par le client. Les clients peuvent envoyer des invitations à leurs amis et à leur famille pour des événements de magasin, des registres de cadeaux, des listes de souhaits, etc.

![Mes invitations](./assets/account-dashboard-my-invitations.png){width="700" zoomable="yes"}

### Processus d’invitation

1. **Le client prépare les invitations** : dans le tableau de bord du compte, le client prépare la liste des destinataires et complète l’invitation. Un message personnalisé peut être inclus, selon la configuration.
1. **Le client envoie des invitations** : une fois prêt, le client clique sur le bouton _[!UICONTROL Send Invitations]_.
1. **Le système gère la transmission** : le système envoie les invitations par lots, en fonction du nombre défini dans la configuration.
1. **Le client surveille la réponse** : le client surveille l’état de chaque invitation depuis le tableau de bord du compte, comme `Sent`, `Accepted` ou `Canceled`.

### Envoyer une invitation

1. Dans la barre latérale de leur compte sur le storefront, le client choisit **[!UICONTROL My Invitations]**.

1. Sur la page _My Invitation_, cliquez sur **[!UICONTROL Send Invitation]**.

1. Définit le nouvel élément d’invitation :

   - Complète les informations du courrier électronique.

   - (Facultatif) Crée une invitation à plusieurs adresses en cliquant sur **+** et en ajoutant une autre adresse électronique.

     Une seule invitation est limitée à cinq adresses électroniques.

   - (Facultatif) Saisissez un message d’accompagnement.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Send Invitation]**.

Une notification d’invitation est envoyée à l’adresse électronique de l’utilisateur invité avec un lien d’instructions pour définir le compte.

>[!NOTE]
>
>Un utilisateur ne peut envoyer qu’une seule invitation à une adresse électronique spécifique. Si vous essayez de renvoyer une invitation à la même adresse électronique, un message d’erreur s’affiche et l’invitation n’est pas envoyée.

## Activation des invitations pour votre boutique

La configuration des invitations active les invitations pour le magasin et détermine la manière dont elles sont envoyées.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Invitations]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL General]** .

   ![Configuration des clients - options générales des invitations](../configuration-reference/customers/assets/invitations-general.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Enable Invitations Functionality]** sur `Yes`.

1. Pour permettre aux clients de gérer les invitations depuis le storefront, définissez **Activer les invitations sur le storefront** sur `Yes`.

1. Définissez **[!UICONTROL Referred Customer Group]** sur l’une des options suivantes :

   - `Same as Inviter`
   - `Default Customer Group from Configuration`

1. Définissez **[!UICONTROL New Accounts Registration]** sur l’une des options suivantes :

   - `By Invitation Only`
   - `Available to All`

1. Pour **[!UICONTROL Allow Customers to Add Custom Message to Invitation Email]**, sélectionnez `Yes`.

1. Pour limiter le nombre d’invitations qui peuvent être envoyées simultanément, saisissez le nombre dans le champ **[!UICONTROL Max Invitations Allowed to be Sent at One Time]** .

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) de **[!UICONTROL Email]** et procédez comme suit :

   ![Configuration des clients - options d’email d’invitations](../configuration-reference/customers/assets/invitations-email.png){width="600" zoomable="yes"}

   - Sélectionnez l’identité du magasin à utiliser comme **[!UICONTROL Customer Invitation Email Sender]**.

   - Sélectionnez le **[!UICONTROL Customer Invitation Email Template]** utilisé pour les invitations envoyées.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

## Envoyer et gérer les invitations dans l’administrateur

Dans la section [Rapports sur les ventes privées](../getting-started/private-sales-reports.md) , vous pouvez voir le nombre d’invitations envoyées au cours d’une période spécifiée ou les clients auxquels vous avez envoyé des invitations.

### Création d’une invitation dans Admin

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Invitations]**.

1. Dans l’écran suivant, saisissez des adresses électroniques pour inviter de nouveaux clients, ajoutez un message personnalisé, choisissez un expéditeur et sélectionnez un groupe d’invités.

   Si vous avez plusieurs vues de magasin, utilisez l’option **[!UICONTROL Send From]** pour spécifier la vue de magasin à partir de laquelle une invitation est envoyée.

   ![Informations sur les invitations](./assets/create-invitation-page.png){width="700" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

### Ignorer les invitations pour une seule entité

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Recherchez l’invitation nécessaire à l’aide de filtres et ouvrez-la en mode d’édition.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Discard Invitation]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

### Ignorer les invitations pour plusieurs entités

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Recherchez et sélectionnez les invitations à ignorer.

1. Dans la partie supérieure gauche, utilisez le menu **[!UICONTROL Actions]** pour choisir **[!UICONTROL Discard Selected]** et cliquez sur **[!UICONTROL Submit]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

### Descriptions des champs

| Champ | Description |
|--- |--- |
| [!UICONTROL Select] | Cochez la case pour sélectionner les invitations à soumettre à une action ou utilisez le contrôle de sélection dans l’en-tête de colonne. Options : `Select All` /` Deselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL ID] | Numéro d’identifiant interne d’une invitation. |
| [!UICONTROL Email] | Adresse électronique du client correspondante |
| [!UICONTROL Invitee] | Adresse électronique de l’utilisateur invité |
| [!UICONTROL Sent] | Heure et date d’envoi d’une invitation |
| [!UICONTROL Registered] | Heure et données de l’enregistrement d’un client |
| [!UICONTROL Status] | État de l’invitation. Options : `Sent` / `Not Sent` / `Accepted` / `Discarded` |
| [!UICONTROL Valid Website] | Le site web correspondant |
| [!UICONTROL Invitee Group] | Groupe de clients d’un invité |

{style="table-layout:auto"}
