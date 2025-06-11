---
title: Ajouter et supprimer des pages
description: Découvrez comment ajouter et supprimer des pages de contenu utilisées dans votre  [!DNL Commerce] .
exl-id: a7a503ea-3631-4be2-81e4-aed2ae9419dc
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '1122'
ht-degree: 0%

---

# Ajouter et supprimer des pages

Le processus d’ajout d’une page de contenu à votre boutique est essentiellement le même pour tout type de page que vous souhaitez créer. Vous pouvez inclure du texte, des images, des blocs de contenu, des variables et des widgets. La plupart des pages de contenu sont conçues pour être lues d’abord par les moteurs de recherche, puis par les utilisateurs. Gardez à l’esprit les besoins de chacune de ces deux audiences différentes lors du choix du titre de la page et de l’URL, ainsi que lors de la composition des métadonnées, des données et du contenu. Une fois la page terminée, vous pouvez l’ajouter à la navigation de votre boutique, la lier à d’autres pages, la lier au pied de page de votre boutique ou l’utiliser comme nouvelle [page d’accueil](page-home-new.md).

![Grille Pages](./assets/pages-grid.png){width="700" zoomable="yes"}

## Ajouter une page

Les instructions suivantes vous guident à travers chaque étape pour créer une page de base. Certaines fonctionnalités avancées sont ignorées, mais sont traitées dans d’autres rubriques.

### Étape 1 : créer la page

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Cliquez sur **[!UICONTROL Add New Page]**.

   ![Nouvelle page](./assets/pages-new-page.png){width="600" zoomable="yes"}

1. Si vous ne souhaitez pas publier la page immédiatement, définissez **[!UICONTROL Enable Page]** sur `No`.

1. Saisissez le **[!UICONTROL Page Title]**.

   Le titre de la page s’affiche dans la navigation [chemin de navigation](../catalog/navigation-breadcrumb-trail.md).

### Étape 2 : terminer le contenu

Ajoutez le contenu de la page en fonction de votre [configuration des outils de contenu avancés](../configuration-reference/general/content-management.md).

#### Utilisation des outils de contenu de Page Builder

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

   ![Contenu avec Page Builder](../page-builder/assets/pb-page-content.png){width="600" zoomable="yes"}

1. Dans la zone de **[!UICONTROL Content Heading]**, saisissez l’en-tête qui doit apparaître en haut de la page.

   Si cette option est activée, l’étape et le panneau [Page Builder](../page-builder/introduction.md) s’affichent sous l’en-tête Contenu. Pour plus d&#39;informations, voir [Workspace](../page-builder/workspace.md). Si _Page Builder_ n’est pas activé, l’éditeur s’ouvre en mode WYSIWYG avec la barre d’outils supérieure.

1. Complétez le contenu et mettez en forme le texte selon vos besoins.

#### Utiliser la barre d’outils de l’éditeur

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

   ![Contenu](./assets/page-content-editor.png){width="600" zoomable="yes"}

1. Dans la zone de **[!UICONTROL Content Heading]**, saisissez l’en-tête qui doit apparaître en haut de la page.

1. Complétez le contenu et mettez le texte en forme selon vos besoins.

   Vous pouvez ajouter des [images](media-storage.md), [variables](../systems/variables-predefined.md) et [widgets](widgets.md) selon vos besoins. Pour plus d’informations, voir [ Utilisation de l’éditeur ](editor.md).

### Étape 3 : remplir les informations d’optimisation pour les moteurs de recherche

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimization]**.

   ![Optimisation du moteur de recherche](./assets/page-search-engine-optimization.png){width="600" zoomable="yes"}

1. Acceptez la valeur par défaut ou saisissez une autre **[!UICONTROL URL Key]** composée de tous les caractères minuscules, avec des tirets au lieu d’espaces.

   La clé URL par défaut a été créée lors de l’enregistrement de la page et est basée sur l’en-tête Contenu.

1. Saisissez un **[!UICONTROL Meta Title]** pour la page.

   Le méta-titre doit contenir moins de 70 caractères et s’afficher dans la barre de titre et dans l’onglet du navigateur.

1. Saisissez les **[!UICONTROL Meta Keywords]** de grande valeur que les moteurs de recherche peuvent utiliser pour indexer la page.

   Séparez les différents mots par une virgule. Certains moteurs de recherche ignorent les méta-mots-clés, mais d’autres les utilisent.

1. Par **[!UICONTROL Meta Description]**, saisissez une brève description de la page pour les listes de résultats de recherche.

   Idéalement, la description doit comporter entre 150 et 160 caractères, avec une limite maximale de 255.

1. Cliquez sur **[!UICONTROL Save]**.

### Étape 4 : spécifier la portée de la page

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Page in Websites]**.

   ![Pages dans les sites web](./assets/page-in-websites.png){width="600" zoomable="yes"}

1. Dans la liste **[!UICONTROL Store View]**, sélectionnez chaque vue où la page doit être disponible.

   Si l’installation comporte plusieurs sites web, sélectionnez chaque site web et stockez l’affichage où la page doit être disponible.

### Étape 5 : identifier la page parente (le cas échéant)

{{ee-feature}}

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Hierarchy]**.

   ![ Hiérarchie ](./assets/page-hierarchy.png){width="600" zoomable="yes"}

1. Si cette page est l’enfant d’une autre page, cochez la case du **[!UICONTROL Parent page]**.

### Étape 6 : Saisie des modifications de conception (facultatif)

1. Pour modifier la disposition de la page, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Design]**.

   ![ Conception ](./assets/page-design.png){width="600" zoomable="yes"}

