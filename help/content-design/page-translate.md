---
title: Traduire une page de contenu
description: Découvrez comment créer une version traduite de chaque page disponible à partir de la vue de magasin spécifique.
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# Traduire une page de contenu

Si votre boutique présente plusieurs vues dans différentes [languages](../stores-purchase/store-localize.md)et que vous avez défini le paramètre régional de chaque vue dans une langue différente, le résultat est un site partiellement traduit. L’étape suivante consiste à créer une version traduite de chaque page disponible à partir de la vue de magasin spécifique. La variable [!UICONTROL Store View] de la colonne _[!UICONTROL Manage Pages]_La liste affiche chaque vue qui comporte une version traduite de la page.

Pour traduire une page de contenu, vous devez créer une autre page qui possède la même clé URL que l’original, mais qui est affectée à la vue de magasin spécifique. Ensuite, mettez à jour la page de la vue spécifique avec le texte traduit. L’exemple suivant montre comment créer une version traduite de la fonction _À propos de nous_ page de la vue du magasin espagnol.

## Étape 1 : Copiez la clé URL de la page à traduire

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Dans la grille, recherchez la page à traduire et ouvrez-la dans _edit_ mode .

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Search Engine Optimization]** et copiez le fichier **[!UICONTROL URL Key]** dans le Presse-papiers.

1. Pour revenir au _[!UICONTROL Pages]_grille, cliquez sur **[!UICONTROL Back]**dans la barre de boutons supérieure.

## Etape 2 : Ajouter une page pour le contenu traduit

1. Cliquez sur **[!UICONTROL Add New Page]**.

1. Saisissez la traduction **[!UICONTROL Page Title]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Content]** et complétez le texte traduit de la page.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Search Engine Optimization]** et procédez comme suit :

   - Collez le **[!UICONTROL URL Key]** que vous avez copié à partir de la page d’origine.

   - Saisissez le texte traduit pour le **[!UICONTROL Meta Title]**, **[!UICONTROL Meta Keywords]**, et **[!UICONTROL Meta Description]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Page in Websites]** section et définition **[!UICONTROL Store View]** dans la vue magasin où la page doit être disponible.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Design]** et définissez la colonne **[!UICONTROL Layout]** de la page.

1. Cliquez sur **[!UICONTROL Save]**.

1. Lorsque vous y êtes invité, actualisez les [caches](../systems/cache-management.md).

## Étape 3 : Vérifier la traduction

Pour vérifier la traduction, accédez au storefront et utilisez le sélecteur de langue pour modifier l’affichage du magasin.

Notez qu’il existe encore des éléments sur la page qui doivent être traduits, y compris les liens de pied de page de l’entreprise. [block](block-add.md), la variable [message de bienvenue](../getting-started/storefront-branding.md#change-the-welcome-message), et [informations sur les produits](../stores-purchase/store-localize.md#localize-products).
