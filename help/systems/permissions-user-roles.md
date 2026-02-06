---
title: Rôles utilisateur
description: Découvrez comment créer des rôles utilisateur et les autorisations associées pour gérer l’accès aux fonctions d’administration.
exl-id: a70f74d4-72b4-4639-a67d-9fc13df65924
feature: Admin Workspace, Roles/Permissions, Security
source-git-commit: dff29b7c3a95d4a0ae5ce16819c41a4560b477c4
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---

# Rôles utilisateur

Pour accorder à une personne un accès restreint à l’administrateur, la première étape consiste à créer un rôle disposant du niveau d’autorisations approprié. Une fois le rôle enregistré, vous pouvez ajouter de nouveaux utilisateurs et leur attribuer le rôle restreint afin de leur accorder un accès limité à l’administrateur.

![Administrateur - Rôles utilisateur](./assets/permissions-role-grid.png){width="600" zoomable="yes"}

## Définition d’un rôle

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Add New Role]**.

1. Suivez les étapes pour définir le rôle :

### Étape 1 : ajouter le nom du rôle

1. Sous _[!UICONTROL Role Information]_, saisissez un **[!UICONTROL Role Name]**descriptif.

1. Sous _[!UICONTROL Current User Identity Verification]_, saisissez votre mot de passe.

   ![Autorisations système - informations sur les rôles](./assets/permissions-role-info.png){width="600" zoomable="yes"}

### Étape 2 : affecter des ressources

>[!IMPORTANT]
>
>Lors de l’affectation de ressources, veillez à désactiver l’accès à l’outil Autorisations si vous limitez l’accès pour un rôle donné. Sinon, les utilisateurs peuvent modifier leurs propres autorisations.

1. Définissez **[!UICONTROL Role Scopes]** sur l’une des options suivantes :

   - `All`
   - `Custom`

   Si le paramètre est défini sur `Custom` pour une installation multisite, cochez la case du site web et stockez l’emplacement où le rôle doit être utilisé.

   ![Ressources du rôle utilisateur - étendue personnalisée](./assets/permissions-role-scope-custom.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Les utilisateurs dotés d’une portée de rôle `Custom` ne sont pas en mesure de créer des sites web et des catégories, d’affecter des produits à des catégories ou de modifier des produits à _[!UICONTROL All Store Views]_portée lorsqu’ils sont affectés à des magasins restreints. Ces utilisateurs ne peuvent pas non plus effectuer d’autres actions_ globales _qui affectent les portées auxquelles ils n’ont pas accès.

1. Sous _[!UICONTROL Roles Resources]_, définissez **[!UICONTROL Resource Access]**sur `Custom`.

   >[!NOTE]
   >
   >Si l’authentification à deux facteurs (2FA) est requise pour se connecter à l’administrateur, veillez à activer le `Permissions` de ressources > `Two Factor Auth` pour ce rôle. Dans le cas contraire, les utilisateurs nouvellement créés avec cette étendue de rôle `Custom` ne peuvent pas configurer 2FA lorsqu’ils accèdent à Admin pour la première fois.

1. Dans l’arborescence de **[!UICONTROL Resource]**, cochez la case de chaque fonctionnalité d’administration à laquelle le rôle peut accéder.

   Pour créer un rôle d&#39;administrateur avec un accès aux paramètres de taxe, choisissez les ressources Ventes/Taxe et Système/Taxe. Si vous configurez un site web pour une région différente de votre [point d’expédition d’origine](../stores-purchase/shipping-settings.md#point-of-origin) par défaut, vous devez autoriser l’accès aux ressources Système/Expédition pour le rôle. Les paramètres d’expédition déterminent le taux de taxe de la boutique utilisé pour les prix du catalogue.

   ![Ressources du rôle d’utilisateur affectées](./assets/permissions-role-resources-product.png){width="600" zoomable="yes"}

   La liste des autorisations disponibles peut inclure des options supplémentaires pour les extensions groupées et installées. En sélectionnant l’autorisation la plus élevée pour chaque fonctionnalité, vous attribuez toutes les autorisations disponibles pour l’utilisateur.

   >[!NOTE]
   >
   >Un utilisateur administrateur doit disposer d’autorisations **[!UICONTROL Sales / Archive]** pour l’étendue de son rôle afin d’afficher les onglets _[!UICONTROL Invoices]_,_[!UICONTROL Credit Memos]_ et Ordre _[!UICONTROL Shipments]_[tabulations](../stores-purchase/order-processing.md).

1. Cliquez ensuite sur **[!UICONTROL Save Role]**.

   Le rôle apparaît désormais dans la grille et peut être attribué aux comptes d’utilisateurs.

## Attribuer un rôle aux utilisateurs

1. Ouvrez l’enregistrement en mode d’édition à partir de la grille _[!UICONTROL Roles]_.

1. Sous _[!UICONTROL Current User Identity Verification]_, saisissez le mot de passe de votre compte utilisateur.

1. Dans le panneau de gauche, choisissez **[!UICONTROL Role Users]**.

   L’option _[!UICONTROL Role Users]_n’apparaît qu’une fois le nouveau rôle enregistré.

   ![Comptes utilisateur affectés au rôle](./assets/permissions-role-users.png){width="600" zoomable="yes"}

1. Pour rechercher un enregistrement d’utilisateur spécifique, procédez comme suit :

   - Saisissez la valeur dans le filtre de recherche en haut d’une colonne et appuyez sur **Entrée**.

   - Lorsque vous êtes prêt à revenir à la liste complète, cliquez sur **[!UICONTROL Reset Filter]**.

1. Cochez la case des utilisateurs et utilisatrices qui doivent être affectés au rôle.

1. Cliquez sur **[!UICONTROL Save Role]**.

## Modifier un rôle

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. Recherchez le rôle à l’aide de filtres au-dessus de la grille et cliquez sur le nom du rôle.

1. Apportez les modifications nécessaires.

   Pour plus d’informations sur les paramètres des rôles, consultez la procédure de création d’un rôle utilisateur .

1. Lorsque vous y êtes invité, saisissez votre mot de passe pour confirmer votre identité.

1. Cliquez sur le **[!UICONTROL Save Role]** .

## Supprimer un rôle

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. Localisez le rôle à l’aide de filtres au-dessus de la grille et ouvrez-le en mode d’édition.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Delete Role]**.

