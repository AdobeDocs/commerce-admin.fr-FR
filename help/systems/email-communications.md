---
title: Configurer les communications par e-mail
description: Découvrez comment configurer les communications par e-mail, y compris le routage des e-mails renvoyés ou des réponses à une adresse e-mail spécifique.
exl-id: 7e62e9c5-f214-4fd5-becc-99dcb093cd5c
feature: Communications, Configuration
TQID: https://experienceleague.adobe.com/0spSxu59rF2KomOWVI5iR9pcg2r-VLm-GiXvJvatnww
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 310
ht-degree: 0%

---

# Configurer les communications par e-mail

Les _Paramètres d’envoi du courrier électronique_ vous permettent d’acheminer les e-mails renvoyés ou les réponses aux e-mails vers une adresse spécifique. Si votre magasin s’exécute sur un serveur SMTP ou Windows, vous pouvez vérifier les paramètres de l’hôte et du port.

>[!IMPORTANT]
>
>**Avis de sécurité** Tous les commerçants doivent immédiatement définir leur configuration d&#39;envoi d&#39;e-mails pour se protéger contre une exploitation potentielle d&#39;exécution de code à distance récemment identifiée. Jusqu’à ce que ce problème soit résolu, il est vivement recommandé d’éviter d’utiliser [!DNL Sendmail] pour les communications par e-mail. Dans l’_[!UICONTROL Mail Sending Settings]_, assurez-vous que_[!UICONTROL Set Return Path]_ est défini sur `No`.

Pour obtenir la liste détaillée des paramètres de configuration, voir [_[!UICONTROL Mail Sending Settings]_](../configuration-reference/advanced/system.md) dans le _Référence de configuration_.

## Configurer les communications par e-mail

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Mail Sending Settings]** et procédez comme suit :

   ![Configuration avancée - Paramètres d’envoi d’e-mails](../configuration-reference/advanced/assets/system-mail-sending-settings.png){width="600" zoomable="yes"}

   - Si nécessaire, définissez **[!UICONTROL Disable Email Communications]** sur `No`.

   - Par **[!UICONTROL Transport]**, choisissez le type de transport pour les communications par e-mail à partir du magasin : `Sendmail` ou `SMTP`

   - Si vous utilisez un serveur SMTP ou Windows, vérifiez les paramètres suivants :

      - **[!UICONTROL Host]** - `localhost` ou autre

      - **[!UICONTROL Port (25)]** - `25` ou autre

   - Par **[!UICONTROL Set Return Path]**, choisissez l’une des options suivantes :

      - `No` - (Mesure de sécurité recommandée) Les itinéraires renvoyaient l’e-mail à l’adresse e-mail par défaut du magasin.
      - `Yes` - Achemine l’e-mail renvoyé vers l’adresse e-mail du magasin par défaut.
      - `Specified` - Achemine les e-mails renvoyés vers l’adresse e-mail spécifiée dans **[!UICONTROL Return Path Email]**.

   - Si vous utilisez un serveur SMTP, configurez la connexion :

      - **[!UICONTROL Username]** - Saisissez le nom d’utilisateur pour le serveur SMTP.
      - **[!UICONTROL Password]** - Saisissez le mot de passe pour le login du serveur SMTP.
      - **[!UICONTROL Auth]** - Choisissez le type d’authentification de la connexion au serveur SMTP : `NONE` , `PLAIN` ou `LOGIN`
      - **[!UICONTROL SSL]** - Choisissez le type de vérification pour le certificat de sécurité du serveur : `SSL` ou `TLS`

     ![Configuration avancée - Paramètres d’envoi d’e-mails](../configuration-reference/advanced/assets/system-mail-sending-settings-smtp.png){width="600" zoomable="yes"}

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales Emails]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL General Settings]** .

1. Définissez **[!UICONTROL Asynchronous sending]** sur `Enable`.

   ![Configuration des ventes - Paramètres généraux des e-mails](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   Pour obtenir la liste détaillée des paramètres de configuration, voir [_Paramètres généraux_](../configuration-reference/sales/sales-emails.md) dans le _Référence de configuration_.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
