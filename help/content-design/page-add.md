---
title: Ajout et suppression de pages
description: Découvrez comment ajouter et supprimer des pages de contenu utilisées dans votre  [!DNL Commerce] boutique.
exl-id: a7a503ea-3631-4be2-81e4-aed2ae9419dc
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '1105'
ht-degree: 0%

---

# Ajout et suppression de pages

Le processus d’ajout d’une page de contenu à votre magasin est pratiquement le même pour tout type de page que vous souhaitez créer. Vous pouvez inclure du texte, des images, des blocs de contenu, des variables et des widgets. La plupart des pages de contenu sont conçues pour être lues par les moteurs de recherche en premier, et par les personnes en second. Gardez les besoins de chacune de ces deux audiences à l’esprit lors du choix du titre de la page et de l’URL, ainsi que lors de la composition des métadonnées et du contenu. Une fois votre page terminée, elle peut être ajoutée à la navigation de votre magasin, liée à d’autres pages, liée au pied de page de votre magasin ou utilisée comme nouvelle [page d’accueil](page-home-new.md).

![Grille de pages](./assets/pages-grid.png){width="700" zoomable="yes"}

## Ajouter une page

Les instructions suivantes vous guident à chaque étape pour créer une page de base. Certaines fonctions avancées sont ignorées, mais sont abordées dans d’autres rubriques.

### Étape 1 : création de la page

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Cliquez sur **[!UICONTROL Add New Page]**.

   ![Nouvelle page](./assets/pages-new-page.png){width="600" zoomable="yes"}

1. Si vous ne souhaitez pas publier la page immédiatement, définissez **[!UICONTROL Enable Page]** sur `No`.

1. Saisissez le **[!UICONTROL Page Title]**.

   Le titre de la page s’affiche dans la navigation [chemin de navigation](../catalog/navigation-breadcrumb-trail.md).

### Etape 2 : compléter le contenu

Ajoutez le contenu de la page en fonction de la [configuration des outils de contenu avancés](../configuration-reference/general/content-management.md).

#### Utilisation des outils de contenu du créateur de pages

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

   ![Contenu avec Page Builder](../page-builder/assets/pb-page-content.png){width="600" zoomable="yes"}

1. Dans la zone **[!UICONTROL Content Heading]**, saisissez l’en-tête qui doit apparaître en haut de la page.

   S’il est activé, l’étape et le panneau [Page Builder](../page-builder/introduction.md) apparaissent sous l’en-tête Contenu. Pour plus d’informations, voir [Workspace](../page-builder/workspace.md). Si _Page Builder_ n’est pas activé, l’éditeur s’ouvre en mode WYSIWYG avec la barre d’outils supérieure.

1. Complétez le contenu et formatez le texte selon vos besoins.

#### Utilisation de la barre d’outils de l’éditeur

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

   ![Contenu](./assets/page-content-editor.png){width="600" zoomable="yes"}

1. Dans la zone **[!UICONTROL Content Heading]**, saisissez l’en-tête qui doit apparaître en haut de la page.

1. Complétez le contenu et formatez le texte selon vos besoins.

   Vous pouvez ajouter [images](media-storage.md), [variables](../systems/variables-predefined.md) et [widgets](widgets.md) si nécessaire. Pour plus d’informations, voir [Utilisation de l’éditeur](editor.md).

### Étape 3 : renseigner les informations d’optimisation pour les moteurs de recherche

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimization]**.

   ![Optimisation du moteur de recherche](./assets/page-search-engine-optimization.png){width="600" zoomable="yes"}

1. Acceptez la valeur par défaut ou entrez un autre **[!UICONTROL URL Key]** constitué de tous les caractères minuscules, avec des tirets au lieu d&#39;espaces.

   La clé URL par défaut a été créée lors de l’enregistrement de la page et repose sur l’en-tête Contenu.

1. Saisissez un **[!UICONTROL Meta Title]** pour la page.

   Le méta-titre doit contenir moins de 70 caractères et s’affiche dans la barre de titre et l’onglet du navigateur.

1. Saisissez le **[!UICONTROL Meta Keywords]** à valeur élevée que les moteurs de recherche peuvent utiliser pour indexer la page.

   Séparez plusieurs mots par une virgule. Certains moteurs de recherche ignorent les méta-mots-clés, mais les utilisent d’autres.

1. Pour **[!UICONTROL Meta Description]**, entrez une brève description de la page pour les listes de résultats de recherche.

   Idéalement, la description doit comporter entre 150 et 160 caractères, avec une limite maximale de 255 caractères.

1. Cliquez sur **[!UICONTROL Save]**.

### Étape 4 : spécification de la portée de la page

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Page in Websites]**.

   ![Pages dans les sites web](./assets/page-in-websites.png){width="600" zoomable="yes"}

1. Dans la liste **[!UICONTROL Store View]**, sélectionnez chaque vue dans laquelle la page doit être disponible.

   Si l’installation comporte plusieurs sites web, sélectionnez chaque site web et affichez l’emplacement de stockage de la page.

### Étape 5 : Identifier la page parente (le cas échéant)

{{ee-feature}}

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Hierarchy]**.

   ![Hiérarchie](./assets/page-hierarchy.png){width="600" zoomable="yes"}

1. Si cette page est un enfant d’une autre page, cochez la case du **[!UICONTROL Parent page]**.

### Étape 6 : Saisir les modifications de conception (facultatif)

1. Pour modifier la mise en page de la page, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Design]**.

   ![Design](./assets/page-design.png){width="600" zoomable="yes"}

