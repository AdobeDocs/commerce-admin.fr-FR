---
title: Invitations à des événements
description: Découvrez comment les clients peuvent envoyer et afficher des invitations à des événements et à des ventes privées à partir du tableau de bord de leurs comptes clients.
exl-id: 6a9123a0-bdb4-4cd6-99cd-658f728aa90c
feature: Promotions/Events, Communications
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%

---

# Invitations à des événements

{{ee-feature}}

Lorsque les invitations sont activées, les clients peuvent envoyer et afficher des invitations à partir du tableau de bord de leurs comptes client. L’e-mail d’invitation comprend un lien vers la page de connexion du client de votre boutique.

## Mes invitations

La section _[!UICONTROL My Invitations]_du compte client répertorie toutes les invitations envoyées par le client. Les clients peuvent envoyer des invitations à leurs amis et à leur famille pour des événements en magasin, des registres de cadeaux, des listes de souhaits, etc.

![Mes invitations](./assets/account-dashboard-my-invitations.png){width="700" zoomable="yes"}

### Workflow d’invitation

1. **Le client prépare les invitations** : depuis le tableau de bord du compte, le client prépare la liste des destinataires et complète l&#39;invitation. Selon la configuration, un message personnalisé peut être inclus.
1. **Le client envoie des invitations** : une fois prêt, le client clique sur le bouton _[!UICONTROL Send Invitations]_.
1. **Le système gère la transmission** : le système envoie les invitations par lots, en fonction du nombre défini dans la configuration.
1. **Le client surveille la réponse** : le client surveille le statut de chaque invitation à partir du tableau de bord du compte, par exemple `Sent`, `Accepted` ou `Canceled`.

### Envoyer une invitation

1. Dans la barre latérale de son compte sur le storefront, le client choisit **[!UICONTROL My Invitations]**.

1. Sur la page _Mon invitation_, clique sur **[!UICONTROL Send Invitation]**.

1. Définit le nouvel élément d&#39;invitation :

   - Complète les informations sur l’e-mail.

   - (Facultatif) Crée une invitation multi-adresses en cliquant sur **+** et en ajoutant une autre adresse e-mail.

     Une seule invitation a une limite de cinq adresses e-mail.

   - (Facultatif) Saisit un message d’accompagnement.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Send Invitation]**.

Une notification d’invitation est envoyée à l’adresse e-mail de l’utilisateur invité avec un lien d’instructions pour définir le compte.

>[!NOTE]
>
>Un utilisateur ne peut envoyer qu’une seule invitation à une adresse e-mail spécifique. Toute tentative de renvoi d’une invitation à la même adresse e-mail génère un message d’erreur qui s’affiche et l’invitation n’est pas envoyée.

## Activer les invitations pour votre boutique

La configuration des invitations active les invitations pour le magasin et détermine comment elles sont envoyées.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Invitations]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL General]** .

   ![Configuration des clients - options générales des invitations](../configuration-reference/customers/assets/invitations-general.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Enable Invitations Functionality]** sur `Yes`.

1. Pour permettre aux clients de gérer les invitations à partir du storefront, définissez **Activer les invitations sur Storefront** sur `Yes`.

1. Définissez **[!UICONTROL Referred Customer Group]** sur l’une des options suivantes :

   - `Same as Inviter`
   - `Default Customer Group from Configuration`

1. Définissez **[!UICONTROL New Accounts Registration]** sur l’une des options suivantes :

   - `By Invitation Only`
   - `Available to All`

1. Pour **[!UICONTROL Allow Customers to Add Custom Message to Invitation Email]**, sélectionnez `Yes`.

1. Pour limiter le nombre d&#39;invitations pouvant être envoyées simultanément, saisissez le nombre dans le champ **[!UICONTROL Max Invitations Allowed to be Sent at One Time]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Email]** et procédez comme suit :

   ![Configuration des clients - options d’e-mail des invitations](../configuration-reference/customers/assets/invitations-email.png){width="600" zoomable="yes"}

   - Sélectionnez l’identité du magasin à utiliser comme **[!UICONTROL Customer Invitation Email Sender]**.

   - Sélectionnez le **[!UICONTROL Customer Invitation Email Template]** utilisé pour les invitations envoyées.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Envoyer et gérer des invitations dans l’administration

Dans la section [Rapports des ventes privées](../getting-started/private-sales-reports.md), vous pouvez voir le nombre d&#39;invitations envoyées au cours d&#39;une période spécifiée ou le nombre de clients auxquels vous avez envoyé des invitations.

### Créer une invitation dans l&#39;Admin

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Invitations]**.

1. Dans l’écran suivant, saisissez les adresses e-mail pour inviter de nouveaux clients, ajoutez un message personnalisé, choisissez un expéditeur et sélectionnez un groupe d’invités.

   Si vous disposez de plusieurs vues de magasin, utilisez l’option **[!UICONTROL Send From]** pour spécifier la vue de magasin à partir de laquelle une invitation est envoyée.

   ![Informations sur les invitations](./assets/create-invitation-page.png){width="700" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save]**.

### Ignorer les invitations pour une seule entité

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Recherchez l’invitation nécessaire à l’aide de filtres et ouvrez-la en mode d’édition.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Discard Invitation]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

### Ignorer les invitations pour plusieurs entités

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Recherchez et sélectionnez les invitations à ignorer.

1. Dans le coin supérieur gauche, utilisez le menu **[!UICONTROL Actions]** pour choisir **[!UICONTROL Discard Selected]** et cliquez sur **[!UICONTROL Submit]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

### Descriptions des champs

| Champ | Description |
|--- |--- |
| [!UICONTROL Select] | Cochez la case pour sélectionner les invitations à faire l’objet d’une action ou utilisez le contrôle de sélection dans l’en-tête de colonne. Options : `Select All` /` Deselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL ID] | Numéro d&#39;identification interne d&#39;une invitation |
| [!UICONTROL Email] | Adresse e-mail du client correspondant |
| [!UICONTROL Invitee] | E-mail de l’utilisateur invité |
| [!UICONTROL Sent] | Date et heure auxquelles une invitation a été envoyée |
| [!UICONTROL Registered] | Heure et données d’enregistrement d’un client |
| [!UICONTROL Status] | Statut de l&#39;invitation. Options : `Sent` / `Not Sent` / `Accepted` / `Discarded` |
| [!UICONTROL Valid Website] | Le site Web correspondant |
| [!UICONTROL Invitee Group] | Groupe de clients d’un invité |

{style="table-layout:auto"}
