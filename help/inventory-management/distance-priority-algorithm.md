---
title: Configuration de l’algorithme de priorité des distances
description: Définissez la configuration permettant de comparer l’emplacement de l’adresse de destination de livraison avec les emplacements sources afin de déterminer la source la plus proche pour effectuer les envois.
exl-id: 4dec179a-25ac-48db-a84b-4974798272b0
feature: Inventory, Configuration
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 0%

---

# Configuration de l’algorithme de priorité des distances

L’algorithme de priorité des distances compare l’emplacement de l’adresse de destination de livraison aux emplacements sources afin de déterminer la source la plus proche pour accomplir les chargements. La distance peut être déterminée par la distance physique ou le temps passé d&#39;un lieu à un autre, en utilisant les données de la base de données ou en suivant les instructions de conduite, de marche ou de vélo. Utilisez cette [Algorithme de sélection de source](selection-reservations.md) pour recommander la source la plus proche des adresses de destination d’expédition.

>[!NOTE]
>
>Si vous utilisez l’algorithme Distance Priority, saisissez l’adresse de la rue complète et les coordonnées GPS de votre [sources](sources-add.md) est recommandé.

Vous disposez de deux options pour calculer la distance et le temps afin de trouver la source la plus proche pour l’exécution de l’expédition :

- **CARTE GOOGLE** - Utilisations [Plateforme Google Maps][1] services permettant de calculer la distance et l’heure entre l’adresse de destination de livraison et les emplacements sources. Cette option utilise la latitude et la longitude de la source (coordonnées GPS) et peut utiliser l’adresse de la rue selon le mode de calcul. Une clé API Google est requise avec [API Geocoding][2] et [API de la matrice de distance][3] activée et vous pouvez encourir des frais via Google.

- **Calcul hors ligne** - Calcule la distance à l’aide des données de géocode téléchargées et importées à l’aide de codes postaux et de coordonnées GPS afin de déterminer la source la plus proche de l’adresse de destination de livraison. Pour configurer cette option, vous pouvez avoir besoin de l’aide du développeur pour télécharger et importer des géocodes à l’aide des instructions de ligne de commande.

