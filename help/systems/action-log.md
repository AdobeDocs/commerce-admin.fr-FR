---
title: Logs d’action
description: Découvrez les journaux d’actions et comment configurer les actions consignées pour vous aider à effectuer le suivi de toutes les modifications apportées à votre magasin.
exl-id: a482adfe-a63f-428b-b078-7542a1e2ecee
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Logs d’action

{{ee-feature}}

La fonction Journaux d’action enregistre (journaux) chaque modification effectuée par un utilisateur administrateur qui travaille dans votre boutique. Vous pouvez ainsi effectuer le suivi de toutes les modifications apportées à votre magasin. Suivi de ces modifications et définition de [Autorisations d’administrateur](permissions.md) pour un utilisateur, peut vous aider à protéger votre boutique contre les modifications indésirables.

Pour la plupart des actions d’administration, les informations consignées incluent l’action, le nom de l’utilisateur, le succès ou l’échec de l’action, ainsi que l’identifiant de l’objet affecté par l’action. L’adresse IP et la date sont également consignées.

Par défaut, toutes les actions d’administration sont activées et consignées. Pour configurer la journalisation des actions d’administration, passez en revue les options et cochez ou décochez la case correspondant à chaque type d’action. Adobe Commerce ne consigne que les types cochés.

Afficher la variable [Rapport Journaux d’action](action-log-report.md) pour consulter les actions et les détails de l’administrateur consignés.

![Configuration avancée - Journalisation des actions d’administration](../configuration-reference/advanced/assets/admin-actions-logging.png){width="600" zoomable="yes"}

Pour obtenir la liste détaillée des paramètres de configuration, voir [Archivage du journal des actions d’administration](../configuration-reference/advanced/system.md) dans le _Référence de configuration_.

## Configuration des actions d’administration pour la journalisation

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Admin]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Admin Actions Logging]** et procédez comme suit pour chaque action :

   - Pour activer la journalisation de l’action par l’administrateur, cochez la case .
   - Pour désactiver la journalisation de l’administrateur de l’action, décochez la case.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

## Archiver le journal des actions d’administrateur

Les journaux des actions d’administration peuvent être archivés pendant n’importe quel nombre de jours. Les archives peuvent également être supprimées après une durée spécifiée.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développer **[!UICONTROL Admin Action Log Archiving]** et définissez les options suivantes :

   - **[!UICONTROL Logs Entry Lifetime, Days]** - Définissez le nombre de jours pour conserver le journal archivé.
   - **[!UICONTROL Log Archiving Frequency]** - Définissez la Fréquence de création des archives.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.
