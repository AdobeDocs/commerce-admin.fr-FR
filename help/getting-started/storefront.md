---
title: Qu'est-ce que la vitrine ?
description: Découvrez les pages et les éléments fonctionnels que votre boutique peut fournir pour prendre en charge l’expérience d’achat pour vos clients.
exl-id: 1c64888f-2bc0-4e2e-b7da-0e7182ea67e0
feature: Storefront
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '776'
ht-degree: 0%

---

# Qu&#39;est-ce que la vitrine ?

Dans votre mise en oeuvre Adobe Commerce ou Magento Open Source, le storefront est la partie externe destinée au public de votre magasin. Il fournit le contenu et les composants fonctionnels que vos clients utilisent pour acheter et acheter.

Le chemin que les clients empruntent à une vente est parfois appelé _chemin d’accès à l’achat_, et votre storefront comprend les composants permettant aux clients de suivre ce chemin. Les sections suivantes présentent un aperçu des types de page de base qui apportent une valeur stratégique : les endroits où les clients visitent généralement votre boutique. À mesure que vous les examinez, tenez compte de différentes fonctionnalités de magasin qui peuvent être utilisées à chaque étape du parcours client.

## Page d’accueil

Saviez-vous que la plupart des gens ne passent que quelques secondes sur une page avant de décider de rester ou d&#39;aller ailleurs ? Il n&#39;est pas long de faire impression. Des études montrent que les gens aiment aussi les photos, surtout d&#39;autres personnes. Quelle que soit la conception choisie, tout ce qui se trouve sur votre page d’accueil doit orienter les visiteurs vers l’étape suivante du processus de vente. L&#39;idée est de guider leur attention dans un flux cohérent d&#39;un point ciblé à l&#39;autre.

![Exemple de page d’accueil storefront](./assets/storefront-homepage-full.png){width="700"}

## Page Catalogue

Les listes de pages de catalogue comportent généralement de petites images de produits et de brèves descriptions et peuvent être formatées sous la forme d’une liste ou d’une grille. Vous pouvez ajouter des blocs, des vidéos et des descriptions riches en mots-clés, ainsi que créer des conceptions spéciales pour une promotion ou une saison. Vous pouvez créer une catégorie spéciale pour présenter un style de vie ou une marque qui est une collection organisée de produits de différentes catégories.

La description initiale du produit donne généralement aux acheteurs suffisamment d’informations pour qu’ils y regardent de plus près. Les personnes qui savent ce qu’elles veulent peuvent ajouter le produit à leur panier et y aller. Les clients qui font leurs achats en se connectant à leurs comptes bénéficient d’une expérience d’achat personnalisée.

![Page de collection sur le storefront](./assets/storefront-collection-page.png){width="700"}

## Résultats de la recherche

Saviez-vous que les personnes qui utilisent la recherche ont presque deux fois plus de chances de faire un achat que les personnes qui ne dépendent que de la navigation ? Vous pouvez considérer ces acheteurs comme _pré-qualifié_.

### [!DNL Live Search]

Avec [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) pour Adobe Commerce, votre boutique offre une expérience de recherche rapide, super pertinente et intuitive. Elle est disponible gratuitement pour Adobe Commerce.

![Exemple de recherche en direct : effectuez une recherche en cours de frappe](./assets/storefront-search-as-you-type.png){width="700"}

### Recherche catalogue standard

Avec [recherche catalogue standard](../catalog/search.md), votre boutique comprend une zone de recherche dans le coin supérieur droit et un lien vers la recherche avancée dans le pied de page. Tous les termes de recherche envoyés par les acheteurs sont enregistrés afin que vous puissiez voir exactement ce qu’ils recherchent. Vous pouvez proposer des suggestions et saisir des synonymes et des fautes d’orthographe courantes. Affichez ensuite une page spécifique lorsqu’un terme de recherche est saisi.

![Exemple de résultats de recherche catalogue standard](./assets/storefront-search-results-page-full.png){width="700"}

## Page de produit

La page produit a beaucoup de choses en cours ! La première chose qui attire votre attention sur la page du produit est l’image principale avec un zoom haute résolution et une galerie de miniatures. Outre le prix et la disponibilité, une section avec onglets contient des informations supplémentaires et une liste des produits associés.

![Exemple de page de produit storefront](./assets/storefront-product-page-full-m.png){width="700"}

## Panier

Le panier est l’endroit où le total de la commande peut être déterminé, ainsi que les coupons de réduction et l’estimation de l’expédition et de la taxe, et un endroit idéal pour afficher vos badges et sceaux de confiance. C&#39;est aussi une opportunité idéale pour proposer un dernier élément. En tant que vente croisée, vous pouvez sélectionner certains articles à proposer comme impulsion d’achat chaque fois qu’un article spécifique apparaît dans le panier.

![Exemple de page de panier storefront](./assets/storefront-cart-full.png){width="700"}

## Page Passage en caisse

Le processus de passage en caisse comprend deux étapes :

1. Informations d’expédition

   La première étape du processus de passage en caisse est que le client remplisse les informations d’adresse de livraison et choisisse le mode de livraison. Si le client dispose d’un compte, l’adresse de livraison est saisie automatiquement, mais peut être modifiée si nécessaire.

   ![Exemple de page de paiement storefront](./assets/storefront-checkout-shipping-full.png){width="700"}

1. Informations de révision et de paiement

   La deuxième étape du processus de passage en caisse est que le client choisisse le mode de paiement et applique éventuellement un code de remise.

   >[!NOTE]
   >
   >Bien que [!DNL Commerce] permet de configurer plusieurs codes de bon. un client ne peut appliquer qu’un seul code de bon au panier. (Voir [Codes de coupon](../merchandising-promotions/price-rules-cart-coupon.md#coupon-codes) pour plus d’informations.)

   ![Exemple de page de paiement storefront](./assets/storefront-checkout-payment-full.png){width="700"}

La barre de progression située en haut de la page suit chaque étape du processus de passage en caisse et la variable _Synthèse des commandes_ affiche les informations qui ont été saisies jusqu’à ce point.

>[!NOTE]
>
>L’exception à la règle du paiement en deux étapes s’applique aux produits virtuels et/ou téléchargeables. S’il n’existe que ces types de produits dans le panier, le passage en caisse est automatiquement transformé en procédure à une étape, car les informations d’expédition ne sont pas requises.
