---
title: Gestion de session
description: Découvrez comment configurer la gestion des sessions pour sécuriser l’administrateur et le storefront.
exl-id: ad954218-aa3e-44e6-b23f-008de7fc7543
role: Admin
feature: Configuration, Security
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# Gestion de session

La [gestion de session](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html) est une bonne pratique de lutte contre le déni de service (DoS) pour la sécurité des API. Une session représente le temps passé par un visiteur sur votre site et n’est pas liée à la durée de connexion des utilisateurs administrateurs ou des clients à leurs comptes.

Une session est une séquence de transactions de requête HTTP réseau et de réponse associées au même utilisateur. Il s’agit d’une méthode d’association d’un client (Admin) à ses données lorsqu’il accède au serveur. Les sessions sont utilisées pour établir des variables, telles que les droits d’accès et les paramètres de localisation, qui s’appliquent à chaque interaction d’un utilisateur avec une application web au cours de la session.

## Taille de la session

Utilisez les paramètres de configuration suivants pour limiter la taille de session maximale pour les utilisateurs administrateurs et les visiteurs du storefront :

- **[!UICONTROL Max Session Size in Admin]** : limite la taille maximale des sessions en octets. Utilisez `0` pour désactiver.
- **[!UICONTROL Max Session Size in Storefront]** : limite la taille maximale des sessions en octets. Utilisez `0` pour désactiver.

>[!TIP]
>
>Les deux paramètres sont mesurés en octets et la valeur par défaut est de `256000` octets (ou 256 Ko).

**_Pour configurer la taille de session maximale, procédez comme suit_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Security]** pour accéder aux paramètres de la session.

   ![Paramètres de session](../configuration-reference/advanced/assets/system-security.png){width="600" zoomable="yes"}

1. Saisissez les nouvelles tailles de session en octets.

   >[!WARNING]
   >
   >Une valeur trop basse peut entraîner des problèmes. Si vous définissez l’une des options sous la valeur par défaut de 256000 octets, un message d’avertissement s’affiche. Si vous cliquez sur **[!UICONTROL No]**, le système modifie la valeur en `256000`.

1. Cliquez sur **[!UICONTROL Save Config]**.

### Sessions d’administrateur

Si vous dépassez la taille de session maximale, un message d’erreur s’affiche et le système consigne la contrainte de taille de session dans le répertoire `var/log`.

Si vous perdez l’accès à l’administrateur après avoir défini une taille de session trop basse, utilisez l’interface de ligne de commande pour réinitialiser la configuration :

```bash
bin/magento config:set system/security/max_session_size_admin 256000
```

### Sessions Storefront

Si vous dépassez la taille de session maximale, aucune erreur ne s’affiche, mais le système consigne la contrainte de taille de session dans le répertoire `var/log`.

## Validation de session

Adobe Commerce et Magento Open Source vous permettent de valider les variables de session à titre de mesure de protection contre d’éventuelles attaques de fixation de session ou tentatives d’empoisonnement ou de détournement de sessions utilisateur. Les paramètres de validation de session déterminent la manière dont les variables de session sont validées lors de chaque visite de la boutique et si l’ID de session est inclus dans l’URL de la boutique.

Pour plus d’informations techniques, voir [Utilisation de Redis pour le stockage de session](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-session.html) dans le _Guide de configuration_.

![Configuration générale - Validation des sessions web](../configuration-reference/general/assets/web-session-validation-settings.png){width="600" zoomable="yes"}

La validation vérifie que les visiteurs sont bien ce qu’ils disent être en comparant la valeur des variables de validation avec les données de session stockées dans les données de `$_SESSION` pour l’utilisateur. La validation échoue si les informations ne sont pas transmises comme prévu et que la variable correspondante est vide. En fonction des paramètres de validation de session, si une variable de session échoue dans le processus de validation, la session cliente s’arrête immédiatement.

L’activation de toutes les variables de validation peut prévenir les attaques, mais peut également avoir un impact sur les performances du serveur. Par défaut, toutes les validations de variables de session sont désactivées. Nous vous recommandons de tester les paramètres afin de trouver la meilleure combinaison pour votre installation d’Adobe Commerce ou de Magento Open Source. L’activation de toutes les variables de validation peut s’avérer indûment restrictive et peut empêcher l’accès aux clients qui disposent de connexions Internet passant par un serveur proxy ou provenant de l’arrière d’un pare-feu. Pour en savoir plus sur les variables de session et leur utilisation, consultez la documentation d’administration système de votre système Linux®.

**_Pour configurer la validation de la session, procédez comme suit_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez _[!UICONTROL General]_&#x200B;et choisissez **[!UICONTROL Web]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Session Validation Settings]** .

1. Définissez chacune des options de configuration :

   - **[!UICONTROL Validate REMOTE_ADDR]** — Définissez sur `Yes` pour vérifier que l&#39;adresse IP d&#39;une requête correspond à ce qui est stocké dans la variable `$_SESSION`.

   - **[!UICONTROL Validate HTTP_VIA]** — Définissez sur `Yes` pour vérifier que l&#39;adresse proxy d&#39;une requête entrante correspond à ce qui est stocké dans la variable `$_SESSION`.

   - **[!UICONTROL Validate HTTP_X_FORWARDED_FOR]** — Définissez sur `Yes` pour vérifier que l&#39;adresse de transfert d&#39;une requête correspond à ce qui est stocké dans la variable `$_SESSION`.

   - **[!UICONTROL Validate HTTP_USER_AGENT]** — Définissez sur `Yes` pour vérifier que le navigateur ou l’appareil utilisé pour accéder au magasin au cours d’une session correspond à ce qui est stocké dans la variable `$_SESSION`.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Durée de vie d’une session d’administrateur

Par mesure de sécurité, le _Admin_ est initialement configuré pour expirer après 900 secondes (15 minutes) d’inactivité du clavier. Vous pouvez ajuster la durée de vie de la session en fonction de votre style de travail.

**_Pour ajuster la durée de vie d’une session d’administrateur :_**

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Faites défiler vers le bas et développez **[!UICONTROL Advanced]** dans le panneau latéral gauche.

1. Cliquez sur **[!UICONTROL Admin]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Security]** .

1. Par **[!UICONTROL Admin Session Lifetime (seconds)]**, saisissez le nombre de secondes pendant lesquelles une session reste active avant d’expirer.

   ![Configuration avancée - Paramètres de sécurité d’administration](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
