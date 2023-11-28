---
title: Configuration des événements
description: Découvrez comment terminer la configuration de base pour activer les événements et configurer le bloc d’événement dans la barre latérale du storefront.
exl-id: 620b2d60-ce6f-4f31-93bb-18d3dd9cdce6
feature: Marketing Tools, Promotions/Events
source-git-commit: 084d2c3381f57a8a4c7e8ffde9da1abd4d8af670
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Configuration des événements

{{ee-feature}}

Avant de pouvoir créer un événement, vous devez effectuer la configuration de base pour activer les événements et configurer le bloc d’événement dans la barre latérale.

## Activation et configuration des événements

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en-dessous.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Catalog Events]** et procédez comme suit :

   ![Configuration du catalogue - événements de catalogue](../configuration-reference/catalog/assets/catalog-events.png){width="600" zoomable="yes"}

   - Définir **[!UICONTROL Enable Catalog Events Functionality]** to `Yes`.

   - Définir **[!UICONTROL Enable Catalog Event Widget on Storefront]** to `Yes`.

   - Saisissez le **[!UICONTROL Number of Events to be Displayed in the Event Slider Sidebar Widget]**. Par défaut, cette valeur est définie sur `5`. Si vous souhaitez afficher un seul événement à la fois dans le curseur, saisissez `1`.

   - Saisissez le nombre de **[!UICONTROL Events to Scroll per Click in Event Slider Sidebar Widget]**. Par défaut, cette valeur est définie sur `2`. Si vous souhaitez que le curseur affiche l’événement suivant dans l’ordre en cliquant dessus, saisissez `1`.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

## Restrictions d’accès

L’accès à une vente, un événement ou un site privé peut être limité aux clients enregistrés qui se connectent ou étendu aux clients non enregistrés qui doivent s’inscrire avant d’accéder à .

![Configuration générale - restrictions du site web](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

### Limitation de l’accès

L’accès à une vente, un événement ou un site privé peut être limité aux clients enregistrés qui se connectent ou étendu aux clients non enregistrés qui doivent s’inscrire avant d’accéder à .

![Configuration générale - restrictions du site web](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL General]** et choisissez **[!UICONTROL General]** en-dessous.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Website Restrictions]** .

1. Définir **[!UICONTROL Access Restriction]** to `Yes`.

1. Définir **[!UICONTROL Restriction Mode]** à l’une des options suivantes :

   - `Website Closed`
   - `Private Sales: Login Only`
   - `Private Sales: Login and Register`

1. Définir **[!UICONTROL Startup Page]** à l’une des options suivantes :

   - `To login form (302 Found)` - Les utilisateurs sont redirigés vers le formulaire de connexion avant d’accéder au site.

   - `To landing page (302 Found)` - Les utilisateurs sont redirigés vers la page d’entrée spécifiée jusqu’à ce qu’ils se connectent.

     >[!IMPORTANT]
     >
     >Veillez à inclure un lien vers la page de connexion à partir de la page d’entrée afin que les clients puissent se connecter pour accéder au site.

1. Choisissez la **[!UICONTROL Landing Page]** qui s’affiche avant que les clients ne se connectent au site de vente privé.

1. Pour que les robots de moteur de recherche et les araignées sachent que la page d’entrée est correcte et qu’il n’y a aucune autre page sur le site à indexer, définissez **[!UICONTROL HTTP Response]** to `200 OK`.

   Dans tous les autres cas, définissez sur `503 Service Unavailable`.

   >[!NOTE]
   >
   >Applicable uniquement si le mode de restriction est défini sur _Site Web fermé_. La page d’entrée est rendue en HTML brut.

1. Si vous souhaitez que les champs de la connexion client et des formulaires de mot de passe soient automatiquement renseignés à partir des entrées précédentes, définissez **[!UICONTROL Enable Autocomplete on login/forgot password forms]** to `Yes`.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

### Limiter les ventes

Par défaut, les produits qui apparaissent dans les événements à venir ou fermés ne sont pas disponibles en vente générale et la variable _[!UICONTROL Add to Cart]_n’apparaît pas dans la liste de produits ou la page de produits.

Pour restaurer la variable _[!UICONTROL Add to Cart]_pour un événement fermé, l’événement doit être supprimé (voir [Mise à jour d’événements](event-create.md#update-events)). Cependant, si un produit est associé à une autre catégorie qui n’a aucune restriction de vente, le bouton est disponible sur la page du produit. De même, le bloc de coche n’apparaît pas sur la page de produits si le produit est associé à une autre catégorie qui n’a aucune restriction de vente.
