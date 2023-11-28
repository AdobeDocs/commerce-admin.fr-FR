---
title: '[!DNL Adobe Commerce Marketplace]'
description: En savoir plus sur les [!DNL Commerce Marketplace], qui offre aux commerçants une sélection organisée de solutions, et fournit aux développeurs qualifiés les outils, la plateforme et l’emplacement idéal pour créer une entreprise florissante.
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: 1a5a00493e9994343c7decc763f2decdd11192c7
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 0%

---

# Adobe Commerce Marketplace

[Adobe Commerce Marketplace][1] est la boutique d’applications qui propose aux commerçants une sélection de solutions organisées et qui fournit aux développeurs qualifiés les outils, la plateforme et l’emplacement de choix pour créer une entreprise florissante. [!DNL Commerce Marketplace] propose une sélection d’extensions disponibles gratuitement, et d’autres qui sont à vendre. Les achats peuvent être payés par carte de crédit ou [PayPal][2].

Toutes les extensions disponibles sur [!DNL Commerce Marketplace] ont fait l&#39;objet d&#39;un examen approfondi. La variable [Programme de qualité des extensions][3] Combinaisons (EQP) [!DNL Commerce] l’expertise, les directives de développement et les outils de vérification pour s’assurer que toutes les extensions sur Commerce Marketplace respectent les normes de codage et les bonnes pratiques. Le processus de révision comprend une vérification automatisée et une révision manuelle de l’assurance qualité. Au cours de ce processus, la structure et le code de chaque extension sont examinés et testés pour détecter des signes d&#39;infection virale ou malveillante, ainsi que toute indication de plagiat. L’examen comprend un examen technique approfondi et un contrôle d’intégrité effectué par une [!DNL Commerce] ingénieur, axé sur la documentation, la structure de codage, les performances, l’évolutivité, la sécurité et la compatibilité avec [!DNL Commerce] core.

Bien que vous puissiez acheter des extensions provenant d’autres sources, seules les extensions disponibles sur [!DNL Commerce Marketplace] sont vérifiés par le biais d’un examen technique et marketing approfondi dans le cadre du programme de qualité de l’extension.

## Ressources de l’application

Les développeurs utilisent traditionnellement PHP pour créer des extensions en cours de processus afin d’ajouter des fonctionnalités, des services et des intégrations à Adobe Commerce. En créant des applications avec une extensibilité hors processus, par opposition aux extensions, vous pouvez éviter des problèmes de compatibilité.

Les ressources suivantes constituent un point de départ pour que les nouveaux utilisateurs se familiarisent avec les applications :

### Ressources commerciales :

- [Configuration des événements d’E/S pour Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/)
- [Configuration des événements pour Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [Configuration du SDK de l’interface utilisateur d’administration](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [Conversion d’une extension en application](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### Ressources du générateur d’applications :

- [Présentation de Commerce App Builder](https://developer.adobe.com/commerce/extensibility/app-development/)
- [Configuration du maillage d’API pour Adobe Developer App Builder](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [Déploiement d’applications App Builder](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [CI/CD pour les applications App Builder](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- Prise en main d’App Builder/Developer Console
   - [Prise en main d’App Builder](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [Présentation des projets et des espaces de travail](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace] informations

Avant d’installer une extension achetée à partir de [!DNL Commerce Marketplace], connectez-vous à [!DNL Commerce] et vérifiez que vous disposez d’une clé d’accès active. Vous pouvez vous connecter à votre [!DNL Commerce] compte à partir de l’en-tête de [[!DNL Marketplace]][1] ou [Magento.com][6].

Votre clé d’accès est un ensemble de clés publiques et privées utilisées pour synchroniser votre [!DNL Commerce] avec votre [!DNL Commerce] et vérifiez vos informations d’identification. Une fois votre compte synchronisé, vous devez saisir votre clé privée chaque fois que vous installez une extension ou un module à partir de Commerce Marketplace ou que vous mettez à niveau votre [!DNL Commerce] installation.

Vous pouvez créer plusieurs clés d’accès à des fins différentes et les activer ou les désactiver selon vos besoins. Cependant, vous devez utiliser la même clé d’accès que celle utilisée pour installer la variable [!DNL Commerce] logiciel. Par exemple, vous ne pouvez pas utiliser une clé d’accès Magento Open Source pour mettre à jour ou mettre à niveau Adobe Commerce, ou inversement. Vous ne pouvez pas non plus utiliser de clé d’accès appartenant à un autre utilisateur ou provenant d’un [compte partagé](commerce-account-share.md).

### Création d’une clé d’accès

1. Se connecter à [!DNL Commerce] compte .

1. Sur le _[!UICONTROL My Account]_, choisissez la méthode **[!UICONTROL Marketplace]**.

1. Dans le coin supérieur droit en regard de votre nom, cliquez sur la flèche vers le bas et choisissez **[!UICONTROL My Profile]**.

   ![Votre [!DNL Marketplace] profile](./assets/marketplace-profile.png){width="600"}

1. Sur le _[!UICONTROL Marketplace]_sous_[!UICONTROL My Products]_, cliquez sur **[!UICONTROL Access Keys]**, puis effectuez l’une des opérations suivantes :

   - Vérifiez si vous disposez déjà d’un ensemble de clés d’accès pour vos achats Marketplace. Vous pouvez créer plusieurs jeux de clés d’accès à des fins différentes.

   ![Accéder aux clés](./assets/access-keys.png){width="600"}

   - Cliquez sur **[!UICONTROL Create a New Access Key]**. Saisissez le nom de la nouvelle paire de clés, puis cliquez sur **[!UICONTROL OK]**. Les caractères valides sont les caractères majuscules et minuscules et les tirets au lieu des espaces.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL OK]**.

   La nouvelle clé d’accès est activée et apparaît dans la liste.

   Remarquez que la variable _Copier_ après chaque clé publique et privée. À l’étape suivante, vous allez copier et coller ces valeurs pour synchroniser votre magasin avec Commerce Marketplace.

## Processus d’installation

>[!IMPORTANT]
>
>À compter d’Adobe Commerce et de Magento Open Source 2.4.0, l’assistant de configuration web est supprimé. Vous devez utiliser la ligne de commande pour [install](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) ou [upgrade](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html) votre instance. Cette exigence inclut également [modules](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) et [extensions](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

Le processus d’installation de [!DNL Marketplace] les achats sont différents pour _on-premise_ installations de Commerce plutôt que pour les installations hébergées sur [Architecture d’Adobe Cloud][4].

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## Assistance

Si vous avez besoin d’aide pour l’installation ou l’utilisation d’une extension, consultez d’abord la documentation qui accompagne l’extension. Si vous ne trouvez pas la réponse à votre question, utilisez les coordonnées figurant dans la liste des extensions pour contacter directement le développeur.

Si ce que vous achetez le Commerce Marketplace ne répond pas à vos besoins, vous pouvez demander un remboursement dans les 25 jours à compter de la date d’achat. Adobe examine toutes les demandes de remboursement et, si elle est approuvée, émet le remboursement approprié.

Pour les problèmes de prise en charge liés au Commerce Marketplace, voir [[!DNL Marketplace] Centre d’aide][5].

[1]: https://marketplace.magento.com/
[2]: https://www.paypal.com/us/home
[3]: https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/
[4]: https://www.adobe.com/commerce/magento/enterprise.html
[5]: https://marketplacesupport.magento.com/hc/en-us
[6]: https://business.adobe.com/products/magento/magento-commerce.html
