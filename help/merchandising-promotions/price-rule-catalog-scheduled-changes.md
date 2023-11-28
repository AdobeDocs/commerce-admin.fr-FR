---
title: Modifications planifiées pour les règles de prix de catalogue
description: Découvrez comment appliquer des règles de prix de catalogue selon le calendrier dans le cadre d’une campagne et les regrouper avec d’autres modifications de contenu.
exl-id: ec4b915f-0a27-438d-b1b0-f1bcd297af6d
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 0%

---

# Modifications planifiées pour les règles de prix de catalogue

{{ee-feature}}

La zone Modifications planifiées s’affiche en haut de la page lorsqu’une nouvelle règle de prix est enregistrée ou mise à jour. Les règles de prix du catalogue peuvent être appliquées selon un calendrier dans le cadre d’une campagne et regroupées avec d’autres modifications de contenu. Vous pouvez créer une campagne en fonction des modifications planifiées apportées à une règle de prix ou appliquer les modifications à une campagne existante.

>[!NOTE]
>
>Toutes les mises à jour planifiées sont appliquées consécutivement. Cela signifie qu’une entité ne peut avoir qu’une seule mise à jour planifiée à un moment donné. Toute mise à jour planifiée est appliquée à toutes les vues de magasin au cours de sa période. Par conséquent, une entité ne peut pas avoir simultanément différentes mises à jour planifiées pour différentes vues de magasin. Toutes les valeurs d’attribut d’entité dans toutes les vues de magasin, qui ne sont pas affectées par la mise à jour planifiée actuelle, sont extraites des valeurs par défaut et non de la mise à jour planifiée précédente.

Si plusieurs règles de prix sont exécutées dans la même campagne, le paramètre Priorité de la règle de prix détermine la règle qui prévaut. Pour en savoir plus, voir [Évaluation du contenu](../content-design/content-staging.md).

>[!IMPORTANT]
>
>Si une campagne contenant une règle de prix est initialement créée sans date de fin, elle ne peut pas être modifiée ultérieurement pour inclure une date de fin. Il est recommandé d’ajouter une date de fin lors de la création de la campagne ou de créer une version dupliquée de la campagne existante et d’ajouter la date de fin au doublon, le cas échéant.

![Règle de prix du catalogue - modifications planifiées](./assets/price-rule-catalog-scheduled.png){width="600" zoomable="yes"}

## Planification d’une mise à jour d’une règle de prix de catalogue

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**Règle de prix du catalogue**.

1. Ouvrez la règle en mode d’édition.

1. Dans le **[!UICONTROL Scheduled Changes]** en haut de la page, cliquez sur **[!UICONTROL Schedule New Update]**.

1. Avec la variable **[!UICONTROL Save as a New Update]** sélectionnée, procédez comme suit :

   - Pour **[!UICONTROL Update Name]**, saisissez le nom de la mise à jour de la règle.

   - Entrez un résumé **[!UICONTROL Description]** de la mise à jour, y compris la manière ou les raisons de son application.

   - Utilisez la variable _Calendrier_ (![Icône Calendrier](../assets/icon-calendar.png)) pour choisir la variable **[!DNL Start Date]** et **[!UICONTROL End Date]** pour que la modification planifiée soit en vigueur. Pour créer une modification non terminée, laissez la date de fin vide.

   ![Règles de prix du catalogue - nouvelles modifications planifiées](./assets/price-rule-catalog-schedule-update.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >La date et l’heure de début et de fin sont déterminées par la date/l’heure et le fuseau horaire par défaut du panneau d’administration, et non par le fuseau horaire d’un site web particulier. Tenez compte du fuseau horaire du site web pour déterminer correctement les heures de début et de fin. Créez des règles distinctes pour les sites web dans différents fuseaux horaires qui doivent démarrer et/ou s’arrêter à des heures locales spécifiques.

1. Faites défiler l’écran vers le bas jusqu’à **[!UICONTROL Rule Information]** et modifiez la règle selon vos besoins.

   Vous pouvez planifier des modifications pour n’importe quel paramètre de règle, y compris les sites web (périmètre)/groupes de clients pour la règle, les conditions de la règle et les actions appliquées par la règle. Pour plus d’informations, voir [Création d’une règle de prix de catalogue](price-rules-catalog-create.md).

   >[!NOTE]
   >
   >Si vous définissez sur l’un des paramètres d’informations de règle, assurez-vous que la variable _[!UICONTROL Status]_est définie correctement. Si vous souhaitez que la modification entraîne une règle appliquée de manière active, l’état doit être`Active`.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

   La modification planifiée s’affiche en haut de la page, avec les dates de début et de fin de la campagne.

## Modification d’une règle planifiée

1. Dans le **[!UICONTROL Scheduled Changes]** en haut de la page, cliquez sur **[!UICONTROL View/Edit]**.

1. Apportez les modifications nécessaires à la mise à jour planifiée.

1. Cliquez sur **[!UICONTROL Save]**.

## Aperçu du changement de règle planifié

1. Dans le **[!UICONTROL Scheduled Changes]** en haut de la page, cliquez sur **[!UICONTROL Preview]**.

   L’aperçu ouvre un nouvel onglet du navigateur qui charge votre storefront avec la modification planifiée appliquée. Accédez à un produit qui est affecté par la modification.

   ![Aperçu des modifications planifiées](./assets/price-rule-catalog-scheduled-update-preview.png){width="600" zoomable="yes"}

1. Dans le coin supérieur gauche de la fenêtre Aperçu, cliquez sur **[!UICONTROL Calendar]**.

   Le détail du calendrier affiche d’autres campagnes planifiées pour le même jour. Chaque enregistrement de la liste est une mise à jour de règle distincte.

   ![Liste des mises à jour planifiées pour une date spécifique](./assets/price-rule-catalog-scheduled-preview-calendar.png){width="600" zoomable="yes"}

1. Pour prévisualiser un autre jour ou heure, cliquez sur le bouton **[!UICONTROL Date & Time]** calendar ![Icône Calendrier](../assets/icon-calendar.png) et procédez comme suit :

   - Choisissez une date et/ou une heure différentes.

   - Cliquez sur **[!UICONTROL Preview]**.

1. Pour revenir au calendrier, cliquez sur **[!UICONTROL Calendar]** dans l’en-tête de la page Aperçu.

   À partir de là, vous pouvez effectuer les opérations suivantes :

   **Partage d’un lien vers l’aperçu**

   Pour partager un lien vers l’aperçu du magasin avec vos collègues, cliquez sur **[!UICONTROL Share]**. Copiez le lien dans le Presse-papiers et collez-le dans le corps d’un message électronique.

   >[!NOTE]
   >
   >Un compte d’utilisateur administrateur est requis pour afficher un aperçu partagé. Si votre [rôle a accès](../systems/permissions-user-roles.md) pour créer un compte utilisateur administrateur, vous devez créer le compte d’un nouvel utilisateur avant de le partager.

   **Modification de la portée de l’aperçu**

   Pour afficher les modifications planifiées pour différentes vues de magasin, cliquez sur **[!UICONTROL Scope]** dans l’en-tête de la page Aperçu. Sélectionnez la vue de site web, de magasin ou de magasin que vous souhaitez prévisualiser.

1. Si nécessaire, revenez au calendrier et cliquez sur **[!UICONTROL View/Edit]** dans le _[!UICONTROL Action]_pour ouvrir une autre mise à jour planifiée.
