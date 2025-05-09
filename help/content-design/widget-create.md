---
title: Création et gestion des widgets
description: Découvrez comment créer et gérer des widgets qui mettent automatiquement à jour le contenu dans votre boutique.
exl-id: 680f2f41-ec51-4ac6-9e92-2817591af3e6
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# Création et gestion des widgets

Les widgets sont des composants réutilisables. Vous pouvez facilement créer des widgets et modifier des widgets existants pour mettre automatiquement à jour le contenu dans votre boutique. Vous pouvez également supprimer les widgets qui ne sont plus utilisés.

![Widgets](./assets/widgets.png){width="700" zoomable="yes"}

## Créer un widget

Le processus de création d’un widget est presque le même pour chaque [type de widget](widgets.md#widget-types). Vous pouvez suivre la première partie des instructions, puis la dernière partie pour le type de widget spécifique souhaité.

### Etape 1 : Sélection du type

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Cliquez sur **[!UICONTROL Add Widget]**.

1. Dans la section _[!UICONTROL Settings]_:

   - Définissez **[!UICONTROL Type]** sur le type de widget que vous souhaitez créer.

   - Vérifiez que le **[!UICONTROL Design Theme]** est défini sur le thème actuel.

     ![Paramètres du widget](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Continue]**.

### Étape 2 : spécification des propriétés et de la disposition du storefront

1. Dans la section _[!UICONTROL Storefront Properties]_:

   - Pour **[!UICONTROL Widget Title]**, saisissez un titre descriptif pour le widget.

     Ce titre est visible uniquement à partir de l’administrateur.

   - Pour **[!UICONTROL Assign to Store Views]**, sélectionnez les vues de magasin où le widget doit être visible.

     Vous pouvez sélectionner une vue de magasin spécifique, ou `All Store Views`. Pour sélectionner plusieurs vues, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

   - (Facultatif) Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre dans lequel cet élément apparaît avec les autres dans la même partie de la page. (`0` = premier, `1` = deuxième, `3` = troisième, etc.)

     ![Propriétés Storefront](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

1. Dans la section _[!UICONTROL Layout Updates]_, cliquez sur **[!UICONTROL Add Layout Update]**.

1. Définissez **[!UICONTROL Display On]** sur le type de page où il doit apparaître.

1. Dans la liste **[!UICONTROL Container]**, sélectionnez la zone de mise en page où elle doit être placée.

   ![Mises à jour de mise en page](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

1. Si le widget est un lien, définissez **[!UICONTROL Template]** sur l’un des éléments suivants :

   - `Block Template` - Formate le contenu de sorte qu’il puisse être placé en tant qu’unité autonome sur la page.
   - `Inline Template` - Formate le contenu afin qu’il puisse être placé dans un autre contenu. Par exemple, un lien situé à l’intérieur d’un paragraphe de texte.

### Étape 3 : définition des options du widget

Les options de chaque type de widget varient légèrement, mais le processus est essentiellement le même. L’exemple suivant affiche la liste des produits pour une catégorie spécifique, avec des commandes de pagination.

1. Dans le panneau de gauche, choisissez **[!UICONTROL Widget Options]**.

1. Cliquez sur **[!UICONTROL Select Block]**.

1. Saisissez un **[!UICONTROL Title]** qui apparaîtra au-dessus de la liste, par exemple `Featured Products`.

1. Pour les contrôles de pagination, définissez **[!UICONTROL Display Page Control]** sur `Yes` et procédez comme suit :

   - Saisissez le **[!UICONTROL Number of Products per Page]**.

   - Saisissez le total **[!UICONTROL Number of Products to Display]**.

   - Définissez **[!UICONTROL Condition]** sur la catégorie de produits à présenter.

     Le processus est identique à la définition d’une condition pour une [règle de prix](../merchandising-promotions/price-rules-catalog.md).

### Etape 4 : Enregistrer et vérifier le résultat

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

1. Lorsque vous y êtes invité, suivez les instructions situées en haut de l’espace de travail pour mettre à jour le cache, le cas échéant.

1. Revenez à votre storefront pour vérifier que le widget fonctionne correctement.

   Pour le déplacer vers un autre emplacement, vous pouvez rouvrir le widget et essayer une autre référence de page ou de bloc.

## Démonstration de création de widgets

Pour en savoir plus sur la création de widgets, regardez cette vidéo :

>[!VIDEO](https://video.tv.adobe.com/v/3411056?quality=12&learn=on&captions=fre_fr)

## Modification d’un widget

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Recherchez le widget à l’aide des filtres situés au-dessus de la grille, puis cliquez sur le nom du widget.

1. Apportez les modifications nécessaires.

   Pour plus d’informations sur les options de widget, passez en revue les étapes de création d’un widget.

1. Cliquez sur le **[!UICONTROL Save]**.

## Suppression d’un widget

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Localisez les widgets à l’aide des filtres situés au-dessus de la grille, puis cochez la case des widgets à supprimer.

1. Dans le coin supérieur gauche de la liste, définissez **[!UICONTROL Actions]** sur `Delete`.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Submit]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.
