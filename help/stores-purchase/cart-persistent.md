---
title: Persistance du panier
description: Découvrez comment un panier persistant effectue le suivi des articles non achetés et enregistre les informations pour la prochaine visite du client.
exl-id: 95c336b3-77ac-4cf6-8fb5-23f4ac4b67d6
feature: Shopping Cart, Configuration
source-git-commit: 26d4bb35c6e1878a8ea8c5f05a982559e5d6dc35
workflow-type: tm+mt
source-wordcount: '1473'
ht-degree: 0%

---

# Persistance du panier

Un panier persistant effectue le suivi des articles non achetés qui restent dans le panier et enregistre les informations pour la prochaine visite du client. Clients qui sont _mémorisé_ peuvent demander que le contenu de leur panier soit restauré la prochaine fois qu’ils visitent votre magasin.

L’utilisation d’un panier persistant peut contribuer à réduire le nombre de paniers abandonnés et à augmenter les ventes. Il est important de comprendre que le panier persistant n’expose à aucun moment les informations de compte sensibles. Pendant que le panier persistant est en cours d’utilisation, les clients enregistrés et les clients invités doivent se connecter à un compte existant ou créer un compte avant de passer le passage en caisse. Pour les clients invités, un panier persistant est le seul moyen de récupérer des informations d’une session précédente.

