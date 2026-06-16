---
title: Modèles d’e-mail
description: Découvrez les modèles d’e-mail et comment les utiliser pour prendre en charge les communications avec vos clients et renforcer votre marque.
exl-id: dfe28c77-607e-41e4-b872-3a07bcd67962
feature: Communications, Configuration
TQID: https://experienceleague.adobe.com/b2RVtAEBH78pLiFPb-HKBbhGhLa-npNL54-cvmlEosA
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1153
ht-degree: 0%

---

# Modèles d’e-mail

Les modèles d’e-mail définissent la disposition, le contenu et la mise en forme des messages automatisés envoyés depuis votre boutique. Ils sont appelés e-mails transactionnels , car chacun est associé à un type de transaction ou d’événement spécifique.

Commerce comprend un ensemble de modèles d’e-mail réactifs qui sont déclenchés par divers événements qui se produisent pendant le fonctionnement de votre boutique. Chaque modèle est optimisé pour n’importe quelle taille d’écran et peut être affiché sur le bureau, ainsi que sur des tablettes et des appareils mobiles. Il existe différents modèles d’e-mail préparés relatifs aux activités des clients, aux ventes, aux alertes de produits, aux actions d’administration et aux messages système que vous pouvez [personnaliser](email-template-custom.md) pour refléter votre marque.

Les e-mails Commerce peuvent être rendus par les clients de messagerie HTML et en texte brut. Il peut y avoir des variations entre les clients dans la façon dont les e-mails sont rendus.

## Préparer le logo de votre e-mail

Les logos peuvent être enregistrés sous l’un des types de fichiers suivants. Les logos avec arrière-plans transparents peuvent être enregistrés au format .GIF ou .PNG.

- JPG/JPEG
- GIF
- PNG

Des dimensions sont spécifiées dans le modèle d’en-tête. Toutefois, pour que votre logo s’affiche correctement sur les appareils haute résolution, l’image chargée doit avoir une taille trois fois supérieure. En règle générale, l’illustration du logo original est créée sous la forme d’une image vectorielle, afin qu’elle puisse être redimensionnée sans perdre en résolution. L’image peut ensuite être enregistrée dans l’un des formats d’image bitmap pris en charge.

<!-- ![Logo 3X display size](./assets/email-logo-third-size.png)-->

Pour tirer parti de l’espace vertical limité de l’en-tête, veillez à recadrer l’image afin d’éliminer tout espace perdu en haut ou en bas. Lors de la modification de l’image, veillez à conserver les proportions du logo, de sorte que la hauteur et la largeur soient redimensionnées proportionnellement.

En règle générale, vous pouvez réduire une image par rapport à son format d’origine, mais pas l’agrandir sans perdre en résolution. Le fait de prendre une petite image et de la mettre à l’échelle dans un éditeur de photos réduit la résolution de l’image. Par exemple, si les dimensions d’affichage du logo sont de 168 pixels de large sur 48 pixels de haut dans le modèle d’en-tête, l’image chargée doit avoir une largeur de 504 pixels de large sur 144 pixels de haut.

| Dimensions du logo | 1 x (taille d’affichage) | 3 x (taille de l’image) |
|----------|----|----|
| Largeur : | 168 px | 504 px |
| Hauteur : | 48 px | 144 px |

{style="table-layout:auto"}

## Configurer des modèles d’e-mail

