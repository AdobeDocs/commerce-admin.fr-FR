---
title: Boîte de réception des messages de l’administrateur
description: 'Découvrez la boîte de réception des messages de l’administrateur, qui fournit des messages importants et utiles d’Adobe et du système [!DNL Commerce] '
exl-id: c53bb0e4-9f18-4d40-8cc4-8c3b485f8d68
TQID: https://experienceleague.adobe.com/3RgVAR8efVGsjazQsH8-3Ohfw1h8SDuqLyCDzMYAAng
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 393
ht-degree: 0%

---

# Boîte de réception des messages de l’administrateur

Votre boutique reçoit régulièrement des messages d’Adobe. Les messages sont classés par importance et peuvent faire référence aux mises à jour système, aux correctifs, aux nouvelles versions, à la maintenance planifiée ou aux événements à venir. L’icône représentant une cloche dans l’en-tête indique le nombre de messages non lus dans votre boîte de réception.

![Administrateur - messages entrants](./assets/admin-inbox-summary.png){width="700" zoomable="yes"}

La page _[!UICONTROL Notifications]_&#x200B;répertorie tous les messages classés par date. Les commandes&#x200B;_[!UICONTROL Action]_ peuvent être utilisées pour marquer des messages individuels comme lus, afficher des informations plus détaillées ou supprimer le message de la boîte de réception.

La configuration détermine la fréquence de mise à jour de la boîte de réception et la manière dont les messages sont diffusés. Si l’administrateur de votre boutique dispose d’une URL sécurisée, les notifications doivent être diffusées via HTTPS.

## Afficher les nouveaux messages entrants

1. Cliquez sur l’icône **[!UICONTROL Notification]** dans l’en-tête et lisez le résumé.

1. Effectuez l’une des opérations suivantes :

   - Si nécessaire, cliquez sur le message pour afficher le texte complet.
   - Pour supprimer le message, cliquez sur l’icône de suppression située à droite du message.
   - Pour afficher la liste complète des Notifications, cliquez sur **[!UICONTROL See All]**.

## Traiter un message critique

Pour envoyer un message d’importance critique, effectuez l’une des opérations suivantes :

- Cliquez sur **[!UICONTROL Read Details]**.
- Pour fermer la boîte d’alerte mais laisser le message actif, cliquez sur **[!UICONTROL Close]**.

## Administrer vos notifications

1. Effectuez l’une des opérations suivantes pour ouvrir la page Notifications :

   - Cliquez sur l’icône **[!UICONTROL Notification]** dans l’en-tête. Si un ou plusieurs nouveaux messages s’affichent, cliquez sur **[!UICONTROL See All]**.

   - Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Notifications]**.

1. Dans la colonne **[!UICONTROL Action]**, effectuez l’une des opérations suivantes :

   - Pour plus d’informations, cliquez sur **[!UICONTROL Read Details]** pour ouvrir la page liée dans une nouvelle fenêtre.

   - Pour conserver le message dans votre boîte de réception, cliquez sur **[!UICONTROL Mark As Read]**.

     ![Administrateur - Marquer les notifications sélectionnées comme lues](./assets/admin-notifications-mark-as-read.png){width="700" zoomable="yes"}

   - Pour supprimer le message, cliquez sur **[!UICONTROL Remove]**.

1. Pour appliquer une action à plusieurs messages, effectuez l’une des opérations suivantes :

   - Cochez la case de la première colonne pour chaque message à gérer.
   - Pour sélectionner plusieurs messages, définissez le contrôle **[!UICONTROL Mass Actions]** selon vos besoins.

1. Définissez le contrôle **[!UICONTROL Actions]** sur l’une des options suivantes :

   - `Mark as Read`
   - `Remove`

1. Cliquez sur **[!UICONTROL Submit]** pour terminer le processus.

## Configuration des notifications

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de navigation de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Notifications]** .

   ![Configuration des notifications](./assets/system-notifications.png){width="600"}

1. Si l’administrateur de votre boutique s’exécute sur une [URL sécurisée](../stores-purchase/store-urls.md), définissez **[!UICONTROL Use HTTPS to Get Feed]** sur `Yes`.

1. Définissez **[!UICONTROL Update Frequency]** pour déterminer la fréquence de mise à jour de votre boîte de réception.

   L’intervalle peut être compris entre une et 24 heures.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

Pour plus d’informations sur les options de configuration [!UICONTROL System], consultez le [_Guide de référence de configuration_](../configuration-reference/advanced/system.md).
