---
title: Configurer les registres de cadeaux
description: Découvrez comment activer les registres de cadeaux et configurer les notifications par e-mail associées.
exl-id: 48193621-731d-4640-8ea8-5b201915cdf1
feature: Gift, Storefront, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---

# Configurer les registres de cadeaux

{{ee-feature}}

Avant de pouvoir proposer des registres cadeaux à vos clients, vous devez activer les registres cadeaux et configurer les notifications par e-mail associées. Adobe Commerce envoie les notifications par e-mail suivantes en réponse aux événements du workflow du registre des cadeaux.

- Lorsqu&#39;un nouveau registre des cadeaux est créé, un e-mail est envoyé au propriétaire avec un lien vers le registre qui peut être partagé.
- En option, le magasin peut envoyer une notification avec un lien vers le registre des cadeaux aux amis et à la famille du propriétaire du registre des cadeaux.
- Le propriétaire est avisé lorsque des articles sont achetés dans le registre des cadeaux, mais n&#39;indique pas l&#39;acheteur.

Adobe Commerce dispose de modèles prédéfinis pour chacun de ces e-mails, qui peuvent être personnalisés pour votre marque.

## Étape 1. Activer les registres de cadeaux

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Gift Registry]**

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL General Options]** et procédez comme suit :

   ![Configuration des clients - Généralités sur le registre des cadeaux](../configuration-reference/customers/assets/gift-registry-general-options.png){width="600" zoomable="yes"}

   - Le registre des cadeaux est activé par défaut. Si nécessaire, définissez **[!UICONTROL Enable Gift Registry]** sur `Yes`.

   - Par **[!UICONTROL Maximum Registrants]**, entrez le nombre maximal de personnes qui peuvent être invitées à participer à un événement de registre des cadeaux.

## Étape 2. Configuration des notifications par e-mail

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Owner Notification]** et procédez comme suit :

   ![Configuration des clients - notification du propriétaire du registre des cadeaux](../configuration-reference/customers/assets/gift-registry-owner-notification.png){width="600" zoomable="yes"}

   - Choisissez le **[!UICONTROL Email Template]** qui avertit les propriétaires de la caisse enregistreuse de cadeaux lorsque leurs caisses enregistreuses sont créées.

   - Sélectionnez le [&#x200B; contact du magasin &#x200B;](../getting-started/store-details.md#store-email-addresses) qui s’affiche en tant que **[!UICONTROL Email Sender]** du message.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Gift Registry Sharing]** et procédez comme suit :

   ![Configuration des clients - Partage du registre des cadeaux](../configuration-reference/customers/assets/gift-registry-gift-registry-sharing.png){width="600" zoomable="yes"}

   - Choisissez le **[!UICONTROL Email Template]** qui avertit les destinataires du registre des cadeaux lorsqu’un registre est partagé avec eux.

   - Sélectionnez l’identifiant de magasin qui s’affiche en tant que **[!UICONTROL Email Sender]** du message.

   - Par **[!UICONTROL Maximum Sent Emails Threshold]**, saisissez le nombre maximal d’e-mails pouvant être envoyés à la fois.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Gift Registry Update]** et procédez comme suit :

   ![Configuration client - Mise à jour du registre des cadeaux](../configuration-reference/customers/assets/gift-registry-gift-registry-update.png){width="600" zoomable="yes"}

   - Choisissez le **[!UICONTROL Email Template]** qui informe les propriétaires du registre des cadeaux des modifications apportées au registre.

   - Sélectionnez l’identifiant de magasin qui s’affiche en tant que **[!UICONTROL Email Sender]** du message.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

1. Lorsque vous y êtes invité, mettez à jour le cache.

   Une fois le cache actualisé, Gift Registry apparaît dans le menu Magasins sous Autres paramètres et devient disponible dans les comptes clients.
