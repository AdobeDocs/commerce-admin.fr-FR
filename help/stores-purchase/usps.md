---
title: United States Postal Service (USPS)
description: Découvrez comment configurer USPS en tant qu’opérateur de livraison pour votre magasin.
exl-id: c9601fb8-f0f9-484a-a2e1-d50ee0f2dbf0
feature: Shipping/Delivery
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# United States Postal Service (USPS)

Le United States Postal Service (Service postal des États-Unis) est un service postal indépendant du gouvernement des États-Unis, qui propose des services de navigation intérieure et internationale par voie terrestre et aérienne.

## Étape 1 : ouverture d’un compte de livraison USPS

Ouvrez une [Outils Web USPS][1] compte . Une fois le processus d’enregistrement terminé, vous recevrez votre ID utilisateur et une URL vers le serveur de test USPS.

Vous pouvez également ouvrir une [Outils Web USPS][1] compte . Une fois le processus d’enregistrement terminé, vous recevrez votre ID utilisateur et une URL vers le serveur de test USPS. Pour en savoir plus sur les outils Web d’USPS, voir leur [Documentation technique][2].

## Étape 2 : Activation d’USPS pour votre magasin

{{beta2-updates}}

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Delivery Methods]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL USPS]** .

   >[!NOTE]
   >
   >Si nécessaire, désélectionnez tout d’abord l’option **[!UICONTROL Use system value]** pour modifier les paramètres suivants, comme décrit.

1. Définir **[!UICONTROL Enabled for Checkout]** to `Yes`.

1. Si nécessaire, saisissez la variable **[!UICONTROL Gateway URL]** pour accéder aux tarifs de livraison USPS.

   >[!IMPORTANT]
   >
   >À compter du 24 juin 2021, les outils Web d’USPS supprimeront la prise en charge de tous les points de terminaison HTTP non sécurisés. Après cette modification, toutes les API des outils Web demandent que sur un point de terminaison HTTP non sécurisé échouent. Assurez-vous que la variable **[!UICONTROL Gateway URL]** utilise le point d’entrée HTTPS sécurisé.

   Par défaut, le champ est prédéfini et n’a normalement pas besoin d’être modifié.

1. Saisissez un **[!UICONTROL Title]** pour cette méthode d’expédition qui s’affiche pendant le passage en caisse.

1. Saisissez le **[!UICONTROL User ID]** et **[!UICONTROL Password]** pour votre compte USPS.

1. Définir **[!UICONTROL Mode]** à l’une des options suivantes :

   - `Development` : exécute USPS dans un environnement de test. Après avoir exécuté USPS dans un environnement de développement, veillez à retourner ultérieurement et à définir le mode sur `Live`.
   - `Live` : exécute USPS dans un environnement de production en direct.

## Etape 3 : compléter la description du conditionnement

1. Pour déterminer comment la commande est gérée si elle est envoyée sous la forme de plusieurs packages, définissez **[!UICONTROL Packages Request Type]** à l’une des options suivantes :

   - `Divide to Equal Weight` - (Une demande) L’envoi de plusieurs packages peut être présenté comme une demande si les packages sont divisés en poids égal.
   - `Use Origin Weight` - (Plusieurs demandes) Plusieurs demandes doivent être envoyées en tant que demandes distinctes si vous utilisez le poids d’origine comme base de calcul des frais d’expédition.

1. Définir **[!UICONTROL Container]** au type d’emballage habituellement utilisé pour expédier les produits commandés pour votre magasin.

1. Définissez la variable **[!UICONTROL Size]** du package type fourni à partir de votre magasin.

1. Définir **[!UICONTROL Machinable]** à l’une des options suivantes :

   - `Yes` - Si votre package type peut être traité par une machine.
   - `No` - Si votre package type doit être traité manuellement.

