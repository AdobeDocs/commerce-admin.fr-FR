---
title: Réseaux sociaux et flux RSS
description: Découvrez comment ajouter des médias sociaux et d’autres intégrations de flux RSS pour accroître la notoriété de la marque et des produits.
exl-id: e4a48870-f53e-4848-8faa-8f2aedaf53b7
feature: Merchandising, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 0%

---

# Réseaux sociaux et flux RSS

De nombreux commerçants utilisent les médias sociaux et d&#39;autres outils numériques pour sensibiliser la marque et les produits. Vous pouvez intégrer votre boutique à vos réseaux sociaux en installant une extension Marketplace ou en ajoutant un module externe à vos pages de contenu. Utilisez des flux RSS pour publier les informations sur vos produits sur les sites d’agrégation d’achats et les inclure même dans vos newsletters. Les clients peuvent s’abonner à vos flux RSS pour en savoir plus sur les nouveaux produits et promotions.

## Réseaux sociaux

Votre magasin peut être connecté aux réseaux sociaux en installant un [Extension Marketplace](../getting-started/commerce-marketplace.md). En outre, vous pouvez facilement ajouter des modules externes de réseaux sociaux, tels que le _Comme_ à des blocs CMS qui peuvent être incorporés dans des pages dans votre magasin.

Les sites de réseau social disposent de nombreux modules externes qui peuvent facilement être ajoutés à votre boutique. En outre, de nombreuses extensions sur le Commerce Marketplace peuvent être utilisées pour intégrer votre boutique aux médias sociaux. L’exemple suivant montre comment ajouter un Facebook _Comme_ à votre boutique.

>[!NOTE]
>
>Adobe Commerce a supprimé le paramètre natif _Social Magento_ Intégration de facebook et ne prend plus en charge l’extension . Accédez au [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=Facebook){:target=&quot;_blank&quot;} pour localiser d’autres extensions pour l’intégration Facebook.

### Étape 1. Obtention du code de bouton

1. Sur le site web des développeurs de métadonnées, accédez au [configuration des boutons](https://developers.facebook.com/docs/plugins/like-button) page.

1. Pour **[!UICONTROL URL to Like]**, saisissez l’URL de la page de votre magasin vers laquelle vous souhaitez que les utilisateurs _Comme_.

   Par exemple, vous pouvez saisir l’URL de la page d’accueil de votre magasin.

1. Choisissez la **[!UICONTROL Layout]** pour le bouton .

1. Saisissez le **[!UICONTROL Width]** en pixels disponibles sur votre site pour le bouton et tout message texte associé.

1. Définir **[!UICONTROL Action Type]** à l’une des options suivantes :

   - `Like`
   - `Recommend`

1. Cliquez sur **[!UICONTROL Get Code]** pour copier le code généré dans le presse-papiers.

### Étape 2. Création d’un bloc de contenu

1. Revenez à l’administrateur de votre boutique.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Block]**.

1. Saisissez un texte descriptif. **[!UICONTROL Block Title]** pour référence interne.

   Par exemple: `Facebook Like Button`.

1. Attribution d’une **[!UICONTROL Identifier]** au bloc, en utilisant tous les caractères minuscules et les traits de soulignement au lieu des espaces.

   Par exemple: `facebook_like_button`.

1. Si votre instance Commerce présente plusieurs vues de magasin, sélectionnez chacune d’elles. **[!UICONTROL Store View]** où le bloc doit être disponible.

1. Ajoutez le fragment de code au contenu du bloc, en fonction de votre outil de contenu :

   - Lorsque vous utilisez [!DNL Page Builder], ajoutez une [Code HTML](../page-builder/html-code.md) bloquez sur la scène et collez le fragment de code que vous avez copié à partir du site Facebook. Sinon, collez le fragment de code dans le **[!UICONTROL Content]** de la boîte.

   - Avec l’éditeur, collez le fragment de code que vous avez copié à partir du site Facebook dans le **[!UICONTROL Content]** de la boîte.

1. Si le bloc n’est pas prêt à être mis en ligne, définissez **[!UICONTROL Enable Block]** to `No`.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Block]**.

### Étape 3. Placez le bloc

1. Ajoutez le bloc, en fonction de votre outil de contenu :

   - Lorsque vous utilisez [!UICONTROL Page Builder], suivez les instructions de la section [ajouter le bloc](../page-builder/block.md) sur la scène.

   - Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Widget]** et procédez comme suit :

   - ![B2B pour Adobe Commerce](../assets/b2b.svg) (Disponible avec B2B pour Adobe Commerce uniquement) Dans le _Paramètres_ , définissez **[!UICONTROL Type]** to `CMS Static Block` et cliquez sur **[!UICONTROL Continue]**.

   - Vérifiez que **[!UICONTROL Design Theme]** est définie sur le thème actif.

   - Cliquez sur **[!UICONTROL Continue]**.

1. Dans le **[!UICONTROL Storefront Properties]** , procédez comme suit :

   - Pour **[!UICONTROL Widget Title]**, saisissez un titre de référence interne.

   - Définir **[!UICONTROL Assign to Store Views]** to `All Store Views`ou à la vue dans laquelle vous souhaitez que l’application soit disponible. Pour sélectionner plusieurs vues, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

   - Saisissez un nombre dans le champ **[!UICONTROL Sort Order]** pour déterminer l’ordre du bloc s’il doit apparaître au même emplacement sur la page que les autres éléments de contenu. La position supérieure est zéro.

