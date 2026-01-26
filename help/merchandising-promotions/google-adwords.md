---
title: Google AdWords
description: Découvrez comment configurer votre boutique Commerce pour le suivi des conversions Google AdWords afin de mesurer les clics publicitaires qui mènent à une vente ou à une autre action importante.
exl-id: 3dd3beba-edcf-4f9e-a527-7ed3609ef1ae
feature: Marketing Tools, Integration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Google AdWords

[Google AdWords](https://www.google.com/adwords/) est un service que vous pouvez utiliser pour placer des annonces dans les résultats de recherche Google et sur les pages de sociétés du réseau d&#39;affichage Google. Le tableau de bord AdWords comprend des outils permettant de gérer vos campagnes, de suivre les réponses et de mesurer les résultats.

Le suivi des conversions affiche le nombre de clics publicitaires qui entraînent une vente ou une autre action importante. La page _Succès_ qui s’affiche pour votre client après la soumission d’une commande permet d’effectuer le suivi des conversions, car elle s’affiche uniquement après une vente. Une fois la configuration Google AdWords de votre boutique terminée, il n’est pas nécessaire de copier le script de suivi des conversions sur la page Succès , car Commerce dispose déjà des informations nécessaires. Pour en savoir plus, consultez l&#39;aide de [Google AdWords](https://support.google.com/adwords/answer/6095821).

![Résultats de la recherche dans Adobe Ad in Google](./assets/google-adwords-adobe-ad.png){width="500"}

## Étape 1. Création d’une campagne Google AdWords

1. Visitez [Google AdWords](https://ads.google.com/) et inscrivez-vous à un compte.

1. Suivez les instructions pour créer une campagne.

1. Pour configurer le suivi des conversions pour votre campagne, procédez comme suit :

   - Dans l’onglet **[!UICONTROL Tools]** de votre tableau de bord AdWords, choisissez **[!UICONTROL Conversions]** et cliquez sur **[!UICONTROL Conversion]**.

   - Lorsque vous êtes invité à saisir la source de conversion, choisissez **[!UICONTROL Website]**.

   - Saisissez le nom de l’action de conversion dont vous souhaitez effectuer le suivi, puis cliquez sur **[!UICONTROL Done]**.

   - Cliquez sur **[!UICONTROL Value]** et, le cas échéant, attribuez une valeur à la conversion. Par exemple :

      - Si vous gagnez 5 $ sur chaque vente, choisissez `Each time it happens` et attribuez une valeur de `$5`.
      - Si la valeur de chaque vente varie, laissez la valeur vide.

     Pour terminer, cliquez sur **[!UICONTROL Done]**.

   - Cliquez sur **[!UICONTROL Conversion windows]** et renseignez les paramètres pour déterminer la durée pendant laquelle les conversions doivent faire l’objet d’un suivi, la catégorie de rapports et le modèle d’attribution.

1. Cliquez ensuite sur **[!UICONTROL Save and Continue]**.

## Étape 2. Obtenir votre balise de conversion

1. Sous **[!UICONTROL Install your tag]**, choisissez pour compter les conversions sur **[!UICONTROL Page load]**.

1. Vous pouvez, de manière optionnelle, ajouter la notification **[!UICONTROL Google Site Stats]** à la page de conversion.

   La notification s’affiche dans le coin inférieur avec un lien vers les normes de sécurité de Google et l’utilisation des cookies.

1. Pour choisir comment gérer la balise AdWords, effectuez l’une des opérations suivantes :

   - Si vous prévoyez d’ajouter le script à votre boutique vous-même, choisissez **[!UICONTROL Save instructions and tag]**.
   - Si vous prévoyez que quelqu’un d’autre ajoute le script à votre boutique, choisissez **[!UICONTROL Email instructions and tag]**.

1. Cliquez ensuite sur **[!UICONTROL Done]**.

## Étape 3. Configuration de votre boutique

{{gtag-api-note}}

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Si vous configurez Google AdWords pour une vue de magasin spécifique, procédez comme suit :

   - Dans le coin supérieur gauche, choisissez le **[!UICONTROL Store View]** à configurer.

   - Lorsque vous êtes invité à confirmer le changement de portée, cliquez sur **[!UICONTROL OK]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Google API]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Google AdWords]** et procédez comme suit :

   - Définissez **[!UICONTROL Enable]** sur `Yes`.

   - Saisissez le **[!UICONTROL Conversion ID]** de votre script Google AdWords.

   ![Configuration des ventes - API Google Ads](../configuration-reference/sales/assets/google-api-google-adwords.png){width="600" zoomable="yes"}

1. Pour formater la notification Google Sites Stat, procédez comme suit :

   - Définissez **[!UICONTROL Conversion Language]** sur la langue identifiée dans votre script AdWords Google.

   - Saisissez le **[!UICONTROL Conversion Format]** à utiliser pour la notification Google Sites Stat sur la page de conversion.

      - `1` : affiche une notification d’une ligne avec un lien vers des informations supplémentaires sur le suivi de Google.
      - `2` : affiche une notification sur deux lignes avec un lien vers des informations supplémentaires sur le suivi de Google.
      - `3` - N’affiche aucune notification du client.

   - Saisissez le [code hexadécimal](https://www.w3schools.com/colors/colors_picker.asp){:target="_blank"} du **[!UICONTROL Conversion Color]** que vous souhaitez utiliser pour le libellé de notification des statistiques du site Google.

   - Saisissez le texte chiffré du **[!UICONTROL Conversion Label]** qui apparaît dans la notification de statut des sites Google.

     Par exemple : `MlEYCOKBnGoQz6CZoAM`

     **Exemple de code de balise AdWords Google**

     ```html
     <!-- Google Code for Back to School Sale Conversion Page -->
     <script type="text/javascript">
     /* <![CDATA[ */
     var google_conversion_id = 999999999;
     var google_conversion_language = "en";
     var google_conversion_format = "3";
     var google_conversion_color = "ffffff";
     var google_conversion_label = "MlEYCOKBnGoQz6CZoAM";
     var google_remarketing_only = false;
     /* ]]> */
     </script>
     
     <script type="text/javascript" src="//www.googleadservices.com/pagead/conversion.js">
     </script>
     <noscript>
     <div style="display:inline;">
     <img height="1" width="1" style="border-style:none;" alt="" src="//www.googleadservices.com/pagead/conversion/872829007/?label=MlEYCOKBnGoQz6CZoAM&amp;guid=ON&amp;script=0"/>
     
     </noscript>
     ```

1. Définissez **[!UICONTROL Conversion Value Type]** sur l’une des options suivantes :

   - `Dynamic` - Détermine qu&#39;une conversion a eu lieu en fonction de la valeur du montant de commande dynamique.
   - `Constant` - Détermine qu’une conversion a eu lieu en fonction d’une valeur spécifique saisie.

   Pour un type de valeur de conversion _Constante_, saisissez un **[!UICONTROL Value]** spécifique pour que le _[!UICONTROL Order Amount]_&#x200B;soit qualifié de conversion.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Étape 4. Vérification de la configuration

En quelques heures, le statut du suivi dans votre tableau de bord Google AdWords passe de `Unverified` à `No recent conversions` ou `Recording conversions`. Lorsqu’une personne clique sur votre annonce et effectue un achat, la conversion s’affiche sur la page Actions de conversion de votre tableau de bord et de votre rapport de campagne.
