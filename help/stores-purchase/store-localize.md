---
title: Localisation de la boutique
description: Découvrez comment localiser une vue de magasin ou de magasin.
exl-id: 64e1b431-f599-444c-9d39-207bb95f0400
topic: Commerce, Localization
source-git-commit: 248c60b20d8554fc73f94cfd249ac3fd7b677f62
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 0%

---

# Localisation de la boutique

La plupart du texte qui semble codé en dur sur les pages de votre magasin peut être instantanément remplacé par une autre langue en modifiant les paramètres régionaux de la vue. La modification du paramètre régional ne traduit pas réellement le texte mot à mot, mais fait simplement référence à une autre table de traduction qui fournit le texte de l’interface utilisé dans tout le magasin. Le texte qui peut être modifié comprend des titres de navigation, des étiquettes, des boutons et des liens tels que _Mon panier_ et _Mon compte_. Vous pouvez également utiliser l’outil [Traduction en ligne](../configuration-reference/advanced/developer.md) pour toucher du texte dans l’interface.

Les packs de langues se trouvent sous [Traductions et localisation][1]{:target="_blank"} en Commerce Marketplace. Les nouvelles extensions sont continuellement ajoutées à Marketplace. Par conséquent, revenez souvent en arrière.

## Étape 1 : installation d’un module de langue

Suivez les instructions standard d’installation de l’extension du pack de langue. Pour plus d’informations sur l’installation d’une extension, voir [Installation générale de l’interface de ligne de commande][2] dans le _Guide des extensions_.

## Étape 2 : création d’une vue de magasin pour la langue

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Cliquez sur **[!UICONTROL Create Store View]**.

1. Définissez les options de la nouvelle vue de magasin :

   - **[!UICONTROL Store]** — Sélectionnez le magasin qui est le parent de la vue.

   - **[!UICONTROL Name]** — Saisissez un nom pour la vue de magasin. Par exemple : le portugais.

     Dans l’en-tête du magasin, le nom apparaît dans le _sélecteur de langues_.

   - **[!UICONTROL Code]** — Entrez un code en minuscules pour identifier la vue. Par exemple : `portuguese`.

   - **[!UICONTROL Status]** — Pour activer la vue, définissez sur `Enabled`.

   - **[!UICONTROL Sort Order]** — (Facultatif) Saisissez un nombre pour déterminer la séquence dans laquelle cette vue est répertoriée avec d’autres vues.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Store View]**.

## Étape 3 : modification des paramètres régionaux de la vue de magasin

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans la liste déroulante **[!UICONTROL Scope]**, sélectionnez la vue de magasin à configurer, puis cliquez sur **[!UICONTROL OK]** lorsque vous y êtes invité.

1. Sur la page de configuration *[!UICONTROL General]*, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) dans la section **[!UICONTROL Locale Options]** .

1. Décochez la case **[!UICONTROL Use Website]** et définissez **[!UICONTROL Locale]** sur la langue que vous souhaitez affecter à la vue.

   S’il existe plusieurs variantes de la langue, veillez à choisir celle de la région ou du dialecte spécifique.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

   Après avoir modifié la langue des paramètres régionaux, le contenu restant que vous avez créé, y compris les noms et descriptions de produits, les catégories, les pages [CMS](../content-design/page-translate.md) et les blocs, doit être traduit séparément pour chaque vue de magasin.

## Localisation des produits

Si votre boutique comporte plusieurs vues dans différentes langues, les mêmes produits sont disponibles dans chaque vue de magasin. Vous pouvez utiliser les mêmes informations de base sur les produits, telles que le SKU, le prix et le niveau de stock, quelle que soit la langue. Ensuite, traduisez uniquement le nom du produit, les champs de description et les métadonnées selon les besoins pour chaque langue.

### Étape 1 : Traduire les champs de produit

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Dans la grille, recherchez le produit à traduire et ouvrez-le en mode d’édition.

1. Dans le coin supérieur gauche, définissez **[!UICONTROL Store View]** sur l’affichage de la traduction et cliquez sur **[!UICONTROL OK]** lorsque vous êtes invité à confirmer.

1. Pour chaque champ à éditer, procédez comme suit :

   - Décochez la case **[!UICONTROL Use Default Value]** située à droite du champ.

   - collez ou saisissez le texte traduit dans le champ .

   Veillez à traduire tous les champs de texte, y compris les libellés [image](../catalog/catalog-images-video.md) et le texte de remplacement, les champs [Optimisation du moteur de recherche](../catalog/product-search-engine-optimization.md) et toutes les informations [Options personnalisées](../catalog/settings-advanced-custom-options.md).

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

### Étape 2 : Traduire les libellés de champ

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Dans la liste, recherchez l’attribut à traduire et ouvrez-le en mode d’édition.

1. Dans le panneau de gauche, choisissez **[!UICONTROL Manage Labels]**.

1. Dans la section _[!UICONTROL Manage Titles]_, saisissez un libellé traduit pour chaque vue de magasin.

   ![Entrer les étiquettes traduites](./assets/product-attribute-labels-translate.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Attribute]**.

### Etape 3 : Traduire toutes les catégories

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Catalog]** > **Catégories**.

1. Dans le coin supérieur gauche, définissez **[!UICONTROL Store View]** sur l’affichage de la traduction et cliquez sur **[!UICONTROL OK]** lorsque vous êtes invité à confirmer.

1. Dans l&#39;arborescence, recherchez la catégorie à traduire et ouvrez-la en mode d&#39;édition.

1. Pour _Informations de base_, traduisez **[!UICONTROL Category Name]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) de la section _[!UICONTROL Content]_et traduisez **[!UICONTROL Description]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) et traduisez les champs suivants :**[!UICONTROL Search Engine Optimization Settings]**

   - **[!UICONTROL Meta Title]**
   - **[!UICONTROL Meta Keywords]**
   - **[!UICONTROL Meta Description]**

1. Dans la section _[!UICONTROL Search Engine Optimization Settings]_, procédez comme suit pour traduire le **[!UICONTROL URL Key]**:

   - Décochez la case **[!UICONTROL Use Default Value]** située à droite du champ.

   - Saisissez le texte traduit.

   - Assurez-vous que la case **[!UICONTROL Create Permanent Redirect for old URL]** est cochée.

   ![Traduire la clé URL](./assets/category-translate-url-key.png)

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Category]**.

1. Répétez le processus pour toutes les catégories utilisées dans le magasin.

### Étape 4 : traduction des options d’attributs et d’attributs de produit

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Sélectionnez l’attribut à traduire.

1. Sélectionnez **[!UICONTROL Manage Labels]** à gauche et définissez les options **[!UICONTROL Managed Titles]** pour définir les traductions des titres d’attribut.

1. Sélectionnez **[!UICONTROL Properties]** à gauche et saisissez les options d’attribut traduites dans la section **[!UICONTROL Manage Options]** .

   ![Gérer les options](./assets/manage-option-tab.png){width="600" zoomable="yes"}

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Attribute]**.


[1]: https://marketplace.magento.com/extensions/content-customizations/translations-localization.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html
