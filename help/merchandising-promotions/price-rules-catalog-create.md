---
title: Créer une règle de prix de catalogue
description: Découvrez comment créer une règle de prix de catalogue qui applique une remise à des produits spécifiques chaque fois qu’un ensemble de conditions est rempli.
exl-id: 53c5745b-f1c4-4ee8-b995-d2c70f639c7d
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 3011d0287c74fd39b44e180733343c39d1cadea7
workflow-type: tm+mt
source-wordcount: '1687'
ht-degree: 0%

---

# Créer une règle de prix de catalogue

Suivez ces instructions pour appliquer une remise à des produits spécifiques chaque fois qu’un ensemble de conditions est rempli. Les remises de la règle de prix catalogue prennent effet avant que le produit ne soit placé dans le panier.

## Étape 1 : ajouter une règle

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rule]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Rule]**.

   La section _[!UICONTROL Rule Information]_&#x200B;comprend des sections extensibles pour les **[!UICONTROL Conditions]**&#x200B;et les **[!UICONTROL Actions]**.

   ![Règle de prix de catalogue - informations](./assets/price-rule-catalog-new-ee.png){width="700" zoomable="yes"}

1. Renseignez les champs **[!UICONTROL Rule Name]** et **[!UICONTROL Description]** .

   Ces champs sont fournis uniquement à titre de référence interne.

1. Définissez la **[!UICONTROL Status]** de la règle de prix selon vos besoins.

   Par défaut, le statut est `Inactive`.

   Une fois la règle créée, son statut peut être mis à jour en le passant sur `Active` ou `Inactive` selon les besoins.

1. Sélectionnez le **[!UICONTROL Websites]** où la règle doit être disponible.

1. Sélectionnez le **[!UICONTROL Customer Groups]** auquel cette règle s’applique.

   - Les options disponibles dépendent des groupes de clients et clientes créés et gérés dans _Clients_ > _Groupes de clients et clientes_.
   - Pour sélectionner plusieurs groupes, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et cliquez sur chaque option.

1. ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Saisissez les dates **[!UICONTROL From]** et **[!UICONTROL To]** pour déterminer quand la règle de prix est en vigueur.

   Vous pouvez saisir les dates ou utiliser la **[!UICONTROL Calendar]** (![icône de calendrier](../assets/icon-calendar.png)) pour choisir les dates. Si vous laissez les dates vides, la règle est activée lorsque la règle de prix est enregistrée.

1. Entrez un nombre pour établir la **[!UICONTROL Priority]** de cette règle par rapport aux autres règles.

   Le paramètre **[!UICONTROL Priority]** détermine la règle qui s’applique lorsqu’un produit répond aux conditions de plusieurs règles de prix. La règle ayant la priorité la plus élevée (numéro le plus bas, par exemple 0, 1, 2, 3...) prend effet.

## Etape 2 : définition des conditions

La plupart des conditions disponibles reposent sur des valeurs d’attribut existantes. Pour appliquer la règle à tous les produits, ne remplissez pas de conditions.

- Si au moins un attribut de produit conditionnel possède une valeur vide, la règle de prix de catalogue n’est pas appliquée au produit.

- Si vous ajoutez `[!UICONTROL Category]` condition d&#39;attribut de produit à des produits groupés ou groupés, la règle de prix n&#39;est correctement appliquée que si tous les articles enfants partagent la même catégorie. Si les articles enfants ne font pas partie de la même catégorie, utilisez plutôt une promotion [Règle de prix du panier](price-rules-cart-create.md) ».

1. Faites défiler vers le bas et développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Conditions]** .

   La première condition apparaît par défaut et stipule :

   `If **ALL** of these conditions are **TRUE**:`

   ![Règle de prix de catalogue - Ligne de condition 1](./assets/catalog-condition1.png){width="400"}

   L&#39;instruction comporte deux liens en gras sur lesquels vous pouvez cliquer pour afficher la sélection d&#39;options pour cette partie de l&#39;instruction. Vous pouvez créer différentes conditions en modifiant la combinaison de ces valeurs.

