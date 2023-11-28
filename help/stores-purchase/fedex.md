---
title: FedEx
description: Découvrez comment configurer FedEx en tant qu’opérateur de transport pour votre magasin.
exl-id: 75bb3ed1-3ae9-418a-be90-888046b28a7b
feature: Shipping/Delivery
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---

# FedEx

FedEx est l&#39;une des plus grandes entreprises de services de transport maritime au monde, fournissant des services de transport aérien, de fret et de transport terrestre avec plusieurs niveaux de priorités.

![Options d’expédition FedEx lors du passage en caisse](./assets/storefront-checkout-shipping-fedex.png){width="700" zoomable="yes"}

>[!NOTE]
>
>FedEx peut utiliser [poids dimensionnel](carriers.md#dimensional-weight) pour déterminer certains tarifs d’expédition. Toutefois, Adobe Commerce et Magento Open Source ne prennent en charge que le calcul des coûts d’expédition en fonction du poids.

## Étape 1 : inscription à la production des services web FedEx

A [Compte marchand FedEx][1] et l’enregistrement pour l’accès à la production des services web FedEx est requis. Après avoir créé un compte FedEx, accédez à la page d’informations du compte de production, puis cliquez sur le _Obtention de la clé de production_ lien au bas de la page pour vous enregistrer et obtenir une clé.

>[!NOTE]
>
>Veillez à copier ou à écrire la clé d’authentification. Il est nécessaire de configurer FedEx dans vos paramètres d’expédition Commerce.

## Étape 2 : activation de FedEx pour votre magasin

{{beta2-updates}}

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Delivery Methods]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL FedEx]** .

1. Définir **[!UICONTROL Enabled for Checkout]** to `Yes`.

1. Pour **[!UICONTROL Title]**, saisissez un titre qui identifie la méthode d’expédition FedEx lors du passage en caisse.

1. Renseignez les informations suivantes de votre compte FedEx :

   - **[!UICONTROL Account ID]**
   - **[!UICONTROL Meter Number]**
   - **[!UICONTROL Key]**
   - **[!UICONTROL Password]**