Pour gérer l’utilisation de la persistance du panier pour votre site ou dans des vues de magasin spécifiques, vous pouvez : [configuration du panier persistant](#configure-a-persistent-cart) paramètres. Pour plus d’informations sur la manière dont ces paramètres affectent l’expérience du nouvel acheteur dans votre vitrine, voir [Workflow de panier persistant](#persistent-cart-workflow).

>[!NOTE]
>
>Lors de l’utilisation d’un panier persistant, il est recommandé de définir la durée de vie de la session du serveur et du cookie de session sur une longue période. Voir [Durée de vie de la session](../customers/customer-online-options.md) pour plus d’informations.

Pour utiliser le panier persistant, le navigateur du client doit être défini pour autoriser les cookies. Deux types de cookies sont utilisés pour les opérations de panier :

- **Cookie de session** - Il existe un cookie de session à court terme lors d’une seule visite sur votre site et expire lorsque le client quitte le site, ou après une période définie.

- **Cookie persistant** - Un cookie persistant à long terme existe toujours après la fin de la session et enregistre le contenu du panier du client pour référence ultérieure.

## Workflow de panier persistant

Lorsque le panier persistant est [enabled](#configure-a-persistent-cart), le workflow dépend de :

- Les valeurs de la variable _Activer Mémoriser_ et _Effacer la persistance lors de la déconnexion_ paramètres
- La décision du client de sélectionner ou d’effacer la variable _Mémoriser_ checkbox
- Lorsque le cookie persistant est effacé

Lorsqu’un cookie persistant est appliqué, une `Not Jane Smith?` s’affiche dans l’en-tête de la page. Cette invite permet au client de mettre fin à la session persistante et de commencer à travailler en tant qu’invité ou de se connecter en tant qu’autre client. Le système conserve un enregistrement du contenu du panier, même si le client utilise par la suite différents périphériques pour faire ses achats dans votre boutique. Par exemple, un client peut ajouter un article dans le panier depuis un ordinateur portable, ajouter d’autres articles depuis un appareil mobile et terminer le processus de passage en caisse depuis une tablette.

Il existe un cookie persistant indépendant distinct pour chaque navigateur. Si le client utilise plusieurs navigateurs lors de sa visite dans votre boutique au cours d’une seule session permanente, les modifications apportées dans un navigateur sont répercutées dans tout autre navigateur lors de l’actualisation de la page. Bien que le panier persistant soit activé, votre boutique crée et conserve un cookie persistant distinct pour chaque navigateur utilisé par un client pour se connecter ou créer un compte.

### Exemple : une session ouverte sur un ordinateur partagé

Jane termine ses achats de vacances avec une session persistante. Elle ajoute un cadeau pour John dans son panier, et quelque chose pour sa mère. Puis elle va à la cuisine pour un en-cas.

John s&#39;assoit à l&#39;ordinateur pour faire des achats rapides pendant que Jane est dans la cuisine. Sans remarquer la variable `Not Jane Smith?` En haut de la page, il trouve un beau cadeau pour Jane et l&#39;ajoute au panier. Quand il va vérifier et se connecte comme lui-même, les deux articles du panier de Jane sont ajoutés à son panier. John est tellement pressé qu&#39;il ne remarque pas les éléments supplémentaires pendant _Examen des commandes_ et envoie la commande. Le chariot de Jane est maintenant vide, et John a acheté tous les cadeaux.

### Mémoriser

Les clients peuvent sélectionner la variable _Mémoriser_ de la page de connexion pour enregistrer le contenu de leur panier.

| Vous Vous Souvenez De Moi ? | Résultat |
| ------------ |  ------ |
| Sélectionné | Crée un cookie persistant et enregistre le contenu du panier pour la prochaine session de connexion du client. |
| Non sélectionné | Ne crée pas de cookie persistant et n’enregistre pas les informations sur le panier pour la prochaine session de connexion du client. |

{style="table-layout:auto"}

### Continuer la persistance lors de la déconnexion - non

| Action | Résultat |
| ------ | ------ |
| Connexion du client | Appelle le cookie persistant en plus du cookie de session, qui est déjà utilisé. |
| Le client se déconnecte | Supprime le cookie de session, mais le cookie persistant reste en vigueur. La prochaine fois que le client se connectera, il restaure les éléments du panier ou les ajoute à tout nouvel élément placé dans le panier. |
| Le client ne se déconnecte pas et le cookie de session expire | Le cookie persistant reste en vigueur. |

{style="table-layout:auto"}

### Effacer la persistance lors de la connexion

| Action | Résultat |
| ------ | ------ |
| Connexion du client | Appelle le cookie persistant en plus du cookie de session, qui est déjà utilisé. |
| Le client se déconnecte | Supprime les deux cookies. |
| Le client ne se déconnecte pas mais le cookie de session expire | Le cookie persistant reste en vigueur. |

{style="table-layout:auto"}

## Paramètres et effets du panier persistants

| Paramètres | Effet |
|----------|--------|
| **[!UICONTROL Enable Remember Me]** est défini sur `No`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**a une valeur quelconque.<br/><br/>La variable** Mémoriser **n’est pas disponible sur la page de connexion et d’enregistrement. | Le cookie persistant n’est pas utilisé. |
| **[!UICONTROL Enable Remember Me]** est défini sur `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**a une valeur quelconque.<br/><br/>** Mémoriser **n’est pas sélectionnée. | Le cookie de session est appliqué comme d’habitude ; le cookie persistant n’est pas utilisé. |
| **[!UICONTROL Enable Remember Me]** est défini sur `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**est défini sur `Yes`.<br/><br/>** Mémoriser **est défini sur `Yes`. | Lorsqu’un client se connecte, les deux cookies sont appliqués. Lorsqu’un client se déconnecte, les deux cookies sont supprimés. Si un client ne se connecte pas mais que le cookie de session expire, le cookie persistant est toujours utilisé. Outre la déconnexion, le cookie persistant est supprimé lorsque sa durée de vie est écoulée ou lorsque le client clique sur la variable `Not Jane Smith` lien. |
| **[!UICONTROL Enable Remember Me]** est défini sur `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**est défini sur `No`.<br/><br/>** Mémoriser **est défini sur `Yes` | Lorsqu’un client se connecte, les deux cookies sont appliqués. Lorsqu’un client se déconnecte, le cookie de session est supprimé, la session persistante se poursuit. Le cookie persistant est supprimé lorsque sa durée de vie est épuisée ou lorsque le client clique sur la variable `Not Jane Smith` lien. |

{style="table-layout:auto"}

## Configurer un panier persistant

Lors de la configuration d’un panier persistant, vous pouvez spécifier la durée de vie des cookies et les options que vous souhaitez mettre à disposition pour diverses activités client.

Pour plus d’informations sur la façon dont le workflow client est déterminé par ces paramètres, voir [Workflow de panier persistant](#persistent-cart-workflow).

>[!NOTE]
>
>Si le cookie de session expire pendant que le client est connecté, le cookie persistant reste actif.

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Persistent Shopping Cart]**.

1. Pour activer le panier persistant et afficher des options supplémentaires, définissez **[!UICONTROL Enable Persistence]** to `Yes`.

   ![Activation et configuration de la persistance du panier](../configuration-reference/customers/assets/persistent-shopping-cart-general.png){width="600" zoomable="yes"}

   Pour plus d’informations sur chacun de ces paramètres de configuration, voir [_Référence de configuration_](../configuration-reference/customers/persistent-shopping-cart.md)

   >[!NOTE]
   >
   >Si nécessaire, effacez la variable **[!UICONTROL Use system value]** pour modifier ces paramètres.

1. Pour **[!UICONTROL Persistence Lifetime (seconds)]**, saisissez la durée (en secondes) pendant laquelle le cookie persistant doit durer.

   La valeur par défaut de 31 536 000 secondes est d’un an. La durée maximale autorisée est de 100 ans.

1. Définir **[!UICONTROL Enable "Remember Me"]** à l’une des options suivantes :

   - `Yes` - Affiche la variable _Mémoriser_ sur la page Connexion de votre boutique, afin que les clients puissent choisir d’enregistrer les informations de leur panier.

   - `No` - La persistance peut toujours être activée, mais les clients n’ont pas la possibilité de choisir s’ils souhaitent enregistrer leurs informations.

1. Pour présélectionner le _Mémoriser_ case à cocher du client, définie **[!UICONTROL Remember Me Default Value]** to `Yes`.

   Le client peut effacer cette option s’il le souhaite.

1. Définir **[!UICONTROL Clear Persistence on Log Out]** à l’une des options suivantes :

   - `Yes` - Le panier est vidé lorsqu’un client enregistré se déconnecte.

   - `No` - Le panier est enregistré lorsqu’un client enregistré se déconnecte.

   >[!NOTE]
   >
   >Si le cookie de session expire pendant que le client est toujours connecté, le cookie persistant reste en cours d’utilisation.

1. Définir **[!UICONTROL Persist Shopping Cart]** à l’une des options suivantes :

   - `Yes` - Si le cookie de session expire, le cookie persistant est conservé. Si un acheteur invité se connecte ultérieurement ou crée un compte, le panier est restauré.

   - `No` - Le panier n’est pas conservé pour les invités une fois le cookie de session expiré.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Défini **[!UICONTROL Persist Wish List]** pour déterminer si l’état des listes de souhaits des clients est conservé lorsque la session se termine :

   - `Yes` - Le contenu de la liste de souhaits est enregistré à la fin de la session.

   - `No` - La liste de souhaits n’est pas enregistrée à la fin de la session.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Défini **[!UICONTROL Persist Recently Ordered Items]** pour déterminer si l’état des éléments récemment commandés est conservé lorsque la session se termine :

   - `Yes` - L’état des éléments récemment commandés est enregistré lorsque la session se termine.

   - `No` - L’état des éléments récemment triés n’est pas enregistré lorsque la session se termine.

1. Définir **[!UICONTROL Persist Currently Compared Products]** to `Yes` ou `No`.

1. Définir **[!UICONTROL Persist Comparison History]** to `Yes` ou `No`.

1. Définir **[!UICONTROL Persist Recently Viewed Products]** to `Yes` ou `No`.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce uniquement) Défini **[!UICONTROL Persist Customer Group Membership and Segmentation]** pour déterminer si l’état des critères d’appartenance et de segmentation du groupe du client est conservé lorsque la session se termine :

   - `Yes` - L’état de l’appartenance au groupe du client et les données de segmentation sont enregistrés à la fin de la session.

   - `No` - L’état de l’appartenance au groupe du client et les données de segmentation ne sont pas enregistrés à la fin de la session.

1. Cliquez sur **[!UICONTROL Save Config]**.