1. Modifiez l’instruction de l’une des manières suivantes :

   - Cliquez sur **[!UICONTROL ALL]** et sélectionnez `ALL` ou `ANY`.
   - Cliquez sur **[!UICONTROL TRUE]** et sélectionnez `TRUE` ou `FALSE`.
   - Laissez la condition inchangée pour appliquer la règle à tous les produits.

   Vous pouvez créer différentes conditions en modifiant la combinaison de ces valeurs. Pour cet exemple, la condition par défaut est utilisée.

1. Cliquez sur l’icône _Ajouter_ (![Ajouter une icône](../assets/icon-add-green-circle.png)) au début de la ligne suivante et sélectionnez une option pour la condition, telle qu’un attribut de produit ou une combinaison.

1. Dans la liste sous **[!UICONTROL Product Attribute]**, choisissez l’attribut que vous souhaitez utiliser comme base de la condition.

   Pour cet exemple, la condition est `Attribute Set`.

   ![Règle de prix de catalogue - Ligne de condition 2](./assets/catalog-condition2.png){width="400"}

   >[!NOTE]
   >
   >Pour qu’un attribut apparaisse dans la liste, il doit être configuré pour être utilisé dans des conditions de règle promotionnelle. Pour en savoir plus, voir [Attributs du produit](../catalog/product-attributes.md).

   >[!NOTE]
   >
   >Lors de l’utilisation de la condition de `is not one of` avec un attribut de produit _SKU_ et un produit configurable, les SKU du produit parent et enfant doivent être sélectionnés. Pour éviter de répertorier tous les SKU enfants dans la règle, vous pouvez utiliser la condition de `does not contain` avec les composants SKU communs d’un produit configurable et de ses produits enfants.

   La condition sélectionnée apparaît dans l’instruction, suivie de deux autres liens en gras. Les options varient en fonction de l’attribut de condition sélectionné. La déclaration dit maintenant :

   `If **ALL** of these conditions are **TRUE**: <br/>Attribute Set **is** …`

1. Cliquez sur **[!UICONTROL is]** et sélectionnez l’opérateur de comparaison qui décrit la condition à remplir.

   Ces options peuvent inclure une option pour différentes comparaisons. Dans cet exemple, les options sont `is` et `is not`.

1. Sélectionnez ou saisissez des valeurs pour la condition.

   Selon la condition, vous pouvez sélectionner des produits dans une grille ou une liste, saisir une valeur numérique, etc.

   ![Règle de prix de catalogue - Ligne de condition 2](./assets/catalog-condition3.png){width="400"}

   L’élément sélectionné apparaît dans l’instruction pour terminer la condition.

   `If **ALL** of these conditions are **TRUE**: <br/> Attribute Set **is Default**`

1. Pour ajouter une autre ligne de condition à l’instruction, cliquez sur l’icône _Ajouter_ (![Ajouter une icône](../assets/icon-add-green-circle.png)) et choisissez l’une des options suivantes :

   - `Conditions Combination`
   - `Product Attribute`

   Répétez le processus jusqu’à ce que toutes les conditions souhaitées soient remplies.

   Si, à tout moment, vous souhaitez supprimer une partie de l&#39;instruction de condition, cliquez sur l&#39;icône **[!UICONTROL Delete]** (![icône Supprimer](../assets/icon-delete-red-circle.png) à la fin de la ligne.

## Étape 3 : définir les actions

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Actions]** et procédez comme suit :

   ![Règle de prix de catalogue - Actions](./assets/price-rule-catalog-actions.png){width="600" zoomable="yes"}

