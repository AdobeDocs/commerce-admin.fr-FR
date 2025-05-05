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

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et sélectionnez **[!UICONTROL Catalog]** sous .

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) de **[!UICONTROL Catalog Events]** et procédez comme suit :

   ![Configuration du catalogue - événements de catalogue](../configuration-reference/catalog/assets/catalog-events.png){width="600" zoomable="yes"}

   - Définissez **[!UICONTROL Enable Catalog Events Functionality]** sur `Yes`.

   - Définissez **[!UICONTROL Enable Catalog Event Widget on Storefront]** sur `Yes`.

   - Saisissez le **[!UICONTROL Number of Events to be Displayed in the Event Slider Sidebar Widget]**. Par défaut, cette valeur est définie sur `5`. Si vous souhaitez afficher un seul événement à la fois dans le curseur, saisissez `1`.

   - Saisissez le nombre de **[!UICONTROL Events to Scroll per Click in Event Slider Sidebar Widget]**. Par défaut, cette valeur est définie sur `2`. Si vous souhaitez que le curseur affiche l’événement suivant en séquence en cliquant dessus, saisissez `1`.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

## Restrictions d’accès

L’accès à une vente, un événement ou un site privé peut être limité aux clients enregistrés qui se connectent ou étendu aux clients non enregistrés qui doivent s’inscrire avant d’accéder à .

![Configuration générale - restrictions du site web](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

### Limitation de l’accès

L’accès à une vente, un événement ou un site privé peut être limité aux clients enregistrés qui se connectent ou étendu aux clients non enregistrés qui doivent s’inscrire avant d’accéder à .

![Configuration générale - restrictions du site web](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL General]** et sélectionnez **[!UICONTROL General]** sous .

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Website Restrictions]** .

1. Définissez **[!UICONTROL Access Restriction]** sur `Yes`.

1. Définissez **[!UICONTROL Restriction Mode]** sur l’une des options suivantes :

   - `Website Closed`
   - `Private Sales: Login Only`
   - `Private Sales: Login and Register`

1. Définissez **[!UICONTROL Startup Page]** sur l’une des options suivantes :

   - `To login form (302 Found)` - Les utilisateurs sont redirigés vers le formulaire de connexion avant d’accéder au site.

   - `To landing page (302 Found)` - Les utilisateurs sont redirigés vers la page d’entrée spécifiée jusqu’à ce qu’ils se connectent.

     >[!IMPORTANT]
     >
     >Veillez à inclure un lien vers la page de connexion à partir de la page d’entrée afin que les clients puissent se connecter pour accéder au site.

1. Sélectionnez le **[!UICONTROL Landing Page]** qui s’affiche avant que les clients ne se connectent au site de vente privée.

1. Pour que les robots de moteur de recherche et les araignées sachent que la page d’entrée est correcte et qu’il n’y a aucune autre page sur le site à indexer, définissez **[!UICONTROL HTTP Response]** sur `200 OK`.

   Dans tous les autres cas, définissez sur `503 Service Unavailable`.

   >[!NOTE]
   >
   >Applicable uniquement si le mode de restriction est défini sur _Site Web fermé_. La page d’entrée est rendue en tant qu’HTML brut.

1. Si vous souhaitez que les champs de la connexion client et des formulaires de mot de passe soient automatiquement renseignés à partir des entrées précédentes, définissez **[!UICONTROL Enable Autocomplete on login/forgot password forms]** sur `Yes`.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

### Limiter les ventes

Par défaut, les produits qui apparaissent dans les événements à venir ou fermés ne sont pas disponibles pour vente générale et le bouton _[!UICONTROL Add to Cart]_&#x200B;n’apparaît pas dans la liste de produits ou la page de produits.

Pour restaurer le bouton _[!UICONTROL Add to Cart]_&#x200B;d&#39;un événement fermé, l&#39;événement doit être supprimé (voir [Mettre à jour les événements](event-create.md#update-events)). Cependant, si un produit est associé à une autre catégorie qui n’a aucune restriction de vente, le bouton est disponible sur la page du produit. De même, le bloc de coche n’apparaît pas sur la page de produits si le produit est associé à une autre catégorie qui n’a aucune restriction de vente.
