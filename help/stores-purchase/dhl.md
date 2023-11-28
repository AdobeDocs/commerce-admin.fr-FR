---
title: DHL
description: Découvrez comment configurer DHL en tant qu’opérateur de livraison pour votre magasin.
exl-id: 765e5f90-3e93-43cf-a5bc-6132e00b506c
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# DHL

DHL offre des services internationaux intégrés et des solutions personnalisées et axées sur le client pour la gestion et le transport des lettres, des marchandises et de l’information.

## Étape 1 : Activation de DHL

1. Sur le _Administration_ barre latérale, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Delivery Methods]**.

1. Développer ![Sélecteur d’extension](../assets/icon-display-expand.png) la valeur **[!UICONTROL DHL]** .

   >[!NOTE]
   >
   >Si nécessaire, effacez d’abord la variable **[!UICONTROL Use system value]** pour modifier les paramètres suivants, comme décrit.

1. Définir **[!UICONTROL Enabled for Checkout]** to `Yes`.

1. En règle générale, vous pouvez accepter la valeur par défaut **[!UICONTROL Gateway URL]**.

   Si DHL vous a donné une autre URL, entrez cette valeur dans ce champ.

1. Utilisez les informations d’identification fournies par DHL pour remplir les champs suivants :

   - **[!UICONTROL Access ID]**
   - **[!UICONTROL Password]**
   - **[!UICONTROL Account Number]**

![Paramètres du compte DHL](../configuration-reference/sales/assets/delivery-methods-dhl-account-settings.png){width="600" zoomable="yes"}

## Étape 2 ; saisissez la description du package et les frais de traitement.

1. Dans le **[!UICONTROL Content Type]** sélectionnez l’option qui décrit le mieux le type de package que vous fournissez :

   - `Documents`
   - `Non documents`

1. Configurez les options de frais de gestion en fonction de vos besoins.

   Les frais de gestion sont facultatifs et s’affichent sous la forme de frais supplémentaires, ajoutés aux frais d’expédition DHL. Si vous souhaitez inclure des frais de traitement, procédez comme suit :

   - Pour **[!UICONTROL Calculate Handling Fee]**, sélectionnez la méthode à utiliser pour calculer les frais de gestion :

      - `Fixed`
      - `Percentage`

   - Pour **[!UICONTROL Handling Applied]**, sélectionnez le mode d’application des frais de traitement :

      - `Per Order`
      - `Per Package`

   - Pour **[!UICONTROL Handling Fee]**, indiquez le montant à imputer, en fonction de la méthode de calcul choisie.

     Si, par exemple, les frais sont calculés à partir d’une somme fixe, saisissez la valeur décimale, par exemple `4.90`. Toutefois, si les frais de traitement sont basés sur un pourcentage de la commande, saisissez le montant en pourcentage. Par exemple, si vous facturez 6 % de la commande, saisissez la valeur `.06`.

   - Pour fractionner le poids total des commandes afin de garantir un calcul précis des frais d’expédition, définissez **[!UICONTROL Divide Order Weight]** to `Yes`.

   - Définissez la variable **[!UICONTROL Weight Unit]** du module à l’une des options suivantes :

      - `Pounds`
      - `Kilograms`

   - Définissez la variable **[!UICONTROL Size]** d’un module standard à l’une des options suivantes :

      - `Regular`
      - `Specific`

     Si vous choisissez `Specific`, saisissez la variable **[!UICONTROL Height]**, **[!UICONTROL Depth]**, et **[!UICONTROL Width]** du paquet en centimètres.

   ![Paramètres du module DHL](../configuration-reference/sales/assets/delivery-methods-dhl-package-settings.png){width="600" zoomable="yes"}

## Étape 3 : spécification des méthodes de diffusion autorisées

1. Pour **[!UICONTROL Allowed Methods]**, choisissez chaque méthode que vous souhaitez mettre à la disposition des clients.

   Pour sélectionner plusieurs méthodes, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

   Pour afficher la liste correcte des méthodes de diffusion, vous devez d&#39;abord indiquer la variable [Pays d’origine](../configuration-reference/sales/shipping-settings.md).

1. Pour **[!UICONTROL Ready Time]**, saisissez le nombre d’heures après l’envoi d’une commande qu’un package est prêt à envoyer.

1. Modifiez la variable **[!UICONTROL Displayed Error Message]** selon les besoins.

   Ce message s’affiche lorsqu’une méthode sélectionnée n’est pas disponible.

1. Si vous souhaitez fournir une [Livraison gratuite](shipping-free.md) via DHL, définissez les options d’expédition gratuites.

   - Pour **[!UICONTROL Free Method]**, choisissez la méthode que vous préférez utiliser pour la livraison gratuite.

   - Définir **[!UICONTROL Free Shipping Amount Threshold]**:

     `Enable` - Si vous proposez une livraison gratuite avec une commande minimale, saisissez la variable **[!UICONTROL Minimum Order Amount for Free Shipping]**.

     `Disable` - Ne s’applique pas à la livraison gratuite de DHL à des commandes.

     Ce paramètre est similaire à celui de la norme _Livraison gratuite_ , mais apparaît dans la section DHL pour que les clients sachent quelle méthode est utilisée pour leur commande.

   - Pour **[!UICONTROL Free Shipping Amount Threshold]**, saisissez le montant minimum requis pour qu’une commande soit admissible à la livraison gratuite.

     ![Méthodes autorisées DHL](../configuration-reference/sales/assets/delivery-methods-dhl-allowed-methods.png){width="600" zoomable="yes"}

## Étape 4 : spécification des pays applicables

1. Définir **[!UICONTROL Ship to Applicable Countries]** à l’une des options suivantes :

   - `All Allowed Countries`
   - `Specific Countries`

   Si vous expédiez vers des pays spécifiques, sélectionnez chaque pays dans la **[!UICONTROL Ship to Specific Countries]** liste.

1. Définir **[!UICONTROL Show Method if Not Applicable]**:

   `Yes` - Affiche DHL comme méthode d’expédition lors du passage en caisse, même si elle n’est pas applicable à la commande.

   `No` - Affiche DHL comme méthode d’expédition lors du passage en caisse uniquement si applicable.

1. Pour créer un fichier journal contenant les détails des envois DHL effectués à partir de votre magasin, définissez **[!UICONTROL Debug]** to `Yes`.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer l’ordre dans lequel DHL apparaît lorsqu’il est répertorié avec d’autres méthodes de diffusion lors du passage en caisse.

   `0` = first, `1` = second, `2` = troisième, etc.

1. Cliquez sur **[!UICONTROL Save Config]**.

   ![Pays applicables DHL](../configuration-reference/sales/assets/delivery-methods-dhl-applicable-countries.png){width="600" zoomable="yes"}
