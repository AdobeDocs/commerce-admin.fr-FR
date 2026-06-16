---
title: Connexion client
description: La fonction de connexion du client sur le storefront permet un accès facile aux comptes des clients.
exl-id: eadcc15a-a052-4213-a818-d5b248d974d2
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/WuMuGVXByzb0PlpkKHnJCT-s7ToHtb1odvTu18LxB-I
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 383
ht-degree: 0%

---

# Connexion client

Les clients ont facilement accès à leurs comptes depuis chaque page de votre boutique. Selon la [configuration](../customers/account-options-new.md), les clients peuvent être redirigés vers le tableau de bord de leur compte ou continuer à acheter après s’être connectés à leur compte.

Si le [CAPTCHA](../systems/security-captcha.md) est activé dans la configuration, la personne doit effectuer correctement un test qui vérifie qu’elle est humaine, avant d’accéder à ses comptes.

Lorsque les clients oublient leurs mots de passe, un lien de réinitialisation est envoyé à l’adresse e-mail associée au compte. La configuration [Options de mot de passe](../customers/password-options.md) contrôle l’expérience client pour les tentatives de connexion :

- Nombre de fois qu’un client peut tenter de saisir un mot de passe
- Nombre de minutes entre les tentatives
- Nombre total de tentatives avant verrouillage du compte
- Durée du verrouillage

![Lien de connexion sur l’en-tête du storefront](assets/storefront-sign-in-create-account.png){width="700" zoomable="yes"}

## Connexion à un compte client

1. Dans l’en-tête du magasin, le client clique sur **[!UICONTROL Sign in]**.

   ![Connexion client](assets/login.png){width="700" zoomable="yes"}

1. Saisit leur adresse **[!UICONTROL Email]** et leur **[!UICONTROL Password]**.

1. Effectue un clic sur **[!UICONTROL Sign in]**.

   >[!IMPORTANT]
   >
   >S’il ne parvient pas à se souvenir de son mot de passe, le client peut cliquer sur **[!UICONTROL Forgot Your Password?]** et suivre les [instructions](../customers/password-reset.md) pour le réinitialiser.

## Définir la redirection vers le tableau de bord du compte après la connexion du client

Vous pouvez configurer le magasin pour rediriger les clients vers le tableau de bord de leur compte après leur connexion ou les laisser continuer leurs achats.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Customer Configuration]**.

1. Développez la section **[!UICONTROL Login Options]** .

1. Définissez **[!UICONTROL Redirect Customer to Account Dashboard after Logging in]** sur l’une des options suivantes :

   - `Yes` - Le tableau de bord du compte s’affiche lorsque les clients se connectent à leur compte.
   - `No` - Les clients peuvent continuer à faire des achats après s’être connectés à leur compte.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Se connecter avec Amazon

Pour les magasins disposant d’une intégration [!DNL Amazon Pay] et [!DNL Login with Amazon] configurée, les clients peuvent se connecter à leur compte d’acheteur Amazon.

1. Dans l’en-tête du magasin, le client clique sur **[!UICONTROL Sign in]**.

1. Effectue un clic sur **[!UICONTROL Login with Amazon]**.

   ![Connexion avec Amazon](assets/amazon-pay.png){width="700" zoomable="yes"}

1. Lorsque vous êtes invité à vous connecter, le client saisit le **[!UICONTROL email address]** et le **[!UICONTROL password]** de son compte d&#39;acheteur Amazon.

   ![Saisie des informations d’identification Amazon](assets/amazon-popup1.png){width="700" zoomable="yes"}

1. Pour accorder à Amazon l’autorisation de partager les informations suivantes de son compte avec la boutique lors du traitement des achats, clique sur **OK**.

   - Nom
   - Adresse e-mail
   - Adresses d’expédition

   ![Octroyer l’autorisation de partager des données](assets/amazon-popup2.png){width="700" zoomable="yes"}

## Se déconnecter d’un compte client

1. Dans le coin supérieur droit à côté de _[!UICONTROL Welcome, Customer Name!]_, le client clique sur le sélecteur de menu **[!UICONTROL v]**.

1. Choisissez **[!UICONTROL Sign Out]**.

Après la déconnexion, le client est redirigé vers la page d’accueil.
