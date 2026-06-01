---
title: Options de mot de passe du client
description: Les options de mot de passe client déterminent le niveau de sécurité des différentes fonctions de votre boutique destinées aux clients.
exl-id: 84dec8e8-3363-4133-bbcc-9e58467749c4
feature: Customers, Configuration, Security
source-git-commit: ea9eeea0fc5213de2787e0b7ea2aed825ca3a9de
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# Options de mot de passe du client

Les options de mot de passe du client déterminent le niveau de sécurité utilisé pour les demandes de réinitialisation de mot de passe, les modèles d’e-mail utilisés pour les notifications du client et la durée de vie du lien de récupération du mot de passe. Vous pouvez autoriser les clients à modifier leurs propres mots de passe ou exiger que seuls les administrateurs de magasin puissent le faire.

## Configurer les options de mot de passe du client

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Customer Configuration]**.

1. Développez la section **[!UICONTROL Password Options]** .

   ![Options de mot de passe](../configuration-reference/customers/assets/customer-configuration-password-options.png){width="600" zoomable="yes"}

1. Définissez la **[!UICONTROL Password Reset Protection Type]** sur la méthode à utiliser pour vérifier les demandes de réinitialisation de mot de passe :

   - `By IP and Email` - Recherchez les tentatives précédentes de réinitialisation du mot de passe pour un e-mail ou une adresse IP spécifique.
   - `By IP` - Recherchez les tentatives précédentes de réinitialisation du mot de passe à partir d’une adresse IP spécifique.
   - `By Email` - Recherchez les tentatives précédentes de réinitialisation du mot de passe pour un e-mail spécifique.
   - `None` - Protection désactivée (aucune limite de réinitialisation du mot de passe).

   Les **[!UICONTROL Max Number of Password Reset Requests]** et **[!UICONTROL Min Time Between Password Reset Requests]** sont calculés en fonction de cette configuration.

1. Pour limiter le nombre de demandes de réinitialisation de mot de passe envoyées par heure, procédez comme suit :

   - Par **[!UICONTROL Max Number of Password Reset Requests]**, saisissez le nombre maximal de demandes de réinitialisation de mot de passe qui peuvent être envoyées par heure.

   - Par **[!UICONTROL Min Time Between Password Reset Requests]**, saisissez le nombre minimum de minutes qui doit s’écouler entre les requêtes.

1. Pour configurer la notification électronique de réinitialisation de mot de passe, procédez comme suit :

   - Définissez **[!UICONTROL Forgot Email Template]** sur le modèle utilisé pour l’e-mail envoyé aux clients qui ont oublié leurs mots de passe.

   - Définissez **[!UICONTROL Remind Email Template]** sur le modèle utilisé lorsqu’un mot de passe client est réinitialisé par un utilisateur administrateur.

   - Définissez **[!UICONTROL Reset Password Template]** sur le modèle utilisé lorsque les clients changent leur mot de passe.

   - Définissez **[!UICONTROL Password Template Email Sender]** sur le [&#x200B; contact du magasin &#x200B;](../getting-started/store-details.md) qui s’affiche comme l’expéditeur des notifications liées aux mots de passe.

1. Renseignez les options de sécurité de réinitialisation de mot de passe suivantes :

   - Par **[!UICONTROL Recovery Link Expiration Period (hours)]**, saisissez le nombre d’heures avant l’expiration du lien de récupération du mot de passe.

   - Si vous souhaitez que les champs des formulaires de connexion du client et de mot de passe oublié soient renseignés automatiquement à partir des entrées précédentes, définissez **[!UICONTROL Enable Autocomplete on login/forgot password forms]** sur `Yes`.

   - Par **[!UICONTROL Number of Required Character Classes]**, saisissez le nombre de types de caractères différents qui doivent être inclus dans un mot de passe en fonction des classes de caractères suivantes :

      - `Lowercase`
      - `Uppercase`
      - `Numeric`
      - `Special Characters`

   - Par **[!UICONTROL Maximum Login Failures to Lockout Account]**, saisissez le nombre de tentatives de connexion ayant échoué jusqu’à ce que le compte client soit verrouillé. Pour un nombre illimité de tentatives, saisissez zéro (`0`).

   - Par **[!UICONTROL Minimum Password Length]**, saisissez le nombre minimum de caractères pouvant être utilisés dans un mot de passe. Le nombre doit être supérieur à zéro.

   - Par **[!UICONTROL Lockout Time (minutes)]**, saisissez le nombre de minutes pendant lesquelles un compte client est verrouillé après un trop grand nombre d’échecs de tentatives de connexion.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
