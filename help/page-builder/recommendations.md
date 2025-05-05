---
title: Ajouter du contenu - Recommandations de produits
description: Découvrez le type de contenu des recommandations de produits , utilisé pour ajouter une liste de recommandations à l’étape [!DNL Page Builder] du.
exl-id: ca90c10d-8d7a-42a2-bb13-2602aa9d6eef
feature: Page Builder, Page Content, Recommendations
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 0%

---

# Ajouter du contenu - Recommandations de produits

Utilisez le type de contenu _Recommandations de produits_ pour ajouter une [unité de recommandation](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/admin/create) active existante à l’[[!DNL Page Builder] étape](workspace.md#stage) pour une page, un bloc ou un bloc dynamique CMS.

>[!NOTE]
>
>Le type de contenu [!DNL Page Builder] _Product Recommendations_ est pris en charge dans Adobe Commerce version 2.4.4 et ultérieure et disponible dans le métapaquet [Product Recommendations version 3.0.x ou ultérieure](https://commercemarketplace.adobe.com/magento-product-recommendations.html). Pour ajouter [!DNL Page Builder] prise en charge des recommandations de produits, [voir les informations d’installation](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/getting-started/install-configure). **Ce type de contenu n’est pas disponible pour Magento Open Source.**

{{$include /help/_includes/page-builder-save-timeout.md}}

## Boîte à outils de recommandations de produits

| Outil | Icon | Description |
| --- | --| --- |
| Déplacer | ![ Icône Déplacer ](./assets/pb-icon-move.png){width="25"} | Déplace le conteneur de recommandations de produits et son contenu vers une autre position sur la scène. |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} | Ouvre la page Modifier la recommandation de produit, qui vous permet de choisir l’unité de recommandation et de modifier les propriétés du conteneur. |
| Masquer | ![Icône Masquer](./assets/pb-icon-hide.png){width="25"} | Masque le conteneur de recommandations de produits actuel et son contenu. |
| Afficher | ![Afficher l’icône](./assets/pb-icon-show.png){width="25"} | Affiche le conteneur de recommandations de produits masqué et son contenu. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="25"} | Effectue une copie en double du conteneur de recommandations de produits et de son contenu. |
| Supprimer | ![Icône Supprimer](./assets/pb-icon-remove.png){width="25"} | Supprime le conteneur de recommandations de produits et son contenu de l’étape. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Ajouter une unité de recommandation existante

1. Assurez-vous d’avoir déjà [créé une unité de recommandation](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/admin/create) pour le type de page [!DNL Page Builder].

>[!NOTE]
>
>Vous ne pouvez créer des unités de recommandation pour le type de page [!DNL Page Builder] que dans la vue de magasin par défaut.

1. Ouvrez la page, le bloc ou le bloc dynamique en mode d’édition.

1. Développez la section _[!UICONTROL Content]_&#x200B;et cliquez sur **[!UICONTROL Edit with Page Builder]**&#x200B;ou dans la zone d’aperçu du contenu pour ouvrir l’espace de travail [!DNL Page Builder].

1. Dans le panneau [!DNL Page Builder] sous _[!UICONTROL Layout]_, faites glisser un espace réservé&#x200B;**[!UICONTROL Row]**&#x200B;vers la scène.

1. Dans le panneau [!DNL Page Builder] sous _[!UICONTROL Add Content]_, faites glisser un espace réservé&#x200B;**[!UICONTROL Product Recommendation]**&#x200B;jusqu’à la ligne.

   ![Ajout du type de contenu de recommandation de produit](./assets/pb-add-prex-drag.png){width="600" zoomable="yes"}

1. Effectuez l’une des opérations suivantes :

   - Cliquez sur **[!UICONTROL Edit Product Recommendation]**.
   - Pointez sur le conteneur vide pour afficher la boîte à outils et cliquez sur l’icône _Paramètres_ (![icône Paramètres](./assets/pb-icon-settings.png)).

   ![Modifier la recommandation de produit](./assets/pb-prex-toolbox.png){width="600" zoomable="yes"}

1. Dans la section _[!UICONTROL Selection]_, cliquez sur **[!UICONTROL Select]**.

1. Dans la liste des recommandations de produits actives, recherchez la ligne contenant l’unité de recommandation à ajouter, puis cliquez sur **[!UICONTROL Select]** dans la dernière colonne.

   ![Recommandation de produit sélectionnée](./assets/pb-prex-select.png){width="600" zoomable="yes"}

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Selected]**.

   Le nom de la recommandation de produit sélectionnée s’affiche dans la section _[!UICONTROL Selection]_&#x200B;de la page&#x200B;_[!UICONTROL Edit Product Recommendation]_.

