---
title: FedEx
description: Découvrez comment configurer FedEx en tant qu’opérateur de transport pour votre magasin.
exl-id: 75bb3ed1-3ae9-418a-be90-888046b28a7b
feature: Shipping/Delivery
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 0%

---

# FedEx

FedEx est l&#39;une des plus grandes entreprises de services de transport maritime au monde, fournissant des services de transport aérien, de fret et de transport terrestre avec plusieurs niveaux de priorités.

![Options d’expédition FedEx lors du passage en caisse](./assets/storefront-checkout-shipping-fedex.png){width="700" zoomable="yes"}

>[!NOTE]
>
>FedEx peut utiliser le [poids dimensionnel](carriers.md#dimensional-weight) pour déterminer certains tarifs de livraison. Toutefois, Adobe Commerce et Magento Open Source ne prennent en charge que le calcul des coûts d’expédition en fonction du poids.

## Étape 1 : inscription à la production des services web FedEx

Un compte marchand FedEx et un enregistrement pour l’accès en production des services web FedEx sont requis. Après avoir créé un compte FedEx, consultez la page d’informations du compte de production, puis cliquez sur le lien _Obtenir la clé de production_ au bas de la page pour vous enregistrer et obtenir une clé.

>[!NOTE]
>
>Veillez à copier ou à écrire la clé d’authentification. Il est nécessaire de configurer FedEx dans vos paramètres d’expédition Commerce.

## Étape 2 : activation de FedEx pour votre magasin

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Delivery Methods]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL FedEx]** .

1. Définissez **[!UICONTROL Enabled for Checkout]** sur `Yes`.

1. Pour **[!UICONTROL Title]**, saisissez un titre qui identifie la méthode d’expédition FedEx lors du passage en caisse.

1. Renseignez les informations suivantes de votre compte FedEx :

   - **[!UICONTROL Account ID]**
   - **[!UICONTROL Api Key]**
   - **[!UICONTROL Secret Key]**

