---
title: Extensions à partir d’Adobe
description: Consultez les informations sur les extensions d’Adobe Commerce et de Magento Open Source publiées par Adobe.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
badgePaas: label="PaaS uniquement" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="S’applique uniquement aux projets Adobe Commerce on Cloud (infrastructure PaaS gérée par Adobe) et aux projets On-premise."
source-git-commit: 36c91007d21834b49351c8b53c617e442deebaa0
workflow-type: tm+mt
source-wordcount: '1356'
ht-degree: 0%

---

# Extensions à partir d’Adobe

Cette rubrique fournit des informations sur les extensions PHP pour Adobe Commerce et Magento Open Source publiées par Adobe.

Les extensions ajoutent des fonctionnalités, des services et des intégrations à Admin et au storefront. Certaines de ces extensions sont développées par le biais de contributions de la communauté Magento Open Source. Certaines extensions sont installées par défaut et d’autres nécessitent une installation distincte.

+++En savoir plus sur l’extension d’Adobe Commerce

Adobe propose deux approches principales pour étendre ou personnaliser vos projets Adobe Commerce :

- Extensibilité en cours de traitement : utilise du code personnalisé et des extensions qui s’exécutent dans le processus d’application Adobe Commerce comme les extensions PHP. Cette approche traditionnelle permet une intégration approfondie, mais nécessite une gestion attentive lors des mises à niveau.

- Extensibilité hors processus : utilise du code personnalisé et des applications qui fonctionnent indépendamment du logiciel principal. Cette approche moderne permet de réduire le coût total de possession :

   - Simplification des mises à niveau puisque les extensions sont découplées du cœur
   - Permettre aux développeurs de mieux contrôler le calendrier et les méthodes d’implémentation
   - Activation de la mise à l’échelle indépendante et de la maintenance des composants d’extension

