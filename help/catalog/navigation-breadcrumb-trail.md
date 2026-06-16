---
title: Chemins de navigation
description: Découvrez les différents modèles de piste de chemin de navigation et comment les configurer pour qu’ils apparaissent sur les pages de contenu et de catalogue.
exl-id: 2f60d48e-960f-437c-8f8f-a3d06cc0840a
feature: Catalog Management, Categories, Site Navigation, Page Content
TQID: https://experienceleague.adobe.com/v1hA4y0MmxxTtH3WbspqosZM1JMk4PMyhK1xeLxALOE
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fcid: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 394
ht-degree: 0%

---

# Chemins de navigation

Un _chemin de navigation_ est un ensemble de liens qui indique au client où il se trouve par rapport aux autres pages du magasin. Il peut cliquer sur n’importe quel lien du chemin de navigation pour revenir à la page précédente.

Le chemin de navigation peut être configuré pour s’afficher sur les pages de contenu et sur les pages de catalogue. Le format et la position du chemin de navigation varient selon le thème, mais il est généralement situé juste en dessous de l’en-tête. Par défaut, le chemin de navigation s’affiche sur les pages CMS.

![Chemin de navigation affiché dans le storefront](./assets/storefront-breadcrumb-trail.png){width="700" zoomable="yes"}

## Types généraux de miettes de pain

Les chemins de navigation peuvent être divisés en trois types principaux, qui diffèrent par leur fonction. L&#39;essence et les principes de base de la mise en œuvre de chaque type de miettes de pain sont décrits ci-dessous.

### Chemins de navigation basés sur une hiérarchie

Ce type de chemin de navigation est basé sur la hiérarchie de catégories configurée sur le site. Les chaînes présentées indiquent à l&#39;utilisateur où elles se trouvent dans la structure. Dans ce cas, chaque lien de texte est destiné à une page qui se trouve un niveau au-dessus de la précédente.

Exemple : `Men > Tops > Hoodies & Sweatshirts`

L’avantage de ce type est que les utilisateurs peuvent facilement voir à quel niveau de catégorie ils appartiennent et ont un accès facile à la navigation entre les pages du catalogue.

### Chemins de navigation basés sur l’historique

La navigation basée sur l’historique (ou le chemin) est similaire au bouton Précédent d’un navigateur. Ce type de navigation permet aux utilisateurs de revenir rapidement aux pages précédentes qu’ils ont visitées sans modification.

L’avantage de ce type est qu’il est particulièrement utile lorsque les clients souhaitent revenir à une page précédente après avoir sélectionné plusieurs filtres sur une page de catégorie.

Exemple : `Home > What's New > Gear > Bags`

### Chemins de navigation basés sur les attributs

Ce type de chemin de navigation affiche les attributs sélectionnés sur la page de catégorie. La principale différence par rapport aux autres types est que les chemins de navigation basés sur les attributs représentent les filtres et les options sélectionnés par le client dans la couche de navigation pour certains produits (tels que le prix, la qualité et la couleur).

Exemple : `Home > Suits > All Suits > Refined by > Slim Fit`

## Ajouter/supprimer des chemins de navigation des pages CMS

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche sous _[!UICONTROL General]_, choisissez **[!UICONTROL Web]**.

   ![Afficher le chemin de navigation pour les pages CMS](../configuration-reference/general/assets/web-default-pages.png){width="600" zoomable="yes"}

1. Développez la section _[!UICONTROL Default Pages]_.

1. Décochez la case **[!UICONTROL Use system value]** .

1. Définissez **[!UICONTROL Show Breadcrumbs for CMS Pages]** sur `No` ou `Yes`.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

>[!NOTE]
>
>La catégorie parent n’est pas affichée sur le chemin de navigation, sur la page de catégorie enfant, lorsqu’elle comporte les paramètres `Browsing Category`= `Deny` [autorisation de catégorie](category-permissions.md).
