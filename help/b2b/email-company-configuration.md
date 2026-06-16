---
title: Configurer l’e-mail de la société
description: Découvrez les options et les modèles d’e-mail utilisés pour envoyer des communications pour les comptes d’entreprise.
exl-id: fd61c0c6-0887-4ff2-8002-906ff615bad9
feature: B2B, Companies, Configuration
role: Admin
TQID: https://experienceleague.adobe.com/MeNTcQzgfeH-DJ3TVQ-655Okr-Qt5Lv97pGZJ-67sxQ
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 676
ht-degree: 0%

---

# Configurer les options d’e-mail de la société

Le [commercial](account-company-manage.md) qui est affecté en tant que contact principal pour une entreprise est configuré par défaut comme expéditeur de nombreux e-mails automatisés envoyés à l’entreprise.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Company Configuration]**.

1. Si nécessaire, définissez **[!UICONTROL Store View]** à la vue du magasin pour définir la [ portée ](../getting-started/websites-stores-views.md#scope-settings) de la configuration.

1. Renseignez la section **[!UICONTROL Company Registration]** :

   >[!NOTE]
   >
   >Décochez la case **[!UICONTROL Use system value]** pour rendre le champ modifiable.

   - Définissez la **[!UICONTROL Company Registration Email Recipient]** sur le [contact du magasin](../getting-started/store-details.md#store-email-addresses) qui doit être averti lorsqu’une nouvelle demande d’enregistrement d’entreprise est reçue.

   - Dans le champ **[!UICONTROL Send Company Registration Email Copy To]** , saisissez l&#39;adresse e-mail de chaque personne qui doit recevoir une copie de la notification d&#39;enregistrement. Séparez plusieurs adresses e-mail par une virgule.

   - Pour déterminer comment la copie de la notification est envoyée, définissez **[!UICONTROL Send Email Copy Method]** sur l’une des options suivantes :

      - `Bcc` - Envoie une _copie de courtoisie invisible_ en incluant le destinataire dans l’en-tête du même e-mail envoyé au client. Le destinataire en Cci n’est pas visible pour le client.
      - `Separate Email` - Envoie la copie sous forme d’e-mail distinct.

   - Si vous avez préparé un modèle d’e-mail à utiliser à la place du modèle par défaut, définissez **[!UICONTROL Default Company Registration Email]** sur le nom du modèle. Par défaut, le modèle de `Company Registration Request` est utilisé.

     ![Configuration des clients - enregistrement de la société](./assets/company-email-options-company-registration.png){width="600" zoomable="yes"}

1. Renseignez la section **[!UICONTROL Customer-Related Emails]** :

   Si vous avez préparé d’autres modèles d’e-mail à utiliser au lieu des valeurs par défaut, choisissez le modèle à utiliser pour chacun des éléments suivants :

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![Configuration des clients - e-mails liés au client](./assets/company-email-options-customer-related-emails.png){width="600" zoomable="yes"}

1. Renseignez la section **[!UICONTROL Company Status Change]** :

   - Définissez **[!UICONTROL Company Status Change for Email Recipient]** sur le [contact du magasin](../getting-started/store-details.md#store-email-addresses) qui doit être averti lorsque le statut d’une société change.

   - Dans le champ **[!UICONTROL Send Company Status Change Email Copy To]** , saisissez l&#39;adresse e-mail de chaque personne qui doit recevoir une copie de la notification de changement de statut. Séparez plusieurs adresses e-mail par une virgule.

   - Pour déterminer comment la copie de la notification est envoyée, définissez **[!UICONTROL Send Email Copy Method]** sur l’une des options suivantes :

      - `Bcc` - Envoie une _copie de courtoisie invisible_ en incluant le destinataire dans l’en-tête du même e-mail envoyé au client. Le destinataire en Cci n’est pas visible pour le client.
      - `Separate Email` - Envoie la copie sous forme d’e-mail distinct.

   - Si vous disposez d’un modèle d’e-mail préparé à utiliser au lieu de la valeur par défaut lorsque le statut de l’entreprise passe de `Pending Approval` à `Active`, définissez **[!UICONTROL Default 'Company Status Change to Active 1' Email]** sur ce modèle. Par défaut, le modèle de `Company Status Active 1` est utilisé.

   - Si vous disposez d’un modèle d’e-mail préparé à utiliser au lieu de la valeur par défaut lorsque le statut de l’entreprise passe de `Rejected` ou `Blocked` à `Active`, définissez **[!UICONTROL Default 'Company Status Change to Active 2' Email]** sur ce modèle. Par défaut, le modèle de `Company Status Active 2` est utilisé.

   - Si vous disposez d’un modèle d’e-mail préparé à utiliser au lieu de la valeur par défaut lorsque le statut de l’entreprise passe à `Rejected`, définissez **[!UICONTROL Default 'Company Status Change to Rejected' Email]** sur ce modèle. Par défaut, le modèle de `Company Status Rejected` est utilisé.

   - Si vous disposez d’un modèle d’e-mail préparé à utiliser au lieu de la valeur par défaut lorsque le statut de l’entreprise passe à `Blocked`, définissez **[!UICONTROL Default 'Company Status Change to Blocked' Email]** sur ce modèle. Par défaut, le modèle de `Company Status Blocked` est utilisé.

   - Si vous disposez d’un modèle d’e-mail préparé à utiliser au lieu de la valeur par défaut lorsque le statut de l’entreprise passe à `Pending Approval`, définissez **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** sur ce modèle. Par défaut, le modèle de `Company Status Pending Approval` est utilisé.

     ![Configuration des clients - changement du statut de la société](./assets/company-email-options-company-status-change.png){width="600" zoomable="yes"}

1. Renseignez la section **[!UICONTROL Company Credit Emails]** :

   - Définissez **[!UICONTROL Company Credit Change Email Sender]** sur le [contact du magasin](../getting-started/store-details.md#store-email-addresses) qui doit être averti lorsqu’une modification est apportée à la limite de crédit affectée à une société. Par défaut, la notification est envoyée au _représentant commercial_.

   - Dans le champ **[!UICONTROL Send Company Credit Change Email Copy To]** , saisissez l&#39;adresse e-mail de chaque personne qui doit recevoir une copie de la notification de modification de crédit. Séparez plusieurs adresses e-mail par une virgule.

   - Pour déterminer comment la copie de la notification est envoyée, définissez **[!UICONTROL Send Email Copy Method]** sur l’une des options suivantes :

      - `Bcc` - Envoie une _copie de courtoisie invisible_ en incluant le destinataire dans l’en-tête du même e-mail envoyé au client. Le destinataire en Cci n’est pas visible pour le client.
      - `Separate Email` - Envoie la copie sous forme d’e-mail distinct.

   - Si vous avez préparé des modèles d’e-mail à utiliser à la place des valeurs par défaut, choisissez le modèle pour chacune des notifications suivantes envoyées à l’administrateur de la société.

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![Configuration des clients - e-mails de crédit d’entreprise](./assets/company-email-options-company-credit.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
