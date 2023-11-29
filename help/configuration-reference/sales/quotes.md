---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Quotes]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Sales] &gt; [!UICONTROL Quotes] de l’administrateur Commerce.
exl-id: 9382552d-1be5-47f2-b0e3-931e5c6298d4
feature: Configuration, Quotes
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Quotes]

{{b2b-feature}}

>[!TIP]
>
>Avec l’installation et l’activation de B2B pour Adobe Commerce, l’expérience d’achat peut être personnalisée avec des fonctionnalités spécifiques à l’entreprise. B2B pour Adobe Commerce est une solution intégrée qui prend en charge les modèles B2B et B2C. Pour plus d’informations sur les fonctionnalités B2B, voir [Guide de l’utilisateur B2B pour Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

{{config}}

<!-- [Quotes](https://docs.magento.com/user-guide/sales/quotes.html) -->

## [!UICONTROL General]

![Général](./assets/quotes-general.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Minimum Amount] | Site Web | Montant minimum du sous-total du panier, après toute remise, qui est requis avant qu’un client puisse envoyer une demande de devis. Valeur par défaut : `0` |
| [!UICONTROL Minimum Amount Message] | Affichage en magasin | Le message qui apparaît dans le panier lorsqu’un client tente d’envoyer une demande de devis, mais que le montant minimum requis n’est pas satisfait. |
| [!UICONTROL Default Expiration Period] | Site Web | Détermine la durée de vie par défaut d’une [guillemet](../../b2b/quote-price-negotiation.md) à partir de la date d’envoi de la demande de devis. Options : `Days` / `Weeks` / `Months` |

{style="table-layout:auto"}

## [!UICONTROL Attached Files]

![Fichiers attachés](./assets/quotes-attached-files.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL File formats for upload] | Global | Détermine les formats de fichier pouvant être joints à un guillemet. Valeurs par défaut prises en charge : `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png`, et `jpeg` |
| [!UICONTROL Maximum file size] | Global | Détermine la taille maximale d’un fichier joint à un guillemet. Ce paramètre peut être remplacé par la configuration du serveur. |

{style="table-layout:auto"}
