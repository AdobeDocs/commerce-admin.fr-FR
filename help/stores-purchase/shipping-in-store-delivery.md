---
title: Diffusion en magasin
description: Découvrez comment configurer une option de diffusion en magasin pour votre magasin.
exl-id: bd64b110-5c39-41c6-8a0c-38561b2a5bf4
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Diffusion en magasin

Avec la méthode de remise en magasin, le client peut sélectionner une source à utiliser comme emplacement de récupération lors du passage en caisse.

![Méthode de remise en magasin lors du passage en caisse](./assets/luma-in-store-example.png){width="700" zoomable="yes"}

Pendant le passage en caisse sur le storefront :

1. Le client clique sur **[!UICONTROL Pick In Store]** ou sélectionne la méthode d’expédition _[!UICONTROL In-Store Pickup Delivery]_.
1. L’onglet de passage en caisse _[!UICONTROL Pick In Store]_s’ouvre.

Lorsque le client dispose d’une adresse, ou a déjà rempli le formulaire d’adresse de livraison avant de passer à l’onglet _[!UICONTROL Pick In Store]_:

- La source la plus proche de l’adresse du client dans le rayon configuré est automatiquement présélectionnée en tant que magasin de ramassage.
- Lorsque le client clique sur **[!UICONTROL Select Other]**, le formulaire de recherche _[!UICONTROL Select Store]_s’ouvre. Seuls les magasins situés à la distance configurée (rayon) du magasin présélectionné s’affichent dans la liste. Tous les magasins de la liste sont triés par distance par rapport au magasin présélectionné.
- Lorsque le client saisit un code postal ou un nom de ville dans le champ de recherche, seuls les magasins situés à la distance (rayon) configurée par rapport à l’emplacement recherché s’affichent dans la liste. Tous les magasins de la liste sont triés par distance par rapport à l’emplacement recherché.
- Lorsque le client efface le code postal ou le nom de la ville du champ de recherche, tous les magasins de relance affectés aux produits du panier sont affichés au client. Tous les magasins de la liste sont triés dans l’ordre croissant des codes source sans aucune limite de distance (rayon).

Si le client n’a pas d’adresse ou n’a pas rempli précédemment le formulaire d’adresse de livraison avant de passer à l’onglet _[!UICONTROL Pick In Store]_:

- La page affiche le message _Nous n’avons pas pu sélectionner l’emplacement de sélection en fonction des informations disponibles_.
- Lorsque le client clique sur **[!UICONTROL Select Store]**, le formulaire de recherche _[!UICONTROL Select Store]_s’ouvre.
- Tous les magasins de ramassage affectés aux produits dans le panier s’affichent dans l’ordre croissant des codes sources sans limite de distance (rayon).
- Lorsque le client saisit un code postal ou un nom de ville dans le champ de recherche, seuls les magasins situés à la distance (rayon) configurée par rapport à l’emplacement recherché s’affichent dans la liste. Tous les magasins de la liste sont triés par distance par rapport à l’emplacement recherché.

## Avant configuration

- Assurez-vous que vous disposez d’un stock et d’une source non par défaut. Pour plus d’informations sur la configuration d’une source comme emplacement de récupération, voir [Ajout d’une source](../inventory-management/sources-add.md).
- Assurez-vous d’avoir configuré un algorithme de priorité des distances. Pour plus d’informations, voir [Configuration de l’algorithme de priorité des distances](../inventory-management/distance-priority-algorithm.md).
- Assurez-vous d’avoir [téléchargé et importé](../inventory-management/cli.md#import-geocodes) tous les codes géographiques nécessaires pour le calcul hors ligne.
- Assurez-vous d’avoir configuré les paramètres [Calcul de destination fiscale par défaut](../configuration-reference/sales/tax.md#default-tax-destination-calculation) .

>[!IMPORTANT]
>
>**Dans le storefront, les résultats de la recherche sont filtrés par distance (rayon) pour afficher les résultats pertinents :**<br><br>
>Si le client a une adresse de livraison, l&#39;emplacement de base pour calculer la distance (rayon) est prélevé sur l&#39;adresse de livraison.<br><br>
>Si le client ne dispose pas d’adresse de livraison, l’emplacement de base pour calculer la distance est extrait des paramètres [Calcul de la destination fiscale par défaut](../configuration-reference/sales/tax.md#default-tax-destination-calculation). Ces paramètres sont définis par vue de magasin et vous devez configurer les paramètres Calcul de destination fiscale par défaut pour vous assurer que la recherche de magasin de prise en charge fonctionne correctement.

## Configuration d’une diffusion en magasin

Tout d’abord, vérifiez que la diffusion en magasin est activée.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Delivery Methods]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL In-Store Delivery]** .

   ![Diffusion en magasin](../configuration-reference/sales/assets/delivery-methods-in-store-delivery.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Enabled]** sur `Yes`.

   >[!NOTE]
   >
   >Si nécessaire, décochez la case **[!UICONTROL Use system value]** pour modifier la valeur par défaut d’un champ.

1. Saisissez le **[!UICONTROL Method Name]** qui décrit la méthode de calcul utilisée pour produire une estimation de livraison.

   Le nom de la méthode s’affiche en regard du taux estimé calculé dans le panier.

1. Saisissez le **[!UICONTROL Title]** que vous souhaitez afficher pour la section _Diffusion en magasin_ lors du passage en caisse.

   Le titre par défaut est `In-Store Pickup Delivery`.

1. Pour facturer aux clients le service de prise en charge en magasin, saisissez les frais dans le champ **[!UICONTROL Price]**.

1. Saisissez le **[!UICONTROL Search Radius]** en kilomètres pour la recherche de l’emplacement de récupération du magasin lors du passage en caisse du magasin.

1. Pour **[!UICONTROL Displayed Error Message]**, saisissez le message qui s’affiche si la diffusion en magasin n’est plus disponible.

   Le message par défaut est `In-Store Delivery is not available. To use this delivery method, please contact us.`

1. Cliquez sur **[!UICONTROL Save Config]**.