1. Pour confirmer l’action, cliquez sur **[!UICONTROL OK]**.

## Démonstration des rôles utilisateur

Regardez cette vidéo pour en savoir plus sur la gestion des rôles utilisateur :

>[!VIDEO](https://video.tv.adobe.com/v/343654?quality=12&learn=on)

## Ressources des rôles

L’accès aux ressources suivantes peut être affecté à un rôle personnalisé. Consultez la page liée pour en savoir plus sur les fonctionnalités associées à chaque ressource.

![Adobe Commerce](../assets/adobe-logo.svg) - Adobe Commerce uniquement

![Adobe Commerce B2B](../assets/b2b.svg) - Disponible avec Adobe Commerce B2B uniquement

| Ressource |   |   |
| --- | --- | --- |
| [`Dashboard`](../getting-started/admin-dashboard.md) |  |  |
| [`Sales`](../stores-purchase/sales-menu.md) | [`Operations`](../stores-purchase/orders.md) |  |
|  | [`Quotes`](../b2b/quotes.md) ![Adobe Commerce B2B](../assets/b2b.svg) <br/>[`Orders`](../stores-purchase/orders.md)<br/>[`Invoices`](../stores-purchase/invoices.md)<br/>[`Shipments`](../stores-purchase/shipments.md)<br/>[`Credit Memos`](../stores-purchase/credit-memos.md)<br/>[`Billing Agreements`](../stores-purchase/paypal-billing-agreements.md)<br/>[`Returns`](../stores-purchase/returns.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Transactions`](../stores-purchase/transactions.md) |
|  | [`Archive`](action-log-archive.md)![Adobe Commerce] |  |
|  | [`Shopping Cart Management`](../stores-purchase/cart.md) |  |
| [`Catalog`](../catalog/catalog-menu.md) | [`Category Permissions`](../catalog/categories.md) ![Adobe Commerce](../assets/adobe-logo.svg) |  |
|  | [`Inventory`](../inventory-management/introduction.md) | [`Products`](../catalog/products-list.md)<br/>[`Categories`](../catalog/categories.md) |
|  | [`Shared Catalog`](../b2b/catalog-shared-create.md) ![Adobe Commerce B2B](../assets/b2b.svg) | [`Manage Shared Catalog`](../b2b/catalog-shared-manage.md) |
| [`Customers`](../customers/guide-overview.md) | [`All Customers`](../customers/customers-all.md)<br/>[`Now Online`](../customers/now-online.md)<br/>[`Customer Groups`](../customers/customer-groups.md)<br/>[`Segments`](../customers/customer-segments.md) ![Adobe Commerce](../assets/adobe-logo.svg) |  |
|  | [`Login as Customer`](../customers/login-as-customer.md) | `Allow Login as Customer Button`<br/>`View Login as Customer Log` ![Adobe Commerce](../assets/adobe-logo.svg) |
|  | [`Companies`](../b2b/account-companies.md) ![Adobe Commerce B2B](../assets/b2b.svg) | [`Manage Companies`](../b2b/account-company-manage.md) <br/>`Add New Company` <br/>`Delete Company` <br/>`Reimburse Balance` |
| [`Carts`](../stores-purchase/shopping-assisted-cart-manage.md) | [`Manage carts`](../stores-purchase/shopping-assisted-cart-manage.md) |  |
| [`My Account`](../customers/account-dashboard-my-account.md) |  |  |
| [`Marketing`](../merchandising-promotions/marketing-menu.md) | [`Promotions`](../merchandising-promotions/marketing-menu.md#uicontrol-promotions) | [`Catalog Price Rule`](../merchandising-promotions/price-rules-catalog.md) <br/>[`Cart Price Rules`](../merchandising-promotions/price-rules-cart.md) <br/>[`Related Products Rules`](../merchandising-promotions/product-related-rules.md)![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Gift Card Accounts`](../stores-purchase/product-gift-card-accounts.md) ![Adobe Commerce](../assets/adobe-logo.svg) |
|  | [`Private Sales`](../merchandising-promotions/events-private-sales.md) ![Adobe Commerce](../assets/adobe-logo.svg) | [`Events`](../merchandising-promotions/event-create.md) <br/>[`Invitations`](../merchandising-promotions/invitations.md) |
|  | `Communications` | [`Email Templates`](email-templates.md) <br/>[`Newsletter Template`](../merchandising-promotions/newsletter-template.md) <br/>[`Newsletter Queue`](../merchandising-promotions/newsletter-queue.md) <br/>[`Newsletter Subscribers`](../merchandising-promotions/newsletter-subscribers.md) <br/>[`Email Reminders`](../merchandising-promotions/email-reminder-rules.md) |
|  | `Sales Channel` | [`Amazon Sales Channel`](https://experienceleague.adobe.com/docs/commerce-channels/amazon/overview.html) |
|  | [`SEO & Search`](../merchandising-promotions/marketing-menu.md#uicontrol-seo--search) | [`Search Terms`](../catalog/search-terms.md) <br/>[`Search Synonyms`](../catalog/search-terms.md#search-synonyms) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`URL Rewrites`](../merchandising-promotions/url-rewrite-custom.md) <br/>[`Site Map`](../merchandising-promotions/sitemap-xml.md) |
|  | [`User Content`](../merchandising-promotions/product-reviews-moderate.md) | [`All Reviews`](../merchandising-promotions/product-reviews.md) <br/>[`Pending Reviews`](../merchandising-promotions/product-reviews-moderate.md) <br/> |  |
| [`Content`](../content-design/content-menu.md) | [`Elements`](../content-design/content-menu.md#uicontrol-elements)) | [`Pages`](../content-design/pages.md)<br/>[`Hierarchy`](../content-design/page-hierarchy.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Blocks`](../content-design/blocks.md)<br/>[`Dynamic Blocks`](../content-design/dynamic-blocks.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Widgets`](../content-design/widgets.md)<br/>[`Media Gallery`](../content-design/media-gallery.md) |  |
|  | [`Design`](../content-design/introduction.md#design) | [`Themes`](../content-design/themes.md)<br/>[`Schedule`](../content-design/schedule.md) |  |
|  | [Évaluation de contenu](../content-design/content-staging.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br /> |  |
| [`Reports`](../getting-started/reports-menu.md) | [`Marketing`](../getting-started/marketing-reports.md) | `Shopping Cart`<br />[`Search Terms`](../catalog/search-terms.md#search-terms-report)<br />`Newsletter Problem Reports` |  |
|  | [`Reviews`](../getting-started/review-reports.md)<br /> |  |
|  | [`Sales`](../getting-started/sales-reports.md) |  |
|  | `System Insights` ![Adobe Commerce](../assets/adobe-logo.svg) | [`Site-Wide Analysis Tool`](https://experienceleague.adobe.com/docs/commerce-operations/tools/site-wide-analysis-tool/access.html) |
|  | [`Customers`](../getting-started/customer-reports.md)<br/>[`Products`](../getting-started/product-reports.md)<br/>[`Private Sales`](../getting-started/private-sales-reports.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br />[`Statistics`](../getting-started/reports-menu.md#uicontrol-statistics)<br />[`Business Intelligence`](../getting-started/business-intelligence.md) |  |
| [`Stores`](../stores-purchase/stores.md) | [`Settings`](../stores-purchase/stores-menu.md) | [`All Stores`](../stores-purchase/stores.md)<br/>[`Configuration`](../configuration-reference/guide-overview.md)<br/>[`Terms and Conditions`](../stores-purchase/terms-and-conditions.md)<br/>[`Order Status`](../stores-purchase/order-status.md) |  |
|  | [`Inventory`](../inventory-management/sources-stocks.md) | [`Sources`](../inventory-management/sources-manage.md)<br/>[`Stocks`](../inventory-management/stocks-manage.md) |  |
|  | [`Taxes`](../stores-purchase/taxes.md) |  |  |
|  | [`Currency`](../stores-purchase/currency.md) | [`Currency Rates`](../stores-purchase/currency-update.md)<br/>[`Currency Symbols`](../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) |  |
|  | [`Attributes`](../catalog/product-attributes.md) | [`Product`](../catalog/attribute-product-create.md)<br/>[`Update Attributes`](../catalog/attribute-product-create.md)<br/>[`Attribute Set`](../catalog/attribute-sets.md)<br/>[`Ratings`](../merchandising-promotions/product-reviews.md#create-custom-ratings) |
|  | [`Other Settings`](../stores-purchase/stores-menu.md) | [`Customer Groups`](../customers/customer-groups.md) |
| [`System`](system-menu.md) | [`Data Transfer`](data-transfer.md) | [`Import`](data-import.md)<br/>[`Export`](data-export.md)<br/>[`Import/Export Tax Rates`](data-transfer-tax-rates.md)<br/>[`Import History`](data-import.md#import-history) |  |
|  | [`Magento Connect`](../getting-started/commerce-marketplace.md) | `Connect Manager`<br/>`Package Extensions` |  |
|  | [`Tools`](system-menu.md#tools) | [`Cache Management`](cache-management.md)<br/>[`Backups`](backups.md)<br/>[`Index Management`](index-management.md)<br/>[`Change Indexer Mode`](index-management.md) |  |
|  | [`Permissions`](permissions.md) | [`All Users`](permissions-users-all.md)<br/>[`Locked Users`](permissions-users-all.md#locked-users)<br/>[`User Roles`](permissions-user-roles.md) |
| [`Action Log`](action-log.md)![Adobe Commerce](../assets/adobe-logo.svg) | [`Report`](action-log.md)<br/>[`Archive`](action-log-archive.md) |
|  | [`Other Settings`](system-menu.md) | [`Notifications`](notifications.md)<br/>[`Custom Variables`](variables-custom.md)<br/>[`Manage Encryption Key`](encryption-key.md) |  |
| [`Global Search`](../getting-started/admin-workspace.md#workspace-search) |  |  |

{style="table-layout:auto"}
