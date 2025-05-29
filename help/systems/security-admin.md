---
title: Configuration de la sécurité de l’administrateur
description: Découvrez comment configurer la sécurité pour l’administrateur de votre boutique.
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# Configuration de la sécurité de l’administrateur

Nous vous recommandons d’adopter une approche multidimensionnelle pour protéger la sécurité de votre magasin. Vous pouvez commencer par utiliser une [URL d’administration personnalisée](../stores-purchase/store-urls.md#use-a-custom-admin-url) difficile à deviner, plutôt que l’évidente « Administration » ou « Serveur principal ». Par défaut, les mots de passe utilisés pour [se connecter](../getting-started/admin-signin.md) à l’administrateur doivent comporter sept caractères ou plus, ainsi que des lettres et des chiffres. En [bonne pratique](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html), utilisez uniquement des mots de passe d’administration forts qui incluent une combinaison de lettres, de chiffres et de symboles. Adobe Commerce et Magento Open Source n’autorisent pas la réutilisation des quatre derniers mots de passe attribués au compte.

La configuration de sécurité d’administration vous permet d’effectuer les opérations suivantes :

- Ajout d’une clé secrète aux URL
- Exiger que les mots de passe respectent la casse
- Limiter la durée des sessions Admin
- Limiter la durée de vie des mots de passe
- Limitez le nombre de tentatives de connexion avant que le compte utilisateur administrateur ne soit [ verrouillé](permissions-users-all.md#locked-users).

Pour une sécurité renforcée, vous pouvez configurer la durée d’inactivité du clavier avant l’expiration de la session en cours et exiger que le nom d’utilisateur et le mot de passe soient sensibles à la casse.

Outre les paramètres de sécurité de cette section, l’[authentification à deux facteurs](security-two-factor-authentication.md) (2FA) est nécessaire pour vérifier l’identité des utilisateurs à l’aide d’un mot de passe à usage unique généré par une application ou un appareil. La première fois que vous vous connectez à l’administrateur, vous êtes invité à configurer 2FA. Pour plus de sécurité, la connexion d’administrateur peut également être configurée pour nécessiter un [ CAPTCHA ](security-captcha.md).

>[!NOTE]
>
>Les magasins qui ont activé l’authentification [!DNL Adobe Identity Management Services] (IMS) ont Adobe Commerce et Magento Open Source 2FA natifs désactivés. Les utilisateurs administrateurs connectés à leur instance Commerce avec leurs informations d’identification Adobe n’ont pas besoin de s’authentifier à nouveau pour de nombreuses tâches d’administration. L’authentification est gérée par Adobe IMS lorsque l’utilisateur administrateur se connecte à sa session en cours. Voir Présentation de l’intégration [[!DNL Adobe Identity Management Service] (IMS)](../getting-started/adobe-ims-integration-overview.md).

Pour obtenir des informations techniques, voir [Présentation de la sécurité](https://developer.adobe.com/commerce/php/architecture/basics/security/){:target="_blank"} dans la documentation destinée aux développeurs.

![Sécurité de l’administrateur](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## Configuration de la sécurité de l’administrateur

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche sous _[!UICONTROL Advanced]_, choisissez **[!UICONTROL Admin]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Security]** .

1. Pour empêcher les utilisateurs administrateurs de se connecter à partir du même compte sur différents appareils, définissez **[!UICONTROL Admin Account Sharing]** sur `No`.

1. Pour déterminer la méthode utilisée pour gérer les demandes de réinitialisation de mot de passe, définissez **[!UICONTROL Password Reset Protection Type]** sur l’une des méthodes suivantes :

   - `By IP and Email` — Le mot de passe peut être réinitialisé en ligne après réception d&#39;une réponse de la notification envoyée à l&#39;adresse e-mail associée au compte d&#39;administrateur.
   - `By IP` — Le mot de passe peut être réinitialisé en ligne sans confirmation supplémentaire.
   - `By Email` — Le mot de passe ne peut être réinitialisé qu&#39;en répondant par e-mail à la notification envoyée à l&#39;adresse e-mail associée au compte Admin.
   - `None` — Seul l&#39;administrateur du magasin peut réinitialiser le mot de passe.

1. Définissez les options de sécurité de connexion :

   - Par **[!UICONTROL Recovery Link Expiration Period (hours)]**, saisissez le nombre d’heures pendant lesquelles un lien de récupération du mot de passe reste valide.

   - Pour déterminer le nombre maximal de demandes de mot de passe qui peuvent être envoyées par heure, saisissez le nombre pour **[!UICONTROL Max Number of Password Reset Requests]**.

   - Par **[!UICONTROL Min Time Between Password Reset Requests]**, saisissez le nombre minimum de minutes qui doit s’écouler entre les demandes de réinitialisation de mot de passe.

   - Pour ajouter une clé secrète à l’URL d’administration par mesure de précaution contre les exploits, définissez **[!UICONTROL Add Secret Key to URLs]** sur `Yes`. Ce paramètre est activé par défaut.

   - Pour exiger que l’utilisation de caractères majuscules et minuscules dans toutes les informations d’identification saisies corresponde à ce qui est stocké dans le système, définissez **[!UICONTROL Login is Case Sensitive]** sur `Yes`.

   - Pour déterminer la durée d’une session d’administrateur avant qu’elle n’expire, saisissez la durée de la session en secondes pour **[!UICONTROL Admin Session Lifetime (seconds)]** champ . La valeur doit être supérieure ou égale à 60 secondes.

   - Par **[!UICONTROL Maximum Login Failures to Lockout Account]**, saisissez le nombre de fois qu’un utilisateur peut essayer de se connecter à l’administrateur avant que le compte ne soit verrouillé. Par défaut, six tentatives sont autorisées. Laissez le champ vide pour un nombre illimité de tentatives de connexion.

   - Par **[!UICONTROL Lockout Time (minutes)]**, saisissez le nombre de minutes pendant lesquelles un compte d’administrateur est verrouillé lorsque le nombre maximal de tentatives est atteint.

1. Définissez les options de mot de passe :

   - Pour limiter la durée de vie des mots de passe d’administration, saisissez le nombre de jours pendant lesquels un mot de passe est valide pour **[!UICONTROL Password Lifetime (days)]**. Pour une durée de vie illimitée, laissez le champ vide.

   - Définissez **[!UICONTROL Password Change]** sur l’une des options suivantes :

      - `Forced` — Nécessite que les utilisateurs administrateurs changent leurs mots de passe après la configuration du compte.
      - `Recommended` — Recommande aux utilisateurs administrateurs de modifier leurs mots de passe après la configuration du compte.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Exigences de mot de passe administrateur

Par défaut, un mot de passe administrateur doit comporter au moins sept caractères et inclure des lettres et des chiffres.