1. Apportez les modifications nécessaires aux [Paramètres avancés](#advanced-settings).

   ![Modifier la recommandation de produit](./assets/pb-prex-edit.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, procédez comme suit :

   - Si vous utilisez une fenêtre de navigateur entièrement agrandie, cliquez sur l’icône _Fermer le plein écran_ (![icône Fermer le plein écran](./assets/pb-icon-reduce.png)) dans le coin supérieur droit de l’espace de travail.

   - Cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

   Lorsque vous revenez à la phase, des images d’espace réservé de produit apparaissent dans le conteneur.

## Modifier les paramètres de l’unité de recommandation

1. Pointez sur le conteneur d’unité de recommandation pour afficher la boîte à outils et cliquez sur l’icône _Paramètres_ (![icône Paramètres](./assets/pb-icon-settings.png)).

   ![Boîte à outils de recommandations](./assets/pb-placeholder-toolbox.png){width="600" zoomable="yes"}

1. Apportez les modifications nécessaires aux [Paramètres avancés](#advanced-settings).

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

## Dupliquer une unité de recommandation

1. Pointez sur le conteneur d’unité de recommandation pour afficher la boîte à outils et cliquez sur l’icône _Dupliquer_ (![icône Dupliquer](./assets/pb-icon-duplicate.png)) dans la boîte à outils.

   Le duplicata apparaît juste en dessous de l’original.

1. Pour déplacer l’unité de recommandation dupliquée vers un nouvel emplacement, placez le pointeur de la souris sur le conteneur et cliquez sur l’icône _Déplacer_ (![Icône Déplacer](./assets/pb-icon-move.png)) de la palette d’outils.

1. Sélectionnez et faites glisser l’unité de recommandation jusqu’à ce que la ligne directrice rouge s’affiche à la nouvelle position.

   Les bordures supérieure et inférieure de chaque conteneur apparaissent sous forme de lignes en tirets lorsque l’unité de recommandation est déplacée.

## Supprimer une unité de recommandation de l’étape

1. Pointez sur le conteneur d’unité de recommandation et cliquez sur l’icône _Supprimer_ ( ![Icône Supprimer](./assets/pb-icon-remove.png)) dans la boîte à outils.

1. Lorsque vous êtes invité à confirmer, cliquez sur **[!UICONTROL OK]**.

## Paramètres avancés

1. Pour contrôler le positionnement de l’unité de recommandations de produits dans le conteneur parent, choisissez l’**[!UICONTROL Alignment]** :

   | Option | Description |
   | ------ | ----------- |
   | `Default` | Applique le paramètre d’alignement par défaut spécifié dans la feuille de style du thème actif. |
   | `Left` | Aligne l’unité le long de la bordure gauche du conteneur parent, en tenant compte de la marge intérieure spécifiée. |
   | `Center` | Aligne l’unité au centre du conteneur parent, en tenant compte de la marge intérieure spécifiée. |
   | `Right` | Aligne l’unité le long de la bordure droite du conteneur parent, en tenant compte de la marge intérieure spécifiée. |

   {style="table-layout:auto"}

1. Définissez le style de **[!UICONTROL Border]** appliqué aux quatre côtés de l’unité de recommandations de produits :

   | Option | Description |
   | ------ | ----------- |
   | `Default` | Applique le style de bordure par défaut spécifié par la feuille de style associée. |
   | `None` | Ne fournit aucune indication visible des bordures de l’unité. |
   | `Dotted` | La bordure de l&#39;unité apparaît sous la forme d&#39;une ligne pointillée. |
   | `Dashed` | La bordure de l’unité s’affiche sous la forme d’une ligne en tirets. |
   | `Solid` | La bordure de l&#39;unité s&#39;affiche sous la forme d&#39;une ligne continue. |
   | `Double` | La bordure de l&#39;unité s&#39;affiche sous la forme d&#39;une ligne double. |
   | `Groove` | La bordure de l&#39;unité s&#39;affiche sous la forme d&#39;une ligne rainurée. |
   | `Ridge` | La bordure de l&#39;unité apparaît sous la forme d&#39;une ligne crantée. |
   | `Inset` | La bordure de l&#39;unité s&#39;affiche sous la forme d&#39;une ligne insérée. |
   | `Outset` | La bordure de l&#39;unité apparaît comme une ligne de départ. |

   {style="table-layout:auto"}

1. Si vous définissez un style de bordure autre que `None`, renseignez les options d’affichage des bordures :

   | Option | Description |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Spécifiez la couleur en choisissant une nuance, en cliquant sur le sélecteur de couleurs ou en saisissant un nom de couleur valide ou une valeur hexadécimale équivalente. |
   | [!UICONTROL Border Width] | Saisissez le nombre de pixels pour la largeur de la ligne de bordure. |
   | [!UICONTROL Border Radius] | Saisissez le nombre de pixels pour définir la taille du rayon utilisé pour arrondir chaque coin de la bordure. |

   {style="table-layout:auto"}

1. (Facultatif) Spécifiez les noms des **[!UICONTROL CSS classes]** de la feuille de style actuelle à appliquer à l&#39;unité.

   Séparez plusieurs noms de classe par un espace.

1. Saisissez les valeurs, en pixels, du **[!UICONTROL Margins and Padding]** pour déterminer les marges extérieures et la marge intérieure de l’unité.

   Saisissez les valeurs correspondantes dans le diagramme.

   | Zone conteneur | Description |
   | ------ | ----------- |
   | [!UICONTROL Margins] | Quantité d&#39;espace vide appliquée au bord extérieur de tous les côtés de l&#39;unité. Options : `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Quantité d&#39;espace vide appliquée au bord intérieur de tous les côtés de l&#39;unité. Options : `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}
