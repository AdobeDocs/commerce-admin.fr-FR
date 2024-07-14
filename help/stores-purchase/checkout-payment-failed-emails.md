---
title: Notification d’échec de paiement
description: Découvrez comment configurer les communications par e-mail pour un mode de paiement qui ne parvient pas à terminer une transaction.
exl-id: c64a4463-64d5-4dad-a8ad-13bfb141b65f
feature: Payments, Communications
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Notification d’échec de paiement

Une notification est envoyée au contact du magasin ou à un utilisateur administrateur désigné si le mode de paiement sélectionné lors du passage en caisse ne parvient pas à terminer la transaction.

## Etape 1 : mettre à jour le modèle d&#39;email

Veillez à avoir mis à jour le modèle d’email nécessaire pour refléter votre marque. Pour obtenir la liste complète des modèles, reportez-vous à la section [Liste de modèles d’email](../systems/email-templates.md#email-template-list).

## Etape 2 : configurer les emails en échec du paiement

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Checkout]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Payment Failed Emails]** .

   ![ Courriers électroniques en échec du paiement ](../configuration-reference/sales/assets/checkout-payment-failed-emails.png){width="600" zoomable="yes"}

1. Définissez les options de paiement des emails en échec :

   - Définissez **[!UICONTROL Payment Failed Email Sender]** sur le contact du magasin qui apparaît comme l’expéditeur du message.
   - Définissez **[!UICONTROL Payment Failed Email Receiver]** sur le contact du magasin qui doit recevoir la notification des échecs de transmission des emails.
   - Définissez **[!UICONTROL Payment Failed Template]** sur le modèle utilisé pour l’e-mail envoyé lorsque le mode de paiement échoue lors de l’extraction.

1. Pour **[!UICONTROL Send Payment Failed Email Copy To]**, saisissez l’adresse électronique de toute personne devant recevoir une copie de la notification d’échec de paiement.

   Si vous envoyez une copie à plusieurs destinataires, séparez chaque adresse par une virgule.

1. Définissez **[!UICONTROL Payment Failed Copy Method]** sur l’une des options suivantes :

   - `Bcc` - Envoie une _copie de politesse aveugle_ en incluant le destinataire dans l’en-tête du même email qui est envoyé au client. Le destinataire Cci n&#39;est pas visible par le client.
   - `Separate Email` - Envoie la copie en tant qu’email distinct.

1. Cliquez sur **[!UICONTROL Save Config]**.
