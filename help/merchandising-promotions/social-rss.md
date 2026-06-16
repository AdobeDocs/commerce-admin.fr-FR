---
title: Réseaux sociaux et flux RSS
description: Découvrez comment ajouter des médias sociaux et d’autres intégrations de flux RSS pour faire connaître votre marque et vos produits.
exl-id: e4a48870-f53e-4848-8faa-8f2aedaf53b7
feature: Merchandising, Communications
TQID: https://experienceleague.adobe.com/jO5CAIJOQ7caLuno4OP4vnhJhIMZahlxL7waFwDyHzY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1175
ht-degree: 0%

---

# Réseaux sociaux et flux RSS

De nombreux commerçants utilisent les médias sociaux et d&#39;autres outils numériques pour faire connaître leur marque et leurs produits. Vous pouvez intégrer votre boutique à vos réseaux sociaux en installant une extension Marketplace ou en ajoutant un plug-in à vos pages de contenu. Utilisez les flux RSS pour publier des informations sur vos produits sur les sites d&#39;agrégation d&#39;achats, et même pour les inclure dans vos newsletters. Les clients peuvent s&#39;abonner à vos flux RSS pour en savoir plus sur les nouveaux produits et les promotions.

## Réseaux sociaux

Votre boutique peut être connectée aux réseaux sociaux en installant une [extension Marketplace](../getting-started/commerce-marketplace.md). En outre, vous pouvez facilement ajouter des modules externes de réseaux sociaux, tels que le bouton _J’aime_ à des blocs CMS qui peuvent être intégrés à des pages de votre boutique.

Les sites de réseaux sociaux disposent de nombreux plug-ins qui peuvent être facilement ajoutés à votre boutique. En outre, il existe de nombreuses extensions sur le Commerce Marketplace qui peuvent être utilisées pour intégrer votre boutique aux médias sociaux. L’exemple suivant montre comment ajouter un bouton Facebook _J’aime_ à votre boutique.

>[!NOTE]
>
>Adobe Commerce a supprimé l’intégration native de _Magento Social_ Facebook et ne prend plus en charge l’extension. Accédez à [&#128279;](https://marketplace.magento.com/catalogsearch/result/?q=Facebook){:target="_blank"} pour trouver d&#39;autres extensions pour l&#39;intégration Facebook.

### Étape 1. Obtenir le code du bouton

1. Sur le site web des développeurs de Meta, accédez à la page [configuration du bouton](https://developers.facebook.com/docs/plugins/like-button).

1. Par **[!UICONTROL URL to Like]**, saisissez l’URL de la page de votre boutique que les utilisateurs doivent _aimer_.

   Par exemple, vous pouvez saisir l’URL de la page d’accueil de votre boutique.

1. Sélectionnez la **[!UICONTROL Layout]** du bouton.

1. Saisissez le **[!UICONTROL Width]** en pixels disponible sur votre site pour le bouton et tout message texte associé.

1. Définissez **[!UICONTROL Action Type]** sur l’une des options suivantes :

   - `Like`
   - `Recommend`

1. Cliquez sur **[!UICONTROL Get Code]** pour copier le code généré dans le presse-papiers.

### Étape 2. Créer un bloc de contenu

1. Retournez dans l’administration de votre boutique.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Block]**.

1. Saisissez un **[!UICONTROL Block Title]** descriptif pour référence interne.

   Par exemple : `Facebook Like Button`.

1. Attribuez un **[!UICONTROL Identifier]** unique au bloc, en utilisant tous les caractères minuscules et les traits de soulignement au lieu des espaces.

   Par exemple : `facebook_like_button`.

1. Si votre instance Commerce comporte plusieurs vues de magasin, choisissez chaque **[!UICONTROL Store View]** où le bloc doit être disponible.

1. Ajoutez le fragment de code au contenu du bloc, en fonction de votre outil de contenu :

   - Lors de l’utilisation de [!DNL Page Builder], ajoutez un bloc [Code HTML](../page-builder/html-code.md) à l’étape et collez le fragment de code que vous avez copié à partir du site Facebook. Sinon, collez le fragment de code dans la zone de **[!UICONTROL Content]**.

   - Avec l’éditeur, collez le fragment de code que vous avez copié du site Facebook dans la zone de **[!UICONTROL Content]**.

1. Si le bloc n’est pas prêt à être lancé, définissez **[!UICONTROL Enable Block]** sur `No`.

1. Cliquez ensuite sur **[!UICONTROL Save Block]**.

### Étape 3. Placer le bloc

1. Ajoutez le bloc en fonction de votre outil de contenu :

   - Lors de l’utilisation de [!UICONTROL Page Builder], suivez les instructions pour [ajouter le bloc](../page-builder/block.md) à l’étape.

   - Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Widget]** et procédez comme suit :

   - ![Adobe Commerce B2B](../assets/b2b.svg) (disponible avec Adobe Commerce B2B uniquement) Dans la section _Paramètres_, définissez **[!UICONTROL Type]** sur `CMS Static Block` et cliquez sur **[!UICONTROL Continue]**.

   - Vérifiez que **[!UICONTROL Design Theme]** est défini sur le thème actuel.

   - Cliquez sur **[!UICONTROL Continue]**.

