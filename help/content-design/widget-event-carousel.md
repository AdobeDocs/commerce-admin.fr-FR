---
title: Widget de carrousel d’événements de catalogue
description: Découvrez comment utiliser un widget de carrousel d’événements de catalogue pour afficher un curseur des événements à venir sur une page.
exl-id: 4e88b253-f320-4c94-9996-94d7005effc6
feature: Page Content, Promotions/Events
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# Widget de carrousel d’événements de catalogue

{{ee-feature}}

Un widget de carrousel d’événements de catalogue affiche un curseur des événements à venir avec un sélecteur de compte à rebours pour chaque événement. Vous pouvez choisir les pages et la zone de la mise en page où le carrousel doit apparaître, et contrôler la largeur et le nombre d’événements qui s’affichent simultanément. Le résultat que vous obtenez dépend de votre thème, de l’emplacement où il est positionné pour apparaître sur la page et des options que vous choisissez.

![Carrousel d’événements dans la barre latérale gauche](./assets/storefront-event-carousel-sidebar-gear.png){width="700" zoomable="yes"}

## Étape 1 : activation du widget du carrousel de catalogue

Avant de commencer, suivez les [instructions](../merchandising-promotions/event-configure.md) pour configurer le widget _Événement de catalogue_ afin qu’il soit activé pour le storefront.

![Configuration d’événement de catalogue](./assets/config-catalog-catalog-events-1.png){width="500" zoomable="yes"}

## Étape 2 : création du widget

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Widget]**.

1. Dans la section _[!UICONTROL Settings]_, procédez comme suit :

   - Définissez **[!UICONTROL Type]** sur `Catalog Events Carousel`.

   - Sélectionnez le **[!UICONTROL Design Theme]** utilisé par le magasin.

1. Cliquez sur **[!UICONTROL Continue]**.

   ![Paramètres de widget pour un carrousel d’événement](./assets/widget-event-carousel-settings.png){width="500" zoomable="yes"}

1. Dans la section _[!UICONTROL Storefront Properties]_, procédez comme suit :

   - Pour **[!UICONTROL Widget Title]**, saisissez un titre descriptif pour le widget.

     Ce titre est visible uniquement à partir de _Admin_.

   - Pour **[!UICONTROL Assign to Store Views]**, sélectionnez les vues de magasin où le widget doit être visible.

     Vous pouvez sélectionner une vue de magasin spécifique, ou `All Store Views`. Pour sélectionner plusieurs vues, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

   - (Facultatif) Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre dans lequel cet élément apparaît avec les autres dans la même partie de la page. (`0` = premier, `1` = deuxième, `3` = troisième, etc.)

     ![Propriétés de storefront de widgets](./assets/widget-event-carousel-storefront-properties.png){width="600" zoomable="yes"}

## Etape 3 : sélection de l&#39;emplacement

1. Dans la section _Mises à jour de la mise en page_, cliquez sur **[!UICONTROL Add Layout Update]**.

1. Définissez **[!UICONTROL Display On]** sur `Specified Page`.

1. Définissez **[!UICONTROL Page]** sur `CMS Home Page`.

1. Définissez **[!UICONTROL Container]** l’un des paramètres suivants :

   - `Main Content Area`
   - `Sidebar Additional`
   - `Sidebar Main`

   >[!NOTE]
   >
   >Les résultats varient en fonction du thème et de la mise en page. Vous devez également spécifier le _[!UICONTROL Catalog Events Carousel Default Template]_dans la configuration de catégorie.

1. Si vous souhaitez que le carrousel d’événements s’affiche à un autre emplacement du storefront, cliquez sur **[!UICONTROL Add Layout Update]** et répétez ces étapes pour cet emplacement.

   ![Mises à jour de mise en page](./assets/widget-event-carousel-layout-updates-catalog-category-sidebar.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save and Continue Edit]**.

   Pour l’instant, vous pouvez ignorer le message pour actualiser le cache.

## Étape 4 : Configuration des options

1. Dans le panneau de gauche, choisissez **[!UICONTROL Widget Options]**.

1. Pour **[!UICONTROL Frame Size]**, entrez le nombre d’événements que vous souhaitez répertorier simultanément dans le curseur.

   Pour afficher un seul événement à la fois, saisissez `1`.

1. Pour **[!UICONTROL Scroll]**, saisissez le nombre de listes d’événements que vous souhaitez faire défiler par clic.

   Pour accéder à l’événement suivant, saisissez `1`.

1. Pour une largeur personnalisée, saisissez le nombre de pixels pour **[!UICONTROL Block Custom Width]**.

   Sur la page d’exemple suivante, la largeur personnalisée est définie sur 250 pixels.

   ![Options de widget de largeur personnalisée](./assets/widget-options-custom-width.png){width="400" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

1. Lorsque vous êtes invité à actualiser le cache, cliquez sur le lien contenu dans le message situé en haut de la page et suivez les instructions.
