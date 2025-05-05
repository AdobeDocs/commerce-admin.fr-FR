---
title: Éléments - Boutons
description: Découvrez le type de contenu Boutons, utilisé pour ajouter un bouton individuel ou un ensemble de boutons dans la scène  [!DNL Page Builder] .
exl-id: 9f1681c5-04b0-4259-aaf6-5d8081bd8cdb
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1586'
ht-degree: 0%

---

# Éléments - Boutons

Utilisez le type de contenu _Boutons_ pour ajouter un bouton individuel ou un ensemble de boutons dans la [[!DNL Page Builder] scène](workspace.md#stage). Vous pouvez disposer les boutons horizontalement ou verticalement, puis les ajouter directement aux rangées, colonnes, onglets et bannières sur la scène.

![Bannière avec un bouton sur le storefront](./assets/pb-storefont-banner-with-button.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Toolbox

Lorsque vous utilisez le type de contenu Boutons , vous ajoutez et modifiez des boutons individuels et le conteneur de boutons qui contient un ou plusieurs boutons. Chacun dispose de sa propre boîte à outils que vous utilisez pour concevoir des boutons sur la scène [!DNL Page Builder].

### Barre d’outils à boutons individuelle

![Boîte à outils de bouton](./assets/pb-elements-button-settings.png){width="500" zoomable="yes"}

| Outil | Icône | Description |
| --------- | -------- | -------------- |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} | Ouvre la page Bouton Modifier dans laquelle vous pouvez modifier les propriétés du bouton. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="25"} | Effectue une copie du bouton. |
| Supprimer | ![Supprimer l’icône](./assets/pb-icon-remove.png){width="25"} | Supprime le bouton de la scène. |

{style="table-layout:auto"}

### Boîte à outils du conteneur de boutons

![Boîte à outils de conteneur de boutons](./assets/pb-elements-buttons-toolbox-settings.png){width="500" zoomable="yes"}

| Outil | Icône | Description |
| --------- | ----------------- | ----------- |
| Déplacer | ![Icône Déplacer](./assets/pb-icon-move.png){width="25"} | Déplace le conteneur de boutons vers un autre emplacement valide de la page. |
| Ajouter | ![Ajouter une icône](./assets/pb-icon-add-button.png){width="25"} | Ajoute un bouton au conteneur. |
| (label) | Bouton | Identifie le conteneur actuel en tant qu’élément de bouton. |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} | Ouvre la page Boutons de modification, dans laquelle vous pouvez modifier les propriétés du conteneur. |
| Masquer | ![Icône Masquer](./assets/pb-icon-hide.png){width="25"} | Masque le conteneur de boutons. |
| Afficher | ![Icône Afficher](./assets/pb-icon-show.png){width="25"} | Affiche le conteneur de boutons masqués. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="25"} | Effectue une copie du conteneur de boutons. |
| Supprimer | ![Supprimer l’icône](./assets/pb-icon-remove.png){width="25"} | Supprime le conteneur de boutons et son contenu de la scène. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Ajouter un bouton individuel

1. Dans le panneau [!DNL Page Builder], développez **[!UICONTROL Elements]** et faites glisser un espace réservé **[!UICONTROL Buttons]** sur une ligne, une colonne ou un ensemble d’onglets sur la scène.

   ![Faire glisser un bouton sur l’étape](./assets/pb-elements-button-drag.png){width="500" zoomable="yes"}

1. Pointez sur le bouton pour afficher la boîte à outils et sélectionnez l’icône _Paramètres_ (![Icône Paramètres](./assets/pb-icon-settings.png)).

