---
title: Configuration des communications par courrier électronique
description: Découvrez comment configurer les communications par courrier électronique, y compris le routage des courriers électroniques renvoyés ou des réponses à une adresse électronique spécifique.
exl-id: 7e62e9c5-f214-4fd5-becc-99dcb093cd5c
feature: Communications, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Configuration des communications par courrier électronique

Les _paramètres d’envoi de courrier_ vous permettent d’acheminer les courriers électroniques renvoyés ou les réponses aux courriers électroniques vers une adresse spécifique. Si votre boutique est en cours d’exécution sur un serveur SMTP ou Windows, vous pouvez vérifier les paramètres d’hôte et de port.

>[!IMPORTANT]
>
>**Avis de sécurité** Tous les commerçants doivent immédiatement définir leur configuration d’envoi de courrier afin de se protéger contre un exploit d’exécution de code distant potentiel récemment identifié. Tant que ce problème n’est pas résolu, il est vivement recommandé d’éviter d’utiliser [!DNL Sendmail] pour les communications par courrier électronique. Dans _[!UICONTROL Mail Sending Settings]_, assurez-vous que&#x200B;_[!UICONTROL Set Return Path]_ est défini sur `No`.

Pour obtenir la liste détaillée des paramètres de configuration, voir [_[!UICONTROL Mail Sending Settings]_](../configuration-reference/advanced/system.md) dans la _référence de configuration_.

## Configuration des communications par courrier électronique

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) de **[!UICONTROL Mail Sending Settings]** et procédez comme suit :

   ![ Configuration avancée - Paramètres d&#39;envoi de courrier ](../configuration-reference/advanced/assets/system-mail-sending-settings.png){width="600" zoomable="yes"}

   - Si nécessaire, définissez **[!UICONTROL Disable Email Communications]** sur `No`.

   - Pour **[!UICONTROL Transport]**, choisissez le type de transport pour les communications par e-mail du magasin : `Sendmail` ou `SMTP`

   - Si vous exécutez sur un serveur SMTP ou Windows, vérifiez les paramètres suivants :

      - **[!UICONTROL Host]** - `localhost` ou autre

      - **[!UICONTROL Port (25)]** - `25` ou autre

   - Pour **[!UICONTROL Set Return Path]**, sélectionnez l’une des options suivantes :

      - `No` - (mesure de sécurité recommandée) Les itinéraires renvoient le courrier électronique à l’adresse électronique de magasin par défaut.
      - `Yes` - Les itinéraires ont renvoyé l’adresse électronique du magasin par défaut.
      - `Specified` - Les itinéraires ont renvoyé le courrier électronique à l’adresse électronique spécifiée dans **[!UICONTROL Return Path Email]**.

   - Si vous exécutez sur un serveur SMTP, configurez la connexion :

      - **[!UICONTROL Username]** - Entrez le nom d’utilisateur de connexion du serveur SMTP.
      - **[!UICONTROL Password]** - Entrez le mot de passe de la connexion au serveur SMTP.
      - **[!UICONTROL Auth]** - Choisissez le type d’authentification pour la connexion au serveur SMTP : `NONE`, `PLAIN` ou `LOGIN`
      - **[!UICONTROL SSL]** - Choisissez le type de vérification pour le certificat de sécurité du serveur : `SSL` ou `TLS`

     ![ Configuration avancée - Paramètres d&#39;envoi de courrier ](../configuration-reference/advanced/assets/system-mail-sending-settings-smtp.png){width="600" zoomable="yes"}

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Sales Emails]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL General Settings]** .

1. Définissez **[!UICONTROL Asynchronous sending]** sur `Enable`.

   ![Configuration des ventes - paramètres généraux de l’email](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   Pour obtenir la liste détaillée des paramètres de configuration, voir [_Paramètres généraux_](../configuration-reference/sales/sales-emails.md) dans la _référence de configuration_.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