1. Si vous avez configuré un environnement de test FedEx et souhaitez travailler dans l’environnement de test, définissez **[!UICONTROL Sandbox Mode]** sur `Yes`.

   >[!NOTE]
   >
   >N’oubliez pas de définir le mode sandbox sur `No` lorsque vous êtes prêt à offrir FedEx comme méthode de livraison à vos clients.

   ![Paramètres du compte FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

## Étape 3 : description du package et frais de gestion

1. Définissez **[!UICONTROL Pickup Type]** sur la méthode de récupération utilisée pour les envois.

   - `DropOff at Fedex Location` - (Par défaut) Indique que vous déposez des envois à votre station FedEx locale.
   - `Contact Fedex to Schedule` - Indique que vous contactez FedEx pour demander une récupération.
   - `Use Scheduled Pickup` - Indique que l’expédition est ramassée dans le cadre d’une récupération planifiée régulière.
   - `On Call` - Indique que la reprise est planifiée en appelant FedEx.
   - `Package Return Program` - Indique que l’expédition est ramassée par le programme FedEx Ground Package Retours.
   - `Regular Stop` - Indique que l’expédition est ramassée selon le calendrier de récupération normal.
   - `Tag` - Indique que la récupération de l’expédition est spécifique à une demande de récupération de balise express ou d’appel au sol. Cela ne s’applique qu’à une étiquette d’expédition de retour.

1. Pour **[!UICONTROL Packages Request Type]**, sélectionnez le type de requête qui décrit le mieux votre préférence lors de la division d’une commande en plusieurs envois :

   - `Divide to equal weight (one request)`
   - `Use origin weight (few requests)`

1. Pour **[!UICONTROL Packaging]**, sélectionnez le type de package FedEx que vous utilisez généralement pour envoyer des produits de votre magasin.

1. Définissez **[!UICONTROL Weight Unit]** sur l’unité de mesure utilisée dans vos paramètres régionaux.

   - `Pounds`
   - `Kilograms`

1. Saisissez le **[!UICONTROL Maximum Package Weight]** autorisé pour les envois FedEx.

   Le poids maximal par défaut de FedEx est de 150 livres. Pour plus d’informations, consultez votre opérateur de livraison. La valeur par défaut est recommandée, sauf si vous avez pris des dispositions spéciales avec FedEx. Voir [Poids dimensionnel](carriers.md#dimensional-weight) pour plus d’informations.

   ![Paramètres du package FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

1. Configurez les options de frais de gestion en fonction de vos besoins.

   Les frais de gestion sont facultatifs et ne sont pas visibles lors de l’extraction. Si vous souhaitez inclure des frais de traitement, procédez comme suit :

   - Définissez **[!UICONTROL Calculate Handling Fee]** :

      - `Fixed Fee`
      - `Percentage`

   - Pour **[!UICONTROL Handling Applied]**, choisissez l’une des méthodes suivantes pour gérer les frais de gestion :

      - `Per Order`
      - `Per Package`

   - Saisissez le **[!UICONTROL Handling Fee]** comme montant `fixed` ou `percentage`, selon la méthode de calcul.

1. Définissez **[!UICONTROL Residential Delivery]** sur l’une des valeurs suivantes, selon que vous vendez Entreprise à consommateur (B2C) ou Entreprise à entreprise (B2B).

   - `Yes` - Pour les diffusions résidentielles B2C.
   - `No` - Pour les diffusions résidentielles B2B.

   ![Paramètres de frais de gestion FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

## Étape 4 : Méthodes autorisées et pays applicables

1. Définissez **[!UICONTROL Allowed Methods]** sur chaque méthode d’expédition que vous souhaitez proposer.

   Lorsque vous choisissez des méthodes, tenez compte de votre compte FedEx, de la fréquence et de la taille de vos envois, et si vous autorisez les envois internationaux. Vous pouvez proposer autant de méthodes que vous le souhaitez, par exemple :

   - La première priorité de l&#39;Europe
   - Options de jour de remise : 1 jour de transport, 2 jours de transport, 2 jours, 2 jours, 2 jours, 3 jours de transport
   - Options intérieures - Express Saver, Ground, First, Overnight, Home Delivery, Standard Overnight
   - Options internationales : économie internationale, transport de l&#39;économie internationale, première internationale, sol international, international, priorité internationale
   - Options de priorité - Fret, priorité nocturne
   - Publication dynamique - Si vous proposez la méthode de publication dynamique (saisissez l’ **identifiant Hub**)
   - Options de transport - Freight, National Freight

1. Si vous souhaitez fournir une option de [livraison gratuite](shipping-free.md) via FedEx, définissez les options de livraison gratuite.

   - Définissez **[!UICONTROL Free Method]** sur la méthode que vous souhaitez utiliser pour la livraison gratuite. Si vous ne souhaitez pas proposer de livraison gratuite via FedEx, choisissez `None`.

   - Pour exiger un montant minimum de commande qui qualifie une commande de livraison gratuite avec FedEx, définissez **[!UICONTROL Enable Free Shipping Threshold]** sur `Enable`. Ensuite, saisissez la valeur minimale dans **[!UICONTROL Free Shipping Amount Threshold]**.

   Ce paramètre est similaire à celui de la méthode d’expédition gratuite standard, mais il apparaît dans la section FedEx lors du passage en caisse, de sorte que les clients savent quelle méthode est utilisée pour leur commande.

1. Si nécessaire, modifiez le **[!UICONTROL Displayed Error Message]**.

   Cette zone de texte est prédéfinie avec un message par défaut, mais vous pouvez saisir un autre message que vous souhaitez afficher si FedEx devient indisponible.

   ![Méthodes de remise FedEx autorisées](../configuration-reference/sales/assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

1. Définissez **[!UICONTROL Ship to Applicable Countries]** :

   - `All Allowed Countries` - Les clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiés dans votre configuration de magasin peuvent utiliser cette méthode de diffusion.

   - `Specific Countries` - Lorsque vous sélectionnez cette option, la liste _Ship to Specific Countries_ s’affiche. Sélectionnez chaque pays de la liste dans lequel ce mode de diffusion peut être utilisé.

1. Si vous souhaitez conserver un journal de toutes les communications entre votre magasin et le système FedEx, définissez **[!UICONTROL Debug]** sur `Yes`.

1. Définissez **[!UICONTROL Show Method if Not Applicable]** :

   - `Yes` - Affiche toutes les méthodes de livraison FedEx aux clients, quelle que soit leur disponibilité.
   - `No` - Affiche uniquement les méthodes de livraison FedEx qui s’appliquent à la commande.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer la séquence dans laquelle FedEx apparaît lorsqu’il est répertorié avec d’autres méthodes de remise lors du passage en caisse.

   `0` = premier, `1` = second, `2` = troisième, etc.

1. Cliquez sur **[!UICONTROL Save Config]**.

   ![Pays applicables FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Commerce déclare toujours le prix complet de la commande à FedEx lors du calcul des frais de livraison. Ce comportement ne peut pas être modifié.
