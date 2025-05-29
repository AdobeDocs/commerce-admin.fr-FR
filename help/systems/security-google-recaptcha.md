---
title: Google reCAPTCHA
description: Découvrez comment configurer Google reCAPTCHA pour un accès administrateur et diverses actions de storefront initiées par les clients enregistrés.
exl-id: c3b53702-0882-4ac4-9cf5-39fefc90005e
role: Admin
feature: Configuration, Security
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '1061'
ht-degree: 0%

---

# Google reCAPTCHA

[Google reCAPTCHA](https://developers.google.com/recaptcha) garantit qu&#39;un être humain, plutôt qu&#39;un ordinateur (ou « robot »), interagit avec votre site web. Contrairement à Adobe Commerce et Magento Open Source standard [CAPTCHA](security-captcha.md), Google reCAPTCHA offre une sécurité renforcée avec une sélection d’options d’affichage et de méthodes différentes. D’autres informations sur le trafic sur le site web sont disponibles dans le tableau de bord de votre compte Google reCAPTCHA.

Google reCAPTCHA est configuré séparément pour l’administration et le storefront.

- Pour l’administrateur, le reCAPTCHA de Google peut être utilisé sur la page [Sign In](../getting-started/admin-signin.md) et lorsqu’un utilisateur demande une réinitialisation de mot de passe. Si le Commerce standard [CAPTCHA](security-captcha.md) est également activé, le reCAPTCHA de Google peut être utilisé en même temps sans aucun problème.

- Pour le storefront, Google reCAPTCHA peut être utilisé pour se connecter à un [compte client](../customers/customer-sign-in.md), envoyer un message à partir de la page [Nous contacter](../getting-started/store-details.md#contact-us-form) et dans de nombreux autres emplacements de storefront.

  ![Google reCAPTCHA - connexion client](./assets/customer-account-login-recaptcha.png){width="700" zoomable="yes"}

Google reCAPTCHA peut être implémenté de plusieurs manières :

- _reCAPTCHA v3 Invisible_ — Utilise un algorithme pour évaluer les interactions utilisateur et détermine la probabilité que l&#39;utilisateur soit humain en fonction d&#39;un score.

- _reCAPTCHA v2 Invisible_ — Effectue la vérification en arrière-plan sans interaction de l&#39;utilisateur. Les utilisateurs et les clientes et utilisateurs sont automatiquement vérifiés, mais il peut être nécessaire de sélectionner des images spécifiques pour relever un défi.

- _reCAPTCHA v2 (« Je ne suis pas un robot »)_ — Valide les requêtes avec la case à cocher _« Je ne suis pas un robot »_.

>[!IMPORTANT]
>
>Avant de pouvoir configurer Google reCAPTCHA, assurez-vous que votre fichier `PHP.ini` comprend le paramètre suivant : `allow_url_fopen = 1`. Cela peut nécessiter l’aide d’un développeur. Voir [Paramètres PHP requis](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html?lang=fr){:target="_blank"} dans le Guide d&#39;installation.

## Étape 1 : générer des clés reCAPTCHA Google

Google reCAPTCHA requiert une paire de clés API pour l’activer. Vous pouvez obtenir ces clés gratuitement via le site reCAPTCHA. Avant de générer les clés, vous devez connaître le type de reCAPTCHA que vous souhaitez utiliser.

1. Ouvrez la page Google reCAPTCHA et connectez-vous à votre compte .

1. Par **[!UICONTROL Label]**, saisissez un nom pour identifier les clés à des fins de référence interne.

   Vous avez besoin d’un ensemble de clés pour chaque type reCAPTCHA utilisé dans votre installation Adobe Commerce ou Magento Open Source. Par exemple : `Commerce Invisible`

1. Par **[!UICONTROL reCAPTCHA type]**, choisissez la méthode que vous souhaitez utiliser.

   - _reCAPTCHA v3 invisible_
   - _reCAPTCHA v2 invisible_
   - _reCAPTCHA v2 (« Je ne suis pas un robot »)_

1. Par **[!UICONTROL Domain]**, saisissez le domaine de votre boutique. Par exemple : mystore.com

   Si vous disposez de plusieurs magasins avec des domaines différents, saisissez chaque domaine sur une ligne distincte.

   - Ajoutez le domaine de votre boutique et tous les sous-domaines.
   - Vous pouvez ajouter des `localhost`, d’autres domaines d’ordinateur virtuel local et des domaines d’évaluation selon les besoins pour les tests.

1. Cochez la case à **[!UICONTROL Accept the reCAPTCHA Terms of Service]**.

1. (Facultatif) Cochez la case **[!UICONTROL Send alerts to owners]** pour envoyer une notification si Google détecte des problèmes ou un trafic suspect.

1. Cliquez sur **[!UICONTROL Submit]** pour terminer l’enregistrement et recevoir les clés.

   >[!IMPORTANT]
   >
   >Toutes les clés ne s’appliquent pas à tous les types de reCAPTCHA et leur mauvaise application peut entraîner un comportement inattendu. Par exemple, les clés reCAPTCHA de Google générées pour reCAPTCHA v2 « Je ne suis pas un robot » ne fonctionnent pas avec _reCAPTCHA v2 invisible_ et peuvent bloquer la fonctionnalité où reCAPTCHA est activé.

## Étape 2 : configurer Google reCAPTCHA pour l’administrateur

[!BADGE PaaS uniquement]{type=Informative url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."}

1. Connectez-vous à votre compte administrateur.

1. Dans la barre latérale d’administration, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le coin supérieur droit, définissez **[!UICONTROL Store View]** sur `Default Config`.

1. Dans le panneau de gauche, développez **[!UICONTROL Security]** et cliquez sur **[!UICONTROL Google reCAPTCHA Admin Panel]**.

   >[!NOTE]
   >
   >Décochez la case **[!UICONTROL Use system value]** pour chaque champ à configurer.

1. Pour utiliser _[!DNL reCAPTCHA v2 ("I am not a robot")]_, développez la section **[!UICONTROL reCAPTCHA v2 ("I am not a robot")]**&#x200B;et procédez comme suit :

   - Par **[!UICONTROL Google API Website Key]**, saisissez la clé de site web qui a été créée pour ce type reCAPTCHA lorsque vous avez enregistré votre compte Google reCAPTCHA.

   - Par **[!UICONTROL Google API Secret Key]**, saisissez la clé secrète associée à votre compte Google reCAPTCHA.

   - Par **[!UICONTROL Size]**, choisissez la taille de la zone reCAPTCHA de Google que vous souhaitez afficher. Options : `Normal (default)` / `Compact`

   - Par **[!UICONTROL Theme]**, choisissez le thème que vous souhaitez utiliser pour appliquer un style à la zone reCAPTCHA de Google. Options : `Light Theme (default)` / `Dark Theme`

   - Par **[!UICONTROL Language Code]**, saisissez le code à deux caractères pour spécifier la langue [ utilisée pour le texte et la messagerie reCAPTCHA de Google](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 - « Je ne suis pas un robot »](../configuration-reference/security/assets/recaptcha-admin-v2-not-robot.png){width="600" zoomable="yes"}

1. Pour utiliser _[!DNL reCAPTCHA v2 Invisible]_, développez la section **[!UICONTROL reCAPTCHA v2 Invisible]**&#x200B;et procédez comme suit :

   - Par **[!UICONTROL Google API Website Key]**, saisissez la clé de site web qui a été créée pour ce type reCAPTCHA lorsque vous avez enregistré votre compte Google reCAPTCHA.

   - Par **[!UICONTROL Google API Secret Key]**, saisissez la clé secrète associée à votre compte Google reCAPTCHA.

   - Par **[!UICONTROL Invisible Badge Position]**, choisissez la position du badge à utiliser sur chaque page. Options : `Inline` / `Bottom Right` / `Bottom Left`

   - Par **[!UICONTROL Theme]**, choisissez le thème à utiliser pour appliquer un style à la zone reCAPTCHA de Google. Options : `Light Theme (default)` / `Dark Theme`

   - Par **[!UICONTROL Language Code]**, saisissez un code à deux caractères qui spécifie la langue [ utilisée pour le texte et la messagerie reCAPTCHA de Google](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 invisible](../configuration-reference/security/assets/recaptcha-admin-v2-invisible.png){width="600" zoomable="yes"}

1. Pour utiliser _[!DNL reCAPTCHA v3 Invisible]_, développez la section **[!UICONTROL reCAPTCHA v3 Invisible]**&#x200B;et procédez comme suit :

   - Par **[!UICONTROL Google API Website Key]**, saisissez la clé de site web qui a été créée pour ce type reCAPTCHA lorsque vous avez enregistré votre compte Google reCAPTCHA.

   - Par **[!UICONTROL Google API Secret Key]**, saisissez la clé secrète associée à votre compte Google reCAPTCHA.

   - Entrez le **[!UICONTROL Minimum Score Threshold]** permettant d’identifier lorsqu’une interaction utilisateur est signalée comme risque potentiel ; où 1,0 est une interaction utilisateur type et 0,0 est probablement un robot. Valeur par défaut : `0.5`

   - Par **[!UICONTROL Invisible Badge Position]**, choisissez la position à utiliser sur chaque page. Options : `Inline` / `Bottom Right` / `Bottom Left`

   - Par **[!UICONTROL Theme]**, choisissez le thème à utiliser pour appliquer un style à la zone reCAPTCHA de Google. Options : `Light Theme (default)` / `Dark Theme`

   - Par **[!UICONTROL Language Code]**, saisissez un code à deux caractères qui spécifie la langue [ utilisée pour le texte et la messagerie reCAPTCHA de Google](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v3 invisible](../configuration-reference/security/assets/recaptcha-admin-v3-invisible.png){width="600" zoomable="yes"}

1. Développez **[!UICONTROL reCAPTCHA Validation Failure Messages]** et saisissez les messages qui s’affichent dans Admin si la validation échoue ou ne peut pas être effectuée.

   ![ Messages d’échec reCAPTCHA ](../configuration-reference/security/assets/recaptcha-admin-failure-messages.png){width="600" zoomable="yes"}

1. Développez la section **[!UICONTROL Admin Panel]** et configurez les éléments suivants selon vos besoins :

   - Définissez **[!UICONTROL Enable for Login]** sur le type reCAPTCHA que vous souhaitez utiliser pour la page de connexion de l’administrateur.

   - Définissez **[!UICONTROL Enable for Forgot Password]** sur le type reCAPTCHA que vous souhaitez utiliser pour les demandes de réinitialisation de mot de passe.

   ![options d’administration reCAPTCHA](../configuration-reference/security/assets/recaptcha-admin-panel.png){width="600" zoomable="yes"}

## Étape 3 : Configurer Google reCAPTCHA pour le storefront

1. Dans le panneau de gauche sous _[!UICONTROL Security]_, choisissez **[!UICONTROL Google reCAPTCHA Storefront]**.

1. Renseignez la section pour chaque type reCAPTCHA que vous souhaitez utiliser dans le storefront.

   Voir les informations dans _Étape 2 : Configuration de Google reCAPTCHA pour l’administrateur_ pour plus d’informations sur les options de chaque type reCAPTCHA.

1. Développez **[!UICONTROL reCAPTCHA Validation Failure Messages]** et saisissez les messages qui s’affichent dans le storefront si la validation échoue ou ne peut pas être effectuée.

1. Développez la section **[!UICONTROL Storefront]** .

   >[!NOTE]
   >
   >Décochez la case **[!UICONTROL Use system value]** pour chaque champ à configurer.

1. Définissez chaque champ d’emplacement de storefront sur le type de reCAPTCHA que vous avez configuré pour utiliser.

   - [!UICONTROL Enable for Customer Login]
   - [!UICONTROL Enable for Forgot Password]
   - [!UICONTROL Enable for Create New Customer Account]
   - [!UICONTROL Enable for Edit Customer Account]
   - [!UICONTROL Enable for Create New Company Account] ![Adobe Commerce B2B](../assets/b2b.svg) (disponible avec Adobe Commerce B2B uniquement)
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

   ![Configuration des options du storefront](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## Étape 4 : enregistrer la configuration

1. Une fois les paramètres de configuration définis, cliquez sur **[!UICONTROL Save Config]**.

1. Dans le message en haut de l’espace de travail, cliquez sur **[!UICONTROL Cache Management]** et actualisez chaque cache non valide.
