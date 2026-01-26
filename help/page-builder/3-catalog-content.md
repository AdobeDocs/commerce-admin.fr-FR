---
title: '[!DNL Page Builder] Présentation de la partie 3 : contenu du catalogue'
description: Découvrez comment ajouter une liste de produits à une  [!DNL Page Builder] .
exl-id: f2a0dc29-6d8f-4b97-a947-72659c01d0cb
feature: Page Builder, Page Content
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1494'
ht-degree: 0%

---

# [!DNL Page Builder] Présentation de la partie 3 : contenu du catalogue

Cet exercice montre à quel point il est facile d’ajouter une liste de produits à une page, de personnaliser les pages de produits et de créer un attribut personnalisé qui ajoute l’espace de travail [!DNL Page Builder] à un jeu d’attributs de produit.

![Liste de produits](./assets/pb-add-content-products-list.png){width="600" zoomable="yes"}

Cet exercice suppose que vous avez terminé [Partie 1 : Page simple](1-simple-page.md) et [Partie 2 : Blocs](2-blocks.md), y compris les conditions préalables et les fichiers d’exemple téléchargés. Suivez les trois parties de cet exercice dans l’ordre.

## Partie 1 : ajout d’une liste de produits

[!DNL Page Builder] facilite l’ajout d’une liste de produits à l’étape. Dans cet exemple, la liste de produits est ajoutée directement à une page.

### Étape 1 : ajouter une liste de produits à l’étape

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Recherchez la _Page simple_ que vous avez créée dans le premier exercice et modifiée dans le second, puis sélectionnez **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_.

1. Développez ![Sélecteur de développement](../assets/icon-display-expand.png) la section **[!UICONTROL Content]**, puis cliquez sur **[!UICONTROL Edit with Page Builder]** ou dans la zone de prévisualisation du contenu.

1. Dans le panneau [!DNL Page Builder] sous _[!UICONTROL Layout]_, faites glisser un **[!UICONTROL Row]**&#x200B;vers le haut de la scène.

1. Dans le panneau [!DNL Page Builder], développez **[!UICONTROL Add Content]** et faites glisser un espace réservé **[!UICONTROL Products]** vers la nouvelle ligne.

   ![Faire glisser un espace réservé de produits sur la ligne](./assets/pb-add-content-products-drag.png){width="600" zoomable="yes"}

### Étape 2 : Composer la condition

