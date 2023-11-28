---
title: '[!UICONTROL Advanced] &gt; [!UICONTROL Admin]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Advanced] &gt; [!UICONTROL Admin] de l’administrateur Commerce.
exl-id: 546b8d01-9611-4415-ab2b-29be560316f5
role: Admin
feature: Configuration, Admin Workspace
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '1215'
ht-degree: 0%

---

# Avancé > Admin

{{config}}

## [!UICONTROL Admin User Emails]

![Admin User Emails](./assets/admin-admin-user-emails.png)<!-- zoom -->

Pour plus d’informations sur la modification de ces paramètres, voir [Mot de passe oublié et courrier électronique de réinitialisation](../../systems/permissions-users-all.md#forgotten-password-and-reset-emails).

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|---------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Forgot Password Email Template] | Global | Identifie le modèle de courrier électronique utilisé pour le message envoyé lorsqu’un utilisateur administrateur oublie son mot de passe. Modèle par défaut : `Forgot Admin Password` |
| [!UICONTROL Forgot and Reset Email Sender] | Global | Identifie le contact de magasin qui apparaît comme l’expéditeur de la _Mot de passe oublié_ e-mail. Expéditeur par défaut : `General Contact`<br/>Autres options d’expéditeur : `Sales Representative`, `Customer Support`, `Custom Email` |
| [!UICONTROL User Notification Template] | Global | Détermine le modèle de courrier électronique utilisé par défaut pour les notifications Admin. Modèle par défaut : `User Notification` |

{style="table-layout:auto"}

## [!UICONTROL Startup Page]

![Page de démarrage](./assets/admin-startup-page.png)<!-- zoom -->

