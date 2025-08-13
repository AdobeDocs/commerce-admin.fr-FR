---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Google API]'
description: Vérifiez les paramètres de configuration sur la page de [!UICONTROL Sales] d’[!UICONTROL Google API] &gt; de l’administrateur Commerce.
exl-id: 5031ad3d-1c9a-4bc6-9bfa-683414dca979
feature: Configuration, Marketing Tools
source-git-commit: 5ee52e8d4f2ebb8fc28f13cca53e87c3529f76d3
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Google API]

{{config}}

## [!UICONTROL Google Analytics]

![Google Analytics](./assets/google-api-analytics-ee.png)<!-- zoom -->

<!-- [Google Analytics](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/google-tools/google-analytics) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Affichage de la boutique | Active l’[!DNL Google Analytics] pour votre boutique. Options : `Yes` / `No` |
| [!UICONTROL Account Type] | Affichage de la boutique | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine les options de configuration en fonction de votre type de compte Google Analytics. Options : Universal Analytics (par défaut) / Google Tag Manager |
| [!UICONTROL Account Number] | Affichage de la boutique | Numéro de compte, ou code de suivi, attribué lors de la création de votre compte [!DNL Google Analytics]. |
| [!UICONTROL Anonymize IP] | Affichage de la boutique | Détermine si les informations d’identification sont supprimées des adresses IP qui apparaissent dans les résultats [!DNL Google Analytics]. |

{style="table-layout:auto"}

## [!UICONTROL Google Analytics - Google Tag Manager]

{{ee-feature}}

![Google Analytics - Type de compte Google Tag Manager](./assets/google-api-analytics-tag-manager.png)<!-- zoom -->

Lorsque **[!UICONTROL Account Type]** est défini sur `Google Tag Manager`, d’autres champs s’affichent.

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container ID] | Affichage de la boutique | ID unique du conteneur de [!DNL Google Tag Manager]. Cette valeur commence généralement par `GTM-`. Cet identifiant se trouve dans votre compte [!DNL Google Tag Manager]. Si [!DNL Google Tag Manager] est déjà installé et configuré pour votre magasin, l’ID de conteneur s’affiche automatiquement dans ce champ. |
| [!UICONTROL List property for the catalog page] | Affichage de la boutique | Identifie la propriété [!DNL Google Tag Manager] associée à la page de catalogue. Valeur par défaut : `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Affichage de la boutique | Identifie la propriété [!DNL Google Tag Manager] associée au bloc de vente croisée. Valeur par défaut : `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Affichage de la boutique | Identifie la propriété [!DNL Google Tag Manager] associée au bloc de vente incitative. Valeur par défaut : `Up-sell` |
| [!UICONTROL List property for the related products block] | Affichage de la boutique | Identifie la propriété [!DNL Google Tag Manager] associée au bloc de produits associés. Valeur par défaut : `Related Products` |
| [!UICONTROL List property for the search results page] | Affichage de la boutique | Identifie la propriété [!DNL Google Tag Manager] associée à la page des résultats de la recherche. Valeur par défaut : `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | Affichage de la boutique | Identifie la propriété [!DNL Google Tag Manager] associée aux libellés des promotions internes. Valeur par défaut : `Label` |

{style="table-layout:auto"}

## [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-google-adwords.png)<!-- zoom -->

<!-- [Google AdWords](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/google-tools/google-adwords) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Affichage de la boutique | Active Google AdWords pour le magasin. Options : `Yes` / `No` |
| [!UICONTROL Conversion ID] | Affichage de la boutique | Identifiant de votre compte Google AdWords. |
| [!UICONTROL Conversion Language] | Affichage de la boutique | Langue utilisée pour les conversions AdWords. Options : `All available languages` |
| [!UICONTROL Conversion Format] | Affichage de la boutique | Détermine le format de la notification [!DNL Google Site Stats] qui apparaît sur la page de conversion. La notification renvoie à une page qui informe les visiteurs sur les cookies utilisés pour suivre leurs visites. Cette valeur numérique est affectée à la variable `google_conversion_format` dans votre script AdWords. Pour en savoir plus, consultez la page [À propos du suivi des conversions](https://support.google.com/google-ads/answer/1722022?hl=en) sur le site web de Google. Options : <br/>**`1`**- Affiche une notification d’une ligne.<br/>**`2`** - (Par défaut) Affiche une notification sur deux lignes. <br/>**`3`**- N’affiche aucune notification du client. |
| [!UICONTROL Conversion Color] | Affichage de la boutique | Détermine la couleur du libellé de conversion. Utilisez un [sélecteur de couleurs](https://www.w3schools.com/colors/colors_picker.asp) pour choisir la valeur hexadécimale. Cette valeur hexadécimale est affectée à la variable `google_conversion_color` dans votre script AdWords. Par exemple : ffffff `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | Affichage de la boutique | Libellé de texte qui s’affiche avec la notification [!DNL Google Site Stats]. Cette chaîne de texte est affectée à la variable `~` dans votre script AdWords. Par exemple : « Merci pour vos achats ! » |
| [!UICONTROL Conversion Value Type] | Affichage de la boutique | Indique le type de valeur utilisé pour déterminer le moment où une conversion a lieu. Options : <br/>**`Dynamic`**- Détermine qu’une conversion a eu lieu en fonction du montant dynamique de la commande.<br/>**`Constant`** - Détermine qu’une conversion a eu lieu en fonction de la valeur saisie. |
| [!UICONTROL Conversion Value] | Affichage de la boutique | Spécifie la valeur utilisée pour un type de valeur de conversion _[!UICONTROL Constant]_. |
| [!UICONTROL Send Order Currency] | Affichage de la boutique | Active les valeurs de conversion de devise spécifiques aux transactions dans AdWords (pour les sites web avec différentes devises de base). |

