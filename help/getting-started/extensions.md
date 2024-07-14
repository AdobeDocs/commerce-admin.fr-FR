---
title: Extensions d’Adobe
description: Consultez les informations sur les extensions d’Adobe Commerce et de Magento Open Source publiées par Adobe.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
source-git-commit: 6414a7aea7dcbe0f2379ed74455518220a1fbd64
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 0%

---

# Extensions d’Adobe

Cette rubrique fournit des informations sur les extensions Adobe Commerce et Magento Open Source publiées par Adobe. Les extensions ajoutent des fonctionnalités, des services et des intégrations à l’administrateur et au storefront. Certaines de ces extensions sont développées par le biais de contributions de la communauté Magento Open Source. Certaines extensions nécessitent une installation distincte, tandis que d’autres sont installées par défaut.

## Extensions installées

Certaines extensions sont automatiquement installées avec Adobe Commerce ou Magento Open Source.

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) offre une gestion améliorée des stocks et des envois sur un ou plusieurs emplacements et canaux de vente avec des algorithmes simultanés de protection des passages en caisse et de correspondance des envois. Effectuez le suivi des quantités de stock, fournissez des quantités de stock vendables précises aux clients et expédiez-les selon des recommandations ou des sélections manuelles afin de contrôler l’ensemble de votre inventaire. Configurez les paramètres de gestion globalement, par source et par produit.

