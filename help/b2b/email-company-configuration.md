---
title: Configuration des courriers électroniques de l’entreprise
description: Découvrez les options et les modèles d’email utilisés pour envoyer des communications pour les comptes d’entreprise.
exl-id: fd61c0c6-0887-4ff2-8002-906ff615bad9
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 0%

---

# Configuration des options de courrier électronique de l’entreprise

Le [représentant commercial](account-company-manage.md) qui est affecté comme contact principal pour une entreprise est configuré par défaut comme l’expéditeur de nombreux messages électroniques automatisés envoyés à la société.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Company Configuration]**.

1. Si nécessaire, définissez **[!UICONTROL Store View]** sur la vue de magasin pour définir la [portée](../getting-started/websites-stores-views.md#scope-settings) de la configuration.

1. Renseignez la section **[!UICONTROL Company Registration]** :

   >[!NOTE]
   >
   >Décochez la case **[!UICONTROL Use system value]** pour rendre le champ modifiable.

   - Définissez **[!UICONTROL Company Registration Email Recipient]** sur le [contact du magasin](../getting-started/store-details.md#store-email-addresses) qui doit être averti lorsqu’une nouvelle demande d’enregistrement de la société est reçue.

   - Dans le champ **[!UICONTROL Send Company Registration Email Copy To]** , saisissez l’adresse électronique de chaque personne devant recevoir une copie de la notification d’enregistrement. Séparez plusieurs adresses électroniques par une virgule.

   - Pour déterminer comment la copie de la notification est envoyée, définissez **[!UICONTROL Send Email Copy Method]** sur l’une des options suivantes :

      - `Bcc` - Envoie une _copie de politesse aveugle_ en incluant le destinataire dans l’en-tête du même email qui est envoyé au client. Le destinataire Cci n&#39;est pas visible par le client.
      - `Separate Email` - Envoie la copie en tant qu’email distinct.

   - Si vous avez préparé un modèle d’email qui doit être utilisé à la place de la valeur par défaut, définissez **[!UICONTROL Default Company Registration Email]** sur le nom du modèle. Par défaut, le modèle `Company Registration Request` est utilisé.

     ![Configuration des clients - enregistrement de la société](./assets/company-email-options-company-registration.png){width="600" zoomable="yes"}

1. Renseignez la section **[!UICONTROL Customer-Related Emails]** :

   Si vous avez préparé d’autres modèles d’email à utiliser à la place des valeurs par défaut, choisissez le modèle que vous souhaitez utiliser pour chacun des éléments suivants :

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![Configuration des clients - emails liés aux clients](./assets/company-email-options-customer-related-emails.png){width="600" zoomable="yes"}

1. Renseignez la section **[!UICONTROL Company Status Change]** :

   - Définissez **[!UICONTROL Company Status Change for Email Recipient]** sur le [contact de magasin](../getting-started/store-details.md#store-email-addresses) qui doit être averti lorsque l’état d’une entreprise change.

   - Dans le champ **[!UICONTROL Send Company Status Change Email Copy To]** , saisissez l’adresse électronique de chaque personne devant recevoir une copie de la notification de changement d’état. Séparez plusieurs adresses électroniques par une virgule.

   - Pour déterminer comment la copie de la notification est envoyée, définissez **[!UICONTROL Send Email Copy Method]** sur l’une des options suivantes :

      - `Bcc` - Envoie une _copie de politesse aveugle_ en incluant le destinataire dans l’en-tête du même email qui est envoyé au client. Le destinataire Cci n&#39;est pas visible par le client.
      - `Separate Email` - Envoie la copie en tant qu’email distinct.

   - Si vous disposez d’un modèle de courrier électronique préparé à utiliser au lieu de la valeur par défaut lorsque l’état de l’entreprise passe de `Pending Approval` à `Active`, définissez **[!UICONTROL Default 'Company Status Change to Active 1' Email]** sur ce modèle. Par défaut, le modèle `Company Status Active 1` est utilisé.

   - Si vous disposez d’un modèle de courrier électronique préparé à utiliser au lieu de la valeur par défaut lorsque l’état de l’entreprise passe de `Rejected` ou `Blocked` à `Active`, définissez **[!UICONTROL Default 'Company Status Change to Active 2' Email]** sur ce modèle. Par défaut, le modèle `Company Status Active 2` est utilisé.

   - Si vous disposez d’un modèle de courrier électronique préparé à utiliser au lieu de la valeur par défaut lorsque l’état de l’entreprise passe à `Rejected`, définissez **[!UICONTROL Default 'Company Status Change to Rejected' Email]** sur ce modèle. Par défaut, le modèle `Company Status Rejected` est utilisé.

   - Si vous disposez d’un modèle de courrier électronique préparé à utiliser au lieu de la valeur par défaut lorsque l’état de l’entreprise passe à `Blocked`, définissez **[!UICONTROL Default 'Company Status Change to Blocked' Email]** sur ce modèle. Par défaut, le modèle `Company Status Blocked` est utilisé.

   - Si vous disposez d’un modèle de courrier électronique préparé à utiliser au lieu de la valeur par défaut lorsque l’état de l’entreprise passe à `Pending Approval`, définissez **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** sur ce modèle. Par défaut, le modèle `Company Status Pending Approval` est utilisé.

     ![Configuration des clients - changement d’état de la société](./assets/company-email-options-company-status-change.png){width="600" zoomable="yes"}

1. Renseignez la section **[!UICONTROL Company Credit Emails]** :

   - Définissez **[!UICONTROL Company Credit Change Email Sender]** sur le [contact de magasin](../getting-started/store-details.md#store-email-addresses) qui doit être averti lorsqu’une modification est apportée à la limite de crédit affectée à une entreprise. Par défaut, la notification est envoyée à _Représentant commercial_.

   - Dans le champ **[!UICONTROL Send Company Credit Change Email Copy To]** , saisissez l’adresse électronique de chaque personne devant recevoir une copie de la notification de changement de crédit. Séparez plusieurs adresses électroniques par une virgule.

   - Pour déterminer comment la copie de la notification est envoyée, définissez **[!UICONTROL Send Email Copy Method]** sur l’une des options suivantes :

      - `Bcc` - Envoie une _copie de politesse aveugle_ en incluant le destinataire dans l’en-tête du même email qui est envoyé au client. Le destinataire Cci n&#39;est pas visible par le client.
      - `Separate Email` - Envoie la copie en tant qu’email distinct.

   - Si vous avez préparé des modèles d’email à utiliser à la place des valeurs par défaut, choisissez le modèle de chacune des notifications suivantes envoyées à l’administrateur de l’entreprise.

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![Configuration des clients - courriers électroniques de crédit de l’entreprise](./assets/company-email-options-company-credit.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
