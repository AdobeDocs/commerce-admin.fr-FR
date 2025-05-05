---
title: Réseaux sociaux et flux RSS
description: Découvrez comment ajouter des médias sociaux et d’autres intégrations de flux RSS pour accroître la notoriété de la marque et des produits.
exl-id: e4a48870-f53e-4848-8faa-8f2aedaf53b7
feature: Merchandising, Communications
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1162'
ht-degree: 0%

---

# Réseaux sociaux et flux RSS

De nombreux commerçants utilisent les médias sociaux et d&#39;autres outils numériques pour sensibiliser la marque et les produits. Vous pouvez intégrer votre boutique à vos réseaux sociaux en installant une extension Marketplace ou en ajoutant un module externe à vos pages de contenu. Utilisez des flux RSS pour publier les informations sur vos produits sur les sites d’agrégation d’achats et les inclure même dans vos newsletters. Les clients peuvent s’abonner à vos flux RSS pour en savoir plus sur les nouveaux produits et promotions.

## Réseaux sociaux

Votre boutique peut être connectée aux réseaux sociaux en installant une [extension Marketplace](../getting-started/commerce-marketplace.md). En outre, vous pouvez facilement ajouter des modules externes sociaux tels que le bouton _J’aime_ aux blocs CMS qui peuvent être incorporés dans des pages de votre magasin.

Les sites de réseau social disposent de nombreux modules externes qui peuvent facilement être ajoutés à votre boutique. En outre, de nombreuses extensions sur le Commerce Marketplace peuvent être utilisées pour intégrer votre boutique aux médias sociaux. L’exemple suivant montre comment ajouter un bouton Facebook _J’aime_ à votre magasin.

>[!NOTE]
>
>Adobe Commerce a supprimé l’intégration Facebook native _Magento Social_ et ne prend plus en charge l’extension. Accédez au [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=Facebook){:target=&quot;_blank&quot;} pour localiser d’autres extensions pour l’intégration Facebook.

### Étape 1. Obtention du code de bouton

1. Sur le site web des développeurs de métadonnées, accédez à la page [configuration de bouton](https://developers.facebook.com/docs/plugins/like-button) .

1. Pour **[!UICONTROL URL to Like]**, saisissez l’URL de la page dans votre magasin que vous souhaitez que les visiteurs _J’aime_.

   Par exemple, vous pouvez saisir l’URL de la page d’accueil de votre magasin.

1. Sélectionnez le bouton **[!UICONTROL Layout]**.

1. Saisissez le **[!UICONTROL Width]** en pixels disponible sur votre site pour le bouton et tout message texte associé.

1. Définissez **[!UICONTROL Action Type]** sur l’une des options suivantes :

   - `Like`
   - `Recommend`

1. Cliquez sur **[!UICONTROL Get Code]** pour copier le code généré dans le Presse-papiers.

### Étape 2. Création d’un bloc de contenu

1. Revenez à l’administrateur de votre boutique.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Block]**.

1. Saisissez un **[!UICONTROL Block Title]** descriptif pour la référence interne.

   Par exemple : `Facebook Like Button`.

1. Attribuez un **[!UICONTROL Identifier]** unique au bloc, en utilisant tous les caractères minuscules et les traits de soulignement au lieu des espaces.

   Par exemple : `facebook_like_button`.

1. Si votre instance Commerce a plusieurs vues de magasin, choisissez chacune **[!UICONTROL Store View]** où le bloc doit être disponible.

1. Ajoutez le fragment de code au contenu du bloc, en fonction de votre outil de contenu :

   - Lors de l’utilisation de [!DNL Page Builder], ajoutez un bloc [HTML Code](../page-builder/html-code.md) à l’étape et collez le fragment de code que vous avez copié à partir du site Facebook. Sinon, collez le fragment de code dans la zone **[!UICONTROL Content]**.

   - Avec l’éditeur, collez le fragment de code que vous avez copié à partir du site Facebook dans la zone **[!UICONTROL Content]**.

1. Si le bloc n&#39;est pas prêt à être mis en ligne, définissez **[!UICONTROL Enable Block]** sur `No`.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Block]**.

### Étape 3. Placez le bloc

