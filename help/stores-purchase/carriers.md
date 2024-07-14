---
title: Configuration des opérateurs de livraison
description: Découvrez la prise en charge des comptes d’expédition commerciale disponibles pour votre boutique.
exl-id: b6098068-12f3-4223-b216-98055a802b19
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---

# Configuration des opérateurs de livraison

Si vous disposez d’un compte commercial avec un opérateur pris en charge, vous pouvez offrir à vos clients la facilité de choisir cet opérateur lors du passage en caisse. Les taux sont automatiquement téléchargés. Il n’est donc pas nécessaire de rechercher les informations.

>[!NOTE]
>
>Voir [Commerce Marketplace](../getting-started/commerce-marketplace.md) pour obtenir des services de livraison supplémentaires pour votre installation Commerce.

Avant de pouvoir offrir à vos clients une sélection de compagnies de transport, vous devez effectuer les étapes suivantes :

- Configurez les [ paramètres d’expédition](shipping-settings.md) pour établir le point d’origine de votre boutique.

- Configurez les paramètres de chaque service de l&#39;opérateur que vous souhaitez proposer.

   - [**UPS**](ups.md) - United Parcel Service (UPS) offre des services de navigation intérieure et internationale par voie terrestre et aérienne à plus de 220 pays.
   - [**USPS**](usps.md) - Le United States Postal Service (USPS) est le service postal indépendant du gouvernement des États-Unis. USPS offre des services de navigation intérieure et internationale par voie terrestre et aérienne.
   - [**FedEx**](fedex.md) - FedEx offre des services de navigation intérieure et internationale par voie terrestre et aérienne à plus de 220 pays.
   - [**DHL**](dhl.md) - DHL offre des services internationaux intégrés et des solutions personnalisées et axées sur le client pour la gestion et le transport de lettres, de marchandises et d’informations.

## Poids dimensionnel

Le poids dimensionnel, parfois appelé poids volumétrique, est une pratique courante dans l&#39;industrie qui fonde le prix du transport sur une combinaison de poids et de volume du paquet. En termes simples, le poids dimensionnel détermine le taux d&#39;expédition en fonction de l&#39;espace occupé par un colis dans la zone de cargaison du transporteur. Le poids dimensionnel est généralement utilisé lorsqu’un paquet est relativement léger par rapport à son volume.

Tous les principaux opérateurs appliquent un poids dimensionnel à certaines cargaisons. Cependant, la manière dont le prix du poids dimensionnel est appliqué varie d&#39;un opérateur à l&#39;autre. Si votre société dispose d’un volume élevé d’envois, même une légère différence de prix d’expédition peut se traduire par des milliers de dollars au cours d’une année.

## Configuration

Les options de configuration varient pour chaque opérateur. Toutefois, les étapes suivantes sont nécessaires :

1. Ouvrez un compte d’expédition avec l’opérateur.

1. Entrez votre numéro de compte ou votre identifiant utilisateur, ainsi que l’URL de la passerelle vers leur système dans la configuration de votre magasin.
