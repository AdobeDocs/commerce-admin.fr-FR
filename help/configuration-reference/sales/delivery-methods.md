---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Delivery Methods]'
description: Examinez les paramètres de configuration sur le [!UICONTROL Sales] &gt; [!UICONTROL Delivery Methods] de l’Administration de Commerce.
exl-id: 159b76a8-3676-4692-9cd6-18947bda4666
feature: Configuration, Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '3773'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Delivery Methods]

{{config}}

## [!UICONTROL Basic Delivery Methods]

### [!UICONTROL Flat Rate]

![Taux forfaitaire](./assets/delivery-methods-flat-rate.png)<!-- zoom -->

<!-- [Flat Rate](https://docs.magento.com/user-guide/shipping/shipping-flat-rate.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site internet | Lorsqu’il est activé, le taux forfaitaire apparaît comme une option dans le _Estimer les frais d&#39;expédition et les taxes_ dans le panier, et dans _Expédition_ lors du passage en caisse. Options : `Yes` / `No` |
| [!UICONTROL Title] | Affichage de la boutique | Nom utilisé pour ce mode d’expédition lors du passage en caisse. |
| [!UICONTROL Method Name] | Affichage de la boutique | Nom qui décrit la méthode de calcul utilisée pour produire une estimation d’expédition. Le nom de la méthode s’affiche en regard du taux estimé calculé dans le panier. La valeur par défaut est `Fixed`. |
| [!UICONTROL Type] | Site internet | Décrit le type de calcul utilisé pour déterminer le taux forfaitaire. Options : <br/>**`None`**- Aucun calcul n’est utilisé. Définit le taux forfaitaire sur zéro, ce qui équivaut à la livraison gratuite.<br/>**`Per Order`** - Facture un seul forfait pour la commande entière. <br/>**`Per Item`**- Facture un taux forfaitaire distinct pour chaque article du panier. Le taux est multiplié par le nombre d’articles du panier, même si la quantité totale comprend une combinaison de différents articles. |
| [!UICONTROL Price] | Site internet | Prix facturé au client pour les frais d&#39;expédition forfaitaires. |
| [!UICONTROL Calculate Handling Fee] | Site internet | Détermine le mode de calcul des frais de gestion, le cas échéant. Options : `Fixed` / `Percent` |
| [!UICONTROL Handling Fee] | Site internet | Saisissez le montant à facturer pour les frais de manutention, en fonction de la méthode que vous avez choisie pour calculer le montant. Par exemple, si les frais sont basés sur des frais fixes, saisissez le montant sous forme de décimale, par exemple 4,90. Toutefois, si les frais de traitement sont basés sur un pourcentage de la commande, saisissez le montant sous forme de pourcentage. Par exemple, si vous facturez 6 % de la commande, saisissez la valeur suivante : `.06`. |
| [!UICONTROL Displayed Error Message] | Affichage de la boutique | Message qui s’affiche si un client ou une cliente choisit le taux forfaitaire, mais que la méthode n’est pas disponible pour une raison quelconque. |
| [!UICONTROL Ship to Applicable Countries] | Site internet | Indique les pays où vous proposez une livraison à taux forfaitaire. Options : <br/>**`All Allowed Countries`**- Les clients de n’importe quel pays spécifié dans la configuration de la boutique peuvent utiliser la livraison à taux forfaitaire.<br/>**`Specific Countries`** - Les clients de pays spécifiques uniquement peuvent utiliser la livraison à taux forfaitaire. |
| [!UICONTROL Ship to Specific Countries] | Site internet | Indique chaque pays où les clients peuvent utiliser la livraison à taux forfaitaire. |
| [!UICONTROL Show Method if Not Applicable] | Site internet | Détermine si le taux forfaitaire apparaît comme une option lors du passage en caisse si la méthode ne s&#39;applique pas à l&#39;achat. Options : `Yes` / `No` |
| [!UICONTROL Sort Order] | Site internet | Nombre qui détermine l’ordre dans lequel le taux forfaitaire apparaît lorsqu’il est répertorié avec d’autres méthodes de diffusion lors du passage en caisse. |

{style="table-layout:auto"}

### [!UICONTROL Free Shipping]

![Livraison gratuite](./assets/delivery-methods-free-shipping.png)<!-- zoom -->

<!-- [Free Shipping](https://docs.magento.com/user-guide/shipping/shipping-free.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site internet | Lorsqu’elle est activée, la livraison gratuite apparaît comme une option dans la section Expédition lors du passage en caisse. Options : `Yes` / `No` |
| [!UICONTROL Title] | Affichage de la boutique | Nom utilisé pour ce mode d’expédition lors du passage en caisse. |
| Nom de la méthode | Affichage de la boutique | Nom qui décrit la méthode de calcul utilisée pour produire une estimation d’expédition. Le nom de la méthode s’affiche en regard du taux estimé calculé dans le panier. La valeur par défaut est `Free`. |
| Montant minimal de la commande | Site internet | Achat minimum requis pour appliquer la livraison gratuite à une commande. |
| Inclure la taxe au montant | Site internet | Détermine si la taxe est incluse dans le calcul du montant minimum de la commande. Options : <br/>**Oui** - La taxe est incluse dans le calcul du montant minimum de la commande (Sous-total + Taxe - Remise).<br/>**Non** - La taxe n&#39;est pas incluse dans le calcul du montant minimum de la commande (Sous-total - Remise). |
| Message d’erreur affiché | Affichage de la boutique | Message qui s’affiche si un client choisit la livraison gratuite, mais que la méthode n’est pas disponible pour une raison quelconque. |
| Expédier vers les pays applicables | Site internet | Indique les pays où vous proposez la livraison gratuite. Options : <br/>**Tous les pays autorisés** - Les clients de n&#39;importe quel pays spécifié dans la configuration de la boutique peuvent utiliser la livraison gratuite. <br/>**Pays spécifiques** - Les clients provenant de pays spécifiques peuvent utiliser la livraison gratuite. |
| Expédition vers des pays spécifiques | Site internet | Indique chaque pays où les clients peuvent utiliser la livraison gratuite. |
| Afficher la méthode si non applicable | Site internet | Détermine si l&#39;option Expédition gratuite apparaît lors du passage en caisse si la méthode ne s&#39;applique pas à l&#39;achat. Options : `Yes` / `No` |
| [!UICONTROL Sort Order] | Site internet | Nombre qui détermine la commande pour laquelle l&#39;expédition gratuite apparaît lorsqu&#39;elle est mise en vente avec d&#39;autres méthodes de livraison lors du passage en caisse. |

{style="table-layout:auto"}

### [!UICONTROL Table Rates]

![Taux de table](./assets/delivery-methods-table-rates.png)<!-- zoom -->

<!-- [Table Rates](https://docs.magento.com/user-guide/shipping/shipping-table-rate.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site internet | Lorsqu’elle est activée, la table des taux s’affiche sous forme d’option dans la section Estimer l’expédition et les taxes du panier, ainsi que dans la section Expédition lors du passage en caisse. Options : `Yes` / `No` |
| [!UICONTROL Title] | Affichage de la boutique | Nom utilisé pour ce mode d’expédition lors du passage en caisse. |
| Nom de la méthode | Affichage de la boutique | Nom qui décrit la méthode de calcul utilisée pour produire une estimation d’expédition. Le nom de la méthode s’affiche en regard du taux estimé calculé dans le panier. La valeur par défaut est `Table Rate`. |
| [!UICONTROL Condition] | Site internet | Détermine la condition sur laquelle est basé le calcul. Le format du fichier CSV chargé est spécifique à chaque condition. Options : `Weight vs. Destination` / `Price vs. Destination` / `# of Items vs. Destination` |
| [!UICONTROL Include Virtual Products in Price Calculation] | Site internet | Détermine si les produits virtuels, qui ne nécessitent pas d&#39;expédition, sont inclus dans les calculs de prix du tableau. |
| [!UICONTROL Calculate Handling Fee] | Site internet | Détermine le mode de calcul des frais de gestion, le cas échéant. Options : `Fixed` / `Percent` |
| [!UICONTROL Handling Fee] | Site internet | Montant des frais qui s’ajoutent aux frais d’expédition pour couvrir les frais de manutention de l’expédition. Saisissez la valeur sous la forme d’une décimale. Par exemple, si la taxe est basée sur un pourcentage, entrez 0,06 au lieu de 6 %. Pour un montant fixe, saisissez `6.00`. |
| [!UICONTROL Displayed Error Message] | Affichage de la boutique | Message qui s’affiche si un client ou une cliente choisit Taux de table, mais que la méthode n’est pas disponible pour une raison quelconque. |
| [!UICONTROL Ship to Applicable Countries] | Site internet | Indique les pays où vous proposez l&#39;expédition à tarif fixe. Options : <br/>**`All Allowed Countries`**- Les clients de n&#39;importe quel pays spécifié dans la configuration du magasin peuvent utiliser l&#39;expédition à tarif fixe.<br/>**`Specific Countries`** - Les clients provenant de pays spécifiques peuvent utiliser l&#39;expédition à tarif fixe. |
| [!UICONTROL Ship to Specific Countries] | Site internet | Indique chaque pays où les clients peuvent utiliser l&#39;expédition à tarif fixe. |
| [!UICONTROL Show Method if Not Applicable] | Site internet | Détermine si les taux de la table s&#39;affichent en tant qu&#39;option lors du passage en caisse si la méthode ne s&#39;applique pas à l&#39;achat. Options : `Yes` / `No` |
| [!UICONTROL Sort Order] | Site internet | Nombre qui détermine l’ordre dans lequel les taux du tableau s’affichent lorsqu’ils sont répertoriés avec d’autres méthodes de diffusion lors du passage en caisse. |

{style="table-layout:auto"}

### [!UICONTROL In-Store Delivery]

![Diffusion En Magasin](./assets/delivery-methods-in-store-delivery.png)<!-- zoom -->

<!-- [In-Store Delivery](https://docs.magento.com/user-guide/shipping/shipping-in-store-delivery.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled] | Site internet | Lorsqu’elle est activée, la diffusion en magasin peut apparaître comme une option dans le _Estimer les frais d&#39;expédition et les taxes_ dans le panier, et dans _Expédition_ lors du passage en caisse. Options : `Yes` / `No` |
| [!UICONTROL Method Name] | Affichage de la boutique | Nom qui identifie la fonction de retrait en magasin comme méthode d’expédition. Cette valeur est affichée sous la forme du libellé d&#39;un onglet en haut de la page Passage en caisse et dans le tableau des modes d&#39;expédition disponibles au bas de la même page. La valeur par défaut est `In-store Delivery`. |
| [!UICONTROL Title] | Affichage de la boutique | Nom utilisé pour ce mode d’expédition lors du passage en caisse. |
| [!UICONTROL Price] | Site internet | Prix que vous facturez au client pour une cueillette en magasin. |
| [!UICONTROL Search Radius] | Site internet | Rayon, en km, à utiliser lors de la recherche d&#39;emplacements de retrait. |
| [!UICONTROL Displayed Error Message] | Affichage de la boutique | Message qui s’affiche lorsqu’un client sélectionne la cueillette en magasin, mais que la méthode de diffusion n’est pas disponible. |

{style="table-layout:auto"}

## [!UICONTROL Carriers]

### [!UICONTROL UPS]

{{ups-api}}

![Paramètres du compte REST UPS](./assets/delivery-methods-ups1.png)<!-- zoom -->

![Paramètres du compte XML UPS](./assets/delivery-methods-ups1.png)<!-- zoom -->

<!-- [UPS REST Account Settings](https://docs.magento.com/user-guide/shipping/ups.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Enabled for Checkout] | Site internet | Détermine si l&#39;onduleur est disponible pour les clients comme méthode d&#39;expédition lors du passage en caisse. Options : `Yes` / `No` |
| [!UICONTROL Enabled for RMA] | Site internet | Détermine si UPS est disponible pour les clients en tant que méthode d&#39;expédition pour une autorisation de retour client. Options : `Yes` / `No` |
| _[!UICONTROL UPS Account Settings]_ |  |  |
| [!UICONTROL Live Account] | Affichage de la boutique | Spécifie que le compte United Parcel Service est actif. Options : `Yes` / `No` |
| [!UICONTROL Title] | Affichage de la boutique | Nom utilisé pour ce mode d’expédition lors du passage en caisse. |
| _[!UICONTROL UPS REST Account Settings]_ |  |  |
| [!UICONTROL Gateway URL] | Site internet | Pour le service REST UPS, affiche les URL suivantes requises pour transmettre des données JSON : URL de passerelle, URL de tracking, URL d’expédition |
| [!UICONTROL Mode] | Site internet | Détermine le mode de transmission utilisé pour les données envoyées au système UPS. Options : <br/>**`Development`**- UPS ne vérifie pas que les données reçues du serveur Commerce sont envoyées via SSL.<br/>**`Live`** - UPS vérifie que les données reçues du serveur Commerce sont envoyées via une couche de socket sécurisée (SSL). |
| ID d’utilisateur | Site internet | Identifiant client de votre compte d&#39;expéditeur UPS. |
| [!UICONTROL Origin of the Shipment] | Site internet | (UPS REST uniquement) Pays ou région d’origine de l’expédition du produit. |
| [!UICONTROL Password] | Affichage de la boutique | Votre secret client du compte expéditeur UPS. |

{style="table-layout:auto"}

![Informations sur le package UPS](./assets/delivery-methods-ups-packaging-settings.png)<!-- zoom -->

<!-- [UPS Package Information](https://docs.magento.com/user-guide/shipping/ups.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL UPS Negotiated Rate Settings]_ |  |  |
| [!UICONTROL Enable Negotiated Rates] | Site internet | (UPS REST uniquement) Active/désactive des tarifs spéciaux, conformément à votre accord avec UPS. Options : `Yes` / `No` |
| [!UICONTROL Packages Request Type] | Site internet | Détermine la manière dont le poids est calculé pour les expéditions comportant plusieurs colis. Options : `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Shipper Number] | Site internet | (UPS REST uniquement) Le numéro d&#39;expéditeur UPS de six caractères est requis pour faire référence à l&#39;utilisation de taux négociés. |
| [!UICONTROL Container] | Site internet | Définit le type de conteneur utilisé pour emballer les expéditions. Options : `Customer Packaging` / `UPS Letter Envelope` / `Customer Packaging` / `UPS Letter Envelope` / `UPS Tube` / `UPS Express Box` / `UPS Worldwide 25 kilo` / `UPS Worldwide 10 kilo` |
| [!UICONTROL Weight Unit] | Site internet | Définit l’unité de mesure par défaut pour le poids du produit dans votre magasin. Voir [Poids dimensionnel](../../stores-purchase/carriers.md#dimensional-weight) pour plus d’informations. |
| [!UICONTROL Tracking URL] | Site internet | (UPS REST uniquement) URL UPS utilisée pour effectuer le suivi des packages. |
| [!UICONTROL Destination Type] | Site internet | Définit le type de destination d&#39;expédition par défaut. Options : `Business` / `Residential` |
| [!UICONTROL Maximum Package Weight] | Site internet | Définit le poids maximum qu&#39;un package peut atteindre, tel que spécifié par UPS. Si les produits commandés dépassent le poids maximum du colis, cette option d&#39;expédition n&#39;est pas disponible. Selon [UPS.com](https://www.ups.com/us/en/global.page), les colis ne doivent pas dépasser 150 lb (70 kg) Vérifiez auprès de votre transporteur le poids maximal. |
| [!UICONTROL Pickup Method] | Site internet | Définit la méthode de prélèvement de l&#39;onduleur. Options : `Regular Daily Pickup` / `On Call Air` / `One Time Pickup` / `Letter Center` / `Customer Counter` |
| [!UICONTROL Minimum Package Weight] | Site internet | Définit le poids minimum qu&#39;un package peut avoir comme spécifié par UPS. Si le poids des produits commandés est inférieur au poids minimum du colis, cette option d&#39;expédition n&#39;est pas disponible. Pour vérifier le poids minimum, vérifiez auprès de votre transporteur. |
| [!UICONTROL Calculate Handling Fee] | Site internet | Définit la méthode de calcul des frais de manutention pour l&#39;expédition au tarif du tableau. Options : <br>**`Fixed`**- Les frais de manutention sont un taux fixe.<br>**`Percent`** - Les frais de gestion sont appliqués en pourcentage du montant de la commande. |
| [!UICONTROL Handling Applied] | Site internet | Indique si des frais de gestion sont appliqués à chaque commande ou à chaque package d&#39;une commande. |
| [!UICONTROL Handling Fee] | Site internet | Définit la gestion incluse dans le prix de livraison. Les frais de manutention peuvent être fixés sous la forme d’un montant fixe ou d’un pourcentage. <br/><br/>**_Remarque :_**Si vous tapez un montant en pourcentage, utilisez le format décimal `0.25` pour 25 %. |

{style="table-layout:auto"}

![Méthodes autorisées UPS](./assets/delivery-methods-ups-allowed-methods.png)<!-- zoom -->

<!-- [UPS Allowed Methods](https://docs.magento.com/user-guide/shipping/ups.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL UPS allowed methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Site internet | Spécifie les méthodes autorisées d&#39;expédition UPS proposées aux clients. Les frais d&#39;expédition sont calculés en fonction du mode d&#39;expédition sélectionné. |
| [!UICONTROL Free Method] | Site internet | Indique la méthode utilisée pour la livraison gratuite via UPS. Pour désactiver la livraison gratuite, choisissez « Aucun ». <br/><br/>**_Remarque :_**Cette méthode est similaire à la méthode de base [Livraison gratuite](../../stores-purchase/shipping-free.md), cependant, il apparaît comme une option d’expédition UPS lors du passage en caisse. |
| [!UICONTROL Free Shipping Amount Threshold] | Site internet | Détermine si la livraison gratuite est appliquée lorsque le montant de la commande atteint le seuil de livraison gratuite. Options : `Enable` / `Disable` |
| [!UICONTROL Free Shipping Amount Threshold] | Site internet | Définit le montant total minimum qu’une commande doit atteindre pour pouvoir bénéficier de la livraison gratuite. |
| [!UICONTROL Displayed Error Message] | Affichage de la boutique | Message d’erreur affiché lorsque ce mode d’expédition n’est pas disponible, quelle qu’en soit la raison. |

{style="table-layout:auto"}

![Pays et autres paramètres applicables à l&#39;UPS](./assets/delivery-methods-ups-ship-to.png)<!-- zoom -->

<!-- [UPS Applicable Countries and Other Settings](https://docs.magento.com/user-guide/shipping/ups.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL UPS Applicable countries and other Settings]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Site internet | Spécifie le pays dans lequel les clients sont autorisés à utiliser ce mode d&#39;expédition. Options : <br/>**`All Allowed Countries`**- Clients de tous les [pays](../../getting-started/store-details.md#country-options) spécifié dans la configuration de votre boutique peut utiliser cette méthode d’expédition.<br/>**`Specific Countries`** - Après avoir choisi cette option, le [!UICONTROL Ship to Specific Countries] La liste s’affiche. Sélectionnez dans la liste chaque pays où ce mode d&#39;expédition peut être utilisé. |
| [!UICONTROL Show Method if Not Applicable] | Site internet | Détermine si UPS apparaît toujours comme option d&#39;expédition lors du passage en caisse. Options : <br/>**`Yes`**- UPS apparaît toujours comme option d&#39;expédition lors du passage en caisse, même s&#39;il ne s&#39;applique pas à la commande.<br/>**`No`** - UPS apparaît comme option d&#39;expédition lors du passage en caisse uniquement si applicable à la commande. (Par exemple, si le poids de la commande dépasse le poids maximal.) |
| [!UICONTROL Debug] | Site internet | Indique si les transmissions de données entre votre magasin et l’onduleur sont consignées dans le système à des fins de débogage. À moins qu’il n’existe un problème qui doit être suivi et consigné, cette option doit être définie sur `No`. |
| [!UICONTROL Sort Order] | Site internet | Nombre qui détermine l&#39;ordre dans lequel UPS apparaît lorsqu&#39;il est répertorié avec d&#39;autres méthodes de diffusion lors du passage en caisse. Enter `0` en haut de la liste. |

{style="table-layout:auto"}

### [!UICONTROL USPS]

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| Activé pour le passage en caisse | Site internet | Détermine si USPS est disponible pour les clients en tant que méthode d&#39;expédition lors du passage en caisse. Options : `Yes` / `No` |
| _[!UICONTROL USPS Account Settings]_ |  |  |
| [!UICONTROL Gateway URL] | Site internet | URL utilisée pour se connecter au système USPS afin de récupérer dynamiquement les frais d’expédition. |
| [!UICONTROL Secure Gateway URL] | Site internet | URL sécurisée utilisée pour se connecter au système USPS via une couche de socket sécurisée (SSL) afin de récupérer de manière dynamique les tarifs d’expédition. |
| [!UICONTROL Title] | Affichage de la boutique | Titre de cette option d’expédition tel qu’il apparaît dans le passage en caisse du panier. |
| [!UICONTROL User ID] | Site internet | Identifiant utilisateur de votre compte d&#39;expéditeur USPS. |
| [!UICONTROL Password] | Site internet | Votre mot de passe de compte d&#39;expéditeur USPS. |
| [!UICONTROL Mode] | Site internet | Détermine le mode de transmission utilisé pour les données envoyées au système USPS. Les options incluent : <br/>**`Development`**- USPS ne vérifie pas que les données reçues du serveur Commerce sont envoyées via SSL.<br/>**`Live`** - USPS vérifie que les données reçues du serveur Commerce sont envoyées via une couche de socket sécurisée (SSL). |

{style="table-layout:auto"}

![Paramètres d&#39;emballage USPS](./assets/delivery-methods-usps-packaging.png)<!-- zoom -->

<!-- [USPS Packaging Settings](https://docs.magento.com/user-guide/shipping/usps.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL USPS packaging Settings]_ |  |  |
| [!UICONTROL Packages Request Type] | Site internet | Détermine la manière dont le poids est calculé pour les expéditions comportant plusieurs colis. Options : `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Container] | Site internet | Définit le type de conteneur utilisé pour emballer les expéditions. Options : `Variable` / `Flat Rate Box` / `Flat Rate Envelope` / `Rectangular` / Non rectangulaire |
| [!UICONTROL Size] | Site internet | Définit l’option Taille sur la taille standard du package d’expédition. Cette option affecte le calcul des frais d&#39;expédition. Options : `Regular` / `Large` / `Oversize` |
| [!UICONTROL Machinable] | Site internet | Indique si le package peut être traité par la machine. Cette option affecte le calcul des frais d&#39;expédition. |
| [!UICONTROL Maximum Package Weight] | Site internet | Définit le poids maximum qu&#39;un package peut avoir comme spécifié par USPS. Si les produits commandés dépassent le poids maximum du colis, cette option d&#39;expédition n&#39;est pas disponible. |

{style="table-layout:auto"}

![Paramètres des frais de gestion USPS](./assets/delivery-methods-usps-handling-fee.png)<!-- zoom -->

<!-- [USPS Handling Fee Settings](https://docs.magento.com/user-guide/shipping/usps.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL USPS Handling Fee settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | Site internet | Définit la méthode de calcul des frais de manutention pour l&#39;expédition au tarif du tableau. Options : <br/>**`Fixed`**- Les frais de manutention sont un taux fixe.<br/>**`Percent`** - Les frais de gestion sont appliqués en pourcentage du montant de la commande. |
| [!UICONTROL Handling Applied] | Site internet | Indique si des frais de gestion sont appliqués à chaque commande ou à chaque package d&#39;une commande. |
| [!UICONTROL Handling Fee] | Site internet | Définit la gestion incluse dans le prix de livraison. Les frais de manutention peuvent être fixés sous la forme d’un montant fixe ou d’un pourcentage. <br/><br/>**_Remarque :_**Lors de la saisie d’un montant en pourcentage, utilisez le format décimal `0.25` pour 25 %. |

{style="table-layout:auto"}

![Méthodes autorisées USPS](./assets/delivery-methods-usps-allowed-methods.png)<!-- zoom -->

<!-- [USPS Allowed Methods](https://docs.magento.com/user-guide/shipping/usps.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL USPS Allowed Methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Site internet | Spécifie les méthodes autorisées d&#39;expédition USPS proposées aux clients. Les frais d&#39;expédition sont calculés en fonction du mode d&#39;expédition sélectionné. |
| [!UICONTROL Free Method] | Site internet | Définit la méthode d&#39;expédition gratuite via USPS ou peut être désactivée en sélectionnant `None`. <br/><br/>**_Remarque :_**Cette méthode d&#39;expédition est similaire à la méthode d&#39;expédition gratuite de votre magasin, mais elle est répertoriée comme une option d&#39;expédition USPS et identifiée comme expédition USPS. |
| [!UICONTROL Minimum Order Amount for Free Shipping] | Site internet | Définit le montant de commande minimal qui doit être atteint pour bénéficier de la livraison gratuite. |
| [!UICONTROL Displayed Error Message] | Affichage de la boutique | Message d&#39;erreur qui s&#39;affiche lorsque USPS n&#39;est pas disponible pour une raison quelconque. |

{style="table-layout:auto"}

![Pays applicables à l&#39;USPS](./assets/delivery-methods-usps-countries.png)<!-- zoom -->

<!-- [USPS Applicable Countries](https://docs.magento.com/user-guide/shipping/usps.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL USPS Applicable Countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Site internet | Spécifie les pays où les commandes peuvent être expédiées. Options : <br/>**`All Allowed Countries`**- Clients de tous les [pays](../../getting-started/store-details.md#country-options) spécifié dans la configuration de votre boutique peut utiliser cette méthode d’expédition.<br/>**`Specific Countries`** - Après avoir choisi cette option, le [!UICONTROL Ship to Specific Countries] La liste s’affiche. Sélectionnez dans la liste chaque pays où ce mode d&#39;expédition peut être utilisé. |
| [!UICONTROL Show Method if Not Applicable] | Site internet | Contrôle l&#39;affichage de l&#39;expédition USPS pendant le passage en caisse. Options : <br/>**`Yes`**- USPS apparaît toujours comme option d&#39;expédition lors du passage en caisse, même s&#39;il ne s&#39;applique pas à la commande.<br/>**`No`** - USPS apparaît comme option d&#39;expédition lors du passage en caisse uniquement s&#39;il s&#39;applique à la commande (c&#39;est-à-dire que le poids de la commande dépasse le poids maximum). |
| [!UICONTROL Debug] | Site internet | Détermine si un journal des transmissions de données entre votre magasin et USPS est conservé par le système à des fins de débogage. À moins qu’il n’existe un problème qui doit être suivi et consigné, cette option doit être définie sur `No`. |
| [!UICONTROL Sort Order] | Site internet | Nombre qui détermine l&#39;ordre dans lequel l&#39;USPS apparaît lorsqu&#39;il est répertorié avec d&#39;autres méthodes de diffusion lors du passage en caisse. Enter `0` en haut de la liste. |

{style="table-layout:auto"}

### [!UICONTROL FedEx]

<!-- [FedEx Account Settings](https://docs.magento.com/user-guide/shipping/fedex.html) -->

#### Paramètres du compte FedEx

![Paramètres du compte FedEx](./assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|-------|------ |-----------------------------------------------------------------------------|
| [!UICONTROL Enabled for Checkout] | Site internet | Détermine si FedEx est disponible pour les clients en tant que méthode d&#39;expédition lors du passage en caisse. Options : `Yes` / `No` |
| [!UICONTROL Title] | Affichage de la boutique | Titre de cette option d’expédition tel qu’il apparaît dans le passage en caisse du panier. |
| [!UICONTROL Account ID] | Site internet | Identifiant de votre compte FedEx. |
| [!UICONTROL Api Key] | Site internet | Votre clé API de compte FedEx. |
| [!UICONTROL Secret Key] | Site internet | Votre clé secrète API de compte FedEx. |
| [!UICONTROL Sandbox Mode] | Site internet | Pour exécuter des transactions FedEx dans un environnement de test, définissez le mode Sandbox sur . `Yes`. Options : `Yes` / `No`. |
| [!UICONTROL Web-Services URL] | Site internet | L’URL requise dépend du paramètre Mode Sandbox . Options : <br/>**`Production`**- URL d&#39;accès aux services web FedEx lorsque le magasin est en ligne.<br/>**`Sandbox`** - URL d’accès à l’environnement de test pour les services web FedEx. |

{style="table-layout:auto"}

#### Paramètres des packages FedEx

![Emballage FedEx](./assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Pickup Type] | Site internet | Dans la liste, sélectionnez la méthode de retrait : <br/>**`DropOff at Fedex Location`**- (Par défaut) Indique que vous déposez les envois à votre station FedEx locale.<br/>**`Contact Fedex to Schedule`** - Indique que vous avez contacté FedEx pour demander un retrait. <br/>**`Use Scheduled Pickup`**- Indique que l&#39;expédition est récupérée dans le cadre d&#39;un ramassage régulier programmé.<br/>**`On Call`** - Indique que le retrait est programmé en appelant FedEx. <br/>**`Package Return Program`**- Indique que l&#39;expédition est récupérée par le Programme de retours de colis FedEx Ground.<br/>**`Regular Stop`** - Indique que l&#39;expédition est récupérée selon le calendrier de récupération standard. <br/>**`Tag`**- Indique que le retrait de l&#39;expédition est spécifique à une demande de retrait d&#39;étiquette express ou d&#39;étiquette d&#39;appel au sol. Ceci s&#39;applique uniquement pour une étiquette d&#39;expédition retour. |
| [!UICONTROL Packages Request Type] | Site internet | Détermine la manière dont le poids est calculé pour les expéditions comportant plusieurs colis. Options : `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Packaging] | Site internet | Dans la liste, sélectionnez le type de conteneur que vous utilisez généralement pour emballer les produits commandés dans votre magasin. |
| [!UICONTROL Weight Unit] | Site internet | Unité utilisée pour le poids du package. Options : `Pounds` (par défaut) / `Kilograms` |
| [!UICONTROL Maximum Package Weight] | Site internet | La valeur par défaut pour FedEx est de 150 livres. Consultez votre transporteur pour connaître le poids maximum pris en charge. L&#39;utilisation de la valeur par défaut est recommandée, sauf si vous avez des arrangements spéciaux avec FedEx. |

{style="table-layout:auto"}

#### Paramètres des frais de gestion FedEx

![Frais de gestion FedEx](./assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Calculate Handling Fee] | Site internet | Détermine la méthode utilisée pour calculer les frais de manutention. Options : `Fixed Fee` / `Percentage` <br/><br/>**_Remarque :_**Les frais de manutention sont facultatifs et apparaissent comme des frais supplémentaires qui s&#39;ajoutent aux frais d&#39;expédition FedEx. |
| [!UICONTROL Handling Applied] | Site internet | Détermine la manière dont les frais de gestion sont appliqués. Options : `Per Order` / `Per Package` |
| [!UICONTROL Handling Fee] | Site internet | Spécifie le montant facturé en tant que frais de manutention, en fonction de la méthode utilisée pour calculer le montant. Si les frais sont basés sur des frais fixes, saisissez le montant sous forme de décimale, par exemple `4.90`. Si les frais de traitement sont basés sur un pourcentage de la commande, saisissez le montant en pourcentage. Par exemple, pour facturer 6 % de la commande, saisissez la valeur : `.06`. |

{style="table-layout:auto"}

#### Méthodes de diffusion FedEx

![Méthodes de diffusion FedEx](./assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Residential Delivery] | Site internet | Choisissez l’une des options suivantes, selon que vous vendez de l’entreprise au consommateur (B2C) ou de l’entreprise à l’entreprise (B2B) : <br/>**`Yes`**- Pour les diffusions B2C<br/>**`No`** - Pour les diffusions B2B |
| [!UICONTROL Allowed Methods] | Site internet | Dans la liste, sélectionnez les modes d’expédition que vous prenez en charge. Les méthodes dépendent de votre compte FedEx, de la fréquence et de la taille de vos envois, et si vous autorisez les envois internationaux. En tant que marchand, vous pourriez décider de n&#39;offrir que le transport terrestre. |
| [!UICONTROL Hub ID] | Site internet | Identifiant fourni par FedEx et utilisé avec le [!DNL Smart Post] méthode. |
| [!UICONTROL Free Method] | Site internet | Dans la liste, sélectionnez la méthode d&#39;expédition que vous préférez utiliser pour les offres d&#39;expédition gratuite. <br/><br/>**_Remarque :_**Cette méthode d&#39;expédition est similaire à la méthode d&#39;expédition gratuite habituelle, mais elle est répertoriée dans les options d&#39;expédition FedEx et est identifiée comme expédition FedEx. |
| [!UICONTROL Free Shipping Amount Threshold] | Site internet | Détermine si un montant de commande minimum est requis pour une livraison gratuite. Options : <br/>**`Enable`**- Permet l&#39;expédition gratuite de FedEx pour les commandes qui respectent le montant minimum.<br/>**`Disable`** - Désactive la livraison gratuite FedEx avec commande minimum. |
| [!UICONTROL Free Shipping Amount Threshold] | Site internet | Spécifie le montant de commande minimum requis pour une livraison gratuite. |
| [!UICONTROL Displayed Error Message] | Affichage de la boutique | Message qui apparaît lorsque FedEx n&#39;est pas disponible pour une raison quelconque. Vous pouvez utiliser le message par défaut ou en saisir un autre. |

{style="table-layout:auto"}

#### Paramètres par pays applicables à FedEx

![Pays applicables à FedEx](./assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| [!UICONTROL Ship to Applicable Countries] | Site internet | Indique les pays où vos clients peuvent expédier par FedEx. Options : <br/>**`All Allowed Countries`**- Clients de tous les [pays](../../getting-started/store-details.md#country-options) spécifié dans la configuration de votre boutique peut utiliser cette méthode d’expédition.<br/>**`Specific Countries`** - Après avoir choisi cette option, le [!UICONTROL Ship to Specific Countries] La liste s’affiche. Sélectionnez dans la liste chaque pays où ce mode d&#39;expédition peut être utilisé. |
| [!UICONTROL Ship to Specific Countries] | Site internet | Indique les pays spécifiques où vos clients peuvent expédier par FedEx. |
| [!UICONTROL Debug] | Site internet | Détermine si un journal des transmissions de données entre votre magasin et FedEx est conservé par le système à des fins de débogage. À moins qu’il n’existe un problème qui doit être suivi et consigné, cette option doit être définie sur `No`. |
| [!UICONTROL Show Method if Not Applicable] | Site internet | Détermine quand FedEx apparaît comme méthode d&#39;expédition lors du passage en caisse. Options : <br/>**`Yes`**- L&#39;option d&#39;expédition FedEx est affichée dans la liste des modes de livraison, que la commande soit admissible ou non.<br/>**`No`** - L&#39;option d&#39;expédition FedEx ne s&#39;affiche pas dans la liste des modes de livraison si elle ne s&#39;applique pas à la commande (par exemple, si le poids de la commande dépasse le poids maximum). |
| [!UICONTROL Sort Order] | Site internet | Nombre qui détermine l&#39;ordre dans lequel FedEx apparaît lorsqu&#39;il est répertorié avec d&#39;autres méthodes de livraison lors du passage en caisse. Enter `0` en haut de la liste. |

{style="table-layout:auto"}

### [!UICONTROL DHL]

![Paramètres du compte DHL](./assets/delivery-methods-dhl-account-settings.png)<!-- zoom -->

<!-- [DHL Account Settings](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL DHL Account Settings]_ |  |  |
| [!UICONTROL Enabled for Checkout] | Site internet | Détermine si DHL est disponible pour les clients en tant que méthode de livraison lors du passage en caisse. Options : `Yes` / `No` |
| [!UICONTROL Title] | Affichage de la boutique | Titre de ce mode d’expédition tel qu’il apparaît lors du passage en caisse. |
| [!UICONTROL Gateway URL] | Site internet | En règle générale, vous pouvez accepter l’URL de passerelle par défaut. Cependant, si DHL vous a fourni une autre URL, saisissez la valeur dans ce champ. |
| [!UICONTROL Access ID] | Site internet | Identifiant d&#39;accès à votre compte d&#39;expéditeur DHL. |
| [!UICONTROL Password] | Site internet | Votre mot de passe de compte d&#39;expéditeur DHL. |
| [!UICONTROL Account Number] | Site internet | Votre numéro de compte expéditeur DHL. |

{style="table-layout:auto"}

![Paramètres du package DHL](./assets/delivery-methods-dhl-package-settings.png)<!-- zoom -->

<!-- [DHL Package Settings](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL DHL Package Settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | Site internet | Les frais de manutention sont facultatifs et apparaissent comme des frais supplémentaires ajoutés aux frais d&#39;expédition DHL. Dans la liste, sélectionnez la méthode à utiliser pour calculer les frais de manutention. Options : Frais fixes / Pourcentage. |
| [!UICONTROL Handling Applied] | Site internet | Dans la liste, sélectionnez la manière dont vous souhaitez que les frais de gestion soient appliqués. Options : `Per Order` / `Per Package` |
| Frais de gestion | Site internet | Saisissez le montant à facturer pour les frais de manutention, en fonction de la méthode que vous avez choisie pour calculer le montant. Par exemple, si les frais sont basés sur des frais fixes, saisissez le montant sous forme de décimale, par exemple `4.90`. Toutefois, si les frais de traitement sont basés sur un pourcentage de la commande, saisissez le montant sous forme de pourcentage. Par exemple, si vous facturez 6 % de la commande, saisissez la valeur suivante : `.06`. |
| [!UICONTROL Divide Order Weight] | Affichage de la boutique | Détermine si le poids d&#39;une commande de plus de 70 kg peut être divisé en unités plus petites pour garantir des frais d&#39;expédition précis. Options : `Yes` / `No` |
| [!UICONTROL Weight Unit] | Affichage de la boutique | Détermine l&#39;unité de mesure du poids utilisée dans les calculs d&#39;expédition. Options : `Pounds` / `Kilograms` |
| [!UICONTROL Size] | Affichage de la boutique | Détermine la taille du package. Options : <br/>**`Regular`**- Les colis expédiés sont conformes aux méthodes d&#39;emballage standard de DHL. Dans le [!UICONTROL Allowed Methods] Sélectionnez chaque méthode d&#39;emballage utilisée pour expédier les produits de votre magasin.<br/>**`Specific`** - Si les colis expédiés ont des dimensions personnalisées, effectuez les opérations suivantes : [!UICONTROL Height (cm)] / [!UICONTROL Depth (cm)] / [!UICONTROL Width (cm)] |

{style="table-layout:auto"}

![Méthodes autorisées DHL](./assets/delivery-methods-dhl-allowed-methods.png)<!-- zoom -->

<!-- DHL Allowed Methods](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL DHL allowed methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Site internet | Dans la liste, sélectionnez chaque mode d&#39;expédition pris en charge. |
| [!UICONTROL Ready Time] | Site internet | Indique le moment où le colis sera prêt pour le retrait (en heures) après la soumission d&#39;une commande. |
| [!UICONTROL Displayed Error Message] | Affichage de la boutique | Ce message s’affiche lorsque DHL n’est plus disponible, quelle qu’en soit la raison. Vous pouvez utiliser le message par défaut ou saisir un message personnalisé. |
| [!UICONTROL Free Method] |  | Cette méthode d&#39;expédition est similaire à la méthode d&#39;expédition gratuite habituelle, mais elle est répertoriée dans les options d&#39;expédition DHL et est identifiée comme expédition DHL. Dans la liste, sélectionnez la méthode d&#39;expédition que vous préférez utiliser pour les offres d&#39;expédition gratuite. |
| [!UICONTROL Free Shipping with Minimum Order Amount] | Site internet | Définissez-le sur l’une des valeurs suivantes : <br/>**`Enable`**- Permettre la livraison gratuite de DHL pour les commandes qui respectent le montant minimum.<br/>**`Disable`** - De ne pas offrir la livraison gratuite DHL avec la commande minimum. |
| [!UICONTROL Minimum Order Amount for Free Shipping] | Site internet | Si vous activez [!UICONTROL Free Shipping with Minimum Order], saisissez la valeur minimale du montant de la commande dans le champ. |

{style="table-layout:auto"}

![Pays DHL applicables](./assets/delivery-methods-dhl-applicable-countries.png)<!-- zoom -->

<!-- [DHL Applicable Countries](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| Champ | [Portée](../../getting-started/websites-stores-views.md#scope-settings) | Description |
|--- |--- |--- |
| _[!UICONTROL DHL applicable countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Site internet | Spécifie le pays dans lequel les clients sont autorisés à utiliser ce mode d&#39;expédition. Options : <br/>**Tous les pays autorisés** - Tous les pays autorisés sont applicables à l&#39;utilisation de la méthode d&#39;expédition gratuite. Les pays autorisés sont spécifiés dans le [!UICONTROL General] page de configuration. <br/>**Pays spécifiques** - Limite cette option d&#39;expédition aux pays spécifiés dans la liste Expédier vers des pays spécifiques. |
| [!UICONTROL Ship to Specific Countries] | Site internet | Spécifie les pays où les expéditions DHL peuvent être envoyées. Cette liste de pays sélectionnés est utilisée si `Specific Countries` est sélectionné dans [!UICONTROL Ship to Applicable Countries] option. |
| [!UICONTROL Show Method if Not Applicable] | Site internet | Détermine quand DHL apparaît comme méthode d&#39;expédition lors du passage en caisse. Options : <br/>**`Yes`**- DHL apparaît toujours comme option d&#39;expédition lors du passage en caisse, même si cela ne s&#39;applique pas à la commande.<br/>**`No`** - DHL apparaît comme option d&#39;expédition lors du passage en caisse seulement si applicable à la commande (c&#39;est-à-dire, le poids de la commande dépasse le poids maximum). |
| [!UICONTROL Debug] | Site internet | Crée un fichier journal contenant les informations d’erreur. |
| [!UICONTROL Sort Order] | Site internet | Nombre qui détermine l’ordre dans lequel DHL apparaît lorsqu’il est répertorié avec d’autres méthodes de diffusion lors du passage en caisse. Pour le placer en haut de la liste, saisissez `0`. |

{style="table-layout:auto"}
