---
title: Créer et mettre à jour des événements
description: Découvrez comment créer un événement associé à une catégorie à partir de votre catalogue.
exl-id: 6c9f6a33-6785-4c3a-add6-dc2a6b16ed88
feature: Marketing Tools, Promotions/Events
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 0%

---

# Créer et mettre à jour des événements

{{ee-feature}}

Chaque événement est associé à une catégorie de votre catalogue et un seul événement peut être associé à une catégorie donnée à la fois. Pour afficher une liste des événements à venir dans votre magasin, vous devez également configurer une [Carrousel Événements Catalogue](../content-design/widget-event-carousel.md) widget.

![Liste des événements](./assets/category-events.png){width="700" zoomable="yes"}

## Créer un événement

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Catalog Event]**.

1. Dans l’arborescence des catégories, sélectionnez la catégorie à associer à l’événement.

   Chaque catégorie ne pouvant comporter qu’un seul événement à la fois, toutes les catégories qui comportent déjà un événement sont désactivées.

   ![Nouvel événement - arborescence de catégories](./assets/catalog-events-category-tree.png){width="500" zoomable="yes"}

1. Définissez la variable **[!UICONTROL Catalog Event Information]**:

   ![Informations sur les événements du catalogue](./assets/catalog-event-information.png){width="700" zoomable="yes"}

   - Pour le **[!UICONTROL Start Date]** de l’événement, utilisez le calendrier (![Icône Calendrier](../assets/icon-calendar.png)) pour choisir la date. Utilisez la variable **[!UICONTROL Hour]** et **[!UICONTROL Minute]** curseur pour définir l’heure à laquelle l’événement commence.

   - Pour le **[!UICONTROL End Date]** de l’événement, utilisez le calendrier (![Icône Calendrier](../assets/icon-calendar.png)) pour choisir la date. Utilisez la variable **[!UICONTROL Hour]** et **[!UICONTROL Minute]** curseur pour définir l’heure de fin de l’événement.

   - Pour charger un **[!UICONTROL Image]** pour le widget d’événement, cliquez sur **[!UICONTROL Choose File]** et sélectionnez le fichier image dans votre répertoire .

   - Dans le **[!UICONTROL Sort Order]** , saisissez un nombre pour indiquer l’ordre dans lequel cet événement apparaît lorsqu’il est répertorié avec d’autres événements.

   - Cochez la case de chaque type de page où vous souhaitez afficher la coche de compte à rebours.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

## Mise à jour d’événements

Les événements peuvent être modifiés à partir de la page Événements ou de la catégorie associée à l’événement. Lorsqu’une catégorie est associée à un événement, un bouton Modifier l’événement s’affiche dans le coin supérieur droit.

### Méthode 1 : modifiez un événement dans la page Événements

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. Recherchez l’événement dans la liste et ouvrez-le en mode d’édition.

1. Apportez les modifications nécessaires à l’événement.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

### Méthode 2 : modifiez un événement d’une catégorie

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Dans l’arborescence de gauche, sélectionnez la catégorie associée à l’événement.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Edit Even]t**.

1. Apportez les modifications nécessaires à l’événement.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

## Suppression d’un événement

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. Recherchez l’événement dans la liste et ouvrez-le en mode d’édition.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Delete]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

## Descriptions des champs

| Champ | [Portée](../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Category] | Global | Lors de la création d’un événement, ce champ renvoie à l’arborescence des catégories. Lors de la modification d’un événement, il est lié à la page de catégorie associée à l’événement. |
| [!UICONTROL Start Date] | Global | Date et heure de début de l’événement dans `MMDDYYYY HH;MM` format. Cliquez sur l&#39;icône de calendrier pour sélectionner la date. |
| [!DNL End Date] | Global | Date et heure de fin de l’événement dans `MMDDYYYY HH;MM` format. Cliquez sur l&#39;icône de calendrier pour sélectionner la date. |
| [!UICONTROL Image] | Affichage en magasin | Télécharge une image qui s’affiche dans la variable [Widget de carrousel Événements de catalogue](../content-design/widget-event-carousel.md). |
| [!UICONTROL Sort Order] | Global | Détermine la séquence dans laquelle cet événement apparaît lorsqu’il est répertorié avec d’autres événements. |
| [!UICONTROL Display Countdown Ticker On] | Global | Affiche le télex de compte à rebours dans l’en-tête de chaque page spécifiée. Options : `Category Page` / `Product Page` |
| [!UICONTROL Status] | Global | Indique l’état de l’événement en fonction de la date de début et de fin. Status est une valeur en lecture seule. Valeurs : `Open` / `Closed` / `Upcoming` |

{style="table-layout:auto"}

## Barre de boutons

| Bouton | Description |
|--- |--- |
| **[!UICONTROL Back]** | Renvoie à la page Événements sans enregistrer le nouvel événement ou les modifications dans un événement existant. |
| **[!UICONTROL Delete]** | Supprime l’événement. |
| **[!UICONTROL Reset]** | Efface le formulaire des modifications non enregistrées et restaure les informations d’événement d’origine. |
| **[!UICONTROL Save and Continue Edit]** | Enregistre toutes les modifications et conserve le formulaire ouvert en mode d’édition. |
| **[!UICONTROL Save]** | Enregistre les modifications, ferme le formulaire et revient à la page Événements . |

{style="table-layout:auto"}
