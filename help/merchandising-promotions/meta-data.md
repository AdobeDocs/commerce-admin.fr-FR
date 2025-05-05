---
title: Métadonnées
description: Découvrez comment entrer des métadonnées riches en mots-clés pour améliorer la façon dont les moteurs de recherche indexent votre site Commerce.
exl-id: 2acc1523-9da6-4e6f-8e4f-607603a61559
feature: Merchandising, Search
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---

# Métadonnées

Votre magasin est chargé avec des emplacements où vous pouvez entrer des métadonnées riches en mots-clés afin d’améliorer la façon dont les moteurs de recherche indexent votre site. Lors de la configuration de votre magasin, vous pouvez saisir des métadonnées préliminaires afin de les terminer ultérieurement. Au fil du temps, vous pouvez affiner les métadonnées afin de cibler les schémas d’achat et les préférences de vos clients.

![ Paramètres du produit - optimisation du moteur de recherche](./assets/product-basic-settings-search-engine-optimization-yoga-strap.png){width="700" zoomable="yes"}

## Titre du méta

Le titre du méta apparaît dans la barre de titre et l’onglet de votre navigateur et dans les listes de résultats de recherche. Le titre du méta doit être propre à la page et contenir moins de 70 caractères.

![Exemple de storefront - meta title](./assets/storefront-home-page-meta-title.png){width="600"}

## Mots-clés des métadonnées

Bien que certains moteurs de recherche ignorent les méta-mots-clés, d’autres continuent de les utiliser. La bonne pratique actuelle consiste à incorporer des mots-clés à valeur élevée dans le méta-titre et la méta-description.

![Recherche de navigateur web - méta-mots-clés](./assets/storefront-meta-description.png){width="500"}

## Description des métadonnées

Les métadonnées fournissent un bref aperçu de la page pour les listes de résultats de recherche. Idéalement, une méta-description doit comporter entre 150 et 160 caractères, bien que le champ accepte jusqu’à 255 caractères.

## Fragments de code riches

Les fragments de code enrichis fournissent des informations détaillées sur les listes de résultats de recherche et d’autres applications. Par défaut, le balisage de données structuré basé sur la norme [schema.org][1] est ajouté au modèle de produit de votre magasin. Par conséquent, des informations supplémentaires sont disponibles pour que les moteurs de recherche puissent inclure des _fragments de code riches_ dans les listes de produits.

## Balise méta canonique

Certains moteurs de recherche pénalisent les sites web comportant plusieurs URL pointant vers le même contenu. La balise méta canonique indique aux moteurs de recherche quelle page indexer lorsque plusieurs URL ont un contenu identique ou similaire. L’utilisation de la balise meta canonique peut améliorer le classement de votre site et agréger les pages vues. La balise méta canonique est placée dans le bloc `<head>` d’une page de produit ou de catégorie. Il fournit un lien vers votre URL préférée, de sorte que les moteurs de recherche lui donnent plus de poids.

### Exemple 1 : un chemin d’accès de catégorie crée des URL en double

Par exemple, si votre catalogue est configuré pour inclure le chemin de catégorie dans les URL de produit, votre boutique génère plusieurs URL qui pointent vers la même page de produit.

    http://mystore.com/gear/bags/driven-backpack.html
    http://mystore.com/driven-backpack.html

### Exemple 2 : URL complète de la page de catégorie

Lorsque les balises META canoniques des catégories sont activées, la page de catégorie de votre magasin comprend une URL canonique vers l’URL de catégorie complète :

    http://mystore.com/gear/bags/

### Exemple 3 : URL complète de la page de produit

Lorsque les balises META canoniques des produits sont activées, la page de produit inclut une URL canonique au nom de domaine/product-url-key, car les clés URL du produit sont globalement uniques.

    http://mystore.com/driven-backpack.html

Si vous incluez également le chemin de catégorie dans les URL de produit, l’URL canonique reste domain-name/product-url-key. Cependant, le produit est également accessible à l’aide de son URL complète, qui inclut la catégorie . Par exemple, si la clé d’URL du produit est `driven-backpack` et est affectée à la catégorie Engrenage > Balises , l’accès au produit est possible à l’aide de l’une des URL.

Vous pouvez éviter d’être pénalisé par les moteurs de recherche en omettant la catégorie de l’URL ou en utilisant la balise meta canonique pour diriger les moteurs de recherche vers un index par produit ou catégorie. Il est recommandé d’activer les balises méta canoniques pour les catégories et les produits.

### Activation de la balise meta canonique

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et sélectionnez **[!UICONTROL Catalog]** sous .

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) de **Optimisation du moteur de recherche** .

   Pour modifier des valeurs de champ, vous devez d’abord décocher la case **Utiliser la valeur système** après chaque champ.

   ![Configuration du catalogue - optimisation du moteur de recherche](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Si vous souhaitez que les moteurs de recherche indexent uniquement les pages de catégorie à l’aide du chemin de catégorie complet, procédez comme suit :

   - Définissez **sur `Yes` l’utilisation de la balise Métadonnées de lien canonique pour les catégories**.

   - Définissez **sur `No` l’option Utiliser la méta-balise de lien canonique pour les produits**.

1. Si vous souhaitez que les moteurs de recherche indexent les pages de produits uniquement au format domain-name/product-url-key , procédez comme suit :

   - Définissez **sur `Yes` l’option Utiliser la méta-balise de lien canonique pour les produits**.

   - Définissez **sur `No` l’utilisation de la balise Métadonnées de lien canonique pour les catégories**.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

## Démonstration des métadonnées

Regardez cette vidéo pour en savoir plus sur la gestion des métadonnées d’optimisation pour les moteurs de recherche :

>[!VIDEO](https://video.tv.adobe.com/v/3410174?quality=12&learn=on&captions=fre_fr)

[1]: https://schema.org/