La configuration détermine le logo qui apparaît dans le modèle d’en-tête par défaut, ainsi que tout modèle [en-tête](email-template-custom.md#header-template) et [pied de page](email-template-custom.md#footer-template) personnalisé que vous souhaitez utiliser pour les e-mails transactionnels envoyés à partir de vos magasins.

![Conception d’e-mail transactionnel](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

Pour obtenir la liste détaillée des paramètres de configuration, voir [_E-mails transactionnels_](../content-design/configuration.md) dans le _Guide de conception et de contenu_.

## Étape 1. Chargez Votre Logo

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Recherchez la vue de magasin que vous souhaitez configurer, puis cliquez sur **[!UICONTROL Edit]** dans la colonne _[!UICONTROL Action]_.

1. Sous _[!UICONTROL Other Settings]_, développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL Transactional Emails]**.

1. Pour charger le **[!UICONTROL Logo Image]** préparé, cliquez sur **[!UICONTROL Upload]** et sélectionnez le fichier sur le système.

1. Par **[!UICONTROL Logo Image Alt]**, saisissez un texte secondaire pour identifier l’image.

1. Saisissez le **[!UICONTROL Logo Width]** et le **[!UICONTROL Logo Height]** en pixels.

   Saisissez chaque valeur sous la forme d’un nombre, sans l’abréviation `px`. Ces valeurs font référence aux dimensions d’affichage du logo dans l’en-tête, et non à la taille réelle de l’image.

## Étape 2. Choisir les modèles d’en-tête et de pied de page

Si vous disposez de modèles d’en-tête et de pied de page personnalisés pour votre boutique ou pour différentes boutiques, vous pouvez spécifier les modèles à utiliser pour chacune d’elles, en fonction de la [portée](../getting-started/websites-stores-views.md#scope-settings) de la configuration. Dans le cas contraire, les modèles par défaut sont utilisés. Pour en savoir plus, voir [Personnalisation des modèles d’e-mail](email-template-custom.md).

1. Choisissez le **[!UICONTROL Header Template]** à utiliser pour tous les e-mails transactionnels.

1. Choisissez le **[!UICONTROL Footer Template]** à utiliser pour tous les e-mails transactionnels.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Liste des modèles d&#39;email

La liste des modèles d’e-mail est organisée par module par ordre alphabétique.

### [!DNL Amazon_Payment]

| Modèle | Chemin de configuration |
|--- |--- |
| `Hard-declined Authorization` | s.o. |
| `Soft-declined Authorization` | s.o. |

{style="table-layout:auto"}

### [!DNL Magento_Checkout]

| Modèle | Chemin de configuration |
|--- |--- |
| `Payment Failed` | **Page:** [!UICONTROL Sales] > [[!UICONTROL Checkout]](../configuration-reference/sales/checkout.md)<br/>**Section:** [!UICONTROL Payment Failed Emails]<br/>**Champ:** [!UICONTROL Payment Failed Template] |

{style="table-layout:auto"}

### [!DNL Magento_Company]

![Adobe Commerce B2B](../assets/b2b.svg) (disponible avec Adobe Commerce B2B uniquement)

| Modèle | Chemin de configuration |
|--- |--- |
| `Assign Company Admin` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Section:** [!UICONTROL Customer-Related Emails]<br/>**Champ:** [!UICONTROL Default 'Assign Company Admin' Email] |
| `Assign Company to Customer` | **Page:** [!UICONTROL Customers] > [Configuration de la société&#x200B;](../configuration-reference/customers/company-configuration.md)<br/>**Section:** [!UICONTROL Customer-Related Emails] <br/>**Champ:** [!UICONTROL Default 'Assign Company to Customer' Email] |
| `Company Admin Changed to Member` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Section:** [!UICONTROL Customer-Related Emails]<br/>**Champ:** [!UICONTROL Default 'Company Admin Changed To Member' Email] |
| `Company Admin Set Inactive` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Section:** [!UICONTROL Customer-Related Emails]<br/>**Champ:** [!UICONTROL Default 'Customer Status Inactive' Email] |
| `Company Invite` | s.o. |
| `Company Registration Request` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Section:** [!UICONTROL Email Options - Company Registration]<br/>**Champ:** [!UICONTROL Default Company Registration Email] |
| `Company Status Active1` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Section:** [!UICONTROL Company Status Change]<br/>**Champ:** [!UICONTROL Default 'Company Status Change To Active 1" Email] |
| `Company Status Active2` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Section:** [!UICONTROL Company Status Change]<br/>**Champ:** [!UICONTROL Default 'Company Status Change To Active 2" Email] |
| `Company Status Blocked` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Section:** [!UICONTROL Company Status Change]<br/>**Champ:** [!UICONTROL Default 'Company Status Change To Blocked" Email] |
| `Company Status Pending Approval` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Section:** [!UICONTROL Company Status Change]<br/>**Champ:** [!UICONTROL Default 'Company Status Change To Pending Approval" Email] |
| `Company Status Rejected` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Section:** [!UICONTROL Company Status Change]<br/>**Champ:** [!UICONTROL Default 'Company Status Change To Rejected" Email] |
| `Customer Status Active` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Section:** [!UICONTROL Customer-Related Emails]<br/>**Champ:** [!UICONTROL Default 'Customer Status Active' Email] |
| `Customer Status Inactive` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Section:** [!UICONTROL Customer-Related Emails]<br/>**Champ:** [!UICONTROL Default 'Company Admin Inactive' Email] |
| `Sales Representative Assigned to Company` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Section:** [!UICONTROL Customer-Related Emails]<br/>**Champ:** [!UICONTROL Default 'Sales Rep Assigned' Email] |

{style="table-layout:auto"}

### [!DNL Magento_CompanyCredit]

![Adobe Commerce B2B](../assets/b2b.svg) (disponible avec Adobe Commerce B2B uniquement)

| Modèle | Chemin de configuration |
|--- |--- |
| `Credit Limit Allocated` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Section:** [!UICONTROL Company Credit]<br/>**Champ:** [!UICONTROL Allocated Email Template] |
| `Credit Limit Updated` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Section:** [!UICONTROL Company Credit]<br/>**Champ:** [!UICONTROL Updated Email Template] |
| `Credit Reimbursed` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Section:** [!UICONTROL Company Credit]<br/>**Champ:** [!UICONTROL Reimbursed Email Template] |
| `Order Refunded to Company Credit` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Section:** [!UICONTROL Company Credit]<br/>**Champ:** [!UICONTROL Refunded Email Template] |
| `Order Reverted to Company Credit` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Section:** [!UICONTROL Company Credit]<br/>**Champ:** [!UICONTROL Reverted Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Contact]

| Modèle | Chemin de configuration |
|--- |--- |
| `Contact Form` | **Page:** [!UICONTROL General] > [[!UICONTROL Contacts]](../configuration-reference/general/contacts.md)<br/>**Section:** [!UICONTROL Email Options]<br/>**Champ:** [!UICONTROL Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Customer]

| Modèle | Chemin de configuration |
|--- |--- |
| `Change Email` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Section:** [!UICONTROL Account Information Options]<br/>**Champ:** [!UICONTROL Change Email Template] |
| Modifier l’e-mail et le mot de passe | **Page:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Section:** [!UICONTROL Account Information Options]<br/>**Champ:** [!UICONTROL Change Email and Password Template] |
| `Forgot Password` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Section:** [!UICONTROL Password Options]<br/>**Champ:** Modèle d’e-mail oublié |
| `New Account` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Section:** [!UICONTROL Create New Account Options]<br/>**Champ:** E-Mail De Bienvenue Par Défaut |
| `New Account (Magento/luma)` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Section:** [!UICONTROL Create New Account Options]<br/>**Champ:** E-Mail De Bienvenue Par Défaut |
| `New Account Confirmation Key` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Section:** [!UICONTROL Create New Account Options]<br/>**Champ:** E-Mail Du Lien De Confirmation |
| `New Account Confirmed` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Section:** [!UICONTROL Create New Account Options]<br/>**Champ:** E-Mail De Bienvenue |
| `New Account Without Password` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Section:** [!UICONTROL Create New Account Options]<br/>**Champ:** E-Mail De Bienvenue Par Défaut Sans Mot De Passe |
| `Remind Password` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Section:** [!UICONTROL Password Options]<br/>**Champ:** Modèle D’E-Mail De Rappel |
| `Reset Password` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Section:** [!UICONTROL Password Options] <br/>**Champ:** Réinitialiser le modèle de mot de passe |

{style="table-layout:auto"}

### [!DNL Magento_CustomerBalance]

![](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

| Modèle | Chemin de configuration |
|--- |--- |
| `Store Credit Update` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Section:** [!UICONTROL Store Credit Options]<br/>**Champ:** [!UICONTROL Store Credit Update Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Directory]

| Modèle | Chemin de configuration |
|--- |--- |
| `Currency Update Warnings` | **Page:** [!UICONTROL General] > [[!UICONTROL Currency Setup]](../configuration-reference/general/currency-setup.md)<br/>**Section:** [!UICONTROL Scheduled Import Settings]<br/>**Champ:** [!UICONTROL Error Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Email]

| Modèle | Chemin de configuration |
|--- |--- |
| `Footer` | s.o. |
| `Footer (Magento/luma)` | s.o. |
| `Header` | s.o. |

{style="table-layout:auto"}

### [!UICONTROL Magento_GiftCard]

![](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

| Modèle | Chemin de configuration |
|--- |--- |
| `Gift Card(s) Purchase` | **Page:** [!UICONTROL Sales] > [[!UICONTROL Gift Cards]](../catalog/product-gift-card-create.md)<br/>**Section:** [!UICONTROL Gift Card Email Settings]<br/>**Champ:** [!UICONTROL Gift Card Notification Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_GiftCardAccount]

| Modèle | Chemin de configuration |
|--- |--- |
| `Gift Card Code/Balance` | **Page:** [!UICONTROL Sales] > [[!UICONTROL Gift Cards]](../catalog/product-gift-card-create.md)<br/>**Section:** [!UICONTROL Email Sent from Gift Card Account Management]<br/>**Champ:** [!UICONTROL Gift Card Template] |

{style="table-layout:auto"}

### [!DNL Magento_GiftRegistry]

| Modèle | Chemin de configuration |
|--- |--- |
| `New Registry` | **Page:** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**Section:** [!UICONTROL Owner Notification]<br/>**Champ:** [!UICONTROL Email Template] |
| `Registry Sharing` | **Page:** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**Section:** [!UICONTROL Gift Registry Sharing]<br/>**Champ:** [!UICONTROL Email Template] |
| `Registry Update` | **Page:** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**Section:** [!UICONTROL Gift Registry Update]<br/>**Champ:** [!UICONTROL Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_InventoryInStorePickupSales]

| Modèle | Chemin de configuration |
|--- |--- |
| `Order is Ready for Pickup` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL Order Ready For Pickup in Store]<br/>**Champ:** [!UICONTROL Order Ready For Pickup Email Template] |
| `Order is Ready for Pickup For Guest` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL Order Ready For Pickup in Store]<br/>**Champ:** [!UICONTROL Order Ready For Pickup Email Template for Guest] |

{style="table-layout:auto"}

### [!DNL Magento_Invitation]

| Modèle | Chemin de configuration |
|--- |--- |
| `Customer Invitation` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Invitation]](../configuration-reference/customers/invitations.md)<br/>**Section:** [!UICONTROL Email]<br/>**Champ:** [!UICONTROL Customer Invitation Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_NegotiableQuote]

![Adobe Commerce B2B](../assets/b2b.svg) (disponible avec Adobe Commerce B2B uniquement)

| Modèle | Chemin de configuration |
|--- |--- |
| `Declined Quote` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL Quote]<br/>**Champ:** [!UICONTROL Declined Quote Template (to Buyer)] |
| `Expiration Date Reset` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL Quote]<br/>**Champ:** [!UICONTROL Expiration Date Reset]<br/> **Page:** [!UICONTROL Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL Quote]<br/>**Champ:** [!UICONTROL Order Ready For Pickup Email Template] |
| `Expiration Warning` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL Quote]<br/>**Champ:** [!UICONTROL Quote Expiration (in 48 hrs)] |
| `Expiration Warning1` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL Quote]<br/>**Champ:** [!UICONTROL Quote Expiration (in 24 hrs)] |
| `New Quote` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL Quote]<br/>**Champ:** [!UICONTROL New Quote Template (to Seller)] |
| `Updated Quote` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL Quote]<br/>**Champ:** [!UICONTROL Updated Quote Template (to Seller)] |

