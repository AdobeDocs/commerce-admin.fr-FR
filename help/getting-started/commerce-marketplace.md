---
title: '[!DNL Adobe Commerce Marketplace]'
description: Découvrez le  [!DNL Commerce Marketplace], qui offre aux commerçants une sélection organisée de solutions et fournit aux développeurs qualifiés les outils, la plateforme et l’emplacement de choix pour créer une entreprise florissante.
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: 20e1439810891b0d19cda62cc2646701ec5a778c
workflow-type: tm+mt
source-wordcount: '1264'
ht-degree: 0%

---

# Adobe Commerce Marketplace

[Adobe Commerce Marketplace][1] est une boutique d’applications qui propose aux marchands une sélection de solutions organisées et qui fournit aux développeurs qualifiés les outils, la plateforme et l’emplacement idéal pour créer une entreprise florissante. [!DNL Commerce Marketplace] offre une sélection d’extensions disponibles gratuitement, et d’autres qui sont à vendre. Les achats peuvent être payés par carte de crédit ou par [PayPal][2].

Toutes les extensions disponibles sur [!DNL Commerce Marketplace] ont fait l’objet d’une révision approfondie. Le [Programme de qualité de l’extension][3] (EQP) combine [!DNL Commerce] expertise, directives de développement et outils de vérification pour s’assurer que toutes les extensions sur Commerce Marketplace respectent les normes de codage et les bonnes pratiques. Le processus de révision comprend une vérification automatisée et une révision manuelle de l’assurance qualité. Au cours de ce processus, la structure et le code de chaque extension sont examinés et testés pour détecter des signes d&#39;infection virale ou malveillante, ainsi que toute indication de plagiat. La révision comprend un examen technique approfondi et un contrôle d’intégrité effectué par un ingénieur [!DNL Commerce], avec un accent sur la documentation, la structure de codage, les performances, l’évolutivité, la sécurité et la compatibilité avec le noyau [!DNL Commerce].

Bien que vous puissiez acheter des extensions à partir d’autres sources, seules les extensions disponibles sur [!DNL Commerce Marketplace] sont vérifiées par un examen technique et marketing approfondi dans le cadre du Programme de qualité des extensions.

## Ressources de l’application

Les développeurs utilisent traditionnellement PHP pour créer des extensions en cours de processus afin d’ajouter des fonctionnalités, des services et des intégrations à Adobe Commerce. En créant des applications avec une extensibilité hors processus, par opposition aux extensions, vous pouvez éviter des problèmes de compatibilité.

Les ressources suivantes constituent un point de départ pour que les nouveaux utilisateurs se familiarisent avec les applications :

### Ressources Commerce

