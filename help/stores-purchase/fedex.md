---
title: FedEx
description: Découvrez comment configurer FedEx en tant que transporteur pour votre boutique.
exl-id: 75bb3ed1-3ae9-418a-be90-888046b28a7b
feature: Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '881'
ht-degree: 0%

---

# FedEx

FedEx est l&#39;une des plus grandes compagnies de transport maritime au monde, fournissant des services aériens, de fret et de transport terrestre avec plusieurs niveaux de priorités.

![Options d&#39;expédition FedEx au passage en caisse](./assets/storefront-checkout-shipping-fedex.png){width="700" zoomable="yes"}

>[!NOTE]
>
>FedEx peut utiliser [poids dimensionnel](carriers.md#dimensional-weight) pour déterminer certains frais d’expédition. Cependant, Adobe Commerce et Magento Open Source ne prennent en charge que le calcul des coûts d’expédition en fonction du poids.

## Étape 1 : S&#39;inscrire à la production de FedEx Web Services

A [Compte marchand FedEx][1] et l’enregistrement pour l’accès à la production des services Web FedEx est requis. Après avoir créé un compte FedEx, lisez la page d&#39;informations du compte de production, puis cliquez sur le lien _Obtention de la clé de production_ lien en bas de la page pour s’inscrire et obtenir une clé.

>[!NOTE]
>
>Veillez à copier ou écrire la clé d’authentification. Il est nécessaire de configurer FedEx dans vos paramètres d’expédition Commerce.

## Étape 2 : activer FedEx pour votre boutique

1. Le _Admin_ barre latérale, accéder à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Delivery Methods]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) le **[!UICONTROL FedEx]** section.

1. Définir **[!UICONTROL Enabled for Checkout]** vers `Yes`.

1. Pour **[!UICONTROL Title]**, saisissez un titre qui identifie la méthode d&#39;expédition FedEx lors du passage en caisse.

1. Saisissez les informations suivantes à partir de votre compte FedEx :

   - **[!UICONTROL Account ID]**
   - **[!UICONTROL Api Key]**
   - **[!UICONTROL Secret Key]**