{style="table-layout:auto"}

### [!DNL Magento_Newsletter]

| Modèle | Chemin de configuration |
|--- |--- |
| `Subscription Confirmation` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**Section:** [!UICONTROL  Subscription Options]<br/>**Champ:** [!UICONTROL Confirmation Email Template] |
| `Subscription Success` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**Section:** [!UICONTROL  Subscription Options]<br/>**Champ:** [!UICONTROL Success Email Template] |
| `Unsubscription Success` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**Section:** [!UICONTROL  Subscription Options]<br/>**Champ:** [!UICONTROL Unsubscription Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_ProductAlert]

| Modèle | Chemin de configuration |
|--- |--- |
| `Cron Error Warning` | **Page:** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**Section:** [!UICONTROL Product Alerts Run Settings]<br/>**Champ:** [!UICONTROL Error Email Template] |
| `Price Alert` | **Page:** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**Section:** [!UICONTROL Product Alerts]<br/>**Champ:** [!UICONTROL Price Alert Email Template] |
| `Stock Alert` | **Page:** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**Section:** [!UICONTROL Product Alerts]<br/>**Champ:** [!UICONTROL Stock Alert Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_PurchaseOrder]

| Modèle | Chemin de configuration |
|--- |--- |
| `Approved Purchase Order` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL Purchase Order Approval]<br/>**Champ:** [!UICONTROL Approved Purchase Order] |
| `Approved, requires payment` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL Purchase Order Approval]<br/>**Champ:** [!UICONTROL Approved, requires payment details (to Buyer)] |
| `Comment added to Purchase Order` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL Purchase Order Approval]<br/>**Champ:** [!UICONTROL Comment added to Purchase Order] |
| `Created and Auto-approved Purchase Order` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL Purchase Order Approval]<br/>**Champ:** [!UICONTROL Created and Automatically approved Purchase Order (to Buyer)] |
| `Created and automatically approved, requires payment details` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL Purchase Order Approval]<br/>**Champ:** [!UICONTROL Created and automatically approved, requires payment details (to Buyer)] |
| `Created and requires Approval Purchase Order` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL Purchase Order Approval]<br/>**Champ:** [!UICONTROL Created and requires Approval Purchase Order (to Buyer)] |
| `Error creating Order from Purchase Order` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL Purchase Order Approval]<br/>**Champ:** [!UICONTROL Error creating Order from Purchase Order (to Buyer)] |
| `Purchase Order requires Approval` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL Purchase Order Approval]<br/>**Champ:** [!UICONTROL Purchase Order requires Approval (to Approver)] |
| `Rejected Purchase Order` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL Purchase Order Approval]<br/>**Champ:** [!UICONTROL Rejected Purchase Order (to Buyer)] |

