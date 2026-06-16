---
title: Listes de produits
description: Découvrez comment modifier la configuration de la liste de produits, qui détermine le nombre de produits qui apparaissent par page et l’attribut utilisé pour trier la liste.
exl-id: 3779d9db-4adb-473b-b9c9-ad066f50b549
feature: Catalog Management, Products, Page Content
TQID: https://experienceleague.adobe.com/XC4xwHkJyLCiHNNCAz6huVbN3j-WwCvKumJtjf0uj-I
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: ae62cf09-5996-4921-bda8-fbe67b62e470
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 792
ht-degree: 0%

---

# Listes de produits

Les listes de produits peuvent être définies pour apparaître par défaut sous la forme d’une liste ou d’une grille. Vous pouvez également déterminer le nombre de produits qui s’affichent par page et l’attribut utilisé pour trier la liste. La liste de produits comprend un ensemble de commandes qui peuvent être utilisées pour trier les produits, modifier le format de la liste, trier par attribut et passer d’une page à l’autre.

>[!NOTE]
>
>Lors du tri d’une catégorie par attribut de produit, les produits ayant les mêmes valeurs d’attribut sont également triés en fonction de leur _[!UICONTROL Product ID]_&#x200B;dans l’ordre croissant.

![Produits affichés sous forme de grille](./assets/storefront-catalog-page.png){width="700" zoomable="yes"}

