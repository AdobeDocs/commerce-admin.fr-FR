---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Sales]'
description: Vérifiez les paramètres de configuration sur la page de [!UICONTROL Sales] d’[!UICONTROL Sales] &gt; de l’administrateur Commerce.
exl-id: 29091aab-e608-4e68-a6fe-f2808c78581c
feature: Configuration, Orders
source-git-commit: 8d73a3a635c20e636c4b8bde41a4f807d3fd9f2e
workflow-type: tm+mt
source-wordcount: '1226'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Sales]

{{config}}

## [!UICONTROL General]

![Général](./assets/sales-general.png)<!-- zoom -->

<!-- [General](https://experienceleague.adobe.com/fr/docs/commerce-admin/stores-sales/site-store/sales-documents) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Hide Customer IP] | Affichage de la boutique | Détermine si l&#39;adresse IP du client apparaît sur les commandes, les factures, les livraisons et les avoirs. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Checkout Totals Sort Order]

![Ordre de tri des totaux de passage en caisse](./assets/sales-checkout-totals-sort-order.png)<!-- zoom -->

<!-- [Checkout Totals Sort Order](https://experienceleague.adobe.com/fr/docs/commerce-admin/stores-sales/point-of-purchase/checkout/checkout-totals-sort-order) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Subtotal] | Site internet | Nombre qui détermine à quel moment le sous-total est calculé par rapport aux autres totaux de passage en caisse. Valeur par défaut : `10` |
| [!UICONTROL Discount] | Site internet | Nombre qui détermine à quel moment la remise est calculée par rapport aux autres totaux de passage en caisse. Valeur par défaut : `20` |
| [!UICONTROL Shipping] | Site internet | Nombre qui détermine à quel moment la livraison est calculée par rapport à d’autres totaux de passage en caisse. Valeur par défaut : `30` |
| [!UICONTROL Tax] | Site internet | Nombre qui détermine le moment où la taxe est calculée par rapport aux autres totaux de passage en caisse. Valeur par défaut : `40` |
| [!UICONTROL Fixed Product Tax] | Site internet | Nombre qui détermine à quel moment la taxe sur les produits fixe est calculée par rapport aux autres totaux de passage en caisse. Valeur par défaut : `50` |
| [!UICONTROL Grand Total] | Site internet | Nombre qui détermine à quel moment le total général est calculé par rapport aux autres totaux de passage en caisse. Valeur par défaut : `100` |

{style="table-layout:auto"}

## [!UICONTROL Reorder]

![Réorganiser](./assets/sales-reorder.png)<!-- zoom -->

<!-- [Reorder](https://experienceleague.adobe.com/fr/docs/commerce-admin/stores-sales/shopper-tools/reorders-allow) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Allow Reorder] | Affichage de la boutique | Détermine si les clients peuvent effectuer une réorganisation à partir de leurs comptes. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Allow Zero Grand Total]

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Allow Zero Grand Total for Credit Memo] | Affichage de la boutique | Détermine la possibilité de créer un avoir avec un total général nul. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Invoice and Packing Slip Design]

![Conception de facture et de bon de livraison](./assets/sales-invoice-packing-slip-design.png)<!-- zoom -->

<!-- [Invoice and Packing Slip Design](https://experienceleague.adobe.com/fr/docs/commerce-admin/stores-sales/site-store/sales-documents) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Logo for PDF Print-outs] | Affichage de la boutique | Identifie le fichier logo qui apparaît dans l&#39;en-tête des factures et des bons de livraison PDF. Types de fichiers autorisés : <br/>JPG/JPEG <br/>TIF/TIFF <br/>PNG |
| [!UICONTROL Logo for HTML Print View] | Affichage de la boutique | Identifie le fichier logo qui apparaît dans l&#39;en-tête de la vue d&#39;impression HTML des factures et des bons de livraison. Types de fichiers autorisés : <br/>JPG /JPEG <br/>GIF <br/>PNG |
| [!UICONTROL Address] | Affichage de la boutique | Adresse du magasin telle que vous souhaitez qu&#39;elle apparaisse sur les factures et les bons de livraison. |

{style="table-layout:auto"}

## [!UICONTROL Minimum Order Amount]

![Montant minimal de la commande](./assets/sales-minimum-order-amount.png)<!-- zoom -->

<!-- [Minimum Order Amount](https://experienceleague.adobe.com/fr/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#minimum-order-amount) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable] | Site internet | Détermine si un montant de commande minimum est défini pour le site. Options : `Yes` / `No` |
| [!UICONTROL Minimum Amount] | Site internet | Spécifie le sous-total minimum, commande après application des remises. |
| [!UICONTROL Include Discount Amount] | Site internet | Détermine si le montant minimum de la commande inclut les remises appliquées. Options : `Yes` / `No` |
| [!UICONTROL Include Tax to Amount] | Site internet | Détermine si le montant minimum de la commande inclut la taxe. Options : `Yes` / `No` |
| [!UICONTROL Description Message] | Affichage de la boutique | Détermine le message qui s’affiche en haut du panier lorsque le total du panier est inférieur au montant de commande minimal. Si rien n’est indiqué, le message par défaut suivant apparaît : `Minimum order amount is $[minimum_amount]` |
| [!UICONTROL Error to Show in Shopping Cart] | Affichage de la boutique | Détermine le message qui s’affiche à partir du lien de panier ou de passage en caisse lorsque le montant de la commande est inférieur au montant minimal requis. Si rien n’est indiqué, un message par défaut s’affiche. |
| [!UICONTROL Validate Each Address Separately in Multi-address Checkout] | Site internet | Pour les commandes multi-articles, détermine si les articles de commande allant à des adresses séparées respectent largement le montant de commande minimum. Options : `Yes` / `No` |
| [!UICONTROL Multi-address Description Message] | Affichage de la boutique | Pour les commandes à plusieurs adresses, détermine le message qui apparaît dans le panier si les articles envoyés à une adresse sont inférieurs au montant de commande minimal. |
| [!UICONTROL Multi-address Error to Show in Shopping Cart] | Affichage de la boutique | Pour les commandes à plusieurs adresses, détermine le message qui s’affiche à partir du lien de panier ou de passage en caisse lorsque le montant de la commande est inférieur au montant minimum requis. Si rien n’est indiqué, un message par défaut s’affiche. |

{style="table-layout:auto"}

## [!UICONTROL Dashboard]

![Tableau de bord](./assets/sales-dashboard.png)<!-- zoom -->

<!-- [Dashboard](https://experienceleague.adobe.com/fr/docs/commerce-admin/start/admin/tools/admin-dashboard) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Use Aggregated Data] | Global | Détermine si des données de ventes agrégées en temps réel sont utilisées pour produire des rapports instantanés de tableaux de bord. Si vous devez traiter une grande quantité de données, vous pouvez améliorer les performances en désactivant l’affichage des données en temps réel. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Orders Cron Settings]

![Paramètres Cron des commandes](./assets/sales-orders-cron-settings.png)<!-- zoom -->

<!-- [Orders Cron Settings](https://experienceleague.adobe.com/fr/docs/commerce-admin/systems/tools/cron) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Pending Payment Order Lifetime] | Site internet | Détermine la durée de vie des commandes en attente, en minutes. Paramètre par défaut : `480` minutes (8 heures) |

{style="table-layout:auto"}

## [!UICONTROL Promotions]

[!BADGE SaaS uniquement]{type=Positive url="https://experienceleague.adobe.com/fr/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce as a Cloud Service (infrastructure SaaS gérée par Adobe)."}

![Paramètres des promotions](./assets/sales-promotions-settings.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Apply Catalog Price Rule on Grouped Price] | Global | Active la [tarification de niveau pour les règles de prix de catalogue](../../catalog/product-price-tier.md) lorsque la quantité d&#39;un prix de niveau est définie sur `1`.  Options : `Yes` / `No` |

## [!UICONTROL Gift Options]

![Options de cadeau](./assets/sales-gift-options.png)<!-- zoom -->

<!-- [Gift Options](https://experienceleague.adobe.com/fr/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#gift-options) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Allow Gift Messages on Order Level] | Site internet | Indiquez si un message cadeau peut être ajouté pour l’ensemble de la commande. |
| [!UICONTROL Allow Gift Messages on Order Items] | Site internet | Indiquez si un message cadeau peut être ajouté pour un article de commande individuel. |
| [!UICONTROL Allow Gift Wrapping on Order Level] | Site internet | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Indiquez si l&#39;emballage cadeau peut être ajouté à l&#39;intégralité de la commande. |
| [!UICONTROL Allow Gift Wrapping for Order Items] | Site internet | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Indiquez si l’emballage du cadeau peut être ajouté pour l’élément de commande individuel. |
| [!UICONTROL Allow Gift Receipt] | Site internet | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Indiquez si un reçu cadeau peut être ajouté pour la commande. |
| [!UICONTROL Allow Printed Card] | Site internet | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Indiquez si une carte imprimée peut être ajoutée pour la commande. |
| [!UICONTROL Default Price for Printed Card] | Site internet | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce uniquement) Spécifiez le prix par défaut de la carte imprimée. |

{style="table-layout:auto"}

## [!UICONTROL Minimum Advertised Price]

![Prix minimum annoncé](./assets/sales-minimum-advertised-price.png)<!-- zoom -->

<!-- [Minimum Advertised Price](https://experienceleague.adobe.com/fr/docs/commerce-admin/catalog/products/pricing/product-price-minimum-advertised) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable MAP] | Site internet | Active le prix minimum annoncé pour votre boutique. Options : `Yes` / `No` |
| [!UICONTROL Display Actual Price] | Site internet | Détermine où le prix réel d&#39;un produit est visible pour le client. Options : <br/>**`In Cart`**- Affiche le prix réel du produit dans le panier.<br/>**`Before Order Confirmation`** - Affiche le prix réel du produit à la fin du processus de passage en caisse, juste avant la confirmation de la commande. <br/>**`On Gesture`**- Affiche le prix réel du produit dans une fenêtre contextuelle lorsque le client clique sur « Cliquer pour voir le prix » ou « Qu’est-ce que c’est ? » lien. |
| [!UICONTROL Default Popup Text Message] | Affichage de la boutique | Message texte qui s’affiche lorsque le client sélectionne le lien « Cliquer pour voir le prix » dans une liste de catégories ou une page d’affichage de produits. |
| [!UICONTROL Default "What's This" Text Message] | Affichage de la boutique | Message texte qui s’affiche lorsque le client clique sur le bouton « Qu’est-ce que c’est ? » lien à partir de la page vue du produit. |
| [!UICONTROL Manufacturer's Suggested Retail Price] | Global | Prix de détail suggéré par le fabricant (PDSF). |

{style="table-layout:auto"}

## [!UICONTROL Multicoupon Settings]

{{ee-feature}}

![Paramètres multipoints](./assets/sales-multicoupon-settings.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Maximum number of coupons per order] | Site internet | Détermine le nombre maximal de coupons autorisés par commande. Cette fonctionnalité est disponible uniquement dans les API Admin, GraphQL et REST. Et il n’est **_pas disponible_** dans Storefront. |

{style="table-layout:auto"}

## [!UICONTROL Order by SKU Settings]

{{ee-feature}}

![Classer par paramètres SKU](./assets/sales-order-by-sku-settings.png)<!-- zoom -->

<!-- [Order by SKU Settings](https://experienceleague.adobe.com/fr/docs/commerce-admin/stores-sales/point-of-purchase/cart/order-by-sku) -->

![Classer par paramètres de SKU pour le groupe de clients](./assets/sales-order-by-sku-settings.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Order by SKU on My Account in Storefront] | Site internet | Détermine si l’option Classer par SKU est disponible dans le tableau de bord du compte client. Options : <br/>**`Yes, for Everyone`**- L’onglet Classer par SKU s’affiche dans le tableau de bord du compte de tous les clients.<br/>**`Yes, for Specified Customer Groups`** - L’onglet Trier par SKU s’affiche dans le tableau de bord du compte pour les membres de groupes spécifiés ou d’un catalogue partagé. <br/>**`No`**- L’onglet Classer par SKU n’est pas disponible dans le compte client. |
| [!UICONTROL Customer Groups] | Site internet | Détermine les groupes de clients. Options : `General` / `Retailer` / `Wholesale` |

{style="table-layout:auto"}

## [!UICONTROL Instant Purchase]

![Achat instantané](./assets/sales-instant-purchase.png)<!-- zoom -->

<!-- [Instant Purchase](https://experienceleague.adobe.com/fr/docs/commerce-admin/stores-sales/point-of-purchase/checkout-instant-purchase) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Affichage de la boutique | Active l’achat instantané pour la vue de magasin, si le coffre est activé pour le mode de paiement, tel que Braintree. Options : `Yes` / `No` |
| [!UICONTROL Button Text] | Affichage de la boutique | Spécifie le texte qui apparaît sur le bouton Achat instantané. Le texte par défaut est `Instant Purchase`. |

{style="table-layout:auto"}

## [!UICONTROL Rate Limiting]

![Limitation de débit](assets/sales-rate-limiting.png)<!-- zoom -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--------------------------------------------------------|--- |------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable rate limiting for placing orders] | Affichage de la boutique | Détermine si la limitation de débit est utilisée pour passer des commandes depuis la vue du magasin (la valeur par défaut est `No`). Options : `Yes` / `No`. |
| [!UICONTROL Requests limit per authenticated customer] | Affichage de la boutique | Nombre de demandes d’achat qu’un client authentifié peut effectuer pendant la période. La limite par défaut est `10`. |
| [!UICONTROL Requests limit per guest] | Affichage de la boutique | Nombre de demandes d’achat qu’un client non authentifié peut effectuer au cours de la période spécifiée. La valeur par défaut est `50`. |
| [!UICONTROL Counter resets in a ...] | Affichage de la boutique | Période pendant laquelle un client authentifié/non authentifié peut effectuer un certain nombre de demandes d’achat (la valeur par défaut est `Minute`). Options : `Minute` / `Hour` /`Day` |

{style="table-layout:auto"}

## [!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]

{{ee-feature}}

![Archivage des commandes, factures, expéditions, avoirs](./assets/sales-orders-invoices-shipments-credit-memos-archiving.png)<!-- zoom -->

Pour plus d’informations sur la modification de ces paramètres, voir [Configurer l’archive des commandes](../../stores-purchase/order-archive.md#configure-the-order-archive) dans le _Guide d’expérience des magasins et des achats_.

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable Archiving] | Global | Détermine si l&#39;archivage est activé. Options : `Yes` / `No` |
| [!UICONTROL Archive Orders Purchased] | Global | Détermine le nombre de jours avant l&#39;archivage d&#39;une commande terminée. Valeur par défaut : `30` |
| [!UICONTROL Order  Statuses to be Archived] | Global | Détermine le [statut](../../stores-purchase/order-status.md) des commandes à archiver. Par défaut, les commandes dont le statut est défini sur Terminé ou Fermé sont archivées. Options : `Pending` / `Processing` / `Suspected Fraud` / `Complete` / `Closed` / `Canceled` / `On Hold` |

{style="table-layout:auto"}

## [!UICONTROL RMA Settings]

{{ee-feature}}

![Paramètres RMA](./assets/sales-rma-settings.png)<!-- zoom -->

Pour plus d’informations sur la modification de ces paramètres, voir [Configurer les retours](../../stores-purchase/rma-configure.md) dans le _Guide d’expérience des magasins et des achats_.

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enable RMA on Storefront] | Site internet | Détermine si les clients peuvent créer et afficher des demandes RMA à partir du storefront. Le retour client peut être appliqué aux commandes nouvelles et existantes. Par défaut, RMA n’est pas activé pour le storefront. Options : `Yes` / `No` |
| [!UICONTROL Enable RMA on Product Level] | Site internet | Détermine la valeur par défaut du champ Activer RMA dans les informations sur le produit. |
| [!UICONTROL Use Store Address] | Site internet | Détermine le nom et l&#39;adresse du contact utilisés pour les expéditions de marchandises retournées. Options : <br/>**`Yes`**- Utilise l’adresse [point d’origine](../../stores-purchase/shipping-settings.md#point-of-origin) des paramètres d’expédition.<br/>**`No`** - Ouvre le formulaire d’adresse pour que vous puissiez saisir une autre adresse. |

{style="table-layout:auto"}