1. Saisissez le **[!UICONTROL Button Text]** à afficher sur le bouton.

   ![ Paramètres de bouton de base](./assets/pb-elements-button-settings-button-text.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Button Type]** sur l’une des options suivantes :

   | Type | Description |
   | ------ | ----------- |
   | `Primary` | Applique le style de bouton principal à partir de la feuille de style active. |
   | `Secondary` | Applique le style de bouton secondaire à partir de la feuille de style active, le cas échéant. |
   | `Link` | Crée un lien hypertexte plutôt qu’un bouton. |

   {style="table-layout:auto"}

   ![Exemple de bouton Principal et secondaire](./assets/pb-elements-button-settings-button-primary-secondary.png){width="500" zoomable="yes"}

1. Définissez le **[!UICONTROL Button Link]** à l’aide de l’un des types suivants :

   - **[!UICONTROL URL]** - Entrez l’URL de destination du lien.

     L’URL peut être soit un lien relatif vers un produit ou une page de votre magasin, soit une URL complète.

     Exemple d’URL relative - `../luma-analog-watch.html`

     Exemple d’URL complète - `http://mystore.com/luma-analog-watch.html`

     Si le lien accède à un autre site web, vous pouvez conserver la page active ouverte sur votre boutique en ouvrant le lien dans un nouvel onglet du navigateur.

     Pour empêcher le visiteur de quitter votre boutique, cochez la case **[!UICONTROL Open in new tab]** .

   - **[!UICONTROL Product]** - Entrez un nom de produit (partiel ou complet) ou un SKU, puis sélectionnez le nom de produit dans la liste.

     >[!NOTE]
     >
     >Les produits sont affichés dans la liste selon les paramètres _Afficher les produits en rupture de stock_ . Pour les marchands multi-Source utilisant [Inventory management](../inventory-management/introduction.md), la liste de produits est limitée par la source affectée au site web par défaut uniquement.

     ![Choix d’un produit pour le lien de bouton](./assets/pb-elements-button-settings-button-link-product-search.png){width="600" zoomable="yes"}

   - **[!UICONTROL Category]** - Entrez un nom de catégorie (partiel ou complet) ou cliquez dans le champ vierge pour afficher l’arborescence des catégories. Sélectionnez ensuite le nom de la catégorie dans l&#39;arborescence.

     ![Choix d’une catégorie pour le lien de bouton](./assets/pb-elements-button-settings-button-link-category-search.png){width="600" zoomable="yes"}

   - **[!UICONTROL Page]** - Entrez le nom d’une page CMS (partielle ou complète) ou cliquez dans le champ vierge pour afficher la liste complète. Sélectionnez ensuite le nom de la page dans la liste des résultats de recherche.

     ![Choisir la page CMS pour le lien de bouton](./assets/pb-elements-button-settings-button-link-page-search.png){width="600" zoomable="yes"}

1. Renseignez les [paramètres avancés][advanced-settings] si nécessaire.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]** dans le coin supérieur droit pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

## Ajouter un ensemble de boutons

Les sections suivantes décrivent une série d’étapes permettant de commencer par un bouton individuel et de créer un ensemble de trois boutons au sein d’un conteneur de boutons. Si vous ne disposez pas déjà d’un bouton individuel, suivez les instructions précédentes pour ajouter un bouton individuel à la scène.

### Etape 1 : créer le second bouton

1. Pointez sur le conteneur de boutons pour afficher la boîte à outils et sélectionnez l’icône _Ajouter_ ( ![Ajouter une icône](./assets/pb-icon-add-button.png){width="20"} ).

   ![Ajouter un autre bouton](./assets/pb-elements-buttons-toolbox-add.png){width="500" zoomable="yes"}

1. Saisissez le texte à afficher sur le deuxième bouton.

