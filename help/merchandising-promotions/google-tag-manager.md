---
title: '[!DNL Google Tag Manager]'
description: Découvrez comment utiliser [!DNL Google Tag Manager] pour gérer les nombreuses balises (fragments de code) liées aux événements de campagne marketing sur vos sites Adobe Commerce.
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '1161'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager] vous aide à gérer les nombreuses balises (fragments de code) liées aux événements de campagne marketing. [!DNL Google Tag Manager] vous permet d’ajouter des balises de suivi à votre site pour mesurer l’audience ou pour personnaliser, recibler ou mener des initiatives marketing de moteur de recherche.

[!DNL Google Tag Manager] transfère directement des données et des événements vers [!DNL Google Analytics], l’amélioration de l’e-commerce et d’autres solutions d’analyse tierces afin de produire une image claire des performances de votre site, de vos produits et promotions.

Vous devriez avoir une [!DNL Google Analytics] et [!DNL Tag Manager] pour continuer ce processus. Les instructions suivantes vous guident tout au long du processus de configuration de vos comptes Google, de configuration de votre boutique Commerce et de création d’une balise.

>[!NOTE]
>
>Si votre entreprise est soumise à des réglementations de confidentialité telles que la variable [Règlement général sur la protection des données](../getting-started/compliance-gdpr.md) et/ou [California Consumer Privacy Act](../getting-started/compliance-ccpa.md), voir [Paramètres de confidentialité de Google](google-tools.md#google-privacy-settings).

## Étape 1. Configurez vos [!DNL Google Analytics] account

Voir [Configuration de la recherche de site](https://support.google.com/analytics/answer/1012264) dans l’aide de Google pour en savoir plus sur les notions de base dont vous avez besoin pour commencer. Reportez-vous également aux guides Google pour [Google Analytics](https://support.google.com/analytics/answer/9304153) et [Gestionnaire de balises de Google](https://support.google.com/tagmanager/answer/6102821).

1. Se connecter à [!DNL Google Analytics] compte .

1. Pour activer **[!UICONTROL Internal Site Search Tracking]**, procédez comme suit :

   - Accédez à **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**.

   - Définir **[!UICONTROL Site Search Tracking]** to `On`.

   - Définir **[!UICONTROL Query]** du paramètre `q`.

   - Une fois terminé, **[!UICONTROL Save]** les paramètres.

1. Pour activer les fonctions d’affichage, procédez comme suit :

   - Choisir **[!UICONTROL Property Settings]**.

   - Sous _[!UICONTROL Advertising Features]_, définit **[!UICONTROL Enable Demographics and Interest Reports]**to `On`.

   - **[!UICONTROL Save]** les paramètres.

1. Pour activer le suivi du commerce électronique, procédez comme suit :

   - Accédez à **[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**.

   - Définir **[!UICONTROL Enable Ecommerce]** to `On`.

   - Définir **[!UICONTROL Enable Enhanced Ecommerce Reporting]** to `On`.

   - **[!UICONTROL Save]** les paramètres.

1. Rechargez la page et vérifiez que tous les paramètres restent `On`.

   >[!NOTE]
   >
   >Si tous les paramètres ne sont pas `On`, répétez les étapes précédentes, enregistrez et rechargez la page. Répétez cette procédure jusqu’à ce que tous les paramètres soient définis sur `On`.

## Étape 2. Configurez vos [!DNL Google Tag Manager] account

Les instructions suivantes expliquent comment configurer un nouveau conteneur avec les paramètres de base. Un exemple [Compositeur](https://developer.adobe.com/commerce/php/development/composer/) Le fichier de configuration (.json) est utilisé pour simplifier le processus, en l’important pour générer une balise dans un nouveau conteneur. Pour cet exemple, il est recommandé de créer un conteneur plutôt que de modifier un conteneur existant.

>[!NOTE]
>
>Pour plus d’informations, voir Google [Exportation et importation de conteneurs](https://support.google.com/tagmanager/answer/6106997). Ces instructions fournissent une présentation pour l’importation d’un exemple JSON dans un nouveau conteneur.

1. Télécharger le fichier lié [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt), ouvrez le fichier dans un éditeur, puis enregistrez-le sous la forme `GTM_M2_Config.json`.

   Le fichier json est directement téléchargé vers [!DNL Google Tag Manager].

1. Accédez à **[!UICONTROL Admin]** > **[!UICONTROL Container]** > **[!UICONTROL Import Container]**.

1. Cliquez sur **[!UICONTROL Choose container file]** et sélectionnez le fichier json.

1. Sous **[!UICONTROL Choose workspace]**, cliquez sur **[!UICONTROL New]**.

1. Saisissez un titre et une description, puis cliquez sur **[!UICONTROL Save]**.

1. Pour importer le fichier, sélectionnez l’une des actions suivantes :

   - La variable **[!UICONTROL Overwrite]** doit être sélectionnée pour un nouveau conteneur.

   - La variable **[!UICONTROL Merge]** doit être sélectionnée si vous utilisez un conteneur existant.

1. Cliquez sur **[!UICONTROL Preview]** pour passer en revue les balises, les déclencheurs et les variables.

1. Pour modifier la variable **[!UICONTROL Google Analytics ID]** qui est référencé dans les variables, procédez comme suit :

   - Accédez à **[!UICONTROL Variables]** > **[!UICONTROL User-Defined Variables]**.

   - Choisir **[!UICONTROL Google Analytics]** et mettre à jour l’espace réservé (`UA-xxxxxx-x`) par les vôtres **[!UICONTROL GA ID]**.

1. Suivez les instructions de Google pour ajouter des balises, des déclencheurs et des variables au nouveau conteneur.

   Si vous souhaitez utiliser un autre conteneur, vous pouvez le déplacer vers le nouveau conteneur.

1. Cliquez sur **[!UICONTROL Confirm]** une fois terminé.

1. Suivez les instructions de Google pour publier le nouveau conteneur.

## Étape 3. Configuration de votre boutique

{{gtag-api-note}}

1. Connectez-vous à l’administrateur de votre boutique Commerce.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Google API]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Google Analytics]** et configurez les éléments suivants :

   ![Configuration des ventes - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - Définir **[!UICONTROL Enable]** to `Yes`.

   - Définir **[!UICONTROL Account type]** to `Google Tag Manager`.

   - Dans le **[!UICONTROL Container ID]** , saisissez votre identifiant GTM (`GTM-xxxxxx`).

   - Si vous utilisez également des Google Analytics pour des expériences de contenu, définissez **Activation des expériences de contenu** to `Yes`.

   - Utilisez les valeurs par défaut pour les champs restants.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

1. Testez votre [!DNL Google Tag Manager] et vérifiez que tout fonctionne correctement.

>[!NOTE]
>
>Chaque conteneur est associé à un site web et vous n’avez besoin que d’un conteneur par compte. Si vous disposez d’une instance Commerce multi-site, vous avez besoin de conteneurs distincts.

## Étape 4. Ajout du code GTM à votre boutique Adobe Commerce

1. Pour copier le code GTM, accédez à **[!UICONTROL Admin]** > **[!UICONTROL Install Google Tag Manager]**.

   Deux fragments de code GTM doivent être ajoutés à votre site Commerce : le premier pour `<head>` et la seconde pour la balise `<body>` balise .

1. Dans l’administrateur Commerce, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**et ouvrez la vue magasin en mode d’édition.

1. Sous _[!UICONTROL Other Settings]_, développer **[!UICONTROL HTML Head]**et collez le code que vous avez copié à partir de GTM pour le `<head>` dans la balise **[!UICONTROL Scripts and Style Sheets]**champ .

   ![Insertion de code dans l’en-tête du HTML](./assets/head-tag.png){width="600" zoomable="yes"}

1. Développer **[!UICONTROL Footer]** et collez le code GTM pour `<body>` dans le **[!UICONTROL Miscellaneous HTML]** champ .

   ![Insertion de code dans le pied de page](./assets/footer-tag-section.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Configuration]**.

## Descriptions des champs

| Champ | Portée | Description |
|--- |--- |--- |
| [!UICONTROL Enable] | Affichage en magasin | Détermine si l’e-commerce amélioré de Google Analytics peut être utilisé pour analyser l’activité dans votre magasin. Options : `Yes` / `No` |
| [!UICONTROL Account type] | Affichage en magasin | Détermine le code de suivi Google utilisé pour surveiller l’activité et le trafic du magasin. Options : `Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | Affichage en magasin | Détermine si les informations d’identification sont supprimées des adresses IP qui apparaissent dans les résultats des Google Analytics. |
| [!UICONTROL Enable Content Experiments] | Affichage en magasin | Active les expériences de contenu Google, qui peuvent être utilisées pour tester jusqu’à dix versions différentes d’une même page. Options : `Yes` / `No` |
| [!UICONTROL Container Id] | Affichage en magasin | If [!DNL Google Tag Manager] est déjà installé et configuré pour votre magasin, l’ID de conteneur apparaît automatiquement dans ce champ. |
| [!UICONTROL List property for the catalog page] | Affichage en magasin | Identifie la propriété Tag Manager associée à la page de catalogue. Valeur par défaut : `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Affichage en magasin | Identifie la propriété Tag Manager associée au bloc de vente croisée. Valeur par défaut : `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Affichage en magasin | Identifie la propriété Tag Manager associée au bloc de vente incitative. Valeur par défaut : `Up-sell` |
| [!UICONTROL List property for the related products block] | Affichage en magasin | Identifie la propriété Tag Manager associée au bloc de produits associé. Valeur par défaut : `Related Products` |
| [!UICONTROL List property for the search results page] | Affichage en magasin | Identifie la propriété Tag Manager associée à la page des résultats de recherche. Valeur par défaut : `Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | Affichage en magasin | Identifie la propriété Tag Manager associée aux étiquettes pour les promotions internes. Valeur par défaut : `Label` |

{style="table-layout:auto"}

## Créer une balise pour le suivi des conversions

Si vous disposez d’un compte Google AdWords, vous pouvez créer une balise qui effectue le suivi des conversions. L’exemple suivant montre comment utiliser les deux [!DNL Google Tag Manager] et [!DNL Google Analytics] pour créer une balise qui se déclenche lors de la conversion de votre magasin. _Succès_ page.

### Étape 1. Création d’une balise

1. Connectez-vous à [!DNL Google Tag Manager] et cliquez sur le lien correspondant au conteneur que vous avez créé pour votre magasin.

1. Dans le **[!UICONTROL New Tag]** , cliquez sur **[!UICONTROL Add a new tag]**.

1. Obtenez les informations suivantes à partir de votre compte AdWords :

   - ID de conversion
   - Étiquette de conversion

   Si vous avez besoin d’aide, consultez Google [site d&#39;assistance](https://support.google.com/tagmanager/answer/6105160).

1. Dans la [!DNL Google Tag Manager] tableau de bord, cliquez sur **[!UICONTROL Google AdWords]** et procédez comme suit :

   - Cliquez sur l’espace réservé du titre et saisissez le nom de la nouvelle balise.

   - Sous **[!UICONTROL Choose Product]**, sélectionnez **[!UICONTROL Google AdWords]**.

   - Sous _[!UICONTROL Choose a Tag Type]_, sélectionnez **[!UICONTROL AdWords Conversion Tracking]**et cliquez sur **[!UICONTROL Continue]**.

1. Saisissez le **[!UICONTROL Conversion ID]** et **[!UICONTROL Conversion Label]** dans votre compte AdWords, puis cliquez sur **[!UICONTROL Continue]**.

### Étape 2. Création d’une règle

Si vous continuez à [!DNL Google Tag Manager] dans le tableau de bord, l’étape suivante consiste à créer une règle qui déclenche la balise sur la page de conversion.

1. Sous **[!UICONTROL Fire On]**, cliquez sur **[!UICONTROL Some Pages]**.

1. Dans le _[!UICONTROL Choose Pages]_, renseignez les paramètres suivants :

   - **[!UICONTROL Name]** - Saisissez un nom pour la description de la page.

   - **[!UICONTROL Variable]** `url`

   - **Opération** - `matches RegEx`

     Pour en savoir plus, voir [Opérateurs de sélecteur Regex et CSS](https://support.google.com/tagmanager/answer/7679109) dans l’aide du Gestionnaire de balises de Google.

   - **[!UICONTROL Value]** - `checkout/success.*`

1. Cochez la case verte, puis cliquez sur **[!UICONTROL Save]**.

   Le déclencheur que vous configurez s’affiche sous la forme d’un bouton bleu dans la section Fire On (Déclencher).

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Tag]**.

### Étape 3. Aperçu et publication

L’étape suivante du processus consiste à prévisualiser la balise. Chaque fois que la balise est prévisualisée, un instantané de la version est enregistré. Lorsque les résultats vous conviennent, accédez à la version à utiliser, puis cliquez sur **[!UICONTROL Publish]**.