Pour plus d’informations sur la modification de ces paramètres, voir [Modifier la page de démarrage](../../getting-started/admin-dashboard.md#change-the-startup-page) dans le _Guide de démarrage_.

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|---------------------------|------------------------------------------------------------------------|------------------------------------------------------------------|
| [!UICONTROL Startup Page] | Global | Détermine la page d’entrée Admin qui s’affiche une fois que vous êtes connecté. |

{style="table-layout:auto"}

### [!UICONTROL Startup Page] options

| Zone |                                                                                                                                                                                                                                                                                                                                                                           | Option |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [`Dashboard`](../../getting-started/admin-dashboard.md) |                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| `Sales` | `Operations` | [`Quotes`](../../b2b/quotes.md) ![B2B pour Adobe Commerce](../../assets/b2b.svg) <br/>[`Orders`](../../stores-purchase/orders.md)<br/>[`Invoices`](../../stores-purchase/invoices.md)<br/>[`Shipments`](../../stores-purchase/shipments.md)<br/>[`Credit Memos`](../../stores-purchase/credit-memos.md)<br/>[`Billing Agreements`](../../stores-purchase/paypal-billing-agreements.md)<br/>[`Returns`](../../stores-purchase/returns.md) ![Adobe Commerce](../../assets/adobe-logo.svg) </span><br/>[`Transactions`](../../stores-purchase/transactions.md)<br/>`Braintree Virtual Terminal` |
| `Catalog` | [`Inventory`](../../inventory-management/introduction.md) | [`Products`](../../catalog/products-list.md)<br/>[`Categories`](../../catalog/categories.md)<br/>[`Shared Catalog`](../../b2b/catalog-shared-create.md) ![B2B pour Adobe Commerce](../../assets/b2b.svg) |
| `Customers` | [`All Customers`](../../customers/customers-all.md)<br/>[`Now Online`](../../customers/now-online.md)<br/>[`Customer Groups`](../../customers/customer-groups.md)<br/>[`Segments`](../../customers/customer-segments.md) ![Adobe Commerce](../../assets/adobe-logo.svg) <br/>[`Companies`](../../b2b/account-companies.md)![B2B pour Adobe Commerce](../../assets/b2b.svg) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| `Marketing` | `Promotions` | [`Catalog Price Rule`](../../merchandising-promotions/price-rules-catalog.md) <br/>[`Cart Price Rules`](../../merchandising-promotions/price-rules-cart.md)) <br/>[`Related Products Rules`](../../merchandising-promotions/product-related-rules.md) ![Adobe Commerce](../../assets/adobe-logo.svg) <br/>[`Gift Card Accounts`](../../stores-purchase/product-gift-card-accounts.md) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | [`Private Sales`](../../merchandising-promotions/events-private-sales.md) ![Adobe Commerce](../../assets/adobe-logo.svg) | [`Events`](../../merchandising-promotions/event-configure.md) <br/>[`Invitations`](../../merchandising-promotions/invitations.md) |
|                                                         | `Communications` | [`Email Templates`](../../systems/email-templates.md) <br/>[`Newsletter Template`](../../merchandising-promotions/newsletter-template.md) <br/>[`Newsletter Queue`](../../merchandising-promotions/newsletter-queue.md) <br/>[`Newsletter Subscribers`](../../merchandising-promotions/newsletter-subscribers.md) <br/>[`Email Reminders`](../../merchandising-promotions/email-reminder-rules.md) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | `SEO & Search` | [`Search Terms`](../../catalog/search-terms.md) <br/>[`Search Synonyms`](../../catalog/search-terms.md#search-synonyms) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`URL Rewrites`](../../merchandising-promotions/url-rewrite.md) <br/>[`Site Map`](../../merchandising-promotions/sitemap-xml.md) |
|                                                         | [`User Content`](../../catalog/settings-advanced-product-reviews.md) | [`All Reviews`](../../catalog/settings-advanced-product-reviews.md) <br/>[`Pending Reviews`](../../merchandising-promotions/product-reviews-moderate.md) <br/> |
| `Content` | `Elements` | [`Pages`](../../content-design/pages.md)<br/>[`Hierarchy`](../../content-design/page-hierarchy.md) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`Blocks`](../../content-design/blocks.md)<br/>[`Dynamic Blocks`](../../content-design/dynamic-blocks.md) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`Widgets`](../../content-design/widgets.md)<br/>[`Media Gallery`](../../content-design/media-storage.md) |
|                                                         | `Design` | [`Configuration`](../../content-design/configuration.md)<br/>[`Themes`](../../content-design/themes.md)<br/>[`Schedule`](../../content-design/schedule.md) |
|                                                         | `Content Staging` ![Adobe Commerce](../../assets/adobe-logo.svg)<br /> | [Tableau de bord](../../content-design/content-staging.md) |
| `Reports` | [`Marketing`](../../getting-started/marketing-reports.md) | `Products in Cart`<br />`Search Terms`<br />`Abandoned Carts`<br />`Newsletter Problem Reports` |
|                                                         | [`Reviews`](../../getting-started/review-reports.md) | `By Customer`<br/> `By Products`<br/> |
|                                                         | [`Sales`](../../getting-started/sales-reports.md) | `Orders`<br/>`Tax`<br/>`Invoiced`<br/>`Shipping`<br/>`Refunds`<br/>`Coupons`<br/>`PayPal Settlement`<br/>`Braintree Settlement` |
|                                                         | `System Insights` | [`Site-Wide Analysis Tool`](https://experienceleague.adobe.com/docs/commerce-operations/tools/site-wide-analysis-tool/access.html) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | [`Customers`](../../getting-started/customer-reports.md) | `Order Total`<br/>`Order Count`<br/>`New`<br/>`Wish Lists`<br/>`Segments`<br/> |
|                                                         | [`Products`](../../getting-started/product-reports.md) | `Views`<br/>`Bestsellers`<br/>`Low Stock`<br/>`Ordered`<br/>`Downloads` |
|                                                         | [`Private Sales`](../../getting-started/private-sales-reports.md) ![Adobe Commerce](../../assets/adobe-logo.svg) | `Invitations`<br/>`Invited Customers`<br/>`Conversions` |
|                                                         | `Statistics` | [`Refresh Statistics`](../../getting-started/sales-reports.md#refresh-statistics) |
|                                                         | [`Business Intelligence`](../../getting-started/business-intelligence.md) | `Advanced Reporting`<br/>`BI Essentials`<br/> |
|                                                         | `Customer Engagement` | `Dashboard`<br/>`Importer Status`<br/>`Automation Enrollment`<br/>`Campaign Sends`<br/>`SMS Sends`<br/>`Cron Tasks`<br/>`Log Viewer`<br/>`Abandoned Carts` |
| `Stores` | `Settings` | [`All Stores`](../../stores-purchase/stores.md)<br/>[`Configuration`](../../configuration-reference/guide-overview.md)<br/>[`Terms and Conditions`](../../stores-purchase/terms-and-conditions.md)<br/>[`Order Status`](../../stores-purchase/order-status.md) |
|                                                         | [`Inventory`](../../inventory-management/introduction.md) | [`Sources`](../../inventory-management/sources-stocks.md#sources)<br/>[`Stocks`](../../inventory-management/sources-stocks.md#stocks) |
|                                                         | [`Taxes`](../../stores-purchase/taxes.md) | [`Tax Rules`](../../stores-purchase/tax-rules.md)<br/>[`Tax Zones and Rates`](../../stores-purchase/tax-zones-rates.md) |
|                                                         | [`Currency`](../../stores-purchase/currency.md) | [`Currency Rates`](../../stores-purchase/currency-configuration.md)<br/>[`Currency Symbols`](../../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) |
|                                                         | `Attributes` | [`Customer`](../../systems/data-attributes-customer.md)<br/>[`Customer Address`](../../systems/data-attributes-customer.md#customer-addresses)<br/>[`Product`](../../systems/data-attributes-product.md)<br/>[`Attribute Set`](../../catalog/attribute-sets.md)<br/>[`Returns`](../../stores-purchase/attributes-returns.md)<br/>[`Ratings`](../../merchandising-promotions/product-reviews.md#create-custom-ratings) |
|                                                         | `Other Settings` | [`Reward Exchange Rates`](../../merchandising-promotions/reward-exchange-rates.md)<br/>[`Gift Wrapping`](../../stores-purchase/cart-configuration.md#gift-wrap)<br/>[`Gift Registry`](../../merchandising-promotions/gift-registry-create.md) |
| `System` | [`Data Transfer`](../../systems/data-transfer.md) | [`Import`](../../systems/data-import.md)<br/>[`Export`](../../systems/data-export.md)<br/>[`Import/Export Tax Rates`](../../systems/data-transfer-tax-rates.md)<br/>[`Import History`](../../systems/data-import.md#import-history)<br/>[`Scheduled Import/Export`](../../systems/data-scheduled-import-export.md) |
|                                                         | `Extensions` | [`Integrations`](../../systems/integrations.md) |
|                                                         | `Tools` | [`Cache Management`](../../systems/cache-management.md)<br/>[`Index Management`](../../systems/index-management.md) |
|                                                         | `Support` | [`Data Collector`](../../systems/support.md#data-collector)<br/>[`System Report`](../../systems/support.md#system-reports) |
|                                                         | `Permissions` | [`All Users`](../../systems/permissions-users-all.md)<br/>[`Locked Users`](../../systems/permissions-users-all.md#locked-users)<br/>[`User Roles`](../../systems/permissions-user-roles.md) |
|                                                         | `Action Log` ![Adobe Commerce](../../assets/adobe-logo.svg) | [`Report`](../../systems/action-log.md)<br/>[`Archive`](../../systems/action-log-archive.md)<br/>[`Bulk Actions`](../../systems/action-log-bulk-actions.md) |
|                                                         | `Other Settings` | [`Notifications`](../../systems/notifications.md)<br/>[`Custom Variables`](../../systems/variables-custom.md)<br/>[`Manage Encryption Key`](../../systems/encryption-key.md) |
| `Find Partners & Extensions` |                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

{style="table-layout:auto"}

<!-- Feature still in development 
## [!UICONTROL Unified Experience]

![Store Configuration for Unified Experience](./assets/admin-uex-configuration.png)

The [!UICONTROL Unified Experience] option is available in Adobe Commerce deployments that have the Commerce Admin Unified Experience extension loaded. This extension enables integration with Experience Cloud to streamline cross-application workflows between Commerce and other Experience Cloud solutions. See [Adobe Experience Cloud Integration for Commerce Admin](../../getting-started/admin-unified-experience-integration-overview.md).

| Field        | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Description                                                                                                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Enable       | Global                                                                 | Determines if the Commerce instance uses the Experience Cloud integration. Before enabling this feature, review the [requirements and configuration instructions](../../getting-started/admin-unified-experience-integration-overview.md). Options: Yes/No.                                                                                                                    |
| Project Name | Global                                                                 | Identifies the instance in the Experience Cloud Commerce Projects workspace when the Unified Experience is enabled. The name can contain only alphanumeric characters and spaces. Defaults to the [cloud environment name](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-architecture.html?lang=en#pro-environment-architecture). |

{style="table-layout:auto"}

-->

## [!UICONTROL Admin Base URL]

![URL de base d’administration](./assets/admin-admin-base-url.png)<!-- zoom -->

Pour plus d’informations sur la définition de ces options, voir [Configuration de l’URL de base](../../stores-purchase/store-urls.md#configure-the-base-url) dans le _Guide d’expérience des magasins et des achats_.

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|------------------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Use Custom Admin URL] | Global | Détermine si une URL personnalisée est utilisée pour accéder à l’administrateur. Options : `Yes` / `No` |
| [!UICONTROL Custom Admin URL] | Global | Spécifie une URL personnalisée pour accéder à l’administrateur. Par défaut, l’URL d’administration est identique à l’URL de base.<br/>**Important :** L’URL d’administration doit se trouver dans la même installation Commerce et avoir la même racine de document que le storefront. |
| [!UICONTROL Use Custom Admin Path] | Global | Détermine si un chemin personnalisé est utilisé pour accéder à l’administrateur. Le chemin par défaut est `admin`. Options : `Yes` / `No` |
| [!UICONTROL Custom Admin Path] | Global | Modifie le nom du chemin d’accès administrateur par défaut en un élément difficile à deviner. Saisissez le nom du chemin personnalisé en minuscules. Par exemple: `aardvark` |

{style="table-layout:auto"}

## [!UICONTROL Security]

![Sécurité](./assets/admin-security.png)<!-- zoom -->

Pour plus d’informations sur la définition de ces options, voir [Configuration de la sécurité d’administration](../../systems/security-admin.md) dans le _Guide des systèmes d’administration_.

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Admin Account Sharing] | Affichage en magasin | Détermine si un utilisateur administrateur peut être connecté au même compte simultanément à partir de différents appareils. Options : <br/>**`Yes`**- Permet plusieurs sessions actives à partir du même compte d’administrateur.<br/>**`No`** - Autorise une seule session active par compte d’administrateur. |
| [!UICONTROL Password Reset Protection Type] | Affichage en magasin | Détermine la méthode utilisée pour gérer les demandes de réinitialisation de mot de passe. Options : <br/>**`By IP and Email`**- Le mot de passe peut être réinitialisé en ligne à la réception d’une réponse de la notification à l’adresse électronique associée au compte administrateur.<br/>**`By IP`** - Le mot de passe peut être réinitialisé en ligne sans confirmation supplémentaire. <br/>**`By Email`**- Le mot de passe ne peut être réinitialisé qu’en répondant par courrier électronique à la notification envoyée à l’adresse électronique associée au compte administrateur.<br/>**`None`** - Le mot de passe ne peut être réinitialisé que par l’administrateur du magasin. |
| [!UICONTROL Recovery Link Expiration Period (hours)] | Global | Détermine le nombre d’heures pendant lesquelles un lien de récupération de mot de passe reste valide. |
| [!UICONTROL Max Number of Password Reset Requests] | Affichage en magasin | Détermine le nombre maximal de demandes de mot de passe pouvant être envoyées par heure. |
| [!UICONTROL Min Time Between Password Reset Requests] | Affichage en magasin | Détermine le nombre minimum de minutes entre les demandes de réinitialisation de mot de passe. |
| [!UICONTROL Add Secret Key to URLs] | Global | Lorsque cette option est activée, ajoute une clé secrète à l’URL d’administration par mesure de précaution contre les exploits. Options : `Yes` / `No` |
| [!UICONTROL Login Is Case Sensitive] | Global | Détermine si les informations d’identification de connexion saisies par un utilisateur doivent correspondre à la casse des informations d’identification stockées. Options : `Yes` / `No` |
| [!UICONTROL Admin Session Lifetime (seconds)] | Global | Détermine la durée d’une session d’administrateur en secondes. |
| [!UICONTROL Maximum Login Failures to Lockout Account] | Global | Détermine le nombre de tentatives de connexion des utilisateurs administrateurs avant que leurs comptes ne soient verrouillés. Si le champ est vide, aucun minimum n’est défini. Valeur par défaut : `6` |
| [!UICONTROL Lockout Time (minutes)] | Global | Détermine le nombre de minutes pendant lesquelles un compte administrateur est verrouillé avant que l’utilisateur puisse essayer de se reconnecter. Valeur par défaut : `30` |
| [!UICONTROL Password Lifetime (days)] | Global | Détermine le nombre de jours avant l’expiration d’un mot de passe administrateur. Si le champ est vide, aucune durée de vie n’est définie. Valeur par défaut : `90` |
| [!UICONTROL Password Change] | Global | Détermine si les utilisateurs administrateurs doivent modifier leurs mots de passe. Options : <br/>**`Forced`**- Nécessite que les utilisateurs administrateurs modifient leurs mots de passe une fois le compte configuré.<br/>**`Recommended`** - Recommande aux utilisateurs administrateurs de modifier leurs mots de passe une fois le compte configuré. |

{style="table-layout:auto"}

## [!UICONTROL Dashboard]

![Tableau de bord](./assets/admin-dashboard.png)<!-- zoom -->

Pour plus d’informations sur la définition de ces options, voir [Tableau de bord Admin](../../getting-started/admin-dashboard.md) dans le _Guide de démarrage_.

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|----------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Charts] | Global | Détermine si le tableau de bord comprend un graphique généré à partir des données de ventes actuelles. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Grids]

![Grilles d’administration](./assets/admin-admin-grids.png)<!-- zoom -->

Pour plus d’informations sur la définition de ces options, voir [Limiter l’affichage du produit](../../catalog/products-list.md#limit-product-display) dans le _Guide de gestion des catalogues_.

>[!NOTE]
>
>Pour améliorer les performances des catalogues volumineux, il est recommandé de limiter le nombre de produits affichés dans la grille.

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|-----------------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Limit Number of Products in Grid] | Global | Détermine si le nombre de produits affichés dans la grille est limité à la valeur _[!UICONTROL Records Limit]_. Options : `Yes` / `No` |
| [!UICONTROL Records Limit] | Global | Définit la limite de nombre de produits dans la grille de produits. La valeur minimale par défaut est : `20000`. |

## [!UICONTROL CAPTCHA]

![CAPTCHA](./assets/admin-captcha.png)<!-- zoom -->

Pour plus d’informations sur la définition de ces options, voir [CAPTCHA](../../systems/security-captcha.md) dans le _Guide des systèmes d’administration_.

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|-------------------------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable CAPTCHA in Admin] | Global | Active CAPTCHA pour la connexion administrateur. Options : `Yes` / `No` |
| [!UICONTROL Font] | Global | Détermine la police utilisée pour afficher le CAPTCHA. Pour ajouter votre propre police, placez le fichier de police dans le même répertoire que votre instance Commerce, puis ajoutez la déclaration au fichier config.xml à l’adresse `app/code/Magento/Captcha/etc` Police par défaut :` LinLibertine` |
| [!UICONTROL Forms] | Global | Détermine les formulaires dans lesquels CAPTCHA est utilisé. Options : `Admin Login` / `Admin Forgot Password` |
| [!UICONTROL Displaying Mode] | Global | Détermine le moment où le CAPTCHA apparaît. Options : <br/>**`Always`**- CAPTCHA est toujours nécessaire pour se connecter.<br/>**`After number of attempts to login`** - Affiche la variable [!UICONTROL Number of Unsuccessful Attempts to Login] champ . Saisissez le nombre de tentatives de connexion autorisées. La valeur 0 (zéro) est similaire au paramètre Mode d’affichage défini sur Toujours. Cette option ne couvre pas les formulaires Mot de passe oublié et Créer un utilisateur. Si CAPTCHA est activé et défini pour apparaître, il est toujours inclus dans le formulaire.<br />**Remarque**: pour suivre le nombre de tentatives de connexion infructueuses, chaque tentative de connexion sous une adresse électronique et depuis une adresse IP est comptabilisée. Le nombre maximal de tentatives de connexion autorisées à partir d’une même adresse IP est de 1 000. Cette limitation s’applique uniquement lorsque CAPTCHA est activé. |
| [!UICONTROL Number of Unsuccessful Attempts to Login] | Global | Détermine le nombre de tentatives de connexion d’une personne avant que le compte ne soit verrouillé. Pour suivre le nombre de tentatives de connexion infructueuses, le système effectue le suivi des tentatives à partir d’une adresse électronique à partir d’une seule adresse IP. Le nombre maximal de tentatives autorisées à partir d’une même adresse IP est de 1 000. Cette limitation s’applique uniquement si CAPTCHA est activé. |
| [!UICONTROL CAPTCHA Timeout (minutes)] | Global | Détermine la durée de vie du CAPTCHA actuel. Lorsque le CAPTCHA expire, l’utilisateur doit recharger la page. |
| [!UICONTROL Number of Symbols] | Global | Détermine le nombre de symboles utilisés dans le CAPTCHA. La valeur maximale autorisée est `8`. Vous pouvez également spécifier une plage, par exemple : `5-8`. |
| [!UICONTROL Symbols Used in CAPTCHA] | Global | Détermine les symboles utilisés dans le CAPTCHA. Seules les lettres (a-z et A-Z) et les chiffres (0-9) sont autorisées. L’ensemble de symboles par défaut proposé dans le champ exclut les symboles similaires tels que i, l ou 1. L’affichage de ces symboles dans CAPTCHA réduit les chances qu’un utilisateur reconnaisse CAPTCHA correctement. |
| [!UICONTROL Case Sensitive] | Global | Détermine si les caractères utilisés dans le CAPTCHA sont sensibles à la casse. Options : `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Actions Logging]

{{ee-feature}}

![Journalisation des actions d’administration](./assets/admin-actions-logging.png)<!-- zoom -->

Pour plus d’informations sur la définition de ces options, voir [Archive de journal des actions](../../systems/action-log-archive.md) dans le _Guide des systèmes d’administration_.

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|-----------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Actions] | Global | Active la journalisation des actions pour chacune des actions sélectionnées : <br/>`Admin My Account` <br/>`Admin Permission Roles` <br/>`Admin Permission Users` <br/>`Admin Sign In` <br/>`CMS Blocks` <br/>`CMS Hierarchy` <br/>`CMS Pages` <br/>`Cache Management` <br/>`Cart Price Rules` <br/>`Catalog Attributes` <br/>`Catalog Categories` <br/>`Catalog Events` <br/>`Catalog Price Rules` <br/>`Catalog Product Tax Classes` <br/>`Catalog Product Templates` <br/>`Catalog Products` <br/>`Catalog Ratings` <br/>`Catalog Reviews` <br/>`Catalog Search` <br/>`Checkout Terms and Conditions` <br/>`Companies` <br/>`Company Credit` <br/>`Custom Variables` <br/>`Customer Groups` <br/>`Customer Invitations` <br/>`Customer Tax Classes` <br/>`Customers` <br/>`Design Configuration` <br/>`Gift Card Accounts` <br/>`Gift Registry Entity` <br/>`Gift Registry Type` <br/>`Index Management` <br/>`Login as a Customer` <br/>`Manage Currency Rates` <br/>`Manage Customer Address Attributes` <br/>`Manage Customer Attributes` <br/>`Manage Design` <br/>`Manage Dynamic Blocks` <br/>`Manage Segments` <br/>`Manage Store Views` <br/>`Manage Stores` <br/>`Manage Websites` <br/>`Negotiable Quotes` <br/>`Newsletter Queue` <br/>`Newsletter Subscribers` <br/>`Newsletter Templates` <br/>`PayPal Settlement Reports` <br/>`Reports` <br/> `Reward Points Rates` <br/>`Rule-Based Product Relations` <br/>`Sales Archive` <br/>`Sales Credit Memos` <br/>`Sales Invoices` <br/>`Sales Order Status` <br/>`Sales Orders` <br/>`Sales Shipments` <br/>`Shared Catalog` <br/>`Shopping Cart Management` <br/>`Store Credit` <br/>`System Backups` <br/>`System Configuration` <br/>`Tax Rates` <br/>`Tax Rules` <br/>`Transactional Emails` <br/>`URL Rewrites` <br/>`Widget` <br/>`XML Sitemap` |

{style="table-layout:auto"}

## [!UICONTROL Admin Usage]

![Utilisation de l’administrateur](./assets/admin-usage.png)<!-- zoom -->

Pour plus d’informations sur la définition de ces options, voir [Collecte de données d’utilisation](../../getting-started/admin.md#usage-data-collection) dans le _Guide de démarrage_.

| Champ | Portée | Description |
|------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Admin Usage Tracking] | Global | Permet à l’Adobe de collecter les données d’utilisation de l’administrateur afin d’améliorer l’expérience d’utilisation de la variable _Administration_ et les produits et services connexes. L’autorisation de la collecte de données permet également d’activer _Conseils intégrés au produit_ qui est conçu pour intégrer du contenu interactif (aide, info-bulles, guides de présentation, informations d’intégration, annonces de fonctionnalités, etc.) au _Administration_. Les administrateurs individuels ne sont pas identifiés dans les données d’utilisation. Options :<br />**`Yes`**- Permet la collecte de données et active _Conseils intégrés au produit_.<br />**`No`** - N’autorise pas la collecte de données ni n’active _Conseils intégrés au produit_. |

{style="table-layout:auto"}
