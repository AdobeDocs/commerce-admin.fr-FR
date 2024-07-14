---
title: Cron (tâches planifiées)
description: Découvrez comment contrôler l’exécution et la planification des tâches Commerce cron à partir de l’administrateur.
exl-id: e0da08ab-212f-4977-9387-0b4b40560cfb
feature: System, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Cron (tâches planifiées)

Adobe Commerce et Magento Open Source exécutent certaines opérations selon le calendrier en exécutant régulièrement un script. Vous pouvez contrôler l’exécution et la planification des tâches Commerce cron à partir de l’administrateur. Les opérations de magasin qui s’exécutent selon un planning cron incluent, sans s’y limiter, les opérations suivantes :

- [Email](email-communications.md)
- [Règles de prix du catalogue](../merchandising-promotions/price-rules-catalog.md)
- [Newsletters](../merchandising-promotions/newsletters.md)
- [Génération du plan de site XML](../merchandising-promotions/sitemap-xml.md)
- [Mises à jour du taux de devise](../stores-purchase/currency-update.md)
- [Inventory management](../inventory-management/introduction.md)

>[!IMPORTANT]
>
>Les services Commerce doivent être installés dans crontab pour s’assurer que les composants principaux et certaines extensions tierces fonctionnent comme prévu. Pour plus d’informations sur l’installation des services sur crontab, reportez-vous aux [instructions du _Guide d’installation_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html).

En outre, vous pouvez configurer les éléments suivants pour qu’ils s’exécutent selon un planning cron :

- Mises à jour de la grille système de commande et réindexation
- Durée de vie du paiement en attente

Assurez-vous que les [URL de base](../stores-purchase/store-urls.md) du magasin sont correctement définies afin que les URL générées lors des opérations cron soient correctes. Pour Adobe Commerce sur l’infrastructure cloud, reportez-vous à la section [Configuration des tâches cron](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html) du _Guide de l’infrastructure Commerce on Cloud_. Pour on-premise, voir [Configurer et exécuter l’icône](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html) dans le _Guide de configuration_.

## Configuration de cron

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Cron]** .

   ![Configuration avancée - tâches cron](../configuration-reference/advanced/assets/system-cron.png){width="600" zoomable="yes"}

1. Définissez les paramètres suivants pour les groupes **[!UICONTROL Index]** et **[!UICONTROL Default]**.

   Les paramètres sont identiques dans chaque section.

   - **[!UICONTROL Generate Schedules Every]** - Définit la fréquence de génération de la planification (en minutes). Les planifications sont stockées dans la base de données.
   - **[!UICONTROL Schedule Ahead for]** - Définit le délai en minutes de planification des tâches cron avancées (en minutes). Par exemple, si ce paramètre est défini sur `10` et que cron s’exécute, les tâches cron sont planifiées pour les 10 prochaines minutes.
   - **[!UICONTROL Missed if not Run Within]** - Définit le temps (en minutes) utilisé pour déterminer une tâche manquée. Si la tâche cron n’est pas exécutée à l’heure planifiée et que l’heure spécifiée expire, elle ne peut pas être exécutée et son état est défini sur `Missed`.
   - **[!UICONTROL History Cleanup Every]** - Définit l’heure (en minutes) pendant laquelle l’historique des tâches terminées est effacé de la base de données.
   - **[!UICONTROL Success History Lifetime]** - Définit la durée (en minutes) pendant laquelle l’historique des tâches cron avec le statut `Successful` reste dans la base de données.
   - **[!UICONTROL Failure History Lifetime]** - Définit la durée (en minutes) pendant laquelle l’historique des tâches cron avec le statut `Error` reste dans la base de données.
   - **[!UICONTROL Use Separate Process]** - Définit si toutes les tâches cron du groupe sont exécutées dans un processus système distinct. Options : `Yes` / `No`

   ![Configuration avancée - index de groupe cron](../configuration-reference/advanced/assets/system-cron-group-index.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
