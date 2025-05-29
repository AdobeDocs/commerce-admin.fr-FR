---
title: CAPTCHA
description: Découvrez comment configurer CAPTCHA pour l’accès administrateur et les différentes actions de storefront initiées par les clients enregistrés.
exl-id: b2867ad5-7d48-4e9f-b84e-3cf0a14ec16f
role: Admin
feature: Configuration, Security
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '959'
ht-degree: 0%

---

# CAPTCHA

Un CAPTCHA est un appareil visuel qui garantit qu’un être humain, plutôt qu’un ordinateur (ou « robot »), interagit avec le site. CAPTCHA est un acronyme pour _Completely Automated Public Turing test to tell Computers and Humans Apart_. Il peut être utilisé pour l’accès administrateur et diverses actions de storefront initiées par les clients enregistrés. Adobe Commerce et Magento Open Source prennent en charge le CAPTCHA standard décrit dans cette rubrique et le [reCAPTCHA Google](security-google-recaptcha.md).

Vous pouvez recharger le CAPTCHA autant de fois que nécessaire en cliquant sur l’icône Recharger dans le coin supérieur droit de l’image. Le CAPTCHA est entièrement configurable et peut être défini pour apparaître à chaque fois, ou uniquement après un nombre défini d’échecs de tentatives de connexion.

![Connexion avec CAPTCHA](./assets/customer-account-login-captcha.png){width="700" zoomable="yes"}

## Configuration de CAPTCHA pour l’administrateur

Pour un niveau de sécurité supplémentaire, vous pouvez ajouter un CAPTCHA à la page Connexion administrateur et mot de passe oublié . Les utilisateurs administrateurs peuvent recharger le CAPTCHA affiché en cliquant sur l’icône _Recharger_ ![icône de rechargement](./assets/CAPTCHA-icon-reload.png) dans le coin supérieur droit de l’image. Le nombre de rechargements est illimité.

![Administrateur - Se connecter avec CAPTCHA](./assets/security-captcha-admin.png){width="300"}

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Admin]**.

1. Dans le coin supérieur droit, définissez **[!UICONTROL Store View]** sur `Default`.

   Si la [portée](../getting-started/websites-stores-views.md#scope-settings) de votre installation Commerce comprend plusieurs sites web, sélectionnez les sites web auxquels vous souhaitez appliquer la configuration CAPTCHA.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL CAPTCHA]** .

1. Définissez **[!UICONTROL Enable CAPTCHA in Admin]** sur `Yes`. Renseignez ensuite les options restantes comme suit :

   ![Administrateur - Configuration de CAPTCHA](../configuration-reference/advanced/assets/admin-captcha.png){width="600" zoomable="yes"}

   - Saisissez le nom du **[!UICONTROL Font]** à utiliser pour les symboles CAPTCHA (par défaut : `LinLibertine`).

     Pour ajouter votre propre police, celle-ci doit se trouver dans le même répertoire que l’installation Commerce et doit être déclarée dans le fichier `config.xml` du module Captcha à l’adresse `app/code/Magento/Captcha/etc`.

   - Sélectionnez l’une des **[!UICONTROL Forms]** suivantes où le CAPTCHA doit être utilisé. Pour choisir plusieurs formulaires, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée.

      - `Admin Login`
      - `Admin Forgot Password`

   - Définissez **[!UICONTROL Displaying Modes]** sur l’une des options suivantes :

      - `Always` — CAPTCHA est toujours nécessaire pour se connecter à l&#39;administrateur.
      - `After number of attempts to login` — Cette option s&#39;applique uniquement au formulaire de connexion de l&#39;administrateur. Lorsque cette option est sélectionnée, le champ _[!UICONTROL Number of Unsuccessful Attempts to Login]_&#x200B;s’affiche. Saisissez le nombre de tentatives de connexion que vous souhaitez autoriser. Une valeur de 0 (zéro) est similaire à la définition du mode d’affichage sur `Always`.

     Pour suivre le nombre de tentatives de connexion infructueuses, chaque tentative de connexion sous une adresse e-mail et à partir d’une adresse IP est comptabilisée. Le nombre maximal de tentatives de connexion autorisées à partir de la même adresse IP est de 1 000. Cette limitation s’applique uniquement lorsque le CAPTCHA est activé.

   - Par **[!UICONTROL Number of Unsuccessful Attempts to Login]**, saisissez le nombre de fois où l’administrateur peut essayer de se connecter avant l’affichage du CAPTCHA. S’il est défini sur zéro (`0`), le CAPTCHA est toujours requis.

   - Par **[!UICONTROL CAPTCHA Timeout (minutes)]**, saisissez le nombre de minutes avant l’expiration du CAPTCHA. Lorsque le CAPTCHA expire, l’administrateur ou l’administratrice doit recharger la page.

   - Saisissez le **[!UICONTROL Number of Symbols]** à afficher dans le CAPTCHA. Vous pouvez utiliser jusqu’à huit (`8`) symboles. Pour un nombre variable de symboles qui change avec chaque CAPTCHA, saisissez une plage (telle que `5-8`).

   - Par **[!UICONTROL Symbols Used in CAPTCHA]**, saisissez les lettres (a-z et A-Z) et les chiffres (0-9) que vous souhaitez afficher de manière aléatoire dans le CAPTCHA. Les symboles difficiles à distinguer des autres symboles, tels que `i`, `l` ou `1`, ne sont pas inclus dans l’ensemble par défaut des symboles CAPTCHA.

   - Définissez **[!UICONTROL Case Sensitive]** sur `Yes` si vous souhaitez que les administrateurs saisissent les caractères en majuscules ou en minuscules exactement comme indiqué dans le CAPTCHA.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Configuration de CAPTCHA pour le storefront

Les clients peuvent être amenés à saisir un CAPTCHA à chaque connexion à leur compte ou après plusieurs tentatives infructueuses de connexion. En outre, de nombreux formulaires utilisés dans l’ensemble du storefront peuvent être configurés pour nécessiter une vérification par CAPTCHA.

![CAPTCHA lors du passage en caisse](./assets/storefront-checkout-payment-captcha.png){width="700" zoomable="yes"}

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Customer Configuration]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL CAPTCHA]** .

