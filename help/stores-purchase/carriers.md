---
title: Paramétrage du transporteur
description: Découvrez la prise en charge des comptes d’expédition commerciale disponibles pour votre boutique.
exl-id: b6098068-12f3-4223-b216-98055a802b19
feature: Shipping/Delivery
source-git-commit: 15118877bb8cc533b2323819db34da0513899e25
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Paramétrage du transporteur

Si vous disposez d&#39;un compte commercial auprès d&#39;un opérateur pris en charge, vous pouvez offrir à vos clients la commodité de choisir cet opérateur lors du passage en caisse. Les taux sont automatiquement téléchargés, de sorte que vous n&#39;avez pas besoin de rechercher les informations.

>[!NOTE]
>
>Consultez [Commerce Marketplace](../getting-started/commerce-marketplace.md) pour obtenir des services de livraison supplémentaires pour votre installation de Commerce.

Avant de pouvoir proposer à vos clients une sélection de transporteurs, vous devez effectuer les étapes suivantes :

- Configurez le [paramètres d’expédition](shipping-settings.md) pour établir le point d’origine de votre boutique.

- Configurez les paramètres de chaque service d&#39;opérateur que vous souhaitez proposer.

   - [**UPS**](ups.md) - United Parcel Service (UPS) offre des services d&#39;expédition nationaux et internationaux par voie terrestre et aérienne à plus de 220 pays.
   - [**USPS**](usps.md) - Le service postal des États-Unis (USPS) est le service postal indépendant du gouvernement des États-Unis. USPS offre des services de transport maritime nationaux et internationaux par voie terrestre et aérienne.
   - [**FedEx**](fedex.md) - FedEx offre des services d&#39;expédition nationaux et internationaux par voie terrestre et aérienne à plus de 220 pays.
   - [**DHL**](dhl.md) - DHL offre des services internationaux intégrés et des solutions personnalisées et axées sur les clients pour la gestion et le transport des lettres, des marchandises et des informations.

## Poids dimensionnel

Le poids dimensionnel, parfois appelé poids volumétrique, est une pratique courante de l&#39;industrie qui fonde le prix de transport sur une combinaison de poids et de volume d&#39;emballage. En termes simples, le poids dimensionnel détermine le tarif d&#39;expédition en fonction de l&#39;espace occupé par un colis dans la zone de chargement du transporteur. Le poids dimensionnel est généralement utilisé lorsqu&#39;un emballage est relativement léger par rapport à son volume.

Tous les grands transporteurs appliquent un poids dimensionnel à certaines expéditions. Cependant, la manière dont la tarification du poids dimensionnel est appliquée varie d&#39;un transporteur à l&#39;autre. Si votre entreprise a un volume d&#39;expéditions élevé, même une légère différence dans le prix d&#39;expédition peut se traduire par des milliers de dollars au cours d&#39;une année.

## Configuration

Les options de configuration varient pour chaque opérateur. Cependant, toutes nécessitent les étapes suivantes :

1. Ouvrez un compte de livraison auprès du transporteur.

1. Saisissez votre numéro de compte ou votre ID utilisateur, ainsi que l’URL de la passerelle vers leur système dans la configuration de votre boutique.

### Obsolescence de l’API des outils Web USPS

Les versions 2.4.6, 2.4.7 et 2.4.8 d’Adobe Commerce utilisent les API des outils web hérités pour une intégration d’expédition prête à l’emploi avec USPS. USPS a introduit les API USPS, une plateforme REST pour remplacer les API des outils web hérités.

Le 25 janvier 2026, USPS mettra hors service les API des outils web hérités. Passée cette date, toutes les requêtes envoyées aux API des outils web échoueront.

Pour éviter toute interruption des services d&#39;expédition USPS, prenez les mesures suivantes avant le 25 janvier 2026 :

- Appliquez le correctif de qualité [&#x200B; Migration de l’API REST USPS &#x200B;](https://experienceleague.adobe.com/en/docs/commerce-operations/tools/quality-patches-tool/patches-available-in-qpt/v1-1-70/ac-15210) pour ajouter la prise en charge de l’intégration aux API REST USPS.

- Mettez à jour la configuration USPS de Commerce pour utiliser les API REST :

   - [Configuration du transporteur USPS](usps.md)

   - [Configuration des étiquettes d&#39;expédition](shipping-label-create.md)

