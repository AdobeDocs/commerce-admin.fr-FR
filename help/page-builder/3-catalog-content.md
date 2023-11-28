---
title: '''[!DNL Page Builder] Partie 3 de la présentation : contenu du catalogue'
description: Découvrez comment ajouter une liste de produits à une [!DNL Page Builder] page.
exl-id: f2a0dc29-6d8f-4b97-a947-72659c01d0cb
feature: Page Builder, Page Content
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '1481'
ht-degree: 0%

---

# [!DNL Page Builder] Présentation de la partie 3 : contenu du catalogue

Cet exercice montre à quel point il est facile d’ajouter une liste de produits à une page, de personnaliser les pages de produits et de créer un attribut personnalisé qui ajoute la variable [!DNL Page Builder] workspace à un jeu d’attributs de produit.

![Liste de produits](./assets/pb-add-content-products-list.png){width="600" zoomable="yes"}

Cet exercice suppose que vous avez terminé [Partie 1 : page simple](1-simple-page.md) et [Partie 2 : blocs](2-blocks.md), y compris les conditions préalables et les fichiers d’exemple téléchargés. Suivez les trois parties de cet exercice dans l’ordre.

## Partie 1 : Ajouter une liste de produits

[!DNL Page Builder] facilite l’ajout d’une liste de produits à l’étape. Dans cet exemple, la liste de produits est ajoutée directement à une page.

### Étape 1 : Ajout d’une liste de produits à l’étape

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Recherchez le _Page simple_ que vous avez créé lors du premier exercice et que vous avez modifié dans le second, puis sélectionnez **[!UICONTROL Edit]** dans le _[!UICONTROL Action]_colonne .

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Content]** et cliquez sur **[!UICONTROL Edit with Page Builder]** ou dans la zone d’aperçu du contenu.

1. Dans le [!DNL Page Builder] panneau sous _[!UICONTROL Layout]_, faites glisser un **[!UICONTROL Row]**en haut de la scène.

1. Dans le [!DNL Page Builder] panneau, développer **[!UICONTROL Add Content]** et faites glisser un **[!UICONTROL Products]** balise d’emplacement de la nouvelle ligne.

   ![Glissement d’un espace réservé de produits sur la ligne](./assets/pb-add-content-products-drag.png){width="600" zoomable="yes"}

### Étape 2 : Composer la condition

1. Passez la souris sur le conteneur de produits vide pour afficher la boîte à outils et sélectionnez l’option _Paramètres_ ( ![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

   ![Boîte à outils Produits](./assets/pb-add-content-products-toolbox.png){width="600" zoomable="yes"}

1. Pour **[!UICONTROL Select Products By]**, choisissez `Condition`.

1. Ajoutez une condition :

   - Cliquez sur le bouton _Ajouter_ (![Icône Ajouter](../assets/icon-add-green-circle.png)).

   - Sous _[!UICONTROL Product Attribute]_, choisissez **[!UICONTROL Category]**.

     ![Choix de l’attribut de catégorie pour la condition](./assets/pb-add-content-products-settings-condition.png){width="600" zoomable="yes"}

   - Procédez comme suit : _[!UICONTROL Category is].._ d’une partie de la condition en cliquant sur l’icône Plus (..), puis sur la fonction _Sélecteur_ (![Icône Sélecteur](../assets/icon-list-chooser.png)).

     ![Définir la condition](./assets/pb-add-content-products-settings-condition-category-is.png){width="600" zoomable="yes"}

   - Dans l’arborescence des catégories, accédez au **Femmes > Principaux** et sélectionnez la catégorie **Tees** .

     ![Choix de la catégorie dans l&#39;arborescence](./assets/pb-add-content-products-settings-condition-category-tree.png){width="600" zoomable="yes"}

   - Cliquez sur la coche (![Icône de coche](../assets/icon-checkmark-green-circle.png)).

     L’ID de catégorie correspondant apparaît dans le champ pour remplir la condition.

### Étape 3 : Paramètres

1. Saisissez le **[!UICONTROL Number of Products to Display]**.

   Par défaut, la liste affiche cinq produits.

1. Définissez les paramètres restants si nécessaire.

   Si nécessaire, utilisez les descriptions de champ à la fin de la variable [Ajouter du contenu - Produits](products.md) à titre de référence.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]** pour enregistrer les paramètres et revenir au [!DNL Page Builder] workspace.

   ![Liste de produits dans l’étape](./assets/pb-add-content-products-list-stage.png){width="600" zoomable="yes"}

1. Dans le coin supérieur droit de l’étape, cliquez sur le bouton _Fermer le plein écran_ ( ![Icône Fermer le plein écran](./assets/pb-icon-reduce.png){width="20"} ).

   Cliquez sur cette icône pour revenir au _[!UICONTROL Content]_pour la page avec l’aperçu affiché.

1. Dans le coin supérieur droit, cliquez sur le bouton **[!UICONTROL Save]** flèche et choisissez **[!UICONTROL Save & Close]**.

## Partie 2 : personnalisation de la page de produits

>[!NOTE]
>
>Un utilisateur administrateur doit disposer des [!UICONTROL Content] autorisations pour leurs [portée du rôle](../systems/permissions-user-roles.md) pour voir [!UICONTROL Edit with Page Builder] et de pouvoir utiliser le Créateur de pages.

Dans cette partie de l’exercice, vous découvrez à quel point il est facile de personnaliser une page de produit en plaçant une vidéo sous l’ensemble des onglets de la page de produit. Processus de mise à jour [page de catégorie](../catalog/categories-content-settings.md) le contenu est fondamentalement le même.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Recherchez un produit simple que vous pouvez utiliser pour cet exemple et ouvrez-le en mode d’édition.

1. Faire défiler vers le bas et développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Content]** .

1. Suivant _[!UICONTROL Description]_, cliquez sur **[!UICONTROL Edit with Page Builder]**.

   ![Contenu de description du produit](./assets/pb-catalog-product-content.png){width="600" zoomable="yes"}

   Si la description du produit a été saisie précédemment sans [!DNL Page Builder], la description actuelle s’affiche sous la forme d’un HTML dans une [Code HTML](html-code.md) conteneur. Avec le thème Luma, la description du produit s’affiche dans l’onglet Détails .

1. Dans le [!DNL Page Builder] panneau sous _[!UICONTROL Layout]_, faites glisser un **[!UICONTROL Row]**sur l’étape, en le plaçant sous le conteneur de code de HTML.

   Recherchez la ligne guide rouge qui s’affiche lorsque la ligne est à la bonne position.

   ![Glissement d’une ligne vers la scène](./assets/catalog-product-content-stage-row-drag.png){width="600" zoomable="yes"}

1. Dans le [!DNL Page Builder] panneau, développer **[!UICONTROL Media]** et faites glisser un **[!UICONTROL Video]** balise d’emplacement de la nouvelle ligne.

   ![Espace réservé de la vidéo dans la ligne](./assets/tutorial3-product-drag-video.png){width="600" zoomable="yes"}

1. Passez la souris sur le conteneur vidéo vide pour afficher la boîte à outils et sélectionnez l’option _Paramètres_ ( ![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

   ![Boîte à outils vidéo](./assets/pb-tutorial3-product-video-toolbox.png){width="500" zoomable="yes"}

1. Saisissez le **[!UICONTROL Video URL]**.

   La vidéo peut être hébergée sur : [YouTube][1] ou [Vimeo][2]. La vidéo de cet exemple se trouve sur YouTube à l’adresse URL suivante :

   `https://www.youtube.com/watch?v=ZpFrNyD4100`

   ![Modification de la vidéo](./assets/pb-tutorial3-product-edit-video.png){width="500" zoomable="yes"}

1. Saisissez le **[!UICONTROL Maximum Width]** en pixels pour l’affichage vidéo.

   Si vous laissez cette option vide, la vidéo remplit l’espace disponible.

1. Cliquez sur **[!UICONTROL Save]** pour enregistrer les paramètres et revenir au [!DNL Page Builder] workspace.

   ![Vidéo dans l’étape du contenu](./assets/pb-tutorial3-product-video.png){width="600" zoomable="yes"}

1. Dans le coin supérieur droit de l’étape, cliquez sur le bouton _Fermer le plein écran_ ( ![Icône Fermer le plein écran](./assets/pb-icon-reduce.png){width="20"} ).

   Cliquez sur cette icône pour revenir au _[!UICONTROL Content]_pour la page avec l’aperçu affiché.

1. Dans le coin supérieur droit, cliquez sur le bouton **[!UICONTROL Save]** flèche et choisissez **[!UICONTROL Save & Close]**.

Dans le storefront, la vidéo apparaît sous l’ensemble d’onglets. Pour voir à quoi ressemble la page sur un appareil mobile, vous pouvez redimensionner la fenêtre.

![Vidéo affichée sur la page du produit](./assets/pb-tutorial3-product-video-storefront.png){width="600" zoomable="yes"}

**Félicitations !** Vous avez terminé la deuxième partie du tutoriel Contenu du catalogue . Conservez le travail que vous avez créé afin que vous puissiez y faire référence ultérieurement.

## Partie 3 : Ajout d’attributs personnalisés

Utilisez la variable [!DNL Page Builder] attribut personnalisé pour ajouter un fonctionnement complet [!DNL Page Builder] espace de travail vers une page de produit, que vous pouvez utiliser pour créer du contenu attrayant. Dans cette partie de l’exercice, vous apprenez à créer un attribut personnalisé à l’aide de la méthode [!DNL Page Builder] type d’entrée et appliquez-le aux pages de produits de votre catalogue. Pour plus d’informations sur ces attributs, voir [Attributs de produit](../catalog/product-attributes.md).

### Étape 1 : créer un produit

Pour éviter toute modification de votre boutique en ligne, créez un produit à l’aide des propriétés décrites.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Product]**.

1. Créez le produit avec les propriétés suivantes :

   - 
     [!UICONTROL Jeu d’attributs]: Default
   - [!UICONTROL Product Name]: mon produit
   - 
     [!UICONTROL SKU]: Tutorial
   - 
     [!UICONTROL Price]: 75.00
   - 
     [!UICONTROL Quantity]: 100
   - [!UICONTROL Stock Status]: en stock
   - 
     [!UICONTROL Weight]: 1
   - [!UICONTROL Categories]: Femmes > Trops > Teies

1. Dans le coin supérieur droit, cliquez sur le bouton **[!UICONTROL Save]** flèche et choisissez **[!UICONTROL Save & Close]**.

### Étape 2 : Création d’attributs personnalisés

Au cours de cette étape, vous créez deux nouveaux attributs personnalisés pour montrer comment la variable [!DNL Page Builder] Les types d’entrée et Éditeur de texte peuvent être utilisés.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Attribute]**.

1. Saisissez un **[!UICONTROL Default Label]** pour l’attribut .

   Pour cet exemple, utilisez `My Page Builder Attribute` pour le libellé.

1. Définir **[!UICONTROL Catalog Input Type for Store Owner]** to `Page Builder`.

   Lors de la création d’un attribut personnalisé, vous pouvez spécifier l’éditeur le plus adapté à l’application en tant que `Page Builder` ou la norme, WYSIWYG `Text Editor`.

   ![[!DNL Page Builder] Type d’entrée](./assets/pb-attribute-page-builder.png){width="600" zoomable="yes"}

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Advanced Attribute Properties]** et définissez les paramètres suivants :

   - [!UICONTROL Attribute Code]: saisissez un code d’attribut dans des caractères minuscules, avec des tirets au lieu d’espaces. Pour cet exemple, utilisez `my_page_builder_attribute`.
   - [!UICONTROL Scope]: acceptez la valeur par défaut, `Store View`.
   - [!UICONTROL Default Value]: saisissez une valeur par défaut pour l’attribut .
   - 
     [!UICONTROL Unique Value]: `No`
   - 
     [!UICONTROL Add to Column Options]: `No`
   - 
     [!UICONTROL Use in Filter Options]: `Yes`

1. Dans le _[!UICONTROL Attribute Information]_sur la gauche, choisissez **[!UICONTROL Storefront Properties]**et définissez les paramètres suivants :

   - 
     [!UICONTROL Use for Promo Rule Conditions]: `Yes`
   - 
     [!UICONTROL Visible on Catalog Pages on Storefront]: `Yes`
   - 
     [!UICONTROL Used in Product Listing]: `Yes`

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Attribute]**.

1. Répétez les étapes précédentes pour créer un second attribut avec les mêmes propriétés de base, mais avec le type d’entrée Éditeur de texte comme suit :

   - [!UICONTROL Default Label]: mon attribut de l’éditeur de texte
   - [!UICONTROL Catalog Input Type for Store Owner]: Éditeur de texte
   - 
     [!UICONTROL Attribute Code]: `my_text_editor_attribute`

### Étape 3 : mise à jour du jeu d’attributs de produit

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

   Dans cet exemple, vous ajoutez temporairement les nouveaux attributs au `default` ensemble d’attributs. À la fin de cet exercice, supprimez les attributs de l’ensemble d’attributs afin de ne pas affecter votre catalogue.

   >[!NOTE]
   >
   >Si vous ne souhaitez pas modifier votre magasin en direct, vous pouvez suivre sans mettre à jour le jeu d’attributs.

1. Recherchez le _[!UICONTROL Default]_défini dans la liste et double-cliquez dessus pour l’ouvrir en mode d’édition.

1. Dans le _Attributs non attribués_ recherchez les nouveaux attributs que vous avez créés et faites-les glisser sur la liste _[!UICONTROL Groups]_colonne, sous **[!UICONTROL Content]**.

   L’emplacement de l’attribut dans la variable [!UICONTROL Groups] détermine l’emplacement d’affichage sur la page.

   ![Nouveaux attributs ajoutés au groupe Contenu](./assets/pb-product-attribute-set.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save]** pour revenir à la liste Visionneuses d’attributs .

1. Lorsque vous y êtes invité, cliquez sur l’icône **[!UICONTROL Cache Management]** lien en haut de la page et actualisez le cache non valide.

### Étape 4 : Mettre à jour le produit

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Dans la grille Produits , recherchez _Mon produit_ et ouvrez-la en mode d’édition.

1. Faire défiler vers le bas et développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Content]** .

   En haut de la section , il existe deux attributs standard pour le contenu du produit :

   - _Description courte_, qui utilise le WYSIWYG standard [éditeur](../content-design/editor.md).
   - _Description_, qui affiche le [!DNL Page Builder] aperçu.

   ![Contenu du produit](./assets/pb-product-content-edit-with-page-builder.png){width="600" zoomable="yes"}

   Lorsque vous faites défiler l’écran jusqu’à la moitié inférieure de la section, il y a les deux attributs que vous avez créés et attribués :

   - _My [!DNL Page Builder] Attribut_, qui affiche le [!DNL Page Builder] aperçu.
   - _Mon attribut Éditeur de texte_, qui utilise l’éditeur WYSIWYG standard.

   ![Modification du contenu du produit](./assets/pb-product-content-my-attributes.png){width="600" zoomable="yes"}

1. Dans le **Mon attribut Éditeur de texte** éditeur, saisissez `Text Editor Attribute placeholder text`.

   - Dans le coin supérieur droit, cliquez sur le bouton **[!UICONTROL Save]** flèche et choisissez **[!UICONTROL Save & Close]**.

1. Pour **Mon attribut Page Builder**, cliquez sur **[!UICONTROL Edit with Page Builder]** et ajoutez le texte de description :

   - Dans le [!DNL Page Builder] panneau, développer **[!UICONTROL Elements]** et faites glisser un **[!UICONTROL Text object]** sur la scène.

   - Entrée `Page Builder attribute placeholder text`.

   - Dans le coin supérieur droit de l’étape, cliquez sur le bouton _Fermer le plein écran_ ( ![Icône Fermer le plein écran](./assets/pb-icon-reduce.png){width="20"} ).

     ![Attributs personnalisés avec texte d’espace réservé](./assets/pb-product-content-attributes.png){width="600" zoomable="yes"}

1. Faites défiler jusqu’à **[!UICONTROL Description]**, cliquez sur **[!UICONTROL Edit with Page Builder]**, puis ajoutez tout texte que vous souhaitez en appliquant la même méthode que l’étape précédente.

1. Dans le coin supérieur droit de la page du produit, cliquez sur **[!UICONTROL Save]** flèche et choisissez **[!UICONTROL Save & Close]**.

1. Si vous y êtes invité, cliquez sur le bouton **[!UICONTROL Cache Management]** dans le message en haut de la page et actualisez le cache non valide.

### Etape 5 : Visualiser le résultat

1. Accédez à votre page d’exemple de produit dans le storefront.

   Dans cet exemple, le produit se trouve dans le volet de navigation supérieur de Women > Tops > Tees.

1. Faites défiler l’écran vers le bas jusqu’à _Mon attribut Page Builder_ informations.

   La position des attributs sur la page du produit est déterminée par le thème. Dans le thème Luma, les nouveaux attributs sont situés juste après la description du produit.

   ![[!DNL Page Builder] Attributs et de l’éditeur de texte dans le storefront](./assets/pb-storefront-product-attribute.png){width="600" zoomable="yes"}

Vous avez terminé la [!DNL Page Builder] exercice Contenu du catalogue . Conservez le travail que vous avez créé afin que vous puissiez y faire référence ultérieurement.

[1]: https://www.youtube.com/
[2]: https://vimeo.com/
