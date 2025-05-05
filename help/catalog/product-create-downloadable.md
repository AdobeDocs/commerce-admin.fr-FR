---
title: Produit téléchargeable
description: Découvrez comment créer un produit téléchargeable qui peut être diffusé sous la forme d’un fichier numérique.
exl-id: c3dd4c5f-adc1-4a8f-a9da-7f0dedd1ee34
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1622'
ht-degree: 0%

---

# Produit téléchargeable

Un produit téléchargeable peut être tout ce que vous pouvez diffuser sous forme de fichier, par exemple un livre électronique, de la musique, une vidéo, une application logicielle ou une mise à jour. Vous pouvez proposer un album à vendre et vendre chaque chanson individuellement. Vous pouvez également utiliser un produit téléchargeable pour diffuser une version électronique de votre catalogue de produits.

Le téléchargement n’étant disponible qu’après l’achat, vous pouvez fournir des exemples, tels qu’un extrait d’un livre, un clip d’un fichier audio ou une bande-annonce d’une vidéo. Le client peut essayer un échantillon avant d’acheter le produit. Les fichiers que vous proposez peuvent être téléchargés sur votre serveur ou depuis un autre serveur.

![Produit téléchargeable](./assets/storefront-product-downloadable.png){width="700" zoomable="yes"}

Les produits téléchargeables peuvent être configurés de manière à exiger que le client se connecte à un compte pour recevoir le lien ou qu’il puisse être envoyé par courrier électronique et partagé avec d’autres utilisateurs. L’état de la commande avant que le téléchargement ne soit disponible, les valeurs par défaut et d’autres options de remise sont définies dans la configuration. Lorsque vous planifiez vos ajouts de catalogue téléchargeables, prenez note des éléments suivants :

- Les produits téléchargeables peuvent être téléchargés sur le serveur ou liés à un autre serveur sur Internet.

- Vous pouvez déterminer le nombre de fois où un client peut télécharger un produit.

- Les clients qui achètent un produit téléchargeable peuvent avoir besoin de se connecter avant de passer en caisse.

- La livraison d’un produit téléchargeable peut être effectuée lorsque la commande est à l’état `Pending` ou `Invoiced`.

- Comme les produits téléchargeables ne sont pas livrés, l’étape _Expédition_ du passage en caisse est ignorée lorsque le panier contient uniquement le produit téléchargeable.


## Configuration des options de téléchargement

