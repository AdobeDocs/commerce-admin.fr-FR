---
title: Ajouter du contenu - Produits
description: En savoir plus sur le type de contenu Produits , utilisé pour ajouter une liste de produits au [!DNL Page Builder] scène.
exl-id: 8ef38669-a6f6-493b-b963-b0fc4e3bbff4
feature: Page Builder, Page Content, Products
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1912'
ht-degree: 0%

---

# Ajouter du contenu - Produits

Utilisez la variable _Produits_ type de contenu pour ajouter une liste de produits au [[!DNL Page Builder] étape](workspace.md#stage), à l’aide d’une mise en page de grille ou de carrousel. Utilisez la variable [Ajouter du contenu - Bloc](block.md) pour placer le bloc sur la balise [!DNL Page Builder] étape, puis placer une liste de produits dans le bloc. Vous pouvez également ajouter la liste de produits directement dans une ligne d’une page.

## Instructions relatives à l’utilisation du carrousel de produit

Le carrousel de produit offre un moyen puissant et attrayant de présenter vos produits. Pour en tirer le meilleur parti, les instructions suivantes sont recommandées :

- Ajoutez des carrousels de produit directement aux conteneurs de largeur de page tels que des lignes, des onglets ou des mises en page à une seule colonne. L’utilisation de dispositions de largeur de page garantit un affichage réactif optimal de vos produits. [!DNL Page Builder] réduit le nombre de produits affichés en fonction de la largeur de la page et non de la largeur du conteneur.

- N’ajoutez pas de carrousel de produit à une colonne étroite. Comme mentionné ci-dessus : [!DNL Page Builder], par défaut, détermine le nombre de produits à afficher en fonction de la largeur de page et non de la largeur de colonne.

- Si vous souhaitez que le carrousel de votre produit fasse défiler automatiquement en continu, définissez les deux **[!UICONTROL Autoplay]** et **[!UICONTROL Infinite Loop]** to `Yes`. Si la lecture automatique est définie sur `Yes` mais la boucle infinie est définie sur `No`, le défilement automatique s’arrête à la fin de la liste de produits.

- Définissez la variable **[!UICONTROL Carousel Mode]** to `Continuous` pour mettre en évidence, centrer et faire défiler un produit à la fois dans le carrousel. Les autres produits sont visibles dans la liste, mais transparents pour mettre en évidence le produit centré.

  ![Liste de produits en mode carrousel continu](./assets/pb-products-settings-carousel-continuous.png){width="600"}

- Pour afficher et faire défiler jusqu’à cinq produits à la fois dans le carrousel, conservez la variable **[!UICONTROL Carousel Mode]** défini sur `Default`.

  ![Liste de produits en mode carrousel par défaut](./assets/pb-products-settings-carousel-default.png){width="600"}

Les instructions suivantes expliquent comment ajouter une liste de produits à un bloc. Vous pouvez ensuite utiliser une [widget](../content-design/widgets.md) pour placer le bloc à un emplacement spécifique sur une page de votre magasin.

{{$include /help/_includes/page-builder-save-timeout.md}}

## Boîte à outils Produits

| Outil | Icône | Description |
| --------- | ------------- | ----------------- |
| Déplacer | ![Icône Déplacer](./assets/pb-icon-move.png){width="25"} | Déplace le conteneur de produits et son contenu vers une autre position sur la scène. |
| Paramètres | ![Icône Paramètres](./assets/pb-icon-settings.png){width="25"} | Ouvre la _Modifier les produits_ dans laquelle vous pouvez sélectionner la liste de produits et modifier les propriétés du conteneur. |
| Masquer | ![Icône Masquer](./assets/pb-icon-hide.png){width="25"} | Masque le conteneur de produits actuel et son contenu. |
| Afficher | ![Icône Afficher](./assets/pb-icon-show.png){width="25"} | Affiche le conteneur de produits masqué et son contenu. |
| Dupliquer | ![Icône Dupliquer](./assets/pb-icon-duplicate.png){width="25"} | Effectue une copie du conteneur de produits et de son contenu. |
| Supprimer | ![Icône Supprimer](./assets/pb-icon-remove.png){width="25"} | Supprime le conteneur de produits et son contenu de la scène. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Création d’un bloc de liste de produits

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Cliquez sur **[!UICONTROL Add New Block]**.

1. Saisissez le **[!UICONTROL Block Title]** et **[!UICONTROL Identifier]**.

1. Choisissez la **[!UICONTROL Store View]** où le bloc doit être disponible.

1. Faites défiler la page vers le bas et cliquez sur **[!UICONTROL Edit with Page Builder]** ou dans la zone d’aperçu du contenu pour ouvrir la [!DNL Page Builder] workspace.

1. Dans le [!DNL Page Builder] panneau, développer **[!UICONTROL Add Content]** et faites glisser un **[!UICONTROL Products]** espace réservé sur la scène.

   ![Ajouter un type de contenu Produits](./assets/pb-add-content-products-drag.png){width="600" zoomable="yes"}

## Configuration du conteneur de la liste de produits

Passez la souris sur le champ vide _Produits_ pour afficher la boîte à outils, puis cliquez sur l’icône _Paramètres_ (![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

![Boîte à outils Produits](./assets/pb-add-content-products-toolbox.png){width="500" zoomable="yes"}

Procédez comme suit : _Paramètres_ selon les sections suivantes :

### Apparence

1. Pour déterminer l’affichage de la liste de produits sur la page, choisissez l’un des types d’aspect suivants :

   | Type | Description |
   | ---- | ----------- |
   | Grille de produits | Affiche les produits dans une grille qui affiche cinq produits par ligne (par défaut), avec autant de lignes que nécessaire pour afficher le nombre entré dans la variable **[!UICONTROL Number of Products to Display]** . |
   | Carrousel de produit | Affiche les produits dans un carrousel (également appelé curseur). Le carrousel affiche jusqu’à cinq produits par diapositive. <br/><br/>**Alerte de réaction**: lorsque vous sélectionnez cet aspect, il est préférable d’ajouter le type de contenu Produits directement à une disposition de ligne, d’onglet ou d’une colonne où il est réactif, en affichant moins de produits par côté sur des écrans plus petits. Si vous l’ajoutez à des types de contenu plus limités que la largeur de la page (une colonne étroite, par exemple), le carrousel affiche plus de produits par diapositive que ne le permet le conteneur, quelle que soit la taille de l’écran. |

   {style="table-layout:auto"}

   ![Apparence du produit](./assets/pb-products-appearances.png){width="300"}

   Si vous choisissez le carrousel de produit, vous devez également configurer la variable [Paramètres du carrousel](#carousel-settings).

1. Pour **[!UICONTROL Select Products By]**, choisissez la méthode de sélection de produit :

   Vous pouvez sélectionner vos produits par catégorie, SKU ou condition. Ces options s’excluent mutuellement. Par exemple, vous ne pouvez pas sélectionner l’option Catégorie, utiliser le sélecteur de catégorie, puis passer à l’option Condition pour ajouter certaines conditions. Vos produits ne sont sélectionnés que selon ce que vous avez défini pour _one_ de ces trois options.

   - **[!UICONTROL Category]** - Sélectionnez cette option pour afficher les produits utilisant une catégorie sélectionnée.

     ![Sélection de produit par catégorie](./assets/pb-products-settings_category.png){width="500"}

     Lorsque cette option est sélectionnée, une **[!UICONTROL Category]** sélecteur. Cliquez sur la flèche et faites défiler l’écran pour sélectionner la catégorie de produits à afficher. Par exemple, dans la variable [!DNL Commerce] données d’exemple, exploration et sélection _Women > Tops > Tees_ affiche tous les produits de cette catégorie.

     ![Sélectionner une catégorie de catalogue](./assets/pb-select-products-by-category.png){width="500"}

   - **[!UICONTROL SKU]** - Sélectionnez cette option pour afficher les produits à l’aide d’un ou de plusieurs SKU

     Lorsque cette option est sélectionnée, une **[!UICONTROL Product SKUs]** zone de texte dans laquelle vous devez entrer une liste de SKU séparés par des virgules à afficher.

     ![Sélection de produit par SKU](./assets/pb-products-settings_sku.png){width="500"}

   - **[!UICONTROL Condition]** - Sélectionnez cette option pour afficher les produits selon une ou plusieurs conditions que vous avez définies.

     Lorsque cette option est sélectionnée, des outils sont disponibles pour ajouter des conditions à votre sélection de produits. Par exemple, vous pouvez sélectionner uniquement les produits dont le genre est défini sur Unisex.

     ![Sélection du produit par condition](./assets/pb-products-settings_condition.png){width="500"}

     >[!NOTE]
     >
     >La sélection de l’option Catégorie ou SKU fournit la variable **[!UICONTROL Sort By]** option de `Position`. Avec cette option de tri, les produits apparaissent dans l’ordre dans lequel ils apparaissent dans votre catalogue.</br>
     >
     >Pour l’option Catégorie , le tri par position affiche les produits dans l’ordre dans lequel ils apparaissent dans votre catalogue. Pour l’option SKU, le tri par position affiche les produits dans l’ordre dans lequel vous les saisissez dans la variable **[!UICONTROL Product SKUs]** textbox.

1. Pour **[!UICONTROL Sort By]**, choisissez l’ordre de tri des produits de la liste :

   | Option | Description |
   | ------ | ----------- |
   | `Position` (pour les options Catégorie et SKU uniquement) | Lorsque vous sélectionnez l’option Catégorie , la Position affiche les produits dans le même ordre que leur position dans le catalogue. Lorsque vous sélectionnez l’option SKU, la position affiche les produits dans le même ordre que les SKU dans la zone de texte des SKU du produit. |
   | `Newest products first` | Trie les produits par date d’ajout au catalogue, en affichant d’abord les produits dont les dates d’entrée sont les plus récentes. |
   | `Oldest products first` | Trie les produits par date d’ajout au catalogue, en affichant d’abord les produits avec les dates d’entrée les plus anciennes. |
   | `Name: A - Z` | Trie les produits par ordre alphabétique. |
   | `Name: Z - A` | Trie les produits par ordre alphabétique inverse. |
   | `SKU: ascending` | Trie les produits par SKU par ordre alphanumérique. |
   | `SKU: descending` | Trie les produits par SKU dans l’ordre alphanumérique inverse. |
   | `Stock: low stock first` | Trie les produits du stock le plus faible au stock le plus élevé disponible. |
   | `Stock: high stock first` | Trie les produits du stock le plus élevé au plus faible disponible. |
   | `Price: high to low` | Trie les produits du prix le plus élevé au plus faible. |
   | `Price: low to high` | Trie les produits du prix le plus bas au plus élevé. |

   {style="table-layout:auto"}

   ![Options de tri des produits](./assets/pb-products-sortby.png){width="300"}

1. Saisissez le **[!UICONTROL Number of Products to Display]** dans le carrousel ou la grille.

   Les valeurs peuvent provenir de `1` to `999`. La valeur par défaut est `5` pour une grille et `20` pour un carrousel.

   >[!NOTE]
   >
   >Certains produits des paramètres Catégorie, SKU ou Condition peuvent ne pas apparaître dans votre grille ou carrousel de produits. Par exemple, les produits désactivés, les produits marqués comme non visibles, les produits en rupture de stock et les produits affectés à un autre site web ne s’affichent pas.

   >[!IMPORTANT]
   >
   >Les prix des produits configurables, groupés et regroupés (prix dynamique) ne sont pas définis dans l’Admin. Par conséquent, ces produits ne s’affichent pas dans la variable **[!UICONTROL Preview]** si les produits sont filtrés par prix. Ces produits ne peuvent pas être commandés correctement dans la variable **[!UICONTROL Preview]** si le prix commande.

### Paramètres du carrousel

1. Pour déterminer l’affichage des produits dans le carrousel, choisissez la variable **[!UICONTROL Carousel Mode]**:

   | Option | Description |
   | ------ | ----------- |
   | `Default` | Par défaut, le carrousel affiche cinq produits par diapositive et réduit de manière réactive ce nombre selon les besoins. |
   | `Continuous` | Le carrousel affiche cinq produits par diapositive par défaut (avec la moitié d’un produit à droite et à gauche), mais il centre et fait défiler un produit à la fois en boucle infinie. Les produits situés à droite et à gauche du produit centré sont grisés afin que le produit central soit mis en surbrillance. |

   {style="table-layout:auto"}

   Si vous basculez entre ces deux modes, les autres paramètres du carrousel sont conservés, à l’exception de la variable **[!UICONTROL Infinite Loop]** qui est toujours défini sur `Yes` en mode continu et que le champ est désactivé.

   ![Paramètres du carrousel](./assets/pb-products-carousel-settings.png){width="600" zoomable="yes"}

1. Si nécessaire, définissez la variable **[!UICONTROL Autoplay]** option à `Yes`.

   Lorsque la lecture automatique est activée, le carrousel commence à défiler automatiquement au chargement de la page. Si vous laissez le paramètre par défaut (`No`), le client doit cliquer sur la navigation de la diapositive (points ou flèches) pour afficher chaque diapositive dans l’ordre.

   Si vous activez cette fonction, saisissez **[!UICONTROL Autoplay Speed]** pour spécifier le délai en millisecondes entre chaque diapositive. La valeur par défaut est `4000` (4 secondes).

1. Si nécessaire, définissez la variable **[!UICONTROL Infinite Loop]** option à `Yes`.

   Lorsque la boucle infinie est activée, le diaporama est lu indéfiniment pendant que la page est ouverte. Si vous laissez le paramètre par défaut (`No`), le diaporama n’est lu qu’une seule fois.

   >[!NOTE]
   >
   >Si vous définissez **[!UICONTROL Infinite Loop]** to `No` et **[!UICONTROL Autoplay]** défini sur `Yes`, la lecture automatique s’arrête à la fin du nombre de produits à afficher.

1. Si nécessaire, définissez la variable **[!UICONTROL Show Arrows]** option à `Yes`.

   Lorsque cette option est activée, chaque diapositive comprend _next_ et _previous_ flèches de navigation à gauche et à droite. Si vous laissez le paramètre par défaut (`No`), les diapositives n’affichent pas les flèches de navigation.

1. Si nécessaire, définissez la variable **[!UICONTROL Show Dots]** option à `No`.

   Lorsque ce paramètre est défini sur le paramètre par défaut (`Yes`), les points de navigation apparaissent au bas du curseur du carrousel. Si vous désactivez ce paramètre, le curseur du carrousel n’affiche pas de points de navigation.

### Avancé

1. Pour contrôler le positionnement de la liste Produits dans le conteneur parent, sélectionnez la variable **[!UICONTROL Alignment]**:

   | Option | Description |
   | ------ | ----------- |
   | `Default` | Applique le paramètre d’alignement par défaut spécifié dans la feuille de style du thème actif. |
   | `Left` | Aligne la liste le long de la bordure gauche du conteneur parent, en tenant compte de toute marge intérieure spécifiée. |
   | `Center` | Aligne la liste au centre du conteneur parent, en tenant compte de toute marge intérieure spécifiée. |
   | `Right` | Aligne la liste le long de la bordure droite du conteneur parent, en tenant compte de toute marge intérieure spécifiée. |

   {style="table-layout:auto"}

1. Définissez la variable **[!UICONTROL Border]** style appliqué aux quatre côtés du conteneur Produits :

   | Option | Description |
   | ------ | ----------- |
   | `Default` | Applique le style de bordure par défaut spécifié par la feuille de style associée. |
   | `None` | Ne fournit aucune indication visible des bordures du conteneur. |
   | `Dotted` | La bordure du conteneur s’affiche sous la forme d’une ligne pointillée. |
   | `Dashed` | La bordure du conteneur s’affiche sous la forme d’une ligne en pointillés. |
   | `Solid` | La bordure du conteneur s’affiche sous la forme d’une ligne pleine. |
   | `Double` | La bordure du conteneur s’affiche sous la forme d’une ligne double. |
   | `Groove` | La bordure du conteneur s’affiche sous forme de ligne droite. |
   | `Ridge` | La bordure du conteneur s’affiche sous la forme d’une ligne à droite. |
   | `Inset` | La bordure du conteneur s’affiche sous la forme d’une ligne d’insertion. |
   | `Outset` | La bordure du conteneur apparaît comme une ligne de départ. |

   {style="table-layout:auto"}

1. Si vous définissez un style de bordure autre que `None`, renseignez les options d’affichage des bordures :

   | Option | Description |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Définissez la couleur en choisissant un échantillon, en cliquant sur le sélecteur de couleurs ou en saisissant un nom de couleur valide ou une valeur hexadécimale équivalente. |
   | [!UICONTROL Border Width] | Saisissez le nombre de pixels pour la largeur de la ligne de bordure. |
   | [!UICONTROL Border Radius] | Saisissez le nombre de pixels pour définir la taille du rayon utilisé pour arrondir chaque coin de la bordure. |

   {style="table-layout:auto"}

1. (Facultatif) Indiquez les noms des **[!UICONTROL CSS classes]** de la feuille de style actuelle à appliquer au conteneur.

   Séparez plusieurs noms de classe par un espace.

1. Saisissez des valeurs, en pixels, pour la variable **[!UICONTROL Margins and Padding]** pour déterminer les marges extérieures et la marge intérieure du conteneur Produits.

   Saisissez les valeurs correspondantes dans le diagramme.

   | Zone de conteneur | Description |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | Espace vide appliqué au bord extérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Espace blanc appliqué au bord intérieur de tous les côtés du conteneur. Options : `Top` / `Right` / `Bottom` / `Left` |


## Enregistrer et prévisualiser sur la scène

Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir au [!DNL Page Builder] workspace.

Si vous avez configuré un carrousel de produit, il doit ressembler à l’exemple suivant :

![Carrousel de produit sur la scène](./assets/pb-products-admin-carousel.png){width="600"}

Vous pouvez désormais utiliser une [widget](../content-design/widgets.md) pour placer ce bloc où vous souhaitez qu&#39;il apparaisse dans le magasin. Vous pouvez également utiliser [Ajouter du contenu - Bloc](block.md) pour ajouter le bloc à une page, un onglet ou un bloc existant.
