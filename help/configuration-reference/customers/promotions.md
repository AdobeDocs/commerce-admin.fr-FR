---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Promotions]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Customers] &gt; [!UICONTROL Promotions] de l’administrateur Commerce.
exl-id: 93035d46-2e9e-466d-a5e3-d69ce6b662b8
feature: Configuration, Promotions/Events
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Promotions]

{{config}}

## [!UICONTROL Automated Email Reminder Rules]

{{ee-feature}}

![Règles de rappel de messagerie automatisée](./assets/promotions-automated-email-reminder-rules.png)<!-- zoom -->

<!-- [Automated Email Reminder Rules](https://experienceleague.adobe.com/fr/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules#configure-email-reminders) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Reminder Emails] | Global | Active les rappels électroniques automatisés. Si cette option est définie sur Non, les paramètres restants sont ignorés. Options : `Yes` / `No` |
| [!UICONTROL Frequency] | Global | Indique la fréquence à laquelle Commerce doit rechercher les nouveaux clients qui remplissent les critères des rappels d’email automatisés. Options : <br/>**`Minute Intervals`**- Envoie l’email selon l’intervalle sélectionné. (5 minutes, 10 minutes, 15 minutes, 20 minutes ou 30 minutes)<br/>**`Hourly`** - Envoie le courriel toutes les heures, à la minute suivant l’heure spécifiée. Saisissez une valeur comprise entre 0 et 59. <br/>**`Daily`**- Envoie le courrier électronique tous les jours, à partir de l’heure de début. |
| [!UICONTROL Interval] | Global | L’intervalle doit être égal ou supérieur à la période de lancement de cron.php. Options : `5 minutes` / `10 minutes` / `15 minutes` / `20 minutes` / `30 minutes` |
| [!UICONTROL Start Time] | Global | Définit le jour, la minute et la seconde d’envoi de l’email. Spécifié au format 24 heures sur 24, selon l’heure du système sur votre serveur. |
| [!UICONTROL Maximum Emails per One Run] | Global | Limite le nombre d&#39;emails envoyés dans un bloc planifié. |
| [!UICONTROL Email Send Failure Threshold] | Global | Nombre de fois où le rappel tente d’envoyer des notifications à une adresse électronique spécifique et échoue. Lorsque la valeur est définie sur 0, aucun seuil n’est défini et les notifications continuent à être envoyées malgré tous les échecs. |
| [!UICONTROL Reminder Email Sender] | Affichage en magasin | Identité de magasin qui apparaît comme expéditeur de l’email. |

{style="table-layout:auto"}

## [!UICONTROL Auto Generated Specific Coupon Codes]

![Codes de bon spécifiques générés automatiquement](./assets/promotions-auto-generated-specific-coupon-codes.png)<!-- zoom -->

<!-- [Auto Generated Specific Coupon Codes](https://experienceleague.adobe.com/fr/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart-coupon#configure-coupon-codes)  -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Code Length] | Global | Définit la longueur du code de bon, à l’exception du préfixe, du suffixe et des séparateurs. |
| [!UICONTROL Code Format] | Global | Définit le format du code de bon. Les options incluent : <br/>**`Alphanumeric`**- Toute combinaison de lettres et de nombres.<br/>**`Alphabetical`** - Lettres uniquement. <br/>**`Numeric`**- Nombres uniquement. |
| [!UICONTROL Code Prefix] | Global | Une valeur ajoutée au début de tous les codes de bon. Si vous ne souhaitez pas utiliser de préfixe, laissez le champ vide. |
| [!UICONTROL Code Suffix] | Global | Une valeur ajoutée à la fin de tous les codes. Si vous ne souhaitez pas utiliser de suffixe, laissez le champ vide. |
| [!UICONTROL Dash Every X Characters] | Global | Intervalle d’insertion d’un tiret (-) dans tous les codes de coupon. Si vous ne souhaitez pas utiliser de tiret, laissez le champ vide. <br/>_&#x200B;**Remarque :**&#x200B;_ Les codes de bon qui ne diffèrent que par un tiret sont considérés comme des codes différents. |

{style="table-layout:auto"}