1. Sous **[!UICONTROL Pricing Structure Rules]**, définissez **[!UICONTROL Apply]** sur l’une des options suivantes :

   - `Apply as percentage of original` - Article bénéficiant d&#39;une remise en soustrayant un pourcentage du prix normal. Par exemple : saisissez la valeur 10 dans le champ Montant de remise pour un prix final marqué en baisse de 10 % par rapport au prix normal.
   - `Apply as fixed amount` - Escompte l&#39;article en soustrayant un montant fixe du prix normal. Par exemple : saisissez la valeur 10 dans le champ Montant de remise pour un prix final inférieur de 10 euros au prix normal.
   - `Adjust final price to this percentage` - Ajuste le prix final d&#39;un pourcentage du prix normal. Par exemple : saisissez 25 dans Montant de remise pour un prix final marqué en baisse de 75 % par rapport au prix normal.
   - `Adjust final price to discount value` - Définit le prix final sur un montant fixe avec remise. Par exemple : saisissez 20 dans Montant de remise pour un prix final de 20 $.

   >[!NOTE]
   >
   >Pour appliquer des remises à montant fixe de manière cohérente sur tous les sites Web avec différentes devises (sans effectuer de conversion à partir de la devise de base globale), définissez l&#39;option **[!UICONTROL Catalog Price Scope]** sur `Website` et définissez une devise de base pour chaque site.

   >[!NOTE]
   >
   >_Prix normal_ fait référence au prix de base du produit sans prix avancé (spécial/niveau/groupe) ni remises promotionnelles. _Prix final_ fait référence au prix réduit qui apparaît dans le panier. <br/>Le prix **_final_** du produit est calculé comme le prix **_minimum_** pertinent, en utilisant la formule suivante : <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

   >[!NOTE]
   >
   >**_Prix fixe_** les options personnalisables du produit ne sont _pas_ affectées par les règles Prix du groupe, Prix de niveau, Prix spécial ou Prix catalogue.

1. Saisissez le **[!UICONTROL Discount Amount]**.

1. Pour arrêter le traitement d’autres règles après l’application de cette règle, définissez **[!UICONTROL Discard Subsequent Rules]** sur `Yes`.

   La définition de cette valeur sur `Yes` permet d’empêcher le système d’appliquer plusieurs remises (règles) au même produit.

## Étape 4 : ajouter des blocs dynamiques associés

{{ee-feature}}

Les [blocs dynamiques](../content-design/dynamic-blocks.md) associés à une règle de prix de catalogue s’affichent dans le storefront chaque fois que les conditions sont remplies. Il s’agit d’une étape facultative.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Related Dynamic Blocks]** .

1. Utilisez le [filtres de recherche](../getting-started/admin-workspace.md) pour localiser les blocs dynamiques à associer à la règle.

1. Cochez la case de la première colonne pour associer le bloc dynamique à la règle.

   ![Règle de prix de catalogue - blocs dynamiques associés](./assets/price-rule-catalog-related-dynamic-blocks.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save and Continue Edit]**.

## Étape 5 : planifier la règle

{{ee-feature}}

>[!NOTE]
>
>La définition de la règle sur active doit être ajoutée en tant que mise à jour planifiée. Pour en savoir plus, voir [Modifications planifiées](price-rule-catalog-scheduled-changes.md).

1. Dans la zone _Modifications planifiées_, cliquez sur **[!UICONTROL Schedule New Update]** en haut de la zone).

   Si la règle comporte une mise à jour planifiée existante, vous pouvez cliquer sur **[!UICONTROL View/Edit]** à droite de la modification répertoriée.

   Vous pouvez modifier la mise à jour existante ou affecter la règle de prix de catalogue à une autre campagne. L’option **Modifier la mise à jour existante** est sélectionnée par défaut.

1. Pour planifier la règle, saisissez le **[!UICONTROL Start Date]** et **[!UICONTROL End Date]** que la règle de prix doit être active.

   Vous pouvez saisir les dates ou choisir les dates dans le _Calendrier_ (![icône Calendrier](../assets/icon-calendar.png)).

   ![Règle de prix de catalogue - mettre à jour le planning](./assets/price-rule-catalog-schedule-update.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save]**.

1. Dans la section _Informations sur les règles_, définissez la **[!UICONTROL Status]** sur `active`.

## Étape 6 : enregistrer et tester la règle

1. Une fois l’opération terminée, enregistrez la règle.

   - ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Cliquez sur **[!UICONTROL Save and Apply]**.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Cliquez sur **[!UICONTROL Save]**.

     La page Informations sur la règle affiche un journal mis à jour dans les modifications planifiées de la règle.

     ![Règles de prix de catalogue - modifications planifiées](./assets/price-rule-scheduled-changes-updated.png){width="600" zoomable="yes"}

