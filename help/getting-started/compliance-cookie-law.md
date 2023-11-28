---
title: Conformité à la loi sur les cookies
description: Pour suivre le rythme de la législation dans de nombreux pays concernant l'utilisation des cookies, Adobe Commerce et Magento Open Source offrent aux commerçants un choix de méthodes pour obtenir le consentement du client.
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: ae43d97bb3031a06ce6a0211ee304aae53e4eb08
workflow-type: tm+mt
source-wordcount: '2145'
ht-degree: 0%

---

# Conformité à la loi sur les cookies

Les cookies sont de petits fichiers qui sont enregistrés sur l’ordinateur de chaque visiteur de votre site et utilisés comme emplacements de stockage temporaires pour information. Les informations enregistrées dans les cookies permettent de personnaliser l’expérience d’achat, de lier les visiteurs à leur panier, de mesurer les schémas de trafic et d’améliorer l’efficacité des promotions. Pour suivre le rythme de la législation dans de nombreux pays concernant l&#39;utilisation des cookies, Adobe Commerce et Magento Open Source offrent aux commerçants un choix de méthodes pour obtenir le consentement du client. Pour obtenir la liste des cookies par défaut dans Adobe Commerce et Magento Open Source, la variable [Référence du cookie](#default-cookies).

>[!NOTE]
>
>Si vous modifiez la valeur par défaut [Paramètres de confidentialité de Google](../merchandising-promotions/google-tools.md#google-privacy-settings) pour se conformer à la [Règlement général sur la protection des données](compliance-gdpr.md), il n’est pas nécessaire d’obtenir le consentement de l’utilisateur pour l’utilisation des cookies Google Analytics.

## Méthode 1 : consentement implicite

Le consentement implicite signifie que les visiteurs de votre boutique ont une compréhension claire du fait que les cookies sont une partie nécessaire des opérations et qu’en utilisant votre site, ils ont indirectement accordé l’autorisation de les utiliser. La clé pour obtenir un consentement implicite consiste à fournir suffisamment d’informations pour qu’un visiteur puisse prendre une décision éclairée. De nombreux magasins affichent un message en haut de toutes les pages standard qui fournit un bref aperçu de la manière dont les cookies sont utilisés, avec un lien vers la politique de confidentialité du magasin. La politique de confidentialité doit décrire le type d’informations collectées par votre boutique et la manière dont elle est utilisée.

## Méthode 2 : consentement exprimé

Exploitation de votre boutique dans _mode restriction des cookies_ demande aux visiteurs d’exprimer leur consentement avant que les cookies ne puissent être enregistrés sur leurs ordinateurs. À moins que le consentement ne soit accordé, de nombreuses fonctionnalités de votre boutique ne sont pas disponibles. Si, par exemple, le Google Analytics est disponible pour votre boutique, il ne peut être appelé qu’après que le visiteur a autorisé l’utilisation des cookies.

## Mode de restriction des cookies

Lorsque le mode de restriction des cookies est activé, les visiteurs de votre boutique sont avertis que les cookies sont requis pour les opérations complètes. Selon votre thème, le message peut s’afficher au-dessus de l’en-tête, sous le pied de page ou ailleurs dans la page. Le message renvoie à votre politique de confidentialité pour plus d’informations et encourage les visiteurs à cliquer sur le bouton Autoriser pour accorder leur consentement. Une fois le consentement accordé, le message disparaît.

Votre [politique de confidentialité](privacy-policy.md)) doit inclure le nom de votre boutique et les coordonnées de votre contact, et expliquer l’objectif de chaque cookie utilisé par votre boutique. Pour en savoir plus, voir [Référence du cookie](#default-cookies).

>[!NOTE]
>
>Si vous modifiez la clé URL de la politique de confidentialité, vous devez également créer une réécriture d’URL personnalisée pour rediriger le trafic vers la nouvelle clé d’URL. Dans le cas contraire, le lien du message Mode de restriction des cookies renvoie `404 Page Not Found`.

![Exemple de storefront - avis de restriction de cookie](./assets/storefront-cookie-restriction-message.png){width="600"}

### Étape 1 : activation du mode restriction des cookies

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de navigation de gauche, sous **[!UICONTROL General]**, choisissez **[!UICONTROL Web]**.

1. Développez l’objet **[!UICONTROL Default Cookie Settings]** et procédez comme suit :

   ![Configuration web - paramètres de cookie par défaut](./assets/web-default-cookie-settings.png){width="600"}

   - Saisissez le **[!UICONTROL Cookie Lifetime]** en secondes.

   - Si vous souhaitez rendre les cookies disponibles pour d’autres dossiers, saisissez la variable **[!UICONTROL Cookie Path]**. Pour rendre les cookies disponibles n’importe où sur le site, entrez une barre oblique (`/`). Cette valeur ne peut contenir que le chemin du cookie, et **_cannot_** contiennent tous les autres paramètres de cookie.

   - Pour mettre les cookies à la disposition d’un sous-domaine, saisissez le nom de sous-domaine dans le champ **[!UICONTROL Cookie Domain]** Champ (`subdomain.yourdomain.com`). Pour rendre les cookies disponibles pour tous les sous-domaines, saisissez le nom de domaine précédé d’un point (`.yourdomain.com`). Cette valeur ne peut contenir que le domaine du cookie, et **_cannot_** contiennent tous les autres paramètres de cookie.

   - Pour empêcher les langages de script, tels que JavaScript, d’accéder aux cookies, veillez à ce que **Utiliser HTTP uniquement** est défini sur `Yes`.

   - Définir **[!UICONTROL Cookie Restriction Mode]** to `Yes`.

     Si nécessaire, décochez la case et cliquez sur **[!UICONTROL OK]** pour confirmer le changement de portée.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous y êtes invité, cliquez sur le bouton **[!UICONTROL Cache Management]** lien dans le message système. Ensuite, actualisez chaque cache non valide.

### Étape 2 : mise à jour de votre politique de confidentialité

Mettez à jour votre [politique de confidentialité](privacy-policy.md) afin qu’elle reflète les informations collectées par votre entreprise et la manière dont elle est utilisée.

## Cookies par défaut

Les cookies par défaut d’Adobe Commerce et de Magento Open Source sont classés comme étant exemptés/non exemptés afin d’aider les marchands à respecter les exigences de confidentialité telles que la variable [RGPD](compliance-gdpr.md). Les marchands doivent utiliser ces informations comme guide et consulter les conseillers juridiques pour mettre à jour leurs politiques de confidentialité et de cookies dans le cadre d’une stratégie de conformité à la réglementation de la confidentialité globale.

Les cookies suivants sont utilisés par [!DNL Commerce] &quot;prêt à l’emploi&quot; pour les installations on-premise et cloud. Ces cookies peuvent être requis par les fonctionnalités qui sont explicitement demandées par le client. Pour en savoir plus sur la durée de vie des cookies de session, voir [Durée de vie de la session](../customers/customer-online-options.md).

Certains de ces cookies peuvent fournir des options de configuration, notamment activer/désactiver, si nécessaire.

### Cookies de fonctionnalités demandés (exemptés)


#### `add_to_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Utilisé par Google Tag Manager. Capture le SKU, le nom, le prix et la quantité du produit supprimés du panier et met les informations à disposition pour une intégration ultérieure par des scripts tiers.

#### `guest-view`

Stocke l’identifiant de commande que les clients utilisent pour récupérer leur état de commande. Vue Commandes d’invités. Utilisé dans _[!DNL Orders and Returns]_des widgets.

- Est-il sécurisé ? Non
- HTTP uniquement : Oui
- Stratégie d’expiration : session
- Module : `Magento_Sales`

#### `login_redirect`

Permet de conserver la page de destination qui était chargée avant que le client ne soit invité à se connecter. Une redirection de connexion est utilisée avec le mini panier pour les clients connectés si la variable [Afficher le mini-panier](../stores-purchase/cart-configuration.md#mini-cart) l’option de configuration est définie sur `Yes`.

- Est-il sécurisé ? Non
- HTTP uniquement : Non
- Stratégie d’expiration : session
- Module : `Magento_Customer`

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Stocke localement le contenu de la bannière pour améliorer les performances.

#### `mage-messages`

Effectue le suivi des messages d’erreur et autres notifications qui s’affichent à l’utilisateur, tels que le message de consentement du cookie, et de divers messages d’erreur. Le message est supprimé du cookie une fois qu’il a été présenté au nouvel acheteur.

Il n’existe pas d’option pour désactiver ce cookie.

- Est-il sécurisé ? Non
- HTTP uniquement : Non
- Politique d’expiration : durée 1 an. Effacé sur le front-end lorsque le message s’affiche pour l’utilisateur.
- Module : `Magento_Theme`

#### `mage-translation-storage` (stockage local)

Stocke le contenu traduit sur demande de l’acheteur. Utilisé lorsque [Stratégie de traduction](../configuration-reference/advanced/developer.md) est configuré comme &quot;Dictionnaire (traduction côté storefront)&quot;.

- Est-il sécurisé ? Non
- HTTP uniquement : Non
- Stratégie d’expiration : selon les règles de stockage local
- Module : `Magento_Translation`

#### `mage-translation-file-version` (stockage local)

Effectue le suivi de la version des traductions dans le stockage local. Utilisé lorsque [Stratégie de traduction](../configuration-reference/advanced/developer.md) est configuré comme `Dictionary (Translation on Storefront side)`.

- Est-il sécurisé ? Non
- HTTP uniquement : Non
- Stratégie d’expiration : selon les règles de stockage local
- Module : `Magento_Translation`

#### `product_data_storage` (stockage local)

Stocke la configuration des données de produit liées aux produits récemment consultés/comparés.

- Est-il sécurisé ? Non
- HTTP uniquement : Non
- Stratégie d’expiration : selon les règles de stockage local
- Module : `Magento_Catalog`

#### `recently_compared_product` (stockage local)

Stocke les ID de produit des produits récemment comparés.

- Est-il sécurisé ? Non
- HTTP uniquement : Non
- Stratégie d’expiration : selon les règles de stockage local
- Module : `Magento_Catalog`

#### `recently_compared_product_previous` (stockage local)

Stocke les ID de produit des produits précédemment comparés pour une navigation facile.

- Est-il sécurisé ? Non
- HTTP uniquement : Non
- Stratégie d’expiration : selon les règles de stockage local
- Module : `Magento_Catalog`

#### `recently_viewed_product` (stockage local)

Stocke les ID de produit des produits récemment consultés pour une navigation facile.

- Est-il sécurisé ? Non
- HTTP uniquement : Non
- Stratégie d’expiration : selon les règles de stockage local
- Module : `Magento_Catalog`

#### `recently_viewed_product_previous` (stockage local)

Stocke les ID de produit des produits récemment consultés pour une navigation facile.

- Est-il sécurisé ? Non
- HTTP uniquement : Non
- Stratégie d’expiration : selon les règles de stockage local
- Module : `Magento_Catalog`

#### `remove_from_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Utilisé par [Gestionnaire de balises de Google](../merchandising-promotions/google-tag-manager.md). Capture le SKU, le nom, le prix et la quantité du produit ajoutés au panier et met les informations à disposition pour une intégration ultérieure par des scripts tiers.

#### `stf`

Enregistre l’heure à laquelle les messages sont envoyés par SendFriend ([Envoyer un courrier électronique à un ami](../stores-purchase/email-a-friend.md)).

- Est-il sécurisé ? Oui
- HTTP uniquement : Oui
- Stratégie d’expiration : session
- Module : `Magento_SendFriend`

#### `X-Magento-Vary`

Paramètre de configuration qui améliore les performances lors de l’utilisation de la mise en cache de contenu statique vernis.

- Est-il sécurisé ? Oui
- HTTP uniquement : Oui
- Stratégie d’expiration : basée sur le paramètre PHP session.cookie_lifetime
- Module : `Magento_PageCache`

#### `form_key`

Mesure de sécurité qui ajoute une chaîne aléatoire à tous les envois de formulaire pour protéger les données de la falsification de requête intersite (CSRF, Cross Site Request Forgery).

- Est-il sécurisé ? Non
- HTTP uniquement : Non
- Stratégie d’expiration :
   - PHP : basé sur le paramètre PHP session.cookie_lifetime
   - JS : session
- Module : cache de page

#### `mage-cache-sessid`

La valeur de ce cookie déclenche le nettoyage de l’espace de stockage du cache local. Lorsque le cookie est supprimé par l’application principale, l’administrateur nettoie le stockage local et définit la valeur du cookie sur `true`.

- Est-il sécurisé ? Non
- HTTP uniquement : Non
- Stratégie d’expiration : session
- Module : `Magento_Customer`

#### `mage-cache-storage`

Stockage local de contenu spécifique au visiteur qui active les fonctions de commerce électronique.

- Est-il sécurisé ? Non
- HTTP uniquement : Non
- Stratégie d’expiration : session
- Module : `Magento_Customer`, `Magento_Persistent`

#### `mage-cache-storage` (stockage local)

Stockage local de contenu spécifique au visiteur qui active les fonctions de commerce électronique.

- Est-il sécurisé ? Non
- HTTP uniquement : Non
- Stratégie d’expiration : session
- Module : `Magento_Customer`, `Magento_Persistent`, `Magento_NegotiableQuote`

#### `mage-cache-storage-section-invalidation` (stockage local)

Force le stockage local de sections de contenu spécifiques qui doivent être invalidées.

- Est-il sécurisé ? Non
- HTTP uniquement : Non
- Stratégie d’expiration : par stockage local
- Module : `Magento_Customer`

#### `persistent_shopping_cart`

Stocke la clé (ID) du panier persistant afin de permettre de restaurer le panier d’un acheteur anonyme.

- Est-il sécurisé ? Oui
- HTTP uniquement : Oui
- Stratégie d’expiration : basée sur [Panier persistant](../stores-purchase/cart-persistent.md) - Configuration de la durée de vie de persistance (secondes)
- Module : `Magento_Persistent`

#### `private_content_version`

Ajoute un nombre et une heure aléatoires uniques aux pages avec le contenu client afin de les empêcher d’être mises en cache sur le serveur.

Il est défini à plusieurs endroits : en PHP, en JavaScript comme cookie et en JavaScript comme stockage local.

Pour HTTP Only=`Yes` (selon la demande), cela signifie que le cookie est sécurisé s’il est défini pendant la demande HTTPS et non sécurisé s’il est défini pendant la demande HTTP.

- Est-il sécurisé ? `Yes` (sur demande), `No`
- HTTP uniquement : `No`
- Stratégie d’expiration : basée sur [Panier persistant](../stores-purchase/cart-persistent.md) - Configuration de la durée de vie de persistance (secondes)
   - PHP : `1` year / `315360000s` (dix ans)
   - JS : `1` day
   - Stockage local JS : par règles de stockage local (pour toujours)
- Module : `Magento_PageCache`, `Magento_Customer`

#### `section_data_ids`

Stocke des informations spécifiques aux clients liées aux actions initiées par les acheteurs, telles que l’affichage des listes de souhaits et les informations de passage en caisse.

- Est-il sécurisé ? `No`
- HTTP uniquement : `No`
- Stratégie d’expiration : `Session`
- Module : `Magento_Customer`

#### `store`

Effectue le suivi de la vue de magasin/des paramètres régionaux spécifiques sélectionnés par l’acheteur.

- Est-il sécurisé ? `No`
- HTTP uniquement : `Yes`
- Stratégie d’expiration : `1` year
- Module : `Magento_Store`

#### `mage-banners-cache-storage` - stockage local

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Stockage local pour la fonctionnalité de bannière.

- Est-il sécurisé ? `No`
- HTTP uniquement : `No`
- Stratégie d’expiration : selon les règles de stockage local
- Module : `Magento_Banner`

## Cookies Google Analytics

Les cookies suivants sont utilisés lors de la [Google Analytics](../merchandising-promotions/google-analytics.md) ou Google Universal Analytics est entièrement activé pour votre installation. Pour désactiver ces cookies en vue de la conformité à la réglementation sur la confidentialité, voir [Paramètres de confidentialité de Google](../merchandising-promotions/google-tools.md#google-privacy-settings). Pour en savoir plus, voir [Utilisation des cookies de Google Analytics sur les sites web][1].

### Cookies Google Universal Analytics - non exemptés

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Bibliothèques JavaScript : `gtag.js` et `analytics.js`

- `_ga`: distingue les visiteurs de votre site.
- `_gid`: distingue les visiteurs de votre site.
- `gat`: utilisé pour ralentir le taux de requête.
- `dc_gtm_<property-id>`: limite le taux de demande lorsque les Google Analytics sont déployés avec [Gestionnaire de balises de Google](../merchandising-promotions/google-tag-manager.md).
- `AMP_TOKEN`: contient un jeton qui peut être utilisé pour récupérer un ID de client auprès du service d’ID de client AMP. D’autres valeurs possibles sont notamment l’exclusion, la demande d’entrée ou une erreur lors de la récupération d’un ID client à partir du service AMP Client ID.
- `_gac_<property-id>`: contient des informations relatives à la campagne pour l’utilisateur. Les balises de conversion Google AdWords lisez ce cookie si Google Analytics est lié à votre [AdWords][2] compte .

### Cookies Google Analytics - non exemptés

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Bibliothèque JavaScript : `ga.js`

- `__utma`: différencie les acheteurs et les sessions. Ce cookie est créé lorsque la bibliothèque JavaScript s’exécute et qu’il n’existe aucun `__utma` du cookie. Le cookie est mis à jour chaque fois que des données sont envoyées aux Google Analytics.
- `__utmt`: utilisé pour ralentir le taux de requête.
- `__utmb`: détermine les nouvelles sessions/visites. Ce cookie est créé lorsque la bibliothèque JavaScript s’exécute et qu’il n’existe aucun `__utmb` du cookie. Le cookie est mis à jour chaque fois que des données sont envoyées aux Google Analytics.
- `_utmz`: enregistre la source de trafic ou la campagne qui explique comment l’acheteur a accédé à votre site. Le cookie est créé lors de l’exécution de la bibliothèque JavaScript et est mis à jour chaque fois que des données sont envoyées aux Google Analytics.
- `__utmv`: stocke les données de variable personnalisée au niveau du visiteur. Ce cookie est créé lorsqu’un développeur utilise la variable `_setCustomVar` avec une variable personnalisée au niveau du visiteur. Ce cookie est mis à jour chaque fois que des données sont envoyées aux Google Analytics.

## Cookies Recommendations de produit

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Les cookies suivants sont utilisés par Product Recommendations pour les clients Adobe Commerce. Ces cookies sont installés avec la variable [Module DataServices](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html).

- `mg_dnt`: vous permet de [restreindre la collecte de données Adobe Commerce ;](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/developer/setting-cookie.html) si vous disposez d’un code personnalisé pour gérer le consentement aux cookies sur votre site.
- `user_allowed_save_cookie`: utilisé pour [mode restriction des cookies](#cookie-restriction-mode).
- `authentication_flag`: indique si un acheteur s’est connecté ou s’est déconnecté. Ce cookie est mis à jour en même temps que la variable `dataservices_customer_id` du cookie.
- `dataservices_customer_id`: indique si un acheteur s’est connecté ou s’est déconnecté. Ce cookie contient l’identifiant unique du client dans le système.
- `dataservices_customer_group`: indique le groupe d’un client. Ce cookie est stocké en tant que [sha1](https://en.wikipedia.org/wiki/SHA-1) somme de contrôle de l’ID de groupe du client.
- `dataservices_cart_id`: identifie les actions du panier d’un acheteur. Ce cookie contient l’identifiant unique du panier du client dans le système.
- `dataservices_product_context`: identifie les interactions produit d’un acheteur. Ce cookie contient l’ID de guillemet unique du client dans le système.

## Cookies supplémentaires

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Les cookies suivants sont définis pour les clients Adobe Commerce. Ces cookies sont installés avec la variable [Module DataServices](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html).

- `mg`: défini par le dispositif de suivi JavaScript Snowplow. Vous trouverez plus d’informations dans la section [Documentation de Snowpload](https://docs.snowplow.io/docs/collecting-data/collecting-from-own-applications/javascript-trackers/javascript-tracker/javascript-tracker-v3/tracker-setup/initialization-options).
- `com.adobe.alloy.getTld`: étant donné le nom d’hôte de la page web actuelle, il s’agit du domaine le plus élevé qui ne correspond pas à un &quot;suffixe public&quot; comme indiqué dans https://publicsuffix.org. Il s’agit essentiellement du domaine le plus élevé qui peut accepter les cookies. Ce cookie fait partie du [Alloy Web SDK](https://github.com/adobe/alloy).

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212
