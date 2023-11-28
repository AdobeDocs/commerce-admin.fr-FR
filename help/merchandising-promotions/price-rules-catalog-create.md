---
title: Créer une règle de prix de catalogue
description: Découvrez comment créer une règle de prix de catalogue qui applique une remise à des produits spécifiques chaque fois qu’un ensemble de conditions est satisfait.
exl-id: 53c5745b-f1c4-4ee8-b995-d2c70f639c7d
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1639'
ht-degree: 0%

---

# Créer une règle de prix de catalogue

Suivez ces instructions pour appliquer une remise à des produits spécifiques chaque fois qu’un ensemble de conditions est satisfait. Les remises des règles de prix du catalogue entrent en vigueur avant que le produit ne soit placé dans le panier.

## Étape 1 : Ajouter une règle

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rule]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Rule]**.

   La variable _[!UICONTROL Rule Information]_comprend des sections extensibles pour **[!UICONTROL Conditions]**et **[!UICONTROL Actions]**.

   ![Règle de prix du catalogue - informations](./assets/price-rule-catalog-new-ee.png){width="700" zoomable="yes"}

1. Procédez comme suit : **[!UICONTROL Rule Name]** et **[!UICONTROL Description]** des champs.

   Ces champs sont réservés à votre référence interne.

1. Définissez la variable **[!UICONTROL Status]** de la règle de prix selon les besoins.

   Par défaut, l’état est `Inactive`.

   >[!NOTE]
   >
   >Une fois la règle créée, son état peut être mis à jour en la définissant sur `Active` ou `Inactive` selon les besoins.

1. Sélectionnez la variable **[!UICONTROL Websites]** où la règle doit être disponible.

1. Sélectionnez la variable **[!UICONTROL Customer Groups]** à laquelle s&#39;applique cette règle.

   Pour sélectionner plusieurs groupes, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

   >[!NOTE]
   >
   >Les options de cette liste dépendent des groupes de clients créés et gérés dans _Clients_ > _Groupes de clients_.

1. ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Saisissez la variable **[!UICONTROL From]** et **[!UICONTROL To]** dates pour déterminer quand la règle de prix est en vigueur.

   Vous pouvez saisir les dates ou utiliser la variable **[!UICONTROL Calendar]** (![Icône Calendrier](../assets/icon-calendar.png)) pour choisir les dates. Si vous laissez les dates vides, la règle est activée lors de l’enregistrement de la règle de prix.

1. Saisissez un nombre pour définir la variable **[!UICONTROL Priority]** de cette règle par rapport aux autres règles.

   >[!NOTE]
   >
   >La variable _[!UICONTROL Priority]_est important lorsque le même produit catalogue répond aux conditions définies pour plusieurs règles de prix. La règle avec le paramètre de priorité le plus élevé (1 étant le plus élevé) devient active pour le produit.

## Etape 2 : définir les conditions

La plupart des conditions disponibles sont basées sur des valeurs d’attribut existantes. Pour appliquer la règle à tous les produits, laissez les conditions vides.

>[!NOTE]
>
>Si au moins un attribut de produit conditionnel a une valeur vide, la règle de prix du catalogue n’est pas appliquée au produit.

>[!NOTE]
>
>Pour appliquer un `Category` condition d’attribut de produit à n’importe quel [lot](../catalog/product-create-bundle.md) ou [groupé](../catalog/product-create-grouped.md) produit, tous les produits enfants doivent être affectés à la même catégorie pour que la règle s’applique correctement. Dans le cas contraire, vous pouvez utiliser une [Règle de prix du panier](price-rules-cart-create.md) à la place.

1. Faire défiler vers le bas et développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Conditions]** .

   La première condition s’affiche par défaut et indique :

   `If **ALL** of these conditions are **TRUE**:`

   ![Règle de prix du catalogue - ligne de condition 1](./assets/catalog-condition1.png){width="400"}

   L’instruction comporte deux liens en gras sur lesquels vous pouvez cliquer pour afficher la sélection des options de cette partie de l’instruction. Vous pouvez créer différentes conditions en modifiant la combinaison de ces valeurs.

