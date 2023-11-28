---
title: Prix spéciaux
description: Découvrez comment proposer des tarifs spéciaux pour une période donnée.
exl-id: 4a1e2045-f0a8-4bae-a5a3-8ce8b258b217
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '851'
ht-degree: 0%

---

# Prix spéciaux

Un prix spécial peut être proposé pour une période donnée. Pendant une période spécifiée, le prix spécial apparaît à la place du prix normal, suivi d’une notation indiquant le prix normal.

![Prix spécial sur une page de produit](./assets/storefront-price-special.png){width="700" zoomable="yes"}

## Appliquer un prix spécial à un produit individuel

Vous pouvez facilement définir un prix spécial pour un seul produit du catalogue.

### Utiliser une mise à jour planifiée

{{ee-feature}}

Adobe Commerce prend en charge les [mises à jour planifiées](../content-design/content-staging-scheduled-update.md). Utilisez ces outils promotionnels pour appliquer un prix spécial à un produit spécifique pendant une période donnée.

1. Ouvrez le produit en mode d’édition.

1. Cliquez sur **[!UICONTROL Scheduled Update]**.

   ![Ajout d’une mise à jour planifiée pour le produit](./assets/product-schedule-new-update.png){width="600" zoomable="yes"}

1. Pour **Nom de la mise à jour**, saisissez un nom pour la promotion prix spécial.

1. Entrez un résumé **[!UICONTROL Description]**.

1. Utilisez la variable _Calendrier_ ( ![icône de calendrier](../assets/icon-calendar.png) ) pour choisir la variable **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** pour la promotion prix spécial.

   Vous pouvez utiliser la variable **[!UICONTROL Hour]** et **[!UICONTROL Minute]** pour choisir également les heures de début et de fin. Cliquez sur **[!UICONTROL Close]** lorsque le début et la fin sont définis.

   ![Enregistrer comme nouvelle mise à jour](./assets/product-price-special-scheduled-update.png){width="600" zoomable="yes"}

1. Faites défiler l’écran vers le bas jusqu’à _Prix_ champ, cliquez sur **[!UICONTROL Advanced Pricing]**, puis saisissez le montant de la variable **[!UICONTROL Special Price]** à appliquer selon la mise à jour planifiée.

   ![Paramètres de tarif spécial](./assets/product-price-special.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Done]** puis **[!DNL Save]**.

   Dans le storefront, le prix spécial doit apparaître à la fois dans la liste des catalogues et sur la page des produits.

   La variable _[!UICONTROL Scheduled Change]_s’affiche en haut de la page.

   ![Modification planifiée](./assets/product-price-special-scheduled-change.png){width="600" zoomable="yes"}

### Utilisation d’une date de début et de fin simple

{{ce-feature}}

Magento Open Source comprend des options simples de date de début et de fin dans les options de tarification avancée.

1. Ouvrez le produit en mode d’édition.

1. Faites défiler l’écran vers le bas jusqu’à _[!UICONTROL Price]_champ, cliquez sur **[!UICONTROL Advanced Pricing]**, puis saisissez la variable **[!UICONTROL Special Price]**quantité.

1. Utilisez la variable _Calendrier_ ( ![Icône Calendrier](../assets/icon-calendar.png) ) pour choisir la variable **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** pour la promotion prix spécial.

   Le prix spécial entrera en vigueur immédiatement après minuit au début de la date de début (00:01) et sera maintenu jusqu&#39;à minuit (23:59) le jour précédant la date de fin.

   ![Modification planifiée](./assets/product-special-price-from-ce.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Done]** puis **[!UICONTROL Save]**.

   Dans le storefront, le prix spécial doit apparaître à la fois dans la liste des catalogues et sur la page des produits.

## Appliquer un prix spécial à plusieurs produits

Vous pouvez également attribuer un prix spécial à plusieurs produits, tels que plusieurs variantes d’une [produit configurable](product-create-configurable.md).

### Définition d’un prix spécial pour les produits sélectionnés

{{ee-feature}}

L’exemple suivant montre comment attribuer le même prix spécial à plusieurs variantes de produits d’un produit configurable dans Adobe Commerce.

1. Sur le _[!UICONTROL Products]_page, cliquez sur **[!UICONTROL Filters]**et saisissez la variable **[!UICONTROL Name]**du produit configurable.