1. Pour modifier la mise en page des colonnes de la page, définissez **[!UICONTROL Layout]** sur l’une des options suivantes :

   - `Empty`
   - `1 column`
   - `2 columns with left bar`
   - `2 columns with right bar`
   - `3 columns`
   - `Page -- Full Width` (Nécessite [Page Builder](../page-builder/introduction.md))
   - `Category -- Full Width` (Nécessite Page Builder)
   - `Product -- Full Width` (Nécessite Page Builder)

1. Pour appliquer un **[!UICONTROL Custom Layout Update]**, choisissez le nom du fichier dans la liste.

   Pour plus d’informations, voir [Mises à jour de la mise en page](layout-updates.md).

1. Pour modifier le thème de la page, définissez **[!UICONTROL New Theme]** sur l’une des options suivantes :

   - `Magento Black`
   - `Magento Luma`

1. ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Pour planifier une modification de conception, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Custom Design Update]** et procédez comme suit :

   ![Mise à jour de conception personnalisée](./assets/page-custom-design-update.png){width="600" zoomable="yes"}

   - Utilisez le calendrier (![Icône Calendrier](../assets/icon-calendar.png)) pour choisir les dates **[!UICONTROL From]** et **[!UICONTROL To]** auxquelles la modification doit prendre effet.

   - Pour appliquer un thème différent à la page, sélectionnez le nom de **[!UICONTROL New Theme]**.

   - Pour modifier la mise en page des colonnes de la page, choisissez le **[!UICONTROL Layout]** à appliquer.

### Étape 7 : aperçu de la page

1. Cliquez sur la flèche **[!UICONTROL Save]** et choisissez **[!UICONTROL Save & Close]** pour revenir à la grille Pages.

1. Recherchez la page dans la grille et sélectionnez **[!UICONTROL View]** dans la colonne _[!UICONTROL Action]_.

1. Pour revenir à la grille, cliquez sur **[!UICONTROL Back]** dans le coin supérieur gauche de la fenêtre du navigateur.

### Étape 8 : Publish de la page

1. Sélectionnez **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_de la grille.

1. Définissez **[!UICONTROL Enable Page]** sur `Yes`.

1. Cliquez sur la flèche **[!UICONTROL Save]** et choisissez **[!UICONTROL Save & Close]**.

## Dupliquer une page

N’importe quelle page de contenu peut être utilisée comme modèle et enregistrée en tant que doublon. Vous pouvez utiliser cette technique pour gagner du temps afin de créer une conception cohérente pour les pages de contenu de votre site. La page en double conserve le titre de la page d’origine, mais les champs Clé URL et État doivent être mis à jour.

![Enregistrer et dupliquer](./assets/page-duplicate-save-menu.png){width="600" zoomable="yes"}

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Dans la grille, recherchez la page à dupliquer et cliquez sur **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_.

1. Cliquez sur la flèche **[!UICONTROL Save]** et choisissez **[!UICONTROL Save & Duplicate]**.

1. Lorsque vous voyez les messages que la page a été enregistrée et dupliquée, cliquez sur **[!UICONTROL Back]** dans la barre de boutons supérieure pour revenir à la grille.

1. Recherchez la page en double dans la grille et notez ce qui suit :

   - Le titre de la page est identique à celui de l’original.
   - Une clé d’URL unique, mais temporaire, est affectée.
   - L’état de la page est `Disabled`.

1. Ouvrez la page en double en mode _Modifier_ et procédez comme suit :

   - Si vous souhaitez publier la page immédiatement, définissez **[!UICONTROL Enable Page]** sur `Yes`.

   - Mettez à jour **[!UICONTROL Page Title]**, si nécessaire.

   - Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) et saisissez l’unique **[!UICONTROL URL Key]** que vous souhaitez utiliser pour la page en double.**[!UICONTROL Search Engine Optimization]**

     ![Clé d’URL temporaire](./assets/page-search-engine-optimization-url-key-duplicate.png){width="600" zoomable="yes"}

   - Mettez à jour le contenu de la page restant, si nécessaire.

1. Cliquez sur la flèche **[!UICONTROL Save]** et choisissez **[!UICONTROL Save & Close]**.

   La page dupliquée de la grille reflète vos modifications.

## Menu Enregistrer

| Commande | Description |
|--- |--- |
| [!UICONTROL Save] | Enregistrez la page active et continuez à travailler. |
| [!UICONTROL Save & New] | Enregistrez la page active, fermez-la, puis commencez une nouvelle page. |
| [!UICONTROL Save & Duplicate] | Enregistrez la page active, fermez-la, puis ouvrez une nouvelle copie en double. |
| [!UICONTROL Save & Close] | Enregistrez la page active, fermez-la, puis revenez à la grille Pages . |

{style="table-layout:auto"}

## Suppression d’une page

Il existe deux manières de supprimer une page créée. Vous pouvez la supprimer de la grille _[!UICONTROL Pages]_ou de la page_[!UICONTROL Edit]_.

### Méthode 1 : supprimer une page de la grille Pages

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Localisez les pages à l’aide de filtres au-dessus de la grille et cochez la case correspondant à une ou plusieurs pages à supprimer.

1. Dans le coin supérieur gauche de la liste, définissez **[!UICONTROL Actions]** sur `Delete`.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

### Méthode 2 : supprimer une page de la page de modification

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Recherchez la page à supprimer.

1. Dans la colonne _[!UICONTROL Actions]_de l’entité de page, cliquez sur **[!UICONTROL Select]**et choisissez **[!UICONTROL Edit]**.

1. Dans la barre de boutons, cliquez sur **[!UICONTROL Delete Page]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.