1. Modifiez l’instruction de l’une des manières suivantes :

   - Cliquez sur **[!UICONTROL ALL]** et sélectionnez `ALL` ou `ANY`.
   - Cliquez sur **[!UICONTROL TRUE]** et sélectionnez `TRUE` ou `FALSE`.
   - Ne modifiez pas la condition pour appliquer la règle à tous les produits.

   Vous pouvez créer différentes conditions en modifiant la combinaison de ces valeurs. Dans cet exemple, la condition par défaut est utilisée.

1. Cliquez sur le bouton _Ajouter_ (![Icône Ajouter](../assets/icon-add-green-circle.png)) au début de la ligne suivante et sélectionnez une option pour la condition, telle qu’un attribut de produit ou une combinaison de produits.

1. Dans la liste sous **[!UICONTROL Product Attribute]**, choisissez l’attribut que vous souhaitez utiliser comme base de la condition.

   Dans cet exemple, la condition est `Attribute Set`.

   ![Règle de prix du catalogue - ligne de condition 2](./assets/catalog-condition2.png){width="400"}

   >[!NOTE]
   >
   >Pour qu’un attribut apparaisse dans la liste, il doit être configuré pour être utilisé dans les conditions des règles promotionnelles. Pour en savoir plus, voir [Attributs de produit](../catalog/product-attributes.md).

   >[!NOTE]
   >
   >Lors de l’utilisation de la variable `is not one of` avec une condition _SKU_ l’attribut de produit et le produit configurable, les SKU de produit parent et enfant doivent être sélectionnés. Pour éviter de répertorier tous les SKU enfants dans la règle, vous pouvez utiliser la variable `does not contain` condition avec les parties SKU courantes d’un produit configurable et de ses produits enfants.

   La condition sélectionnée s’affiche dans l’instruction, suivie de deux autres liens en gras. Les options diffèrent selon l’attribut de condition que vous sélectionnez. La déclaration dit maintenant :

   `If **ALL** of these conditions are **TRUE**: <br/>Attribute Set **is** …`

1. Cliquez sur **[!UICONTROL is]** et sélectionnez l’opérateur de comparaison qui décrit la condition à remplir.

   Ces options peuvent inclure une option pour différentes comparaisons. Dans cet exemple, les options sont : `is` et `is not`.

1. Sélectionnez ou saisissez des valeurs pour la condition.

   Selon la condition, vous pouvez sélectionner des produits dans une grille ou une liste, saisir une valeur numérique, etc.

   ![Règle de prix du catalogue - ligne de condition 2](./assets/catalog-condition3.png){width="400"}

   L’élément sélectionné apparaît dans l’instruction pour remplir la condition.

   `If **ALL** of these conditions are **TRUE**: <br/> Attribute Set **is Default**`

1. Pour ajouter une autre ligne de condition à l’instruction, cliquez sur le bouton _Ajouter_ (![Icône Ajouter](../assets/icon-add-green-circle.png)) et sélectionnez l’une des options suivantes :

   - `Conditions Combination`
   - `Product Attribute`

   Répétez le processus jusqu’à ce que toutes les conditions souhaitées soient remplies.

   Si vous souhaitez supprimer une partie de l’instruction de condition, cliquez sur le bouton **[!UICONTROL Delete]** (![Icône Supprimer](../assets/icon-delete-red-circle.png) en fin de ligne.

## Etape 3 : définir les actions

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png)la valeur **[!UICONTROL Actions]** et procédez comme suit :

   ![Règle de prix du catalogue - actions](./assets/price-rule-catalog-actions.png){width="600" zoomable="yes"}

