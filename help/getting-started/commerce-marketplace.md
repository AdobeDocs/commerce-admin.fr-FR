---
title: '[!DNL Adobe Commerce Marketplace]'
description: Découvrez le  [!DNL Commerce Marketplace], qui offre aux commerçants une sélection organisée de solutions et fournit aux développeurs qualifiés les outils, la plateforme et l’emplacement idéal pour créer une entreprise florissante.
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: 17ec998812d21ab5815546e0f015965c2d35c853
workflow-type: tm+mt
source-wordcount: '1281'
ht-degree: 0%

---

# Adobe Commerce Marketplace

[Adobe Commerce Marketplace][1] est la boutique d’applications qui offre aux commerçants une sélection organisée de solutions et fournit aux développeurs qualifiés les outils, la plateforme et l’emplacement idéal pour créer une entreprise florissante. [!DNL Commerce Marketplace] propose une sélection d’extensions disponibles gratuitement, ainsi que d’autres à vendre. Les achats peuvent être réglés par carte de crédit ou [PayPal][2].

Toutes les extensions disponibles sur [!DNL Commerce Marketplace] ont passé un examen approfondi. Le [Programme de qualité des extensions][3] (EQP) associe une expertise [!DNL Commerce], des directives de développement et des outils de vérification pour s’assurer que toutes les extensions sur Commerce Marketplace répondent aux normes de codage et aux bonnes pratiques. Le processus de révision comprend à la fois une vérification automatisée et une révision manuelle de l’assurance qualité. Au cours du processus, la structure et le code de chaque extension sont examinés et testés pour rechercher des preuves d&#39;infection par virus/malware, et toute indication de plagiat. L’examen comprend un examen technique approfondi et un contrôle de l’intégrité menés par un ingénieur en [!DNL Commerce], avec un accent particulier sur la documentation, la structure de codage, les performances, l’évolutivité, la sécurité et la compatibilité avec le cœur de [!DNL Commerce].

Bien que vous puissiez acheter des extensions auprès d’autres sources, seules les extensions disponibles sur [!DNL Commerce Marketplace] sont vérifiées au moyen d’un examen technique et marketing approfondi dans le cadre du programme de qualité des extensions.

## Ressources de l’application

Les développeurs ont traditionnellement utilisé PHP pour créer des extensions en cours de traitement afin d&#39;ajouter des fonctions, des services et des intégrations à Adobe Commerce. En créant des applications avec une extensibilité hors processus, par opposition aux extensions, vous pouvez éviter des problèmes de compatibilité.

Les ressources suivantes constituent un point de départ pour que les nouveaux utilisateurs se familiarisent avec les applications :

### Ressources Commerce