{style="table-layout:auto"}

### [!DNL Magento_Reminder]

![](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

| Modèle | Chemin de configuration |
|--- |--- |
| `Promotion Notification/Reminder` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Promotions]](../configuration-reference/customers/promotions.md)<br/>**Section:** [!UICONTROL Automated Email Reminder Rules]<br/>**Champ:** [!UICONTROL Reminder Email Sender] |

{style="table-layout:auto"}

### [!DNL Magento_Reward]

![](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

| Modèle | Chemin de configuration |
|--- |--- |
| `Balance Update` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Reward Points]](../configuration-reference/customers/reward-points.md)<br/>**Section:** [!UICONTROL Email Notification Settings]<br/>**Champ:** [!UICONTROL Balance Update Email] |
| `Points Expiry Warning` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Reward Points]](../configuration-reference/customers/reward-points.md)<br/>**Section:** [!UICONTROL Email Notification Settings]<br/>**Champ:** [!UICONTROL Reward Points Expiry Warning Email] |

{style="table-layout:auto"}

### [!DNL Magento_Rma]

![](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

| Modèle | Chemin de configuration |
|--- |--- |
| `New RMA` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL  RMA]<br/>**Champ:** [!UICONTROL RMA Email Template] |
| `New RMA for Guest` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL  RMA]<br/>**Champ:** [!UICONTROL RMA Email Template for Guest] |
| `RMA Admin Comments` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL  RMA Admin Comments]<br/>**Champ:** [!UICONTROL RMA Comment Email Template] |
| `RMA Admin Comments for Guest` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL  RMA Admin Comments]<br/>**Champ:** [!UICONTROL RMA Comment Email Template for Guest] |
| `RMA Authorization` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL  RMA Authorization]<br/>**Champ:** [!UICONTROL RMA Authorization Email Template] |
| `RMA Authorization for Guest` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL  RMA Authorization]<br/>**Champ:** [!UICONTROL RMA Authorization Email Template for Guest] |
| `RMA Customer Comments` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Section:** [!UICONTROL RMA Customer Comments]<br/>**Champ:** [!DNL RMA Comment Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Sales]

