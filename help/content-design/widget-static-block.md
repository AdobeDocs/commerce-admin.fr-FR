---
title: Utiliser un widget pour positionner un bloc
description: Découvrez comment utiliser un widget de bloc statique pour placer un contenu existant presque n’importe où dans votre boutique.
exl-id: 174deef2-33c4-4f1a-8ca8-4969be209bc7
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# Utiliser un widget pour positionner un bloc

Le _bloc statique CMS_ [widget](widgets.md) vous permet de placer un [bloc de contenu](blocks.md) existant presque n’importe où dans votre magasin.

![Widgets](./assets/widgets.png){width="700" zoomable="yes"}

## Étape 1 : Sélection du type de widget

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Widget]**.

1. Dans la section _Settings_ , définissez **[!UICONTROL Type]** sur `CMS Static Block` et cliquez sur **[!UICONTROL Continue]**.

1. Vérifiez que le **[!UICONTROL Design Theme]** est défini sur le thème actuel et cliquez sur **[!UICONTROL Continue]**.

   ![Paramètres du widget](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Dans la section _[!UICONTROL Storefront Properties]_, procédez comme suit :

   - Pour **[!UICONTROL Widget Title]**, saisissez un titre descriptif pour le widget.

     Ce titre est visible uniquement à partir de _Admin_.

   - Pour **[!UICONTROL Assign to Store Views]**, sélectionnez les vues de magasin où le widget est visible.

     Vous pouvez sélectionner une vue de magasin spécifique, ou `All Store Views`. Pour sélectionner plusieurs vues, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

   - (Facultatif) Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre dans lequel cet élément apparaît avec les autres dans la même partie de la page. (`0` = premier, `1` = deuxième, `3` = troisième, etc.)

     ![Propriétés Storefront](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

## Étape 2 : terminer les mises à jour de la mise en page du widget

1. Dans la section _[!UICONTROL Layout Updates]_, cliquez sur **[!UICONTROL Add Layout Update]**.

1. Définissez **[!UICONTROL Display On]** sur la catégorie, le produit ou la page dans laquelle vous souhaitez que le bloc apparaisse.

1. Pour placer le bloc sur une page spécifique, procédez comme suit :

   - Sélectionnez l&#39; **[!UICONTROL Page]** où vous souhaitez que le bloc s&#39;affiche.

   - Sélectionnez le **[!UICONTROL Block Reference]** qui identifie l&#39;emplacement d&#39;affichage du bloc sur la page.

   - Acceptez le paramètre par défaut pour **[!UICONTROL Template]**, défini sur `CMS Static Block Default Template`.

     ![Mises à jour de mise en page](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

### Options de mise à jour de mise en page

| Champ | Description |
|--- |--- |
| **_[!UICONTROL Categories]_** |  |
| [!UICONTROL Anchor Categories] | Affiche le widget sur la page de catégorie de l’ancre.<br/>**[!UICONTROL Categories]**- Catégories dans lesquelles l’ancre est affichée. Options : `All` /`Specific Categories`<br/>**[!UICONTROL Container]** - Définissez le conteneur sur la partie de la mise en page où vous souhaitez afficher le widget.<br/>**[!UICONTROL Template]**- Détermine le thème de la mise en page. |
| [!UICONTROL Non-Anchor Categories] | Affiche le widget sur la page de catégorie de non-ancrage.<br/>**[!UICONTROL Categories]**- Catégories dans lesquelles l’ancre est affichée. Options : `All` /`Specific Categories`<br/>**[!UICONTROL Container]** - Définissez le conteneur sur la partie de la mise en page où vous souhaitez afficher le widget.<br/>**[!UICONTROL Template]**- Détermine le thème de la mise en page. |
| **_[!UICONTROL Products]_** |  |
| Tous les types de produit | Affiche le widget sur un type spécifique de page de produit ou sur toutes les pages de produit. <br/>**[!UICONTROL Products]**- Produits pour lesquels le widget s’affiche. Options : `All` /` Specific Products`<br/>**[!UICONTROL Container]** - Définissez le conteneur sur la partie de la mise en page où vous souhaitez afficher le widget.<br/>**[!UICONTROL Template]**- Détermine le thème de la mise en page. |
| **_[!UICONTROL Generic Pages]_** |  |
| [!UICONTROL All Pages] | Affiche le widget sur toutes les pages. <br/>**[!UICONTROL Container]**- Définissez le conteneur sur la partie de la mise en page où vous souhaitez afficher le widget.<br/>**[!UICONTROL Template]** - Détermine le thème de la mise en page. |
| [!UICONTROL Specified Page] | Affiche le widget sur une page spécifique. Options : <br/>**[!UICONTROL Page]**- Pages pour lesquelles le widget est affiché.<br/>**[!UICONTROL Container]** - Définissez le conteneur sur la partie de la mise en page où vous souhaitez afficher le widget.<br/>**Modèle** - Détermine le thème de la mise en page. |
| [!UICONTROL Page Layouts] | Affiche le widget sur les pages avec une disposition spécifique. <br/>**[!UICONTROL Page]**- Pages pour lesquelles le widget est affiché.<br/>**[!UICONTROL Container]** - Définissez le conteneur sur la partie de la mise en page où vous souhaitez afficher le widget.<br/>**[!UICONTROL Template]**- Détermine le thème de la mise en page. |

{style="table-layout:auto"}

## Etape 3 : placez le bloc

1. Dans le panneau de gauche, sélectionnez **[!UICONTROL Widget Options]**.

1. Cliquez sur **[!UICONTROL Select Block…]** et sélectionnez le bloc à placer dans la liste.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

   L’application apparaît désormais dans la liste.

1. Lorsque vous y êtes invité, suivez les instructions situées en haut de la page pour mettre à jour l’index et le cache de la page.

1. Revenez à votre vitrine pour vérifier que le bloc s’affiche à l’emplacement approprié.

   Pour déplacer le bloc, vous pouvez rouvrir le widget ou essayer une autre référence de page ou de bloc.