- [Configuration d’événements I/O pour Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/)
- [Configuration des événements pour Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [Configuration du SDK de l’interface utilisateur d’administration](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [Convertir une extension en application](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### Ressources App Builder

- [Présentation d’Commerce App Builder](https://developer.adobe.com/commerce/extensibility/app-development/)
- [Configuration du maillage API pour Adobe Developer App Builder](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [Déploiement des applications App Builder](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [CI/CD pour les applications App Builder](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- Prise en main d’App Builder/Developer Console
   - [Prise en main d’App Builder](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [Présentation des projets et des espaces de travail](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace] des informations d’identification

Avant de pouvoir installer une extension achetée auprès de [!DNL Commerce Marketplace], connectez-vous à votre compte [!DNL Commerce] et vérifiez que vous disposez d’une clé d’accès active. Vous pouvez vous connecter à votre compte [!DNL Commerce] à partir de l’en-tête de [[!DNL Marketplace]][1] ou [Magento.com][6].

Votre clé d’accès est un ensemble de clés publiques et privées utilisé pour synchroniser votre installation [!DNL Commerce] avec votre compte [!DNL Commerce] et vérifier vos informations d’identification. Une fois le compte synchronisé, vous devez saisir votre clé privée chaque fois que vous installez une extension ou un module à partir de Commerce Marketplace ou que vous mettez à niveau votre installation [!DNL Commerce].

Vous pouvez créer plusieurs clés d’accès à différentes fins et les activer ou les désactiver si nécessaire. Cependant, vous devez utiliser la même clé d’accès que celle utilisée pour installer le logiciel [!DNL Commerce]. Par exemple, vous ne pouvez pas utiliser une clé d’accès Magento Open Source pour mettre à jour ou mettre à niveau Adobe Commerce, ou inversement. Vous ne pouvez pas non plus utiliser une clé d’accès appartenant à un autre utilisateur ou provenant d’un [compte partagé](commerce-account-share.md).

### Création d’une clé d’accès

1. Connectez-vous à votre compte [!DNL Commerce].

1. Sur la page _[!UICONTROL My Account]_, choisissez l’onglet **[!UICONTROL Marketplace]**.

1. Dans le coin supérieur droit à côté de votre nom, cliquez sur la flèche vers le bas et choisissez **[!UICONTROL My Profile]**.

   ![Votre profil [!DNL Marketplace]](./assets/marketplace-profile.png){width="600"}

1. Dans l’onglet _[!UICONTROL Marketplace]_&#x200B;sous&#x200B;_[!UICONTROL My Products]_, cliquez sur **[!UICONTROL Access Keys]**, puis effectuez l’une des opérations suivantes :

   - Vérifiez si vous disposez déjà d’un jeu de clés d’accès pour vos achats sur Marketplace. Vous pouvez créer plusieurs jeux de clés d’accès à des fins différentes.

   ![Clés d’accès](./assets/access-keys.png){width="600"}

   - Cliquez sur **[!UICONTROL Create a New Access Key]**. Saisissez le nom de la nouvelle paire de clés, puis cliquez sur **[!UICONTROL OK]**. Les caractères valides comprennent des caractères majuscules et minuscules ainsi que des tirets au lieu d’espaces.

1. Cliquez ensuite sur **[!UICONTROL OK]**.

   Votre nouvelle clé d’accès est activée et apparaît dans la liste.

   Remarquez le lien _Copy_ après chaque clé publique et privée. À l’étape suivante, vous allez copier et coller ces valeurs pour synchroniser votre boutique avec Commerce Marketplace.

## Processus d’installation

>[!IMPORTANT]
>
>À partir d’Adobe Commerce et de Magento Open Source 2.4.0, l’assistant de configuration web est supprimé et vous devez utiliser la ligne de commande pour [installer](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html?lang=fr) ou [mettre à niveau](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html?lang=fr) votre instance. Cette exigence inclut également les [modules](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html?lang=fr) et [extensions](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html?lang=fr).

Le processus d’installation pour [!DNL Marketplace] achats est différent pour les installations _on-premise_ de Commerce et pour les installations hébergées sur [l’architecture cloud Adobe][4].

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## Support technique

Si vous avez besoin d’aide pour installer ou utiliser une extension, commencez par consulter la documentation qui accompagne l’extension. Si vous ne trouvez pas la réponse à votre question, utilisez les coordonnées figurant dans la liste des extensions pour contacter directement le développeur. Si ce que vous achetez sur Marketplace ne répond pas à vos besoins, vous pouvez [demander un remboursement](#refund-requests) dans les 25 jours suivant la date d&#39;achat. Adobe examine toutes les demandes de remboursement et (si elles sont approuvées) émet le remboursement approprié. Pour les problèmes liés à Commerce Marketplace :

Méthode 1 : envoyez une demande d’assistance à partir du formulaire [Adobe Commerce Marketplace - Nous contacter](https://commercemarketplace.adobe.com/contact-us/).

Méthode 2 : [prise en charge des e-mails](mailto:commercemarketplacesupport@adobe.com).

### Problèmes de passage en caisse

Les champs d’adresse de votre profil de compte doivent être renseignés à des fins de vérification dans le système d’achat Marketplace.

1. Ajoutez les champs d’adresse à votre profil de compte Marketplace.
1. Enregistrez le profil mis à jour.
1. Poursuivez votre passage en caisse.

### Problèmes de connexion

Les problèmes de connexion sont généralement liés à une incohérence entre votre MAGEID et votre adresse e-mail dans la base de données du compte. Contactez l’assistance marketing pour obtenir de l’aide.

>[!INFO]
>
>Les achats d’application et d’extension ne peuvent pas être [transférés](#purchase-transfers) vers un nouveau compte.

### Questions open source

L’équipe d’assistance du Marketplace résout les problèmes liés aux sites [commercemarketplace.adobe.com/](https://commercemarketplace.adobe.com/) et [commercedeveloper.adobe.com/](https://commercedeveloper.adobe.com/) uniquement. Veuillez adresser vos questions sur Magento Open Source au [Forum de la communauté](https://community.magento.com/) ou [contacter un partenaire](https://business.adobe.com/fr/products/magento/partners.html) qui peut vous aider à utiliser Magento Open Source.

### Demandes de remboursement

Pour demander un remboursement pour un achat sur Marketplace, connectez-vous à votre compte et procédez comme suit :

1. Cliquez sur [!UICONTROL **Mon profil**] > [!UICONTROL **Historique des achats**].
1. Recherchez l’achat et cliquez sur [!UICONTROL **Demander un remboursement**].
1. Remplissez le formulaire de demande de remboursement.

L’assistance Marketplace demandera des informations une fois la demande de remboursement générée. L&#39;option de remboursement est disponible pendant 25 jours après la date d&#39;achat. Voir le [Contrat client Marketplace](https://www.adobe.com/legal/terms/enterprise-licensing/magento-legacy-terms.html).

### Factures de commande

Vous pouvez télécharger les factures de commande à partir de l’[!UICONTROL **Historique des achats**] de votre compte Marketplace. La facture ne fournit pas la TVA ni l&#39;adresse du vendeur, car il ne s&#39;agit pas d&#39;une exigence de Marketplace pour le moment.

Pour télécharger une facture de commande pour un achat Marketplace, connectez-vous à votre compte Marketplace et procédez comme suit :

1. Cliquez sur [!UICONTROL **Mon profil**] > [!UICONTROL **Historique des achats**].
1. Localisez l’achat.
1. Cliquez sur l’icône d’imprimante dans le coin supérieur droit de la commande.

### Transferts d’achat

L’équipe d’assistance Marketplace n’a pas la possibilité de transférer les achats vers un autre compte. Vous devez acheter toutes les applications et extensions sous le compte Commerce principal pour éviter des problèmes d’installation et de déploiement. Adobe Commerce a droit à un identifiant unique. Étant donné que le compositeur est utilisé pour l’installation, un seul ensemble de [clés d’accès](#create-an-access-key) liées au compte principal peut être utilisé. La seule solution disponible est de [demander un remboursement](#refund-requests) à partir du compte d’achat Marketplace (si la politique de remboursement d’Adobe Commerce l’autorise).

Vous pouvez [partager](commerce-account-share.md) une instance Commerce via le compte principal. L’accès partagé accorde des autorisations spéciales à un compte subordonné à partir d’un compte principal. Le point d’accès partagé est généré à partir du compte principal. Le compte principal peut être le compte Commerce autorisé, le compte marchand principal ou un compte partagé au sein d’une organisation.

Ces autorisations spéciales accordent le même niveau d’accès sur Adobe Commerce que le principal, mais elles ne sont pas transférées vers Adobe Commerce Marketplace ou Developer Portal. Cela signifie que l’achat d’une extension à partir d’un compte subordonné sur la Marketplace ne peut pas être partagé avec le compte principal. L’accès partagé est à sens unique (compte principal vers le compte subordonné). Cela ne fonctionne pas lorsqu’un compte subordonné tente d’effectuer un partage vers le compte principal.

[1]: https://marketplace.magento.com/
[2]: https://www.paypal.com/us/home
[3]: https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/
[4]: https://www.adobe.com/commerce/magento/enterprise.html
[6]: https://business.adobe.com/fr/products/magento/magento-commerce.html
