---
title: Conformité à la loi sur les cookies
description: Pour suivre le rythme de la législation dans de nombreux pays concernant l'utilisation des cookies, Adobe Commerce et Magento Open Source offrent aux commerçants un choix de méthodes pour obtenir le consentement du client.
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: 04e8fe7cf303f434bab748df447eef8ac1097196
workflow-type: tm+mt
source-wordcount: '1825'
ht-degree: 0%

---

# Conformité à la loi sur les cookies

Les cookies sont de petits fichiers qui sont enregistrés sur l’ordinateur de chaque visiteur de votre site et utilisés comme emplacements de stockage temporaires pour information. Les informations enregistrées dans les cookies permettent de personnaliser l’expérience d’achat, de lier les visiteurs à leur panier, de mesurer les schémas de trafic et d’améliorer l’efficacité des promotions. Pour suivre le rythme de la législation dans de nombreux pays concernant l&#39;utilisation des cookies, Adobe Commerce et Magento Open Source offrent aux commerçants un choix de méthodes pour obtenir le consentement du client. Pour obtenir la liste des cookies par défaut dans Adobe Commerce et Magento Open Source, reportez-vous à la [référence sur les cookies](#default-cookies).

>[!NOTE]
>
>Si vous modifiez les [ paramètres de confidentialité de Google ](../merchandising-promotions/google-tools.md#google-privacy-settings) par défaut pour vous conformer au [Règlement général sur la protection des données](compliance-gdpr.md), il n’est pas nécessaire d’obtenir le consentement de l’utilisateur pour l’utilisation des cookies Google Analytics.

## Mode de restriction des cookies

Lorsque le mode de restriction des cookies est activé, les visiteurs de votre boutique sont avertis que les cookies sont requis pour les opérations complètes. Selon votre thème, le message peut s’afficher au-dessus de l’en-tête, sous le pied de page ou ailleurs dans la page. Le message renvoie à votre politique de confidentialité pour plus d’informations et encourage les visiteurs à cliquer sur le bouton Autoriser pour accorder leur consentement. Une fois le consentement accordé, le message disparaît.

Votre [politique de confidentialité](privacy-policy.md)) doit inclure le nom de votre boutique et les coordonnées de votre contact, et expliquer l’objectif de chaque cookie utilisé par votre boutique. Pour en savoir plus, voir [Référence du cookie](#default-cookies).

>[!NOTE]
>
>Si vous modifiez la clé URL de la politique de confidentialité, vous devez également créer une réécriture d’URL personnalisée pour rediriger le trafic vers la nouvelle clé d’URL. Dans le cas contraire, le lien du message Mode de restriction des cookies renvoie `404 Page Not Found`.

![Exemple de storefront - avis de restriction de cookie](./assets/storefront-cookie-restriction-message.png){width="600"}

### Étape 1 : activation du mode restriction des cookies

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de navigation de gauche sous **[!UICONTROL General]**, choisissez **[!UICONTROL Web]**.

1. Développez la section **[!UICONTROL Default Cookie Settings]** et procédez comme suit :

   ![ Configuration web - paramètres de cookie par défaut](./assets/web-default-cookie-settings.png){width="600"}

   - Saisissez le **[!UICONTROL Cookie Lifetime]** en secondes.

   - Si vous souhaitez rendre les cookies disponibles pour d’autres dossiers, saisissez le **[!UICONTROL Cookie Path]**. Pour rendre les cookies disponibles n’importe où sur le site, entrez une barre oblique (`/`). Cette valeur ne peut contenir que le chemin du cookie et **_ne peut pas_** contenir d’autres paramètres de cookie.

   - Pour rendre les cookies disponibles pour un sous-domaine, saisissez le nom du sous-domaine dans le champ **[!UICONTROL Cookie Domain]** (`subdomain.yourdomain.com`). Pour rendre les cookies disponibles pour tous les sous-domaines, saisissez le nom de domaine précédé d’un point (`.yourdomain.com`). Cette valeur ne peut contenir que le domaine du cookie et **_ne peut pas_** contenir d’autres paramètres de cookie.

   - Pour empêcher les langages de script, tels que JavaScript, d’accéder aux cookies, assurez-vous que l’option **Utiliser HTTP uniquement** est définie sur `Yes`.

   - Définissez **[!UICONTROL Cookie Restriction Mode]** sur `Yes`.

     Si nécessaire, décochez la case et cliquez sur **[!UICONTROL OK]** pour confirmer le changement de portée.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

1. Lorsque vous êtes invité à mettre à jour le cache, cliquez sur le lien **[!UICONTROL Cache Management]** dans le message système et actualisez chaque cache non valide.

### Étape 2 : mise à jour de votre politique de confidentialité

Mettez à jour votre [politique de confidentialité](privacy-policy.md) afin qu’elle reflète les informations collectées par votre entreprise et la manière dont elle est utilisée.

## Cookies par défaut

Les cookies par défaut d’Adobe Commerce et de Magento Open Source sont classés comme étant exemptés/non exemptés afin d’aider les marchands à respecter les exigences de confidentialité telles que le [RGPD](compliance-gdpr.md). Les marchands doivent utiliser ces informations comme guide et consulter les conseillers juridiques pour mettre à jour leurs politiques de confidentialité et de cookies dans le cadre d’une stratégie de conformité à la réglementation de la confidentialité globale.

Les cookies suivants sont utilisés par [!DNL Commerce] &quot;prêts à l’emploi&quot; pour les installations on-premise et cloud. Ces cookies peuvent être requis par les fonctionnalités qui sont explicitement demandées par le client. Pour en savoir plus sur la durée de vie des cookies de session, voir [Durée de vie de la session](../customers/customer-online-options.md).

Certains de ces cookies peuvent fournir des options de configuration, notamment activer/désactiver, si nécessaire.

### Cookies de fonctionnalités demandés (exemptés)

#### `add_to_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Capture le SKU, le nom, le prix et la quantité du produit supprimés du panier. Permet aux Google Analytics de savoir quand un produit a été ajouté à un panier.

#### `guest-view`

Associe une commande d’invité à un invité (car il n’existe aucun compte pour invité).

#### `login_redirect`

Enregistre l’URL de redirection pour orienter l’utilisateur en cas de connexion réussie et d’enregistrement de l’utilisateur. Enregistre la page sur laquelle se trouvait un utilisateur avant de se connecter (afin de déterminer l’emplacement auquel il reviendra après s’être connecté).

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Stocke localement le contenu de la bannière pour améliorer les performances. Le contenu de la bannière désigne tout contenu qu’un commerçant peut afficher sur son site Web.

#### `mage-messages`

Effectue le suivi des messages d’erreur et autres notifications qui s’affichent à l’utilisateur, tels que le message de consentement du cookie, et de divers messages d’erreur. Le message est supprimé du cookie une fois qu’il a été présenté au nouvel acheteur. Il n’existe pas d’option pour désactiver ce cookie. Il s’agit de la manière dont les informations ponctuelles sont communiquées à l’utilisateur, telles que les messages d’erreur.

#### `product_data_storage` (stockage local)

Stocke la configuration des données de produit utilisées pour utiliser les fonctions &quot;Récemment consultées&quot; et &quot;Comparer les produits&quot;. Stocke les paramètres spécifiques d’un utilisateur (par exemple, s’il a récemment consulté un produit ou comparé des produits).

#### `recently_compared_product` (stockage local)

Stocke les ID de produit des produits récemment comparés.

#### `recently_compared_product_previous` (stockage local)

Stocke les ID de produit des produits précédemment comparés pour une navigation facile.

#### `recently_viewed_product` (stockage local)

Stocke les ID de produit des produits récemment consultés pour une navigation facile.

#### `recently_viewed_product_previous` (stockage local)

Stocke les ID de produit des produits récemment consultés pour une navigation facile.

#### `remove_from_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Permet aux Google Analytics de savoir quand un produit a été supprimé d’un panier.

#### `stf`

Enregistre l’heure à laquelle les messages sont envoyés par le module SendFriend ([Envoyer un courrier électronique à un ami](../stores-purchase/email-a-friend.md)). Lorsqu’un acheteur envoie un lien vers un produit, ce cookie enregistre un horodatage et conserve un nombre.

#### `X-Magento-Vary`

Indique à quel moment une nouvelle version d’une page doit être diffusée à partir du cache. Prend en charge les performances du site web.

#### `form_key`

Mécanisme de sécurité qui contient une valeur générée de manière aléatoire pour empêcher les attaques CSRF (Cross Site Request Forgery) en permettant de déterminer si une requête provient d’une source réelle ou d’un acteur incorrect. Il s’agit d’une pratique standard du secteur pour empêcher les attaques CSRF.

#### `mage-cache-sessid`

Utile pour déterminer quand nettoyer le stockage local dans le navigateur après l’expiration de la session. Il est utilisé pour déterminer si le stockage local doit être nettoyé. L’absence de ce cookie déclenche le nettoyage du stockage local.

#### `mage-cache-storage`

Stockage local de contenu spécifique au visiteur qui active les fonctions de commerce électronique. Non utilisé par défaut, mais lorsqu’il est utilisé, il est utilisé pour accélérer le passage en caisse afin que les informations utilisateur de base soient disponibles lorsque quelqu’un quitte et revient.

#### `mage-cache-storage-section-invalidation`

Stocke des informations relatives aux sections de la page qui doivent être invalidées et supprimées.

#### `persistent_shopping_cart`

Stocke l’identifiant clé d’un panier persistant afin de permettre de restaurer le panier d’un acheteur anonyme.

#### `private_content_version`

Ajoute un nombre et une heure aléatoires uniques aux pages avec le contenu client afin de les empêcher d’être mises en cache sur le serveur. Il est défini à plusieurs endroits : en PHP, dans JavaScript comme cookie et dans JavaScript comme stockage local.

#### `section_data_ids`

Stocke des informations spécifiques aux clients liées aux actions initiées par les acheteurs, telles que l’affichage des listes de souhaits et les informations de passage en caisse.

#### `store`

Effectue le suivi de la vue/des paramètres régionaux de magasin spécifiques sélectionnés par l’acheteur.

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Stockage local pour la fonctionnalité de bannière. La bannière désigne les ressources générales du site web, toutes les informations affichées pour un acheteur.

#### `PHPSESSID`

Effectue le suivi des sessions utilisateurs sur le storefront. Voici les acheteurs qui utilisent les produits finaux.

#### `admin`

Effectue le suivi des sessions utilisateur côté administrateur.

#### `loggedOutReasonCode`

Défini lorsqu’un utilisateur administrateur est verrouillé après un certain nombre de tentatives de mot de passe infructueuses.

#### `section_data_clean`

Défini lorsqu’un utilisateur change de vue de magasin. La présence de ce cookie entraîne JavaScript à recharger certaines sections de la page afin de refléter la vue de magasin correcte.

#### `lang`

Défini indirectement par le module Admin Analytics. Utilisé uniquement dans une zone administrative d’un magasin. Non applicable aux acheteurs.

#### `s_fid`

Défini indirectement par le module Admin Analytics. Horodatage de l’ID de visiteur unique de secours. Elle permet d’identifier un visiteur unique si le cookie standard `s_vi` n’est pas disponible en raison de restrictions des cookies tiers. Utilisé uniquement dans une zone administrative d’un magasin. Non applicable aux acheteurs.

#### `s_cc`

Défini indirectement par le module Admin Analytics. Il est défini et lu par le code JavaScript pour déterminer si les cookies sont activés. Utilisé uniquement dans une zone administrative d’un magasin. Non applicable aux acheteurs.

#### `apt.sid`

Défini par la bibliothèque Gainsight PX indirectement utilisé par le module Admin Analytics. Ce cookie a pour objectif d’autoriser le suivi des ID de session persistante sous le domaine de niveau supérieur du produit et est utilisé comme ID de référence pour la session active. Utilisé uniquement dans une zone administrative d’un magasin. Non applicable aux acheteurs.

#### `apt.uid`

Défini par la bibliothèque Gainsight PX indirectement utilisé par le module Admin Analytics. Ce cookie a pour objectif d’autoriser le suivi des identifiants persistants sous le domaine de niveau supérieur du produit et est utilisé comme ID de référence pour l’entité utilisateur. Utilisé uniquement dans une zone administrative d’un magasin. Non applicable aux acheteurs.

#### `s_sq`

Défini indirectement par le module Admin Analytics. Utilisé par la fonction ClickMap qui collecte des données sur l’endroit où les visiteurs cliquent et sur ce qu’ils cliquent. Stocke les informations de chaque clic. Utilisé uniquement dans une zone administrative d’un magasin. Non applicable aux acheteurs.

#### `pagebuilder_modal_dismissed`

Défini par le module Page Builder. Contient un indicateur qui empêche les invites suivantes demandant à un administrateur de confirmer l’ouverture d’une action spécifique si l’administrateur les avait explicitement ignorées auparavant. Utilisé uniquement dans une zone administrative d’un magasin. Non applicable aux acheteurs.

#### `pagebuilder_template_apply_confirm`

Défini par le module Page Builder. Contient un indicateur qui empêche les invites suivantes demandant à un administrateur de confirmer l’ouverture d’une action spécifique si l’administrateur les avait explicitement ignorées auparavant. Utilisé uniquement dans une zone administrative d’un magasin. Non applicable aux acheteurs.

#### `accordion-{VARIABLE}-{VARIABLE}`

Utilisation dans le cadre de l’implémentation des fonctionnalités d’onglets uniquement dans une zone administrative d’un magasin. Non applicable aux acheteurs.

## Cookies Recommendations de produit

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Les cookies suivants sont utilisés par Product Recommendations pour les clients Adobe Commerce. Ces cookies sont installés avec le [module DataServices](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure).

- `mg_dnt` : vous permet de [restreindre la collecte de données Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/developer/setting-cookie) si vous disposez d’un code personnalisé pour gérer le consentement aux cookies sur votre site.
- `user_allowed_save_cookie` : utilisé pour le [mode restriction de cookie](#cookie-restriction-mode).
- `authentication_flag` : indique si un acheteur s’est connecté ou s’est déconnecté. Ce cookie est mis à jour en même temps que le cookie `dataservices_customer_id`.
- `dataservices_customer_id` : indique si un acheteur s’est connecté ou s’est déconnecté. Ce cookie contient l’identifiant unique du client dans le système.
- `dataservices_customer_group` : indique un groupe de clients. Ce cookie est stocké en tant que somme de contrôle [sha1](https://en.wikipedia.org/wiki/SHA-1) de l’ID de groupe du client.
- `dataservices_cart_id` : identifie les actions du panier d’un acheteur. Ce cookie contient l’identifiant unique du panier du client dans le système.
- `dataservices_product_context` : identifie les interactions produit d’un acheteur. Ce cookie contient l’ID de guillemet unique du client dans le système.

## Cookies supplémentaires

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Les cookies suivants sont définis pour les clients Adobe Commerce. Ces cookies sont installés avec le [module DataServices](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure).

- `mg` : défini par le dispositif de suivi JavaScript Snowplow. Vous trouverez plus d’informations dans la [documentation Snowplow](https://docs.snowplow.io/docs/collecting-data/collecting-from-own-applications/javascript-trackers/web-tracker/tracker-setup/initialization-options).
- `com.adobe.alloy.getTld` : étant donné le nom d’hôte de la page web actuelle, il s’agit du domaine le plus élevé qui ne correspond pas à un &quot;suffixe public&quot; comme indiqué dans https://publicsuffix.org. Il s’agit essentiellement du domaine le plus élevé qui peut accepter les cookies. Ce cookie fait partie du [Alloy Web SDK](https://github.com/adobe/alloy).

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212
