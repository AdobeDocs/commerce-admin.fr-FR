---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Delivery Methods]'
description: Vérifiez les paramètres de configuration sur la page [!UICONTROL Sales] &gt; [!UICONTROL Delivery Methods] de l’administrateur Commerce.
exl-id: 159b76a8-3676-4692-9cd6-18947bda4666
feature: Configuration, Shipping/Delivery
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '3812'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Delivery Methods]

{{config}}

## [!UICONTROL Basic Delivery Methods]

### [!UICONTROL Flat Rate]

![Taux d&#39;aplatissement](./assets/delivery-methods-flat-rate.png)<!-- zoom -->

<!-- [Flat Rate](https://docs.magento.com/user-guide/shipping/shipping-flat-rate.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site Web | Lorsque cette option est activée, le taux plat s’affiche comme option dans la variable _Estimation de la livraison et des taxes_ du panier, et dans la variable _Expédition_ durant le passage en caisse. Options : `Yes` / `No` |
| [!UICONTROL Title] | Affichage en magasin | Nom utilisé pour ce mode d’expédition lors du passage en caisse. |
| [!UICONTROL Method Name] | Affichage en magasin | Nom qui décrit la méthode de calcul utilisée pour produire une estimation de livraison. Le nom de la méthode s’affiche en regard du taux estimé calculé dans le panier. La valeur par défaut est `Fixed`. |
| [!UICONTROL Type] | Site Web | Décrit le type de calcul utilisé pour déterminer le taux forfaitaire. Options : <br/>**`None`**- Aucun calcul n’est utilisé. Définit le taux plat sur zéro, ce qui équivaut à la livraison gratuite.<br/>**`Per Order`** - Facture un seul taux forfaitaire pour l’ensemble de la commande. <br/>**`Per Item`**- Facture un taux forfaitaire distinct pour chaque article du panier. Le taux est multiplié par le nombre d’articles dans le panier, même si la quantité totale inclut une combinaison d’articles différents. |
| [!UICONTROL Price] | Site Web | Prix que vous facturez au client pour l’expédition à taux fixe. |
| [!UICONTROL Calculate Handling Fee] | Site Web | Détermine le mode de calcul des frais de traitement, le cas échéant. Options : `Fixed` / `Percent` |
| [!UICONTROL Handling Fee] | Site Web | Indiquez le montant qui sera imputé sur les frais de traitement, selon la méthode que vous avez choisie pour calculer le montant. Si, par exemple, les frais sont basés sur des frais fixes, indiquez le montant sous forme de décimale, comme 4,90. Toutefois, si les frais de traitement sont basés sur un pourcentage de la commande, saisissez le montant en pourcentage. Par exemple, si vous facturez 6 % de la commande, saisissez la valeur `.06`. |
| [!UICONTROL Displayed Error Message] | Affichage en magasin | Un message qui s’affiche si un client choisit le taux plat, mais que la méthode n’est pas disponible pour une raison quelconque. |
| [!UICONTROL Ship to Applicable Countries] | Site Web | Identifie les pays dans lesquels vous proposez une expédition à taux plat. Options : <br/>**`All Allowed Countries`**- Les clients de n’importe quel pays spécifié dans la configuration du magasin peuvent utiliser la livraison à taux plat.<br/>**`Specific Countries`** - Les clients de pays spécifiques peuvent uniquement utiliser la livraison à taux plat. |
| [!UICONTROL Ship to Specific Countries] | Site Web | Identifie chaque pays dans lequel les clients peuvent utiliser l’expédition à taux plat. |
| [!UICONTROL Show Method if Not Applicable] | Site Web | Détermine si le taux d’aplatissement apparaît comme une option lors de l’extraction si la méthode ne s’applique pas à l’achat. Options : `Yes` / `No` |
| [!UICONTROL Sort Order] | Site Web | Un nombre qui détermine l’ordre dans lequel le taux d’aplatissement s’affiche lorsqu’il est répertorié avec d’autres méthodes de diffusion lors du passage en caisse. |

{style="table-layout:auto"}

### [!UICONTROL Free Shipping]

![Livraison gratuite](./assets/delivery-methods-free-shipping.png)<!-- zoom -->

<!-- [Free Shipping](https://docs.magento.com/user-guide/shipping/shipping-free.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site Web | Lorsque cette option est activée, la fonction Expédition gratuite apparaît comme option dans la section Expédition lors du passage en caisse. Options : `Yes` / `No` |
| [!UICONTROL Title] | Affichage en magasin | Nom utilisé pour ce mode d’expédition lors du passage en caisse. |
| Nom de méthode | Affichage en magasin | Nom qui décrit la méthode de calcul utilisée pour produire une estimation de livraison. Le nom de la méthode s’affiche en regard du taux estimé calculé dans le panier. La valeur par défaut est `Free`. |
| Montant minimal de la commande | Site Web | L’achat minimum requis pour appliquer la livraison gratuite à une commande. |
| Inclure la taxe au montant | Site Web | Détermine si la taxe est incluse dans le calcul du montant de commande minimum. Options : <br/>**Oui** - Taxe incluse lors du calcul du montant minimum de la commande (Subtotal + Taxe - Remise).<br/>**Non** - Taxe non incluse dans le calcul de la taxe minimum (sous-total - escompte). |
| Message d’erreur affiché | Affichage en magasin | Un message qui s’affiche si un client choisit la livraison gratuite, mais que la méthode n’est pas disponible pour une raison quelconque. |
| Expédier aux pays applicables | Site Web | Identifie les pays où vous proposez la livraison gratuite. Options : <br/>**Tous les pays autorisés** - Les clients de n’importe quel pays spécifié dans la configuration du magasin peuvent utiliser la livraison gratuite. <br/>**Pays spécifiques** - Les clients de pays spécifiques peuvent uniquement utiliser la livraison gratuite. |
| Ship to Specific Countries | Site Web | Identifie chaque pays où les clients peuvent utiliser la livraison gratuite. |
| Afficher la méthode si cela n’est pas applicable | Site Web | Détermine si l’option Livraison gratuite apparaît comme option lors de l’extraction si la méthode ne s’applique pas à l’achat. Options : `Yes` / `No` |
| [!UICONTROL Sort Order] | Site Web | Numéro qui détermine la commande que la livraison gratuite apparaît lorsqu’elle est répertoriée avec d’autres méthodes de livraison lors du passage en caisse. |

{style="table-layout:auto"}

### [!UICONTROL Table Rates]

![Taux sur les tableaux](./assets/delivery-methods-table-rates.png)<!-- zoom -->

<!-- [Table Rates](https://docs.magento.com/user-guide/shipping/shipping-table-rate.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site Web | Lorsque cette option est activée, les taux de tableau s’affichent comme une option dans la section Estimer l’expédition et la taxe du panier, ainsi que dans la section Expédition lors du passage en caisse. Options : `Yes` / `No` |
| [!UICONTROL Title] | Affichage en magasin | Nom utilisé pour ce mode d’expédition lors du passage en caisse. |
| Nom de méthode | Affichage en magasin | Nom qui décrit la méthode de calcul utilisée pour produire une estimation de livraison. Le nom de la méthode s’affiche en regard du taux estimé calculé dans le panier. La valeur par défaut est `Table Rate`. |
| [!UICONTROL Condition] | Site Web | Détermine la condition sur laquelle repose le calcul. Le format du fichier CSV chargé est spécifique à chaque condition. Options : `Weight vs. Destination` / `Price vs. Destination` / `# of Items vs. Destination` |
| [!UICONTROL Include Virtual Products in Price Calculation] | Site Web | Détermine si les produits virtuels, qui ne nécessitent pas d’expédition, sont inclus dans les calculs de prix du taux de tableau. |
| [!UICONTROL Calculate Handling Fee] | Site Web | Détermine le mode de calcul des frais de traitement, le cas échéant. Options : `Fixed` / `Percent` |
| [!UICONTROL Handling Fee] | Site Web | Montant des frais ajoutés aux frais d’expédition pour couvrir les frais de gestion de l’expédition. Saisissez la valeur sous forme de décimale. Par exemple, si la taxe est basée sur un pourcentage, entrez 0,06 au lieu de 6 %. Pour un montant fixe, saisissez `6.00`. |
| [!UICONTROL Displayed Error Message] | Affichage en magasin | Un message qui s’affiche si un client choisit les taux de tableau, mais que la méthode n’est pas disponible pour une raison quelconque. |
| [!UICONTROL Ship to Applicable Countries] | Site Web | Identifie les pays dans lesquels vous proposez l’expédition à taux de tableau. Options : <br/>**`All Allowed Countries`**- Les clients de n’importe quel pays spécifié dans la configuration du magasin peuvent utiliser l’expédition à taux de tableau.<br/>**`Specific Countries`** - Les clients de pays spécifiques peuvent uniquement utiliser l’expédition à taux de tableau. |
| [!UICONTROL Ship to Specific Countries] | Site Web | Identifie chaque pays dans lequel les clients peuvent utiliser l’expédition à taux de tableau. |
| [!UICONTROL Show Method if Not Applicable] | Site Web | Détermine si les taux du tableau s’affichent comme une option lors de l’extraction si la méthode ne s’applique pas à l’achat. Options : `Yes` / `No` |
| [!UICONTROL Sort Order] | Site Web | Un nombre qui détermine l’ordre dans lequel les taux du tableau apparaissent lorsqu’ils sont répertoriés avec d’autres méthodes de remise lors de l’extraction. |

{style="table-layout:auto"}

### [!UICONTROL In-Store Delivery]

![Diffusion en magasin](./assets/delivery-methods-in-store-delivery.png)<!-- zoom -->

<!-- [In-Store Delivery](https://docs.magento.com/user-guide/shipping/shipping-in-store-delivery.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site Web | Lorsque cette option est activée, la diffusion en magasin peut apparaître comme option dans la variable _Estimation de la livraison et des taxes_ du panier, et dans la variable _Expédition_ durant le passage en caisse. Options : `Yes` / `No` |
| [!UICONTROL Method Name] | Affichage en magasin | Nom qui identifie la fonction de récupération en magasin comme méthode d’expédition. Cette valeur s’affiche sous forme de libellé d’un onglet en haut de la page Passage en caisse pour la livraison et dans le tableau des méthodes d’expédition disponibles au bas de la même page. La valeur par défaut est `In-store Delivery`. |
| [!UICONTROL Title] | Affichage en magasin | Nom utilisé pour ce mode d’expédition lors du passage en caisse. |
| [!UICONTROL Price] | Site Web | Le prix que vous facturez au client pour un nettoyage en magasin. |
| [!UICONTROL Search Radius] | Site Web | Rayon, en km, à utiliser lors de la recherche d’emplacements de récupération. |
| [!UICONTROL Displayed Error Message] | Affichage en magasin | Message qui s’affiche lorsqu’un client sélectionne une sélection en magasin, mais que la méthode de remise n’est pas disponible. |

{style="table-layout:auto"}

## [!UICONTROL Carriers]

### [!UICONTROL UPS]

{{ups-api}}

{{beta2-updates}}

![Paramètres du compte XML UPS](./assets/delivery-methods-ups1.png)<!-- zoom -->

<!-- [UPS XML Account Settings](https://docs.magento.com/user-guide/shipping/ups.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled for Checkout] | Site Web | Détermine si UPS est disponible pour les clients comme méthode d’expédition lors du passage en caisse. Options : `Yes` / `No` |
| [!UICONTROL Enabled for RMA] | Site Web | Détermine si UPS est disponible pour les clients en tant que méthode d’expédition pour une RAM. Options : `Yes` / `No` |
| [!UICONTROL UPS Type] | Affichage en magasin | Spécifie la méthode utilisée pour se connecter au système d’expédition UPS. Options : <br/>**`United Parcel Service XML`**- (Par défaut) Votre magasin envoie un fichier XML avec des données à UPS en tant que demande.<br/>**`United Parcel Service`** - Votre boutique envoie des paires clé-valeur à UPS en tant que requête. <br/><br/>**_Remarque :_**Le type de service United Parcel standard est planifié pour une obsolescence dans Commerce. Pour de nouvelles configurations, vous devez utiliser la variable [!UICONTROL United Parcel Service XML] type. |
| _[!UICONTROL UPS Account Settings]_ |  |  |
| [!UICONTROL Live Account] | Affichage en magasin | Indique que le compte United Parcel Service est actif. Options : `Yes` / `No` |
| [!UICONTROL Gateway URL] | Site Web | URL qui se connecte au système UPS pour récupérer les tarifs d’expédition dynamiques. UPS interrompt la prise en charge du protocole HTTP. Valeur par défaut : `https://www.ups.com/using/services/rave/qcostcgi.cgi` |
| [!UICONTROL Title] | Affichage en magasin | Nom utilisé pour ce mode d’expédition lors du passage en caisse. |
| _[!UICONTROL UPS XML Account Settings]_ |  |  |
| [!UICONTROL Access License Number] | Site Web | Votre numéro de licence d’accès au compte de l’expéditeur UPS. |
| [!UICONTROL Gateway XML URL] | Site Web | Pour le service XML UPS, affiche les URL suivantes, requises pour transmettre des données XML : URL XML de passerelle, URL XML de suivi, URL XML de confirmation de livraison, URL XML d’acceptation de livraison |
| [!UICONTROL Mode] | Site Web | Détermine le mode de transmission des données envoyées au système UPS. Options : <br/>**`Development`**- UPS ne vérifie pas que les données reçues du serveur Commerce sont envoyées via SSL.<br/>**`Live`** - UPS vérifie que les données reçues du serveur Commerce sont envoyées via une couche de socket sécurisée (SSL). |
| Identifiant utilisateur | Site Web | Votre identifiant utilisateur de compte de l&#39;expéditeur UPS. |
| [!UICONTROL Origin of the Shipment] | Site Web | (UPS XML uniquement) Pays ou région d’où provient l’expédition du produit. |
| [!UICONTROL Password] | Affichage en magasin | Votre mot de passe du compte de l&#39;expéditeur UPS. |

{style="table-layout:auto"}

![Informations sur le package UPS](./assets/delivery-methods-ups-packaging-settings.png)<!-- zoom -->

<!-- [UPS Package Information](https://docs.magento.com/user-guide/shipping/ups.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL UPS Negotiated Rate Settings]_ |  |  |
| [!UICONTROL Enable Negotiated Rates] | Site Web | (UPS XML uniquement) Active/désactive les taux spéciaux, conformément à votre accord avec UPS. Options : `Yes` / `No` |
| [!UICONTROL Packages Request Type] | Site Web | Détermine le mode de calcul du poids des envois comportant plusieurs packages. Options : `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Shipper Number] | Site Web | (UPS XML uniquement) Le numéro d’expéditeur UPS à six caractères est requis pour que la référence utilise des taux négociés. |
| [!UICONTROL Container] | Site Web | Définit le type de conteneur utilisé pour empaqueter les envois de commande. Options : `Customer Packaging` / `UPS Letter Envelope` / `Customer Packaging` / `UPS Letter Envelope` / `UPS Tube` / `UPS Express Box` / `UPS Worldwide 25 kilo` / `UPS Worldwide 10 kilo` |
| [!UICONTROL Weight Unit] | Site Web | Définit l’unité de mesure par défaut du poids du produit dans votre magasin. Voir [Poids dimensionnel](../../stores-purchase/carriers.md#dimensional-weight) pour plus d’informations. |
| [!UICONTROL Tracking XML URL] | Site Web | (UPS XML uniquement) URL UPS utilisée pour effectuer le suivi des modules. |
| [!UICONTROL Destination Type] | Site Web | Définit le type de destination d’expédition par défaut. Options : `Business` / `Residential` |
| [!UICONTROL Maximum Package Weight] | Site Web | Définit le poids maximal qu’un package peut être spécifié par UPS. Si les produits commandés dépassent le poids maximal du package, cette option d&#39;expédition n&#39;est pas disponible. Selon [UPS.com](https://www.ups.com/us/en/global.page), les packages ne peuvent pas dépasser 150 lbs (70 kg) Vérifiez auprès de votre opérateur de transport le poids maximal. |
| [!UICONTROL Pickup Method] | Site Web | Définit la méthode de récupération UPS. Options : `Regular Daily Pickup` / `On Call Air` / `One Time Pickup` / `Letter Center` / `Customer Counter` |
| [!UICONTROL Minimum Package Weight] | Site Web | Définit le poids minimum qu’un package peut être tel que spécifié par UPS. Si le poids des produits commandés est inférieur au poids minimum du package, cette option d&#39;expédition n&#39;est pas disponible. Pour vérifier le poids minimum, contactez votre opérateur de transport. |
| [!UICONTROL Calculate Handling Fee] | Site Web | Définit la méthode de calcul des frais de gestion pour les frais d’expédition à taux variable. Options : <br>**`Fixed`**- Les frais de traitement sont un taux fixe.<br>**`Percent`** - Les frais de gestion sont appliqués en pourcentage du montant de la commande. |
| [!UICONTROL Handling Applied] | Site Web | Indique si les frais de traitement sont appliqués à chaque commande ou à chaque module dans une commande. |
| [!UICONTROL Handling Fee] | Site Web | Définit la gestion incluse dans le prix de livraison. Les frais de gestion peuvent être définis sous la forme d’un montant fixe ou d’un pourcentage. <br/><br/>**_Remarque :_**Si vous saisissez un pourcentage, utilisez le format décimal `0.25` pour 25 %. |

{style="table-layout:auto"}

![Méthodes UPS autorisées](./assets/delivery-methods-ups-allowed-methods.png)<!-- zoom -->

<!-- [UPS Allowed Methods](https://docs.magento.com/user-guide/shipping/ups.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL UPS allowed methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Site Web | Spécifie les méthodes d’expédition UPS autorisées proposées aux clients. Les taux d’expédition sont calculés en fonction du mode de livraison sélectionné. |
| [!UICONTROL Free Method] | Site Web | Identifie la méthode utilisée pour la méthode d’expédition gratuite via UPS. Pour désactiver la livraison gratuite, sélectionnez &quot;Aucun&quot;. <br/><br/>**_Remarque :_**Cette méthode est similaire à la méthode de base [Livraison gratuite](../../stores-purchase/shipping-free.md), toutefois, il apparaît comme une option d’expédition UPS lors du passage en caisse. |
| [!UICONTROL Free Shipping Amount Threshold] | Site Web | Détermine si la livraison gratuite est appliquée lorsque le montant de la commande respecte le seuil de livraison gratuite. Options : `Enable` / `Disable` |
| [!UICONTROL Free Shipping Amount Threshold] | Site Web | Définit le montant total minimum qu’une commande doit atteindre pour être admissible à la livraison gratuite. |
| [!UICONTROL Displayed Error Message] | Affichage en magasin | Message d’erreur affiché lorsque ce mode de livraison n’est pas disponible pour une raison quelconque. |

{style="table-layout:auto"}

![UPS applicable aux pays et autres paramètres](./assets/delivery-methods-ups-ship-to.png)<!-- zoom -->

<!-- [UPS Applicable Countries and Other Settings](https://docs.magento.com/user-guide/shipping/ups.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL UPS Applicable countries and other Settings]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Site Web | Indique les pays dans lesquels les clients sont autorisés à utiliser ce mode de livraison. Options : <br/>**`All Allowed Countries`**- Clients de tous les [pays](../../getting-started/store-details.md#country-options) spécifié dans votre configuration de magasin peut utiliser ce mode de livraison.<br/>**`Specific Countries`** - Après avoir choisi cette option, la variable [!UICONTROL Ship to Specific Countries] s’affiche. Sélectionnez chaque pays de la liste dans lequel ce mode de livraison peut être utilisé. |
| [!UICONTROL Show Method if Not Applicable] | Site Web | Détermine si UPS apparaît toujours comme option d’expédition lors du passage en caisse. Options : <br/>**`Yes`**- UPS apparaît toujours comme option d’expédition lors du passage en caisse, même s’il n’est pas applicable à la commande.<br/>**`No`** - UPS apparaît comme option d’expédition lors du passage en caisse uniquement si applicable à la commande. (Par exemple, si le poids de la commande dépasse le poids maximal.) |
| [!UICONTROL Debug] | Site Web | Indique si les transmissions de données entre votre magasin et UPS sont enregistrées dans le système pour le débogage. À moins qu’un problème doive être suivi et consigné, cette option doit être définie sur `No`. |
| [!UICONTROL Sort Order] | Site Web | Numéro qui détermine l’ordre dans lequel UPS apparaît lorsqu’il est répertorié avec d’autres méthodes de diffusion lors du passage en caisse. Entrée `0` en haut de la liste. |

{style="table-layout:auto"}

### [!UICONTROL USPS]

{{beta2-updates}}

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| Activé pour le passage en caisse | Site Web | Détermine si USPS est disponible pour les clients comme méthode d’expédition lors du passage en caisse. Options : `Yes` / `No` |
| _[!UICONTROL USPS Account Settings]_ |  |  |
| [!UICONTROL Gateway URL] | Site Web | URL utilisée pour se connecter au système USPS afin de récupérer dynamiquement les tarifs d’expédition. |
| [!UICONTROL Secure Gateway URL] | Site Web | URL sécurisée utilisée pour se connecter au système USPS via une couche de socket sécurisée (SSL) afin de récupérer dynamiquement les tarifs d’expédition. |
| [!UICONTROL Title] | Affichage en magasin | Titre de cette option d’expédition telle qu’elle apparaît dans le passage en caisse du panier. |
| [!UICONTROL User ID] | Site Web | Identifiant d’utilisateur de compte du chargeur USPS. |
| [!UICONTROL Password] | Site Web | Votre mot de passe du compte du chargeur USPS. |
| [!UICONTROL Mode] | Site Web | Détermine le mode de transmission des données envoyées au système USPS. Les options incluent : <br/>**`Development`**- USPS ne vérifie pas que les données reçues du serveur Commerce sont envoyées via SSL.<br/>**`Live`** - USPS vérifie que les données reçues du serveur Commerce sont envoyées via une couche de socket sécurisée (SSL). |

{style="table-layout:auto"}

![Paramètres de package USPS](./assets/delivery-methods-usps-packaging.png)<!-- zoom -->

<!-- [USPS Packaging Settings](https://docs.magento.com/user-guide/shipping/usps.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL USPS packaging Settings]_ |  |  |
| [!UICONTROL Packages Request Type] | Site Web | Détermine le mode de calcul du poids des envois comportant plusieurs packages. Options : `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Container] | Site Web | Définit le type de conteneur utilisé pour empaqueter les envois de commande. Options : `Variable` / `Flat Rate Box` / `Flat Rate Envelope` / `Rectangular` / Non rectangulaire |
| [!UICONTROL Size] | Site Web | Définit l’option Taille sur la taille du package d’expédition type. Cette option a une incidence sur le calcul du taux de livraison. Options : `Regular` / `Large` / `Oversize` |
| [!UICONTROL Machinable] | Site Web | Indique si le package peut être traité par l’ordinateur. Cette option a une incidence sur le calcul du taux de livraison. |
| [!UICONTROL Maximum Package Weight] | Site Web | Définit le poids maximal qu’un package peut être spécifié par USPS. Si les produits commandés dépassent le poids maximal du package, cette option d&#39;expédition n&#39;est pas disponible. |

{style="table-layout:auto"}

![Paramètres des frais de gestion USPS](./assets/delivery-methods-usps-handling-fee.png)<!-- zoom -->

<!-- [USPS Handling Fee Settings](https://docs.magento.com/user-guide/shipping/usps.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL USPS Handling Fee settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | Site Web | Définit la méthode de calcul des frais de gestion pour les frais d’expédition à taux variable. Options : <br/>**`Fixed`**- Les frais de traitement sont un taux fixe.<br/>**`Percent`** - Les frais de gestion sont appliqués en pourcentage du montant de la commande. |
| [!UICONTROL Handling Applied] | Site Web | Indique si les frais de traitement sont appliqués à chaque commande ou à chaque module dans une commande. |
| [!UICONTROL Handling Fee] | Site Web | Définit la gestion incluse dans le prix de livraison. Les frais de gestion peuvent être définis sous la forme d’un montant fixe ou d’un pourcentage. <br/><br/>**_Remarque :_**Lorsque vous saisissez un pourcentage, utilisez le format décimal `0.25` pour 25 %. |

{style="table-layout:auto"}

![Méthodes USPS autorisées](./assets/delivery-methods-usps-allowed-methods.png)<!-- zoom -->

<!-- [USPS Allowed Methods](https://docs.magento.com/user-guide/shipping/usps.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL USPS Allowed Methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Site Web | Spécifie les méthodes d’expédition USPS autorisées proposées aux clients. Les taux d’expédition sont calculés en fonction du mode de livraison sélectionné. |
| [!UICONTROL Free Method] | Site Web | Définit la méthode d’expédition gratuite via USPS ou peut être désactivée en sélectionnant `None`. <br/><br/>**_Remarque :_**Cette méthode d’expédition est similaire à la méthode d’expédition gratuite de votre magasin, mais elle est répertoriée comme une option d’expédition USPS et identifiée comme expédition USPS. |
| [!UICONTROL Minimum Order Amount for Free Shipping] | Site Web | Définit le montant minimum de commande qui doit être respecté pour être admissible à la livraison gratuite. |
| [!UICONTROL Displayed Error Message] | Affichage en magasin | Message d’erreur qui s’affiche lorsque USPS n’est pas disponible pour une raison quelconque. |

{style="table-layout:auto"}

![USPS Applicable Countries](./assets/delivery-methods-usps-countries.png)<!-- zoom -->

<!-- [USPS Applicable Countries](https://docs.magento.com/user-guide/shipping/usps.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL USPS Applicable Countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Site Web | Indique les pays dans lesquels les commandes peuvent être expédiées. Options : <br/>**`All Allowed Countries`**- Clients de tous les [pays](../../getting-started/store-details.md#country-options) spécifié dans votre configuration de magasin peut utiliser ce mode de livraison.<br/>**`Specific Countries`** - Après avoir choisi cette option, la variable [!UICONTROL Ship to Specific Countries] s’affiche. Sélectionnez chaque pays de la liste dans lequel ce mode de livraison peut être utilisé. |
| [!UICONTROL Show Method if Not Applicable] | Site Web | Contrôle l’affichage de l’expédition USPS lors du passage en caisse. Options : <br/>**`Yes`**- USPS apparaît toujours comme option d’expédition lors du passage en caisse, même s’il n’est pas applicable à la commande.<br/>**`No`** - USPS apparaît comme option d’expédition lors du passage en caisse uniquement si applicable à la commande (c’est-à-dire que le poids de la commande dépasse la quantité maximale). |
| [!UICONTROL Debug] | Site Web | Détermine si un journal des transmissions de données entre votre magasin et USPS est conservé par le système pour le débogage. À moins qu’un problème doive être suivi et consigné, cette option doit être définie sur `No`. |
| [!UICONTROL Sort Order] | Site Web | Un nombre qui détermine l’ordre dans lequel USPS apparaît lorsqu’il est répertorié avec d’autres méthodes de diffusion lors du passage en caisse. Entrée `0` en haut de la liste. |

{style="table-layout:auto"}

### [!UICONTROL FedEx]

{{beta2-updates}}

![Paramètres du compte FedEx](./assets/delivery-methods-fedex-account-settings.png)<!-- zoom -->

<!-- [FedEx Account Settings](https://docs.magento.com/user-guide/shipping/fedex.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL FedEx Account Settings]_ |  |  |
| [!UICONTROL Enabled for Checkout] | Site Web | Détermine si FedEx est disponible pour les clients comme méthode d’expédition lors du passage en caisse. Options : `Yes` / `No` |
| [!UICONTROL Title] | Affichage en magasin | Titre de cette option d’expédition telle qu’elle apparaît dans le passage en caisse du panier. |
| [!UICONTROL Account ID] | Site Web | Votre identifiant de compte FedEx. |
| [!UICONTROL Meter Number] | Site Web | Votre numéro de compteur FedEx. |
| [!UICONTROL Key] | Site Web | Votre clé de compte FedEx. |
| [!UICONTROL Password] | Site Web | Mot de passe de votre compte FedEx. |
| [!UICONTROL Sandbox Mode] | Site Web | Pour exécuter des transactions FedEx dans un environnement de test, définissez le mode Sandbox sur `Yes`. Options : `Yes` / `No`. |
| [!UICONTROL Web-Services URL] | Site Web | L’URL requise dépend du paramètre Mode sandbox . Options : <br/>**`Production`**- L’URL d’accès aux services Web FedEx lorsque le magasin est actif.<br/>**`Sandbox`** - URL d’accès à l’environnement de test pour les services web FedEx. |

{style="table-layout:auto"}

![Packages FedEx](./assets/delivery-methods-fedex-packaging.png)<!-- zoom -->

<!-- [FedEx Packaging](https://docs.magento.com/user-guide/shipping/fedex.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL FedEx Packaging Settings]_ |  |  |
| [!UICONTROL Packages Request Type] | Site Web | Détermine le mode de calcul du poids des envois comportant plusieurs packages. Options : `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Packaging] | Site Web | Dans la liste, sélectionnez le type de conteneur que vous utilisez généralement pour regrouper les produits commandés dans votre magasin. |
| [!UICONTROL Dropoff] | Site Web | Dans la liste, sélectionnez la méthode de sélection : <br/>**`Regular Pickup`**- (Par défaut) Si vous avez un volume élevé d’envois, il peut être rentable d’organiser des prises régulières.<br/>**`Request Courier`** - Vous devez appeler et demander un courrier FedEx pour ramasser les envois. <br/>**`Drop Box`**- Vous devez déposer vos envois dans votre boîte de dépôt FedEx locale.<br/>**`Business Service Center`** - Vous devez déposer vos envois à votre centre de service commercial FedEx local. <br/>**`Station`**- Vous devez déposer vos envois dans votre station FedEx locale. |
| [!UICONTROL Maximum Package Weight] | Site Web | La valeur par défaut de FedEx est de 150 livres. Consultez votre opérateur de transport pour obtenir le poids maximal pris en charge. Il est recommandé d’utiliser la valeur par défaut, sauf si vous avez des arrangements spéciaux avec FedEx. |

{style="table-layout:auto"}

![Frais de gestion FedEx](./assets/delivery-methods-fedex-handling-fee.png)<!-- zoom -->

<!-- [FedEx Handling Fee](https://docs.magento.com/user-guide/shipping/fedex.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL FedEx Handling Fee Settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | Site Web | Détermine la méthode utilisée pour calculer les frais de traitement. Options : `Fixed Fee` / `Percentage` <br/><br/>**_Remarque :_**Les frais de gestion sont facultatifs et apparaissent comme des frais supplémentaires qui s’ajoutent aux frais de livraison FedEx. |
| [!UICONTROL Handling Applied] | Site Web | Détermine le mode d’application des frais de traitement. Options : `Per Order` / `Per Package` |
| [!UICONTROL Handling Fee] | Site Web | Indique le montant imputé en tant que frais de traitement, en fonction de la méthode de calcul du montant. Si le coût est calculé sur la base d’un coût fixe, entrez le montant sous forme de décimale, par exemple `4.90`. Si les frais de traitement sont basés sur un pourcentage de la commande, saisissez le montant en pourcentage. Par exemple, pour facturer 6 % de la commande, saisissez la valeur `.06`. |

{style="table-layout:auto"}

![Méthodes de remise FedEx](./assets/delivery-methods-fedex-delivery-methods.png)<!-- zoom -->

<!-- [FedEx Delivery Methods](https://docs.magento.com/user-guide/shipping/fedex.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL FedEx delivery methods]_ |  |  |
| [!UICONTROL Residential Delivery] | Site Web | Définissez cette variable sur l’une des valeurs suivantes, selon que vous vendez Entreprise à Consommateur (B2C) ou Entreprise à Entreprise (B2B) : <br/>**`Yes`**- Pour les diffusions B2C<br/>**`No`** - Pour les diffusions B2B |
| [!UICONTROL Allowed Methods] | Site Web | Dans la liste, sélectionnez les méthodes d’expédition que vous prenez en charge. Les méthodes dépendent de votre compte FedEx, de la fréquence et de la taille de vos envois, et si vous autorisez les envois internationaux. En tant que commerçant, vous pouvez décider de ne proposer que la navigation terrestre. |
| [!UICONTROL Hub ID] | Site Web | Identifiant fourni par FedEx utilisé avec la variable [!DNL Smart Post] . |
| [!UICONTROL Free Method] | Site Web | Dans la liste, sélectionnez le mode de livraison que vous préférez utiliser pour les offres d’expédition gratuite. <br/><br/>**_Remarque :_**Cette méthode de livraison est similaire à la méthode de livraison gratuite habituelle, mais elle est répertoriée dans les options de livraison FedEx et est identifiée comme expédition FedEx. |
| [!UICONTROL Free Shipping Amount Threshold] | Site Web | Détermine si un montant minimum de commande est requis pour la livraison gratuite. Options : <br/>**`Enable`**- Permet la livraison gratuite de FedEx pour les commandes qui correspondent au montant minimum.<br/>**`Disable`** - Désactive la livraison gratuite de FedEx avec la commande minimale. |
| [!UICONTROL Free Shipping Amount Threshold] | Site Web | Indique le montant minimum de commande requis pour la livraison gratuite. |
| [!UICONTROL Displayed Error Message] | Affichage en magasin | Le message qui s’affiche lorsque FedEx n’est pas disponible pour une raison quelconque. Vous pouvez utiliser le message par défaut ou en saisir un autre. |

{style="table-layout:auto"}

![Pays applicables FedEx](./assets/delivery-methods-fedex-applicable-countries.png)<!-- zoom -->

<!-- [FedEx Applicable Countries](https://docs.magento.com/user-guide/shipping/fedex.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL FedEx Applicable Countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Site Web | Indique les pays où vos clients peuvent envoyer par FedEx. Options : <br/>**`All Allowed Countries`**- Clients de tous les [pays](../../getting-started/store-details.md#country-options) spécifié dans votre configuration de magasin peut utiliser ce mode de livraison.<br/>**`Specific Countries`** - Après avoir choisi cette option, la variable [!UICONTROL Ship to Specific Countries] s’affiche. Sélectionnez chaque pays de la liste dans lequel ce mode de livraison peut être utilisé. |
| [!UICONTROL Ship to Specific Countries] | Site Web | Indique les pays spécifiques où vos clients peuvent envoyer par FedEx. |
| [!UICONTROL Debug] | Site Web | Détermine si un journal des transmissions de données entre votre magasin et FedEx est géré par le système pour le débogage. À moins qu’un problème doive être suivi et consigné, cette option doit être définie sur `No`. |
| [!UICONTROL Show Method if Not Applicable] | Site Web | Détermine le moment où FedEx apparaît comme méthode de livraison lors du passage en caisse. Options : <br/>**`Yes`**- L’option de livraison FedEx s’affiche dans la liste des méthodes de livraison, que la commande soit admissible ou non.<br/>**`No`** - L&#39;option de livraison FedEx n&#39;apparaît pas dans la liste des méthodes de livraison si elle n&#39;est pas applicable à la commande (par exemple, si le poids de la commande dépasse le poids maximum). |
| [!UICONTROL Sort Order] | Site Web | Numéro qui détermine la commande que FedEx apparaît lorsqu’il est répertorié avec d’autres méthodes de livraison lors du passage en caisse. Entrée `0` en haut de la liste. |

{style="table-layout:auto"}

### [!UICONTROL DHL]

![Paramètres du compte DHL](./assets/delivery-methods-dhl-account-settings.png)<!-- zoom -->

<!-- [DHL Account Settings](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL DHL Account Settings]_ |  |  |
| [!UICONTROL Enabled for Checkout] | Site Web | Détermine si DHL est disponible pour les clients comme méthode d’expédition lors du passage en caisse. Options : `Yes` / `No` |
| [!UICONTROL Title] | Affichage en magasin | Le titre de cette méthode d’expédition tel qu’il apparaît lors du passage en caisse. |
| [!UICONTROL Gateway URL] | Site Web | En règle générale, vous pouvez accepter l’URL de passerelle par défaut. Cependant, si DHL vous a donné une autre URL, saisissez la valeur dans ce champ. |
| [!UICONTROL Access ID] | Site Web | Identifiant d’accès au compte de l’expéditeur DHL. |
| [!UICONTROL Password] | Site Web | Votre mot de passe du compte de l’expéditeur DHL. |
| [!UICONTROL Account Number] | Site Web | Votre numéro de compte de l&#39;expéditeur de la DHL. |

{style="table-layout:auto"}

![Paramètres du module DHL](./assets/delivery-methods-dhl-package-settings.png)<!-- zoom -->

<!-- [DHL Package Settings](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL DHL Package Settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | Site Web | Les frais de gestion sont facultatifs et s’affichent sous la forme d’un supplément ajouté aux frais d’expédition de DHL. Dans la liste, sélectionnez la méthode à utiliser pour calculer les frais de traitement. Options : Flux fixe / Pourcentage. |
| [!UICONTROL Handling Applied] | Site Web | Dans la liste, sélectionnez le mode d’application des frais de traitement. Options : `Per Order` / `Per Package` |
| Gestion des frais | Site Web | Indiquez le montant qui sera imputé sur les frais de traitement, selon la méthode que vous avez choisie pour calculer le montant. Si, par exemple, les frais sont calculés à partir d’une somme fixe, saisissez la valeur décimale, par exemple `4.90`. Toutefois, si les frais de traitement sont basés sur un pourcentage de la commande, saisissez le montant en pourcentage. Par exemple, si vous facturez 6 % de la commande, saisissez la valeur `.06`. |
| [!UICONTROL Divide Order Weight] | Affichage en magasin | Détermine si le poids d’une commande de plus de 70 kg peut être divisé en unités plus petites afin d’assurer des frais de livraison précis. Options : `Yes` / `No` |
| [!UICONTROL Weight Unit] | Affichage en magasin | Détermine l’unité de mesure du poids utilisé dans les calculs d’expédition. Options : `Pounds` / `Kilograms` |
| [!UICONTROL Size] | Affichage en magasin | Détermine la taille du module. Options : <br/>**`Regular`**- Les packages livrés sont conformes aux méthodes de conditionnement standard DHL. Dans le [!UICONTROL Allowed Methods] sélectionnez chaque méthode d’emballage utilisée pour expédier les produits de votre magasin.<br/>**`Specific`** - Si les packages livrés ont des dimensions personnalisées, procédez comme suit : [!UICONTROL Height (cm)] / [!UICONTROL Depth (cm)] / [!UICONTROL Width (cm)] |

{style="table-layout:auto"}

![Méthodes autorisées DHL](./assets/delivery-methods-dhl-allowed-methods.png)<!-- zoom -->

<!-- DHL Allowed Methods](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL DHL allowed methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Site Web | Dans la liste, sélectionnez chaque méthode d’expédition que vous prenez en charge. |
| [!UICONTROL Ready Time] | Site Web | Indique le moment où le module sera prêt pour le sélecteur, en heures, après l’envoi d’une commande. |
| [!UICONTROL Displayed Error Message] | Affichage en magasin | Ce message s’affiche lorsque DHL devient indisponible pour une raison quelconque. Vous pouvez utiliser le message par défaut ou saisir votre propre message. |
| [!UICONTROL Free Method] |  | Cette méthode d’expédition est similaire à la méthode d’expédition gratuite classique. Cependant, elle est répertoriée dans les options d’expédition DHL et est identifiée comme expédition DHL. Dans la liste, sélectionnez le mode de livraison que vous préférez utiliser pour les offres d’expédition gratuite. |
| [!UICONTROL Free Shipping with Minimum Order Amount] | Site Web | Définissez sur l’une des options suivantes : <br/>**`Enable`**- Pour autoriser la livraison gratuite de DHL pour les commandes qui correspondent au montant minimum.<br/>**`Disable`** - Ne pas proposer l&#39;expédition gratuite DHL avec une commande minimale. |
| [!UICONTROL Minimum Order Amount for Free Shipping] | Site Web | Si vous activez [!UICONTROL Free Shipping with Minimum Order], saisissez la valeur minimum du montant de la commande dans le champ . |

{style="table-layout:auto"}

![Pays applicables DHL](./assets/delivery-methods-dhl-applicable-countries.png)<!-- zoom -->

<!-- [DHL Applicable Countries](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL DHL applicable countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Site Web | Indique les pays dans lesquels les clients sont autorisés à utiliser ce mode de livraison. Options : <br/>**Tous les pays autorisés** - Tous les pays autorisés sont applicables pour utiliser la méthode de livraison gratuite. Les pays autorisés sont spécifiés dans la variable [!UICONTROL General] page de configuration. <br/>**Pays spécifiques** - Limite cette option d’expédition aux pays spécifiés dans la liste Ship to Specific Countries. |
| [!UICONTROL Ship to Specific Countries] | Site Web | Indique les pays où les envois DHL peuvent être envoyés. Cette liste de pays sélectionnée est utilisée si `Specific Countries` est sélectionné dans la variable [!UICONTROL Ship to Applicable Countries] . |
| [!UICONTROL Show Method if Not Applicable] | Site Web | Détermine à quel moment DHL apparaît comme méthode d’expédition lors du passage en caisse. Options : <br/>**`Yes`**- DHL apparaît toujours comme option d’expédition lors du passage en caisse, même si elle n’est pas applicable à la commande.<br/>**`No`** - DHL apparaît comme option d’expédition lors du passage en caisse uniquement si applicable à la commande (c’est-à-dire que le poids de la commande dépasse la quantité maximale). |
| [!UICONTROL Debug] | Site Web | Crée un fichier journal contenant des informations d’erreur. |
| [!UICONTROL Sort Order] | Site Web | Numéro qui détermine l’ordre dans lequel la DHL apparaît lorsqu’elle est répertoriée avec d’autres méthodes de diffusion lors de l’extraction. Pour le placer en haut de la liste, saisissez `0`. |

{style="table-layout:auto"}
