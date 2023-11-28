---
title: '''[!DNL Page Builder] Présentation partie 2 : blocs'
description: Découvrez la différence entre les blocs simples et les blocs dynamiques lors de l’utilisation de [!DNL Page Builder].
exl-id: 864a3078-8cb3-4add-bdb7-14189aba535e
feature: Page Builder, Page Content
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '2053'
ht-degree: 0%

---

# [!DNL Page Builder] Présentation de la partie 2 : blocs

L’exercice suivant illustre la différence entre [blocs simples](../content-design/blocks.md) et [blocs dynamiques](dynamic-block.md)et comment utiliser [!DNL Page Builder] pour créer chaque type de bloc.

>[!NOTE]
>
>[!DNL Page Builder] possède un nouveau type de contenu appelé _Bannière_, qui apparaît dans le premier exercice pas à pas et n’est pas lié à la fonctionnalité de bannière précédente. Quelle était auparavant l’option Bannière dans [Menu Contenu](../content-design/content-menu.md), est maintenant _Bloc dynamique_.

![Bloc dynamique dans la vitrine](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

Cet exercice suppose que vous avez terminé [Partie 1 : page simple](1-simple-page.md), y compris les conditions préalables et [fichiers d’exemple téléchargés](./assets/simple-page-assets.zip). Suivez les parties de cet exercice pas à pas dans l’ordre.

>[!NOTE]
>
>Ces exercices pratiques sont mis à jour pour prendre en compte les modifications récentes apportées à la variable [!DNL Page Builder] dans la version 2.4.1. Si vous utilisez une version antérieure d’Adobe Commerce, utilisez la variable [!DNL Page Builder] exercices inclus dans la variable [[!DNL Commerce] 2.3 Guide de l’utilisateur](https://docs.magento.com/user-guide/v2.3/cms/page-builder-learn.html).

## Partie 1 : créer un bloc simple

Dans cet exercice de présentation, vous créez un bloc simple avec du contenu provenant de [!DNL Google Maps]. Les blocs simples sont parfois appelés _Blocs CMS_ ou _bloc statique_, car le contenu ne change pas. Un bloc simple est idéal pour le contenu que vous souhaitez peut-être réutiliser.

### Etape 1 : créer un bloc

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Block]**.

1. Pour **[!UICONTROL Block Title]**, saisissez `Google Map`.

1. Pour **[!UICONTROL Identifier]**, saisissez `google-map`.

1. Choisissez la **[!UICONTROL Store View]** où le bloc doit être disponible.

   ![Informations sur le bloc](./assets/pb-tutorial2-block-new-google-map.png){width="600" zoomable="yes"}

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]**.

### Étape 2 : Ajout d’une [!DNL Google Map]

1. Faites défiler l’écran vers le bas jusqu’à [!DNL Page Builder] aperçu du contenu (actuellement vide) et cliquez sur **[!UICONTROL Edit with Page Builder]**.

1. Dans le [!DNL Page Builder] panneau, développer **[!UICONTROL Media]** et faites glisser un **[!UICONTROL Map]** espace réservé sur la scène.

   ![Faire glisser une carte sur la scène](./assets/pb-media-map-drag.png){width="600" zoomable="yes"}

   Une carte de l’emplacement de votre magasin s’affiche si [!DNL Google Maps] est configuré pour votre boutique.

   ![Carte Google configurée pour votre magasin](./assets/pb-tutorial2-google-map.png){width="600" zoomable="yes"}

   Un mappage d’espace réservé apparaît si [!DNL Google Maps] n’est pas encore configuré pour votre magasin.

   ![[!DNL Google Maps] espace réservé](./assets/pb-tutorial2-media-map-not-configured.png){width="600" zoomable="yes"}

1. Dans le coin supérieur droit de l’étape, cliquez sur le bouton _Fermer le plein écran_ (![Icône Fermer le plein écran](./assets/pb-icon-reduce.png)).

   Cliquez sur cette icône pour revenir au _[!UICONTROL Content]_pour le bloc dont l&#39;aperçu est affiché.

1. Dans le coin supérieur droit, cliquez sur le bouton **[!UICONTROL Save]** flèche et choisissez **[!UICONTROL Save & Close]**.

### Étape 3 : Configuration [!DNL Google Maps]

If [!DNL Google Maps] est déjà configuré pour votre magasin, vous pouvez ignorer cette étape et passer à l’étape suivante.

1. Accédez au [Console Google Cloud Platform](https://console.cloud.google.com/google/maps-apis/overview).

1. Cliquez sur la liste déroulante du projet et sélectionnez ou créez le projet pour lequel vous souhaitez ajouter une clé API.

1. Pour configurer vos informations d’identification d’API, suivez les [instructions][1] dans le [!DNL Google Maps] la documentation.

1. Copiez votre clé API dans le Presse-papiers.

1. Revenez au [!DNL Commerce] Admin et accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, sous _[!UICONTROL General]_, choisissez **[!UICONTROL Content Management]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

   ![Outils de contenu avancé](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

   Pour plus d’informations sur la variable [!UICONTROL Content Management Advanced Tools] options de configuration, voir [_Guide de référence de configuration_](../configuration-reference/general/content-management.md).

1. Pour **[!UICONTROL Google Maps API Key]**, collez la clé que vous avez copiée.

1. Cliquez sur **[!UICONTROL Test Key]**.

   En cas de problème avec votre clé, revenez à la variable [!DNL Google Maps] Plateforme pour résoudre le problème. Ensuite, réessayez.

1. Une fois votre clé vérifiée, cliquez sur **[!UICONTROL Save Config]**.

### Etape 4 : Ajouter le bloc à une page

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Dans la grille, recherchez le _[!UICONTROL Simple Page]_que vous avez créé dans le premier tutoriel et sélectionnez **[!UICONTROL Edit]**dans le_[!UICONTROL Action]_ colonne .

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Content]** et cliquez sur **[!UICONTROL Edit with Page Builder]** ou dans la zone d’aperçu du contenu.

1. Dans le [!DNL Page Builder] panneau sous _[!UICONTROL Layout]_, faites glisser un **[!UICONTROL Row]**espace réservé en haut de la scène.

   ![Ajout de la rangée en haut de l’étape](./assets/pb-tutorial2-elements-row-drag-top.png){width="600" zoomable="yes"}

1. Dans le [!DNL Page Builder] panneau, développer **[!UICONTROL Add Content]** et faites glisser un **[!UICONTROL Block]** balise d’emplacement de la nouvelle ligne.

1. Passez la souris sur le conteneur de blocs vide pour afficher la boîte à outils et sélectionnez l’option _Paramètres_ (![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

   ![Blocage d’outil](./assets/pb-add-content-block-toolbox.png){width="600" zoomable="yes"}

1. Sur la page Modifier le bloc , cliquez sur **[!UICONTROL Select Block]**.

   ![Sélectionner un bloc](./assets/pb-add-content-block-settings-block-select.png){width="600" zoomable="yes"}

1. Dans la zone de recherche, saisissez `map` et appuyez sur la touche Entrée/Retour pour trouver le bloc que vous avez créé.

   ![Rechercher un bloc dans la liste](./assets/pb-add-content-block-settings-block-find.png){width="600" zoomable="yes"}

1. Dans la grille, cliquez sur **[!UICONTROL Select]** pour choisir la variable [!DNL Google Maps] bloque.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]** pour enregistrer les paramètres et revenir au [!DNL Page Builder] workspace.

1. Dans le coin supérieur droit de l’étape, cliquez sur le bouton _Fermer le plein écran_ (![Icône Fermer le plein écran](./assets/pb-icon-reduce.png)).

   Cliquez sur cette icône pour revenir au _[!UICONTROL Content]_pour la page avec l’aperçu affiché.

1. Dans le coin supérieur droit, cliquez sur le bouton **[!UICONTROL Save]** flèche et choisissez **[!UICONTROL Save & Close]**.

**Félicitations !** Vous avez terminé la première partie de l’exercice Bloc . Veillez à conserver votre travail à titre de référence.

## Partie 2 : créer un bloc dynamique

Un bloc dynamique comprend une logique qui détermine où, quand et à qui il apparaît. Dans cet exercice pas à pas, vous créez un bloc dynamique pour une promotion qui est déclenchée lorsque les conditions des règles de prix sont remplies et qui ne s’affiche que pour un segment de client spécifique. Le résultat de cet exemple est similaire à la bannière créée lors du premier exercice, mais avec une logique qui contrôle le moment où elle apparaît dans le storefront.

![Exemple de promotion de tee Luma](./assets/pb-tutorial2-dynamic-block-row-page.png){width="600" zoomable="yes"}

### Etape 1 : créer un bloc dynamique

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

   ![Liste Blocs dynamiques](./assets/pb-tutorial2-block-dynamic-add.png){width="700" zoomable="yes"}

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Dynamic Block]**.

   ![Nouvelle page de bloc dynamique](./assets/pb-tutorial2-block-dynamic-new.png){width="600" zoomable="yes"}

1. Renseignez les paramètres de base du nouveau bloc dynamique :

   - Définir **[!UICONTROL Enable Dynamic Block]** to `Yes`.

   - Pour **[!UICONTROL Dynamic Block Name]**, saisissez `Tee Shirt Promo`.

   - Définir **[!UICONTROL Dynamic Block Type]** to `Content Area` et cliquez sur **[!UICONTROL Done]**.

     Le type de bloc dynamique détermine où dans [mise en page](../content-design/page-layout.md) que le bloc est placé. Lors de la configuration d’un bloc dynamique pour votre magasin, tenez compte de la mise en page et de la variable [thème](../content-design/themes.md), afin que vous puissiez utiliser l’espace disponible. Certains magasins disposent d’une zone de contenu active limitée à une largeur fixe, tandis que d’autres étendent la largeur totale de l’écran.

     ![Paramètre Type de bloc dynamique](./assets/pb-dynamic-block-type.png){width="600" zoomable="yes"}

   - Pour **[!UICONTROL Customer Segment]**, cochez la case de chaque segment à appliquer au bloc dynamique et cliquez sur **Terminé** pour enregistrer la liste de segments.

     Dans l’exemple suivant, il existe deux [segments client](../customers/customer-segments.md) qui identifient les clients enregistrés par sexe. Ce bloc dynamique s’affiche uniquement pour les clientes enregistrées qui sont connectées à leurs comptes lorsqu’elles font leurs achats dans votre boutique.

     ![Choix des segments client](./assets/pb-dynamic-block-customer-segment.png){width="600" zoomable="yes"}

### Étape 2 : Définition des paramètres

Faites défiler l’écran vers le bas jusqu’à _[!UICONTROL Content]_, qui affiche une valeur vide [!DNL Page Builder] prévisualisation du contenu, puis cliquez sur **[!UICONTROL Edit with Page Builder]**. Ensuite, effectuez les tâches suivantes :

**Tâche 1 :** Ajout d’une image d’arrière-plan

1. Passez la souris sur le conteneur de rangées pour afficher la boîte à outils et sélectionnez l’option _Paramètres_ (![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

1. Sous _[!UICONTROL Appearance]_, choisissez **[!UICONTROL Full Bleed]**.

1. Pour **[!UICONTROL Minimum Height]**, saisissez `400px`.

1. Faites défiler l’écran jusqu’à _[!UICONTROL Background]_et définissez la variable **[!UICONTROL Background Image]**en cliquant **[!UICONTROL Select from Gallery]**et le choix de la variable `wide-banner-background.png` image téléchargée dans le premier tutoriel.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]** pour appliquer les paramètres et revenir au [!DNL Page Builder] workspace.

   ![Rangée avec l’image](./assets/pb-tutorial2-row-image.png){width="600" zoomable="yes"}

**Tâche 2 :** Ajouter des colonnes

Dans le [!DNL Page Builder] panneau sous _[!UICONTROL Layout]_, faites glisser un **[!UICONTROL Column]**espace réservé sur la ligne.

![Faire glisser le type de colonne sur la ligne](./assets/pb-tutorial2-column-drag.png){width="600" zoomable="yes"}

La ligne est maintenant divisée en deux colonnes de largeur égale.

**Tâche 3 :** Ajouter du texte

1. Dans le [!DNL Page Builder] panneau, développer **[!UICONTROL Elements]** et faites glisser un **Texte** balise d’emplacement de la seconde colonne.

   ![Faire glisser une zone de texte dans la seconde colonne](./assets/pb-tutorial2-column-text-drag.png){width="600" zoomable="yes"}

1. Saisissez les trois lignes de texte suivantes dans l’éditeur :

   `Even more ways to mix and match.`

   `Buy 3 Luma tees and get a 4th free.`

   `Shop Tees >`

   ![Saisie de texte pour la colonne](./assets/pb-tutorial2-column-text-editor.png){width="600" zoomable="yes"}

1. Sélectionnez les trois lignes de texte et utilisez la barre d’outils pour définir la variable **Hauteur de ligne** to `40px`.

   ![Définition de la hauteur de ligne](./assets/pb-tutorial2-column-text-editor-line-height.png){width="600" zoomable="yes"}

1. Définissez la variable **[!UICONTROL Font Size]** pour chaque ligne, comme suit :

   | Ligne | Taille de police |
   |-----| ---------- |
   | Ligne 1 : | `28px` |
   | Ligne 2 : | `24px` |
   | Ligne 3 : | `18px` |

   Comme ce bloc peut être placé n’importe où sur la page, utilisez le style de paragraphe par défaut plutôt que les niveaux d’en-tête. De plus, ne vous inquiétez pas que le texte ne soit pas encore correctement renvoyé à la ligne dans la colonne.  

   ![Texte formaté](./assets/pb-tutorial2-column-text-editor-text-formatted.png){width="600" zoomable="yes"}

**Tâche 4 :** Ajout d’un lien

Lors du premier exercice, vous avez appris à utiliser le [Bouton](buttons.md) type de contenu pour créer un lien. Cet exemple montre comment insérer un lien à partir de la barre d&#39;outils de l&#39;éditeur.

1. Dans un autre onglet du navigateur, ouvrez le storefront et accédez à la page qui doit être la destination cible du lien.

   Vous pouvez utiliser l’URL complète ou une URL relative qui omet la référence à votre domaine de magasin.

   URL complète : `https://mystore.com/women/tops-women/tees-women.html`

   URL relative : `../women/tops-women/tees-women.html`

1. Revenez au [!DNL Page Builder] l’onglet espace de travail et l’éditeur de texte, sélectionnez `Shop Tees >` texte sur la troisième ligne, puis choisissez **Gras** (![Bouton Gras](./assets/editor-btn-bold.png)) dans la barre d’outils de l’éditeur.

1. Avec la variable `Shop Tees >` texte de la troisième ligne toujours sélectionnée, choisissez **Lien d’insertion/de modification** (![Bouton Insérer/Modifier un lien](./assets/pb-icon-add-link.png)) dans la barre d’outils de l’éditeur.

   ![Insérer un lien](./assets/pb-tutorial2-column-text-editor-link-insert.png){width="600" zoomable="yes"}

1. Pour **[!UICONTROL URL]**, saisissez le lien relatif que vous avez préparé.

1. Définir **[!UICONTROL Target]** to `None`.

   Ce paramètre permet d’ouvrir la page dans la même fenêtre du navigateur, plutôt que d’ouvrir un nouvel onglet.

1. Pour **[!UICONTROL Title]**, saisissez `Shop Tees`.

   L’attribut de lien Titre est utilisé par certains navigateurs comme info-bulle.

1. Pour enregistrer le lien et revenir au [!DNL Page Builder] espace de travail, cliquez sur **[!UICONTROL OK]**.

   ![Détails du lien](./assets/pb-tutorial2-column-text-editor-link-insert-detail.png){width="600" zoomable="yes"}

1. Dans le coin supérieur droit de l’étape, cliquez sur le bouton _Fermer le plein écran_ (![Icône Fermer le plein écran](./assets/pb-icon-reduce.png)).

   Cliquez sur cette icône pour revenir au _[!UICONTROL Content]_pour le bloc dynamique avec l&#39;aperçu affiché.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]**.

### Étape 3 : Ajouter une règle de prix

1. Ouvrez le _Promo de la chemise_ bloc dynamique en mode édition à nouveau.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Related Promotions]** et cliquez sur **[!UICONTROL Add Cart Price Rules]**.

   ![Promotions connexes](./assets/pb-dynamic-blocks-related-promotions.png){width="600" zoomable="yes"}

1. Sur le _Ajout de règles de prix de panier connexes_ , cochez la case correspondant au _Achetez 3 t-shirts et obtenez la 4ème offre gratuite_ règle de prix et cliquez sur **[!UICONTROL Add Selected]**.

   ![Ajout d’une règle de prix de panier associée](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

   La règle de prix apparaît dans la variable _Promotions connexes_ sous _Règle de prix du panier connexe_. Vous pouvez associer plusieurs règles de prix à un bloc dynamique. Cependant, cet exemple simple n’en utilise qu’un seul.

   ![Règle de prix du panier sélectionnée](./assets/pb-dynamic-block-related-cart-price-rule-list.png){width="600" zoomable="yes"}

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]**.

### Etape 4 : Ajouter le bloc dynamique à une page

1. Dans le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**

1. Recherchez le _Page simple_ que vous avez créé dans le [premier exercice pas à pas](1-simple-page.md) et ouvrez-la en mode d’édition.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Content]** et cliquez sur **[!UICONTROL Edit with Page Builder]**.

1. Passez la souris sur la rangée supérieure avec la même image que le bloc dynamique pour afficher la boîte à outils et le _Supprimer_ ( ![Icône Supprimer](./assets/pb-icon-remove.png){width="20"} ).

   Pour confirmer la suppression de la ligne de la page, cliquez sur  **[!UICONTROL OK]** .

1. Dans le [!DNL Page Builder] panneau sous _[!UICONTROL Layout]_, faites glisser un nouveau **[!UICONTROL Row]**espace réservé en haut de la scène.

1. Dans le [!DNL Page Builder] panneau, développer **[!UICONTROL Add Content]** et faites glisser un **[!UICONTROL Dynamic Block]** balise d’emplacement de la nouvelle ligne.

   ![Faire glisser un bloc dynamique sur la ligne](./assets/pb-dynamic-block-drag.png){width="600" zoomable="yes"}

1. Passez la souris sur le conteneur de blocs dynamiques pour afficher la boîte à outils et sélectionner l’option _Paramètres_ ( ![Icône Paramètres](./assets/pb-icon-settings.png){width="20"} ).

   ![Boîte à outils de bloc dynamique](./assets/pb-dynamic-block-settings.png){width="600" zoomable="yes"}

1. Sur le _[!UICONTROL Edit Dynamic Block]_page, cliquez sur **[!UICONTROL Select Dynamic Block]**.

   ![Sélectionner un bloc dynamique](./assets/pb-dynamic-block-select.png){width="600" zoomable="yes"}

1. Recherchez le _[!DNL Tee Shirt Promo]_bloc dynamique que vous avez créé et cliquez sur **[!UICONTROL Select]**.

   Un résumé des informations du bloc dynamique apparaît ci-dessous.

   ![Informations sur les blocs dynamiques](./assets/pb-tutorial2-dynamic-block-edit.png){width="600" zoomable="yes"}

1. Acceptation de la valeur par défaut **[!UICONTROL Template]**, `Dynamic Block Block Template`.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]** pour enregistrer les paramètres et revenir au [!DNL Page Builder] workspace.

   ![Bloc dynamique dans l’aperçu de la page](./assets/pb-tutorial2-dynamic-block-on-page.png){width="600" zoomable="yes"}

1. Dans le coin supérieur droit de l’étape, cliquez sur le bouton _Fermer le plein écran_ (![Icône Fermer le plein écran](./assets/pb-icon-reduce.png)).

   Cliquez sur cette icône pour revenir au _[!UICONTROL Content]_pour la page avec l’aperçu affiché.

1. Dans le coin supérieur droit, cliquez sur le bouton **[!UICONTROL Save]** flèche et choisissez **[!UICONTROL Save & Close]**.

Vous avez terminé la deuxième partie de l’exercice Bloc. Veillez à conserver votre travail à titre de référence.

## Partie 3 : mettre à jour le bloc dynamique

Dans cette dernière partie de l’exercice, vous modifiez un bloc dynamique pendant que la page est active dans votre magasin. Ensuite, connectez-vous au magasin en tant que membre du segment client pour faire apparaître le bloc.

![Exemple de bloc dynamique dans le storefront](./assets/pb-tutorial2-dynamic-block-storefront.png){width="600" zoomable="yes"}

### Etape 1 : Editer le bloc dynamique

1. Dans le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

1. Recherchez votre _[!DNL Tee Shirt Promo]_bloc dynamique dans la grille et ouvrez-le en mode édition.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Content]** et cliquez sur **[!UICONTROL Edit with Page Builder]**.

1. Modifiez la largeur de la colonne :

   - Pointez sur la bordure entre les deux colonnes.

   - Maintenez le bouton de la souris enfoncé et faites glisser les deux divisions de la bordure vers la gauche.

     ![Divisions de grille](./assets/pb-tutorial2-dynamic-block-edit-column-width.png){width="600" zoomable="yes"}

     La première colonne est maintenant composée de quatre des 12 (4/12) divisions de grille larges et la seconde de huit des 12 (8/12) divisions larges.

     ![Deux colonnes inégales](./assets/pb-tutorial2-dynamic-block-edit-column-width-changed.png){width="600" zoomable="yes"}

1. Modifiez la couleur du texte :

   - Sélectionnez les deux premières lignes de texte.

   - Dans la barre d’outils de l’éditeur, choisissez **[!UICONTROL Text Color]** et cliquez sur le bouton **[!UICONTROL White]** échantillon.

   ![Couleur du texte](./assets/pb-tutorial2-dynamic-block-edit-text-color.png){width="600" zoomable="yes"}

1. Dans le coin supérieur droit de l’étape, cliquez sur le bouton _Fermer le plein écran_ (![Icône Fermer le plein écran](./assets/pb-icon-reduce.png)).

   Cliquez sur cette icône pour revenir au _[!UICONTROL Content]_pour le bloc dynamique avec l&#39;aperçu affiché.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]**.

### Étape 2 : affichage du bloc dynamique

Ce bloc dynamique n’étant visible que par les membres d’un segment de client spécifique, vous devez vous connecter en tant que client qui est membre du segment de client pour afficher la promotion. Dans cet exemple, le bloc ne s&#39;affiche que pour les clientes féminines.

1. Ouvrez une fenêtre de navigateur sur votre vitrine.

1. Pour afficher votre exemple de page, modifiez l’URL dans la barre d’adresse comme suit :

   mystore.com/sample-page

   Si votre magasin est configuré pour inclure le suffixe html, incluez le suffixe comme suit :

   mystore.com/sample-page.html

1. Se connecter en tant que cliente féminine :

   - Dans le coin supérieur droit de votre page d’accueil, cliquez sur **[!UICONTROL Sign In]**.

   - Si les exemples de données Luma sont installés sur votre système, utilisez les informations d’identification suivantes :

     **[!UICONTROL Email]** - `roni_cost@example.com`

     **[!UICONTROL Password]** -  `roni_cost3@example.com`

   - Cliquez sur **[!UICONTROL Sign In]**.

   - Revenez à la page d&#39;exemple pour voir le bloc dynamique que vous avez créé avec la Promotion de la Tee Shirt.

   ![Bloc dynamique affiché pour un segment de client](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

Vous avez terminé l’exercice Bloc . Veillez à conserver votre travail à titre de référence.

Lorsque vous êtes prêt, passez à [Partie 3 : contenu du catalogue](3-catalog-content.md)

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