1. Dans la section **[!UICONTROL Storefront Properties]**, procédez comme suit :

   - Par **[!UICONTROL Widget Title]**, saisissez un titre pour référence interne.

   - Définissez **[!UICONTROL Assign to Store Views]** sur `All Store Views` ou sur la vue dans laquelle vous souhaitez que l’application soit disponible. Pour sélectionner plusieurs vues, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et cliquez sur chaque option.

   - Saisissez un nombre dans le champ **[!UICONTROL Sort Order]** pour déterminer l’ordre du bloc s’il est affecté à apparaître au même emplacement sur la page que les autres éléments de contenu. La position supérieure est zéro.

1. Dans la section _[!UICONTROL Layout Updates]_, cliquez sur **[!UICONTROL Add Layout Update]**&#x200B;et définissez **[!UICONTROL Display On]**&#x200B;à la catégorie, au produit ou à la page où vous souhaitez que le bloc apparaisse.

   Par exemple, si vous choisissez `All Pages` et positionnez le bloc dans l’en-tête ou le pied de page, le bloc apparaît au même endroit sur chaque page du magasin.

   Pour placer le bloc sur une page spécifique, procédez comme suit :

   - Définissez **[!UICONTROL Display On]** sur `Specified Page` et sélectionnez le **[!UICONTROL Page]** où vous souhaitez que le bloc apparaisse.

   - Choisissez la **[!UICONTROL Block Reference]** pour identifier l’emplacement du bloc sur la page où il doit être placé.

   - Acceptez le paramètre par défaut pour **[!UICONTROL Template]**, qui est défini sur `CMS Static Block Default Template`.

   - Cliquez sur **[!UICONTROL Save and Continue Edit]**.

1. Dans le panneau de gauche, choisissez **[!UICONTROL Widget Options]**.

1. Cliquez sur **[!UICONTROL Select Block…]** et sélectionnez le bloc à placer.

1. Cliquez ensuite sur **[!UICONTROL Save]**.

1. Lorsque vous y êtes invité, suivez les instructions situées en haut de l’espace de travail pour mettre à jour le cache d’index et de page.

   Le widget apparaît désormais dans la liste _[!UICONTROL Widgets]_.

### Étape 4. Vérifier l’emplacement dans le magasin

Revenez à votre storefront pour vérifier que le bloc est à l’emplacement correct. Pour déplacer le bloc, vous pouvez rouvrir le widget et essayer d’utiliser une autre référence de page ou de bloc.

## Flux RSS

