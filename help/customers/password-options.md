---
title: Options de mot de passe du client
description: Les options de mot de passe du client déterminent le niveau de sécurité pour les différentes fonctions de votre magasin qui s’adressent aux clients.
exl-id: 84dec8e8-3363-4133-bbcc-9e58467749c4
feature: Customers, Configuration, Security
source-git-commit: ea9eeea0fc5213de2787e0b7ea2aed825ca3a9de
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# Options de mot de passe du client

Les options de mot de passe client déterminent le niveau de sécurité utilisé pour les demandes de réinitialisation de mot de passe, les modèles d’email utilisés pour la notification client et la durée de vie du lien de récupération de mot de passe. Vous pouvez autoriser les clients à modifier leurs propres mots de passe ou exiger que seuls les administrateurs de magasin puissent le faire.

## Configuration des options de mot de passe du client

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Customer Configuration]**.

1. Développez l’objet **[!UICONTROL Password Options]** .

   ![Options de mot de passe](../configuration-reference/customers/assets/customer-configuration-password-options.png){width="600" zoomable="yes"}

1. Définissez la variable **[!UICONTROL Password Reset Protection Type]** à la méthode que vous souhaitez utiliser pour vérifier les demandes de réinitialisation de mot de passe :

   - `By IP and Email` - Recherchez les tentatives précédentes de réinitialisation du mot de passe d’un courrier électronique spécifique ou d’une adresse IP spécifique.
   - `By IP` - Recherchez les tentatives précédentes de réinitialisation du mot de passe à partir d’une adresse IP spécifique.
   - `By Email` - Recherchez les tentatives précédentes de réinitialisation du mot de passe pour un courrier électronique spécifique.
   - `None` - Protection désactivée (aucune limite pour la réinitialisation du mot de passe).

   La variable **[!UICONTROL Max Number of Password Reset Requests]** et **[!UICONTROL Min Time Between Password Reset Requests]** sont calculées en fonction de cette configuration.

1. Pour limiter le nombre de demandes de réinitialisation de mot de passe envoyées par heure, procédez comme suit :

   - Pour **[!UICONTROL Max Number of Password Reset Requests]**, saisissez le nombre maximal de demandes de réinitialisation de mot de passe qui peuvent être envoyées par heure.

   - Pour **[!UICONTROL Min Time Between Password Reset Requests]**, saisissez le nombre minimum de minutes qui doivent s’écouler entre les requêtes.

1. Pour configurer la notification électronique de réinitialisation du mot de passe, procédez comme suit :

   - Définir **[!UICONTROL Forgot Email Template]** au modèle utilisé pour l’email envoyé aux clients qui ont oublié leurs mots de passe.

   - Définir **[!UICONTROL Remind Email Template]** au modèle utilisé lorsqu’un utilisateur administrateur réinitialise un mot de passe client.

   - Définir **[!UICONTROL Reset Password Template]** au modèle utilisé lorsque les clients modifient leurs mots de passe.

   - Définir **[!UICONTROL Password Template Email Sender]** à la fonction [contact de magasin](../getting-started/store-details.md) qui s’affiche comme expéditeur de notifications liées au mot de passe.

1. Renseignez les options de sécurité de réinitialisation de mot de passe suivantes :

   - Pour **[!UICONTROL Recovery Link Expiration Period (hours)]**, saisissez le nombre d’heures avant l’expiration du lien de récupération du mot de passe.

   - Si vous souhaitez que les champs de la connexion client et des formulaires de mot de passe soient automatiquement renseignés à partir des entrées précédentes, définissez **[!UICONTROL Enable Autocomplete on login/forgot password forms]** to `Yes`.

   - Pour **[!UICONTROL Number of Required Character Classes]**, saisissez le nombre de types de caractères différents qui doivent être inclus dans un mot de passe en fonction des classes de caractères suivantes :

      - `Lowercase`
      - `Uppercase`
      - `Numeric`
      - `Special Characters`

   - Pour **[!UICONTROL Maximum Login Failures to Lockout Account]**, saisissez le nombre de tentatives de connexion ayant échoué jusqu’à ce que le compte client soit verrouillé. Pour les tentatives illimitées, saisissez zéro (`0`).

   - Pour **[!UICONTROL Minimum Password Length]**, saisissez le nombre minimum de caractères pouvant être utilisés dans un mot de passe. Le nombre doit être supérieur à zéro.

   - Pour **[!UICONTROL Lockout Time (minutes)]**, saisissez le nombre de minutes pendant lesquelles un compte client est verrouillé après l’échec de trop de tentatives de connexion.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.
