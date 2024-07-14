---
title: Traduire une page de contenu
description: Découvrez comment créer une version traduite de chaque page disponible à partir de la vue de magasin spécifique.
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# Traduire une page de contenu

Si votre boutique comporte plusieurs vues dans différentes [langues](../stores-purchase/store-localize.md) et que vous avez défini le paramètre régional de chaque vue dans une langue différente, le résultat est un site partiellement traduit. L’étape suivante consiste à créer une version traduite de chaque page disponible à partir de la vue de magasin spécifique. La colonne [!UICONTROL Store View] de la liste _[!UICONTROL Manage Pages]_affiche chaque vue ayant une version traduite de la page.

Pour traduire une page de contenu, vous devez créer une autre page qui possède la même clé URL que l’original, mais qui est affectée à la vue de magasin spécifique. Ensuite, mettez à jour la page de la vue spécifique avec le texte traduit. L’exemple suivant montre comment créer une version traduite de la page _À propos de nous_ pour la vue de magasin en espagnol.

## Étape 1 : Copiez la clé URL de la page à traduire

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Dans la grille, recherchez la page à traduire et ouvrez-la en mode _edit_.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) de la section **[!UICONTROL Search Engine Optimization]** et copiez les **[!UICONTROL URL Key]** dans le Presse-papiers.

1. Pour revenir à la grille _[!UICONTROL Pages]_, cliquez sur **[!UICONTROL Back]**dans la barre de boutons supérieure.

## Etape 2 : Ajouter une page pour le contenu traduit

1. Cliquez sur **[!UICONTROL Add New Page]**.

1. Saisissez le **[!UICONTROL Page Title]** traduit.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) et complétez le texte traduit de la page.**[!UICONTROL Content]**

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) de **[!UICONTROL Search Engine Optimization]** et procédez comme suit :

   - Collez le **[!UICONTROL URL Key]** que vous avez copié depuis la page d’origine.

   - Saisissez le texte traduit pour **[!UICONTROL Meta Title]**, **[!UICONTROL Meta Keywords]** et **[!UICONTROL Meta Description]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) de la section **[!UICONTROL Page in Websites]** et définissez **[!UICONTROL Store View]** sur la vue du magasin où la page doit être disponible.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) et définissez la colonne **[!UICONTROL Design]** de la page.**[!UICONTROL Layout]**

1. Cliquez sur **[!UICONTROL Save]**.

1. Lorsque vous y êtes invité, actualisez les [caches](../systems/cache-management.md) non valides.

## Étape 3 : Vérifier la traduction

Pour vérifier la traduction, accédez au storefront et utilisez le sélecteur de langue pour modifier l’affichage du magasin.

Notez qu’il existe encore des éléments sur la page qui doivent être traduits, notamment les liens de pied de page [block](block-add.md), le [message de bienvenue](../getting-started/storefront-branding.md#change-the-welcome-message) et les [informations sur le produit](../stores-purchase/store-localize.md#localize-products).