1. Mettez à jour les propriétés d’une règle :

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Cliquez sur **[!UICONTROL Edit]** pour afficher la page _[!UICONTROL Rule Information]_.

   - ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Cliquez sur la règle dans la liste pour afficher la page _[!UICONTROL Rule Information]_.

1. Testez la règle pour vous assurer qu’elle fonctionne correctement.

   Les règles de prix sont automatiquement traitées avec d&#39;autres règles système chaque nuit. Lorsque vous créez une règle de prix, patientez suffisamment longtemps pour qu’elle pénètre dans le système avant de la tester pour vérifier qu’elle fonctionne correctement. À mesure que de nouvelles règles sont ajoutées, Commerce recalcule les prix et les priorités en conséquence.

## Démonstration des règles de prix de catalogue

Regardez cette vidéo pour en savoir plus sur la création de règles de prix de catalogue :

>[!VIDEO](https://video.tv.adobe.com/v/3410848?quality=12&learn=on&captions=fre_fr)

## Descriptions des champs

### [!UICONTROL Rule Information]

| Champ | Description |
|-----|-----------|
| [!UICONTROL Rule name] | (Obligatoire) Le nom de la règle est utilisé à des fins de référence interne. |
| [!UICONTROL Description] | Une description de la règle doit inclure l’objectif de la règle et expliquer comment elle est utilisée. |
| [!UICONTROL Websites] | (Obligatoire) Identifie les sites Web où la règle peut être utilisée. |
| [!UICONTROL Customer Groups] | (Obligatoire) Identifie les groupes de clients auxquels la règle s’applique. |
| [!UICONTROL Priority] | Nombre qui indique la priorité de cette règle par rapport aux autres. Les priorités du plus haut au plus bas sont `0,1,2,3...` |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Détermine si la règle est active dans le magasin. Options : `Yes` / `No` |
| [!UICONTROL From] | ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Spécifie le premier jour où la règle de prix est en vigueur. Si rien n’est indiqué, la règle de prix prend effet lors de l’enregistrement. |
| [!UICONTROL To] | ![Magento Open Source](../assets/open-source.svg) (Magento Open Source uniquement) Indique le dernier jour où la règle de prix est en vigueur. Si rien n’est indiqué, la règle de prix se poursuit indéfiniment. |

{style="table-layout:auto"}

### [!UICONTROL Conditions]

Spécifie les conditions qui doivent être remplies avant que la règle de prix catalogue ne soit appliquée. Si rien n’est indiqué, la règle s’applique à tous les produits.

### [!UICONTROL Actions]

| Champ | Description |
|-----|-----------|
| [!UICONTROL Apply] | Détermine le type de calcul appliqué à l&#39;achat. Options : <br/>**[!UICONTROL Apply as percentage of original]**- Article de remises en soustrayant un pourcentage du prix normal.<br/>**[!UICONTROL Apply as fixed amount]** - Escompte l&#39;article en soustrayant un montant fixe du prix normal. <br/>**[!UICONTROL Adjust final price to this percentage]**- Ajuste le prix final d&#39;un pourcentage du prix normal.<br/>**[!UICONTROL Adjust final price to discount value]** - Définit le prix final sur un montant fixe avec remise. <br/><br/>**_Remarque :_**&#x200B;prix normal fait référence au prix de base du produit sans prix avancé (spécial/niveau/groupe) ni remises promotionnelles. Le prix final fait référence au prix réduit qui apparaît dans le panier. <br/>Le prix&#x200B;**_final _**&#x200B;du produit est calculé comme le prix&#x200B;**_minimum _**&#x200B;pertinent, en utilisant la formule suivante : <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)` |
| [!UICONTROL Discount Amount] | (Obligatoire) Montant de la remise proposée. |
| [!UICONTROL Discard Subsequent Rules] | Détermine si des règles supplémentaires peuvent être appliquées à cet achat. Pour empêcher l&#39;application de plusieurs remises au même achat, sélectionnez `Yes`. Options : `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Related Dynamic Blocks]

{{ee-feature}}

Identifie tout [bloc dynamique](../content-design/dynamic-blocks.md) associé à la règle.
