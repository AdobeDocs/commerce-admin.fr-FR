---
title: Media - Map
description: Découvrez le type de contenu Mappage, utilisé pour ajouter un mappage de [!DNL Google Maps] Platform à l’étape [!DNL Page Builder] .
exl-id: 91fea8f8-d48a-43f1-ba2a-212c7130cee9
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1571'
ht-degree: 0%

---

# Media - Map

Utilisez le type de contenu _Map_ pour ajouter une carte de [[!DNL Google Maps] Platform][1] à l’ [[!DNL Page Builder] étape](workspace.md#stage). Par exemple, vous pouvez ajouter une carte à un bloc, puis le bloc aux pages [À propos de nous](../content-design/pages.md#about-us) et [Nous contacter](../getting-started/store-details.md#contact-us-form).

Pour tirer le meilleur parti de [!DNL Google Maps] Platform, vous pouvez personnaliser la carte, mettre en surbrillance les emplacements de vos magasins et utiliser Google [Places][2] pour ajouter des informations riches sur votre magasin à tous les [!DNL Google Maps].

## Avantages de l’incorporation d’une carte Google

1. Fournit aux acheteurs une gamme complète d’informations sur votre entreprise (numéro de téléphone, site web, critiques, évaluations, etc.) directement sur votre site.

1. Une carte Google permet généralement de voir les attractions, les parcs, les restaurants, etc. Ces informations aident vos clients à déterminer votre emplacement physique et à planifier leur voyage.

1. Permet aux clients de trouver facilement l’adresse de votre boutique physique sans avoir à ouvrir une nouvelle fenêtre de navigateur et quitter votre site.

1. Si vous disposez d’une chaîne de magasins physiques, l’ajout d’une carte Google sur votre site contribue à accroître la notoriété et la crédibilité de votre marque sous la forme d’éléments mis en évidence.

![Exemple de storefront - map avec location](./assets/pb-media-maps-storefront.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Boîte à outils de mappage

La boîte à outils de carte s’affiche lorsque vous placez le pointeur de la souris sur le conteneur de cartes.

| Outil | Icône | Description |
|--- |--- |--- |
| Déplacer | ![Icône Déplacer](./assets/pb-icon-move.png){width="25"} | Déplace la carte vers une autre position sur la scène. |
| (label) | [!UICONTROL Map] | Identifie le conteneur de contenu actuel en tant que mappage. Passez la souris sur le conteneur de mappage pour afficher la boîte à outils. |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} | Ouvre la page Modifier la carte dans laquelle vous pouvez modifier les propriétés de la carte et du conteneur. |
| Masquer | ![Icône Masquer](./assets/pb-icon-hide.png){width="25"} | Masque la carte active. |
| Afficher | ![Icône Afficher](./assets/pb-icon-show.png){width="25"} | Affiche la carte masquée. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="25"} | Effectue une copie de la carte. |
| Supprimer | ![Supprimer l’icône](./assets/pb-icon-remove.png){width="25"} | Supprime la carte de la scène. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Configurer [!DNL Google Maps] pour votre administrateur

Avant d’ajouter une carte, vous devez d’abord ouvrir un [compte][3] pour une version d’évaluation gratuite de [!DNL Google Maps] Platform. L’essai gratuit dure 12 mois et comprend un crédit de 300 $. Si vous utilisez votre crédit, Google ne facture pas votre compte sans votre permission.

### Étape 1 : Obtention de la clé d’API [!DNL Google Maps]

Selon que vous disposez déjà d’une clé [!DNL Google Maps], utilisez l’une des procédures suivantes pour obtenir la clé d’API requise pour la configuration. Pour configurer une clé [!DNL Google Maps], vous devez être un administrateur de site autorisé à activer la facturation pour votre compte. Si vous n’êtes pas prêt à configurer un compte de plateforme [!DNL Google Maps], vous pouvez ignorer cette étape et utiliser la carte d’espace réservé pour l’instant.

