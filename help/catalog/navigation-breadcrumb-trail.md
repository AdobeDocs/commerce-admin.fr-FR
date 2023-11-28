---
title: Chemins de navigation
description: Découvrez les différents schémas de cheminement de navigation et comment les configurer pour apparaître sur les pages de contenu et de catalogue.
exl-id: 2f60d48e-960f-437c-8f8f-a3d06cc0840a
feature: Catalog Management, Categories, Site Navigation, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Chemins de navigation

A _cheminement de navigation_ est un ensemble de liens qui indique au client où il se trouve par rapport à d’autres pages du magasin. Ils peuvent cliquer sur n’importe quel lien du chemin de navigation pour revenir à la page précédente.

Le chemin de navigation peut être configuré pour s’afficher sur les pages de contenu et sur les pages de catalogue. Le format et la position du chemin de navigation varient selon le thème, mais il se trouve généralement juste sous l’en-tête . Par défaut, le chemin de navigation s’affiche sur les pages CMS.

![Chemin de navigation affiché dans le storefront](./assets/storefront-breadcrumb-trail.png){width="700" zoomable="yes"}

## Types généraux de miettes à pain

Les chemins de navigation peuvent être divisés en trois types principaux, dont l’objet diffère. L’essence et les principes de base de la mise en oeuvre de chaque type de miettes à pain sont décrits ci-dessous.

### Chemin de navigation basé sur la hiérarchie

Ce type de chemin de navigation est basé sur la hiérarchie de catégories configurée sur le site. Les chaînes présentées indiquent à l&#39;utilisateur où elles se trouvent dans la structure. Dans ce cas, chaque lien texte est destiné à une page dont le niveau est supérieur à celui de la page précédente.

Exemple : `Men > Tops > Hoodies & Sweatshirts`

L’avantage de ce type est que les utilisateurs peuvent facilement voir dans quel niveau de catégorie ils se trouvent et avoir un accès facile à la navigation entre les pages du catalogue.

### Chemins de navigation basés sur l’historique

La navigation basée sur l’historique (ou chemin d’accès) est similaire au bouton Précédent d’un navigateur. Ce type de navigation permet aux utilisateurs de revenir rapidement aux pages précédentes visitées sans modification.

L’avantage de ce type de filtres est qu’il s’avère particulièrement utile lorsque les clients souhaitent revenir à une page précédente après avoir sélectionné plusieurs filtres sur une page de catégorie.

Exemple : `Home > What's New > Gear > Bags`

### Chemin de navigation basé sur les attributs

Ce type de chemin de navigation affiche les attributs sélectionnés sur la page de catégorie. La principale différence par rapport aux autres types réside dans le fait que les chemins de navigation basés sur les attributs représentent les filtres et options sélectionnés par le client dans la couche de navigation pour certains produits (prix, qualité et couleur, par exemple).

Exemple : `Home > Suits > All Suits > Refined by > Slim Fit`

## Ajout/suppression du chemin de navigation des pages CMS

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, sous _[!UICONTROL General]_, choisissez **[!UICONTROL Web]**.

   ![Afficher le chemin de navigation des pages CMS](../configuration-reference/general/assets/web-default-pages.png){width="600" zoomable="yes"}

1. Développez l’objet _[!UICONTROL Default Pages]_.

1. Désélectionnez l’option **[!UICONTROL Use system value]** .

1. Définir **[!UICONTROL Show Breadcrumbs for CMS Pages]** to `No` ou `Yes`.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

>[!NOTE]
>
>La catégorie parente n’est pas affichée dans le rail de chemin de navigation, sur la page de catégorie enfant, lorsqu’elle comporte `Browsing Category`= `Deny` [autorisation de catégorie](category-permissions.md) paramètres.
