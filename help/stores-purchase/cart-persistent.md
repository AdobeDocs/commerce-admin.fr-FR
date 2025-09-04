---
title: Persistance du panier
description: Découvrez comment un panier persistant suit les articles non achetés et enregistre les informations pour la prochaine visite du client.
exl-id: 95c336b3-77ac-4cf6-8fb5-23f4ac4b67d6
feature: Shopping Cart, Configuration
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '1038'
ht-degree: 0%

---

# Persistance du panier

Un panier persistant enregistre une référence au compte du client sur l’appareil actuel, ce qui garantit que le contenu du panier reste accessible à l’expiration de la session connectée.

Si un client est _en mémoire_, le contenu de son panier reste accessible sur l’appareil actuel à l’expiration de la session connectée. Une fois la session expirée, le panier du client est accessible à l’aide de la session de panier persistante. Si le même client se connecte sur un autre appareil ou navigateur et ajoute quelque chose à son panier, puis revient à l’appareil avec une session persistante active, son panier est mis à jour avec les articles ajoutés.

L’utilisation d’un panier persistant peut réduire le nombre de paniers abandonnés et augmenter les ventes. Le panier persistant **n’expose pas** les informations de compte sensibles à tout moment.

Pour gérer l’utilisation de la persistance du panier pour votre site ou dans des vues de magasin spécifiques, vous pouvez [configurer les paramètres de panier persistants](#configure-a-persistent-cart). Pour plus d’informations sur la manière dont ces paramètres affectent l’expérience client dans votre storefront, voir [Workflow de panier persistant](#persistent-cart-workflow).

>[!NOTE]
>
>La fonctionnalité de panier persistant est disponible uniquement pour les clients enregistrés et connectés. Les acheteurs invités ne peuvent pas utiliser la fonctionnalité de panier persistant.

## Workflow de panier persistant

Lorsque le panier persistant est [activé](#configure-a-persistent-cart), le workflow dépend des éléments suivants :

- Les valeurs des paramètres _[!UICONTROL Enable Remember Me]_&#x200B;et&#x200B;_[!UICONTROL Clear Persistence on Log Out]_
- Décision du client de cocher ou de décocher la case _[!UICONTROL Remember Me]_
- Lorsque le cookie persistant est effacé

Lorsque la session du client expire, un lien de `Not Jane Smith?` s’affiche dans l’en-tête de la page dans les conditions suivantes :
- le client connecté a sélectionné l’option _[!UICONTROL Remember Me]_&#x200B;et un cookie persistant est appliqué
- le client se déconnecte lorsque le système est configuré avec _[!UICONTROL Clear Persistence on Sign Out]_&#x200B;défini sur `No`.

Le système conserve un enregistrement du contenu du panier sur l’appareil actuel, même si la session connectée expire. Le lien `Not Jane Smith?` permet au client de mettre fin à la session persistante et de commencer à travailler en tant qu’invité ou de se connecter en tant que client différent ou identique.

Si le client a coché la case _[!UICONTROL Remember Me]_&#x200B;lors de la connexion, votre boutique crée et conserve un cookie persistant distinct. Ce cookie permet de garder le panier du client accessible même après la fermeture du navigateur ou l’accès à un autre site et l’expiration de la session connectée.

Si ce même client visite votre magasin à l’aide de plusieurs navigateurs lors de la connexion ou lorsqu’une session persistante est active, les modifications qu’il apporte au contenu du panier dans un navigateur sont répercutées dans les autres navigateurs lors de l’actualisation de la page.

>[!NOTE]
>
>Pour assurer la synchronisation du panier sur plusieurs appareils ou navigateurs, les clients doivent se connecter à chaque nouvel appareil qu’ils utilisent pour faire des achats. Pour les clients connectés, le contenu du panier est synchronisé sur plusieurs appareils et navigateurs à condition qu’ils soient connectés sous le même compte, quelle que soit la configuration du panier persistant.

### Comportement de la case à cocher « Se souvenir de moi »

Les clients peuvent cocher la case _[!UICONTROL Remember Me]_&#x200B;sur la page de connexion, la fenêtre contextuelle d’authentification, les connexions à la caisse ou lors de la création d’un compte pour que le contenu du panier reste accessible sur l’appareil actuel à l’expiration de la session connectée.

| Vous Vous Souvenez De Moi ? | Résultat |
| ------------ |  ------ |
| Sélectionné | Crée un cookie persistant et conserve le contenu du panier accessible sur l’appareil actuel à l’expiration de la session de connexion du client. |
| Non sélectionné | Ne crée pas de cookie persistant et ne conserve pas le contenu du panier accessible sur l’appareil actuel à l’expiration de la session de connexion. Notez que le contenu du panier est toujours enregistré dans le compte du client et rechargé la prochaine fois que le client se connecte. |

{style="table-layout:auto"}

![Mémoriser mes identifiants de client](./assets/remember-me-customer-login.png){width="600" zoomable="yes"}
![Pop-up Mémoriser mon authentification](./assets/remember-me-authentication-pop-up.png){width="600" zoomable="yes"}
![Mémoriser mes connexions à Checkout](./assets/remember-me-checkout-sign-ins.png){width="600" zoomable="yes"}

### Effacer la persistance sur le comportement de déconnexion

Lorsque le client se connecte ou s’enregistre avec l’option _Mémoriser mon nom_ sélectionnée, la configuration de l’option _Effacer la persistance lors de la déconnexion_ détermine le comportement du panier persistant.

|  | Effacer la persistance lors de la déconnexion définie sur Oui | Effacer la persistance lors de la déconnexion définie sur Non |
| ------ | ------ | ------ |
| _Mémorisé_ le client se déconnecte | Supprime les cookies de session et persistants afin que le contenu du panier disparaisse sur l’appareil actuel jusqu’à ce que le même client se reconnecte. | Supprime le cookie de session, mais le cookie persistant reste en vigueur. Le contenu du panier reste accessible sur l’appareil actuel. |
| _En mémoire_ le client ne se déconnecte pas mais le cookie de session expire | Le cookie persistant reste en vigueur et le contenu du panier est accessible à partir de l’appareil actuel. | Le cookie persistant reste en vigueur et le contenu du panier est accessible à partir de l’appareil actuel. |

### Exemple de session ouverte sur un ordinateur partagé

Jane termine ses achats de vacances en tant que cliente _mémorisée_ connectée. Elle ajoute un cadeau pour John à son panier, et quelque chose pour sa mère. Ensuite, elle va à la cuisine pour une collation et sa session de connexion expire.

John s&#39;assoit à l&#39;ordinateur pour faire quelques achats rapides pendant que Jane est dans la cuisine. Sans remarquer le lien `Not Jane Smith?` en haut de la page, John trouve un joli cadeau pour Jane et l&#39;ajoute au panier. Lorsqu’il quitte l’hôtel, il constate que les adresses d’expédition et de facturation sont préremplies et pense qu’il est connecté. John est tellement pressé qu&#39;il ne remarque pas les articles supplémentaires pendant _Révision de l&#39;ordre_ et soumet l&#39;ordre. Le panier de Jane est maintenant vide, et John a acheté tous les cadeaux.

## Configuration d’un panier persistant

Lors de la configuration d’un panier persistant, vous pouvez spécifier la durée de vie des cookies et les options que vous souhaitez rendre disponibles pour diverses activités client.

Pour utiliser le panier persistant, le navigateur du client doit être défini sur autoriser les cookies. Deux types de cookies sont utilisés pour les opérations liées au panier :

- **Cookie de session** - Un cookie de session à court terme existe lors d’une seule visite sur votre site. Ce cookie expire lorsque le client se déconnecte ou lorsque la session expire.

- **Cookie persistant** - Un cookie persistant à long terme continue d’exister après la fin de la session connectée. Ce cookie permet de s’assurer que le contenu du panier d’un client reste accessible lorsque ce dernier se déconnecte ou que la session expire.

Pour plus d’informations sur l’impact de ces paramètres de configuration sur le workflow client, voir [Workflow de panier persistant](#persistent-cart-workflow).

{{$include /help/_includes/persistent-cart-configuration.md}}

<!-- Last updated from includes: 2024-10-31 10:02:14 -->
