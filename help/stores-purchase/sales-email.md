---
title: E-mails de vente
description: Découvrez comment configurer les e-mails de vente pour prendre en charge les communications destinées aux clients concernant leurs commandes.
exl-id: b205dc61-08cc-4783-810c-686ccf2ba300
feature: Communications, Orders
TQID: https://experienceleague.adobe.com/M9-GhmO0XeRC9sgZmQXpv759NN-5cM92Bd8ZxxM96yg
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 436
ht-degree: 0%

---

# E-mails de vente

Plusieurs e-mails sont déclenchés par les événements liés à une commande. La configuration est similaire. Assurez-vous d’identifier le contact du magasin qui apparaît comme l’expéditeur du message, le modèle d’e-mail à utiliser et toute autre personne qui doit recevoir une copie du message. Les e-mails de ventes peuvent être envoyés lorsqu’ils sont déclenchés par un événement ou par un intervalle prédéterminé.

![Configuration des ventes - e-mails de vente](./assets/config-sales-sales-email-full.png){width="600" zoomable="yes"}

## Étape 1. Mettre à jour les modèles d’e-mail

Veillez à mettre à jour le modèle [en-tête d’e-mail](../systems/email-template-custom.md#header-template) afin qu’il reflète votre marque et les autres modèles d’e-mail si nécessaire. Pour obtenir la liste complète des modèles, voir [ Modèles d’e-mail ](../systems/email-templates.md).

## Étape 2. Choisir le type de transmission

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales Emails]**.

1. Si nécessaire, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) dans la section **[!UICONTROL General Settings]** .

   ![Configuration des ventes - Paramètres généraux des e-mails de ventes](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   Par défaut, l’envoi asynchrone est défini sur `Disable`. Pour modifier le paramètre système, désélectionnez la case **[!UICONTROL Use system value]** et définissez **[!UICONTROL Asynchronous sending]** sur l’une des options suivantes :

   - `Disable` - Envoie un e-mail de vente lorsqu’il est déclenché par un événement.
   - `Enable` - Envoie un e-mail de vente à intervalles réguliers prédéterminés.

   La prise en charge d’Adobe Commerce recommande d’activer l’envoi asynchrone pour améliorer les performances du placement des commandes. Voir [ Bonnes pratiques de configuration pour le traitement des commandes ](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/maintenance/order-processing-configuration.html) dans la base de connaissances du support Adobe Commerce.

## Étape 3. Complétez les détails de chaque e-mail de vente

1. Si nécessaire, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) dans la section **[!UICONTROL Order]** .

   ![Configuration des ventes - Commande d’e-mails de vente](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. Vérifiez que **[!UICONTROL Enabled]** est défini sur `Yes` (par défaut).

1. Définissez **[!UICONTROL New Order Confirmation Email]** sur le contact du magasin qui apparaît comme l’expéditeur du message.

1. Définissez **[!UICONTROL New Order Confirmation Template]** sur le modèle utilisé pour l’e-mail envoyé aux clients enregistrés.

1. Définissez **[!UICONTROL New Order Confirmation Template for Guest]** sur le modèle utilisé pour l’e-mail envoyé aux invités qui n’ont pas de compte dans votre boutique.

1. Par **[!UICONTROL Send Order Email Copy To]**, saisissez l’adresse e-mail de toute personne qui doit recevoir une copie de l’e-mail de nouvelle commande.

   Si vous envoyez une copie à plusieurs destinataires, séparez chaque adresse par une virgule.

1. Définissez **[!UICONTROL Send Order Email Copy Method]** sur l’une des options suivantes :

   - `Bcc` - Envoie une _copie de courtoisie invisible_ en incluant le destinataire dans l’en-tête du même e-mail envoyé au client. Le destinataire en Cci n’est pas visible pour le client.
   - `Separate Email` - Envoie la copie sous forme d’e-mail distinct.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Order Comments]** et répétez ces étapes.

   ![Configuration des ventes - Commentaires de commande des e-mails de ventes](../configuration-reference/sales/assets/sales-emails-order-comments.png){width="600" zoomable="yes"}

1. Effectuez la configuration pour les types d’e-mail de vente restants :

   - **[!UICONTROL Invoice]** / **[!UICONTROL Invoice Comments]**
   - **[!UICONTROL Shipment]** / **[!UICONTROL Shipment Comments]**
   - **[!UICONTROL Credit Memo]** / **[!UICONTROL Credit Memo Comments]**

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

   Lorsque vous y êtes invité, cliquez sur le lien [Gestion du cache](../systems/cache-management.md) dans le message en haut de l’espace de travail et effacez tous les caches non valides.
