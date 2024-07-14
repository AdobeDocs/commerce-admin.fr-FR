---
title: Configuration de la sécurité d’administration
description: Découvrez comment configurer la sécurité pour votre administrateur de magasin.
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
source-git-commit: e301cfaeec3a8427fff6138ba041bdbd7433c137
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 0%

---

# Configuration de la sécurité d’administration

Nous vous recommandons d’adopter une approche multidimensionnelle pour protéger la sécurité de votre magasin. Vous pouvez commencer par utiliser une [URL d’administration personnalisée](../stores-purchase/store-urls.md#use-a-custom-admin-url) qui n’est pas facile à deviner, plutôt que l’évident &quot;Admin&quot; ou &quot;Serveur principal&quot;. Par défaut, les mots de passe utilisés pour [se connecter](../getting-started/admin-signin.md) à l’administrateur doivent comporter au moins sept caractères et contenir à la fois des lettres et des chiffres. En tant que [ bonne pratique](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html), utilisez uniquement des mots de passe administrateur difficiles à deviner qui incluent une combinaison de lettres, de chiffres et de symboles. Adobe Commerce et Magento Open Source ne permettent pas la réutilisation des quatre derniers mots de passe affectés au compte.

La configuration relative à la sécurité de l’administrateur vous permet d’effectuer les opérations suivantes :

- Ajout d’une clé secrète aux URL
- Requiert que les mots de passe soient sensibles à la casse
- Limitation de la durée des sessions d’administration
- Limiter la durée de vie des mots de passe
- Limitez le nombre de tentatives de connexion qui peuvent être effectuées avant que le compte d’utilisateur administrateur soit [verrouillé](permissions-users-all.md#locked-users).

Pour une sécurité accrue, vous pouvez configurer la durée d’inactivité du clavier avant l’expiration de la session en cours et exiger que le nom d’utilisateur et le mot de passe soient sensibles à la casse.

Outre les paramètres de sécurité de cette section, l’ [authentification à deux facteurs](security-two-factor-authentication.md) (2FA) est nécessaire pour vérifier l’identité des utilisateurs avec un mot de passe unique généré par une application ou un appareil. Vous êtes invité à configurer 2FA la première fois que vous vous connectez à l’administrateur. Pour plus de sécurité, la connexion administrateur peut également être configurée pour exiger un [CAPTCHA](security-captcha.md).

>[!NOTE]
>
>Les magasins qui ont activé l’authentification [!DNL Adobe Identity Management Services] (IMS) ont natif Adobe Commerce et Magento Open Source 2FA désactivé. Les utilisateurs administrateurs connectés à leur instance Commerce avec leurs informations d’identification d’Adobe n’ont pas besoin de se réauthentifier pour de nombreuses tâches d’administration. L’authentification est gérée par Adobe IMS lorsque l’utilisateur administrateur se connecte à sa session en cours. Voir [[!DNL Adobe Identity Management Service] (IMS) Présentation de l’intégration ](../getting-started/adobe-ims-integration-overview.md).

Pour plus d’informations techniques, voir [Présentation de la sécurité](https://developer.adobe.com/commerce/php/architecture/basics/security/){:target=&quot;_blank&quot;} dans la documentation destinée aux développeurs.

![Sécurité de l’administrateur](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## Configuration de la sécurité d’administration

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche sous _[!UICONTROL Advanced]_, choisissez **[!UICONTROL Admin]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Security]** .

1. Pour empêcher les utilisateurs administrateurs de se connecter à partir du même compte sur différents appareils, définissez **[!UICONTROL Admin Account Sharing]** sur `No`.

1. Pour déterminer la méthode utilisée pour gérer les demandes de réinitialisation de mot de passe, définissez **[!UICONTROL Password Reset Protection Type]** sur l’une des options suivantes :

   - `By IP and Email` : le mot de passe peut être réinitialisé en ligne après réception d’une réponse à partir de la notification et envoyée à l’adresse électronique associée au compte administrateur.
   - `By IP` — Le mot de passe peut être réinitialisé en ligne sans confirmation supplémentaire.
   - `By Email` : le mot de passe ne peut être réinitialisé qu’en répondant par courrier électronique à la notification envoyée à l’adresse électronique associée au compte administrateur.
   - `None` — Le mot de passe ne peut être réinitialisé que par l’administrateur du magasin.

1. Définissez les options de sécurité de connexion :

   - Pour **[!UICONTROL Recovery Link Expiration Period (hours)]**, saisissez le nombre d’heures pendant lesquelles un lien de récupération de mot de passe reste valide.

   - Pour déterminer le nombre maximal de demandes de mot de passe qui peuvent être envoyées par heure, saisissez le nombre pour **[!UICONTROL Max Number of Password Reset Requests]**.

   - Pour **[!UICONTROL Min Time Between Password Reset Requests]**, saisissez le nombre minimum de minutes qui doivent s’écouler entre les demandes de réinitialisation de mot de passe.

   - Pour ajouter une clé secrète à l’URL d’administration par mesure de précaution contre les exploits, définissez **[!UICONTROL Add Secret Key to URLs]** sur `Yes`. Ce paramètre est activé par défaut.

   - Pour exiger que l’utilisation de caractères majuscules et minuscules dans les informations d’identification de connexion saisies corresponde à ce qui est stocké dans le système, définissez **[!UICONTROL Login is Case Sensitive]** sur `Yes`.

   - Pour déterminer la durée d’une session d’administrateur avant son expiration, saisissez la durée de la session en secondes pour le champ **[!UICONTROL Admin Session Lifetime (seconds)]** . La valeur doit être de 60 secondes ou plus.

   - Pour **[!UICONTROL Maximum Login Failures to Lockout Account]**, saisissez le nombre de fois où un utilisateur peut essayer de se connecter à l’administrateur avant que le compte ne soit verrouillé. Par défaut, six tentatives sont autorisées. Laissez le champ vide pour un nombre illimité de tentatives de connexion.

   - Pour **[!UICONTROL Lockout Time (minutes)]**, saisissez le nombre de minutes de verrouillage d’un compte administrateur lorsque le nombre maximum de tentatives est atteint.

1. Définition des options de mot de passe :

   - Pour limiter la durée de vie des mots de passe administrateur, saisissez le nombre de jours pendant lesquels un mot de passe est valide pour **[!UICONTROL Password Lifetime (days)]**. Pour une durée de vie illimitée, laissez le champ vide.

   - Définissez **[!UICONTROL Password Change]** sur l’une des options suivantes :

      - `Forced` — Nécessite que les utilisateurs administrateurs modifient leurs mots de passe après la configuration du compte.
      - `Recommended` — Recommande aux utilisateurs administrateurs de modifier leurs mots de passe après la configuration du compte.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

## Exigences en matière de mot de passe administrateur

Par défaut, un mot de passe administrateur doit comporter au moins sept caractères et contenir à la fois des lettres et des chiffres.
