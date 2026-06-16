---
title: Tarifs spéciaux
description: Découvrez comment proposer des tarifs spéciaux pour une période donnée.
exl-id: 4a1e2045-f0a8-4bae-a5a3-8ce8b258b217
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/j6DspCgn2P4-pHxXuOd-AiJCL0SBezxg-rn6yYmMIk8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
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
source-wordcount: 855
ht-degree: 0%

---

# Tarifs spéciaux

Un prix spécial peut être offert pour une période déterminée. Pendant la période spécifiée, le prix spécial apparaît au lieu du prix normal, suivi d&#39;une notation qui affiche le prix normal.

![Prix spécial sur une page produit](./assets/storefront-price-special.png){width="700" zoomable="yes"}

## Appliquer un prix spécial à un produit individuel

Vous pouvez facilement définir un prix spécial pour un seul produit du catalogue.

### Utiliser une mise à jour planifiée

{{ee-feature}}

Adobe Commerce prend en charge les [&#x200B; mises à jour planifiées &#x200B;](../content-design/content-staging-scheduled-update.md). Utilisez ces outils promotionnels pour appliquer un prix spécial à un produit spécifique pendant une période spécifiée.

1. Ouvrez le produit en mode d’édition.

1. Cliquez sur **[!UICONTROL Scheduled Update]**.

   ![Ajouter une mise à jour planifiée pour le produit](./assets/product-schedule-new-update.png){width="600" zoomable="yes"}

1. Pour **Mettre à jour le nom**, saisissez un nom pour la promotion de prix spéciaux.

1. Saisissez un bref **[!UICONTROL Description]**.

1. Utilisez l’icône _Calendrier_ ( ![icône de calendrier](../assets/icon-calendar.png) ) pour choisir les **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** de la promotion de prix spéciaux.

   Vous pouvez également utiliser les curseurs **[!UICONTROL Hour]** et **[!UICONTROL Minute]** pour choisir l’heure de début et de fin. Cliquez sur **[!UICONTROL Close]** lorsque le début et la fin sont définis.

   ![Enregistrer comme nouvelle mise à jour](./assets/product-price-special-scheduled-update.png){width="600" zoomable="yes"}

1. Faites défiler l’écran jusqu’au champ _Prix_, cliquez sur **[!UICONTROL Advanced Pricing]**, puis saisissez le montant du **[!UICONTROL Special Price]** à appliquer en fonction de la mise à jour planifiée.

   ![Paramètres de tarification spéciaux](./assets/product-price-special.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Done]** puis sur **[!DNL Save]**.

   En vitrine, le prix spécial doit apparaître à la fois dans la liste du catalogue et sur la page produit.

   La _[!UICONTROL Scheduled Change]_&#x200B;s’affiche en haut de la page.

   ![Modification planifiée](./assets/product-price-special-scheduled-change.png){width="600" zoomable="yes"}

### Utiliser une date de début et de fin simple

{{ce-feature}}

Magento Open Source inclut des options de date de début et de fin simples dans les options de Tarification avancée.

1. Ouvrez le produit en mode d’édition.

1. Faites défiler jusqu’au champ _[!UICONTROL Price]_, cliquez sur **[!UICONTROL Advanced Pricing]**, puis saisissez le montant de la **[!UICONTROL Special Price]**.

1. Utilisez l’icône _Calendrier_ ( ![icône Calendrier](../assets/icon-calendar.png) ) pour choisir les **[!UICONTROL Start Date]** et les **[!UICONTROL End Date]** de la promotion de prix spéciaux.

   Le prix spécial entre en vigueur immédiatement après minuit au début de la date de début (00:01) et se poursuit jusqu’à juste avant minuit (23:59) le jour précédant la date de fin.

   ![Modification planifiée](./assets/product-special-price-from-ce.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Done]** puis sur **[!UICONTROL Save]**.

   En vitrine, le prix spécial doit apparaître à la fois dans la liste du catalogue et sur la page produit.

## Appliquer un prix spécial à plusieurs produits

Vous pouvez également attribuer un prix spécial à plusieurs produits, par exemple plusieurs variations d’un [produit configurable](product-create-configurable.md).

### Fixer un prix spécial pour les produits sélectionnés

{{ee-feature}}

L’exemple suivant montre comment attribuer le même prix spécial à plusieurs variations de produit d’un produit configurable dans Adobe Commerce.

1. Sur la page _[!UICONTROL Products]_, cliquez sur **[!UICONTROL Filters]**&#x200B;et saisissez le **[!UICONTROL Name]**&#x200B;du produit configurable.

1. Définissez **[!UICONTROL Type]** sur `Configurable Product`, puis cliquez sur **[!UICONTROL Apply Filters]**.

1. Si vous souhaitez attribuer le même prix spécial à tous les produits, définissez le contrôle dans l&#39;en-tête de la première colonne sur `Select All`.

   Vous pouvez également cocher la case de chaque produit que vous souhaitez inclure.

1. Définissez la commande **[!UICONTROL Actions]** sur `Update attributes`.

1. Faites défiler jusqu’au champ _[!UICONTROL Special Price]_, cochez la case **[!UICONTROL Change]**&#x200B;située sous le champ&#x200B;_[!UICONTROL Special Price]_ et saisissez le prix spécial que vous souhaitez proposer.

   ![Champs Prix spécial](./assets/product-price-special-commerce.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save]**.

Le prix spécial disponible dans la boutique apparaît dans les annonces du catalogue et sur la page produit. Pour un produit configurable, le prix normal s’affiche également sur la page produit lorsque les options sont sélectionnées.

### Définir un prix spécial et une période pour les produits sélectionnés

{{ce-feature}}

L’exemple suivant montre comment attribuer le même prix spécial à plusieurs variations de produit d’un produit configurable dans Magento Open Source.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Cliquez sur **[!UICONTROL Filters]**.

1. Saisissez le **[!UICONTROL Name]** du produit configurable.

1. Définissez **[!UICONTROL Type]** sur `Simple Product`.

   ![&#x200B; Filtres &#x200B;](./assets/product-price-special-filter.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Apply Filters]**.

   La grille répertorie tous les produits simples qui sont associés en tant que variations du produit configurable.

1. Si vous souhaitez attribuer le même prix spécial à tous les produits, définissez le contrôle dans l&#39;en-tête de la première colonne sur `Select All`.

   Vous pouvez également cocher la case de chaque produit que vous souhaitez inclure.

1. Définissez la commande **[!UICONTROL Actions]** sur `Update attributes`.

   ![Mettre à jour les attributs](./assets/product-price-special-action-update-attributes-ce.png){width="600" zoomable="yes"}

1. Faites défiler jusqu’au champ _** et procédez comme suit :[!UICONTROL Special Price]

   - Cochez la case **[!UICONTROL Change]** sous le champ _[!UICONTROL Special Price]** et saisissez le prix spécial que vous souhaitez proposer.

   - Cochez la case **[!UICONTROL Change]** située sous le champ _Date de début du prix spécial_, cliquez sur le _Calendrier_ ( ![icône Calendrier](../assets/icon-calendar.png) ), puis choisissez la première date de la promotion du prix spécial.

     Le prix spécial entre en vigueur immédiatement après minuit au début de la date de début (00:01) et se poursuit jusqu’à juste avant minuit (23:59) le jour précédant la date de fin.

   - Cochez la case **[!UICONTROL Change]** située sous le champ _Date de fin du prix spécial_, cliquez sur le _Calendrier_ ( ![icône Calendrier](../assets/icon-calendar.png) ), puis choisissez la dernière date de la promotion du prix spécial.

   ![Champs Prix spécial](./assets/product-price-special-action-update-attributes-fields-ce.png){width="600" zoomable="yes"}

1. Cliquez ensuite sur **[!UICONTROL Save]**.

   Un message indique le nombre d&#39;enregistrements mis à jour avec le prix spécial.

   Le prix spécial est disponible dans le magasin à la date spécifiée et apparaît dans les annonces de catalogue et sur la page produit. Pour un produit configurable, le prix normal s’affiche également sur la page produit lorsque les options sont sélectionnées.

   ![Prix spécial pour le produit configurable](./assets/storefront-special-price-configurable-product-detail.png){width="600" zoomable="yes"}

## Test

Si le prix spécial n’apparaît pas correctement dans le storefront sur les pages de liste de catalogue et de produits, videz le cache de votre navigateur :

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > **[!UICONTROL Cache Management]**.

1. Cliquez sur **[!UICONTROL Flush Magento Cache]**.

>[!NOTE]
>
>Le prix du produit **_final_** est calculé comme étant le prix pertinent **_minimum_** selon la formule suivante : <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Prix fixe_** les options personnalisables du produit ne sont _pas_ affectées par les règles Prix du groupe, Prix de niveau, Prix spécial ou Prix catalogue.
