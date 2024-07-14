---
title: Navigation supérieure
description: Découvrez comment définir le menu principal d’un magasin, qui fonctionne comme un répertoire pour les différents services.
exl-id: 8b71fe73-2716-4820-9e57-4cb1e6888132
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 0%

---

# Navigation supérieure

Le menu principal de votre boutique est semblable à un répertoire pour les différents services de votre boutique. Chaque option représente une catégorie de produits différente. La position et la présentation de la navigation supérieure peuvent varier en fonction du thème, mais son fonctionnement est essentiellement le même.

![Navigation supérieure](./assets/storefront-top-navigation.png){width="700" zoomable="yes"}

La structure de catégorie de votre catalogue peut influencer la façon dont votre site est indexé par les moteurs de recherche. Plus une catégorie est imbriquée en profondeur, moins il est probable qu’elle soit complètement indexée. En règle générale, utiliser entre un et trois niveaux visibles est le plus efficace. La [catégorie racine](category-root.md) compte comme premier niveau, bien qu’elle n’apparaisse pas dans le menu. Le nombre maximal de niveaux disponibles dans la navigation supérieure est déterminé par la configuration. En outre, il peut y avoir une limite au nombre de niveaux de menu pris en charge par votre thème de magasin. Par exemple, l’exemple de thème Luma prend en charge jusqu’à cinq niveaux, y compris la racine.

## Comptage des niveaux de menu

| Élément | Description |
|--- |--- |
| Niveau 1 | Le premier niveau est la catégorie racine, qui dans l’exemple de données est appelée &quot;Catégorie par défaut&quot;. La racine est un conteneur pour le menu et son nom n’apparaît pas comme option dans le menu. |
| Niveau 2 | Sur un écran de bureau, la navigation supérieure est le menu principal qui s’affiche en haut de la page. Sur un appareil mobile, le menu principal s’affiche généralement sous la forme d’un menu déroulant d’options. Les options de deuxième niveau dans le magasin Luma sont _Nouveautés_, _Femmes_, _Hommes_, _Gear_, _Formation_ et _Vente_. |
| Niveau 3 | Le troisième niveau apparaît sous chaque option de menu principal. Par exemple, sous _Women_, les options de troisième niveau sont _Top_ et _Bottoms_. |
| Niveau 4 | Les options de quatrième niveau sont des sous-catégories qui sortent d’une option de troisième niveau. Par exemple, sous _Tops_, les options de menu de quatrième niveau sont _Jackets_, _Hoodies &amp; Sweatshirts_, _Tees_ et _Bras &amp; Tanks_. |

{style="table-layout:auto"}

## Définition de la navigation supérieure

Pour qu’une catégorie apparaisse dans le volet de navigation supérieur d’un magasin, procédez comme suit :

### Etape 1 : créer une catégorie

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Définissez un **[!UICONTROL Store View]** pour déterminer où la nouvelle catégorie doit être disponible.

1. Dans l&#39;arborescence des catégories, sélectionnez la catégorie parente de la nouvelle catégorie.

   Si vous commencez à partir du début sans aucune donnée, il peut y avoir seulement deux catégories dans la liste : _Catégorie par défaut_, qui est la racine, et une _catégorie d’exemple_.

1. Cliquez sur **[!UICONTROL Add Subcategory]**.

1. Renseignez les informations de base avec les paramètres suivants :

   - **[!UICONTROL Enable Category]** défini sur `Yes`
   - **[!UICONTROL Include in Menu]** défini sur `Yes`

1. Dans Paramètre d’affichage défini sur **[!UICONTROL Anchor]** sur `Yes`.

1. Renseignez tous les autres [paramètres de catégorie](category-create.md) requis.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

Pour une installation multi-magasin, un menu principal différent peut être affecté en tant que [catégorie racine](category-root.md) pour chaque [magasin](../stores-purchase/stores.md#add-stores).

### Étape 2 : définition de la profondeur de la navigation supérieure

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et sélectionnez **[!UICONTROL Catalog]** sous .

1. Développez la section **[!UICONTROL Category Top Navigation]** .

   ![Navigation supérieure des catégories](../configuration-reference/catalog/assets/catalog-category-top-navigation.png){width="600" zoomable="yes"}

   La profondeur de la navigation supérieure ayant une [portée de configuration](../getting-started/websites-stores-views.md#scope-settings) globale, le paramètre s’applique à tous les sites web, magasins et vues de magasin dans l’installation Commerce. La section de configuration _[!UICONTROL Category Top Navigation]_est disponible uniquement lorsque_[!UICONTROL Store View]_ dans le coin supérieur gauche est défini sur `Default Config`.

   Pour obtenir une liste détaillée de ces options, reportez-vous à la section [Navigation supérieure des catégories](../configuration-reference/catalog/catalog.md#layered-navigation) dans la _Référence de configuration_.

1. Pour limiter le nombre de sous-catégories qui apparaissent dans le volet de navigation supérieur, saisissez le nombre **[!UICONTROL Maximal Depth]**.

   La valeur par défaut est `0`, ce qui ne limite pas le nombre de niveaux de sous-catégorie.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
