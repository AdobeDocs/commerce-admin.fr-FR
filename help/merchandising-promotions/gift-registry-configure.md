---
title: Configuration des registres de cadeaux
description: Découvrez comment activer les registres d’achats et configurer les notifications électroniques associées.
exl-id: 48193621-731d-4640-8ea8-5b201915cdf1
feature: Gift, Storefront, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---

# Configuration des registres de cadeaux

{{ee-feature}}

Avant de pouvoir proposer des registres de cadeaux à vos clients, vous devez activer les registres de cadeaux et configurer les notifications par e-mail associées. Adobe Commerce envoie les notifications suivantes en réponse aux événements du workflow du registre des cadeaux.

- Lorsqu’un nouveau registre de cadeaux est créé, un courrier électronique est envoyé au propriétaire avec un lien vers le registre qui peut être partagé.
- En option, la boutique peut envoyer une notification contenant un lien vers le registre des cadeaux aux amis et à la famille du propriétaire du registre des cadeaux.
- Le propriétaire est informé lorsque des articles sont achetés dans le registre des cadeaux, mais n’indique pas l’acheteur.

Adobe Commerce comporte des modèles prédéfinis pour chacun de ces emails qui peuvent être personnalisés pour votre marque.

## Étape 1. Activation des enregistrements de cadeau

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Gift Registry]**

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) de **[!UICONTROL General Options]** et procédez comme suit :

   ![Configuration des clients - général du registre des cadeaux](../configuration-reference/customers/assets/gift-registry-general-options.png){width="600" zoomable="yes"}

   - Le registre des cadeaux est activé par défaut. Si nécessaire, définissez **[!UICONTROL Enable Gift Registry]** sur `Yes`.

   - Pour **[!UICONTROL Maximum Registrants]**, entrez le nombre maximal de personnes qui peuvent être invitées à participer à un événement de registre des cadeaux.

## Étape 2. Configuration des notifications par courrier électronique

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) de **[!UICONTROL Owner Notification]** et procédez comme suit :

   ![Configuration des clients - notification du propriétaire du registre des cadeaux](../configuration-reference/customers/assets/gift-registry-owner-notification.png){width="600" zoomable="yes"}

   - Sélectionnez le **[!UICONTROL Email Template]** qui avertit les propriétaires du registre des cadeaux lors de la création de leurs registres.

   - Sélectionnez le [contact de magasin](../getting-started/store-details.md#store-email-addresses) qui apparaît comme le **[!UICONTROL Email Sender]** du message.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) de **[!UICONTROL Gift Registry Sharing]** et procédez comme suit :

   ![Configuration des clients - partage de registre des cadeaux](../configuration-reference/customers/assets/gift-registry-gift-registry-sharing.png){width="600" zoomable="yes"}

   - Sélectionnez le **[!UICONTROL Email Template]** qui avertit les destinataires du registre-cadeau lorsqu’un registre est partagé avec eux.

   - Sélectionnez l’identifiant de magasin qui apparaît comme le **[!UICONTROL Email Sender]** du message.

   - Pour **[!UICONTROL Maximum Sent Emails Threshold]**, saisissez le nombre maximal de courriers électroniques pouvant être envoyés simultanément.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) de **[!UICONTROL Gift Registry Update]** et procédez comme suit :

   ![Configuration des clients - mise à jour du registre des cadeaux](../configuration-reference/customers/assets/gift-registry-gift-registry-update.png){width="600" zoomable="yes"}

   - Sélectionnez le **[!UICONTROL Email Template]** qui avertit les propriétaires du registre-cadeau des modifications apportées au registre.

   - Sélectionnez l’identifiant de magasin qui apparaît comme le **[!UICONTROL Email Sender]** du message.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous y êtes invité, mettez à jour le cache.

   Une fois le cache actualisé, le registre des cadeaux s’affiche dans le menu Magasins sous Autres paramètres et est disponible dans les comptes clients.
