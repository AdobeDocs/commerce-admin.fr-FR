---
title: Persistance du panier
description: Découvrez comment un panier persistant effectue le suivi des articles non achetés et enregistre les informations pour la prochaine visite du client.
exl-id: 95c336b3-77ac-4cf6-8fb5-23f4ac4b67d6
feature: Shopping Cart, Configuration
source-git-commit: 2bddf979333bdafbfb6b445140515942b1115eea
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 0%

---

# Persistance du panier

Un panier persistant enregistre une référence au compte du client sur l’appareil actuel, en veillant à ce que le contenu du panier reste accessible à l’expiration de la session connecté.

Si un client est _mémorisé_, le contenu de son panier reste accessible sur l’appareil actuel à l’expiration de la session de connexion. Une fois la session expirée, le panier du client est accessible à l’aide de la session de panier persistante. Si le même client se connecte à un autre appareil ou navigateur et ajoute quelque chose à son panier, puis revient sur le périphérique avec une session persistante active, son panier est mis à jour avec les éléments ajoutés.

L’utilisation d’un panier persistant peut réduire le nombre de paniers abandonnés et augmenter les ventes. Le panier persistant **n’expose pas** les informations de compte sensibles à tout moment.

Pour gérer l’utilisation de la persistance du panier pour votre site ou dans des vues de magasin spécifiques, vous pouvez [configurer les paramètres du panier persistant](#configure-a-persistent-cart). Pour plus d’informations sur la façon dont ces paramètres affectent l’expérience du nouvel acheteur dans votre vitrine, voir [Workflow du panier persistant](#persistent-cart-workflow).

>[!NOTE]
>
>La fonctionnalité de panier persistant est disponible uniquement pour les clients enregistrés et connectés. Les acheteurs invités ne peuvent pas utiliser la fonction Panier persistant.

## Workflow de panier persistant

Lorsque le panier persistant est [activé](#configure-a-persistent-cart), le workflow dépend des éléments suivants :

- Les valeurs des paramètres _[!UICONTROL Enable Remember Me]_et_[!UICONTROL Clear Persistence on Log Out]_
- La décision du client de cocher ou de décocher la case _[!UICONTROL Remember Me]_
- Lorsque le cookie persistant est effacé

À l’expiration de la session client, un lien `Not Jane Smith?` s’affiche dans l’en-tête de la page sous les conditions suivantes :
- le client connecté a sélectionné l’option _[!UICONTROL Remember Me]_et un cookie persistant est appliqué.
- le client se déconnecte lorsque le système est configuré avec _[!UICONTROL Clear Persistence on Sign Out]_défini sur `No`.

Le système conserve un enregistrement du contenu du panier sur l’appareil actuel, même si la session de connexion expire. Le lien `Not Jane Smith?` permet au client de mettre fin à la session persistante et de commencer à travailler en tant qu’invité, ou de se connecter en tant qu’autre client ou en tant que même client.

Si le client a coché la case _[!UICONTROL Remember Me]_lors de la connexion, votre boutique crée et conserve un cookie persistant distinct. Ce cookie permet de garder le panier du client accessible même après avoir fermé le navigateur ou accédé à un autre site et l’expiration de sa session de connexion.

Si ce même client visite votre boutique à l’aide de plusieurs navigateurs lorsqu’il est connecté ou lorsqu’une session persistante est active, les modifications apportées au contenu du panier par le client dans un navigateur sont répercutées dans d’autres navigateurs lors de l’actualisation de la page.

>[!NOTE]
>
>Pour garantir la synchronisation du panier sur plusieurs appareils ou navigateurs, les clients doivent se connecter à chaque nouvel appareil qu’ils utilisent pour leurs achats. Pour les clients connectés, le contenu du panier est synchronisé sur plusieurs appareils et navigateurs tant qu’ils sont connectés sous le même compte, quelle que soit la configuration du panier persistant.

### Comportement de la case à cocher &quot;Se souvenir de moi&quot;

Les clients peuvent cocher la case _[!UICONTROL Remember Me]_sur la page de connexion ou lors de la création d’un nouveau compte pour que le contenu du panier reste accessible sur l’appareil actif à l’expiration de la session de connexion.

| Vous Vous Souvenez De Moi ? | Résultat |
| ------------ |  ------ |
| Sélectionné | Crée un cookie persistant et permet de conserver le contenu du panier accessible sur l’appareil actif à l’expiration de la session de connexion client. |
| Non sélectionné | Ne crée pas de cookie persistant et ne conserve pas le contenu du panier accessible sur l’appareil actif à l’expiration de la session de connexion. Notez que le contenu du panier est toujours enregistré dans le compte du client et rechargé la prochaine fois que le client se connecte. |

{style="table-layout:auto"}

### Persistance claire du comportement de déconnexion

Lorsque le client se connecte ou s’enregistre avec l’option _Mémoriser_ sélectionnée, la configuration de l’option _Effacer la persistance de la connexion_ détermine le comportement du panier persistant.

|  | Effacer la persistance de la déconnexion en définissant sur Oui | Effacer la persistance de la déconnexion définie sur Non |
| ------ | ------ | ------ |
| _Remembered_ le client se déconnecte | Supprime les cookies de session et persistants de sorte que le contenu du panier disparaisse sur l’appareil actuel jusqu’à ce que le même client se reconnecte. | Supprime le cookie de session, mais le cookie persistant reste en vigueur. Le contenu du panier reste accessible sur l’appareil actuel. |
| _Remembered_ le client ne se déconnecte pas mais le cookie de session expire | Le cookie persistant reste en vigueur et le contenu du panier est accessible à partir de l’appareil actuel. | Le cookie persistant reste en vigueur et le contenu du panier est accessible à partir de l’appareil actuel. |

### Exemple de session ouverte sur un ordinateur partagé

Jane termine ses achats de vacances en tant que client connecté _mémembered_. Elle ajoute un cadeau pour John dans son panier, et quelque chose pour sa mère. Ensuite, elle va à la cuisine pour un en-cas et sa session de connexion expire.

John s&#39;assoit à l&#39;ordinateur pour faire des achats rapides pendant que Jane est dans la cuisine. Sans remarquer le lien `Not Jane Smith?` situé en haut de la page, John trouve un joli cadeau pour Jane et l’ajoute au panier. Lorsqu&#39;il passe en caisse, il remarque que les adresses d&#39;expédition et de facturation sont pré-renseignées et pense qu&#39;il est connecté. John est tellement pressé qu’il ne remarque pas les éléments supplémentaires pendant _Order Review_ et qu’il envoie la commande. Le chariot de Jane est maintenant vide, et John a acheté tous les cadeaux.

## Configurer un panier persistant

Lors de la configuration d’un panier persistant, vous pouvez spécifier la durée de vie des cookies et les options que vous souhaitez mettre à disposition pour diverses activités client.

Pour utiliser le panier persistant, le navigateur du client doit être défini pour autoriser les cookies. Deux types de cookies sont utilisés pour les opérations de panier :

- **Cookie de session** - Un cookie de session à court terme existe lors d’une seule visite sur votre site. Ce cookie expire lorsque le client se déconnecte ou lorsque la session expire.

- **Cookie persistant** - Un cookie persistant à long terme continue d’exister après la fin de la session de connexion. Ce cookie permet de s’assurer que le contenu du panier d’un client reste accessible lorsque le client se déconnecte ou que la session expire.

Pour plus d’informations sur l’impact de ces paramètres de configuration sur le processus client, voir [Processus du panier persistant](#persistent-cart-workflow).

{{$include /help/_includes/persistent-cart-configuration.md}}