>[!NOTE]
>
>Pour un site web multi-magasin avec plusieurs pays, configurez la variable [destination de taxe par défaut](../stores-purchase/tax-class.md#default-tax-destination){target="_blank"} pour chaque pays.

## Utilisation des mappages Google

Vous n’avez pas besoin d’un compte Google pour commencer. Le processus inclut la création de compte et de projet Google, si nécessaire. Cette option nécessite l’ajout d’un compte de facturation et d’un mode de paiement à votre compte Google pour terminer les configurations et utiliser l’algorithme.
Cependant, l’algorithme basé sur les distances de Google MAP est recommandé comme plus avancé et plus précis par rapport au calcul hors ligne.

### Étape 1 : création de la clé API Google

La clé provient de la fonction [Plateforme Google Maps][1] et doivent avoir [API Geocoding][2] et [API de la matrice de distance][3] activée. Pour plus d’informations, voir [Configuration de l’algorithme de priorité des distances](distance-priority-algorithm.md).

1. Visite [Plateforme Google Maps][1] et cliquez sur **[!UICONTROL Get Started]**.

1. Pour activer la plateforme, sélectionnez **[!UICONTROL Maps, Routes, and Places]** et cliquez sur **[!UICONTROL Continue]**.

   ![Plateforme Google Maps pour votre clé](assets/inventory-google-key1.png){width="350" zoomable="yes"}

1. Connectez-vous avec un compte Google ou créez-en un.

1. Configurez un projet :

   - Sélectionnez un projet ou saisissez un nouveau nom de projet.

   - Pour accepter les termes, sélectionnez `Yes`.

   - Cliquez sur **[!UICONTROL Next]**.

1. Saisissez un compte de facturation ou créez-en un. Vous pouvez ignorer et ajouter un compte de facturation ultérieurement.

   Un compte de facturation est nécessaire pour utiliser ce service.

1. Pour ouvrir et configurer vos options Google Cloud Platform, cliquez sur **[!UICONTROL Console]**.

   - Ouvrez votre projet.

   - Développez le menu, puis cliquez sur **[!UICONTROL APIs & Services]** > **[!UICONTROL Library]**.

     ![Services d’API Google](assets/inventory-google-key2.png){width="350" zoomable="yes"}

   - Recherchez [API Geocoding][2] et [API de la matrice de distance][3]. Sélectionnez et activez chaque service.

1. Développez le menu, cliquez sur **[!UICONTROL APIs & Services]** > **[!UICONTROL Credentials]** et copiez la clé API Google.

   ![Copie de clé API Google](assets/inventory-google-key3.png){width="350" zoomable="yes"}

### Étape 2 : configuration du fournisseur Google MAP

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Inventory]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur _[!UICONTROL Distance Provider for Distance Based SSA]_section et définition **[!UICONTROL Provider]**to `Google MAP`.

   ![Fournisseurs d’une SSA basée sur les distances](assets/config-catalog-inventory-distance-provider.png){width="350" zoomable="yes"}

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur _[!UICONTROL Google Distance Provider]_et configurez les paramètres :

   - Pour **[!UICONTROL Google API Key]**, saisissez la clé copiée à partir de votre compte Google.

   - Pour **[!UICONTROL Computation mode]**, sélectionnez une configuration.

     >[!NOTE]
     >
     >Lors de l’utilisation de cet algorithme pour l’expédition, si les itinéraires et les données ne reviennent pas pour le mode de calcul sélectionné (conduite, vélo ou marche) pour une expédition, l’ASS utilise par défaut la priorité source. La définition de la variable [priorité des sources par stock](stocks-prioritize-sources.md) est recommandé.

     | Option | Description |
     | ----- | ----- |
     | `Driving` | (Par défaut) Demande les instructions de conduite standard à l’aide du réseau routier. |
     | `Walking` | Demande des instructions de marche en utilisant des chemins piétonniers et des trottoirs (le cas échéant). |
     | `Bicycling` | Demande des instructions cyclables en utilisant des pistes cyclables et des rues préférées (le cas échéant). La variable [Service de matrice de distance][4] est disponible uniquement aux États-Unis et dans certaines villes canadiennes. |

   - Pour **[!UICONTROL Value]**, sélectionnez un type de valeur :

     | Option | Description |
     | ----- | ----- |
     | `Distance` | (Par défaut) Renvoie la distance entre les points en mesures (kilomètres et mètres) ou impériale (kilomètres et pieds). |
     | `Time to Destination` | Renvoie le temps nécessaire pour voyager des emplacements sources vers l’adresse d’expédition en heures et minutes. |

   ![Fournisseur de distance Google](assets/config-catalog-inventory-distance-provider-settings.png){width="350" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

## Utilisation du calcul hors ligne

Les calculs hors ligne utilisent des codes pays pour déterminer la distance entre la destination de livraison et les adresses source. Cette option peut nécessiter l’aide du développeur pour la configuration. Utilisez une [!DNL Inventory Management] Commande d’interface de ligne de commande pour télécharger et importer des données à partir de [geonames.org][5].

>[!NOTE]
>
>Les géocodes importés depuis [geonames.org][5] ont des limites pour certains pays, comme le Canada et l&#39;Irlande. Voir [Fichiers de code postal GeoNames][6] pour plus d’informations.

### Étape 1 : téléchargement et import de géocodes

Effectuez la configuration de ligne de commande complète pour télécharger et importer des pays de codes géographiques vers et où trouver des emplacements sources dans . Cette étape peut nécessiter l’aide des développeurs pour les tâches de ligne de commande. Voir [Importer des géocodes](cli.md#import-geocodes).

Exécutez ces commandes chaque fois que vous souhaitez ajouter d’autres codes géographiques.

### Etape 2 : paramétrer le calcul

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Inventory]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur _[!UICONTROL Distance Provider for Distance Based SSA]_.

1. Désélectionnez l’option **[!UICONTROL Use system value]** case à cocher et définition **[!UICONTROL Provider]** to `Offline Calculation`.

   ![Fournisseurs de distance pour l’ASS basée sur les distances](assets/inventory-distance-offline.png){width="350" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

[1]: https://cloud.google.com/maps-platform/
[2]: https://developers.google.com/maps/documentation/geocoding/start
[3]: https://developers.google.com/maps/documentation/distance-matrix/start
[4]: https://developers.google.com/maps/documentation/javascript/distancematrix#travel_modes
[5]: https://www.geonames.org/
[6]: https://download.geonames.org/export/zip/readme.txt
