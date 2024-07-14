---
title: Intégrations
description: Découvrez comment configurer les informations d’identification OAuth et l’URL de redirection pour les intégrations tierces.
exl-id: b7632994-b07b-4cdb-b62c-79bc7a3a01c8
role: Admin, Developer
feature: System, Integration, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# Intégrations

La définition d’une intégration dans l’administrateur Commerce détermine l’emplacement des informations d’identification OAuth et de l’URL de redirection pour les intégrations tierces, et identifie les ressources d’API disponibles nécessaires à l’intégration. Pour plus d’informations sur le processus d’enregistrement de l’intégration, voir [Authentification basée sur OAuth](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) dans la documentation destinée aux développeurs Commerce.

![Intégrations](./assets/integrations.png){width="700" zoomable="yes"}

## Processus d’intégration

1. **Autoriser l’intégration** - Accédez à la page **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**, recherchez l’intégration appropriée et autorisez-la.
1. **Vérifier et établir la connexion** - Lorsque vous y êtes invité, acceptez l’accès demandé. Si vous êtes redirigé vers un tiers, connectez-vous au système ou créez un compte. Une fois la connexion établie, vous revenez à la page d’intégration.
1. **Recevez la confirmation de l’intégration autorisée** - Le système envoie une notification indiquant que l’intégration a été autorisée avec succès. Après avoir configuré une intégration et reçu les informations d’identification, il n’est plus nécessaire d’effectuer des appels pour accéder aux jetons ou de demander des jetons.

## Ajout d’une intégration

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

   ![Nouvelle intégration](./assets/integration-new.png){width="600" zoomable="yes"}

1. Renseignez les informations d’intégration suivantes :

   - Saisissez le **[!UICONTROL Name]** de l&#39;intégration et l&#39;adresse de contact **[!UICONTROL Email]**.

   - Saisissez le **[!UICONTROL Callback URL]** où les informations d’identification OAuth peuvent être envoyées lors de l’utilisation d’OAuth pour l’exchange du jeton. L&#39;utilisation de `https://` est fortement recommandée.

   - Saisissez le **[!UICONTROL Identity Link URL]** pour rediriger les utilisateurs vers un compte tiers avec ces informations d’identification d’intégration Adobe Commerce ou Magento Open Source.

   >[!NOTE]
   >
   > L’étiquette d’avertissement `Integration not secure` s’affiche à côté de chaque nom d’intégration sur la grille [!UICONTROL Integrations] comme rappel, jusqu’à ce que les URL HTTPS soient enregistrées dans les champs [!UICONTROL Callback URL] et [!UICONTROL Identity Link URL].

   - Lorsque vous y êtes invité, saisissez votre mot de passe pour confirmer votre identité.

1. Dans le panneau de gauche, sélectionnez **[!UICONTROL API]** et procédez comme suit :

   - Définissez **[!UICONTROL Resource Access]** sur l’une des options suivantes :

      - `All`
      - `Custom`

   - Pour un accès personnalisé, cochez la case de chaque ressource nécessaire.

     ![Intégrations - API disponible](./assets/integrations-available-api.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

## Activation d’une intégration

Par défaut, une intégration enregistrée s’affiche sur la grille avec l’état `Inactive`. Pour l’activer, procédez comme suit :

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. Recherchez l’intégration nouvellement créée et cliquez sur le lien **[!UICONTROL Activate]** .

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Allow]**.

   Cette action affiche les jetons d’intégration pour les extensions. Copiez ces informations dans un emplacement sécurisé et chiffré à utiliser avec votre intégration.

   ![Jetons d’intégration pour les extensions](./assets/integration-tokens-for-extensions.png){width="600" zoomable="yes"}

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Done]**.

## Réautoriser une intégration

Pour générer un nouveau jeton d’accès à l’intégration et un nouveau secret de jeton d’accès, réautorisez l’intégration à partir de l’administrateur :

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. Recherchez l’intégration avec l’état **[!UICONTROL Active]**.

1. Dans la colonne _[!UICONTROL Activate]_, cliquez sur **[!UICONTROL Reauthorize]**.

1. Cliquez sur **[!UICONTROL Reauthorize]** pour approuver l’accès aux ressources de l’API.

1. Enregistrez les nouveaux jetons d’intégration pour les extensions et cliquez sur **[!UICONTROL Done]**.

## Modification du paramètre de sécurité de l’accès des invités à l’API

Par défaut, le système n’autorise pas l’accès anonyme des invités à CMS, catalogue et autres ressources de magasin. Si vous devez modifier le paramètre, procédez comme suit :

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Services]** et choisissez **[!UICONTROL Magento Web API]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Web API Security Setting]** .

   ![ Configuration des services - Paramètres de sécurité de l’API web](../configuration-reference/services/assets/web-api-security.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Allow Anonymous Guest Access]** sur `Yes`.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

Pour plus d’informations, voir [Limitation de l’accès aux API web anonymes](https://developer.adobe.com/commerce/webapi/rest/use-rest/anonymous-api-security/) dans la documentation destinée aux développeurs Commerce.

## Suppression d’une intégration

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. Recherchez l’intégration existante et cliquez sur l’icône ( ![icône de corbeille](../assets/icon-delete-trashcan-solid.png) ) dans la colonne **[!UICONTROL Delete]** .

1. Pour confirmer votre action, cliquez sur **[!UICONTROL OK]**.