| Modèle | Chemin de configuration |
|--- |--- |
| `Credit Memo Update` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Credit Memo Contents]<br/>**Champ:** [!UICONTROL Credit Memo Comment Email Template] |
| `Credit Memo Update (Magento/luma)` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Credit Memo Comments]<br/>**Champ:** [!UICONTROL Credit Memo Comment Email Template] |
| `Credit Memo Update for Guest` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Credit Memo Comments]<br/>**Champ:** [!UICONTROL Credit Memo Comment Email Template for Guest] |
| `Credit Memo Update for Guest (Magento/luma)` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Credit Memo Comments]<br/>**Champ:** [!UICONTROL Credit Memo Comment Email Template for Guest] |
| `Invoice Update` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Invoice Comments]<br/>**Champ:** [!UICONTROL Invoice Comment Email Template] |
| `Invoice Update (Magento/luma)` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Invoice Comments]<br/>**Champ:** [!UICONTROL Invoice Comment Email Template] |
| `Invoice Update for Guest` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Invoice Comments]<br/>**Champ:** [!UICONTROL Invoice Comment Email Template for Guest] |
| `Invoice Update for Guest (Magento/luma)` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Invoice Comments]<br/>**Champ:** [!UICONTROL Invoice Comment Email Template for Guest] |
| `New Credit Memo` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Credit Memo]<br/>**Champ:** [!UICONTROL Credit Memo Email Template] |
| `New Credit Memo (Magento/luma)` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]]../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Credit Memo]<br/>**Champ:** [!UICONTROL Credit Memo Email Template] |
| `New Credit Memo for Guest` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Credit Memo]<br/>**Champ:** [!UICONTROL Credit Memo Email Template for Guest] |
| `New Credit Memo for Guest (Magento/luma)` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Credit Memo]<br/>**Champ:** [!UICONTROL Credit Memo Email Template for Guest] |
| `New Invoice` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Invoice]<br/>**Champ:** [!UICONTROL Invoice Email Template] |
| `New Invoice (Magento/luma)` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Invoice]<br/>**Champ:** [!UICONTROL Invoice Email Template] |
| `New Invoice for Guest` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Invoice]<br/>**Champ:** [!UICONTROL Invoice Email Template for Guest] |
| `New Invoice for Guest (Magento/luma)` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Invoice]<br/>**Champ:** [!UICONTROL Invoice Email Template for Guest] |
| `New Order` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Order]<br/>**Champ:** [!UICONTROL New Order Confirmation Template] |
| `New Order (Magento/luma)` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Order]<br/>**Champ:** [!UICONTROL New Order Confirmation Template] |
| `New Order for Guest` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Order]<br/>**Champ:** [!UICONTROL New Order Confirmation Template for Guest] |
| `New Order for Guest (Magento/luma)` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Order]<br/>**Champ:** [!UICONTROL New Order Confirmation Template for Guest] |
| `New Shipment` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Shipment]<br/>**Champ:** [!UICONTROL Shipment Email Template] |
| `New Shipment (Magento/luma)` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Shipment]<br/>**Champ:** [!UICONTROL Shipment Email Template] |
| `New Shipment for Guest` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Shipment]<br/>**Champ:** [!UICONTROL Shipment Email Template for Guest] |
| `New Shipment for Guest (Magento/luma)` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Shipment]<br/>**Champ:** [!UICONTROL Shipment Email Template for Guest] |
| `Order Update` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Order Comments]<br/>**Champ:** [!UICONTROL Order Comment Email Template] |
| `Order Update (Magento/luma)` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Order Comments]<br/>**Champ:** [!UICONTROL Order Comment Email Template] |
| `Order Update for Guest` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Order Comments]<br/>**Champ:** [!UICONTROL Order Comment Email Template for Guest] |
| `Order Update for Guest (Magento/luma)` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Order Comments]<br/>**Champ:** [!UICONTROL Order Comment Email Template for Guest] |
| `Shipment Update` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Shipment Comments]<br/>**Champ:** [!UICONTROL Shipment Comment Email Template] |
| `Shipment Update (Magento/luma)` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Shipment Comments]<br/>**Champ:** [!UICONTROL Shipment Comment Email Template] |
| `Shipment Update for Guest` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Shipment Comments]<br/>**Champ:** [!UICONTROL Shipment Comment Email Template for Guest] |
| `Shipment Update for Guest (Magento/luma)` | **Page:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Section:** [!UICONTROL Shipment Comments]<br/>**Champ:** [!UICONTROL Shipment Comment Email Template for Guest] |