1. Saisissez le **[!UICONTROL Maximum Package Weight]** selon les exigences de l’opérateur.

   ![Paramètres de package USPS](../configuration-reference/sales/assets/delivery-methods-usps-packaging.png){width="600" zoomable="yes"}

## Étape 4 : configuration des frais de gestion

Les frais de gestion sont facultatifs et s’affichent sous la forme de frais supplémentaires, ajoutés aux frais d’expédition DHL. Si vous souhaitez inclure des frais de traitement, procédez comme suit :

1. Définir **[!UICONTROL Calculate Handling Fee]** à l’une des méthodes suivantes :

   - `Fixed`
   - `Percent`

1. Pour déterminer la manière dont les frais de traitement sont appliqués, définissez **[!UICONTROL Handling Applied]** à l’une des options suivantes :

   - `Per Order`
   - `Per Package`

1. Saisissez le montant de la variable **[!UICONTROL Handling Fee]** à charger.

   Pour saisir un pourcentage, utilisez le format décimal . Par exemple, saisissez `0.25` pour 25 %.

   ![Frais de gestion USPS](../configuration-reference/sales/assets/delivery-methods-usps-handling-fee.png){width="600" zoomable="yes"}

## Étape 5 : spécification des méthodes autorisées et des pays applicables

1. Pour **[!UICONTROL Allowed Methods]**, choisissez chaque méthode d’expédition USPS à la disposition de vos clients.

   Les méthodes apparaissent sous USPS lors du passage en caisse. Pour sélectionner plusieurs méthodes, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

1. Si vous souhaitez fournir une [Livraison gratuite](shipping-free.md) via USPS, définissez les options d’expédition gratuites :

   - Définir **[!UICONTROL Free Method]** à la méthode que vous souhaitez utiliser pour la livraison gratuite. Si vous ne souhaitez pas proposer de livraison gratuite via USPS, choisissez `None`.

   - Pour exiger un montant minimum de commande qui qualifie une commande d’expédition gratuite avec USPS, définissez **[!UICONTROL Enable Free Shipping Threshold]** to `Enable`. Ensuite, saisissez la valeur minimale de **[!UICONTROL Free Shipping Amount Threshold]**.

1. Si nécessaire, modifiez la variable **[!UICONTROL Displayed Error Message]**.

   Cette zone de texte est prédéfinie avec un message par défaut, mais vous pouvez saisir un autre message que vous souhaitez afficher si USPS devient indisponible.

   ![Méthodes USPS autorisées](../configuration-reference/sales/assets/delivery-methods-usps-allowed-methods.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Ship to Applicable Countries]** à l’une des options suivantes :

   - `All Allowed Countries` - Clients de tous les [pays](../getting-started/store-details.md#country-options) spécifié dans votre configuration de magasin peut utiliser cette méthode de diffusion.
   - `Specific Countries` - Lorsque vous sélectionnez cette option, la variable _Ship to Specific Countries_ s’affiche. Sélectionnez chaque pays de la liste dans lequel ce mode de diffusion peut être utilisé.

   ![USPS Applicable Countries](../configuration-reference/sales/assets/delivery-methods-usps-countries.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Show Method if Not Applicable]** à l’une des options suivantes :

   - `Yes` - Répertorie toutes les méthodes d’expédition USPS disponibles lors du passage en caisse, y compris les méthodes qui ne s’appliquent pas à l’expédition.
   - `No` - Répertorie uniquement les méthodes d’expédition USPS applicables à l’expédition.

1. Pour créer un fichier journal contenant les détails des envois USPS effectués depuis votre magasin, définissez **[!UICONTROL Debug]** to `Yes`.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre dans lequel USPS apparaît lorsqu’il est répertorié avec d’autres méthodes de remise lors du passage en caisse.

   `0` = first, `1` = second, `2` = troisième, etc.

1. Cliquez sur **[!UICONTROL Save Config]**.


[1]: https://secure.shippingapis.com/registration/
[2]: https://www.usps.com/business/web-tools-apis/welcome.htm
