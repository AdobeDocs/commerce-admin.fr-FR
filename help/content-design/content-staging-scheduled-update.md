---
title: Planifier une mise à jour du contenu
description: Consultez cet exemple de campagne utilisé pour planifier un changement de prix temporaire pour un produit.
exl-id: 36b7d7f6-4590-4192-a82b-e5f645b05f62
feature: Page Content, Staging
source-git-commit: b3897ba034770229ef8f3117231bed286abdddb9
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 0%

---

# Planifier une mise à jour du contenu

{{ee-feature}}

L’exemple suivant montre comment planifier une modification de prix temporaire pour un produit. Il inclut la planification et la prévisualisation des modifications, ainsi que l’affichage des mises à jour planifiées sur le calendrier. Bien que cet exemple n’inclue qu’une seule modification, une campagne peut inclure plusieurs modifications apportées aux produits, aux règles de prix, aux pages CMS et à d’autres entités qui doivent avoir lieu en même temps. Suivez une méthode similaire pour spécifier les dates de début et de fin pour l’attribut [!UICONTROL Set Product As New].

>[!NOTE]
>Vous devez créer une mise à jour planifiée pour spécifier une date de début (et de fin) pour [!UICONTROL Set Product As New]. Pour [!UICONTROL Special Price] et [!UICONTROL Design Change], les champs de date de début et de fin sont supprimés d’Adobe Commerce et disponibles dans Magento Open Source uniquement.
>
>Toutes les mises à jour planifiées sont appliquées consécutivement, ce qui signifie que toute entité ne peut avoir qu’une seule mise à jour planifiée à la fois. Toute mise à jour planifiée est appliquée à toutes les vues de magasin au cours de sa période. Par conséquent, une entité ne peut pas avoir une mise à jour planifiée différente pour différentes vues de magasin en même temps. Toutes les valeurs d’attribut d’entité dans toutes les vues de magasin, qui ne sont pas affectées par la mise à jour planifiée actuelle, sont extraites des valeurs par défaut et non de la mise à jour planifiée précédente.

## Planification d’une mise à jour d’un produit

1. Dans la grille _[!UICONTROL Products]_, ouvrez un produit en mode d’édition.

1. Dans la zone _[!UICONTROL Scheduled Changes]_située en haut de la page, cliquez sur **[!UICONTROL Schedule New Update]**.

   ![Planifier une nouvelle mise à jour](./assets/content-staging-product-schedule-new-update.png){width="600" zoomable="yes"}

1. Lorsque l’option **[!UICONTROL Save as a New Update]** est sélectionnée, définissez les paramètres de base de la mise à jour :

   - Pour **[!UICONTROL Update Name]**, saisissez un nom pour la nouvelle campagne d’évaluation de contenu.

   - Saisissez un résumé **[!UICONTROL Description]** de la mise à jour et comment l&#39;utiliser.

   - Utilisez l’outil Calendrier (![Icône Calendrier](../assets/icon-calendar.png)) pour choisir la **Date de début** et la **Date de fin** pour la campagne.

     Pour créer une campagne ouverte, ne spécifiez pas de date de fin (laissez vide). Dans cet exemple, la campagne doit commencer à minuit (le 1er janvier 2021) à 00h00 (heure du Pacifique).


     Pour une campagne de règles de prix créée sans date de fin, une date de fin ne peut pas être ajoutée ultérieurement. Dans ce cas, il est nécessaire de créer une campagne et de définir la date de début sur la date de fin de l&#39;ancienne campagne et celle du nouveau. À cette date de début, l’ancienne campagne se termine et la nouvelle campagne commence comme définie.

     ![Planification de la mise à jour d’un produit](./assets/content-staging-campaign-schedule-update.png){width="600" zoomable="yes"}

     >[!NOTE]
     >
     >La date de début et la date de fin de la campagne doivent être définies à l’aide du fuseau horaire d’administrateur **_default_**, converti à partir du fuseau horaire local de chaque site web. Par exemple, lorsque plusieurs sites web se trouvent dans des fuseaux horaires différents, mais que vous souhaitez lancer une campagne basée sur un fuseau horaire (par défaut) aux États-Unis, vous devez planifier une mise à jour distincte pour chaque fuseau horaire local. Dans ce cas, définissez **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** comme convertis à partir de chaque fuseau horaire de site web local sur le fuseau horaire d’administrateur par défaut.

1. Faites défiler l’écran jusqu’à _[!UICONTROL Price]_et cliquez sur **[!UICONTROL Advanced Pricing]**.

1. Saisissez un **[!UICONTROL Special Price]** pour le produit pendant la campagne planifiée et cliquez sur **[!UICONTROL Done]**.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

   La modification planifiée s’affiche en haut de la page du produit, avec les dates de début et de fin de la campagne.

   ![Modification planifiée](./assets/content-staging-product-scheduled-update-preview-rope.png){width="600" zoomable="yes"}

## Modifier la modification planifiée

1. Dans la zone _Modifications planifiées_ située en haut de la page, cliquez sur **[!UICONTROL View/Edit]**.

1. Apportez les modifications nécessaires à la mise à jour planifiée.

1. Cliquez sur **[!UICONTROL Save]**.

## Aperçu de la modification planifiée

Dans la zone _Modifications planifiées_ située en haut de la page, cliquez sur **[!UICONTROL Preview]**.

L’aperçu ouvre un nouvel onglet du navigateur et indique comment le produit s’affiche pendant la campagne planifiée.

>[!NOTE]
>
>Un aperçu intermédiaire d’une mise à jour planifiée commence toujours à partir de la vue de magasin **default**, ce qui émule l’expérience du client de navigation dans la campagne de mise à jour intermédiaire.

Pour plus d’informations sur l’utilisation des outils de contenu d’aperçu pour modifier la date et la portée de l’aperçu, voir [Aperçu d’une campagne](content-staging-preview.md). Vous pouvez également partager un lien vers l’aperçu du magasin avec vos collègues.