1. Sous **[!UICONTROL Pricing Structure Rules]**, définit **[!UICONTROL Apply]** à l’une des options suivantes :

   - `Apply as percentage of original` - Article de réduction en soustrayant un pourcentage du prix normal. Par exemple : saisissez 10 dans Montant de remise pour un prix final qui est marqué à 10 % par rapport au prix normal.
   - `Apply as fixed amount` - Article de réduction en soustrayant un montant fixe du prix normal. Par exemple : saisissez 10 dans Montant de remise pour un prix final qui est 10 $ de moins que le prix normal.
   - `Adjust final price to this percentage` - Ajuste le prix final d&#39;un pourcentage du prix normal. Par exemple : saisissez 25 dans Montant de remise pour un prix final qui est marqué à 75 % par rapport au prix normal.
   - `Adjust final price to discount value` - Définit le prix final sur un montant fixe et actualisé. Par exemple : saisissez 20 dans Montant de remise pour un prix final de 20,00 $.

   >[!NOTE]
   >
   >_Prix régulier_ fait référence au prix de base du produit sans aucune remise promotionnelle (prix spécial/niveau/groupe) ou promotionnelle. _Prix final_ fait référence au prix réduit qui apparaît dans le panier. <br/>La variable **_final_** le prix du produit est calculé comme suit : **_minimum_** prix pertinent, selon la formule suivante : <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

   >[!NOTE]
   >
   >**_Prix fixe_** les options personnalisables du produit sont _not_ affectés par les règles de prix de groupe, de prix de niveau, de prix spécial ou de prix de catalogue ;

1. Saisissez le **[!UICONTROL Discount Amount]**.

1. Pour arrêter le traitement d’autres règles après l’application de cette règle, définissez **[!UICONTROL Discard Subsequent Rules]** to `Yes`.

   >[!NOTE]
   >
   >Définissez cette variable sur `Yes` est une protection qui empêche le système d’appliquer plusieurs remises (règles) au même produit.

## Étape 4 : Ajout de blocs dynamiques associés

{{ee-feature}}

[Blocs dynamiques](../content-design/dynamic-blocks.md) qui sont associés à une règle de prix de catalogue apparaissent dans le storefront chaque fois que les conditions sont remplies. Il s’agit d’une étape facultative.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png)la valeur **[!UICONTROL Related Dynamic Blocks]** .

1. Utilisez la variable [filtres de recherche](../getting-started/admin-workspace.md) pour localiser les blocs dynamiques à associer à la règle.

1. Cochez la case dans la première colonne pour associer le bloc dynamique à la règle.

   ![Règle de prix du catalogue - blocs dynamiques associés](./assets/price-rule-catalog-related-dynamic-blocks.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save and Continue Edit]**.

## Étape 5 : Planification de la règle

{{ee-feature}}

>[!NOTE]
>
>La définition de la règle sur active doit être ajoutée en tant que mise à jour planifiée. Pour en savoir plus, voir [Modifications planifiées](price-rule-catalog-scheduled-changes.md).

1. Dans le _Modifications planifiées_ , cliquez sur **[!UICONTROL Schedule New Update]** en haut de la boîte).

   Si la règle comporte une mise à jour planifiée existante, vous pouvez cliquer sur **[!UICONTROL View/Edit]** à droite de la modification répertoriée.

   Vous pouvez soit modifier la mise à jour existante, soit attribuer la règle de prix du catalogue à une autre campagne. La variable **Modifier la mise à jour existante** est sélectionnée par défaut.

1. Pour planifier la règle, saisissez la variable **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** que la règle de prix doit être active.

   Vous pouvez saisir les dates ou choisir parmi les _Calendrier_ (![Icône Calendrier](../assets/icon-calendar.png)).

   ![Règle de prix du catalogue - calendrier de mise à jour](./assets/price-rule-catalog-schedule-update.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save]**.

1. Dans le _Informations sur la règle_ , définissez la variable **[!UICONTROL Status]** to `active`.

## Étape 6 : enregistrer et tester la règle

1. Une fois la règle terminée, enregistrez-la.

   - ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Cliquez sur **[!UICONTROL Save and Apply]**.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Cliquez sur **[!UICONTROL Save]**.

     La page Informations sur les règles affiche une chronologie mise à jour dans les Modifications planifiées de la règle.

     ![Règles de prix du catalogue - modifications planifiées](./assets/price-rule-scheduled-changes-updated.png){width="600" zoomable="yes"}