1. Si vous avez configuré un sandbox FedEx et souhaitez travailler dans l’environnement de test, définissez **[!UICONTROL Sandbox Mode]** vers `Yes`.

   >[!NOTE]
   >
   >N’oubliez pas de définir le mode Sandbox sur . `No` lorsque vous êtes prêt à proposer FedEx comme méthode d&#39;expédition à vos clients.

   ![Paramètres du compte FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

## Etape 3 : Description du package et frais de gestion

1. Définir **[!UICONTROL Pickup Type]** à la méthode de prélèvement utilisée pour les expéditions.

   - `DropOff at Fedex Location` - (Par défaut) Indique que vous déposez les envois à votre station FedEx locale.
   - `Contact Fedex to Schedule` - Indique que vous avez contacté FedEx pour demander un retrait.
   - `Use Scheduled Pickup` - Indique que l&#39;expédition est récupérée dans le cadre d&#39;un ramassage régulier programmé.
   - `On Call` - Indique que le retrait est programmé en appelant FedEx.
   - `Package Return Program` - Indique que l&#39;expédition est récupérée par le Programme de retours de colis FedEx Ground.
   - `Regular Stop` - Indique que l&#39;expédition est récupérée selon le calendrier de récupération standard.
   - `Tag` - Indique que le retrait de l&#39;expédition est spécifique à une demande de retrait d&#39;étiquette express ou d&#39;étiquette d&#39;appel au sol. Ceci s&#39;applique uniquement pour une étiquette d&#39;expédition retour.

1. Pour **[!UICONTROL Packages Request Type]**, sélectionnez le type de demande qui décrit le mieux vos préférences lors du fractionnement d&#39;une commande en plusieurs livraisons :

   - `Divide to equal weight (one request)`
   - `Use origin weight (few requests)`

1. Pour **[!UICONTROL Packaging]**, sélectionnez le type d’emballage FedEx que vous utilisez généralement pour expédier des produits à partir de votre magasin.

1. Définir **[!UICONTROL Weight Unit]** à l’unité de mesure utilisée dans vos paramètres régionaux.

   - `Pounds`
   - `Kilograms`

1. Saisir le **[!UICONTROL Maximum Package Weight]** autorisés pour les expéditions FedEx.

   Le poids maximum par défaut de FedEx est de 150 livres. Pour plus d&#39;informations, consultez votre transporteur. La valeur par défaut est recommandée, sauf si vous avez pris des dispositions spéciales avec FedEx. Voir [Poids dimensionnel](carriers.md#dimensional-weight) pour plus d’informations.

   ![Paramètres du package FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

1. Configurez les options de frais de gestion en fonction de vos besoins.

   Les frais de gestion sont facultatifs et ne sont pas visibles lors du passage en caisse. Si vous souhaitez inclure des frais de manutention, procédez comme suit :

   - Définir **[!UICONTROL Calculate Handling Fee]**:

      - `Fixed Fee`
      - `Percentage`

   - Pour **[!UICONTROL Handling Applied]**, choisissez l’une des méthodes suivantes pour gérer les frais de traitement :

      - `Per Order`
      - `Per Package`

   - Saisir le **[!UICONTROL Handling Fee]** en tant que `fixed` montant ou `percentage`, en fonction de la méthode de calcul.

1. Définir **[!UICONTROL Residential Delivery]** à l’un des éléments suivants, selon que vous vendez de l’entreprise au consommateur (B2C) ou de l’entreprise à l’entreprise (B2B).

   - `Yes` - Pour les diffusions résidentielles B2C.
   - `No` - Pour les diffusions résidentielles B2B.

   ![Paramètres des frais de gestion FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

## Étape 4 : Méthodes autorisées et pays applicables

1. Définir **[!UICONTROL Allowed Methods]** à chaque mode d&#39;expédition que vous souhaitez proposer.

   Lorsque vous choisissez des méthodes, tenez compte de votre compte FedEx, de la fréquence et de la taille de vos envois, et si vous autorisez les envois internationaux. Vous pouvez proposer autant de méthodes que vous le souhaitez, ou en proposer autant, par exemple :

   - Priorité Europe d&#39;abord
   - Options de jour de livraison : 1 jour de fret, 2 jours de fret, 2 jours, 2 jours, 3 jours de fret
   - Options domestiques - Express Saver, Ground, First, Overnight, Home Delivery, Standard Overnight
   - Options internationales-Économie internationale, Intl Economy Freight, International First, International Ground, International, Priorité Intl
   - Options de priorité-Transport, Priorité de nuit
   - Smart Post-If offrant la méthode Smart Post (saisir la valeur **Identifiant du hub**)
   - Options de transport-Transport, transport national

1. Si vous souhaitez fournir un [Livraison gratuite](shipping-free.md) par le biais de FedEx, définissez les options d&#39;expédition gratuite.

   - Définir **[!UICONTROL Free Method]** à la méthode que vous souhaitez utiliser pour la livraison gratuite. Si vous ne voulez pas offrir la livraison gratuite par FedEx, choisissez `None`.

   - Pour exiger un montant de commande minimum qui qualifie une commande pour une livraison gratuite avec FedEx, définissez **[!UICONTROL Enable Free Shipping Threshold]** vers `Enable`. Saisissez ensuite la valeur minimale en . **[!UICONTROL Free Shipping Amount Threshold]**.

   Ce paramètre est similaire à celui de la méthode d&#39;expédition gratuite standard, mais il apparaît dans la section FedEx lors du passage en caisse, afin que les clients sachent quelle méthode est utilisée pour leur commande.

1. Si nécessaire, modifiez le **[!UICONTROL Displayed Error Message]**.

   Cette zone de texte est prédéfinie avec un message par défaut, mais vous pouvez saisir un message différent que vous souhaitez afficher si FedEx n&#39;est plus disponible.

   ![Méthodes de livraison autorisées par FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

1. Définir **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries` - Clients de tous les [pays](../getting-started/store-details.md#country-options) spécifiée dans la configuration de votre boutique peut utiliser cette méthode de diffusion.

   - `Specific Countries` - Lorsque vous choisissez cette option, le _Expédition vers des pays spécifiques_ La liste s’affiche. Sélectionnez dans la liste les pays où cette méthode de diffusion peut être utilisée.

1. Si vous souhaitez conserver un journal de toutes les communications entre votre magasin et le système FedEx, définissez **[!UICONTROL Debug]** vers `Yes`.

1. Définir **[!UICONTROL Show Method if Not Applicable]**:

   - `Yes` - Affiche toutes les méthodes d&#39;expédition FedEx aux clients, quelle que soit leur disponibilité.
   - `No` - Affiche uniquement les méthodes d&#39;expédition FedEx qui s&#39;appliquent à la commande.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre pour déterminer l&#39;ordre dans lequel FedEx apparaît lorsqu&#39;il est répertorié avec d&#39;autres méthodes de diffusion lors du passage en caisse.

   `0` = first, `1` = seconde, `2` = troisième, etc.

1. Clic **[!UICONTROL Save Config]**.

   ![Pays applicables à FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Lors du calcul des frais d&#39;expédition, Commerce déclare toujours le prix total de la commande à FedEx. Ce comportement ne peut pas être modifié.

[1]: https://www.fedex.com/login/web/jsp/contactInfo1.jsp
