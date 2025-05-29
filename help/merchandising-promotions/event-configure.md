---
title: Configuration d’événements
description: Découvrez comment effectuer la configuration de base pour activer les événements et configurer le bloc d’événement dans la barre latérale du storefront.
exl-id: 620b2d60-ce6f-4f31-93bb-18d3dd9cdce6
feature: Marketing Tools, Promotions/Events
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Configuration d’événements

{{ee-feature}}

Avant de pouvoir créer un événement, vous devez effectuer la configuration de base pour activer les événements et configurer le bloc d’événement dans la barre latérale.

## Activation et configuration d’événements

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en dessous.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Catalog Events]** et procédez comme suit :

   ![Configuration du catalogue - Événements de catalogue](../configuration-reference/catalog/assets/catalog-events.png){width="600" zoomable="yes"}

   - Définissez **[!UICONTROL Enable Catalog Events Functionality]** sur `Yes`.

   - Définissez **[!UICONTROL Enable Catalog Event Widget on Storefront]** sur `Yes`.

   - Saisissez le **[!UICONTROL Number of Events to be Displayed in the Event Slider Sidebar Widget]**. Par défaut, cette valeur est définie sur `5`. Si vous ne souhaitez afficher qu’un seul événement à la fois dans le curseur, saisissez `1`.

   - Saisissez le nombre de **[!UICONTROL Events to Scroll per Click in Event Slider Sidebar Widget]**. Par défaut, cette valeur est définie sur `2`. Si vous souhaitez que le curseur affiche l’événement suivant dans l’ordre lorsque l’utilisateur clique dessus, saisissez `1`.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Restrictions d’accès

L’accès à une vente privée, à un événement ou à un site peut être limité aux clients enregistrés qui se connectent ou étendu aux clients non enregistrés qui doivent s’enregistrer avant d’y accéder.

![Configuration générale - restrictions relatives au site web](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

### Restreindre l’accès

L’accès à une vente privée, à un événement ou à un site peut être limité aux clients enregistrés qui se connectent ou étendu aux clients non enregistrés qui doivent s’enregistrer avant d’y accéder.

![Configuration générale - restrictions relatives au site web](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL General]** et choisissez **[!UICONTROL General]** en dessous.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Website Restrictions]** .

1. Définissez **[!UICONTROL Access Restriction]** sur `Yes`.

1. Définissez **[!UICONTROL Restriction Mode]** sur l’une des options suivantes :

   - `Website Closed`
   - `Private Sales: Login Only`
   - `Private Sales: Login and Register`

1. Définissez **[!UICONTROL Startup Page]** sur l’une des options suivantes :

   - `To login form (302 Found)` - Les utilisateurs sont redirigés vers le formulaire de connexion avant d’accéder au site.

   - `To landing page (302 Found)` - Les utilisateurs sont redirigés vers la page de destination spécifiée jusqu’à leur connexion.

     >[!IMPORTANT]
     >
     >Veillez à inclure un lien vers la page de connexion à partir de la page de destination afin que les clients puissent se connecter pour accéder au site.

1. Choisissez le **[!UICONTROL Landing Page]** qui s’affiche avant que les clients ne se connectent au site de vente privé.

1. Pour informer les robots des moteurs de recherche et les araignées que la page de destination est correcte et qu’il n’y a pas d’autres pages du site à indexer, définissez **[!UICONTROL HTTP Response]** sur `200 OK`.

   Dans tous les autres cas, définissez sur `503 Service Unavailable`.

   >[!NOTE]
   >
   >Applicable uniquement si le mode de restriction est défini sur _Site Web fermé_. La page de destination est rendue en tant qu’HTML brut.

1. Si vous souhaitez que les champs des formulaires de connexion du client et de mot de passe oublié soient renseignés automatiquement à partir des entrées précédentes, définissez **[!UICONTROL Enable Autocomplete on login/forgot password forms]** sur `Yes`.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

### Limiter les ventes

Par défaut, les produits qui apparaissent dans les événements à venir ou fermés ne sont pas disponibles à la vente générale et le bouton _[!UICONTROL Add to Cart]_&#x200B;n’apparaît pas dans la liste de produits ou la page des produits.

Pour restaurer le bouton _[!UICONTROL Add to Cart]_&#x200B;d&#39;un événement fermé, l&#39;événement doit être supprimé (voir [Mettre à jour les événements](event-create.md#update-events)). Cependant, si un produit est associé à une autre catégorie qui n’a pas de restrictions de vente, le bouton est disponible sur la page des produits. De même, le bloc de signet n’apparaît pas sur la page produit si le produit est associé à une autre catégorie qui n’a pas de restrictions de vente.
