---
title: Modifications planifiées pour les catégories
description: Découvrez comment planifier des modifications de catégorie pour prendre en charge les campagnes marketing et les promotions de magasin.
exl-id: 9e25082f-4e76-4148-b76e-dca0b14971eb
feature: Catalog Management, Categories
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# Modifications planifiées pour les catégories

{{ee-feature}}

Les mises à jour de catégorie peuvent être appliquées selon le calendrier et regroupées avec d’autres modifications de contenu. Vous pouvez créer une campagne en fonction des modifications planifiées apportées à la catégorie ou appliquer les modifications à une campagne existante. Pour en savoir plus, voir [Évaluation du contenu](../content-design/content-staging.md).

>[!NOTE]
>
>Toutes les mises à jour planifiées sont appliquées consécutivement, ce qui signifie que toute entité ne peut avoir qu’une seule mise à jour planifiée à la fois. Toute mise à jour planifiée est appliquée à toutes les vues de magasin au cours de sa période. Par conséquent, une entité ne peut pas avoir plusieurs mises à jour planifiées pour différentes vues de magasin en même temps. Toutes les valeurs d’attribut d’entité dans toutes les vues de magasin, qui ne sont pas affectées par la mise à jour planifiée actuelle, sont extraites des valeurs par défaut et non de la mise à jour planifiée précédente.

## Planification d’une mise à jour d’une catégorie

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Dans l&#39;arborescence de gauche, sélectionnez la catégorie à modifier.

1. Dans le _Modifications planifiées_ en haut de la page, cliquez sur **[!UICONTROL Schedule New Update]**.

   ![Modifications planifiées](./assets/category-scheduled-changes.png){width="600" zoomable="yes"}

1. Avec la variable **[!UICONTROL Save as a New Update]** sélectionnée, définissez les paramètres de base de la mise à jour :

   - Pour **[!UICONTROL Update Name]**, saisissez le nom de la nouvelle campagne d’évaluation de contenu.

   - Entrez un résumé **[!UICONTROL Description]** de la mise à jour et de son utilisation.

   - Utilisez le calendrier ( ![Icône Calendrier](../assets/icon-calendar.png) ) pour choisir la méthode **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** pour la campagne.

   >[!IMPORTANT]
   >
   >Campagne **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** doit être défini à l’aide de la variable **_default_** Fuseau horaire de l’administrateur, converti à partir du fuseau horaire local de chaque site web. Par exemple, avec plusieurs sites web dans différents fuseaux horaires où vous souhaitez lancer une campagne selon un fuseau horaire des États-Unis, vous devez planifier une mise à jour distincte pour chaque fuseau horaire local. Vous définissez la variable **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** pour chacune d’elles, qui est convertie du fuseau horaire local du site web en fuseau horaire d’administration par défaut.

   ![Modifications planifiées](./assets/category-scheduled-changes-new-update.png){width="600" zoomable="yes"}

1. Apportez les modifications nécessaires à la mise à jour planifiée.

1. Pour prévisualiser les modifications, cliquez sur **[!UICONTROL Preview]** dans la barre de boutons supérieure droite.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

## Attribuer à une mise à jour existante

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Dans l&#39;arborescence de gauche, sélectionnez la catégorie à modifier.

1. Dans le _Modifications planifiées_ en haut de la page, cliquez sur **[!UICONTROL Schedule New Update]**.

1. Sélectionner **[!UICONTROL Assign to Existing Campaign]**.

1. Dans la liste, recherchez la campagne nécessaire et cliquez sur **[!UICONTROL Select]**.

1. Apportez les modifications nécessaires à la mise à jour planifiée.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.