1. Cliquez sur le nouveau bouton pour afficher sa boîte à outils et sélectionnez l’icône _Paramètres_ ( ![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

   ![Modification du bouton](./assets/pb-elements-button-set-edit-button2-toolbox.png){width="500" zoomable="yes"}

1. Définissez **[!UICONTROL Button Type]** sur `Secondary`.

1. Configurez le **[!UICONTROL Button Link]** selon vos besoins.

   Dans l’exemple suivant, le lien est une URL relative qui accède à la page [Nous contacter](../getting-started/store-details.md#contact-us-form).

   ![Paramètres du bouton Nous contacter](./assets/pb-elements-button-set-edit-button2-toolbox-settings.png){width="600" zoomable="yes"}

1. Renseignez les [paramètres avancés][advanced-settings] si nécessaire.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

### Etape 2 : créer le troisième bouton

1. Cliquez à nouveau sur le second bouton sur l’étape et sélectionnez l’icône _Dupliquer_ ( ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="20"} ).

   ![Duplication d&#39;un bouton](./assets/pb-elements-button-set-contact-us-toolbox-duplicate.png){width="500" zoomable="yes"}

1. Saisissez le texte à afficher sur le troisième bouton.

1. Cliquez sur le troisième bouton pour afficher la boîte à outils et sélectionnez l’icône _Paramètres_ ( ![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

   ![Toolbox pour le troisième bouton](./assets/pb-elements-button-set-find-us-toolbox-settings.png){width="500" zoomable="yes"}

1. Mettez à jour **[!UICONTROL Button Link]** si nécessaire.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

### Etape 3 : mettre à jour le conteneur de boutons

1. Pointez sur le conteneur de boutons pour afficher la boîte à outils et sélectionnez l’icône _Paramètres_ ( ![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

   ![Boîte à outils de conteneur de boutons](./assets/pb-elements-buttons-toolbox-settings.png){width="500" zoomable="yes"}

1. Sous _[!UICONTROL Appearance]_, choisissez **[!UICONTROL Stacked]**.

1. Définissez **[!UICONTROL All Buttons are same size]** sur `Yes`.

   ![Boutons empilés de la même taille](./assets/pb-elements-buttons-settings-appearance-stacked.png){width="300"}

1. Mettez à jour les paramètres restants si nécessaire, à l’aide des descriptions de [Modifier les paramètres d’un conteneur de boutons][button-container].

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

   L’ensemble de boutons empilés complet apparaît sur la scène, avec un bouton principal et deux boutons secondaires.

   ![Boutons empilés sur l&#39;étape](./assets/pb-elements-buttons-stacked.png){width="500" zoomable="yes"}

## Déplacer un bouton

1. Cliquez sur le bouton à déplacer.

1. Sélectionnez l’icône Déplacer ( ![Icône Déplacer](./assets/pb-icon-move.png){width="20"} ) qui s’affiche juste avant le texte du bouton et faites-la glisser vers un nouvel emplacement pour le bouton dans le conteneur de boutons.

   ![Déplacement d’un bouton](./assets/pb-elements-button-set-move-button.png){width="500" zoomable="yes"}

## Modification des paramètres d’un bouton

1. Cliquez sur le bouton sur l’étape pour afficher la boîte à outils et choisissez l’icône _Paramètres_ ( ![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

   ![Boîtes à outils de bouton](./assets/pb-elements-button-toolboxes.png){width="500" zoomable="yes"}

1. Mettez à jour les paramètres standard si nécessaire.

   - **[!UICONTROL Button Text]** - Entrez le texte à afficher sur le bouton (peut également être mis à jour directement à partir de la scène).

   - **[!UICONTROL Button Type]** - Détermine le format du bouton.

     | Type | Description |
     | ------ | ----------- |
     | `Primary` | Applique le style de bouton principal à partir de la feuille de style active. |
     | `Secondary` | Applique le style de bouton secondaire à partir de la feuille de style active, le cas échéant. |
     | `Link` | Crée un lien hypertexte plutôt qu’un bouton. |

     {style="table-layout:auto"}

   - **[!UICONTROL Button Link]** - Détermine la page de destination diffusée lorsque l’utilisateur clique sur le bouton.

     | Option | Description |
     | ------ | ----------- |
     | `URL` | Utilise une URL relative ou complète pour identifier la page de destination. |
     | `Product` | Identifie la page de destination en fonction du nom du produit ou du SKU. Vous pouvez rechercher le nom du produit en fonction d’un nom partiel ou complet. Le produit est ensuite sélectionné dans la liste des résultats de recherche. |
     | `Category` | Identifie la page de destination en tant que catégorie ou sous-catégorie spécifique dans l’arborescence de catégories. |
     | `Page` | Identifie la page de destination en tant que page CMS spécifique. |

     {style="table-layout:auto"}

1. Renseignez les [paramètres avancés][advanced-settings] si nécessaire.

1. Pour enregistrer les paramètres et revenir à l’espace de travail [!DNL Page Builder], cliquez sur **[!UICONTROL Save]** dans le coin supérieur droit.

## Modification des paramètres d’un conteneur de boutons

1. Pointez sur le conteneur de boutons pour afficher la boîte à outils et sélectionnez l’icône _Paramètres_ ( ![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

1. Mettez à jour les paramètres **[!UICONTROL Appearance]** si nécessaire.

   - Utilisez les options de disposition pour afficher les boutons horizontalement ou verticalement dans le conteneur :

     | Option | Description |
     | ------ | ----------- |
     | `Inline` | Dispose les boutons horizontalement. |
     | `Stacked` | Dispose les boutons verticalement. |

     {style="table-layout:auto"}

   - Définissez l’option **[!UICONTROL All buttons are same size]** en fonction de vos préférences.

     Lorsqu’il est défini sur `Yes`, tous les boutons du conteneur ont une taille cohérente, en fonction de la longueur du texte du bouton le plus long.

1. Renseignez les [paramètres avancés][advanced-settings] si nécessaire.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

## Modification des paramètres avancés

Vous pouvez modifier les paramètres _[!UICONTROL Advanced]_&#x200B;de boutons individuels et du conteneur de boutons.

1. Pour contrôler le positionnement dans le conteneur parent, choisissez le **[!UICONTROL Alignment]** :

   | Option | Description |
   | ------ | ----------- |
   | `Default` | Applique le paramètre d’alignement par défaut spécifié dans la feuille de style du thème actif. |
   | `Left` | Aligne le contenu le long de la bordure gauche du conteneur parent, en tenant compte de toute marge intérieure spécifiée. |
   | `Center` | Aligne le contenu au centre du conteneur parent, en tenant compte de toute marge intérieure spécifiée. |
   | `Right` | Aligne le contenu le long de la bordure droite du conteneur parent, en tenant compte de toute marge intérieure spécifiée. |

   {style="table-layout:auto"}

1. Définissez le style **[!UICONTROL Border]** appliqué aux quatre côtés du conteneur de boutons ou de boutons :

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

1. Si vous définissez un style de bordure autre que `None`, renseignez les options d’affichage de la bordure :

   | Option | Description |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Définissez la couleur en choisissant un échantillon, en cliquant sur le sélecteur de couleurs ou en saisissant un nom de couleur valide ou une valeur hexadécimale équivalente. |
   | [!UICONTROL Border Width] | Saisissez le nombre de pixels pour la largeur de la ligne de bordure. |
   | [!UICONTROL Border Radius] | Saisissez le nombre de pixels pour définir la taille du rayon utilisé pour arrondir chaque coin de la bordure. |

   {style="table-layout:auto"}

1. (Facultatif) Indiquez les noms de **[!UICONTROL CSS classes]** dans la feuille de style actuelle à appliquer au conteneur de boutons ou de boutons.

   Séparez plusieurs noms de classe par un espace.

1. Saisissez des valeurs, en pixels, pour le **[!UICONTROL Margins and Padding]** afin de déterminer les marges extérieures et la marge intérieure du conteneur de boutons ou de boutons.

   Saisissez les valeurs correspondantes dans le diagramme.

   | Zone de conteneur | Description |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | Espace vide appliqué au bord extérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Espace blanc appliqué au bord intérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

[advanced-settings]: #change-advanced-settings
[button-container]: #change-settings-for-a-button-container
