---
title: Configurer des listes de souhaits
description: Découvrez comment configurer la fonctionnalité de liste de souhaits pour vos clients de magasin.
exl-id: 479455f1-282f-4277-b132-45c5867fb21c
feature: Customers, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# Configurer des listes de souhaits

La configuration de la liste de souhaits active les listes de souhaits et détermine le modèle d’email et l’expéditeur des emails utilisés lors du partage d’une liste de souhaits.

## Activer la fonctionnalité de liste de souhaits

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Wish List]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL General Options]** et procédez comme suit :

   ![Configuration des clients - paramètres généraux de la liste de souhaits](../configuration-reference/customers/assets/wishlist-general-options.png){width="600" zoomable="yes"}

   - Basculer **[!UICONTROL Enabled]** to `Yes`, qui active le module de liste de souhaits pour le magasin.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Basculement **[!UICONTROL Enable Multiple Wish Lists]** to `Yes`, qui permet aux clients de créer et de gérer plusieurs listes de souhaits.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Pour limiter le nombre de listes de souhaits que les clients peuvent avoir associées à leur compte, saisissez la valeur de **[!UICONTROL Number of Multiple Wish Lists]**.

   - Basculer **[!UICONTROL Show in Sidebar]** to `Yes`, qui affiche les listes de souhaits dans la barre latérale.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Share Options]** et procédez comme suit :

   ![Configuration des clients - options de partage de liste de souhaits](../configuration-reference/customers/assets/wishlist-share-options.png){width="600" zoomable="yes"}

   - Définissez la variable **[!UICONTROL Email Sender]** au contact du magasin qui doit apparaître comme expéditeur du message. Options : contact général, représentant commercial, service clientèle, courrier électronique personnalisé.

   - Définissez la variable **[!UICONTROL Email Template]** à utiliser lorsqu’un client partage une liste de souhaits.

   - Pour limiter le nombre total d’emails qu’un client peut envoyer, saisissez une **[!UICONTROL Max Emails Allowed to be Sent]** . La valeur par défaut est 10 et la valeur maximale autorisée est de 10 000.

   - Pour limiter la taille du message, saisissez la valeur **[!UICONTROL Email Text Length Limit]**. La valeur par défaut est 255.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL My Wish List Link]** section et définition **[!UICONTROL Display Wish List Summary]** à l’une des options suivantes :

   - `Display number of items in wish list`
   - `Display item quantities`

   ![Configuration des clients - affichage de la liste de souhaits](../configuration-reference/customers/assets/wishlist-my-wishlist-link.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

## Ajouter une recherche de liste de souhaits

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

Vous trouverez n’importe quelle liste de souhaits publics à l’aide de la recherche par liste de souhaits . [widget](../content-design/widgets.md). Le widget permet à un client de rechercher par nom ou adresse électronique du propriétaire de la liste de souhaits. Les clients de la boutique peuvent trouver des listes de souhaits qui appartiennent à d’autres clients, les consulter et leur commander des produits, ou ajouter les produits à leurs propres listes de souhaits. Si un article est acheté à partir d’une liste de souhaits publique par un autre client, il n’est pas supprimé de la liste de souhaits d’origine. La variable _Recherche dans la liste de souhaits_ Vous pouvez ajouter un widget à n’importe quelle page de votre boutique afin de faciliter la recherche des listes de souhaits des amis et des membres de votre famille par les clients.

![Exemple de storefront - recherche de liste de souhaits](./assets/storefront-wishlist-search.png){width="700" zoomable="yes"}

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Widget]**.

1. Dans le _[!UICONTROL Settings]_, procédez comme suit :

   - Définir **[!UICONTROL Type]** to `Wish List Search`.

   - Définir **[!UICONTROL Design Theme]** au thème du magasin où est ajoutée la liste de souhaits.

   - Cliquez sur **[!UICONTROL Continue]**.

1. Procédez comme suit : _[!UICONTROL Storefront Properties]_:

   - Saisissez le **[!UICONTROL Widget Title]**.

   - Définir **[!UICONTROL Assign to Store Views]** à la vue ou au site web sur lequel le widget doit être utilisé.

   - Pour **[!UICONTROL Sort Order]**, saisissez un nombre pour déterminer le positionnement du widget dans son conteneur.

     `0` = first (par défaut), `1` = second, `2` = troisième, etc.

1. Dans le _[!UICONTROL Layout Updates]_, cliquez sur **[!UICONTROL Add Layout Update]**et défini **[!UICONTROL Display on]**à l’une des options suivantes :

   - _[!UICONTROL Categories]_

      - `Anchor Categories`
      - `Non-Anchor Categories`

   - _[!UICONTROL Products]_

      - `All Product Type`
      - `Simple Product`
      - `Virtual Product`
      - `Bundle Product`
      - `Configurable Product`
      - `Downloadable Product`
      - `Gift Card`
      - `Grouped Product`

   - _[!UICONTROL Generic Page]_

      - `All Pages`
      - `Specified Page`
      - `Page Layouts`

1. Dans le **[!UICONTROL Container]** , choisissez la zone de la mise en page où elle doit être placée.

   ![Widget de recherche de liste de souhaits - mise en page](./assets/widget-wishlist-search-storefront.png){width="700" zoomable="yes"}

1. Dans le panneau de gauche, choisissez **[!UICONTROL Widget Options]**.

1. Définir **[!UICONTROL Quick Search Form Types]** à l’une des options suivantes :

   - `All Forms` - Les clients peuvent effectuer une recherche en fonction de tous les paramètres disponibles.
   - `Owner Name` - Les clients peuvent rechercher des listes de souhaits par nom de propriétaire.
   - `Owner Email` - Les clients peuvent rechercher des listes de souhaits par adresse électronique du propriétaire.

   >[!NOTE]
   >
   >Les adresses de livraison ne sont pas incluses dans les listes de souhaits.

1. Configurez les propriétés du widget restantes selon les besoins, en suivant la procédure standard [instructions](../content-design/widget-create.md).

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

1. Lorsque vous y êtes invité, actualisez tous les caches non valides.
