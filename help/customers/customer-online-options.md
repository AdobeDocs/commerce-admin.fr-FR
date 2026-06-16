---
title: Durée de vie de la session client
description: La durée de vie de la session client détermine la durée de vie d’une session d’achats client.
exl-id: 7180631a-3233-40f3-92bf-b329fc260cf9
feature: Customers, Configuration, Security
TQID: https://experienceleague.adobe.com/cJ8Rv5zMkTvZMfrl-nj-3xy3guSPDlxa7HZ-ZG7kLFw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 403
ht-degree: 0%

---

# Durée de vie de la session client

La durée de vie d’une session d’achat client est déterminée par plusieurs facteurs, notamment la durée de la session du serveur, l’utilisation d’un [panier persistant](../stores-purchase/cart-persistent.md) et la durée de vie des informations stockées dans le navigateur. Bien qu’ils soient liés à la même expérience client, il s’agit de processus distincts avec des événements d’expiration et des durées de vie différents.

| Processus | Description |
| --- | --- |
| Session | Informations stockées sur le serveur, telles que le contenu du panier. Si la session du serveur expire avant l’expiration du cookie, les clients peuvent perdre le contenu du panier et réduire les risques de sécurité. |
| Cookie de session | Informations stockées dans le navigateur sous la forme d’un nombre ou d’une chaîne de caractères. Si le cookie de session expire avant la session du serveur, le client est déconnecté. Le cookie de session est supprimé lorsque le client ferme la fenêtre du navigateur. Par défaut, la durée de vie des cookies est définie sur 3 600 secondes, soit une heure. S’il n’y a aucune activité de clavier pendant cette période, la session en cours se termine et les clients doivent se reconnecter à leurs comptes pour continuer leurs achats. |

{style="table-layout:auto"}

Si le [panier persistant](../stores-purchase/cart-persistent.md) est activé, le contenu du panier est enregistré pour la prochaine connexion des clients à leurs comptes. Lors de l’utilisation d’un panier persistant, il est recommandé de définir la durée de vie de la session du serveur et du cookie de session sur une longue période.

Sur le serveur, la durée de la session est contrôlée par le fichier `php.ini` et plusieurs variables. Actuellement, Adobe Commerce ne dispose pas d’un paramètre de configuration d’administration qui contrôle la durée de la session du serveur.

## Configuration de la durée de vie des cookies

1. Dans la barre latérale _Admin_, accédez à [!UICONTROL **Magasins**] > _[!UICONTROL Settings]_>[!UICONTROL **Configuration**].

1. Si vous disposez de plusieurs magasins, définissez le sélecteur de **[!UICONTROL Store View]** dans le coin supérieur droit du magasin auquel s’applique la configuration.

1. Dans le panneau de gauche sous **[!UICONTROL General]**, choisissez **[!UICONTROL Web]**.

1. Développez la section **[!UICONTROL Default Cookie Settings]** .

   ![Paramètres de cookie par défaut](../configuration-reference/general/assets/web-default-cookie-settings.png){width="600" zoomable="yes"}

1. Pour modifier la valeur par défaut, décochez la case **[!UICONTROL Use system value]** et saisissez la nouvelle valeur en secondes.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.

## Configuration de la fonctionnalité _Mémoriser mon_

Pour faciliter la connexion, la fonction **[!UICONTROL Remember Me]** permet aux titulaires de compte utilisateur d’éviter de saisir leurs informations d’identification chaque fois qu’ils accèdent au storefront. Pour des raisons de sécurité, la fonction de persistance est désactivée par défaut.

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Customers]** et choisissez **[!UICONTROL Persistent Shopping Cart]**.

1. Développez la section **[!UICONTROL General Options]** .

1. Par **[!UICONTROL Enable Persistence]**, définissez sur `Yes`. (Désélectionnez la case **[!UICONTROL Use system value]** pour permettre de modifier le paramètre par défaut.)

1. Par **[!UICONTROL Enable "Remember Me"]**, définissez sur `Yes` ou `No` en fonction de vos besoins.

1. Cliquez ensuite sur **[!UICONTROL Save Config]**.
