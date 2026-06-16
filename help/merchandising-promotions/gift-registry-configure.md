---
title: Configurer les registres de cadeaux
description: Découvrez comment activer les registres de cadeaux et configurer les notifications par e-mail associées.
exl-id: 48193621-731d-4640-8ea8-5b201915cdf1
feature: Gift, Storefront, Configuration
TQID: https://experienceleague.adobe.com/a7DRiAPSkWhBIPdXPXnH3HB1uw9d4WY4vXOtfgg9kRY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 358
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

   - Sélectionnez le [ contact du magasin ](../getting-started/store-details.md#store-email-addresses) qui s’affiche en tant que **[!UICONTROL Email Sender]** du message.

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
