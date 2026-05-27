---
title: Envoyer un e-mail à un ami
description: Découvrez comment fournir un lien d’e-mail qui permet à vos clients de partager facilement des liens vers des produits avec leurs amis.
exl-id: 46cf9994-6490-4cb4-85b7-9a7cab7783e0
feature: Storefront, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '414'
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