>[!NOTE]
>
>Cette extension a été développée dans le cadre du projet [[!DNL Inventory Management]](https://github.com/magento/inventory) (anciennement MSI) par le biais du programme d’ingénierie communautaire.

[!DNL Inventory Management] installe toutes les fonctionnalités activées par défaut. Aucune autre procédure n’est nécessaire pour activer ces fonctionnalités d’inventaire. Pour plus d’informations sur les fonctionnalités [!DNL Inventory Management], consultez le [[!DNL Inventory Management] Guide de l’utilisateur](../inventory-management/guide-overview.md).

### Braintree

PayPal et Gene Commerce ont développé ensemble l’extension Braintree officielle pour les magasins Commerce 2.4.x. Grâce à une meilleure expérience de passage en caisse conçue pour générer des conversions, les mises à jour incluent des options PayLater qui affichent automatiquement les messages et boutons PayLater pertinents aux consommateurs pendant les achats et pendant le passage en caisse.

Cette extension est installée par défaut, mais requiert un [compte de Braintree](https://www.braintreepayments.com/) et une configuration dans l’administrateur pour être activée pour votre boutique. Pour déterminer les frais qui s’appliquent lors de l’utilisation de Braintree pour traiter vos transactions, vérifiez le [prix Braintree](https://www.braintreepayments.com/braintree-pricing).

Pour plus d’informations sur la configuration du Braintree dans l’administrateur, consultez la rubrique [Braintree](../stores-purchase/braintree.md) du _Guide d’expérience des ventes et des achats_.

### Google reCAPTCHA

Google reCAPTCHA offre un niveau de sécurité plus élevé pour le storefront et l’interface utilisateur d’administration que celui disponible avec CAPTCHA standard et vous permet d’effectuer les opérations suivantes :

- Vérifiez quand les clients créent des comptes, récupèrent des mots de passe, se connectent à leurs comptes ou contactent votre société.
- Renforcez la sécurité lorsque les utilisateurs administrateurs se connectent.

Elle réduit les erreurs utilisateur potentielles lors de la saisie d’un code Captcha et encourage la conversion de panier sans ajouter d’obstacles lors du passage en caisse. [Activez et configurez reCAPTCHA](../systems/security-google-recaptcha.md) à l’aide de vérifications invisibles ou interactives afin d’améliorer l’accès sécurisé à l’ [!DNL Commerce] Admin et au storefront.

### Authentification à deux facteurs

L’administrateur [!DNL Commerce] permet d’accéder à toutes les données de votre boutique, de vos commandes et de vos clients. [L’authentification à deux facteurs](../systems/security-two-factor-authentication.md) (2FA ou TFA) améliore la sécurité en exigeant une authentification supplémentaire, au-delà du nom de connexion et du mot de passe standard, pour accéder à l’administrateur [!DNL Commerce] à partir de tous les appareils. L’extension prend en charge plusieurs authentificateurs, y compris l’authentificateur Google, l’auteur, [!DNL Duo] et les clés U2F. Cette authentification s’applique uniquement aux utilisateurs administrateurs. Elle n’est pas disponible pour les comptes clients storefront.

Ces fonctionnalités sont activées par défaut. Chaque utilisateur administrateur doit installer et configurer l’un des authentificateurs pris en charge.

>[!NOTE]
>
>Les magasins Adobe Commerce qui ont activé l’authentification Adobe Identity Management Services (IMS) pour l’administrateur ont désactivé Commerce 2FA natif. Les utilisateurs connectés à l’administrateur à l’aide de leurs informations d’identification d’Adobe n’ont pas besoin de se réauthentifier pour de nombreuses tâches d’administration. L’authentification est gérée par Adobe IMS lorsque l’utilisateur administrateur se connecte à sa session en cours. Voir [Présentation de l’intégration d’Adobe Identity Management Service (IMS)](./adobe-ims-integration-overview.md).

## Extensions à ajouter

[[!DNL Commerce Marketplace]](https://marketplace.magento.com/) est la ressource eCommerce globale pour les applications et services qui étendent les solutions [!DNL Commerce] avec de puissantes nouvelles fonctionnalités. Adobe publie plusieurs extensions par le biais de [!DNL Marketplace] qui peuvent être installées et configurées dans votre boutique Adobe Commerce ou Magento Open Source afin de fournir des intégrations et des fonctionnalités améliorées.

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce uniquement

L’extension [!DNL Live Search] connecte votre boutique au service Live Search, une plateforme de recherche gratuite d’Adobe Commerce qui permet aux vendeurs de fournir aux clients une expérience de recherche améliorée grâce à l’IA. Créé avec l’intelligence artificielle de l’Adobe, Adobe Sensei, Intelligent Faceting aide les marchands à faire plus avec moins en supprimant le travail manuel autour de la facette/filtrage.

Pour plus d’informations, consultez le [Guide de l’utilisateur de la recherche en direct](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html) .

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce uniquement

L’extension [!DNL Product Recommendations] connecte votre boutique au service Recommendations de produit, un puissant outil marketing que vous pouvez utiliser pour augmenter les conversions, les recettes et l’engagement. [!DNL Product Recommendations] a été créé par Adobe Commerce et est piloté par Adobe Sensei, une intelligence artificielle testée sur le champ de bataille, afin que vous puissiez stimuler l’engagement et la conversion en toute confiance. Cette fonctionnalité supprime le travail manuel requis pour adresser des recommandations de produits pertinentes à chaque acheteur.

Pour plus d’informations, consultez le [[!DNL Product Recommendations] Guide de l’utilisateur](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html?lang=en) .

### [!DNL Catalog Service]

[!DNL Catalog Service] vous permet de fournir aux clients une expérience de produit optimisée tout en améliorant les performances, l’évolutivité et l’augmentation des conversions. Pour plus d’informations, consultez le [[!DNL Catalog Service] Guide de l’utilisateur](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html) .

### [!DNL Payment Services]

[!DNL Payment services] pour Adobe Commerce et Magento Open Source est une solution de paiement entièrement intégrée qui simplifie le processus de gestion des paiements et donne à vos clients la possibilité de payer à leur guise. Réconciliez en toute sécurité toutes les données de paiement et de transaction au sein de l’administrateur Adobe Commerce, ce qui vous permet de gérer les commandes et les paiements à un seul endroit tout en effectuant un passage en caisse transparent. Pour plus d’informations, consultez le [[!DNL Payment Services] Guide de l’utilisateur](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html) .

### [!DNL Store Fulfillment]

L’exécution de magasin pour Adobe Commerce et Magento Open Source permet à un client d’acheter en ligne, de prendre en main son expérience client (BOPIS) et d’optimiser sa productivité en fournissant un workflow d’exécution complet activé sur un appareil mobile. Pour plus d’informations, consultez le [[!DNL Store Fulfillment] Guide de l’utilisateur](https://experienceleague.adobe.com/docs/commerce-merchant-services/store-fulfillment/guide-overview.html) .

### [!DNL Amazon Sales Channel]

[!DNL Amazon Sales Channel] pour Adobe Commerce vous permet d’intégrer votre base de données de liste Amazon Seller Central à votre catalogue de produits [!DNL Commerce] et de gérer vos listes et ventes Amazon dans l’administrateur Commerce. Pour plus d’informations, consultez le [[!DNL Amazon Sales] Guide de l’utilisateur](https://experienceleague.adobe.com/docs/commerce-channels/amazon/guide-overview.html) .

### [!DNL Channel Manager]

[!DNL Channel Manager] vous permet d’augmenter les ventes, d’atteindre de nouveaux clients, de rationaliser les opérations et de gagner du temps en intégrant un catalogue de produits Adobe Commerce ou Magento Open Source à Walmart Marketplace. Après avoir installé et configuré l’extension, votre personnel peut gérer en toute transparence les listes, les stocks, les commandes, les retours et les remboursements de Walmart Marketplace depuis le [!DNL Commerce Admin]. Pour plus d’informations, consultez le [[!DNL Channel Manager] Guide de l’utilisateur](https://experienceleague.adobe.com/docs/commerce-channels/channel-manager/guide-overview.html) .