Adobe Commerce propose des stratégies et des outils pour prendre en charge ces deux types d’extensibilité. Pour en savoir plus, voir [Extensibilité d’Adobe Commerce](https://developer.adobe.com/commerce/extensibility/).

+++

## Extensions d’Adobe installées par défaut

Les extensions Adobe ci-dessous sont incluses dans Adobe Commerce et installées automatiquement avec l’application Adobe Commerce. Certaines extensions nécessitent une configuration ou une activation supplémentaires dans l’administration, comme indiqué dans la description de l’extension.

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

## Extensions Adobe nécessitant une installation

Adobe propose des extensions supplémentaires qui doivent être installées séparément à l’aide du compositeur. Ces extensions sont disponibles par le biais de différents canaux :

- Accès au référentiel (repo.magento.com)

  Les extensions suivantes nécessitent la configuration du compte et des informations d’identification à installer. Contactez votre représentant de compte Adobe pour obtenir de l’aide.

   - [Adobe Commerce B2B](#adobe-commerce-b2b)
   - [Intégration d’AEM Assets pour Commerce](#assets-integration-for-commerce)

- Adobe Commerce Marketplace

  Les extensions d’Adobe ci-dessous sont accessibles au public à l’adresse [marketplace.magento.com](https://marketplace.magento.com). Ces extensions sont disponibles sans frais supplémentaires.

   - [Recherche en direct](#live-search)
   - [Recommandations de produit](#product-recommendations)
   - [Service de catalogue](#catalog-service)
   - [Services de paiement](#payment-services)

### [!DNL Adobe Commerce B2B]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce uniquement, nécessite une licence distincte.

[!DNL Adobe Commerce B2B] est une extension intégrée qui transforme les magasins Commerce standard en plateformes complètes business-to-business. Il permet aux entreprises de gérer des structures organisationnelles complexes avec plusieurs acheteurs, des rôles personnalisés et des autorisations d’achat sous des comptes d’entreprise unifiés. Les principales fonctionnalités comprennent les catalogues et les prix spécifiques à la société, les devis négociables, la gestion des commandes, les listes de demandes d&#39;approvisionnement et les fonctionnalités de commande rapide. La solution prend en charge les modèles B2B et B2C sur une seule instance, ce qui la rend flexible pour divers besoins commerciaux. L’extension nécessite une licence distincte et s’intègre de manière transparente aux fonctionnalités principales d’Adobe Commerce pour fournir une solution d’e-commerce B2B complète.

Pour la mise en service, contactez votre représentant de compte Adobe. Pour plus d’informations sur l’implémentation et les étapes de configuration, consultez le [[!DNL B2B for Adobe Commerce] Guide de l’utilisateur](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

### [!DNL AEM Assets Integration for Commerce]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce uniquement, nécessite également des licences pour Adobe Experience Manager (AEM) Assets et AEM Dynamic Media.

[!DNL AEM Assets Integration for Commerce] connecte Adobe Commerce au système de gestion des ressources numériques (DAM) de Adobe Experience Manager afin de fournir un contrôle centralisé sur toutes les ressources numériques. Cette intégration permet une synchronisation automatisée des ressources, des mises à jour en temps réel et une réutilisation efficace du contenu sur les storefronts de commerce. En associant les puissantes fonctionnalités de gestion des ressources d’AEM à Commerce, les entreprises bénéficient de workflows rationalisés, d’expériences de marque cohérentes et d’une diffusion multimédia optimisée grâce à une infrastructure cloud.

Pour la mise en service, contactez votre représentant de compte Adobe. Pour plus d’informations sur l’implémentation et les étapes de configuration, consultez le [[!DNL Assets Integration] Guide de l’utilisateur](../content-design/aem-assets-integration.md).

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce uniquement

Live Search est une fonctionnalité exclusive à Adobe Commerce qui fournit une solution de recherche optimisée par l’IA avec une fonctionnalité de « recherche en temps réel ». Il offre des résultats rapides et pertinents avec des miniatures de produit lorsque les acheteurs saisissent des informations, ainsi qu’un facettage intelligent qui ajuste automatiquement les filtres en fonction du comportement d’achat. La solution comprend des fonctionnalités de marchandisage pour l’enrichissement et l’enterrement des produits, la gestion des synonymes et l’analyse de recherche. Inclus avec Adobe Commerce sans frais supplémentaires, [!DNL Live Search] remplace la fonctionnalité de recherche par défaut par une expérience de recherche plus sophistiquée basée sur SaaS. Pour commencer, une configuration minimale est nécessaire.

Pour plus d’informations sur l’implémentation et connaître les exigences techniques, consultez le [Guide d’utilisation de Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html).

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce uniquement

[!DNL Product Recommendations] est une fonctionnalité exclusive à Adobe Commerce, optimisée par la technologie d’IA d’Adobe, qui fournit des suggestions de produits personnalisées dans l’ensemble du parcours d’achat des clients. La solution analyse en temps réel le comportement des acheteurs et les relations entre les produits afin de générer automatiquement des recommandations pertinentes, sans nécessiter de règles de marchandisage manuelles. Cette approche axée sur l’IA permet d’augmenter les taux de conversion et le potentiel de chiffre d’affaires tout en créant des expériences de découverte de produits plus attrayantes pour les acheteurs.

Pour obtenir des informations détaillées sur l’implémentation et connaître les bonnes pratiques, consultez le [[!DNL Product Recommendations] Guide de l’utilisateur](https://experienceleague.adobe.com/docs/commerce/product-recommendations/overview.html).

### [!DNL Catalog Service]

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"} Installations Adobe Commerce et Magento Open Source

[!DNL Catalog Service] est une solution hautes performances pour Adobe Commerce et Magento Open Source qui offre un accès optimisé aux données de catalogue par le biais de points d’entrée GraphQL. Il conserve une base de données synchronisée distincte pour les détails du produit et les informations connexes, en contournant la communication directe de l’application pour offrir des temps de chargement de page plus rapides. Ce service est particulièrement utile pour les pages de détails de produits, les listes de catégories et les pages de résultats de recherche, ce qui le rend idéal pour les implémentations commerciales traditionnelles et découplées.

Pour obtenir des instructions de configuration et des détails techniques, consultez le [[!DNL Catalog Service] Guide de l’utilisateur](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html).

>[!NOTE]
>
>Les services de catalogue sont installés automatiquement lorsque Live Search ou les recommandations de produits sont activés. Aucune installation manuelle n’est requise.

### [!DNL Payment Services]

[!BADGE Pris en charge]{type=Informative tooltip="Pris en charge"} Installations Adobe Commerce et Magento Open Source

[!DNL Payment Services] est une solution de paiement clé en main pour les magasins Adobe Commerce et Magento Open Source qui offre des fonctionnalités complètes de traitement des paiements. Le service intègre une fonctionnalité de passerelle de paiement sécurisée avec une protection contre la fraude intégrée, tout en offrant plusieurs options de paiement, notamment les cartes de crédit/débit, PayPal, Venmo (États-Unis) et les plans PayLater. Il offre des rapports de transaction et une gestion des commandes unifiés via l&#39;interface d&#39;administration de Commerce, ce qui permet aux commerçants de suivre facilement les paiements, de gérer les flux de trésorerie et de rapprocher les données financières en un seul endroit.

Pour obtenir des instructions détaillées sur les étapes de configuration et les options de paiement, consultez le [[!DNL Payment Services]  Guide de l’utilisateur ](https://experienceleague.adobe.com/en/docs/commerce/payment-services/overview).