Les paramètres de configuration téléchargeables déterminent les valeurs par défaut et les options de remise des produits téléchargeables, et déterminent si les invités peuvent acheter des téléchargements.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et sélectionnez **[!UICONTROL Catalog]** sous .

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur _[!UICONTROL Downloadable Product Options]_.

   ![Options de produit téléchargeables](../configuration-reference/catalog/assets/catalog-downloadable-product-options.png){width="700" zoomable="yes"}

   Pour obtenir la liste détaillée de ces options de configuration, voir [_Options de produit téléchargeables_](../configuration-reference/catalog/catalog.md#downloadable-product-options) dans la _référence de configuration_.

1. Pour déterminer l’état du processus de commande lorsque le téléchargement devient disponible, définissez **[!UICONTROL Order Item Status to Enable Downloads]** sur l’une des options suivantes :

   - `Pending`
   - `Invoiced`

1. Pour définir une limite par défaut sur le nombre de téléchargements qu’un seul client peut effectuer, saisissez le nombre **[!UICONTROL Default Maximum Number of Downloads]**.

1. Définissez **[!UICONTROL Shareable]** sur l’une des options suivantes :

   - `Yes` - Permet aux clients d’envoyer par courrier électronique le lien de téléchargement à d’autres personnes.
   - `No` - Empêche les clients de partager le lien de téléchargement avec d’autres en exigeant qu’ils se connectent à leurs comptes pour accéder aux liens de téléchargement.

1. Pour **[!UICONTROL Default Sample Title]**, saisissez l’en-tête qui doit apparaître au-dessus de la sélection des exemples.

   ![Exemple de titre](./assets/product-downloadable-config-sample-title.png){width="400"}

1. Pour **[!UICONTROL Default Link Title]**, saisissez le texte par défaut à utiliser pour les liens de téléchargement.

1. Si vous souhaitez que le lien de téléchargement s’ouvre dans une nouvelle fenêtre du navigateur, définissez **[!UICONTROL Opens Links in New Window]** sur `Yes`.

   Ce paramètre permet de garder ouverte la fenêtre du navigateur pour votre magasin.

1. Pour déterminer comment le contenu téléchargeable est diffusé, définissez **[!UICONTROL Use Content Disposition]** sur l’une des options suivantes :

   - `Attachment` - Délivre le lien de téléchargement par courrier électronique en tant que pièce jointe.
   - `Inline` - Diffuse le lien de téléchargement sous forme de lien sur une page web.

1. Si vous souhaitez que les acheteurs s’inscrivent à un compte client et se connectent avant d’acheter un téléchargement, définissez **[!UICONTROL Disable Guest Checkout if Cart Contains Downloadable Items]** sur `Yes`.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

## Créer un produit téléchargeable

Les instructions suivantes montrent le processus de création d’un produit téléchargeable à l’aide d’un [modèle de produit](attribute-sets.md), de champs obligatoires et de paramètres de base. Chaque champ obligatoire est marqué d’un astérisque rouge (`*`). Lorsque vous avez terminé les étapes de base, vous pouvez définir les autres paramètres du produit selon vos besoins.

>[!NOTE]
>
>Les noms de fichiers téléchargeables peuvent inclure des lettres et des chiffres. Un tiret ou un trait de soulignement peut être utilisé pour représenter un espace entre les mots. Les caractères non valides du nom de fichier sont remplacés par un trait de soulignement.

### Etape 1 : Sélection du type de produit

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Dans le menu _[!UICONTROL Add Product]_( ![Flèche de menu](../assets/icon-menu-down-arrow-red.png){width="25"} ) dans le coin supérieur droit, choisissez `Downloadable Product`.

   ![Ajouter un produit téléchargeable](./assets/product-add-downloadable.png){width="700" zoomable="yes"}

### Étape 2 : sélection du jeu d’attributs

Les exemples de données incluent un [jeu d’attributs](attribute-sets.md) appelé _Téléchargeable_ qui comporte des champs spéciaux pour les produits téléchargeables. Vous pouvez utiliser un modèle existant ou en créer un autre avant l’enregistrement du produit.

Pour choisir le jeu d’attributs utilisé comme modèle pour le produit, effectuez l’une des opérations suivantes :

- Pour **[!UICONTROL Search]**, saisissez le nom du jeu d’attributs.

- Dans la liste, choisissez l’ensemble d’attributs `Downloadable`.

Le formulaire est mis à jour pour refléter la modification.

![Choisir un jeu d’attributs](./assets/product-create-choose-attribute-set-downloadable.png){width="600" zoomable="yes"}

### Étape 3 : Définissez les paramètres requis

1. Saisissez le **[!UICONTROL Product Name]**.

1. Acceptez la valeur par défaut **[!UICONTROL SKU]** basée sur le nom du produit ou saisissez-en une autre.

1. Saisissez le produit **[!UICONTROL Price]**.

1. Comme le produit n’est pas encore prêt à être publié, définissez **[!UICONTROL Enable Product]** sur `No`.

1. cliquez sur **[!UICONTROL Save]** et continuez.

   Lorsque le produit est enregistré, le programme de sélection [Affichage magasin](introduction.md#product-scope) s’affiche dans le coin supérieur gauche.

1. Sélectionnez l’ **[!UICONTROL Store View]** où le produit doit être disponible.

   ![Choisir la vue de magasin](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### Étape 4 : définition des paramètres de base

1. Définissez **[!UICONTROL Tax Class]** sur l’une des options suivantes :

   - `None`
   - `Taxable Goods`

1. Saisissez le **[!UICONTROL Quantity]** du produit en stock.

   Prenez note des points suivants :

   - Par défaut, **[!UICONTROL Stock Status]** est défini sur `Out of Stock`.

   - Comme les produits téléchargeables ne sont pas livrés, le champ **[!UICONTROL Weight]** n’est pas utilisé. Si vous activez cette fonctionnalité, elle devient un [produit simple](product-create-simple.md) et le _Est-ce que ce produit téléchargeable ?L’onglet_ ne peut pas être utilisé.

   >[!NOTE]
   >
   >Si vous activez [Inventory management](../inventory-management/introduction.md), les vendeurs Source uniques définissent la quantité dans cette section. Les marchands multi-Source ajoutent des sources et des quantités dans la section Sources . Voir la section suivante _Attribuer des sources et des quantités (Inventory management)_ .

1. Acceptez le paramètre par défaut **[!UICONTROL Visibility]** de `Catalog, Search`.

1. Pour afficher le produit dans la [liste des nouveaux produits](../content-design/widget-new-products-list.md), cochez la case **[!UICONTROL Set Product as New]** .

1. Pour attribuer _[!UICONTROL Categories]_&#x200B;au produit, cliquez sur la zone **[!UICONTROL Select…]**&#x200B;et effectuez l’une des opérations suivantes :

   **Choisissez une catégorie existante** :

   - Commencez à taper dans la zone jusqu’à ce que vous trouviez une correspondance.

   - Cochez la case de chaque catégorie à attribuer.

   **Créer une catégorie** :

   - Cliquez sur **[!UICONTROL New Category]**.

   - Saisissez le **[!UICONTROL Category Name]** et choisissez le **[!UICONTROL Parent Category]**, qui détermine sa position dans la [structure de menu](category-root.md).

   - Cliquez sur **[!UICONTROL Create Category]**.

1. Définissez **[!UICONTROL Format]** sur l’une des options suivantes :

   - `Download`
   - `DVD`

   Si nécessaire, vous pouvez modifier l’ [attribut](attribute-product-create.md) pour ajouter d’autres valeurs.

   Il peut y avoir des attributs supplémentaires qui décrivent le produit. La sélection varie en fonction de l’ensemble d’attributs. Vous pouvez la terminer ultérieurement.

#### Affecter des sources et des quantités ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

### Étape 5 : renseigner les informations téléchargeables

Faites défiler l’écran vers le bas, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) de la section _[!UICONTROL Downloadable Information]_&#x200B;et cochez la case **[!UICONTROL Is this downloadable product?]**.

Lorsqu’elle est activée, la section _[!UICONTROL Downloadable Information]_&#x200B;comporte deux parties. La première partie décrit chaque lien de téléchargement et la seconde partie décrit chaque fichier d’exemple. La valeur par défaut de la plupart de ces options peut être définie dans la [configuration](#configure-the-download-options).

![Informations téléchargeables](./assets/product-downloadable-information.png){width="600" zoomable="yes"}

#### Remplir les liens

1. Dans la section _[!UICONTROL Links]_, saisissez le **[!UICONTROL Title]**&#x200B;que vous souhaitez utiliser comme en-tête pour les liens de téléchargement.

1. Le cas échéant, cochez la case **[!UICONTROL Links can be purchased separately]** .

1. Cliquez sur **[!UICONTROL Add Link]** et procédez comme suit :

   - Saisissez les **[!UICONTROL Title]** et **[!UICONTROL Price]** du téléchargement.

   - Pour les fichiers **[!UICONTROL File]** et **[!UICONTROL Sample]**, choisissez l’une des méthodes de distribution suivantes pour les téléchargements :

      - `Upload File` - Choisissez cette méthode pour charger le fichier de distribution sur le serveur. Accédez au fichier et sélectionnez-le pour le transfert.
      - `URL` - Choisissez cette méthode pour accéder au fichier de distribution à partir d’une URL. Saisissez l’URL complète vers le fichier de téléchargement.

   >[!NOTE]
   >
   >Vous ne pouvez pas utiliser de liens vers des ressources externes comme produits téléchargeables. Les domaines de lien valides sont prédéfinis par programmation dans le fichier `env.php` (voir [référence env.php](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/files/config-reference-envphp.html) dans le _Guide de configuration_).

   - Définissez **[!UICONTROL Shareable]** sur l’une des options suivantes :

      - `No` - Nécessite que les clients se connectent à leurs comptes pour accéder au lien de téléchargement.

      - `Yes` - Envoie le lien par courrier électronique, que les clients peuvent partager avec d’autres personnes.

      - `Use Config` - Utilise la méthode spécifiée dans la configuration [Options de produit téléchargeable](../configuration-reference/catalog/catalog.md) .

   - Effectuez l’une des opérations suivantes :

      - Pour limiter les téléchargements par client, saisissez le nombre maximal pour **[!UICONTROL Max. Downloads]**.
      - Pour autoriser un nombre illimité de téléchargements, cochez la case **[!UICONTROL Unlimited]** .

   ![Détails du lien](./assets/product-downloadable-link-detail.png){width="600" zoomable="yes"}

1. Pour ajouter un autre lien, cliquez sur **[!UICONTROL Add Link]** et répétez ces étapes.

#### Remplissage des exemples

1. Dans la section _[!UICONTROL Samples]_, saisissez le **[!UICONTROL Title]**&#x200B;que vous souhaitez utiliser comme en-tête pour les exemples.

1. Pour renseigner les informations de chaque échantillon, cliquez sur **[!UICONTROL Add Link]**.

   ![Exemples](./assets/product-downloadable-samples.png){width="600" zoomable="yes"}

1. Renseignez le détail du lien comme suit :

   - Saisissez le **[!UICONTROL Title]** de l’échantillon individuel.

   - Choisissez l&#39;une des méthodes de distribution suivantes :

      - `Upload File` - Choisissez cette méthode pour charger le fichier de distribution sur le serveur. Accédez au fichier et sélectionnez-le pour le transfert.
      - `URL` - Choisissez cette méthode pour accéder au fichier de distribution à partir d’une URL. Saisissez l’URL complète vers le fichier de téléchargement.

   - Pour ajouter un autre exemple, cliquez sur **[!UICONTROL Add Link]** et répétez ces étapes.

   - Pour modifier l’ordre des exemples, appuyez sur l’icône _Modifier l’ordre_ ( ![Contrôleur de position](../assets/icon-sort-order.png) ) et faites glisser l’échantillon vers une nouvelle position.

### Étape 6 : renseigner les informations sur le produit

Faites défiler l’écran vers le bas et renseignez les informations des sections suivantes selon vos besoins :

- [Contenu](product-content.md)
- [Images et vidéos](product-images-and-video.md)
- [Optimisation du moteur de recherche](product-search-engine-optimization.md)
- [Produits associés, ventes consécutives et ventes croisées](related-products-up-sells-cross-sells.md)
- [Options personnalisables](settings-advanced-custom-options.md)
- [Produits sur les sites web](settings-basic-websites.md)
- [Conception](settings-advanced-design.md)
- [Options de cadeau](product-gift-options.md)

### Étape 7 : Publish du produit

Si vous êtes prêt à publier le produit dans le catalogue, définissez **[!UICONTROL Enable Product]** sur `Yes` et effectuez l’une des opérations suivantes :

**Méthode 1 :** Enregistrer et prévisualiser

- Dans le coin supérieur droit, cliquez sur **[!UICONTROL Save]**.

- Pour afficher le produit dans votre boutique, sélectionnez **[!UICONTROL Customer View]** dans le menu _Admin_ ( ![Flèche de menu](../assets/icon-menu-down-arrow-black.png) ).

  Le magasin s’ouvre dans un nouvel onglet du navigateur.

  ![Affichage client](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

**Méthode 2 :** Enregistrer et fermer

Dans le menu _[!UICONTROL Save]_( ![Flèche de menu](../assets/icon-menu-down-arrow-red.png){width="25"} ), choisissez **[!UICONTROL Save & Close]**.

## Expérience Storefront

Dans le tableau de bord du compte client, la page _[!UICONTROL My Downloadable Products]_&#x200B;pointe vers chaque commande de produits téléchargeables. Les téléchargements deviennent disponibles à partir du compte du client lorsque la commande est terminée.

![Mes produits téléchargeables](./assets/customer-account-my-downloadable-products.png){width="700" zoomable="yes"}

Le tableau suivant décrit les valeurs de _Mes produits téléchargeables_ :

| Colonne | Description |
|--- |--- |
| [!UICONTROL Order#] | [order](../stores-purchase/orders.md) dans lequel le produit téléchargeable a été acheté. Fournit un lien vers le détail de la commande. |
| [!UICONTROL Date] | Date de création de la commande. |
| [!UICONTROL Title] | Nom du produit téléchargeable acheté avec la commande. Fournit un lien vers le produit téléchargeable. |
| [!UICONTROL Status] | État du traitement des commandes. |
| [!UICONTROL Remaining Downloads] | Nombre de téléchargements disponibles du produit téléchargé. |

_&#x200B;**Pour télécharger un fichier de produit à partir du tableau de bord du compte**&#x200B;_

1. Dans le tableau de bord de leur compte, le client choisit **[!UICONTROL My Downloadable Products]**.

1. Recherche l’ordre dans la liste et clique sur le lien situé après le titre.

1. Dans le coin inférieur droit de la fenêtre de téléchargement, cliquez sur l’icône _télécharger_ .

1. Localise le fichier à l’emplacement de téléchargement et enregistre le fichier à l’emplacement souhaité.