{style="table-layout:auto"}

### [!DNL Magento_ScheduledImportExport]

![](../assets/adobe-logo.svg) (Adobe Commerce uniquement)

| Modèle | Chemin de configuration |
|--- |--- |
| `Export Failed` | **Page:** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**Section:** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**Champ:** [!UICONTROL Export Failed Template] |
| `File History Clean Failed` | **Page:** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**Section:** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**Champ:** [!UICONTROL Error Email Template] |
| `Import Failed` | **Page:** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**Section:** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**Champ:** [!UICONTROL Import Failed Template] |

{style="table-layout:auto"}

### [!DNL Magento_SendFriend]

| Modèle | Chemin de configuration |
|--- |--- |
| `Send Product Link to Friend` | **Page:** [!UICONTROL Catalog] > [[!UICONTROL Email to a Friend]](../configuration-reference/catalog/email-to-a-friend.md)<br/>**Section:** [!UICONTROL Email Templates]<br/>**Champ:** [!UICONTROL Select Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Sitemap]

| Modèle | Chemin de configuration |
|--- |--- |
| `Sitemap Generation Settings` | **Page:** [!UICONTROL Catalog] > [[!UICONTROL XML Sitemap]](../configuration-reference/catalog/xml-sitemap.md)<br/>**Section:** [!UICONTROL Generation Settings]<br/>**Champ:** [!UICONTROL Error Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_TwoFactorAuth]

| Modèle | Chemin de configuration |
|--- |--- |
| `2FA Configuration Required by User` | s.o. |
| `2FA Configuration Required for the Application` | s.o. |

{style="table-layout:auto"}

### [!DNL Magento_User]

| Modèle | Chemin de configuration |
|--- |--- |
| `Forgot Admin Password` | **Page:** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**Section:** [!UICONTROL Admin User Emails]<br/>**Champ:** Modèle d’e-mail Mot de passe oublié |
| `User Notification` | **Page:** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**Section:** [!UICONTROL Admin User Emails]<br/>**Champ:** Modèle De Notification De L’Utilisateur |
| `New User Notification` | **Page:** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**Section:** [!UICONTROL Admin User Emails]<br/>**Champ:** [!UICONTROL New User Notification Template] |

{style="table-layout:auto"}

### [!DNL Magento_Wishlist]

| Modèle | Chemin de configuration |
|--- |--- |
| `Magento Wish List Sharing` | **Page:** [!UICONTROL Customers] > [[!UICONTROL Wish List]](../configuration-reference/customers/wishlist.md)<br/>**Section:** [!UICONTROL Share Options]<br/>**Champ:** [!UICONTROL Email Template] |

{style="table-layout:auto"}
