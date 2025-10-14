---
title: Configuration du panier
description: Découvrez les fonctionnalités du panier que vous pouvez configurer pour prendre en charge l’expérience d’achat dans votre boutique.
exl-id: b98ec7ce-9354-4f03-b67e-dd1587f0c866
feature: Shopping Cart, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '2449'
ht-degree: 0%

---

# Configuration du panier

La configuration du panier détermine le fonctionnement du panier pour vos clients de magasin, notamment le moment où le client est redirigé vers la page du panier et les images utilisées pour les miniatures de produit. Vous pouvez également exiger une commande pour atteindre un montant minimum avant le début du processus de passage en caisse, spécifier le nombre de jours pendant lesquels les prix entre guillemets restent valides et spécifier l’ordre des éléments dans la section _Totaux de commande_.

[**Mini panier**](#mini-cart) - Configurez cette option pour déterminer si le lien/l’icône du panier affiche le nombre de produits (ou SKU) différents dans le panier, ou la quantité totale de tous les articles.

[**Lien vers le mini panier**](#configure-the-cart-link) - Configurez cette option pour déterminer si le mini panier s’affiche lorsqu’un client clique sur le nombre d’articles de l’icône de panier en haut d’une page de magasin.

[**Rediriger vers le panier**](#redirect-to-cart) : configurez cette option pour déterminer si la page du panier s’affiche chaque fois qu’un article est ajouté au panier ou uniquement lorsqu’un client choisit d’accéder à la page.

[**Durée de vie des citations**](#quote-lifetime) - Configurez cette option pour spécifier la durée de validité d’un prix.

[**Montant minimum de la commande**](#minimum-order-amount) - Configurez ces options pour spécifier un montant minimum, une fois les remises appliquées, que les sous-totaux de la commande doivent respecter et que la messagerie affichée dans le panier est suffisante.

[**Quantité minimale de commande**](#minimum-order-quantity) - Configurez ces options pour spécifier un nombre minimum d’éléments requis pour passer une commande.

[**Miniatures du panier**](#cart-thumbnails) - Configurez les options de miniatures du panier pour déterminer les miniatures affichées dans le panier pour les produits regroupés ou configurables.

[**Options de cadeau**](#gift-options) - Configurez les options de cadeau pour déterminer si les clients peuvent ajouter un message cadeau ou une carte de voeux, et si des options d’emballage-cadeau sont disponibles.

>[!NOTE]
>
>Pour plus d’informations sur la configuration du processus de passage en caisse, voir [Options de passage en caisse](checkout-process.md).

## Mini panier

Le _mini panier_ affiche un résumé des articles du panier. Elle est activée par défaut et s’affiche lorsque vous cliquez sur le lien Panier en haut de la page.
Le lien peut être configuré pour afficher le nombre de produits (ou SKU) différents dans le panier, ou la quantité totale de tous les articles.

![L’acheteur affiche la barre latérale du panier à partir d’une page de produit](./assets/storefront-mini-cart-watch.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Pour un client _enregistré_, il arrive que le mini panier ne soit pas synchronisé automatiquement sur plusieurs appareils et navigateurs. Pour synchroniser le mini-panier dans ce cas, le client peut simplement ouvrir la page [panier](cart.md) sur ce périphérique ou navigateur.

### Configuration du mini panier

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Checkout]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur _[!UICONTROL Mini Cart]_.

   ![Configuration du mini panier](../configuration-reference/sales/assets/checkout-mini-cart.png){width="600" zoomable="yes"}

1. Si le paramètre est défini pour une vue de magasin spécifique, [choisissez la vue de magasin](../configuration-reference/scope-change.md#set-the-scope) où la configuration s’applique.

   Lorsque vous y êtes invité, cliquez sur **[!UICONTROL OK]** pour continuer.

1. Définissez **[!UICONTROL Display Mini Cart]** sur l’une des options suivantes :

   - `Yes` - Affiche le mini panier sur les pages du magasin. L’aspect de la barre latérale dépend du thème.
   - `No` - Désactive l’affichage du mini panier sur les pages de magasin.

1. Si l’affichage est activé, mettez à jour les autres options pour configurer l’affichage :

   - Pour **[!UICONTROL Number of Items to Display Scrollbar]**, saisissez le nombre d’éléments pouvant apparaître dans la barre latérale avant le déclenchement de la barre de défilement.
   - Pour **[!UICONTROL Maximum Display Recently Added Item(s)]**, saisissez le nombre maximal d’éléments récemment ajoutés que vous souhaitez voir apparaître dans le mini panier.

1. Cliquez sur **[!UICONTROL Save Config]**.

### Configuration du lien du panier

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Checkout]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL My Cart Link]** .

1. Définissez **[!UICONTROL Display Cart Summary]** sur l’un des paramètres suivants :

   - `Display item quantities` - Ce paramètre affiche le nombre total de produits dans le panier, en ajoutant les quantités pour chaque produit.
   - `Display number of items in cart` - Ce paramètre affiche le nombre d’articles dans le panier, quelle que soit la quantité.

   ![Options de configuration pour le lien Mon panier](../configuration-reference/sales/assets/checkout-my-cart-link.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Save Config]**.

## Redirection vers le panier

La page Panier peut être configurée pour s’afficher chaque fois qu’un article est ajouté au panier ou uniquement lorsque les clients choisissent d’accéder à la page. Les informations de base sur les articles actuellement dans le panier sont toujours disponibles dans le [mini panier](#mini-cart). Il s’agit d’équilibrer les avantages de laisser les clients continuer à faire leurs achats, avec les avantages d’encourager les clients à effectuer leur passage en caisse. Cela peut être une simple question de préférence personnelle. Cependant, si vous souhaitez la sauvegarder avec des nombres, vous pouvez exécuter un test A/B pour déterminer quelle approche produit un taux de conversion plus élevé.

**_Pour configurer le moment où le panier apparaît :_**

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Checkout]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Shopping Cart]** .

   ![Les paramètres de configuration du panier ont été développés sur la page](../configuration-reference/sales/assets/checkout-shopping-cart.png){width="600" zoomable="yes"}

1. Si le paramètre est défini pour une vue de magasin spécifique, [choisissez la vue de magasin](../configuration-reference/scope-change.md#set-the-scope) où la configuration s’applique.

   Lorsque vous y êtes invité, cliquez sur **[!UICONTROL OK]** pour continuer.

1. Définissez **[!UICONTROL After Adding a Product Redirect to Shopping Cart]** sur l’une des options suivantes :

   - `Yes` - Affiche la page du panier immédiatement après l’ajout d’un produit au panier.
   - `No` - Désactive la redirection vers le panier après l’ajout d’un produit au panier.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Durée de vie des citations

Avec l’installation et l’activation d’Adobe Commerce B2B, vous pouvez ajouter la prise en charge de la fonction _Quotes_. Cette fonctionnalité permet aux acheteurs autorisés d’initier le processus de négociation des prix en envoyant une demande à partir du panier. La grille _Guillemets_ répertorie chaque citation reçue et conserve un historique de la communication entre l’acheteur et le vendeur. Pour plus d’informations sur les fonctionnalités B2B, voir [Guillemets négociés](../b2b/quotes.md) dans le _Guide de l’utilisateur d’Adobe Commerce B2B_.

Vous pouvez déterminer la durée de validité d’un prix en définissant la durée de vie du prix du panier dans la configuration. Par exemple, si un acheteur laisse un panier sans surveillance au bout de plusieurs jours, le prix des devis de certains articles peut ne plus être le même. Par défaut, la durée de vie du guillemet est définie sur 30 jours.

**_Pour configurer la durée de vie des guillemets :_**

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Checkout]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Shopping Cart]** .

   ![Les paramètres de configuration du panier ont été développés sur la page](../configuration-reference/sales/assets/checkout-shopping-cart.png){width="600" zoomable="yes"}

1. Si le paramètre est défini pour une vue de magasin spécifique, [choisissez la vue de magasin](../configuration-reference/scope-change.md#set-the-scope) où la configuration s’applique.

   Lorsque vous y êtes invité, cliquez sur **[!UICONTROL OK]** pour continuer.

1. Pour **[!UICONTROL Quote Lifetime (days)]**, saisissez le nombre de jours pendant lesquels un prix entre guillemets reste valide.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Montant minimum de la commande

La configuration vous permet de spécifier un montant minimum, après application des remises, auquel les sous-totaux de la commande doivent être respectés. Les commandes envoyées à plusieurs adresses peuvent être requises pour respecter le montant minimal de la commande par adresse. Le bouton Passage en caisse n’est disponible qu’une fois le montant minimum de la commande atteint.

![Le panier affiche un message de commande minimum](./assets/storefront-cart-minimum-order-amount.png){width="700" zoomable="yes"}

**_Pour configurer un montant minimum de commande :_**

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et sélectionnez **[!UICONTROL Sales]** sous .

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Minimum Order Amount]** .

   ![&#x200B; Les options de configuration de commande minimale développées sur la page](../configuration-reference/sales/assets/sales-minimum-order-amount.png){width="600" zoomable="yes"}

1. Pour exiger un montant de commande minimal, définissez **[!UICONTROL Enable]** sur `Yes`.

1. Si l’ordre minimum est activé, définissez les options suivantes pour configurer les exigences :

   - Saisissez le **[!UICONTROL Minimum Amount]** requis pour le sous-total après l’application des remises.

   - Définissez **[!UICONTROL Include Discount Amount]** sur l’une des options suivantes :

      - `Yes` - Nécessite que le sous-total corresponde au montant minimum avec toutes les remises incluses. En prenant l’exemple d’un montant minimum de 50 $, si le panier contient un supplément de 60 $ auquel une remise de 25 % est appliquée, le sous-total obtenu est de 45 $ et le panier ne satisfait pas le minimum.
      - `No` - Nécessite que le sous-total corresponde au montant minimum sans aucune remise.

   - Définissez **[!UICONTROL Include Tax to Amount]** sur l’une des options suivantes :

      - `Yes` - Nécessite que le sous-total corresponde au montant minimum avec taxe incluse.
      - `No` - Nécessite que le sous-total corresponde au montant minimum sans taxe.

1. Si vous le souhaitez, vous pouvez personnaliser les paramètres de message relatifs au montant minimum de la commande :

   - Pour **[!UICONTROL Description Message]**, saisissez le texte à utiliser pour personnaliser le message qui s’affiche en haut du panier lorsque le sous-total ne correspond pas au montant minimum.

   - Pour **[!UICONTROL Error to Show in Shopping Cart]**, saisissez le texte que vous souhaitez utiliser pour personnaliser le message d’erreur du panier.

   Laissez les champs de description du message vides pour utiliser les messages par défaut.

1. Si nécessaire, configurez le paramètre de quantité minimale de commande pour les commandes à plusieurs adresses :

   - Pour exiger que chaque adresse d’un ordre à plusieurs adresses respecte la valeur de commande minimale, définissez **[!UICONTROL Validate Each Address Separately in Multi-address Checkout]** sur `Yes`.

   - Si vous le souhaitez, vous pouvez personnaliser les paramètres de message relatifs au montant minimum de la commande :

      - **[!UICONTROL Multi-address Description Message]** - Entrez le texte que vous souhaitez utiliser pour personnaliser le message qui apparaît en haut du panier pour les commandes à plusieurs adresses qui ne respectent pas le minimum.

      - **[!UICONTROL Multi-address Error to Show in Shopping Cart]** - Entrez le texte que vous souhaitez utiliser pour personnaliser le message d’erreur du panier pour les commandes à plusieurs adresses qui ne respectent pas le minimum, saisissez le texte dans la zone.

     Laissez les champs de description du message vides pour utiliser les messages par défaut.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Quantité de commande minimale

Vous pouvez définir la quantité minimale autorisée pour une commande. La quantité minimale peut également être configurée en fonction de chaque groupe de clients.

1. Accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Catalog]** et choisissez **[!UICONTROL Inventory]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Product Stock Options]** .

   ![Options Stock de produits](../configuration-reference/catalog/assets/catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

1. Pour **[!UICONTROL Minimum Qty Allowed in Shopping Cart]**, définissez la quantité minimale du produit pour une commande.

   Si nécessaire, décochez la case **[!UICONTROL Use system value]** pour modifier ces paramètres.

   - Définissez le paramètre **[!UICONTROL Customer Group]** sur un groupe spécifique et saisissez le **[!UICONTROL Minimum Qty]** correspondant. Pour ajouter un autre groupe et une limite de quantité, cliquez sur **[!UICONTROL Add Minimum Qty]**.

   - Pour définir la même limite de quantité minimale pour tous les clients, conservez la sélection `ALL GROUPS` et saisissez la valeur **[!UICONTROL Minimum Qty]**.

1. Cliquez sur **[!UICONTROL Save Config]**.

   ![Quantité minimale requise dans le panier](./assets/minimum-qty-allowed-in-shopping-cart.png){width="700" zoomable="yes"}

## Miniatures du panier

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

Les miniatures affichées dans le panier donnent aux clients un aperçu rapide des articles qu’ils sont sur le point d’acheter. Toutefois, pour les produits avec plusieurs options, l’image peut ne pas correspondre à la variante du produit figurant dans le panier. Si le client achète un article dans une couleur spécifique, idéalement, la miniature du panier doit correspondre.

L’image miniature des produits regroupés et configurables peut être définie pour afficher l’image du produit &quot;parent&quot; ou de la variante de produit.

![Le panier affiche des images miniatures pour chaque produit](./assets/storefront-cart.png){width="700" zoomable="yes"}

**_Pour configurer les miniatures de panier :_**

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Checkout]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Shopping Cart]** .

   ![Les paramètres de configuration du panier ont été développés sur la page](../configuration-reference/sales/assets/checkout-shopping-cart.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Grouped Product Image]** pour déterminer la miniature utilisée dans le panier pour les [produits groupés](../catalog/product-create-grouped.md) :

   - `Product Thumbnail Itself` - Utilise la miniature affectée à la variation de produit ajoutée au panier.
   - `Parent Product Thumbnail` - Utilise la miniature affectée au produit parent.

1. Définissez **[!UICONTROL Configurable Product Image]** pour déterminer la miniature utilisée dans le panier pour les [produits configurables](../catalog/product-create-configurable.md) :

   - `Product Thumbnail Itself` - Utilise la miniature affectée à la variation de produit ajoutée au panier.
   - `Parent Product Thumbnail` - Utilise la miniature affectée au produit parent.

1. Cliquez sur **[!UICONTROL Save Config]**.

## Options de cadeau

La sélection des options de cadeau disponibles s’affiche dans le panier avant le début du processus de passage en caisse. La configuration des options de cadeau détermine si les clients peuvent ajouter un message cadeau ou une carte de voeux, et si des options d’emballage de cadeau sont disponibles. Chaque article de la commande peut comporter un message distinct et un emballage cadeau. Lorsqu’ils sont appliqués à l’ensemble de la commande, les clients peuvent également ajouter un reçu cadeau et une carte de voeux.

![Exemple de vitrine - Options de cadeau dans le panier](./assets/storefront-cart-gift-options-for-products-or-order.png){width="700" zoomable="yes"}

La configuration des options de cadeau s’applique à l’ensemble du site web, mais elle peut être remplacée au niveau du produit.

### Activation des options de cadeau

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et sélectionnez **[!UICONTROL Sales]** sous .

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) **[!UICONTROL Gift Options]** sur la page.

   ![Configuration des ventes - Paramètres des options de cadeau](../configuration-reference/sales/assets/sales-gift-options.png){width="600" zoomable="yes"}

1. Définissez les options du message cadeau en fonction de vos préférences :

   - Pour **[!UICONTROL Allow Gift Messages on Order Level]**, sélectionnez `Yes` pour activer un seul message cadeau pour l’ensemble de la commande.
   - Pour **[!UICONTROL Allow Gift Messages for Order Items]**, sélectionnez `Yes` pour activer l’ajout de messages-cadeaux distincts pour des articles individuels dans le panier du client.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Définissez les options d’encapsulage du cadeau selon vos préférences :

   - Pour **[!UICONTROL Allow Gift Wrapping on Order Level]**, sélectionnez `Yes` pour activer un seul emballage cadeau pour l’ensemble de la commande.
   - Pour **[!UICONTROL Allow Gift Wrapping for Order Items]**, sélectionnez `Yes` pour activer l’ajout d’un emballage cadeau individuellement à chaque article du panier du client.

   Vous pouvez également définir différentes [conceptions d’emballage cadeau](#gift-wrap) afin que les clients puissent choisir l’encapsulation.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Pour offrir aux clients la possibilité d&#39;inclure un reçu de cadeau, définissez **[!UICONTROL Allow Gift Receipt]** sur `Yes`.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Pour offrir aux clients la possibilité d’inclure une carte imprimée, définissez **[!UICONTROL Allow Printed Card]** sur `Yes`.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Saisissez le **[!UICONTROL Default Price for Printed Card]**.

1. Cliquez sur **[!UICONTROL Save Config]**.

### Placement de cadeau

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

L’emballage cadeau est disponible pour tout produit qui peut être livré et qui peut être proposé pour des articles individuels ou pour l’ensemble de la commande. Vous pouvez facturer un prix distinct pour chaque conception de retour à la ligne et charger une miniature pour chaque conception qui apparaît comme une option pour un produit du panier. Lorsqu’un client clique sur la miniature de retour à la ligne du cadeau, une image en taille réelle s’affiche. Lors de la révision du passage en caisse, les frais de retour à la ligne des cadeaux s’affichent avec les autres [totaux de passage en caisse](checkout-totals-sort-order.md) dans la section _Résumé de la commande_ .

L’image de retour à la ligne du cadeau doit être un échantillon qui affiche le modèle répété et peut également inclure un échantillon du ruban à utiliser. Vous pouvez scanner le papier ou prendre une photo d&#39;un paquet emballé. L’image téléchargée peut être une image GIF, JPG ou PNG et doit être carrée. Dans l’exemple suivant, l’image de retour à la ligne du cadeau téléchargée fait 230 x 230 pixels.

![Options de cadeau dans le panier](./assets/storefront-cart-gift-options-gift-wrap.png){width="700" zoomable="yes"}

#### Ajouter une conception d’emballage cadeau

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Wrapping]**.

   ![Grille de recouvrement de cadeau](./assets/gift-wrapping.png){width="700" zoomable="yes"}

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add Gift Wrapping]**.

1. Saisissez le nom du **[!UICONTROL Gift Wrapping Design]** qui apparaîtra lors du passage en caisse.

   Si nécessaire, vous pouvez modifier le **[!UICONTROL Scope]** et configurer un nom différent pour chaque vue de magasin.

1. Sélectionnez l’ **[!UICONTROL Websites]** où la conception du retour à la ligne est disponible.

1. Définissez **[!UICONTROL Status]** sur `Enabled`.

   Si vous disposez d’une option d’encapsulation saisonnière, vous pouvez la définir sur `Disabled` lorsque vous ne souhaitez pas que cette option soit disponible.

1. Saisissez le **[!UICONTROL Price]** de la conception de l’emballage cadeau.

   Ce paramètre peut être remplacé par le prix du emballage cadeau défini au niveau du produit.

   ![Nouveau encapsulage de cadeau](./assets/gift-wrapping-new.png){width="600" zoomable="yes"}

1. Pour télécharger une miniature **[!UICONTROL Image]** de l’encapsulage du cadeau, cliquez sur **[!UICONTROL Choose File]** et sélectionnez le fichier à télécharger dans votre répertoire.

   Une miniature de l’image s’affiche dans le _[!UICONTROL Gift Wrapping Information]_&#x200B;après l’enregistrement.

1. Cliquez sur **[!UICONTROL Save]**.

#### Modifier la conception d’un emballage cadeau

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Wrapping]**.