1. Pour modifier la disposition des colonnes de la page, définissez **[!UICONTROL Layout]** sur l’une des options suivantes :

   - `Empty`
   - `1 column`
   - `2 columns with left bar`
   - `2 columns with right bar`
   - `3 columns`
   - `Page -- Full Width` (Nécessite [Page Builder](../page-builder/introduction.md))
   - `Category -- Full Width` (Nécessite Page Builder)
   - `Product -- Full Width` (Nécessite Page Builder)

1. Pour appliquer un **[!UICONTROL Custom Layout Update]**, choisissez le nom du fichier dans la liste.

   Pour plus d’informations, voir [ Mises à jour de la disposition ](layout-updates.md).

1. Pour modifier le thème de la page, définissez **[!UICONTROL New Theme]** sur l’une des options suivantes :

   - `Magento Black`
   - `Magento Luma`

1. ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Pour planifier une modification de conception, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Custom Design Update]** et procédez comme suit :

   ![Mise à jour de la conception personnalisée](./assets/page-custom-design-update.png){width="600" zoomable="yes"}

   - Utilisez le calendrier (![icône Calendrier](../assets/icon-calendar.png)) pour choisir les dates **[!UICONTROL From]** et **[!UICONTROL To]** auxquelles la modification doit prendre effet.

   - Pour appliquer un autre thème à la page, sélectionnez le nom du **[!UICONTROL New Theme]**.

   - Pour modifier la disposition des colonnes de la page, choisissez la **[!UICONTROL Layout]** à appliquer.

### Étape 7 : prévisualiser la page

1. Cliquez sur la flèche **[!UICONTROL Save]** et choisissez **[!UICONTROL Save & Close]** pour revenir à la grille Pages.

1. Recherchez la page dans la grille et sélectionnez **[!UICONTROL View]** dans la colonne _[!UICONTROL Action]_.

1. Pour revenir à la grille, cliquez sur **[!UICONTROL Back]** dans le coin supérieur gauche de la fenêtre du navigateur.

### Étape 8 : publier la page

1. Sélectionnez **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_&#x200B;de la grille.

1. Définissez **[!UICONTROL Enable Page]** sur `Yes`.

1. Cliquez sur la flèche **[!UICONTROL Save]** et choisissez **[!UICONTROL Save & Close]**.

## Dupliquer une page

N’importe quelle page de contenu peut être utilisée comme modèle et enregistrée en tant que doublon. Utilisez cette technique pour gagner du temps et créer une conception cohérente pour les pages de contenu de l’ensemble de votre site. Le duplicata de page conserve le titre de la page d’origine, mais les champs Clé URL et Statut doivent être mis à jour.

![Enregistrer et dupliquer](./assets/page-duplicate-save-menu.png){width="600" zoomable="yes"}

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Dans la grille, recherchez la page à dupliquer et cliquez sur **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_.

1. Cliquez sur la flèche **[!UICONTROL Save]** et choisissez **[!UICONTROL Save & Duplicate]**.

1. Lorsque les messages qui indiquent que la page a été enregistrée et dupliquée s’affichent, cliquez sur **[!UICONTROL Back]** dans la barre de boutons supérieure pour revenir à la grille.

1. Recherchez la page en double dans la grille et notez ce qui suit :

   - Le titre de la page est identique à celui de l’original.
   - Une clé d’URL unique, mais temporaire, est attribuée.
   - Le statut de la page est `Disabled`.

1. Ouvrez la page en double en mode _Modifier_ et procédez comme suit :

   - Si vous souhaitez publier la page immédiatement, définissez **[!UICONTROL Enable Page]** sur `Yes`.

   - Mettez à jour le **[!UICONTROL Page Title]**, si nécessaire.

   - Développez ![Sélecteur de développement](../assets/icon-display-expand.png) la section **[!UICONTROL Search Engine Optimization]** et saisissez le **[!UICONTROL URL Key]** unique que vous souhaitez utiliser pour la page en double.

     ![Clé URL temporaire](./assets/page-search-engine-optimization-url-key-duplicate.png){width="600" zoomable="yes"}

   - Mettez à jour le contenu de page restant, si nécessaire.

1. Cliquez sur la flèche **[!UICONTROL Save]** et choisissez **[!UICONTROL Save & Close]**.

   La page en double dans la grille reflète vos modifications.

## Enregistrer le menu

| Commande | Description |
|--- |--- |
| [!UICONTROL Save] | Enregistrer la page active et continuer à travailler. |
| [!UICONTROL Save & New] | Enregistrez et fermez la page active, puis commencez une nouvelle page. |
| [!UICONTROL Save & Duplicate] | Enregistrer et fermer la page active, et ouvrir un nouveau duplicata. |
| [!UICONTROL Save & Close] | Enregistrer et fermer la page active, puis revenir à la grille Pages. |

{style="table-layout:auto"}

## Suppression d’une page

Il existe deux manières de supprimer une page créée. Vous pouvez le supprimer de la grille de _[!UICONTROL Pages]_&#x200B;ou de la page de&#x200B;_[!UICONTROL Edit]_.

### Méthode 1 : suppression d’une page de la grille Pages

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Recherchez les pages à l’aide de filtres au-dessus de la grille et cochez la case d’une ou plusieurs pages à supprimer.

1. Dans le coin supérieur gauche de la liste, définissez **[!UICONTROL Actions]** sur `Delete`.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

### Méthode 2 : supprimer une page de la page d’édition

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Recherchez la page à supprimer.

1. Dans la colonne _[!UICONTROL Actions]_&#x200B;de l’entité de page, cliquez sur **[!UICONTROL Select]**&#x200B;et choisissez **[!UICONTROL Edit]**.

1. Dans la barre de boutons, cliquez sur **[!UICONTROL Delete Page]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.