![Configuration du CAPTCHA du client](../configuration-reference/customers/assets/customer-configuration-captcha.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Enable CAPTCHA on Storefront]** sur `Yes`. Renseignez ensuite les options restantes comme suit :

   - Saisissez le nom du **[!UICONTROL Font]** à utiliser pour les symboles CAPTCHA (par défaut : `LinLibertine`).

     Pour ajouter votre propre police, le fichier de police doit résider dans le même répertoire que votre installation Commerce et doit être déclaré dans le fichier `config.xml` du module CAPTCHA.

   - Sélectionnez l’une des **[!UICONTROL Forms]** suivantes où le CAPTCHA doit être utilisé. Pour choisir plusieurs formulaires, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée.

      - `Applying coupon code`
      - `Checkout/Placing Order`
      - `Create user`
      - `Login`
      - `Forgot password`
      - `Contact Us`
      - `Change password`
      - `Share Wishlist Form`
      - `Payflow Pro` (voir l’article [correctif de sécurité](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/paypal-payflow-pro-active-carding-activity.html) _Base de connaissances_)
      - `Send to Friend Form` ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement)
      - `Add Gift Card Code` ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement)
      - `Create company` ![Adobe Commerce B2B](../assets/b2b.svg) (disponible avec Adobe Commerce B2B uniquement)

   - Définissez **[!UICONTROL Displaying Mode]** sur l’une des options suivantes :

      - `Always` — CAPTCHA est toujours nécessaire pour accéder aux formulaires sélectionnés.
      - `After number of attempts to login` — Saisissez le nombre de tentatives de connexion avant l&#39;affichage du CAPTCHA. Une valeur de 0 (zéro) est similaire à « Toujours ». Lorsque cette option est sélectionnée, le nombre de tentatives de connexion infructueuses s’affiche. Cette option ne s’applique pas au formulaire Mot de passe oublié qui, s’il est activé, affiche toujours le CAPTCHA.

   - Par **[!UICONTROL Number of Unsuccessful Attempts to Login]**, saisissez le nombre de fois où un client peut se connecter sans succès avant l’affichage du CAPTCHA. S’il est défini sur zéro (`0`), le CAPTCHA est toujours utilisé.

   - Par **[!UICONTROL CAPTCHA Timeout (minutes)]**, saisissez le nombre de minutes avant l’expiration du CAPTCHA. Lorsque le CAPTCHA expire, le ou la client(e) doit recharger la page pour générer un nouveau CAPTCHA.

   - Saisissez le **[!UICONTROL Number of Symbols]** à afficher dans le CAPTCHA. Vous pouvez utiliser jusqu’à huit (`8`) symboles. Pour un nombre variable de symboles qui change avec chaque CAPTCHA, saisissez une plage (telle que `5-8`).

   - Par **[!UICONTROL Symbols Used in CAPTCHA]**, saisissez les lettres (a-z et A-Z) et les chiffres (0-9) que vous souhaitez afficher de manière aléatoire dans le CAPTCHA. Le jeu de caractères par défaut n’inclut pas de symboles similaires tels que `I` ou `1`. Pour de meilleurs résultats, utilisez des symboles que les utilisateurs peuvent identifier facilement.

   - Définissez **[!UICONTROL Case Sensitive]** sur `Yes` si vous souhaitez que les clients saisissent les caractères en majuscules ou en minuscules exactement comme indiqué dans le CAPTCHA.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
