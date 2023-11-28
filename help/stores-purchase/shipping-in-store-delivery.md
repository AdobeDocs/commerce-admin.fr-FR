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

1. Le client clique **[!UICONTROL Pick In Store]** ou sélectionne la variable _[!UICONTROL In-Store Pickup Delivery]_mode de livraison.
1. La variable _[!UICONTROL Pick In Store]_l’onglet passage en caisse s’affiche.

Lorsque le client dispose d’une adresse ou a rempli précédemment le formulaire d’adresse de livraison avant de passer à la variable _[!UICONTROL Pick In Store]_tab :

- La source la plus proche de l’adresse du client dans le rayon configuré est automatiquement présélectionnée en tant que magasin de ramassage.
- Lorsque le client clique **[!UICONTROL Select Other]**, la variable _[!UICONTROL Select Store]_le formulaire de recherche s’ouvre. Seuls les magasins situés à la distance configurée (rayon) du magasin présélectionné s’affichent dans la liste. Tous les magasins de la liste sont triés par distance par rapport au magasin présélectionné.
- Lorsque le client saisit un code postal ou un nom de ville dans le champ de recherche, seuls les magasins situés à la distance (rayon) configurée par rapport à l’emplacement recherché s’affichent dans la liste. Tous les magasins de la liste sont triés par distance par rapport à l’emplacement recherché.
- Lorsque le client efface le code postal ou le nom de la ville du champ de recherche, tous les magasins de relance affectés aux produits du panier sont affichés au client. Tous les magasins de la liste sont triés dans l’ordre croissant des codes source sans aucune limite de distance (rayon).

Si le client n’a pas d’adresse ou n’a pas rempli précédemment le formulaire d’adresse d’expédition avant de passer à la variable _[!UICONTROL Pick In Store]_tab :

- La page affiche la variable _Nous n’avons pas pu présélectionner l’emplacement de sélection en fonction des informations disponibles._ message.
- Lorsque le client clique **[!UICONTROL Select Store]**, la variable _[!UICONTROL Select Store]_le formulaire de recherche s’ouvre.
- Tous les magasins de ramassage affectés aux produits dans le panier s’affichent dans l’ordre croissant des codes sources sans limite de distance (rayon).
- Lorsque le client saisit un code postal ou un nom de ville dans le champ de recherche, seuls les magasins situés à la distance (rayon) configurée par rapport à l’emplacement recherché s’affichent dans la liste. Tous les magasins de la liste sont triés par distance par rapport à l’emplacement recherché.

## Avant configuration

- Assurez-vous que vous disposez d’un stock et d’une source non par défaut. Pour plus d’informations sur la configuration d’une source en tant qu’emplacement de récupération, voir [Ajouter une source](../inventory-management/sources-add.md).
- Assurez-vous d’avoir configuré un algorithme de priorité des distances. Pour plus d’informations, voir [Configuration de l’algorithme de priorité des distances](../inventory-management/distance-priority-algorithm.md).
- Assurez-vous que [téléchargé et importé](../inventory-management/cli.md#import-geocodes) tous les géocodes nécessaires pour le calcul hors ligne.
- Vérifiez que vous avez configuré [Calcul de la destination de la taxe par défaut](../configuration-reference/sales/tax.md#default-tax-destination-calculation) paramètres.

>[!IMPORTANT]
>
>**Dans le storefront, les résultats de la recherche sont filtrés par distance (rayon) pour afficher les résultats pertinents :**<br><br>
>Si le client a une adresse de livraison, l’emplacement de base pour calculer la distance (rayon) est prélevé sur l’adresse de livraison.<br><br>
>Si le client ne dispose pas d’adresse de livraison, l’emplacement de base pour calculer la distance est extrait de la variable [Calcul de la destination de la taxe par défaut](../configuration-reference/sales/tax.md#default-tax-destination-calculation) paramètres. Ces paramètres sont définis par vue de magasin et vous devez configurer les paramètres Calcul de destination fiscale par défaut pour vous assurer que la recherche de magasin de prise en charge fonctionne correctement.

## Configuration d’une diffusion en magasin

Tout d’abord, vérifiez que la diffusion en magasin est activée.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Delivery Methods]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL In-Store Delivery]** .

   ![Diffusion en magasin](../configuration-reference/sales/assets/delivery-methods-in-store-delivery.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Enabled]** to `Yes`.

   >[!NOTE]
   >
   >Si nécessaire, effacez la variable **[!UICONTROL Use system value]** pour modifier la valeur par défaut d’un champ.

1. Saisissez le **[!UICONTROL Method Name]** qui décrit la méthode de calcul utilisée pour produire une estimation de livraison.

   Le nom de la méthode s’affiche en regard du taux estimé calculé dans le panier.

1. Saisissez le **[!UICONTROL Title]** que vous souhaitez afficher pour _Diffusion en magasin_ durant le passage en caisse.

   Le titre par défaut est : `In-Store Pickup Delivery`.

1. Pour facturer aux clients le service de prise en charge en magasin, saisissez les frais dans la variable **[!UICONTROL Price]** champ .

1. Saisissez le **[!UICONTROL Search Radius]** en kilomètres pour la recherche de l’emplacement de récupération du magasin lors du passage en caisse du storefront.

1. Pour **[!UICONTROL Displayed Error Message]**, saisissez le message qui s’affiche si la diffusion en magasin n’est plus disponible.

   Le message par défaut est : `In-Store Delivery is not available. To use this delivery method, please contact us.`

1. Cliquez sur **[!UICONTROL Save Config]**.