## Configurer les listes de produits

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Catalog]** en dessous.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Storefront]** .

   ![Options de configuration de Storefront](../configuration-reference/catalog/assets/catalog-storefront.png){width="600" zoomable="yes"}

   Pour obtenir la liste détaillée de ces options, voir [Storefront](../configuration-reference/catalog/catalog.md#storefront) dans le _Guide de référence de configuration_.

   >[!NOTE]
   >
   >Pour afficher correctement les produits et leurs prix en fonction du _tri des produits par prix_, assurez-vous que les paramètres d&#39;affichage des prix dans le [paramétrage de la taxe](../configuration-reference/sales/tax.md) ont la même valeur (`Excluding Tax` **ou** `Including Tax`). Pour l’_[!UICONTROL Calculation Settings]_, vérifiez la valeur **[!UICONTROL Catalog Prices]**. Et pour&#x200B;_[!UICONTROL Price Display Settings]_, vérifiez la valeur **[!UICONTROL Display Product Prices in Catalog]** . Si elles ont des valeurs différentes, les filtres de prix dans la navigation superposée peuvent ne pas filtrer et trier correctement les produits par prix.

1. Définissez la **[!UICONTROL List Mode]** par défaut sur l’une des valeurs suivantes :

   - `Grid Only`
   - `List Only`
   - `Grid (default) / List`
   - `List (default / Grid`

1. Par **[!UICONTROL Products per Page on Grid Allowed Values]**, saisissez le nombre de produits que vous souhaitez afficher par page lorsqu’ils sont affichés au format grille.

   Pour saisir une sélection de valeurs, séparez chaque nombre par une virgule.

1. Par **[!UICONTROL Products per Page on Grid Default Value]**, saisissez le nombre de produits par défaut à afficher dans la grille par page.

1. Par **[!UICONTROL Products per Page on List Allowed Values]**, saisissez le nombre de produits qui doivent apparaître par page lorsqu’ils sont affichés sous forme de liste.

   Pour saisir une sélection de valeurs, séparez chaque nombre par une virgule.

1. Par **[!UICONTROL Products per page on List Default Value]**, saisissez le nombre par défaut de produits qui apparaissent dans la liste, par page.

1. Définissez **[!UICONTROL Product Listing Sorted by]** sur l’attribut par défaut initialement utilisé pour trier la liste.

1. Pour permettre aux clients de répertorier tous les produits, définissez **[!UICONTROL Allow All Products on Page]** sur `Yes`.

1. Si vous souhaitez conserver tous les paramètres de pagination lorsque les clients parcourent les listes de catalogue, définissez **[!UICONTROL Remember Category Pagination]** sur `Yes`.

   L’activation de ce paramètre garantit que le nombre de produits affichés dans une liste ou une grille est conservé lorsque les acheteurs passent d’une catégorie à une autre. Par défaut, ce champ est défini sur `No`, car il utilise davantage d’espace de stockage en cache et peut avoir un impact sur la façon dont les pages sont indexées par les moteurs de recherche.

1. Si vous utilisez un [catalogue plat](catalog-flat.md) (**non recommandé**), procédez comme suit :

   - Pour afficher une liste de catégories de produits plate, définissez **[!UICONTROL Use Flat Catalog Category]** sur `Yes`.

   - Pour afficher une liste de produits plate, définissez **[!UICONTROL Use Flat Catalog Product]** sur `Yes`.

1. Si vous souhaitez autoriser les références dynamiques pour les ressources multimédias dans les URL de catégorie et de produit, définissez **[!UICONTROL Allow Dynamic Media URLs in Products and Categories]** sur `Yes`.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Contrôles de page

| Contrôle | Description |
|--- |--- |
| [!UICONTROL View As] | Affiche les produits au format grille ou liste. |
| [!UICONTROL Sort By] | Modifie l’ordre de tri de la liste. |
| [!UICONTROL Show Per Page] | Détermine le nombre de produits qui s’affichent par page. |
| Liens de pagination | Liens de navigation vers d’autres pages. |

{style="table-layout:auto"}

## Contrôles de pagination

Les paramètres de pagination apparaissent en haut et en bas de la liste et contrôlent le format des liens de pagination pour les listes de produits. Vous pouvez définir le nombre de liens qui apparaissent dans le contrôle et configurer les liens Suivant et Précédent. Pour que les liens de pagination s’affichent, la liste doit contenir plus de produits que le nombre autorisé par page dans la configuration de la liste de produits.

![&#x200B; Contrôles de pagination &#x200B;](./assets/storefront-pagination-controls.png){width="700" zoomable="yes"}

### Contrôles de pagination de Storefront

| Contrôle | Description |
|--- |--- |
| ![Afficher la grille](./assets/controls-pagination-list-grid.png) | [!UICONTROL View As] - Affiche la liste au format Grille ou Liste. |
| ![Trier par](./assets/control-pagination-sort-by.png) | [!UICONTROL Sort By] - Modifie l’ordre de tri de la liste. La propriété storefront _[!UICONTROL Used for Sorting in Product Listing]_&#x200B;détermine les [attributs de produit](../catalog/product-attributes.md) qui peuvent être utilisés pour trier la liste. |
| ![Afficher par page](./assets/control-pagination-show-per-page.png) | [!UICONTROL Show Per Page] - Détermine le nombre de produits qui s’affichent par page. |
| ![&#x200B; Liens de pagination &#x200B;](./assets/control-pagination.png) | Liens de pagination : liens de navigation vers d’autres pages. |

{style="table-layout:auto"}

### Configuration des contrôles de pagination

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Recherchez la vue de magasin à configurer et, dans la colonne **[!UICONTROL Action]**, cliquez sur **[!UICONTROL Edit]**.

1. Sous **[!UICONTROL Other Settings]**, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Pagination]** .

   ![&#x200B; Pagination &#x200B;](./assets/config-design-pagination.png){width="600" zoomable="yes"}

   Pour plus d’informations sur ces paramètres, voir [Configuration de la conception](../content-design/configuration.md).

1. Par **[!UICONTROL Pagination Frame]**, saisissez le nombre de liens qui doivent apparaître dans le contrôle de pagination.

1. Par **[!UICONTROL Pagination Frame Skip]**, saisissez le nombre de liens que vous souhaitez ignorer avant d’afficher le prochain ensemble de liens dans le contrôle de pagination.

   Par exemple, si le cadre de pagination comporte cinq liens et que vous souhaitez passer aux cinq liens suivants, combien de liens voulez-vous ignorer ? Si vous définissez la valeur sur quatre (`4`), le dernier lien du jeu précédent est le premier lien du jeu suivant.

1. Par **[!UICONTROL Anchor Text for Previous]**, saisissez le texte que vous souhaitez afficher pour le lien Précédent .

   Laissez vide pour utiliser la flèche par défaut.

1. Par **[!UICONTROL Anchor Text for Next]**, saisissez le texte que vous souhaitez afficher pour le lien Suivant. Laissez vide pour utiliser la flèche par défaut.

1. Cliquez ensuite sur **[!UICONTROL Save Configuration]**.
