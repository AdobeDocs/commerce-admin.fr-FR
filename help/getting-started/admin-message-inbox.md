---
title: Boîte de réception des messages de l’administrateur
description: Découvrez la boîte de réception du message Admin, qui fournit des messages importants et utiles depuis Adobe et depuis le [!DNL Commerce] système.
exl-id: c53bb0e4-9f18-4d40-8cc4-8c3b485f8d68
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# Boîte de réception des messages de l’administrateur

Votre boutique reçoit régulièrement des messages d’Adobe. Les messages sont classés par importance et peuvent faire référence aux mises à jour du système, aux correctifs, aux nouvelles versions, à la maintenance planifiée ou aux événements à venir. L’icône représentant une cloche dans l’en-tête indique le nombre de messages non lus dans votre boîte de réception.

![Admin - messages entrants](./assets/admin-inbox-summary.png){width="700" zoomable="yes"}

La variable _[!UICONTROL Notifications]_répertorie tous les messages classés par date. La variable_[!UICONTROL Action]_ Vous pouvez utiliser des commandes pour marquer des messages individuels comme lus, afficher des informations plus détaillées ou supprimer le message de la boîte de réception.

La configuration détermine la fréquence de mise à jour de la boîte de réception et la diffusion des messages. Si votre administrateur de magasin dispose d’une URL sécurisée, les notifications doivent être diffusées via HTTPS.

## Afficher les nouveaux messages entrants

1. Cliquez sur le bouton **[!UICONTROL Notification]** dans l’en-tête et lisez le résumé.

1. Effectuez l’une des opérations suivantes :

   - Si nécessaire, cliquez sur le message pour afficher le texte intégral.
   - Pour supprimer le message, cliquez sur l’icône de suppression située à droite du message.
   - Pour afficher la liste complète des notifications, cliquez sur **[!UICONTROL See All]**.

## adresser un message critique ;

Pour un message d’importance critique, effectuez l’une des opérations suivantes :

- Cliquez sur **[!UICONTROL Read Details]**.
- Pour fermer la boîte d’alerte, mais conserver le message actif, cliquez sur **[!UICONTROL Close]**.

## Administration des notifications

1. Pour ouvrir la page Notifications, effectuez l’une des opérations suivantes :

   - Cliquez sur le bouton **[!UICONTROL Notification]** dans l’en-tête. Si un ou plusieurs nouveaux messages s’affichent, cliquez sur **[!UICONTROL See All]**.

   - Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Notifications]**.

1. Dans le **[!UICONTROL Action]** , effectuez l’une des opérations suivantes :

   - Pour plus d’informations, cliquez sur **[!UICONTROL Read Details]** pour ouvrir la page liée dans une nouvelle fenêtre.

   - Pour conserver le message dans votre boîte de réception, cliquez sur **[!UICONTROL Mark As Read]**.

     ![Admin - Marquer les notifications sélectionnées comme lues](./assets/admin-notifications-mark-as-read.png){width="700" zoomable="yes"}

   - Pour supprimer le message, cliquez sur **[!UICONTROL Remove]**.

1. Pour appliquer une action à plusieurs messages, effectuez l’une des opérations suivantes :

   - Cochez la case dans la première colonne pour chaque message à gérer.
   - Pour sélectionner plusieurs messages, définissez la variable **[!UICONTROL Mass Actions]** le contrôle, le cas échéant.

1. Définissez la variable **[!UICONTROL Actions]** à l’une des options suivantes :

   - `Mark as Read`
   - `Remove`

1. Cliquez sur **[!UICONTROL Submit]** pour terminer le processus.

## Configurer les notifications

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de navigation de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png)la valeur **[!UICONTROL Notifications]** .

   ![Configuration des notifications](./assets/system-notifications.png){width="600"}

1. Si votre administrateur de magasin s’exécute sur une [URL sécurisée](../stores-purchase/store-urls.md), définit **[!UICONTROL Use HTTPS to Get Feed]** to `Yes`.

1. Définir **[!UICONTROL Update Frequency]** pour déterminer la fréquence de mise à jour de votre boîte de réception.

   L’intervalle peut être compris entre une et 24 heures.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

Pour plus d’informations sur la variable [!UICONTROL System] options de configuration, voir [_Guide de référence de configuration_](../configuration-reference/advanced/system.md).
