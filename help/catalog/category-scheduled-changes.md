---
title: Modifications planifiées pour les catégories
description: Découvrez comment planifier des modifications de catégorie pour prendre en charge les campagnes marketing et les promotions de magasin.
exl-id: 9e25082f-4e76-4148-b76e-dca0b14971eb
feature: Catalog Management, Categories
source-git-commit: 74cc26e74c3efabc914c27b6d8327a85a77fd6e6
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---

# Modifications planifiées pour les catégories

{{ee-feature}}

Les mises à jour de catégorie peuvent être appliquées selon le calendrier et regroupées avec d’autres modifications de contenu. Vous pouvez créer une campagne en fonction des modifications planifiées apportées à la catégorie ou appliquer les modifications à une campagne existante. Pour en savoir plus, voir [Évaluation de contenu](../content-design/content-staging.md).

>[!NOTE]
>
>L’onglet [!UICONTROL Schedule Design Update] a été supprimé dans ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce et ne peut pas être modifié directement sur la catégorie. Vous devez créer une mise à jour planifiée pour ces activations.

>[!NOTE]
>
>Toutes les mises à jour planifiées sont appliquées consécutivement, ce qui signifie que toute entité ne peut avoir qu’une seule mise à jour planifiée à la fois. Toute mise à jour planifiée est appliquée à toutes les vues de magasin au cours de sa période. Par conséquent, une entité ne peut pas avoir plusieurs mises à jour planifiées pour différentes vues de magasin en même temps. Toutes les valeurs d’attribut d’entité dans toutes les vues de magasin, qui ne sont pas affectées par la mise à jour planifiée actuelle, sont extraites des valeurs par défaut et non de la mise à jour planifiée précédente.

## Planification d’une mise à jour d’une catégorie

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Dans l&#39;arborescence de gauche, sélectionnez la catégorie à modifier.

1. Dans la zone _Modifications planifiées_ située en haut de la page, cliquez sur **[!UICONTROL Schedule New Update]**.

   ![Modifications planifiées](./assets/category-scheduled-changes.png){width="600" zoomable="yes"}

1. Lorsque l’option **[!UICONTROL Save as a New Update]** est sélectionnée, définissez les paramètres de base de la mise à jour :

   - Pour **[!UICONTROL Update Name]**, saisissez un nom pour la nouvelle campagne d’évaluation de contenu.

   - Saisissez un résumé **[!UICONTROL Description]** de la mise à jour et comment l&#39;utiliser.

   - Utilisez l’outil Calendrier ( ![Icône Calendrier](../assets/icon-calendar.png) ) pour choisir les **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** pour la campagne.

   >[!IMPORTANT]
   >
   >Les campagnes **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** doivent être définies à l’aide du fuseau horaire d’ **_par défaut_** de l’administrateur, converti à partir du fuseau horaire local de chaque site web. Par exemple, avec plusieurs sites web dans différents fuseaux horaires où vous souhaitez lancer une campagne selon un fuseau horaire des États-Unis, vous devez planifier une mise à jour distincte pour chaque fuseau horaire local. Vous définissez les **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** pour chacun d’eux, qui est converti du fuseau horaire du site web local vers le fuseau horaire d’administration par défaut.

   ![Modifications planifiées](./assets/category-scheduled-changes-new-update.png){width="600" zoomable="yes"}

1. Apportez les modifications nécessaires à la mise à jour planifiée.

1. Pour prévisualiser les modifications, cliquez sur **[!UICONTROL Preview]** dans la barre de boutons en haut à droite.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

## Attribuer à une mise à jour existante

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Dans l&#39;arborescence de gauche, sélectionnez la catégorie à modifier.

1. Dans la zone _Modifications planifiées_ située en haut de la page, cliquez sur **[!UICONTROL Schedule New Update]**.

1. Sélectionnez **[!UICONTROL Assign to Existing Campaign]**.

1. Dans la liste, recherchez la campagne nécessaire et cliquez sur **[!UICONTROL Select]**.

1. Apportez les modifications nécessaires à la mise à jour planifiée.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Si une campagne est liée à plusieurs catégories, elle ne peut être modifiée qu’à partir du [tableau de bord d’évaluation du contenu](../content-design/content-staging-dashboard.md).