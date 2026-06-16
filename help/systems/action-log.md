---
title: Logs d’action
description: Découvrez les journaux d’actions et comment configurer les actions consignées pour vous aider à suivre toutes les modifications apportées à votre boutique.
exl-id: a482adfe-a63f-428b-b078-7542a1e2ecee
feature: Logs, Configuration
TQID: https://experienceleague.adobe.com/UtJhP452hJXDyEyjxrknuF4WPoLza-UcnuWxP6ILtq8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 289
ht-degree: 0%

---

# Logs d’action

{{ee-feature}}

La fonctionnalité Journaux d’actions enregistre (journaux) chaque modification apportée par un utilisateur administrateur qui travaille dans votre boutique. Vous pouvez ainsi suivre toutes les modifications apportées à votre boutique. Le suivi de ces modifications et la définition des [autorisations d’administrateur](permissions.md) pour un utilisateur peuvent vous aider à protéger votre boutique contre les modifications indésirables.

Pour la plupart des actions d’administration, les informations consignées incluent l’action, le nom de l’utilisateur, le succès ou l’échec de l’action et l’identifiant de l’objet affecté par l’action. L’adresse IP et la date sont également consignées.

Par défaut, toutes les actions d’administration sont activées et consignées. Pour configurer la journalisation des actions d’administration, passez en revue les options et cochez ou décochez la case de chaque type d’action. Adobe Commerce enregistre uniquement les types vérifiés.

Affichez le [rapport Journaux d’actions](action-log-report.md) pour consulter les actions d’administration consignées et les détails.

![Configuration avancée - Journalisation des actions d’administration](../configuration-reference/advanced/assets/admin-actions-logging.png){width="600" zoomable="yes"}

Pour obtenir la liste détaillée des paramètres de configuration, voir [Archivage du journal des actions d’administration](../configuration-reference/advanced/system.md) dans la _Référence de configuration_.

## Configuration des actions d’administration pour la journalisation

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL Admin]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Admin Actions Logging]** et procédez comme suit pour chaque action :

   - Pour activer la journalisation des administrateurs pour l’action, cochez la case.
   - Pour désactiver la journalisation de l’administrateur pour l’action, décochez la case.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Archiver le journal des actions d’administration

Les journaux d’action d’administration peuvent être archivés pendant un nombre indéfini de jours. Les archives peuvent également être supprimées après une durée spécifiée.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développez **[!UICONTROL Admin Action Log Archiving]** et définissez les options suivantes :

   - **[!UICONTROL Logs Entry Lifetime, Days]** - Définissez le nombre de jours de conservation du journal archivé.
   - **[!UICONTROL Log Archiving Frequency]** - Définissez la fréquence de création des archives.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