{style="table-layout:auto"}

## [!UICONTROL Google GTag]

{{gtag-api-note}}

### [!UICONTROL Google Analytics4]

![Google Analytics4](./assets/google-api-gtag-google-analytics4.png)<!-- zoom -->

<!-- [Google Analytics4](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/google-tools/google-analytics) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Affichage de la boutique | Active Google Analytics 4 pour votre boutique. Options : `Yes` / `No` |
| [!UICONTROL Account Type] | Affichage de la boutique | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine les options de configuration en fonction de votre type de compte Google Analytics. Options : `Google Analytics4` (par défaut) / `Google Tag Manager` |
| [!UICONTROL Measurement ID] | Affichage de la boutique | Numéro de compte, ou code de suivi, attribué lors de la création de votre compte Google Analytics. |
| [!UICONTROL Anonymize IP] | Affichage de la boutique | Détermine si les informations d’identification sont supprimées des adresses IP qui apparaissent dans les résultats de Google Analytics. |

{style="table-layout:auto"}

### [!UICONTROL Google Analytics4 - Google Tag Manager]

{{ee-feature}}

![Google Analytics4 - Type de compte Google Tag Manager](./assets/google-api-gtag-google-analytics4-gtm.png)<!-- zoom -->

Lorsque **[!UICONTROL Account Type]** est défini sur `Google Tag Manager`, d’autres champs s’affichent.

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container Id] | Affichage de la boutique | ID unique du conteneur de [!DNL Google Tag Manager]. Cette valeur commence généralement par `GTM-`. Cet identifiant se trouve sur votre compte Google Tab Manager. Si [!DNL Google Tag Manager] est déjà installé et configuré pour votre magasin, l’ID de conteneur s’affiche automatiquement dans ce champ. |
| [!UICONTROL List property for the catalog page] | Affichage de la boutique | Identifie la propriété [!DNL Google Tag Manager] associée à la page de catalogue. Valeur par défaut : `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Affichage de la boutique | Identifie la propriété [!DNL Google Tag Manager] associée au bloc de vente croisée. Valeur par défaut : `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Affichage de la boutique | Identifie la propriété [!DNL Google Tag Manager] associée au bloc de vente incitative. Valeur par défaut : `Up-sell` |
| [!UICONTROL List property for the related products block] | Affichage de la boutique | Identifie la propriété [!DNL Google Tag Manager] associée au bloc de produits associés. Valeur par défaut : `Related Products` |
| [!UICONTROL List property for the search results page] | Affichage de la boutique | Identifie la propriété [!DNL Google Tag Manager] associée à la page des résultats de la recherche. Valeur par défaut : `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | Affichage de la boutique | Identifie la propriété [!DNL Google Tag Manager] associée aux libellés des promotions internes. Valeur par défaut : `Label` |

{style="table-layout:auto"}

### [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-gtag-google-adwords.png)<!-- zoom -->

<!-- -- Google AdWords](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/google-tools/google-adwords) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Affichage de la boutique | Active Google AdWords pour le magasin. Options : `Yes` / `No` |
| [!UICONTROL Conversion ID] | Affichage de la boutique | Identifiant de votre compte Google AdWords. |
| [!UICONTROL Conversion Language] | Affichage de la boutique | Langue utilisée pour les conversions AdWords. Options : toutes les langues disponibles |
| [!UICONTROL Conversion Format] | Affichage de la boutique | Détermine le format de la notification Statistiques du site Google qui s’affiche sur la page de conversion. La notification renvoie à une page qui informe les visiteurs sur les cookies utilisés pour suivre leurs visites. Cette valeur numérique est affectée à la variable `google_conversion_format` dans votre script AdWords. Pour en savoir plus, consultez la page [À propos du suivi des conversions](https://support.google.com/google-ads/answer/1722022?hl=en) sur le site web de Google. Options : <br/>**`1`**- Affiche une notification d’une ligne.<br/>**`2`** - (Par défaut) Affiche une notification sur deux lignes. <br/>**`3`**- N’affiche aucune notification du client. |
| [!UICONTROL Conversion Color] | Affichage de la boutique | Détermine la couleur du libellé de conversion. Utilisez un [sélecteur de couleurs](https://www.w3schools.com/colors/colors_picker.asp) pour choisir la valeur hexadécimale. Cette valeur hexadécimale est affectée à la variable `google_conversion_color` dans votre script AdWords. Par exemple : ffffff `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | Affichage de la boutique | Libellé de texte qui s’affiche avec la notification Statut du site Google. Cette chaîne de texte est affectée à la variable `~` dans votre script AdWords. Par exemple : « Merci pour vos achats ! » |
| [!UICONTROL Conversion Value Type] | Affichage de la boutique | Indique le type de valeur utilisé pour déterminer le moment où une conversion a lieu. Options : <br/>**`Dynamic`**- Détermine qu’une conversion a eu lieu en fonction du montant dynamique de la commande.<br/>**`Constant`** - Détermine qu’une conversion a eu lieu en fonction de la valeur saisie. |
| [!UICONTROL Conversion Value] | Affichage de la boutique | Spécifie la valeur utilisée pour un type de valeur de conversion _[!UICONTROL Constant]_. |
| [!UICONTROL Send Order Currency] | Affichage de la boutique | Active les valeurs de conversion de devise spécifiques aux transactions dans AdWords (pour les sites web avec différentes devises de base). |

{style="table-layout:auto"}