1. Mettez à jour les propriétés d’une règle :

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Cliquez sur **[!UICONTROL Edit]** pour afficher la variable _[!UICONTROL Rule Information]_page.

   - ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Cliquez sur la règle dans la liste pour afficher la variable _[!UICONTROL Rule Information]_page.

1. Testez la règle pour vous assurer qu’elle fonctionne correctement.

   Les règles de prix sont automatiquement traitées avec d’autres règles système chaque nuit. Lorsque vous créez une règle de prix, laissez suffisamment de temps pour qu’elle entre dans le système avant de la tester pour s’assurer qu’elle fonctionne correctement. À mesure que de nouvelles règles sont ajoutées, le Commerce recalcule les prix et les priorités en conséquence.

## Démonstration de la règle de prix du catalogue

Regardez cette vidéo pour en savoir plus sur la création de règles de prix de catalogue :

>[!VIDEO](https://video.tv.adobe.com/v/343834?quality=12)

## Descriptions des champs

### [!UICONTROL Rule Information]

| Champ | Description |
|-----|-----------|
| [!UICONTROL Rule name] | (Obligatoire) Le nom de la règle est à titre de référence interne. |
| [!UICONTROL Description] | Une description de la règle doit inclure l’objet de la règle et expliquer comment elle est utilisée. |
| [!UICONTROL Websites] | (Obligatoire) Identifie les sites web sur lesquels la règle peut être utilisée. |
| [!UICONTROL Customer Groups] | (Obligatoire) Identifie les groupes de clients auxquels s’applique la règle. |
| [!UICONTROL Priority] | Un nombre qui indique la priorité de cette règle par rapport aux autres. La priorité la plus élevée est le numéro 1. |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Détermine si la règle est active dans le magasin. Options : `Yes` / `No` |
| [!UICONTROL From] | ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Indique le premier jour où la règle de prix est en vigueur. Si rien n’est indiqué, la règle de prix entre en vigueur lorsqu’elle est enregistrée. |
| [!UICONTROL To] | ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Indique le dernier jour où la règle de prix est en vigueur. Si rien n’est indiqué, la règle de prix continue indéfiniment. |

{style="table-layout:auto"}

### [!UICONTROL Conditions]

Indique les conditions qui doivent être remplies avant que la règle de prix du catalogue ne prenne effet. Si rien n’est indiqué, la règle s’applique à tous les produits.

### [!UICONTROL Actions]

| Champ | Description |
|-----|-----------|
| [!UICONTROL Apply] | Détermine le type de calcul appliqué à l’achat. Options : <br/>**[!UICONTROL Apply as percentage of original]**- Article de réduction en soustrayant un pourcentage du prix normal.<br/>**[!UICONTROL Apply as fixed amount]** - Article de réduction en soustrayant un montant fixe du prix normal. <br/>**[!UICONTROL Adjust final price to this percentage]**- Ajuste le prix final d&#39;un pourcentage du prix normal.<br/>**[!UICONTROL Adjust final price to discount value]** - Définit le prix final sur un montant fixe et actualisé. <br/><br/>**_Remarque :_**Le prix régulier fait référence au prix de base du produit sans aucune remise promotionnelle (promotionnel/de niveau/de groupe) ou promotionnelle. Le prix final fait référence au prix réduit qui apparaît dans le panier. <br/>La variable**_final _**le prix du produit est calculé comme suit :**_minimum _**prix pertinent, selon la formule suivante : <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)` |
| [!UICONTROL Discount Amount] | (Obligatoire) Montant de la remise proposée. |
| [!UICONTROL Discard Subsequent Rules] | Détermine si des règles supplémentaires peuvent être appliquées à cet achat. Pour empêcher que plusieurs remises ne soient appliquées au même achat, sélectionnez `Yes`. Options : `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Related Dynamic Blocks]

{{ee-feature}}

Identifie tout [blocs dynamiques](../content-design/dynamic-blocks.md) qui sont associés à la règle.
