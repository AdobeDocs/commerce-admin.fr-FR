---
title: Définition de la tarification et de la structure du catalogue partagées
description: Avec Adobe Commerce B2B, découvrez comment configurer le prix et la structure d’un catalogue partagé.
exl-id: 67caf56f-1b31-44bb-98dc-ea6ea7d8a4d5
feature: B2B, Companies, Catalog Management
role: Admin
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 0%

---

# Définition de la tarification et de la structure du catalogue partagées

La configuration de la tarification et de la structure d’un catalogue partagé est un processus en deux étapes. Votre emplacement actuel dans le processus est mis en surbrillance avec un numéro dans la barre de progression en haut de la page. Vous pouvez à tout moment afficher l’autre étape du processus en cliquant sur la barre de progression. Par exemple, si vous travaillez sur une tarification personnalisée, vous pouvez revenir à la page de sélection de produits à titre de référence. Cliquez simplement sur **[!UICONTROL Products]** dans la barre de progression en haut de la page, puis cliquez sur **[!UICONTROL Pricing]** pour revenir à la page de tarification personnalisée. Votre travail n&#39;est pas perdu dans ce processus.

![Produits dans le catalogue](./assets/shared-catalog-products-workspace.png){width="700" zoomable="yes"}

Dans l’arborescence de catégories standard, la catégorie racine est le conteneur le plus élevé et est appelée _Catégorie par défaut_ dans les exemples de données. Cependant, lorsque les catalogues partagés sont activés, l’arborescence de catégories comporte un conteneur externe appelé _Catalogue racine_. Le catalogue racine englobe toutes les autres structures de catégorie existant dans le système. Pour plus d’informations, voir [Portée du catalogue](../catalog/introduction.md#catalog-scope).

## Étape 1 : ouverture de la configuration de la structure et du prix du catalogue partagé

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**

1. Pour le catalogue partagé dans la grille, accédez à la _[!UICONTROL Action]_colonne et cliquez sur **[!UICONTROL Set Pricing and Structure]**.

   ![Définition de la tarification et de la structure pour le catalogue partagé](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. La première fois que le catalogue partagé est configuré, cliquez sur **[!UICONTROL Configure]** pour poursuivre en effectuant les étapes suivantes.

## Etape 2 : Sélection des produits

La première étape du processus consiste à choisir les produits que vous souhaitez inclure dans le catalogue partagé. La page de sélection de produits comprend la variable [arborescence de catégories](../catalog/category-create.md) à gauche, et une grille de produit synchronisée à droite. Si vous cliquez sur une catégorie dans l&#39;arborescence, les produits de la catégorie apparaissent dans la grille.

Seules les catégories avec les produits sélectionnés apparaissent dans la variable [navigation supérieure](../catalog/navigation-top.md) lorsque le catalogue partagé est affiché à partir du storefront. Par défaut, seuls les trois premiers niveaux de catégorie sont inclus dans la navigation du storefront, à l’exception de la catégorie racine.

1. Utilisez la variable **Magasin** sélectionnez [scope](../catalog/introduction.md#product-scope) de la configuration.

   La portée de la configuration ne peut être définie qu’avant que le catalogue partagé ne soit enregistré pour la première fois. Si vous modifiez ultérieurement la sélection de produits, le programme de sélection de magasin n’est pas disponible.

   ![Sélectionner un magasin](./assets/shared-catalog-products-scope.png){width="600" zoomable="yes"}

1. Dans l’arborescence des catégories, effectuez l’une des opérations suivantes :

   - Pour inclure tous les produits, cliquez sur **[!UICONTROL Select all]** ou cochez la case de la catégorie parent.
   - Pour inclure des catégories spécifiques de produits, cochez la case de chaque catégorie à inclure.
   - Pour inclure ou exclure un produit individuel, cochez ou désélectionnez la case correspondant.

   La notation sous chaque catégorie de l’arborescence indique le nombre de produits de la catégorie qui sont actuellement inclus dans le catalogue partagé. La notation sous le [catégorie racine](../catalog/category-root.md) affiche le nombre total de produits de toutes les catégories actuellement sélectionnées pour le catalogue partagé.

1. Pour visualiser les produits de la catégorie dans la grille, cliquez sur le nom de la catégorie dans l&#39;arborescence. Lorsqu’une catégorie est sélectionnée, les événements suivants se produisent :

   - Le bouton bascule de la première colonne de la grille est défini sur le vert. _Activé_ position de chaque produit sélectionné.
   - Si un produit est affecté à plusieurs catégories et n’est pas sélectionné dans l’une d’elles, il reste disponible dans les autres catégories, ainsi que lors de l’utilisation de [recherche catalogue](../catalog/search.md).
   - Le système définit automatiquement [Autorisations de catégorie](../catalog/category-permissions.md) to `Allow` pour les produits sélectionnés.

1. Si nécessaire, utilisez les filtres et autres contrôles de grille pour trouver les produits que vous souhaitez inclure dans le catalogue partagé.

   Vous pouvez sélectionner ou omettre individuellement des produits en cliquant sur le bouton de sélection dans la première colonne.

   Si vous sélectionnez une catégorie sans produit, mais liée au contenu CMS ou à un lien externe, elle s’affiche dans la barre de navigation supérieure du storefront.

   Les paramètres de catégorie que vous effectuez ne sont pas enregistrés définitivement dans la base de données tant que la configuration n’a pas été enregistrée. Cependant, elles sont temporairement enregistrées lorsque vous travaillez sur la structure et le prix.

1. Cliquez sur **[!UICONTROL Next]**.

   ![Sélection de produits pour le catalogue](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## Étape 3 : définition de prix personnalisés

Vous pouvez définir une tarification personnalisée pour chaque produit individuellement ou utiliser la variable _[!UICONTROL Action]_contrôle pour définir la tarification personnalisée comme un montant ou un pourcentage fixe pour plusieurs enregistrements de produit.

- **[!UICONTROL Fixed]**: spécifie le prix final du produit. Par exemple, si vous saisissez un prix fixe de 10,00 $, le prix dans la vitrine de la société correspondante est de 10,00 $.

  >[!NOTE]
  >
  >La valeur minimale entre le Prix de base et la valeur fixe saisie est utilisée comme prix final du produit.

  >[!NOTE]
  >
  >**_Prix fixe_** les options personnalisables du produit sont _not_ affectés par les règles de prix de groupe, de prix de niveau, de prix spécial ou de prix de catalogue ;

- **[!UICONTROL Percentage]**: détermine le prix personnalisé en fonction du pourcentage de remise. Par exemple, pour offrir une remise de 10 %, définissez le type de prix personnalisé sur `Percentage` et saisissez `10`. Le prix personnalisé escompté est 90 % du prix du produit d’origine.

Pour définir la remise sur un montant fixe ou un pourcentage pour les types de produits suivants, utilisez la variable _[!UICONTROL Custom Price]_dans la grille :

- [Simple](../catalog/product-create-simple.md) (y compris les variations de produit configurables)
- [Bundle](../catalog/product-create-bundle.md)
- [Téléchargeable](../catalog/product-create-downloadable.md)
- [Virtuel](../catalog/product-create-virtual.md)

La colonne Prix personnalisé est vide pour la variable [configurable](../catalog/product-create-configurable.md) et [groupé](../catalog/product-create-grouped.md) types de produits et pour [cartes cadeau](../catalog/product-gift-card-create.md).

La sélection de produits dans la grille ne peut pas être modifiée à partir de la fonction _Prix personnalisés_ page. Vous pouvez toutefois utiliser l’indicateur de progression en haut de la page pour revenir à l’étape précédente et modifier la sélection de produits.

![Sélection de produits pour le catalogue](./assets/shared-catalog-custome-prices-step-3.png){width="600" zoomable="yes"}

### Appliquer un prix personnalisé

1. Pour une installation multi-site, définissez **[!UICONTROL Website]** sur le site web où les prix personnalisés s’appliquent.

   ![Choisir le site web](./assets/shared-catalog-scope-pricing.png){width="600" zoomable="yes"}

1. Utilisez l’une des méthodes suivantes pour sélectionner les produits auxquels s’applique la tarification personnalisée.

   - Utilisez l’arborescence des catégories pour sélectionner tous les produits d’une catégorie spécifique.
   - Définissez la variable _[!UICONTROL Mass Actions]_dans l’en-tête pour `Select All`.
   - Cochez la case correspondant aux produits individuels.

   La grille affiche les produits des catégories actuellement sélectionnées. Vous pouvez utiliser les commandes standard pour rechercher des produits et filtrer la liste.

   ![Tout sélectionner](./assets/shared-catalog-custom-pricing-mass-actions.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Actions]** à l’une des options suivantes :

   - `Set Discount` - Applique un pourcentage de remise à tous les produits sélectionnés. Chaque prix de produit affecté s’affiche sous la forme d’une **_rabais_** prix.
   - `Adjust Fixed Price` - Applique un pourcentage de remise fixe sur tous les produits sélectionnés. Chaque prix de produit affecté s’affiche sous la forme d’une **_fixed_** prix.

   ![Contrôle des actions - Définir la remise](./assets/shared-catalog-set-custom-prices-discount-action.png){width="600" zoomable="yes"}

1. Lorsque vous y êtes invité, saisissez la remise ou l’ajustement de prix, puis cliquez sur **[!UICONTROL Apply]**.

   ![Définir la remise](./assets/shared-catalog-set-custom-prices-discount.png){width="400"}<br/>

   ![Ajuster le prix fixe](./assets/shared-catalog-set-custom-fixed-prices.png){width="400"}

   La remise est appliquée à tous les produits sélectionnés, et la variable _Prix personnalisé_ reflète le type de remise et le montant appliqué.

   ![Colonne de prix personnalisée avec remise](./assets/shared-catalog-set-custom-prices-discount-applied.png){width="600" zoomable="yes"}

### Appliquer un prix de niveau

[Prix de niveau](../catalog/product-price-tier.md) vous permet d’offrir une remise en quantité sur les produits du catalogue partagé. La variable _Prix de niveau_ de la grille contient un lien vers la _Tarifs avancés_ options qui s’appliquent spécifiquement au catalogue partagé. Si le produit comprend déjà le niveau de prix, le nombre de niveaux existants s’affiche entre parenthèses après le lien.

Les instructions suivantes expliquent comment appliquer un niveau de prix à un seul produit. Pour appliquer des tarifs de niveau à plusieurs produits, reportez-vous à la section [Prix du niveau d&#39;import](../systems/data-import-price-tier.md).

1. Pour le produit dans la grille, accédez à la _Prix de niveau_ colonne et cliquez sur **[!UICONTROL Configure]**.

   ![Configurer le prix de niveau](./assets/shared-catalog-tier-price-configure.png){width="600" zoomable="yes"}

1. Sur le _Tarifs avancés_ page, cliquez sur **[!UICONTROL Add Price]** et procédez comme suit :

   ![Catalogue et prix de niveau](./assets/shared-catalog-tier-price-configure-add-price.png){width="600" zoomable="yes"}

   - Définir **[!UICONTROL Website]** sur le site web où s’applique le prix du niveau.
   - Saisissez la quantité de produit à acheter pour bénéficier de la remise.
   - Définir **[!UICONTROL Price]** à l’un des types de remise suivants :
      - `Fixed`
      - `Discount`
   - Saisissez le montant de la remise.
   - Pour accéder à un autre niveau, cliquez sur **Ajouter un prix** et répétez le processus pour définir le niveau suivant.

   ![Prix à plusieurs niveaux](./assets/shared-catalog-tier-price-configure-multiple-tiers.png){width="600" zoomable="yes"}

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Done]**.

   Dans la grille, le nombre de niveaux est indiqué entre parenthèses dans le _[!UICONTROL Tier Price]_colonne .

   ![Plusieurs niveaux](./assets/shared-catalog-tier-price-configure-parentheses.png){width="600" zoomable="yes"}

## Enregistrer la structure et le prix

Une fois la tarification personnalisée terminée, cliquez sur **[!UICONTROL Generate Catalog]** then **[!UICONTROL Save]**.

Le catalogue partagé est maintenant enregistré dans la base de données. Son nom apparaît dans la variable _[!UICONTROL Shared Catalog]_de la colonne_[!UICONTROL Products]_ grid. L’étape suivante consiste à [affecter le catalogue partagé à une entreprise ;](./catalog-shared-assign-companies.md).
