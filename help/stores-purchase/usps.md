---
title: Service postal des États-Unis (USPS)
description: Découvrez comment configurer USPS en tant que transporteur pour votre boutique.
exl-id: c9601fb8-f0f9-484a-a2e1-d50ee0f2dbf0
feature: Shipping/Delivery
source-git-commit: d5beff4d450dab21f74e5baec6b718b844963858
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 0%

---

# Service postal des États-Unis (USPS)

Le United States Postal Service est le service postal indépendant du gouvernement des États-Unis, qui offre des services de transport intérieur et international par voie terrestre et aérienne.

## Étape 1 : Ouvrir un compte d&#39;expédition USPS

Ouvrez un compte [USPS Web Tools][1]. Une fois le processus d&#39;enregistrement terminé, vous recevrez votre identifiant utilisateur et une URL vers le serveur de test USPS.

Vous pouvez également ouvrir un compte [USPS Web Tools][1]. Une fois le processus d&#39;enregistrement terminé, vous recevrez votre identifiant utilisateur et une URL vers le serveur de test USPS. Pour en savoir plus sur les outils Web USPS, consultez leur [documentation technique][2].

## Étape 2 : activer USPS pour votre magasin

{{$include /help/_includes/usps-api-type-configuration-note.md}}

1. Dans la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Delivery Methods]**.

1. Développez ![Sélecteur d’extension](../assets/icon-display-expand.png) la section **[!UICONTROL USPS]** .

   >[!NOTE]
   >
   >Si nécessaire, décochez d’abord la case **[!UICONTROL Use system value]** pour modifier les paramètres suivants comme décrit.

1. Définissez **[!UICONTROL Enabled for Checkout]** sur `Yes`.

1. Définissez **[!UICONTROL USPS Type]** sur `USPS Rest APIs` si vous utilisez l’API REST USPS.

   Si vous utilisez l&#39;API Web Tools d&#39;USPS, définissez **[!UICONTROL USPS Type]** sur `USPS Web Tools API`.

1. Si nécessaire, saisissez le **[!UICONTROL Gateway URL]** pour accéder aux tarifs d&#39;expédition USPS.

   Le champ est prédéfini par défaut et n’a normalement pas besoin d’être modifié.

1. Saisissez un **[!UICONTROL Title]** pour ce mode d&#39;expédition qui s&#39;affiche lors du passage en caisse.

1. Utilisez les informations d&#39;identification fournies par USPS pour remplir les champs suivants :

   Si vous utilisez les API REST USPS, vous devez fournir les informations d’identification suivantes :

   - **[!UICONTROL Consumer Key]**
   - **[!UICONTROL Consumer Secret]**
   - **[!UICONTROL Pricing Options]**

   Si vous utilisez l&#39;API Web Tools d&#39;USPS, vous devez fournir les informations d&#39;identification suivantes :

   - **[!UICONTROL User ID]**
   - **[!UICONTROL Password]**

1. Définissez **[!UICONTROL Mode]** sur l’une des options suivantes :

   - `Development` - Exécute USPS dans un environnement de test. Après avoir exécuté USPS dans un environnement de développement, assurez-vous de revenir ultérieurement et de définir le mode sur `Live`.
   - `Live` - Exécute USPS dans un environnement de production actif.

## Étape 3 : Compléter la description de l&#39;emballage

1. Pour déterminer comment la commande est gérée si elle est envoyée sous la forme de plusieurs packages, définissez **[!UICONTROL Packages Request Type]** sur l’une des options suivantes :

   - `Divide to Equal Weight` - (Une demande) L&#39;expédition de plusieurs colis peut être soumise en une seule demande si les colis sont divisés par un poids égal.
   - `Use Origin Weight` - (Demandes multiples) Plusieurs colis doivent être soumis en tant que demandes distinctes si le poids d&#39;origine est utilisé comme base de calcul des frais d&#39;expédition.

1. Définissez **[!UICONTROL Container]** sur le type d’emballage normalement utilisé pour expédier les produits commandés pour votre magasin.

1. Définissez la **[!UICONTROL Size]** du package type expédié à partir de votre magasin.

1. Définissez **[!UICONTROL Machinable]** sur l’une des options suivantes :

   - `Yes` - Si votre package type peut être traité par une machine.
   - `No` - Si votre package type doit être traité manuellement.

