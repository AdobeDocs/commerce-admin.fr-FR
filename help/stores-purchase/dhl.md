---
title: DHL
description: Découvrez comment configurer DHL en tant qu’opérateur de livraison pour votre magasin.
exl-id: 765e5f90-3e93-43cf-a5bc-6132e00b506c
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# DHL

DHL offre des services internationaux intégrés et des solutions personnalisées et axées sur le client pour la gestion et le transport des lettres, des marchandises et de l’information.

## Étape 1 : Activation de DHL

1. Sur la barre latérale _Admin_, accédez à **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Dans le panneau de gauche, développez **[!UICONTROL Sales]** et choisissez **[!UICONTROL Delivery Methods]**.

1. Développez la section ![Sélecteur d’extension](../assets/icon-display-expand.png) sur **[!UICONTROL DHL]** .

   >[!NOTE]
   >
   >Si nécessaire, décochez d’abord la case **[!UICONTROL Use system value]** pour modifier les paramètres suivants, comme décrit.

1. Définissez **[!UICONTROL Enabled for Checkout]** sur `Yes`.

1. En règle générale, vous pouvez accepter la valeur par défaut **[!UICONTROL Gateway URL]**.

   Si DHL vous a donné une autre URL, entrez cette valeur dans ce champ.

1. Utilisez les informations d’identification fournies par DHL pour remplir les champs suivants :

   - **[!UICONTROL Access ID]**
   - **[!UICONTROL Password]**
   - **[!UICONTROL Account Number]**

![Paramètres du compte DHL](../configuration-reference/sales/assets/delivery-methods-dhl-account-settings.png){width="600" zoomable="yes"}

## Étape 2 ; saisissez la description du package et les frais de traitement.

1. Dans la liste **[!UICONTROL Content Type]**, sélectionnez l’option qui décrit le mieux le type de package que vous fournissez :

   - `Documents`
   - `Non documents`

1. Configurez les options de frais de gestion en fonction de vos besoins.

   Les frais de gestion sont facultatifs et s’affichent sous la forme de frais supplémentaires, ajoutés aux frais d’expédition DHL. Si vous souhaitez inclure des frais de traitement, procédez comme suit :

   - Pour **[!UICONTROL Calculate Handling Fee]**, sélectionnez la méthode à utiliser pour calculer les frais de gestion :

      - `Fixed`
      - `Percentage`

   - Pour **[!UICONTROL Handling Applied]**, sélectionnez le mode d’application des frais de gestion :

      - `Per Order`
      - `Per Package`

   - Pour **[!UICONTROL Handling Fee]**, indiquez le montant à imputer, en fonction de la méthode de calcul choisie.

     Par exemple, si le coût est basé sur des frais fixes, saisissez le montant sous forme de décimale, par exemple `4.90`. Toutefois, si les frais de traitement sont basés sur un pourcentage de la commande, saisissez le montant en pourcentage. Par exemple, si vous chargez six pour cent de la commande, saisissez la valeur `.06`.

   - Pour répartir le poids total des commandes afin d&#39;assurer un calcul précis des frais d&#39;expédition, définissez **[!UICONTROL Divide Order Weight]** sur `Yes`.

   - Définissez la **[!UICONTROL Weight Unit]** du package sur l’une des options suivantes :

      - `Pounds`
      - `Kilograms`

   - Définissez le **[!UICONTROL Size]** d’un package type sur l’un des éléments suivants :

      - `Regular`
      - `Specific`

     Si vous choisissez `Specific`, saisissez les valeurs **[!UICONTROL Height]**, **[!UICONTROL Depth]** et **[!UICONTROL Width]** du package en centimètres.

   ![Paramètres du package DHL](../configuration-reference/sales/assets/delivery-methods-dhl-package-settings.png){width="600" zoomable="yes"}

## Étape 3 : spécification des méthodes de diffusion autorisées

1. Pour **[!UICONTROL Allowed Methods]**, choisissez chaque méthode que vous souhaitez mettre à la disposition des clients.

   Pour sélectionner plusieurs méthodes, maintenez la touche Ctrl (PC) ou la touche Commande (Mac) enfoncée, puis cliquez sur chaque option.

   Pour afficher la liste correcte des méthodes de diffusion, vous devez d’abord spécifier le [pays d’origine](../configuration-reference/sales/shipping-settings.md).

1. Pour **[!UICONTROL Ready Time]**, saisissez le nombre d’heures après l’envoi d’une commande qu’un package est prêt à envoyer.

1. Modifiez le **[!UICONTROL Displayed Error Message]** selon vos besoins.

   Ce message s’affiche lorsqu’une méthode sélectionnée n’est pas disponible.

1. Si vous souhaitez fournir une option de [livraison gratuite](shipping-free.md) via DHL, définissez les options de livraison gratuite.

   - Pour **[!UICONTROL Free Method]**, choisissez la méthode que vous préférez utiliser pour la livraison gratuite.

   - Définissez **[!UICONTROL Free Shipping Amount Threshold]** :

     `Enable` - Si vous proposez la livraison gratuite avec la commande minimale, saisissez le **[!UICONTROL Minimum Order Amount for Free Shipping]**.

     `Disable` - Ne s’applique pas à la livraison gratuite de DHL pour les commandes.

     Ce paramètre est similaire à celui de la méthode _Livraison gratuite_ standard, mais il apparaît dans la section DHL pour que les clients sachent quelle méthode est utilisée pour leur commande.

   - Pour **[!UICONTROL Free Shipping Amount Threshold]**, saisissez le montant minimum pour qu’une commande puisse être admissible à la livraison gratuite.

     ![Méthodes DHL autorisées](../configuration-reference/sales/assets/delivery-methods-dhl-allowed-methods.png){width="600" zoomable="yes"}

## Étape 4 : spécification des pays applicables

1. Définissez **[!UICONTROL Ship to Applicable Countries]** sur l’une des options suivantes :

   - `All Allowed Countries`
   - `Specific Countries`

   Si vous effectuez des envois vers des pays spécifiques, sélectionnez chaque pays dans la liste **[!UICONTROL Ship to Specific Countries]**.

1. Définissez **[!UICONTROL Show Method if Not Applicable]** :

   `Yes` - Affiche DHL comme méthode d’expédition lors du passage en caisse, même si elle n’est pas applicable à la commande.

   `No` - Affiche DHL comme méthode d’expédition lors du passage en caisse uniquement si applicable.

1. Pour créer un fichier journal contenant les détails des envois DHL effectués à partir de votre magasin, définissez **[!UICONTROL Debug]** sur `Yes`.

1. Pour **[!UICONTROL Sort Order]**, saisissez un nombre afin de déterminer la séquence dans laquelle DHL apparaît lorsqu’il est répertorié avec d’autres méthodes de diffusion lors de l’extraction.

   `0` = premier, `1` = second, `2` = troisième, etc.

1. Cliquez sur **[!UICONTROL Save Config]**.

   ![Pays applicables DHL](../configuration-reference/sales/assets/delivery-methods-dhl-applicable-countries.png){width="600" zoomable="yes"}