1. Si vous avez configuré un environnement de test FedEx et souhaitez travailler dans l’environnement de test, définissez **[!UICONTROL Sandbox Mode]** to `Yes`.

   >[!NOTE]
   >
   >N’oubliez pas de définir le mode Sandbox sur . `No` lorsque vous êtes prêt à proposer FedEx comme méthode d’expédition à vos clients.

   ![Paramètres du compte FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

## Étape 3 : description du package et frais de gestion

1. Sélectionnez la variable **[!UICONTROL Packages Request Type]** à l’option qui décrit le mieux votre choix lors de la division d’une commande en plusieurs envois :

   - `Divide to equal weight (one request)`
   - `Use origin weight (few requests)`

1. Sélectionnez le type de **[!UICONTROL Packaging]** généralement utilisé pour envoyer des produits de votre magasin.

1. Définir **[!UICONTROL Dropoff]** à la méthode de prise en charge utilisée pour la diffusion.

   - `Regular Pickup` - Si vous avez un volume élevé d&#39;envois, il peut être rentable de conclure des accords avec FedEx pour des récupérations régulières.

   - `Request Courier` - Vous devez appeler et demander un courrier FedEx pour ramasser les envois.

   - `Drop Box` - Vous devez déposer vos envois dans la boîte de dépôt FedEx la plus proche.

   - `Business Service Center` - Vous devez déposer vos envois à votre centre de service commercial FedEx local.

   - `Station` - Vous devez déposer vos envois dans votre station FedEx locale.

1. Définir **[!UICONTROL Weight Unit]** à l’unité de mesure utilisée dans vos paramètres régionaux.

   - `Pounds`
   - `Kilograms`

1. Saisissez le **[!UICONTROL Maximum Package Weight]** autorisé pour les envois FedEx.

   Le poids maximal par défaut de FedEx est de 150 livres. Pour plus d’informations, consultez votre opérateur de livraison. La valeur par défaut est recommandée, sauf si vous avez pris des dispositions spéciales avec FedEx. Voir [Poids dimensionnel](carriers.md#dimensional-weight) pour plus d’informations.

   ![Paramètres du package FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

1. Configurez les options de frais de gestion en fonction de vos besoins.

   Les frais de gestion sont facultatifs et ne sont pas visibles lors de l’extraction. Si vous souhaitez inclure des frais de traitement, procédez comme suit :

   - Définir **[!UICONTROL Calculate Handling Fee]**:

      - `Fixed Fee`
      - `Percentage`

   - Pour **[!UICONTROL Handling Applied]**, sélectionnez l’une des méthodes suivantes pour gérer les frais de gestion :

      - `Per Order`
      - `Per Package`

   - Saisissez le **[!UICONTROL Handling Fee]** as a `fixed` montant ou `percentage`, selon la méthode de calcul.

1. Définir **[!UICONTROL Residential Delivery]** à l’un des éléments suivants, selon que vous vendez Entreprise à consommateur (B2C) ou Entreprise à entreprise (B2B).

   - `Yes` - Pour les diffusions résidentielles B2C.
   - `No` - Pour les diffusions résidentielles B2B.

   ![Paramètres des frais de gestion FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

## Étape 4 : Méthodes autorisées et pays applicables

1. Définir **[!UICONTROL Allowed Methods]** à chaque méthode d’expédition que vous souhaitez proposer.

   Lorsque vous choisissez des méthodes, tenez compte de votre compte FedEx, de la fréquence et de la taille de vos envois, et si vous autorisez les envois internationaux. Vous pouvez proposer autant de méthodes que vous le souhaitez, par exemple :

   - La première priorité de l&#39;Europe
   - Options de jour de remise : 1 jour de transport, 2 jours de transport, 2 jours, 2 jours, 2 jours, 3 jours de transport
   - Options intérieures - Express Saver, Ground, First, Overnight, Home Delivery, Standard Overnight
   - Options internationales : économie internationale, transport de l&#39;économie internationale, première internationale, sol international, international, priorité internationale
   - Options de priorité - Fret, priorité nocturne
   - Publication dynamique Si vous proposez la méthode de publication dynamique (saisissez la variable **ID de Hub**)
   - Options de transport - Freight, National Freight

1. Si vous souhaitez fournir une [Livraison gratuite](shipping-free.md) via FedEx, définissez les options de livraison gratuites.

   - Définir **[!UICONTROL Free Method]** à la méthode que vous souhaitez utiliser pour la livraison gratuite. Si vous ne souhaitez pas proposer de livraison gratuite via FedEx, choisissez `None`.

   - Pour exiger un montant minimum de commande qui qualifie une commande de livraison gratuite avec FedEx, définissez **[!UICONTROL Enable Free Shipping Threshold]** to `Enable`. Ensuite, saisissez la valeur minimale de **[!UICONTROL Free Shipping Amount Threshold]**.

   Ce paramètre est similaire à celui de la méthode d’expédition gratuite standard, mais il apparaît dans la section FedEx lors du passage en caisse, de sorte que les clients savent quelle méthode est utilisée pour leur commande.

1. Si nécessaire, modifiez la variable **[!UICONTROL Displayed Error Message]**.

   Cette zone de texte est prédéfinie avec un message par défaut, mais vous pouvez saisir un autre message que vous souhaitez afficher si FedEx devient indisponible.

   ![Méthodes de remise FedEx autorisées](../configuration-reference/sales/assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries` - Clients de tous les [pays](../getting-started/store-details.md#country-options) spécifié dans votre configuration de magasin peut utiliser cette méthode de diffusion.

   - `Specific Countries` - Lorsque vous sélectionnez cette option, la variable _Ship to Specific Countries_ s’affiche. Sélectionnez chaque pays de la liste dans lequel ce mode de diffusion peut être utilisé.

1. Si vous souhaitez conserver un journal de toutes les communications entre votre magasin et le système FedEx, définissez **[!UICONTROL Debug]** to `Yes`.

1. Définir **[!UICONTROL Show Method if Not Applicable]**:

   - `Yes` - Affiche toutes les méthodes de livraison FedEx pour les clients, quelle que soit leur disponibilité.
   - `No` - Affiche uniquement les méthodes de livraison FedEx qui s’appliquent à la commande.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer la séquence dans laquelle FedEx apparaît lorsqu’il est répertorié avec d’autres méthodes de remise lors du passage en caisse.

   `0` = first, `1` = second, `2` = troisième, etc.

1. Cliquez sur **[!UICONTROL Save Config]**.

   ![Pays applicables FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Commerce déclare toujours le prix de la commande complète à FedEx lors du calcul des frais de livraison. Ce comportement ne peut pas être modifié.

[1]: https://www.fedex.com/login/web/jsp/contactInfo1.jsp
