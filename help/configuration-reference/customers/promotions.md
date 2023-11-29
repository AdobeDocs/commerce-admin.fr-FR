---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Promotions]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Customers] &gt; [!UICONTROL Promotions] de l’administrateur Commerce.
exl-id: 93035d46-2e9e-466d-a5e3-d69ce6b662b8
feature: Configuration, Promotions/Events
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Promotions]

{{config}}

## [!UICONTROL Automated Email Reminder Rules]

{{ee-feature}}

![Règles de rappel de courrier électronique automatisé](./assets/promotions-automated-email-reminder-rules.png)<!-- zoom -->

<!-- [Automated Email Reminder Rules](https://docs.magento.com/user-guide/marketing/email-reminder-rules-configure.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Reminder Emails] | Global | Active les rappels électroniques automatisés. Si cette option est définie sur Non, les paramètres restants sont ignorés. Options : `Yes` / `No` |
| [!UICONTROL Frequency] | Global | Indique la fréquence à laquelle Commerce doit vérifier les nouveaux clients qui remplissent les critères des rappels électroniques automatisés. Options : <br/>**`Minute Intervals`**- Envoie l’email selon l’intervalle sélectionné. (5 minutes, 10 minutes, 15 minutes, 20 minutes ou 30 minutes)<br/>**`Hourly`** - Envoie le courrier électronique toutes les heures, à la minute près après l’heure spécifiée. Saisissez une valeur comprise entre 0 et 59. <br/>**`Daily`**- Envoie le courrier électronique tous les jours, à partir de l’heure de début. |
| [!UICONTROL Interval] | Global | L’intervalle doit être égal ou supérieur à la période de lancement de cron.php. Options : `5 minutes` / `10 minutes` / `15 minutes` / `20 minutes` / `30 minutes` |
| [!UICONTROL Start Time] | Global | Définit le jour, la minute et la seconde d’envoi de l’email. Spécifié au format 24 heures sur 24, selon l’heure du système sur votre serveur. |
| [!UICONTROL Maximum Emails per One Run] | Global | Limite le nombre d&#39;emails envoyés dans un bloc planifié. |
| [!UICONTROL Email Send Failure Threshold] | Global | Nombre de fois où le rappel tente d’envoyer des notifications à une adresse électronique spécifique et échoue. Lorsque la valeur est définie sur 0, aucun seuil n’est défini et les notifications continuent à être envoyées malgré tous les échecs. |
| [!UICONTROL Reminder Email Sender] | Affichage en magasin | Identité de magasin qui apparaît comme expéditeur de l’email. |

{style="table-layout:auto"}

## [!UICONTROL Auto Generated Specific Coupon Codes]

![Codes de bon spécifiques générés automatiquement](./assets/promotions-auto-generated-specific-coupon-codes.png)<!-- zoom -->

<!-- [Auto Generated Specific Coupon Codes](https://docs.magento.com/user-guide/marketing/price-rules-cart-coupon-code-configure.md  -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Code Length] | Global | Définit la longueur du code de bon, à l’exception du préfixe, du suffixe et des séparateurs. |
| [!UICONTROL Code Format] | Global | Définit le format du code de bon. Les options incluent : <br/>**`Alphanumeric`**- Toute combinaison de lettres et de nombres.<br/>**`Alphabetical`** - Lettres uniquement. <br/>**`Numeric`**- Nombres uniquement. |
| [!UICONTROL Code Prefix] | Global | Une valeur ajoutée au début de tous les codes de bon. Si vous ne souhaitez pas utiliser de préfixe, laissez le champ vide. |
| [!UICONTROL Code Suffix] | Global | Une valeur ajoutée à la fin de tous les codes. Si vous ne souhaitez pas utiliser de suffixe, laissez le champ vide. |
| [!UICONTROL Dash Every X Characters] | Global | Intervalle d’insertion d’un tiret (-) dans tous les codes de coupon. Si vous ne souhaitez pas utiliser de tiret, laissez le champ vide. <br/>_**Remarque :**_ Les codes coupon qui ne diffèrent que par un tiret sont considérés comme des codes différents. |

{style="table-layout:auto"}