1. Ajoutez le bloc, en fonction de votre outil de contenu :

   - Lorsque vous utilisez [!UICONTROL Page Builder], suivez les instructions pour [ajouter le bloc](../page-builder/block.md) à la scène.

   - Sur la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Widget]** et procédez comme suit :

   - ![Adobe Commerce B2B](../assets/b2b.svg) (Disponible avec Adobe Commerce B2B uniquement) Dans la section _Paramètres_, définissez **[!UICONTROL Type]** sur `CMS Static Block` et cliquez sur **[!UICONTROL Continue]**.

   - Vérifiez que **[!UICONTROL Design Theme]** est défini sur le thème actuel.

   - Cliquez sur **[!UICONTROL Continue]**.

1. Dans la section **[!UICONTROL Storefront Properties]** , procédez comme suit :

   - Pour **[!UICONTROL Widget Title]**, saisissez un titre de référence interne.

   - Définissez **[!UICONTROL Assign to Store Views]** sur `All Store Views` ou sur la vue dans laquelle vous souhaitez que l’application soit disponible. Pour sélectionner plusieurs vues, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

   - Saisissez un nombre dans le champ **[!UICONTROL Sort Order]** pour déterminer l’ordre du bloc s’il doit apparaître au même emplacement sur la page que les autres éléments de contenu. La position supérieure est zéro.

1. Dans la section _[!UICONTROL Layout Updates]_, cliquez sur **[!UICONTROL Add Layout Update]**&#x200B;et définissez **[!UICONTROL Display On]**&#x200B;sur la catégorie, le produit ou la page où vous souhaitez que le bloc apparaisse.

   Par exemple, si vous choisissez `All Pages` et positionnez le bloc dans l’en-tête ou le pied de page, le bloc apparaît au même endroit sur chaque page du magasin.

   Pour placer le bloc sur une page spécifique, procédez comme suit :

   - Définissez **[!UICONTROL Display On]** sur `Specified Page` et sélectionnez l’ **[!UICONTROL Page]** où vous souhaitez que le bloc apparaisse.

   - Sélectionnez le **[!UICONTROL Block Reference]** pour identifier l&#39;emplacement sur la page où le bloc doit être placé.

   - Acceptez le paramètre par défaut pour **[!UICONTROL Template]**, défini sur `CMS Static Block Default Template`.

   - Cliquez sur **[!UICONTROL Save and Continue Edit]**.

1. Dans le panneau de gauche, choisissez **[!UICONTROL Widget Options]**.

1. Cliquez sur **[!UICONTROL Select Block…]** et sélectionnez le bloc que vous souhaitez placer.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save]**.

1. Lorsque vous y êtes invité, suivez les instructions situées en haut de l’espace de travail pour mettre à jour l’index et le cache de page.

   Le widget apparaît désormais dans la liste _[!UICONTROL Widgets]_.

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

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le coin supérieur droit, définissez **[!UICONTROL Store View]** sur les vues où les flux doivent être disponibles.

   Si vous êtes invité à confirmer, cliquez sur **[!UICONTROL OK]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL RSS Feeds]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) de la section **[!UICONTROL Rss Config]** et définissez **[!UICONTROL Enable RSS]** sur `Enable`.

   ![ Configuration du catalogue - flux RSS](../configuration-reference/catalog/assets/rss-feeds-rss-config.png){width="600" zoomable="yes"}

   Si nécessaire, décochez la case **[!UICONTROL Use Default]** pour modifier la valeur par défaut.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) de la section **[!UICONTROL Wish List]** et définissez **[!UICONTROL Enable RSS]** sur `Enable`.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) de la section **[!UICONTROL Catalog]** et définissez d’autres flux sur `Enable` si nécessaire.

   - **[!UICONTROL New Products]**
   - **[!UICONTROL Special Products]**
   - **[!UICONTROL Coupons/Discounts]**
   - **[!UICONTROL Top Level Category]**

   ![Catalog - Paramètres des flux RSS](../configuration-reference/catalog/assets/rss-feeds-catalog.png){width="600" zoomable="yes"}

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) de la section **[!UICONTROL Order]** et définissez **[!UICONTROL Customer Order Status Notification]** sur `Enable`.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

1. Consultez le résultat sur le storefront avec `/rss` à la fin de l’URL de la page.