1. Saisissez le **[!UICONTROL Maximum Package Weight]** en fonction des exigences de l’opérateur.

   ![Paramètres d&#39;emballage USPS](../configuration-reference/sales/assets/delivery-methods-usps-packaging.png){width="600" zoomable="yes"}

## Étape 4 : Configurer les frais de gestion

Les frais de manutention sont facultatifs et apparaissent comme des frais supplémentaires qui sont ajoutés aux frais d&#39;expédition DHL. Si vous souhaitez inclure des frais de manutention, procédez comme suit :

1. Définissez **[!UICONTROL Calculate Handling Fee]** l’une des méthodes suivantes :

   - `Fixed`
   - `Percent`

1. Pour déterminer comment les frais de gestion sont appliqués, définissez **[!UICONTROL Handling Applied]** sur l’une des options suivantes :

   - `Per Order`
   - `Per Package`

1. Saisissez le montant de la **[!UICONTROL Handling Fee]** à facturer.

   Pour saisir un pourcentage, utilisez le format décimal. Par exemple, saisissez `0.25` pour 25 %.

   ![Frais de gestion USPS](../configuration-reference/sales/assets/delivery-methods-usps-handling-fee.png){width="600" zoomable="yes"}

## Étape 5 : spécifier les méthodes autorisées et les pays applicables

1. Par **[!UICONTROL Allowed Methods]**, choisissez chaque méthode d&#39;expédition USPS disponible pour vos clients.

   Les méthodes s’affichent sous USPS lors du passage en caisse. Pour sélectionner plusieurs méthodes, maintenez la touche Ctrl (PC) ou Commande (Mac) enfoncée et cliquez sur chaque option.

1. Si vous souhaitez fournir une option [Livraison gratuite](shipping-free.md) via USPS, définissez les options de livraison gratuite :

   - Définissez **[!UICONTROL Free Method]** sur la méthode que vous souhaitez utiliser pour la livraison gratuite. Si vous ne voulez pas offrir la livraison gratuite par USPS, choisissez `None`.

   - Pour exiger un montant de commande minimum qui qualifie une commande pour une livraison gratuite avec USPS, définissez **[!UICONTROL Enable Free Shipping Threshold]** sur `Enable`. Saisissez ensuite la valeur minimale en **[!UICONTROL Free Shipping Amount Threshold]**.

1. Si nécessaire, modifiez la **[!UICONTROL Displayed Error Message]**.

   Cette zone de texte est prédéfinie avec un message par défaut, mais vous pouvez saisir un message différent que vous souhaitez afficher si USPS n&#39;est plus disponible.

   ![&#x200B; Méthodes autorisées USPS &#x200B;](../configuration-reference/sales/assets/delivery-methods-usps-allowed-methods.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Ship to Applicable Countries]** sur l’une des options suivantes :

   - `All Allowed Countries` - Les clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiés dans la configuration de votre boutique peuvent utiliser cette méthode de diffusion.
   - `Specific Countries` - Lorsque vous sélectionnez cette option, la liste _Livrer à des pays spécifiques_ s&#39;affiche. Sélectionnez dans la liste chaque pays où ce mode de diffusion peut être utilisé.

   ![Pays applicables USPS](../configuration-reference/sales/assets/delivery-methods-usps-countries.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Show Method if Not Applicable]** sur l’une des options suivantes :

   - `Yes` - Répertorie tous les modes d&#39;expédition USPS disponibles lors du passage en caisse, y compris les modes qui ne s&#39;appliquent pas à l&#39;expédition.
   - `No` - Répertorie uniquement les méthodes d&#39;expédition USPS applicables à l&#39;expédition.

1. Pour créer un fichier journal contenant les détails des expéditions USPS effectuées à partir de votre magasin, définissez **[!UICONTROL Debug]** sur `Yes`.

1. Par **[!UICONTROL Sort Order]**, saisissez un nombre pour déterminer l&#39;ordre dans lequel USPS apparaît lorsqu&#39;il est répertorié avec d&#39;autres méthodes de diffusion lors du passage en caisse.

   `0` = premier, `1` = deuxième, `2` = troisième, etc.

1. Cliquez sur **[!UICONTROL Save Config]**.

[1]: https://secure.shippingapis.com/registration/
[2]: https://www.usps.com/business/web-tools-apis/welcome.htm
