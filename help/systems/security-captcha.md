---
title: CAPTCHA
description: Découvrez comment configurer CAPTCHA pour l’accès administrateur et diverses actions de storefront initiées par les clients enregistrés.
exl-id: b2867ad5-7d48-4e9f-b84e-3cf0a14ec16f
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---

# CAPTCHA

Un CAPTCHA est un appareil visuel qui garantit qu&#39;un être humain, plutôt qu&#39;un ordinateur (ou &quot;robot&quot;), interagit avec le site. CAPTCHA est un acronyme pour _Test public de Turing entièrement automatisé pour informer les ordinateurs et les humains de leur éparpillement_. Il peut être utilisé pour l’accès administrateur et pour diverses actions storefront initiées par les clients enregistrés. Adobe Commerce et Magento Open Source prennent en charge le CAPTCHA standard décrit dans cette rubrique et [Google reCAPTCHA](security-google-recaptcha.md).

Vous pouvez recharger le CAPTCHA autant de fois que nécessaire en cliquant sur l’icône Recharger dans le coin supérieur droit de l’image. Le CAPTCHA est entièrement configurable et peut être défini pour s’afficher à chaque fois ou uniquement après un nombre défini de tentatives de connexion ayant échoué.

![Connexion avec CAPTCHA](./assets/customer-account-login-captcha.png){width="700" zoomable="yes"}

## Configuration de CAPTCHA pour l’administrateur

Pour un niveau de sécurité supplémentaire, vous pouvez ajouter un CAPTCHA à la page Admin Se connecter et Mot de passe oublié . Les utilisateurs administrateurs peuvent recharger le CAPTCHA affiché en cliquant sur le bouton _Recharger_ ![icône de rechargement](./assets/CAPTCHA-icon-reload.png) dans le coin supérieur droit de l’image. Le nombre de rechargements est illimité.

![Administration - Connexion avec CAPTCHA](./assets/security-captcha-admin.png){width="300"}

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Admin]**.

1. Dans le coin supérieur droit, définissez **[!UICONTROL Store View]** to `Default`.

   Si la variable [scope](../getting-started/websites-stores-views.md#scope-settings) de votre installation Commerce comprend plusieurs sites web, sélectionnez les sites web auxquels vous souhaitez appliquer la configuration CAPTCHA.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL CAPTCHA]** .

1. Définir **[!UICONTROL Enable CAPTCHA in Admin]** to `Yes`. Renseignez ensuite les autres options comme suit :

   ![Admin - Configuration CAPTCHA](../configuration-reference/advanced/assets/admin-captcha.png){width="600" zoomable="yes"}

   - Saisissez le nom du **[!UICONTROL Font]** à utiliser pour les symboles CAPTCHA (par défaut : `LinLibertine`).

     Pour ajouter votre propre police, le fichier de police doit se trouver dans le même répertoire que votre installation Commerce et doit être déclaré dans la variable `config.xml` fichier du module Captcha à l’adresse `app/code/Magento/Captcha/etc`.

   - Sélectionnez l’une des options suivantes : **[!UICONTROL Forms]** où le CAPTCHA doit être utilisé. Pour sélectionner plusieurs formulaires, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée.

      - `Admin Login`
      - `Admin Forgot Password`

   - Définir **[!UICONTROL Displaying Modes]** à l’une des options suivantes :

      - `Always` — CAPTCHA est toujours nécessaire pour se connecter à l’administrateur.
      - `After number of attempts to login` — Cette option s’applique uniquement au formulaire Connexion d’administrateur. Lorsque cette option est sélectionnée, la variable _[!UICONTROL Number of Unsuccessful Attempts to Login]_s’affiche. Saisissez le nombre de tentatives de connexion que vous souhaitez autoriser. Une valeur de 0 (zéro) est similaire au paramètre Mode d’affichage défini sur `Always`.

     Pour suivre le nombre de tentatives de connexion infructueuses, chaque tentative de connexion sous une adresse électronique et depuis une adresse IP est comptabilisée. Le nombre maximal de tentatives de connexion autorisées à partir d’une même adresse IP est de 1 000. Cette limitation s’applique uniquement lorsque CAPTCHA est activé.

   - Pour **[!UICONTROL Number of Unsuccessful Attempts to Login]**, saisissez le nombre de fois où l’administrateur peut tenter de se connecter avant que CAPTCHA n’apparaisse. Si elle est définie sur zéro (`0`), CAPTCHA est toujours requis.

   - Pour **[!UICONTROL CAPTCHA Timeout (minutes)]**, saisissez le nombre de minutes avant l’expiration du CAPTCHA. Lorsque le CAPTCHA expire, l’administrateur doit recharger la page.

   - Saisissez le **[!UICONTROL Number of Symbols]** pour apparaître dans le CAPTCHA. Jusqu’à huit (`8`) peuvent être utilisés. Pour un nombre variable de symboles qui change avec chaque CAPTCHA, saisissez une plage (telle que `5-8`).

   - Pour **[!UICONTROL Symbols Used in CAPTCHA]**, saisissez les lettres (a-z et A-Z) et les chiffres (0-9) que vous souhaitez afficher de manière aléatoire dans le CAPTCHA. Symboles difficiles à distinguer des autres symboles, tels que `i`, `l`, ou `1`, ne sont pas inclus dans l’ensemble par défaut des symboles CAPTCHA.

   - Définir **[!UICONTROL Case Sensitive]** to `Yes` si vous souhaitez exiger des administrateurs qu’ils saisissent les caractères en majuscules ou en minuscules exactement comme indiqué dans le CAPTCHA.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

## Configuration de CAPTCHA pour le storefront

Les clients peuvent être tenus d’entrer un CAPTCHA chaque fois qu’ils se connectent à leurs comptes ou après plusieurs tentatives infructueuses de connexion. De plus, de nombreux formulaires utilisés sur le storefront peuvent être configurés pour exiger une vérification par CAPTCHA.

![CAPTCHA lors du passage en caisse](./assets/storefront-checkout-payment-captcha.png){width="700" zoomable="yes"}

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Customer Configuration]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL CAPTCHA]** .