- [Configuration des événements d’E/S pour Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/)
- [Configuration des événements pour Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [ Configuration du SDK de l’interface utilisateur d’administration ](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [Conversion d’une extension en application](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### Ressources App Builder

- [ {Commerce App Builder Overview](https://developer.adobe.com/commerce/extensibility/app-development/)
- [Configuration d’un comptage d’API pour Adobe Developer App Builder](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [Déploiement d’applications App Builder](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [CI/CD pour les applications App Builder](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- Prise en main d’App Builder/Developer Console
   - [Prise en main d’App Builder](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [Présentation des projets et des espaces de travail](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace] credentials

Avant de pouvoir installer une extension achetée à partir de [!DNL Commerce Marketplace], connectez-vous à votre compte [!DNL Commerce] et vérifiez que vous disposez d’une clé d’accès active. Vous pouvez vous connecter à votre compte [!DNL Commerce] à partir de l’en-tête de [[!DNL Marketplace]][1] ou [Magento.com][6].

Votre clé d’accès est un ensemble de clés publiques et privées qui est utilisé pour synchroniser votre installation [!DNL Commerce] avec votre compte [!DNL Commerce] et vérifier vos informations d’identification. Une fois votre compte synchronisé, vous devez saisir votre clé privée chaque fois que vous installez une extension ou un module à partir de Commerce Marketplace ou mettez à niveau votre installation [!DNL Commerce].

Vous pouvez créer plusieurs clés d’accès à des fins différentes et les activer ou les désactiver selon vos besoins. Cependant, vous devez utiliser la même clé d’accès que celle utilisée pour installer le logiciel [!DNL Commerce]. Par exemple, vous ne pouvez pas utiliser une clé d’accès Magento Open Source pour mettre à jour ou mettre à niveau Adobe Commerce, ou inversement. Vous ne pouvez pas non plus utiliser de clé d’accès appartenant à un autre utilisateur ou provenant d’un [compte partagé](commerce-account-share.md).

### Création d’une clé d’accès

1. Connectez-vous à votre compte [!DNL Commerce].

1. Sur la page _[!UICONTROL My Account]_, sélectionnez l’onglet **[!UICONTROL Marketplace]**.

1. Dans le coin supérieur droit en regard de votre nom, cliquez sur la flèche vers le bas et choisissez **[!UICONTROL My Profile]**.

   ![Votre [!DNL Marketplace] profil](./assets/marketplace-profile.png){width="600"}

1. Sur l’onglet _[!UICONTROL Marketplace]_sous_[!UICONTROL My Products]_, cliquez sur **[!UICONTROL Access Keys]**, puis effectuez l’une des opérations suivantes :

   - Vérifiez si vous disposez déjà d’un ensemble de clés d’accès pour vos achats Marketplace. Vous pouvez créer plusieurs jeux de clés d’accès à des fins différentes.

   ![Accéder aux clés](./assets/access-keys.png){width="600"}

   - Cliquez sur **[!UICONTROL Create a New Access Key]**. Saisissez le nom de la nouvelle paire de clés et cliquez sur **[!UICONTROL OK]**. Les caractères valides sont les caractères majuscules et minuscules et les tirets au lieu des espaces.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL OK]**.

   La nouvelle clé d’accès est activée et apparaît dans la liste.

   Notez le lien _Copier_ après chaque clé publique et privée. À l’étape suivante, vous allez copier et coller ces valeurs pour synchroniser votre magasin avec Commerce Marketplace.

## Processus d’installation

>[!IMPORTANT]
>
>À compter d’Adobe Commerce et de Magento Open Source 2.4.0, l’assistant de configuration web est supprimé. Vous devez utiliser la ligne de commande pour [installer](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) ou [mettre à niveau](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html) votre instance. Cette exigence inclut également [modules](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) et [extensions](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

Le processus d’installation pour les [!DNL Marketplace] achats est différent pour les installations _On-premise_ de Commerce que pour les installations hébergées sur [l’architecture Adobe Cloud][4].

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## Assistance

Si vous avez besoin d’aide pour l’installation ou l’utilisation d’une extension, consultez d’abord la documentation qui accompagne l’extension. Si vous ne trouvez pas la réponse à votre question, utilisez les coordonnées figurant dans la liste des extensions pour contacter directement le développeur. Si ce que vous achetez sur Marketplace ne répond pas à vos besoins, vous pouvez [demander un remboursement](#refund-requests) dans les 25 jours à compter de la date d’achat. Adobe passe en revue toutes les demandes de remboursement et, si elles sont approuvées, émet le remboursement approprié. Pour tout problème lié au Commerce Marketplace, contactez le [support](mailto:commercemarketplacesupport@adobe.com).

### Problèmes d’extraction

Les champs d’adresse de votre profil de compte doivent être renseignés à des fins de vérification dans le système d’achat Marketplace.

1. Ajoutez les champs d’adresse dans votre profil de compte Marketplace.
1. Enregistrez le profil mis à jour.
1. Poursuivez votre passage en caisse.

### Problèmes de connexion

Les problèmes de connexion sont généralement liés à une incohérence entre votre MAGEID et votre adresse électronique dans la base de données de compte. Contactez l’assistance de Marketplace pour obtenir de l’aide.

>[!INFO]
>
>Les achats d’applications et d’extensions ne peuvent pas être [transférés](#purchase-transfers) vers un nouveau compte.

### Questions open source

L’équipe d’assistance de Marketplace résout uniquement les problèmes liés aux sites [commercemarketplace.adobe.com/](https://commercemarketplace.adobe.com/) et [commercedeveloper.adobe.com/](https://commercedeveloper.adobe.com/) . Pour toute question sur le Magento Open Source, contactez le [Forum de la communauté](https://community.magento.com/) ou [contactez un partenaire](https://business.adobe.com/products/magento/partners.html) qui peut vous aider à contacter le Magento Open Source.

### Demandes de remboursement

Pour demander un remboursement pour un achat Marketplace, connectez-vous à votre compte et procédez comme suit :

1. Cliquez sur [!UICONTROL **Mon profil**] > [!UICONTROL **Historique des achats**].
1. Recherchez l’achat et cliquez sur [!UICONTROL **Demander un remboursement**].
1. Remplissez le formulaire de bon de remboursement.

L’assistance marketing demandera des informations une fois la demande de remboursement générée. L&#39;option de remboursement est disponible pendant 25 jours après la date d&#39;achat. Voir le [contrat client Marketplace](https://www.adobe.com/legal/terms/enterprise-licensing/magento-legacy-terms.html).

### factures de commande

Vous pouvez télécharger des factures de commande à partir de l’[!UICONTROL **historique des achats**] dans votre compte Marketplace. La facture ne fournit pas la TVA ou l&#39;adresse du vendeur, car il ne s&#39;agit pas pour l&#39;instant d&#39;une obligation Marketplace.

Pour télécharger une facture de commande pour un achat Marketplace, connectez-vous à votre compte Marketplace et procédez comme suit :

1. Cliquez sur [!UICONTROL **Mon profil**] > [!UICONTROL **Historique des achats**].
1. Recherchez l’achat.
1. Cliquez sur l’icône de l’imprimante dans le coin supérieur droit de la commande.

### Transferts d’achat

L’équipe d’assistance Marketplace n’a pas la possibilité de transférer des achats vers un autre compte. Vous devez acheter toutes les applications et extensions sous le compte Commerce principal pour éviter des problèmes d’installation et de déploiement. Adobe Commerce a droit à un identifiant unique. Comme le compositeur est utilisé pour l’installation, un seul ensemble de [clés d’accès](#create-an-access-key) liées au compte principal peut être utilisé. La seule solution disponible est de [demander un remboursement](#refund-requests) auprès du compte d’achat Marketplace (si autorisé par la politique de remboursement d’Adobe Commerce).

Vous pouvez [partager](commerce-account-share.md) une instance Commerce par le biais du compte principal. L’accès partagé accorde des autorisations spéciales à un compte subordonné à partir d’un compte principal. Le point d’accès partagé est généré à partir du compte principal. Le compte principal peut être le compte Commerce autorisé, le compte marchand principal ou un compte partagé au sein d’une organisation.

Ces autorisations spéciales accordent le même niveau d’accès à Adobe Commerce que l’instance principale, mais elles ne sont pas transférées vers Adobe Commerce Marketplace ni vers Developer Portal. Cela signifie que l’achat d’une extension à partir d’un compte subordonné dans Marketplace ne peut pas être partagé avec le compte principal. L&#39;accès partagé est une rue à sens unique (compte principal à subordonné). Cela ne fonctionne pas lorsqu’un compte subordonné tente de partager à nouveau le compte principal.

[1]: https://marketplace.magento.com/
[2]: https://www.paypal.com/us/home
[3]: https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/
[4]: https://www.adobe.com/commerce/magento/enterprise.html
[6]: https://business.adobe.com/products/magento/magento-commerce.html
