---
title: '[!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings]'
description: Vérifiez les paramètres de configuration sur la page de [!UICONTROL Global Settings] d’[!UICONTROL Sales Channels] &gt; de l’administrateur Commerce.
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

Ces paramètres sont disponibles lors de l’installation de [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html).

![Paramètres Sales Channel](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| Champ | [Portée](../getting-started/websites-stores-views.md#scope-settings) | Description |
|-----|---------|------|
| [!UICONTROL Clear Log History] | Global | Options : <br/><br/>**`Once Daily`**: sélectionnez cette option pour effacer l’historique des activités de votre boutique une fois par jour.<br/><br/>**`Once Weekly`** : sélectionnez cette option pour effacer l’historique des activités de votre boutique une fois par semaine.<br/><br/>**`Once Monthly`**: (par défaut) sélectionnez cette option pour effacer l’historique des activités de votre boutique une fois par mois. |
| [!UICONTROL Background Tasks (CRON) Source] | Global | Sélectionnez `Magento CRON` pour indiquer que le [!DNL Amazon Sales Channel] utilise les paramètres cron de Commerce pour déterminer les intervalles de communication et de synchronisation des données avec Amazon Seller Central. |
| [!UICONTROL Enable Debug Logging] | Global | Sélectionnez `Enabled` pour collecter des données de synchronisation supplémentaires lorsque le dépannage est nécessaire.<br/><br/>Cette option est désactivée par défaut et ne doit être activée qu’en cas de nécessité pour le dépannage, car la journalisation continue a un impact négatif sur les performances. Si cette option est activée pour le dépannage, elle doit être désactivée une fois l’opération terminée. |
| [!UICONTROL Read-Only Mode] | Global | Sélectionnez `Enabled` pour bloquer toutes les requêtes d’API de changement d’état sortantes. Les modifications potentielles sont enregistrées, mais pas envoyées, jusqu’à ce que le mode lecture seule soit désactivé. Pour recommencer les transferts de données, sélectionnez `Disabled`.<br/><br/>Lorsqu’une base de données est migrée vers une nouvelle copie de l’instance (détectée lorsque l’URL d’un magasin change dans la configuration), le mode lecture seule est automatiquement activé.<br/><br/>Il est conçu pour être utilisé sur des copies de l’instance de production, comme _Staging_ ou _QA_, et ne doit pas être utilisé sur l’instance de production.<br/><br/>**_Remarque _**: le cache de configuration doit être effacé pour que les [!UICONTROL Read-Only Mode] puissent l’activer. |

{style="table-layout:auto"}
