---
title: '[!UICONTROL Customers] > [!UICONTROL Promotions]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Promotions] de [!UICONTROL Customers] &gt ; de l’administrateur Commerce.
exl-id: 93035d46-2e9e-466d-a5e3-d69ce6b662b8
feature: Configuration, Promotions/Events
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Promotions]

{{config}}

## [!UICONTROL Automated Email Reminder Rules]

{{ee-feature}}

![Règles de rappel d’e-mail automatisées](./assets/promotions-automated-email-reminder-rules.png)<!-- zoom -->

<!-- [Automated Email Reminder Rules](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules#configure-email-reminders) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Reminder Emails] | Global | Active les rappels par e-mail automatisés. Si cette valeur est définie sur Non, les paramètres restants sont ignorés. Options : `Yes` / `No` |
| [!UICONTROL Frequency] | Global | Indique la fréquence à laquelle Commerce doit rechercher les nouveaux clients qui remplissent les critères pour les rappels par e-mail automatisés. Options : <br/>**`Minute Intervals`**- Envoie l’e-mail selon l’intervalle sélectionné. (5 minutes, 10 minutes, 15 minutes, 20 minutes ou 30 minutes)<br/>**`Hourly`** - Envoie un e-mail toutes les heures, à la minute suivant l’heure spécifiée. Saisissez une valeur entre 0 et 59. <br/>**`Daily`**- Envoie un e-mail tous les jours, à partir de l’heure de début. |
| [!UICONTROL Interval] | Global | L&#39;intervalle doit être égal ou supérieur à votre période de lancement cron.php. Options : `5 minutes` / `10 minutes` / `15 minutes` / `20 minutes` / `30 minutes` |
| [!UICONTROL Start Time] | Global | Définit le jour, la minute et la seconde où l’e-mail est envoyé. Spécifié au format 24 heures, en fonction de l’heure système sur votre serveur. |
| [!UICONTROL Maximum Emails per One Run] | Global | Limite le nombre d&#39;emails envoyés dans un bloc planifié. |
| [!UICONTROL Email Send Failure Threshold] | Global | Le nombre de fois où le rappel tente d’envoyer des notifications à une adresse e-mail spécifique et échoue. Lorsque la valeur est définie sur 0, il n’existe aucun seuil et les notifications continuent d’être envoyées malgré les échecs. |
| [!UICONTROL Reminder Email Sender] | Affichage de la boutique | Identité du magasin qui apparaît comme expéditeur de l’e-mail. |

{style="table-layout:auto"}

## [!UICONTROL Auto Generated Specific Coupon Codes]

![Codes de coupon spécifiques générés automatiquement](./assets/promotions-auto-generated-specific-coupon-codes.png)<!-- zoom -->

<!-- [Auto Generated Specific Coupon Codes](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart-coupon#configure-coupon-codes)  -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Code Length] | Global | Définit la longueur du code coupon, à l’exclusion du préfixe, du suffixe et des séparateurs. |
| [!UICONTROL Code Format] | Global | Définit le format du code bon. Les options incluent : <br/>**`Alphanumeric`**- Toute combinaison de lettres et de chiffres.<br/>**`Alphabetical`** - Lettres uniquement. <br/>**`Numeric`**- Nombres uniquement. |
| [!UICONTROL Code Prefix] | Global | Valeur ajoutée au début de tous les codes coupon. Si vous ne souhaitez pas utiliser de préfixe, laissez le champ vide. |
| [!UICONTROL Code Suffix] | Global | Valeur ajoutée à la fin de tous les codes. Si vous ne souhaitez pas utiliser de suffixe, laissez le champ vide. |
| [!UICONTROL Dash Every X Characters] | Global | Intervalle pour insérer un tiret (-) dans tous les codes coupon. Si vous ne souhaitez pas utiliser de tiret, laissez le champ vide. <br/>_&#x200B;**Remarque :**&#x200B;_ les codes coupon qui ne diffèrent que d’un tiret sont considérés comme des codes différents. |

{style="table-layout:auto"}
