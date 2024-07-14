---
title: Configuration des images du produit
description: Découvrez comment définir une taille maximale en pixels (largeur et hauteur) et redimensionner automatiquement les fichiers image du produit lors du téléchargement.
exl-id: d8fce5f8-eddf-4335-9a72-24036db077db
feature: Catalog Management, Products, Media
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%

---

# Configuration des images du produit

Si vous prévoyez de télécharger des images volumineuses pour affichage sur la page _[!UICONTROL Product Details]_, vous pouvez définir une taille maximale en pixels (largeur et hauteur) et redimensionner automatiquement les fichiers lors du téléchargement. Pour prendre en charge ce type de chargement d’image de produit, il existe une option permettant d’activer le redimensionnement automatique des fichiers image plus volumineux au fur et à mesure du chargement. Pour les produits que vous souhaitez ajouter à votre catalogue mais que vous ne disposez pas encore d’une ressource image à afficher, vous pouvez configurer une image d’espace réservé.

## Redimensionnement des images du produit

Lors du téléchargement d’images de produit, vous pouvez ajouter des images plus grandes de tailles variées afin de fournir des zooms détaillés de haute qualité sur la page _[!UICONTROL Product Details]_. Pour vous assurer que toutes les images ont une taille et une apparence similaires, il existe une option de redimensionnement d’image afin de s’assurer que toutes les images correspondent à une taille de pixel spécifique. Cette option redimensionne automatiquement toutes les images de produit à l’aide des paramètres de configuration, ce qui peut vous aider à optimiser les performances du zoom, à accélérer le chargement des images et à uniformiser l’aspect des images de votre produit.

>[!NOTE]
>
>Pour une meilleure compatibilité, il est recommandé de télécharger toutes les images de produit avec le profil colorimétrique `sRGB`. Tous les autres profils colorimétriques sont automatiquement convertis dans le profil colorimétrique `sRGB` lors du chargement de l’image du produit, ce qui peut entraîner une incohérence des couleurs dans l’image chargée.

La définition d’une largeur et d’une hauteur maximales en pixels redimensionne l’image selon les dimensions physiques par pixel. Commerce redimensionne l’image en fonction de la largeur ou de la hauteur la plus élevée, tout en conservant les proportions. La réduction de la qualité des images de JPG réduit la taille du fichier.

Par exemple, un JPG de 3 000 x 2 100 pixels à 100 % peut correspondre à un fichier image de 5 Mo ou plus. Le redimensionnement de cette image réduirait la largeur à 1 920 pixels, en conservant les proportions et la qualité à 80 % afin de fournir un fichier beaucoup plus petit avec une qualité élevée.

### Activer le redimensionnement des images

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Advanced]** et choisissez **[!UICONTROL System]**.

1. Développez ![Développer le sélecteur](../assets/icon-display-expand.png) de la section _Configuration de téléchargement d’images_ .

   Pour modifier les paramètres par défaut, désélectionnez la case **[!UICONTROL Use system value]** si nécessaire.

   ![Configuration de téléchargement d’image](../configuration-reference/advanced/assets/system-image-upload-configuration.png){width="600" zoomable="yes"}

   Pour obtenir la liste détaillée de ces paramètres de configuration, voir [_Configuration du téléchargement d’images_](../configuration-reference/advanced/system.md#image-upload-configuration) dans la _référence de configuration_.

1. Pour l’activer, assurez-vous que **[!UICONTROL Enable Frontend Resize]** est défini sur `Yes`.

1. Saisissez un paramètre **[!UICONTROL Quality]** compris entre `1` et `100` %.

   Un paramètre compris entre 80 et 90 % est recommandé pour une taille de fichier réduite et une qualité élevée.

1. Définissez le **[!UICONTROL Maximum Width]** en pixels pour l’image.

   Lorsque l’image est redimensionnée, elle ne dépasse pas cette largeur et conserve des proportions.

1. Définissez le **[!UICONTROL Maximum Height]** en pixels pour l’image.

   Lorsque l’image est redimensionnée, elle ne dépasse pas cette hauteur et conserve des proportions.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

### Descriptions des champs

| Champ | [Portée](../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Quality] | Global | Détermine la qualité JPG de l’image redimensionnée. Une qualité inférieure réduit la taille du fichier. 80 à 90 % est recommandé pour réduire la taille du fichier avec une qualité élevée. Valeur par défaut : 80 |
| [!UICONTROL Enable Frontend Resize] | Global | Permet à Commerce de redimensionner les images volumineuses et surdimensionnées que vous pouvez télécharger pour la page _[!UICONTROL Product Details]_. Commerce redimensionne les fichiers image à l’aide de JavaScript lors du téléchargement du fichier. Lorsque l’image est redimensionnée, elle conserve les proportions exactes, pour respecter et ne pas dépasser la taille la plus grande pour Largeur maximale ou Hauteur maximale. Valeur par défaut : `Yes` |
| [!UICONTROL Maximum Width] | Global | Détermine la largeur maximale en pixels de l’image. Lorsque l’image est redimensionnée, elle ne dépasse pas cette largeur. Valeur par défaut : `1920` |
| [!UICONTROL Maximum Height] | Global | Détermine la hauteur maximale en pixels de l’image. Lorsque l’image est redimensionnée, elle ne dépasse pas cette hauteur. Valeur par défaut : `1200` |

{style="table-layout:auto"}

## Espaces réservés pour les images

Adobe Commerce et Magento Open Source utilisent des images temporaires comme espaces réservés jusqu’à ce que les images permanentes du produit soient disponibles. Un espace réservé différent peut être chargé pour chaque rôle. L’image d’espace réservé initial est un exemple de logo que vous pouvez remplacer par l’image de votre choix.

![Espace réservé de l’image](./assets/storefront-image-placeholder.png){width="600" zoomable="yes"}

**_Pour télécharger des images d’espace réservé :_**

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et sélectionnez **[!UICONTROL Catalog]** sous .

1. Développez ![Icône d’extension](../assets/icon-display-expand.png) de la section **[!UICONTROL Product Image Placeholders]** .

   ![Espace réservé de l’image du produit](../configuration-reference/catalog/assets/catalog-product-image-placeholders.png){width="600" zoomable="yes"}

   Pour obtenir la liste détaillée de ces paramètres de configuration, voir [_Espace réservé de l’image du produit_](../configuration-reference/catalog/catalog.md#product-image-placeholders) dans la _référence de configuration_.

1. Pour chaque rôle d’image, cliquez sur **[!UICONTROL Choose File]**, recherchez l’image sur votre ordinateur et téléchargez le fichier.

   Vous pouvez utiliser la même image pour les trois rôles ou télécharger une image d’espace réservé différente pour chaque rôle.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

Pour plus d’informations sur les rôles d’image et les tailles recommandées, voir [Téléchargement d’une image](product-image.md#upload-an-image).
