---
title: '[!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings] de l’administrateur Commerce.
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

Ces paramètres sont disponibles lorsque [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html) est installé.

![Paramètres du Sales Channel](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| Champ | [Portée](../getting-started/websites-stores-views.md#scope-settings) | Description |
|-----|---------|------|
| [!UICONTROL Clear Log History] | Global | Options :<br/><br/>**`Once Daily`**: sélectionnez cette option pour effacer quotidiennement l’historique des activités de votre magasin.<br/><br/>**`Once Weekly`**: sélectionnez cette option pour effacer l’historique des activités de votre magasin une fois par semaine.<br/><br/>**`Once Monthly`**: (par défaut) sélectionnez cette option pour effacer une fois par mois l’historique des activités de votre magasin. |
| [!UICONTROL Background Tasks (CRON) Source] | Global | Sélectionner `Magento CRON` pour spécifier que la variable [!DNL Amazon Sales Channel] utilise vos paramètres cron Commerce pour déterminer les intervalles de communication et de synchronisation des données avec Amazon Seller Central. |
| [!UICONTROL Enable Debug Logging] | Global | Sélectionner `Enabled` pour collecter des données de synchronisation supplémentaires lorsque la résolution des problèmes est nécessaire.<br/><br/>Cette option est désactivée par défaut et ne doit être activée que si nécessaire à des fins de dépannage, car la journalisation continue a un impact négatif sur les performances. S’il est activé pour le dépannage, il doit être désactivé une fois terminé.<br/><br/>**_Remarque _**: la journalisation du Sales Channel Amazon est écrite dans la variable `/var/log/channel_amazon.log` et peuvent être affichés dans [mode développeur](../systems/developer-tools.md#operation-modes). |
| [!UICONTROL Read-Only Mode] | Global | Sélectionner `Enabled` pour bloquer toutes les demandes d’API qui changent l’état sortantes. Les modifications potentielles sont enregistrées, mais ne sont pas envoyées, tant que le mode lecture seule n’est pas désactivé. Pour redémarrer les transferts de données, sélectionnez `Disabled`.<br/><br/>Lorsqu&#39;une base de données est migrée vers une nouvelle copie de l&#39;instance (détectée lorsque l&#39;URL d&#39;un magasin change dans la configuration), le mode lecture seule est automatiquement activé.<br/><br/>Il est conçu pour être utilisé sur des copies de l’instance de production, comme _Évaluation_ ou _QA_, et ne doit pas être utilisé sur l’instance de production.<br/><br/>**_Remarque _**: le cache de configuration doit être effacé pour [!UICONTROL Read-Only Mode] pour l’activer. |

{:style=&quot;table-layout:auto&quot;}
