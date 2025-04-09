---
title: '[!DNL Google Tag Manager]'
description: Découvrez comment utiliser  [!DNL Google Tag Manager]  gérer les nombreuses balises (fragments de code) liées à vos événements de campagne marketing sur vos sites Adobe Commerce.
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: 22a619db0b0673dc520b9bdc5d6cd0c8ffecdf08
workflow-type: tm+mt
source-wordcount: '1459'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager] est un outil puissant qui vous permet de gérer et de déployer efficacement diverses balises (fragments de code) associées à vos événements de campagne marketing. [!DNL Google Tag Manager] vous permet d’ajouter des balises de suivi à votre site pour mesurer l’audience ou pour personnaliser, recibler ou mener des initiatives marketing dans les moteurs de recherche.

[!DNL Google Tag Manager] transfère directement les données et les événements à [!DNL Google Analytics], à Enhanced Ecommerce et à d’autres solutions d’analyse tierces afin de dresser un tableau clair des performances de votre site, de vos produits et de vos promotions.

Vous devez disposer d’un compte [!DNL Google Analytics] et [!DNL Tag Manager] pour poursuivre ce processus. Les instructions suivantes vous guident tout au long du processus de configuration de vos comptes Google, de votre magasin Commerce et de la création d’une balise.

>[!NOTE]
>
>Si votre entreprise est soumise à des réglementations de confidentialité telles que le [Règlement général sur la protection des données](../getting-started/compliance-gdpr.md) et/ou la [Loi californienne sur la protection de la vie privée des consommateurs](../getting-started/compliance-ccpa.md), consultez [Paramètres de confidentialité de Google](google-tools.md#google-privacy-settings).

## Étape 1. Configuration de votre compte [!DNL Google Analytics]

Voir [Configuration de la recherche de site](https://support.google.com/analytics/answer/1012264) dans l’aide de Google pour connaître les principes de base dont vous avez besoin pour commencer. Consultez également les guides Google pour [Google Analytics](https://support.google.com/analytics/answer/9304153) et [Google Tag Manager](https://support.google.com/tagmanager/answer/6102821).

1. Connectez-vous à votre compte [!DNL Google Analytics].

1. Pour **[!UICONTROL Internal Site Search Tracking]** activer, procédez comme suit :

   - Accédez à **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**.

   - Définissez **[!UICONTROL Site Search Tracking]** sur `On`.

   - Définissez **[!UICONTROL Query]** paramètre sur `q`.

   - Une fois l’opération terminée, **[!UICONTROL Save]** les paramètres.

1. Pour activer les fonctionnalités d&#39;affichage, procédez comme suit :

   - Choisissez **[!UICONTROL Property Settings]**.

   - Sous _[!UICONTROL Advertising Features]_, définissez **[!UICONTROL Enable Demographics and Interest Reports]**sur `On`.

   - **[!UICONTROL Save]** les paramètres.

1. Pour activer le suivi eCommerce, procédez comme suit :

   - Accédez à **[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**.

   - Définissez **[!UICONTROL Enable Ecommerce]** sur `On`.

   - Définissez **[!UICONTROL Enable Enhanced Ecommerce Reporting]** sur `On`.

   - **[!UICONTROL Save]** les paramètres.

1. Rechargez la page et vérifiez que tous les paramètres restent `On`.

   >[!NOTE]
   >
   >Si tous les paramètres ne sont pas `On`, répétez les étapes précédentes, enregistrez et rechargez la page. Répétez ce processus jusqu’à ce que tous les paramètres soient définis sur `On`.

## Étape 2. Configuration de votre compte [!DNL Google Tag Manager]

Les instructions suivantes indiquent comment configurer un nouveau conteneur avec les paramètres de base. Un exemple de fichier de configuration [Composer](https://developer.adobe.com/commerce/php/development/composer/) (.json) est utilisé pour simplifier le processus d’importation afin de générer une balise dans un nouveau conteneur. Pour cet exemple, il est recommandé de créer un conteneur plutôt que de modifier un conteneur existant.

>[!NOTE]
>
>Pour plus d’informations, voir Google [Exportation et importation de conteneur](https://support.google.com/tagmanager/answer/6106997). Ces instructions fournissent une procédure pas à pas pour importer un exemple de fichier JSON dans un nouveau conteneur.

1. Téléchargez le fichier lié [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt), ouvrez-le dans un éditeur et enregistrez-le en tant que `GTM_M2_Config.json`.

   Le fichier json est chargé directement dans [!DNL Google Tag Manager].

1. Accédez à **[!UICONTROL Admin]** > **[!UICONTROL Container]** > **[!UICONTROL Import Container]**.

1. Cliquez sur **[!UICONTROL Choose container file]** et sélectionnez le fichier json.

1. Sous **[!UICONTROL Choose workspace]**, cliquez sur **[!UICONTROL New]**.

1. Saisissez un titre et une description, puis cliquez sur **[!UICONTROL Save]**.

1. Pour importer le fichier, sélectionnez l’une des actions suivantes :

   - L’option **[!UICONTROL Overwrite]** doit être sélectionnée pour un nouveau conteneur.

   - L’option **[!UICONTROL Merge]** doit être sélectionnée si vous utilisez un conteneur existant.

1. Cliquez sur **[!UICONTROL Preview]** pour passer en revue les balises, les déclencheurs et les variables.

1. Pour modifier le **[!UICONTROL Google Analytics ID]** référencé dans les variables, procédez comme suit :

   - Accédez à **[!UICONTROL Variables]** > **[!UICONTROL User-Defined Variables]**.

   - Choisissez **[!UICONTROL Google Analytics]** et mettez à jour l’espace réservé (`UA-xxxxxx-x`) avec votre propre **[!UICONTROL GA ID]**.

1. Suivez les instructions de Google pour ajouter des balises, des déclencheurs et des variables au nouveau conteneur.

   Si vous souhaitez utiliser des paramètres d’un autre conteneur, vous pouvez les déplacer vers le nouveau conteneur.

1. Cliquez sur **[!UICONTROL Confirm]** une fois l’opération terminée.

1. Suivez les instructions de Google pour publier le nouveau conteneur.

## Étape 3. Configuration de votre boutique

{{gtag-api-note}}

1. Connectez-vous à l’administration de votre boutique Commerce.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Google API]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Google Analytics]** et configurez les éléments suivants :

   ![Configuration des ventes - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - Définissez **[!UICONTROL Enable]** sur `Yes`.

   - Définissez **[!UICONTROL Account type]** sur `Google Tag Manager`.

   - Dans le champ **[!UICONTROL Container ID]** , saisissez votre identifiant GTM (`GTM-xxxxxx`).

   - Si vous utilisez également Google Analytics pour des expériences de contenu, définissez **Activer les expériences de contenu** sur `Yes`.

   - Utilisez les valeurs par défaut pour les champs restants.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

1. Testez vos paramètres [!DNL Google Tag Manager] et vérifiez que tout fonctionne correctement.

>[!NOTE]
>
>Chaque conteneur est associé à un site web et vous n’avez besoin que d’un seul conteneur par compte. Si vous disposez d’une instance Commerce multisite, vous avez besoin de conteneurs distincts.

## Descriptions des champs

| Champ | Champ d’application | Description |
|--- |--- |--- |
| [!UICONTROL Enable] | Affichage de la boutique | Détermine si l’e-commerce amélioré de Google Analytics peut être utilisé pour analyser l’activité dans votre magasin. Options : `Yes` / `No` |
| [!UICONTROL Account type] | Affichage de la boutique | Détermine le code de suivi Google utilisé pour surveiller l’activité et le trafic du magasin. Options : `Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | Affichage de la boutique | Détermine si les informations d’identification sont supprimées des adresses IP qui apparaissent dans les résultats de Google Analytics. |
| [!UICONTROL Enable Content Experiments] | Affichage de la boutique | Active les expériences de contenu Google, qui peuvent être utilisées pour tester jusqu’à dix versions différentes d’une même page. Options : `Yes` / `No` |
| [!UICONTROL Container Id] | Affichage de la boutique | Si [!DNL Google Tag Manager] est déjà installé et configuré pour votre magasin, l’ID de conteneur s’affiche automatiquement dans ce champ. |
| [!UICONTROL List property for the catalog page] | Affichage de la boutique | Identifie la propriété du Gestionnaire de balises associée à la page de catalogue. Valeur par défaut : `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Affichage de la boutique | Identifie la propriété du Gestionnaire de balises associée au bloc de ventes croisées. Valeur par défaut : `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Affichage de la boutique | Identifie la propriété du Gestionnaire de balises associée au bloc de vente incitative. Valeur par défaut : `Up-sell` |
| [!UICONTROL List property for the related products block] | Affichage de la boutique | Identifie la propriété du Gestionnaire de balises associée au bloc de produits associés. Valeur par défaut : `Related Products` |
| [!UICONTROL List property for the search results page] | Affichage de la boutique | Identifie la propriété du Gestionnaire de balises associée à la page des résultats de recherche. Valeur par défaut : `Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | Affichage de la boutique | Identifie la propriété du Gestionnaire de balises associée aux libellés des promotions internes. Valeur par défaut : `Label` |

{style="table-layout:auto"}

## Créer une balise pour le suivi des conversions

Si vous disposez d’un compte Google AdWords, vous pouvez créer une balise pour effectuer le suivi des conversions. L’exemple suivant montre comment utiliser à la fois [!DNL Google Tag Manager] et [!DNL Google Analytics] pour créer une balise qui se déclenche sur la page Conversion _Succès_ de votre boutique.

### Étape 1. Créer une balise

1. Connectez-vous à votre compte [!DNL Google Tag Manager] et cliquez sur le lien du conteneur que vous avez créé pour votre boutique.

1. Dans la zone de **[!UICONTROL New Tag]**, cliquez sur **[!UICONTROL Add a new tag]**.

1. Obtenez les informations suivantes à partir de votre compte AdWords :

   - ID de conversion
   - Libellé de conversion

   Si vous avez besoin d’aide, consultez le [site d’assistance](https://support.google.com/tagmanager/answer/6105160) de Google.

1. Dans le tableau de bord [!DNL Google Tag Manager], cliquez sur **[!UICONTROL Google AdWords]** et procédez comme suit :

   - Cliquez sur l’espace réservé au titre et saisissez un nom pour la nouvelle balise.

   - Sous **[!UICONTROL Choose Product]**, sélectionnez **[!UICONTROL Google AdWords]**.

   - Sous _[!UICONTROL Choose a Tag Type]_, sélectionnez **[!UICONTROL AdWords Conversion Tracking]**et cliquez sur **[!UICONTROL Continue]**.

1. Saisissez les **[!UICONTROL Conversion ID]** et **[!UICONTROL Conversion Label]** de votre compte AdWords, puis cliquez sur **[!UICONTROL Continue]**.

### Étape 2. Créer une règle

Depuis le tableau de bord de [!DNL Google Tag Manager], l’étape suivante consiste à créer une règle qui déclenche la balise sur la page de conversion.

1. Sous **[!UICONTROL Fire On]**, cliquez sur **[!UICONTROL Some Pages]**.

1. Dans la section _[!UICONTROL Choose Pages]_, renseignez les paramètres suivants :

   - **[!UICONTROL Name]** - Saisissez un nom pour la description de la page.

   - **[!UICONTROL Variable]** `url`

   - **Opération** - `matches RegEx`

     Pour en savoir plus, voir [Opérateurs de sélecteurs Regex et CSS](https://support.google.com/tagmanager/answer/7679109) dans l’aide du gestionnaire de balises Google.

   - **[!UICONTROL Value]** - `checkout/success.*`

1. Cochez la case verte et cliquez sur **[!UICONTROL Save]**.

   Le déclencheur que vous configurez apparaît sous la forme d’un bouton bleu dans la section Déclencher.

1. Cliquez ensuite sur **[!UICONTROL Save Tag]**.

### Étape 3. Prévisualiser et publier

L’étape suivante du processus consiste à prévisualiser la balise . Chaque fois que la balise est prévisualisée, un instantané de la version est enregistré. Lorsque les résultats vous conviennent, accédez à la version que vous souhaitez utiliser, puis cliquez sur **[!UICONTROL Publish]**.

## Balise HTML personnalisée avec JavaScript

Cette section explique comment ajouter une valeur à usage unique CSP au JavaScript de balise HTML personnalisé pour l’exécuter sur la page de passage en caisse, en veillant à la conformité aux exigences de la politique de sécurité du contenu (CSP). Cet ajout améliore la sécurité du site en empêchant l’exécution de scripts non autorisés. Pour plus d’informations, consultez la documentation [ Politique de sécurité du contenu ](https://developer.adobe.com/commerce/php/development/security/content-security-policies).

>[!NOTE]
>
>L’importation de la variable globale `cspNonce` dans Google Tag Manager est prise en charge uniquement sur Adobe Commerce version 2.4.8 et ultérieure.

>[!WARNING]
>
>L’ajout de scripts inconnus à votre boutique peut compromettre les données. Les scripts autorisés sur la page de passage en caisse peuvent voler des informations client sensibles, y compris des détails de paiement. Il est essentiel de prendre des précautions pour protéger votre compte Google Tag Manager. Ajoutez uniquement des scripts de confiance, vérifiez et auditez régulièrement vos balises et implémentez des mesures de sécurité solides telles que l’authentification à deux facteurs (2FA) et les contrôles d’accès.

### Étape 1. Création d’une variable à usage unique CSP

Vous pouvez créer une variable à usage unique CSP qui peut être utilisée dans votre gestionnaire de balises Google en important la configuration de la variable ou en la configurant manuellement.

#### Importer la configuration des variables

La variable CSP Nonce est incluse dans l’exemple de conteneur [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt). Vous pouvez créer la variable en important ce code dans votre espace de travail.

#### Créer la variable manuellement

Si vous ne pouvez pas importer la configuration de variable, procédez comme suit pour la créer.

1. Dans votre espace de travail, accédez à la section **Variables** dans la barre latérale.
1. Cliquez sur le bouton **Nouveau** au bas de la page dans la section **Variables définies par l’utilisateur**.
1. Nommez la variable `gtmNonce`.
1. Cliquez sur l’icône en forme de crayon pour modifier la variable.
1. Sélectionnez **Variable JavaScript** dans la section **Variable de page**.
1. Dans le champ **Nom global de la variable**, saisissez `window.cspNonce`.
1. Enregistrez la variable.

Pour en savoir plus sur les [variables du gestionnaire de balises Google](https://support.google.com/tagmanager/answer/7683056?hl=en), consultez [Types de variables définis par l’utilisateur pour le web](https://support.google.com/tagmanager/answer/7683362?hl=en) dans la documentation de Google. Cette documentation fournit des conseils détaillés sur la création et la gestion de variables personnalisées afin d’adapter la gestion des balises à des besoins spécifiques de marketing et d’analyse.

### Étape 2. Création d’une balise HTML personnalisée

1. Dans votre espace de travail, accédez à la section **Balises** dans la barre latérale.
1. Cliquez sur le bouton **Nouveau**.
1. Dans la section **Configuration de balise**, sélectionnez **Balise HTML personnalisée**.
1. Saisissez le JavaScript requis dans la zone de texte, puis ajoutez un attribut à usage unique à la balise `<script>` d’ouverture qui pointe vers la variable que vous avez créée à l’étape précédente. Par exemple :

   ```html
   <script nonce="{{gtmNonce}}">
       // Your JavaScript code here
   </script>
   ```

1. Sélectionnez **Support document.write**.
1. Dans la section **Déclenchement**, sélectionnez le déclencheur de votre choix. Par exemple, **Initialisation du consentement - Toutes les pages**.

Pour plus d’informations sur la [Balises](https://support.google.com/tagmanager/answer/3281060) dans le Gestionnaire de balises de Google, voir [Balises personnalisées](https://support.google.com/tagmanager/answer/6107167) dans la documentation de Google.
