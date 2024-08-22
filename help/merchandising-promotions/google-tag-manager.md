---
title: '[!DNL Google Tag Manager]'
description: Découvrez comment utiliser  [!DNL Google Tag Manager]  pour gérer les nombreuses balises (fragments de code) liées aux événements de campagne marketing sur vos sites Adobe Commerce.
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: be426ca16fb7a72ebeda4a2f92c0f0062a9acc62
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager] est un outil puissant qui vous aide à gérer et déployer efficacement diverses balises (fragments de code) associées à vos événements de campagne marketing. [!DNL Google Tag Manager] vous permet d’ajouter des balises de suivi à votre site pour mesurer l’audience, ou pour personnaliser, recibler ou mener des initiatives marketing de moteur de recherche.

[!DNL Google Tag Manager] transfère directement des données et des événements vers [!DNL Google Analytics], l’e-commerce amélioré et d’autres solutions d’analyse tierces afin de produire une image claire des performances de votre site, de vos produits et de vos promotions.

Vous devez disposer d’un compte [!DNL Google Analytics] et [!DNL Tag Manager] pour continuer ce processus. Les instructions suivantes vous guident tout au long du processus de configuration de vos comptes Google, de votre boutique Commerce et de création d’une balise.

>[!NOTE]
>
>Si votre entreprise est soumise à des réglementations de confidentialité telles que le [Règlement général sur la protection des données](../getting-started/compliance-gdpr.md) et/ou le [California Consumer Privacy Act](../getting-started/compliance-ccpa.md), reportez-vous à la section [Paramètres de confidentialité de Google](google-tools.md#google-privacy-settings).

## Étape 1. Configuration de votre compte [!DNL Google Analytics]

Voir [Configuration de la recherche de site](https://support.google.com/analytics/answer/1012264) dans l’aide de Google pour obtenir les informations de base dont vous avez besoin pour commencer. Consultez également les guides Google pour les [Google Analytics](https://support.google.com/analytics/answer/9304153) et [Gestionnaire de balises Google](https://support.google.com/tagmanager/answer/6102821).

1. Connectez-vous à votre compte [!DNL Google Analytics].

1. Pour activer **[!UICONTROL Internal Site Search Tracking]**, procédez comme suit :

   - Accédez à **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**.

   - Définissez **[!UICONTROL Site Search Tracking]** sur `On`.

   - Définissez le paramètre **[!UICONTROL Query]** sur `q`.

   - Une fois terminé, **[!UICONTROL Save]** les paramètres.

1. Pour activer les fonctions d’affichage, procédez comme suit :

   - Sélectionnez **[!UICONTROL Property Settings]**.

   - Sous _[!UICONTROL Advertising Features]_, définissez **[!UICONTROL Enable Demographics and Interest Reports]**sur `On`.

   - **[!UICONTROL Save]** des paramètres.

1. Pour activer le suivi du commerce électronique, procédez comme suit :

   - Accédez à **[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**.

   - Définissez **[!UICONTROL Enable Ecommerce]** sur `On`.

   - Définissez **[!UICONTROL Enable Enhanced Ecommerce Reporting]** sur `On`.

   - **[!UICONTROL Save]** des paramètres.

1. Rechargez la page et vérifiez que tous les paramètres restent `On`.

   >[!NOTE]
   >
   >Si tous les paramètres ne sont pas `On`, répétez les étapes précédentes, enregistrez et rechargez la page. Répétez cette procédure jusqu’à ce que tous les paramètres soient définis sur `On`.

## Étape 2. Configuration de votre compte [!DNL Google Tag Manager]

Les instructions suivantes expliquent comment configurer un nouveau conteneur avec les paramètres de base. Un exemple de fichier de configuration [Composer](https://developer.adobe.com/commerce/php/development/composer/) (.json) est utilisé pour simplifier le processus, en l’important pour générer une balise dans un nouveau conteneur. Pour cet exemple, il est recommandé de créer un conteneur plutôt que de modifier un conteneur existant.

>[!NOTE]
>
>Pour plus d’informations, voir Google [Export et import de conteneur](https://support.google.com/tagmanager/answer/6106997). Ces instructions fournissent une présentation pour l’importation d’un exemple JSON dans un nouveau conteneur.

1. Téléchargez le fichier lié [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt), ouvrez le fichier dans un éditeur et enregistrez-le sous le nom `GTM_M2_Config.json`.

   Le fichier json est directement téléchargé vers [!DNL Google Tag Manager].

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

   - Sélectionnez **[!UICONTROL Google Analytics]** et mettez à jour l’espace réservé (`UA-xxxxxx-x`) avec votre propre **[!UICONTROL GA ID]**.

1. Suivez les instructions de Google pour ajouter des balises, des déclencheurs et des variables au nouveau conteneur.

   Si vous souhaitez utiliser un autre conteneur, vous pouvez le déplacer vers le nouveau conteneur.

1. Cliquez sur **[!UICONTROL Confirm]** une fois terminé.

1. Suivez les instructions de Google pour publier le nouveau conteneur.

## Étape 3. Configuration de votre boutique

{{gtag-api-note}}

1. Connectez-vous à l’administrateur de votre boutique Commerce.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Google API]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) et configurez les éléments suivants :**[!UICONTROL Google Analytics]**

   ![Configuration des ventes - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - Définissez **[!UICONTROL Enable]** sur `Yes`.

   - Définissez **[!UICONTROL Account type]** sur `Google Tag Manager`.

   - Dans le champ **[!UICONTROL Container ID]** , saisissez votre identifiant GTM (`GTM-xxxxxx`).

   - Si vous utilisez également des Google Analytics pour des expériences de contenu, définissez **Activer les expériences de contenu** sur `Yes`.

   - Utilisez les valeurs par défaut pour les champs restants.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

1. Testez vos paramètres [!DNL Google Tag Manager] et vérifiez que tout fonctionne correctement.

>[!NOTE]
>
>Chaque conteneur est associé à un site web et vous n’avez besoin que d’un conteneur par compte. Si vous disposez d’une instance Commerce multi-site, vous avez besoin de conteneurs distincts.

## Descriptions des champs

| Champ | Portée | Description |
|--- |--- |--- |
| [!UICONTROL Enable] | Affichage en magasin | Détermine si l’e-commerce amélioré de Google Analytics peut être utilisé pour analyser l’activité dans votre magasin. Options : `Yes` / `No` |
| [!UICONTROL Account type] | Affichage en magasin | Détermine le code de suivi Google utilisé pour surveiller l’activité et le trafic du magasin. Options : `Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | Affichage en magasin | Détermine si les informations d’identification sont supprimées des adresses IP qui apparaissent dans les résultats des Google Analytics. |
| [!UICONTROL Enable Content Experiments] | Affichage en magasin | Active les expériences de contenu Google, qui peuvent être utilisées pour tester jusqu’à dix versions différentes d’une même page. Options : `Yes` / `No` |
| [!UICONTROL Container Id] | Affichage en magasin | Si [!DNL Google Tag Manager] est déjà installé et configuré pour votre magasin, l’ID de conteneur apparaît automatiquement dans ce champ. |
| [!UICONTROL List property for the catalog page] | Affichage en magasin | Identifie la propriété Tag Manager associée à la page de catalogue. Valeur par défaut : `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Affichage en magasin | Identifie la propriété Tag Manager associée au bloc de vente croisée. Valeur par défaut : `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Affichage en magasin | Identifie la propriété Tag Manager associée au bloc de vente incitative. Valeur par défaut : `Up-sell` |
| [!UICONTROL List property for the related products block] | Affichage en magasin | Identifie la propriété Tag Manager associée au bloc de produits associé. Valeur par défaut : `Related Products` |
| [!UICONTROL List property for the search results page] | Affichage en magasin | Identifie la propriété Tag Manager associée à la page des résultats de recherche. Valeur par défaut : `Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | Affichage en magasin | Identifie la propriété Tag Manager associée aux étiquettes pour les promotions internes. Valeur par défaut : `Label` |

{style="table-layout:auto"}

## Créer une balise pour le suivi des conversions

Si vous disposez d’un compte Google AdWords, vous pouvez créer une balise qui effectue le suivi des conversions. L’exemple suivant montre comment utiliser [!DNL Google Tag Manager] et [!DNL Google Analytics] pour créer une balise qui se déclenche sur la page de conversion _Succès_ de votre magasin.

### Étape 1. Création d’une balise

1. Connectez-vous à votre compte [!DNL Google Tag Manager] et cliquez sur le lien correspondant au conteneur que vous avez créé pour votre magasin.

1. Dans la zone **[!UICONTROL New Tag]**, cliquez sur **[!UICONTROL Add a new tag]**.

1. Obtenez les informations suivantes à partir de votre compte AdWords :

   - ID de conversion
   - Étiquette de conversion

   Si vous avez besoin d&#39;aide, rendez-vous sur le [site d&#39;assistance](https://support.google.com/tagmanager/answer/6105160) de Google.

1. Dans le tableau de bord [!DNL Google Tag Manager], cliquez sur **[!UICONTROL Google AdWords]** et procédez comme suit :

   - Cliquez sur l’espace réservé du titre et saisissez le nom de la nouvelle balise.

   - Sous **[!UICONTROL Choose Product]**, sélectionnez **[!UICONTROL Google AdWords]**.

   - Sous _[!UICONTROL Choose a Tag Type]_, sélectionnez **[!UICONTROL AdWords Conversion Tracking]**et cliquez sur **[!UICONTROL Continue]**.

1. Saisissez les **[!UICONTROL Conversion ID]** et **[!UICONTROL Conversion Label]** de votre compte AdWords et cliquez sur **[!UICONTROL Continue]**.

### Étape 2. Créer une règle

Suite au tableau de bord [!DNL Google Tag Manager], l’étape suivante consiste à créer une règle qui déclenche la balise sur la page de conversion.

1. Sous **[!UICONTROL Fire On]**, cliquez sur **[!UICONTROL Some Pages]**.

1. Dans la section _[!UICONTROL Choose Pages]_, renseignez les paramètres suivants :

   - **[!UICONTROL Name]** - Entrez un nom pour la description de la page.

   - **[!UICONTROL Variable]** `url`

   - **Opération** - `matches RegEx`

     Pour en savoir plus, voir [Opérateurs de sélecteur Regex et CSS](https://support.google.com/tagmanager/answer/7679109) dans l’aide du Gestionnaire de balises de Google.

   - **[!UICONTROL Value]** - `checkout/success.*`

1. Cochez la case verte et cliquez sur **[!UICONTROL Save]**.

   Le déclencheur que vous configurez s’affiche sous la forme d’un bouton bleu dans la section Fire On (Déclencher).

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Tag]**.

### Étape 3. Aperçu et publication

L’étape suivante du processus consiste à prévisualiser la balise. Chaque fois que la balise est prévisualisée, un instantané de la version est enregistré. Lorsque les résultats vous conviennent, accédez à la version que vous souhaitez utiliser, puis cliquez sur **[!UICONTROL Publish]**.
