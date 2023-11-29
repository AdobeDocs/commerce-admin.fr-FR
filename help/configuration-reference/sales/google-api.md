---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Google API]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Sales] &gt; [!UICONTROL Google API] de l’administrateur Commerce.
exl-id: 5031ad3d-1c9a-4bc6-9bfa-683414dca979
feature: Configuration, Marketing Tools
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '978'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Google API]

{{config}}

## [!UICONTROL Google Analytics]

![Google Analytics](./assets/google-api-analytics-ee.png)<!-- zoom -->

<!-- [Google Analytics](https://docs.magento.com/user-guide/marketing/google-universal-analytics.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Affichage en magasin | Active [!DNL Google Analytics] pour votre magasin. Options : `Yes` / `No` |
| [!UICONTROL Account Type] | Affichage en magasin | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine les options de configuration en fonction du type de compte Google Analytics. Options : Universal Analytics (par défaut) / Google Tag Manager |
| [!UICONTROL Account Number] | Affichage en magasin | Le numéro de compte, ou code de suivi, qui a été attribué lors de la création de votre [!DNL Google Analytics] compte . |
| [!UICONTROL Anonymize IP] | Affichage en magasin | Détermine si les informations d’identification sont supprimées des adresses IP qui apparaissent dans [!DNL Google Analytics] résultats. |
| [!UICONTROL Enable Content Experiments] | Affichage en magasin | Active [Expériences de contenu Google](https://support.google.com/analytics/answer/9366791?hl=en&amp;ref_topic=1745207), qui peut être utilisé pour tester jusqu’à dix versions différentes d’une même page. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Google Analytics - Google Tag Manager]

{{ee-feature}}

![Google Analytics - Type de compte Google Tag Manager](./assets/google-api-analytics-tag-manager.png)<!-- zoom -->

When **[!UICONTROL Account Type]** est défini sur `Google Tag Manager`, d’autres champs s’affichent.

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container ID] | Affichage en magasin | L’identifiant unique de la variable [!DNL Google Tag Manager] conteneur. Cette valeur commence généralement par `GTM-`. Cet identifiant se trouve dans votre [!DNL Google Tag Manager] compte . If [!DNL Google Tag Manager] est déjà installé et configuré pour votre magasin, l’ID de conteneur apparaît automatiquement dans ce champ. |
| [!UICONTROL List property for the catalog page] | Affichage en magasin | Identifie la variable [!DNL Google Tag Manager] de la page de catalogue. Valeur par défaut : `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Affichage en magasin | Identifie la variable [!DNL Google Tag Manager] propriété associée au bloc de vente croisée. Valeur par défaut : `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Affichage en magasin | Identifie la variable [!DNL Google Tag Manager] de la propriété associée au bloc de vente incitative. Valeur par défaut : `Up-sell` |
| [!UICONTROL List property for the related products block] | Affichage en magasin | Identifie la variable [!DNL Google Tag Manager] de la propriété associée au bloc de produits associé. Valeur par défaut : `Related Products` |
| [!UICONTROL List property for the search results page] | Affichage en magasin | Identifie la variable [!DNL Google Tag Manager] de la page des résultats de la recherche. Valeur par défaut : `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | Affichage en magasin | Identifie la variable [!DNL Google Tag Manager] propriété associée aux étiquettes pour les promotions internes. Valeur par défaut : `Label` |

{style="table-layout:auto"}

## [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-google-adwords.png)<!-- zoom -->

<!-- [Google AdWords](https://docs.magento.com/user-guide/marketing/google-adwords.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Affichage en magasin | Active Google AdWords pour le magasin. Options : `Yes` / `No` |
| [!UICONTROL Conversion ID] | Affichage en magasin | Identifiant de votre compte Google AdWords. |
| [!UICONTROL Conversion Language] | Affichage en magasin | Langue utilisée pour les conversions AdWords. Options : `All available languages` |
| [!UICONTROL Conversion Format] | Affichage en magasin | Détermine le format de la variable [!DNL Google Site Stats] qui s’affiche sur la page de conversion. La notification renvoie à une page qui informe les visiteurs des cookies utilisés pour effectuer le suivi de leurs visites. Cette valeur numérique est affectée à la variable `google_conversion_format` dans votre script AdWords. Pour en savoir plus, voir [À propos du suivi des conversions](https://support.google.com/google-ads/answer/1722022?hl=en) sur le site web de Google. Options : <br/>**`1`**- Affiche une notification d’une seule ligne.<br/>**`2`** - (Par défaut) Affiche une notification sur deux lignes. <br/>**`3`**- N’affiche aucune notification du client. |
| [!UICONTROL Conversion Color] | Affichage en magasin | Détermine la couleur du libellé de conversion. Utilisez une [sélecteur de couleurs](https://www.w3schools.com/colors/colors_picker.asp) pour choisir la valeur hexadécimale. Cette valeur hexadécimale est affectée au `google_conversion_color` dans votre script AdWords. Par exemple : ffffff  `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | Affichage en magasin | Un libellé de texte qui s’affiche avec la propriété [!DNL Google Site Stats] notification. Cette chaîne de texte est attribuée à la variable `~` dans votre script AdWords. Par exemple : &quot;Merci pour vos achats !&quot; |
| [!UICONTROL Conversion Value Type] | Affichage en magasin | Indique le type de valeur utilisé pour déterminer le moment où une conversion a lieu. Options : <br/>**`Dynamic`**- Détermine qu’une conversion s’est produite en fonction du montant de la commande dynamique.<br/>**`Constant`** - Détermine qu’une conversion s’est produite en fonction de la valeur saisie. |
| [!UICONTROL Conversion Value] | Affichage en magasin | Indique la valeur utilisée pour un événement _[!UICONTROL Constant]_type de valeur de conversion. |
| [!UICONTROL Send Order Currency] | Affichage en magasin | Active les valeurs de conversion de devise spécifiques aux transactions dans AdWords (pour les sites web avec des devises de base différentes). |

{style="table-layout:auto"}

## [!UICONTROL Google GTag]

{{gtag-api-note}}

### [!UICONTROL Google Analytics4]

![Google Analytics4](./assets/google-api-gtag-google-analytics4.png)<!-- zoom -->

<!-- [Google Analytics4](https://docs.magento.com/user-guide/marketing/google-universal-analytics.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Affichage en magasin | Active Google Analytics 4 pour votre magasin. Options : `Yes` / `No` |
| [!UICONTROL Account Type] | Affichage en magasin | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Détermine les options de configuration en fonction du type de compte Google Analytics. Options : `Google Analytics4` (par défaut) / `Google Tag Manager` |
| [!UICONTROL Measurement ID] | Affichage en magasin | Numéro de compte, ou code de suivi, qui a été attribué lors de la création de votre compte Google Analytics. |
| [!UICONTROL Anonymize IP] | Affichage en magasin | Détermine si les informations d’identification sont supprimées des adresses IP qui apparaissent dans les résultats des Google Analytics. |
| [!UICONTROL Enable Content Experiments] | Affichage en magasin | Active [Expériences de contenu Google](https://support.google.com/analytics/answer/9366791?hl=en&amp;ref_topic=1745207), qui peut être utilisé pour tester jusqu’à dix versions différentes d’une même page. Options : `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Google Analytics4 - Google Tag Manager]

{{ee-feature}}

![Google Analytics 4 - Type de compte Google Tag Manager](./assets/google-api-gtag-google-analytics4-gtm.png)<!-- zoom -->

When **[!UICONTROL Account Type]** est défini sur `Google Tag Manager`, d’autres champs s’affichent.

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container Id] | Affichage en magasin | L’identifiant unique de la variable [!DNL Google Tag Manager] conteneur. Cette valeur commence généralement par `GTM-`. Cet identifiant se trouve dans votre compte Gestionnaire d’onglets Google. If [!DNL Google Tag Manager] est déjà installé et configuré pour votre magasin, l’ID de conteneur apparaît automatiquement dans ce champ. |
| [!UICONTROL List property for the catalog page] | Affichage en magasin | Identifie la variable [!DNL Google Tag Manager] de la page de catalogue. Valeur par défaut : `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Affichage en magasin | Identifie la variable [!DNL Google Tag Manager] propriété associée au bloc de vente croisée. Valeur par défaut : `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Affichage en magasin | Identifie la variable [!DNL Google Tag Manager] de la propriété associée au bloc de vente incitative. Valeur par défaut : `Up-sell` |
| [!UICONTROL List property for the related products block] | Affichage en magasin | Identifie la variable [!DNL Google Tag Manager] de la propriété associée au bloc de produits associé. Valeur par défaut : `Related Products` |
| [!UICONTROL List property for the search results page] | Affichage en magasin | Identifie la variable [!DNL Google Tag Manager] de la page des résultats de la recherche. Valeur par défaut : `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | Affichage en magasin | Identifie la variable [!DNL Google Tag Manager] propriété associée aux étiquettes pour les promotions internes. Valeur par défaut : `Label` |

{style="table-layout:auto"}

### [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-gtag-google-adwords.png)<!-- zoom -->

<!-- -- Google AdWords](https://docs.magento.com/user-guide/marketing/google-adwords.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Affichage en magasin | Active Google AdWords pour le magasin. Options : `Yes` / `No` |
| [!UICONTROL Conversion ID] | Affichage en magasin | Identifiant de votre compte Google AdWords. |
| [!UICONTROL Conversion Language] | Affichage en magasin | Langue utilisée pour les conversions AdWords. Options : toutes les langues disponibles |
| [!UICONTROL Conversion Format] | Affichage en magasin | Détermine le format de la notification Statistiques du site Google qui apparaît sur la page de conversion. La notification renvoie à une page qui informe les visiteurs des cookies utilisés pour effectuer le suivi de leurs visites. Cette valeur numérique est affectée à la variable `google_conversion_format` dans votre script AdWords. Pour en savoir plus, voir [À propos du suivi des conversions](https://support.google.com/google-ads/answer/1722022?hl=en) sur le site web de Google. Options : <br/>**`1`**- Affiche une notification d’une seule ligne.<br/>**`2`** - (Par défaut) Affiche une notification sur deux lignes. <br/>**`3`**- N’affiche aucune notification du client. |
| [!UICONTROL Conversion Color] | Affichage en magasin | Détermine la couleur du libellé de conversion. Utilisez une [sélecteur de couleurs](https://www.w3schools.com/colors/colors_picker.asp) pour choisir la valeur hexadécimale. Cette valeur hexadécimale est affectée au `google_conversion_color` dans votre script AdWords. Par exemple : ffffff  `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | Affichage en magasin | Libellé de texte qui s’affiche avec la notification Statistiques du site Google. Cette chaîne de texte est attribuée à la variable `~` dans votre script AdWords. Par exemple : &quot;Merci pour vos achats !&quot; |
| [!UICONTROL Conversion Value Type] | Affichage en magasin | Indique le type de valeur utilisé pour déterminer le moment où une conversion a lieu. Options : <br/>**`Dynamic`**- Détermine qu’une conversion s’est produite en fonction du montant de la commande dynamique.<br/>**`Constant`** - Détermine qu’une conversion s’est produite en fonction de la valeur saisie. |
| [!UICONTROL Conversion Value] | Affichage en magasin | Indique la valeur utilisée pour un événement _[!UICONTROL Constant]_type de valeur de conversion. |
| [!UICONTROL Send Order Currency] | Affichage en magasin | Active les valeurs de conversion de devise spécifiques aux transactions dans AdWords (pour les sites web avec des devises de base différentes). |

{style="table-layout:auto"}