1. Accédez à la [console Google Cloud Platform](https://cloud.google.com/console/google/maps-apis/overview).

1. Cliquez sur la liste déroulante du projet et sélectionnez ou créez le projet pour lequel vous souhaitez ajouter une clé API.

1. Pour configurer vos informations d’identification d’API, suivez les [instructions][4] de la documentation [!DNL Google Maps].

1. Copiez votre clé API dans le Presse-papiers.

### Étape 2 : configurer [!DNL Google Maps] dans [!DNL Commerce]

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche sous _[!UICONTROL General]_, choisissez **[!UICONTROL Content Management]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

   ![Outils de contenu avancé](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

   Pour plus d’informations sur les options de configuration des outils avancés de gestion de contenu, consultez le [Guide de référence de configuration](../configuration-reference/general/content-management.md).

1. Pour **[!UICONTROL Google Maps API Key]**, collez la clé que vous avez copiée à l’étape 1.

1. Cliquez sur **[!UICONTROL Test Key]**.

   En cas de problème avec votre clé, revenez au site de la plateforme [!DNL Google Maps] pour résoudre le problème. Ensuite, réessayez.

1. Une fois votre clé vérifiée, cliquez sur **[!UICONTROL Save Config]**.

## Ajout d’une carte à l’étape

1. Ouvrez la page, le bloc ou le bloc dynamique dans l&#39;espace de travail [!DNL Page Builder].

1. Dans le panneau [!DNL Page Builder], développez **[!UICONTROL Media]** et faites glisser un espace réservé **[!UICONTROL Map]** sur la scène.

   ![Faire glisser une carte vers l’étape](./assets/pb-media-map-drag.png){width="600" zoomable="yes"}

   Si [!DNL Google Maps] Platform est configuré pour votre magasin, une carte s’affiche pour l’emplacement de votre magasin.

   ![[!DNL Google Maps]](./assets/pb-tutorial2-google-map.png){width="600" zoomable="yes"}

   Si [!DNL Google Maps] Platform n’est pas encore configuré pour votre magasin, un mappage d’espace réservé s’affiche à la place.

   ![[!DNL Google Maps] Espace réservé](./assets/pb-tutorial2-media-map-not-configured.png){width="600" zoomable="yes"}

## Ajout d’un emplacement de carte personnalisé

1. Pointez sur le conteneur de mappage pour afficher la boîte à outils et sélectionnez l’icône _Paramètres_ ( ![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

1. Dans le coin supérieur droit de la page _[!UICONTROL Edit Map]_, cliquez sur **[!UICONTROL Add Location]**.

1. Saisissez le **[!UICONTROL Location Name]** que vous souhaitez associer à l’épingle sur la carte.

1. Collectez les coordonnées de l’emplacement que vous souhaitez utiliser pour l’emplacement personnalisé.

   Vous pouvez également faire glisser la épingle dans la zone **[!UICONTROL Position]** de la carte affichée.

   Si nécessaire, accédez à [[!DNL Google Maps]][5] dans une nouvelle fenêtre de navigateur et utilisez l’une des méthodes suivantes pour obtenir les coordonnées :

   ![Coordonnées de carte](./assets/pb-media-maps-settings-add-location-coordinates.png){width="600" zoomable="yes"}

   **Méthode 1 :** Copier de l’URL

   - Dans le coin supérieur gauche, saisissez l’adresse dans la zone **[!UICONTROL Search]** et cliquez sur l’icône _Rechercher_ ( ![Icône de recherche](../assets/icon-magnify-search.png){width="20"} ).

   - Copiez les coordonnées dans l’URL et collez-les dans un bloc-notes.

   **Méthode 2 :** Copie de &quot;Qu’est-ce qu’il y a ici ?&quot;

   - Cliquez avec le bouton droit de la souris sur l’épingle rouge qui marque l’emplacement sur la carte et sélectionnez **[!UICONTROL What's here?]** dans le menu.

   - Dans le libellé affiché, copiez le texte, y compris les coordonnées, et collez le texte dans un bloc-notes.

1. Saisissez les nombres, sans la virgule, dans chacune des zones **[!UICONTROL Coordinates]**.

   Vous pouvez également saisir toutes les informations restantes qui doivent être disponibles sur la carte.

1. Renseignez toutes les autres informations que vous souhaitez associer à l’emplacement de la carte :

   | Option | Description |
   | ------ | ----------- |
   | [!UICONTROL Phone Number] | Numéro de téléphone de l’emplacement. |
   | [!UICONTROL Street Address] | Adresse de la rue de l&#39;emplacement. |
   | [!UICONTROL City] | La ville de l’emplacement. |
   | [!UICONTROL Region/State] | Région ou état de l’emplacement. |
   | [!UICONTROL Zip/Postal Code] | Code postal de l’emplacement. |
   | [!UICONTROL Country] | Pays de l’emplacement. |
   | [!UICONTROL Comment] | Tous les commentaires que vous souhaitez inclure. |

   {style="table-layout:auto"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

   Le nouvel emplacement apparaît dans la carte et dans la grille d’emplacement de la carte sur la page _[!UICONTROL Edit Map]_.

   ![[!DNL Page Builder] - map location grid](./assets/pb-media-maps-settings-add-location-grid.png){width="600" zoomable="yes"}

## Donner un style à la carte {#styling}

Utilisez l’ [!DNL Google Maps] assistant de style de plateforme pour appliquer l’un des six thèmes prédéfinis ou créer un thème personnalisé. Vous pouvez générer un fichier JSON avec les propriétés de style map ou un lien vers la carte stylisée.

### Modification du style de carte

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche sous _[!UICONTROL General]_, choisissez **[!UICONTROL Content Management]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. Sous la zone de texte **[!UICONTROL Google Maps Style]**, cliquez sur [Créer un style de carte][6].

   Cette action ouvre l’[[!DNL Google Maps]  Assistant de style de plateforme][6] dans un onglet distinct, où vous pouvez définir un style pour votre projet de plateforme [!DNL Google Maps].

1. Cliquez sur **[!UICONTROL Create a Style]** et suivez les instructions fournies.

   Une fois l’opération terminée, cliquez sur **[!UICONTROL Finish]**.

1. Exportez le style terminé sous forme de code JSON ou d’URL afin de pouvoir l’ajouter à la configuration [!DNL Commerce].

   - **JSON** : sous la zone avec le code JSON généré, cliquez sur **[!UICONTROL Copy JSON]**.

   - **[!UICONTROL URL]** : sous la zone avec l’URL générée, cliquez sur **[!UICONTROL Copy URL]**.

1. Revenez à l’onglet de votre navigateur d’administration et collez le code ou l’URL généré dans la zone **Style de mappage Google**.

   Si vous utilisez une URL, remplacez l’espace réservé `YOUR_API_KEY` par votre clé d’API [!DNL Google Maps]. Cette URL est liée à votre carte Google stylisée.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save Config]**.

### Modification des paramètres de carte

1. Pointez sur le conteneur de mappage pour afficher la boîte à outils et sélectionnez l’icône _Paramètres_ ( ![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

1. Modifiez les paramètres de base selon les besoins :

   | Option | Description |
   | ------ | ----------- |
   | [!UICONTROL Height] | Indique la hauteur de la carte affichée en pixels. |
   | [!UICONTROL Show Controls] | Détermine si les commandes Google Map standard s’affichent. |

   {style="table-layout:auto"}

1. Modifiez les paramètres _[!UICONTROL Advanced]_selon les besoins :

   - Pour contrôler le positionnement horizontal du contenu de la carte ajouté au conteneur, choisissez un **[!UICONTROL Alignment]** :

     | Option | Description |
     | ------ | ----------- |
     | `Default` | Applique le paramètre d’alignement par défaut spécifié dans la feuille de style du thème actif. |
     | `Left` | Aligne le contenu le long de la bordure gauche du conteneur de mappage, en tenant compte de toute marge intérieure spécifiée. |
     | `Center` | Aligne le contenu au centre du conteneur de mappage, en tenant compte de toute marge intérieure spécifiée. |
     | `Right` | Aligne le contenu le long de la bordure droite du conteneur de mappage, en tenant compte de toute marge intérieure spécifiée. |

     {style="table-layout:auto"}

   - Définissez le style **[!UICONTROL Border]** appliqué aux quatre côtés du conteneur de mappage :

     | Option | Description |
     | ------ | ----------- |
     | `Default` | Applique le style de bordure par défaut spécifié par la feuille de style associée. |
     | `None` | Ne fournit aucune indication visible des bordures du conteneur. |
     | `Dotted` | La bordure du conteneur s’affiche sous la forme d’une ligne pointillée. |
     | `Dashed` | La bordure du conteneur s’affiche sous la forme d’une ligne en pointillés. |
     | `Solid` | La bordure du conteneur s’affiche sous la forme d’une ligne pleine. |
     | `Double` | La bordure du conteneur s’affiche sous la forme d’une ligne double. |
     | `Groove` | La bordure du conteneur s’affiche sous forme de ligne droite. |
     | `Ridge` | La bordure du conteneur s’affiche sous la forme d’une ligne à droite. |
     | `Inset` | La bordure du conteneur s’affiche sous la forme d’une ligne d’insertion. |
     | `Outset` | La bordure du conteneur apparaît comme une ligne de départ. |

     {style="table-layout:auto"}

   - Si vous définissez un style de bordure autre que `None`, renseignez les options d’affichage de la bordure :

     ![Couleur de bordure](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

     | Option | Description |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Définissez la couleur en choisissant un échantillon, en cliquant sur le sélecteur de couleurs ou en saisissant un nom de couleur valide ou une valeur hexadécimale équivalente. |
     | [!UICONTROL Border Width] | Saisissez le nombre de pixels pour la largeur de la ligne de bordure. |
     | [!UICONTROL Border Radius] | Saisissez le nombre de pixels pour définir la taille du rayon utilisé pour arrondir chaque coin de la bordure. |

     {style="table-layout:auto"}

   - (Facultatif) Indiquez les noms de **[!UICONTROL CSS classes]** de la feuille de style actuelle à appliquer au conteneur de mappage.

     Séparez plusieurs noms de classe par un espace.

   - Entrez des valeurs, en pixels, pour que **[!UICONTROL Margins and Padding]** indique les marges extérieures et la marge intérieure du conteneur de cartes.

     Saisissez chaque valeur correspondante dans le diagramme de conteneur de mappages.

     | Zone de conteneur | Description |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | Espace vide appliqué au bord extérieur de tous les côtés du conteneur. |
     | [!UICONTROL Padding] | Espace blanc appliqué au bord intérieur de tous les côtés du conteneur. |

     {style="table-layout:auto"}

     >[!NOTE]
     >
     >La marge intérieure n’est pas disponible pour le type de contenu Carte .

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

### Modifier la taille de la grille

La taille de la grille détermine la taille de la carte associée à une [colonne](column.md) sur la scène [!DNL Page Builder]. Par défaut, la carte est large de 12 colonnes, avec un maximum de 16 colonnes.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche sous _[!UICONTROL General]_, choisissez **[!UICONTROL Content Management]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. Mettez à jour les options de grille selon les besoins :

   >[!NOTE]
   >
   >Si nécessaire, décochez la case **[!UICONTROL Use system value]** pour modifier ces paramètres.

   - Pour **[!UICONTROL Default Column Grid Size]**, saisissez une nouvelle valeur pour la taille par défaut de la grille.

   - Pour **[!UICONTROL Maximum Column Grid Size]**, saisissez une nouvelle valeur pour la taille de grille maximale par défaut.

   ![Paramètres de taille de grille de colonne](./assets/pb-configure-advanced-content-tools-grid-size.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

[1]: https://cloud.google.com/maps-platform/
[2]: https://cloud.google.com/maps-platform/places/
[3]: https://cloud.google.com/maps-platform/user-guide/
[4]: https://developers.google.com/maps/documentation/javascript/get-api-key
[5]: https://www.google.com/maps
[6]: https://mapstyle.withgoogle.com/
