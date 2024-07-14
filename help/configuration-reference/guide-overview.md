---
title: Guide de référence de configuration
description: Consultez des informations descriptives sur tous les paramètres de configuration de la boutique d’administrateurs Commerce organisés par les onglets, pages et sections de configuration.
exl-id: b0359ba4-3643-4355-9154-adfedb369ec3
source-git-commit: 323ea635286fcb9a2bcc7f4f56b32c1518a7beef
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Guide de référence de configuration

Ce guide est destiné aux commerçants et aux administrateurs système qui travaillent dans Adobe Commerce ou Magento Open Source. Il fournit des informations de référence pour tous les paramètres de configuration de magasin accessibles à partir de la barre latérale _Admin_ sur **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

Il ne contient pas de détails sur les fonctionnalités d’Adobe Commerce et de Magento Open Source, ni sur les procédures de configuration de magasin.

Ce guide est organisé en fonction de la configuration de la navigation gauche :

| Onglet Configuration | Onglets Enfants |
| ----------------- | ---------- |
| **[!UICONTROL General]** <br/><br/> Les sections de configuration _[!UICONTROL General]_déterminent les paramètres de magasin, les URL, le thème, la devise, les adresses électroniques, les contacts de magasin, l’éditeur et le rapport de tableau de bord. | - [[!UICONTROL General]](./general/general.md)<br>- [[!UICONTROL B2B Features]](./general/b2b-features.md)<br>- [[!UICONTROL Web]](./general/web.md)<br>- [[!UICONTROL Currency Setup]](./general/currency-setup.md)<br>- [[!UICONTROL Store Email Addresses]](./general/store-email-addresses.md)<br>- [[!UICONTROL Contacts]](./general/contacts.md)<br>- [[!UICONTROL Reports]](./general/reports.md)<br>- [[!UICONTROL Content Management]](./general/content-management.md)<br>- [[!UICONTROL New Relic Reporting]](./general/new-relic-reporting.md)<br>- [[!UICONTROL Advanced Reporting]](./general/advanced-reporting.md) |
| **[!UICONTROL Catalog]** <br/><br/> Les paramètres de configuration _[!UICONTROL Catalog]_déterminent les paramètres du produit et de l’inventaire, contrôlent le plan du site et la génération de flux RSS, et spécifient le modèle d’email utilisé pour partager des produits avec des amis. | - [[!UICONTROL Catalog]](./catalog/catalog.md)<br>- [[!UICONTROL Visual Merchandiser]](./catalog/visual-merchandiser.md)<br>- [[!UICONTROL Inventory]](./catalog/inventory.md)<br>- [[!UICONTROL XML Sitemap]](./catalog/xml-sitemap.md)<br>- [[!UICONTROL RSS Feeds]](./catalog/rss-feeds.md)<br>- [[!UICONTROL Email to a Friend]](./catalog/email-to-a-friend.md) |
| **[!UICONTROL Security]** <br/><br/>Les paramètres de configuration _[!UICONTROL Security]_contrôlent la sécurité du magasin, l’authentification à deux facteurs et la fonctionnalité Google reCAPTCHA. | - [[!UICONTROL 2FA]](./security/2fa.md)<br>- [[!UICONTROL Google reCAPTCHA Admin Panel]](./security/google-recaptcha-admin.md)<br>- [[!UICONTROL Google reCAPTCHA Storefront]](./security/google-recaptcha-storefront.md)<br>- [[!UICONTROL Security.txt]](./security/security-txt.md) |
| **[!UICONTROL Customers]** <br/><br/> Les paramètres de configuration _[!UICONTROL Customers]_établissent les options de base de connexion et de compte client, les paramètres de newsletter, la liste de souhaits et le format des codes de bons générés automatiquement. | - [[!UICONTROL Login as Customer]](./customers/login-as-customer.md)<br>- [[!UICONTROL Newsletter]](./customers/newsletter.md)<br>- [[!UICONTROL Company Configuration]](./customers/company-configuration.md)<br>- [[!UICONTROL Customer Configuration]](./customers/customer-configuration.md)<br>- [[!UICONTROL Requisition Lists]](./customers/requisition-lists.md)<br>- [[!UICONTROL Wish List]](./customers/wishlist.md)<br>- [[!UICONTROL Invitations]](./customers/invitations.md)<br>- [[!UICONTROL Reward Points]](./customers/reward-points.md)<br>- [[!UICONTROL Promotions]](./customers/promotions.md)<br>- [[!UICONTROL Gift Registry]](./customers/gift-registry.md)<br>- [[!UICONTROL Persistent Shopping Cart]](./customers/persistent-shopping-cart.md) |
| **[!UICONTROL Sales]** <br/><br/> Les paramètres de configuration _[!UICONTROL Sales]_déterminent les paramètres de passage en caisse et de taxe, les options de paiement et d’expédition, les envois d’emails et de PDF et les paramètres de l’API Google. | - [[!UICONTROL Sales]](./sales/sales.md)<br>- [[!UICONTROL Sales Emails]](./sales/sales-emails.md)<br>- [[!UICONTROL Quotes]](./sales/quotes.md)<br>- [[!UICONTROL PDF Print-outs]](./sales/pdf-print-outs.md)<br>- [[!UICONTROL Tax]](./sales/tax.md)<br>- [[!UICONTROL Checkout]](./sales/checkout.md)<br>- [[!UICONTROL Shipping Settings]](./sales/shipping-settings.md)<br>- [[!UICONTROL Multishipping Settings]](./sales/multishipping-settings.md)<br>- [[!UICONTROL Delivery Methods]](./sales/delivery-methods.md)<br>- [[!UICONTROL Google API]](./sales/google-api.md)<br>- [[!UICONTROL 3D Secure]](./sales/3d-secure.md)<br>- [[!UICONTROL Gift Cards]](./sales/gift-cards.md)<br>- [[!UICONTROL Payment Methods]](./sales/payment-methods.md) |
| **[!UICONTROL Sales Channels]** <br/><br/>Lorsque l’extension [!DNL Amazon Sales Channel] est installée, les paramètres _[!UICONTROL Sales Channels]_contrôlent les opérations d’intégration automatisée avec votre boutique Amazon. | - [[!UICONTROL Global Settings]](sales-channels.md) |
| **[!UICONTROL Services]** <br/><br/>Les paramètres de configuration _[!UICONTROL Services]_déterminent les paramètres d’intégration de l’API Commerce, y compris SOAP et OAuth. | - [[!UICONTROL Web API]](./services/magento-web-api.md)<br>- [[!UICONTROL Commerce Services]](./services/saas.md)<br>- [[!UICONTROL OAuth]](./services/oauth.md) |
| **[!UICONTROL Advanced]** <br/><br/> Les paramètres de configuration _[!UICONTROL Advanced]_déterminent les paramètres d’administration par défaut, divers paramètres de configuration du système, des contrôles de module avancés et des outils de développement. | - [[!UICONTROL Admin]](./advanced/admin.md)<br>- [[!UICONTROL System]](./advanced/system.md)<br>- [[!UICONTROL Developer]](./advanced/developer.md) |

{style="table-layout:auto"}

Il ne contient pas de détails sur les fonctionnalités d’Adobe Commerce et de Magento Open Source, ni sur les procédures de configuration de magasin.

## Documentation disponible

{{docs-links}}