1. Définir **[!UICONTROL Type]** to `Configurable Product` et cliquez sur **[!UICONTROL Apply Filters]**.

1. Si vous souhaitez attribuer le même prix spécial à tous les produits, définissez le contrôle dans l’en-tête de la première colonne sur `Select All`.

   Vous pouvez également cocher la case de chaque produit que vous souhaitez inclure.

1. Définissez la variable **[!UICONTROL Actions]** contrôler à `Update attributes`.

1. Faites défiler l’écran vers le bas jusqu’à _[!UICONTROL Special Price]_et sélectionnez le champ **[!UICONTROL Change]**sous la case_[!UICONTROL Special Price]_ et indiquez le prix spécial que vous souhaitez proposer.

   ![Champs de prix spécial](./assets/product-price-special-commerce.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

Le prix spécial disponible dans le magasin apparaît dans les listes de catalogues et sur la page du produit. Pour un produit configurable, le prix normal apparaît également sur la page du produit lorsque les options sont sélectionnées.

### Définition d’un prix spécial et d’une période pour les produits sélectionnés

{{ce-feature}}

L’exemple suivant montre comment attribuer le même prix spécial à plusieurs variantes de produits d’un produit configurable en Magento Open Source.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Cliquez sur **[!UICONTROL Filters]**.

1. Saisissez le **[!UICONTROL Name]** du produit configurable.

1. Définir **[!UICONTROL Type]** to `Simple Product`.

   ![Filtres](./assets/product-price-special-filter.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Apply Filters]**.

   La grille répertorie tous les produits simples associés en tant que variantes du produit configurable.

1. Si vous souhaitez attribuer le même prix spécial à tous les produits, définissez le contrôle dans l’en-tête de la première colonne sur `Select All`.

   Vous pouvez également cocher la case de chaque produit que vous souhaitez inclure.

1. Définissez la variable **[!UICONTROL Actions]** contrôler à `Update attributes`.

   ![Mise à jour des attributs](./assets/product-price-special-action-update-attributes-ce.png){width="600" zoomable="yes"}

1. Faites défiler jusqu’au _[!UICONTROL Special Price]** et procédez comme suit :

   - Sélectionnez la variable **[!UICONTROL Change]** sous la case à cocher _[!UICONTROL Special Price]** et indiquez le prix spécial que vous souhaitez proposer.

   - Sélectionnez la variable **[!UICONTROL Change]** sous la case _Prix spécial à partir de la date_ , cliquez sur le champ _Calendrier_ ( ![Icône Calendrier](../assets/icon-calendar.png) ), et choisissez la première date de la promotion spéciale de prix.

     Le prix spécial entrera en vigueur immédiatement après minuit au début de la date de début (00:01) et sera maintenu jusqu&#39;à minuit (23:59) le jour précédant la date de fin.

   - Sélectionnez la variable **[!UICONTROL Change]** sous la case _Prix spécial à date_ , cliquez sur le champ _Calendrier_ ( ![Icône Calendrier](../assets/icon-calendar.png) ), et choisissez la dernière date de la promotion spéciale du prix.

   ![Champs de prix spéciaux](./assets/product-price-special-action-update-attributes-fields-ce.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

   Un message indique le nombre d&#39;enregistrements mis à jour avec le prix spécial.

   Le prix spécial est disponible dans le magasin à la date indiquée et apparaît dans les listes de catalogues et sur la page du produit. Pour un produit configurable, le prix normal apparaît également sur la page du produit lorsque les options sont sélectionnées.

   ![Prix spécial pour un produit configurable](./assets/storefront-special-price-configurable-product-detail.png){width="600" zoomable="yes"}

## Tests

Si le prix spécial n’apparaît pas correctement dans le storefront à la fois sur la liste des catalogues et les pages de produits, effacez le cache de votre navigateur :

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL System]** > **[!UICONTROL Cache Management]**.

1. Cliquez sur **[!UICONTROL Flush Magento Cache]**.

>[!NOTE]
>
>La variable **_final_** le prix du produit est calculé comme suit : **_minimum_** prix pertinent, selon la formule suivante : <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Prix fixe_** les options personnalisables du produit sont _not_ affectés par les règles de prix de groupe, de prix de niveau, de prix spécial ou de prix de catalogue ;
