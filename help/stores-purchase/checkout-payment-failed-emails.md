---
title: Notification d’échec de paiement
description: Découvrez comment configurer les communications par e-mail pour un mode de paiement qui ne parvient pas à effectuer une transaction.
exl-id: c64a4463-64d5-4dad-a8ad-13bfb141b65f
feature: Payments, Communications
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Notification d’échec de paiement

Une notification est envoyée au contact du magasin ou à un utilisateur administrateur désigné si le mode de paiement sélectionné lors du passage en caisse ne parvient pas à terminer la transaction.

## Étape 1 : mettre à jour le modèle d’e-mail

Assurez-vous d’avoir mis à jour le modèle d’e-mail nécessaire pour refléter votre marque. Pour obtenir la liste complète des modèles, voir [Liste de modèles d’e-mail](../systems/email-templates.md#email-template-list).

## Étape 2 : configurer les e-mails d&#39;échec de paiement

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Checkout]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Payment Failed Emails]** .

   ![E-mails en échec de paiement](../configuration-reference/sales/assets/checkout-payment-failed-emails.png){width="600" zoomable="yes"}

1. Définissez les options pour les e-mails d’échec de paiement :

   - Définissez **[!UICONTROL Payment Failed Email Sender]** sur le contact du magasin qui apparaît comme l’expéditeur du message.
   - Définissez **[!UICONTROL Payment Failed Email Receiver]** sur le contact du magasin qui doit recevoir une notification des transmissions d’e-mail ayant échoué.
   - Définissez **[!UICONTROL Payment Failed Template]** sur le modèle utilisé pour l’e-mail envoyé lorsque le mode de paiement échoue lors du passage en caisse.

1. Par **[!UICONTROL Send Payment Failed Email Copy To]**, saisissez l&#39;adresse e-mail de toute personne qui doit recevoir une copie de la notification d&#39;échec de paiement.

   Si vous envoyez une copie à plusieurs destinataires, séparez chaque adresse par une virgule.

1. Définissez **[!UICONTROL Payment Failed Copy Method]** sur l’une des options suivantes :

   - `Bcc` - Envoie une _copie de courtoisie invisible_ en incluant le destinataire dans l’en-tête du même e-mail envoyé au client. Le destinataire en Cci n’est pas visible pour le client.
   - `Separate Email` - Envoie la copie sous forme d’e-mail distinct.

1. Cliquez sur **[!UICONTROL Save Config]**.