1. Dans le _[!UICONTROL Layout Updates]_, cliquez sur **[!UICONTROL Add Layout Update]**et défini **[!UICONTROL Display On]**à la catégorie, au produit ou à la page dans laquelle vous souhaitez que le bloc apparaisse.

   Par exemple, si vous choisissez `All Pages` et positionnez le bloc dans l&#39;en-tête ou dans le pied de page, le bloc apparaît au même endroit sur chaque page du magasin.

   Pour placer le bloc sur une page spécifique, procédez comme suit :

   - Définir **[!UICONTROL Display On]** to `Specified Page` et sélectionnez la variable **[!UICONTROL Page]** où vous souhaitez que le bloc apparaisse.

   - Choisissez la **[!UICONTROL Block Reference]** pour identifier l’emplacement sur la page où le bloc doit être placé.

   - Acceptez le paramètre par défaut pour **[!UICONTROL Template]**, qui est défini sur `CMS Static Block Default Template`.

   - Cliquez sur **[!UICONTROL Save and Continue Edit]**.

1. Dans le panneau de gauche, choisissez **[!UICONTROL Widget Options]**.

1. Cliquez sur **[!UICONTROL Select Block…]** et choisissez le bloc à placer.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

1. Lorsque vous y êtes invité, suivez les instructions situées en haut de l’espace de travail pour mettre à jour l’index et le cache de page.

   Le widget apparaît désormais dans la _[!UICONTROL Widgets]_liste.

### Étape 4. Vérification de l’emplacement dans le magasin

Revenez à votre vitrine pour vérifier que le bloc se trouve au bon endroit. Pour déplacer le bloc, vous pouvez rouvrir le widget pour essayer une autre référence de page ou de bloc.

## Flux RSS

RSS (Really Simple Syndication) est un format de données XML utilisé pour distribuer des informations en ligne. Vos clients peuvent s’abonner à vos flux RSS pour en savoir plus sur les nouveaux produits et promotions. Les flux RSS peuvent également être utilisés pour publier les informations sur vos produits sur des sites d’agrégation d’achats et peuvent être inclus dans des newsletters.

Lorsque les flux RSS sont activés, les ajouts aux produits, aux spécialités, aux catégories et aux coupons sont automatiquement envoyés aux abonnés de chaque flux. Un lien vers tous les flux RSS que vous publiez se trouve dans le pied de page de votre boutique.

![Icône de flux RSS](./assets/icon-rss.png){width="100"}<br/>

Le logiciel requis pour lire un flux RSS est appelé un lecteur de flux, et permet aux internautes de s&#39;abonner à des titres, des blogs, des podcasts, et bien plus encore. Google Reader est l’un des nombreux lecteurs de flux disponibles gratuitement en ligne.

![Exemple de storefront - flux RSS](./assets/storefront-rss-feeds.png){width="700" zoomable="yes"}

### Avantages de la configuration d’un flux RSS

- Téléchargez la dernière mise à jour depuis votre boutique ou blog
- Publicités légères
- Partages ordinaires
- Optimisation du référencement
- Augmentation des ventes

### Types de flux RSS

| Flux RSS | Description |
|--- |--- |
| [!UICONTROL Wish List] | Lorsqu’il est activé, un lien de flux RSS apparaît en haut des pages de liste de souhaits des clients. En outre, la page de partage des listes de souhaits comprend une case à cocher qui vous permet d’inclure un lien vers le flux à partir des listes de souhaits partagées. |
| [!UICONTROL New Products] | Publie la notification des nouveaux produits ajoutés au catalogue. |
| [!UICONTROL Special Products] | Publie la notification de tous les produits dont les tarifs sont spéciaux. |
| [!UICONTROL Coupons / Discounts] | Publie la notification de tout coupon spécial ou réduction disponible dans la boutique. |
| [!UICONTROL Top Level Category] | Publie la notification de toute modification sur la structure de catégorie de niveau supérieur de votre catalogue, qui est répercutée dans le menu principal. |
| [!UICONTROL Customer Order Status] | Permet aux clients de suivre l’état de leur commande par flux RSS. Une fois activé, un lien de flux RSS s’affiche dans la commande. |

{style="table-layout:auto"}

### Configuration de flux RSS pour votre boutique

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le coin supérieur droit, définissez **[!UICONTROL Store View]** aux vues dans lesquelles les flux doivent être disponibles.

   Si vous êtes invité à confirmer, cliquez sur **[!UICONTROL OK]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL RSS Feeds]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Rss Config]** section et définition **[!UICONTROL Enable RSS]** to `Enable`.

   ![Configuration de catalogue - flux RSS](../configuration-reference/catalog/assets/rss-feeds-rss-config.png){width="600" zoomable="yes"}

   Si nécessaire, effacez le **[!UICONTROL Use Default]** pour modifier la valeur par défaut.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Wish List]** section et définition **[!UICONTROL Enable RSS]** to `Enable`.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Catalog]** et définir d’autres flux sur `Enable` selon les besoins.

   - **[!UICONTROL New Products]**
   - **[!UICONTROL Special Products]**
   - **[!UICONTROL Coupons/Discounts]**
   - **[!UICONTROL Top Level Category]**

   ![Catalogue : paramètres des flux RSS](../configuration-reference/catalog/assets/rss-feeds-catalog.png){width="600" zoomable="yes"}

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL Order]** section et définition **[!UICONTROL Customer Order Status Notification]** to `Enable`.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

1. Afficher le résultat sur le storefront avec `/rss` à la fin de l’URL de la page.

