---
title: Modifications planifiées pour les catégories
description: Découvrez comment planifier des modifications de catégorie pour prendre en charge les campagnes marketing et stocker les promotions.
exl-id: 9e25082f-4e76-4148-b76e-dca0b14971eb
feature: Catalog Management, Categories
TQID: https://experienceleague.adobe.com/OEeNwdPokv1ZM4JFV-fnphk6wWDAQuYI-hu1CCzVibg
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
source-wordcount: 464
ht-degree: 0%

---

# Modifications planifiées pour les catégories

{{ee-feature}}

Les mises à jour de catégorie peuvent être appliquées selon le calendrier et regroupées avec d’autres modifications de contenu. Vous pouvez créer une campagne basée sur les modifications planifiées apportées à la catégorie ou appliquer les modifications à une campagne existante. Pour en savoir plus, voir [Évaluation du contenu](../content-design/content-staging.md).

Lorsque vous planifiez des modifications pour des catégories, tenez compte des points suivants :

- Toutes les mises à jour planifiées sont appliquées de manière consécutive, ce qui signifie que toute entité ne peut avoir qu’une seule mise à jour planifiée à la fois. Toute mise à jour planifiée est appliquée à toutes les vues de magasin au cours de sa période. Par conséquent, une entité ne peut pas avoir plusieurs mises à jour planifiées pour différentes vues de magasin en même temps. Toutes les valeurs d’attribut d’entité dans toutes les vues de magasin, qui ne sont pas affectées par la mise à jour planifiée actuelle, sont extraites des valeurs par défaut, et non de la mise à jour planifiée précédente.

- Si une campagne est liée à plusieurs catégories, elle ne peut être modifiée qu’à partir du [Tableau de bord d’évaluation de contenu](../content-design/content-staging-dashboard.md).

- Si une campagne est liée à plusieurs catégories, elle ne peut être modifiée qu’à partir du [Tableau de bord d’évaluation de contenu](../content-design/content-staging-dashboard.md).

>[!NOTE]
>
>L’onglet [!UICONTROL Schedule Design Update] a été supprimé dans ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce et ne peut pas être modifié directement dans la catégorie. Vous devez créer une mise à jour planifiée pour ces activations.

## Planifier une mise à jour pour une catégorie

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Dans l’arborescence de catégorie à gauche, choisissez la catégorie à modifier.

1. Dans la zone _Modifications planifiées_ en haut de la page, cliquez sur **[!UICONTROL Schedule New Update]**.

   ![Modifications planifiées](./assets/category-scheduled-changes.png){width="600" zoomable="yes"}

1. Lorsque l’option **[!UICONTROL Save as a New Update]** est sélectionnée, définissez les paramètres de base de la mise à jour :

   - Par **[!UICONTROL Update Name]**, saisissez un nom pour la nouvelle campagne d’évaluation de contenu.

   - Saisissez un bref **[!UICONTROL Description]** de la mise à jour et de son utilisation.

   - Utilisez l’outil Calendrier ( ![icône Calendrier](../assets/icon-calendar.png) ) pour choisir les **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** de la campagne.

   >[!IMPORTANT]
   >
   >Les **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** de Campaign doivent être définis à l’aide du fuseau horaire d’administration **_par défaut_**, converti à partir du fuseau horaire local de chaque site web. Par exemple, si plusieurs sites web se trouvent dans des fuseaux horaires différents et que vous souhaitez démarrer une campagne en fonction d’un fuseau horaire des États-Unis, vous devez planifier une mise à jour distincte pour chaque fuseau horaire local. Vous définissez les **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** de chaque, qui est converti du fuseau horaire du site web local en fuseau horaire par défaut de l’administrateur.

   ![Modifications planifiées](./assets/category-scheduled-changes-new-update.png){width="600" zoomable="yes"}

1. Apportez les modifications nécessaires à la mise à jour planifiée.

1. Pour prévisualiser les modifications, cliquez sur **[!UICONTROL Preview]** dans la barre de boutons supérieure droite.

1. Cliquez ensuite sur **[!UICONTROL Save]**.

## Affecter à une mise à jour existante

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Dans l’arborescence de catégorie à gauche, choisissez la catégorie à modifier.

1. Dans la zone _Modifications planifiées_ en haut de la page, cliquez sur **[!UICONTROL Schedule New Update]**.

1. Sélectionnez **[!UICONTROL Assign to Existing Campaign]**.

1. Dans la liste, recherchez la campagne nécessaire et cliquez sur **[!UICONTROL Select]**.

1. Apportez les modifications nécessaires à la mise à jour planifiée.

1. Cliquez ensuite sur **[!UICONTROL Save]**.
