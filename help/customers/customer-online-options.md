---
title: Durée de la session client
description: La durée de vie de la session client détermine la durée de vie d’une session d’achat client.
exl-id: 7180631a-3233-40f3-92bf-b329fc260cf9
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Durée de la session client

La durée de vie d’une session d’achat client est déterminée par plusieurs facteurs, notamment la durée de la session du serveur, l’utilisation d’un [panier persistant](../stores-purchase/cart-persistent.md) et la durée de vie des informations stockées dans le navigateur. Bien qu’elles soient liées à la même expérience client, il s’agit de processus distincts avec des événements d’expiration et des durées de vie différents.

| Processus | Description |
| --- | --- |
| Session | Informations stockées sur le serveur, telles que le contenu du panier. Si la session du serveur expire avant l’expiration du cookie, les clients risquent de perdre le contenu du panier et de réduire les risques de sécurité. |
| Cookie de session | Informations stockées dans le navigateur sous la forme d’un nombre ou d’une chaîne de caractères. Si le cookie de session expire avant la session du serveur, le client est déconnecté. Le cookie de session est supprimé lorsque le client ferme la fenêtre du navigateur. Par défaut, la durée de vie du cookie est définie sur 3 600 secondes, ou une heure. S’il n’y a pas d’activité clavier pendant cette période, la session en cours se termine et les clients doivent se reconnecter à leurs comptes pour continuer à effectuer des achats. |

{style="table-layout:auto"}

Si [Panier persistant](../stores-purchase/cart-persistent.md) est activé, le contenu du panier est enregistré pour la prochaine fois que les clients se connectent à leurs comptes. Lors de l’utilisation d’un panier persistant, il est recommandé de définir la durée de vie de la session du serveur et du cookie de session sur une longue période.

Sur le serveur, la durée de la session est contrôlée par le fichier `php.ini` et plusieurs variables. Actuellement, Adobe Commerce ne dispose pas d’un paramètre de configuration Administrateur contrôlant la durée de la session du serveur.

## Configuration de la durée de vie du cookie

1. Sur la barre latérale _Admin_, accédez à [!UICONTROL **Magasins**] > _[!UICONTROL Settings]_>[!UICONTROL **Configuration**].

1. Si vous disposez de plusieurs magasins, définissez le programme de sélection **[!UICONTROL Store View]** dans le coin supérieur droit sur le magasin où s’applique la configuration.

1. Dans le panneau de gauche sous **[!UICONTROL General]**, choisissez **[!UICONTROL Web]**.

1. Développez la section **[!UICONTROL Default Cookie Settings]** .

   ![Paramètres du cookie par défaut](../configuration-reference/general/assets/web-default-cookie-settings.png){width="600" zoomable="yes"}

1. Pour modifier la valeur par défaut, décochez la case **[!UICONTROL Use system value]** et saisissez la nouvelle valeur en secondes.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.

## Configurer la fonctionnalité _Mémoriser_

Pour faciliter la connexion, la fonction **[!UICONTROL Remember Me]** permet aux titulaires de compte d’utilisateur d’éviter de saisir leurs informations d’identification chaque fois qu’ils entrent dans le storefront. Pour des raisons de sécurité, la fonction de persistance est désactivée par défaut.

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Persistent Shopping Cart]**.

1. Développez la section **[!UICONTROL General Options]** .

1. Pour **[!UICONTROL Enable Persistence]**, définissez sur `Yes`. (Décochez la case **[!UICONTROL Use system value]** pour permettre de modifier le paramètre par défaut.)

1. Pour **[!UICONTROL Enable "Remember Me"]**, définissez sur `Yes` ou `No` en fonction de vos besoins.

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Save Config]**.
