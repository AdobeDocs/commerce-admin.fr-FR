---
title: Envoyer un e-mail à un ami
description: Découvrez comment fournir un lien d’e-mail qui permet à vos clients de partager facilement des liens vers des produits avec leurs amis.
exl-id: 46cf9994-6490-4cb4-85b7-9a7cab7783e0
feature: Storefront, Configuration
TQID: https://experienceleague.adobe.com/a75E4X5mTDXeCQKysvIecdU3OhsICiWTtwh7k-oK9cw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 414
ht-degree: 0%

---

# Envoyer un e-mail à un ami

Le lien d’e-mail permet à vos clients de partager facilement des liens vers des produits avec leurs amis. Dans le magasin Luma de démonstration, le lien E-mail s’affiche sous la forme d’une icône d’enveloppe. Le modèle de message peut être personnalisé en fonction de votre voix et de votre marque. Pour éviter les spams, vous pouvez limiter le nombre de destinataires de chaque e-mail et le nombre de produits qui peuvent être partagés sur une période d’une heure.

![Exemple de storefront - envoyer un e-mail à un ami](./assets/storefront-email-a-friend.png){width="700" zoomable="yes"}

## Configurer email-a-friend

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Email to a Friend]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Email Templates]** et définissez les options suivantes :

   ![Configuration du catalogue - Modèles d’e-mail](../configuration-reference/catalog/assets/email-to-a-friend-email-templates.png){width="600" zoomable="yes"}

   Pour obtenir une description détaillée de chacun de ces paramètres de configuration, voir [Modèles d’e-mail](../configuration-reference/catalog/email-to-a-friend.md) dans le _Guide de référence de configuration_.

   Pour modifier le paramètre par défaut d’un champ, décochez la case **[!UICONTROL Use system value]** pour rendre le champ modifiable.

   - Définissez **[!UICONTROL Enabled]** sur `Yes`.

   - Définissez **[!UICONTROL Select Email Template]** sur le modèle que vous souhaitez utiliser comme base pour les messages.

   - Si vous souhaitez que seuls les clients enregistrés puissent envoyer des e-mails à leurs amis, définissez **[!UICONTROL Allow for Guests]** sur `No`.

   - Par **[!UICONTROL Max Recipients]**, saisissez le nombre maximal d’amis qui peuvent être sur la liste de distribution pour un seul message.

   - Par **[!UICONTROL Max Products Sent in 1 Hour]**, saisissez le nombre maximal de produits qui peuvent être partagés par un seul utilisateur avec des amis sur une période d’une heure.

   - Pour identifier l’expéditeur des e-mails, définissez **[!UICONTROL Limit Sending By]** sur l’une des méthodes suivantes :

     `IP Address` - (Recommandé) Identifie l’expéditeur à l’aide de l’adresse IP de l’ordinateur utilisé pour envoyer les e-mails.

     `Cookie (unsafe)` - Identifie l’expéditeur par cookie de navigateur. Cette méthode est moins efficace, car l’expéditeur ou l’expéditrice peut supprimer le cookie pour contourner la limite.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Envoyer un e-mail à un ami sur le storefront

Lorsque cette fonctionnalité est configurée, les clients du magasin suivent les étapes suivantes pour partager des informations sur les produits avec leurs amis.

1. Sur une page de catalogue, le client clique sur le lien **[!UICONTROL Email]**.

1. Si la fonction n’est configurée que pour les utilisateurs enregistrés, effectue l’une des opérations suivantes :

   - Se connecte à votre compte client.
   - S’inscrit(e) pour un nouveau compte.

1. Complète la **[!UICONTROL Message]** et renseigne le **[!UICONTROL Name]** et le **[!UICONTROL Email Address]** du destinataire.

   Si nécessaire, le client peut ajouter d&#39;autres destinataires :

   - Effectue un clic sur **[!UICONTROL Add Invitee]**.

   - Saisit le **[!UICONTROL Name]** et le **[!UICONTROL Email Address]** de la personne supplémentaire.

     Ils peuvent envoyer le message à autant de personnes supplémentaires que la configuration le permet. Il peut supprimer l’invité ajouté en cliquant sur le lien **[!DNL Remove]**.

1. Une fois prêt à envoyer le message, clique sur **[!UICONTROL Send Email]**.

   ![Exemple de storefront - envoyer un e-mail à un ami](./assets/storefront-email-a-friend-form.png){width="700" zoomable="yes"}
