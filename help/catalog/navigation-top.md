---
title: Volet de navigation supérieur
description: Découvrez comment définir le menu principal d’un magasin, qui fonctionne comme un répertoire pour les différents services.
exl-id: 8b71fe73-2716-4820-9e57-4cb1e6888132
feature: Catalog Management, Categories, Site Navigation
TQID: https://experienceleague.adobe.com/REad4AtBdJeK2eVNRo1XiTrrjJqmTs6oJfum260IfOk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: c18ed297-2187-4aec-affb-9d9654eca6fcid: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 581
ht-degree: 0%

---

# Volet de navigation supérieur

Le menu principal de votre boutique est comme un répertoire des différents services de votre boutique. Chaque option représente une catégorie de produits différente. La position et la présentation de la barre de navigation supérieure peuvent varier en fonction du thème, mais son fonctionnement est essentiellement le même.

![Navigation supérieure](./assets/storefront-top-navigation.png){width="700" zoomable="yes"}

La structure des catégories de votre catalogue peut influencer la qualité de l’indexation de votre site par les moteurs de recherche. Plus une catégorie est imbriquée profondément, moins elle a de chances d’être complètement indexée. Généralement, utiliser entre un et trois niveaux visibles est le plus efficace. La [catégorie racine](category-root.md) compte comme le premier niveau, bien qu&#39;elle n&#39;apparaisse pas dans le menu. Le nombre maximal de niveaux disponibles dans la barre de navigation supérieure est déterminé par la configuration. En outre, il peut y avoir une limite au nombre de niveaux de menu pris en charge par le thème de votre boutique. Par exemple, l’exemple de thème Luma prend en charge jusqu’à cinq niveaux, racine incluse.

## Comptage des niveaux de menu

| Poste | Description |
|--- |--- |
| Niveau 1 | Le premier niveau est la catégorie racine, qui dans les données d’exemple est nommée « Catégorie par défaut ». La racine est un conteneur pour le menu et son nom n’apparaît pas en tant qu’option dans le menu. |
| Niveau 2 | Sur un écran de bureau, le menu de navigation supérieur est le menu principal qui s’affiche en haut de la page. Sur un appareil mobile, le menu principal s’affiche généralement sous la forme d’un menu déroulant d’options. Les options de deuxième niveau de la boutique Luma sont _Nouveautés_, _Femmes_, _Hommes_, _Équipement_, _Formation_ et _Vente_. |
| Niveau 3 | Le troisième niveau apparaît sous chaque option de menu principal. Par exemple, sous _Femmes_, les options de troisième niveau sont _Haut_ et _Bas_. |
| Niveau 4 | Les options de quatrième niveau sont des sous-catégories qui partent d’une option de troisième niveau. Par exemple, sous _Tops_, les options de menu de quatrième niveau sont _Vestes_, _Hoodies &amp; Sweatshirts_, _Tees_ et _Bras &amp; Tanks_. |

{style="table-layout:auto"}

## Définir la barre de navigation supérieure

Pour qu’une catégorie apparaisse dans le volet de navigation supérieur d’un magasin, procédez comme suit :

### Étape 1 : créer une catégorie

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Définissez une **[!UICONTROL Store View]** pour déterminer où la nouvelle catégorie doit être disponible.

1. Dans l’arborescence des catégories, sélectionnez la catégorie parent de la nouvelle catégorie.

   Si vous commencez sans données, il se peut que la liste ne contienne que deux catégories : _Catégorie par défaut_, qui est la racine, et une _Catégorie d’exemple_.

1. Cliquez sur **[!UICONTROL Add Subcategory]**.

1. Renseignez les informations de base avec les paramètres suivants :

   - **[!UICONTROL Enable Category]** défini sur `Yes`
   - **[!UICONTROL Include in Menu]** défini sur `Yes`

1. Dans le paramètre d’affichage , définissez **[!UICONTROL Anchor]** sur `Yes`.

1. Renseignez tous les autres [paramètres de catégorie](category-create.md) requis.

1. Cliquez ensuite sur **[!UICONTROL Save]**.

Pour une installation multi-magasin, un menu principal différent peut être affecté en tant que [catégorie racine](category-root.md) pour chaque [magasin](../stores-purchase/stores.md#add-stores).

### Étape 2 : définir la profondeur de la navigation supérieure

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en dessous.

1. Développez la section **[!UICONTROL Category Top Navigation]** .

   ![Navigation supérieure de catégorie](../configuration-reference/catalog/assets/catalog-category-top-navigation.png){width="600" zoomable="yes"}

   Comme la profondeur de la navigation supérieure a une portée globale [configuration](../getting-started/websites-stores-views.md#scope-settings), le paramètre s’applique à tous les sites web, magasins et vues de magasin dans l’installation de Commerce. La section Configuration du _[!UICONTROL Category Top Navigation]_n’est disponible que lorsque la_[!UICONTROL Store View]_ dans le coin supérieur gauche est définie sur `Default Config`.

   Pour obtenir la liste détaillée de ces options, voir [Navigation supérieure de catégorie](../configuration-reference/catalog/catalog.md#layered-navigation) dans le _Guide de référence de configuration_.

1. Pour limiter le nombre de sous-catégories qui apparaissent dans le volet de navigation supérieur, saisissez le nombre de **[!UICONTROL Maximal Depth]**.

   La valeur par défaut est `0`, ce qui ne limite pas le nombre de niveaux de sous-catégorie.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