1. Pointez sur le conteneur de produits vide pour afficher la boîte à outils et sélectionnez l’icône _Paramètres_ ( ![icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

   ![Boîte à outils Produits](./assets/pb-add-content-products-toolbox.png){width="600" zoomable="yes"}

1. Par **[!UICONTROL Select Products By]**, choisissez `Condition`.

1. Ajoutez une condition :

   - Cliquez sur l’icône _Ajouter_ (![Ajouter une icône](../assets/icon-add-green-circle.png)).

   - Sous _[!UICONTROL Product Attribute]_, choisissez **[!UICONTROL Category]**.

     ![Choix de l&#39;attribut category pour la condition](./assets/pb-add-content-products-settings-condition.png){width="600" zoomable="yes"}

   - Renseignez la partie _[!UICONTROL Category is]..._ de la condition en cliquant sur l’icône Plus (...), puis cliquez sur l’icône _Sélecteur_ (![icône Sélecteur](../assets/icon-list-chooser.png)).

     ![Définition de la condition](./assets/pb-add-content-products-settings-condition-category-is.png){width="600" zoomable="yes"}

   - Dans l’arborescence des catégories, descendez jusqu’à la catégorie **Femmes > Tops** et cochez la case **Tees**.

     ![Choix de la catégorie dans l&#39;arborescence](./assets/pb-add-content-products-settings-condition-category-tree.png){width="600" zoomable="yes"}

   - Cliquez sur l’icône en forme de coche (![icône en forme de coche](../assets/icon-checkmark-green-circle.png)).

     L’identifiant de catégorie correspondant s’affiche dans le champ pour remplir la condition.

### Étape 3 : définition des paramètres

1. Saisissez le **[!UICONTROL Number of Products to Display]**.

   Par défaut, la liste affiche cinq produits.

1. Renseignez les paramètres restants selon vos besoins.

   Si nécessaire, utilisez les descriptions des champs à la fin de la page [Ajouter du contenu - Produits](products.md) pour vous y référer.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]** pour enregistrer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

   ![Liste de produits dans l’étape](./assets/pb-add-content-products-list-stage.png){width="600" zoomable="yes"}

1. Dans le coin supérieur droit de la scène, cliquez sur l’icône _Fermer le plein écran_ ( ![Icône Fermer le plein écran](./assets/pb-icon-reduce.png){width="20"} ).

   Cliquer sur cette icône vous renvoie à la section _[!UICONTROL Content]_&#x200B;de la page dont l’aperçu est affiché.

1. Dans le coin supérieur droit, cliquez sur la flèche **[!UICONTROL Save]** et choisissez **[!UICONTROL Save & Close]**.

## Partie 2 : personnalisation de la page produit

>[!NOTE]
>
>Un utilisateur administrateur doit disposer d’autorisations [!UICONTROL Content] pour son [étendue de rôle](../systems/permissions-user-roles.md) pour voir [!UICONTROL Edit with Page Builder] boutons et pouvoir utiliser Page Builder.

Dans cette partie de l’exercice, vous découvrirez à quel point il est facile de personnaliser une page produit en plaçant une vidéo sous l’ensemble d’onglets de la page produit. Le processus de mise à jour du contenu [page de catégorie](../catalog/categories-content-settings.md) est fondamentalement le même.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Recherchez un produit simple que vous pouvez utiliser pour cet exemple et ouvrez-le en mode d’édition.

1. Faites défiler vers le bas et développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Content]** .

1. En regard de _[!UICONTROL Description]_, cliquez sur **[!UICONTROL Edit with Page Builder]**.

   ![Contenu de la description du produit](./assets/pb-catalog-product-content.png){width="600" zoomable="yes"}

   Si la description du produit a été saisie précédemment sans [!DNL Page Builder], la description actuelle s’affiche sous la forme d’HTML dans un conteneur [Code HTML](html-code.md). Avec le thème Luma , la description du produit s’affiche dans l’onglet Détail .

1. Dans le panneau [!DNL Page Builder] sous _[!UICONTROL Layout]_, faites glisser un **[!UICONTROL Row]**&#x200B;vers la scène, en le plaçant sous le conteneur de code HTML.

   Recherchez l&#39;indicateur rouge qui doit apparaître lorsque la ligne se trouve à la bonne position.

   ![Faire glisser une ligne vers l’étape](./assets/catalog-product-content-stage-row-drag.png){width="600" zoomable="yes"}

1. Dans le panneau [!DNL Page Builder], développez **[!UICONTROL Media]** et faites glisser un espace réservé **[!UICONTROL Video]** vers la nouvelle ligne.

   ![&#x200B; Espace réservé de la vidéo dans la ligne &#x200B;](./assets/tutorial3-product-drag-video.png){width="600" zoomable="yes"}

1. Pointez sur le conteneur vidéo vide pour afficher la boîte à outils et sélectionnez l’icône _Paramètres_ ( ![icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

   ![&#x200B; Boîte à outils vidéo &#x200B;](./assets/pb-tutorial3-product-video-toolbox.png){width="500" zoomable="yes"}

1. Saisissez le **[!UICONTROL Video URL]**.

   La vidéo peut être hébergée sur [YouTube](https://www.youtube.com/) ou [Vimeo](https://vimeo.com/). La vidéo de cet exemple se trouve sur YouTube à l’adresse URL suivante :

   `https://www.youtube.com/watch?v=ZpFrNyD4100`

   ![&#x200B; Modification de la vidéo &#x200B;](./assets/pb-tutorial3-product-edit-video.png){width="500" zoomable="yes"}

1. Saisissez le **[!UICONTROL Maximum Width]** en pixels de l’affichage vidéo.

   Si vous ne renseignez pas cette option, la vidéo remplit l’espace disponible.

1. Cliquez sur **[!UICONTROL Save]** pour enregistrer les paramètres et revenir à l’espace de travail [!DNL Page Builder].

   ![Vidéo dans l’étape du contenu](./assets/pb-tutorial3-product-video.png){width="600" zoomable="yes"}

1. Dans le coin supérieur droit de la scène, cliquez sur l’icône _Fermer le plein écran_ ( ![Icône Fermer le plein écran](./assets/pb-icon-reduce.png){width="20"} ).

   Cliquer sur cette icône vous renvoie à la section _[!UICONTROL Content]_&#x200B;de la page dont l’aperçu est affiché.

1. Dans le coin supérieur droit, cliquez sur la flèche **[!UICONTROL Save]** et choisissez **[!UICONTROL Save & Close]**.

Dans le storefront, la vidéo s’affiche sous l’ensemble d’onglets. Pour voir à quoi ressemble la page sur un appareil mobile, vous pouvez redimensionner la fenêtre.

![Vidéo affichée sur la page du produit](./assets/pb-tutorial3-product-video-storefront.png){width="600" zoomable="yes"}

**Félicitations !** Vous avez terminé la deuxième partie du tutoriel sur le contenu du catalogue. Conservez le travail que vous avez créé afin de pouvoir y faire référence ultérieurement.

## Partie 3 : ajout d’attributs personnalisés

Utilisez l’attribut personnalisé [!DNL Page Builder] pour ajouter un espace de travail [!DNL Page Builder] entièrement fonctionnel à une page produit, que vous pouvez utiliser pour créer du contenu attrayant. Dans cette partie de l’exercice, vous apprendrez à créer un attribut personnalisé à l’aide du type d’entrée [!DNL Page Builder] et à l’appliquer aux pages de produits de votre catalogue. Pour plus d’informations sur ces attributs, voir [Attributs du produit](../catalog/product-attributes.md).

### Étape 1 : créer un produit

Pour éviter toute modification de votre boutique en ligne, créez un produit à l’aide des propriétés décrites.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Product]**.

1. Créez le produit avec les propriétés suivantes :

   - &#x200B;
     [!UICONTROL Jeu D&#39;Attributs]: Default
   - [!UICONTROL Product Name] : Mon produit
   - &#x200B;
     [!UICONTROL SKU]: Tutorial
   - &#x200B;
     [!UICONTROL Price]: 75.00
   - &#x200B;
     [!UICONTROL Quantity]: 100
   - [!UICONTROL Stock Status] : en stock
   - &#x200B;
     [!UICONTROL Weight]: 1
   - [!UICONTROL Categories] : Femmes > Tops > Tees

1. Dans le coin supérieur droit, cliquez sur la flèche **[!UICONTROL Save]** et choisissez **[!UICONTROL Save & Close]**.

### Étape 2 : créer des attributs personnalisés

Au cours de cette étape, vous créez deux nouveaux attributs personnalisés pour montrer comment les types d’entrée [!DNL Page Builder] et Éditeur de texte peuvent être utilisés.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Attribute]**.

1. Saisissez un **[!UICONTROL Default Label]** pour l’attribut.

   Pour cet exemple, utilisez `My Page Builder Attribute` comme libellé.

1. Définissez **[!UICONTROL Catalog Input Type for Store Owner]** sur `Page Builder`.

   Lors de la création d’un attribut personnalisé, vous pouvez spécifier l’éditeur le plus adapté à l’application comme `Page Builder` ou `Text Editor` WYSIWYG standard.

   Type d’entrée ![[!DNL Page Builder]](./assets/pb-attribute-page-builder.png){width="600" zoomable="yes"}

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Advanced Attribute Properties]** et définissez les paramètres suivants :

   - [!UICONTROL Attribute Code] : saisissez un code d’attribut en minuscules, en utilisant des tirets au lieu d’espaces. Pour cet exemple, utilisez `my_page_builder_attribute`.
   - [!UICONTROL Scope] : acceptez la valeur par défaut, `Store View`.
   - [!UICONTROL Default Value] : saisissez une valeur par défaut pour l’attribut.
   - &#x200B;
     [!UICONTROL Unique Value]: `No`
   - &#x200B;
     [!UICONTROL Add to Column Options]: `No`
   - &#x200B;
     [!UICONTROL Use in Filter Options]: `Yes`

1. Dans le panneau _[!UICONTROL Attribute Information]_&#x200B;à gauche, choisissez **[!UICONTROL Storefront Properties]**&#x200B;et effectuez les paramètres suivants :

   - &#x200B;
     [!UICONTROL Use for Promo Rule Conditions]: `Yes`
   - &#x200B;
     [!UICONTROL Visible on Catalog Pages on Storefront]: `Yes`
   - &#x200B;
     [!UICONTROL Used in Product Listing]: `Yes`

1. Cliquez ensuite sur **[!UICONTROL Save Attribute]**.

1. Répétez les étapes précédentes pour créer un second attribut avec les mêmes propriétés de base, mais avec le type d’entrée Éditeur de texte comme suit :

   - [!UICONTROL Default Label] : Mon attribut d’éditeur de texte
   - [!UICONTROL Catalog Input Type for Store Owner] : éditeur de texte
   - &#x200B;
     [!UICONTROL Code d&#39;attribut]: `my_text_editor_attribute`

### Étape 3 : mettre à jour le jeu d’attributs de produit

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

   Pour cet exemple, vous ajoutez temporairement les nouveaux attributs au jeu d’attributs `default`. À la fin de cet exercice, supprimez les attributs du jeu d’attributs sans affecter votre catalogue.

   >[!NOTE]
   >
   >Si vous ne souhaitez pas modifier votre boutique en direct, vous pouvez suivre sans mettre à jour le jeu d’attributs.

1. Recherchez le jeu d’attributs _[!UICONTROL Default]_&#x200B;dans la liste et double-cliquez dessus pour l’ouvrir en mode d’édition.

1. Dans la liste _Attributs non affectés_, recherchez les nouveaux attributs que vous avez créés et faites glisser chacun d’eux vers la colonne _[!UICONTROL Groups]_, sous **[!UICONTROL Content]**.

   L’emplacement de l’attribut dans la colonne [!UICONTROL Groups] détermine son emplacement sur la page.

   ![Nouveaux attributs ajoutés au groupe Contenu](./assets/pb-product-attribute-set.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save]** pour revenir à la liste Jeux d’attributs .

1. Lorsque vous y êtes invité, cliquez sur le lien **[!UICONTROL Cache Management]** en haut de la page et actualisez tout cache non valide.

### Étape 4 : mettre à jour le produit

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Dans la grille Produits , recherchez _Mon produit_ et ouvrez-le en mode d’édition.

1. Faites défiler vers le bas et développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Content]** .

   En haut de la section, vous trouverez deux attributs standard pour le contenu du produit :

   - _Description courte_, qui utilise l’éditeur [&#x200B; WYSIWYG standard](../content-design/editor.md).
   - _Description_, qui affiche l’aperçu [!DNL Page Builder].

   ![Contenu du produit](./assets/pb-product-content-edit-with-page-builder.png){width="600" zoomable="yes"}

   Lorsque vous faites défiler la page jusqu’à la moitié inférieure de la section, vous accédez aux deux attributs que vous avez créés et affectés :

   - _Mon attribut de [!DNL Page Builder]_, qui affiche l’aperçu [!DNL Page Builder].
   - _Mon attribut d’éditeur de texte_, qui utilise l’éditeur WYSIWYG standard.

   ![Modification du contenu du produit](./assets/pb-product-content-my-attributes.png){width="600" zoomable="yes"}

1. Dans l’éditeur **Mon attribut d’éditeur de texte**, saisissez `Text Editor Attribute placeholder text`.

   - Dans le coin supérieur droit, cliquez sur la flèche **[!UICONTROL Save]** et choisissez **[!UICONTROL Save & Close]**.

1. Pour **Mon attribut Page Builder**, cliquez sur **[!UICONTROL Edit with Page Builder]** et ajoutez le texte de description :

   - Dans le panneau [!DNL Page Builder], développez **[!UICONTROL Elements]** et faites glisser un **[!UICONTROL Text object]** sur la scène.

   - Saisissez `Page Builder attribute placeholder text`.

   - Dans le coin supérieur droit de la scène, cliquez sur l’icône _Fermer le plein écran_ ( ![Icône Fermer le plein écran](./assets/pb-icon-reduce.png){width="20"} ).

     ![Attributs personnalisés avec texte d’espace réservé](./assets/pb-product-content-attributes.png){width="600" zoomable="yes"}

1. Faites défiler jusqu’à **[!UICONTROL Description]**, cliquez sur **[!UICONTROL Edit with Page Builder]**, puis ajoutez le texte de votre choix en utilisant la même méthode que l’étape précédente.

1. Dans le coin supérieur droit de la page produit, cliquez sur la flèche **[!UICONTROL Save]** et choisissez **[!UICONTROL Save & Close]**.

1. Si vous y êtes invité, cliquez sur le lien **[!UICONTROL Cache Management]** du message en haut de la page et actualisez tout cache non valide.

### Etape 5 : Visualiser le résultat

1. Accédez à l’exemple de page de produit dans le storefront.

   Dans cet exemple, le produit se trouve dans le volet de navigation supérieur sous Femmes > Tops > Tees.

1. Faites défiler l’écran jusqu’aux informations _Mon attribut Page Builder_.

   La position des attributs sur la page du produit est déterminée par le thème. Dans le thème Luma , les nouveaux attributs se trouvent juste après la description du produit.

   ![[!DNL Page Builder] et les attributs de l’éditeur de texte dans le storefront](./assets/pb-storefront-product-attribute.png){width="600" zoomable="yes"}

Vous avez terminé l’exercice de contenu du catalogue [!DNL Page Builder]. Conservez le travail que vous avez créé afin de pouvoir y faire référence ultérieurement.
