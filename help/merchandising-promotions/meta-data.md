---
title: Données Meta
description: Découvrez comment saisir des métadonnées riches en mots-clés pour améliorer la manière dont les moteurs de recherche indexent votre site Commerce.
exl-id: 2acc1523-9da6-4e6f-8e4f-607603a61559
feature: Merchandising, Search
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 0%

---

# Données Meta

>[!TIP]
>
>Pour Adobe Commerce as a Cloud Service, consultez les [&#x200B; directives relatives aux métadonnées &#x200B;](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/metadata/?lang=fr) dans la documentation de Commerce Storefront

Votre boutique contient de nombreux emplacements où vous pouvez saisir des métadonnées riches en mots-clés afin d’améliorer la façon dont les moteurs de recherche indexent votre site. Lors de la configuration de votre boutique, vous pouvez saisir des métadonnées préliminaires, avec l’intention de les terminer ultérieurement. Au fil du temps, vous pouvez affiner les métadonnées pour cibler les schémas et les préférences d’achat de vos clients.

![Paramètres du produit - Optimisation du moteur de recherche](./assets/product-basic-settings-search-engine-optimization-yoga-strap.png){width="700" zoomable="yes"}

## Titre du Meta

Le méta-titre s’affiche dans la barre de titre et dans l’onglet de votre navigateur et dans les listes de résultats de recherche. Le méta-titre doit être propre à la page et comporter moins de 70 caractères.

![Exemple de storefront - méta-titre](./assets/storefront-home-page-meta-title.png){width="600"}

## Mots-clés Meta

Bien que certains moteurs de recherche ignorent les méta-mots-clés, d’autres continuent de les utiliser. La bonne pratique actuelle consiste à incorporer des mots-clés à forte valeur ajoutée au méta-titre et à la méta-description.

![Recherche dans un navigateur web - mots-clés méta](./assets/storefront-meta-description.png){width="500"}

## Description du Meta

Les descriptions de Meta donnent un bref aperçu de la page des résultats de recherche. Idéalement, une méta-description doit comporter entre 150 et 160 caractères, bien que le champ accepte jusqu’à 255 caractères.

## Fragments de code riches

Les fragments de code riches fournissent des informations détaillées pour les résultats de recherche et d’autres applications. Par défaut, le balisage de données structurées basé sur la norme [schema.org](https://schema.org/) est ajouté au modèle de produit de votre boutique. Par conséquent, les moteurs de recherche disposent de plus d’informations à inclure en tant que _fragments de code enrichis_ dans les listes de produits.

## Balise meta canonique

Certains moteurs de recherche pénalisent les sites web qui comportent plusieurs URL pointant vers le même contenu. La balise meta canonique indique aux moteurs de recherche la page à indexer lorsque plusieurs URL ont un contenu identique ou similaire. L’utilisation de la balise meta canonique peut améliorer le classement de votre site et agréger les pages vues. La balise de métadonnées canonique est placée dans le bloc `<head>` d’une page de produit ou de catégorie. Il fournit un lien vers l’URL de votre choix. Les moteurs de recherche lui donnent donc plus de poids.

### Exemple 1 : le chemin d’accès à la catégorie crée des URL en double

Par exemple, si votre catalogue est configuré pour inclure le chemin d’accès à la catégorie dans les URL de produit, votre boutique génère plusieurs URL qui pointent vers la même page de produit.

    http://mystore.com/gear/bags/driven-backpack.html
    http://mystore.com/driven-backpack.html

### Exemple 2 : URL complète de la page de catégorie

Lorsque les balises de métadonnées canoniques pour les catégories sont activées, la page de catégorie de votre magasin inclut une URL canonique vers l’URL de catégorie complète :

    http://mystore.com/gear/bags/

### Exemple 3 : URL complète de la page de produits

Lorsque les balises de métadonnées canoniques pour les produits sont activées, la page de produit inclut une URL canonique vers le nom de domaine/la clé d’URL de produit, car les clés d’URL de produit sont globalement uniques.

    http://mystore.com/driven-backpack.html

Si vous incluez également le chemin d’accès à la catégorie dans les URL de produit, l’URL canonique reste domain-name/product-url-key. Cependant, le produit est également accessible à l’aide de son URL complète, qui inclut la catégorie . Par exemple, si la clé URL du produit est `driven-backpack` et est affectée à la catégorie Engrenage > Sacs , le produit est accessible à l’aide de l’une des URL.

Vous pouvez éviter d’être pénalisé par les moteurs de recherche en omettant la catégorie de l’URL ou en utilisant la balise meta canonique pour diriger les moteurs de recherche vers l’index par produit ou catégorie. Il est recommandé d’activer les balises de métadonnées canoniques pour les catégories et les produits.

### Activation de la balise de métadonnées canonique

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en dessous.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **Optimisation du moteur de recherche**.

   Pour modifier les valeurs de champ, vous devez d’abord décocher la case **Utiliser la valeur système** après chaque champ.

   ![Configuration du catalogue - Optimisation du moteur de recherche](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Si vous souhaitez que les moteurs de recherche indexent uniquement les pages de catégorie à l’aide du chemin de catégorie complet, procédez comme suit :

   - Définissez **Utiliser la balise Meta de lien canonique pour les catégories** sur `Yes`.

   - Définissez **Utiliser la balise Meta de lien canonique pour les produits** sur `No`.

1. Si vous souhaitez que les moteurs de recherche indexent les pages de produits uniquement à l’aide du format nom-de-domaine/nom-de-produit-URL-clé, procédez comme suit :

   - Définissez **Utiliser la balise Meta de lien canonique pour les produits** sur `Yes`.

   - Définissez **Utiliser la balise Meta de lien canonique pour les catégories** sur `No`.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Démonstration des données Meta

Regardez cette vidéo pour en savoir plus sur la gestion des métadonnées d’optimisation du moteur de recherche :

>[!VIDEO](https://video.tv.adobe.com/v/3410174?captions=fre_fr&quality=12&learn=on)