RSS (Really Simple Syndication) est un format de données XML utilisé pour la distribution d&#39;informations en ligne. Vos clients peuvent s&#39;abonner à vos flux RSS pour en savoir plus sur les nouveaux produits et promotions. Les flux RSS peuvent également être utilisés pour publier des informations sur vos produits sur des sites d&#39;agrégation d&#39;achats et peuvent être inclus dans des newsletters.

Lorsque les flux RSS sont activés, tous les ajouts aux produits, promotions, catégories et coupons sont automatiquement envoyés aux abonnés de chaque flux. Un lien vers tous les flux RSS que vous publiez se trouve dans le pied de page de votre boutique.

![icône de flux RSS](./assets/icon-rss.png){width="100"}<br/>

Le logiciel requis pour lire un flux RSS s&#39;appelle un lecteur de flux et permet aux gens de s&#39;abonner aux titres, aux blogs, aux balados, et bien plus encore. Google Reader est l&#39;un des nombreux lecteurs de flux qui sont disponibles en ligne gratuitement.

![Exemple de storefront - Flux RSS](./assets/storefront-rss-feeds.png){width="700" zoomable="yes"}

### Avantages de la configuration d&#39;un flux RSS

- Téléchargez la dernière mise à jour depuis votre boutique ou blog
- Publicités légères
- Actions ordinaires
- Optimiser l’optimisation du moteur de recherche
- Augmenter les ventes

### Types de flux RSS

| Flux RSS | Description |
|--- |--- |
| [!UICONTROL Wish List] | Lorsqu’il est activé, un lien de flux RSS s’affiche en haut des pages de liste de souhaits des clients. En outre, la page de partage de listes de souhaits comprend une case à cocher qui vous permet d’inclure un lien vers le flux à partir de listes de souhaits partagées. |
| [!UICONTROL New Products] | Publie la notification des nouveaux produits ajoutés au catalogue. |
| [!UICONTROL Special Products] | Publie une notification de tous les produits avec des prix spéciaux. |
| [!UICONTROL Coupons / Discounts] | Publie une notification de tous les coupons ou remises spéciaux disponibles dans le magasin. |
| [!UICONTROL Top Level Category] | Publie une notification de toute modification apportée à la structure de catégorie de niveau supérieur de votre catalogue, qui est répercutée dans le menu principal. |
| [!UICONTROL Customer Order Status] | Permet aux clients de suivre l&#39;état de leur commande par flux RSS. Lorsqu’il est activé, un lien de flux RSS s’affiche sur la commande. |

{style="table-layout:auto"}

### Configurer des flux RSS pour votre boutique

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le coin supérieur droit, définissez **[!UICONTROL Store View]** sur les vues où les flux doivent être disponibles.

   Si vous êtes invité à confirmer, cliquez sur **[!UICONTROL OK]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL RSS Feeds]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Rss Config]** et définissez **[!UICONTROL Enable RSS]** sur `Enable`.

   ![Configuration du catalogue - Flux RSS](../configuration-reference/catalog/assets/rss-feeds-rss-config.png){width="600" zoomable="yes"}

   Si nécessaire, décochez la case **[!UICONTROL Use Default]** pour modifier la valeur par défaut.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Wish List]** et définissez **[!UICONTROL Enable RSS]** sur `Enable`.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Catalog]** et définissez d’autres flux à `Enable` si nécessaire.

   - **[!UICONTROL New Products]**
   - **[!UICONTROL Special Products]**
   - **[!UICONTROL Coupons/Discounts]**
   - **[!UICONTROL Top Level Category]**

   ![Catalogue - Paramètres des flux RSS](../configuration-reference/catalog/assets/rss-feeds-catalog.png){width="600" zoomable="yes"}

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Order]** et définissez **[!UICONTROL Customer Order Status Notification]** sur `Enable`.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

1. Voir le résultat sur le storefront avec `/rss` à la fin de l’URL de la page.