![Configuration de CAPTCHA client](../configuration-reference/customers/assets/customer-configuration-captcha.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Enable CAPTCHA on Storefront]** to `Yes`. Renseignez ensuite les autres options comme suit :

   - Saisissez le nom du **[!UICONTROL Font]** à utiliser pour les symboles CAPTCHA (par défaut : `LinLibertine`).

     Pour ajouter votre propre police, le fichier de police doit se trouver dans le même répertoire que votre installation Commerce et doit être déclaré dans la variable `config.xml` du module CAPTCHA.

   - Sélectionnez l’une des options suivantes : **[!UICONTROL Forms]** où le CAPTCHA doit être utilisé. Pour sélectionner plusieurs formulaires, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée.

      - `Applying coupon code`
      - `Checkout/Placing Order`
      - `Create user`
      - `Login`
      - `Forgot password`
      - `Contact Us`
      - `Change password`
      - `Share Wishlist Form`
      - `Payflow Pro` (voir [correctif de sécurité](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/paypal-payflow-pro-active-carding-activity.html) _Base de connaissances_ article)
      - `Send to Friend Form` ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement)
      - `Add Gift Card Code` ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement)
      - `Create company` ![B2B pour Adobe Commerce](../assets/b2b.svg) (Disponible avec B2B pour Adobe Commerce uniquement)

   - Définir **[!UICONTROL Displaying Mode]** à l’une des options suivantes :

      - `Always` — CAPTCHA est toujours nécessaire pour accéder aux formulaires sélectionnés.
      - `After number of attempts to login` — Saisissez le nombre de tentatives de connexion avant que CAPTCHA n’apparaisse. Une valeur de 0 (zéro) est similaire à &quot;Toujours&quot;. Lorsque cette option est sélectionnée, le nombre de tentatives de connexion infructueuses s’affiche. Cette option ne s’applique pas au formulaire Mot de passe oublié qui, s’il est activé, affiche toujours le CAPTCHA.

   - Pour **[!UICONTROL Number of Unsuccessful Attempts to Login]**, saisissez le nombre de fois où un client peut se connecter sans succès avant que CAPTCHA n’apparaisse. Si elle est définie sur zéro (`0`), CAPTCHA est toujours utilisé.

   - Pour **[!UICONTROL CAPTCHA Timeout (minutes)]**, saisissez le nombre de minutes avant l’expiration du CAPTCHA. Lorsque le CAPTCHA expire, le client doit recharger la page pour générer un nouveau CAPTCHA.

   - Saisissez le **[!UICONTROL Number of Symbols]** pour apparaître dans le CAPTCHA. Jusqu’à huit (`8`) peuvent être utilisés. Pour un nombre variable de symboles qui change avec chaque CAPTCHA, saisissez une plage (telle que `5-8`).

   - Pour **[!UICONTROL Symbols Used in CAPTCHA]**, saisissez les lettres (a-z et A-Z) et les chiffres (0-9) que vous souhaitez afficher de manière aléatoire dans le CAPTCHA. Le jeu de caractères par défaut ne contient pas de symboles similaires tels que `I` ou `1`. Pour de meilleurs résultats, utilisez des symboles que les utilisateurs peuvent facilement identifier.

   - Définir **[!UICONTROL Case Sensitive]** to `Yes` si vous souhaitez que les clients saisissent les caractères en majuscules ou en minuscules exactement comme indiqué dans le CAPTCHA.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.
