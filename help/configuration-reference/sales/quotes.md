---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Quotes]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Sales] &gt; [!UICONTROL Quotes] de l’administrateur Commerce.
exl-id: 9382552d-1be5-47f2-b0e3-931e5c6298d4
feature: Configuration, Quotes
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Quotes]

{{b2b-feature}}

>[!TIP]
>
>Avec l’installation et l’activation d’Adobe Commerce B2B, l’expérience d’achat peut être personnalisée avec des fonctionnalités spécifiques à l’entreprise. Adobe Commerce B2B est une solution intégrée qui prend en charge les modèles B2B et B2C. Pour plus d’informations sur les fonctionnalités B2B, consultez le [Guide de l’utilisateur d’Adobe Commerce B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

{{config}}

<!-- [Quotes](https://experienceleague.adobe.com/en/docs/commerce-admin/b2b/quotes/quotes) -->

## [!UICONTROL General]

![Général](./assets/quotes-general.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Minimum Amount] | Site Web | Montant minimum du sous-total du panier, après toute remise, qui est requis avant qu’un client puisse envoyer une demande de devis. Valeur par défaut : `0` |
| [!UICONTROL Minimum Amount Message] | Affichage en magasin | Le message qui apparaît dans le panier lorsqu’un client tente d’envoyer une demande de devis, mais que le montant minimum requis n’est pas satisfait. |
| [!UICONTROL Default Expiration Period] | Site Web | Détermine la durée de vie par défaut d’un [guillemet](../../b2b/quote-price-negotiation.md) comme période à partir de la date d’envoi de la demande de guillemet. Options : `Days` / `Weeks` / `Months` |

{style="table-layout:auto"}

## [!UICONTROL Attached Files]

![Fichiers attachés](./assets/quotes-attached-files.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL File formats for upload] | Global | Détermine les formats de fichier pouvant être joints à un guillemet. Valeurs par défaut prises en charge : `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png` et `jpeg` |
| [!UICONTROL Maximum file size] | Global | Détermine la taille maximale d’un fichier joint à un guillemet. Ce paramètre peut être remplacé par la configuration du serveur. |

{style="table-layout:auto"}
