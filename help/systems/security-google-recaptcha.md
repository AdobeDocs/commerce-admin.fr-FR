---
title: Google reCAPTCHA
description: Découvrez comment configurer Google reCAPTCHA pour l’accès administrateur et diverses actions de storefront initiées par les clients enregistrés.
exl-id: c3b53702-0882-4ac4-9cf5-39fefc90005e
role: Admin
feature: Configuration, Security
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 0%

---

# Google reCAPTCHA

[Google reCAPTCHA](https://developers.google.com/recaptcha) garantit qu&#39;un être humain, plutôt qu&#39;un ordinateur (ou &quot;bot&quot;), interagit avec votre site web. Contrairement à la norme Adobe Commerce et Magento Open Source [CAPTCHA](security-captcha.md), Google reCAPTCHA offre une sécurité renforcée avec une sélection d’options et de méthodes d’affichage différentes. D’autres informations sur le trafic du site web sont disponibles dans le tableau de bord de votre compte Google reCAPTCHA.

Google reCAPTCHA est configuré séparément pour l’administrateur et le storefront.

- Pour l’administrateur, Google reCAPTCHA peut être utilisé sur la page [Se connecter](../getting-started/admin-signin.md) et lorsqu’un utilisateur demande la réinitialisation d’un mot de passe. Si le Commerce standard [CAPTCHA](security-captcha.md) est également activé, Google reCAPTCHA peut être utilisé en même temps sans problème.

- Pour le storefront, Google reCAPTCHA peut être utilisé pour se connecter à un [compte client](../customers/customer-sign-in.md), envoyer un message à partir de la page [Nous contacter](../getting-started/store-details.md#contact-us-form) et dans de nombreux autres emplacements du storefront.

  ![Google reCAPTCHA - connexion client](./assets/customer-account-login-recaptcha.png){width="700" zoomable="yes"}

Google reCAPTCHA peut être implémenté de plusieurs façons :

- _reCAPTCHA v3 Invisible_ — Utilise un algorithme pour évaluer les interactions utilisateur et détermine la probabilité que l’utilisateur soit humain sur la base d’un score.

- _reCAPTCHA v2 Invisible_ — Effectue une vérification en arrière-plan sans interaction de l’utilisateur. Les utilisateurs et les clients sont automatiquement vérifiés, mais il peut être nécessaire de sélectionner des images spécifiques pour relever un défi.

- _reCAPTCHA v2 (&quot;Je ne suis pas un robot&quot;)_ — Valide les demandes avec la case à cocher _&quot;Je ne suis pas un robot&quot;_.

>[!IMPORTANT]
>
>Avant de pouvoir configurer Google reCAPTCHA, vérifiez que votre fichier `PHP.ini` comprend le paramètre suivant : `allow_url_fopen = 1`. Cela peut nécessiter l’aide des développeurs. Voir [Paramètres PHP requis](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html?lang=fr){:target=&quot;_blank&quot;} dans le Guide d’installation.

## Étape 1 : Génération des clés Google reCAPTCHA

Google reCAPTCHA nécessite une paire de clés API à activer. Vous pouvez obtenir ces clés gratuitement sur le site reCAPTCHA. Avant de générer les clés, vous devez connaître le type de reCAPTCHA que vous souhaitez utiliser.

1. Ouvrez la page Google reCAPTCHA et connectez-vous à votre compte.

1. Pour **[!UICONTROL Label]**, saisissez un nom pour identifier les clés à des fins de référence interne.

   Vous avez besoin d’un ensemble de clés pour chaque type reCAPTCHA utilisé dans votre installation Adobe Commerce ou Magento Open Source. Par exemple : `Commerce Invisible`

1. Pour **[!UICONTROL reCAPTCHA type]**, choisissez la méthode à utiliser.

   - _reCAPTCHA v3 Invisible_
   - _reCAPTCHA v2 Invisible_
   - _reCAPTCHA v2 (&quot;Je ne suis pas un robot&quot;)_

1. Pour **[!UICONTROL Domain]**, saisissez le domaine de votre boutique. Par exemple : mystore.com

   Si vous disposez de plusieurs magasins avec des domaines différents, saisissez chaque domaine sur une ligne distincte.

   - Ajoutez votre domaine de magasin et tous les sous-domaines.
   - Vous pouvez ajouter `localhost`, d’autres domaines VM locaux et des domaines intermédiaires si nécessaire pour le test.

1. Cochez la case **[!UICONTROL Accept the reCAPTCHA Terms of Service]**.

1. (Facultatif) Cochez la case **[!UICONTROL Send alerts to owners]** pour envoyer une notification si Google détecte des problèmes ou du trafic suspect.

1. Cliquez sur **[!UICONTROL Submit]** pour terminer l’enregistrement et recevoir les clés.

   >[!IMPORTANT]
   >
   >Toutes les clés ne sont pas applicables pour tous les types de reCAPTCHA, et leur application incorrecte peut entraîner un comportement inattendu. Par exemple, les clés Google reCAPTCHA générées pour reCAPTCHA v2 &quot;Je ne suis pas un robot&quot; ne fonctionnent pas avec _reCAPTCHA v2 Invisible_ et peuvent bloquer les fonctionnalités où reCAPTCHA est activé.

## Étape 2 : Configuration de Google reCAPTCHA pour l’administrateur

1. Connectez-vous à votre compte d’administrateur.

1. Dans la barre latérale Admin, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le coin supérieur droit, définissez **[!UICONTROL Store View]** sur `Default Config`.

1. Dans le panneau de gauche, développez **[!UICONTROL Security]** et cliquez sur **[!UICONTROL Google reCAPTCHA Admin Panel]**.

   >[!NOTE]
   >
   >Décochez la case **[!UICONTROL Use system value]** pour chaque champ que vous souhaitez configurer.

1. Pour utiliser _[!DNL reCAPTCHA v2 ("I am not a robot")]_, développez la section **[!UICONTROL reCAPTCHA v2 ("I am not a robot")]**&#x200B;et procédez comme suit :

   - Pour **[!UICONTROL Google API Website Key]**, saisissez la clé du site web qui a été créée pour ce type reCAPTCHA lorsque vous avez enregistré votre compte Google reCAPTCHA.

   - Pour **[!UICONTROL Google API Secret Key]**, saisissez la clé secrète associée à votre compte Google reCAPTCHA.

   - Pour **[!UICONTROL Size]**, choisissez la taille de la zone Google reCAPTCHA que vous souhaitez afficher. Options : `Normal (default)` / `Compact`

   - Pour **[!UICONTROL Theme]**, choisissez le thème que vous souhaitez utiliser pour mettre en forme la zone Google reCAPTCHA. Options : `Light Theme (default)` / `Dark Theme`

   - Pour **[!UICONTROL Language Code]**, saisissez le code à deux caractères pour spécifier la [langue utilisée pour le texte et la messagerie reCAPTCHA Google](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 - &quot;Je ne suis pas un robot&quot;](../configuration-reference/security/assets/recaptcha-admin-v2-not-robot.png){width="600" zoomable="yes"}

1. Pour utiliser _[!DNL reCAPTCHA v2 Invisible]_, développez la section **[!UICONTROL reCAPTCHA v2 Invisible]**&#x200B;et procédez comme suit :

   - Pour **[!UICONTROL Google API Website Key]**, saisissez la clé du site web qui a été créée pour ce type reCAPTCHA lorsque vous avez enregistré votre compte Google reCAPTCHA.

   - Pour **[!UICONTROL Google API Secret Key]**, saisissez la clé secrète associée à votre compte Google reCAPTCHA.

   - Pour **[!UICONTROL Invisible Badge Position]**, choisissez la position du badge à utiliser sur chaque page. Options : `Inline` / `Bottom Right` / `Bottom Left`

   - Pour **[!UICONTROL Theme]**, choisissez le thème à utiliser pour mettre en forme la zone Google reCAPTCHA. Options : `Light Theme (default)` / `Dark Theme`

   - Pour **[!UICONTROL Language Code]**, saisissez un code à deux caractères qui spécifie la [langue utilisée pour le texte et la messagerie reCAPTCHA Google](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 Invisible](../configuration-reference/security/assets/recaptcha-admin-v2-invisible.png){width="600" zoomable="yes"}

1. Pour utiliser _[!DNL reCAPTCHA v3 Invisible]_, développez la section **[!UICONTROL reCAPTCHA v3 Invisible]**&#x200B;et procédez comme suit :

   - Pour **[!UICONTROL Google API Website Key]**, saisissez la clé du site web qui a été créée pour ce type reCAPTCHA lorsque vous avez enregistré votre compte Google reCAPTCHA.

   - Pour **[!UICONTROL Google API Secret Key]**, saisissez la clé secrète associée à votre compte Google reCAPTCHA.

   - Saisissez le **[!UICONTROL Minimum Score Threshold]** pour identifier le moment où une interaction utilisateur est signalée comme risque potentiel ; où 1.0 est une interaction utilisateur type et 0.0 est probablement un bot. Valeur par défaut : `0.5`

   - Pour **[!UICONTROL Invisible Badge Position]**, choisissez la position à utiliser sur chaque page. Options : `Inline` / `Bottom Right` / `Bottom Left`

   - Pour **[!UICONTROL Theme]**, choisissez le thème à utiliser pour mettre en forme la zone Google reCAPTCHA. Options : `Light Theme (default)` / `Dark Theme`

   - Pour **[!UICONTROL Language Code]**, saisissez un code à deux caractères qui spécifie la [langue utilisée pour le texte et la messagerie reCAPTCHA Google](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v3 Invisible](../configuration-reference/security/assets/recaptcha-admin-v3-invisible.png){width="600" zoomable="yes"}

1. Développez **[!UICONTROL reCAPTCHA Validation Failure Messages]** et saisissez les messages qui apparaissent dans l’Admin si la validation échoue ou ne peut pas être terminée.

   ![reCAPTCHA Messages d’échec](../configuration-reference/security/assets/recaptcha-admin-failure-messages.png){width="600" zoomable="yes"}

1. Développez la section **[!UICONTROL Admin Panel]** et configurez les éléments suivants selon vos besoins :

   - Définissez **[!UICONTROL Enable for Login]** sur le type reCAPTCHA que vous souhaitez utiliser pour la page Admin Se connecter .

   - Définissez **[!UICONTROL Enable for Forgot Password]** sur le type reCAPTCHA que vous souhaitez utiliser pour les demandes de réinitialisation de mot de passe.

   ![reCAPTCHA admin options](../configuration-reference/security/assets/recaptcha-admin-panel.png){width="600" zoomable="yes"}

## Étape 3 : configurer Google reCAPTCHA pour le storefront

1. Dans le panneau de gauche sous _[!UICONTROL Security]_, choisissez **[!UICONTROL Google reCAPTCHA Storefront]**.

1. Renseignez la section pour chaque type reCAPTCHA que vous souhaitez utiliser dans le storefront.

   Pour plus d’informations sur les options de chaque type reCAPTCHA, reportez-vous aux informations de l’ _Étape 2 : configuration de Google reCAPTCHA pour l’administrateur_ .

1. Développez **[!UICONTROL reCAPTCHA Validation Failure Messages]** et saisissez les messages qui s’affichent dans le storefront si la validation échoue ou ne peut pas être terminée.

1. Développez la section **[!UICONTROL Storefront]** .

   >[!NOTE]
   >
   >Décochez la case **[!UICONTROL Use system value]** pour chaque champ que vous souhaitez configurer.

1. Définissez chaque champ d’emplacement du storefront sur le type reCAPTCHA que vous avez configuré pour utiliser.

   - [!UICONTROL Enable for Customer Login]
   - [!UICONTROL Enable for Forgot Password]
   - [!UICONTROL Enable for Create New Customer Account]
   - [!UICONTROL Enable for Edit Customer Account]
   - [!UICONTROL Enable for Create New Company Account] ![Adobe Commerce B2B](../assets/b2b.svg) (Disponible avec Adobe Commerce B2B uniquement)
   - [!UICONTROL Enable for Contact Us]
   - [!UICONTROL Enable for Product Review]
   - [!UICONTROL Enable for Newsletter Subscription]
   - [!UICONTROL Enable for Gift Card] ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement)
   - [!UICONTROL Enable for Invitation Create Account]
   - [!UICONTROL Enable for Send To Friend]
   - [!UICONTROL Enable for Checkout/Placing Order]
   - [!UICONTROL Enable for Wishlist Sharing]
   - [!UICONTROL Enable for Coupon Codes]
   - [!UICONTROL Enable for PayPal PayflowPro payment form]

   ![Configuration des options Storefront](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## Etape 4 : enregistrer la configuration

1. Une fois les paramètres de configuration terminés, cliquez sur **[!UICONTROL Save Config]**.

1. Dans le message situé en haut de l’espace de travail, cliquez sur **[!UICONTROL Cache Management]** et actualisez chaque cache non valide.
