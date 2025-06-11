---
title: Création et gestion de widgets
description: Découvrez comment créer et gérer les widgets qui mettent automatiquement à jour le contenu de votre boutique.
exl-id: 680f2f41-ec51-4ac6-9e92-2817591af3e6
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# Création et gestion de widgets

Les widgets sont des composants réutilisables. Vous pouvez facilement créer des widgets et modifier des widgets existants pour mettre automatiquement à jour le contenu de votre boutique. Vous pouvez également supprimer les widgets qui ne sont plus utilisés.

![ Widgets ](./assets/widgets.png){width="700" zoomable="yes"}

## Créer un widget

Le processus de création d’un widget est presque le même pour chaque [type de widget](widgets.md#widget-types). Vous pouvez suivre la première partie des instructions, puis terminer la dernière partie pour le type spécifique de widget que vous souhaitez.

### Etape 1 : sélection du type

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Cliquez sur **[!UICONTROL Add Widget]**.

1. Dans la section _[!UICONTROL Settings]_:

   - Définissez **[!UICONTROL Type]** sur le type de widget que vous souhaitez créer.

   - Vérifiez que la **[!UICONTROL Design Theme]** est définie sur le thème actif.

     ![Paramètres du widget](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Continue]**.

### Étape 2 : spécifier les propriétés et la disposition du storefront

1. Dans la section _[!UICONTROL Storefront Properties]_:

   - Par **[!UICONTROL Widget Title]**, saisissez un titre descriptif pour le widget.

     Ce titre est visible uniquement par l’administrateur.

   - Par **[!UICONTROL Assign to Store Views]**, sélectionnez les vues de la boutique dans lesquelles vous souhaitez que le widget soit visible.

     Vous pouvez sélectionner une vue de magasin spécifique, ou `All Store Views`. Pour sélectionner plusieurs vues, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et cliquez sur chaque option.

   - (Facultatif) Par **[!UICONTROL Sort Order]**, saisissez un nombre pour déterminer l’ordre dans lequel cet élément apparaît avec les autres dans la même partie de la page. (`0` = premier, `1` = deuxième, `3` = troisième, etc.)

     ![Propriétés du storefront](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

1. Dans la section _[!UICONTROL Layout Updates]_, cliquez sur **[!UICONTROL Add Layout Update]**.

1. Définissez **[!UICONTROL Display On]** sur le type de page où elle doit apparaître.

1. Dans la liste **[!UICONTROL Container]**, choisissez la zone de la mise en page où elle doit être placée.

   ![ Mises à jour de la disposition ](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

1. Si le widget est un lien, définissez **[!UICONTROL Template]** sur l’une des options suivantes :

   - `Block Template` - Met en forme le contenu afin qu’il puisse être placé en tant qu’unité autonome sur la page.
   - `Inline Template` - Met en forme le contenu afin qu’il puisse être placé dans un autre contenu. Par exemple, un lien qui rentre dans un paragraphe de texte.

### Étape 3 : définition des options du widget

Les options de chaque type de widget varient légèrement, mais le processus est essentiellement le même. L’exemple suivant affiche la liste des produits d’une catégorie spécifique, avec des contrôles de pagination.

1. Dans le panneau de gauche, choisissez **[!UICONTROL Widget Options]**.

1. Cliquez sur **[!UICONTROL Select Block]**.

1. Saisissez un **[!UICONTROL Title]** à afficher au-dessus de la liste, par exemple `Featured Products`.

1. Pour les contrôles de pagination, définissez **[!UICONTROL Display Page Control]** sur `Yes` et procédez comme suit :

   - Saisissez le **[!UICONTROL Number of Products per Page]**.

   - Saisissez le **[!UICONTROL Number of Products to Display]** total.

   - Définissez **[!UICONTROL Condition]** sur la catégorie de produits à afficher.

     Le processus est identique à la définition d’une condition pour une [règle de prix](../merchandising-promotions/price-rules-catalog.md).

### Étape 4 : enregistrer et vérifier le résultat

1. Cliquez ensuite sur **[!UICONTROL Save]**.

1. Lorsque vous y êtes invité, suivez les instructions situées en haut de l’espace de travail pour mettre à jour le cache si nécessaire.

1. Revenez à votre storefront pour vérifier que le widget fonctionne correctement.

   Pour le déplacer vers un autre emplacement, vous pouvez rouvrir le widget et essayer une autre référence de page ou de bloc.

## Démonstration de la création du widget

Pour en savoir plus sur la création de widgets, regardez cette vidéo :

>[!VIDEO](https://video.tv.adobe.com/v/3411056?quality=12&learn=on&captions=fre_fr)

## Modification d’un widget

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Recherchez le widget en utilisant les filtres au-dessus de la grille, puis cliquez sur le nom du widget.

1. Apportez les modifications nécessaires.

   Pour plus d’informations sur les options de widget, consultez la procédure de création d’un widget .

1. Cliquez sur le **[!UICONTROL Save]** .

## Suppression d’un widget

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Recherchez les widgets à l’aide des filtres situés au-dessus de la grille, puis cochez la case des widgets à supprimer.

1. Dans le coin supérieur gauche de la liste, définissez **[!UICONTROL Actions]** sur `Delete`.

1. Cliquez ensuite sur **[!UICONTROL Submit]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.