1. Recherchez l’enregistrement d’emballage cadeau dans la liste.

1. Dans la colonne _Action_, cliquez sur **[!UICONTROL Edit]**.

   ![Modifier les informations d’emballage de cadeau](./assets/gift-wrapping-edit.png){width="600" zoomable="yes"}

1. Effectuez les modifications nécessaires.

1. Cliquez sur **[!UICONTROL Save]**.

#### Supprimer des conceptions de retour à la ligne

Une fois la grille _Gift Wrapping_ ouverte, utilisez l’une de ces méthodes pour supprimer les conceptions de retour automatique à la ligne.

**_Méthode 1 : suppression d’une seule conception de retour à la ligne cadeau_**

1. Ouvrez la conception d’emballage cadeau en mode d’édition.

1. Dans la partie supérieure de l’espace de travail, cliquez sur **[!UICONTROL Delete]**.

1. Lorsque vous y êtes invité, cliquez sur **[!UICONTROL OK]** pour confirmer.

**_Méthode 2 : supprimer plusieurs conceptions de retour à la ligne de cadeau_**

1. Dans la grille _Gift Wrapping_, cochez la case de chaque conception de cadeau à supprimer.

1. Définissez le contrôle **[!UICONTROL Actions]** sur `Delete`.

1. Cliquez sur **[!UICONTROL Submit]**.

### Taxe sur les options de cadeau

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

Les prix d’emballage de cadeau et de carte-cadeau imprimée peuvent être configurés pour inclure ou exclure la taxe, ou pour afficher les deux options. Vous pouvez également spécifier une classe fiscale pour ces éléments, au niveau global ou au niveau du site web.

**_Pour configurer les taxes des options de cadeau :_**

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Tax]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Tax Classes]** .

   ![Configuration de classe de taxe](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Tax Class for Gift Options]** sur la classe fiscale applicable.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** .

   ![Commandes, factures, paramètres d’affichage des notes de crédit](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Display Gift Wrapping Prices]** sur l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Définissez **[!UICONTROL Display Printed Card Prices]** sur l’une des options suivantes :

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Cliquez sur **[!UICONTROL Save Config]**.
