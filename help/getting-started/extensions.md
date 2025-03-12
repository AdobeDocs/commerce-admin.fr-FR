---
title: Extensions à partir d’Adobe
description: Consultez les informations sur les extensions d’Adobe Commerce et de Magento Open Source publiées par Adobe.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 0%

---

# Extensions à partir d’Adobe

Cette rubrique fournit des informations sur les extensions d’Adobe Commerce et de Magento Open Source publiées par Adobe. Les extensions ajoutent des fonctionnalités, des services et des intégrations à Admin et au storefront. Certaines de ces extensions sont développées par le biais de contributions de la communauté Magento Open Source. Certaines extensions nécessitent une installation distincte et d’autres sont installées par défaut.

## Extensions installées

Certaines extensions sont automatiquement installées avec Adobe Commerce ou Magento Open Source.

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) offre une gestion améliorée des stocks et des expéditions sur un ou plusieurs sites et canaux de vente avec une protection de passage en caisse et des algorithmes de rapprochement des expéditions simultanés. Suivez vos quantités en stock, fournissez des quantités de stock vendables précises aux clients et expédiez-les selon des recommandations ou des sélections manuelles pour contrôler l&#39;ensemble de votre stock. Configurez les paramètres de gestion globalement, par source et par produit.

>[!NOTE]
>
>Cette extension a été développée dans le cadre du projet [[!DNL Inventory Management]](https://github.com/magento/inventory) (anciennement MSI) par le biais du programme de génie communautaire.

[!DNL Inventory Management] s’installe avec toutes les fonctionnalités activées par défaut. Aucune étape supplémentaire n&#39;est nécessaire pour activer ces fonctions d&#39;inventaire. Pour plus d’informations sur les fonctionnalités de [!DNL Inventory Management], consultez le [[!DNL Inventory Management] Guide de l’utilisateur](../inventory-management/guide-overview.md).

### Braintree

PayPal et Gene Commerce ont développé ensemble l&#39;extension Braintree officielle pour les magasins Commerce 2.4.x. Offrant une expérience de passage en caisse améliorée conçue pour stimuler la conversion, les mises à jour comprennent des options PayLater qui affichent automatiquement les messages et boutons PayLater pertinents aux consommateurs lors de l&#39;achat et pendant le passage en caisse.

Cette extension est installée par défaut, mais nécessite un compte [Braintree](https://www.braintreepayments.com/) ainsi qu’une configuration dans l’interface d’administration pour être activée pour votre boutique. Pour déterminer les frais applicables lors de l&#39;utilisation de Braintree pour traiter vos transactions, vérifiez le prix de [Braintree](https://www.braintreepayments.com/braintree-pricing).

Pour plus d’informations sur la configuration de Braintree dans Admin, consultez la rubrique [Braintree](../stores-purchase/braintree.md) dans le _Guide de l’expérience client_.

### Google reCAPTCHA

Google reCAPTCHA offre un niveau de sécurité plus élevé pour le storefront et l’interface utilisateur d’administration que celui disponible avec le CAPTCHA standard, et vous permet d’effectuer les opérations suivantes :

- Vérifiez quand les clients créent des comptes, récupèrent des mots de passe, se connectent à leurs comptes ou contactent votre entreprise.
- Amélioration de la sécurité lorsque les utilisateurs administrateurs se connectent.

Cela réduit le risque d’erreur de l’utilisateur lors de la saisie d’un code Captcha et encourage la conversion du panier sans ajouter de obstacles lors du passage en caisse. [Activez et configurez reCAPTCHA](../systems/security-google-recaptcha.md) à l’aide de contrôles invisibles ou interactifs pour améliorer l’accès sécurisé à l’administrateur [!DNL Commerce] et au storefront.

### Authentification à deux facteurs

L’administrateur [!DNL Commerce] fournit un accès complet à votre magasin, à vos commandes et aux données de vos clients. [Authentification à deux facteurs](../systems/security-two-factor-authentication.md) (2FA ou TFA) améliore la sécurité en exigeant une authentification supplémentaire, au-delà du nom d’utilisateur et du mot de passe standard, pour accéder à [!DNL Commerce] Admin depuis tous les appareils. L’extension prend en charge plusieurs authentificateurs, y compris les clés Google Authenticator, Authy, [!DNL Duo] et U2F. Cette authentification s’applique uniquement aux utilisateurs administrateurs. Il n’est pas disponible pour les comptes clients storefront.

Ces fonctionnalités sont activées par défaut. Chaque utilisateur administrateur doit installer et configurer l’un des authentificateurs pris en charge.

>[!NOTE]
>
>Les magasins Adobe Commerce qui ont activé l’authentification Adobe Identity Management Services (IMS) pour l’administrateur ont Commerce 2FA natif désactivé. Les utilisateurs connectés à Admin avec leurs informations d’identification Adobe n’ont pas besoin de s’authentifier à nouveau pour de nombreuses tâches d’administration. L’authentification est gérée par Adobe IMS lorsque l’utilisateur administrateur se connecte à sa session en cours. Voir [Présentation de l’intégration du service Adobe Identity Management (IMS)](./adobe-ims-integration-overview.md).

## Extensions à ajouter

Le [[!DNL Commerce Marketplace]](https://marketplace.magento.com/) est la ressource mondiale d’e-commerce pour les applications et les services qui étendent [!DNL Commerce] solutions grâce à de nouvelles fonctionnalités puissantes. Adobe publie plusieurs extensions par le biais du [!DNL Marketplace] qui peuvent être installées et configurées dans votre boutique Adobe Commerce ou Magento Open Source afin de fournir des intégrations et des fonctionnalités améliorées.

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce uniquement

L’extension [!DNL Live Search] connecte votre boutique au service Live Search, une plateforme de recherche gratuite d’Adobe Commerce qui permet aux vendeurs de proposer aux clients une expérience de recherche améliorée par l’IA. Conçu avec l’intelligence artificielle d’Adobe, Adobe Sensei, le facettage intelligent permet aux commerçants de faire plus avec moins en supprimant le travail manuel de facettisation/filtrage.

Pour plus d’informations, consultez le [Guide d’utilisation de Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/guide-overview.html).

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce uniquement

L’extension [!DNL Product Recommendations] connecte votre boutique au service de recommandations de produits, un puissant outil marketing que vous pouvez utiliser pour augmenter les conversions, les recettes et l’engagement. [!DNL Product Recommendations] a été créé par Adobe Commerce et repose sur son intelligence artificielle testée au combat, Adobe Sensei, afin que vous puissiez stimuler l’engagement et la conversion en toute confiance. Cette fonctionnalité supprime le travail manuel nécessaire pour adresser des recommandations de produits appropriées à chaque acheteur.

Pour plus d’informations, consultez le [[!DNL Product Recommendations] Guide de l’utilisateur](https://experienceleague.adobe.com/docs/commerce/product-recommendations/guide-overview.html?lang=en).

### [!DNL Catalog Service]

Le [!DNL Catalog Service] vous permet d’offrir aux clients une expérience de produit optimisée tout en améliorant les performances, l’évolutivité et les conversions. Pour plus d’informations, consultez le [[!DNL Catalog Service] Guide de l’utilisateur](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html).

### [!DNL Payment Services]

[!DNL Payment services] pour Adobe Commerce et Magento Open Source est une solution de paiement entièrement intégrée qui simplifie le processus de gestion des paiements et permet à vos clients de payer leur compte. Réconciliez en toute sécurité toutes les données de paiement et de transaction au sein de l’administration Adobe Commerce, ce qui vous permet de gérer les commandes et les paiements au même endroit tout en effectuant un passage en caisse transparent. Pour plus d’informations, consultez le [[!DNL Payment Services] Guide de l’utilisateur](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html).

### [!DNL Store Fulfillment]

Store Fulfillment for Adobe Commerce and Magento Open Source offre une expérience client BOPIS (achat en ligne, retrait en magasin) supérieure et optimise la productivité des employés en fournissant un workflow d’exécution complet activé par le biais d’un appareil mobile. Pour plus d’informations, consultez le [[!DNL Store Fulfillment] Guide de l’utilisateur](https://experienceleague.adobe.com/docs/commerce/store-fulfillment/guide-overview.html).

### [!DNL Amazon Sales Channel]

Le [!DNL Amazon Sales Channel] pour Adobe Commerce vous permet d’intégrer votre base de données de listes centrale des vendeurs Amazon à votre catalogue de produits [!DNL Commerce] et de gérer vos listes et ventes Amazon dans l’administration Commerce. Pour plus d’informations, consultez le [[!DNL Amazon Sales] Guide de l’utilisateur](https://experienceleague.adobe.com/docs/commerce-channels/amazon/guide-overview.html).

### [!DNL Channel Manager]

[!DNL Channel Manager] vous permet d’augmenter les ventes, d’atteindre de nouveaux clients, de rationaliser les opérations et de gagner du temps en intégrant un catalogue de produits Adobe Commerce ou Magento Open Source à Walmart Marketplace. Après avoir installé et configuré l&#39;extension, votre personnel peut gérer les listes, les stocks, les commandes, les retours et les remboursements de Walmart Marketplace de manière transparente à partir du [!DNL Commerce Admin]. Pour plus d’informations, consultez le [[!DNL Channel Manager] Guide de l’utilisateur](https://experienceleague.adobe.com/docs/commerce-channels/channel-manager/guide-overview.html).
