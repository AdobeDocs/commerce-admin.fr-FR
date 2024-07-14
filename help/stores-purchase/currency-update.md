---
title: Mise à jour des taux de change
description: Découvrez comment définir manuellement les taux de devise ou les importer dans votre boutique.
exl-id: 316a7bc8-1118-46e7-82ff-891ada04cd13
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Mise à jour des taux de change

Les taux de change peuvent être définis manuellement ou importés dans le magasin. Pour vous assurer que votre banque de données dispose des taux les plus récents, vous pouvez configurer les taux de devise à mettre à jour automatiquement selon le calendrier.

Avant d’importer des taux de change, effectuez la [configuration du taux de devise](currency-configuration.md) pour spécifier les devises que vous acceptez et pour établir la connexion et le planning d’importation.

![Taux de change](./assets/stores-currency-rate-update.png){width="600" zoomable="yes"}

## Mise à jour manuelle d’un taux de devise

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. Cliquez sur le taux à modifier et saisissez la nouvelle valeur pour chaque devise prise en charge.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Currency Rates]**.

## Importer des taux de change

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. Définissez **[!UICONTROL Import Service]** sur le fournisseur de taux de change.

   Le fournisseur par défaut est `fixer.io (legacy)`.

   >[!IMPORTANT]
   >
   >À compter de la version 2.4.6, le service [[!DNL Fixer.io]](https://fixer.io/) est obsolète et remplacé par le service [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api). Il est vivement recommandé d’utiliser un compte APILayer au lieu d’un compte [!DNL Fixer.io] obsolète.

1. Cliquez sur **[!UICONTROL Import]**.

   Les taux mis à jour apparaissent dans la liste _[!UICONTROL Currency Rates]_. Si les taux ont changé depuis la dernière mise à jour, l’ancien taux apparaît ci-dessous à titre de référence.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Currency Rates]**.

1. Lorsque vous êtes invité à mettre à jour le cache, cliquez sur le lien **[!UICONTROL Cache Management]** et actualisez le cache non valide.

   ![ Message système : actualisez le cache non valide](./assets/currency-cache-update.png){width="600" zoomable="yes"}

## Importer les taux de change selon le calendrier

1. Assurez-vous que [Cron](../systems/cron.md) est activé pour votre magasin.

1. Pour spécifier les devises que vous acceptez et établir la connexion et le planning de l’importation, effectuez la [Configuration du taux de devise](currency-configuration.md).

1. Pour vérifier que les taux sont importés selon le calendrier, consultez la liste _[!UICONTROL Currency Rates]_.

1. Patientez pendant la période du paramètre de fréquence défini pour le planning et vérifiez à nouveau les taux.
