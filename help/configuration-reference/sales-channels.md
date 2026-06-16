---
title: '[!UICONTROL Sales Channels] > [!UICONTROL Global Settings]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Global Settings] de [!UICONTROL Sales Channels] &gt ; de l’administrateur Commerce.
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
TQID: https://experienceleague.adobe.com/jnjAspEdJbx3unjmoqgH12JEiLz4ThbgFGeFOArOonU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 225
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

Ces paramètres sont disponibles lors de l’installation de [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html?lang=fr).

![Paramètres &#x200B;](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| Champ | [Portée](../getting-started/websites-stores-views.md#scope-settings) | Description |
|-----|---------|------|
| [!UICONTROL Clear Log History] | Global | Options : <br/><br/>**`Once Daily`**: sélectionnez cette option pour effacer l’historique des activités de votre boutique une fois par jour.<br/><br/>**`Once Weekly`** : sélectionnez cette option pour effacer l’historique des activités de votre boutique une fois par semaine.<br/><br/>**`Once Monthly`**: (par défaut) sélectionnez cette option pour effacer l’historique des activités de votre boutique une fois par mois. |
| [!UICONTROL Background Tasks (CRON) Source] | Global | Sélectionnez `Magento CRON` pour indiquer que le [!DNL Amazon Sales Channel] utilise les paramètres cron de Commerce pour déterminer les intervalles de communication et de synchronisation des données avec Amazon Seller Central. |
| [!UICONTROL Enable Debug Logging] | Global | Sélectionnez `Enabled` pour collecter des données de synchronisation supplémentaires lorsque le dépannage est nécessaire.<br/><br/>Cette option est désactivée par défaut et ne doit être activée qu’en cas de nécessité pour le dépannage, car la journalisation continue a un impact négatif sur les performances. Si cette option est activée pour le dépannage, elle doit être désactivée une fois l’opération terminée. |
| [!UICONTROL Read-Only Mode] | Global | Sélectionnez `Enabled` pour bloquer toutes les requêtes d’API de changement d’état sortantes. Les modifications potentielles sont enregistrées, mais pas envoyées, jusqu’à ce que le mode lecture seule soit désactivé. Pour relancer les transferts de données, sélectionnez `Disabled`.<br/><br/>Lorsqu’une base de données est migrée vers une nouvelle copie de l’instance (détectée lorsque l’URL d’un magasin change dans la configuration), le mode lecture seule est automatiquement activé.<br/><br/>Il est conçu pour être utilisé sur des copies de l’instance de production, telles que _Staging_ ou _QA_, et ne doit pas être utilisé sur l’instance de production.<br/><br/>**_Remarque _**: le cache de configuration doit être effacé pour que les [!UICONTROL Read-Only Mode] puissent l’activer. |

{style="table-layout:auto"}
