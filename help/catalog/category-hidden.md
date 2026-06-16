---
title: Catégories masquées
description: Découvrez comment utiliser des catégories masquées à des fins internes ou créer un lien vers une catégorie qui n’est pas incluse dans le menu de navigation.
exl-id: 43aa74b3-b4cd-488d-aa58-fa2c468fe3a2
feature: Catalog Management, Categories
TQID: https://experienceleague.adobe.com/vXJFiYxeTBcRQxdc4XGrPEPKuBAcqr-mnuUlh1WIskM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 186
ht-degree: 0%

---

# Catégories masquées

Il existe de nombreuses façons d’utiliser les catégories masquées. Vous pouvez créer des niveaux de catégorie supplémentaires pour vos propres besoins internes, mais afficher uniquement les catégories de niveau supérieur pour vos clients. Vous pouvez également créer un lien vers une catégorie qui n’est pas incluse dans le menu de navigation.

## Créer des catégories masquées

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Dans l’arborescence des catégories, sélectionnez la catégorie à masquer et procédez comme suit :

   - Définissez **[!UICONTROL Is Active]** sur `Yes`.
   - Définissez **[!UICONTROL Include in Menu]** sur `No`.

1. Dans la section **[!UICONTROL Display Settings]**, définissez **[!UICONTROL Anchor]** sur `No`.

   ![Catégorie masquée](./assets/hidden-categories.png){width="600" zoomable="yes"}

   La catégorie masquée est active, mais n’apparaît pas dans le menu supérieur ni dans la navigation superposée.

1. Renseignez les paramètres suivants pour chaque sous-catégorie masquée afin de créer des sous-catégories :

   >[!NOTE]
   >
   >Bien que la catégorie soit masquée, vous pouvez créer des sous-catégories sous celle-ci et les rendre actives.

   - Définissez **[!UICONTROL Enable Category]** sur `Yes`.
   - Dans la section **[!UICONTROL Display Settings]**, définissez **[!UICONTROL Anchor]** sur `Yes`.

   En tant que catégories actives, vous pouvez désormais les lier à partir d’autres emplacements de votre boutique, mais elles n’apparaissent pas dans le menu.

1. Cliquez ensuite sur **[!UICONTROL Save]**.
