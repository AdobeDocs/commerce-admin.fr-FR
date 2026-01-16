---
title: Google reCAPTCHA Enterprise
description: Découvrez comment configurer Google reCAPTCHA Enterprise pour protéger votre storefront Adobe Commerce as a Cloud Service des robots et des activités frauduleuses.
role: Admin
feature: Configuration, Security
badgeSaas: label="SaaS uniquement" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce as a Cloud Service (infrastructure SaaS gérée par Adobe)."
source-git-commit: dde1d634a1c6c7435668a8ad6084b926cc0d6193
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 0%

---

# Google reCAPTCHA Enterprise

[!BADGE  Sandbox ]{type=Caution tooltip="Les éléments répertoriés sont actuellement disponibles uniquement dans les environnements Sandbox. Adobe publie d’abord les mises à jour de Sandbox afin que vous puissiez tester les modifications à venir avant qu’elles ne soient déployées en production."}

[Google reCAPTCHA Enterprise](https://cloud.google.com/security/products/recaptcha#protect-against-fraud-and-abuse-with-modern-bot-protection-and-fraud-prevention-platform) fournit une protection avancée des robots pour votre storefront Adobe Commerce as a Cloud Service en utilisant l&#39;analyse de risque adaptative et le machine learning pour différencier les utilisateurs humains des robots. Cela permet d’empêcher les activités frauduleuses, le spam et les abus sur votre site.

>[!NOTE]
>
>Cette fonctionnalité ne fournit PAS de prise en charge reCAPTCHA pour l’administrateur.

Voir [Google reCAPTCHA V3 et V2](security-google-recaptcha.md) pour plus d&#39;informations sur la configuration d&#39;autres versions de Google reCAPTCHA.

## Fonctionnalités

Google reCAPTCHA Enterprise offre les fonctionnalités suivantes :

- **Détection de robot avancée** : utilise des modèles de machine learning de Google Cloud pour une détection de robot supérieure
- **Analyse de la note de risque** : fournit des notes de risque détaillées (0,0 à 1,0) pour chaque interaction
- **Seuils configurables** : définissez les scores de risque minimum acceptables par client
- **Prise en charge multi-tenant** : configuration par client avec des projets Google Cloud isolés
- **Informations d’identification chiffrées** : informations d’identification de compte de service stockées chiffrées dans une base de données
- **Protection des formulaires** : protège tous les formulaires Commerce standard, y compris la connexion, le passage en caisse, les révisions de produits, etc.

## Conditions préalables

Vous avez besoin des ressources suivantes avant de pouvoir configurer Google reCAPTCHA Enterprise pour votre storefront Adobe Commerce as a Cloud Service :

- Un compte Google Cloud actif avec reCAPTCHA Enterprise activé.
- Accès à la console cloud Google pour créer et gérer des clés reCAPTCHA Enterprise.

Sur les installations Adobe Commerce as a Cloud Service à plusieurs clients, chaque client doit avoir ses propres clés de projet Google Cloud et reCAPTCHA Enterprise.

## Étape 1 : Configurer Google reCAPTCHA Enterprise

Suivez ces étapes générales pour configurer Google reCAPTCHA Enterprise pour votre storefront. Pour obtenir des instructions détaillées, consultez la documentation de [Google reCAPTCHA Enterprise](https://docs.cloud.google.com/recaptcha/docs/overview).

1. [Créez un projet Google Cloud](https://developers.google.com/workspace/guides/create-project) pour votre implémentation reCAPTCHA Enterprise.

1. Activez l’API [reCAPTCHA Enterprise](https://docs.cloud.google.com/recaptcha/docs/prepare-environment).

1. Créez une clé de site reCAPTCHA Enterprise [clé de site](https://docs.cloud.google.com/recaptcha/docs/choose-key-type) basée sur les scores.

1. Créez un compte de service avec le rôle IAM `roles/recaptchaenterprise.admin`.

1. Téléchargez le fichier de clé JSON du compte de service, qui contient les informations d’identification nécessaires pour authentifier votre storefront Adobe Commerce as a Cloud Service avec Google reCAPTCHA Enterprise.

## Étape 2 : configuration de Google reCAPTCHA pour le storefront

1. Dans le panneau de gauche sous _[!UICONTROL Security]_, choisissez **[!UICONTROL Google reCAPTCHA Storefront]**.

1. Renseignez la section **[!UICONTROL reCAPTCHA Enterprise]** comme suit.

   - Par **[!UICONTROL Site Key]**, copiez et collez votre clé de site reCAPTCHA Enterprise à partir de votre console cloud Google.

   - Par **[!UICONTROL Google Cloud Project ID]**, copiez et collez l’ID de projet à partir de votre projet Google Cloud.

   - Par **[!UICONTROL Service Account JSON]**, copiez le contenu du fichier de clé JSON du compte de service que vous avez téléchargé à l’[Étape 1 : configurer Google reCAPTCHA Enterprise](#step-1-set-up-google-recaptcha-enterprise).

   - Par **[!UICONTROL Minimum Score Threshold]**, saisissez le score minimal (0,0 à 1,0) pour identifier lorsqu’une interaction utilisateur est signalée comme risque potentiel. Un score de 1,0 est une interaction utilisateur type, et 0,0 est probablement un robot.

   - Par **[!UICONTROL Badge Position]**, choisissez la position du badge reCAPTCHA invisible sur chaque page. Options : `Inline` / `Bottom Right` / `Bottom Left`.

   - Par **[!UICONTROL Theme]**, choisissez `Light Theme` (par défaut) ou `Dark Theme` pour déterminer le style de la zone reCAPTCHA de Google.

   - Par **[!UICONTROL Language Code]**, saisissez un [code à deux caractères](https://developers.google.com/recaptcha/docs/language) qui spécifie la langue utilisée pour le texte et la messagerie reCAPTCHA de Google.

   - Par **[!UICONTROL Validation Failure Message]**, vous pouvez éventuellement modifier le message affiché sur le storefront en cas d’échec de la validation.


1. Développez la section **[!UICONTROL Storefront]** et définissez chaque formulaire storefront que vous souhaitez protéger sur **[!UICONTROL reCAPTCHA Enterprise]**.

   {{recaptcha-forms-list}}

   ![Configuration des options du storefront](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## Étape 3 : enregistrer la configuration

1. Une fois les paramètres de configuration définis, cliquez sur **[!UICONTROL Save Config]**.

1. Dans le message en haut de l’espace de travail, cliquez sur **[!UICONTROL Cache Management]** et actualisez chaque cache non valide.
